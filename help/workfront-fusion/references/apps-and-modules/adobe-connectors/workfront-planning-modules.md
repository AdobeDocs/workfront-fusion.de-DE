---
title: Adobe Workfront Planning-Module
description: Mit den  [!DNL Adobe Workfront Planning]  können Sie ein Adobe Workfront Fusion-Szenario auf der Grundlage von Ereignissen in Ihrem  [!DNL Adobe] Workfront Planning-Konto starten, Vereinbarungen und andere Datensätze erstellen, lesen oder aktualisieren, nach Datensätzen anhand von von Ihnen festgelegten Kriterien suchen und Dokumente hochladen.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
TQID: https://experienceleague.adobe.com/QHOFWDOT-18-c0b3wLXsRV5cjGVxlcyLhvZdkev3GFg
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: f0e185778e01b71a91837531a082e88485e97ca2
workflow-type: tm+mt
source-wordcount: 6075
ht-degree: 35%

---


# Adobe Workfront Planning-Module

Mit den [!DNL Adobe Workfront Planning]-Modulen können Sie einen Trigger erstellen, wenn in Workfront Planning Ereignisse eintreten. Sie können auch Datensätze erstellen, lesen, aktualisieren und löschen oder einen benutzerdefinierten API-Aufruf an Ihr [!DNL Adobe Workfront Planning]-Konto durchführen.

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
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td>
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Voraussetzungen

Für den Zugriff auf Workfront Planning sind folgende Voraussetzungen erforderlich:

* Ein neues Workfront-Paket und eine neue Lizenz. Workfront Planning ist nicht für ältere Workfront-Pakete oder -Lizenzen verfügbar.
* Ein Workfront-Planungspaket.
* Die Workfront-Instanz Ihres Unternehmens muss in das einheitliche Adobe-Erlebnis integriert werden.

## Informationen zur Adobe Workfront Planning-API

Der Adobe Workfront Planning-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td><pre><code>https://&#123;&#123;connection.host&#125;&#125;/maestro/api/&#123;&#123;common.maestroApiVersion&#125;&#125;/</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Planning mit Workfront Fusion verbinden

Der Workfront Planning-Connector verwendet OAuth 2.0, um eine Verbindung zu Workfront Planning herzustellen.

Sie können direkt aus einem Workfront Planning Fusion-Modul heraus eine Verbindung zu Ihrem Workfront Planning-Konto erstellen.

* [Verbindung mit Workfront Planning über Client-ID und Client-Geheimnis herstellen](#connect-to-workfront-planning-using-client-id-and-client-secret)
* [Herstellen einer Verbindung mit Workfront Planning über eine Server-zu-Server-Verbindung](#connect-to-workfront--planning-using-a-server-to-server-connection)

### Verbindung mit Workfront Planning über Client-ID und Client-Geheimnis herstellen

1. Klicken Sie in einem beliebigen Adobe Workfront **Planungsmodul neben dem Feld Verbindung** Hinzufügen“.
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
          <p><b>Adobe Workfront-Auth</b>-Verbindung auswählen.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für die neue Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre Workfront-Client-ID ein. Diese finden Sie im Workfront-Bereich „Setup“ unter „OAuth2-Programme“. Öffnen Sie die Anwendung, zu der eine Verbindung hergestellt werden soll, um die Client-ID anzuzeigen.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr Workfront-Client-Geheimnis ein. Diese finden Sie im Workfront-Bereich „Setup“ unter „OAuth2-Programme“. Wenn Sie in Workfront kein Client-Geheimnis für Ihre OAuth2-Anwendung besitzen, können Sie ein anderes generieren. Anweisungen hierzu finden Sie in der Workfront-Dokumentation.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentifizierungs-URL]</td>
        <td>Hier kann der Standardwert bleiben. Sie können aber auch die URL Ihrer Workfront-Instanz gefolgt von <code>/integrations/oauth2</code> eingeben. <p>Beispiel: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host-Präfix]</td>
        <td>In den meisten Fällen sollte dieser Wert auf <code>origin</code> gesetzt werden.
      </tr>
    </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

   Wenn Sie nicht bei Workfront Planning angemeldet sind, werden Sie zu einem Anmeldebildschirm weitergeleitet. Nach der Anmeldung können Sie die Verbindung zulassen.

>[!NOTE]
>
>* OAuth 2.0-Verbindungen zur Workfront-API sind nicht mehr auf API-Schlüssel angewiesen.
>* Um eine Verbindung zu einer Workfront-Sandbox-Umgebung herzustellen, müssen Sie in dieser Umgebung eine OAuth2-Anwendung erstellen und dann die Client-ID und das Client-Geheimnis, die von dieser Anwendung generiert wurden, in Ihrer Verbindung verwenden.

### Herstellen einer Verbindung mit Workfront Planning über eine Server-zu-Server-Verbindung

1. Klicken Sie in einem beliebigen Adobe Workfront **Planungsmodul neben dem Feld Verbindung** Hinzufügen“.
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
          <p>Wählen Sie <b>Adobe Workfront-Server-zu-Server-Verbindung</b> aus.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für die neue Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instanzname]</td>
        <td>
          <p>Geben Sie den Namen Ihrer Instanz ein (auch als Domain bezeichnet).</p><p>Wenn Ihre URL z. B. <code>https://example.my.workfront.com</code> lautet, geben Sie <code>example</code> ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instanzen-Lane]</td>
        <td>
          <p>Geben Sie den Umgebungstyp für die Verbindung ein.</p><p>Wenn Ihre URL z. B. <code>https://example.my.workfront.com</code> lautet, geben Sie <code>my</code> ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre Workfront-Client-ID ein. Diese finden Sie im Workfront-Bereich „Setup“ unter „OAuth2-Programme“. Öffnen Sie die Anwendung, zu der eine Verbindung hergestellt werden soll, um die Client-ID anzuzeigen.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr Workfront-Client-Geheimnis ein. Diese finden Sie im Workfront-Bereich „Setup“ unter „OAuth2-Programme“. Wenn Sie in Workfront kein Client-Geheimnis für Ihre OAuth2-Anwendung besitzen, können Sie ein anderes generieren. Anweisungen hierzu finden Sie in der Workfront-Dokumentation.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Bereiche]</td>
        <td>Geben Sie alle zutreffenden Bereiche für diese Verbindung ein.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host-Präfix]</td>
        <td>In den meisten Fällen sollte dieser Wert auf <code>origin</code> gesetzt werden.
      </tr>
    </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

   Wenn Sie nicht bei Workfront Planning angemeldet sind, werden Sie zu einem Anmeldebildschirm weitergeleitet. Nach der Anmeldung können Sie die Verbindung zulassen.

