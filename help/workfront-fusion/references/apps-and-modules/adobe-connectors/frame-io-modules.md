---
title: Frame.io-Module
description: Das [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] Konto.
author: Becky
feature: Workfront Fusion
exl-id: 121b145c-d04d-44b9-b673-ea2928e2346d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1969'
ht-degree: 0%

---

# [!DNL Frame.io]

Mit den [!DNL Adobe Workfront Fusion] [!DNL Frame.io] können Sie Assets und Kommentare in Ihrem [!DNL Frame.io]-Konto überwachen, erstellen, aktualisieren, abrufen oder löschen.

Eine Videoeinführung zum Frame.io-Connector finden Sie unter:

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

Um [!DNL Frame.io] Module verwenden zu können, müssen Sie über ein [!DNL Frame.io] verfügen

## Frame.io-API-Informationen

Der Frame.io-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.frame.io/v2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Frame.io] mit [!UICONTROL Adobe Workfront Fusion] verbinden

Sie können eine Verbindung zu [!DNL Frame.io] über ein API-Token oder mithilfe von OAuth 2.0 herstellen.

[Verbinden mit [!DNL Frame.io] mithilfe eines API-Tokens](#connect-to-frameio-using-an-api-token)

[Herstellen einer Verbindung  [!DNL Frame.io]  OAuth 2.0 PKCE](#connect-to-frameio-using-oauth-20-pkce)

### Verbindung zu [!DNL Frame.io] über ein API-Token herstellen

Um Ihr [!DNL Frame.io]-Konto mithilfe eines API-Tokens mit [!DNL Workfront Fusion] zu verbinden, müssen Sie das API-Token in Ihrem [!DNL Frame.io]-Konto erstellen und es in das [!DNL Workfront Fusion] [!DNL Frame.io] [!UICONTROL Create a connection]-Dialogfeld einfügen.

1. Melden Sie sich bei Ihrem [!DNL Frame.io] an.
1. Navigieren Sie zur Seite **[!UICONTROL Tokens]** im [!DNL Frame.io] Developer.
1. Klicken Sie auf **[!UICONTROL New]**.
1. Geben Sie den Namen des Tokens ein, wählen Sie die gewünschten Bereiche aus und klicken Sie auf **[!UICONTROL Create]**.
1. Kopieren Sie das angegebene Token.
1. Navigieren Sie zu [!DNL Workfront Fusion] und öffnen Sie das **[!UICONTROL Create a connection]**-Dialogfeld des [!DNL Frame.io].
1. Wählen Sie im Feld **[!UICONTROL Connection type]** die Option **[!DNL Frame.io]** aus.
1. Geben Sie das Token, das Sie in Schritt 5 kopiert haben, in das Feld **[!UICONTROL Your [!DNL Frame.io] API Key]** ein und klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung herzustellen.

Die Verbindung wurde hergestellt. Sie können mit der Einrichtung des Moduls fortfahren.

### Herstellen einer Verbindung zu [!DNL Frame.io] über OAuth 2.0 PKCE

Sie können mit OAuth 2.0 PKCE mit einer optionalen Client-ID eine Verbindung zu [!DNL Frame.io] herstellen. Wenn Sie eine Client-ID in Ihre Verbindung einbeziehen möchten, müssen Sie eine OAuth 2.0-App in Ihrem [!DNL Frame.io]-Konto erstellen.

* [Herstellen einer Verbindung mit [!DNL Frame.io] mithilfe von OAuth 2.0 PKCE (ohne Client-ID)](#connect-to-frameio-using-using-oauth-20-pkce-without-client-id)
* [Herstellen einer Verbindung mit [!DNL Frame.io] mithilfe von OAuth 2.0 PKCE (mit Client-ID)](#connect-to-frameio-using-using-oauth-20-pkce-with-client-id)

#### Herstellen einer Verbindung zu [!DNL Frame.io] über OAuth 2.0 PKCE (ohne Client-ID)

1. Navigieren Sie zu [!DNL Workfront Fusion] und öffnen Sie das **[!UICONTROL Create a connection]**-Dialogfeld des [!DNL Frame.io].
1. Wählen Sie im Feld **[!UICONTROL Connection type]** die Option **[!UICONTROL [!DNL Frame.io] OAuth 2.0 PKCE]** aus.
1. Geben Sie im Feld **[!UICONTROL Connection name]** einen Namen für die neue Verbindung ein.
1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung herzustellen.

Die Verbindung wurde hergestellt. Sie können mit der Einrichtung des Moduls fortfahren.

#### Verbinden von mit [!DNL Frame.io] über OAuth 2.0 PKCE (mit Client-ID)

1. Erstellen Sie eine OAuth 2.0-App in [!DNL Frame.io]. Anweisungen finden Sie in der [!DNL Frame.io] Dokumentation zu [!UICONTROL OAuth 2.0 Code Authorization Flow].

   >[!IMPORTANT]
   >
   >Beim Erstellen der OAuth 2.0-App in [!DNL Frame.io]:
   >
   >* Geben Sie Folgendes als Umleitungs-URI ein:
   >   
   >  Nord- und Südamerika / APAC `https://app.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >  EMEA `https://app-eu.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >* Aktivieren Sie die Option PCKE .


1. Kopieren Sie die bereitgestellte `client_id`.
1. Navigieren Sie zu [!DNL Workfront Fusion] und öffnen Sie das **[!UICONTROL Create a connection]**-Dialogfeld des [!DNL Frame.io].
1. Wählen Sie im Feld **[!UICONTROL Connection type]** die Option **[!UICONTROL [!DNL Frame.io] OAuth 2.0 PKCE]** aus.
1. Geben Sie im Feld **[!UICONTROL Connection name]** einen Namen für die neue Verbindung ein.
1. Klicken Sie auf **[!UICONTROL Show advanced settings]**.
1. Geben Sie die in Schritt 2 kopierte `client_id` in das Feld **[!UICONTROL Client ID]** ein.
1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung herzustellen.

Die Verbindung wurde hergestellt. Sie können mit der Einrichtung des Moduls fortfahren.

## [!DNL Frame.io] Module und ihre Felder

Beim Konfigurieren [!DNL Frame.io] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Frame.io] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Assets](#assets)
* [Kommentare](#comments)
* [Projekte](#projects)
* [Sonstige](#other)

### Assets

* [[!UICONTROL Create an Asset]](#create-an-asset)
* [[!UICONTROL Delete an Asset]](#delete-an-asset)
* [[!UICONTROL Get an Asset]](#get-an-asset)
* [[!UICONTROL List Assets]](#list-assets)
* [[!UICONTROL Update an Asset]](#update-an-asset)
* [[!UICONTROL Watch Asset Deleted]](#watch-asset-deleted)
* [[!UICONTROL Watch Asset Label Updated]](#watch-asset-label-updated)
* [[!UICONTROL Watch New Asset]](#watch-new-asset)

#### [!UICONTROL Create an Asset]

Dieses Aktionsmodul erstellt ein neues Asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, für das Sie ein Asset erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das Sie ein Asset erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Wählen Sie den Ordner aus oder ordnen Sie die ID des Ordners zu, in dem Sie ein Asset erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Wählen Sie aus, ob Sie einen Ordner oder eine Datei erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie den Namen der neuen Datei oder des neuen Ordners ein.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">File Type </td> 
    <td> <p>Select the type of file you want to upload.</p> </td> 
   </tr>
  --> <!--
   <tr> 
    <td role="rowheader">File Size </td> 
    <td> <p>The file size in bytes.</p> </td> 
   </tr>
  --> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>Geben Sie die URL der Datei ein, die Sie hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>Geben Sie eine kurze Beschreibung des Assets ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Asset]

Dieses Aktionsmodul löscht ein angegebenes Asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das das zu löschende Asset enthält, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Wählen Sie das Projekt oder die Assets aus, die Sie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, der das zu löschende Asset enthält</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Wählen Sie das Asset aus, das Sie löschen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Asset]

Dieses Aktionsmodul ruft Asset-Details ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das das Asset enthält, zu dem Sie Details abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Wählen Sie das Projekt aus, das das Asset enthält, zu dem Sie Details abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, der das Asset enthält, zu dem Sie Details abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Wählen Sie das Asset aus oder ordnen Sie die ID des Assets zu, zu dem Sie Details abrufen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Assets]

Dieses Suchmodul ruft alle Assets im Ordner des angegebenen Projekts ab.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das den Ordner enthält, aus dem Sie Assets abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Wählen Sie das Projekt aus, das den Ordner enthält, aus dem Sie Assets abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, aus dem Sie Assets auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Assets fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### `[!UICONTROL Update an Asset]`

Mit diesem Aktionsmodul können Sie den Namen, die Beschreibung oder die benutzerdefinierten Felder eines vorhandenen Assets aktualisieren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, für das Sie ein Asset aktualisieren möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das Sie ein Asset aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Wählen Sie den Ordner aus oder ordnen Sie die ID des Ordners zu, in dem Sie ein Asset aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie den Namen der aktualisierten Datei ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>Geben Sie eine kurze Beschreibung des aktualisierten Assets ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Asset Deleted]

Dieses Trigger-Modul startet ein Szenario, wenn ein Asset gelöscht wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Geben Sie den Namen des Webhooks ein, z. B. Asset gelöscht.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das dieser Webhook erstellt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Asset Label Updated]

Dieses Statusmodul startet ein Trigger, wenn der Status eines Assets festgelegt, geändert oder entfernt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Geben Sie den Namen des Webhooks ein, z. B. Asset-Status aktualisiert.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das dieser Webhook erstellt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch New Asset]

Dieses Trigger-Modul startet ein Szenario, wenn ein neues Asset erstellt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Geben Sie den Namen des Webhooks ein, z. B. „Asset erstellt“.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das dieser Webhook erstellt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Kommentare

* [[!UICONTROL Create a Comment]](#create-a-comment)
* [[!UICONTROL Delete a Comment]](#delete-a-comment)
* [[!UICONTROL Get a Comment]](#get-a-comment)
* [[!UICONTROL List Comments]](#list-comments)
* [[!UICONTROL Update a Comment]](#update-a-comment)
* [[!UICONTROL Watch Comment Updated]](#watch-comment-updated)
* [[!UICONTROL Watch New Comment]](#watch-new-comment)

#### [!UICONTROL Create a Comment]

Dieses Aktionsmodul fügt dem Asset einen neuen Kommentar oder eine neue Antwort hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Wählen Sie aus, ob Sie einen Kommentar erstellen oder auf einen Kommentar antworten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das das Asset enthält, dem Sie einen Kommentar hinzufügen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, das das Asset enthält, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Wählen Sie den Ordner aus oder ordnen Sie die ID des Ordners zu, der das Asset enthält, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Wählen Sie das Asset aus, dem Sie einen Kommentar hinzufügen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Wählen Sie den Kommentar aus, dem Sie eine Antwort hinzufügen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Geben Sie den Textinhalt des Kommentars oder der Antwort ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Geben Sie die Bildnummer im Video ein, mit der der Kommentar verknüpft werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Comment]

Dieses Aktionsmodul löscht einen vorhandenen Kommentar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID]</td> 
   <td> <p> Wählen Sie das Team aus, dem das Projekt gehört, das das Asset enthält, aus dem Sie einen Kommentar löschen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, das das Asset enthält, aus dem Sie einen Kommentar löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p> Wählen Sie den Ordner aus, der das Asset enthält, aus dem Sie einen Kommentar löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Wählen Sie das Asset aus, das den Kommentar enthält, den Sie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Wählen Sie den Kommentar aus, den Sie löschen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Comment]

Dieses Aktionsmodul ruft Details des angegebenen Kommentars ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das den Ordner enthält, aus dem Sie Assets abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, das den Ordner enthält, aus dem Sie Assets abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, aus dem Sie Assets auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Wählen Sie das Asset aus, das den Kommentar enthält, den Sie abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Wählen Sie den Kommentar aus, zu dem Sie Details abrufen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Comments]

Dieses Suchmodul ruft alle Kommentare des angegebenen Assets ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das den Ordner enthält, aus dem Sie Kommentare abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, das den Ordner enthält, aus dem Sie Kommentare abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, der das Asset enthält, dessen Kommentare Sie auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Wählen Sie das Asset aus, für das Sie Kommentare auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Kommentaren fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Comment]

Dieses Aktionsmodul bearbeitet einen vorhandenen Kommentar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das das Asset enthält, für das Sie einen Kommentar aktualisieren möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Wählen Sie das Projekt \ aus, das das Asset enthält, zu dem Sie einen Kommentar aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, der das Asset enthält, für das Sie einen Kommentar aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Wählen Sie das Asset aus, für das Sie einen Kommentar aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Wählen Sie den Kommentar aus, den Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Geben Sie den Textinhalt des Kommentars ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Geben Sie die Bildnummer im Video ein, mit dem der Kommentar verknüpft ist.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comment Updated]

Dieses Kommentarmodul startet ein Trigger, wenn ein Kommentar bearbeitet wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Geben Sie den Namen des Webhooks ein, z. B. Kommentar bearbeitet.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das dieser Webhook erstellt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch New Comment]

Dieses Trigger-Modul startet ein Szenario, wenn ein neuer Kommentar oder eine neue Antwort erstellt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Den Namen des Webhooks eingeben, z. B. Neuer Kommentar.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das dieser Webhook erstellt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projekte

#### [!UICONTROL List Projects]

Dieses Suchmodul ruft alle Projekte für das angegebene Team ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das Sie Projekte abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Projekten fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstige

#### [!UICONTROL Make an API Call]

Mit diesem Modul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://api.frame.io</code> ein. Beispiel: <code> /v2/teams</code></p> <p>Hinweis: Eine Liste der verfügbaren Endpunkte finden Sie in der [!DNL Frame.io] API-Referenz.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Geben Sie die Abfragezeichenfolge der Anfrage ein. Klicken Sie für jeden Parameter, den Sie in die Abfragezeichenfolge aufnehmen möchten, auf <b>[!UICONTROL Add item]</b> und geben Sie den Namen des Felds und den gewünschten Wert ein.</p> </td> 
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

**Beispiel:** Der folgende API-Aufruf gibt alle Teams und ihre Details in Ihrem [!DNL Frame.io]-Konto zurück:

URL: `/v2/teams`

Methode: `GET`

![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

Das Ergebnis finden Sie in der -Ausgabe des Moduls unter Bundle > Body.

In unserem Beispiel wurden die Details von 1 Team zurückgegeben:

![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)
