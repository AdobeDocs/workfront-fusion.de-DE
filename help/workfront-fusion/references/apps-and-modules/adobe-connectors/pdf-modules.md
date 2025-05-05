---
title: Adobe PDF Services
description: Adobe PDF Services
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '4125'
ht-degree: 0%

---

# [!DNL Adobe PDF Services]

Mit dem [!DNL Adobe Workfront Fusion] [!DNL Adobe PDF Services] können Sie Daten aus einer PDF-Datei extrahieren oder eine neue PDF-Datei aus den von Ihnen bereitgestellten Daten generieren. Darüber hinaus können Sie eine Vielzahl von Dateitypen in PDFs oder PDFs in andere Dateitypen konvertieren. Mit PDF-Services können Sie außerdem Metadaten einer PDF-Datei kombinieren, komprimieren oder lesen sowie den Passwortschutz für die Datei steuern.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

Informationen über die für PDF-Services verwendete API finden Sie unter [Adobe Document Generation API](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html).

## Sicherheitsüberlegungen bei der Verwendung von [!DNL Adobe PDF Services]

Der [!DNL Adobe PDF Services] kann Ihre Dateien lesen, konvertieren oder ändern, Ihre Dateien oder Daten jedoch weder [!DNL Adobe] noch [!DNL Workfront Fusion] speichern. Dies bedeutet, dass:

* Sie behalten die Kontrolle über Ihre Dateien, einschließlich ihrer Sicherheit
* Sie benötigen kein [!UICONTROL Adobe]-Speicher- oder Cloud-Speicherkonto, um die PDF-Services zu verwenden.

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
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Oder</p>
   <p>Legacy: Workfront Fusion für Arbeitsautomatisierung und -integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Prime oder Workfront auswählen: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>Ultimate Workfront-Paket: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um eine OAuth-Server-zu-Server-Verbindung zu erstellen, müssen Sie die Adobe PDF Services-API in Ihrer Adobe Developers Console hinzufügen. Wählen Sie beim Hinzufügen der API die Option OAuth-Server-zu-Server aus.

Anweisungen finden Sie unter [Hinzufügen einer API zu einem Projekt mithilfe von OAuth](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/) in der Entwicklerdokumentation für Adobe.

## Adobe PDF Services-API-Informationen

Der Adobe PDF Services-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://pdf-services-stage.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v2.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung zu [!DNL Adobe PDF Services]

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe PDF Services]:

1. Klicken Sie in einem beliebigen [!DNL Adobe PDF Services] auf **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Verbindungstyp]</td>
          <td>
            <p>Wählen Sie aus, ob Sie eine Server-zu-Server-Verbindung oder eine JWT-Verbindung erstellen möchten.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Verbindungsname]</td>
          <td>
            <p>Geben Sie einen Namen für diese Verbindung ein.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-ID]</td>
          <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL Client ID] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].<p>Anweisungen zum Suchen von Anmeldeinformationen finden Sie unter <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Anmeldeinformationen</a> in der Adobe-Entwicklerdokumentation.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
          <td>Geben Sie Ihren [!DNL Adobe] [!UICONTROL Client Secret] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].<p>Anweisungen zum Suchen von Anmeldeinformationen finden Sie unter <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Anmeldeinformationen</a> in der Adobe-Entwicklerdokumentation.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID des technischen Kontos] (nur JWT)</td>
          <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL ID des technischen Kontos] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].<p>Anweisungen zum Suchen von Anmeldeinformationen finden Sie unter <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Anmeldeinformationen</a> in der Adobe-Entwicklerdokumentation.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Organisations-ID] (nur JWT)</td>
          <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL Organisations-ID] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].<p>Anweisungen zum Suchen von Anmeldeinformationen finden Sie unter <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Anmeldeinformationen</a> in der Adobe-Entwicklerdokumentation.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Meta Scopes] (nur JWT)</td>
          <td>
            Geben Sie alle für die Verbindung erforderlichen Metabereiche ein.
          </td>
        </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Privater Schlüssel]</td>
        <td>
          <p>Wenn Sie eine JWT-Verbindung ausgewählt haben, geben Sie den privaten Schlüssel ein, der beim Erstellen Ihrer Anmeldeinformationen im [!DNL Adobe Developer Console] generiert wurde. </p>
          <p>So extrahieren Sie Ihren privaten Schlüssel oder Ihr Zertifikat:</p>
          <ol>
            <li value="1">
              <p>Klicken Sie auf <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Wählen Sie den zu extrahierenden Dateityp aus.</p>
            </li>
            <li value="3">
              <p>Wählen Sie die Datei aus, die den privaten Schlüssel oder das Zertifikat enthält.</p>
            </li>
            <li value="4">
              <p>Geben Sie das Kennwort für die Datei ein.</p>
            </li>
            <li value="5">
              <p>Klicken Sie auf <b>[!UICONTROL Speichern]</b>, um die Datei zu extrahieren und zur Verbindungseinrichtung zurückzukehren.</p>
            </li>
          </ol>
        </td>
      </tr>
       </tbody>
    </table>
