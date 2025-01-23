---
title: CloudConvert-Module
description: CloudConvert-Module
author: Becky
feature: Workfront Fusion
exl-id: 52c4d18a-8bee-44d6-9a2c-cc9e157e1dde
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '2486'
ht-degree: 0%

---

# [!DNL CloudConvert]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die CloudConvert verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden. Mit den [!DNL CloudConvert]-Modulen können Sie Aufträge und Aufgaben überwachen und verwalten sowie Dateien in Ihr [!DNL CloudConvert]-Konto importieren und exportieren.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Plan*</td>
  <td> <p>[!UICONTROL Pro] oder höher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung und -integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den [!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Adobe Workfront] verfügen, muss Ihr Unternehmen [!DNL Adobe Workfront Fusion] kaufen und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden. [!DNL Workfront Fusion] ist im [!UICONTROL Ultimate] [!DNL Workfront] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

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

## [!DNL CloudConvert] mit [!DNL Workfront Fusion] verbinden {#connect-cloudconvert-to-workfront-fusion}

Um Ihr [!DNL CloudConvert]-Konto mit [!DNL Workfront Fusion] zu verbinden, müssen Sie den API-Schlüssel von Ihrem [!DNL CloudConvert]-Konto abrufen.

1. Melden Sie sich bei Ihrem [!DNL CloudConvert] Konto an und öffnen Sie Ihre [!UICONTROL Dashboard].
1. Öffnen Sie den Abschnitt **[!UICONTROL Authorization]>[!UICONTROL API Keys]** .
1. Klicken Sie auf **[!UICONTROL Create New API key]**.
1. Geben Sie den Namen für den API-Schlüssel ein, aktivieren Sie die gewünschten Bereiche und klicken Sie dann auf **[!UICONTROL Create]**.
1. Kopieren Sie das bereitgestellte Token und bewahren Sie es an einem sicheren Ort auf.
1. Beginnen Sie [!DNL Workfront Fusion] mit der Erstellung eines Szenarios und öffnen Sie das **[!UICONTROL Create a connection]**-Dialogfeld des [!DNL CloudConvert].

   Anweisungen finden Sie unter [Erstellen eines Szenarios in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

1. Geben Sie das Token ein, das Sie in Schritt 5 gespeichert haben, und klicken Sie dann auf **[!UICONTROL Continue]** , um die Verbindung herzustellen.

## [!DNL CloudConvert] Module und ihre Felder {#cloudconvert-modules-and-their-fields}

Beim Konfigurieren [!DNL CloudConvert] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL CloudConvert] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Allgemeine Aufgaben](#common-tasks)
* [Aufträge](#jobs)
* [Aufgaben](#tasks)
* [Sonstige](#other)

### Allgemeine Aufgaben

* [Erfassen einer Website](#capture-a-website)
* [[!UICONTROL Convert a file]](#convert-a-file)
* [Erstellen eines Archivs](#create-an-archive)
* [Dateien zusammenführen](#merge-files)
* [Datei optimieren](#optimize-a-file)

#### [!UICONTROL Capture a Website]

Dieses Aktionsmodul erfasst eine bestimmte Website und speichert sie im PDF-, JPG- oder PNG-Format.

Geben Sie die URL der Website und andere Informationen an, z. B. wo die Informationen gespeichert werden sollen.

Das Modul gibt die ID der Datei und aller zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie die URL der Website ein, die Sie erfassen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format] </td> 
   <td>Wählen Sie aus, ob Sie die erfasste Website im PNG-, JPG- oder PDF-Format speichern möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td>Geben Sie einen Dateinamen (einschließlich Erweiterung) für die Zielausgabedatei ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>(Optional) Definieren Sie Anfrage-Header. </p> <p>Dies ist beispielsweise nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conversion and engine specific options] </p> </td> 
   <td>Geben Sie Konversions- und Engine-spezifische Optionen an. Informationen zu den verfügbaren Optionen finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]-</a> für <code>input_format</code> und <code>output_format</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a file] </td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie auch Dateidaten in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Convert a file]

Konvertiert eine Datei in ein ausgewähltes Ausgabeformat.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input file]</td> 
   <td>Wählen Sie aus, ob Sie eine Datei mit [!DNL Workfront Fusion] hochladen möchten, oder geben Sie die URL an, von der die Datei hochgeladen werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a file]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Import a File from URL]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Geben Sie die URL der Datei ein, die Sie konvertieren möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL Headers]</strong></p> <p>Definieren Sie Anfrage-Header (optional). Dies ist beispielsweise dann nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Format]</td> 
   <td>Wählen Sie aus, ob Sie das Eingabeformat der zu konvertierenden Datei angeben möchten. Wenn kein Wert angegeben ist, wird die Erweiterung der Eingabedatei als Eingabeformat verwendet.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Input Format]</td> 
   <td>Das aktuelle Format der Datei auswählen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td>Wählen Sie das Zieldateiformat aus, in das Sie die Datei konvertieren möchten.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL File Name]</td> 
   <td>Wählen Sie einen Dateinamen (einschließlich Erweiterung) für die Ziel-Ausgabedatei.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Conversion and engine specific options] </p> </td> 
   <td>Geben Sie Konversions- und Engine-spezifische Optionen an. Informationen zu den verfügbaren Optionen finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]-</a> für <code>input_format</code> und <code>output_format</code>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Download a file] </td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie auch Dateidaten in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an Archive]

