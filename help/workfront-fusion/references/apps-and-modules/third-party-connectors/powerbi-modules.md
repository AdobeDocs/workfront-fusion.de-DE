---
title: Power BI Module
description: Adobe Workfront Fusion erfordert zusätzlich zu einer Adobe Workfront-Lizenz eine Adobe Workfront Fusion-Lizenz.
author: Becky
feature: Workfront Fusion
exl-id: 73eb70e1-3f3d-419d-9cde-3ec3cda224f8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2082'
ht-degree: 0%

---

# [!DNL Power BI] Module

[!DNL Power BI] ist ein Programm, mit dem Sie Daten visualisieren und für Ihre Stakeholder darstellen können. Es kann Daten aus einer Vielzahl von Quellen aufnehmen.

>[!NOTE]
>
>[!DNL Workfront Fusion] ist keine Datenquelle. [!DNL Workfront Fusion] können zwar Datenquellen erstellen und verwenden, aber Ihre Daten werden nicht gespeichert.


## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Plan*</td> 
   <td> <p>[!DNL Pro] oder höher</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td> 
   <td> <p>[!DNL Plan], [!DNL Work]</p> </td> 
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

&#42;Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

&#42;&#42;Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Microsoft Power BI-API-Informationen

Der Microsoft Power BI-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.powerbi.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.0.2</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Power BI] Module und ihre Felder