1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.


## [!DNL Adobe PDF Services] Module und ihre Felder

Beim Konfigurieren von [!DNL PDF Services] zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können je nach Faktoren wie Ihrer Zugriffsebene in der App oder im Service weitere Felder angezeigt werden. Ein fetter Titel in einem Modul kennzeichnet ein erforderliches Feld.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Kombinieren von PDF-Dateien]](#combine-pdf-files)
* [[!UICONTROL Komprimieren Sie PDF-Dateien]](#compress-pdf-files)
* [[!UICONTROL Dokument in PDF-Datei konvertieren]](#convert-document-to-pdf-file)
* [[!UICONTROL Konvertieren von HTML in PDF-Datei]](#convert-html-to-pdf-file)
* [[!UICONTROL Konvertieren des Bildes in eine PDF-Datei]](#convert-image-to-pdf-file)
* [[!UICONTROL Konvertieren von PDF in ein Dokument]](#convert-pdf-to-document)
* [[!UICONTROL Konvertieren von PDF in ein Bild]](#convert-pdf-to-image)
* [[!UICONTROL Text/Tabelle extrahieren]](#extract-text--table)
* [[!UICONTROL Dokument generieren]](#generate-document)
* [[!UICONTROL Linearisieren einer PDF-Datei]](#linearize-a-pdf-file)
* [Erstellen eines benutzerdefinierten API-Aufrufs](#make-a-custom-api-call)
* [[!UICONTROL OCR für PDF-Datei]](#ocr-for-pdf-file)
* [[!UICONTROL Seitenbearbeitung]](#page-manipulation)
* [[!UICONTROL Automatisches Tagging der Barrierefreiheit von PDF]](#pdf-accessibility-auto-tag)
* [[!UICONTROL PDF-Dateieigenschaften]](#pdf-file-properties)
* [[!UICONTROL Schützen der PDF-Datei]](#protect-pdf-file)
* [[!UICONTROL Entfernen des Schutzes einer PDF-Datei]](#remove-protection-of-a-pdf-file)
* [PDF-Datei teilen](#split-a-pdf-file)

### [!UICONTROL Kombinieren von PDF-Dateien]

Dieses Aktionsmodul fasst mehrere PDF-Dateien zusammen und kombiniert sie in einer PDF-Datei. Beispielsweise könnte dieses Modul alle Dokumente in einem [!UICONTROL Workfront]-Projekt nach Abschluss des Projekts zu einem einzigen PDF kombinieren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Dokumente]</td> 
   <td> <p>Sie können ein Aggregator-Modul verwenden, um Dokumente zu sammeln, die in einer PDF kombiniert werden sollen, oder Sie können die Dokumente manuell hinzufügen. </p> <p>Es wird empfohlen, ein [!UICONTROL Array Aggregator]-Modul zu verwenden, um die Ausgabe eines vorherigen Moduls zu aggregieren. Mithilfe eines Aggregators müssen Sie nicht wissen, welche Namen, Speicherorte oder Anzahl von Dateien kombiniert werden sollen. Die Verwendung eines Aggregators ist daher viel flexibler und skalierbarer als die manuelle Eingabe der zu kombinierenden Dokumente.</p> <p>Um das Dateimodul [!UICONTROL PDF kombinieren] mit einem Aggregator verwenden zu können, müssen Sie die Zuordnung für das Feld [!UICONTROL -Dokumente] aktivieren. </p> <p>In diesem Beispiel identifiziert das Modul [!UICONTROL READ RELATED RECORDS] Dokumente, die mit einem Projekt verknüpft sind, und das Modul [!UICONTROL DOWNLOAD DOCUMENTS] lädt jedes davon herunter. Alle PDFs werden in einem Array aggregiert, das an das Dateimodul [!UICONTROL Combine PDF] übergeben wird.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>Sie können Dokumente auch manuell eingeben.</p> <p>Für jedes Dokument, das in die kombinierte PDF aufgenommen werden soll:</p> 
    <ol> 
     <li value="1"> <p>Klicken Sie auf [!UICONTROL Dokument hinzufügen]</p> </li> 
     <li value="2"> <p>Wählen Sie im Feld [!UICONTROL Source-Datei] das Modul aus, das das einzuschließende Dokument ausgibt, oder ordnen Sie den Namen und die Daten der Quelldatei zu. </p> </li> 
     <li value="3"> <p>(Optional) Wenn Sie nur bestimmte Seiten aus der Quelldatei einbeziehen möchten, klicken Sie für jeden Seitenbereich, den Sie hinzufügen möchten, im Feld [!UICONTROL Pages] auf <strong>[!UICONTROL Element hinzufügen]</strong>, geben Sie dann die erste und letzte Seite des einzuschließenden Seitenbereichs ein und klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong>. Sie können mehrere Seitenbereiche aus einem einzelnen Dokument einbeziehen.</p> </li> 
     <li value="4"> <p>Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Komprimieren Sie PDF-Dateien]

Dieses Aktionsmodul nimmt eine PDF-Datei und komprimiert sie. Dies kann nützlich sein, um Bandbreite oder Speicher zu sparen.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss im PDF-Format vorliegen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Komprimierungsgrad]</td> 
   <td>Wählen Sie die Komprimierungsstufe aus, die Sie verwenden möchten.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Dokument in PDF-Datei konvertieren]

Dieses Tool konvertiert ein Dokument in eine PDF-Datei. Die Quelldatei muss eines der folgenden Dokumentenformate aufweisen:

* DOC
* XLS
* PPT
* TXT
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss in einem der folgenden Formate vorliegen:</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>XLS</p> </li> 
     <li> <p>PPT</p> </li> 
     <li> <p>TXT</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td> <p>Wählen Sie die Standardsprache für das Quelldokument. Dadurch kann das Modul eine geeignete Schriftart auswählen, wenn diese nicht in der Quelldatei enthalten ist.</p> <p>Wählen Sie aus den folgenden Sprachen aus:</p> 
    <ul> 
     <li> <p>en-US (Standard): Englisch (USA)</p> </li> 
     <li> <p>ca-ES: Katalanisch (Spanien)</p> </li> 
     <li> <p>CS-CZ: Tschechisch (Tschechische Republik)</p> </li> 
     <li> <p>da-DK: Dänisch (Dänemark)</p> </li> 
     <li> <p>de-DE: Deutsch (Deutschland)</p> </li> 
     <li> <p>en-AE: Englisch (Vereinigte Arabische Emirate)</p> </li> 
     <li> <p>en-GB: Englisch (Vereinigtes Königreich)</p> </li> 
     <li> <p>en-IL: Englisch (Israel)</p> </li> 
     <li> <p>en-US: Englisch (Vereinigte Staaten von Amerika)</p> </li> 
     <li> <p>es-ES: Spanisch (Spanien)</p> </li> 
     <li> <p>es-MX: Spanisch (Mexiko)</p> </li> 
     <li> <p>eu-ES: Baskisch (Spanien)</p> </li> 
     <li> <p>FI-FI: Finnisch (Finnland)</p> </li> 
     <li> <p>fr-CA: Französisch (Kanada)</p> </li> 
     <li> <p>fr-FR: Französisch (Frankreich)</p> </li> 
     <li> <p>fr-MA: Französisch (Marokko)</p> </li> 
     <li> <p>hr-hr: Kroatisch (Kroatien)</p> </li> 
     <li> <p>hu-hu: Ungarisch (Ungarn)</p> </li> 
     <li> <p>it-IT: Italienisch (Italien)</p> </li> 
     <li> <p>JA-JP: Japanisch (Japan)</p> </li> 
     <li> <p>kr-KR: Koreanisch (Südkorea)</p> </li> 
     <li> <p>NB-NO: Norwegisch Bokmål (Norwegen)</p> </li> 
     <li> <p>NL-NL: Niederländisch (Niederlande)</p> </li> 
     <li> <p>PL-PL: Polnisch (Polen)</p> </li> 
     <li> <p>pt-BR: Portugiesisch (Brasilien)</p> </li> 
     <li> <p>PT-PT: Portugiesisch (Portugal)</p> </li> 
     <li> <p>ro-RO: Rumänisch (Rumänien)</p> </li> 
     <li> <p>RU-RU: Russisch (Russland)</p> </li> 
     <li> <p>SK-SK: Slowakisch (Slowakei)</p> </li> 
     <li> <p>sl-SI: Slowenisch (Slowenien)</p> </li> 
     <li> <p>SV-SE: Schwedisch (Schweden)</p> </li> 
     <li> <p>TR-TR: Türkisch (Türkei)</p> </li> 
     <li> <p>UK-UA: Ukrainisch (Ukraine)</p> </li> 
     <li> <p>zh-CN: Chinesisch (Festlandchina)</p> </li> 
     <li> <p>zh-TW: Chinesisch (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Konvertieren von HTML in PDF-Datei]

Dieses Tool konvertiert eine HTML-Datei in eine PDF-Datei.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Wichtig: Die Source-Datei muss im HTML- oder ZIP-Format vorliegen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON]</td> 
   <td> <p>Wenn Ihr HTML auf JavaScript-Variablen verweist, können Sie diese Variablen hier einbeziehen. </p> <p>Klicken Sie für jede Variable auf <strong>[!UICONTROL Element hinzufügen]</strong> und schließen Sie den Schlüssel und den Wert der Variablen ein.</p> <p>Hinweis:   
     <ul> 
      <li> <p>Beim Erstellen einer PDF aus einer ZIP-Datei muss das Quellmaterial ein Skriptelement enthalten, z. B.: <code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code> </p> </li> 
      <li> <p>Beim Erstellen einer PDF über eine URL wird der Inhalt dieses JSON-Objekts in die VM des Browsers eingefügt, bevor die Seite gerendert wird. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kopf- und Fußzeile einschließen]</td> 
   <td> <p>Aktivieren Sie diese Option, um Kopf- und Fußzeilen für das PDF-Dokument zu erstellen.</p> 
    <ul> 
     <li> <p>Die Kopfzeile enthält ein Datum und den Titel des Dokuments.</p> </li> 
     <li> <p>Die Fußzeile enthält den Dateinamen und eine Seitennummer.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seitenbreite]</td> 
   <td>Geben Sie die Breite des Papiers in Zoll ein. Das -Modul verwendet diese Informationen zum Formatieren der Seiten in der erstellten PDF-Datei.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seitenhöhe]</td> 
   <td>Geben Sie die Höhe des Papiers in Zoll ein. Das -Modul verwendet diese Informationen zum Formatieren der Seiten in der erstellten PDF-Datei.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Konvertieren des Bildes in eine PDF-Datei]

Dieses Tool konvertiert ein Bild in eine PDF-Datei.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Bilddatei der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Konvertieren von PDF in ein Dokument]

Dieses Tool konvertiert eine PDF-Datei in ein -Dokument. Sie können eines der folgenden Formate für die Ausgabedatei auswählen.

* DOC
* DOCX
* PPTX
* XLSX
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss im PDF-Format vorliegen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabedateiformat]</td> 
   <td> <p>Wählen Sie das Format aus, in dem die Dateien ausgegeben werden sollen:</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>DOCX</p> </li> 
     <li> <p>PPTX</p> </li> 
     <li> <p>XLSX</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td> <p>Wählen Sie die Standardsprache für das Quelldokument. Dadurch kann das Modul eine geeignete Schriftart auswählen, wenn diese nicht in der Quelldatei enthalten ist.</p> <p>Wählen Sie aus den folgenden Sprachen aus:</p> 
    <ul> 
     <li> <p>en-US (Standard): Englisch (USA)</p> </li> 
     <li> <p>ca-ES: Katalanisch (Spanien)</p> </li> 
     <li> <p>CS-CZ: Tschechisch (Tschechische Republik)</p> </li> 
     <li> <p>da-DK: Dänisch (Dänemark)</p> </li> 
     <li> <p>de-DE: Deutsch (Deutschland)</p> </li> 
     <li> <p>en-AE: Englisch (Vereinigte Arabische Emirate)</p> </li> 
     <li> <p>en-GB: Englisch (Vereinigtes Königreich)</p> </li> 
     <li> <p>en-IL: Englisch (Israel)</p> </li> 
     <li> <p>en-US: Englisch (Vereinigte Staaten von Amerika)</p> </li> 
     <li> <p>es-ES: Spanisch (Spanien)</p> </li> 
     <li> <p>es-MX: Spanisch (Mexiko)</p> </li> 
     <li> <p>eu-ES: Baskisch (Spanien)</p> </li> 
     <li> <p>FI-FI: Finnisch (Finnland)</p> </li> 
     <li> <p>fr-CA: Französisch (Kanada)</p> </li> 
     <li> <p>fr-FR: Französisch (Frankreich)</p> </li> 
     <li> <p>fr-MA: Französisch (Marokko)</p> </li> 
     <li> <p>hr-hr: Kroatisch (Kroatien)</p> </li> 
     <li> <p>hu-hu: Ungarisch (Ungarn)</p> </li> 
     <li> <p>it-IT: Italienisch (Italien)</p> </li> 
     <li> <p>JA-JP: Japanisch (Japan)</p> </li> 
     <li> <p>kr-KR: Koreanisch (Südkorea)</p> </li> 
     <li> <p>NB-NO: Norwegisch Bokmål (Norwegen)</p> </li> 
     <li> <p>NL-NL: Niederländisch (Niederlande)</p> </li> 
     <li> <p>PL-PL: Polnisch (Polen)</p> </li> 
     <li> <p>pt-BR: Portugiesisch (Brasilien)</p> </li> 
     <li> <p>PT-PT: Portugiesisch (Portugal)</p> </li> 
     <li> <p>ro-RO: Rumänisch (Rumänien)</p> </li> 
     <li> <p>RU-RU: Russisch (Russland)</p> </li> 
     <li> <p>SK-SK: Slowakisch (Slowakei)</p> </li> 
     <li> <p>sl-SI: Slowenisch (Slowenien)</p> </li> 
     <li> <p>SV-SE: Schwedisch (Schweden)</p> </li> 
     <li> <p>TR-TR: Türkisch (Türkei)</p> </li> 
     <li> <p>UK-UA: Ukrainisch (Ukraine)</p> </li> 
     <li> <p>zh-CN: Chinesisch (Festlandchina)</p> </li> 
     <li> <p>zh-TW: Chinesisch (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Konvertieren von PDF in ein Bild]

Dieses Tool konvertiert einen PDF in ein Bild im PNG- oder JPEG-Format, das dann als Liste ausgegeben oder in einer ZIP-Datei kombiniert wird.

Wenn es als ZIP-Datei ausgegeben wird, wird die PDF in ein Bild pro Seite konvertiert, und jedes Bild endet mit der Seitenzahl. Die Bilddateien werden dann zu einer ZIP-Datei zusammengefasst.

Beispielsweise würde eine Datei namens „TestFile“ mit acht Seiten acht Bilder erzeugen, „TestFile_1“ bis „TestFile_8“. Die Ausgabe des Moduls ist eine ZIP-Datei mit den 8 Bildern.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss im PDF-Format vorliegen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabedateiformat]</td> 
   <td> <p>Wählen Sie das Format aus, in dem die Dateien ausgegeben werden sollen:</p> 
    <ul> 
     <li>PNG</li> 
     <li>JPEG</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabetyp]</td> 
   <td> <p>Wählen Sie aus, ob die Dateien als Liste von Dateien oder als ZIP-Datei ausgegeben werden sollen.</td> 
  </tr> 
  <tr> 
 </tbody> 
</table>

### [!UICONTROL Text/Tabelle extrahieren]

Mit diesem Aktionsmodul können Sie Daten aus einer PDF-Datei extrahieren. Das Modul gibt einzelne Textelemente aus, z. B. einen Absatz oder den Text in einer einzelnen Zelle einer Tabelle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Elemente, die als JSON extrahiert werden sollen]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL -Text]</p> </li> 
     <li> <p>[!UICONTROL -Tabellen]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Begrenzungsrahmen extrahieren?]</td> 
   <td>Aktivieren Sie diese Option, um Daten über den Begrenzungsrahmen des Textes zu extrahieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stilinformationen für die Ausgabe einschließen?]</td> 
   <td>Aktivieren Sie diese Option, um der JSON-Ausgabe Stilinformationen hinzuzufügen.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Dokument generieren]

