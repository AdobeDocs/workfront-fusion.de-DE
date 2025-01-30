---
title: Salesforce-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Salesforce verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 3c7c03a7-67ea-4673-90b0-7d0506d9fa10
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '2708'
ht-degree: 0%

---

# [!DNL Salesforce]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Salesforce] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Eine Videoeinführung zum Salesforce-Connector finden Sie unter:

* [Salesforce](https://video.tv.adobe.com/v/3427027/){target=_blank}

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

>[!NOTE]
>
>* Nicht alle Editionen von [!DNL Salesforce] verfügen über API-Zugriff. Weitere Informationen finden Sie in den Informationen zu [!DNL Salesforce] Editionen mit API-Zugriff auf der [!DNL Salesforce] Community-Site.
>* Informationen zu bestimmten Fehlern, die von der [!DNL Salesforce]-API zurückgegeben werden, finden Sie in den Dokumenten zur [!DNL Salesforce]-API. Sie können auch den Status der [!DNL Salesforce]-API auf mögliche Service-Ausfälle überprüfen.
>

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

Um [!DNL Salesforce]-Module verwenden zu können, müssen Sie über ein [!DNL Salesforce]-Konto verfügen.

## Salesforce-API-Informationen

Der Salesforce-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> {connection.instanceUrl}</td>
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v62.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.15.14</td> 
  </tr>
 </tbody> 
 </table>

## Über die Suche nach [!DNL Salesforce] Objekten

Bei der Suche nach Objekten können Sie entweder einzelne Suchbegriffe eingeben oder eine komplexere Abfrage mit Platzhaltern und Operatoren erstellen:

* Verwenden Sie den Sternchen-Platzhalter (\*) als Ersatz für null oder mehr Zeichen. Bei einer Suche nach Ca\* werden beispielsweise Elemente gefunden, die mit Ca beginnen
* Mit einem Fragezeichen (?) als Ersatz für ein einzelnes Zeichen. Bei einer Suche nach Jon?n werden beispielsweise Elemente mit dem Begriff John oder Joan, aber nicht Jon gefunden
* Verwenden Sie den Anführungszeichen-Operator (“ „), um eine exakte Übereinstimmung der Phrasen zu finden. Beispiel: „Montagstreffen“

Weitere Informationen zu Suchmöglichkeiten finden Sie in der [!DNL Salesforce] Entwicklerdokumentation zu SOQL und SOSL.

## Erstellen einer Verbindung zu [!DNL Salesforce]

So erstellen Sie eine Verbindung für Ihre [!DNL Salesforce]:

1. Klicken Sie in einem beliebigen [!DNL Salesforce] auf **[!UICONTROL Add]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Geben Sie einen Namen für die neue Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Wählen Sie aus, ob eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung hergestellt werden soll.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Geben Sie Ihre Salesforce-Client-ID ein.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Geben Sie Ihr Salesforce-Client-Geheimnis ein. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Sandbox]</td>
        <td>Aktivieren Sie diese Option, wenn es sich um eine Sandbox-Umgebung handelt.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL API Version]</td>
        <td>Geben Sie die Version der Salesforce-API ein, die Sie verwenden möchten. Die Standardversion ist 62.0.</td>
      </tr>
    </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu speichern und zum Modul zurückzukehren.


## [!DNL Salesforce] Module und ihre Felder