Beim Konfigurieren von [!DNL Power BI] zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können je nach Faktoren wie Ihrer Zugriffsebene in der App oder im Service weitere Felder angezeigt werden. Ein fetter Titel in einem Modul kennzeichnet ein erforderliches Feld.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Dashboards](#dashboards)
* [Berichte](#reports)
* [Datensatz](#dataset)
* [Apps](#apps)
* [Sonstige](#other)

### Dashboards

* [Dashboard erstellen](#create-a-dashboard)
* [Dashboard abrufen](#get-a-dashboard)
* [Dashboard-Kachel abrufen](#get-a-dashboard-tile)
* [Dashboard-Kacheln auflisten](#list-dashboard-tiles)
* [Auflisten von Dashboards](#list-dashboards)

#### [!UICONTROL Create a Dashboard]

Dieses Aktionsmodul erstellt ein neues Dashboard.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Geben Sie einen Namen für das Dashboard ein oder ordnen Sie ihn zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der das neue Dashboard gehören soll, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dashboard]

Dieses Aktionsmodul ruft Metadaten eines angegebenen Dashboards ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des Dashboards, für das Sie Metadaten abrufen möchten, aus oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dashboard ID]</td>
      <td>
        <p>Geben Sie die ID des Dashboards ein, für das Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der die Dashboards gehören, für die Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dashboard Tile]

Dieses Aktionsmodul ruft Metadaten einer angegebenen Dashboard-Kachel ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen der abzurufenden Dashboard-Details aus oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dashboard ID]</td>
      <td>
        <p>Geben Sie die ID des Dashboards ein, für das Sie Details abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tile ID]</td>
      <td>Geben Sie die ID der [!DNL Power BI]-Kachel ein, für die Sie Details abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der die Kachel gehört, die Sie abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Dashboard Tiles]

Dieses Suchmodul ruft eine Liste von Dashboard-Kacheln ab.

<table>
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
    <td>
      <p>Wählen Sie die Option zum Auswählen des Dashboards aus, dessen Kacheln Sie auflisten möchten, oder ordnen Sie sie zu.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Dashboard ID]</td>
    <td>
      <p>Geben Sie die ID des Dashboards ein, das die Kacheln enthält, die Sie auflisten möchten, oder ordnen Sie sie zu.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Group ID]  </td>
    <td>Wählen Sie die ID der Gruppe aus oder ordnen Sie sie zu, der die Dashboards gehören, die die Kacheln enthalten, die Sie auflisten möchten.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limit]  </td>
    <td>
      <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p>
    </td>
  </tr>
</tbody>
</table>

#### [!UICONTROL List Dashboards]

Dieses Suchmodul ruft eine Liste von Dashboards ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>
        <p>Wählen Sie die ID der Gruppe aus, der die Dashboards gehören, die Sie auflisten möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p>
      </td>
    </tr>
  </tbody>
</table>

### Berichte

* [Kopieren eines Berichts](#copy-a-report)
* [Löschen eines Berichts](#delete-a-report)
* [Bericht abrufen](#get-a-report)
* [Berichte auflisten](#list-reports)

#### [!UICONTROL Copy a Report]

Dieses Aktionsmodul kopiert einen vorhandenen Bericht.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des zu kopierenden Berichts aus oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Geben Sie die ID des Berichts ein, den Sie kopieren möchten, oder mappen Sie sie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Bericht gehört, den Sie kopieren möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL New Copied Report Name]</td>
      <td>Geben Sie einen Namen für den neuen Bericht ein oder mappen Sie ihn.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Delete a Report]

Dieses Aktionsmodul löscht einen Bericht.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des zu löschenden Berichts aus oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Geben Sie die ID des Berichts ein, den Sie löschen möchten, oder mappen Sie sie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Bericht gehört, den Sie löschen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Report]

Dieses Aktionsmodul ruft Metadaten eines angegebenen Berichts ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des Berichts aus, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Geben Sie die ID des Berichts ein, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Bericht gehört, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Reports]

Dieses Suchmodul ruft eine Liste von Berichten ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>
        <p>Wählen Sie die ID der Gruppe aus, der die Berichte gehören, die Sie auflisten möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p>
      </td>
    </tr>
  </tbody>
</table>


### Datensatz

* [Hinzufügen/Löschen von Zeilen in einer Datensatztabelle](#add-or-delete-rows-in-a-dataset-table)
* [Erstellen eines Datensatzes](#create-a-dataset)
* [Löschen eines Datensatzes](#delete-a-dataset)
* [Datensatz abrufen](#get-a-dataset)
* [Auflisten von Datensätzen](#list-datasets)
* [Aktualisieren eines Datensatzes](#refresh-a-dataset)

#### [!UICONTROL Add or Delete Rows in a Dataset Table]

Dieses Aktionsmodul fügt Zeilen einer angegebenen Push-Datensatztabelle hinzu oder löscht sie.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a table]</td>
      <td>Wählen Sie die Option aus oder ordnen Sie sie zu, um den Datensatz auszuwählen, der die Tabelle enthält, die Sie anpassen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dataset ID]</td>
      <td>Geben Sie die ID des Datensatzes ein, der die Zeilen enthält, die Sie hinzufügen oder löschen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Table Name]  </td>
      <td>
        <p>Geben Sie den Namen der Tabelle ein, die die Zeilen enthält, die Sie hinzufügen oder löschen möchten, oder ordnen Sie ihn zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Geben Sie die ID der Gruppe ein, der der Datensatz gehört, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Select the Action]</td>
      <td>
        <p>Wählen Sie die Aktion aus, die Sie durchführen möchten, oder ordnen Sie sie zu.</p>
        <ul>
          <li>
            <p>[!UICONTROL Add rows]</p>
          </li>
          <li>
            <p>[!UICONTROL Delete All Rows]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rows]</td>
      <td>
        <p>Fügen Sie die Zeilenfelder hinzu.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Key]</b>
            </p>
            <p>Geben Sie den Schlüsselnamen ein oder ordnen Sie ihn zu.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Field Type]</b>
            </p>
            <p>Wählen Sie den Feldtyp aus oder ordnen Sie ihn zu:</p>
            <ul>
              <li>
                <p>Boolesch</p>
              </li>
              <li>
                <p>Datum</p>
              </li>
              <li>
                <p>Text</p>
              </li>
              <li>
                <p>Zahl</p>
              </li>
            </ul>
          </li>
          <li>
            <p>[!UICONTROL Value]</p>
            <p>Schlüsselwert eingeben oder zuordnen.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Create a Dataset]