Das [!UICONTROL Generate Document]-Modul ist eine leistungsstarke Methode, um eine PDF zu erstellen, die ausgewählte Daten enthält. Sie können sie mit einer [!DNL Microsoft Word]-Vorlage formatieren oder Daten im JSON-Format bereitstellen.

Weitere Informationen zur Funktion [!UICONTROL [!DNL Adobe PDF Services] Dokument generieren &#x200B;] Sie unter [Überblick über die Dokumenterstellung](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html) in der [!DNL Adobe Document Services].

* [Verwenden des Moduls [!UICONTROL Dokument generieren] mit einer  [!DNL Microsoft Word] -Vorlage](#use-the-generate-document-module-with-a-microsoft-word-template)
* [Verwenden des Moduls [!UICONTROL Dokument generieren] mit JSON](#use-the-generate-document-module-with-json)

#### Verwenden des [!UICONTROL Generate Document]-Moduls mit einer [!DNL Microsoft Word] Vorlage


>[!NOTE]
>
>Weitere Informationen zu Microsoft Word-Vorlagen finden Sie unter [Microsoft Word-Vorlagenmodule](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md).
>
>Sie müssen keine Microsoft Word-Vorlagenmodule verwenden, um eine Microsoft Word-Vorlage mit dem PDF Services Generate Document-Modul zu verwenden.


Um das Modul [!UICONTROL Dokument generieren] mit einer [!UICONTROL Microsoft Word]-Vorlage zu verwenden, müssen Sie zunächst die Vorlage erstellen. Anweisungen hierzu finden Sie in der [!DNL Microsoft Office]-Dokumentation unter „Erstellen einer Vorlage“.

Füllen Sie die Modulfelder [!UICONTROL Dokument generieren] wie folgt aus:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Diese Quelldatei ist die [!DNL Microsoft Word] Vorlage, die das -Modul zum Generieren der neuen PDF verwendet.</p> <p>Es wird empfohlen, ein Projekt in [!DNL Workfront] für die [!DNL Microsoft Word] Vorlagen zu erstellen, die Sie in [!DNL Workfront Fusion] verwenden. Anschließend können Sie das Modul [!DNL Workfront] &gt; [!UICONTROL Dokument herunterladen] verwenden, um die entsprechende Vorlage in Ihr Szenario zu ziehen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabeformat]</td> 
   <td> <p>Format des erstellten Dokuments auswählen.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Daten für Zusammenführung]</td> 
   <td> <p>Füllen Sie für jedes Wert-Tag in Ihrer Vorlage, das Sie durch Text ersetzen möchten, Folgendes aus:</p> 
    <ul> 
     <li> <p>[!UICONTROL -Schlüssel]</p> <p>Einen Schlüssel eingeben. In der Vorlage entspricht der Schlüssel dem Text, der im Wert -Tag angezeigt wird. Wenn Sie beispielsweise Text im Wert-Tag-<code>&#123;&#123;name&#125;&#125;</code> platzieren möchten, geben Sie <code>name </code>im Schlüsselfeld ein.</p> </li> 
     <li> <p>Werttyp</p> <p>Wählen Sie aus, ob die Daten im Wertfeld ein Wert, ein Objekt oder ein Array von Objekten sind.</p> </li> 
     <li> <p>[!UICONTROL -Wert]</p> <p>Geben Sie den Text ein, der im generierten Dokument anstelle des Wert-Tags angezeigt werden soll, oder ordnen Sie ihn zu.</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Verwenden des Moduls [!UICONTROL Dokument generieren] mit JSON

Um das Modul [!UICONTROL Dokument generieren] mit JSON zu verwenden, füllen Sie die Felder wie folgt aus:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabeformat]</td> 
   <td> <p>Format des erstellten Dokuments auswählen.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Daten für Zusammenführung]</td> 
   <td> <p>Um JSON in diesem Modul verwenden zu können, müssen Sie die Zuordnung für dieses Feld aktivieren.</p> <p>Geben Sie die JSON-Datei ein, aus der das Dokument generiert werden soll, oder ordnen Sie sie zu. </p> <p>Sie können JSON direkt in dieses Feld eingeben oder die JSON-Ausgabe aus einem JSON-Modul zuordnen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Linearisieren einer PDF-Datei]

