---
title: DocuSign-Module
description: Mit  [!DNL Adobe Workfront Fusion DocuSign]  Modulen können Sie den Umschlagstatus überwachen und abrufen, Umschläge suchen und abrufen oder ein Dokument herunterladen und senden, um sich bei Ihrem  [!DNL DocuSign]  anzumelden.
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1631'
ht-degree: 0%

---

# DocuSign-Module

Mit den [!DNL Adobe Workfront Fusion] [!DNL DocuSign]-Modulen können Sie den Umschlagstatus überwachen und abrufen, Umschläge suchen und abrufen oder ein Dokument herunterladen und senden, um sich bei Ihrem [!DNL DocuSign]-Konto anzumelden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

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

Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Voraussetzungen

Um [!DNL DocuSign]-Module verwenden zu können, müssen Sie über ein [!DNL DocuSign]-Konto verfügen.

## DocuSign-API-Informationen

Der DocuSign-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>1.18.11</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL DocuSign] mit [!DNL Workfront Fusion] verbinden {#connect-docusign-to-workfront-fusion}

So erstellen Sie eine Verbindung für Ihre [!DNL DocuSign]:

1. Klicken Sie **[!UICONTROL Add]** neben dem [!UICONTROL Connection], wenn Sie mit der Konfiguration des ersten [!DNL DocuSign] beginnen.
1. Geben Sie Folgendes ein:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Einen Namen für die neue [!DNL DocuSign] eingeben</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Account type]</td> 
      <td>Wählen Sie aus, ob das Konto, mit dem Sie eine Verbindung herstellen möchten, ein Produktionskonto oder ein Demokonto ist.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fahren Sie fort wie in [Verbindung herstellen mit [!DNL Adobe Workfront Fusion]  - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md#connect) beschrieben.

## [!DNL DocuSign] Module und ihre Felder

Beim Konfigurieren [!DNL DocuSign] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL DocuSign] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)

### Auslöser

#### [!UICONTROL Watch envelopes]

