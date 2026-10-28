---
title: Debugging eines Szenarios
description: Mit dem Adobe Workfront Fusion DevTool können Sie Szenarien verstehen und Fehler beheben. Das DevTool fügt den Chrome Developer Tools ein zusätzliches Bedienfeld hinzu. Mithilfe dieses Debugger-Bedienfelds können Sie alle manuellen Ausführungen Ihres Szenarios überprüfen, alle ausgeführten Vorgänge überprüfen und die Details jedes durchgeführten API-Aufrufs anzeigen. Sie können sehen, welches Modul, welcher Vorgang oder welche einzelne Antwort den Fehler verursacht hat, und dieses Wissen verwenden, um Ihr Szenario zu verfeinern.
author: Becky
feature: Workfront Fusion
exl-id: 34215370-27e3-4c28-8bd1-a16268900b86
TQID: 'https://experienceleague.adobe.com/7NXYVXxbQvgKnqvRUNV-ySBApe9kl-Kn57sSKCh4NLE'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '1962'
ht-degree: 5%
---
# Debugging eines Szenarios

Das Adobe Workfront Fusion-DevTool hilft Ihnen, Szenarien zu verstehen und Fehler zu beheben. Mit dem DevTool können Sie alle manuellen Ausführungen Ihres Szenarios überprüfen, alle ausgeführten Vorgänge überprüfen und die Details jedes durchgeführten API-Aufrufs anzeigen. Sie können sehen, welches Modul, welcher Vorgang oder welche einzelne Antwort den Fehler verursacht hat, und dieses Wissen verwenden, um Ihr Szenario zu verfeinern.

>[!NOTE]
>
>Die Protokollierung im Debugger-Bedienfeld ist für vertrauliche Szenarien, automatische Ausführungen und erfolgreiche Vorgänge eingeschränkt oder nicht verfügbar.

