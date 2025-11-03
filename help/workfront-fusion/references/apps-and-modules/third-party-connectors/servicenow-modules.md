---
title: ServiceNow-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die verwenden [!DNL ServiceNow] und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1628'
ht-degree: 1%

---

# [!DNL ServiceNow]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL ServiceNow] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Um [!DNL ServiceNow]-Module verwenden zu können, müssen Sie über ein [!DNL ServiceNow]-Konto verfügen.

## ServiceNow-API-Informationen

Der ServiceNow-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://{{connection.instance}}/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL ServiceNow] mit Workfront Fusion

So erstellen Sie eine Verbindung für Ihre [!DNL ServiceNow]:

1. Klicken Sie **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung], wenn Sie mit der Konfiguration des ersten [!DNL ServiceNow] beginnen.
1. Geben Sie Folgendes ein:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Verbindungsname]</p> </td> 
      <td>Geben Sie einen Namen für die neue [!DNL ServiceNow] ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Umgebung]</p> </td> 
      <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Kennwort]</p> </td> 
      <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Benutzername]</p> </td> 
      <td>Geben Sie Ihren [!DNL ServiceNow] Benutzernamen ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Kennwort]</p> </td> 
      <td>Geben Sie Ihr ServiceNow-Kennwort ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL-Instanz]</p> </td> 
      <td> <p>Geben Sie die Adresse Ihres [!DNL ServiceNow] Kontos ohne <code>https://</code> ein (normalerweise <code>&lt;company>.service-now.com</code>).</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **Fortfahren**, um die Verbindung zu speichern und zum Modul zurückzukehren.

   <!--Markdown placeholder-->

## [!UICONTROL ServiceNow]-Module und ihre Felder

Beim Konfigurieren von [!DNL ServiceNow] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL ServiceNow] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Wenn ein benutzerdefinierter Datensatz in einem Feld vom Typ &quot;[!UICONTROL Record]&quot; ausgewählt wird, kann es einige Zeit dauern, bis die benutzerdefinierten Felder geladen sind.
>
>* Wenn keine benutzerdefinierten Datensätze vorhanden sind, ist das Dropdown-Feld „Datensatztyp“ leer.

### Trigger

#### [!UICONTROL Einträge beobachten]

Dieses Trigger-Modul aktiviert ein Szenario, wenn ein Datensatz erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL, Tabellentyp]</td> 
   <td>Wählen Sie aus, ob es sich bei der Tabelle, die Sie beobachten möchten, um eine benutzerdefinierte Tabelle oder eine Standardtabelle handelt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Typ des Datensatzes aus, den Sie beobachten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Anzeige]</td> 
   <td>Wählen Sie den Typ der Werte aus, die Sie anzeigen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Felder aus, die das Modul ausgeben soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL filter]</td> 
   <td>Wählen Sie aus, ob neue oder aktualisierte Datensätze überwacht werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Datensatz erstellen]](#create-a-record)
* [[!UICONTROL Benutzerdefinierter API-Aufruf]](#custom-api-call)
* [[!UICONTROL Deaktivieren von Benutzern]](#deactivate-a-user)
* [[!UICONTROL Löschen eines Datensatzes]](#delete-a-record)
* [[!UICONTROL Anlage herunterladen]](#download-an-attachment)
* [[!UICONTROL Eintrag lesen]](#read-a-record)
* [[!UICONTROL Anlage hochladen]](#upload-an-attachment)
* [[!UICONTROL Aktualisieren eines Datensatzes]](#update-a-record)

#### [!UICONTROL Datensatz erstellen]

Dieses Aktionsmodul erstellt einen neuen [!DNL ServiceNow].

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL, Tabellentyp]</td> 
   <td>Wählen Sie aus, ob Sie einen Datensatz in einer benutzerdefinierten Tabelle oder einer Standardtabelle erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Typ [!DNL ServiceNow] Datensatzes aus, den das Modul erstellen soll. Anschließend können Sie die verfügbaren Felder für diesen Datensatztyp ausfüllen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL ServiceNow]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL ServiceNow] nicht durchgeführt werden kann.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL relative URL]</td> 
   <td> Geben Sie einen Pfad relativ zu <code>https://&ltinstance_url&gt/api/</code> ein. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
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

#### [!UICONTROL Deaktivieren von Benutzern]

Dieses Aktionsmodul deaktiviert einen Benutzer in [!DNL ServiceNow] mithilfe der System-ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Benutzersystem-ID]</td> 
   <td> Geben Sie die eindeutige [!DNL ServiceNow]-ID des Benutzers ein, den Sie das Modul deaktivieren möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Löschen eines Datensatzes]

Dieses Aktionsmodul löscht einen Vorfall oder einen Benutzer.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie aus, ob Sie einen Vorfall oder einen Benutzer löschen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System-ID]</td> 
   <td>Geben Sie die eindeutige [!DNL ServiceNow]-ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Anlage herunterladen]

