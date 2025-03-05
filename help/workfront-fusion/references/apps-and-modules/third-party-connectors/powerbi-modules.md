---
title: Power BI-Module
description: Adobe Workfront Fusion erfordert zusätzlich zu einer Adobe Workfront-Lizenz eine Adobe Workfront Fusion-Lizenz.
author: Becky
feature: Workfront Fusion
exl-id: 73eb70e1-3f3d-419d-9cde-3ec3cda224f8
source-git-commit: 85cd8dbf70dff220f593fa669b447bf5df2a21a2
workflow-type: tm+mt
source-wordcount: '2494'
ht-degree: 0%

---

# [!DNL Power BI] Module

[!DNL Power BI] ist ein Programm, mit dem Sie Daten visualisieren und für Ihre Stakeholder darstellen können. Es kann Daten aus einer Vielzahl von Quellen aufnehmen.

>[!NOTE]
>
>[!DNL Workfront Fusion] ist keine Datenquelle. [!DNL Workfront Fusion] können zwar Datenquellen erstellen und verwenden, aber Ihre Daten werden nicht gespeichert.


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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
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

## Microsoft Power BI API-Informationen

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

#### [!UICONTROL Erstellen eines Dashboards]

Dieses Aktionsmodul erstellt ein neues Dashboard.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Geben Sie einen Namen für das Dashboard ein oder ordnen Sie ihn zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der das neue Dashboard gehören soll, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Dashboard abrufen]

Dieses Aktionsmodul ruft Metadaten eines angegebenen Dashboards ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL - Dashboard-ID eingeben]</td>
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
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der die Dashboards gehören, für die Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Dashboard-Kachel abrufen]

Dieses Aktionsmodul ruft Metadaten einer angegebenen Dashboard-Kachel ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL - Dashboard-ID eingeben]</td>
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
      <td role="rowheader">[!UICONTROL Kachel-ID]</td>
      <td>Geben Sie die ID der [!DNL Power BI]-Kachel ein, für die Sie Details abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der die Kachel gehört, die Sie abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Dashboard-Kacheln auflisten]

Dieses Suchmodul ruft eine Liste von Dashboard-Kacheln ab.

<table>
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL - Dashboard-ID eingeben]</td>
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
    <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
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

#### [!UICONTROL Dashboards auflisten]

Dieses Suchmodul ruft eine Liste von Dashboards ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
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

#### [!UICONTROL Kopieren eines Berichts]

Dieses Aktionsmodul kopiert einen vorhandenen Bericht.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL - Berichts-ID eingeben]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des zu kopierenden Berichts aus oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Berichts-ID]</td>
      <td>
        <p>Geben Sie die ID des Berichts ein, den Sie kopieren möchten, oder mappen Sie sie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Bericht gehört, den Sie kopieren möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Neuer kopierter Berichtsname]</td>
      <td>Geben Sie einen Namen für den neuen Bericht ein oder mappen Sie ihn.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Löschen eines Berichts]

Dieses Aktionsmodul löscht einen Bericht.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL - Berichts-ID eingeben]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des zu löschenden Berichts aus oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Berichts-ID]</td>
      <td>
        <p>Geben Sie die ID des Berichts ein, den Sie löschen möchten, oder mappen Sie sie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Bericht gehört, den Sie löschen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Bericht abrufen]

Dieses Aktionsmodul ruft Metadaten eines angegebenen Berichts ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL - Berichts-ID eingeben]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des Berichts aus, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Berichts-ID]</td>
      <td>
        <p>Geben Sie die ID des Berichts ein, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Bericht gehört, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Berichte auflisten]

Dieses Suchmodul ruft eine Liste von Berichten ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
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

#### [!UICONTROL Hinzufügen oder Löschen von Zeilen in einer Datensatztabelle]

Dieses Aktionsmodul fügt Zeilen einer angegebenen Push-Datensatztabelle hinzu oder löscht sie.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tabelle eingeben]</td>
      <td>Wählen Sie die Option aus oder ordnen Sie sie zu, um den Datensatz auszuwählen, der die Tabelle enthält, die Sie anpassen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datensatz-ID]</td>
      <td>Geben Sie die ID des Datensatzes ein, der die Zeilen enthält, die Sie hinzufügen oder löschen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tabellenname]  </td>
      <td>
        <p>Geben Sie den Namen der Tabelle ein, die die Zeilen enthält, die Sie hinzufügen oder löschen möchten, oder ordnen Sie ihn zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Geben Sie die ID der Gruppe ein, der der Datensatz gehört, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Aktion auswählen]</td>
      <td>
        <p>Wählen Sie die Aktion aus, die Sie durchführen möchten, oder ordnen Sie sie zu.</p>
        <ul>
          <li>
            <p>[!UICONTROL Zeilen hinzufügen]</p>
          </li>
          <li>
            <p>[!UICONTROL Alle Zeilen löschen]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Zeilen]</td>
      <td>
        <p>Fügen Sie die Zeilenfelder hinzu.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL key]</b>
            </p>
            <p>Geben Sie den Schlüsselnamen ein oder ordnen Sie ihn zu.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Feldtyp]</b>
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
            <p>[!UICONTROL-Wert]</p>
            <p>Schlüsselwert eingeben oder zuordnen.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Erstellen eines Datensatzes]

