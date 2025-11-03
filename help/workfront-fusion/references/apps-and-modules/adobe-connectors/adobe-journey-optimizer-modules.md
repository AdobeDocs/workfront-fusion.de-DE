---
title: Adobe Journey Optimizer-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die verwenden [!DNL Adobe Journey Optimizer] und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 1d0ccf4d-9f06-4210-86ec-7da7970f6a47
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '3709'
ht-degree: 0%

---

# [!DNL Adobe Journey Optimizer]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Adobe Journey Optimizer] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden. Mit [!DNL Adobe Journey Optimizer]-Modulen können Sie Datensätze erstellen, lesen, aktualisieren oder löschen oder einen benutzerdefinierten API-Aufruf an die [!DNL Adobe Journey Optimizer]-API durchführen.


Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

Bevor Sie den [!DNL Adobe Journey Optimizer]-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein aktives [!DNL Adobe Journey Optimizer] verfügen.

## Adobe Journey Optimizer-API-Informationen

Der Adobe Journey Optimizer-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>{connection.url}</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.7.11</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung mit Adobe Journey Optimizer

Sie können eine Verbindung in einem beliebigen Adobe Journey Optimizer-Modul erstellen.

1. Klicken Sie in einem beliebigen Modul **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre [!UICONTROL Adobe] [!UICONTROL Client-ID] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihren [!DNL Adobe] [!UICONTROL Client Secret] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Organisations-ID]</td>
        <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL Organisations-ID] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Sandbox-Name]</td>
        <td>Geben Sie den Namen der Sandbox ein, die diese Verbindung verwenden soll.</td>
        </tr>
      </tbody>
    </table>



   <!--Markdown 0032 placeholder-->


## [!DNL Adobe Journey Optimizer] Module und ihre Felder

