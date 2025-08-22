---
title: Debuggen eines Szenarios
description: Mit dem Adobe Workfront Fusion DevTool können Sie Szenarien verstehen und Fehler beheben. Das DevTool fügt den Chrome Developer Tools ein zusätzliches Bedienfeld hinzu. Mithilfe dieses Debugger-Bedienfelds können Sie alle manuellen Ausführungen Ihres Szenarios überprüfen, alle ausgeführten Vorgänge überprüfen und die Details jedes durchgeführten API-Aufrufs anzeigen. Sie können sehen, welches Modul, welcher Vorgang oder welche einzelne Antwort den Fehler verursacht hat, und dieses Wissen verwenden, um Ihr Szenario zu verfeinern.
author: Becky
feature: Workfront Fusion
exl-id: 34215370-27e3-4c28-8bd1-a16268900b86
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1483'
ht-degree: 0%

---

# Debuggen eines Szenarios

Das Adobe Workfront Fusion-DevTool hilft Ihnen, Szenarien zu verstehen und Fehler zu beheben. Mit dem DevTool können Sie alle manuellen Ausführungen Ihres Szenarios überprüfen, alle ausgeführten Vorgänge überprüfen und die Details jedes durchgeführten API-Aufrufs anzeigen. Sie können sehen, welches Modul, welcher Vorgang oder welche einzelne Antwort den Fehler verursacht hat, und dieses Wissen verwenden, um Ihr Szenario zu verfeinern.

>[!NOTE]
>
>Die Protokollierung im Debugger-Bedienfeld ist für vertrauliche Szenarien, automatische Ausführungen und erfolgreiche Vorgänge eingeschränkt oder nicht verfügbar.

Eine Videoeinführung und exemplarische Anleitung für das Fusion DevTool finden Sie unter

* [Fusion-Entwicklungstool](https://video.tv.adobe.com/v/3427031/){target=_blank}
* [Anleitung zu Devtool](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/fusion/troubleshooting-and-error-handling/dev-tool-walkthrough.html?lang=de)

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz</td> 
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Plan für [!UICONTROL Select] oder [!UICONTROL Prime] Workfront: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>[!UICONTROL Ultimate] Workfront-Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Unternehmen sein.</p>
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Team sein.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Zugriff auf DevTool

Wenn Sie Fusion in der Adobe Unified Shell verwenden oder auf das neue Fusion-Erlebnis aktualisiert haben, können Sie über den Szenario-Editor auf das DevTool zugreifen.

1. Klicken Sie auf **Helper-Tools** ![Helper-Tools](assets/debugger-icon.png) unten auf dem Bildschirm.

Oder:

1. Wechseln Sie zum Szenario-Editor für das Szenario, das Sie debuggen möchten.

   Den Szenario-Editor finden Sie unter [Der Szenario-Editor](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Klicken Sie mit der rechten Maustaste in einen leeren Bereich der Seite (nicht auf ein Modul).
1. Wählen Sie **DevTool öffnen**.

## Verwenden des Workfront Fusion-Dev-Tools

Workfront Fusion Devtool ist in drei Hauptabschnitte unterteilt. Sie finden diese im linken Bereich Ihres DevTool-Fensters.

* [Live-Stream](#live-stream)
* [Szenario-Debugger](#scenario-debugger)
* [Tools](#tools)

### Live-Stream

Live Stream zeigt an, was im Hintergrund passiert, wenn Sie in Ihrem Szenario einmal auf Ausführen klicken.

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
     <!--<tr> 
      <td role="rowheader"> <p>Enable Console Logging</p> </td> 
      <td> <p>Click the computer icon <img src="assets/console-computer-icon.png"> in the top-right corner of the Devtool's left panel.</p> <p>Logging in the console is enabled when the computer icon is green.</p> </td> 
     </tr>-->
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

Der Szenario-Debugger ist für komplexere Szenarien nützlich. Es zeigt den Verlauf der Szenario-Ausführungen an und ermöglicht es Ihnen, Module anhand ihres Namens oder ihrer ID zu durchsuchen.

1. Klicken Sie auf das Symbol **[!UICONTROL Szenario-]**![Debugger-Symbol](assets/scenario-debugger-icon.png), um den Szenario-Debugger zu öffnen.
1. (Optional) Geben Sie den Suchbegriff (Name oder Modul-ID) in das Suchfeld ein.
1. Klicken Sie auf den Modulnamen.
1. Klicken Sie auf den Vorgang, um die Anfragedetails anzuzeigen.

### Tools

Das Workfront Fusion DevTool bietet Tools, die die Einrichtung Ihres Szenarios erleichtern.

1. Klicken Sie auf **[!UICONTROL Tools]**-Symbol ![Konsolen-Tools-Symbol](assets/console-tools-icon.png), um die Tools zu öffnen.
1. Wählen Sie das gewünschte Tool aus
1. Konfigurieren Sie die Felder wie unten beschrieben.
1. Klicken Sie auf **[!UICONTROL Ausführen]**.

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
   <td role="rowheader">[!UICONTROL -Modul] </td> 
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
   <td role="rowheader"> <p>[!UICONTROL -Modul]</p> </td> 
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
