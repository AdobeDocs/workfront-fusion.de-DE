---
title: CloudConvert-Module
description: CloudConvert-Module
author: Becky
feature: Workfront Fusion
exl-id: 52c4d18a-8bee-44d6-9a2c-cc9e157e1dde
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '3161'
ht-degree: 0%

---

# [!DNL CloudConvert]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die CloudConvert verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden. Mit den [!DNL CloudConvert]-Modulen können Sie Aufträge und Aufgaben überwachen und verwalten sowie Dateien in Ihr [!DNL CloudConvert]-Konto importieren und exportieren.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## CloudConvert-API-Informationen

Der CloudConvert-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.cloudconvert.com/v2/</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v2.14.22</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL CloudConvert] mit Workfront Fusion {#connect-cloudconvert-to-workfront-fusion}

Um Ihr [!DNL CloudConvert]-Konto mit Workfront Fusion zu verbinden, müssen Sie den API-Schlüssel von Ihrem [!DNL CloudConvert]-Konto abrufen.

1. Melden Sie sich bei Ihrem [!DNL CloudConvert] Konto an und öffnen Sie Ihr [!UICONTROL Dashboard].
1. Öffnen Sie den **[!UICONTROL Autorisierung] > [!UICONTROL API-Schlüssel]**.
1. Klicken Sie **[!UICONTROL Neuen API-Schlüssel erstellen]**.
1. Geben Sie den Namen für den API-Schlüssel ein, aktivieren Sie die gewünschten Bereiche und klicken Sie dann auf **[!UICONTROL Erstellen]**.
1. Kopieren Sie das bereitgestellte Token und bewahren Sie es an einem sicheren Ort auf.
1. Beginnen Sie in Workfront Fusion mit der Erstellung eines Szenarios und öffnen Sie das Dialogfeld [!DNL CloudConvert]Verbindung erstellen **[!UICONTROL des]**.

   Anweisungen finden Sie unter [Erstellen eines Szenarios in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

1. Geben Sie das Token ein, das Sie in Schritt 5 gespeichert haben, und klicken Sie dann auf **[!UICONTROL Weiter]**, um die Verbindung herzustellen.

## [!DNL CloudConvert] Module und ihre Felder {#cloudconvert-modules-and-their-fields}

Beim Konfigurieren von [!DNL CloudConvert] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL CloudConvert] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Allgemeine Aufgaben](#common-tasks)
* [Aufträge](#jobs)
* [Aufgaben](#tasks)
* [Sonstiges](#other)

### Allgemeine Aufgaben

* [Erfassen einer Website](#capture-a-website)
* [[!UICONTROL Datei konvertieren]](#convert-a-file)
* [Erstellen eines Archivs](#create-an-archive)
* [Dateien zusammenführen](#merge-files)
* [Datei optimieren](#optimize-a-file)

#### [!UICONTROL Erfassen einer Website]

Dieses Aktionsmodul erfasst eine angegebene Website und speichert sie im PDF-, JPG- oder PNG-Format.

Geben Sie die URL der Website und andere Informationen an, z. B. wo die Informationen gespeichert werden sollen.

Das Modul gibt die ID der Datei und aller zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie die URL der Website ein, die Sie erfassen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabeformat] </td> 
   <td>Wählen Sie aus, ob Sie die erfasste Website im PNG-, JPG- oder PDF-Format speichern möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dateiname] </td> 
   <td>Geben Sie einen Dateinamen (einschließlich Erweiterung) für die Zielausgabedatei ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen] </td> 
   <td> <p>(Optional) Definieren Sie Anfrage-Header. </p> <p>Dies ist beispielsweise nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Konvertierungs- und Engine-spezifische Optionen] </p> </td> 
   <td>Geben Sie Konversions- und Engine-spezifische Optionen an. Informationen zu den verfügbaren Optionen finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]-</a> für <code>input_format</code> und <code>output_format</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei herunterladen] </td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie auch Dateidaten in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei konvertieren]

Konvertiert eine Datei in ein ausgewähltes Ausgabeformat.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eingabedatei]</td> 
   <td>Wählen Sie aus, ob Sie eine Datei mit Workfront Fusion hochladen möchten, oder geben Sie die URL an, über die die Datei hochgeladen werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei hochladen]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei von URL importieren]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Geben Sie die URL der Datei ein, die Sie konvertieren möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL-Kopfzeilen]</strong></p> <p>Definieren Sie Anfrage-Header (optional). Dies ist beispielsweise dann nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Format]</td> 
   <td>Wählen Sie aus, ob Sie das Eingabeformat der zu konvertierenden Datei angeben möchten. Wenn kein Wert angegeben ist, wird die Erweiterung der Eingabedatei als Eingabeformat verwendet.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Input Format]</td> 
   <td>Das aktuelle Format der Datei auswählen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Ausgabeformat]</td> 
   <td>Wählen Sie das Zieldateiformat aus, in das Sie die Datei konvertieren möchten.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Dateiname]</td> 
   <td>Wählen Sie einen Dateinamen (einschließlich Erweiterung) für die Ziel-Ausgabedatei.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Konvertierungs- und Engine-spezifische Optionen] </p> </td> 
   <td>Geben Sie Konversions- und Engine-spezifische Optionen an. Informationen zu den verfügbaren Optionen finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]-</a> für <code>input_format</code> und <code>output_format</code>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Datei herunterladen] </td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie auch Dateidaten in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen eines Archivs]

