---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Demo-exemplarische Vorgehensweise einer benutzerdefinierten Erweiterung
description: Demo-exemplarische Vorgehensweise einer benutzerdefinierten Erweiterung
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 964
ht-degree: 0%

---


# Beispielanleitung zum Erstellen einer benutzerdefinierten Erweiterung in Fusion

>[!NOTE]
>
>Dieser Artikel setzt eine gewisse Vertrautheit mit Software-Entwicklungs-Tools voraus.

In dieser Demo wird erläutert, wie Sie eine benutzerdefinierte Erweiterung erstellen, bereitstellen und in Fusion ausführen.

Zu diesem Datensatz gehören:

* Strukturieren Sie eine App Builder-App aus der generischen Experience Cloud-Shell-Vorlage.
* Targeting der App an einem Fusion-Erweiterungspunkt.
* Stellen Sie die App im Staging-Arbeitsbereich bereit.
* Aktivieren Sie Staging-Tests in Fusion und zeigen Sie, wie die App ausgeführt wird.

Ausgehend von der Vorlage und nicht von einer leeren `--standalone-app` wird der SPA-Bootstrap für Sie generiert: `index.js`, `exc-runtime.js`, `App.js` mit Routing und `ErrorBoundary` sowie eine `ExtensionRegistration`. Die Live-Schritte in der Demo bestehen darin, die Konfiguration erneut anzusprechen und zwei Dateien zu bearbeiten, was genau dem entspricht, wie die echte `fusion-uix-guest` erstellt wurde.

>[!NOTE]
>
> **Zeit:** Die Live-Demo dauert etwa 10 Minuten, nachdem Ihre Tools eingerichtet wurden. Sie müssen die einmalige Einrichtung (Knoten 18/20, `aio` CLI, `aio login`) **vor** der Demo durchführen. Anweisungen finden Sie unter [Einrichten von Tools und Konten für Benutzeroberflächenerweiterungen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).


## Vorbereitung

Dies muss nur einmal durchgeführt werden und kann vor der Demo außerhalb der Kamera erfolgen.

```sh
node --version          # must be 18 or 20
aio --version           # @adobe/aio-cli installed
aio login               # signs you into your Adobe org
aio console org select  # pick the org you'll demo in (same org as Fusion)
```

In der Demo-Organisation müssen zwei Dinge zutreffen:

* Der `fusion/nav-organization/1` Erweiterungspunkt wurde in die Organisation integriert. Wenn es nicht integriert ist, schlägt die Bereitstellung mit Fehler 1060 fehl. Weitere Informationen finden Sie unter [Fehlerbehebung bei benutzerdefinierten Erweiterungen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).
* Die Funktion für benutzerdefinierte Erweiterungen ist im Fusion-Host aktiviert. (Diese Funktion ist standardmäßig aktiviert). Da Sie einen Staging-Build anstelle eines veröffentlichten demonstrieren, aktivieren Sie auch den **Staging-Erweiterungen**-Schalter in Ihrem Fusion-Profil. (Dieser Schalter wird in Schritt 7 angezeigt.) Fusion zeigt nur veröffentlichte Erweiterungen an, bis Sie dies tun.

## Schritt 1: App aus der generischen Vorlage generieren

```sh
aio app init my-fusion-extension --template @adobe/generator-app-excshell
cd my-fusion-extension
```

* Wählen Sie **Neues Projekt erstellen** aus, wenn Sie dazu aufgefordert werden, und akzeptieren Sie den vorgeschlagenen Namen.
* `@adobe/generator-app-excshell` ist die generische **Experience Cloud Shell**-Benutzeroberflächenerweiterungsvorlage und ist nicht produktspezifisch. Es erstellt eine vollständige, funktionierende SPA unter `src/dx-excshell-1/`.

>[!NOTE]
>
>Wenn Sie das Menü bevorzugen, führen Sie `aio app init my-fusion-extension` aus, wählen Sie **Erweiterungen oder eigenständige Anwendung hinzufügen** > **Vorlagen** und wählen Sie **&quot;App Builder UIX Extension for Experience Cloud Shell“**.

Sie erhalten eine Reihe von Dateien, einschließlich der folgenden:

```
my-fusion-extension/
|-- app.config.yaml
|-- src/dx-excshell-1/
    |-- ext.config.yaml
    |-- web-src/src/
        |-- index.js          // SPA bootstrap (exc-app Runtime + React render)
        |-- exc-runtime.js    // Experience Cloud Shell runtime glue
        |-- components/
            |-- App.js                    // Router + ErrorBoundary (generated)
            |-- ExtensionRegistration.js  // sample registration (generated)
```

