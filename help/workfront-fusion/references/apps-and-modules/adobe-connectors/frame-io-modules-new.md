---
title: Frame.io-Module
description: Die [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] Konto.
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: 52dbf75ebb65a1de1a7a86619af4c7633e0cbe03
workflow-type: tm+mt
source-wordcount: '4399'
ht-degree: 87%

---

# [!DNL Frame.io] V4-Module

>[!IMPORTANT]
>
>In diesem Artikel wird die neue Version des Frame.io-Connectors beschrieben. Dieser Connector wird verwendet, um eine Verbindung zu Frame.io Version 4 herzustellen.
>
>Anweisungen zur älteren Version des Frame.io-Connectors finden Sie unter [Frame.io-Connector für ältere Versionen](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).

Mit den [!DNL Frame.io]-Modulen von Adobe Workfront Fusion können Sie Medienelemente und Kommentare in Ihrem [!DNL Frame.io]-Konto überwachen, erstellen, aktualisieren, abrufen oder löschen.

Workfront bietet zwei Frame.io-Connectoren an, abhängig von der Version von Frame.io, zu der Sie eine Verbindung herstellen.

| Connector | Frame.io-Version |
|---|---|
| Frame.io | V4 |
| Frame.io (alt) | V3 |

Anweisungen zur älteren Version des Frame.io-Connectors finden Sie unter [Frame.io-Connector für ältere Versionen](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


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
   <td> <p>Jedes Paket für Adobe Workfront Workflow und Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: keine Workfront Fusion-Lizenz erforderlich</p>
   <p>Connector-basiert (alt): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Adobe Workfront Fusion erworben werden.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Angaben in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um [!DNL Frame.io]-Module verwenden zu können, müssen Sie über ein [!DNL Frame.io]-Konto verfügen

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
   <td> V2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>V1.0.76</td> 
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
1. Klicken Sie auf **Continue**.
1. Wenn Sie zur Anmeldung bei Ihrem Frame.io-Konto aufgefordert werden, führen Sie diese durch.
1. Wenn Sie Mitglied mehrerer Frame.io-Organisationen sind, wählen Sie die Organisation aus, die Sie für diese Verbindung verwenden möchten.

Die Verbindung wird hergestellt.

### Manuelles Erstellen einer Verbindung mit Benutzeranmeldeinformationen

Sie können eine Verbindung mit Benutzeranmeldeinformationen erstellen, indem Sie sich bei Frame.io anmelden oder eine Client-ID oder einen geheimen Client-Schlüssel angeben.

Um eine Server-zu-Server-Verbindung zu erstellen, müssen Sie zunächst eine Anwendung in der Adobe Developer Console konfigurieren.

* [Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console](#create-user-credentials-in-the-adobe-developer-console)
* [Konfigurieren einer Verbindung mit Benutzerauthentifizierung](#configure-a-user-authentication-connection)

#### Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console

Falls Sie noch keine Server-zu-Server-Anmeldeinformationen für ein Adobe Developer Console-Projekt haben, können Sie diese erstellen.

1. Öffnen Sie die [Adobe Developer Console](https://developer.adobe.com/).
1. Wählen Sie ein vorhandenes Projekt in der Adobe Developer Console aus, das für diese Verbindung verwendet werden soll

   Oder

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
1. Klicken Sie auf **Next**.
1. Klicken Sie auf **Save configured API**.
1. Klicken Sie auf der Produktseite auf die Karte für die soeben erstellten Anmeldeinformationen.

   Hier finden Sie Ihre Client-ID und Ihren geheimen Client-Schlüssel.

>[!NOTE]
>
> Es wird empfohlen, dieses Fenster geöffnet zu lassen, während Sie mit der Konfiguration Ihrer Verbindung in Adobe Workfront Fusion beginnen. Sie können die Client-ID kopieren und den geheimen Client-Schlüssel von dieser Seite abrufen und kopieren, um beide in die Verbindungsfelder einzufügen.


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
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>Wählen Sie die Option <b>IMS User authentication</b> aus.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Geben Sie einen Namen für diese Verbindung ein.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Geben Sie Ihre [!DNL Adobe]-[!UICONTROL Client-ID] ein. Diese finden Sie im Abschnitt für [!UICONTROL Credentials details] der [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie unter <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console</a> in diesem Artikel.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Geben Sie Ihren geheimen [!DNL Adobe]-[!UICONTROL Client-Schlüssel] ein. Diesen finden Sie im Abschnitt für [!UICONTROL Credentials details] der [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie unter <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Benutzeranmeldeinformationen in der Adobe Developer Console</a> in diesem Artikel.</p>
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
1. Wählen Sie ein vorhandenes Projekt in der Adobe Developer Console aus, das für diese Verbindung verwendet werden soll

   Oder

   Erstellen Sie ein neues Projekt in der Adobe Developer Console. Anweisungen finden Sie auf der Seite zum [Erstellen eines leeren Projekts](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Klicken Sie auf der Seite für den Projektüberblick oder der Seite für erste Schritte mit Ihrem neuen Projekt auf die Option **Add API**.
1. Suchen Sie auf der sich öffnenden Seite nach der Option **Frame.io API** und klicken Sie darauf.
1. Wählen Sie auf der Seite zum Auswählen des Authentifizierungstyps die Option **Server-to-Server-Authentication** aus und klicken Sie auf **Next**.
1. Geben Sie einen Namen für die Anmeldeinformationen ein. Auf diese Weise können Sie die Anmeldeinformationen später im Bereich für API-Anmeldeinformationen der Adobe Admin Console identifizieren.
1. Klicken Sie auf **Next**.
1. Wählen Sie auf der Seite zum Auswählen von Produktprofilen das Produktprofil aus, das das Frame.io-Konto enthält, mit dem Sie eine Verbindung herstellen möchten.
1. Klicken Sie auf die Option für **Save configured API**.
1. Klicken Sie auf der Produktseite auf die Karte für die soeben erstellten Anmeldeinformationen.

   Hier finden Sie Ihre Client-ID und Ihren geheimen Client-Schlüssel.

>[!NOTE]
>
> Es wird empfohlen, dieses Fenster geöffnet zu lassen, während Sie mit der Konfiguration Ihrer Verbindung in Adobe Workfront Fusion beginnen. Sie können die Client-ID kopieren und den geheimen Client-Schlüssel von dieser Seite abrufen und kopieren, um beide in die Verbindungsfelder einzufügen.


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
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>Wählen Sie die Option <b>IMS Server to Server</b> aus.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Geben Sie einen Namen für diese Verbindung ein.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Geben Sie Ihre [!DNL Adobe]-[!UICONTROL Client-ID] ein. Diese finden Sie im Abschnitt [!UICONTROL Credentials details] der [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie unter <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Server-zu-Server-Anmeldeinformationen in der Adobe Developer Console</a> in diesem Artikel.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Geben Sie Ihren geheimen [!DNL Adobe]-[!UICONTROL Client-Schlüssel] ein. Diese finden Sie im Abschnitt [!UICONTROL Credentials details] der [!DNL Adobe Developer Console].<p>Anweisungen zum Erstellen von Anmeldeinformationen finden Sie unter <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Erstellen von Server-zu-Server-Anmeldeinformationen in der Adobe Developer Console</a> in diesem Artikel.</p>
        </tr>
       </tbody>
    </table>
1. Klicken Sie auf **[!UICONTROL Continue]**, um die Verbindung zu speichern und zum Modul zurückzukehren.




## [!DNL Frame.io]-Module und ihre Felder

Beim Konfigurieren von [!DNL Frame.io]-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Dienst weitere [!DNL Frame.io]-Felder angezeigt werden. Eine fett formatierte Überschrift in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche für Zuordnung über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Medienelemente](#assets)
* [Kommentare](#comments)
* [Ordner](#folders)
* [Projekte](#projects)
* [Freigaben](#shares)
* [Arbeitsbereiche](#workspaces)
* [Metadaten](#metadata)
* [Sonstiges](#other)

### Medienelemente

* [[!UICONTROL Erstellen eines Medienelements]](#create-an-asset)
* [[!UICONTROL Löschen eines Medienelements]](#delete-an-asset)
* [[!UICONTROL Abrufen eines Medienelements]](#get-an-asset)
* [[!UICONTROL Auflisten von Medienelementen]](#list-assets)
* [Überwachen eines gelöschten Medienelements](#watch-asset-deleted)
* [Überwachen eines neuen Medienelements](#watch-new-asset)

#### [!UICONTROL Erstellen eines Medienelements] <!--different for v4-->

Dieses Aktionsmodul erstellt ein neues Asset. Sie können eine lokale Datei hochladen oder die URL für eine Remote-Datei angeben, aus der das Asset erstellt werden soll.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das Projekt enthält, für das Sie ein Medienelement erstellen möchten.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus oder ordnen Sie die ID des Arbeitsbereichs zu, der das Projekt enthält, für das Sie ein Medienelement erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das Sie ein Medienelement erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pfad] </td> 
   <td> <p>Wählen Sie den Pfad aus, in dem Sie ein Medienelement erstellen möchten.</p> </td> 
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
   <td>[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Quelldatei zu.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>Select the media type for this asset.</p> </td> 
  </tr> -->
  </tbody> 
</table>

#### [!UICONTROL Erstellen eines Assets (veraltet)] <!--different for v4-->

Dieses Aktionsmodul erstellt ein neues Medienelement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das Projekt enthält, für das Sie ein Medienelement erstellen möchten.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus oder ordnen Sie die ID des Arbeitsbereichs zu, der das Projekt enthält, für das Sie ein Medienelement erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das Sie ein Medienelement erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pfad] </td> 
   <td> <p>Wählen Sie den Pfad aus, in dem Sie ein Medienelement erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dateiname] </td> 
   <td> <p>Geben Sie den Namen der Datei ein, die Sie für dieses Medienelement verwenden möchten.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">Dateigröße </td> 
    <td> <p>Geben Sie die Dateigröße in Byte ein oder ordnen Sie sie zu.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Quell-URL] </td> 
   <td> <p>Wenn Sie eine Datei erstellen, geben Sie die URL der Datei ein, die Sie hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Medientyp] </td> 
   <td> <p>Wählen Sie den Medientyp für dieses Medienelement aus.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL Löschen eines Medienelements]

Dieses Aktionsmodul löscht ein angegebenes Medienelement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das Medienelement enthält, das Sie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Medienelement-ID] </td> 
   <td> <p>Wählen Sie das Medienelement aus, das Sie löschen möchten oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Abrufen eines Medienelements]

Dieses Aktionsmodul ruft Medienelement-Details ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das Medienelement enthält, das Sie abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Medienelement-ID] </td> 
   <td> <p>Wählen Sie das Medienelement aus, das Sie abrufen möchten oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Auflisten von Medienelementen]

Dieses Suchmodul ruft alle Medienelemente im Ordner des angegebenen Projekts ab.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das die Medienelemente enthält, die Sie auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Medienelemente] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Medienelementen ein, die das Modul während jedes Ausführungszyklus eines Szenarios zurückgeben soll, oder ordnen Sie eine Zahl zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Überwachen eines gelöschten Medienelements

Dieses Auslösermodul startet ein Szenario, wenn ein Medienelement gelöscht wird.

Wählen Sie den Webhook aus, den Sie für dieses Modul verwenden möchten, oder klicken Sie neben dem Feld „Webhook“ auf „Hinzufügen“ und geben Sie die folgenden Informationen ein:

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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das auf gelöschte Medienelemente überwacht werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Überwachen eines neuen Medienelements

Dieses Auslösermodul startet ein Szenario, wenn ein neues Medienelement erstellt wird.

Wählen Sie den Webhook aus, den Sie für dieses Modul verwenden möchten, oder klicken Sie neben dem Feld „Webhook“ auf „Hinzufügen“ und geben Sie die folgenden Informationen ein:

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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das auf neue Medienelemente überwacht werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Kommentare

* [[!UICONTROL Erstellen eines Kommentars]](#create-a-comment)
* [[!UICONTROL Löschen eines Kommentars]](#delete-a-comment)
* [[!UICONTROL Abrufen eines Kommentars]](#get-a-comment)
* [[!UICONTROL Auflisten von Kommentaren]](#list-comments)
* [[!UICONTROL Aktualisieren eines Kommentars]](#update-a-comment)
* [Überwachen von Kommentaraktualisierungen](#watch-comment-updated)
* [Überwachen eines neuen Kommentars](#watch-new-comment)

#### [!UICONTROL Erstellen eines Kommentars]

Dieses Aktionsmodul fügt dem Medienelement einen neuen Kommentar oder eine neue Antwort hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das das Medienelement enthält, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus oder ordnen Sie die ID des Arbeitsbereichs zu, der das Medienelement enthält, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, das das Medienelement enthält, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pfad] </td> 
   <td> <p>Wählen Sie den Pfad zu dem Medienelement aus, dem Sie einen Kommentar hinzufügen möchten.</p> </td> 
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
   <td> <p>Wenn es sich bei dem Medienelement um eine PDF-Datei handelt, geben Sie die Seite ein, an die der Kommentar angehängt werden soll, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Löschen eines Kommentars]

Dieses Aktionsmodul löscht einen vorhandenen Kommentar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das den Kommentar enthält, den Sie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentar-ID] </td> 
   <td> <p>Geben Sie die ID des Kommentars ein, den Sie löschen möchten, oder ordnen Sie die ID zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Abrufen eines Kommentars]

Dieses Aktionsmodul ruft Details des angegebenen Kommentars ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
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

#### [!UICONTROL Auflisten von Kommentaren]

Dieses Suchmodul ruft alle Kommentare des angegebenen Medienelements ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Medienelement enthält, von dem Sie Kommentare abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, der das Medienelement enthält, von dem Sie Kommentare abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, das das Medienelement enthält, von dem Sie Kommentare abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pfad] </td> 
   <td> <p>Wählen Sie den Pfad zu dem Medienelement aus, dessen Kommentare Sie auflisten möchten.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Kommentare] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Kommentaren ein, die das Modul während jedes Ausführungszyklus eines Szenarios zurückgeben soll, oder ordnen Sie eine Zahl zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren eines Kommentars]

Dieses Aktionsmodul bearbeitet einen vorhandenen Kommentar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Projekt mit dem Medienelement enthält, für das Sie einen Kommentar aktualisieren möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentar-ID] </td> 
   <td> <p>Wählen Sie den Kommentar aus, den Sie aktualisieren möchten.</p> </td> 
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
   <td> <p>Wenn es sich bei dem Medienelement um eine PDF-Datei handelt, geben Sie die Seite ein, an die der Kommentar angehängt ist, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Überwachen von Kommentaraktualisierungen

Dieses Auslösermodul startet ein Szenario, wenn ein Kommentar aktualisiert wird.

Wählen Sie den Webhook aus, den Sie für dieses Modul verwenden möchten, oder klicken Sie neben dem Feld „Webhook“ auf „Hinzufügen“ und geben Sie die folgenden Informationen ein:

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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das auf aktualisierte Kommentare überwacht werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Überwachen eines neuen Kommentars

Dieses Auslösermodul startet ein Szenario, wenn ein Kommentar erstellt wird.

Wählen Sie den Webhook aus, den Sie für dieses Modul verwenden möchten, oder klicken Sie neben dem Feld „Webhook“ auf „Hinzufügen“ und geben Sie die folgenden Informationen ein:

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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus oder ordnen Sie die ID des Kontos zu, das auf neue Kommentare überwacht werden soll.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem Sie einen Ordner erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, in dem Sie einen Ordner erstellen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus, in dem Sie einen Ordner erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pfad] </td> 
   <td> <p>Wählen Sie den Pfad aus, in dem Sie einen Ordner erstellen möchten.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie dem neuen Ordner einen Namen zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projekte

* [Erstellen eines Projekts](#create-a-project)
* [Einladen von Personen zu einem Frame.io-Projekt](#invite-users-to-frameio-project)
* [Auflisten von Projekten](#list-projects)

#### Erstellen eines Projekts

Dieses Aktionsmodul erstellt ein neues Projekt in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem Sie ein Projekt erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, in dem Sie ein Projekt erstellen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen Namen für das neue Projekt ein oder ordnen Sie dem neuen Projekt einen Namen zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Einladen von Personen zu einem Frame.io-Projekt

Dieses Aktionsmodul lädt Personen zum angegebenen Frame.io-Projekt ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Projekt enthält, zu dem Sie eine Person einladen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, der das Projekt enthält, zu dem Sie eine Person einladen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Projekt-ID </td> 
   <td> <p>Wählen Sie das Projekt aus, zu dem Sie eine Person einladen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Benutzer-ID </td> 
   <td> <p>Wählen Sie die Person aus, die Sie zum Projekt einladen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Auflisten von Projekten]

Dieses Suchmodul ruft alle Projekte für das angegebene Team ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Medienelement enthält, von dem Sie Projekte abrufen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus, der das Medienelement enthält, von dem Sie Projekte abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Projekte] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Projekten ein, die das Modul während jedes Ausführungszyklus eines Szenarios zurückgeben soll, oder ordnen Sie eine Zahl zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Freigaben

* [Hinzufügen eines Medienelements zu einem Freigabe-Link](#add-an-asset-to-a-share-link)
* [Erstellen eines Freigabe-Links](#create-a-share-link)

#### Hinzufügen eines Medienelements zu einem Freigabe-Link

Dieses Aktionsmodul fügt ein Medienelement zu einem Freigabe-Link in Frame.io hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das den Freigabe-Link enthält, zu dem Sie ein Medienelement hinzufügen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Freigabe-Link-ID] </td> 
   <td> <p>Wählen Sie den Freigabe-Link aus, zu dem Sie ein Medienelement hinzufügen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Medienelement-ID] </td> 
   <td> <p>Geben Sie die ID des Medienelements ein, das Sie zu dem Freigabe-Link hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem Sie einen Freigabe-Link erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
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
   <td role="rowheader">Medienelemente </td> 
   <td> <p>Klicken Sie für jedes Medienelement, das Sie zum Freigabe-Link hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Medienelement-ID ein.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Beschreibung </td> 
   <td> <p>Geben Sie eine Beschreibung für den Freigabe-Link ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie das Ablaufdatum für den Freigabe-Link ein oder ordnen Sie es zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Geben Sie einen Namen für den neuen Freigabe-Link ein oder ordnen Sie dem Freigabe-Link einen Namen zu.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, in dem Sie einen Arbeitsbereich erstellen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen neuen Namen für den Arbeitsbereich ein oder ordnen Sie dem Arbeitsbereich einen neuen Namen zu.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Medienelement enthält, von dem Sie Arbeitsbereiche abrufen möchten, oder ordnen Sie es zu.</p> </td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konto-ID] </td> 
   <td> <p>Wählen Sie das Konto aus, das die Dateien enthält, für die Sie Metadaten aktualisieren möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereich-ID] </td> 
   <td> <p>Wählen Sie den Arbeitsbereich aus oder ordnen Sie die ID des Arbeitsbereichs zu, der das Projekt enthält, für das Sie ein Medienelement erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt-ID] </td> 
   <td> <p>Wählen Sie das Projekt aus oder ordnen Sie die ID des Projekts zu, für das Sie ein Medienelement erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-IDs] </td> 
   <td> <p>Klicken Sie für jede Datei, für die Sie die Metadaten aktualisieren möchten, auf <b>Element hinzufügen</b> und geben Sie die ID der Datei ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Werte] </td> 
   <td> <p>Klicken Sie für jedes Feld, für das Sie die Metadaten aktualisieren möchten, auf <b>Element hinzufügen</b> und geben Sie die ID der Felddefinition und den Wert, den Sie in dieses Feld einfügen möchten, ein oder mappen Sie sie. Alle im Feld Datei-IDs angegebenen Dateien werden mit diesem Feldwert aktualisiert.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

* [Erstellen eines benutzerdefinierten API-Aufrufs](#make-a-custom-api-call)
* [Überwachen der Aktualisierung des Metadatenwerts](#watch-metadata-value-updated)


#### [!UICONTROL Durchführen eines benutzerdefinierten API-Aufrufs]

Mit diesem Modul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Verbindung] </td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
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
   <td> <p>Geben Sie die Abfragezeichenfolge der Anfrage ein. Klicken Sie für jeden Parameter, den Sie in die Abfragezeichenfolge aufnehmen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie den Feldnamen sowie den gewünschten Wert ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p>Fügen Sie den Textinhalt für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Überwachen der Aktualisierung des Metadatenwerts

Dieses Auslösermodul startet ein Szenario, wenn ein Kommentar aktualisiert wird.

Wählen Sie den Webhook aus, den Sie für dieses Modul verwenden möchten, oder klicken Sie neben dem Feld „Webhook“ auf „Hinzufügen“ und geben Sie die folgenden Informationen ein:

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
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Frame.io] finden Sie unter <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Frame.io] mit Adobe Workfront Fusion</a> in diesem Artikel.</td> 
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
