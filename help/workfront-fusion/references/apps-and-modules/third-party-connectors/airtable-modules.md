---
title: Airtable-Module
description: Adobe Workfront Fusion erfordert zusätzlich zu einer Adobe Workfront-Lizenz eine Adobe Workfront Fusion-Lizenz.
author: Becky
feature: Workfront Fusion
exl-id: 3b445b50-5812-4ded-9788-f467991e0b52
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1890'
ht-degree: 2%

---

# Airtable-Module


Mit dem [!DNL Airtable]-Connector für Adobe Workfront Fusion können Sie ein Szenario starten, das auf Ereignissen in Ihrem [!DNL Airtable] basiert, Datensätze erstellen, hochladen und aktualisieren, Datensätze suchen und benutzerdefinierte API-Aufrufe an die Airtable-API durchführen.

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Plan*</td>
  <td> <p>[!UICONTROL Pro] oder höher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz*</td>
   <td> <p>[!UICONTROL -Plan], [!UICONTROL -Arbeit]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td> <p>[!UICONTROL Workfront Fusion for Work Automation and Integration] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>Ihr Unternehmen muss Adobe Workfront Fusion sowie Adobe Workfront erwerben, um die in diesem Artikel beschriebenen Funktionen nutzen zu können.</td> 
  </tr> 
 </tbody> 
</table>

Wenden Sie sich an Ihren Workfront-Administrator, um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Voraussetzungen

Sie müssen über ein Airtable-Konto verfügen, um die Funktion in diesem Artikel verwenden zu können.

<!--
<p>For more information, see the tutorial .</p>
-->

## Airtable API-Informationen

Der Airtable-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://api.airtable.com/v0</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v3.3.28</td> 
  </tr>
 </tbody> 
 </table>

## Airtable mit Workfront Fusion verbinden {#connect-airtable-to-workfront-fusion}

<!--

1. Log in to your Airtable account.
1. Open your account overview and generate the API key.
-->
1. Öffnen Sie Workfront Fusion und **Sie das Dialogfeld** Verbindung erstellen“ des gewünschten Moduls.
1. Geben Sie einen Namen für die Verbindung ein.
1. (Optional) Klicken Sie auf Erweiterte Einstellungen anzeigen und geben Sie Ihre Airtable-Client-ID und Ihren geheimen Client-Schlüssel ein.
1. Klicken Sie auf **Fortfahren**, um die Verbindung herzustellen und zum Modul zurückzukehren.

## Flugfähige Module und ihre Felder

### Einträge