Dieses Tool linearisiert ein PDF-Dokument, um ein Web-optimiertes PDF-Dokument zu erstellen. Ein linearisiertes PDF-Dokument kann Seite für Seite angezeigt werden, ohne dass das gesamte Dokument heruntergeladen werden muss.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul erstellt eine benutzerdefinierte HTTP-Anfrage an die PDF Services-API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> Geben Sie einen relativen Pfad oder eine URL ein. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen automatisch hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Felder]</td> 
   <td> <p>Klicken Sie für jedes Feld, das Sie dem API-Aufruf hinzufügen möchten, <b> „Element hinzufügen</b> und geben Sie den Schlüssel und den optionalen Wert des Felds ein.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### [!UICONTROL OCR für PDF-Datei]

Mit diesem Tool wird die optische Zeichenerkennung (OCR) für eine Datei durchgeführt und ein PDF erstellt.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Wählen Sie die Sprache dieses Dokuments aus.<p>Sprachoptionen finden Sie unter <a href="#convert-document-to-pdf-file" class="MCXref xref" >Dokument in PDF-Datei </a>) in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL OCR-Typ]</td> 
   <td> 
    <ul> 
     <li> <p>Der Typ [!UICONTROL Geändertes Originalbild] stellt sicher, dass Text durchsuchbar und auswählbar ist, ändert aber das Originalbild während des Bereinigungsprozesses (z. B. entzerrt), bevor er eine unsichtbare Textebene darüber platziert. Dieser Typ entfernt unerwünschte Artefakte und kann in einigen Szenarien zu einem besser lesbaren Dokument führen. </p> </li> 
     <li> <p>Der Typ [!UICONTROL Unchanged original image] überlagert ebenfalls eine durchsuchbare Textebene über dem Originalbild, aber in diesem Fall ist das Originalbild unverändert. Dieser Typ erzeugt maximale Wiedergabetreue gegenüber dem Originalbild.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Seitenbearbeitung]

