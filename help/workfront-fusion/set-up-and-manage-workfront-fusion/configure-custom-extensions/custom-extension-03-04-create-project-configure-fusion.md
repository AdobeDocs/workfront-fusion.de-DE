---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Erstellen eines Projekts für die Erweiterbarkeit der Benutzeroberfläche
description: Erstellen eines Projekts für die Erweiterbarkeit der Benutzeroberfläche
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 1360
ht-degree: 0%

---

# Erstellen eines Projekts für die Erweiterbarkeit der Benutzeroberfläche

>[!NOTE]
>
>Dieser Artikel setzt eine gewisse Vertrautheit mit Software-Entwicklungs-Tools voraus.

Um eine benutzerdefinierte Benutzeroberflächenerweiterung zu erstellen, müssen Sie dafür ein App Builder-Projekt erstellen.

Auf dieser Seite wird beschrieben, wie Sie mit der `aio` Befehlszeile ein generisches App Builder-Projekt generieren. „Generisch“ bedeutet, dass das Projekt **nicht** von einer produktspezifischen Vorlage beginnt. Wenn Sie mit einer generischen App beginnen, wird das Projekt vereinfacht und es wird ermöglicht, eine Verbindung mit Workfront Fusion herzustellen.

Es kann nützlich sein, sich mit den folgenden Konzepten und der folgenden Terminologie bezüglich der Erstellung eines Projekts zur Verwendung mit der Adobe Fusion-KI-Erweiterbarkeit vertraut zu machen.