Dieses Aktionsmodul erstellt einen neuen Datensatz.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Geben Sie einen Namen für den Datensatz ein oder mappen Sie ihn.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der neue Datensatz gehören soll, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default Mode]</td>
      <td>
        <p>Wählen Sie den Standardmodus für den Datensatz aus oder ordnen Sie ihn zu:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL As Azure]</b>: Ein Datensatz mit einer Live-Verbindung zu [!DNL Azure Analysis Service]</p>
          </li>
          <li>
            <p><b>[!UICONTROL As on Prem]</b>: Ein Datensatz mit einer Live-Verbindung zu [!DNL On-premise Analysis] Service</p>
          </li>
          <li>
            <p><b>[!DNL Push]</b>: Ein Datensatz, der den programmgesteuerten Zugriff für das Pushen von Daten in ermöglicht [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Push Streaming]</b>: Ein Datensatz, der Daten-Streaming unterstützt und programmgesteuerten Zugriff für das Pushen von Daten in ermöglicht [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Streaming]</b>: Ein Datensatz, der Daten-Streaming unterstützt</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tables]</td>
      <td>Fügen Sie dem Datensatz Tabellen hinzu. Felder finden Sie unter <a href="#Table" class="MCXref_0">Tabellenfelder</a></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Data sources]</td>
      <td>Hinzufügen der Datenquellen. Felder finden Sie unter <a href="#Data" class="MCXref_0">Datenquellenfelder</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Default Retention Policy]  </td>
      <td>
        <p>Wählen Sie die beabsichtigte Richtlinie für den Datensatz aus oder ordnen Sie sie zu:</p>
        <ul>
          <li>
            <p>[!UICONTROL None]</p>
          </li>
          <li>
            <p>[!UICONTROL Basic FIFO]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### Tabellenfelder

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>
        <p>  Geben Sie einen Namen für die Tabelle ein oder mappen Sie ihn.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Columns]</td>
      <td>
        <p>Fügen Sie die Spalten hinzu:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Geben Sie einen Spaltennamen ein (zuordnen).</p>
          </li>
          <li>
            <p><b>[!UICONTROL Data Type]</b>
            </p>
            <p>Auswählen oder Zuordnen des Datentyps:</p>
            <ul>
              <li>
                <p>[!UICONTROL String]</p>
              </li>
              <li>
                <p>[!UICONTROL Integer]</p>
              </li>
              <li>
                <p>[!UICONTROL Boolean]</p>
              </li>
              <li>
                <p>[!UICONTROL Date Time]</p>
              </li>
            </ul>
          </li>
          <li>
            <p><b>[!UICONTROL Format String]</b>
            </p>
            <p>Geben Sie die Formatzeichenfolge ein (zuordnen).</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rows]</td>
      <td>Zeilendetails eingeben oder zuordnen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Measures]</td>
      <td>Fügen Sie die Kennzahl für die Tabellen hinzu.</td>
    </tr>
  </tbody>
</table>

##### Datenquellenfelder

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Database]  </td>
      <td>
        <p>Geben Sie die Datenbank ein, die Sie verwenden möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Server]  </td>
      <td>
        <p>Geben Sie den Namen des Servers ein, den Sie verwenden möchten, oder ordnen Sie ihn zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]  </td>
      <td>
        <p>Geben Sie die URL ein, die Sie verwenden möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data source ID]</td>
      <td>
        <p>  Geben Sie die ID der Datenquelle ein oder mappen Sie sie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data source Type]  </td>
      <td>
        <p>Wählen Sie den Datenquellentyp aus oder ordnen Sie ihn zu. Beispiel: SQL.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gateway ID]  </td>
      <td>Geben Sie die ID des Gateways ein, das Sie verwenden möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Delete a Dataset]

Dieses Aktionsmodul löscht einen Datensatz.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des Datensatzes aus, den Sie löschen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Geben Sie die ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Datensatz gehört, den Sie löschen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dataset]