Mit diesem Modul können Sie Seiten in einem PDF-Dokument selektiv drehen oder löschen. Sie können beispielsweise die Hochformat- in die Querformat-Ansicht ändern oder bestimmte Seiten aus dem PDF-Dokument entfernen.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Aktion]</td> 
   <td> <p>Wählen Sie die Aktion aus, die Sie mit der Datei durchführen möchten.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL DELETE]</b> </p> <p>Wählen Sie diese Option, um Seiten aus dem Dokument zu löschen.</p><p>Klicken Sie für jeden Seitenbereich, den Sie löschen möchten, auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie dann die erste und letzte Seite des Seitenbereichs ein. </p> <p>Hinweis:   
     <ul> 
      <li> <p>Sie können negative Zahlen verwenden, um vom Ende des Dokuments zurückzuzählen. Die letzte Seite eines Dokuments ist -1, die vorletzte Seite -2 usw.</p> </li> 
      <li> <p>Um eine einzelne Seite zu löschen, legen Sie dieselbe Seitennummer als Beginn und Ende des Bereichs fest.</p></ul> </li> 
     <li> <p><b>[!UICONTROL Rotate]</b> </p> <p>Wählen Sie diese Option, um Seiten zu drehen, und geben Sie dann den Winkel (in Grad im Uhrzeigersinn) ein, um den die Dokumentseiten relativ zu ihrer Anfangsausrichtung gedreht werden sollen.</p> <p>Um von Hochformat zu Querformat oder umgekehrt zu drehen, drehen Sie die Seite um 90 oder 270 Grad.</p> <p>Wenn eine Seite umgedreht ist, drehen Sie sie um 180 Grad.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pages]</td> 
   <td> <p>Klicken Sie für jeden Seitenbereich, den Sie löschen möchten, auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie dann die erste und letzte Seite des Seitenbereichs ein. </p> <p>Hinweis:   
     <ul> 
      <li> <p>Sie können negative Zahlen verwenden, um vom Ende des Dokuments zurückzuzählen. Die letzte Seite eines Dokuments ist -1, die vorletzte Seite -2 usw.</p> </li> 
      <li> <p>Um eine einzelne Seite zu löschen, legen Sie dieselbe Seitennummer als Beginn und Ende des Bereichs fest.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Automatisches Tagging der Barrierefreiheit von PDF]

