---
title: Adobe Express-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Adobe Express verwenden.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: eab04db9a38020ed973f98d7f8f290ccd183251c
workflow-type: tm+mt
source-wordcount: '1372'
ht-degree: 17%

---

# Adobe Express-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Adobe Express verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: keine Workfront Fusion-Lizenz erforderlich</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Bevor Sie den Adobe Express-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein gültiges Adobe Express-Konto verfügen.

## Erstellen einer Verbindung mit Adobe Express

So erstellen Sie eine Verbindung für Ihre Adobe Express-Module:

1. Klicken Sie in einem beliebigen Modul **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Verbindungsname</td>
        <td>
          <p>Geben Sie einen Namen für die Verbindung ein.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Umgebung</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td>
        </tr>
        <tr>
        <td role="rowheader">Typ</td>
        <td>Wählen Sie aus, ob eine Verbindung zu einem Service-Konto oder einem persönlichen Konto hergestellt werden soll.</td>
        </tr>
        <tr>
        <td role="rowheader">Client-ID</td>
        <td>Geben Sie Ihre Adobe-Client-ID ein. Diese finden Sie im Abschnitt Anmeldedaten des Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Client-Geheimnis</td>
        <td>Geben Sie Ihr Adobe-Client-Geheimnis ein. Diese finden Sie im Abschnitt Anmeldedaten des Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Verbindung zu speichern und zum Modul zurückzukehren.


## Adobe Express-Module und ihre Felder

Beim Konfigurieren von Adobe Express-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service können zusätzlich dazu weitere Adobe Express-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Aktionen

#### Exportieren von Ausgabedarstellungen

Dieses Modul exportiert ein Dokument in das JPG- oder PNG-Format. Sie kann vorsignierte URLs für die Seitenausgabedarstellungen bereitstellen, die vier Stunden gültig sind.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Express finden Sie unter <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Express</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dokument</td> 
   <td>Wählen Sie das Dokument aus, für das Sie eine Ausgabedarstellung exportieren möchten.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Seitenzahlen</td> 
   <td>Geben Sie die Seitenzahlen ein, die Sie in die Ausgabedarstellung einbeziehen möchten, oder mappen Sie sie. Eine kommagetrennte Zeichenfolge von Seitenzahlen, für die die Ausgabedarstellungsanfrage gestellt wird. Beispiel: „1,2,3“. Seitenbereiche können ebenfalls angegeben werden. Beispiel: „1-3“ umfasst die Seiten 1, 2 und 3. Ein weiteres Beispiel ist „1,3-5“, das die Seiten 1, 3, 4 und 5 umfasst. „1-" kann verwendet werden, um alle Seiten anzugeben, während „5-" Seite 5 bis zur letzten Seite anzeigt. Wenn sie nicht angegeben wird, wird standardmäßig die erste Seite berücksichtigt. Seitenzahlen beginnen bei 1.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Ausgabedarstellungstyp</td> 
   <td>Wählen Sie den Typ der Ausgabedarstellung aus, die Sie exportieren möchten: Bild, Video oder PDF</td> 
  </tr>
  <tr> 
   <td role="rowheader">Format</td> 
   <td>Wählen Sie das Dateiformat für Ihre Ausgabedarstellung aus.</td> 
  </tr>
  <tr> 
   <td role="rowheader">PDF-Typ</td> 
   <td>Wenn Sie eine PDF exportieren, wählen Sie aus, ob eine standardmäßige oder eine druckbare PDF exportiert werden soll.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Größe</td> 
   <td>Wenn Sie ein Bild oder Video exportieren, geben Sie die Größe der längsten Seite in Pixel ein bzw. mappen Sie diese. Das Seitenverhältnis wird beibehalten. Für Bilder wird eine Mindestgröße von 1 Pixel und eine maximale Größe von 8.192 Pixel unterstützt. Wenn nicht angegeben, wird die Standardgröße der Seite berücksichtigt.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Herunterladen einzelner PDF-Dateien</td> 
   <td>Wenn Sie eine PDF exportieren, wählen Sie aus, ob die Seiten als separate PDF-Dateien heruntergeladen werden sollen. Wenn „true“, wird jede Seite als eigene PDF-Datei heruntergeladen. Bei „false“ werden alle Seiten in einer PDF-Datei zusammengefasst.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Konfiguration</td> 
   <td>Wenn Sie eine PDF exportieren, wählen Sie aus, ob die PDF in der Standard- oder Druckkonfiguration verwendet werden soll.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Phase der Barrierefreiheit</td> 
   <td>Wenn Sie eine standardmäßige PDF exportieren, wählen Sie aus, ob Barrierefreiheits-Tags in die PDF aufgenommen werden sollen.</td> 
  </tr>
  <tr> 
   <td role="rowheader">bluten</td> 
   <td>Wenn Sie eine Druck-PDF exportieren, wählen Sie aus, ob Anschnitteeinstellungen in den Export einbezogen werden sollen</td> 
  </tr>
  <tr> 
   <td role="rowheader">Anzapfungseinstellungen &gt; Betrag</td> 
   <td>Geben Sie den Betrag des Anschnitts ein.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Anzapfungseinstellungen &gt; Einheiten</td> 
   <td>Wählen Sie aus, ob sich der Betrag auf Zoll oder Millimeter bezieht.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Beschneiden</td> 
   <td>Wenn Sie eine Druck-PDF exportieren, legen Sie fest, ob Zuschnitteinstellungen in den Export einbezogen werden sollen</td> 
  </tr>
  <tr> 
   <td role="rowheader">Einstellungen für das Zuschneiden &gt; Betrag</td> 
   <td>Geben Sie den Betrag des Zuschnittspielraums ein.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Einstellungen für das Zuschneiden &gt; Einheiten</td> 
   <td>Wählen Sie aus, ob sich der Betrag auf Zoll oder Millimeter bezieht.</td> 
  </tr>
 </tbody> 