Ermöglicht das Hinzufügen einer oder mehrerer Dateien zum ZIP, RAR, 7Z, TAR, TAR.GZ oder TAR.BZ2 Archiv.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Input Files]</p> </td> 
   <td> <p>Geben Sie die Dateien an, die Sie dem Archiv hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a file from URL]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>Geben Sie die URL der Datei ein, die Sie archivieren möchten.</p> <p><strong>[!UICONTROL Headers]</strong> </p> <p>Definieren Sie Anfrage-Header (optional). Dies ist beispielsweise dann nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p> Zielformat der archivierten Datei auswählen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p> Geben Sie den Dateinamen (einschließlich Erweiterung) der Zielausgabedatei ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options] </td> 
   <td> <p>Geben Sie Konversions- und Engine-spezifische Optionen an. Informationen zu den verfügbaren Optionen finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]-</a> für <code>input_format</code> und <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a File]</td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie auch Dateidaten in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Merge Files]

Führt mindestens zwei Dateien zu einer PDF zusammen. Wenn Eingabedateien keine PDF sind, werden sie automatisch in PDF konvertiert.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Input Files]</p> </td> 
   <td> <p>Geben Sie die Dateien an, die zusammengeführt werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a file from URL]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>Geben Sie die URL der Datei ein, die Sie archivieren möchten.</p> <p><strong>[!UICONTROL Headers]</strong> </p> <p>Definieren Sie Anfrage-Header (optional). Dies ist beispielsweise dann nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p> Zielformat der zusammengeführten Datei auswählen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p> Geben Sie den Dateinamen (einschließlich Erweiterung) der Zielausgabedatei ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options] </td> 
   <td> <p>Geben Sie Konversions- und Engine-spezifische Optionen an. Informationen zu den verfügbaren Optionen finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]-</a> für <code>input_format</code> und <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a File]</td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie auch Dateidaten in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Optimize a File]

Dieses Aktionsmodul optimiert und komprimiert eine Datei im PDF-, PNG- oder JPG-Format.

Sie geben die Datei und die Parameter für die Optimierung und Speicherung an.

Das Modul gibt die ID der Datei und aller zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input File]</td> 
   <td>Wählen Sie aus, ob Sie eine Datei mit Workfront Fusion hochladen möchten, oder geben Sie die URL an, von der die Datei hochgeladen werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Upload a File]</p> </td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Import a file from URL] </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: Geben Sie die URL der Datei ein, die Sie konvertieren möchten.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (Optional) Definieren Sie Anfrage-Header. Dies ist beispielsweise nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optimization for] </td> 
   <td> <p>Wählen Sie das Optimierungsprofil für spezifische Zielanforderungen aus.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Web]</strong>: Optimierung für das Web (Standard)</p> 
      <ul> 
       <li>Entfernen redundanter und unnötiger Daten aus dem Web</li> 
       <li>Downsample, Clip und intelligente Komprimierung von Bildern</li> 
       <li>Zusammenführen und Untergruppen von Schriftarten</li> 
       <li>Farben in RGB konvertieren</li> 
      </ul> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Print]</strong>: Optimierung für den Druck</p> 
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
     <li> <p><strong>[!UICONTROL Scanned images]</strong>: Optimierung für gescannte Bilder</p> 
      <ul> 
       <li> <p>Profil optimiert für PDF, die hauptsächlich aus Rasterbildern bestehen</p> </li> 
       <li> <p>Komprimieren Sie die Bilder, ohne die visuelle Qualität erheblich zu beeinträchtigen.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL maximal size reduction]</strong>: Optimierung für maximale Größenreduzierung</p> 
      <ul> 
       <li> <p>Maximal mögliche Komprimierung verwenden</p> </li> 
       <li> <p>Kann die visuelle Qualität beeinträchtigen</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input format] </td> 
   <td>Wählen Sie das Format der Eingabedatei aus, die Sie optimieren möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p>Geben Sie einen Dateinamen (einschließlich Erweiterung) für die Zielausgabedatei ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options]</td> 
   <td> <p>Geben Sie Konversions- und Engine-spezifische Optionen an. Informationen zu den verfügbaren Optionen finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]-</a> für <code>input_format</code> und <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a file]</td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie auch Dateidaten in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Jobs