>[!NOTE]
>
>* OAuth 2.0-Verbindungen zur Workfront-API sind nicht mehr auf API-Schlüssel angewiesen.
>* Um eine Verbindung zu einer Workfront-Sandbox-Umgebung herzustellen, müssen Sie in dieser Umgebung eine OAuth2-Anwendung erstellen und dann die Client-ID und das Client-Geheimnis, die von dieser Anwendung generiert wurden, in Ihrer Verbindung verwenden.

## [!DNL Adobe Workfront Planning] Version 2-Module und ihre Felder

>[!IMPORTANT]
>
>Die Module in diesem Abschnitt gehören zum Workfront Planning V2-Connector.Module im Workfront Planning V1-Connector finden Sie unter [[!DNL Adobe Workfront Planning] Module der Version 1 und deren Felder](#adobe-workfront-planning-version-1-modules-and-their-fields).

Beim Konfigurieren von Workfront-Planungsmodulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere Workfront-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

* [Arbeitsbereiche](#workspaces-v2)
* [Eintragstypen](#record-types-v2)
* [Einträge](#records-v2)
* [Felder](#fields-v2)
* [Ansichten](#views-v2)
* [Berechtigungen](#permissions-v2)
* [Sonstiges](#other-v2)

### Arbeitsbereiche (v2)

* [Arbeitsbereich erstellen](#create-a-workspace-v2)
* [Löschen eines Arbeitsbereichs](#delete-a-workspace-v2)
* [Alle Arbeitsbereiche abrufen](#get-all-workspaces-v2)
* [Abrufen eines Arbeitsbereichs](#get-a-workspace-v2)
* [Aktualisieren eines Arbeitsbereichs](#update-a-workspace-v2)

#### Erstellen eines Arbeitsbereichs (v2)

Dieses Aktionsmodul erstellt einen neuen Arbeitsbereich in Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace-Name]</p>
      </td>
      <td>Geben Sie einen Namen für den neuen Arbeitsbereich ein oder ordnen Sie ihn zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Beschreibung</p>
      </td>
      <td>Beschreibung für den neuen Arbeitsbereich eingeben oder zuordnen&gt; 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Farbe</p>
      </td>
      <td>Wählen Sie die Farbe aus, die Sie für den neuen Datensatztyp verwenden möchten</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Symbol</p>
      </td>
      <td>Ordnen Sie das Symbol zu, das Sie für diesen Datensatztyp verwenden möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Besitzerin bzw. Besitzer</p>
      </td>
      <td>Geben Sie die Adobe IMS-Benutzer-ID des Benutzers ein, dem der Arbeitsbereich gehören soll, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Löschen eines Arbeitsbereichs (v2)

Dieses Aktionsmodul löscht einen einzelnen Arbeitsbereich, angegeben durch eine ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich-ID]</p>
      </td>
      <td>Geben Sie die ID des Arbeitsbereichs ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Alle Arbeitsbereiche abrufen (v2)

Dieses Modul ruft eine Liste aller Arbeitsbereiche ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Arbeitsbereiche]</p>
      </td>
      <td>Geben Sie die maximale Anzahl von Arbeitsbereichen ein, die das Modul während eines Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
  </tbody>
</table>

#### Abrufen eines Arbeitsbereichs (v2)

Dieses Modul ruft einen Arbeitsbereich anhand seiner ID ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich-ID]</p>
      </td>
      <td>Geben Sie die ID des Arbeitsbereichs ein, den Sie abrufen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Aktualisieren eines Arbeitsbereichs (v2)

Dieses Aktionsmodul aktualisiert einen neuen Arbeitsbereich in Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, den Sie aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace-Name]</p>
      </td>
      <td>Geben Sie einen Namen für den neuen Arbeitsbereich ein oder ordnen Sie ihn zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Beschreibung</p>
      </td>
      <td>Beschreibung für den neuen Arbeitsbereich eingeben oder zuordnen&gt; 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Farbe</p>
      </td>
      <td>Wählen Sie die Farbe aus, die Sie für den neuen Datensatztyp verwenden möchten</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Symbol</p>
      </td>
      <td>Ordnen Sie das Symbol zu, das Sie für diesen Datensatztyp verwenden möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Besitzerin bzw. Besitzer</p>
      </td>
      <td>Geben Sie die Adobe IMS-Benutzer-ID des Benutzers ein, dem der Arbeitsbereich gehören soll, oder ordnen Sie sie zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Abschnitte vom Typ „Datensatz“</p>
      </td>
      <td>Klicken Sie für jeden Datensatztypabschnitt, den Sie diesem Arbeitsbereich hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Namen des Abschnitts, die Datensatztyp-IDs und die Frage ein, ob Sie vorhandene Datensatztyp-IDs überschreiben möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Datensatztyp-Abschnitte &gt; Überschreiben</p>
      </td>
      <td>Wählen Sie aus, ob die vorhandenen Abschnitte durch die aus dem Modul ersetzt werden sollen. Wenn dies nicht der Fall ist, werden Abschnitte aus dem Modul zur vorhandenen Liste der Abschnitte hinzugefügt.</td> 
    </tr>
  </tbody>
</table>


### Datensatztypen (v2)

* [Datensatztyp erstellen](#create-a-record-type-v2)
* [Datensatztyp löschen](#delete-a-record-type-v2)
* [Abrufen globaler Datensatztypen](#get-global-record-types-v2)
* [Datensatztyp abrufen](#get-a-record-type-v2)
* [Datensatztypen abrufen](#get-record-types-v2)
* [Aktualisieren eines Datensatztyps](#update-a-record-type-v2)

#### Erstellen eines Datensatztyps (v2)

Dieses Aktionsmodul erstellt einen neuen Datensatztyp im ausgewählten Arbeitsbereich.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, in dem Sie einen Datensatztyp erstellen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Anzeigename</p>
      </td>
      <td>Geben Sie einen Namen für den neuen Datensatztyp ein oder ordnen Sie ihn zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Beschreibung</p>
      </td>
      <td>Geben Sie eine Beschreibung für den neuen Datensatztyp ein oder ordnen Sie sie zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Symbol</p>
      </td>
      <td>Ordnen Sie das Symbol zu, das Sie für diesen Datensatztyp verwenden möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Farbe</p>
      </td>
      <td>Wählen Sie die Farbe aus, die Sie für den neuen Datensatztyp verwenden möchten</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Source-Datensatztyp</p>
      </td>
      <td>Wenn Sie einen anderen Datensatztyp als Ausgangspunkt kopieren, wählen Sie diesen Datensatztyp aus.</td> 
    </tr>
  </tbody>
</table>

#### Löschen eines Datensatztyps (V2)

Dieses Aktionsmodul löscht einen einzelnen Datensatztyp, angegeben durch die ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatztyp-ID]</p>
      </td>
      <td>Geben Sie die ID des Datensatztyps ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Abrufen globaler Datensatztypen (v2)

Dieses Modul ruft eine Liste von Datensatztypen in einem Adobe Workfront Planning-Konto ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Einen Arbeitsbereich auswählen. Das Modul gibt globale Datensatztypen zurück, die diesem Arbeitsbereich hinzugefügt werden können.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Datensatztypen]</p>
      </td>
      <td>Geben Sie die maximale Anzahl von Datensatztypen ein, die das Modul während eines Ausführungszyklus zurückgibt, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Datensatztyp abrufen (V2)

Dieses Modul ruft einen Datensatztyp anhand seiner ID ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatztyp-ID]</p>
      </td>
      <td>Geben Sie die ID des Datensatztyps ein, den Sie abrufen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Datensatztypen abrufen (v2)

Dieses Modul ruft eine Liste der in einem bestimmten Arbeitsbereich verfügbaren Datensatztypen ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, für den Sie Datensatztypen abrufen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Datensatztypen]</p>
      </td>
      <td>Geben Sie die maximale Anzahl von Datensatztypen ein, die das Modul während eines Ausführungszyklus zurückgibt, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Aktualisieren eines Datensatztyps (V2)

Dieses Modul aktualisiert einen Datensatztyp.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, in dem Sie einen Datensatztyp aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, in dem Sie einen Datensatztyp aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Anzeigename</p>
      </td>
      <td>Geben Sie einen Namen für den Datensatztyp ein oder ordnen Sie ihn zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Beschreibung</p>
      </td>
      <td>Geben Sie eine Beschreibung für den Datensatztyp ein oder ordnen Sie sie zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Primäre Feld-ID</p>
      </td>
      <td>Geben Sie die ID des Felds ein, das als Titel des Datensatztyps verwendet wird, oder ordnen Sie sie zu.</td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>Symbol</p>
      </td>
      <td>Ordnen Sie das Symbol zu, das Sie für diesen Datensatztyp verwenden möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Farbe</p>
      </td>
      <td>Wählen Sie die Farbe aus, die Sie für den neuen Datensatztyp verwenden möchten</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Mit Workspace-IDs verknüpfbar</p>
      </td>
      <td>Klicken Sie für jeden Arbeitsbereich, mit dem dieser Datensatztyp verknüpft werden kann, auf <b>Element hinzufügen</b> und geben Sie die ID des Arbeitsbereichs ein.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Verknüpfbar mit Workspace IDs &gt; Überschreiben</p>
      </td>
      <td>Wählen Sie aus, ob vorhandene Arbeitsbereiche durch die aus dem Modul ersetzt werden sollen. Wenn dies nicht der Fall ist, werden Arbeitsbereiche aus dem Modul zur vorhandenen Liste der Arbeitsbereiche hinzugefügt.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Autorisiert zum Erstellen eines dynamischen Datensatztyps</p>
      </td>
      <td>Klicken Sie für jeden Betreff, der berechtigt ist, dynamische Datensatztypen aus diesem Datensatztyp zu erstellen, auf <b>Element hinzufügen</b> und geben Sie den Typ und die ID des Betreffs ein.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Autorisiert zum Erstellen eines dynamischen Datensatztyps &gt; Überschreiben</p>
      </td>
      <td>Wählen Sie aus, ob vorhandene Themen durch die aus dem Modul ersetzt werden sollen. Wenn nicht, werden die Themen aus dem Modul zur vorhandenen Liste der Themen hinzugefügt.</td> 
    </tr>
  </tbody>
</table>



### Datensätze (v2)

* [Eintrag erstellen](#create-a-record-v2)
* [Eintrag löschen](#delete-a-record-v2)
* [Datensatz abrufen](#get-a-record-v2)
* [Datensätze nach Datensatztyp abrufen](#get-records-by-record-type-v2)
* [Datensätze verschieben](#move-records-v2)
* [Datensätze suchen](#search-records-v2)
* [Eintrag aktualisieren](#update-a-record-v2)

#### Erstellen eines Datensatzes (v2)

Diese Aktion erstellt in Workfront Planning einen einzigen Datensatz.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, in dem Sie einen Datensatz erstellen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Typ des Eintrags aus, der erstellt werden soll.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Andere Felder</p>
      </td>
      <td>Geben Sie die Werte ein, die der neue Datensatz haben soll. Diese Felder basieren auf dem von Ihnen ausgewählten Datensatztyp und sind für Ihre Workfront Planning-Organisation eindeutig.</td> 
    </tr>
  </tbody>
</table>

#### Löschen eines Datensatzes (v2)

Dieses Aktionsmodul löscht einen einzelnen Datensatz, angegeben durch eine ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatz-ID]</p>
      </td>
      <td>Geben Sie die ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</td> 
    </tr>
  </tbody>
</table>

#### Datensatz abrufen (v2)

Dieses Aktionsmodul ruft einen Datensatz ab, der durch seine ID angegeben wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich-ID]</p>
      </td>
      <td>Geben Sie die ID des Datensatzes ein, den Sie abrufen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Datensätze nach Datensatztyp abrufen (V2)

Dieses Modul ruft eine Liste aller Datensätze des angegebenen Datensatztyps ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, der die Datensätze enthält, die Sie abrufen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Datensatztyp aus, den Sie zurückgeben möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Datensätze]</p>
      </td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während eines Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
  </tbody>
</table>

#### Datensätze verschieben (v2)

Dieses Modul ordnet einen oder mehrere Datensätze innerhalb eines Datensatztyps neu an, indem angegeben wird, wo sie platziert werden sollen.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, der die Datensätze enthält, die Sie verschieben möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Datensatztyp aus, den Sie verschieben möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, der die Datensätze enthält, die Sie verschieben möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, der die Datensätze enthält, die Sie verschieben möchten.</td> 
    </tr>
  </tbody>
</table>

#### Datensätze suchen (v2)

Gibt Datensätze anhand von angegebenen Kriterien zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, der die Datensätze enthält, die Sie abrufen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Datensatztyp aus, der die abzurufenden Datensätze enthält.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Andere Felder]</p>
      </td>
      <td>Geben Sie für jedes Feld, nach dem Sie filtern möchten, den Operator und den Wert für dieses Feld ein. Diese Felder basieren auf dem von Ihnen ausgewählten Datensatztyp und sind für Ihre Workfront Planning-Organisation eindeutig.</td> 
    </tr>
  </tbody>
</table>

#### Aktualisieren eines Datensatzes (v2)

Dieses Modul aktualisiert den angegebenen Datensatz.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, der den Datensatz enthält, den Sie aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatztyp-ID]</p>
      </td>
      <td>Wählen Sie den Typ des Datensatzes aus, den Sie aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatz-ID]</p>
      </td>
      <td>Geben Sie die ID des Datensatzes ein, den Sie aktualisieren möchten, oder mappen Sie sie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Andere Felder]</p>
      </td>
      <td>Werte für andere Felder eingeben. Die verfügbaren Felder hängen vom ausgewählten Datensatz ab.</td> 
    </tr>
  </tbody>
</table>


### Felder (v2)

* [Erstellen eines Felds](#create-a-field-v2)
* [Löschen eines Felds](#delete-a-field-v2)
* [Abrufen eines Felds](#get-a-field-v2)
* [Abrufen von Feldern nach Datensatztyp](#get-fields-by-record-type-v2)
* [Feld aktualisieren](#update-a-field-v2)

#### Erstellen eines Felds (v2)

Dieses Aktionsmodul erstellt ein neues Feld für den angegebenen Datensatztyp.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, in dem Sie ein Feld erstellen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Datensatztyp aus, für den Sie ein Feld erstellen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Anzeigename</p>
      </td>
      <td>Geben Sie einen Namen für das neue Feld ein oder ordnen Sie dem neuen Feld einen Namen zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Beschreibung</p>
      </td>
      <td>Geben Sie eine Beschreibung für das neue Feld ein oder mappen Sie sie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Feldtyp</p>
      </td>
      <td>Wählen Sie den Datentyp für das Feld aus.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Andere Felder</p>
      </td>
      <td>Es können weitere für den ausgewählten Feldtyp spezifische Felder verfügbar sein. Werte für diese Felder ausfüllen.</td> 
    </tr>
  </tbody>
</table>

#### Löschen eines Felds (v2)

Dieses Aktionsmodul löscht ein einzelnes Feld, angegeben durch eine ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Feld-ID]</p>
      </td>
      <td>Geben Sie die ID des Felds ein, das Sie löschen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Abrufen eines Felds (V2)

Dieses Modul ruft ein Feld anhand seiner ID ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Feld-ID]</p>
      </td>
      <td>Geben Sie die ID des Felds ein, das Sie abrufen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Abrufen von Feldern nach Datensatztyp (V2)

Dieses Modul ruft eine Liste von Feldern für einen bestimmten Datensatztyp ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, der die Felder enthält, die Sie zurückgeben möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Datensatztyp aus, für den Sie Felder zurückgeben möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Felder]</p>
      </td>
      <td>Geben Sie die maximale Anzahl von Feldern ein, die das Modul während eines Ausführungszyklus zurückgibt, oder mappen Sie sie.</td> 
    </tr>
  </tbody>
</table>

#### Aktualisieren eines Felds (V2)

Dieses Modul aktualisiert ein Feld teilweise anhand seiner ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcentyp]</p>
      </td>
      <td>Wählen Sie den Ressourcentyp aus, der das Feld enthält, das Sie aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Feld-ID]</p>
      </td>
      <td>Wählen Sie das Feld aus, das Sie aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Anzeigename]</p>
      </td>
      <td>Geben Sie einen Namen für das Feld ein oder ordnen Sie ihn zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Beschreibung]</p>
      </td>
      <td>Geben Sie eine Beschreibung für das Feld ein oder mappen Sie sie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Andere Parameter]</p>
      </td>
      <td>Geben Sie Werte für andere Feldparameter ein. Die verfügbaren Parameter hängen vom ausgewählten Feld ab.</td> 
    </tr>
  </tbody>
</table>


### Ansichten (v2)

* [Erstellen einer Ansicht](#create-a-view-v2)
* [Löschen einer Ansicht](#delete-a-view-v2)
* [Ansicht abrufen](#get-a-view-v2)
* [Ansichten nach Datensatztyp abrufen](#get-views-by-record-type-v2)
* [Aktualisieren einer Ansicht](#update-a-view-v2)

#### Erstellen einer Ansicht (v2)

Dieses Aktionsmodul erstellt eine neue Ansicht für den ausgewählten Datensatztyp.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, in dem Sie eine Ansicht erstellen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Datensatztyp aus, für den Sie eine Ansicht erstellen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Namen anzeigen</p>
      </td>
      <td>Geben Sie einen Namen für die neue Ansicht ein oder mappen Sie ihn.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ansichtstyp</p>
      </td>
      <td>Wählen Sie aus, ob die neue Ansicht eine Tabellen-, Timeline- oder Kalenderansicht ist.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Feld für Startdatum</p>
      </td>
      <td>Wenn es sich bei der Ansicht um eine Timeline- oder Kalenderansicht handelt, wählen Sie das Feld aus, das die Ansicht verwendet, um den Datensatz auf der Timeline zu platzieren.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Feld für Enddatum.</p>
      </td>
      <td>Wenn es sich bei der Ansicht um eine Timeline- oder Kalenderansicht handelt, wählen Sie das Feld aus, das die Ansicht zum Bestimmen des Enddatums auf der Timeline verwendet.</td> 
    </tr>
  </tbody>
</table>

#### Löschen einer Ansicht (v2)

Dieses Aktionsmodul löscht eine einzelne Ansicht, angegeben durch eine ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ansichts-ID]</p>
      </td>
      <td>Geben Sie die ID der Ansicht ein, die Sie löschen möchten, oder mappen Sie sie.</td> 
    </tr>
  </tbody>
</table>

#### Ansicht abrufen (v2)

Dieses Modul ruft anhand seiner ID eine Ansicht ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ansichts-ID]</p>
      </td>
      <td>Geben Sie die ID der Ansicht ein, die Sie abrufen möchten, oder mappen Sie sie.</td> 
    </tr>
  </tbody>
</table>

#### Ansichten nach Datensatztyp abrufen (V2)

Dieses Modul ruft eine Liste von Ansichten für den jeweiligen Datensatztyp ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, der die Ansichten enthält, die Sie abrufen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Datensatztyp aus, der die Ansichten enthält, die Sie abrufen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Ansichten]</p>
      </td>
      <td>Geben Sie die maximale Anzahl von Ansichten ein, die das Modul während eines Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
  </tbody>
</table>

#### Aktualisieren einer Ansicht (V2)

Dieses Aktionsmodul aktualisiert die angegebene Ansicht.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Wählen Sie den Arbeitsbereich aus, in dem Sie eine Ansicht aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Datensatztyp aus, für den Sie eine Ansicht aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ansichts-ID</p>
      </td>
      <td>Wählen Sie die Ansicht aus, die Sie aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Namen anzeigen</p>
      </td>
      <td>Geben Sie einen Namen für die neue Ansicht ein oder mappen Sie ihn.</td> 
    </tr>
  </tbody>
</table>

### Berechtigungen (v2)

* [Schließen von Zugriffsanfragen](#dismiss-access-requests-v2)
* [Abrufen aller Mitglieder und ihrer Rollen für eine Ressource](#get-all-members-and-their-roles-for-a-resource-v2)
* [Abrufen der effektiven Berechtigungen des aktuellen Benutzers für eine Ressource](#get-the-current-users-effective-permissions-on-a-resource-v2)
* [Auflisten ausstehender Zugriffsanfragen für eine Ressource](#list-pending-access-requests-for-a-resource-v2)
* [Anfordern des Zugriffs auf eine Ressource](#request-access-to-a-resource-v2)

#### Schließen von Zugriffsanfragen (v2)

Dieses Aktionsmodul schließt eine oder mehrere Zugriffsanfragen ab, angegeben durch eine ID.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcentyp]</p>
      </td>
      <td>Geben Sie die ID der Workspace ein, die Sie löschen möchten, oder mappen Sie sie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcen-ID]</p>
      </td>
      <td>Geben Sie die ID der Ressource ein, für die Sie Zugriffsanfragen verwerfen möchten, oder mappen Sie sie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Anfrage-IDs]</p>
      </td>
      <td>Klicken Sie für jede Zugriffsanfrage, die Sie verwerfen möchten, auf <b>Element hinzufügen</b> und geben Sie die Anforderungs-ID ein.</td> 
    </tr>
  </tbody>
</table>

#### Abrufen aller Mitglieder und ihrer Rollen für eine Ressource (V2)

Dieses Modul listet alle Benutzer, Gruppen und Teams auf, die eine explizite Freigabebeziehung zur Ressource haben. Die in der Verbindung für dieses Modul verwendeten Anmeldeinformationen müssen über Verwaltungsberechtigungen für die Ressource verfügen.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcentyp]</p>
      </td>
      <td>Wählen Sie den Ressourcentyp aus, für den Sie Informationen abrufen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcen-ID]</p>
      </td>
      <td>Geben Sie die ID der Ressource ein, für die Sie Informationen abrufen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Abrufen der effektiven Berechtigungen des aktuellen Benutzers für eine Ressource (V2)

Dieses Modul gibt die Anzeigen-, Bearbeitungs-, Lösch- und Hinzufügen-Berechtigungen der aktuellen Benutzerin bzw. des aktuellen Benutzers für eine bestimmte Ressource zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcentyp]</p>
      </td>
      <td>Wählen Sie den Ressourcentyp aus, für den Sie Berechtigungen abrufen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcen-ID]</p>
      </td>
      <td>Geben Sie die ID der Ressource ein, für die Sie Berechtigungen abrufen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Auflisten ausstehender Zugriffsanfragen für eine Ressource (V2)

Dieses Modul gibt alle ausstehenden Zugriffsanfragen für die angegebene Ressource zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcentyp]</p>
      </td>
      <td>Wählen Sie den Ressourcentyp aus, für den Sie Informationen abrufen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcen-ID]</p>
      </td>
      <td>Geben Sie die ID der Ressource ein, für die Sie Informationen abrufen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Anfordern des Zugriffs auf eine Ressource (V2)

Dieses Modul erstellt oder aktualisiert eine Zugriffsanfrage für den aktuellen Benutzer bzw. die aktuelle Benutzerin auf der angegebenen Ressource.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcentyp]</p>
      </td>
      <td>Wählen Sie den Ressourcentyp aus, für den Sie eine Zugriffsanfrage erstellen oder aktualisieren möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ressourcen-ID]</p>
      </td>
      <td>Geben Sie die ID der Ressource ein, für die Sie eine Zugriffsanfrage erstellen oder aktualisieren möchten, oder ordnen Sie sie zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nachricht]</p>
      </td>
      <td>Geben Sie den Text einer Nachricht ein, die Sie in die Zugriffsanfrage aufnehmen möchten, oder ordnen Sie ihn zu.</td> 
    </tr>
  </tbody>
</table>



### Sonstige (v2)

* [Authentifizierungs-ID von Workfront-ID abrufen](#get-auth-id-from-workfront-id-v2)
* [Benutzerdefinierten API-Aufruf erstellen](#make-a-custom-api-call-v2)
* [Ereignisse überwachen](#watch-events-v2)

#### Authentifizierungs-ID von Workfront ID abrufen (V2)

Dieses Modul verwendet eine Workfront-Benutzer-ID und gibt die entsprechende Autorisierungs-ID zurück, die von Planning verwendet wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workfront-Benutzer-ID]</p>
      </td>
      <td>Geben Sie die Workfront-ID des Benutzers ein, für den Sie eine Autorisierungs-ID abrufen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Erstellen eines benutzerdefinierten API-Aufrufs (V2)&lt;table

Dieses Modul führt einen benutzerdefinierten Aufruf an die Workfront Planning-API durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Geben Sie einen Pfad relativ zu<code> https://&lt;WORKFRONT_DOMAIN>/maestro/api/.</code> ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API-Version]</td> 
   <td>Wählen Sie die Version der Workfront-API aus, die vom Modul verwendet werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden in Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Header]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Dadurch wird der Content-Typ der Anfrage bestimmt.</p> <p>Beispiel:<code> {"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> <p>Tipp: Es wird empfohlen, Informationen mittels JSON-Text und nicht als Abfrageparameter zu senden.</p> </td> 
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

#### Ereignisse ansehen (v2)

Dieses Trigger-Modul startet ein Szenario, wenn ein Datensatz, ein Datensatztyp oder ein Arbeitsbereich in Workfront Planning erstellt, aktualisiert oder gelöscht wird.

>[!IMPORTANT]
>
>Sie können dieses Modul später bearbeiten, wodurch der Webhook bearbeitet wird.
>
>Beachten Sie beim Aktualisieren eines Webhooks Folgendes:
>
>* Der bearbeitete Webhook wird von Workfront-Ereignisabonnements als neues Abonnement behandelt. Der Verlauf der Ereignisabonnements wird für die vorherige Webhook-Konfiguration nicht beibehalten, da dies als separates Ereignisabonnement betrachtet wird.
>* Der Wechsel vom alten zum neuen Ereignisabonnement ist möglicherweise nicht perfekt synchronisiert. Es ist daher möglich, ein Ereignis zweimal zu erhalten (wenn das neue Abonnement vor dem alten abläuft) oder ein Ereignis zu verpassen (wenn das alte Abonnement vor dem Start des neuen abläuft).
>
>Weitere Informationen zum Bearbeiten von Webhooks finden Sie unter [Bearbeiten von Webhooks](/help/workfront-fusion/manage-scenarios/edit-webhooks.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Wählen Sie den Webhook aus, den Sie verwenden möchten, oder klicken Sie auf Hinzufügen , um einen neuen zu erstellen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objekttyp]</td>
      <td>Wählen Sie aus, ob Datensätze, Datensatztypen oder Arbeitsbereiche überwacht werden sollen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL zu überwachende Objekte]</td>
      <td>Wählen Sie aus, ob Sie neue, aktualisierte, neue und aktualisierte oder gelöschte Datensätze ansehen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Konfigurationstyp]</td>
      <td>Wählen Sie aus, ob Sie eine einfache oder eine erweiterte Konfiguration wünschen. <p>Weitere Informationen zur erweiterten Konfiguration finden Sie unter <a href="#example-of-advanced-logic-in-the-watch-events-module" class="MCXref xref" >Beispiel für eine erweiterte Logik im Modul Ereignisse </a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Status]</td>
      <td>Wählen Sie aus, ob der alte oder der neue Status überwacht werden soll.<ul><li><p><b>[!UICONTROL Neuer Status]</b></p><p>Lösen Sie ein Szenario aus, wenn sich der Eintrag <b>in</b> einen bestimmten Wert ändert.</p></li><li><p><b>[!UICONTROL Alter Status]</b></p><p>Lösen Sie ein Szenario aus, wenn sich der Eintrag <b>von</b> einem bestimmten Wert ändert.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Arbeitsbereich]</td>
      <td>Wenn Sie Datensätze beobachten, wählen Sie die Workspace aus, die Sie auf Datensätze überwachen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Eintragstyp]</td>
      <td>Wählen Sie beim Überwachen von Datensätzen den Typ des Datensatzes aus, auf den Sie achten möchten.</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Ereignisfilter]</p> </td> 
      <td> <p>Sie können Filter festlegen, um nur auf Einträge zu achten, die die von Ihnen ausgewählten Kriterien erfüllen.</p> <p>Geben Sie für jeden Filter Folgendes an: das Feld, das vom Filter ausgewertet werden soll, den Operator und den Wert, den der Filter zulassen soll. Sie können mehr als einen Filter verwenden, indem Sie UND-Regeln hinzufügen.</p> <p>Hinweis: Filter in vorhandenen Workfront-Webhooks können nicht bearbeitet werden. Um verschiedene Filter für Workfront-Ereignisabonnements einzurichten, entfernen Sie den aktuellen Webhook und erstellen Sie einen neuen.</p> <p>Weitere Informationen zu Ereignisfiltern finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Ereignisabonnementfilter in den Workfront- &gt; [!UICONTROL Ereignisse beobachten]-Modulen</a> im Artikel zu Workfront-Modulen.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL zu überwachende Objekte]</td>
      <td>Wählen Sie aus, ob Sie auf neue Nachrichten achten möchten. Aktualisierte, neue und aktualisierte oder gelöschte Datensätze.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Von dieser Verbindung vorgenommene Aktualisierungen ausschließen]</p>
      </td>
      <td>Aktivieren Sie diese Option, um zu verhindern, dass das Szenario ausgelöst wird, wenn eine Änderung durch die von diesem Modul verwendete Verbindung vorgenommen wird. Dadurch wird verhindert, dass eine weitere Instanz des Szenarios ausgelöst wird, wenn dieses Szenario eine auslösende Aktion ausführt.</td> 
    </tr>
  </tbody>
