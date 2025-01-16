---
title: Partnermodule
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die  [!DNL Bynder] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 0a45f8a7-12cc-41cc-9135-92f4779afac0
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# [!DNL Bynder]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Bynder] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um [!DNL Bynder]-Module verwenden zu können, müssen Sie über ein [!DNL Bynder]-Konto verfügen.

## Binder-API-Informationen

Der Binder-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.25.21</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL Bynder] mit Workfront Fusion  {#connect-bynder-to-workfront-fusion}

* [Erstellen einer Verbindung zu [!DNL Bynder] von [!DNL Workfront Fusion]](#create-a-connection-to-bynder-from-workfront-fusion)
* [Generieren eines [!UICONTROL Client ID] und [!UICONTROL Client Secret] in [!DNL Bynder] (optional)](#generate-a-client-id-and-client-secret-in-bynder-optional)

### Erstellen einer Verbindung zu [!DNL Bynder] aus [!DNL Workfront Fusion]

Sie können direkt aus einem [!DNL Bynder]-Modul heraus eine Verbindung von [!DNL Workfront Fusion] zu Ihrem [!DNL Bynder]-Konto erstellen.

1. Klicken Sie in einem beliebigen [!DNL Bynder] auf **[!UICONTROL Add]** neben dem Feld [!UICONTROL Connection] .
1. Wählen Sie die [!DNL Bynder] Domain aus, mit der Sie eine Verbindung herstellen möchten.
1. (Optional) Klicken Sie auf **[!UICONTROL Advanced settings]** und geben Sie dann Ihre [!UICONTROL Client ID] und [!UICONTROL Client Secret] ein.

   Anweisungen zum Generieren der Client-ID und des Client-Geheimnisses finden Sie unter [Generieren einer Client-ID und eines Client-Geheimnisses in [!DNL Bynder] (optional)](#generate-a-client-id-and-client-secret-in-bynder-optional) in diesem Artikel.

1. Geben Sie im Fenster [!UICONTROL login] Ihren Benutzernamen (E-Mail-Adresse) und Ihr Passwort ein.
1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

### [!UICONTROL Client ID] und [!UICONTROL Client Secret] in [!DNL Bynder] generieren (optional)

Wenn Sie eine Verbindung mit der Client-ID und dem Client-Geheimnis erstellen möchten, können Sie sie aus Ihrem [!DNL Bynder]-Konto generieren. Die Client-ID und der geheime Client-Schlüssel werden beim Erstellen einer App in [!DNL Bynder] generiert.

Anweisungen zum Erstellen einer App in [!DNL Bynder] finden Sie unter [OAuth 2.0-](https://developer-docs.bynder.com/api/authentication-oauth2-oauth-apps/)) in der [!DNL Bynder].

>[!NOTE]
>
>Geben Sie beim Erstellen der App in [!DNL Bynder] Folgendes als `redirect uri` ein:
>
>`https://app.workfrontfusion.com/oauth/cb/workfront-bynder`

## [!DNL Bynder] Module und ihre Felder

Beim Konfigurieren [!DNL Bynder] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Bynder] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktionen](#actions)
* [Suchvorgänge](#searches)
* [Trigger](#triggers)

### Aktionen

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Read asset metadata]](#read-asset-metadata)
* [[!UICONTROL Update asset metadata]](#update-asset-metadata)
* [[!UICONTROL Add assets to a collection]](#add-assets-to-a-collection)
* [[!UICONTROL Remove assets from collection]](#remove-assets-from-collection)
* [[!UICONTROL Add a tag to assets]](#add-a-tag-to-assets)
* [[!UICONTROL Remove a tag] aus Assets](#remove-a-tag-from-assets)
* [[!UICONTROL Download asset]](#download-asset)
* [[!UICONTROL Upload asset]](#upload-asset)

#### [!UICONTROL Custom API Call]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Bynder]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Bynder] nicht durchgeführt werden kann.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

Das Modul gibt einen Status-Code zusammen mit den Kopfzeilen und dem Hauptteil des API-Aufrufs zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://{your-bynder-domain}/api/{api-version}/</code> ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
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

#### [!UICONTROL Read asset metadata]

Dieses Aktionsmodul liest die Metadaten eines Assets.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Geben Sie die ID des Assets ein, für das Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update asset metadata]

Dieses Aktionsmodul aktualisiert die Metadaten eines vorhandenen Assets.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Geben Sie die ID des Assets ein, für das Sie Metadaten aktualisieren möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Informationen eingeben möchten, und geben Sie dann die Informationen, mit denen Sie die Metadaten aktualisieren möchten, in diese Felder ein oder ordnen Sie sie zu. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metaproperties]</p> </td> 
   <td>Wählen Sie die Optionen aus, die Sie aktualisieren möchten, und geben Sie dann die Informationen in diese Eigenschaften ein oder ordnen Sie sie ihnen zu. Metaeigenschaften sind Informationen über das Asset, die keine bestimmten Felder im Asset darstellen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add assets to a collection]

Dieses Aktionsmodul fügt ein oder mehrere Assets zu einer Sammlung hinzu.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Geben Sie die ID der Sammlung ein, der Sie Assets hinzufügen möchten, oder mappen Sie sie.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Klicken Sie für jedes Asset, das Sie der Sammlung hinzufügen möchten, auf <strong>[!UICONTROL Add item]</strong> und geben Sie dann die Asset-ID ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assets from collection]

Dieses Aktionsmodul entfernt ein oder mehrere Assets aus einer Sammlung.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Geben Sie die ID der Sammlung ein, aus der Sie Assets entfernen möchten, oder mappen Sie sie.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Klicken Sie für jedes Asset, das Sie aus der Sammlung entfernen möchten, auf <strong>[!UICONTROL Add item]</strong> und geben Sie dann die Asset-ID ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add a tag to assets]

Hinzufügen eines Tags zu einem oder mehreren Assets

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>Geben Sie die ID des Tags ein, das Sie zu Assets hinzufügen möchten, oder ordnen Sie sie zu.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Klicken Sie für jedes Asset, das Sie taggen möchten, auf <strong>[!UICONTROL Add item]</strong> und geben Sie dann die Asset-ID ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a tag from assets]

Entfernen eines Tags aus einem oder mehreren Assets

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>Geben Sie die ID des Tags ein, das Sie aus Assets entfernen möchten, oder ordnen Sie sie zu.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Klicken Sie für jedes Asset, aus dem Sie ein Tag entfernen möchten, auf <strong>[!UICONTROL Add item]</strong> und geben Sie dann die Asset-ID ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download asset]

Dieses Aktionsmodul lädt ein einzelnes Asset herunter.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Geben Sie die ID des Assets ein, das Sie herunterladen möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset version]</td> 
   <td> <p>Geben Sie die Version des Assets ein, das Sie herunterladen möchten, oder ordnen Sie sie zu. Um die neueste Version des Assets herunterzuladen, lassen Sie das Feld leer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload asset]

Dieses Aktionsmodul lädt ein einzelnes Asset hoch.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save as]</td> 
   <td> <p>Wählen Sie aus, wie Sie die hochgeladene Datei speichern möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL New asset]</strong> </p> <p>Wählen Sie die Felder und Metaeigenschaften aus, für die Sie Informationen eingeben möchten, und geben Sie dann die Informationen in diese Felder ein.</p> <p>Geben Sie die ID der Marke ein, die Sie für das hochgeladene Asset verwenden möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL New asset version]</strong> </p> <p>Geben Sie die ID des Assets ein, für das Sie eine neue Version hochladen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL List record]](#list-record)
* [[!UICONTROL Search for assets]](#search-for-assets)

#### [!UICONTROL List record]

Dieses Suchmodul ruft alle Elemente eines bestimmten Typs ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Wählen Sie den Typ des aufzulistenden Datensatzes aus.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Read all collections]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read information about all tags]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read all assets of a collection]</strong> </p> <p>Geben Sie die ID der Sammlung ein, für die Sie Assets auflisten möchten, oder ordnen Sie sie zu.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for assets]