* [[!UICONTROL Create a Job (advanced)]](#create-a-job-advanced)
* [[!UICONTROL New Job Event]](#new-job-event)
* [[!UICONTROL List Jobs]](#list-jobs)
* [[!UICONTROL Get a Job]](#get-a-job)
* [[!UICONTROL Delete a Job]](#delete-a-job)

#### [!UICONTROL Create a Job (advanced)]

Dieses Modul erstellt einen Auftrag. Ein Auftrag kann eine oder mehrere Aufgaben sein, die im Feld [!UICONTROL Name] identifiziert und mithilfe des Felds [!UICONTROL Input] miteinander verknüpft werden.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input Files]</td> 
   <td> <p>Wählen Sie aus, ob Sie eine Datei mit [!DNL Workfront Fusion] hochladen möchten, oder geben Sie die URL an, von der die Datei hochgeladen werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a File from URL]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: Geben Sie die URL der Datei ein, die Sie verarbeiten möchten.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (Optional) Definieren Sie Anfrage-Header. Dies ist beispielsweise nützlich, wenn für die angegebene URL eine Autorisierung erforderlich ist.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tasks]</p> </td> 
   <td> <p>Fügen Sie Aufgaben hinzu, die innerhalb des Auftrags ausgeführt werden sollen.</p> <p>Beschreibungen der Felder der Vorgänge finden Sie im entsprechenden Abschnitt.</p> 
    <ul> 
     <li><a href="#convert-a-file" class="MCXref xref">[!UICONTROL Convert a file]</a> </li> 
     <li><a href="#capture-a-website" class="MCXref xref">[!UICONTROL Capture a Websit]E</a> </li> 
     <li><a href="#optimize-a-file" class="MCXref xref">[!UICONTROL Optimize a File]</a> </li> 
     <li><a href="#create-an-archive" class="MCXref xref">[!UICONTROL Create an Archive]</a> </li> 
     <li><a href="#merge-files" class="MCXref xref">[!UICONTROL Merge Files]</a> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Execute a Command]</strong> </p> <p>Weitere Informationen zum Ausführen eines Befehls finden Sie in der <a href="https://cloudconvert.com/api/v2/command#command-tasks">[!DNL CloudConvert] API-Dokumentation</a>.</p> </li> 
     <li> <p><strong>[!UICONTROL Export a File to Temporary URL]</strong> </p> <p> Geben Sie den Aufgabennamen und den Namen der Eingabeaufgabe an (z. B. „Konversion„).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag] </td> 
   <td> <p>Tag eingeben. Tags sind beliebige Zeichenfolgen, um den Auftrag zu identifizieren. Sie haben keine Auswirkungen und können verwendet werden, um den Auftrag mit einer ID zu verknüpfen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Job]

Dieses Modul löscht einen Auftrag einschließlich aller Aufgaben und Daten.

>[!NOTE]
>
>Aufträge werden 24 Stunden nach ihrem Ende automatisch gelöscht.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td> <p>Geben Sie die ID des Auftrags ein, den Sie löschen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Job]

Dieses Modul ruft Auftragsdetails ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td> <p>Geben Sie die ID des Auftrags ein, zu dem Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Jobs]

Dieses Modul ruft alle Aufträge ab, die in Ihrem Konto ausgeführt wurden.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
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

#### [!UICONTROL New Job Event]

Trigger, wenn ein Vorgang in Ihrem Konto oder einer Aufgabe erstellt wird, abgeschlossen wird oder fehlschlägt.