</table>

#### Varianten erzeugen

Dieses Modul erstellt eine Dokumentvariante basierend auf den bereitgestellten Eingabeparametern. Nach der Verarbeitung speichert es das generierte Dokument vorübergehend und stellt es dem Benutzer in einem bestimmten Ordner zur Verfügung. Das Dokument bleibt 30 Tage lang verfügbar. Danach wird es automatisch entfernt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Express finden Sie unter <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Express</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dokument</td> 
   <td>Wählen Sie das Dokument aus, für das Sie Varianten generieren möchten.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Seitenzahlen</td> 
   <td>Geben Sie die Seitenzahlen ein, die Sie in die Ausgabedarstellung einbeziehen möchten, oder mappen Sie sie. Eine kommagetrennte Zeichenfolge von Seitenzahlen, für die die Variantenanforderung ausgeführt wird. Beispiel: „1,2,3“. Seitenbereiche können ebenfalls angegeben werden. Beispiel: „1-3“ umfasst die Seiten 1, 2 und 3. Ein weiteres Beispiel ist „1,3-5“, das die Seiten 1, 3, 4 und 5 umfasst. „1-" kann verwendet werden, um alle Seiten anzugeben, während „5-" Seite 5 bis zur letzten Seite anzeigt. Wenn sie nicht angegeben wird, wird standardmäßig die erste Seite berücksichtigt. Seitenzahlen beginnen bei 1.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Bevorzugter Dokumentname.</td> 
   <td>Geben Sie einen Namen für das neue Dokument ein oder ordnen Sie ihn zu. Wenn Sie keinen Namen angeben oder der Name bereits verwendet wird, generiert das System einen eindeutigen Namen.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Projekt-ID</td> 
   <td>Geben Sie die ID des Projekts ein, in dem die Varianten gespeichert werden.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Andere Felder</td> 
   <td>Werte für andere Felder eingeben. Die verfügbaren Felder basieren auf dem ausgewählten Dokument.</td> 
  </tr>
 </tbody> 
</table>


### Suchvorgänge

#### Abrufen getaggter Dokumente

Dieses Modul ruft eine Liste mit getaggten Dokumenten zusammen mit relevanten Metadaten ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Express finden Sie unter <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Express</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Startindex</td> 
   <td>Geben Sie den Startindex der Paginierung ein oder ordnen Sie ihn zu. Verwenden Sie dies, wenn Sie eine andere Ergebnisliste abgerufen haben und diese Liste fortsetzen möchten. Der Standardindex ist 0.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Ergebnissen ein, die das Modul für jeden Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sortieren nach</td> 
   <td>Wählen Sie das Attribut aus, nach dem Sie die Ergebnisse sortieren möchten.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Richtung</td> 
   <td>Wählen Sie aus, ob die Ergebnisse auf- oder absteigend sortiert werden sollen.</td> 
  </tr>
 </tbody> 
</table>

#### Dokumentdetails abrufen

Dieses Modul ruft Details zu den Seiten und mit Tags versehenen Elementen innerhalb eines bestimmten Dokuments ab. Es wird eine paginierte Liste der Seiten des Dokuments und Metadaten zu jeder Seite zurückgegeben. Wenn das Dokument getaggte Elemente enthält, enthält die API die entsprechenden Details, wie Größe und Position. Wenn das Dokument keine getaggten Elemente enthält, wird ein leeres -Array zurückgegeben. Die Antwort enthält Informationen zur Paginierung, die Benutzenden beim Navigieren auf den Seiten des Dokuments helfen. Es können maximal 10 Seiten in einem Zyklus zurückgegeben werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Express finden Sie unter <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Express</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dokument</td> 
   <td>Wählen Sie das Dokument aus, für das Sie Seiten und Details zurückgeben möchten.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Start Seite</td> 
   <td>Geben Sie die Seitennummer der ersten Seite ein, von der Details abgerufen werden, oder mappen Sie sie.</td>

#### Abrufen des Status eines Vorgangs

Dieses Modul ruft den Status eines Auftrags anhand seiner Auftrags-ID ab. Je nach Vorgangstyp kann die Antwort auftragsspezifische Details enthalten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Express finden Sie unter <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Express</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Auftrags-ID</td> 
   <td>Geben Sie die ID des Auftrags ein, für den Sie Details abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr>

