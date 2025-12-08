---
filename: adobe-indesign-modules
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe InDesign-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Adobe InDesign verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
source-git-commit: 30ddefa8519e6f2052308482137d0fa018676902
workflow-type: tm+mt
source-wordcount: '1693'
ht-degree: 20%

---


# Adobe InDesign-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Adobe InDesign verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Bevor Sie den Adobe InDesign-Connector verwenden können, müssen Sie über ein gültiges Adobe InDesign-Konto verfügen.

## Erstellen einer Verbindung mit Adobe InDesign

So erstellen Sie eine Verbindung für Ihre Adobe InDesign-Module:

1. Klicken Sie in einem beliebigen Adobe InDesign **Modul** Hinzufügen) neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col>
      </col>
      <col>
      </col>
      <tbody>
        <tr>
          <td role="rowheader">Verbindungsname</td>
          <td>
            <p>Geben Sie einen Namen für die Verbindung ein.</p>
          </td>
        </tr>
      <tr>
        <td role="rowheader">Umgebung</td>
        <td>
          <p>Wählen Sie aus, ob eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung hergestellt werden soll.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Typ</td>
        <td>
          <p>Wählen Sie aus, ob eine Verbindung zu einem Service-Konto oder einem persönlichen Konto hergestellt werden soll.</p>
        </td>
      </tr>
        <tr>
          <td role="rowheader">Client-ID</td>
          <td>Geben Sie Ihre Adobe-Client-ID ein. Diese finden Sie im Abschnitt Anmeldedaten des Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Client-Geheimnis</td>
          <td>Geben Sie Ihr Adobe-Client-Geheimnis ein. Diese finden Sie im Abschnitt Anmeldedaten des Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">IMS-Organisations-ID</td>
          <td>Geben Sie Ihre Adobe-Organisations-ID ein. Diese finden Sie im Abschnitt Anmeldedaten des Adobe Developer Console</td>
        </tr>
      </tbody>
    </table>
1. Klicken Sie auf **Weiter**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## InDesign-Module und ihre Felder

Beim Konfigurieren von Adobe InDesign-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service können zusätzlich dazu weitere Adobe InDesign-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Aktionen

