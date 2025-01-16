---
title: ServiceNow-Module
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die  [!DNL ServiceNow] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 0%

---

# [!DNL ServiceNow]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL ServiceNow] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um [!DNL ServiceNow]-Module verwenden zu können, müssen Sie über ein [!DNL ServiceNow]-Konto verfügen.

## ServiceNow-API-Informationen

Der ServiceNow-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://{{connection.instance}}/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL ServiceNow] mit [!DNL Workfront Fusion] verbinden

So erstellen Sie eine Verbindung für Ihre [!DNL ServiceNow]:

1. Klicken Sie **[!UICONTROL Add]** neben dem [!UICONTROL Connection], wenn Sie mit der Konfiguration des ersten [!DNL ServiceNow] beginnen.
1. Geben Sie Folgendes ein:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Einen Namen für die neue [!DNL ServiceNow] eingeben</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Username]</p> </td> 
      <td>Geben Sie Ihren [!DNL ServiceNow] Benutzernamen ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>Geben Sie Ihr ServiceNow-Kennwort ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Instance]</p> </td> 
      <td> <p>Geben Sie die Adresse Ihres [!DNL ServiceNow] Kontos ohne <code>https://</code> ein (normalerweise <code>&lt;company>.service-now.com</code>).</p> </td> 
     </tr> 
    </tbody> 
   </table>

   <!--Markdown placeholder-->

## [!UICONTROL ServiceNow] Module und ihre Felder

Beim Konfigurieren [!DNL ServiceNow] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL ServiceNow] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>Wenn in einem Feld &quot;[!UICONTROL Record type]&quot; ein benutzerdefinierter Datensatz ausgewählt ist, kann es einige Zeit dauern, bis die benutzerdefinierten Felder geladen sind.
>
>Wenn keine benutzerdefinierten Datensätze vorhanden sind, ist die Dropdown-Liste leer.

* [[!UICONTROL Watch records]](#watch-records)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Deactivate a User]](#deactivate-a-user)
* [[!UICONTROL Download an attachment]](#download-an-attachment)
* [[!UICONTROL Upload an attachment]](#upload-an-attachment)
* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Delete a record]](#delete-a-record)
* [[!UICONTROL Search for records]](#search-for-records)

### [!UICONTROL Watch records]

Dieses Trigger-Modul aktiviert ein Szenario, wenn ein Datensatz erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Wählen Sie aus, ob es sich bei der Tabelle, die Sie beobachten möchten, um eine benutzerdefinierte Tabelle oder eine Standardtabelle handelt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Wählen Sie den Typ des Datensatzes aus, den Sie beobachten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Wählen Sie den Typ der Werte aus, die Sie anzeigen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Wählen Sie die Felder aus, die das Modul ausgeben soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Wählen Sie aus, ob neue oder aktualisierte Datensätze überwacht werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Custom API Call]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL ServiceNow]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL ServiceNow] nicht durchgeführt werden kann.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Relative URL]</td> 
   <td> <p>Geben Sie die Adresse auf dem Webserver ein, mit der das Modul interagieren soll.</p> <p>Sie können eine relative URL eingeben, was bedeutet, dass Sie das Protokoll (z. B. <code>http://</code>) nicht am Anfang einschließen müssen. Dies weist den Webserver darauf hin, dass die Interaktion auf dem Server stattfindet.</p> <p>Beispiel: <code>[!DNL /api/conversations].create</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Read a record]

Dieses Aktionsmodul liest einen [!DNL ServiceNow]-Datensatz unter Verwendung der System-ID.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>Geben Sie die eindeutige [!DNL ServiceNow]-ID des Datensatzes ein, den das Modul lesen soll, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Wählen Sie aus, ob sich der Datensatz, den Sie lesen möchten, in einer benutzerdefinierten Tabelle oder einer Standardtabelle befindet.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Wählen Sie den Typ [!DNL ServiceNow] Datensatzes aus, den das Modul lesen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Wählen Sie den Typ der Werte aus, die Sie anzeigen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Wählen Sie die Felder aus, die das Modul ausgeben soll.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Deactivate a User]