>[!NOTE]
>
>In der neuen -Version sind mehrere DevTool-Tools im Szenario-Editor integriert, sodass Sie sie verwenden können, ohne das DevTool zu öffnen:
>
>| Tool | Wo Sie sie in der neuen -Version finden |
>| ---------- | ---------- |
>| Abrufen von App-Metadaten | Klicken Sie mit der rechten Maustaste auf ein Modul und wählen Sie **App-Metadaten**. |
>| Zuordnung kopieren | Klicken Sie mit der rechten Maustaste auf das Quellmodul, wählen Sie **Zuordnung kopieren** aus und fügen Sie es dann in ein kompatibles Modul ein. |
>| Filter kopieren | Klicken Sie mit der rechten Maustaste auf den gefilterten Link, wählen Sie **Filter kopieren** und fügen Sie ihn dann in einen anderen Link ein. |
>| Modulnamen kopieren | Klicken Sie mit der rechten Maustaste auf ein Modul und wählen **Modulnamen kopieren** oder **Modulnamen einfügen**. |
>| Swapverbindung | Öffnen Sie Suchen und Ersetzen und verwenden Sie dann die Registerkarte **Verbindung** . |
>| Swap-Variable | Öffnen Sie Suchen und Ersetzen und verwenden Sie dann die Registerkarte **Variable** . |
>| Quelle neu zuordnen | Öffnen Sie Suchen und Ersetzen und verwenden Sie dann die Registerkarte **Source**. |
>
>Diese Tools sind auch weiterhin auf der Registerkarte **Tools** des DevTools verfügbar, zusammen mit dem Modul Fokus , Module nach Zuordnung suchen und Base 64 . Sie können auch die `base64()`- und Binärkonvertierungsfunktionen in Zuordnungen verwenden.
>
>Sie können Anfrage- und Antwortdetails auch direkt aus dem [Live-Protokoll](/help/workfront-fusion/manage-scenarios/live-trail.md) und dem Ausführungsverlauf im Szenario-Editor anzeigen. Weitere Informationen zum Suchen und Ersetzen finden Sie unter [Variablen, Quellen und Verbindungen in einem Szenario suchen und &#x200B;](/help/workfront-fusion/manage-scenarios/find-and-replace.md).
<!-- BECKY CHECK ME: DevTool screenshots (10/27/26) show all ten tools still on the Tools tab, so this note now says the seven built-in tools are available in both places. The release notes implied only Focus a module, Find modules by mapping, and Base 64 would remain. Confirm after release whether the other seven are removed from the DevTool, and update this note and the Tools section if so.  -->
<!-- BECKY CHECK ME: note added from the 10/23/26 release notes; the DevTool is NOT being removed. This article still needs a fuller restructure (new/classic split for the seven tools, Live Trail section or separate article). Confirm the menu labels. -->

Eine Videoeinführung und exemplarische Anleitung für das Fusion DevTool finden Sie unter

* [Fusion-Entwicklungstool](https://video.tv.adobe.com/v/3427031/){target=_blank}
* [Anleitung für Entwickler](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/fusion/troubleshooting-and-error-handling/dev-tool-walkthrough.html?lang=en)

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Ein beliebiges Adobe Workfront Workflow- und Adobe Workfront Automation and Integration-Paket</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Zugriff auf DevTool

Wenn Sie Fusion in der Adobe Unified Shell verwenden oder auf das neue Fusion-Erlebnis aktualisiert haben, können Sie über den Szenario-Editor auf das DevTool zugreifen.

### Zugriff auf das DevTool in der neuen -Version

1. Wechseln Sie zum Szenario-Editor für das Szenario, das Sie debuggen möchten.

   Den Szenario-Editor finden Sie unter [Der Szenario-Editor](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Klicken Sie auf das Dreipunkt-Symbol im Bereich Steuerelemente und wählen Sie dann **DevTool** aus.

Oder:

1. Wechseln Sie zum Szenario-Editor für das Szenario, das Sie debuggen möchten.
1. Klicken Sie mit der rechten Maustaste in einen leeren Bereich der Seite (nicht auf ein Modul).
1. Wählen Sie **DevTool öffnen**.

Das DevTool wird in einem Bedienfeld unter der Arbeitsfläche geöffnet.

<!-- BECKY CHECK ME: new-experience access steps from your 10/27/26 notes (three-dot menu in Controls, or right-click). Confirm the menu label ('DevTool') and the 'panel below the canvas' description, and add a screenshot. I assumed the Helper tools icon steps below apply to the classic experience only; confirm. -->

### Zugriff auf das DevTool in der klassischen -Version

1. Klicken Sie auf **Helper-Tools** ![Helper-Tools](assets/debugger-icon.png) unten auf dem Bildschirm.

Oder:

1. Wechseln Sie zum Szenario-Editor für das Szenario, das Sie debuggen möchten.

   Den Szenario-Editor finden Sie unter [Der Szenario-Editor](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Klicken Sie mit der rechten Maustaste in einen leeren Bereich der Seite (nicht auf ein Modul).
1. Wählen Sie **DevTool öffnen**.

## Verwenden des Workfront Fusion-Dev-Tools

Workfront Fusion Devtool ist in drei Hauptabschnitte unterteilt, sowie einen Hilfe-Link. Sie finden diese im linken Bereich Ihres DevTool-Fensters.

* [Live-Stream](#live-stream)
* [Szenario-Debugger](#scenario-debugger)
* [Tools](#tools)
* **DevTool-Hilfe**: Klicken Sie auf das Fragezeichen-Symbol, um den Artikel zum DevTool zu öffnen.

<!-- BECKY CHECK ME: the DevTool left panel now has a fourth item, 'DevTool help' (question mark icon), per your 10/27/26 screenshots. Confirm the label, that it opens this article or another one, and whether to apply this to the classic experience too. Retake the left-panel screenshot. -->

### Live-Stream

Live Stream zeigt an, was im Hintergrund passiert, wenn Sie in Ihrem Szenario einmal auf Ausführen klicken.

<!-- BECKY CHECK ME: HOLD: in the new experience, Live Stream shows a 'no events available' message even while a scenario is running, which may be a bug. No updates have been made to this section. Re-test after release before changing anything here. If it is intended behavior, this section may need to point to Live Trail instead. -->

1. Klicken Sie auf das **[!UICONTROL Live-Stream]**-Symbol ![Live-Stream-](assets/live-stream-icon.png)), um den Abschnitt Live-Stream zu öffnen.
1. Führen Sie einen der folgenden Schritte aus:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Aktion</th> 
      <th>Anleitung</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td role="rowheader">Anfrageinformationen anzeigen</td> 
      <td> <p>Sie können die folgenden Informationen für jedes Modul in Ihrem Szenario anzeigen</p> 
       <ul> 
        <li> <p>Anfragekopfzeilen (API-Endpunkt-URL, HTTP-Methode, Uhrzeit und Datum, an dem die Anfrage aufgerufen wurde, Anfragekopfzeilen und Abfragezeichenfolge)</p> </li> 
        <li> <p>Anfragetext</p> </li> 
        <li> <p>Antwort-Header</p> </li> 
        <li> <p>Antworttext</p> </li> 
       </ul> <p>Um diese Informationen anzuzeigen, klicken Sie auf die entsprechende Registerkarte im rechten Bedienfeld des Workfront Fusion DevTools.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Ereignisse nach Inhalt suchen</p> </td> 
      <td> <p>Geben Sie den Suchbegriff in das Suchfeld im linken Bereich des Workfront Fusion DevTools ein, um nur Anfragen anzuzeigen, die den Suchbegriff enthalten.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Liste der Anfragen löschen </p> </td> 
      <td> <p>Klicken Sie auf das Papierkorb-Symbol in der oberen rechten Ecke des linken Bedienfelds von DevTool, um die Liste der Anfragen zu löschen, die vom Workfront Fusion DevTool aufgezeichnet wurden. </p> </td> 
     </tr> 
     <!--
     <tr>
      <td role="rowheader"> <p>Enable Console Logging</p> </td> 
      <td> <p>Click the computer icon <img src="assets/console-computer-icon.png"> in the top-right corner of the Devtool's left panel.</p> <p>Logging in the console is enabled when the computer icon is green.</p> </td> 
     </tr>
     -->
     <tr> 
      <td role="rowheader"> <p>Rufen Sie die Anfrage im rohen JSON-Format oder cURL ab.</p> </td> 
      <td> 
       <ul> 
        <li> <p><strong>Roh-JSON</strong> </p> <p>Klicken Sie auf <strong>[!UICONTROL Copy RAW]</strong> in der oberen rechten Ecke des rechten Fensterbereichs von Devtool.</p> </li> 
        <li> <p><strong>cURL</strong> </p> <p>Klicken Sie auf <strong>[!UICONTROL Copy cURL]</strong> in der oberen rechten Ecke des rechten Bereichs des Devtools.</p> </li> 
       </ul> </td> 
     </tr> 
    </tbody> 
   </table>

### Szenario-Debugger

>[!NOTE]
>
>Um schnell von einem fehlerhaften Szenario zum Debugger zu wechseln, können Sie auf **Details abrufen** in der Fehlermeldung in der Modulausgabe klicken.
>
>![Erhalten Sie Details in der Modulausgabe](assets/go-to-debugger.png)

Der Szenario-Debugger ist für komplexere Szenarien nützlich. Es zeigt den Verlauf der Szenario-Ausführungen an und ermöglicht es Ihnen, Module anhand ihres Namens oder ihrer ID zu durchsuchen.

1. Klicken Sie auf das Symbol **[!UICONTROL Szenario-]**![Debugger-Symbol](assets/scenario-debugger-icon.png), um den Szenario-Debugger zu öffnen.

   Der Szenario-Debugger listet die Module in Ihrem Szenario auf. Jedes Modul zeigt seinen Namen, die App und die Aktion sowie ein nummeriertes Badge mit der Modul-ID an.

1. (Optional) Geben Sie den Suchbegriff (Name oder Modul-ID) in das Feld **Suchmodule nach Name oder ID** ein.
1. Klicken Sie auf den Modulnamen.

   Die Zyklen der letzten Ausführung des Moduls werden neben der Modulliste aufgeführt. Wenn das Modul keine Ausführungsdaten hat, zeigt der Szenario-Debugger &quot;**Ergebnis gefunden“**.

1. Erweitern Sie einen Zyklus und klicken Sie dann auf einen Vorgang.

   Jede Operation zeigt an, ob sie erfolgreich war und wie lange sie dauerte, z **B. (Operation 1** mit einer Dauer von 0 ms.

1. Überprüfen Sie die Details der Anfrage. Verwenden Sie die Registerkarten, um Folgendes anzuzeigen:

   * **Anfrage-Header**: Die API-Endpunkt-URL, die HTTP-Methode, bei der die Anfrage aufgerufen wurde, und die Anfrage-Header.
   * **Anfrageinhalt**
   * **Antwort-Header**
   * **Antworttext**

1. (Optional) Um die Anfrage zu kopieren, klicken Sie auf **Roh kopieren** oder **cURL kopieren**.

<!-- BECKY CHECK ME: Scenario Debugger steps expanded from your 10/27/26 new-experience DevTool screenshots. Confirm: (1) the 'Search modules by Name or ID' label; (2) that the module list sub-labels, badge (module ID), cycle/operation layout, and 'No Result found' state are described correctly; (3) the tab names, since Response Body was partly hidden behind the Copy buttons in the screenshot; (4) whether Copy RAW and Copy cURL copy the request only or the request and response; (5) whether the classic experience's Scenario Debugger looks the same, or this needs a new/classic split. The screenshot also shows a collapsed 'Live trail' tab with an event count on the right edge of the editor; see the Live Trail article. Retake the Scenario Debugger screenshots. -->

### Tools

Das Workfront Fusion DevTool bietet Tools, die die Einrichtung Ihres Szenarios erleichtern.

1. Klicken Sie auf **[!UICONTROL Tools]**-Symbol ![Konsolen-Tools-Symbol](assets/console-tools-icon.png), um die Tools zu öffnen.
1. (Optional) Um ein Tool zu finden, geben Sie seinen Namen in das Feld **Tool nach Namen suchen** ein.
1. Wählen Sie das gewünschte Tool aus
1. Konfigurieren Sie die Felder wie unten beschrieben.
1. Klicken Sie auf **[!UICONTROL Ausführen]**.

Bis Sie ein Tool auswählen, werden Sie auf der rechten Seite des Bedienfelds aufgefordert, eines auszuwählen. Ein Link am unteren Rand der Registerkarte Tools führt Sie zum Artikel über das DevTool.

<!-- BECKY CHECK ME: added from your 10/27/26 screenshots: the 'Search tool by name' field, the select-a-tool prompt, and the link to the DevTool article. Confirm the field label and link destination; retake the Tools screenshot. -->

Tools und ihre Felder:

* [Fokussieren eines Moduls](#focus-a-module)
* [Module nach Zuordnung suchen](#find-modules-by-mapping)
* [Abrufen von App-Metadaten](#get-app-metadata)
* [Zuordnung kopieren](#copy-mapping)
* [Filter kopieren](#copy-filter)
* [Modulnamen kopieren](#copy-module-name)
* [Wechseln der Verbindung](#swap-connection)
* [Swap-Variable](#swap-variable)
* [Base 64](#base-64)
* [Source neu zuordnen](#remap-source)

#### [!UICONTROL Fokussieren eines Moduls]

Öffnet die Einstellungen des angegebenen Moduls nach ID.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Modul-ID]</td>
        <td>Geben Sie die ID des Moduls ein, um dessen Einstellungen zu öffnen.</td>
    </tr>
</table>

#### [!UICONTROL Module nach Zuordnung suchen]

Ermöglicht die Suche nach den Modulwerten für einen bestimmten Begriff. Die Ausgabe enthält IDs von Modulen, die den gesuchten Begriff enthalten.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Schlüsselwort]</td> 
   <td> <p> Geben Sie den Begriff ein, nach dem Sie suchen möchten. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nur Werte verwenden]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um nur in den Werten der Modulfelder zu suchen.</p> <p>Deaktivieren Sie diese Option, um auch nach den Namen der Modulfelder zu suchen.</p> <p>Die Suche wird über die Parameter Name und Titel durchgeführt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Abrufen von App-Metadaten]

Ruft Metadaten der App anhand des Modulnamens oder der ID der App ab. Dies ist beispielsweise nützlich, wenn Sie die Version der in Ihrem Szenario verwendeten App kennen müssen.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source-Modul]</td>
        <td>Wählen Sie das Modul aus, für das Sie Metadaten abrufen möchten.</td>
    </tr>
</table>

#### [!UICONTROL Zuordnung kopieren]

Kopiert Werte aus dem Quellmodul in das Zielmodul.

>[!CAUTION]
>
>Stellen Sie sicher, dass Sie die richtigen Quell- und Zielmodule festlegen. Wenn Sie einen anderen Modultyp auswählen, werden die Werte im Zielmodul gelöscht.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Modul]</td> 
   <td> <p> Wählen Sie das Modul aus oder geben Sie die ID des Moduls ein, aus dem Sie die Feldwerte kopieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target-Modul]</p> </td> 
   <td> <p>Wählen Sie das Modul aus oder geben Sie die ID des Moduls ein, in das Sie die Werte des Quellmoduls einfügen möchten.</p> <p>Wichtig: Die Werte im Zielmodul werden überschrieben.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Filter kopieren]

Kopiert die Filtereinstellungen vom Quell- zum Zielmodul.

>[!NOTE]
>
>Die Kopieraktion wird für den Filter ausgeführt, der auf der linken Seite des ausgewählten Moduls platziert ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Modul]</td> 
   <td> <p> Wählen Sie das Modul aus oder geben Sie die ID des Moduls ein, aus dem Sie Filterwerte kopieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target-Modul]</p> </td> 
   <td> <p>Wählen Sie das Modul aus oder geben Sie die ID des Moduls ein, in das Sie die Filterwerte aus dem Quellmodul einfügen möchten.</p> <p>Wichtig: Die Werte im Zielmodul werden überschrieben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Einstellung der Ausweichroute beibehalten]</p> </td> 
   <td> <p>Der Quellfilter wird als Fallback-Route festgelegt. Aktivieren Sie diese Option, um auch festzulegen, dass der Zielfilter als Ausweichroute festgelegt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Modulnamen kopieren]

Kopiert den Namen des ausgewählten Moduls in die Zwischenablage.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modul] </td> 
   <td> <p>Wählen Sie das Modul aus, dessen Namen Sie kopieren möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Wechseln der Verbindung]

Dupliziert eine Verbindung vom Quellmodul zu jedem Modul im Szenario derselben App.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source-Modul]</td>
        <td>Wählen Sie das Modul aus oder geben Sie die ID des Moduls ein, aus dem Sie die Verbindung duplizieren möchten.</td>
    </tr>
</table>

#### [!UICONTROL Swap-Variable]

Sucht im Szenario nach angegebenen Variablen und ersetzt sie durch eine neue Variable.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable zum Suchen]</td> 
   <td> <p> Suchen Sie die Variable Pille, die Sie aus dem Variablenmodul in Ihrem Szenario ersetzen möchten, und kopieren Sie sie in dieses Feld ([!UICONTROL Variable zum Suchen]). Im Feld wird sie mit doppelten geschweiften Klammern angezeigt. Beispiel: <code>&#123;&#123;5.value&#125;&#125;</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL durch] ersetzen</p> </td> 
   <td> <p>Suchen Sie im Variablenmodul in Ihrem Szenario die Variable, mit der Sie die Variable ersetzen möchten, und kopieren Sie sie in dieses Feld ([!UICONTROL Variable zum Suchen]). Im Feld wird sie mit doppelten geschweiften Klammern angezeigt. Beispiel: <code>&#123;&#123;5.value&#125;&#125;</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Modul]</p> </td> 
   <td> <p>Wählen Sie das Variablenmodul aus, in dem Sie die Variable ersetzen möchten. Wenn kein Modul ausgewählt ist, wird die Variable im gesamten Szenario ersetzt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Base 64]

