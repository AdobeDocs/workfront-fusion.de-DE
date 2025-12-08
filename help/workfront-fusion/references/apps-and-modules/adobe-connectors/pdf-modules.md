---
title: Adobe PDF Services
description: Adobe PDF Services
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: ht
source-wordcount: '4151'
ht-degree: 100%

---

# [!DNL Adobe PDF Services]

Mit den [!DNL Adobe PDF Services] von Adobe Workfront Fusion können Sie Daten aus einer PDF-Datei extrahieren oder aus von Ihnen bereitgestellten Daten eine neue PDF-Datei generieren. Darüber hinaus können Sie eine Vielzahl von Dateitypen in PDFs oder PDFs in andere Dateitypen konvertieren. Mit PDF Services können Sie außerdem Metadaten einer PDF-Datei kombinieren, komprimieren oder lesen sowie den Kennwortschutz für die Datei steuern.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Erstellen von Szenarios: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

Informationen über die für PDF Services verwendete API finden Sie unter [Adobe Document Generation-API](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html).

## Sicherheitshinweise bei der Verwendung der [!DNL Adobe PDF Services]

Die [!DNL Adobe PDF Services] können Ihre Dateien lesen, konvertieren oder ändern, aber weder [!DNL Adobe] noch Workfront Fusion speichern Ihre Dateien oder Daten. Das bedeutet:

* Sie behalten die Kontrolle über Ihre Dateien, einschließlich ihrer Sicherheit
* Sie benötigen kein [!UICONTROL Adobe]-Speicher- oder Cloud-Speicherkonto, um PDF Services zu verwenden.

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

Um eine OAuth-Server-zu-Server-Verbindung zu erstellen, müssen Sie die Adobe PDF Services-API in Ihrer Adobe Developer Console hinzufügen. Wählen Sie beim Hinzufügen der API die OAuth-Server-zu-Server-Option aus.

Anweisungen finden Sie unter [Hinzufügen einer API zu einem Projekt mithilfe von OAuth-Benutzerauthentifizierungs-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication) in der Entwicklerdokumentation von Adobe.

## Informationen zur Adobe PDF Services-API

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

## Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe PDF Services]-Module:

1. Klicken Sie in einem beliebigen [!DNL Adobe PDF Services]-Modul neben dem Feld „Verbindung“ auf **[!UICONTROL Hinzufügen]**.

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
            <p>Wählen Sie aus, ob eine Server-zu-Server-Verbindung oder eine JWT-Verbindung erstellt werden soll.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Verbindungsname]</td>
          <td>
            <p>Geben Sie einen Namen für die Verbindung ein.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-ID]</td>
          <td>Geben Sie Ihre [!DNL Adobe]-[!UICONTROL Client-ID] ein. Diese finden Sie im Abschnitt mit den [!UICONTROL Anmeldeinformationen] der [!DNL Adobe Developer Console].<p>Anweisungen zum Auffinden von Anmeldeinformationen finden Sie unter <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication?lang=de#credentials" class="MCXref xref" >Anmeldeinformationen</a> in der Entwicklerdokumentation von Adobe.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
          <td>Geben Sie Ihr [!DNL Adobe]-[!UICONTROL Client-Geheimnis] ein. Dieses finden Sie im Abschnitt mit den [!UICONTROL Anmeldeinformationen] der [!DNL Adobe Developer Console].<p>Anweisungen zum Auffinden von Anmeldeinformationen finden Sie unter <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication?lang=de#credentials" class="MCXref xref" >Anmeldeinformationen</a> in der Entwicklerdokumentation von Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID des technischen Kontos] (nur JWT)</td>
          <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL ID des technischen Kontos] ein. Diese finden Sie im Abschnitt mit den [!UICONTROL Anmeldeinformationen-Details] der [!DNL Adobe Developer Console].<p>Anweisungen zum Auffinden von Anmeldeinformationen finden Sie unter <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication?lang=de#credentials" class="MCXref xref" >Anmeldeinformationen</a> in der Entwicklerdokumentation von Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Organisations-ID] (nur JWT)</td>
          <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL Organisations-ID] ein. Diese finden Sie im Abschnitt mit den [!UICONTROL Anmeldeinformationen] der [!DNL Adobe Developer Console].<p>Anweisungen zum Auffinden von Anmeldeinformationen finden Sie unter <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication?lang=de#credentials" class="MCXref xref" >Anmeldeinformationen</a> in der Entwicklerdokumentation von Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Metabereiche] (nur JWT)</td>
          <td>
            Geben Sie alle für die Verbindung erforderlichen Metabereiche ein.
          </td>
        </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Privater Schlüssel]</td>
        <td>
          <p>Wenn Sie eine JWT-Verbindung ausgewählt haben, geben Sie den privaten Schlüssel ein, der beim Erstellen Ihrer Anmeldeinformationen in der [!DNL Adobe Developer Console] generiert wurde. </p>
          <p>So extrahieren Sie Ihren privaten Schlüssel oder Ihr Zertifikat:</p>
          <ol>
            <li value="1">
              <p>Klicken Sie auf <b>[!UICONTROL Extrahieren]</b>.</p>
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
1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Verbindung zu speichern und zum Modul zurückzukehren.