Dieses Aktionsmodul lädt eine Anlage in einem [!DNL ServiceNow] herunter.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anlagensystemkennung]</td> 
   <td> Geben Sie die eindeutige [!DNL ServiceNow]-ID des Anhangs ein, den das Modul herunterladen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eintrag lesen]

Dieses Aktionsmodul liest einen [!DNL ServiceNow]-Datensatz unter Verwendung der System-ID.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatz-System-ID]</td> 
   <td>Geben Sie die eindeutige [!DNL ServiceNow]-ID des Datensatzes ein, den das Modul lesen soll, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL, Tabellentyp]</td> 
   <td>Wählen Sie aus, ob sich der Datensatz, den Sie lesen möchten, in einer benutzerdefinierten Tabelle oder einer Standardtabelle befindet.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Typ [!DNL ServiceNow] Datensatzes aus, den das Modul lesen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Anzeige]</td> 
   <td>Wählen Sie den Typ der Werte aus, die Sie anzeigen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Felder aus, die das Modul ausgeben soll.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren eines Datensatzes]

Dieses Aktionsmodul erstellt einen neuen [!DNL ServiceNow].

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatz-System-ID]</td> 
   <td>Geben Sie die eindeutige [!DNL ServiceNow]-ID des Datensatzes ein, den Sie aktualisieren möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL, Tabellentyp]</td> 
   <td>Wählen Sie aus, ob sich der zu aktualisierende Datensatz in einer benutzerdefinierten Tabelle oder einer Standardtabelle befindet.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Typ [!DNL ServiceNow] Datensatzes aus, den das Modul aktualisieren soll. Anschließend können Sie die verfügbaren Felder für diesen Datensatztyp ausfüllen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Anlage hochladen]

Dieses Aktionsmodul lädt eine Anlage in einen [!DNL ServiceNow].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tabellenname]</td> 
   <td>Geben Sie den Namen der Tabelle ein, in die Sie die Anlage hochladen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System-ID]</td> 
   <td>Geben Sie die eindeutige [!DNL ServiceNow]-ID des Elements ein, in das Sie die Anlage hochladen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

#### [!UICONTROL Suche nach Datensätzen]

Dieses Modul sucht mithilfe ausgewählter Kriterien nach Datensätzen.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres ServiceNow-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL ServiceNow] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL, Tabellentyp]</td> 
   <td>Wählen Sie aus, ob die zu durchsuchende Tabelle eine benutzerdefinierte Tabelle oder eine Standardtabelle ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Typ des Datensatzes aus, nach dem Sie suchen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ergebnissatz]</td> 
   <td>Wählen Sie aus, ob das Modul alle Datensätze zurückgeben soll, die den Kriterien entsprechen, oder nur den ersten Eintrag, der damit übereinstimmt. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl von Datensätzen]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Suchtyp]</td> 
   <td> <p>Wählen Sie aus, welchen Suchtyp das Modul ausführen soll.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Erweiterte Abfrage]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL-Suchanfrage]</p> <p>Geben Sie die benutzerdefinierte Suchabfrage ein. Informationen zum [!DNL ServiceNow] benutzerdefinierter Suchabfragen finden Sie in der <a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">ServiceNow-Abfragedokumentation</a>.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Simple]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Suchkriterien]</p> <p>Geben Sie die Kriterien ein, nach denen das Modul suchen soll. </li> 
       <li> <p>[!UICONTROL Sortieren nach]</p> <p>Geben Sie an, nach welchem Feld das Modul die Ergebnisse sortieren soll und ob sie auf- oder absteigend sortiert werden sollen.</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Anzeige]</td> 
   <td>Wählen Sie den Typ der Werte aus, die Sie anzeigen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Felder aus, die das Modul ausgeben soll.</td> 
  </tr> 
 </tbody> 
</table>