</table>

Ein Beispiel für die Verwendung der erweiterten Logik in diesem Modul finden Sie [Beispiel für die erweiterte Logik im Modul Ereignisse beobachten](#example-of-advanced-logic-in-the-watch-events-module).






## [!DNL Adobe Workfront Planning] Version 1-Module und ihre Felder

>[!IMPORTANT]
>
>Die Module in diesem Abschnitt gehören zum Workfront Planning V1-Connector.Module im Workfront Planning V2-Connector finden Sie unter [[!DNL Adobe Workfront Planning] Module der Version 2 und deren Felder](#adobe-workfront-planning-version-2-modules-and-their-fields).

Beim Konfigurieren von Workfront-Planungsmodulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere Workfront-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)
* [Nicht kategorisiert](#uncategorized)

### Auslöser

#### Ereignisse überwachen

Dieses Trigger-Modul startet ein Szenario, wenn ein Datensatz, ein Datensatztyp oder ein Arbeitsbereich in Workfront Planning erstellt, aktualisiert oder gelöscht wird.

>[!IMPORTANT]
>
>Sie können dieses Modul später bearbeiten, wodurch der Webhook bearbeitet wird.
>
>Beachten Sie beim Aktualisieren eines Webhooks Folgendes:
>
>* Der bearbeitete Webhook wird von Workfront-Ereignisabonnements als neues Abonnement behandelt. Der Verlauf der Ereignisabonnements wird für die vorherige Webhook-Konfiguration nicht beibehalten, da dies als separates Ereignisabonnement betrachtet wird.
>* Der Wechsel vom alten zum neuen Ereignisabonnement ist möglicherweise nicht perfekt synchronisiert. Es ist daher möglich, ein Ereignis zweimal zu erhalten (wenn das neue Abonnement vor dem alten abläuft) oder ein Ereignis zu verpassen (wenn das alte Abonnement vor dem Start des neuen abläuft).
>
>Weitere Informationen zum Bearbeiten von Webhooks finden Sie unter [Bearbeiten von Webhooks](/help/workfront-fusion/manage-scenarios/edit-webhooks.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Wählen Sie den Webhook aus, den Sie verwenden möchten, oder klicken Sie auf Hinzufügen , um einen neuen zu erstellen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objekttyp]</td>
      <td>Wählen Sie aus, ob Datensätze, Datensatztypen oder Arbeitsbereiche überwacht werden sollen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Status]</td>
      <td>Wählen Sie aus, ob der alte oder der neue Status überwacht werden soll.<ul><li><p><b>[!UICONTROL Neuer Status]</b></p><p>Lösen Sie ein Szenario aus, wenn sich der Eintrag <b>in</b> einen bestimmten Wert ändert.</p></li><li><p><b>[!UICONTROL Alter Status]</b></p><p>Lösen Sie ein Szenario aus, wenn sich der Eintrag <b>von</b> einem bestimmten Wert ändert.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Arbeitsbereich]</td>
      <td>Wenn Sie Datensätze beobachten, wählen Sie die Workspace aus, die Sie auf Datensätze überwachen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Eintragstyp]</td>
      <td>Wählen Sie beim Überwachen von Datensätzen den Typ des Datensatzes aus, auf den Sie achten möchten.</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Ereignisfilter]</p> </td> 
      <td> <p>Sie können Filter festlegen, um nur auf Einträge zu achten, die die von Ihnen ausgewählten Kriterien erfüllen.</p> <p>Geben Sie für jeden Filter Folgendes an: das Feld, das vom Filter ausgewertet werden soll, den Operator und den Wert, den der Filter zulassen soll. Sie können mehr als einen Filter verwenden, indem Sie UND-Regeln hinzufügen.</p> <p>Hinweis: Filter in vorhandenen Workfront-Webhooks können nicht bearbeitet werden. Um verschiedene Filter für Workfront-Ereignisabonnements einzurichten, entfernen Sie den aktuellen Webhook und erstellen Sie einen neuen.</p> <p>Weitere Informationen zu Ereignisfiltern finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Ereignisabonnementfilter in den Workfront- &gt; [!UICONTROL Ereignisse beobachten]-Modulen</a> im Artikel zu Workfront-Modulen.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL zu überwachende Objekte]</td>
      <td>Wählen Sie aus, ob Sie auf neue Nachrichten achten möchten. Aktualisierte, neue und aktualisierte oder gelöschte Datensätze.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Von dieser Verbindung vorgenommene Aktualisierungen ausschließen]</p>
      </td>
      <td>Aktivieren Sie diese Option, um zu verhindern, dass das Szenario ausgelöst wird, wenn eine Änderung durch die von diesem Modul verwendete Verbindung vorgenommen wird. Dadurch wird verhindert, dass eine weitere Instanz des Szenarios ausgelöst wird, wenn dieses Szenario eine auslösende Aktion ausführt.</td> 
    </tr>
  </tbody>