## [!DNL Adobe PDF Services]-Module und ihre Felder

Beim Konfigurieren der [!DNL PDF Services] werden in Workfront Fusion die unten aufgeführten Felder angezeigt. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL PDF-Dateien kombinieren]](#combine-pdf-files)
* [[!UICONTROL PDF-Dateien komprimieren]](#compress-pdf-files)
* [[!UICONTROL Dokument in PDF-Datei konvertieren]](#convert-document-to-pdf-file)
* [[!UICONTROL HTML in PDF-Datei konvertieren]](#convert-html-to-pdf-file)
* [[!UICONTROL Bild in PDF-Datei konvertieren]](#convert-image-to-pdf-file)
* [[!UICONTROL PDF in Dokument konvertieren]](#convert-pdf-to-document)
* [[!UICONTROL PDF in Bild konvertieren]](#convert-pdf-to-image)
* [[!UICONTROL Text/Tabelle extrahieren]](#extract-text--table)
* [[!UICONTROL Dokument generieren]](#generate-document)
* [[!UICONTROL PDF-Datei linearisieren]](#linearize-a-pdf-file)
* [Benutzerdefinierten API-Aufruf erstellen](#make-a-custom-api-call)
* [[!UICONTROL OCR für PDF-Datei]](#ocr-for-pdf-file)
* [[!UICONTROL Seitenbearbeitung]](#page-manipulation)
* [[!UICONTROL PDFs für Barrierefreiheit automatisch taggen]](#pdf-accessibility-auto-tag)
* [[!UICONTROL PDF-Dateieigenschaften]](#pdf-file-properties)
* [[!UICONTROL PDF-Datei schützen]](#protect-pdf-file)
* [[!UICONTROL Schutz einer PDF-Datei aufheben]](#remove-protection-of-a-pdf-file)
* [PDF-Datei teilen](#split-a-pdf-file)

### [!UICONTROL PDF-Dateien kombinieren]

Dieses Aktionsmodul kombiniert mehrere PDF-Dateien in einer PDF-Datei. Beispielsweise könnten Sie mit diesem Modul alle Dokumente in einem [!UICONTROL Workfront]-Projekt nach Abschluss des Projekts in einem einzigen PDF kombinieren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokumente]</td> 
   <td> <p>Sie können ein Aggregatormodul verwenden, um Dokumente zu sammeln, die in einer PDF-Datei kombiniert werden sollen. Sie können die Dokumente aber auch manuell hinzufügen. </p> <p>Es wird empfohlen, ein [!UICONTROL Array-Aggregator]-Modul zu verwenden, um eine Ausgabe aus einem vorherigen Modul zu aggregieren. Bei Verwendung eines Aggregators müssen Sie Namen, Speicherorte oder Anzahl der zu kombinierenden Dateien nicht kennen. Ein Aggregator ist daher gegenüber der manuellen Eingabe der zu kombinierenden Dokumente deutlich flexibler und skalierbarer.</p> <p>Um das Dateimodul „[!UICONTROL PDF kombinieren]“ mit einem Aggregator verwenden zu können, müssen Sie die Zuordnung für das Feld „[!UICONTROL Dokumente]“ aktivieren. </p> <p>In diesem Beispiel identifiziert das Modul „[!UICONTROL Verwandte Einträge lesen]“ die mit einem Projekt verknüpften Dokumente, die dann vom Modul „[!UICONTROL Dokumente herunterladen]“ jeweils heruntergeladen werden. Alle PDFs werden in einem Array aggregiert, das an das Dateimodul „[!UICONTROL PDF kombinieren]“ übergeben wird.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>Sie können Dokumente auch manuell eingeben.</p> <p>Gehen Sie für jedes Dokument, das in die kombinierte PDF-Datei eingeschlossen werden soll, wie folgt vor:</p> 
    <ol> 
     <li value="1"> <p>Klicken Sie auf „[!UICONTROL Dokument hinzufügen]“.</p> </li> 
     <li value="2"> <p>Wählen Sie im Feld „[!UICONTROL Quelldatei]“ das Modul aus, das das einzuschließende Dokument ausgibt, oder ordnen Sie den Namen und die Daten der Quelldatei zu. </p> </li> 
     <li value="3"> <p>(Optional) Wenn Sie nur bestimmte Seiten aus der Quelldatei einschließen möchten, klicken Sie für jeden hinzuzufügenden Seitenbereich im Feld „[!UICONTROL Seiten]“ auf <strong>[!UICONTROL Element hinzufügen]</strong>. Geben Sie anschließend die erste und letzte Seite des einzuschließenden Seitenbereichs ein und klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong>. Sie können mehrere Seitenbereiche aus einem einzelnen Dokument einschließen.</p> </li> 
     <li value="4"> <p>Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF-Dateien komprimieren]

Dieses Aktionsmodul komprimiert eine PDF-Datei. Dies kann nützlich sein, um Bandbreite oder Speicher einzusparen.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss im PDF-Format vorliegen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Komprimierungsstufe]</td> 
   <td>Wählen Sie die gewünschte Komprimierungsstufe aus.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Dokument in PDF-Datei konvertieren]

Dieses Tool konvertiert ein Dokument in eine PDF-Datei. Die Quelldatei muss eines der folgenden Dokumentformate aufweisen:

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
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
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
   <td role="rowheader">[!UICONTROL Sprache]</td> 
   <td> <p>Wählen Sie die Standardsprache für das Quelldokument. Dadurch kann das Modul eine geeignete Schrift auswählen, wenn diese nicht in der Quelldatei enthalten ist.</p> <p>Wählen Sie aus den folgenden Sprachen aus:</p> 
    <ul> 
     <li> <p>en-US (Standard): Englisch (USA)</p> </li> 
     <li> <p>ca-ES: Katalanisch (Spanien)</p> </li> 
     <li> <p>cs-CZ: Tschechisch (Tschechische Republik)</p> </li> 
     <li> <p>da-DK: Dänisch (Dänemark)</p> </li> 
     <li> <p>de-DE: Deutsch (Deutschland)</p> </li> 
     <li> <p>en-AE: Englisch (Vereinigte Arabische Emirate)</p> </li> 
     <li> <p>en-GB: Englisch (Vereinigtes Königreich)</p> </li> 
     <li> <p>en-IL: Englisch (Israel)</p> </li> 
     <li> <p>en-US: Englisch (USA)</p> </li> 
     <li> <p>es-ES: Spanisch (Spanien)</p> </li> 
     <li> <p>es-MX: Spanisch (Mexiko)</p> </li> 
     <li> <p>eu-ES: Baskisch (Spanien)</p> </li> 
     <li> <p>fi-FI: Finnisch (Finnland)</p> </li> 
     <li> <p>fr-CA: Französisch (Kanada)</p> </li> 
     <li> <p>fr-FR: Französisch (Frankreich)</p> </li> 
     <li> <p>fr-MA: Französisch (Marokko)</p> </li> 
     <li> <p>hr-HR: Kroatisch (Kroatien)</p> </li> 
     <li> <p>hu-HU: Ungarisch (Ungarn)</p> </li> 
     <li> <p>it-IT: Italienisch (Italien)</p> </li> 
     <li> <p>ja-JP: Japanisch (Japan)</p> </li> 
     <li> <p>kr-KR: Koreanisch (Südkorea)</p> </li> 
     <li> <p>nb-NO: Norwegisches Bokmål (Norwegen)</p> </li> 
     <li> <p>nl-NL: Niederländisch (Niederlande)</p> </li> 
     <li> <p>pl-PL: Polnisch (Polen)</p> </li> 
     <li> <p>pt-BR: Portugiesisch (Brasilien)</p> </li> 
     <li> <p>pt-PT: Portugiesisch (Portugal)</p> </li> 
     <li> <p>ro-RO: Rumänisch (Rumänien)</p> </li> 
     <li> <p>ru-RU: Russisch (Russland)</p> </li> 
     <li> <p>sk-SK: Slowakisch (Slowakei)</p> </li> 
     <li> <p>sl-SI: Slowenisch (Slowenien)</p> </li> 
     <li> <p>sv-SE: Schwedisch (Schweden)</p> </li> 
     <li> <p>tr-TR: Türkisch (Türkei)</p> </li> 
     <li> <p>uk-UA: Ukrainisch (Ukraine)</p> </li> 
     <li> <p>zh-CN: Chinesisch (Festlandchina)</p> </li> 
     <li> <p>zh-TW: Chinesisch (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL HTML in PDF-Datei konvertieren]

Dieses Tool konvertiert eine HTML-Datei in eine PDF-Datei.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Wichtig: Die Quelldatei muss im HTML- oder ZIP-Format vorliegen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON]</td> 
   <td> <p>Wenn Ihr HTML-Code auf JavaScript-Variablen verweist, können Sie diese Variablen hier einschließen. </p> <p>Klicken Sie für jede Variable auf <strong>[!UICONTROL Element hinzufügen]</strong> und schließen Sie den Schlüssel und den Wert der Variablen ein.</p> <p>Hinweis:   
     <ul> 
      <li> <p>Beim Erstellen einer PDF-Datei aus einer ZIP-Datei muss das Quellmaterial ein Skriptelement wie <code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code> enthalten. </p> </li> 
      <li> <p>Beim Erstellen einer PDF-Datei über eine URL wird der Inhalt dieses JSON-Objekts in die VM des Browsers eingefügt, bevor die Seite gerendert wird. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kopf- und Fußzeile einschließen]</td> 
   <td> <p>Aktivieren Sie diese Option, um Kopf- und Fußzeilen für das PDF-Dokument zu erstellen.</p> 
    <ul> 
     <li> <p>Die Kopfzeile enthält ein Datum und den Dokumenttitel.</p> </li> 
     <li> <p>Die Fußzeile enthält den Dateinamen und eine Seitenzahl.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seitenbreite]</td> 
   <td>Geben Sie die Breite des Papiers in Zoll ein. Das Modul nutzt diese Informationen zum Formatieren der Seiten in der erstellten PDF-Datei.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seitenhöhe]</td> 
   <td>Geben Sie die Höhe des Papiers in Zoll ein. Das Modul nutzt diese Informationen zum Formatieren der Seiten in der erstellten PDF-Datei.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Bild in PDF-Datei konvertieren]

Dieses Tool konvertiert ein Bild in eine PDF-Datei.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Quelldatei und die Bilddatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF in Dokument konvertieren]

Dieses Tool konvertiert eine PDF-Datei in ein Dokument. Sie können eines der folgenden Formate für die Ausgabedatei auswählen.

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
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
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
   <td role="rowheader">[!UICONTROL Sprache]</td> 
   <td> <p>Wählen Sie die Standardsprache für das Quelldokument. Dadurch kann das Modul eine geeignete Schrift auswählen, wenn diese nicht in der Quelldatei enthalten ist.</p> <p>Wählen Sie aus den folgenden Sprachen aus:</p> 
    <ul> 
     <li> <p>en-US (Standard): Englisch (USA)</p> </li> 
     <li> <p>ca-ES: Katalanisch (Spanien)</p> </li> 
     <li> <p>cs-CZ: Tschechisch (Tschechische Republik)</p> </li> 
     <li> <p>da-DK: Dänisch (Dänemark)</p> </li> 
     <li> <p>de-DE: Deutsch (Deutschland)</p> </li> 
     <li> <p>en-AE: Englisch (Vereinigte Arabische Emirate)</p> </li> 
     <li> <p>en-GB: Englisch (Vereinigtes Königreich)</p> </li> 
     <li> <p>en-IL: Englisch (Israel)</p> </li> 
     <li> <p>en-US: Englisch (USA)</p> </li> 
     <li> <p>es-ES: Spanisch (Spanien)</p> </li> 
     <li> <p>es-MX: Spanisch (Mexiko)</p> </li> 
     <li> <p>eu-ES: Baskisch (Spanien)</p> </li> 
     <li> <p>fi-FI: Finnisch (Finnland)</p> </li> 
     <li> <p>fr-CA: Französisch (Kanada)</p> </li> 
     <li> <p>fr-FR: Französisch (Frankreich)</p> </li> 
     <li> <p>fr-MA: Französisch (Marokko)</p> </li> 
     <li> <p>hr-HR: Kroatisch (Kroatien)</p> </li> 
     <li> <p>hu-HU: Ungarisch (Ungarn)</p> </li> 
     <li> <p>it-IT: Italienisch (Italien)</p> </li> 
     <li> <p>ja-JP: Japanisch (Japan)</p> </li> 
     <li> <p>kr-KR: Koreanisch (Südkorea)</p> </li> 
     <li> <p>nb-NO: Norwegisches Bokmål (Norwegen)</p> </li> 
     <li> <p>nl-NL: Niederländisch (Niederlande)</p> </li> 
     <li> <p>pl-PL: Polnisch (Polen)</p> </li> 
     <li> <p>pt-BR: Portugiesisch (Brasilien)</p> </li> 
     <li> <p>pt-PT: Portugiesisch (Portugal)</p> </li> 
     <li> <p>ro-RO: Rumänisch (Rumänien)</p> </li> 
     <li> <p>ru-RU: Russisch (Russland)</p> </li> 
     <li> <p>sk-SK: Slowakisch (Slowakei)</p> </li> 
     <li> <p>sl-SI: Slowenisch (Slowenien)</p> </li> 
     <li> <p>sv-SE: Schwedisch (Schweden)</p> </li> 
     <li> <p>tr-TR: Türkisch (Türkei)</p> </li> 
     <li> <p>uk-UA: Ukrainisch (Ukraine)</p> </li> 
     <li> <p>zh-CN: Chinesisch (Festlandchina)</p> </li> 
     <li> <p>zh-TW: Chinesisch (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF in Bild konvertieren]

Dieses Tool konvertiert eine PDF-Datei in ein Bild im PNG- oder JPEG-Format, das dann als Liste ausgegeben oder in einer ZIP-Datei kombiniert wird.

Wenn sie als ZIP-Datei ausgegeben wird, wird die PDF-Datei in ein Bild pro Seite konvertiert, und jedes Bild endet mit der Seitenzahl. Die Bilddateien werden dann in einer ZIP-Datei kombiniert.

Beispielsweise werden bei einer Datei namens „Testdatei“ mit acht Seiten acht Bilder erzeugt: „Testdatei_1“ bis „Testdatei_8“. Die Ausgabe des Moduls ist eine ZIP-Datei mit den acht Bildern.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
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

Mit diesem Aktionsmodul können Sie Daten aus einer PDF-Datei extrahieren. Das Modul gibt einzelne Textelemente aus, z. B. einen Absatz oder den Text in einer einzelnen Zelle einer Tabelle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Als JSON zu extrahierende Elemente]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Text]</p> </li> 
     <li> <p>[!UICONTROL Tabellen]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Begrenzungsrahmen extrahieren?]</td> 
   <td>Aktivieren Sie diese Option, um Daten über den Begrenzungsrahmen des Texts zu extrahieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stilinformationen für Ausgabe einschließen?]</td> 
   <td>Aktivieren Sie diese Option, um der JSON-Ausgabe Stilinformationen hinzuzufügen.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Dokument generieren]

Das Modul [!UICONTROL Dokument generieren] liefert eine leistungsstarke Methode, um eine PDF-Datei mit den von Ihnen ausgewählten Daten zu erstellen. Sie können sie mit einer [!DNL Microsoft Word]-Vorlage formatieren oder Daten im JSON-Format bereitstellen.

Weitere Informationen zur [!UICONTROL [!DNL Adobe PDF Services]-Funktionalität „Dokument generieren“] finden Sie in der [!DNL Adobe Document Services]-Dokumentation unter [Überblick über die Dokumenterstellung](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html).

* [Verwenden des Moduls [!UICONTROL Dokument generieren] mit einer  [!DNL Microsoft Word] -Vorlage](#use-the-generate-document-module-with-a-microsoft-word-template)
* [Verwenden des Moduls [!UICONTROL Dokument generieren] mit JSON](#use-the-generate-document-module-with-json)

#### Verwenden des Moduls [!UICONTROL Dokument generieren] mit einer [!DNL Microsoft Word]-Vorlage


>[!NOTE]
>
>Weitere Informationen zu Microsoft Word-Vorlagen finden Sie unter [Microsoft Word-Vorlagenmodule](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md).
>
>Sie müssen keine Microsoft Word-Vorlagenmodule verwenden, um eine Microsoft Word-Vorlage mit dem PDF-Services-Modul „Dokument generieren“ nutzen zu können.


Um das Modul [!UICONTROL Dokument generieren] mit einer [!UICONTROL Microsoft Word]-Vorlage zu verwenden, müssen Sie zunächst die Vorlage erstellen. Anweisungen hierzu finden Sie in der [!DNL Microsoft Office]-Dokumentation unter „Erstellen einer Vorlage“.

Füllen Sie die Modulfelder [!UICONTROL Dokument generieren] wie folgt aus:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Diese Quelldatei ist die [!DNL Microsoft Word]-Vorlage, die das Modul zum Generieren der neuen PDF-Datei verwendet.</p> <p>Es wird empfohlen, ein Projekt in Workfront für die [!DNL Microsoft Word]-Vorlagen zu erstellen, die Sie in Workfront Fusion verwenden. Anschließend können Sie das Modul unter „Workfront“ &gt; „[!UICONTROL Dokument herunterladen]“ verwenden, um die entsprechende Vorlage in Ihr Szenario einzufügen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabeformat]</td> 
   <td> <p>Wählen Sie das Format für das generierte Dokument aus:</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Daten für Zusammenführung]</td> 
   <td> <p>Geben Sie für jedes in Ihrer Vorlage durch Text zu ersetzende Wert-Tag Folgendes an:</p> 
    <ul> 
     <li> <p>[!UICONTROL Schlüssel]</p> <p>Geben Sie einen Schlüssel ein. In der Vorlage entspricht der Schlüssel dem Text, der im Wert-Tag angezeigt wird. Wenn Sie beispielsweise Text im Wert-Tag <code>&#123;&#123;name&#125;&#125;</code> platzieren möchten, geben Sie <code>name </code>in das Feld „Schlüssel“ ein.</p> </li> 
     <li> <p>Werttyp</p> <p>Wählen Sie aus, ob es sich bei den Daten im Wertfeld um einen Wert, ein Objekt oder ein Array von Objekten handelt.</p> </li> 
     <li> <p>[!UICONTROL Wert]</p> <p>Geben Sie den Text ein, der im generierten Dokument anstelle des Wert-Tags angezeigt werden soll, oder ordnen Sie diesen zu.</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Verwenden des Moduls [!UICONTROL Dokument generieren] mit JSON

Um das Modul [!UICONTROL Dokument generieren] mit JSON zu verwenden, füllen Sie die nachstehenden Felder wie folgt aus:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabeformat]</td> 
   <td> <p>Wählen Sie das Format für das generierte Dokument aus:</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Daten für Zusammenführung]</td> 
   <td> <p>Um JSON in diesem Modul verwenden zu können, müssen Sie die Zuordnung für dieses Feld aktivieren.</p> <p>Geben Sie die JSON-Datei ein, aus der das Dokument generiert werden soll, oder ordnen Sie diese zu. </p> <p>Sie können JSON direkt in dieses Feld eingeben oder die JSON-Ausgabe aus einem JSON-Modul zuordnen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF-Datei linearisieren]

