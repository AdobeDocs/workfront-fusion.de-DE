---
title: Allocadia-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die Allocadia verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 9a6fccd6-6eee-42dc-a678-c1f34280d139
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1304'
ht-degree: 0%

---

# [!DNL Allocadia]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Allocadia] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Plan*</td>
  <td> <p>[!UICONTROL Pro] oder höher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
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

Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

## [!DNL Allocadia] mit [!DNL Workfront Fusion] verbinden

Sie können direkt aus einem [!DNL Allocadia]-Modul heraus eine Verbindung zu Ihrem [!DNL Allocadia]-Konto herstellen.

1. Klicken Sie in einem beliebigen [!DNL Allocadia] auf **[!UICONTROL Add]** neben dem Feld [!UICONTROL Connection] .
1. Wählen Sie aus, ob Sie den Nordamerika- oder den Europa-Server verwenden möchten.
1. Geben Sie Ihren Benutzernamen und Ihr Kennwort ein.
1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Allocadia] Module und ihre Felder

Beim Konfigurieren [!DNL Allocadia] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Allocadia] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

#### [!UICONTROL Watch Record]

Dieses Trigger-Modul führt ein Szenario aus, in dem Objekte eines bestimmten Typs hinzugefügt, aktualisiert oder beides werden. Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz oder den Datensätzen verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> <table style="table-layout:auto"> <col> 
 <col> 
 <tbody> 
  <tr> 
   td role=„rowHeader“&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Allocadia-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect Allocadia] zu Workfront </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>Wählen Sie aus, ob das Szenario nur neue, [!UICONTROL Updated Records Only] oder neue und aktualisierte Datensätze ansehen soll.</p> </td> 
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
   <td role="rowheader">Grenze</td> 
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

#### [!UICONTROL Custom API Call]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Allocadia]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Allocadia] nicht durchgeführt werden kann.

Die Aktion basiert auf dem von Ihnen angegebenen Entitätstyp (Allocadia-Objekttyp).

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Allocadia]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://api-na.allocadia.com/{version}</code> oder <code>https://api-eu.allocadia.com/{version}</code> ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read Record]

Dieses Aktionsmodul liest Daten aus einem einzelnen Datensatz in [!DNL Allocadia].

Sie geben die ID des Datensatzes an.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role=„rowHeader“&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Allocadia]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Wählen Sie den Typ [!DNL Allocadia] Datensatzes aus, den das Modul lesen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten. Die verfügbaren Felder hängen von der ausgewählten [!UICONTROL Entity Type] ab.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die eindeutige [!DNL Allocadia]-ID des Datensatzes ein, den das Modul lesen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Record]

Dieses Aktionsmodul erstellt einen Datensatz.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role=„rowHeader“&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Allocadia]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
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

#### [!UICONTROL Delete Record]

Dieses Aktionsmodul löscht einen bestimmten Datensatz.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role=„rowHeader“&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Allocadia]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td> <p>Wählen Sie den Typ der Entität aus, die Sie löschen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Line item]</strong> </p> <p>Zeileneintrags-ID eingeben</p> </li> 
     <li> <p><strong>[!UICONTROL Column Choice]</strong> </p> <p>Wählen Sie das Budget aus, aus dem Sie einen Datensatz löschen möchten, und geben Sie dann die Spalten-ID und die Auswahl-ID ein.</p> </li> 
     <li> <p><strong>[!UICONTROL Forecast Tags]</strong> </p> <p>Wählen Sie das Budget aus, aus dem Sie einen Datensatz löschen möchten, und geben Sie dann die Tag-ID ein.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update Record]

Dieses Aktionsmodul aktualisiert einen Datensatz, z. B. ein Zeilenelement, ein Benutzer oder eine Spaltenauswahl.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Allocadia]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Wählen Sie den Typ [!DNL Allocadia] Datensatzes aus, den das Modul aktualisieren soll. Andere Felder werden je nach ausgewähltem Entitätstyp angezeigt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Wählen Sie das Budget aus, in dem Sie einen Datensatz aktualisieren möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

#### [!UICONTROL Search Record]

Dieses Suchmodul sucht in einem -Objekt nach Datensätzen, [!DNL Allocadia] mit der angegebenen Suchanfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Sie geben den Typ der gewünschten Datensätze an.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role=„rowHeader“&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Allocadia]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Allocadia] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Wählen Sie den Typ [!DNL Allocadia] Datensatzes aus, nach dem das Modul suchen soll. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Wählen Sie das Budget aus, das Sie durchsuchen möchten. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Wählen Sie aus, ob das Modul alle übereinstimmenden Datensätze oder nur den ersten übereinstimmenden Datensatz zurückgeben soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal count of records]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>Wählen Sie das Feld aus, nach dem Sie suchen möchten, wählen Sie den Vorgang aus und geben Sie den Wert ein, nach dem Sie suchen möchten, oder ordnen Sie ihn zu. Sie können [!DNL AND] oder [!DNL OR] Regeln hinzufügen, um Ihre Suche weiter zu filtern.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten. Die verfügbaren Felder hängen vom ausgewählten Entitätstyp ab.</p> </td> 
  </tr> 
 </tbody> 
</table>
