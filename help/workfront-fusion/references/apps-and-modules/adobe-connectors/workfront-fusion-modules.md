---
title: Workfront Fusion-Module
description: Mit dem Workfront Fusion-Connector können Sie Ihre eigene Fusion-Organisation innerhalb eines Szenarios verwalten, einschließlich Datensätzen, Hooks, Szenarien und Verbindungen.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 557ec6de4ccf0753005fed3e4772d2eb9317537d
workflow-type: tm+mt
source-wordcount: 1374
ht-degree: 21%

---

# Workfront Fusion-Module

Mit dem Workfront Fusion-Connector können Sie Ihre eigene Fusion-Organisation innerhalb eines Szenarios verwalten. Im Gegensatz zu anderen Connectoren, die Fusion mit einer Anwendung oder einem Service eines Drittanbieters verbinden, ermöglicht dieser Connector es einem Szenario, die eigene API von Fusion aufzurufen, ähnlich wie der Adobe Workfront-Connector es einem Szenario ermöglicht, Workfront zu verwalten.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Erstellen von Szenarios: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Verbinden von Workfront Fusion mit Workfront Fusion

1. Klicken Sie in einem beliebigen Workfront Fusion **[!UICONTROL Modul]** dem Feld Verbindung auf „Hinzufügen“.
1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Verbindungstyp]</td> 
      <td>Wählen Sie den Verbindungstyp aus, den Sie erstellen möchten.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Verbindungsname]</td> 
      <td>Geben Sie einen Namen für die Verbindung ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client-ID]</td> 
      <td>Geben Sie Ihre [!DNL Adobe]-[!UICONTROL Client-ID] ein. Dies finden Sie im Abschnitt mit den [!UICONTROL -Anmeldeinformationen] im [!DNL Adobe Developer Console].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client-Geheimnis]</td> 
      <td>Geben Sie Ihr [!DNL Adobe]-[!UICONTROL Client-Geheimnis] ein. Dies finden Sie im Abschnitt mit den [!UICONTROL -Anmeldeinformationen] im [!DNL Adobe Developer Console].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Organisations-ID]</td> 
      <td>Geben Sie Ihre [!DNL Adobe] IMS-Organisations-ID ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Region]</td> 
      <td>Wählen Sie den Fusion-Bereich für diese Verbindung.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie auf **[!UICONTROL Continue]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## Workfront Fusion-Module und ihre Felder

