---
title: Module erweitern
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die [!UICONTROL Widen] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 11376e58-a44b-4766-85dc-e2421b0112de
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 1%

---

# [!DNL Widen]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!UICONTROL Widen] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um [!UICONTROL Widen]-Module verwenden zu können, müssen Sie über ein [!UICONTROL Widen]-Konto verfügen.

## API-Informationen erweitern

Der Widen-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.10.11</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Widen] mit [!DNL Workfront Fusion] verbinden {#connect-widen-to-workfront-fusion}

Sie können direkt aus einem [!DNL Widen]-Modul heraus eine Verbindung zu Ihrem [!DNL Widen]-Konto herstellen.

1. Klicken Sie in einem beliebigen [!DNL Widen] auf **[!UICONTROL Add]** neben dem Feld [!UICONTROL Connection] .
1. Wählen Sie die [!DNL Widen] Domain aus, mit der Sie eine Verbindung herstellen möchten.
1. Geben Sie das Token für Ihr [!DNL Widen] ein. Anweisungen zum Auffinden dieses Tokens finden Sie unter [[!DNL Widen] API-FAQs](https://community.widen.com/collective/s/article/API-FAQs).
1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Widen] Module und ihre Felder

Beim Konfigurieren [!DNL Widen] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Widen] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger-Module](#trigger-modules)
* [Aktionsmodule](#action-modules)
* [Suchmodule](#search-modules)

### Trigger-Module

#### [!UICONTROL Watch assets]

Dieses Trigger-Modul startet ein Szenario, wenn ein Asset erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Widen]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Widen] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p>Wählen Sie aus, ob Sie neue oder aktualisierte Assets ansehen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Wählen Sie die Eigenschaften aus, die Sie zusätzlich zu den Asset-Feldern in die Modulausgabe aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Wählen Sie die Felder aus, die Sie in die Modulausgabe aufnehmen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionsmodule

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Read asset info]](#read-asset-info)
* [[!UICONTROL Add assets to collections]](#add-assets-to-collections)
* [[!UICONTROL Remove assets from collection]](#remove-assets-from-collection)
* [[!UICONTROL Update asset metadata]](#update-asset-metadata)
* [[!UICONTROL Download File]](#download-file)
* [Datei [!UICONTROL Upload]](#upload-a-file)

#### [!UICONTROL Custom API Call]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Widen]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Widen] nicht durchgeführt werden kann.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Widen]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Widen] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Wählen Sie aus, ob Sie die neueste Version der [!DNL Widen]-API oder Version 1.0 verwenden möchten</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie die URL für Ihren API-Aufruf ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] Fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
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

#### [!UICONTROL Read asset info]

Dieses Aktionsmodul ruft ein einzelnes Asset anhand seiner eindeutigen ID ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Widen]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Widen] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Geben Sie die ID des Assets ein, für das Sie Informationen lesen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Wählen Sie die Eigenschaften aus, die Sie zusätzlich zu den Asset-Feldern in die Modulausgabe aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Wählen Sie die Felder aus, die Sie in die Modulausgabe aufnehmen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add assets to collections]

Dieses Aktionsmodul fügt ein oder mehrere Assets zu Sammlungen hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Widen]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Widen] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collections ID]</td> 
   <td> <p>Für jede Sammlung, der Sie die Assets hinzufügen möchten:</p> 
    <ol> 
     <li value="1"> <p> Klicken Sie auf <strong>[!UICONTROL Add]</strong>.</p> </li> 
     <li value="2"> <p>Geben Sie die [!UICONTROL Collection ID] ein oder ordnen Sie sie zu.</p> </li> 
     <li value="3"> <p>Klicken Sie auf <strong>[!UICONTROL Add item]</strong>.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> <p>Für jedes Asset, das Sie einer Sammlung hinzufügen möchten:</p> 
    <ol> 
     <li value="1"> <p> Klicken Sie auf <strong>[!UICONTROL Add]</strong>.</p> </li> 
     <li value="2"> <p>Geben Sie die Asset-ID ein oder ordnen Sie sie zu.</p> </li> 
     <li value="3"> <p>Klicken Sie auf <strong>[!UICONTROL Add item]</strong>.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assets from collection]