Ermöglicht das Hinzufügen einer oder mehrerer Dateien zum ZIP, RAR, 7Z, TAR, TAR.GZ oder TAR.BZ2 Archiv.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Eingabedateien]</p> </td> 
   <td> <p>Geben Sie die Dateien an, die Sie dem Archiv hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei hochladen]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Datei von URL importieren]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>Geben Sie die URL der Datei ein, die Sie archivieren möchten.</p> <p><strong>[!UICONTROL-Kopfzeilen]</strong> </p> <p>Definieren Sie Anfrage-Header (optional). Dies ist beispielsweise dann nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabeformat]</td> 
   <td> <p> Zielformat der archivierten Datei auswählen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dateiname]</td> 
   <td> <p> Geben Sie den Dateinamen (einschließlich Erweiterung) der Zielausgabedatei ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konvertierungs- und Engine-spezifische Optionen] </td> 
   <td> <p>Geben Sie Konversions- und Engine-spezifische Optionen an. Informationen zu den verfügbaren Optionen finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]-</a> für <code>input_format</code> und <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei herunterladen]</td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie auch Dateidaten in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dateien zusammenführen]

Führt mindestens zwei Dateien in einer PDF zusammen. Wenn Eingabedateien keine PDFs sind, werden sie automatisch in PDF konvertiert.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Eingabedateien]</p> </td> 
   <td> <p>Geben Sie die Dateien an, die zusammengeführt werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei hochladen]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Datei von URL importieren]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>Geben Sie die URL der Datei ein, die Sie archivieren möchten.</p> <p><strong>[!UICONTROL-Kopfzeilen]</strong> </p> <p>Definieren Sie Anfrage-Header (optional). Dies ist beispielsweise dann nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabeformat]</td> 
   <td> <p> Zielformat der zusammengeführten Datei auswählen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dateiname]</td> 
   <td> <p> Geben Sie den Dateinamen (einschließlich Erweiterung) der Zielausgabedatei ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konvertierungs- und Engine-spezifische Optionen] </td> 
   <td> <p>Geben Sie Konversions- und Engine-spezifische Optionen an. Informationen zu den verfügbaren Optionen finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]-</a> für <code>input_format</code> und <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei herunterladen]</td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie auch Dateidaten in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei optimieren]

Dieses Aktionsmodul optimiert und komprimiert eine Datei im PDF-, PNG- oder JPG-Format.

Sie geben die Datei und die Parameter für die Optimierung und Speicherung an.