Dieses Tool linearisiert ein PDF-Dokument, um ein Web-optimiertes PDF-Dokument zu erstellen. Ein linearisiertes PDF-Dokument kann seitenweise angezeigt werden, ohne dass dazu das gesamte Dokument heruntergeladen werden muss.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Benutzerdefinierten API-Aufruf erstellen

Dieses Aktionsmodul erstellt eine benutzerdefinierte HTTP-Anfrage an die PDF Services-API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> Geben Sie einen relativen Pfad oder eine URL ein. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Header]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungs-Header automatisch hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Felder]</td> 
   <td> <p>Klicken Sie für jedes dem API-Aufruf hinzufügende Feld auf <b>Element hinzufügen</b> und geben Sie den Schlüssel und den optionalen Wert des Felds ein.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrem JSON-Objekt verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### [!UICONTROL OCR für PDF-Datei]

Mit diesem Tool wird die optische Zeichenerkennung (Optical Character Recognition, OCR) auf eine Datei angewendet und eine PDF-Datei erstellt.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sprache]</td> 
   <td>Wählen Sie die Sprache dieses Dokuments aus.<p>Weitere Informationen zu Sprachoptionen finden Sie in diesem Artikel unter <a href="#convert-document-to-pdf-file" class="MCXref xref" >Dokument in PDF-Datei konvertieren</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL OCR-Typ]</td> 
   <td> 
    <ul> 
     <li> <p>Wenn Sie den Typ „[!UICONTROL Geändertes Originalbild]“ auswählen, ist der Text durchsuchbar und auswählbar. Allerdings wird das Originalbild während der Bereinigung geändert (z. B. begradigt), bevor eine unsichtbare Textebene darüber platziert wird. Bei diesem Typ werden unerwünschte Artefakte entfernt, was in bestimmten Szenarios zu einem besser lesbaren Dokument führen kann. </p> </li> 
     <li> <p>Wenn Sie den Typ „[!UICONTROL Unverändertes Originalbild]“ auswählen, wird das Originalbild ebenfalls mit einer durchsuchbaren Textebene überlagert. In diesem Fall bleibt das Originalbild aber unverändert. Dieser Typ führt zu maximaler Wiedergabetreue gegenüber dem Originalbild.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Seitenbearbeitung]