Beim Konfigurieren von Workfront Fusion-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktionen](#actions)
* [Exportieren](#export)
* [Sonstiges](#misc)

### Aktionen

* [Klonen eines Datensatzes](#clone-a-record)
* [Eintrag erstellen](#create-a-record)
* [Eintrag löschen](#delete-a-record)
* [Einträge auflisten](#list-records)
* [Eintrag lesen](#read-a-record)
* [Eintrag aktualisieren](#update-a-record)

#### Klonen eines Datensatzes

Dieses Modul erstellt eine Kopie des angegebenen Datensatzes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> Wählen Sie den Typ des Datensatzes aus, den Sie klonen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Szenario-ID</td> 
   <td> Geben Sie die ID des Szenarios ein, das Sie klonen möchten, oder mappen Sie sie. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name</td> 
   <td> Geben Sie einen Namen für das neue Szenario ein oder mappen Sie ihn.</td> 
  </tr> 
 </tbody> 
</table>

#### Eintrag erstellen

Dieses Modul erstellt einen Datensatz mit den angegebenen Daten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> Wählen Sie den Typ des Eintrags aus, der erstellt werden soll. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-Kennung</td> 
   <td> Geben Sie die ID des Teams ein, dem dieser Datensatz gehören soll, oder mappen Sie sie. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name</td> 
   <td> Geben Sie einen Namen für den neuen Datensatz ein oder mappen Sie ihn.</td> 
  </tr> 
 </tbody> 
</table>

#### Eintrag löschen

Dieses Modul löscht einen angegebenen Datensatz.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> Wählen Sie den Typ des Datensatzes aus, den Sie löschen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Andere Felder</td> 
   <td>Geben Sie Werte für alle anderen Felder ein. Die verfügbaren Felder hängen vom ausgewählten Datensatztyp ab. </td> 
  </tr> 
 </tbody> 
</table>

#### Einträge auflisten

Dieses Modul gibt mithilfe von Cursor-basierten Paging- und Eigenschaftsfiltern eine ausgelagerte Liste von Datensätzen zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td>Wählen Sie den Datensatztyp aus, für den Sie eine Liste zurückgeben möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eigenschaft</td> 
   <td>Klicken Sie für jeden Eigenschaftsfilter, für den Sie Ergebnisse zurückgeben möchten, auf <b>Element hinzufügen</b> und geben Sie das Feld, den Operator und den Wert ein, nach dem Sie filtern möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Starten</td> 
   <td>Geben Sie den Ort ein, an dem Sie die zurückgegebenen Ergebnisse starten möchten. Dies wird für die Paginierung verwendet.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul für jeden Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sortieren nach</td> 
   <td>Wählen Sie das Feld aus, nach dem die Ergebnisse sortiert werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Richtung</td> 
   <td>Wählen Sie aus, ob die Ergebnisse auf- oder absteigend sortiert werden sollen.</td> 
  </tr> 
 </tbody> 
</table>

#### Eintrag lesen

Dieses Modul ruft den angegebenen Datensatz ab

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> Wählen Sie den Typ des Datensatzes aus, den Sie löschen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Andere Felder</td> 
   <td>Geben Sie Werte für alle anderen Felder ein. Die verfügbaren Felder hängen vom ausgewählten Datensatztyp ab. </td> 
  </tr> 
 </tbody> 
</table>

#### Eintrag aktualisieren

Aktualisiert einen angegebenen Datensatz.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> Wählen Sie den Typ des Datensatzes aus, den Sie aktualisieren möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name</td> 
   <td> Geben Sie einen neuen Namen für den Datensatz ein oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td> Geben Sie die ID des Datensatzes ein, den Sie aktualisieren möchten, oder mappen Sie sie. </td> 
  </tr> 
 </tbody> 
</table>

### Exportieren

#### Aktivitätsprotokolle exportieren

Dieses Modul exportiert Aktivitätsprotokolle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dateityp</td> 
   <td>Wählen Sie das Dateiformat aus, in das Sie Protokolle exportieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eigenschaft</td> 
   <td>Klicken Sie für jeden Eigenschaftsfilter, für den Sie Ergebnisse zurückgeben möchten, auf <b>Element hinzufügen</b> und geben Sie das Feld, den Operator und den Wert ein, nach dem Sie filtern möchten. Sie können auch nach dem Vorhandensein des Felds filtern.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Starten</td> 
   <td>Geben Sie den Ort ein, an dem Sie die zurückgegebenen Ergebnisse starten möchten. Dies wird für die Paginierung verwendet.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul für jeden Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sortieren nach</td> 
   <td>Wählen Sie das Feld aus, nach dem die Ergebnisse sortiert werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Richtung</td> 
   <td>Wählen Sie aus, ob die Ergebnisse auf- oder absteigend sortiert werden sollen.</td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

* [Abrufen von Warteschlangenstatistiken für einen Hook](#get-queue-statistics-for-a-hook)
* [Datensatzabhängigkeiten abrufen](#get-record-dependencies)
* [Auflisten von Szenarien für eine Verbindung](#list-scenarios-for-a-connection)
* [Auflisten der Fusion-Regionen und -Organisationen](#list-the-fusion-regions-and-organizations)

#### Abrufen von Warteschlangenstatistiken für einen Hook

Dieses Modul gibt Warteschlangenstatistiken für den angegebenen Hook zurück: die Anzahl der aktuell in der Warteschlange befindlichen Ereignisse, das Warteschlangenlimit und ob der Hook aktiviert ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  <tr> 
   <td role="rowheader">Hook-ID</td> 
   <td> Geben Sie die ID des Hooks ein, für den Sie Details zurückgeben möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Datensatzabhängigkeiten abrufen

Dieses Modul ruft die Abhängigkeiten des Datensatzes ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> Wählen Sie den Datensatztyp aus, für den Sie Abhängigkeiten abrufen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Szenario-ID</td> 
   <td> Geben Sie die ID des Datensatzes ein, für den Sie Abhängigkeiten abrufen möchten, oder ordnen Sie sie zu. </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### Auflisten von Szenarien für eine Verbindung

Dieses Modul gibt eine paginierte Liste von Szenarien zurück, die auf die angegebene Verbindung verweisen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verbindungs-ID</td> 
   <td>Geben Sie die ID der Verbindung ein, für die Sie Szenarien zurückgeben möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eigenschaft</td> 
   <td>Klicken Sie für jeden Eigenschaftsfilter, für den Sie Ergebnisse zurückgeben möchten, auf <b>Element hinzufügen</b> und geben Sie das Feld, den Operator und den Wert ein, nach dem Sie filtern möchten. Sie können auch nach dem Vorhandensein des Felds filtern.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Starten</td> 
   <td>Geben Sie den Ort ein, an dem Sie die zurückgegebenen Ergebnisse starten möchten. Dies wird für die Paginierung verwendet.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul für jeden Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sortieren nach</td> 
   <td>Wählen Sie das Feld aus, nach dem die Ergebnisse sortiert werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Richtung</td> 
   <td>Wählen Sie aus, ob die Ergebnisse auf- oder absteigend sortiert werden sollen.</td> 
  </tr> 
 </tbody> 
</table>

#### Auflisten der Fusion-Regionen und -Organisationen

Dieses Modul gibt die Regions- und Organisations-ID für jede Fusion-Organisation zurück, auf die die Verbindung zugreifen kann, basierend auf den Anmeldeinformationen und dem Zugriff der in der Verbindung verwendeten Anmeldeinformationen im IMS-Benutzerprofil.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Workfront Fusion mit Workfront Fusion finden Sie unter <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront Fusion mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
 </tbody> 
</table>