Beim Konfigurieren von [!DNL Adobe Journey Optimizer] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Adobe Journey Optimizer] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Konfigurationsverwaltung](#configuration-management)
* [Package-Verwaltung](#package-management)
* [Datensatz-Management](#record-management)
* [Nachrichten-Management](#message-management)
* [Statusprüfungen](#status-checks)
* [Suchvorgänge](#searches)
* [Sonstiges](#other)




### Konfigurationsverwaltung

* [Erstellen einer Konfiguration](#create-a-configuration)
* [Bereitstellen einer Konfiguration](#deploy-a-configuration)
* [Aktualisieren einer Konfiguration](#update-a-configuration)
* [Bereitstellung einer Konfiguration aufheben](#undeploy-a-configuration)
* [Überprüfen, ob die Konfiguration bereitgestellt werden kann](#check-if-configuration-can-be-deployed)
* [Löschen einer Konfiguration](#delete-a-configuration)
* [Abrufen einer Konfiguration](#get-a-configuration)

#### Erstellen einer Konfiguration

Dieses Aktionsmodul erstellt einen Begrenzungs-Endpunkt oder eine Drosselungskonfiguration.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurationstyp auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Begrenzungs- oder eine Drosselungskonfiguration erstellen.<ul><li><p><b>Begrenzung</b></p>Fahren Sie mit <a href="#capping-fields" class="MCXref xref" >Begrenzungsfelder</a> fort.</li><li><p><b>Drosselung</b></p>Fahren Sie <a href="#throttling-fields" class="MCXref xref" >Felder drosseln</a>.</li></ul></td> 
  </tr> 
   </tbody> 
</table>

##### Begrenzungsfelder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie die URL des Endpunkts ein, den Sie konfigurieren möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IMS-Organisations-ID]</td> 
   <td>Geben Sie die Adobe IMS-ID der Organisation ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methoden]</td> 
   <td>Wählen Sie die in dieser Konfiguration zu verwendenden Methoden aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Service]</td> 
   <td>Wählen Sie aus, ob Sie eine Aktion oder eine Datenquelle für diese Konfiguration verwenden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale HTTP-Verbindungen]</td> 
   <td>Geben Sie die maximale Anzahl gleichzeitiger Verbindungen zu diesem Endpunkt ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Aufrufe]</td> 
   <td>Geben Sie die maximale Anzahl von Aufrufen ein, die in dem im Feld Zeitraum angegebenen Zeitraum ausgeführt werden sollen, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zeitraum (Millisekunden)]</td> 
   <td>Geben Sie die Anzahl der Millisekunden ein, die sich auf das Feld Maximale Anzahl an Aufrufen bezieht, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

##### Einschränkungsfelder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Geben Sie einen Namen für diese Konfiguration ein oder ordnen Sie ihn zu.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td>Geben Sie eine Beschreibung für diese Konfiguration ein oder ordnen Sie sie zu.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL URL-Muster]</td> 
   <td>Geben Sie die URL für den Endpunkt ein, den Sie einschränken möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methoden]</td> 
   <td>Wählen Sie die in dieser Konfiguration zu verwendenden Methoden aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximaler Durchsatz]</td> 
   <td>Wählen Sie aus, ob Sie eine Aktion oder eine Datenquelle für diese Konfiguration verwenden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale HTTP-Verbindungen]</td> 
   <td>Geben Sie die maximale Anzahl gleichzeitiger Verbindungen zu diesem Endpunkt ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Aufrufe]</td> 
   <td>Geben Sie den maximalen Durchsatz für diesen Endpunkt ein, oder ordnen Sie ihn zu. Dieser Wert muss zwischen 200 und 5000 liegen.</td> 
  </tr> 
 </tbody> 
</table>

#### Bereitstellen einer Konfiguration

Dieses Aktionsmodul stellt die angegebene Begrenzungs- oder Drosselungskonfiguration bereit.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurationstyp auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Begrenzungs- oder eine Drosselungskonfiguration bereitstellen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurations-ID]</td> 
   <td>Geben Sie die ID der Konfiguration ein, die Sie bereitstellen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren einer Konfiguration

Dieses Aktionsmodul aktualisiert die angegebene Begrenzungs- oder Drosselungskonfiguration.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurationstyp auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Begrenzungs- oder eine Drosselungskonfiguration aktualisieren möchten.<ul><li><p><b>Begrenzung</b></p>Informationen zu Feldern finden <a href="#capping-fields" class="MCXref xref" >Begrenzungsfelder</a> im Abschnitt Erstellen einer Konfiguration dieses Artikels.</li><li><p><b>Drosselung</b></p>Informationen zu Feldern finden <a href="#throttling-fields" class="MCXref xref" > unter </a> im Abschnitt Erstellen einer Konfiguration dieses Artikels.</li></ul></td> 
  </tr> 
  </tbody> 
</table>

#### Bereitstellung einer Konfiguration aufheben

Dieses Aktionsmodul hebt die Bereitstellung einer Begrenzungs- oder Drosselungskonfiguration auf. Der Konfigurationsstatus wird wieder in den Status vor der Bereitstellung geändert (`created` oder `updated`).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurationstyp auswählen]</td> 
   <td>Wählen Sie aus, ob Sie die Bereitstellung einer Begrenzungs- oder Drosselungskonfiguration aufheben möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurations-ID]</td> 
   <td>Geben Sie die ID der Konfiguration ein, deren Bereitstellung Sie aufheben möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Überprüfen, ob die Konfiguration bereitgestellt werden kann

Dieses Aktionsmodul überprüft, ob eine Begrenzungs- oder Drosselungskonfiguration bereitgestellt werden kann.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurationstyp auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Begrenzungs- oder eine Drosselungskonfiguration überprüfen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurations-ID]</td> 
   <td>Geben Sie die ID der Konfiguration ein, die Sie überprüfen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Löschen einer Konfiguration

Dieses Aktionsmodul löscht einen Begrenzungs-Endpunkt oder eine Drosselungskonfiguration.

Wenn die Konfiguration bereitgestellt wurde, muss die Bereitstellung aufgehoben werden, bevor sie gelöscht werden kann.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurationstyp auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Begrenzungs- oder Einschränkungskonfiguration löschen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurations-ID]</td> 
   <td>Geben Sie die ID der Konfiguration ein, die Sie löschen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen einer Konfiguration

