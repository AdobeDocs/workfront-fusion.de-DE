---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Erstellen der benutzerdefinierten Erweiterungs-Benutzeroberfläche
description: Erstellen der benutzerdefinierten Erweiterungs-Benutzeroberfläche
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
source-wordcount: 440
ht-degree: 0%

---


# Erstellen der benutzerdefinierten Erweiterungs-Benutzeroberfläche

>[!NOTE]
>
>Dieser Artikel setzt eine gewisse Vertrautheit mit Software-Entwicklungs-Tools voraus.

In diesem Verfahren wird beschrieben, wie der Bildschirm erstellt wird, den die Benutzer sehen, und die **Verbindung („Handshake„)** mit Fusion abgeschlossen wird.

Während dieses Vorgangs sollten Sie beachten, dass Ihre Erweiterung in zwei Frames ausgeführt wird: dem ausgeblendeten **Registrierungs**-Frame und dem sichtbaren **UI**-Frame.

Informationen zu Frames in Bezug auf benutzerdefinierte Erweiterungen finden Sie unter [Frames in einer Benutzeroberflächenerweiterung](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension).

Anweisungen zum Erstellen des Registrierungsrahmens finden Sie unter [Erstellen eines Projekts für die Erweiterbarkeit der Benutzeroberfläche](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).

## Route zwischen den beiden Frames

Beide Frames laden dieselbe `index.html`. Ein kleiner Frontend-Router entscheidet anhand der URL, welche Komponente angezeigt werden soll.

1. Routen in `web-src/src/components/App.js` einrichten. Der wesentliche Teil ist:

   ```jsx
   import { HashRouter as Router, Routes, Route } from "react-router-dom";
   import ExtensionRegistration from "./ExtensionRegistration";
   import DashboardWidget from "./DashboardWidget";
   
   export default function App() {
     return (
       <Router>
         <Routes>
           {/* Background frame: registers the extension with Fusion */}
           <Route index element={<ExtensionRegistration />} />
           <Route path="index.html" element={<ExtensionRegistration />} />
   
           {/* Visible frame: the URL you returned from getWidget() */}
           <Route path="my-widget" element={<DashboardWidget />} />
         </Routes>
       </Router>
     );
   }
   ```

   Diese Routen sind wie folgt der vorherigen Konfiguration zugeordnet:

   * Die Standardroute (`index`) rendert **`ExtensionRegistration`**, den ausgeblendeten Rahmen, der `register(...)` aufruft.
   * Die `my-widget` Route rendert **`DashboardWidget`**, Ihre sichtbare Benutzeroberfläche. Dies entspricht dem `url: "/index.html#/my-widget"`, den Sie von `getWidget()` auf [vorherigen Seite) &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).

   >[!NOTE]
   >
   > **Die Routen und die `getWidget`-URL müssen übereinstimmen.** Wenn Sie den Routennamen ändern, ändern Sie auch den `url`, oder Fusion lädt eine leere Seite.