* [Trigger ](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

* [[!UICONTROL Watch for Records]](#watch-for-records)
* [[!UICONTROL Watch Outbound Messages]](#watch-outbound-messages)
* [[!UICONTROL Watch a field]](#watch-a-field)

#### [!UICONTROL Watch for Records]

Dieses Trigger-Modul führt ein Szenario aus, wenn ein Datensatz in einem Objekt erstellt oder aktualisiert wird. Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz oder den Datensätzen verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Wählen Sie den Typ [!DNL Salesforce] Datensatzes aus, den das Modul überwachen soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Fields]</td> 
   <td>Wählen Sie die Felder aus, die das Modul überwachen soll. Die verfügbaren Felder hängen vom Typ des Datensatzes ab.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal count of records]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Legen Sie fest, ob das Szenario nur neue Datensätze des ausgewählten Typs oder neue Datensätze des ausgewählten Typs und alle anderen Änderungen an Datensätzen dieses Typs sehen soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Outbound Messages]

Dieses Trigger-Modul führt ein Szenario aus, wenn jemand eine Nachricht sendet. Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz oder den Datensätzen verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Dieses Modul erfordert einige zusätzliche Einstellungen:

1. Navigieren Sie zur Seite [!DNL Salesforce].

   Um auf die Setup-Seite zuzugreifen, klicken Sie auf die Schaltfläche mit der Bezeichnung &quot;[!UICONTROL Setup]&quot; in der oberen rechten Ecke des [!DNL Salesforce] Kontos. Suchen Sie auf der Seite &quot;[!DNL Salesforce] Setup“ die Leiste &quot;[!UICONTROL Quick Find / Search]&quot; auf der linken Seite. Suchen Sie nach &quot;[!UICONTROL Workflow Rules].“

1. Klicken Sie auf **[!UICONTROL Workflow Rules]**.
1. Klicken Sie auf der [!UICONTROL Workflow Rules] Seite, die angezeigt wird, auf **[!UICONTROL New Rule]** und wählen Sie den Objekttyp aus, auf den die Regel angewendet werden soll (z. B. &quot;[!UICONTROL Opportunity]&quot;, wenn Sie Aktualisierungen der Opportunity-Datensätze überwachen).
1. Klicken Sie auf **[!UICONTROL Next]**.
1. Legen Sie einen Regelnamen, Bewertungskriterien und Regelkriterien fest und klicken Sie dann auf **[!UICONTROL Save]** und **[!UICONTROL Next]**.

1. Klicken Sie auf **[!UICONTROL Done]**.
1. Klicken Sie in der neu erstellten Workflow-Regel auf **[!UICONTROL Edit]**..
1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Add Workflow Action]** die Option **[!UICONTROL New Outbound Message]** aus.

1. Geben Sie Namen, Beschreibung, Endpunkt-URL und die Felder an, die Sie in die neue ausgehende Nachricht einbeziehen möchten, und klicken Sie dann auf **[!UICONTROL Save]**.

   Das Feld **[!UICONTROL Endpoint URL]** enthält die URL, die auf der [!DNL Salesforce]-[!UICONTROL Outbound Message] in [!DNL Workfront Fusion] angegeben ist.

1. Konfigurieren Sie ein Szenario, das mit dem [!UICONTROL Outbound Message] beginnt.

1. Klicken Sie auf das Symbol **&lt;/>** unten rechts und kopieren Sie die bereitgestellte URL.
1. Kehren Sie zur Seite **[!UICONTROL Workflow Rules]** zurück, suchen Sie die neu erstellte Regel und klicken Sie dann auf **[!UICONTROL Activate]**.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook]</td> 
   <td> <p>Wählen Sie den Webhook aus, mit dem Sie ausgehende Nachrichten beobachten möchten. Um einen Webhook hinzuzufügen, klicken Sie auf <strong>[!UICONTROL Add]</strong> und geben Sie den Namen und die Verbindung des Webhooks ein.</p> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Wählen Sie den Typ [!DNL Salesforce] Datensatzes aus, den das Modul auf ausgehende Nachrichten überwachen soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Fields]</td> 
   <td> <p>Wählen Sie die Felder aus, die das Modul auf ausgehende Nachrichten überwachen soll. Die verfügbaren Felder hängen vom Typ des Datensatzes ab.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### *[!UICONTROL Watch a field]*

