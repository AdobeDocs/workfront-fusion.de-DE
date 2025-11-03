---
title: Frame.io (Legacy)-Module
description: Das [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] Konto.
author: Becky
feature: Workfront Fusion
exl-id: 121b145c-d04d-44b9-b673-ea2928e2346d
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '2666'
ht-degree: 0%

---

# [!DNL Frame.io] Legacy-Module

>[!IMPORTANT]
>
>In diesem Artikel wird die veraltete Version des Frame.io-Connectors beschrieben. Dieser Connector wird verwendet, um eine Verbindung mit Frame.io Version 3 herzustellen.
>
>Anweisungen zur neuen (Beta) Version des Frame.io-Connectors finden Sie unter [Frame.io Beta-Connector](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules-new.md).

Mit den Adobe Workfront Fusion [!DNL Frame.io]-Modulen können Sie Assets und Kommentare in Ihrem [!DNL Frame.io]-Konto überwachen, erstellen, aktualisieren, abrufen oder löschen.

Workfront bietet zwei Frame.io-Connectoren, die auf der Version von Frame.io basieren, mit der Sie eine Verbindung herstellen.

| Connector | Frame.io-Version |
|---|---|
| Frame.io (Beta) | v4 |
| Frame.io (veraltet) | v3 |

Anweisungen zur neuen Version des Frame.io-Connectors finden Sie unter [Frame.io Beta-Connector](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules-new.md).

Eine Videoeinführung zum Frame.io-Connector finden Sie unter:

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

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

## Verbinden von [!DNL Frame.io] mit [!UICONTROL Adobe Workfront Fusion]

Sie können eine Verbindung zu [!DNL Frame.io] über ein API-Token oder mithilfe von OAuth 2.0 herstellen.