Dieses Aktionsmodul gibt die Begrenzungs- oder Drosselungskonfiguration zurück, die durch die angegebene ID identifiziert wird. Die neueste Definition wird zurückgegeben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurationstyp auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Begrenzungs- oder eine Drosselungskonfiguration abrufen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurations-ID]</td> 
   <td>Geben Sie die ID der Konfiguration ein, die Sie abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>




### Package-Verwaltung

* [Erstellen eines Pakets](#create-a-package)
* [Aktualisieren eines Pakets](#update-a-package)
* [Löschen eines Pakets](#delete-a-package)
* [Suchen eines Pakets](#look-up-a-package)
* [Package importieren](#import-a-package)
* [Veröffentlichen eines Pakets](#publish-a-package)
* [Import übermitteln](#submit-an-import)



#### Erstellen eines Pakets

Dieses Aktionsmodul erstellt ein Multi-Artefakt-Paket.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Geben Sie einen Namen für das Paket ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td>Geben Sie eine Beschreibung des Pakets ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ablaufdatum]</td> 
   <td>Geben Sie den Zeitstempel ein, der das Ablaufdatum für das Paket definiert, oder ordnen Sie ihn zu. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package Type]</td> 
   <td>Wählen Sie den Pakettyp aus, den Sie erstellen möchten.<ul><li><p><b>Voll</b></p>Das Paket enthält alle Artefakte</p></li><li><p><b>Teilweise</b></p><p>Das Paket enthält nur Artefakte, die Sie hinzufügen. </p></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Artefakte]</td> 
   <td>Wenn Sie ein Teilpaket erstellen, klicken Sie für jedes Artefakt, das Sie hinzufügen möchten, auf <b>Artefakt hinzufügen</b> und geben Sie die ID, den Typ und den Titel des Artefakts an. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Sandbox]</td> 
   <td>Geben Sie den Namen und die IMS-Organisations-ID der Sandbox ein, die die Elemente enthält, die das Paket enthalten soll, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren eines Pakets

Dieses Aktionsmodul fügt Artefakte zu einem Paket hinzu oder löscht sie aus einem Paket oder aktualisiert die Paketmetadaten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aktion auswählen]</td> 
   <td>Wählen Sie die Aktion aus, die Sie durchführen möchten.<ul><li><p><b>Artefakt hinzufügen</b></p><p>Klicken Sie für jedes Artefakt, das Sie hinzufügen möchten<b> auf „Artefakt hinzufügen</b> und geben Sie die ID, den Typ und den Titel des Artefakts an. Geben Sie dann das Ablaufdatum für das Paket ein oder ordnen Sie es zu. </p></li><li><p><b>Artefakt löschen</b></p><p>Klicken Sie für jedes Artefakt, das Sie löschen möchten<b> auf „Artefakt hinzufügen</b> und geben Sie die ID, den Typ und den Titel des Artefakts an. </p></li><li><p><b>Aktualisieren von Metadaten</b></p><p>Geben Sie neue Werte für den Namen, die Beschreibung oder den Namen der Quell-Sandbox oder die IMS-Organisations-ID ein.</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

#### Löschen eines Pakets

Dieses Aktionsmodul löscht ein Multi-Artefakt-Paket.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package-ID]</td> 
   <td>Geben Sie die ID des Pakets ein, das Sie löschen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Suchen eines Pakets

Dieses Aktionsmodul ruft Details des angegebenen Pakets ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package-ID]</td> 
   <td>Geben Sie die ID des Pakets ein, für das Sie Details zurückgeben möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Package importieren