Das Modul gibt die ID der Datei und aller zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eingabedatei]</td> 
   <td>Wählen Sie aus, ob Sie eine Datei mit Workfront Fusion hochladen möchten, oder geben Sie die URL an, von der die Datei hochgeladen werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Datei hochladen]</p> </td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei von URL importieren] </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: Geben Sie die URL der Datei ein, die Sie konvertieren möchten.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (Optional) Definieren Sie Anfrage-Header. Dies ist beispielsweise nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optimierung für] </td> 
   <td> <p>Wählen Sie das Optimierungsprofil für spezifische Zielanforderungen aus.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Web]</strong>: Web-Optimierung (Standard)</p> 
      <ul> 
       <li>Entfernen redundanter und unnötiger Daten aus dem Web</li> 
       <li>Downsample, Clip und intelligente Komprimierung von Bildern</li> 
       <li>Zusammenführen und Untergruppen von Schriftarten</li> 
       <li>Farben in RGB konvertieren</li> 
      </ul> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL print]</strong>: Optimierung für den Druck</p> 
      <ul> 
       <li> <p>Entfernen Sie redundante und unnötige Daten für den Druck</p> </li> 
       <li> <p>Downsample, Clip und intelligente Komprimierung von Bildern</p> </li> 
       <li> <p>Zusammenführen und Untergruppen von Schriftarten</p> </li> 
       <li> <p>Farben in CMYK konvertieren</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Archive]</strong>: Optimierung für Archivierungszwecke</p> 
      <ul> 
       <li> <p>Entfernen redundanter und unnötiger Daten für die Archivierung</p> </li> 
       <li> <p>Bilder intelligent komprimieren</p> </li> 
       <li> <p>Zusammenführen und Untergruppen von Schriftarten</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Gescannte Bilder]</strong>: Optimierung für gescannte Bilder</p> 
      <ul> 
       <li> <p>Profil optimiert für PDFs, die hauptsächlich aus Rasterbildern bestehen</p> </li> 
       <li> <p>Komprimieren Sie die Bilder, ohne die visuelle Qualität erheblich zu beeinträchtigen.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL maximale Größenreduktion]</strong>: Optimierung für maximale Größenreduktion</p> 
      <ul> 
       <li> <p>Maximal mögliche Komprimierung verwenden</p> </li> 
       <li> <p>Kann die visuelle Qualität beeinträchtigen</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eingabeformat] </td> 
   <td>Wählen Sie das Format der Eingabedatei aus, die Sie optimieren möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dateiname]</td> 
   <td> <p>Geben Sie einen Dateinamen (einschließlich Erweiterung) für die Zielausgabedatei ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konvertierungs- und Engine-spezifische Optionen]</td> 
   <td> <p>Geben Sie Konversions- und Engine-spezifische Optionen an. Informationen zu den verfügbaren Optionen finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]-</a> für <code>input_format</code> und <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei herunterladen]</td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie auch Dateidaten in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aufträge

* [[!UICONTROL Erstellen eines Auftrags (erweitert)]](#create-a-job-advanced)
* [[!UICONTROL Neues Auftragsereignis]](#new-job-event)
* [[!UICONTROL Aufträge auflisten]](#list-jobs)
* [[!UICONTROL Such dir einen Job]](#get-a-job)
* [[!UICONTROL Auftrag löschen]](#delete-a-job)

#### [!UICONTROL Erstellen eines Auftrags (erweitert)]

Dieses Modul erstellt einen Auftrag. Ein Auftrag kann eine oder mehrere Aufgaben sein, die im Feld [!UICONTROL Name] identifiziert und mithilfe des Felds [!UICONTROL Eingabe] miteinander verknüpft werden.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eingabedateien]</td> 
   <td> <p>Wählen Sie aus, ob Sie eine Datei mit Workfront Fusion hochladen möchten, oder geben Sie die URL an, von der die Datei hochgeladen werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei hochladen]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Datei von URL importieren]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: Geben Sie die URL der Datei ein, die Sie verarbeiten möchten.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (Optional) Definieren Sie Anfrage-Header. Dies ist beispielsweise nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Aufgaben]</p> </td> 
   <td> <p>Fügen Sie Aufgaben hinzu, die innerhalb des Auftrags ausgeführt werden sollen.</p> <p>Beschreibungen der Felder der Vorgänge finden Sie im entsprechenden Abschnitt.</p> 
    <ul> 
     <li><a href="#convert-a-file" class="MCXref xref">[!UICONTROL Datei konvertieren]</a> </li> 
     <li><a href="#capture-a-website" class="MCXref xref">[!UICONTROL, um eine Website zu erfassen]e</a> </li> 
     <li><a href="#optimize-a-file" class="MCXref xref">[!UICONTROL Datei optimieren]</a> </li> 
     <li><a href="#create-an-archive" class="MCXref xref">[!UICONTROL Archiv erstellen]</a> </li> 
     <li><a href="#merge-files" class="MCXref xref">[!UICONTROL Dateien zusammenführen]</a> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Befehl ausführen]</strong> </p> <p>Weitere Informationen zum Ausführen eines Befehls finden Sie in der <a href="https://cloudconvert.com/api/v2/command#command-tasks">[!DNL CloudConvert] API-Dokumentation</a>.</p> </li> 
     <li> <p><strong>[!UICONTROL Datei in temporäre URL exportieren]</strong> </p> <p> Geben Sie den Aufgabennamen und den Namen der Eingabeaufgabe an (z. B. „Konversion„).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag] </td> 
   <td> <p>Tag eingeben. Tags sind beliebige Zeichenfolgen, um den Auftrag zu identifizieren. Sie haben keine Auswirkungen und können verwendet werden, um den Auftrag mit einer ID zu verknüpfen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Auftrag löschen]

