---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Fehlerbehebung bei benutzerdefinierten Erweiterungen
description: Fehlerbehebung bei benutzerdefinierten Erweiterungen
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 1136
ht-degree: 0%

---


# Fehlerbehebung bei benutzerdefinierten Erweiterungen

>[!NOTE]
>
>Dieser Artikel setzt eine gewisse Vertrautheit mit Software-Entwicklungs-Tools voraus.

In diesem Artikel werden einige Lösungen für die Probleme vorgestellt, auf die Sie am ehesten beim Erstellen benutzerdefinierter Erweiterungen stoßen, und zwar in der Reihenfolge, in der sie während der Entwicklung auftreten.

## Schnellprüfliste

Wenn etwas nicht funktioniert, überprüfen Sie diese zuerst:

* Node.js ist Version 18 oder 20 (`node --version`).
* Sie sind angemeldet (`aio login`) und befinden sich in der richtigen Organisation/im richtigen Projekt/Arbeitsbereich (`aio console where`).
* Der Name des Erweiterungspunkts stimmt genau überein, einschließlich der Version: `fusion/nav-organization/1`.
* Der `url` in `getWidget()` entspricht einer Route in Ihrer App.
* Ihre sichtbare Benutzeroberfläche ruft `attach({ id })` auf.
* Sie sehen den richtigen Satz von Erweiterungen in Fusion:
  * Um einen Staging-Build anzuzeigen, stellen Sie ihn in der Staging-Umgebung bereit und aktivieren Sie den Schalter Staging-Erweiterungen in Ihrem Fusion-Profil (Produkteinstellungen > Fusion-Profil > Voreinstellungen).
  * Um eine veröffentlichte Erweiterung anzuzeigen, stellen Sie sie in der Produktion bereit und lassen Sie sie genehmigen.

## Fehler 1060: „Erweiterungspunkt ist nicht vorhanden“

**Vollständige Meldung:** `CoreConsoleAPISDK ... 1060: Extension point 'fusion/nav-organization/1' does not exist` während der `aio app deploy`.

**Was bedeutet** Der Fusion-Erweiterungspunkt ist für Ihre Adobe-Organisation noch nicht aktiviert („eingebunden„). Adobe überprüft zum Zeitpunkt der Bereitstellung, ob der Erweiterungspunkt im Katalog Ihres Unternehmens vorhanden ist. Dies ist **kein** Problem mit Ihrem Code oder Ihrer YAML.

**Fehlerbehebung:** Bitten Sie das Fusion-Team, die Erweiterungspunkte (`fusion/nav-organization/1` und/oder `fusion/nav-team/1`) für Ihre IMS-Organisation zu integrieren. Wenn Sie das Onboarding anfordern, fügen Sie Folgendes ein:

* Ihre **IMS-Organisations-ID** (`XXXX@AdobeOrg`),
* die **Erweiterungspunkte** die Sie benötigen,
* Ihre **Developer Console-Projekt- und -**.

Sobald das Onboarding bestätigt wurde, führen Sie `aio app deploy` erneut aus.


## „Warten auf die erste Nachricht vom Ziel-iframe“ / Das Bedienfeld dreht sich unendlich

**Was bedeutet:** Fusion hat Ihre sichtbare Benutzeroberfläche geöffnet, aber den Handshake nicht abgeschlossen, sodass die Zeit für Fusion abgelaufen ist.

**Häufige Ursachen:**

* `attach` befindet sich nur in der Registrierungskomponente, nicht im sichtbaren Widget.
* Der `url` in `getWidget()` verweist auf eine Route, die die Komponente **Registrierung** (oder eine leere Seite) anstelle Ihres Widgets rendert.
* Der an `attach` übergebene `id` unterscheidet sich von dem in `register` verwendeten `id`. Sie müssen identisch sein. Behalten Sie also beide `Constants.js` bei.

**Beheben:** Stellen Sie sicher, dass Ihre **sichtbaren** Komponentenaufrufe `attach({ id })`:

```jsx
useEffect(() => {
  attach({ id: extensionId }).catch(console.error);
}, []);
```

Weitere Informationen finden Sie unter [Erstellen der benutzerdefinierten Erweiterungs-Benutzeroberfläche](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).



## Die Nav-Schaltfläche wird in Fusion nicht angezeigt