Dieses Aktionsmodul ruft die in Konflikt stehenden Objekte in der angegebenen Ziel-Sandbox ab. Widersprüchliche Objekte stellen ähnliche Objekte dar, die bereits in der Ziel-Sandbox vorhanden sind.

Sie müssen ein Paket veröffentlichen, bevor Sie es importieren können.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package-ID]</td> 
   <td>Geben Sie die ID des Pakets ein, das Sie importieren möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Ziel-Sandbox]</td> 
   <td>Geben Sie den Namen der Sandbox ein, in die Sie das Paket importieren möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Veröffentlichen eines Pakets

Sie müssen ein Paket veröffentlichen, bevor Sie es importieren können.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package-ID]</td> 
   <td>Geben Sie die ID des Pakets ein, das Sie veröffentlichen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Import übermitteln

Dieses Aktionsmodul sendet einen Import für ein Paket, nachdem Sie Konflikte überprüft und Ersetzungen bereitgestellt haben. Das Ergebnis wird als Payload bereitgestellt, die den Importvorgang für die Ziel-Sandbox startet, wie in der Payload angegeben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package-ID]</td> 
   <td>Geben Sie die ID des Pakets ein, das Sie veröffentlichen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Geben Sie einen Namen für den Importauftrag ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td>Beschreibung des Importvorgangs eingeben oder zuordnen</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Ziel-Sandbox-Name)]</td> 
   <td>Geben Sie den Namen der Sandbox ein, an die Sie den Import senden, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Ziel-Sandbox) IMS-Organisations-ID]</td> 
   <td>Geben Sie die Adobe IMS-Organisations-ID für die Sandbox ein, an die Sie den Import senden, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source Sandbox)-ID]</td> 
   <td>Geben Sie die ID der Sandbox ein, die das Paket enthält, das Sie veröffentlichen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source-Sandbox)-Typ]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source Sandbox)-Link]</td> 
   <td>Geben Sie den Link für das Paket ein, das Sie veröffentlichen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>


<!--

### Artifact management

* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)

#### Copy artifacts synchronously

This action module copies artifacts from a source sandbox into a destination sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination sandbox]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to copy, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

#### Export Artifacts asynchronously

This action module exports artifacts from the specified sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to export, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



#### Import Artifacts asynchronously

This action module imports a snapshot containing artifacts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Snapshot ID]</td> 
   <td>Enter or map the ID of the snapshot you want to import.</td> 
  </tr> 
 </tbody> 
</table>

-->

### Datensatz-Management

* [Erstellen eines Datensatzes](#create-a-record)
* [Aktualisieren eines Datensatzes](#update-a-record)
* [Löschen eines Datensatzes](#delete-a-record)
* [Patch eines Datensatzes](#patch-a-record)
* [Datensatz abrufen](#get-a-record)

#### Erstellen eines Datensatzes

Dieses Aktionsmodul erstellt eine neue Inhaltsvorlage oder ein neues Inhaltsfragment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content-Typ auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Inhaltsvorlage oder ein Inhaltsfragment erstellen.<ul><li><p><b>Inhaltsvorlage</b></p>Fahren Sie fort <a href="#template-fields" class="MCXref xref" >Vorlagenfelder</a>.</li><li><p><b>Inhaltsfragment</b></p>Fahren Sie mit <a href="#fragment-fields" class="MCXref xref" >Fragmentfelder</a> fort.</li></ul></td> 
  </tr> 
  </tbody> 
</table>

##### Vorlagenfelder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Geben Sie einen Namen für diese Inhaltsvorlage ein oder ordnen Sie ihn zu.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td>Beschreibung für diese Inhaltsvorlage eingeben oder zuordnen.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Typ]</td> 
   <td>Wählen Sie den Vorlagentyp aus, den Sie erstellen möchten.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanäle]</td> 
   <td>Die in dieser Vorlage enthaltenen Kanäle auswählen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inhaltsvorlagenherkunft]</td> 
   <td>Quelle für diese Vorlage auswählen.</td>  
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadaten]</td> 
   <td>Um benutzerdefinierte Eigenschaften in die neue Vorlage aufzunehmen, wählen Sie „Metadaten hinzufügen“ und geben Sie den Schlüssel und den Wert der Metadaten ein oder ordnen Sie ihn zu. Wiederholen Sie den Vorgang für jedes benutzerdefinierte Feld, das Sie einbeziehen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL E-Mail HTML]</td> 
   <td>Geben Sie die HTML der in dieser Vorlage enthaltenen E-Mail ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Editor-Kontext]</td> 
   <td>Um benutzerdefinierte Eigenschaften in die E-Mail aufzunehmen, wählen Sie „Editor-Kontext hinzufügen“ und geben Sie den Schlüssel und den Wert des Kontexts ein oder ordnen Sie ihn zu. Wiederholen Sie den Vorgang für jedes benutzerdefinierte Feld, das Sie einbeziehen möchten.</td> 
  </tr> 
 </tbody> 
