---
title: Frame.io (Beta)-Module
description: Das [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] Konto.
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: cc1ce10fccf159a0c17a3bba978d88c0d1013cbf
workflow-type: tm+mt
source-wordcount: '2936'
ht-degree: 1%

---

# [!DNL Frame.io] Beta (V4)-Module

>[!IMPORTANT]
>
>Dieser Artikel beschreibt die neue (Beta-)Version des Frame.io-Connectors. Dieser Connector wird verwendet, um eine Verbindung mit Frame.io Version 4 herzustellen.
>
>Anweisungen zur alten Version des Frame.io-Connectors finden Sie unter [Frame.io Legacy-Connector](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).

Mit den [!DNL Adobe Workfront Fusion] [!DNL Frame.io] können Sie Assets und Kommentare in Ihrem [!DNL Frame.io]-Konto überwachen, erstellen, aktualisieren, abrufen oder löschen.

Workfront bietet zwei Frame.io-Connectoren, die auf der Version von Frame.io basieren, mit der Sie eine Verbindung herstellen.

| Connector | Frame.io-Version |
|---|---|
| Frame.io (Beta) | v4 |
| Frame.io (veraltet) | v3 |

Anweisungen zur alten Version des Frame.io-Connectors finden Sie unter [Frame.io Legacy-Connector](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


Eine Videoeinführung zum Frame.io-Connector finden Sie unter:

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

Um [!DNL Frame.io] Module verwenden zu können, müssen Sie über ein [!DNL Frame.io] verfügen

## Frame.io-API-Informationen

Der Frame.io-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.frame.io/v4</td> 
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

Sie können automatisch eine Verbindung mit Benutzeranmeldeinformationen herstellen, manuell eine Verbindung mit Benutzeranmeldeinformationen erstellen oder eine Server-zu-Server-Verbindung erstellen.

* [Automatisch mit Benutzeranmeldeinformationen verbinden](#connect-automatically-with-user-credentials#)
* [Manuelles Erstellen einer Verbindung mit Benutzeranmeldeinformationen](#create-a-user-credentials-connection-manually)
* [Erstellen einer Server-zu-Server-Verbindung](#create-a-server-to-server-connection)

### Automatisch mit Benutzeranmeldeinformationen verbinden

Diese Methode erstellt automatisch eine Verbindung, wenn Sie bei Frame.io angemeldet sind, oder verbindet Sie mit der Anmeldeseite von Frame.io, damit Sie sich anmelden können.

1. Klicken Sie in einem beliebigen Frame.io-Beta **[!UICONTROL Modul]** Hinzufügen“ neben dem Feld Verbindung .
1. Geben Sie einen Namen für die Verbindung ein.
1. Klicken Sie **Weiter**.
1. Wenn Sie aufgefordert werden, sich bei Ihrem Frame.io-Konto anzumelden, führen Sie diesen Schritt aus.
1. Wenn Sie Mitglied mehrerer Frame.io-Organisationen sind, wählen Sie die Organisation aus, die Sie für diese Verbindung verwenden möchten.

Die Verbindung wird erstellt.

### Manuelles Erstellen einer Verbindung mit Benutzeranmeldeinformationen

Sie können eine Verbindung mit Benutzeranmeldeinformationen erstellen, indem Sie sich bei Frame.io anmelden oder eine Client-ID oder ein Client-Geheimnis angeben.

Um eine Server-zu-Server-Verbindung zu erstellen, müssen Sie zunächst eine Anwendung in der Adobe Developer Console konfigurieren.

* [Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console](#create-user-credentials-in-the-adobe-developer-console)
* [Konfigurieren einer Benutzerauthentifizierungsverbindung](#configure-a-user-authentication-connection)

#### Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console

Wenn Sie noch keine Server-zu-Server-Anmeldeinformationen für ein Adobe Developer Console-Projekt haben, können Sie sie erstellen.

1. Öffnen Sie die [Adobe Developer Console](https://developer.adobe.com/).
1. Vorhandenes Projekt in der Adobe Developer Console auswählen, das für diese Verbindung verwendet werden soll

   Oder

   Erstellen Sie ein neues Projekt in der Adobe Developer Console. Anweisungen finden Sie unter [Leeres Projekt erstellen](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Klicken Sie auf der Seite „Projektübersicht“ oder auf der Seite Erste Schritte mit Ihrem neuen Projekt auf **API hinzufügen**.
1. Suchen Sie auf der sich öffnenden Seite nach „Frame.io **&quot; und klicken Sie darauf**.
1. Wählen Sie auf der Seite Authentifizierungstyp auswählen die Option **Benutzerauthentifizierung** und klicken Sie auf **Weiter**.
1. Wählen Sie auf der Seite Anmeldedaten für Benutzerauthentifizierung hinzufügen die Option **OAuth Web App** aus und klicken Sie auf **Weiter**.
1. Geben Sie auf der Seite Anmeldedaten für OAuth-Web-App konfigurieren Folgendes ein:   <table style="table-layout:auto">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Standard-Umleitungs-URI]</td>
          <td>
            <p><code>https://oauth.app.workfrontfusion.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Umleitungs-URI-Muster]</td>
          <td>
            <p><code>https://oauth\.app\.workfrontfusion\.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
       </tbody>
    </table>
1. Klicken Sie **Weiter**.
1. Klicken Sie **Konfigurierte API speichern**.
1. Klicken Sie auf der Produktseite auf die Karte für die soeben erstellten Anmeldeinformationen.

   Hier finden Sie Ihre Client-ID und Ihr Client-Geheimnis.

>[!NOTE]
>
> Es wird empfohlen, dieses Fenster offen zu lassen, wenn Sie mit der Konfiguration Ihrer Verbindung in Adobe Workfront Fusion beginnen. Sie können die Client-ID kopieren und Client-Geheimnis von dieser Seite abrufen und kopieren, um es in die Verbindungsfelder einzufügen.


#### Konfigurieren einer Benutzerauthentifizierungsverbindung

1. Klicken Sie in einem beliebigen Frame.io-Beta **[!UICONTROL Modul]** Hinzufügen“ neben dem Feld Verbindung .
1. Klicken Sie im Feld Verbindung erstellen auf **Erweiterte Einstellungen anzeigen**.

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
            <p>Wählen Sie <b>IMS-Benutzerauthentifizierung</b> aus.</p>
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
          <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL Client ID] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie unter <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console</a> in diesem Artikel.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
          <td>Geben Sie Ihren [!DNL Adobe] [!UICONTROL Client Secret] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie unter <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console</a> in diesem Artikel.</p>
        </tr>
       </tbody>
    </table>
1. Wenn Sie aufgefordert werden, sich bei Ihrem Frame.io-Konto anzumelden, führen Sie diesen Schritt aus.
1. Wenn Sie Mitglied mehrerer Frame.io-Organisationen sind, wählen Sie die Organisation aus, die Sie für diese Verbindung verwenden möchten.

Die Verbindung wird erstellt.


### Erstellen einer Server-zu-Server-Verbindung

Um eine Server-zu-Server-Verbindung zu erstellen, müssen Sie zunächst eine Anwendung in der Adobe Developer Console konfigurieren.

* [Erstellen von Server-zu-Server-Anmeldeinformationen in der Adobe Developer Console](#create-server-to-server-credentials-in-the-adobe-developer-console)
* [Konfigurieren einer Server-zu-Server-Verbindung](#configure-a-server-to-server-connection)

#### Erstellen von Server-zu-Server-Anmeldeinformationen in der Adobe Developer Console

Wenn Sie noch keine Server-zu-Server-Anmeldeinformationen für ein Adobe Developer Console-Projekt haben, können Sie sie erstellen.

1. Öffnen Sie die [Adobe Developer Console](https://developer.adobe.com/).
1. Vorhandenes Projekt in der Adobe Developer Console auswählen, das für diese Verbindung verwendet werden soll

   Oder

   Erstellen Sie ein neues Projekt in der Adobe Developer Console. Anweisungen finden Sie unter [Leeres Projekt erstellen](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Klicken Sie auf der Seite „Projektübersicht“ oder auf der Seite Erste Schritte mit Ihrem neuen Projekt auf **API hinzufügen**.
1. Suchen Sie auf der sich öffnenden Seite nach „Frame.io **&quot; und klicken Sie darauf**.
1. Wählen Sie auf der Seite Authentifizierungstyp auswählen die Option **Server-zu-Server** und klicken Sie auf **Weiter**.
1. Geben Sie einen Namen für die Anmeldeinformationen ein. Auf diese Weise können Sie die Anmeldeinformationen später im Bereich API-Anmeldeinformationen der Adobe Admin Console identifizieren.
1. Klicken Sie **Weiter**.
1. Wählen Sie auf der Seite Produktprofile auswählen das Produktprofil aus, das das Frame.io-Konto enthält, mit dem Sie eine Verbindung herstellen möchten.
1. Klicken Sie **Konfigurierte API speichern**.
1. Klicken Sie auf der Produktseite auf die Karte für die soeben erstellten Anmeldeinformationen.

   Hier finden Sie Ihre Client-ID und Ihr Client-Geheimnis.

>[!NOTE]
>
> Es wird empfohlen, dieses Fenster offen zu lassen, wenn Sie mit der Konfiguration Ihrer Verbindung in Adobe Workfront Fusion beginnen. Sie können die Client-ID kopieren und Client-Geheimnis von dieser Seite abrufen und kopieren, um es in die Verbindungsfelder einzufügen.


#### Konfigurieren einer Server-zu-Server-Verbindung

1. Klicken Sie in einem beliebigen Frame.io-Beta **[!UICONTROL Modul]** Hinzufügen“ neben dem Feld Verbindung .

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
            <p>Wählen Sie <b>IMS-Server zu Server</b> aus.</p>
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
          <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL Client ID] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie unter <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Server-zu-Server-Anmeldeinformationen in der Adobe Developer Console</a> in diesem Artikel.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
          <td>Geben Sie Ihren [!DNL Adobe] [!UICONTROL Client Secret] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie unter <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Server-zu-Server-Anmeldeinformationen in der Adobe Developer Console</a> in diesem Artikel.</p>
        </tr>
       </tbody>
    </table>
1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.




## [!DNL Frame.io] Module und ihre Felder

Beim Konfigurieren [!DNL Frame.io] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Frame.io] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Assets](#assets)
* [Kommentare](#comments)
* [Ordner](#folders)
* [Projekte](#projects)
* [Aktien](#shares)
* [Arbeitsbereiche](#workspaces)
* [Sonstige](#other)

### Assets

* [[!UICONTROL Erstellen eines Assets]](#create-an-asset)
* [[!UICONTROL Löschen eines Assets]](#delete-an-asset)
* [[!UICONTROL Asset abrufen]](#get-an-asset)
* [[!UICONTROL Assets auflisten]](#list-assets)
* [[!UICONTROL Aktualisieren eines Assets]](#update-an-asset)

#### [!UICONTROL Erstellen eines Assets] <!--different for v4-->

Dieses Aktionsmodul erstellt ein neues Asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das Projekt enthält, für das Sie ein Asset erstellen möchten.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus oder ordnen Sie die ID des Arbeitsbereichs zu, der das Projekt enthält, für das Sie ein Asset erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das Sie ein Asset erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL path] </td> 
   <td> <p>Wählen Sie den Pfad aus, unter dem Sie ein Asset erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dateiname] </td> 
   <td> <p>Geben Sie den Namen der Datei ein, die Sie für dieses Asset verwenden möchten.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">Dateigröße </td> 
    <td> <p>Geben Sie die Dateigröße in Byte ein oder mappen Sie sie.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>Wenn Sie eine Datei erstellen, geben Sie die URL der Datei ein, die Sie hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Medientyp] </td> 
   <td> <p>Medientyp für dieses Asset auswählen.</p> </td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das zu löschende Asset enthält.</p> </td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das abzurufende Asset enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Wählen Sie das Asset aus, das Sie abrufen möchten, oder ordnen Sie es zu.</p> </td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das -Konto aus oder ordnen Sie die ID des -Kontos zu, das die Assets enthält, die Sie auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Assets] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Kommentare

* [[!UICONTROL Kommentar erstellen]](#create-a-comment)
* [[!UICONTROL Kommentar löschen]](#delete-a-comment)
* [[!UICONTROL Kommentar abrufen]](#get-a-comment)
* [[!UICONTROL Kommentare auflisten]](#list-comments)
* [[!UICONTROL Kommentar aktualisieren]](#update-a-comment)

#### [!UICONTROL Kommentar erstellen]

Dieses Aktionsmodul fügt dem Asset einen neuen Kommentar oder eine neue Antwort hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das Asset enthält, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Arbeitsbereichs zu, der das Asset enthält, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, das das Asset enthält, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL path] </td> 
   <td> <p>Wählen Sie den Pfad zum Asset aus, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Text]</td> 
   <td> <p> Geben Sie den Textinhalt des Kommentars oder der Antwort ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zeitstempel] </td> 
   <td> <p>Geben Sie die Bildnummer im Video ein, mit der der Kommentar verknüpft werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Seite] </td> 
   <td> <p>Wenn es sich bei dem Asset um ein PDF handelt, geben Sie die Seite ein, an die der Kommentar angehängt werden soll, oder ordnen Sie sie zu.</p> </td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das den Kommentar enthält, den Sie löschen möchten.</p> </td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das den Kommentar enthält, zu dem Sie Details abrufen möchten.</p> </td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Asset enthält, von dem Sie Kommentare abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, der das Asset enthält, von dem Sie Kommentare abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, das das Asset enthält, von dem Sie Kommentare abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL path] </td> 
   <td> <p>Wählen Sie den Pfad aus, der zu dem Asset führt, dessen Kommentare Sie auflisten möchten.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Kommentare] </td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Projekt mit dem Asset enthält, für das Sie einen Kommentar aktualisieren möchten, oder ordnen Sie es zu.</p> </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL-Seite] </td> 
   <td> <p>Wenn es sich bei dem Asset um ein PDF handelt, geben Sie die Seite ein, an die der Kommentar angehängt ist, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ordner

#### Erstellen eines Ordners

Dieses Aktionsmodul erstellt einen neuen Ordner in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem Sie einen Ordner erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, in dem Sie einen Ordner erstellen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie die aus, in der Sie einen Ordner erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL path] </td> 
   <td> <p>Wählen Sie den Pfad aus, unter dem Sie einen Ordner erstellen möchten.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projekte

* [Erstellen eines Projekts](#create-a-project)
* [Auflisten von Projekten](#list-projects)

#### Erstellen eines Projekts

Dieses Aktionsmodul erstellt ein neues Projekt in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem Sie ein Projekt erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, in dem Sie ein Projekt erstellen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen Namen für das neue Projekt ein oder mappen Sie ihn.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Projekte auflisten]

Dieses Suchmodul ruft alle Projekte für das angegebene Team ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Asset enthält, von dem Sie Projekte abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, der das Asset enthält, von dem Sie Projekte abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Projekte] </td> 
   <td> <p>Maximale Anzahl von Projekten eingeben oder zuordnen
   Das Modul soll bei jedem Ausführungszyklus des Szenarios zurückgegeben werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktien

* [Hinzufügen eines Assets zu einem Freigabe-Link](#add-an-asset-to-a-share-link)
* [Erstellen eines Freigabe-Links](#create-a-share-link)

#### Hinzufügen eines Assets zu einem Freigabe-Link

Dieses Aktionsmodul fügt ein Asset zu einem Freigabe-Link in Frame.io hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das den Freigabe-Link enthält, dem Sie ein Asset hinzufügen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Freigabe-Link-ID] </td> 
   <td> <p>Wählen Sie den Freigabe-Link aus, dem Sie ein Asset hinzufügen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Geben Sie die ID des Assets ein, das Sie dem Freigabe-Link hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen eines Freigabe-Links

Dieses Aktionsmodul erstellt einen neuen Freigabe-Link in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, für das Sie einen Freigabe-Link erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, in dem Sie einen Freigabe-Link erstellen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, in dem Sie einen Freigabe-Link erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Zugriff </td> 
   <td> <p>Wählen Sie aus, ob dieser Link öffentlichen oder eingeschränkten Zugriff hat.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Assets </td> 
   <td> <p>Klicken Sie für jedes Asset, das Sie zum Freigabe-Link hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie die Asset-ID ein.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Beschreibung </td> 
   <td> <p>Geben Sie eine Beschreibung für den Freigabe-Link ein oder mappen Sie sie.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie das Ablaufdatum für den Freigabe-Link ein oder mappen Sie es.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen Namen für den neuen Freigabe-Link ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie eine Passphrase für den Freigabe-Link ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Arbeitsbereiche

#### Arbeitsbereich erstellen

Dieses Aktionsmodul erstellt einen neuen Arbeitsbereich in Frame.io

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem Sie einen Arbeitsbereich erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen neuen Namen für den Arbeitsbereich ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Auflisten von Arbeitsbereichen

Dieses Modul listet alle Arbeitsbereiche in einem Konto auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Asset enthält, von dem Sie Arbeitsbereiche abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Arbeitsbereiche] </td> 
   <td> <p>Maximale Anzahl von Arbeitsbereichen eingeben oder zuordnen
   Das Modul soll bei jedem Ausführungszyklus des Szenarios zurückgegeben werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstige

#### [!UICONTROL Erstellen eines benutzerdefinierten API-Aufrufs]

Mit diesem Modul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit [!DNL Adobe Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://api.frame.io</code> ein. Beispiel: <code> /v4/me</code></p> <p>Hinweis: Eine Liste der verfügbaren Endpunkte finden Sie in der [!DNL Frame.io] API-Referenz.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Methode]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
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
