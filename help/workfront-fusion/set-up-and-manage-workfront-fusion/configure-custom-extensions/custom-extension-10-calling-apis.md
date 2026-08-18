---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Aufrufen von Workfront- und Fusion-APIs aus Ihrer Erweiterung
description: Aufrufen von Workfront- und Fusion-APIs aus Ihrer Erweiterung
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1083
ht-degree: 0%

---


# Aufrufen von Workfront- und Fusion-APIs aus Ihrer Erweiterung

>[!NOTE]
>
>Dieser Artikel setzt eine gewisse Vertrautheit mit Software-Entwicklungs-Tools voraus.

Die Fusion-Kontextreferenz gibt Ihnen das IMS-Token des angemeldeten Benutzers. Ein natürlicher nächster Schritt besteht daher darin, Workfront- oder Fusion-APIs aufzurufen und echte Daten anzuzeigen. Dies ist aufgrund von CORS nicht möglich. In diesem Artikel wird gezeigt, wie Sie diese Einschränkung mithilfe einer App Builder-Laufzeitaktion als Server-seitigem Proxy umgehen können. Außerdem wird ein Beispiel dafür gegeben (das Ereignisabonnement-Dashboard).

## Warum ein direkter Browser-Aufruf fehlschlägt (CORS)

Ihre sichtbare Benutzeroberfläche wird in einem `<iframe>` ausgeführt, der vom CDN von Adobe bereitgestellt wird (`https://<your-app>.adobeio-static.net`). Wenn diese Seite `fetch(...)` einer Workfront- oder Fusion-API mit einer **Herkunft**, erzwingt der Browser Cross-Origin Resource Sharing (CORS). Sofern die API nicht explizit `Access-Control-Allow-Origin` für Ihre CDN-Herkunft zurückgibt, blockiert der Browser die Antwort. Diese APIs ermöglichen keine Zulassungsliste beliebiger Erweiterungsursprünge, sodass direkte Aufrufe des Gasts fehlschlagen.

