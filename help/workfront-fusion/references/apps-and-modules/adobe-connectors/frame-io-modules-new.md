---
title: Frame.io-Module
description: Die [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] Konto.
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: 3cb613c11500dfc94774783ee0b38e6f1768de20
workflow-type: tm+mt
source-wordcount: '4539'
ht-degree: 85%

---

# [!DNL Frame.io] V4-Module

>[!IMPORTANT]
>
>In diesem Artikel wird die neue Version des Frame.io-Connectors beschrieben. Dieser Connector wird verwendet, um eine Verbindung zu Frame.io Version 4 herzustellen.
>
>Anweisungen zur Legacy-Version des Frame.io-Connectors finden Sie unter [Frame.io-Connector für Legacy-Versionen](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).

Mit den [!DNL Frame.io]-Modulen von Adobe Workfront Fusion können Sie Assets und Kommentare in Ihrem [!DNL Frame.io]-Konto überwachen, erstellen, aktualisieren, abrufen oder löschen.

Workfront bietet zwei Frame.io-Connectoren an, abhängig von der Frame.io-Version, zu der Sie eine Verbindung herstellen.

| Connector | Frame.io-Version |
|---|---|
| Frame.io | V4 |
| Frame.io (Legacy) | V3 |

Anweisungen zur Legacy-Version des Frame.io-Connectors finden Sie unter [Frame.io-Connector für Legacy-Versionen](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


Eine Videoeinführung zum Frame.io-Connector finden Sie über folgenden Link:

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

Um [!DNL Frame.io]-Module verwenden zu können, müssen Sie über ein [!DNL Frame.io]-Konto verfügen.

## Informationen zur Frame.io-API

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

Sie können automatisch oder manuell eine Verbindung mit Benutzeranmeldeinformationen oder eine Server-zu-Server-Verbindung erstellen.

* [Automatisches Erstellen einer Verbindung mit Benutzeranmeldeinformationen](#connect-automatically-with-user-credentials#)
* [Manuelles Erstellen einer Verbindung mit Benutzeranmeldeinformationen](#create-a-user-credentials-connection-manually)
* [Erstellen einer Server-zu-Server-Verbindung](#create-a-server-to-server-connection)

### Automatisches Erstellen einer Verbindung mit Benutzeranmeldeinformationen

Diese Methode stellt automatisch eine Verbindung her, wenn Sie bei Frame.io angemeldet sind, oder leitet Sie zur Anmeldeseite von Frame.io weiter, damit Sie sich anmelden können.

1. Klicken Sie in einem beliebigen Frame.io-Modul neben dem Verbindungsfeld auf die Option **[!UICONTROL Add]**.
1. Geben Sie einen Namen für die Verbindung ein.
1. Klicken Sie auf **Fortfahren**.
1. Wenn Sie zur Anmeldung bei Ihrem Frame.io-Konto aufgefordert werden, führen Sie diese durch.
1. Wenn Sie Mitglied mehrerer Frame.io-Organisationen sind, wählen Sie die Organisation aus, die Sie für diese Verbindung verwenden möchten.

Die Verbindung wird hergestellt.

### Manuelles Erstellen einer Verbindung mit Benutzeranmeldeinformationen

Sie können eine Verbindung mit Benutzeranmeldeinformationen erstellen, indem Sie sich bei Frame.io anmelden oder eine Client-ID bzw. ein Client-Geheimnis angeben.

Um eine Server-zu-Server-Verbindung zu erstellen, müssen Sie zunächst eine Anwendung in der Adobe Developer Console konfigurieren.

* [Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console](#create-user-credentials-in-the-adobe-developer-console)
* [Konfigurieren einer Verbindung mit Benutzerauthentifizierung](#configure-a-user-authentication-connection)

#### Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console

Falls Sie noch keine Server-zu-Server-Anmeldeinformationen für ein Adobe Developer Console-Projekt haben, können Sie diese erstellen.

1. Öffnen Sie die [Adobe Developer Console](https://developer.adobe.com/).
1. Wählen Sie ein vorhandenes Projekt in der Adobe Developer Console aus, das für diese Verbindung verwendet werden soll.

   ODER

   Erstellen Sie ein neues Projekt in der Adobe Developer Console. Anweisungen finden Sie auf der Seite zum [Erstellen eines leeren Projekts](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Klicken Sie auf der Seite für den Projektüberblick oder der Seite für erste Schritte mit Ihrem neuen Projekt auf die Option **Add API**.
1. Suchen Sie auf der sich öffnenden Seite nach der Option **Frame.io API** und klicken Sie darauf.
1. Wählen Sie auf der Seite zum Auswählen des Authentifizierungstyps die Option **User Authentication** aus und klicken Sie auf **Next**.
1. Wählen Sie auf der Seite zum Hinzufügen von Benutzerauthentifizierung und Anmeldeinformationen die Option **OAuth Web App** aus und klicken Sie auf **Next**.
1. Geben Sie auf der Seite zum Konfigurieren von Anmeldeinformationen für OAuth-Web-Anwendungen Folgendes ein:   <table style="table-layout:auto">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Standardumleitungs-URI]</td>
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
1. Klicken Sie auf **Weiter**.
1. Klicken Sie auf **Save configured API**.
1. Klicken Sie auf der Produktseite auf die Karte für die soeben erstellten Anmeldeinformationen.

   Hier finden Sie Ihre Client-ID und Ihr Client-Geheimnis.

>[!NOTE]
>
> Es wird empfohlen, dieses Fenster geöffnet zu lassen, während Sie mit der Konfiguration Ihrer Verbindung in Adobe Workfront Fusion beginnen. Sie können die Client-ID kopieren und das Client-Geheimnis von dieser Seite abrufen und kopieren, um beide in die Verbindungsfelder einzufügen.


#### Konfigurieren einer Verbindung mit Benutzerauthentifizierung

1. Klicken Sie in einem beliebigen Frame.io-Modul neben dem Verbindungsfeld auf **[!UICONTROL Add]**.
1. Klicken Sie im Feld zum Erstellen einer Verbindung auf **Show advanced settings**.

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
            <p>Wählen Sie die Option <b>IMS User authentication</b> aus.</p>
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
          <td>Geben Sie Ihre [!DNL Adobe]-[!UICONTROL Client-ID] ein. Diese finden Sie im Abschnitt mit den [!UICONTROL Anmeldeinformationen-Details] der [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie in diesem Artikel unter <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console</a>.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
          <td>Geben Sie Ihr [!DNL Adobe]-[!UICONTROL Client-Geheimnis] ein. Diese finden Sie im Abschnitt mit den [!UICONTROL Anmeldeinformationen-Details] der [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie in diesem Artikel unter <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console</a>.</p>
        </tr>
       </tbody>
    </table>
1. Wenn Sie zur Anmeldung bei Ihrem Frame.io-Konto aufgefordert werden, führen Sie diese durch.
1. Wenn Sie Mitglied mehrerer Frame.io-Organisationen sind, wählen Sie die Organisation aus, die Sie für diese Verbindung verwenden möchten.

Die Verbindung wird hergestellt.


### Erstellen einer Server-zu-Server-Verbindung

Um eine Server-zu-Server-Verbindung zu erstellen, müssen Sie zunächst eine Anwendung in der Adobe Developer Console konfigurieren.

* [Erstellen von Server-zu-Server-Anmeldeinformationen in der Adobe Developer Console](#create-server-to-server-credentials-in-the-adobe-developer-console)
* [Konfigurieren einer Server-zu-Server-Verbindung](#configure-a-server-to-server-connection)

#### Erstellen von Server-zu-Server-Anmeldeinformationen in der Adobe Developer Console

Falls Sie noch keine Server-zu-Server-Anmeldeinformationen für ein Adobe Developer Console-Projekt haben, können Sie diese erstellen.

1. Öffnen Sie die [Adobe Developer Console](https://developer.adobe.com/).
1. Wählen Sie ein vorhandenes Projekt in der Adobe Developer Console aus, das für diese Verbindung verwendet werden soll.

   ODER

   Erstellen Sie ein neues Projekt in der Adobe Developer Console. Anweisungen finden Sie auf der Seite zum [Erstellen eines leeren Projekts](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Klicken Sie auf der Seite für den Projektüberblick oder der Seite für erste Schritte mit Ihrem neuen Projekt auf die Option **Add API**.
1. Suchen Sie auf der sich öffnenden Seite nach der Option **Frame.io API** und klicken Sie darauf.
1. Wählen Sie auf der Seite zum Auswählen des Authentifizierungstyps die Option **Server-to-Server Authentication** aus und klicken Sie auf **Next**.
1. Geben Sie einen Namen für die Anmeldeinformationen ein. Auf diese Weise können Sie die Anmeldeinformationen später im Bereich für API-Anmeldeinformationen der Adobe Admin Console identifizieren.
1. Klicken Sie auf **Weiter**.
1. Wählen Sie auf der Seite zum Auswählen von Produktprofilen das Produktprofil aus, das das Frame.io-Konto enthält, mit dem Sie eine Verbindung herstellen möchten.
1. Klicken Sie auf **Save configured API**.
1. Klicken Sie auf der Produktseite auf die Karte für die soeben erstellten Anmeldeinformationen.

   Hier finden Sie Ihre Client-ID und Ihr Client-Geheimnis.

>[!NOTE]
>
> Es wird empfohlen, dieses Fenster geöffnet zu lassen, während Sie mit der Konfiguration Ihrer Verbindung in Adobe Workfront Fusion beginnen. Sie können die Client-ID kopieren und das Client-Geheimnis von dieser Seite abrufen und kopieren, um beide in die Verbindungsfelder einzufügen.


#### Konfigurieren einer Server-zu-Server-Verbindung

1. Klicken Sie in einem beliebigen Frame.io-Modul neben dem Verbindungsfeld auf **[!UICONTROL Add]**.

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
            <p>Wählen Sie die Option <b>IMS Server to Server</b> aus.</p>
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
          <td>Geben Sie Ihre [!DNL Adobe]-[!UICONTROL Client-ID] ein. Diese finden Sie im Abschnitt mit den [!UICONTROL Anmeldeinformationen-Details] der [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie in diesem Artikel unter <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Server-zu-Server-Anmeldeinformationen in der Adobe Developer Console</a>.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
          <td>Geben Sie Ihr [!DNL Adobe]-[!UICONTROL Client-Geheimnis] ein. Diese finden Sie im Abschnitt mit den [!UICONTROL Anmeldeinformationen-Details] der [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie in diesem Artikel unter <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Server-zu-Server-Anmeldeinformationen in der Adobe Developer Console</a>.</p>
        </tr>
       </tbody>
    </table>
1. Klicken Sie auf **[!UICONTROL Continue]**, um die Verbindung zu speichern und zum Modul zurückzukehren.




## [!DNL Frame.io]-Module und ihre Felder

Beim Konfigurieren von [!DNL Frame.io]-Modulen werden in Workfront Fusion die unten aufgeführten Felder angezeigt. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere [!DNL Frame.io]-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Assets](#assets)
* [Kommentare](#comments)
* [Ordner](#folders)
* [Projekte](#projects)
* [Freigaben](#shares)
* [Arbeitsbereiche](#workspaces)
* [Metadaten](#metadata)
* [Sonstiges](#other)

### Assets

* [[!UICONTROL Asset erstellen]](#create-an-asset)
* [[!UICONTROL Asset löschen]](#delete-an-asset)
* [[!UICONTROL Asset abrufen]](#get-an-asset)
* [[!UICONTROL Assets auflisten]](#list-assets)
* [Gelöschtes Asset überwachen](#watch-asset-deleted)
* [Neues Asset überwachen](#watch-new-asset)

#### [!UICONTROL Asset erstellen] <!--different for v4-->

Dieses Aktionsmodul erstellt ein neues Asset. Sie können eine lokale Datei hochladen oder die URL für eine Remote-Datei angeben, aus der das Asset erstellt werden soll.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das Projekt enthält, für das ein Asset erstellt werden soll.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus oder ordnen Sie die ID des Arbeitsbereichs zu, der das Projekt enthält, für das ein Asset erstellt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das ein Asset erstellt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pfad] </td> 
   <td> <p>Wählen Sie den Pfad aus, unter dem ein Asset erstellt werden soll.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td> <p>Enter the name of the file that you want to use for this asset.</p> </td> 
  </tr> -->
    <tr> 
    <td role="rowheader">Upload-Typ </td> 
    <td> <p>Wählen Sie aus, ob Sie ein Asset aus einer lokalen Datei oder einer Remote-Lebensdauer erstellen möchten.</p> </td> 
   </tr>
    <tr> 
    <td role="rowheader">Dateigröße </td> 
    <td> <p>Wenn Sie eine lokale Datei hochladen, geben Sie die Dateigröße in Byte ein oder ordnen Sie sie zu.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Quell-URL] </td> 
   <td> <p>Wenn Sie das Asset aus einer Remote-Datei erstellen, geben Sie die URL der Datei ein, die Sie hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Quelldatei zu.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>Select the media type for this asset.</p> </td> 
  </tr> -->
  </tbody> 
</table>

#### [!UICONTROL Erstellen eines Assets (veraltet)] <!--different for v4-->

Dieses Aktionsmodul erstellt ein neues Asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das Projekt enthält, für das ein Asset erstellt werden soll.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus oder ordnen Sie die ID des Arbeitsbereichs zu, der das Projekt enthält, für das ein Asset erstellt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das ein Asset erstellt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pfad] </td> 
   <td> <p>Wählen Sie den Pfad aus, unter dem ein Asset erstellt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dateiname] </td> 
   <td> <p>Geben Sie den Namen der Datei ein, die für dieses Asset verwendet werden soll.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">Dateigröße </td> 
    <td> <p>Geben Sie die Dateigröße in Byte ein oder ordnen Sie diese zu.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Quell-URL] </td> 
   <td> <p>Wenn Sie eine Datei erstellen, geben Sie die URL der Datei ein, die hochgeladen werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Medientyp] </td> 
   <td> <p>Wählen Sie den Medientyp für dieses Asset aus.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL Asset löschen]

Dieses Aktionsmodul löscht ein angegebenes Asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das zu löschende Asset enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Wählen Sie das Asset aus, das gelöscht werden soll, oder ordnen Sie dieses zu.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das abzurufende Asset enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Wählen Sie das Asset aus, das abgerufen werden soll, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Asset auflisten]

Dieses Suchmodul ruft alle Assets im Ordner des angegebenen Projekts ab.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das die aufzulistenden Assets enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Assets] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, die das Modul während jedes Ausführungszyklus eines Szenarios zurückgeben soll, oder ordnen Sie eine Zahl zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Gelöschtes Asset überwachen

Dieses Auslösermodul startet ein Szenario, wenn ein Asset gelöscht wird.

Wählen Sie den Webhook aus, der für dieses Modul verwendet werden soll, oder klicken Sie neben dem Feld „Webhook“ auf „Hinzufügen“ und geben Sie die folgenden Informationen ein:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name] </td> 
   <td> <p>Geben Sie einen Namen für den neuen Webhook ein.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das auf gelöschte Assets überwacht werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Neues Asset überwachen

Dieses Auslösermodul startet ein Szenario, wenn ein neues Asset erstellt wird.

Wählen Sie den Webhook aus, der für dieses Modul verwendet werden soll, oder klicken Sie neben dem Feld „Webhook“ auf „Hinzufügen“ und geben Sie die folgenden Informationen ein:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name] </td> 
   <td> <p>Geben Sie einen Namen für den neuen Webhook ein.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das auf neue Assets überwacht werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Kommentare

* [[!UICONTROL Kommentar erstellen]](#create-a-comment)
* [[!UICONTROL Kommentar löschen]](#delete-a-comment)
* [[!UICONTROL Kommentar abrufen]](#get-a-comment)
* [[!UICONTROL Kommentare auflisten]](#list-comments)
* [[!UICONTROL Kommentar aktualisieren]](#update-a-comment)
* [Kommentaraktualisierungen überwachen](#watch-comment-updated)
* [Neue Kommentare überwachen](#watch-new-comment)

#### [!UICONTROL Kommentar erstellen]

Dieses Aktionsmodul fügt dem Asset einen neuen Kommentar oder eine neue Antwort hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das Asset enthält, dem ein Kommentar hinzugefügt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus oder ordnen Sie die ID des Arbeitsbereichs zu, der das Asset enthält, dem ein Kommentar hinzugefügt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, das das Asset enthält, dem ein Kommentar hinzugefügt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pfad] </td> 
   <td> <p>Wählen Sie den Pfad zu dem Asset aus, dem ein Kommentar hinzugefügt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Geben Sie den Textinhalt des Kommentars oder der Antwort ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zeitstempel] </td> 
   <td> <p>Geben Sie die Frame-Nummer in dem Video ein, mit dem der Kommentar verknüpft werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seite] </td> 
   <td> <p>Wenn es sich bei dem Asset um eine PDF-Datei handelt, geben Sie die Seite ein, an die der Kommentar angefügt werden soll, oder ordnen Sie diese zu.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das den zu löschenden Kommentar enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentar-ID] </td> 
   <td> <p>Geben Sie die ID des Kommentars ein, der gelöscht werden soll, oder ordnen Sie diese zu.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das den Kommentar enthält, zu dem Details abgerufen werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentar-ID] </td> 
   <td> <p>Wählen Sie den Kommentar aus, zu dem Details abgerufen werden sollen.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Asset enthält, von dem Kommentare abgerufen werden sollen, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, der das Asset enthält, von dem Kommentare abgerufen werden sollen, oder ordnen Sie diesen zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, das das Asset enthält, von dem Kommentare abgerufen werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pfad] </td> 
   <td> <p>Wählen Sie den Pfad zu dem Asset aus, dessen Kommentare aufgelistet werden sollen.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Kommentare] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Kommentaren ein, die das Modul während jedes Ausführungszyklus eines Szenarios zurückgeben soll, oder ordnen Sie eine Zahl zu.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Projekt mit dem Asset enthält, für das ein Kommentar aktualisiert werden soll, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentar-ID] </td> 
   <td> <p>Wählen Sie den Kommentar aus, der aktualisiert werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Geben Sie den Textinhalt des Kommentars ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zeitstempel] </td> 
   <td> <p>Geben Sie die Frame-Nummer in dem Video ein, mit dem der Kommentar verknüpft ist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seite] </td> 
   <td> <p>Wenn es sich bei dem Asset um eine PDF-Datei handelt, geben Sie die Seite ein, an die der Kommentar angefügt ist, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Kommentaraktualisierungen überwachen

Dieses Auslösermodul startet ein Szenario, wenn ein Kommentar aktualisiert wird.

Wählen Sie den Webhook aus, der für dieses Modul verwendet werden soll, oder klicken Sie neben dem Feld „Webhook“ auf „Hinzufügen“ und geben Sie die folgenden Informationen ein:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name] </td> 
   <td> <p>Geben Sie einen Namen für den neuen Webhook ein.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das auf aktualisierte Kommentare überwacht werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Neue Kommentare überwachen

Dieses Auslösermodul startet ein Szenario, wenn ein Kommentar erstellt wird.

Wählen Sie den Webhook aus, der für dieses Modul verwendet werden soll, oder klicken Sie neben dem Feld „Webhook“ auf „Hinzufügen“ und geben Sie die folgenden Informationen ein:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name] </td> 
   <td> <p>Geben Sie einen Namen für den neuen Webhook ein.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das auf neue Kommentare überwacht werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ordner

#### Ordner erstellen

Dieses Aktionsmodul erstellt einen neuen Ordner in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem ein Ordner erstellt werden soll, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, in dem ein Ordner erstellt werden soll, oder ordnen Sie diesen zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, in dem ein Ordner erstellt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pfad] </td> 
   <td> <p>Wählen Sie den Pfad aus, unter dem ein Ordner erstellt werden soll.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie dem neuen Ordner einen Namen zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projekte

* [Projekt erstellen](#create-a-project)
* [Benutzende zu einem Frame.io-Projekt einladen](#invite-users-to-frameio-project)
* [Projekte auflisten](#list-projects)

#### Projekt erstellen

Dieses Aktionsmodul erstellt ein neues Projekt in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem ein Projekt erstellt werden soll, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, in dem ein Projekt erstellt werden soll, oder ordnen Sie diesen zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen Namen für das neue Projekt ein oder ordnen Sie dem neuen Projekt einen Namen zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Benutzende zu einem Frame.io-Projekt einladen

Dieses Aktionsmodul lädt Benutzende zum angegebenen Frame.io-Projekt ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Projekt enthält, zu dem eine Person eingeladen werden soll, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, der das Projekt enthält, zu dem eine Person eingeladen werden soll, oder ordnen Sie diesen zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Projekt-ID </td> 
   <td> <p>Wählen Sie das Projekt aus, zu dem eine Person eingeladen werden soll, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Benutzer-ID </td> 
   <td> <p>Wählen Sie die Person aus, die zum Projekt eingeladen werden soll, oder ordnen Sie diese zu.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Asset enthält, von dem Projekte abgerufen werden sollen, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, der das Asset enthält, von dem Projekte abgerufen werden sollen, oder ordnen Sie diesen zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Projekte] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Projekten ein, die das Modul während jedes Ausführungszyklus eines Szenarios zurückgeben soll, oder ordnen Sie eine Zahl zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Freigaben

* [Assets zu einem Freigabe-Link hinzufügen](#add-an-asset-to-a-share-link)
* [Freigabe-Link erstellen](#create-a-share-link)

#### Assets zu einem Freigabe-Link hinzufügen

Dieses Aktionsmodul fügt ein Asset zu einem Freigabe-Link in Frame.io hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das den Freigabe-Link enthält, dem ein Asset hinzugefügt werden soll, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Freigabe-Link-ID] </td> 
   <td> <p>Wählen Sie den Freigabe-Link aus, dem ein Asset hinzugefügt werden soll, oder ordnen Sie diesen zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID] </td> 
   <td> <p>Geben Sie die ID des Assets ein, das dem Freigabe-Link hinzugefügt werden soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Freigabe-Link erstellen

Dieses Aktionsmodul erstellt einen neuen Freigabe-Link in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem ein Freigabe-Link erstellt werden soll, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, in dem ein Freigabe-Link erstellt werden soll, oder ordnen Sie diesen zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, in dem ein Freigabe-Link erstellt werden soll, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Zugriff </td> 
   <td> <p>Wählen Sie aus, ob dieser Link öffentlichen oder eingeschränkten Zugriff hat.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Assets </td> 
   <td> <p>Klicken Sie für jedes Asset, das zum Freigabe-Link hinzugefügt werden soll, auf <b>Element hinzufügen</b> und geben Sie die Asset-ID ein.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Beschreibung </td> 
   <td> <p>Geben Sie eine Beschreibung für den Freigabe-Link ein oder ordnen Sie diese zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie das Ablaufdatum für den Freigabe-Link ein oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen Namen für den neuen Freigabe-Link ein oder ordnen Sie dem Freigabe-Link einen Namen zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie eine Passphrase für den Freigabe-Link ein oder ordnen Sie diese zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Arbeitsbereiche

#### Arbeitsbereich erstellen

Dieses Aktionsmodul erstellt einen neuen Arbeitsbereich in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem ein Arbeitsbereich erstellt werden soll, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen neuen Namen für den Arbeitsbereich ein oder ordnen Sie dem Arbeitsbereich einen neuen Namen zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Arbeitsbereiche auflisten

Dieses Modul listet alle Arbeitsbereiche in einem Konto auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Asset enthält, von dem Arbeitsbereiche abgerufen werden sollen, oder ordnen Sie dieses zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Arbeitsbereiche] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Arbeitsbereichen ein, die das Modul während jedes Ausführungszyklus eines Szenarios zurückgeben soll, oder ordnen Sie eine Zahl zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Metadaten

* [Erstellen eines Felds auf Kontoebene](#create-an-account-level-field)
* [Löschen eines Felds auf Kontoebene](#delete-an-account-level-field)
* [Metadaten abrufen](#get-metadata)
* [Felder auf Kontoebene auflisten](#list-account-level-fields)
* [Aktualisieren einer Felddefinition auf Kontoebene](#update-an-account-level-field-definition)
* [Aktualisieren von Metadaten über mehrere Dateien hinweg](#update-metadata-across-multiple-files)

#### Erstellen eines Felds auf Kontoebene

Dieses Aktionsmodul erstellt und konfiguriert ein neues Metadatenfeld auf Kontoebene.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem Sie die Metadaten erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Feldtyp </td> 
   <td> <p>Wählen Sie den Typ des Metadatenfelds aus, das Sie erstellen möchten, und konfigurieren Sie dann die Optionen für dieses Feld.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen Namen für das neue Feld ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Löschen eines Felds auf Kontoebene

Dieses Aktionsmodul löscht ein einzelnes Metadatenfeld auf Kontoebene.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das zu löschende Metadatenfeld enthält, oder ordnen Sie es zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Felddefinitions-ID </td> 
   <td> <p>Geben Sie die ID des Felds ein, das Sie löschen möchten, oder ordnen Sie sie zu. Feld-IDs finden Sie mit dem Modul Felder auf Listenkontenebene .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Metadaten abrufen

Dieses Aktionsmodul ruft die Metadaten für eine Datei in Frame.io ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das die Datei enthält, für die Sie Metadaten abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Datei-ID </td> 
   <td> <p>Geben Sie die ID der Datei ein, für die Sie Metadaten abrufen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Null anzeigen </td> 
   <td> <p>Aktivieren Sie diese Option, um Felder mit einem Wert von null in die Ausgabe aufzunehmen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Felder auf Kontoebene auflisten

Dieses Modul ruft eine Liste von Metadatenfeldern auf Kontoebene für das angegebene Konto ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, dessen Felder Sie auflisten möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Vereinbarungen]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Feldern ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren einer Felddefinition auf Kontoebene

Dieses Modul aktualisiert die Definition eines einzelnen vorhandenen Metadatenfelds.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem Sie die Metadaten erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Felddefinitions-ID </td> 
   <td> <p>Geben Sie die ID des Felds ein, das Sie aktualisieren möchten, oder ordnen Sie sie zu. Feld-IDs finden Sie mit dem Modul Felder auf Listenkontenebene .</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Feldtyp </td> 
   <td> <p>Wenn Sie den Feldtyp des Felds ändern möchten, wählen Sie den Typ des Metadatenfelds aus, das Sie erstellen möchten, und konfigurieren Sie dann die Optionen für dieses Feld.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen neuen Namen für das Feld ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren von Metadaten über mehrere Dateien hinweg

Dieses Modul aktualisiert Metadatenfelder in einer oder mehreren Dateien mit von Ihnen angegebenen Werten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das die Dateien enthält, für die Sie Metadaten aktualisieren möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus oder ordnen Sie die ID des Arbeitsbereichs zu, der das Projekt enthält, für das ein Asset erstellt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das ein Asset erstellt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-IDs] </td> 
   <td> <p>Klicken Sie für jede Datei, für die Sie die Metadaten aktualisieren möchten, auf <b>Element hinzufügen</b> und geben Sie die ID der Datei ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Werte] </td> 
   <td> <p>Klicken Sie für jedes Feld, für das Sie die Metadaten aktualisieren möchten, auf <b>Element hinzufügen</b> und geben Sie die ID der Felddefinition und den Wert, den Sie in dieses Feld einfügen möchten, ein oder mappen Sie sie. Alle im Feld Datei-IDs angegebenen Dateien werden mit diesem Feldwert aktualisiert.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

* [Benutzerdefinierten API-Aufruf erstellen](#make-a-custom-api-call)
* [Ereignisse ansehen](#watch-events)
* [Aktualisierung des Metadatenwerts überwachen](#watch-metadata-value-updated)


#### [!UICONTROL Benutzerdefinierten API-Aufruf durchführen]

Mit diesem Modul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://api.frame.io</code> ein. Beispiel: <code> /v4/me</code></p> <p>Hinweis: Eine Liste der verfügbaren Endpunkte finden Sie in der API-Referenz von [!DNL Frame.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Methode]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Header]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt automatisch Autorisierungs-Header hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge] </td> 
   <td> <p>Geben Sie die Abfragezeichenfolge der Anfrage ein. Klicken Sie für jeden Parameter, der in die Abfragezeichenfolge eingeschlossen werden soll, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie den Feldnamen sowie den gewünschten Wert ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p>Fügen Sie den Textinhalt für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrem JSON-Objekt verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Ereignisse ansehen

Dieses Instant Trigger-Modul startet ein Szenario, wenn das ausgewählte Ereignis in Frame.io auftritt.

Sie können einen vorhandenen Webhook verwenden oder einen neuen erstellen.

So erstellen Sie einen neuen Webhook:

1. Klicken Sie neben dem Feld „Webhook“ auf **Hinzufügen**.
1. Geben Sie die folgenden Informationen ein:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
     <td role="rowheader">Webhook-Name </td> 
      <td> <p>Geben Sie einen Namen für den neuen Webhook ein.</p> </td> 
     </tr> 
     <tr> 
       <td role="rowheader">[!UICONTROL Verbindung] </td> 
       <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
     </tr> 
     <tr> 
     <td role="rowheader">[!UICONTROL Konto-ID] </td> 
      <td> <p>Wählen Sie das Konto aus, das den Arbeitsbereich enthält, in dem Sie Ereignisse beobachten möchten, oder ordnen Sie es zu.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Arbeitsbereich-ID]</td> 
      <td> <p>Geben Sie die ID des Arbeitsbereichs ein, in dem Sie Ereignisse beobachten möchten.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL-Ereignisse]</td> 
      <td> <p>Wählen Sie die Ereignisse aus, für die Sie dieses Modul Trigger erstellen möchten</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **Speichern**, um den Webhook zu speichern und zum Modul zurückzukehren.
1. Klicken Sie **Modul Ereignisse** auf OK, um die Konfiguration zu speichern.


#### Aktualisierung des Metadatenwerts überwachen

Dieses Auslösermodul startet ein Szenario, wenn ein Kommentar aktualisiert wird.

Wählen Sie den Webhook aus, der für dieses Modul verwendet werden soll, oder klicken Sie neben dem Feld „Webhook“ auf „Hinzufügen“ und geben Sie die folgenden Informationen ein:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name] </td> 
   <td> <p>Geben Sie einen Namen für den neuen Webhook ein.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie in diesem Artikel unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das auf aktualisierte Metadatenwerte überwacht werden soll.</p> </td> 
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