[Verbinden mit [!DNL Frame.io] mithilfe eines API-Tokens](#connect-to-frameio-using-an-api-token)

[Herstellen einer Verbindung  [!DNL Frame.io]  OAuth 2.0 PKCE](#connect-to-frameio-using-oauth-20-pkce)

### Verbindung zu [!DNL Frame.io] über ein API-Token herstellen

Um Ihr [!DNL Frame.io]-Konto mithilfe eines API-Tokens mit Workfront Fusion zu verbinden, müssen Sie das API-Token in Ihrem [!DNL Frame.io]-Konto erstellen und in das Dialogfeld [!DNL Frame.io][!UICONTROL  Verbindung erstellen] von Workfront Fusion einfügen.

1. Melden Sie sich bei Ihrem [!DNL Frame.io] an.
1. Navigieren Sie zur Seite **[!UICONTROL Token]** im [!DNL Frame.io] Developer.
1. Klicken Sie auf **[!UICONTROL Neu]**.
1. Geben Sie den Namen des Tokens ein, wählen Sie die gewünschten Bereiche aus und klicken Sie auf **[!UICONTROL Erstellen]**.
1. Kopieren Sie das angegebene Token.
1. Wechseln Sie zu Workfront Fusion und öffnen Sie das Dialogfeld [!DNL Frame.io]Verbindung erstellen **[!UICONTROL des]**.
1. Wählen Sie im Feld **[!UICONTROL Verbindungstyp]** die Option **[!DNL Frame.io]**.
1. Geben Sie das Token, das Sie in Schritt 5 kopiert haben, in das Feld **[!UICONTROL Ihr [!DNL Frame.io] API-Schlüssel]** ein
1. Klicken Sie **[!UICONTROL Weiter]**, um die Verbindung herzustellen und zum Modul zurückzukehren.

### Herstellen einer Verbindung zu [!DNL Frame.io] über OAuth 2.0 PKCE

Sie können mit OAuth 2.0 PKCE mit einer optionalen Client-ID eine Verbindung zu [!DNL Frame.io] herstellen. Wenn Sie eine Client-ID in Ihre Verbindung einbeziehen möchten, müssen Sie eine OAuth 2.0-App in Ihrem [!DNL Frame.io]-Konto erstellen.

* [Herstellen einer Verbindung mit [!DNL Frame.io] mithilfe von OAuth 2.0 PKCE (ohne Client-ID)](#connect-to-frameio-using-using-oauth-20-pkce-without-client-id)
* [Herstellen einer Verbindung mit [!DNL Frame.io] mithilfe von OAuth 2.0 PKCE (mit Client-ID)](#connect-to-frameio-using-using-oauth-20-pkce-with-client-id)

#### Herstellen einer Verbindung zu [!DNL Frame.io] über OAuth 2.0 PKCE (ohne Client-ID)

1. Wechseln Sie zu Workfront Fusion und öffnen Sie das Dialogfeld [!DNL Frame.io]Verbindung erstellen **[!UICONTROL des]**.
1. Wählen Sie im Feld **[!UICONTROL Verbindungstyp]** die Option **[!UICONTROL [!DNL Frame.io]OAuth 2.0 PKCE]**.
1. Geben Sie im Feld „Verbindungsname“ einen **[!UICONTROL für die neue]** ein.
1. Klicken Sie **[!UICONTROL Weiter]**, um die Verbindung herzustellen und zum Modul zurückzukehren.

#### Verbinden von mit [!DNL Frame.io] über OAuth 2.0 PKCE (mit Client-ID)

1. Erstellen Sie eine OAuth 2.0-App in [!DNL Frame.io]. Anweisungen finden Sie in der [!DNL Frame.io]-Dokumentation unter [!UICONTROL OAuth 2.0-Code-Autorisierungsfluss].

   >[!IMPORTANT]
   >
   >Beim Erstellen der OAuth 2.0-App in [!DNL Frame.io]:
   >
   >* Geben Sie Folgendes als Umleitungs-URI ein:
   >   
   >     * **Nord- und Südamerika / APAC**: `https://app.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >     * **EMEA**: `https://app-eu.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >* Aktivieren Sie die Option PCKE .


1. Kopieren Sie die bereitgestellte `client_id`.
1. Wechseln Sie zu Workfront Fusion und öffnen Sie das Dialogfeld [!DNL Frame.io]Verbindung erstellen **[!UICONTROL des]**.
1. Wählen Sie im Feld **[!UICONTROL Verbindungstyp]** die Option **[!UICONTROL [!DNL Frame.io]OAuth 2.0 PKCE]**.
1. Geben Sie im Feld „Verbindungsname“ einen **[!UICONTROL für die neue]** ein.
1. Klicken Sie **[!UICONTROL Erweiterte Einstellungen anzeigen]**.
1. Geben Sie die in Schritt 2 kopierte `client_id` in das Feld **[!UICONTROL Client-ID]** ein.
1. Klicken Sie **[!UICONTROL Weiter]**, um die Verbindung herzustellen und zum Modul zurückzukehren.

## [!DNL Frame.io] Module und ihre Felder

Beim Konfigurieren von [!DNL Frame.io] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Frame.io] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Assets](#assets)
* [Kommentare](#comments)
* [Projekte](#projects)
* [Sonstiges](#other)

### Assets

* [[!UICONTROL Erstellen eines Assets]](#create-an-asset)
* [[!UICONTROL Löschen eines Assets]](#delete-an-asset)
* [[!UICONTROL Asset abrufen]](#get-an-asset)
* [[!UICONTROL Assets auflisten]](#list-assets)
* [[!UICONTROL Aktualisieren eines Assets]](#update-an-asset)
* [[!UICONTROL Gelöschtes Asset ansehen]](#watch-asset-deleted)
* [[!UICONTROL Asset-Kennzeichnung ansehen aktualisiert]](#watch-asset-label-updated)
* [[!UICONTROL Neues Asset ansehen]](#watch-new-asset)

#### [!UICONTROL Erstellen eines Assets]

Dieses Aktionsmodul erstellt ein neues Asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, für das Sie ein Asset erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das Sie ein Asset erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID] </td> 
   <td> <p>Wählen Sie den Ordner aus oder ordnen Sie die ID des Ordners zu, in dem Sie ein Asset erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Typ] </td> 
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
   <td> <p>Wenn Sie eine Datei erstellen, geben Sie die URL der Datei ein, die Sie hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung] </td> 
   <td> <p>Wenn Sie eine Datei erstellen, geben Sie eine kurze Beschreibung des Assets ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bezeichnung] </td> 
   <td> <p>Wenn Sie eine Datei erstellen, wählen Sie aus, ob die Datei gerade erstellt wird, überprüft werden muss oder genehmigt wurde.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Löschen eines Assets]

Dieses Aktionsmodul löscht ein angegebenes Asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das das zu löschende Asset enthält, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID]</td> 
   <td> <p> Wählen Sie das Projekt oder die Assets aus, die Sie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, der das zu löschende Asset enthält</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Wählen Sie das Asset aus, das Sie löschen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Asset abrufen]

Dieses Aktionsmodul ruft Asset-Details ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das das Asset enthält, zu dem Sie Details abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID]</td> 
   <td> <p> Wählen Sie das Projekt aus, das das Asset enthält, zu dem Sie Details abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, der das Asset enthält, zu dem Sie Details abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Wählen Sie das Asset aus oder ordnen Sie die ID des Assets zu, zu dem Sie Details abrufen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assets auflisten]

Dieses Suchmodul ruft alle Assets im Ordner des angegebenen Projekts ab.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das den Ordner enthält, aus dem Sie Assets abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID]</td> 
   <td> <p> Wählen Sie das Projekt aus, das den Ordner enthält, aus dem Sie Assets abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, aus dem Sie Assets auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren eines Assets]

Mit diesem Aktionsmodul können Sie den Namen, die Beschreibung oder die benutzerdefinierten Felder eines vorhandenen Assets aktualisieren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, für das Sie ein Asset aktualisieren möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das Sie ein Asset aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID] </td> 
   <td> <p>Wählen Sie den Ordner aus oder ordnen Sie die ID des Ordners zu, in dem Sie ein Asset aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Geben Sie die ID des Assets ein, das Sie aktualisieren möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie den Namen der aktualisierten Datei ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung] </td> 
   <td> <p>Geben Sie eine kurze Beschreibung des aktualisierten Assets ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Gelöschtes Asset ansehen]