Dieses Feldmodul startet ein Trigger, wenn ein Feld in [!DNL Salesforce] aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, der das Feld enthält, das vom Modul überwacht werden soll. Sie müssen einen Datensatztyp auswählen, der in [!DNL Salesforce] Einrichtung aktiviert [!UICONTROL Field History]. Weitere Informationen finden Sie unter <a href="https://help.salesforce.com/articleView?id=tracking_field_history.htm&amp;type=5">Feldverlaufsverfolgung</a> in der [!DNL Salesforce]. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Field]</td> 
   <td> <p>Wählen Sie die Felder aus, die das Modul auf Änderungen überwachen soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Feldern ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Create a Record]](#create-a-record)
* [[!UICONTROL Read a Record]](#read-a-record)
* [[!UICONTROL Delete a Record]](#delete-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Upload Attachment/Document]](#upload-attachmentdocument)
* [[!UICONTROL Download Attachment/Document]](#download-attachmentdocument)
* [Datei hochladen](#upload-file)

#### [!UICONTROL Create a Record]

Dieses Aktionsmodul erstellt einen neuen Datensatz in einem -Objekt.

Mit dem Modul können Sie auswählen, welche der Objektfelder im Modul verfügbar sind. Dadurch wird die Anzahl der Felder reduziert, die beim Einrichten des Moduls durchgescrollt werden müssen.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Record Type] </p> </td> 
   <td> <p>Wählen Sie den Typ [!DNL Salesforce] Datensatzes aus, den das Modul erstellen soll. Die Felder werden je nach dem im Feld [!UICONTROL Record Type] ausgewählten Datensatztyp verfügbar. Diese Felder basieren auf der [!DNL Salesforce]-API.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Wählen Sie die Felder aus, die das Modul beim Erstellen des neuen Datensatzes konfigurieren soll. Erforderliche Felder befinden sich oben in der Liste. </p> <p>Die Felder, die Sie auswählen, werden unter diesem Feld geöffnet. Sie können jetzt Werte in diese Felder eingeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a Record]

Dieses Aktionsmodul liest Daten aus einem einzelnen -Objekt in [!DNL Salesforce].

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Record Type]</td>
    <td>Wählen Sie den Typ [!DNL Salesforce] Datensatzes aus, den das Modul [action].read.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Record Fields]</td>
    <td>Wählen Sie die Felder aus, die das Modul lesen soll. Sie müssen mindestens ein Feld auswählen.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL ID]</td>
    <td> <p>Geben Sie die eindeutige [!DNL Salesforce]-ID des Datensatzes ein, den das Modul lesen soll, oder mappen Sie sie.</p> <p>Um die ID abzurufen, öffnen Sie das [!DNL Salesforce] in Ihrem Browser und kopieren Sie den Text am Ende der URL nach dem letzten Schrägstrich (/). Beispiel: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Record]

Dieses Aktionsmodul löscht einen vorhandenen Datensatz in einem Objekt.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Wählen Sie den Typ [!DNL Salesforce] Datensatzes aus, den das Modul löschen soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Geben Sie die eindeutige [!DNL Salesforce]-ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</p> <p>Um die ID abzurufen, öffnen Sie das [!DNL Salesforce] in Ihrem Browser und kopieren Sie den Text am Ende der URL nach dem letzten Schrägstrich (/). Beispiel: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Salesforce]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Salesforce] nicht durchgeführt werden kann.

Das -Modul gibt Folgendes zurück:

* **[!UICONTROL Status Code]** (Zahl): Dies zeigt den Erfolg oder Misserfolg Ihrer HTTP-Anfrage an. Dies sind Standardcodes, die Sie im Internet nachschlagen können.
* **[!UICONTROL Headers]** (Objekt): Ein detaillierterer Kontext für die Antwort/den Status-Code, der sich nicht auf den Ausgabetext bezieht. Nicht alle Kopfzeilen, die in einer Antwort-Kopfzeile angezeigt werden, sind Antwort-Kopfzeilen, sodass einige möglicherweise nicht für Sie nützlich sind.

  Die Antwort-Header hängen von der HTTP-Anfrage ab, die Sie beim Konfigurieren des Moduls ausgewählt haben.

* **[!UICONTROL Body]** (Objekt): Je nach der HTTP-Anfrage, die Sie beim Konfigurieren des Moduls ausgewählt haben, erhalten Sie möglicherweise einige Daten zurück. Diese Daten, z. B. die Daten aus einer [!UICONTROL GET], sind in diesem Objekt enthalten.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu ein<code> &lt;Instance URL&gt;/services/data/v46.0/</code>.</p> <p>Eine Liste der verfügbaren Endpunkte finden Sie im <a href="https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_what_is_rest_api.htm">Salesforce REST API-Entwicklerhandbuch</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu, z. B. <code>{"Content-type":"application/json"}</code>. Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu. Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
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