</table>

##### Fragmentfelder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Geben Sie einen Namen für dieses Inhaltsfragment ein oder ordnen Sie ihn zu.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td>Geben Sie eine Beschreibung für dieses Inhaltsfragment ein oder ordnen Sie sie zu.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Typ]</td> 
   <td>Wählen Sie den Vorlagentyp aus, den Sie erstellen möchten.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanäle]</td> 
   <td>Die in dieser Vorlage enthaltenen Kanäle auswählen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inhaltsfragment-Herkunft]</td> 
   <td>Quelle für dieses Fragment auswählen</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadaten]</td> 
   <td>Um benutzerdefinierte Eigenschaften in die neue Vorlage aufzunehmen, wählen Sie „Metadaten hinzufügen“ und geben Sie den Schlüssel und den Wert der Metadaten ein oder ordnen Sie ihn zu. Wiederholen Sie den Vorgang für jedes benutzerdefinierte Feld, das Sie einbeziehen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Inhalt]</td> 
   <td>Geben Sie den Inhalt des Fragments ein oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Editor-Kontext]</td> 
   <td>Um benutzerdefinierte Eigenschaften in die E-Mail aufzunehmen, wählen Sie „Editor-Kontext hinzufügen“ und geben Sie den Schlüssel und den Wert des Kontexts ein oder ordnen Sie ihn zu. Wiederholen Sie den Vorgang für jedes benutzerdefinierte Feld, das Sie einbeziehen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren eines Datensatzes

Dieses Aktionsmodul aktualisiert eine Inhaltsvorlage oder ein Inhaltsfragment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content-Typ auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Begrenzungs- oder eine Drosselungskonfiguration aktualisieren möchten.<ul><li><p><b>Vorlage</b></p>Felder finden Sie <a href="#template-fields" class="MCXref xref" >Vorlagenfelder</a> im Abschnitt Erstellen eines Datensatzes in diesem Artikel.</li><li><p><b>Fragment</b></p>Felder finden Sie <a href="#fragment-fields" class="MCXref xref" >Fragmentfelder</a> im Abschnitt Erstellen eines Datensatzes in diesem Artikel.</li></ul></td> 
  </tr> 
  </tbody> 
  </table>

#### Löschen eines Datensatzes

Dieses Aktionsmodul löscht eine Inhaltsvorlage oder ein Inhaltsfragment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content-Typ auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Inhaltsvorlage oder ein Inhaltsfragment löschen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorlagen-/Fragment-ID]</td> 
   <td>Geben Sie die ID der Vorlage oder des Fragments ein, die bzw. das Sie löschen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### Patch eines Datensatzes