## Schritt 2: Fusion-Gastbibliothek hinzufügen

Die Vorlage enthält bereits React, React Spectrum und Exc-App. Fügen Sie die Bibliothek hinzu, die mit dem Fusion-Host spricht:

```sh
npm install @adobe/uix-guest
```

## Schritt 3: Targeting der Konfiguration auf Fusion

Öffnen Sie **`app.config.yaml`** und ändern **nur den Schlüssel des Erweiterungspunkts** vom Experience Cloud-Shell-Punkt zum Fusion-Pfad (lassen Sie den `$include` unverändert):

```yaml
extensions:
  fusion/nav-organization/1:                 # was: dx/excshell/1
    $include: src/dx-excshell-1/ext.config.yaml
```

Sie müssen nichts anderes in der Konfiguration ändern. Der Ordnername `dx-excshell-1` ist intern und wirkt sich nicht auf Fusion aus, sodass Sie ihn beibehalten können. Das Umbenennen würde auch bedeuten, dass alle Aktionspfade aktualisiert werden. Überspringen Sie das für die Demo.

>[!NOTE]
>
>Wenn Sie den Abschnitt &quot;**&quot;**, verwenden Sie stattdessen `fusion/nav-team/1`. Um sowohl **Organisation** Team in der Produktion zu versenden, verwenden Sie **zwei separate Projekte**. Ein Erweiterungspunkt-Bundle pro Registrierungsnamen vermeidet eine Kollision zwischen freigegebenen Apps.

## Schritt 4: Registrierungs- und Widget-Dateien bearbeiten

Alle Pfade befinden sich unter `src/dx-excshell-1/web-src/src/components/`.

### **`ExtensionRegistration.js`**

Die generierte Datei registriert ein Experience Cloud Shell-Beispiel. Ersetzen Sie die `methods` durch den Fusion **`dashboard.getWidget`**-Vertrag, damit Fusion Ihren Titel und den Wohnort der Benutzeroberfläche kennt:

```js
import { Text } from "@adobe/react-spectrum";
import { register } from "@adobe/uix-guest";
import metadata from "../../../../app-metadata.json";
import { extensionId } from "./Constants";

function ExtensionRegistration() {
  const init = async () => {
    await register({
      id: extensionId,
      metadata,
      methods: {
        dashboard: {
          getWidget() {
            return {
              id: extensionId,
              title: "My Fusion tool",          // label on the Fusion nav button
              description: "Hello from App Builder",
              url: "/index.html#/widget",       // route to the visible UI (4b)
              widgetSize: { defaultWidth: 6, defaultHeight: 6 },
              hideWidgetHeader: false,
            };
          },
        },
      },
    });
  };
  init().catch(console.error);

  return <Text>Registering with Fusion...</Text>;
}

export default ExtensionRegistration;
```

Wenn `Constants.js` daneben nicht vorhanden ist, erstellen Sie es:

```js
module.exports = { extensionId: "my-fusion-extension" };
```

### `DashboardWidget.js`

Erstellen Sie diese Datei. Dadurch wird der Handshake abgeschlossen und der Live Fusion-Kontext angezeigt:

```js
import { useEffect, useState } from "react";
import { Flex, Heading, Text, View } from "@adobe/react-spectrum";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

export default function DashboardWidget() {
  const [ctx, setCtx] = useState(null);

  useEffect(() => {
    attach({ id: extensionId })
      .then((guest) => {
        const read = () =>
          KEYS.reduce((acc, k) => ({ ...acc, [k]: guest.sharedContext.get(k) }), {});
        setCtx(read());
        guest.addEventListener("contextchange", () => setCtx(read()));
      })
      .catch((e) => console.error("attach failed", e));
  }, []);

  return (
    <View padding="size-300">
      <Heading level={2}>Hello from App Builder</Heading>
      {!ctx ? (
        <Text>Connecting to Fusion...</Text>
      ) : (
        <Flex direction="column" gap="size-100" marginTop="size-200">
          <Text>User: {ctx.user?.name ?? ctx.imsUserId}</Text>
          <Text>Organization: {ctx.organization?.name} (id {ctx.organization?.id})</Text>
          <Text>Team: {ctx.team?.name ?? "-"}</Text>
        </Flex>
      )}
    </View>
  );
}
```

### `App.js`

Der generierte Router sendet bereits `index`/`index.html` an `ExtensionRegistration`. Fügen Sie eine Route für das Widget hinzu und importieren Sie sie:

```js
import DashboardWidget from "./DashboardWidget";
// ...inside <Routes>, alongside the existing ExtensionRegistration routes:
<Route exact path="widget" element={<DashboardWidget />} />
```