Dieses Suchmodul sucht anhand der von Ihnen angegebenen Kriterien nach Assets.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criteria]</td> 
   <td> <p>Geben Sie die Suchkriterien ein. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Field]</strong> </p> <p>Wählen Sie das Feld aus, das Sie für Ihre Suche verwenden möchten</p> </li> 
     <li> <p><strong>[!UICONTROL Logical Operator]</strong> </p> <p>Wählen Sie den Operator aus, den Sie für Ihre Suche verwenden möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Geben Sie den Wert, nach dem im ausgewählten Feld gesucht werden soll, ein oder ordnen Sie ihn zu. Der Werttyp sollte mit dem Datentyp des ausgewählten Felds übereinstimmen. </p> <p>Weitere Informationen zu Datentypen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Elementdatentypen in [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Wählen Sie aus, ob das erste übereinstimmende Asset oder alle übereinstimmenden Assets zurückgegeben werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Wählen Sie das Feld aus, nach dem Sie sortieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort Direction]</td> 
   <td> <p>Wählen Sie aus, ob auf- oder absteigend sortiert werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Trigger

#### [!UICONTROL Watch assets]

Dieses Trigger-Modul startet ein Szenario, wenn ein Asset erstellt oder aktualisiert wird.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit [!DNL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> <!--
    <td role="rowheader">Event type</td>
   --> <!--
    <td>Select whether you want to start the scenario when a new asset is created or when an existing asset is updated.</td>
   --> 
  </tr> 
  <tr>
     <td role="rowheader">[!UICONTROL Collections]</td>
   <td> <p>Wählen Sie die Sammlung aus, die Sie auf neue Assets überwachen möchten. Um alle Sammlungen zu sehen, lassen Sie dieses Feld leer.</p> </td> 
  </tr> 
  <tr> <!--
    <td role="rowheader">Outputs</td>
   --> <!--
    <td>Select the fields that you want to include in the output.</td>
   --> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Limit]</td>

<td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>