Dieses Aktionsmodul aktualisiert einen Datensatz mit PATCH im JSON Pointer-Format

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content-Typ auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Inhaltsvorlage oder ein Inhaltsfragment patchen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorlagen-/Fragment-ID]</td> 
   <td>Geben Sie die ID der Vorlage oder des Fragments ein, die bzw. das Sie patchen möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload-Daten]</td> 
   <td>So fügen Sie der Payload dieses Patches einen Datensatz hinzu: <ol><li>Klicken Sie <b>Datensatz hinzufügen</b>.</li><li>Wählen Sie den Vorgang aus: Hinzufügen, Entfernen oder Ersetzen.</li><li>Wählen Sie im Feld Pfad aus, ob Sie den Namen oder die Beschreibung patchen möchten.</li><li> Geben Sie im Feld Von eine Zeichenfolge ein, die einen JSON-Zeigerwert enthält, oder ordnen Sie sie zu.</li><li>Geben Sie im Feld Wert den Wert ein, der im Vorgang verwendet werden soll.</li></ol></td> 
  </tr> 
 </tbody> 
</table>

#### Datensatz abrufen

Dieses Aktionsmodul gibt die Inhaltsvorlage oder das Inhaltsfragment zurück, die bzw. das durch die angegebene ID identifiziert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content-Typ auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Inhaltsvorlage oder ein Inhaltsfragment abrufen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorlagen-/Fragment-ID]</td> 
   <td>Geben Sie die ID der Vorlage oder des Fragments ein, die bzw. das Sie abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>


### Nachrichten-Management

* [Trigger einer unitären Nachrichtenausführung](#trigger-a-unitary-message-execution)
* [Trigger einer zielgruppenbasierten Nachricht](#trigger-an-audience-based-message)
* [Überprüfen des Status einer zielgruppenbasierten Nachricht](#check-the-status-for-audience-based-message)



#### Trigger einer unitären Nachrichtenausführung

Trigger Dieses Aktionsmodul sendet eine einheitliche Nachricht an die von Ihnen angegebenen Empfänger.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anfrage-ID]</td> 
   <td>Geben Sie die ID der mit dieser Nachricht verknüpften Anfrage ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kampagnen-ID]</td> 
   <td>Geben Sie die ID der Kampagne ein, die mit dieser Nachricht verknüpft ist, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Empfänger]</td> 
   <td>Klicken Sie für jeden Empfänger, den Sie diese Nachricht erhalten möchten<b> auf „Empfänger hinzufügen</b> und geben Sie Folgendes ein:
   <ul>
   <li><p><b>Typ</b></p>Wählen Sie <code>aep</code> aus.</li>
   <li><p><b>Benutzer-ID</b></p>Geben Sie die Adobe Experience Platform-Profilkennung des Empfängers ein oder ordnen Sie sie zu.</li>
   <li><p><b>Namespace</b></p>Geben Sie den Namespace des Adobe Experience Platform-Profils des Empfängers ein oder ordnen Sie ihn zu.</li>
   <li><p><b>E-Mail-Adresse</b></p></li>
   <li><p><b>Mobiltelefonnummer</b></p></li>
   <li><p><b>Vorname</b></p></li>
   <li><p><b>Last name</b></p></li>
   <li><p><b>Produkt</b></p>Geben Sie das mit dieser Nachricht verknüpfte Produkt ein oder ordnen Sie es zu. Dies wird für die dynamische Variablenersetzung im Nachrichteninhalt verwendet.</li>
   </ul></td> 
  </tr> 
 </tbody> 
</table>

#### Trigger einer zielgruppenbasierten Nachricht

Dieses Aktionsmodul Trigger die Ausführung einer zielgruppenbasierten Nachricht basierend auf der von Ihnen angegebenen Anfrage und Kampagne.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anfrage-ID]</td> 
   <td>Geben Sie die ID der mit dieser Nachricht verknüpften Anfrage ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kampagnen-ID]</td> 
   <td>Geben Sie die ID der Kampagne ein, die mit dieser Nachricht verknüpft ist, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Product]</td> 
   <td>Geben Sie das mit dieser Nachricht verknüpfte Produkt ein oder ordnen Sie es zu. Dies wird für die dynamische Variablenersetzung im Nachrichteninhalt verwendet.</td> 
  </tr> 
 </tbody> 