* [Datensatz erstellen](#create-a-record)
* [Löschen eines Datensatzes](#delete-a-record)
* [Datensatz abrufen](#get-a-record)
* [Datensätze suchen](#search-records)
* [Aktualisieren eines Datensatzes](#update-a-record)
* [Eintrag aktualisieren](#upsert-a-record)
* [Einträge beobachten](#watch-records)
* [Antworten ansehen](#watch-responses)
* [Durchführen eines API-Aufrufs](#make-an-api-call)

#### Erstellen eines Datensatzes {#create-a-record}

Dieses Aktionsmodul erstellt einen neuen Datensatz.

Sie geben die Daten an, die im Datensatz gespeichert werden sollen, und legen fest, wo sie gespeichert werden sollen.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Airtable-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Verbinden von Airtable mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Wählen Sie die Basis aus, zu der der neue Datensatz gehören soll.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabelle </td> 
   <td> <p>Wählen Sie die Tabelle aus, zu der der neue Datensatz gehören soll.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Eintrag</p> </td> 
   <td> <p>Geben Sie die Werte für den neuen Datensatz ein. Die verfügbaren Felder basieren auf der von Ihnen ausgewählten Tabelle.</p> <!--<p>For more information on field types, search for "Supported field types" in the Airtable documentation.</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>Multiple lines of text, which may contain "mention tokens", for example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong> : Add the attachment. Airtable will download the file from the provided <code>url</code> and keep its own copy of it. If the File name field is left empty, Airtable generates the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05 (ISO 8601 formatted date)</li> 
     <li>Phone number:</li> 
     <li><strong>Emails</strong>: A valid email address.</li> 
     <li><strong>URL</strong>: A valid URL (for example, airtable.com or https://airtable.com/universe).</li> 
     <li><strong>Number</strong>: Enter a number.</li> 
     <li><strong>Currency</strong>: Currency value.</li> 
     <li><strong>Percent</strong>: A percentage value. Must be higher than or equal to 0.</li> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation. </li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs will be reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Intelligente Links</td> 
   <td> <p>Aktivieren Sie diese Option, um Namen anstelle von Datensatz-IDs in Felder einzugeben, die mit einer anderen Tabelle verknüpft sind. Der Datensatz wird automatisch in der verknüpften Tabelle erstellt, wenn keine Übereinstimmung vorliegt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Löschen eines Datensatzes {#delete-a-record}

Dieses Aktionsmodul löscht einen bestimmten Datensatz.

Sie geben die ID und die Speicherorte des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Airtable-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Verbinden von Airtable mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Wählen Sie die Basis aus, die den Datensatz enthält, den Sie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabelle </td> 
   <td> <p>Wählen Sie die Tabelle aus, die den Datensatz enthält, den Sie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Datensatz-ID</td> 
   <td> <p>Geben Sie die eindeutige Airtable-ID des Datensatzes ein, den das Modul löschen soll, oder ordnen Sie sie zu. Sie können die ID abrufen, indem Sie beispielsweise das Modul Datensätze suchen verwenden.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Datensatz abrufen {#get-a-record}

Dieses Aktionsmodul ruft Datensatzdetails ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Airtable-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Verbinden von Airtable mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Wählen Sie die Basis aus, die die Tabelle mit dem abzurufenden Datensatz enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabelle</td> 
   <td> <p> Wählen Sie die Tabelle aus, die den Datensatz enthält, für den Sie Details abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Datensatz-ID</td> 
   <td> <p> Geben Sie die ID des Datensatzes ein, für den Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Datensätze suchen {#search-records}

Dieses Suchmodul sucht in einem Objekt in Airtable nach Datensätzen, die mit der von Ihnen angegebenen Suchabfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Airtable-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Verbinden von Airtable mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Wählen Sie die Basis aus, nach der Sie nach Datensätzen suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabelle </td> 
   <td> <p>Wählen Sie die Tabelle aus, nach der Sie nach Datensätzen suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Formel</p> </td> 
   <td> <p>Eine Formel zum Filtern von Datensätzen. Die Formel wird für jeden Datensatz ausgewertet. Wenn das Ergebnis nicht <code>0</code>, <code>false</code>, <code>""</code>, <code>NaN</code>, <code>[]</code> oder <code>#Error!</code> ist, wird der Datensatz in die Antwort aufgenommen.</p> <p>In Kombination mit dem <code>view</code> werden nur Datensätze in dieser Ansicht zurückgegeben, die der Formel entsprechen.</p> <p>Um beispielsweise nur Datensätze einzuschließen, bei denen Name nicht leer ist, übergeben Sie:<code> NOT({Name} = '')</code></p> <p>Weitere Informationen finden Sie, wenn Sie in der Dokumentation zum Airtable-Support nach Informationen zu Formelfeldverweisen suchen.</p> </td> 
  </tr> 
  <tr> 
   <td>Sortieren </td> 
   <td> <p>Wählen Sie die Sortierrichtung und das Feld aus, nach dem Sie die Ergebnisse sortieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Ansicht </td> 
   <td> <p>Wählen Sie die Ansicht aus, nach der Sie nach Datensätzen suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Limit</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren eines Datensatzes {#update-a-record}

Dieses Aktionsmodul aktualisiert einen bestimmten Datensatz.

Geben Sie die ID des Datensatzes und die neuen Daten an, die er enthalten soll.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Airtable-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Verbinden von Airtable mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Wählen Sie die Basis aus, die den Datensatz enthält, den Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabelle </td> 
   <td> <p>Wählen Sie die Tabelle aus, die den zu aktualisierenden Datensatz enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>Datensatz-ID </td> 
   <td> <p>Geben Sie die eindeutige Airtable-ID des Datensatzes ein, den Sie aktualisieren möchten, oder ordnen Sie sie zu. Sie können die ID abrufen, indem Sie beispielsweise das Modul Datensätze suchen verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Eintrag</p> </td> 
   <td> <p>Geben Sie die Werte für den neuen Datensatz ein. Die verfügbaren Felder hängen von der ausgewählten Tabelle ab.</p> <!--<p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Intelligente Links</td> 
   <td> <p>Geben Sie Namen anstelle von Datensatz-IDs zu Feldern ein, die mit einer anderen Tabelle verknüpft sind. Der Datensatz wird automatisch in der verknüpften Tabelle erstellt, wenn keine Übereinstimmung vorliegt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren eines Datensatzes

Dieses Aktionsmodul aktualisiert oder fügt einen bestimmten Datensatz ein.

Geben Sie die ID des Datensatzes und die neuen Daten an, die er enthalten soll.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Airtable-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Verbinden von Airtable mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Wählen Sie die Basis aus, die den Datensatz enthält, den Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabelle </td> 
   <td> <p>Wählen Sie die Tabelle aus, die den zu aktualisierenden Datensatz enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>Datensatz-ID </td> 
   <td> <p>Wenn Sie einen Datensatz aktualisieren, geben Sie die eindeutige Airtable-ID des Datensatzes ein, den das Modul aktualisieren soll, oder mappen Sie sie. Sie können die ID abrufen, indem Sie beispielsweise das Modul Datensätze suchen verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Eintrag</p> </td> 
   <td> <p>Geben Sie die Werte für den neuen Datensatz ein. Die verfügbaren Felder hängen von der ausgewählten Tabelle ab.</p> <!-- <p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Intelligente Links</td> 
   <td> <p>Geben Sie Namen anstelle von Datensatz-IDs zu Feldern ein, die mit einer anderen Tabelle verknüpft sind. Der Datensatz wird automatisch in der verknüpften Tabelle erstellt, wenn keine Übereinstimmung vorliegt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Einträge beobachten {#watch-records}

Dieses Tabellenmodul startet ein Trigger, wenn ein Datensatz in der angegebenen Tabelle erstellt oder aktualisiert wird.

>[!NOTE]
>
>Um dieses Modul verwenden zu können, müssen Sie in Ihrer Tabelle das Feld Erstellungszeit oder Letzte Änderungszeit erstellen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Airtable-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Verbinden von Airtable mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Basis </td> 
   <td> <p>Wählen Sie die Basis aus, die Sie auf neue Datensätze überwachen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabelle </td> 
   <td> <p>Wählen Sie die Tabelle aus, die auf neue Datensätze überwacht werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Trigger-Konfiguration</p> </td> 
   <td> <p>Feld "Trigger"</p> <p>Ein <code>Created Time</code> oder <code>Last Modified Time</code> Feld, das zum Sortieren von Datensätzen verwendet wird. Wenn Sie in Ihrem Schema kein <code>Created Time</code>- oder <code>Last Modified Time</code> haben, müssen Sie eines erstellen. </p> <p>Titelfeld</p> <p>Ein Feld, das als Bezeichnung für einen Datensatz verwendet wird, z. B. im Dialogfeld „Startpunkt auswählen“.</p> </td> 
  </tr> 
  <tr> 
   <td>Limit</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus überwachen soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>Ansicht</td> 
   <td> <p>Wählen Sie die Ansicht aus, die Sie verwenden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Formel</p> </td> 
   <td> <p>Eine Formel zum Filtern von Datensätzen. Die Formel wird für jeden Datensatz ausgewertet. Wenn das Ergebnis nicht <code>0</code>, <code>false</code>, <code>""</code>, <code>NaN</code>, <code>[]</code> oder <code>#Error!</code> ist, wird der Datensatz in die Antwort aufgenommen.</p> <p>In Kombination mit dem <code>view</code> werden nur Datensätze in dieser Ansicht zurückgegeben, die der Formel entsprechen.</p> <p>Um beispielsweise nur Datensätze einzuschließen, bei denen Name nicht leer ist, übergeben Sie:<code> NOT({Name} = '')</code></p> <p>Weitere Informationen finden Sie in den Informationen zu Formelfeldverweisen in der Dokumentation zum Airtable-Support .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Antworten ansehen

Dieses Trigger-Modul startet ein Szenario, wenn ein Formular gesendet wird.

>[!NOTE]
>
>Diese Funktion ist nur für den kostenpflichtigen Airtable Pro-Plan verfügbar.

Die Webhook-URL muss in Workfront Fusion generiert und dann zur Formularkonfiguration in Airtable hinzugefügt werden.

1. Fügen Sie das Modul Neue Antworten ansehen zu Ihrem Workfront Fusion-Szenario hinzu.
1. Erstellen und kopieren Sie die Webhook-URL.

   <!--For instructions, see [ (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/).-->

1. Melden Sie sich bei Ihrem Airtable-Konto an.
1. Öffnen Sie die Basis und die Tabelle, die Sie für das Formular verwenden möchten, und erstellen Sie eine Formularansicht.
1. Legen Sie das Formular nach Bedarf fest, scrollen Sie im Formular nach unten und aktivieren Sie die Option Umleiten zur URL nach der Übermittlung des Formulars.
1. Geben Sie die in Schritt 2 generierte Webhook-URL in das angezeigte Dialogfeld ein und fügen Sie die ?record_id={record_id} unmittelbar nach der Webhook-URL hinzu, um die Datensatz-ID in die Ausgabe des Moduls aufzunehmen. Klicken Sie dann auf Speichern. Die resultierende URL sieht z. B. wie folgt aus:
1. Kehren Sie zu Ihrem Workfront Fusion-Szenario zurück und führen Sie das Modul Antworten beobachten nur aus, um Felder aus Airtable zu laden und diese Felder den anderen Modulen zuordnen zu können.
1. Senden des Formulars in Airtable, wobei die Option Umleiten an URL nach dem Senden des Formulars aktiviert ist und Webhook-URL hinzugefügt wurde (Schritt 6 oben).

   Das Modul Antworten beobachten wird ausgelöst und die gewünschten Daten werden geladen.

1. Fügen Sie das Modul Airtable > Get a Record unmittelbar nach dem Modul Airtable > Watch Responses hinzu und ordnen Sie die record_id dem Feld Record ID zu.

Jedes Mal, wenn das Formular übermittelt wird, wird das Modul Antworten beobachten in Ihrem Workfront Fusion-Szenario ausgelöst und das Modul Datensatz abrufen gibt die übermittelten Formulardetails zurück.

#### Durchführen eines API-Aufrufs

#### Benutzerdefinierter API-Aufruf

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Airtable]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Airtable] nicht durchgeführt werden kann.

Die Aktion basiert auf dem von Ihnen angegebenen Entitätstyp (Allocadia-Objekttyp).

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Verbindung</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Airtable-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Verbinden von Airtable mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://api.airtable.com/</code> ein. Beispiel: <code>v0/{base}/{table}</code> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Methode</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kopfzeilen</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Abfragezeichenfolge</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form von Schlüssel und Wert hinzu</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Textkörper</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