Informationen zu CORS finden Sie unter [CORS](https://developer.mozilla.org/docs/Web/HTTP/CORS).

## Aufrufen einer eigenen Laufzeitaktion ohne CORS

Die Lösung dafür ist, Ihre eigene Laufzeitaktion ohne CORS aufzurufen.

App Builder-Apps können Laufzeitaktionen enthalten. Hierbei handelt es sich um kleine Server-lose Funktionen, die Server-seitig auf Adobe I/O Runtime ausgeführt werden. Server-zu-Server-Aufrufe unterliegen keinem Browser-CORS. Und da die Aktion Teil Ihrer App ist, kann der Gast sie mit einer relativen URL aufrufen, die dieselbe Herkunft hat und daher nicht blockiert wird.

```
  Guest UI (browser, adobeio-static.net)
     │  fetch('/api/v1/web/<app>/wf-proxy?...')   ← relative = same-origin, no CORS
     ▼
  Your runtime action  (Adobe I/O Runtime, server-side)
     │  fetch('https://fusion.adobe.com/api/v3/...')  ← server-to-server, no CORS
     ▼
  Workfront / Fusion API
```

Die Aktion empfängt das IMS-Token des Benutzers vom Gast und leitet es Upstream weiter, sodass weiterhin Aufrufe im Namen des Benutzers mit seinen Berechtigungen durchgeführt werden.

## Schritt 1: Aktion deklarieren

Laufzeitaktionen werden in `app.config.yaml` unter der `runtimeManifest` der Erweiterung deklariert. Fügen Sie eine `wf-proxy` Aktion neben Ihrer Erweiterung hinzu:

```yaml
extensions:
  fusion/nav-organization/1:
    $include: src/fusion-nav-organization-1/ext.config.yaml
    runtimeManifest:
      packages:
        fusion-uix-guest:                # ← your package name; part of the action URL
          license: Apache-2.0
          actions:
            wf-proxy:
              function: src/fusion-nav-organization-1/actions/wf-proxy/index.js
              web: 'yes'                  # exposes it at /api/v1/web/<package>/wf-proxy
              runtime: nodejs:22
              inputs:
                LOG_LEVEL: debug
              annotations:
                require-adobe-auth: false # see note below
                final: true
```

Die Aktion ist erreichbar unter:

```
/api/v1/web/<package>/<action>     e.g.  /api/v1/web/fusion-uix-guest/wf-proxy
```

### `require-adobe-auth`: true vs. false

Diese Anmerkung steuert, ob das Gateway von Adobe ein IMS-Token validiert, bevor Ihre Aktion ausgeführt wird.

* **`true`:** Der sichere Standard.  Nicht authentifizierte Aufrufe werden vom Gateway zurückgewiesen. Der Validator ist jedoch strikt darauf festgelegt, welche Kopfzeilen er erwartet, und kann Anfragen ablehnen oder benutzerdefinierte Kopfzeilen löschen, die für den Upstream-Aufruf erforderlich sind. In diesem Fall wird sie als `401` angezeigt, obwohl Ihr Token gültig ist.
* **`false`:** Überspringt die Gateway-Prüfung. Ihre Aktion ist dann öffentlich aufrufbar, sodass Sie **müssen** die Autorisierung selbst durchsetzen. Fordern Sie einen `Authorization` Bearer in der Aktion an und lehnen Sie ihn ab, wenn er fehlt, und leiten Sie ihn dann an den Upstream weiter, wo Workfront und Fusion ihn validieren. In Kombination mit einer strikten Zielgruppenanpassung, die in Schritt 2 beschrieben wird, ist dies der verlässliche Pfad für einen Proxy, der benutzerdefinierte Header übergeben muss.

>[!TIP]
>
> Erst `true`. Wenn Sie eine `401` sehen, die Sie nicht erklären können, weil das Token gültig ist und an anderer Stelle funktioniert, wechseln Sie zu `false` **und** Sie die Bearer-Prüfung und -Zulassungsliste in Ihrer Aktion, damit die Sicherheit weiter oben erzwungen wird.

## Schritt 2: Aktion für einen auf die Zulassungsliste gesetzt Proxy schreiben

`src/fusion-nav-organization-1/actions/wf-proxy/index.js` erstellen. Zwei Regeln sorgen dafür, dass dies sicher ist: eine Zulassungsliste von Upstream-Zielen, sodass die Aktion nicht als offenes Relais verwendet werden kann, und ein erforderliches Bearer-Token, das Upstream weitergeleitet wird.

```js
const fetch = require('node-fetch')
const { Core } = require('@adobe/aio-sdk')
const { errorResponse, getBearerToken, checkMissingRequestInputs } = require('../utils')

// Page-through query params (see "Paginate list results" below).
const pageQuery = (p) => {
  const q = new URLSearchParams()
  if (p.start != null) q.set('start', p.start)
  if (p.limit != null) q.set('limit', p.limit)
  return q
}

// Only these upstreams may be reached. Never build the URL from arbitrary input.
const TARGETS = {
  subscriptions: {
    method: 'GET',
    url: () => 'https://<your-wf-host>/attask/eventsubscription/api/v1/subscriptions',
  },
  hooks: {
    method: 'GET',
    // Fusion hooks are team-scoped: teamId is a REQUIRED query param (see below).
    url: (p) => {
      const q = pageQuery(p)
      if (p.teamId) q.set('teamId', p.teamId)
      return `https://fusion.adobe.com/api/v3/hooks?${q.toString()}`
    },
  },
  scenarios: {
    method: 'GET',
    url: (p) => {
      const q = pageQuery(p)
      if (p.fusionOrgId) q.set('organizationId', p.fusionOrgId)
      return `https://fusion.adobe.com/api/v3/scenarios?${q.toString()}`
    },
  },
}

async function main (params) {
  const logger = Core.Logger('main', { level: params.LOG_LEVEL || 'info' })
  try {
    const missing = checkMissingRequestInputs(params, ['target'], ['Authorization'])
    if (missing) return errorResponse(400, missing, logger)

    const target = TARGETS[params.target]
    if (!target) return errorResponse(400, `unknown target '${params.target}'`, logger)

    const token = getBearerToken(params)              // reads params.__ow_headers.authorization
    const headers = { authorization: `Bearer ${token}`, 'content-type': 'application/json' }
    if (params.orgId) headers['x-gw-ims-org-id'] = params.orgId        // Adobe IMS org id
    if (params.fusionOrgId) headers['x-organization-id'] = params.fusionOrgId  // Fusion tenant id
    if (params.teamId) headers['x-team-id'] = params.teamId            // Fusion team id

    const res = await fetch(target.url(params), { method: target.method, headers })
    const text = await res.text()
    let body
    try { body = JSON.parse(text) } catch (e) { body = text }

    if (!res.ok) {
      return { statusCode: res.status, body: { error: `upstream ${res.status}`, target: params.target, details: body } }
    }
    return { statusCode: 200, body }
  } catch (error) {
    logger.error(error)
    return errorResponse(500, 'server error: ' + error.message, logger)
  }
}