Dieses Trigger-Modul startet ein Szenario, in dem ein Umschlag gesendet, zugestellt, signiert, abgeschlossen oder abgelehnt wird.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Wählen Sie das Konto aus, das die Datensätze enthält, die Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p> Wählen Sie den Ereignistyp aus, den Sie beobachten möchten.</p> 
    <ul> 
     <li>[!UICONTROL Document completed]</li> 
     <li>[!UICONTROL Document declined]</li> 
     <li>[!UICONTROL Document sent]</li> 
     <li>[!UICONTROL Document signed]</li> 
     <li>[!UICONTROL New document in Inbox]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Output fields]</p> </td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Modulausgabe aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download a document]](#download-a-document)
* [[!UICONTROL Read an envelope]](#read-an-envelope)
* [[!UICONTROL Upload a file to an envelope]](#upload-a-file-to-an-envelope)
* [[!UICONTROL Create a new envelope]](#create-a-new-envelope)
* [[!UICONTROL Add Recipient to Envelope]](#add-recipient-to-envelope)
* [[!UICONTROL Add custom field]](#add-custom-field)
* [[!UICONTROL Modify custom field]](#modify-custom-field)
* [[!UICONTROL Send envelope]](#send-envelope)

#### [!UICONTROL Custom API Call]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Account]</td> 
   <td>Geben Sie das Konto ein, das Sie für den Zugriff auf die [!DNL DocuSign]-API verwenden möchten, oder ordnen Sie es zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Geben Sie die Adresse auf dem Webserver ein, mit der das Modul interagieren soll.</p> <p>Sie können eine relative URL eingeben, was bedeutet, dass Sie das Protokoll (z. B. <code>http://</code>) nicht am Anfang einschließen müssen. Dies weist den Webserver darauf hin, dass die Interaktion auf dem Server stattfindet.</p> <p>Beispiel: <code>[!DNL /api/conversations].create</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Dadurch wird der Inhaltstyp der Anfrage bestimmt.</p> <p>Beispiel:<code> {"Content-type":"application/json"}</code></p> <p>Hinweis: Wenn Fehler auftreten und es schwierig ist, deren Ursprung zu ermitteln, sollten Sie die Kopfzeilen basierend auf der [!DNL Workfront] Dokumentation ändern. Wenn Ihr benutzerdefinierter API-Aufruf einen 422-HTTP-Anfragefehler zurückgibt, versuchen Sie es mit einer „Content-Type“:„text/plain“-Kopfzeile.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Ergebnissen ein, die während eines Ausführungszyklus bearbeitet werden sollen, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Beispiel:** Listenumschläge
>
>Der folgende API-Aufruf gibt Umschläge ab dem angegebenen Datum in Ihrem [!DNL DocuSign]-Konto zurück:
>
>**URL**: `/v2.1/accounts/{accountId}/envelopes/`
>
>**Methode**: `GET`
>
>**Abfragezeichenfolge**:
>
>* **key**: `from_date`
>
>* **Wert**: `YYYY-MM-DD`
>
>Gibt an, wann mit der Prüfung auf Statusänderungen für Umschläge im Konto begonnen wird.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)
>
>Das Ergebnis finden Sie in der -Ausgabe des Moduls unter Paket > Hauptteil > Umschläge.
>
>In unserem Beispiel wurden 6 Umschläge zurückgegeben:
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

#### [!UICONTROL Download a document]

Dieses Aktionsmodul lädt ein einzelnes Dokument herunter.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Dokument enthält, das Sie herunterladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die Kennung des Umschlags ein, den Sie herunterladen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Document ID]</p> </td> 
   <td> <p>Geben Sie die ID des Dokuments ein, das Sie herunterladen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Certificate]</td> 
   <td>Wählen Sie <strong>[!UICONTROL Yes]</strong> aus, wenn Sie das Envelope-Signaturzertifikat in den Download einbeziehen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents by User ID]</td> 
   <td>Wählen Sie <strong>[!UICONTROL Yes]</strong> aus, wenn Sie Empfängern erlauben möchten, Dokumente nach Benutzer-ID abzurufen. Wenn beispielsweise ein(e) Benutzende(r) in zwei verschiedenen Routing-Aufträgen mit unterschiedlichen Sichtbarkeiten enthalten ist, werden bei Verwendung dieser Option alle Dokumente aus beiden Routen zurückgegeben.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encrypt]</td> 
   <td>Wählen Sie <strong>[!UICONTROL Yes]</strong> aus, wenn die in der Antwort zurückgegebenen PDF-Bytes für alle in Ihrem [!DNL DocuSign]-Konto konfigurierten Schlüsselmanager verschlüsselt werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Wählen Sie die Sprache.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Changes]</td> 
   <td>Bei Festlegung auf <strong>[!UICONTROL Yes]</strong> werden alle geänderten Felder für die zurückgegebene PDF gelb hervorgehoben und optionale Signaturen oder Initialen rot umrandet.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watermark]</td> 
   <td> <p>Wählen Sie <strong>[!UICONTROL No]</strong> aus, um das Wasserzeichen aus den PDF-Dokumenten zu entfernen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read an envelope]

Dieses Aktionsmodul liest Informationen über einen Envelope in [!DNL DocuSign] unter Verwendung der Envelope-ID.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Dokument enthält, dessen Informationen Sie lesen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die ID des Dokuments ein, aus dem Informationen gelesen werden sollen, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Wählen Sie die Eigenschaften aus, die in der Modulausgabe angezeigt werden sollen. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file to an envelope]

Dieses Modul lädt eine angegebene Datei in einen vorhandenen Envelope in DocuSign hoch.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Wählen Sie das Konto aus, das den Umschlag enthält, in den Sie eine Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die ID des Umschlags ein, in den Sie eine Datei hochladen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder geben Sie den Namen und die Daten der Quelldatei ein.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a new envelope]

Dieses Aktionsmodul erstellt aus einer Vorlage einen neuen Umschlag. Gibt die ID des neuen Envelopes sowie den Status des neuen Envelopes zurück.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td>

<td> <p>Anweisungen zum Verbinden Ihres DocuSign-Kontos mit Workfront Fusion finden Sie in den Artikeln unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Account] </td>
   <td> <p>Wählen Sie das Konto aus, das den Umschlag enthält, in den Sie eine Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template]</td>
   <td> <p> Wählen Sie die Vorlage aus, aus der Sie den neuen Umschlag erstellen möchten. Vorlagen sind je nach ausgewähltem [!UICONTROL Account] verfügbar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL After creation]
   </td> 
   <td> <p>Wählen Sie aus, ob Sie den Umschlag als Entwurf speichern oder zum Signieren senden möchten.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template recipients]</td>
    <td>Empfänger dieses Briefumschlags auswählen</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add Recipient to Envelope]