Dieses Aktionsmodul entfernt ein oder mehrere Assets aus Sammlungen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Widen]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Widen] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collections ID]</td> 
   <td> <p>Für jede Sammlung, aus der Sie die Assets entfernen möchten:</p> 
    <ol> 
     <li value="1"> <p> Klicken Sie auf <strong>[!UICONTROL Add]</strong>.</p> </li> 
     <li value="2"> <p>Sammlungs-ID eingeben oder zuordnen.</p> </li> 
     <li value="3"> <p>Klicken Sie auf <strong>[!UICONTROL Add item]</strong>.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ASSETS ID</td> 
   <td> <p>Für jedes Asset, das Sie aus einer Sammlung entfernen möchten:</p> 
    <ol> 
     <li value="1"> <p> Klicken Sie auf <strong>[!UICONTROL Add]</strong>.</p> </li> 
     <li value="2"> <p>Geben Sie die Asset-ID ein oder ordnen Sie sie zu.</p> </li> 
     <li value="3"> <p>Klicken Sie auf <strong>[!UICONTROL Add item]</strong>.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update asset metadata]

Dieses Aktionsmodul aktualisiert die Metadatenfelder eines Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Widen]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Widen] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Geben Sie die ID des Assets ein, bei dem Sie die Metadaten aktualisieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata type]</td> 
   <td> <p>Wählen Sie den Metadatentyp für die Metadaten aus, die Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Wählen Sie die Metadatenfelder aus, die Sie aktualisieren möchten. Geben Sie für jedes Feld den neuen Wert für das Feld ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download File]

Dieses Aktionsmodul lädt ein Asset von Ihrem [!DNL Widen]-Konto herunter.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Widen]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Widen] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Geben Sie die ID des Assets ein, das Sie herunterladen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

Dieses Aktionsmodul lädt eine Datei in Ihr [!DNL Widen]-Konto hoch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Widen]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Widen] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Profile]</td> 
   <td> <p>Wählen Sie das Upload-Profil aus, das das Modul verwenden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Method]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Datei hochladen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL From File]</strong> </p> <p>Wählen Sie die Quelldatei aus einem vorherigen Modul aus oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL By URL]</strong> </p> <p>Geben Sie die URL der Datei ein, die Sie hochladen möchten, oder mappen Sie sie.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Geben Sie einen Namen für die hochgeladene Datei ein oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata Type]</td> 
   <td>Wählen Sie den Metadatentyp für die Datei aus, die Sie hochladen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Wählen Sie die Metadatenfelder aus, die Sie in den Datei-Upload einbeziehen möchten. Geben Sie für jedes Feld den [!UICONTROL value] für das Feld ein.</td> 
  </tr> 
 </tbody> 
</table>

### Suchmodule

* [[!UICONTROL Read collection assets]](#read-collection-assets)
* [[!UICONTROL Search assets]](#search-assets)

#### [!UICONTROL Read collection assets]

Dieses Aktionsmodul ruft eine Liste von Assets in einer Sammlung ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Widen]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Widen] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Geben Sie die ID der Sammlung ein, die die Assets enthält, die Sie lesen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td>Geben Sie die Nummer des ersten Elements ein, das Sie auflisten möchten, oder ordnen Sie sie zu. Dies ist eine Möglichkeit, die Datensätze zu paginieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort By]</td> 
   <td> <p>Wählen Sie die Eigenschaft aus, nach der Sie die Assets sortieren möchten. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>Wählen Sie aus, ob Assets in auf- oder absteigender Reihenfolge sortiert werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Wählen Sie die Felder aus, die Sie in die Modulausgabe aufnehmen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search assets]

Dieses Suchmodul ruft eine Liste von Assets ab, die den spezifischen Suchkriterien entsprechen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Widen]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Widen] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search query]</td> 
   <td> <p>Geben Sie die Kriterien ein, nach denen Sie Assets suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort By]</td> 
   <td> <p>Wählen Sie aus, wie die Assets sortiert werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>Wählen Sie aus, ob Assets in auf- oder absteigender Reihenfolge sortiert werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include deleted]</td> 
   <td>Aktivieren Sie diese Option, um gelöschte Assets in die Suche einzubeziehen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Include archived]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um archivierte Assets in die Suche einzuschließen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search document text]</td> 
   <td>Aktivieren Sie diese Option, um Dokumenttext in Ihre Suche aufzunehmen, oder wählen Sie „false“ aus, um nur Assets einzuschließen, deren Titel den Suchkriterien entspricht.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Offset]</td> 
   <td>Geben Sie die Nummer des ersten Elements ein, für das Sie Details abrufen möchten, oder ordnen Sie sie zu. Dies ist eine Möglichkeit, die Datensätze zu paginieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scroll]</td> 
   <td>Aktivieren Sie diese Option, um das Scrollen zu ermöglichen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Wählen Sie die Eigenschaften aus, die Sie zusätzlich zu den Asset-Feldern in die Modulausgabe aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Wählen Sie die Felder aus, die Sie in die Modulausgabe aufnehmen möchten.</td> 
  </tr> 
 </tbody> 
</table>