* [Erstellen von Ausgabedarstellungen](#create-rendition)
* [Löschen eines benutzerdefinierten Skripts](#delete-a-custom-script)
* [Zusammenführen von Daten](#merge-data)
* [Links neu zuordnen](#remap-links)
* [Senden einer Anfrage zur Ausführung eines benutzerdefinierten Skripts](#submit-a-custom-script-execution-request)

#### Erstellen von Ausgabedarstellungen

Dieses Aktionsmodul erstellt eine JPEG-, PNG- oder PDF-Ausgabedarstellung eines bestimmten InDesign-Dokuments und gibt sie zurück. Die Struktur von `StatusCompletedRespons/output/data` finden Sie unter `RenditionOutputData`. Eine Liste der möglichen Fehler-Codes in `FailedEvent` finden Sie unter `RenditionFailedData`.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu Adobe InDesign finden Sie unter <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Erstellen einer Verbindung zu Adobe InDesign</a> in diesem Artikel.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Typ</p>
      </td>
      <td>Wählen Sie den Dateityp der Ausgabedarstellung aus, die Sie erstellen möchten. 
      <ul><li>JPEG</li><li>PNG</li><li>PDF</li></ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Für jedes Asset, das Sie der Ausgabedarstellung hinzufügen möchten:<ol><li>Klicken Sie <b>Element hinzufügen</b>.</li><li>Wählen Sie die Quelle des Assets aus oder ordnen Sie sie zu.</li><li>Geben Sie ein Ziel ein. Das Ziel ist ein Pfad relativ zu einem temporären Basisverzeichnis (Arbeitsverzeichnis), in das die Ressource heruntergeladen wird. Dadurch werden die Assets innerhalb der Parameter identifiziert. Sie kann nicht mit "..“ hochgefahren werden oder "/". Es muss ein gültiger Dateiname vorhanden sein.</td>
    </tr>
    <tr>
      <td role="rowheader">Zieldokument</td>
      <td>Geben Sie das Dokument ein, das verarbeitet und gerendert werden soll, oder ordnen Sie es zu. Derzeit wird jeweils nur ein Dokument unterstützt.</td>
    </tr>
    <tr>
      <td role="rowheader">Andere Felder</td>
   <td>Für andere Felder siehe die im Modul enthaltenen Informationen.</td>     </tr>
  </tbody>
</table>

#### Löschen eines benutzerdefinierten Skripts

Dieses Aktionsmodul löscht ein einzelnes registriertes benutzerdefiniertes Skript. Alle Versionen des Skripts werden dauerhaft entfernt.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu Adobe InDesign finden Sie unter <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Erstellen einer Verbindung zu Adobe InDesign</a> in diesem Artikel.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Skriptname</p>
      </td>
      <td>Geben Sie den Namen des Skripts ein, das Sie löschen möchten, oder ordnen Sie ihn zu.</td>
    </tr>
  </tbody>
</table>

#### Zusammenführen von Daten

Dieses Modul erstellt InDesign-Dokumente oder PDFs, indem CSV-Daten mit InDesign-Vorlagen zusammengeführt werden. Zu den Ausgabeformaten gehören JPEG-, PNG-, PDF- und InDesign-Dokumente.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu Adobe InDesign finden Sie unter <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Erstellen einer Verbindung zu Adobe InDesign</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Für jedes Asset, das Sie der Datenzusammenführung hinzufügen möchten:<ol><li>Klicken Sie <b>Element hinzufügen</b>.</li><li>Wählen Sie die Quelle des Assets aus oder ordnen Sie sie zu.</li><li>Geben Sie ein Ziel ein. Das Ziel ist ein Pfad relativ zu einem temporären Basisverzeichnis (Arbeitsverzeichnis), in das die Ressource heruntergeladen wird. Dadurch werden die Assets innerhalb der Parameter identifiziert. Sie kann nicht mit "..“ hochgefahren werden oder "/". Es muss ein gültiger Dateiname vorhanden sein.</td>
    </tr>
    <tr>
      <td role="rowheader">Zieldokument</td>
      <td>Geben Sie das Dokument ein, das als Vorlage für die Zusammenführung verwendet werden soll, oder ordnen Sie es zu.</td>
    </tr>
    <tr>
      <td role="rowheader">Datenquelle</td>
      <td>Geben Sie die zu verwendenden Quelldateien ein oder mappen Sie sie.</td>
    </tr>
    <tr>
      <td role="rowheader">Andere Felder</td>
   <td>Für andere Felder siehe die im Modul enthaltenen Informationen.</td>     </tr>
  </tbody>
</table>

#### Links neu zuordnen

Dieses Modul ersetzt dateibasierte Links in InDesign-Dokumenten durch Adobe Experience Manager (AEM)-URLs. Dies kann für die Arbeit mit Adobe Experience Manager über Adobe Asset Link nützlich sein.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu Adobe InDesign finden Sie unter <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Erstellen einer Verbindung zu Adobe InDesign</a> in diesem Artikel.</td>
      </tr>
    <tr>
      <td role="rowheader">AEM-Token</td>
      <td>Geben Sie das für das technische AEM-Konto generierte Bearer-Token ohne das Bearer-Keyword ein oder ordnen Sie es zu.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Für jedes Asset, das Sie dem Modul hinzufügen möchten:<ol><li>Klicken Sie <b>Element hinzufügen</b>.</li><li>Wählen Sie die Quelle des Assets aus oder ordnen Sie sie zu.</li><li>Geben Sie ein Ziel ein. Das Ziel ist ein Pfad relativ zu einem temporären Basisverzeichnis (Arbeitsverzeichnis), in das die Ressource heruntergeladen wird. Dadurch werden die Assets innerhalb der Parameter identifiziert. Sie kann nicht mit "..“ hochgefahren werden oder "/". Es muss ein gültiger Dateiname vorhanden sein.</td>
    </tr>
    <tr>
      <td role="rowheader">Zieldokument</td>
      <td>Geben Sie das Dokument ein, in dem Sie Links neu zuordnen möchten, oder ordnen Sie es zu.</td>
    </tr>
    <tr>
      <td role="rowheader">Datenquelle</td>
      <td>Geben Sie die Quelldateien ein, die zum Extrahieren und Abgleichen von Tags verwendet werden sollen, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">Andere Felder</td>
   <td>Für andere Felder siehe die im Modul enthaltenen Informationen.</td>     </tr>
  </tbody>
</table>

#### Senden einer Anfrage zur Ausführung eines benutzerdefinierten Skripts

Dieses Aktionsmodul sendet eine Ausführungsanfrage für ein benutzerdefiniertes Skript. Sie definieren die Eingabe-Assets und -Parameter, die das benutzerdefinierte Skript während der Ausführung verwenden soll.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu Adobe InDesign finden Sie unter <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Erstellen einer Verbindung zu Adobe InDesign</a> in diesem Artikel.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Skript-ID</p>
      </td>
      <td>Geben Sie die ID des benutzerdefinierten Skripts ein oder mappen Sie sie.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Für jedes Asset, für das Sie eine Ausführungsanfrage senden möchten, <ol><li>Klicken Sie <b>Element hinzufügen</b>.</li><li>Wählen Sie die Quelle des Assets aus oder ordnen Sie sie zu.</li><li>Geben Sie ein Ziel ein. Das Ziel ist ein Pfad relativ zu einem temporären Basisverzeichnis (Arbeitsverzeichnis), in das die Ressource heruntergeladen wird. Dadurch werden die Assets innerhalb der Parameter identifiziert. Sie kann nicht mit "..“ hochgefahren werden oder "/". Es muss ein gültiger Dateiname vorhanden sein.</td>
    </tr>
    <tr>
      <td role="rowheader">Andere Felder</td>
   <td>Für andere Felder siehe die im Modul enthaltenen Informationen.</td>     </tr>
  </tbody>
</table>

### Suchvorgänge

* [Abrufen benutzerdefinierter Skriptdetails](#get-custom-script-details)
* [Abrufen von Datenzusammenführungstags](#get-data-merge-tags)
* [Dokumentinformationen abrufen](#get-document-information)
* [Auflisten benutzerdefinierter Skripte](#list-custom-scripts)

#### Abrufen benutzerdefinierter Skriptdetails

Dieses Suchmodul ruft Details eines einzelnen registrierten benutzerdefinierten Skripts ab, einschließlich Version, Download-Link, Registrierungsdatum und Skriptname.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu Adobe InDesign finden Sie unter <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Erstellen einer Verbindung zu Adobe InDesign</a> in diesem Artikel.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Skriptname</p>
      </td>
      <td>Geben Sie den Namen des Skripts ein, für das Sie Details abrufen möchten, oder ordnen Sie ihn zu.</td>
    </tr>
  </tbody>
</table>

#### Abrufen von Datenzusammenführungstags

Dieses Modul ruft die Datenzusammenführungs-Tags aus einem Dokument ab.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu Adobe InDesign finden Sie unter <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Erstellen einer Verbindung zu Adobe InDesign</a> in diesem Artikel.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Für jedes Asset, das Sie dem Modul hinzufügen möchten:<ol><li>Klicken Sie <b>Element hinzufügen</b>.</li><li>Wählen Sie die Quelle des Assets aus oder ordnen Sie sie zu.</li><li>Geben Sie ein Ziel ein. Das Ziel ist ein Pfad relativ zu einem temporären Basisverzeichnis (Arbeitsverzeichnis), in das die Ressource heruntergeladen wird. Dadurch werden die Assets innerhalb der Parameter identifiziert. Sie kann nicht mit "..“ hochgefahren werden oder "/". Es muss ein gültiger Dateiname vorhanden sein.</td>
    </tr>
    <tr>
      <td role="rowheader">Zieldokument</td>
      <td>Geben Sie das Dokument ein, von dem Sie Tags abrufen möchten, oder ordnen Sie es zu.</td>
    </tr>
    <tr>
      <td role="rowheader">Datenquelle</td>
      <td>Geben Sie die Quelldateien ein, die zum Extrahieren und Abgleichen von Tags verwendet werden sollen, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">Andere Felder</td>
   <td>Für andere Felder siehe die im Modul enthaltenen Informationen.</td>     </tr>
  </tbody>
</table>

#### Dokumentinformationen abrufen

Dieses Modul ruft umfassende Informationen zu INDD/IDML-Dokumenten ab und gibt Daten basierend auf den aktivierten Informationstypen zurück, die in der Anfrage angegeben sind.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu Adobe InDesign finden Sie unter <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Erstellen einer Verbindung zu Adobe InDesign</a> in diesem Artikel.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Für jedes Asset, das Sie dem Modul hinzufügen möchten:<ol><li>Klicken Sie <b>Element hinzufügen</b>.</li><li>Wählen Sie die Quelle des Assets aus oder ordnen Sie sie zu.</li><li>Geben Sie ein Ziel ein. Das Ziel ist ein Pfad relativ zu einem temporären Basisverzeichnis (Arbeitsverzeichnis), in das die Ressource heruntergeladen wird. Dadurch werden die Assets innerhalb der Parameter identifiziert. Sie kann nicht mit "..“ hochgefahren werden oder "/". Es muss ein gültiger Dateiname vorhanden sein.</td>
    </tr>
    <tr>
      <td role="rowheader">Zieldokument</td>
      <td>Geben Sie das Dokument ein, aus dem Sie Informationen abrufen möchten, oder ordnen Sie es zu.</td>
    </tr>
     <tr>
      <td role="rowheader">Andere Felder</td>
   <td>Für andere Felder siehe die im Modul enthaltenen Informationen.</td>     </tr>
  </tbody>
</table>

#### Auflisten benutzerdefinierter Skripte

Dieses Modul ruft Details zur neuesten Version aller registrierten benutzerdefinierten Skripte ab, einschließlich Version, Download-Link, Registrierungsdatum und Skriptname. Die Ergebnisse werden anhand der Listenlänge paginiert.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu Adobe InDesign finden Sie unter <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Erstellen einer Verbindung zu Adobe InDesign</a> in diesem Artikel.</td>
      </tr>
    <tr>
      <td role="rowheader">Seitennummer</td>
      <td>Geben Sie die Seitennummer ein, von der aus Sie beginnen möchten, oder mappen Sie sie zu.</td>
    </tr>
  <tr> 
   <td>Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Legen Sie die maximale Anzahl von Teams oder Gruppen fest, die Workfront Fusion während eines Ausführungszyklus zurückgeben soll.</td> 
  </tr> 
  </tbody>
</table>


### Sonstige

#### Benutzerdefinierten API-Aufruf erstellen

Dieses Modul führt einen benutzerdefinierten API-Aufruf an die Adobe InDesign-API durch

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu Adobe InDesign finden Sie unter <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Erstellen einer Verbindung zu Adobe InDesign</a> in diesem Artikel.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Path</p>
      </td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://indesign.adobe.io/v3</code> ein.</p><p> Beispiel: <code>/create-rendition</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Methode</p>
      </td>
      <td>
        <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter [HTTP-Anfragemethoden](/help/workfront-fusion/references/modules/http-request-methods.md).</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Header</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt automatisch Autorisierungs-Header hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Abfragezeichenfolge  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
      </td>
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