* **Adobe Developer Console** (<https://developer.adobe.com/console>) ist das Web-Dashboard, in dem sich Ihr Projekt befindet.

* **Terminologie**:

  | Begriff | Bedeutung |
  | ------ | --------------- |
  | **Organisation** | Die Adobe-Organisation Ihres Unternehmens. Die gleiche Organisation, die Sie in Fusion verwenden. |
  | **Projekt** | Ein Container für eine Anwendung/Erweiterung. Sie erstellen ein Projekt für Ihre Erweiterung. |
  | **Arbeitsbereich** | Eine Kopie der Projektkonfiguration für einen Arbeitsschritt. Jedes Projekt hat einen **Produktions** Arbeitsbereich, und Sie verwenden normalerweise auch einen **Staging**-Arbeitsbereich zum Testen. Stellen Sie sich Arbeitsbereiche wie Umgebungen vor. |
  | **Anmeldedaten/Services** | Berechtigungen, die Ihre App verwenden darf. Die für Sie erstellten Standardeinstellungen reichen aus, um zu starten. |

* Es gibt zwei Möglichkeiten, ein Projekt zu erstellen:

  * **Automatisch (empfohlen):** Der Befehl `aio app init` erstellt das Projekt und die Arbeitsbereiche für Sie, während Sie den Code generieren. Dieser Artikel beschreibt diesen Prozess.
  * **Manuell** Sie erstellen das Projekt zuerst selbst in der Developer Console und zeigen dann `aio` darauf. Wir empfehlen, dies nur zu tun, wenn Ihre Organisation erfordert, dass Projekte zentral erstellt werden.

* Bei der Entscheidung, welcher Arbeitsbereich verwendet werden soll, muss zuerst entwickelt und **„Staging** bereitgestellt werden. Fusion lädt einen Staging-Build nur, wenn der Benutzer Staging-Tests in seinem Fusion-Profil aktiviert (Menü Benutzeravatar > Produkteinstellungen > Fusion-Profil > Voreinstellungen > Staging-Erweiterungen). Andernfalls werden nur veröffentlichte Produktions-Erweiterungen angezeigt. Sie können auch eine lokale Vorschau mit `aio app run` anzeigen und später zur **Produktion** weiterleiten.

  Weitere Informationen zum Hochstufen zur Produktion finden Sie unter [Erweiterung veröffentlichen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).


## `aio app init` ausführen

1. Öffnen Sie ein Terminal.
1. Verschieben Sie im Terminal in den Ordner, in dem Sie die Projekte ablegen.
1. Durchgang:

   ```sh
   aio app init my-fusion-extension --standalone-app
   ```

   * `my-fusion-extension` ist der Ordner-/App-Name. Sie können diesen Namen auswählen, jedoch Kleinbuchstaben, Bindestriche und keine Leerzeichen verwenden.
   * `--standalone-app` weist die CLI an, ein **-Anwendungsskelett zu erstellen** anstatt Sie zu bitten, eine Produktvorlage auszuwählen. Dies ist der Schlüssel, um die AEM-Vorlage (oder eine andere) zu vermeiden.

1. Wenn Sie dazu aufgefordert werden **wählen Sie Ihre Organisation** (wenn Sie zu mehreren gehören).
1. Wenn Sie dazu aufgefordert werden, wählen **Neues Projekt erstellen** und akzeptieren Sie den vorgeschlagenen Namen oder wählen Sie ein vorhandenes leeres Projekt aus.

   Der Befehl richtet die Arbeitsbereiche **Staging** und **Produktion** automatisch ein.

   Der Befehl generiert auch Dateien im `my-fusion-extension` Ordner und führt `npm install` aus.

1. Fahren Sie [Projekterstellung bestätigen](#confirm-project-creation) fort.

>[!NOTE]
>
> **Wenn Sie das interaktive Menü bevorzugen:** Führen Sie `aio app init my-fusion-extension` > (ohne `--standalone-app`) aus. Wenn **gefragt wird: „Nach welchen Vorlagen möchten Sie suchen?“** oder eine Checkliste mit Vorlagen anzeigt. Wählen Sie dazu keine Produktvorlage wie AEM aus. Wählen Sie die Option zum Erstellen einer **eigenständigen Anwendung** / **„Alle Erweiterungspunkte → keine“**.

## Projekterstellung überprüfen

1. Wechseln Sie im Terminal in den erstellten Ordner:

   ```sh
   cd my-fusion-extension
   ```

   Es sollte eine ähnliche Struktur angezeigt werden (einige Dateien ausgelassen):

   ```
   my-fusion-extension/
   |--- app.config.yaml   // main configuration (you will edit this)
   |---  package.json   //dependencies and scripts
   |---  src/    // your source code
   |---  web-src/  or  src/.../web-src/  // front-end files (HTML/JS)
   ```

   Die beiden Dateien, die Sie am meisten interessieren, sind:

   * **`app.config.yaml`**: Die zentrale Konfiguration. Später werden Sie hier einen `extensions:` Abschnitt hinzufügen, der Ihre App mit einem Fusion-Erweiterungspunkt verbindet.
   * **`package.json`**: Listet die Bibliotheken auf, die Ihre App verwendet. Sie fügen hier die Gastbibliothek der Erweiterbarkeit der Adobe-Benutzeroberfläche hinzu.

1. Fahren Sie mit [Hinzufügen erforderlicher Bibliotheken](#add-required-libraries) fort.

>[!TIP]
>
> Machen Sie sich keine Gedanken, wenn sich Ihr generiertes Layout in den verschiedenen CLI-Versionen geringfügig unterscheidet. Dieses Verfahren teilt Ihnen genau mit, welche Dateien erstellt werden sollen und was in sie eingefügt werden soll, damit Sie die erwartete Struktur unabhängig vom Ausgangspunkt abgleichen können.

## Erforderliche Bibliotheken hinzufügen

Ihre Erweiterung benötigt zwei Bibliotheken:

* **`@adobe/uix-guest`**: Ermöglicht es Ihrer App, mit Fusion (dem Host) zu sprechen.
* **`@adobe/react-spectrum`**: Adobes React-UI-Komponenten, sodass Ihr Bildschirm dem Erscheinungsbild von Adobe entspricht. (Optional, aber empfohlen. Stattdessen können Sie auch Nur-HTML verwenden.)

Installieren dieser Bibliotheken:

1. Führen Sie im Terminal Folgendes aus:

   ```sh
   npm install @adobe/uix-guest @adobe/react-spectrum
   ```

1. (Bedingt) Wenn das generierte Projekt React nicht bereits enthält, installieren Sie es auch:

   ```sh
   npm install react react-dom react-router-dom
   ```

1. Fahren Sie mit [Bestätigen der Projekt-Builds](#confirm-the-project-builds) fort.

## Bestätigen der Projekt-Builds

Bevor Sie Änderungen vornehmen, stellen Sie sicher, dass das leere Projekt Builds erstellt

1. Führen Sie im Terminal Folgendes aus:

   ```sh
   aio app build
   ```

   Wenn dies fehlerfrei abgeschlossen wird, sind Ihre Tools und Ihr Projekt korrekt konfiguriert. Sie sind bereit, das Projekt mit Fusion zu verbinden.

   >[!TIP]
   >
   > **Wenn der Build fehlschlägt,** die häufigste Ursache eine nicht unterstützte Node.js-Version. Führen Sie `node --version` aus und stellen Sie sicher, dass es 18 oder 20 ist.
   >
   >* Informationen zur Installation von Node.js finden Sie unter [Einrichten der Tools](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
   >* Weitere Informationen zu möglichen Fehlern finden Sie unter [Fehlerbehebung](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

1. Fahren Sie fort [Konfigurieren des Projekts für Fusion](#configure-the-project-for-fusion).

## Konfigurieren des Projekts für Fusion

Der nächste Schritt beim Einrichten Ihrer benutzerdefinierten Erweiterung besteht darin, Ihr generisches Projekt mit Workfront Fusion zu verbinden.

Sie werden:

1. [Erstellen eines Ordners für Ihre Erweiterung](#create-a-folder-for-your-extension)
1. App Builder über einen Fusion **Erweiterungspunkt** (in `app.config.yaml`) informieren.
1. Beschreiben Sie die Teile Ihrer Erweiterung (in `ext.config.yaml`).
1. **Registrieren** Ihr Widget, damit Fusion den Titel und den Lebensraum der Benutzeroberfläche kennt.

Wir verwenden überall `fusion/nav-organization/1`. Um stattdessen den Abschnitt Team auszuwählen, tauschen Sie überall `fusion/nav-team/1` aus. Um beide zu unterstützen, wiederholen Sie das Muster für jedes.

## Erstellen eines Ordners für Ihre Erweiterung

1. Erstellen Sie Ihre Dateien, sodass das Projekt wie folgt aussieht:

   ```
   my-fusion-extension/
   |-- app.config.yaml
   |-- src/
          |-- fusion-nav-organization-1/          // one folder per extension point
             |-- ext.config.yaml
             |-- web-src/
                |-- src/
                   |-- components/
                      |-- App.js
                      |-- ExtensionRegistration.js
                      |-- DashboardWidget.js
                      |-- Constants.js
   ```

   Es wird empfohlen, den Ordner nach dem Erweiterungspunkt (`fusion-nav-organization-1`) zu benennen. Der genaue Name liegt bei Ihnen, er muss jedoch mit dem übereinstimmen, auf den Sie in `app.config.yaml` verweisen.

1. Fahren Sie fort[ den Erweiterungspunkt in `app.config.yaml`](#declare-the-extension-point-in-appconfigyaml) zu deklarieren.

## Deklarieren des Erweiterungspunkts in `app.config.yaml`

1. Öffnen Sie `app.config.yaml` und aktualisieren Sie seinen Inhalt wie folgt:

   ```yaml
   extensions:
     fusion/nav-organization/1:
       $include: src/fusion-nav-organization-1/ext.config.yaml
   ```

   Dieser Inhalt beschreibt Folgendes:

   * `extensions:`: Diese App implementiert einen oder mehrere Erweiterungspunkte.
   * `fusion/nav-organization/1`: Der Fusion-Steckplatz, an den Sie sich anschließen. **Der Name muss genau übereinstimmen** einschließlich Version `1`.
   * `$include:`: Dies verweist auf eine zweite Konfigurationsdatei (die im nächsten Schritt erstellt wurde), die den Inhalt dieser Erweiterung beschreibt. Wenn Sie sie in einer separaten Datei speichern, bleibt `app.config.yaml` sauber und Sie können später weitere Erweiterungspunkte hinzufügen.

   >[!NOTE]
   >
   >Wenn Sie beide Erweiterungen als Ziel auswählen, listen Sie beide mit jeweils einem eigenen Ordner auf:
   >
   > ```yaml
   > extensions:
   >     fusion/nav-organization/1:
   >         $include: src/fusion-nav-organization-1/ext.config.yaml
   >     fusion/nav-team/1:
   >         $include: src/fusion-nav-team-1/ext.config.yaml
   > ```

   1. Fahren Sie fort[Beschreiben Sie die Erweiterung in `ext.config.yaml`](#describe-the-extension-in-extconfigyaml)

## Beschreiben Sie die Erweiterung in `ext.config.yaml`

1. `src/fusion-nav-organization-1/ext.config.yaml` erstellen mit:

   ```yaml
   operations:
      view:
       - type: web
         impl: index.html
   web: web-src
   hooks:
     pre-app-build: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
      pre-app-run: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
   ```

   Dieser Inhalt beschreibt Folgendes:

   * **`operations.view`**: Deklariert, dass Ihre Erweiterung eine **Ansicht** (eine sichtbare Benutzeroberfläche) bereitstellt, die von `index.html` bereitgestellt wird. Dadurch wird Ihre Erweiterung zu einem Bildschirm, anstatt nur im Hintergrund ausgeführt zu werden.
   * **`web: web-src`**: Der Ordner, der Ihre Frontend-Dateien enthält. App Builder erstellt alles hier unter und hostet es im Content Delivery Network (CDN) von Adobe.
   * **`hooks`**: Kleine Befehle, die automatisch zur Build-/Laufzeit ausgeführt werden. Das `generate-metadata.js`-Skript wird mit `@adobe/uix-guest` ausgeliefert und erzeugt eine `app-metadata.json`-Datei, die Ihr Registrierungs-Code benötigt (siehe Schritt 4). Sie schreiben dieses Skript nicht, Sie verweisen nur darauf.

   >[!NOTE]
   >
   > Wenn Sie auch Server-seitige Logik benötigen, können Sie auch Server-lose `actions` (kleine Backend-Funktionen) hinzufügen. Aktionen sind optional und nicht erforderlich, um eine Benutzeroberfläche zu rendern. Daher lassen wir sie aus, um diesen Leitfaden fokussiert zu halten. Wenn Sie sie später hinzufügen, deklarieren Sie hier einen `actions:` Ordner und in `app.config.yaml` einen `runtimeManifest:`. Der häufigste Grund für das Hinzufügen einer solchen API ist der Aufruf von Workfront/Fusion-APIs, ohne dass dabei Browser-CORS aufgerufen wird.
   > Informationen zum Aufrufen von APIs finden Sie unter [Aufrufen von Workfront- und Fusion-APIs](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).
1. Fahren Sie fort [Festlegen einer stabilen Erweiterungs-ID](#set-a-stable-extension-id).

## Festlegen einer stabilen Erweiterungs-ID

Ihre Erweiterung erfordert eine eindeutige ID, die beide Frames gemeinsam haben.

Informationen zu Frames in Bezug auf benutzerdefinierte Erweiterungen finden Sie unter [Frames in einer Benutzeroberflächenerweiterung](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension).

1. `src/fusion-nav-organization-1/web-src/src/components/Constants.js` erstellen:

   ```js
   module.exports = {
     extensionId: 'my-fusion-extension'
   };
   ```

   Verwenden Sie denselben Wert überall dort, wo Ihr Code auf die Erweiterungs-ID verweist.
1. Fahren Sie fort [Widget registrieren](#register-your-widget).


## Widget registrieren

„Registrierung“ ist, wie der versteckte Hintergrund Rahmen teilt Fusion, was Ihre Erweiterung bietet. Sie deklarieren eine `dashboard.getWidget()` Methode, die den Titel Ihres Widgets und die URL seiner sichtbaren Benutzeroberfläche zurückgibt.

1. `src/fusion-nav-organization-1/web-src/src/components/ExtensionRegistration.js` erstellen.
Der wichtige Teil ist der `register(...)`:

   ```js
   import { register } from "@adobe/uix-guest";
   import metadata from "../../../../app-metadata.json";
   import { extensionId } from "./Constants";
   
   async function init() {
     await register({
       id: extensionId,
       metadata,
       methods: {
         dashboard: {
           getWidget() {
             return {
               id: extensionId,
               title: "My Fusion tool",        // shown on the Fusion nav button
               description: "What this tool does",
               url: "/index.html#/my-widget",  // route to your visible UI
               hideWidgetHeader: false          // false = Fusion shows the title
             };
           }
         }
       }
      });
   }
   
   init().catch(console.error);
   ```

   Wichtigste Punkte:

   * **`title`** ist die Bezeichnung, die Fusion auf die Navigationsschaltfläche setzt. Wenn `hideWidgetHeader` `false` ist, zeigt Fusion den Titel auch als Kopfzeile über der Benutzeroberfläche an.
   * **`url`** ist der Weg zu Ihrer *sichtbaren* Benutzeroberfläche innerhalb derselben App. Hier finden Sie eine Hash-Route (`#/my-widget`), die von Ihrem Frontend-Router (auf der nächsten Seite eingerichtet) verarbeitet wird. Sie muss auf die Komponente aufgelöst werden, die den Bildschirm rendert.
   * **`metadata`** stammt aus `app-metadata.json`, das der `generate-metadata`-Hook zum Zeitpunkt der Erstellung für Sie erstellt. Importieren Sie sie wie gezeigt.
   * Der `dashboard.getWidget` Methodenname ist der vereinbarte Vertrag mit Fusion-Aufrufen zur Ermittlung Ihres Widgets. Behalten Sie den `dashboard` Namespace und den `getWidget` bei.

Das Backend Ihrer Erweiterung ist jetzt abgeschlossen. Der nächste Schritt zum Erstellen der Benutzeroberfläche der Erweiterung.

Anweisungen zum Erstellen der Benutzeroberfläche finden Sie unter [Erstellen der benutzerdefinierten Erweiterungs-Benutzeroberfläche](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).