>[!NOTE]
>
>* Der vom [!UICONTROL Create a Job (advanced)] Modul erstellte Auftrag besteht aus *mehreren* Aufgaben.
>* Der [!UICONTROL New Job Event] Trigger wird auch ausgelöst, wenn eine *individuelle* Aufgabe erstellt, abgeschlossen oder fehlgeschlagen wird.
>

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhhook name]</td> 
   <td>Den Webhook-Namen eingeben. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format] </td> 
   <td>Wählen Sie aus, ob Sie die erfasste Website im PNG-, JPG- oder PDF-Format speichern möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event]</td> 
   <td>Wählen Sie aus, ob das Modul ausgelöst wird, wenn der Auftrag oder die Aufgabe erstellt wird, abgeschlossen wird oder fehlschlägt.</td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Wenn Sie mit dem Array-Aggregator arbeiten (z. B. wenn Sie viele Dateien in verschiedenen Formaten haben, die konvertiert werden sollen), verwenden Sie die Option **[!UICONTROL I don't know the input format]** im Dialogfeld [!UICONTROL Add a task] . Andernfalls wird der Fehler zurückgegeben.
>* Verknüpfen von Aufgaben innerhalb des Auftrags (Name > Eingabe, Name > Eingabe usw.):
>
>  ![](/help/workfront-fusion/references/apps-and-modules/assets/linking-name-across-jobs-350x808.png)>

### Aufgaben

* [[!UICONTROL Get a Task]](#get-a-task)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL List Tasks]](#list-tasks)
* [[!UICONTROL Retry a Task]](#retry-a-task)
* [[!UICONTROL Cancel a Task]](#cancel-a-task)
* [[!UICONTROL Delete a Task]](#delete-a-task)

#### [!UICONTROL Cancel a Task]

Mit diesem Modul wird eine Aufgabe mit dem Status Warten oder Verarbeiten abgebrochen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Geben Sie die ID der Aufgabe ein, die Sie abbrechen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Task]

Aufgabe einschließlich aller Daten löschen

>[!NOTE]
>
>Aufgaben werden 24 Stunden nach ihrem Ende automatisch gelöscht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Geben Sie die ID der Aufgabe ein (zuordnen), die Sie löschen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

Dieses Modul ruft den Dateinamen und die Dateidaten von der angegebenen Aufgabe ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Geben Sie die ID der Aufgabe ein, von der Sie die Datei herunterladen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Task]

Dieses Modul ruft Aufgabendetails ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p>Geben Sie die ID der Aufgabe ein, zu der Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Tasks]

Dieses Modul ruft alle Aufgaben in Ihrem Konto basierend auf den Filtereinstellungen ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Aufgabenstatus auswählen, um die zurückgegebenen Aufgaben zu filtern nach.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID] </td> 
   <td> <p>Geben Sie die Auftrags-ID ein oder ordnen Sie sie zu, um nur Aufgaben innerhalb des angegebenen Auftrags zurückzugeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation] </td> 
   <td> <p>Geben Sie den Vorgangstyp ein, um nur Aufgaben mit dem angegebenen Vorgang zurückzugeben. </p> <p>Hinweis: Verwenden Sie das Modul [!UICONTROL List Possible Operations] zum Abrufen von Vorgängen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Retry a Task]

Dieses Modul erstellt eine neue Aufgabe basierend auf den Einstellungen (Payload) einer anderen Aufgabe.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Geben Sie die ID der Aufgabe ein, aus der Sie eine neue Aufgabe erstellen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstige

* [[!UICONTROL Get My Info]](#get-my-info)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Get My Info]

Ruft authentifizierte Kontodetails zum aktuellen Benutzer ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL CloudConvert]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL CloudConvert] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Ermöglicht die Durchführung eines benutzerdefinierten API-Aufrufs.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [Fusion App]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://api.cloudconvert.com/</code> ein. Beispiel: <code>/v2/tasks</code></p> <p>Eine Liste der verfügbaren Endpunkte finden Sie in der Dokumentation zur <a href="https://cloudconvert.com/api/v2">[!DNL CloudConvert] API v2</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion 2.0 fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Fügen Sie den Hauptteil des API-Aufrufs in Form eines standardmäßigen JSON-Objekts hinzu. Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** Aufgaben auflisten

Der folgende API-Aufruf gibt alle Aufgaben aus Ihrem CloudFront-Konto zurück:

URL: `/v2/tasks`

Methode: `GET`

![](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-input.png)

Treffer der Suche finden Sie in der Modulausgabe unter [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL data].

In unserem Beispiel wurden 6 Aufgaben zurückgegeben:

![](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-output.png)

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
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL The output file size exceeds the limit allowed for your scenario.]</span> </p> </td> 
   <td> <p>Siehe Dateigrößenbeschränkungen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL You have exceeded the maximum conversion time.]</span> </p> </td> 
   <td> <p>Der kostenlose [!DNL CloudConvert] bietet täglich 25 Konversionsminuten. Wenn Ihre Nutzung die Grenze des kostenlosen Plans überschreitet, können Sie zu einem (Prepaid-) Paket oder Abonnement wechseln.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL Failed to read frame size: Could not seek to 1508. �/output/JLIADSA00137P0.mp3: Invalid argument.]</span> </p> </td> 
   <td> <p>Dieser Fehler wird z.B. beim Konvertieren von Dateien aus MP3 in WAV ausgelöst. Stellen Sie sicher, dass Sie die richtige Region ausgewählt haben, da sie Verweise auf -Dateien findet, aber nicht nur auf die richtige Datei.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL RuntimeError:] </p> <p><span style="font-weight: normal;">[!UICONTROL Maximum number of repeats exceeded.]</span> </p> </td> 
   <td> <p>Suchen Sie den entsprechenden [!DNL CloudConvert] Auftrag in der Liste der Aufträge im [!DNL CloudConvert]-Dashboard und überprüfen Sie die Dauer des Auftrags:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-duration-350x177.png" style="width: 350;height: 177;"> </p> <p>Die maximale Wartezeit des Moduls [!DNL CloudConvert] &gt; [!UICONTROL Convert a File] ist auf 3 Minuten festgelegt. Wenn die Dauer des Auftrags 3 Minuten überschreitet (möglicherweise aufgrund einer temporären Überlastung des [!DNL CloudConvert]-Services), gibt das Modul den oben genannten Fehler aus.</p> <p>Erwägen Sie in diesem Fall eine der folgenden Optionen:</p> 
    <ul> 
     <li>Aktivieren Sie die Option <strong>[!UICONTROL Allow storing of Incomplete Executions]</strong> in den Szenario-Einstellungen, um die unvollständigen Ausführungen für eine spätere manuelle Auflösung zu speichern. Optional können Sie eine Fehlerbehandlungsroute an das [!DNL CloudConvert] mit der [!UICONTROL Break] anhängen, um die unvollständigen Ausführungen automatisch aufzulösen.</li> 
     <li>Deaktivieren Sie die Option <strong>[!UICONTROL Download a file] </strong> Modul [!DNL CloudConvert] &gt; [!UICONTROL Convert a file] . In diesem Fall wartet das Modul nicht auf das Konvertierungsergebnis. Um das Konvertierungsergebnis zu erhalten, erstellen Sie ein neues Szenario und verwenden Sie den Trigger [!DNL CloudConvert] &gt; [!UICONTROL New Job Event] .</li> 
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
>1. Klicken Sie auf **[!UICONTROL Select File]** und wählen Sie Ihre Beispiel-MOV-Datei.
>1. Klicken Sie auf das Dropdown-Menü neben **[!UICONTROL Convert to]** und wählen Sie **[!UICONTROL MP4]** aus.
>
>1. Klicken Sie auf das Symbol **[!UICONTROL wrench]** .
>1. Konfigurieren Sie die MP4-Komprimierungseinstellungen nach Bedarf.
>1. Klicken Sie auf **[!UICONTROL Convert]**.
>1. Nachdem die Konvertierung abgeschlossen ist, klicken Sie auf **[!UICONTROL Download]**.
>1. Sehen Sie sich das konvertierte Video an.
>1. Wiederholen Sie die Schritte 1 bis 8, bis Sie die optimalen Konvertierungseinstellungen für Schritt 5 gefunden haben.
>1. [https://cloudconvert.com/api/v2/convert#convert-tasks](https://cloudconvert.com/api/v2/convert#convert-tasks) besuchen
>1. Wählen Sie **[!UICONTROL mov]** für das Feld **[!UICONTROL input_format]** aus.
>
>1. Wählen Sie **[!UICONTROL mp4]** für das Feld **[!UICONTROL output_format]** aus.
>
>1. Eine Liste aller möglichen Parameter wie video_codec, crf, etc. wird angezeigt.
>1. Fügen Sie in Workfront Fusion 2.0 das Modul **[!UICONTROL CloudConvert]** > **[!UICONTROL Convert a File]** in Ihr Szenario ein.
>
>1. Öffnen Sie die Einstellungen des Moduls.
>1. Konfigurieren Sie das Modul wie unten gezeigt:
>
>   ![](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-mp4-example.png)
>
>1. Stellen Sie sicher, dass Sie alle Einstellungen im Feld Konversions- und Engine-spezifische Optionen einbeziehen: Suchen Sie für jede Einstellung aus Schritt 5 den entsprechenden Parameter aus Schritt 13 und den entsprechenden Wert.