Dieses Aktionsmodul erstellt eine PDF, die für Anwendungsfälle mit Barrierefreiheit getaggt wird. Außerdem wird ein optionaler Microsoft Excel-Bericht erstellt, der Probleme auflistet und Fehlerbehebungen vorschlägt.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shift-Überschriften]</td> 
   <td> <p>Aktivieren Sie diese Option, um Überschriften im Dokument zu verschieben.</p> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bericht generieren]</td> 
   <td> <p>Aktivieren Sie diese Option, um einen Bericht zu generieren, der Zugänglichkeitsprobleme in der PDF zusammen mit ihrem Speicherort auflistet und Vorschläge zur Behebung dieser Probleme gibt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF-Dateieigenschaften]

Dieses Tool extrahiert grundlegende Informationen über das Dokument, z. B.:

* Seitenzahl
* PDF-Version
* Ob die Datei verschlüsselt ist
* Ob die Datei linearisiert ist
* ob die Datei eingebettete Dateien enthält

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Schützen einer PDF-Datei]

Dieses Tool sichert ein PDF-Dokument mit einem Benutzer- oder Besitzerkennwort. Außerdem werden Einschränkungen für bestimmte Funktionen wie Drucken, Bearbeiten und Kopieren im PDF-Dokument festgelegt. Sie wählen den Typ des zu verschlüsselnden Inhalts und den Verschlüsselungsalgorithmus aus.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss im PDF-Format vorliegen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kennwortschutztyp]</td> 
   <td> <p>Aktivieren Sie diese Option, um Kennwörter zum Verschlüsseln des PDF-Eingabedokuments zu verwenden. Wenn Sie diese Option aktivieren, müssen Sie einen Wert für eine oder beide der folgenden Optionen angeben und eingeben: </p> 
    <ul> 
     <li> <p>[!UICONTROL -Benutzerkennwort]</p> </li> 
     <li> <p>[!UICONTROL Besitzerkennwort] </p> </li> 
    </ul> <p>Jedes Kennwort kann bis zu 128 Zeichen lang sein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verschlüsselungsalgorithmus]</td> 
   <td> <p>Wählen Sie den Verschlüsselungsalgorithmus. </p> 
    <ul> 
     <li> <p>[!UICONTROL AES-128-Verschlüsselung]</p> <p>Das Passwort unterstützt nur LATEIN-I-Zeichen. </p> </li> 
     <li> <p>[!UICONTROL AES-256-Verschlüsselung]</p> <p>Das Kennwort unterstützt den Unicode-Zeichensatz</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zu verschlüsselnder Inhalt]</td> 
   <td> <p>Wählen Sie den Typ des zu verschlüsselnden Inhalts aus.</p> 
    <ul> 
     <li> <p>[!UICONTROL Alle Inhalte]</p> </li> 
     <li> <p>[!UICONTROL Alle Inhalte außer Metadaten]</p> </li> 
     <li> <p>[!UICONTROL Nur eingebettete Daten] </p> </li> 
    </ul> <p>Durch die Auswahl von "[!UICONTROL Only embedded data]" werden alle bereitgestellten Zugriffsberechtigungen als unwirksam gerendert.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Berechtigungen]</td> 
   <td> <p>Wählen Sie alle Berechtigungen aus, die Sie einbeziehen möchten, um das Drucken, Bearbeiten oder Kopieren von Inhalten zuzulassen.</p> <p>Berechtigungseinstellungen werden nur verwendet, wenn im Feld [!UICONTROL Kennwortschutztyp] das [!UICONTROL Kennwort für Inhaber] festgelegt ist.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Entfernen des Schutzes einer PDF-Datei]