Dieses Aktionsmodul deaktiviert einen Benutzer in [!DNL ServiceNow] mithilfe der System-ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User System ID]</td> 
   <td> Geben Sie die eindeutige [!DNL ServiceNow]-ID des Benutzers ein, den Sie das Modul deaktivieren möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Download an attachment]

Dieses Aktionsmodul lädt eine Anlage in einem [!DNL ServiceNow] herunter.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment System ID]</td> 
   <td> Geben Sie die eindeutige [!DNL ServiceNow]-ID des Anhangs ein, den das Modul herunterladen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Upload an attachment]

Dieses Aktionsmodul lädt eine Anlage in einen [!DNL ServiceNow].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table name]</td> 
   <td>Geben Sie den Namen der Tabelle ein, in die Sie die Anlage hochladen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>Geben Sie die eindeutige [!DNL ServiceNow]-ID des Systems ein, in das Sie die Anlage hochladen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Namen für den Anhang eingeben oder zuordnen</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File content]</td> 
   <td>Geben Sie die Datei ein, die Sie in [!DNL ServiceNow] hochladen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Create a record]

Dieses Aktionsmodul erstellt einen neuen [!DNL ServiceNow].

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Wählen Sie aus, ob Sie einen Datensatz in einer benutzerdefinierten Tabelle oder einer Standardtabelle erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Wählen Sie den Typ [!DNL ServiceNow] Datensatzes aus, den das Modul erstellen soll. Anschließend können Sie die verfügbaren Felder für diesen Datensatztyp ausfüllen.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a record]

Dieses Aktionsmodul erstellt einen neuen [!DNL ServiceNow].

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>Geben Sie die eindeutige [!DNL ServiceNow]-ID des Datensatzes ein, den Sie aktualisieren möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Wählen Sie aus, ob sich der zu aktualisierende Datensatz in einer benutzerdefinierten Tabelle oder einer Standardtabelle befindet.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Wählen Sie den Typ [!DNL ServiceNow] Datensatzes aus, den das Modul aktualisieren soll. Anschließend können Sie die verfügbaren Felder für diesen Datensatztyp ausfüllen.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a record]

Dieses Aktionsmodul löscht einen Vorfall oder einen Benutzer.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Wählen Sie aus, ob Sie einen Vorfall oder einen Benutzer löschen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>Geben Sie die eindeutige [!DNL ServiceNow]-ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Search for records]

Dieses Modul sucht mithilfe ausgewählter Kriterien nach Datensätzen.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>Wählen Sie aus, ob die zu durchsuchende Tabelle eine benutzerdefinierte Tabelle oder eine Standardtabelle ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Wählen Sie den Typ des Datensatzes aus, nach dem Sie suchen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Wählen Sie aus, ob das Modul alle Datensätze zurückgeben soll, die den Kriterien entsprechen, oder nur den ersten Eintrag, der damit übereinstimmt. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal count of records]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search type]</td> 
   <td> <p>Wählen Sie aus, welchen Suchtyp das Modul ausführen soll.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Advanced query]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Query]</p> <p>Geben Sie die benutzerdefinierte Suchabfrage ein. Informationen zum [!DNL ServiceNow] benutzerdefinierter Suchabfragen finden Sie in der <a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">ServiceNow-Abfragedokumentation</a>.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Simple]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Criteria]</p> <p>Geben Sie die Kriterien ein, nach denen das Modul suchen soll. <!--For more information on setting up search filters, see <a href="." class="MCXref xref">Add a filter to a scenario in Adobe Workfront Fusion</a>.</p>--> </li> 
       <li> <p>[!UICONTROL Sort by]</p> <p>Geben Sie an, nach welchem Feld das Modul die Ergebnisse sortieren soll und ob sie auf- oder absteigend sortiert werden sollen.</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Wählen Sie den Typ der Werte aus, die Sie anzeigen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Wählen Sie die Felder aus, die das Modul ausgeben soll.</td> 
  </tr> 
 </tbody> 
</table>