</table>

Ein Beispiel für die Verwendung der erweiterten Logik in diesem Modul finden Sie [Beispiel für die erweiterte Logik im Modul Ereignisse beobachten](#example-of-advanced-logic-in-the-watch-events-module).

### Aktionen

* [Datensatztyp löschen](#delete-a-record-type)
* [Erstellen eines benutzerdefinierten KI-Aufrufs](#make-a-custom-api-call)

#### Datensatztyp löschen

Dieses Aktionsmodul löscht einen einzelnen Datensatztyp in Workfront Planning anhand seiner ID.

>[!WARNING]
>
>Durch das Löschen eines Datensatztyps in Workfront Planning werden auch alle Datensätze in der Datensatztyptabelle gelöscht.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatztyp-ID]</p>
      </td>
      <td>Geben Sie die ID des Datensatztyps ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td> 
    </tr>
  </tbody>
</table>

#### Benutzerdefinierten API-Aufruf erstellen

Dieses Modul führt einen benutzerdefinierten API-Aufruf an die [!DNL Adobe Workfront Planning]-API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Pfad eingeben für <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Methode]</p>
      </td>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Header]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt automatisch Autorisierungs-Header hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Abfragezeichenfolge]  </td>
      <td>
        <p>Klicken Sie für jedes Schlüssel/Wert-Paar, das Sie der Abfragezeichenfolge hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Schlüssel und den Wert ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Text]</td>
   <td> <p>Fügen Sie den Textinhalt für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrem JSON-Objekt verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>