Dieses Aktionsmodul ruft Metadaten eines angegebenen Datensatzes ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des Berichts aus, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Geben Sie die ID des Datensatzes ein, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Datensatz gehört, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Datasets]

Dieses Suchmodul ruft eine Liste von Datensätzen ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Bericht gehört, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>
        <p>Geben Sie die maximale Anzahl von Datensätzen ein, denen das Modul während jedes Szenario-Ausführungszyklus [Aktion] zugeordnet werden soll.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Refresh a Dataset]

Dieses Aktionsmodul aktualisiert einen angegebenen Datensatz.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a dataset]</td>
      <td>Wählen Sie die Option zum Auswählen des Datensatzes, den Sie aktualisieren möchten, aus oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dataset ID]</td>
      <td>Geben Sie die ID des Datensatzes ein, den Sie aktualisieren möchten, oder mappen Sie sie.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Table Name]  </td>
      <td>
        <p>Geben Sie den Namen der Tabelle ein, die die Zeilen enthält, die Sie hinzufügen oder löschen möchten, oder ordnen Sie ihn zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Geben Sie die ID der Gruppe ein, der der Datensatz gehört, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Notify Option]  </td>
      <td>
        <p>Wählen oder mappen Sie die zu benachrichtigende Option:</p>
        <ul>
          <li>
            <p>[!UICONTROL Mail on Completion]</p>
          </li>
          <li>
            <p>[!UICONTROL Mail on Failure]</p>
          </li>
          <li>
            <p>[!UICONTROL No Notification]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Apps

* [Abrufen einer App](#get-an-app)
* [Abrufen des Dashboards einer App](#get-an-apps-dashboard)
* [Abrufen eines App-Berichts](#get-an-apps-report)
* [Auflisten der Dashboards der App](#list-apps-dashboards)
* [Auflisten der Berichte der App](#list-apps-reports)
* [Apps auflisten](#list-apps)
* [Apps ansehen](#watch-apps)

#### [!UICONTROL Get an App]

Dieses Aktionsmodul ruft Metadaten einer angegebenen App ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>Wählen Sie die ID der App aus, die Sie abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an App's Dashboard]

Dieses Aktionsmodul ruft Metadaten des Dashboards einer angegebenen App ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>Wählen Sie die ID der App aus, die das abzurufende Dashboard enthält, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>  Wählen Sie die ID des Dashboards aus, das Sie abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an App's Report]

Dieses Aktionsmodul ruft Metadaten des Berichts einer bestimmten App ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>Wählen Sie die ID der App aus, die den abzurufenden Bericht enthält, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>  Wählen Sie die ID des Berichts aus, den Sie abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Apps]

Dieses Suchmodul ruft eine Liste aller installierten Apps ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List App's Dashboards]

Dieses Suchmodul ruft eine Liste von Dashboards aus einer angegebenen App ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]</td>
      <td>Wählen Sie die ID der App aus, aus der Sie Dashboards auflisten möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List App's Reports]

Dieses Suchmodul ruft eine Liste aller Berichte aus der angegebenen App ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]</td>
      <td>Wählen Sie die ID der App aus oder ordnen Sie sie zu, aus der Sie Berichte auflisten möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Watch Apps]

Dieses Trigger-Modul startet ein Szenario, wenn eine App aktualisiert wird.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p>
      </td>
    </tr>
  </tbody>
</table>

### Sonstige

#### [!UICONTROL Make an API Call]

Dieses Aktionsmodul führt einen API-Aufruf an die [!DNL Power BI]-API aus.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundlegende Anweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://api.powerbi.com</code> ein. Beispiel: <code>/v1.0/myorg/datasets</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
      <td>
        <p>Wählen Sie die [!UICONTROL HTTP] Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter [!UICONTROL HTTP] von Anfragemethoden.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungs- und X-API-Schlüssel-Header hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
