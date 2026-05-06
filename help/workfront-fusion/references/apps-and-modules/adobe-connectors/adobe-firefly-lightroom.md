---
title: Adobe Firefly-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Adobe Firefly Lightroom verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 965cb643039be36eb3608cd801439a6a055974e4
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 16%

---

# Adobe Firefly Lightroom-Module

<!--add to tocs-->

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Adobe Firefly Lightroom verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Bevor Sie den Adobe Firefly Lightroom-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein gültiges Adobe Firefly Lightroom-Konto verfügen.

## Erstellen einer Verbindung mit Adobe Firefly Lightroom

So erstellen Sie eine Verbindung für Ihre Adobe Firefly Lightroom-Module:

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


## Adobe Firefly Lightroom-Module und ihre Felder

Beim Konfigurieren von Adobe Firefly Lightroom-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service werden möglicherweise auch zusätzliche Adobe Firefly Lightroom-Felder angezeigt. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [XMP zu Bild hinzufügen](#add-xmp-to-image)
* [Lightroom-Bearbeitungen anwenden](#apply-lightroom-edits)
* [Anwenden von Lightroom-Vorgaben](#apply-lightroom-presets)
* [Automatisch ausrichten](#auto-straighten)
* [Auto-Ton](#auto-tone)


### XMP zu Bild hinzufügen

Dieses Modul wendet eine XMP-basierte Lightroom-Vorgabe auf ein Bild an.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe Firefly Lightroom finden Sie unter <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Erstellen einer Verbindung mit Adobe Firefly Lightroom</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bild-URL</td> 
   <td>Geben Sie eine vordefinierte URL für das Bild ein, auf das Sie XMP anwenden möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Speichertyp</td> 
   <td>Wählen Sie den Speichertyp aus, in dem das Bild gespeichert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">XMP-Inhalte</td> 
   <td>Geben Sie den Text des XMP-Inhalts ein, den Sie dem Bild hinzufügen möchten, oder ordnen Sie ihn zu. Dies sollte eine XML-Zeichenfolge sein.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Ausrichtung</td> 
    <td>EXIF-Ausrichtung eingeben oder zuordnen, um sie auf das Bild anzuwenden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ausgabespeicher</td> 
    <td>Wählen Sie aus, wo die Ausgabedatei gespeichert werden soll. <p>Der interne Fusion-Speicher speichert das Bild nicht außerhalb des Szenarios, ermöglicht jedoch anderen Modulen im Szenario den Zugriff auf das Bild.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ausgabetyp</td> 
   <td>Wählen Sie den Dateityp für die Ausgabedatei.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Überschreiben</td> 
   <td>Wählen Sie Ja, wenn das Modul die Ausgabe überschreiben soll, wenn sie bereits vorhanden ist. Dies gilt nur für den Adobe Cloud-Speicher.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualität</td> 
   <td>Geben Sie die Qualität des Ausgabebilds ein oder mappen Sie sie. 1 ist die niedrigste und 12 die höchste Qualität. Dies gilt nur für JPEG-Dateien.</td> 
  </tr> 
 </tbody> 
</table>

### Lightroom-Bearbeitungen anwenden

Dieses Modul wendet eine oder mehrere Lightroom-Bearbeitungen auf ein Bild an. Die Bearbeitungen umfassen Belichtung, Kontrast, Schärfe und Sättigung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe Firefly Lightroom finden Sie unter <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Erstellen einer Verbindung mit Adobe Firefly Lightroom</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bild-URL</td> 
   <td>Geben Sie eine vordefinierte URL für das Bild ein, auf das Sie XMP anwenden möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Speichertyp</td> 
   <td>Wählen Sie den Speichertyp aus, in dem das Bild gespeichert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Optionen bearbeiten</td> 
   <td>Legen Sie alle Bearbeitungsoptionen fest, die Sie auf das Bild anwenden möchten.<p>Weitere Informationen zu Optionen finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/lightroom/api/#operation/applyEdits">Anwenden von Lightroom-Bearbeitungen</a> in der Dokumentation zur Adobe Firefly Lightroom-API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ausgabespeicher</td> 
    <td>Wählen Sie aus, wo die Ausgabedatei gespeichert werden soll. <p>Der interne Fusion-Speicher speichert das Bild nicht außerhalb des Szenarios, ermöglicht jedoch anderen Modulen im Szenario den Zugriff auf das Bild.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ausgabetyp</td> 
   <td>Wählen Sie den Dateityp für die Ausgabedatei.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Überschreiben</td> 
   <td>Wählen Sie Ja, wenn das Modul die Ausgabe überschreiben soll, wenn sie bereits vorhanden ist. Dies gilt nur für den Adobe Cloud-Speicher.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualität</td> 
   <td>Geben Sie die Qualität des Ausgabebilds ein oder mappen Sie sie. 1 ist die niedrigste und 12 die höchste Qualität. Dies gilt nur für JPEG-Dateien.</td> 
  </tr> 
 </tbody> 
</table>

### Anwenden von Lightroom-Vorgaben

Dieses Modul wendet eine oder mehrere XMP Lightroom-Vorgaben mithilfe der angegebenen XMP-Vorgabedateien auf das jeweilige Bild an.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe Firefly Lightroom finden Sie unter <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Erstellen einer Verbindung mit Adobe Firefly Lightroom</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bild-URL</td> 
   <td>Geben Sie eine vordefinierte URL für das Bild ein, auf das Sie XMP anwenden möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Speichertyp</td> 
   <td>Wählen Sie den Speichertyp aus, in dem das Bild gespeichert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Voreinstellungen</td> 
   <td>Klicken Sie für jede Vorgabe, die Sie anwenden möchten, auf <b>Element hinzufügen</b>, geben Sie die vordefinierte URL der Vorgabe ein und wählen Sie ihren Speichertyp aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ausgabespeicher</td> 
    <td>Wählen Sie aus, wo die Ausgabedatei gespeichert werden soll. <p>Der interne Fusion-Speicher speichert das Bild nicht außerhalb des Szenarios, ermöglicht jedoch anderen Modulen im Szenario den Zugriff auf das Bild.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ausgabetyp</td> 
   <td>Wählen Sie den Dateityp für die Ausgabedatei.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Überschreiben</td> 
   <td>Wählen Sie Ja, wenn das Modul die Ausgabe überschreiben soll, wenn sie bereits vorhanden ist. Dies gilt nur für den Adobe Cloud-Speicher.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualität</td> 
   <td>Geben Sie die Qualität des Ausgabebilds ein oder mappen Sie sie. 1 ist die niedrigste und 12 die höchste Qualität. Dies gilt nur für JPEG-Dateien.</td> 
  </tr> 
 </tbody> 
</table>

### Automatisch ausrichten

Dieses Modul richtet ein Bild automatisch gerade, indem es die Transformation Auto Upright anwendet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe Firefly Lightroom finden Sie unter <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Erstellen einer Verbindung mit Adobe Firefly Lightroom</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bild-URL</td> 
   <td>Geben Sie eine vordefinierte URL für das Bild ein, auf das Sie XMP anwenden möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Speichertyp</td> 
   <td>Wählen Sie den Speichertyp aus, in dem das Bild gespeichert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aufrecht-Modus</td> 
   <td>Wählen Sie den Typ des aufrechten Modus aus, den Sie verwenden möchten. Wenn Sie keinen Wert festlegen, wird automatisch ein entsprechender Modus bereitgestellt.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Zuschnitt beschränken</td> 
   <td>Wählen Sie aus, ob das gerade Bild abgeschnitten werden soll, um alle leeren Kanten zu entfernen.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">Ausgabespeicher</td> 
    <td>Wählen Sie aus, wo die Ausgabedatei gespeichert werden soll. <p>Der interne Fusion-Speicher speichert das Bild nicht außerhalb des Szenarios, ermöglicht jedoch anderen Modulen im Szenario den Zugriff auf das Bild.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ausgabetyp</td> 
   <td>Wählen Sie den Dateityp für die Ausgabedatei.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Überschreiben</td> 
   <td>Wählen Sie Ja, wenn das Modul die Ausgabe überschreiben soll, wenn sie bereits vorhanden ist. Dies gilt nur für den Adobe Cloud-Speicher.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualität</td> 
   <td>Geben Sie die Qualität des Ausgabebilds ein oder mappen Sie sie. 1 ist die niedrigste und 12 die höchste Qualität. Dies gilt nur für JPEG-Dateien.</td> 
  </tr> 
 </tbody> 
</table>


### Auto-Ton

Dieses Modul korrigiert Belichtung, Kontrast, Schärfe und Sättigung eines Bildes automatisch.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe Firefly Lightroom finden Sie unter <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Erstellen einer Verbindung mit Adobe Firefly Lightroom</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bild-URL</td> 
   <td>Geben Sie eine vordefinierte URL für das Bild ein, auf das Sie XMP anwenden möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Speichertyp</td> 
   <td>Wählen Sie den Speichertyp aus, in dem das Bild gespeichert werden soll.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Ausgabespeicher</td> 
    <td>Wählen Sie aus, wo die Ausgabedatei gespeichert werden soll. <p>Der interne Fusion-Speicher speichert das Bild nicht außerhalb des Szenarios, ermöglicht jedoch anderen Modulen im Szenario den Zugriff auf das Bild.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ausgabetyp</td> 
   <td>Wählen Sie den Dateityp für die Ausgabedatei.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Überschreiben</td> 
   <td>Wählen Sie Ja, wenn das Modul die Ausgabe überschreiben soll, wenn sie bereits vorhanden ist. Dies gilt nur für den Adobe Cloud-Speicher.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualität</td> 
   <td>Geben Sie die Qualität des Ausgabebilds ein oder mappen Sie sie. 1 ist die niedrigste und 12 die höchste Qualität. Dies gilt nur für JPEG-Dateien.</td> 
  </tr> 
 </tbody> 
</table>