### Suchvorgänge

#### Datensätze suchen

Dieses Aktionsmodul ruft eine Liste von Datensätzen basierend auf von Ihnen angegebenen Kriterien ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Arbeitsbereich]</p>
      </td>
      <td>Geben Sie die Workspace ein, die die zu durchsuchenden Datensätze enthält, oder ordnen Sie sie zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eintragstyp]</p>
      </td>
      <td>Wählen Sie den Datensatztyp aus, den Sie suchen möchten.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatzfelder]</p>
      </td>
      <td>Suchen Sie für jedes Feld, das Sie bei der Suche verwenden möchten, dieses Feld, wählen Sie den Operator aus und geben Sie den Wert ein, nach dem Sie suchen möchten, oder mappen Sie ihn. Felder sind je nach ausgewähltem Datensatztyp verfügbar.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL-Bedingung für Filter]</p>
      </td>
      <td>Bedingung für die Filter auswählen:<ul><li><b>UND</b><p>Das Modul gibt Datensätze zurück, <b> (alle</b> der von Ihnen ausgewählten Feldwerte erfüllen.</p></li><li><b>ODER</b><p>Das Modul gibt Datensätze zurück, <b> (beliebige</b> der ausgewählten Feldwerte erfüllen.</p></li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Beschränkung]</p>
      </td>
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</p> </td> 
    </tr>
  </tbody>
</table>


### Nicht kategorisiert


#### Eintrag erstellen

Diese Aktion erstellt in Workfront Planning einen einzigen Datensatz.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatztyp-ID]</p>
      </td>
      <td>Geben Sie den Typ des Datensatzes ein, den Sie erstellen möchten, oder ordnen Sie ihn zu. Die verfügbaren Datensatztypen basieren auf Ihrem Workfront Planning-Konto.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Andere Felder</p>
      </td>
      <td>Geben Sie die Werte ein, die der neue Datensatz haben soll. Diese Felder basieren auf dem von Ihnen ausgewählten Datensatztyp.</td> 
    </tr>
    <tr>
  </tbody>