Dieses Aktionsmodul fügt einen oder mehrere Empfänger zu einem vorhandenen Umschlag hinzu. Wenn der Umschlag bereits gesendet wurde, wird dem Empfänger eine E-Mail gesendet. Dieses Modul gilt nicht für Umschläge, die bereits abgeschlossen wurden.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>Anweisungen zum Verbinden Ihres DocuSign-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Account] </td>
   <td> <p>Wählen Sie das Konto aus, das den Umschlag enthält, dem Sie Empfänger hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Envelope ID]</td>
    <td>Wählen Sie die Zuordnung oder die ID des Umschlags aus, dem Sie den Empfänger hinzufügen möchten.</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[!UICONTROL Recipient type]</td>
   <td> <p> Wählen Sie den Empfängertyp aus, den Sie dem Umschlag hinzufügen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agent]</p> </li> 
     <li> <p>[!UICONTROL Carbon copy]</p> </li> 
     <li> <p>[!UICONTROL Certified delivery]</p> </li> 
     <li> <p>[!UICONTROL In-person signer]</p> </li> 
     <li> <p>[!UICONTROL Intermediary]</p> </li> 
     <li> <p>[!UICONTROL Signer]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Email]</td>
   <td> <p>Geben Sie die E-Mail-Adresse des Empfängers ein, den Sie zum Umschlag hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Name]</td>
   <td>Geben Sie den Namen des Empfängers ein, den Sie dem Umschlag hinzufügen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Routing order]</td>
   <td> <p>Routingnummer des Empfängers eingeben oder zuordnen. Die Routing-Nummer bestimmt die Reihenfolge, in der Empfänger Ihre Dokumente erhalten und signieren.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Email body]</td>
   <td>Geben Sie den Text (Inhalt) der E-Mail ein, die an den Empfänger gesendet wird, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Email subject]</td>
   <td>Geben Sie den Betreff der E-Mail ein, die an den Empfänger gesendet wird, oder ordnen Sie ihn zu.</td> 
  </tr> 
    <td role="rowheader">[!UICONTROL Private message]</td>
   <td> <li> <p>Nur der ausgewählte Empfänger sieht die private Nachricht sowie die allgemeine Nachricht. Die private Nachricht ist auf 1.000 Zeichen begrenzt.</p> </li> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Authentication]</td> 
   <td> <p>Wählen Sie die Authentifizierungsmethode aus, mit der Sie die Identität des Empfängers bestätigen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL None]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Access code]</strong> </p> <p>Geben Sie den Zugriffscode ein oder ordnen Sie ihn zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Phone]</strong> </p> <p>Telefonnummer eingeben oder zuordnen</p> </li> 
     <li> <p><strong>[!UICONTROL SMS]</strong> </p> <p>Telefonnummer eingeben oder zuordnen</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add custom field]

Dieses Aktionsmodul fügt dem Dokument ein benutzerdefiniertes Feld hinzu

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Dokument enthält, dem Sie ein benutzerdefiniertes Feld hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die ID des Umschlags ein, der das Dokument enthält, dem Sie ein benutzerdefiniertes Feld hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Geben Sie einen Namen für das neue Feld ein, das Sie hinzufügen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Aktivieren Sie diese Option, wenn das hinzugefügte Feld ein erforderliches Feld sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Aktivieren Sie diese Option, wenn das Feld sichtbar sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Geben Sie den Wert (Inhalt) des hinzugefügten Felds ein oder ordnen Sie ihn zu. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify custom field]

Dieses Aktionsmodul ändert ein benutzerdefiniertes Feld mithilfe des Feldnamens.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Dokument enthält, in dem Sie ein benutzerdefiniertes Feld ändern möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die ID des Umschlags ein, der das Dokument enthält, in dem Sie ein benutzerdefiniertes Feld ändern möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field ID]</td> 
   <td>Geben Sie die ID des Felds ein, das Sie ändern möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Geben Sie den Namen des Felds ein, das Sie ändern möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Aktivieren Sie diese Option, wenn das geänderte Feld ein erforderliches Feld sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Aktivieren Sie diese Option, wenn das Feld sichtbar sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Geben Sie den Wert (Inhalt) des geänderten Felds ein oder ordnen Sie ihn zu. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send envelope]

Dieses Aktionsmodul sendet einen Briefumschlag-Entwurf an seine Empfänger.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Wählen Sie das Konto aus, das den Briefumschlagentwurf enthält, den Sie an die Empfänger senden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die ID des Briefumschlags-Entwurfs ein, den Sie an die Empfänger senden möchten, oder mappen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>