Dieses Modul löscht einen Auftrag einschließlich aller Aufgaben und Daten.

>[!NOTE]
>
>Aufträge werden 24 Stunden nach ihrem Ende automatisch gelöscht.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorgangs-ID]</td> 
   <td> <p>Geben Sie die ID des Auftrags ein, den Sie löschen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Such dir einen Job]

Dieses Modul ruft Auftragsdetails ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorgangs-ID]</td> 
   <td> <p>Geben Sie die ID des Auftrags ein, zu dem Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufträge auflisten]

Dieses Modul ruft alle Aufträge ab, die in Ihrem Konto ausgeführt wurden.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Wählen Sie den Auftragsstatus aus, um die zurückgegebenen Aufträge zu filtern nach.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die Anzahl der Aufträge fest, die Workfront Fusion 2.0 während eines Ausführungszyklus zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Neues Auftragsereignis]

Trigger, wenn ein Vorgang in Ihrem Konto oder einer Aufgabe erstellt wird, abgeschlossen wird oder fehlschlägt.

>[!NOTE]
>
>* Der vom Modul [!UICONTROL Auftrag erstellen (erweitert)] erstellte Auftrag besteht aus *mehreren* Aufgaben.
>* Der [!UICONTROL Neues Auftragsereignis]-Trigger wird auch ausgelöst, wenn eine *individuelle* Aufgabe erstellt wurde, abgeschlossen wurde oder fehlgeschlagen ist.
>

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name]</td> 
   <td>Den Webhook-Namen eingeben. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabeformat] </td> 
   <td>Wählen Sie aus, ob Sie die erfasste Website im PNG-, JPG- oder PDF-Format speichern möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Ereignis]</td> 
   <td>Wählen Sie aus, ob das Modul ausgelöst wird, wenn der Auftrag oder die Aufgabe erstellt wird, abgeschlossen wird oder fehlschlägt.</td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Wenn Sie mit dem Array-Aggregator arbeiten (z. B. müssen Sie viele Dateien in verschiedenen Formaten konvertieren), verwenden Sie die Option **[!UICONTROL ich kenne das Eingabeformat nicht]** im Dialogfeld [!UICONTROL Aufgabe hinzufügen]. Andernfalls wird der Fehler zurückgegeben.
>* Verknüpfen von Aufgaben innerhalb des Auftrags (Name > Eingabe, Name > Eingabe usw.):
>
>  ![Name über Aufträge hinweg verknüpfen](/help/workfront-fusion/references/apps-and-modules/assets/linking-name-across-jobs-350x808.png)>

### Aufgaben

* [[!UICONTROL Aufgabe abrufen]](#get-a-task)
* [[!UICONTROL Datei herunterladen]](#download-a-file)
* [[!UICONTROL Aufgaben auflisten]](#list-tasks)
* [[!UICONTROL Aufgabe wiederholen]](#retry-a-task)
* [[!UICONTROL Aufgabe abbrechen]](#cancel-a-task)
* [[!UICONTROL Aufgabe löschen]](#delete-a-task)

#### [!UICONTROL Aufgabe abbrechen]

Mit diesem Modul wird eine Aufgabe mit dem Status Warten oder Verarbeiten abgebrochen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aufgaben-ID]</td> 
   <td> <p> Geben Sie die ID der Aufgabe ein, die Sie abbrechen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufgabe löschen]

Aufgabe einschließlich aller Daten löschen

>[!NOTE]
>
>Aufgaben werden 24 Stunden nach ihrem Ende automatisch gelöscht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aufgaben-ID]</td> 
   <td> <p> Geben Sie die ID der Aufgabe ein (zuordnen), die Sie löschen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei herunterladen]

Dieses Modul ruft den Dateinamen und die Dateidaten von der angegebenen Aufgabe ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aufgaben-ID]</td> 
   <td> <p> Geben Sie die ID der Aufgabe ein, von der Sie die Datei herunterladen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufgabe abrufen]