</table>

#### Überprüfen des Status für zielgruppenbasierte Nachrichten

Dieses Aktionsmodul überprüft den Status einer zielgruppenbasierten Batch-Nachricht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichtenausführungs-ID]</td> 
   <td>Geben Sie die ID der Nachrichtenausführung ein, die Sie überprüfen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### Statusprüfungen

<!--* [Check service health](#check-service-health)-->
* [Überprüfen der Importabhängigkeiten](#check-the-import-dependencies)
* [Überprüfen des Status eines Importvorgangs](#check-the-status-of-an-import-job)

<!--

#### Check service health

This action module checks that the service represented by the connection is running.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
 </tbody> 
</table>

-->

#### Überprüfen der Importabhängigkeiten

Dieses Aktionsmodul prüft die Abhängigkeiten auf Paket-Artefakte. Auf diese Weise können Sie überprüfen, ob Sie über Berechtigungen zum Importieren von Paket-Artefakten verfügen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package-ID]</td> 
   <td>Geben Sie die ID des Pakets ein, für das Sie die Berechtigungen überprüfen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ziel-Sandbox]</td> 
   <td>Geben Sie den Namen der Sandbox ein, in die Sie das Paket importieren möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Überprüfen des Status eines Importvorgangs

Dieses Aktionsmodul prüft, ob ein Importvorgang erfolgreich oder fehlgeschlagen ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorgangs-ID]</td> 
   <td>Geben Sie die ID des Auftrags ein, für den Sie Daten abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [Auflisten aller abhängigen Objekte](#list-all-dependent-objects)
* [Auflisten der Konfigurationen](#list-configurations)
* [Export- und Importvorgänge auflisten](#list-export-and-import-jobs)
* [Auflisten von Paketen](#list-packages)
* [Einträge auflisten](#list-records)

#### Auflisten aller abhängigen Objekte

Dieses Suchmodul listet alle abhängigen Objekte für Objekte im angegebenen Paket auf

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package-Objekte]</td> 
   <td>Klicken Sie für jedes Objekt im Paket, für das Sie ein abhängiges Objekt zurückgeben möchten, auf <b>Objekt hinzufügen</b> und geben Sie den Namen und den Typ des Objekts ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package-ID]</td> 
   <td>Geben Sie die ID des Pakets ein, für das Sie abhängige Objekte auflisten möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Ziel-Sandbox]</td> 
   <td>Geben Sie den Namen der Sandbox ein, die das Paket enthält, für das Sie abhängige Objekte auflisten möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Auflisten der Konfigurationen

Dieses Aktionsmodul listet alle Begrenzungs- oder Drosselungskonfigurationen auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Konfigurationstyp auswählen]</td> 
   <td>Wählen Sie aus, ob Sie Begrenzungskonfigurationen oder Einschränkungskonfigurationen auflisten möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### Export- und Importvorgänge auflisten

Dieses Suchmodul listet den aktuellen Export- und Importvorgang auf. Sie können Abfrageparameter verwenden, um die Liste zu filtern.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</td> 
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortieren nach]</td> 
      <td>Auswählen, ob die Ergebnisse nach Erstellungsdatum oder Änderungsdatum sortiert werden sollen.</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Abfrageparameter]</td> 
   <td>Klicken Sie für jeden Abfrageparameter, nach dem Sie filtern möchten, auf <b>Abfrageparameter hinzufügen</b>, wählen Sie dann das Feld und den Operator aus und geben Sie den Feldwert für den Filter ein.</td> 
  </tr> 
 </tbody> 
</table>



#### Auflisten von Paketen

