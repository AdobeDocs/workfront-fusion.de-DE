---
title: Allocadia-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Allocadia verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 9a6fccd6-6eee-42dc-a678-c1f34280d139
TQID: https://experienceleague.adobe.com/bCfkq5fzw21hmZWLrWztL27g2RAlBbyk9vPEQ-v6bBU
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1467
ht-degree: 56%

---

# [!DNL Allocadia]-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Allocadia] verwenden, und diese mit verschiedenen Anwendungen und Services von Drittanbietern verbinden.

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

Um [!DNL Allocadia] Module verwenden zu können, müssen Sie über ein [!DNL Allocadia]-Konto verfügen.

## [!DNL Allocadia] API-Informationen

Der Allocadia-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.7.6</td> 
  </tr>
 </tbody> 
</table>

## Verbinden von [!DNL Allocadia] mit Workfront Fusion

Sie können direkt aus einem [!DNL Allocadia]-Modul heraus eine Verbindung zu Ihrem [!DNL Allocadia]-Konto herstellen.

1. Klicken Sie in einem [!DNL Allocadia] Modul **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Wählen Sie aus, ob Sie den Nordamerika- oder den Europa-Server verwenden möchten.
1. Geben Sie Ihren Benutzernamen und Ihr Kennwort ein.
1. Klicken Sie auf **[!UICONTROL Fortsetzen]**, um die Verbindung zu erstellen und zum Modul zurückzukehren.

## [!DNL Allocadia]-Module und ihre Felder

Beim Konfigurieren von [!DNL Allocadia]-Modulen werden in Workfront Fusion die unten aufgeführten Felder angezeigt. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere [!DNL Allocadia]-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

#### [!UICONTROL Eintrag überwachen]

Dieses Auslösermodul führt ein Szenario aus, wenn Objekte eines bestimmten Typs hinzugefügt und/oder aktualisiert werden. Das Modul gibt alle Standardfelder zurück, die mit dem Eintrag bzw. den Einträgen verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> <table style="table-layout:auto"> <col> 
 <col> 
 <tbody> 
  <tr> 
   td role=„rowHeader“&gt; <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Allocadia-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect Allocadia] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>Wählen Sie aus, ob das Szenario nur neue, [!UICONTROL Nur aktualisierte Datensätze] oder neue und aktualisierte Datensätze ansehen soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Entitätstyp</td> 
   <td>Wählen Sie den Allocadia-Datensatztyp aus, den das Modul überwachen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ausgaben</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten. Die verfügbaren Felder hängen vom ausgewählten Entitätstyp ab.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beschränkungen</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus überwachen soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [Benutzerdefinierter API-Aufruf](#custom-api-call)
* [Datensatz lesen](#read-record)
* [Datensatz erstellen](#create-record)
* [Datensatz löschen](#delete-record)
* [Eintrag aktualisieren](#update-record)

#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Allocadia]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, was über die anderen [!DNL Allocadia]-Module nicht möglich ist.

Die Aktion basiert auf dem von Ihnen angegebenen Entitätstyp (Allocadia-Objekttyp).

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Allocadia]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://api-na.allocadia.com/{version}</code> oder <code>https://api-eu.allocadia.com/{version}</code> ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Header]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
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

#### [!UICONTROL Datensatz lesen]

Dieses Aktionsmodul liest Daten aus einem einzelnen Datensatz in [!DNL Allocadia].

Geben Sie die ID des Eintrags an.

Das Modul gibt alle Standardfelder zurück, die mit dem Eintrag verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role=„rowHeader“&gt; <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Allocadia]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td>Wählen Sie den Typ [!DNL Allocadia] Datensatzes aus, den das Modul lesen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten. Die verfügbaren Felder hängen vom ausgewählten [!UICONTROL Entity Type] ab.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die eindeutige [!DNL Allocadia]-ID des Datensatzes ein, den das Modul lesen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datensatz erstellen]

Dieses Aktionsmodul erstellt einen Datensatz.

Das Modul gibt daraufhin die ID des Eintrags und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role=„rowHeader“&gt; <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Allocadia]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td>Wählen Sie aus, ob ein neuer Datensatz basierend auf einem Zeileneintrag oder einer Spaltenauswahl erstellt werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Wählen Sie das Budget aus, in dem Sie einen Datensatz erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Column choices]</td> 
   <td>Wählen Sie die Spalte aus, die Sie zum Erstellen eines neuen Datensatzes verwenden möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Label]</td> 
   <td>Titel für den neuen Datensatz eingeben oder zuordnen</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eintrag löschen]

Dieses Aktionsmodul löscht einen bestimmten Datensatz.

Geben Sie die ID des Eintrags an.

Das Modul gibt daraufhin die ID des Eintrags und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role=„rowHeader“&gt; <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Allocadia]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td> <p>Wählen Sie den Typ der Entität aus, die Sie löschen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Zeileneintrag]</strong> </p> <p>Zeileneintrags-ID eingeben</p> </li> 
     <li> <p><strong>[!UICONTROL Spaltenauswahl]</strong> </p> <p>Wählen Sie das Budget aus, aus dem Sie einen Datensatz löschen möchten, und geben Sie dann die Spalten-ID und die Auswahl-ID ein.</p> </li> 
     <li> <p><strong>[!UICONTROL Forecast Tags]</strong> </p> <p>Wählen Sie das Budget aus, aus dem Sie einen Datensatz löschen möchten, und geben Sie dann die Tag-ID ein.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eintrag aktualisieren]

Dieses Aktionsmodul aktualisiert einen Datensatz, z. B. ein Zeilenelement, ein Benutzer oder eine Spaltenauswahl.

Geben Sie die ID des Eintrags an.

Das Modul gibt daraufhin die ID des Eintrags und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Allocadia]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td>Wählen Sie den Typ [!DNL Allocadia] Datensatzes aus, den das Modul aktualisieren soll. Andere Felder werden je nach ausgewähltem Entitätstyp angezeigt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Wählen Sie das Budget aus, in dem Sie einen Datensatz aktualisieren möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

#### [!UICONTROL Datensatz suchen]

Dieses Suchmodul sucht in einem -Objekt nach Datensätzen, [!DNL Allocadia] mit der angegebenen Suchanfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Sie geben den Typ der gewünschten Datensätze an.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role=„rowHeader“&gt; <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Allocadia]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td>Wählen Sie den Typ [!DNL Allocadia] Datensatzes aus, nach dem das Modul suchen soll. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Wählen Sie das Budget aus, das Sie durchsuchen möchten. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ergebnissatz]</td> 
   <td>Wählen Sie aus, ob das Modul alle übereinstimmenden Datensätze oder nur den ersten übereinstimmenden Datensatz zurückgeben soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl von Datensätzen]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Suchkriterien]</td> 
   <td>Wählen Sie das Feld aus, nach dem Sie suchen möchten, wählen Sie den Vorgang aus und geben Sie den Wert ein, nach dem Sie suchen möchten, oder ordnen Sie ihn zu. Sie können [!DNL AND] oder [!DNL OR] Regeln hinzufügen, um Ihre Suche weiter zu filtern.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten. Die verfügbaren Felder hängen vom ausgewählten Entitätstyp ab.</p> </td> 
  </tr> 
 </tbody> 
</table>