Dieses Trigger-Modul startet ein Szenario, wenn ein Asset, das zum angegebenen Team gehört, gelöscht wird.

Da dies ein sofortiger Trigger ist, müssen Sie einen Webhook für das Modul auswählen oder erstellen, um es zu verwenden.

Wenn Sie einen Webhook hinzufügen, geben Sie die folgenden Informationen ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name]</td> 
   <td> <p> Geben Sie einen Namen für den Webhook ein, z. B. „Asset gelöscht“</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das dieser Webhook erstellt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Asset-Kennzeichnung ansehen aktualisiert]

Dieses Trigger-Modul startet ein Szenario, wenn die Beschriftung für ein Asset, das der angegebenen Gruppe gehört, festgelegt, geändert oder entfernt wird.

Da dies ein sofortiger Trigger ist, müssen Sie einen Webhook für das Modul auswählen oder erstellen, um es zu verwenden.

Wenn Sie einen Webhook hinzufügen, geben Sie die folgenden Informationen ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name]</td> 
   <td> <p> Geben Sie einen Namen für den Webhook ein, z. B. „Asset-Status aktualisiert“.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das dieser Webhook erstellt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Neues Asset ansehen]

Dieses Teammodul startet ein Trigger, wenn ein neues Asset für das angegebene Team erstellt wird.

Da dies ein sofortiger Trigger ist, müssen Sie einen Webhook für das Modul auswählen oder erstellen, um es zu verwenden.

Wenn Sie einen Webhook hinzufügen, geben Sie die folgenden Informationen ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name]</td> 
   <td> <p> Geben Sie einen Namen für den Webhook ein, z. B. „Asset erstellt“</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das dieser Webhook erstellt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Kommentare

* [[!UICONTROL Kommentar erstellen]](#create-a-comment)
* [[!UICONTROL Kommentar löschen]](#delete-a-comment)
* [[!UICONTROL Kommentar abrufen]](#get-a-comment)
* [[!UICONTROL Kommentare auflisten]](#list-comments)
* [[!UICONTROL Kommentar aktualisieren]](#update-a-comment)
* [[!UICONTROL Kommentar wurde aktualisiert]](#watch-comment-updated)
* [[!UICONTROL Neuen Kommentar ansehen]](#watch-new-comment)

#### [!UICONTROL Kommentar erstellen]

Dieses Aktionsmodul fügt dem Asset einen neuen Kommentar oder eine neue Antwort hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Typ] </td> 
   <td> <p>Wählen Sie aus, ob Sie einen Kommentar erstellen oder auf einen Kommentar antworten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das das Asset enthält, dem Sie einen Kommentar hinzufügen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, das das Asset enthält, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID] </td> 
   <td> <p>Wählen Sie den Ordner aus oder ordnen Sie die ID des Ordners zu, der das Asset enthält, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Wählen Sie das Asset aus, dem Sie einen Kommentar hinzufügen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentar-ID] </td> 
   <td> <p>Wählen Sie den Kommentar aus, dem Sie eine Antwort hinzufügen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Text]</td> 
   <td> <p> Geben Sie den Textinhalt des Kommentars oder der Antwort ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zeitstempel] </td> 
   <td> <p>Geben Sie die Bildnummer im Video ein, mit der der Kommentar verknüpft werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kommentar löschen]

Dieses Aktionsmodul löscht einen vorhandenen Kommentar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID]</td> 
   <td> <p> Wählen Sie das Team aus, dem das Projekt gehört, das das Asset enthält, aus dem Sie einen Kommentar löschen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID]</td> 
   <td> <p> Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, das das Asset enthält, aus dem Sie einen Kommentar löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID]</td> 
   <td> <p> Wählen Sie den Ordner aus, der das Asset enthält, aus dem Sie einen Kommentar löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Geben Sie die ID des Assets ein, das den zu löschenden Kommentar enthält, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentar-ID] </td> 
   <td> <p>Geben Sie die ID des Kommentars ein, den Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kommentar abrufen]