>[!INFO]
>
>**Beispiel:** Der folgende API-Aufruf gibt die Liste aller Benutzer in Ihrem [!DNL Salesforce]-Konto zurück:
>
>* **URL**: `query`
>
>* **Methode**: [!UICONTROL GET]
>
>* **Abfragezeichenfolge**:
>
>* **key**: `q`
>
>* **Wert**: `SELECT Id, Name, CreatedDate, LastModifiedDate FROM User LIMIT 10`
>
>Treffer der Suche finden Sie in der Modulausgabe unter **[!UICONTROL Bundle]> [!UICONTROL Body] >[!UICONTROL records]**.
>
>In unserem Beispiel wurden 6 Benutzer zurückgegeben:
>
>![Treffer für die Suche](/help/workfront-fusion/references/apps-and-modules/assets/matches-of-the-search-350x573.png)


#### [!UICONTROL Upload Attachment/Document]

Dieses Aktionsmodul lädt eine Datei hoch und hängt sie an einen von Ihnen angegebenen Datensatz an oder lädt ein Dokument hoch.

Das Modul gibt die ID des Anhangs oder Dokuments und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type of Upload]</td> 
   <td>Wählen Sie aus, ob das Modul eine Anlage oder ein Dokument hochladen soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Objekts ein, zu dem Sie eine Anlage hochladen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder]</td> 
   <td>Wählen Sie den Ordner aus, der die Datei enthält, die das Modul hochladen soll. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download Attachment/Document]

Dieses Aktionsmodul lädt ein Dokument oder eine Anlage aus einem Datensatz herunter.

Sie geben die ID des Datensatzes und den gewünschten Download-Typ an.

Das Modul gibt die ID des Anhangs oder Dokuments und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Type of Download]</td>
    <td> <p>Geben Sie den Dateityp an, den Sie von Salesforce herunterladen möchten.</p> 
     <ul> 
      <li>[!UICONTROL Attachment]</li> 
      <li>[!UICONTROL Document]</li> 
      <li>[!UICONTROL ContentDocument] (Dies ist ein Dokument, das in [!DNL Saleforce CRM Content] oder [!DNL Salesforce Files] in eine Bibliothek hochgeladen wurde.)</li> 
     </ul> </td>
  </tr> 
  <tr>
    <td> <p>[!UICONTROL ID] / </p> <p>[!UICONTROL Attachment ID] / </p> <p>[!UICONTROL ContentDocument ID]</p> </td>
    <td> <p>Geben Sie die eindeutige [!DNL Salesforce]-ID des Datensatzes ein, den das Modul herunterladen soll, oder ordnen Sie sie zu.</p> <p>Um die ID abzurufen, öffnen Sie das [!DNL Salesforce] in Ihrem Browser und kopieren Sie den Text am Ende der URL nach dem letzten Schrägstrich (/). Beispiel: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Update a Record]

Dieses Aktionsmodul bearbeitet einen Datensatz in einem -Objekt.

Mit dem Modul können Sie auswählen, welche der Objektfelder im Modul verfügbar sind. Dadurch wird die Anzahl der Felder reduziert, die beim Einrichten des Moduls durchgescrollt werden müssen.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Datensatzes ein, den Sie aktualisieren möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Record Type] </p> </td> 
   <td> <p>Wählen Sie den Typ [!DNL Salesforce] Datensatzes aus, den das Modul aktualisieren soll. Die Felder werden je nach dem im Feld Datensatztyp ausgewählten Datensatztyp verfügbar. Diese Felder basieren auf der [!DNL Salesforce]-API.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Wählen Sie die Felder aus, die das Modul beim Erstellen des neuen Datensatzes konfigurieren soll. Erforderliche Felder befinden sich oben in der Liste. </p> <p>Die Felder, die Sie auswählen, werden unter diesem Feld geöffnet. Sie können jetzt Werte in diese Felder eingeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Datei hochladen