Mit diesem Tool wird die Sicherheit (Kennwortschutz) von einem PDF-Dokument entfernt.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss im PDF-Format vorliegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kennwort]</td> 
   <td>Geben Sie das Passwort ein, mit dem die Datei derzeit geschützt ist.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF-Datei teilen]

Dieses Aktionsmodul teilt ein PDF-Dokument in mehrere kleinere Dokumente auf. Geben Sie an, ob die Seite nach Anzahl der Dateien, Seiten pro Datei oder Seitenbereichen aufgeteilt werden soll.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe PDF Services] finden Sie unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe PDF Services]</a> in diesem Artikel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss im PDF-Format vorliegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split-Option]</td> 
   <td>Wählen Sie aus, wie die Datei aufgeteilt werden soll. 
   <ul>
   <li><p><b>Seitenbereiche</b></p><p>Klicken Sie für jeden Seitenbereich, den Sie in ein separates Dokument aufteilen möchten, auf <b>Hinzufügen</b> und geben Sie die Seite, auf der Sie beginnen möchten, und die Seite, auf der Sie enden möchten, ein.</p></li>
   <li><p><b>Seitenzahl</b></p><p>Geben Sie die Anzahl der Seiten ein, die in die neuen Dokumente aufgenommen werden sollen.</p></li>
   <li><p><b>Dateianzahl</b></p><p>Geben Sie die Anzahl der Dateien mit gleichmäßiger Größe ein, in die Sie das Dokument aufteilen möchten.</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