exports.main = main
```

`getBearerToken`, `errorResponse` und `checkMissingRequestInputs` stammen aus dem generierten `actions/utils.js`, in dem die Vorlage sie Strukturvorlagen erstellt. `getBearerToken` liest `params.__ow_headers.authorization`, wo das Gateway die Kopfzeile für eingehende `Authorization` ablegt.

## Schritt 3: Aktion des Gastes aufrufen

`fetch` Sie in Ihrer Benutzeroberfläche die Aktion mit einer relativen URL (identischer Herkunft) und senden Sie das IMS-Token als Bearer. Übergeben Sie die Organisations- und Team-IDs, die der Upstream-Benutzer als Abfrageparameter benötigt.

```js
const PROXY_URL = "/api/v1/web/fusion-uix-guest/wf-proxy";

async function callProxy(target, token, { imsOrgId, fusionOrgId, teamId, start, limit } = {}) {
  const params = new URLSearchParams({ target });
  if (imsOrgId) params.set("orgId", imsOrgId);          // → x-gw-ims-org-id
  if (fusionOrgId) params.set("fusionOrgId", fusionOrgId); // → x-organization-id
  if (teamId) params.set("teamId", teamId);             // → x-team-id
  if (start != null) params.set("start", start);        // pagination offset
  if (limit != null) params.set("limit", limit);        // pagination page size
  const res = await fetch(`${PROXY_URL}?${params.toString()}`, {
    headers: { authorization: `Bearer ${token}` },
  });
  if (!res.ok) throw new Error(`${target} request failed: ${res.status}`);
  return res.json();
}
```

Abrufen von `token`, `imsOrgId`, `fusionOrgId` und `teamId` aus dem Kontext:

```js
const token       = connection.sharedContext.get("imsToken");
const imsOrgId    = connection.sharedContext.get("imsOrgId");
const fusionOrgId = connection.sharedContext.get("organization")?.id; // Fusion tenant id
const teamId      = connection.sharedContext.get("team")?.id;
```

Weitere Informationen zum Kontext finden Sie unter [Die Fusion-Kontextreferenz](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

## Besonderheiten der Fusion v3-API

Funktionsweise des Dashboards im Hinblick auf `https://fusion.adobe.com/api/v3`:

| Kopfzeile/Parameter | Wert | Anmerkungen |
| ---------------- | ------- | ------- |
| `Authorization` | `Bearer <imsToken>` | Das IMS-Token des Benutzers aus dem Kontext. |
| `x-organization-id` | `organization.id` | Die eigene Mandanten-ID von Fusion, nicht die IMS-Organisations-ID. Fusion identifiziert den Mandanten durch Folgendes. |
| `x-team-id` | `team.id` | Senden Sie , wenn der Aufruf Team-bezogen ist. |
| `x-gw-ims-org-id` | `imsOrgId` | Adobe IMS-Organisations-ID für das Gateway. |

Beachten Sie folgende Einschränkungen:

* **`GET /api/v3/hooks`ist teambezogen:** `teamId` ist ein **erforderlicher Abfrageparameter** (`/api/v3/hooks?teamId=...`). Ohne sie bekommt man eine `400`. Dies bedeutet, dass die Erweiterungspunkte nur für das *-aktive Team zurückkommen* um eine Organisation abzudecken, Teams zu schleifen und zusammenzuführen.
* **`GET /api/v3/scenarios`** arbeitet mit `organizationId` (`/api/v3/scenarios?organizationId=...`).