</table>

### Eintrag löschen

Dieses Aktionsmodul löscht den angegebenen Datensatz in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatz-ID]</p>
      </td>
      <td>Geben Sie die ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</td> 
    </tr>
  </tbody>
</table>

### Datensatz abrufen

Dieses Aktionsmodul ruft einen einzelnen Datensatz aus [!DNL Adobe Workfront Planning] ab, angegeben durch die Kennung.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datensatz-ID]</td>
      <td>Geben Sie die ID des Datensatzes ein, den Sie abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

### Datensätze nach Datensatztyp abrufen

Dieses Aktionsmodul ruft alle Datensätze des angegebenen Typs ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Arbeitsbereich]</td>
      <td>Wählen Sie den Arbeitsbereich aus, der die abzurufenden Datensätze enthält, oder ordnen Sie ihn zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Eintragstyp]</td>
      <td>Wählen Sie den Typ des Datensatzes aus, den Sie abrufen möchten.</td>
    </tr>
    <!--
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
    -->
  </tbody>
</table>

### Datensatztypen abrufen

Dieses Aktionsmodul ruft eine Liste von Datensatztypen in einem [!DNL Adobe Workfront Planning] ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Arbeitsbereich]</td>
      <td>Wählen Sie den Arbeitsbereich aus, der die Datensatztypen enthält, die Sie abrufen möchten, oder ordnen Sie ihn zu.</td>
    </tr>
  </tbody>