Dieses Suchmodul listet alle Pakete in Ihrer Organisation auf. Sie können Abfrageparameter verwenden, um die Liste zu filtern.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</td> 
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortieren nach]</td> 
      <td>Auswählen, ob die Ergebnisse nach Erstellungsdatum oder Änderungsdatum sortiert werden sollen.</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Abfrageparameter]</td> 
   <td>Klicken Sie für jeden Abfrageparameter, nach dem Sie filtern möchten, auf <b>Abfrageparameter hinzufügen</b>, wählen Sie dann das Feld und den Operator aus und geben Sie den Feldwert für den Filter ein.</td> 
  </tr> 
 </tbody> 
</table>

#### Einträge auflisten

Dieses Suchmodul listet alle Begrenzungs- oder Drosselungskonfigurationen auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content-Typ auswählen]</td> 
   <td>Wählen Sie aus, ob Sie eine Inhaltsvorlage oder ein Inhaltsfragment abrufen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortieren nach]</td> 
   <td>Geben Sie den Parameternamen ein, nach dem diese Liste sortiert werden soll, oder ordnen Sie ihn zu. <code>-</code> oder <code>+</code> hinzufügen, um auf- oder absteigend zu sortieren. Wenn kein Vorzeichen angegeben ist, wird die Liste absteigend sortiert.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td>Dieses Feld dient zur Paginierung. Geben Sie die Kriterien für die nächste Seite in Bezug auf die Eigenschaft ein, die im Feld Sortieren nach angegeben ist, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortieren nach]</td> 
   <td>Geben Sie den Parameternamen ein, nach dem diese Liste sortiert werden soll, oder ordnen Sie ihn zu. <code>-</code> oder <code>+</code> hinzufügen, um auf- oder absteigend zu sortieren. Wenn kein Vorzeichen angegeben ist, wird die Liste absteigend sortiert.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nach Eigenschaft filtern]</td> 
   <td>Klicken Sie für jeden Eigenschaftsfilter, den Sie hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie den Schlüssel und den Wert der Eigenschaft ein. Datensätze, die den für die Eigenschaft angegebenen Wert enthalten, werden in die Liste aufgenommen.</td> 
  </tr> 
 </tbody> 
</table>


### Sonstiges


#### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt einen benutzerdefinierten API-Aufruf an die Adobe Journey Optimizer-API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer] finden Sie unter <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Journey Optimizer]</a> in diesem Artikel.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Geben Sie einen Pfad relativ zur Basis-URL ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL-Methode]</p>
      </td>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL-Kopfzeilen]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt automatisch Autorisierungs-, <code>x-api-key</code>- und <code>x-gw-ims-org-id</code> hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Abfragezeichenfolge]  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL body]</td>
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>







<!--

* [Check if configuration can be deployed](#check-if-configuration-can-be-deployed)
* [Check service health](#check-service-health)
* [Check the import dependencies](#check-the-import-dependencies)
* [Check the status for audience-based message](#status-for-audience-based-message)
* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Create a configuration](#create-a-configuration)
* [Create a package](#create-a-package)
* [Create a record](#create-a-record)
* [Delete a configuration](#delete-a-configuration)
* [Delete a package](#delete-a-package)
* [Delete a record](#delete-a-record)
* [Deploy a configuration](#deploy-a-configuration)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Get a configuration](#get-a-configuration)
* [Get a record](#get-a-record)
* [Import a package](#import-a-package)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)
* [List all dependent objects](#list-all-dependent-objects)
* [List export and import jobs](#list-import-and-export-jobs)
* [Look up a package](#look-up-a-package)
* [Make a custom API call](#make-a-custom-api-call)
* [Patch a record](#patch-a-record)
* [Publish a package](#publish-a-package)
* [Submit an import](#submit-an-import)
* [Trigger a unitary message execution](#trigger-a-unitary-message-execution)
* [Trigger an audience-based message](#trigger-an-audience-based-message)
* [Undeploy a configuration](#undeploy-a-configuration)
* [Update a configuration](#update-a-configuration)
* [Update a package](#update-a-package)
* [Update a record](#update-a-record)
* [List configurations](#list-configurations)
* [List packages](#list-packages)
* [List records](#list-records)

-->