Ermöglicht die Kodierung der eingegebenen Daten in Base64 oder die Dekodierung von Base64. Einige Anfragen sind mit Base64 codiert. Dieses Tool kann nützlich sein, wenn Sie in der kodierten Anfrage nach bestimmten Daten suchen möchten.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Vorgang] </td> 
   <td> <p>Wählen Sie aus, ob die Daten aus dem Feld [!UICONTROL Raw Data] in Base64 kodiert oder Base64 in Raw Data dekodiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Rohdaten]</p> </td> 
   <td> <p> Geben Sie die Daten, die Sie für Base64 codieren möchten, oder Base64 ein, wenn Sie für Rohdaten decodieren möchten, je nach der im Feld [!UICONTROL -Vorgang] oben ausgewählten Option.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Source neu zuordnen]

Ermöglicht das Ändern der Zuordnungsquelle von einem Modul zu einem anderen.

Zunächst müssen Sie das Modul, das Sie als Quellmodul verwenden möchten, zur Route in Ihrem Szenario hinzufügen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Modul] </td> 
   <td> <p> Wählen Sie das Modul aus, das Sie als Zuordnungsquelle für andere Module in Ihrem Szenario ersetzen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target-Modul]</p> </td> 
   <td> <p>Wählen Sie das Modul aus, das Sie als neue Zuordnungsquelle verwenden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Modul zum Bearbeiten]</p> </td> 
   <td> <p>Wählen Sie das Modul aus, für das Sie die Zuordnung ändern möchten, wenn Sie die Zuordnung nicht im gesamten Szenario ändern möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>