</table>

### Eintrag aktualisieren

Diese Aktion aktualisiert einen einzelnen Datensatz in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Workfront Planning]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatz-ID]</p>
      </td>
      <td>Geben Sie den Typ des Datensatzes ein, den Sie aktualisieren möchten, oder ordnen Sie ihn zu. Die verfügbaren Datensatztypen basieren auf Ihrem Workfront Planning-Konto.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Andere Felder</p>
      </td>
      <td>Geben Sie die neuen Werte ein, die der Datensatz haben soll. Diese Felder basieren auf dem von Ihnen ausgewählten Datensatztyp.</td> 
    </tr>
    <tr>
  </tbody>
</table>


## Verwenden von JSONata für eine lesbare Aufschlüsselung der `record-types`

Der folgende JSONata-Ausdruck erstellt eine für Menschen lesbare Ausgabe der Planning-Abfrage, die Ihnen die Aufschlüsselung der Datensatztypen liefert. Dadurch können der Name des Datensatztyps, die Feldnamen und gegebenenfalls die Feldoptionennamen anhand eines Namens für Menschen lesbar gemacht werden, während der Rest der Struktur intakt bleibt.

```
(
    $s0 := ({"data":$ ~> | fields | {"options":(options){name:$}} |});
    $s1 := ({"data":$s0.data ~> | **.fields | {"options_name":(options.*){displayName:$}} | });
    $s2 := $s1 ~> | data | {"fields":(fields){displayName:$}} |; 
    $s2.data{displayName:$}
)
```