Dieses Aktionsmodul ruft Details des angegebenen Kommentars ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das den Ordner enthält, aus dem Sie Assets abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, das den Ordner enthält, aus dem Sie Assets abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, aus dem Sie Assets auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Wählen Sie das Asset aus, das den Kommentar enthält, den Sie abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentar-ID] </td> 
   <td> <p>Wählen Sie den Kommentar aus, zu dem Sie Details abrufen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kommentare auflisten]

Dieses Suchmodul ruft alle Kommentare des angegebenen Assets ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das den Ordner enthält, aus dem Sie Kommentare abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, das den Ordner enthält, aus dem Sie Kommentare abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, der das Asset enthält, dessen Kommentare Sie auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Wählen Sie das Asset aus, für das Sie Kommentare auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Kommentaren ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kommentar aktualisieren]

Dieses Aktionsmodul bearbeitet einen vorhandenen Kommentar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, dem das Projekt gehört, das das Asset enthält, für das Sie einen Kommentar aktualisieren möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, das das Asset enthält, für das Sie einen Kommentar aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID] </td> 
   <td> <p>Wählen Sie den Ordner aus, der das Asset enthält, für das Sie einen Kommentar aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Wählen Sie das Asset aus, für das Sie einen Kommentar aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentar-ID] </td> 
   <td> <p>Wählen Sie den Kommentar aus, den Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Text]</td> 
   <td> <p> Geben Sie den Textinhalt des Kommentars ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zeitstempel] </td> 
   <td> <p>Geben Sie die Bildnummer im Video ein, mit dem der Kommentar verknüpft ist.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kommentar wurde aktualisiert]

Dieses Kommentarmodul startet ein Trigger, wenn ein Kommentar bearbeitet wird.

Da dies ein sofortiger Trigger ist, müssen Sie einen Webhook für das Modul auswählen oder erstellen, um es zu verwenden.

Wenn Sie einen Webhook hinzufügen, geben Sie die folgenden Informationen ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name] </td> 
   <td> <p>Geben Sie den Namen des Webhooks ein, z. B. Kommentar bearbeitet.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das dieser Webhook erstellt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Neuen Kommentar ansehen]

Dieses Trigger-Modul startet ein Szenario, wenn ein neuer Kommentar oder eine neue Antwort erstellt wird.

Da dies ein sofortiger Trigger ist, müssen Sie einen Webhook für das Modul auswählen oder erstellen, um es zu verwenden.

Wenn Sie einen Webhook hinzufügen, geben Sie die folgenden Informationen ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name] </td> 
   <td> <p>Den Namen des Webhooks eingeben, z. B. Neuer Kommentar.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das dieser Webhook erstellt wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projekte

#### [!UICONTROL Projekte auflisten]

Dieses Suchmodul ruft alle Projekte für das angegebene Team ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team-ID] </td> 
   <td> <p>Wählen Sie das Team aus, für das Sie Projekte abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Projekten ein, die das Modul während jedes Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

#### [!UICONTROL Erstellen eines API-Aufrufs]

Mit diesem Modul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://api.frame.io</code> ein. Beispiel: <code> /v2/teams</code></p> <p>Hinweis: Eine Liste der verfügbaren Endpunkte finden Sie in der [!DNL Frame.io] API-Referenz.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Methode]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt Autorisierungs-Header automatisch hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge] </td> 
   <td> <p>Geben Sie die Abfragezeichenfolge der Anfrage ein. Klicken Sie für jeden Parameter, den Sie in die Abfragezeichenfolge aufnehmen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie den Namen des Felds und den gewünschten Wert ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


<!-- 
**Example:** The following API call returns all teams and its details in your [!DNL Frame.io] account:

URL: `/v2/teams`

Method: `GET`

![API call example](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![API call output](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