Dieses Modul ruft Aufgabendetails ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aufgaben-ID]</td> 
   <td> <p>Geben Sie die ID der Aufgabe ein, zu der Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufgaben auflisten]

Dieses Modul ruft alle Aufgaben in Ihrem Konto basierend auf den Filtereinstellungen ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Aufgabenstatus auswählen, um die zurückgegebenen Aufgaben zu filtern nach.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorgangs-ID] </td> 
   <td> <p>Geben Sie die Auftrags-ID ein oder ordnen Sie sie zu, um nur Aufgaben innerhalb des angegebenen Auftrags zurückzugeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Vorgang] </td> 
   <td> <p>Geben Sie den Vorgangstyp ein, um nur Aufgaben mit dem angegebenen Vorgang zurückzugeben. </p> <p>Hinweis: Verwenden Sie das Modul [!UICONTROL List Possible Operations], um Vorgänge abzurufen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufgabe wiederholen]

Dieses Modul erstellt eine neue Aufgabe basierend auf den Einstellungen (Payload) einer anderen Aufgabe.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aufgaben-ID]</td> 
   <td> <p> Geben Sie die ID der Aufgabe ein, aus der Sie eine neue Aufgabe erstellen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

* [[!UICONTROL Meine Infos abrufen]](#get-my-info)
* [[!UICONTROL Erstellen eines API-Aufrufs]](#make-an-api-call)

#### [!UICONTROL Meine Infos abrufen]

Ruft authentifizierte Kontodetails zum aktuellen Benutzer ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen eines API-Aufrufs]

Ermöglicht die Durchführung eines benutzerdefinierten API-Aufrufs.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres CloudConvert-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://api.cloudconvert.com/</code> ein. Beispiel: <code>/v2/tasks</code></p> <p>Eine Liste der verfügbaren Endpunkte finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2">[!DNL CloudConvert] API v2</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion 2.0 fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des API-Aufrufs in Form eines standardmäßigen JSON-Objekts hinzu. Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** Aufgaben auflisten

Der folgende API-Aufruf gibt alle Aufgaben aus Ihrem CloudFront-Konto zurück:

URL: `/v2/tasks`

Methode: `GET`

![API-Beispieleingabe](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-input.png)

Treffer der Suche finden Sie in der Modulausgabe unter [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL data].

In unserem Beispiel wurden 6 Aufgaben zurückgegeben:

![API-Beispielausgabe](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-output.png)

## Fehlerbehebung {#troubleshooting}

In der folgenden Tabelle finden Sie mögliche Fehler und deren Lösungen:

<table style="table-layout:auto">
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> <p>Fehler</p> </th> 
   <th>Nächste Schritte</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL Die Größe der Ausgabedatei überschreitet das für Ihr Szenario zulässige Limit.]</span> </p> </td> 
   <td> <p>Siehe Dateigrößenbeschränkungen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL Sie haben die maximale Konvertierungszeit überschritten.]</span> </p> </td> 
   <td> <p>Der kostenlose [!DNL CloudConvert] bietet täglich 25 Konversionsminuten. Wenn Ihre Nutzung die Grenze des kostenlosen Plans überschreitet, können Sie zu einem (Prepaid-) Paket oder Abonnement wechseln.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL konnte die Rahmengröße nicht lesen: Es konnte nicht nach 1508 gesucht werden. �/output/JLIADSA00137P0.mp3: Ungültiges Argument.]</span> </p> </td> 
   <td> <p>Dieser Fehler wird z.B. beim Konvertieren von Dateien aus MP3 in WAV ausgelöst. Stellen Sie sicher, dass Sie die richtige Region ausgewählt haben, da sie Verweise auf -Dateien findet, aber nicht nur auf die richtige Datei.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL RuntimeError:] </p> <p><span style="font-weight: normal;">[!UICONTROL Maximale Anzahl von Wiederholungen überschritten.]</span> </p> </td> 
   <td> <p>Suchen Sie den entsprechenden [!DNL CloudConvert] Auftrag in der Liste der Aufträge im [!DNL CloudConvert]-Dashboard und überprüfen Sie die Dauer des Auftrags:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-duration-350x177.png" style="width: 350;height: 177;"> </p> <p>Der Timeout des Moduls [!DNL CloudConvert] &gt; [!UICONTROL Convert a File] ist auf 3 Minuten festgelegt. Wenn die Dauer des Auftrags 3 Minuten überschreitet (möglicherweise aufgrund einer temporären Überlastung des [!DNL CloudConvert]-Services), gibt das Modul den oben genannten Fehler aus.</p> <p>Erwägen Sie in diesem Fall eine der folgenden Optionen:</p> 
    <ul> 
     <li>Aktivieren Sie die Option <strong>[!UICONTROL Speicherung unvollständiger Ausführungen zulassen</strong> in den Szenarioeinstellungen, um die unvollständigen Ausführungen für eine spätere manuelle Auflösung zu speichern. Optional können Sie dem [!DNL CloudConvert]-Modul mit der [!UICONTROL Break]-Direktive eine Fehlerbehandlungsroute anhängen, um die unvollständigen Ausführungen automatisch aufzulösen.</li> 
     <li>Deaktivieren Sie die Option <strong>[!UICONTROL Datei herunterladen</strong> im Modul [!DNL CloudConvert] &gt; [!UICONTROL Datei konvertieren]. In diesem Fall wartet das Modul nicht auf das Konvertierungsergebnis. Um das Konvertierungsergebnis zu erhalten, erstellen Sie ein neues Szenario und verwenden Sie den Trigger [!DNL CloudConvert] &gt; [!UICONTROL New Job Event].</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel-Workflow für [!DNL CloudConvert] Connector

>[!INFO]
>
>**Beispiel:** Konvertieren eines Videos aus dem MOV- in das MP4-Format
>
>1. [https://cloudconvert.com/video-converter](https://>cloudconvert.com/video-converter) besuchen
>1. Klicken Sie **[!UICONTROL Datei auswählen]** und wählen Sie Ihre MOV-Beispieldatei aus.
>1. Klicken Sie auf das Dropdown-Menü neben **[!UICONTROL Konvertieren in]** und wählen Sie **[!UICONTROL MP4]**.
>
>1. Klicken Sie auf **[!UICONTROL Symbol]** Schraubenschlüssel“.
>1. Konfigurieren Sie die MP4-Komprimierungseinstellungen nach Bedarf.
>1. Klicken Sie **[!UICONTROL Konvertieren]**.
>1. Klicken Sie nach Abschluss der Konvertierung auf **[!UICONTROL Herunterladen]**.
>1. Sehen Sie sich das konvertierte Video an.
>1. Wiederholen Sie die Schritte 1 bis 8, bis Sie die optimalen Konvertierungseinstellungen für Schritt 5 gefunden haben.
>1. [https://cloudconvert.com/api/v2/convert#convert-tasks](https://cloudconvert.com/api/v2/convert#convert-tasks) besuchen
>1. Wählen Sie **[!UICONTROL mov]** für das Feld **[!UICONTROL input_format]** aus.
>
>1. Wählen Sie **[!UICONTROL mp4]** für das Feld **[!UICONTROL output_format]**.
>
>1. Eine Liste aller möglichen Parameter wie video_codec, crf, etc. wird angezeigt.
>1. Fügen Sie in Workfront Fusion 2.0 das Modul **[!UICONTROL CloudConvert]** > **[!UICONTROL Datei konvertieren]** in Ihr Szenario ein.
>
>1. Öffnen Sie die Einstellungen des Moduls.
>1. Konfigurieren Sie das Modul wie unten gezeigt:
>
>   ![CloudConvert-Beispiel](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-mp4-example.png)
>
>1. Stellen Sie sicher, dass Sie alle Einstellungen im Feld Konversions- und Engine-spezifische Optionen einbeziehen: Suchen Sie für jede Einstellung aus Schritt 5 den entsprechenden Parameter aus Schritt 13 und den entsprechenden Wert.