Dieses Aktionsmodul lädt eine einzelne Datei in Salesforce hoch.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu[!DNL  Adobe Workfront Fusion] - Grundlegende Anweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document linking]</td> 
   <td>Auswählen, ob ein Inhaltsdokument-Link angewendet werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL linkedEntityId]</td> 
   <td>Bei Verwendung der Dokumentverknüpfung geben Sie die ID des verknüpften Objekts ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ShareType]</td> 
   <td>Wenn Sie die Dokumentverknüpfung verwenden, wählen Sie Berechtigungen für die Datei aus.<ul><li><b>Viewer-Berechtigung</b><p>Der/die Benutzende kann die Datei anzeigen.</p></li><li><b>Berechtigung des Mitarbeiters</b><p>Der Benutzer kann die Datei anzeigen und bearbeiten.</p></li><li><b>Abgeleitete Berechtigungen</b><p>Berechtigungen basieren auf den Berechtigungen des Benutzers für den zugehörigen Datensatz, z. B. eine Bibliothek.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Wenn Sie die Dokumentverknüpfung verwenden, geben Sie die Sichtbarkeit des Dokuments ein oder mappen Sie sie.<ul><li><b>Alle Benutzer</b><p>Verfügbar für alle Benutzer mit Berechtigungen</p></li><li><b>Interne Benutzer</b><p>Verfügbar für interne Benutzer mit Berechtigungen.</p></li><li><b>SharedUsers</b><p>Verfügbar für Benutzer, die den Feed sehen können, an den die Datei gesendet wird.</p></li></ul></td> 
  </tr>

### Suchvorgänge

#### [!UICONTROL Search with Query]

Dieses Suchmodul sucht in einem -Objekt nach Datensätzen, [!DNL Salesforce] mit der angegebenen Suchanfrage übereinstimmen. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search Type]</td> 
   <td> <p>Wählen Sie die Art der Suche aus, die das Modul durchführen soll:</p> 
    <ul> 
     <li> <p>[!UICONTROL Simple]</p> </li> 
     <li> <p>[!UICONTROL Using SOSL (Salesforce Object Search Language)]</p> </li> 
     <li> <p>[!UICONTROL Using SOQL (Salesforce Object Query Language)]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Type] </p> </td> 
   <td> <p>Wenn Sie den Typ Einfache Suche ausgewählt haben, wählen Sie den Typ [!DNL Salesforce] Datensatzes aus, nach dem das Modul suchen soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] / [!UICONTROL SOSL Query] / [!UICONTROL SOQL Query]</td> 
   <td> <p>Geben Sie die Abfrage ein, nach der Sie suchen möchten.</p> <p>Weitere Informationen zu SOSL finden Sie unter <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_sosl.htm">Salesforce Object Search Language (SOSL)</a> in der [!DNL Salesforce].</p> <p>Weitere Informationen zu SOQL finden Sie unter <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql.htm">Salesforce Object Query Language (SOQL)</a> in der [!DNL Salesforce].</p> <p>Hinweis: Beachten Sie, dass der Wert des Parameters <code>RETURNING </code>die Ausgabe des Moduls beeinflusst. Wenn Sie <code>LIMIT</code> verwenden, ignorieren [!DNL Fusion] die Einstellungen im [!UICONTROL Maximal count of records]. Wenn Sie kein Limit festlegen, fügt Fusion den Wert [!UICONTROL LIMIT = Maximal count of records] ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal count of records]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search]

Dieses Aktionsmodul ruft alle Datensätze ab, die ein bestimmtes Kriterium erfüllen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL Salesforce]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu[!DNL  Adobe Workfront Fusion] - Grundlegende Anweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Wählen Sie den Typ des Objekts aus, nach dem Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>Wählen Sie das Feld aus, nach dem Sie suchen möchten, den Operator, den Sie in Ihrer Abfrage verwenden möchten, und den Wert, nach dem Sie im Feld suchen. Sie können Abfragen mithilfe von AND oder OR verbinden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Wählen Sie aus, ob das Modul alle übereinstimmenden Datensätze oder nur den ersten übereinstimmenden Datensatz zurückgeben soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal]</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus abrufen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>