Mit diesem Modul können Sie Seiten in einem PDF-Dokument selektiv drehen oder löschen. Sie können beispielsweise eine Ansicht im Hochformat in eine Ansicht im Querformat ändern oder bestimmte Seiten aus dem PDF-Dokument entfernen.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aktion]</td> 
   <td> <p>Wählen Sie die Aktion aus, die für die Datei durchgeführt werden soll.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Löschen]</b> </p> <p>Wählen Sie diese Option aus, um Seiten aus dem Dokument zu löschen.</p><p>Klicken Sie für jeden zu löschenden Seitenbereich auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie dann die erste und letzte Seite des Seitenbereichs ein. </p> <p>Hinweis:   
     <ul> 
      <li> <p>Sie können negative Zahlen verwenden, um vom Ende des Dokuments zurückzuzählen. Die letzte Seite eines Dokuments entspricht der Zahl „-1“, die vorletzte Seite „-2“ usw.</p> </li> 
      <li> <p>Um eine einzelne Seite zu löschen, legen Sie dieselbe Seitenzahl als Beginn und Ende des Bereichs fest.</p></ul> </li> 
     <li> <p><b>[!UICONTROL Drehen]</b> </p> <p>Wählen Sie diese Option aus, um Seiten zu drehen, und geben Sie dann den Winkel (in Grad im Uhrzeigersinn) ein, um den die Dokumentseiten relativ zu ihrer Anfangsausrichtung gedreht werden sollen.</p> <p>Um vom Hochformat ins Querformat oder umgekehrt zu wechseln, drehen Sie die Seite um 90 bzw. 270 Grad.</p> <p>Wenn eine Seite auf dem Kopf steht, drehen Sie sie um 180 Grad.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seiten]</td> 
   <td> <p>Klicken Sie für jeden zu löschenden Seitenbereich auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie dann die erste und letzte Seite des Seitenbereichs ein. </p> <p>Hinweis:   
     <ul> 
      <li> <p>Sie können negative Zahlen verwenden, um vom Ende des Dokuments zurückzuzählen. Die letzte Seite eines Dokuments entspricht der Zahl „-1“, die vorletzte Seite „-2“ usw.</p> </li> 
      <li> <p>Um eine einzelne Seite zu löschen, legen Sie dieselbe Seitenzahl als Beginn und Ende des Bereichs fest.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschränkung]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDFs für Barrierefreiheit automatisch taggen]