Informationen zur Verwendung von JSONata-Modulen finden Sie unter [JSONata-Module](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/jsonata-module.md).

## Beispiel für die erweiterte Logik im Modul Ereignisse beobachten

Dies ist ein Beispiel für das Format, das die erweiterte Logik bei Verwendung des Moduls Workfront-Planung > Ereignisse beobachten annimmt.

```
[
  {
    "fieldName": "recordTypeId",
    "fieldValue": "Rt68c886502d4b5554ee80896b",
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "planning"
    },
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "active"
    },
    "comparison": "eq",
    "state": "newState"
  }
]
```

Beachten Sie Folgendes bei der Verwendung der erweiterten Logik im Modul Ereignisse beobachten:

* Der erste `"fieldvalue":` ist die Kennung des Planungs-Datensatztyps, die von der URL abgerufen wird. In diesem Beispiel ist die Kennung des Planungs-Datensatztyps `Rt68c886502d4b5554ee80896b`.
* Planungsdaten werden in einem Array namens `data ` zurückgegeben, das in diesem Beispiel als `"fieldName": "data"` angezeigt wird.
* Planning-Feldnamen werden als IDs zurückgegeben, die mit `F` beginnen.
* Da dieses Beispiel mit einem `OR` Filter-Connector ausgewertet wird, hat es zwei Einträge für dasselbe Feld (`F68c886502d4b5554eec808975`).  Die beiden Dropdown-Optionen, nach denen das Modul filtert, sind `"planning"` und `"active"`.