Wenn die Navigationsschaltfläche für Ihre benutzerdefinierte Erweiterung in Fusion nicht angezeigt wird, überprüfen Sie diese Elemente in der richtigen Reihenfolge:

1. **Schaut ihr euch die richtigen Erweiterungen an?** Standardmäßig zeigt Fusion nur veröffentlichte Erweiterungen an, die in der Produktion bereitgestellt und genehmigt wurden. Wenn Sie einen Staging-Build testen, aktivieren Sie den Schalter Staging-Erweiterungen in Ihrem Fusion-Profil (Produkteinstellungen > Fusion-Profil > Voreinstellungen) und laden Sie neu. Staging-Elemente sind mit **(Staging)**.
Weitere Informationen finden Sie unter [Veröffentlichen einer benutzerdefinierten Erweiterung](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. **Wurde sie widerrufen oder zurückgenommen?** Eine widerrufene oder zurückgenommene Erweiterung wird in Fusion nicht mehr ohne Fehler angezeigt. Wenn eine zuvor funktionierende Schaltfläche verschwunden ist, überprüfen Sie, ob sie in Adobe Exchange noch aktiv ist, bevor Sie nach einem Codeproblem suchen.
1. **Wird sie im richtigen Arbeitsbereich bereitgestellt?** Stellen Sie den Staging-Arbeitsbereich für den Arbeitsbereich bereit, den Sie tatsächlich laden, wenn Sie den Staging-Test -Schalter verwenden.
1. **Wird sie in der richtigen Organisation bereitgestellt?** Melden Sie sich bei Fusion mit einem Konto in der **IMS** Organisation an, für die Sie bereitgestellt haben.
1. **Ist es im richtigen Abschnitt?** `fusion/nav-organization/1` wird unter **Organisation** angezeigt; `fusion/nav-team/1` wird unter **Team** angezeigt (Sie müssen zuerst ein Team auswählen).
1. **Gibt es einen Typo für den Namen eines Erweiterungspunkts?** Er muss sowohl im `app.config.yaml` als auch im `ext.config.yaml` des Ordners exakt `fusion/nav-organization/1` lesen.


## Die Schaltfläche wird angezeigt, das Bedienfeld ist jedoch leer

Wenn die Schaltfläche angezeigt wird, das Bedienfeld jedoch leer ist, überprüfen Sie Folgendes:

* **Routenabweichung:** der `url` von `getWidget()` (z. B. `/index.html#/my-widget`) muss mit einem `<Route>` in `App.js` übereinstimmen. Bei einer Nichtübereinstimmung wird eine Seite ohne Komponente geladen.
* **JavaScript-Fehler:** Öffnen Sie die Registerkarte Entwickler-Tools Ihres Browsers (F12) > **Konsole** und suchen Sie nach Fehlern aus dem iframe. Beheben des gemeldeten Fehlers und erneute Bereitstellung.
* **Kopfzeile fehlt/dupliziert:** `hideWidgetHeader` in `getWidget()` steuert, ob Fusion den Titel über Ihrer Benutzeroberfläche anzeigt. Legen Sie sie auf `true` fest, wenn Sie Ihre eigene Kopfzeile rendern.

## Der iframe ist blockiert (Content Security Policy / „Rejected to Frame„)

Fusion ermöglicht nur Erweiterungen, die auf dem App Builder CDN (`*.adobeio-static.net`) von Adobe gehostet werden. In diesem CDN werden Ihre Dateien standardmäßig `aio app deploy`. Wenn Sie Ihre Benutzeroberfläche an einem anderen Ort hosten, z. B. in einer benutzerdefinierten Domain, weigert sich Fusion, sie zu laden. Stellen Sie die Bereitstellung entweder wie dokumentiert über App Builder bereit oder fragen Sie das Fusion-Team, ob Ihre Domain auf die Zulassungsliste gesetzt werden kann.

## Kontext ist leer oder veraltet

* **Leer direkt nach dem Laden:** Lesen des Kontexts **danach** `attach` wird aufgelöst, nicht vorher. Bis dahin den Status „Wird verbunden…“ anzeigen.
* **Wird nicht aktualisiert, wenn der Benutzer die Organisation oder das Team wechselt** Abonnieren Sie das `contextchange` Ereignis und lesen Sie Ihre Schlüssel im Handler erneut. Weitere Informationen finden Sie unter [Lesen der Context Fusion-Freigaben](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md#read-the-context-fusion-shares) im Artikel Erstellen der benutzerdefinierten Erweiterungs-Benutzeroberfläche.
* **Datumsangaben sehen falsch aus** Datumsfelder werden als ISO **Zeichenfolgen**, nicht `Date`. Verpacken Sie sie in `new Date(...)`. Siehe [Datumsangaben](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md#dates) im Artikel Die Fusion-Kontextreferenz.

## Der Aufruf einer API schlägt mit einem CORS-Fehler fehl

**Problem:** Die Browser-Konsole zeigt *„Kein &#39;Access-Control-Allow-Origin&#39;-Header“* an (oder die Anfrage ist blockiert), wenn Ihre Benutzeroberfläche eine Workfront/Fusion-API direkt aufruft.

**Fehlerbehebung:** Rufen Sie diese APIs nicht über den Browser auf. Leiten Sie den Aufruf über Ihre eigene App Builder-**Laufzeitaktion** (serverseitig, ohne CORS) und veranlassen Sie den Gastaufruf der Aktion mit einer relativen URL derselben Herkunft. Weitere Informationen finden Sie unter [Aufrufen von Workfront- und Fusion-](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).


## Proxy-Aktion gibt 401 selbst mit einem gültigen Token zurück

**Was bedeutet:** Mit `require-adobe-auth: true` validiert das Gateway von Adobe den Aufruf, bevor Ihre Aktion ausgeführt wird, und kann ihn ablehnen oder benutzerdefinierte Kopfzeilen ablegen, die für Ihre Upstream-Anforderungen erforderlich sind. Dies wird als `401` angezeigt.

**Beheben:** Sie `require-adobe-auth: false` für die Aktion **und** Sie die Autorisierung selbst durch. Fordern Sie einen `Authorization` Bearer in der Aktion an, leiten Sie sie stromaufwärts weiter und behalten Sie eine strikte Ziel-Zulassungsliste bei. Siehe [Require-adobe-auth: true vs. false](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#require-adobe-auth-true-vs-false).

## `GET /api/v3/hooks` gibt 400 zurück

**Was bedeutet:** Der Endpunkt Hooks **Team-Bereich**, `teamId` ist also ein erforderlicher Abfrageparameter.

**fix:**-Aufruf `/api/v3/hooks?teamId=<team.id>`. Die Hooks kommen nur für das aktive Team zurück. Um eine Organisation abzudecken, schleifen Sie ihre Teams und fusionieren Sie. Szenarien akzeptieren dagegen `organizationId`. Siehe [&#x200B; zur Fusion v3-API](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#fusion-v3-api-specifics).


## `aio`-Fehler

* **`aio: command not found`:** Die CLI ist unter Ihrem PFAD nicht installiert oder nicht installiert. Führen Sie `npm install -g @adobe/aio-cli` erneut aus und öffnen Sie dann ein neues Terminal.
* **Build/Bereitstellung schlägt auf einer brandneuen Knotenversion fehl:** Verwenden Sie den Knoten **18 oder 20 LTS**. Sehr neue, nicht-LTS-Releases brechen manchmal die Toolchain.
* **„Sie sind kein Entwickler“ / Ihre Organisation kann nicht angezeigt werden:** Ihr Adobe-Organisationsadministrator muss Ihnen die Rolle **Entwickler** und Zugriff auf App Builder gewähren. Weitere Informationen finden Sie unter [Einrichten von Tools und Konten für Benutzeroberflächenerweiterungen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
* **401 / Ungültiges Token während der Bereitstellung oder Erkennung:** Ihre Sitzung abgelaufen ist oder Sie Umgebungen mischen. Führen Sie `aio logout` dann `aio login` aus, bestätigen Sie die `aio console where` und stellen Sie sie in dem Arbeitsbereich bereit, den Sie laden.

## Sammeln von Informationen für den Support

Sammeln Sie diese Informationen, um die Diagnose viel schneller zu stellen:

* Der exakte ausgeführte Befehl und die Fehlerausgabe **full**.
* Ihre **IMS-Organisations**-ID, **Projekt** und **Arbeitsbereich**.
* Der **Erweiterungspunkt** auf den Sie abzielen.
* Ob die `aio app deploy` erfolgreich war und ob die Erweiterung **veröffentlicht** (oder bei einem Staging-Test, ob die Staging-Erweiterungen eingeschaltet sind).
* Alle Fehler im Browser **Konsole** (F12) beim Öffnen des Bedienfelds in Fusion.