>[!NOTE]
>
> Die offizielle Referenz sind die [Workfront Fusion-APIs von Adobe](https://developer.adobe.com/workfront-fusion-apis/). Die Kopfzeilen-/Authentifizierungsanforderungen variieren je nach Gateway. Diese Tabelle spiegelt wider, was für die Demo tatsächlich benötigt wurde. Wenn ein Aufruf `401`/`400` zurückgibt, überprüfen Sie diese Kopfzeilen zuerst erneut.

## Ergebnisse der Paginierungsliste

Listenendpunkte (Hooks, Szenarien) in Fusion v3 geben jeweils eine **Seite** zurück, nicht den gesamten Satz. Eine Antwort sieht wie folgt aus:

```json
{
  "items": [ /* ...this page of records... */ ],
  "_page": { "start": 0, "limit": 100, "total": 342 }
}
```

Die Datensätze befinden sich unter **`items`** und die Paginierungsmetadaten sind unter **`_page`**. Sie seitenweise mit den Abfrageparametern **`start`** (Versatz) und **`limit`** (Seitengröße). Der obige Proxy durchläuft beide , sodass Seite im Gast durch Schleife läuft, bis Sie alles erfasst haben:

```js
const PAGE_LIMIT = 100;

async function fetchAllPages(target, token, opts = {}) {
  const all = [];
  let start = 0;
  // Stop when a page returns fewer than PAGE_LIMIT items, or when _page.total is reached.
  for (;;) {
    const res = await callProxy(target, token, { ...opts, start, limit: PAGE_LIMIT });
    const items = res.items ?? [];
    all.push(...items);

    const total = res._page?.total;
    const done = items.length < PAGE_LIMIT || (total != null && all.length >= total);
    if (done) break;
    start += PAGE_LIMIT;
  }
  return all;
}
```

Wenn Sie lieber außerhalb des Browsers paging möchten, führen Sie dieselbe Schleife innerhalb der Laufzeitaktion durch und geben Sie das zusammengeführte `items`-Array in einer Antwort zurück. Gehen Sie in beiden Fällen nicht davon aus, dass die erste Seite der gesamte Ergebnissatz ist. Ein Team mit mehr als einer Hook-Seite würde ansonsten so aussehen, als hätte es fehlende Szenarien.

## Sicherheitscheckliste

* **Zulassungsliste Upstreams.** Erstellen Sie die Ziel-URL niemals aus der unformatierten Client-Eingabe. Ordnen Sie einen kurzen `target` einer festen URL zu, wie in Schritt 2 beschrieben. Dadurch wird verhindert, dass Ihre Aktion zu einem offenen Relais wird.
* **Bearer-Token erforderlich** in der Aktion und leiten Sie es stromaufwärts weiter. Workfront und Fusion können die Benutzerberechtigungen erzwingen.
* **Token nie protokollieren.** `imsToken` ist eine Berechtigung. Achten Sie `LOG_LEVEL` darauf, was `stringParameters` druckt.
* **Nur über HTTPS weiterleiten** an vertrauenswürdige Adobe- und Workfront-Hosts.

## Arbeitsbeispiel: das Ereignisabonnement-Dashboard

Das Demo-Dashboard verbindet drei Quellen, um pro Workfront-Ereignisabonnement anzuzeigen, ob ein übereinstimmendes Fusionsszenario in Ordnung ist:

1. `fetchSubscriptions()` → Workfront-Ereignisabonnements (mit empfangenen/übergebenen Zählern).
1. `fetchHooks(teamId)` → Fusion-Hooks für das aktive Team (Seite mit `fetchAllPages`).
1. `fetchScenarios(fusionOrgId)` → Fusion-Szenarien für die Organisation (Seite mit `fetchAllPages`).

Der **join** verkettet sie, aber es gibt einen Haken, den es wert ist, erwähnt zu werden: ein Workfront-Abonnement und der Fusion-Hook, auf den es live verweist **verschiedene Hosts**, sodass ihre URL-Felder nicht Byte für Byte gleich sind. Was stabil ist, ist das **Token am Ende der Webhook-** (das letzte Pfadsegment). Übereinstimmung bei diesem nachfolgenden Token, nicht der vollständigen URL. Der `scenarioId` des Hooks stimmt dann mit dem `id` eines Szenarios überein:

```
subscription.targetUrl  ──(trailing token)──▶  hook.url
                                                hook.scenarioId  ──▶  scenario.id
```

```js
// Reduce a webhook URL to its trailing token so hosts/bases can differ.
function hookKey(url) {
  if (!url) return "";
  const path = String(url).trim().toLowerCase().split(/[?#]/)[0].replace(/\/+$/, "");
  const i = path.lastIndexOf("/");
  return i >= 0 ? path.slice(i + 1) : path;
}

// Index hooks by token, then look each subscription up by the same token.
const hooksByToken = new Map(hooks.map((h) => [hookKey(pick(h, ["url", "address", "targetUrl"], "")), h]));
const hook = hooksByToken.get(hookKey(pick(sub, ["url", "endpointUrl", "targetUrl", "target.url", "callbackUrl"], "")));
```

Status wird aus dem Join abgeleitet:

* **Broken**: kein übereinstimmender Hook, oder der Hook ist `gone`.
* **Filtern**: abgeglichen, aber `passed < received` (Ereignisse kommen an, werden aber vor der Ausführung des Szenarios herausgefiltert).
* **Gesund**: zugeordnet und übergeben.

Da sich die tatsächlichen Payload-Formen unterscheiden, ordnet der Client die Felder defensiv zu und versucht mehrere mögliche Schlüssel pro Feld auszuprobieren, sodass ein geringfügiger API-Unterschied die Tabelle nicht beeinträchtigt:

```js
function pick(obj, keys, fallback) {
  for (const key of keys) {
    const value = key.split(".").reduce((acc, part) => (acc == null ? acc : acc[part]), obj);
    if (value != null) return value;
  }
  return fallback;
}
```

Dies ist nur ein Beispiel. Dasselbe Proxy-Muster funktioniert für jede benötigte Workfront- oder Fusion-API.