Dieses Aktionsmodul erstellt eine PDF-Datei, die für Anwendungsfälle mit Barrierefreiheit getaggt ist. Außerdem wird ein optionaler Microsoft Excel-Bericht erstellt, in dem Probleme aufgelistet sind und Fehlerbehebungen vorschlagen werden.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Überschriften verschieben]</td> 
   <td> <p>Aktivieren Sie diese Option, um Überschriften im Dokument zu verschieben.</p> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bericht generieren]</td> 
   <td> <p>Aktivieren Sie diese Option, um einen Bericht zu generieren, in dem Probleme hinsichtlich der Barrierefreiheit in der PDF-Datei samt Fehlerort aufgelistet sind und der Vorschläge zur Behebung dieser Probleme enthält.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF-Dateieigenschaften]

Dieses Tool extrahiert grundlegende Informationen zum Dokument, z. B.:

* Seitenzahl
* PDF-Version
* ob die Datei verschlüsselt ist
* ob die Datei linearisiert ist
* ob die Datei eingebettete Dateien enthält

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF-Datei schützen]

Dieses Tool schützt ein PDF-Dokument mit einem Benutzer- oder Besitzerkennwort. Außerdem werden Einschränkungen für bestimmte Funktionen wie Drucken, Bearbeiten und Kopieren im PDF-Dokument festgelegt. Sie bestimmen den Typ des zu verschlüsselnden Inhalts und den Verschlüsselungsalgorithmus.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss im PDF-Format vorliegen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Typ des Kennwortschutzes]</td> 
   <td> <p>Aktivieren Sie diese Option, um das PDF-Eingabedokument mithilfe von Kennwörtern zu verschlüsseln. Wenn Sie diese Option aktivieren, müssen Sie einen Wert für eine oder beide der folgenden Optionen angeben und eingeben: </p> 
    <ul> 
     <li> <p>[!UICONTROL Benutzerkennwort]</p> </li> 
     <li> <p>[!UICONTROL Besitzerkennwort] </p> </li> 
    </ul> <p>Jedes Kennwort kann bis zu 128 Zeichen lang sein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verschlüsselungsalgorithmus]</td> 
   <td> <p>Legen Sie den Verschlüsselungsalgorithmus fest. </p> 
    <ul> 
     <li> <p>[!UICONTROL AES-128-Verschlüsselung]</p> <p>Das Kennwort unterstützt nur LATIN-I-Zeichen. </p> </li> 
     <li> <p>[!UICONTROL AES-256-Verschlüsselung]</p> <p>Das Kennwort unterstützt den Unicode-Zeichensatz.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zu verschlüsselnder Inhalt]</td> 
   <td> <p>Wählen Sie den Typ des zu verschlüsselnden Inhalts aus:</p> 
    <ul> 
     <li> <p>[!UICONTROL Alle Inhalte]</p> </li> 
     <li> <p>[!UICONTROL Alle Inhalte außer Metadaten]</p> </li> 
     <li> <p>[!UICONTROL Nur eingebettete Daten] </p> </li> 
    </ul> <p>Durch Auswahl der Option „[!UICONTROL Nur eingebettete Daten]“ werden alle bereitgestellten Zugriffsberechtigungen unwirksam.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Berechtigungen]</td> 
   <td> <p>Wählen Sie alle Berechtigungen aus, die erteilt werden sollen, um das Drucken, Bearbeiten oder Kopieren von Inhalten zuzulassen.</p> <p>Berechtigungseinstellungen werden nur verwendet, wenn im Feld „[!UICONTROL Typ des Kennwortschutzes]“ die Option „[!UICONTROL Besitzerkennwort]“ ausgewählt ist.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Schutz einer PDF-Datei aufheben]