Dieses Aktionsmodul erstellt einen neuen Datensatz.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Geben Sie einen Namen für den Datensatz ein oder mappen Sie ihn.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der neue Datensatz gehören soll, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Standardmodus]</td>
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
      <td role="rowheader">[!UICONTROL-Tabellen]</td>
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
            <p>[!UICONTROL none]</p>
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
      <td role="rowheader">[!UICONTROL Spalten]</td>
      <td>
        <p>Fügen Sie die Spalten hinzu:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL name]</b>
            </p>
            <p>Geben Sie einen Spaltennamen ein (zuordnen).</p>
          </li>
          <li>
            <p><b>[!UICONTROL Datentyp]</b>
            </p>
            <p>Auswählen oder Zuordnen des Datentyps:</p>
            <ul>
              <li>
                <p>[!UICONTROL String]</p>
              </li>
              <li>
                <p>[!UICONTROL Ganzzahl]</p>
              </li>
              <li>
                <p>[!UICONTROL Boolesch]</p>
              </li>
              <li>
                <p>[!UICONTROL Datum/Uhrzeit]</p>
              </li>
            </ul>
          </li>
          <li>
            <p><b>[!UICONTROL Format-String]</b>
            </p>
            <p>Geben Sie die Formatzeichenfolge ein (zuordnen).</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Zeilen]</td>
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
      <td role="rowheader">[!UICONTROL-Datenbank]  </td>
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
      <td role="rowheader">[!UICONTROL Datenquellen-ID]</td>
      <td>
        <p>  Geben Sie die ID der Datenquelle ein oder mappen Sie sie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datenquellentyp]  </td>
      <td>
        <p>Wählen Sie den Datenquellentyp aus oder ordnen Sie ihn zu. Beispiel: SQL.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gateway-ID]  </td>
      <td>Geben Sie die ID des Gateways ein, das Sie verwenden möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Löschen eines Datensatzes]

Dieses Aktionsmodul löscht einen Datensatz.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL - Berichts-ID eingeben]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des Datensatzes aus, den Sie löschen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Berichts-ID]</td>
      <td>
        <p>Geben Sie die ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Datensatz gehört, den Sie löschen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Datensatz abrufen]

Dieses Aktionsmodul ruft Metadaten eines angegebenen Datensatzes ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL - Berichts-ID eingeben]</td>
      <td>
        <p>Wählen Sie die Option zum Auswählen des Berichts aus, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Berichts-ID]</td>
      <td>
        <p>Geben Sie die ID des Datensatzes ein, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Datensatz gehört, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Datensätze auflisten]

Dieses Suchmodul ruft eine Liste von Datensätzen ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Wählen Sie die ID der Gruppe aus, der der Bericht gehört, für den Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>
        <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Aktualisieren eines Datensatzes]

Dieses Aktionsmodul aktualisiert einen angegebenen Datensatz.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datensatz eingeben]</td>
      <td>Wählen Sie die Option zum Auswählen des Datensatzes, den Sie aktualisieren möchten, aus oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datensatz-ID]</td>
      <td>Geben Sie die ID des Datensatzes ein, den Sie aktualisieren möchten, oder mappen Sie sie.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tabellenname]  </td>
      <td>
        <p>Geben Sie den Namen der Tabelle ein, die die Zeilen enthält, die Sie hinzufügen oder löschen möchten, oder ordnen Sie ihn zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gruppen-ID]  </td>
      <td>Geben Sie die ID der Gruppe ein, der der Datensatz gehört, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Option Benachrichtigen]  </td>
      <td>
        <p>Wählen oder mappen Sie die zu benachrichtigende Option:</p>
        <ul>
          <li>
            <p>[!UICONTROL E-Mail nach Abschluss]</p>
          </li>
          <li>
            <p>[!UICONTROL Mail bei Fehler]</p>
          </li>
          <li>
            <p>[!UICONTROL Keine Benachrichtigung]</p>
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

#### [!UICONTROL App abrufen]

Dieses Aktionsmodul ruft Metadaten einer angegebenen App ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App-ID]  </td>
      <td>
        <p>Wählen Sie die ID der App aus, die Sie abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Abrufen des Dashboards einer App]

Dieses Aktionsmodul ruft Metadaten des Dashboards einer angegebenen App ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App-ID]  </td>
      <td>
        <p>Wählen Sie die ID der App aus, die das abzurufende Dashboard enthält, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Berichts-ID]</td>
      <td>
        <p>  Wählen Sie die ID des Dashboards aus, das Sie abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Abrufen eines App-Berichts]

Dieses Aktionsmodul ruft Metadaten des Berichts einer bestimmten App ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App-ID]  </td>
      <td>
        <p>Wählen Sie die ID der App aus, die den abzurufenden Bericht enthält, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Berichts-ID]</td>
      <td>
        <p>  Wählen Sie die ID des Berichts aus, den Sie abrufen möchten, oder ordnen Sie sie zu.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Apps auflisten]

Dieses Suchmodul ruft eine Liste aller installierten Apps ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Dashboards der App auflisten]

Dieses Suchmodul ruft eine Liste von Dashboards aus einer angegebenen App ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App-ID]</td>
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

#### [!UICONTROL Berichte der App auflisten]

Dieses Suchmodul ruft eine Liste aller Berichte aus der angegebenen App ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App-ID]</td>
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

#### [!UICONTROL Apps ansehen]

Dieses Trigger-Modul startet ein Szenario, wenn eine App aktualisiert wird.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
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

#### [!UICONTROL Erstellen eines API-Aufrufs]

Dieses Aktionsmodul führt einen API-Aufruf an die [!DNL Power BI]-API aus.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Power BI]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL path]</p>
      </td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://api.powerbi.com</code> ein. Beispiel: <code>/v1.0/myorg/datasets</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL-Methode]</p>
      </td>
      <td>
        <p>Wählen Sie die [!UICONTROL HTTP]-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter [!UICONTROL HTTP]-Anfragemethoden.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL-Kopfzeilen]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungs- und X-API-Schlüssel-Header hinzu.</p>
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