1. Fahren Sie fort [Vervollständigen Sie den Handshake mit `attach`](#complete-the-handshake-with-attach).

## Vervollständigen Sie den Handshake mit `attach`

Dies ist die wichtigste Zeile in der sichtbaren Benutzeroberfläche. Wenn Fusion Ihren UI-Frame öffnet, wartet er darauf, dass dieser Frame „eingecheckt“ wird. Ihr Code checkt ein, indem er `attach({ id })` aufruft.

**Wenn dies ausgelassen wird, tritt bei Fusion eine Zeitüberschreitung auf** mit einem Fehler wie &quot;*wartet auf die erste Nachricht vom Ziel-iframe“*

1. Fügen Sie Folgendes zu `web-src/src/components/DashboardWidget.js` hinzu:

   ```jsx
   import { useEffect, useState } from "react";
   import { attach } from "@adobe/uix-guest";
   import { extensionId } from "./Constants";
   
   export default function DashboardWidget() {
     const [connection, setConnection] = useState(null);
   
     useEffect(() => {
       // Tell Fusion this UI frame is ready. Required.
       attach({ id: extensionId })
         .then(setConnection)
         .catch((e) => console.error("attach failed", e));
     }, []);
   
     if (!connection) {
       return <p>Connecting to Fusion...</p>;
     }
   
     return <h2>Hello from my Fusion extension!</h2>;
   }
   ```

   Dieser Code bewirkt Folgendes:

   * `attach({ id })` gibt ein &quot;**&quot; zurück** sobald Fusion antwortet. Wir empfehlen, dies zu speichern, da Sie es im nächsten Schritt verwenden werden, um den von Fusion gesendeten Kontext zu lesen.
   * Bis die Verbindung aufgelöst ist, wird kurz „Verbindung wird hergestellt…“ Meldung wird angezeigt.
   * Verwendet die **gleiche`extensionId`**, die Sie in `Constants.js` festgelegt haben.

   An dieser Stelle haben Sie eine funktionierende Erweiterung: Sie registriert, fügt hinzu und zeigt eine Nachricht an. Alles, was danach steht, ist über die Verwendung der Daten, die Fusion Ihnen gibt.

1. Fahren Sie fort [Lesen Sie den Kontext Fusion-Freigaben](#read-the-context-fusion-shares).

## Lesen des Kontexts von Fusion-Freigaben

Nachdem sie angehängt wurde, stellt die Verbindung einen **freigegebenen Kontext** mit Informationen über den aktuellen Benutzer, die aktuelle Organisation und das aktuelle Team bereit. Sie können einzelne Werte mit `connection.sharedContext.get("<key>")` lesen:

```jsx
const orgId = connection.sharedContext.get("imsOrgId");
const organization = connection.sharedContext.get("organization"); // full Fusion org
const user = connection.sharedContext.get("user");                 // full Fusion user
```

Dieses Beispiel zeigt ein vollständiges, reaktives Beispiel, das auch aktualisiert wird, wenn Benutzende die Organisation oder das Team wechseln:

```jsx
import { useEffect, useState } from "react";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

function readContext(source) {
  // sharedContext behaves like a Map (.get); the change event gives a plain object.
  const get =
    typeof source.get === "function" ? (k) => source.get(k) : (k) => source[k];
  return Object.fromEntries(KEYS.map((k) => [k, get(k)]));
}

export default function DashboardWidget() {
  const [context, setContext] = useState(null);

  useEffect(() => {
    let cleanup = () => {};
    attach({ id: extensionId })
      .then((connection) => {
        // 1) initial values
        setContext(readContext(connection.sharedContext));

        // 2) react to org/team/user changes pushed by Fusion
        const onChange = (event) =>
          setContext(readContext(event?.detail?.context ?? connection.sharedContext));
        connection.addEventListener("contextchange", onChange);
        cleanup = () => connection.removeEventListener?.("contextchange", onChange);
      })
      .catch((e) => console.error("attach failed", e));
    return () => cleanup();
  }, []);

  if (!context) return <p>Connecting to Fusion...</p>;

  return (
    <div>
      <h2>{context.organization?.name ?? "No organization"}</h2>
      <p>Signed in as {context.user?.name} ({context.user?.email})</p>
      <p>IMS org: {context.imsOrgId}</p>
    </div>
  );
}
```

Beachten Sie Folgendes:

* **Anfangswerte lesen** von `connection.sharedContext.get(key)` direkt nach der `attach`.
* **Abonnieren Sie`contextchange`**, um synchron zu bleiben. Fusion löst dieses Ereignis aus, wenn sich die aktive Organisation, das aktive Team oder der aktive Benutzer ändert. Die neuen Werte kommen am `event.detail.context` an.

Die vollständige Liste der Schlüssel und deren Inhalt finden Sie in der [Kontextreferenz zu Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

Um mit der Konfiguration Ihrer benutzerdefinierten Erweiterung fortzufahren, navigieren Sie zu [Die Fusion-Kontextreferenz](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).