> Der Routenpfad (`widget`) muss dem Hash in `getWidget().url` (`/index.html#/widget`) entsprechen. Behalten Sie die generierten `index.js`/`exc-runtime.js` und den Rest der `App.js` exakt als Strukturvorlage bei, da dies der Bootstrap ist, den Sie von der Vorlage bereitstellen wollten.

## Schritt 5: Erstellen

```sh
aio app build
```

Dadurch wird das Frontend kompiliert und der Metadaten-Hook ausgeführt, der `app-metadata.json` generiert. Beheben Sie etwaige Fehler, bevor Sie fortfahren.

## Schritt 6: Staging-Bereitstellung

```sh
aio console workspace select     # choose Stage
aio app deploy
```

`deploy` hostet Ihre Benutzeroberfläche im CDN von Adobe und registriert den Erweiterungsendpunkt im Staging-Arbeitsbereich, über den Fusion sie ermitteln kann. Die CLI druckt die Endpunkt-URL, z. B. `https://<project>-stage.adobeio-static.net`.

## Schritt 7: Aktivieren Sie das Staging-Testing und zeigen Sie die Erweiterung in Fusion an

1. Öffnen Sie Fusion in Experience Cloud, angemeldet bei derselben Organisation, für die Sie bereitgestellt haben.
1. Öffnen Sie das Menü des Benutzeravatars und gehen Sie zu **Produkteinstellungen** > **Fusionsprofil** > **Voreinstellungen**.
1. Schalten Sie den **Staging-Erweiterungen** ein und bestätigen Sie das Neuladen.

   Fusion lädt jetzt Erweiterungen aus dem Staging-Arbeitsbereich und markiert sie **(Staging)**.
1. Navigieren Sie zum **Organisation** im linken Navigationsbereich.

   Ihr **„My Fusion Tool (Stage)“** Button erscheint.
1. Klicken Sie auf die **„My Fusion Tool (Stage)“**.
Ihre Benutzeroberfläche wird im Hauptbedienfeld geladen und zeigt den Live-Benutzer, die Organisation und das Team an.
1. **Wechseln Sie die aktive Organisation oder das aktive Team** in Fusion.

   Das Bedienfeld wird aktualisiert und zeigt Live-Kontext (`contextchange`) an.

>[!TIP]
>
>Wenn die Schaltfläche nicht angezeigt wird, laden Sie sie einmal neu, da die Erkennung pro Sitzung zwischengespeichert wird. Siehe dann [Fehlerbehebung bei benutzerdefinierten Erweiterungen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).


## Iteration während der Demo

Nehmen Sie eine Änderung vor und erstellen Sie dann erneut und stellen Sie erneut bereit.  Benutzer sehen die aktualisierte Erweiterung, wenn sie sie das nächste Mal öffnen.

```sh
aio app build && aio app deploy
```

## Nach der Demo zur Produktion wechseln

Die Bühne reicht aus, um es vorzuführen. Um die Veröffentlichung organisationsweit durchzuführen, wechseln Sie zum Arbeitsbereich Produktion , stellen Sie bereit und senden Sie die Genehmigungsanfrage. Die Anfrage muss mit der Rolle eines Systemadministrators gesendet werden. Den vollständigen Prozess finden Sie unter [Version für die Produktion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md#release-on-production).

## Demo-Talktrack (optional)

Während der Live-Demo sollten Sie die folgenden Punkte beachten:

* **„Ich habe mit der generischen Experience Cloud-Shell-Vorlage begonnen.“** Es strukturiert die gesamte SPA-Shell, sodass ich nur den Erweiterungspunkt neu ausgewählt und zwei Dateien bearbeitet habe.
* **„Fusion ist der Host, meine App ist der Gast.“** Sie werden in separaten Frames ausgeführt und beziehen sich auf die Erweiterbarkeit der Benutzeroberfläche von Adobe SDK ohne benutzerdefinierte Netzwerke.
* **„Registrierung vs. Ansicht“** Der ausgeblendete Rahmen *registriert* was ich anbiete (`dashboard.getWidget`), und der sichtbare Rahmen *hängt* und liest Kontext.
* **„Staging-Tests sind ein Switch pro Benutzer.** Fusion zeigt standardmäßig nur veröffentlichte Erweiterungen an. Ich habe in meinem Fusion-Profil Stage-Erweiterungen aktiviert, um meinen Stage-Build ohne Produktionsfreigabe zu laden.
* **Live-Kontext.** Wenn die Organisation oder das Team gewechselt wird, wird der Kontext erneut gesendet und der Gast wird erneut gerendert.