Dieses Tool hebt die Sicherheit (den Kennwortschutz) eines PDF-Dokuments auf.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss im PDF-Format vorliegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kennwort]</td> 
   <td>Geben Sie das Kennwort ein, mit dem die Datei derzeit geschützt ist.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF-Datei teilen]

Dieses Aktionsmodul teilt ein PDF-Dokument in mehrere kleinere Dokumente auf. Geben Sie an, ob es nach der Anzahl der Dateien, der Seiten pro Datei oder Seitenbereichen geteilt werden soll.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die für dieses Modul verwendet werden soll.</p> Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe PDF Services] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe PDF Services]</a>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p>Die Quelldatei muss im PDF-Format vorliegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilungsoption]</td> 
   <td>Wählen Sie aus, wie die Datei geteilt werden soll: 
   <ul>
   <li><p><b>Seitenbereiche</b></p><p>Klicken Sie für jeden Seitenbereich, der in ein separates Dokument aufgeteilt werden soll, auf <b>Hinzufügen</b> und geben Sie die Seite ein, auf der das Dokument beginnen und enden soll.</p></li>
   <li><p><b>Seitenzahl</b></p><p>Geben Sie die Anzahl der Seiten ein, die in die neuen Dokumente eingeschlossen werden sollen.</p></li>
   <li><p><b>Dateianzahl</b></p><p>Geben Sie die Anzahl gleich großer Dateien ein, in die das Dokument aufgeteilt werden soll.</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

