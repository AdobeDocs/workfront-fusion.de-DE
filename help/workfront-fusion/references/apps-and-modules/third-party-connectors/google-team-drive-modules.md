---
title: Google Team Drive-Module
description: Mit  [!DNL Adobe Workfront Fusion Google Team Drive]  Modulen können Sie Dateien überwachen, hochladen, aktualisieren, kopieren, löschen oder abrufen und Ordner in Ihrem  [!DNL Google Shared]  erstellen.
author: Becky
feature: Workfront Fusion
exl-id: 95dd9d23-1df9-40da-8fd0-646cc697bfc8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# [!DNL Google Team Drive]

Die [!DNL Adobe Workfront Fusion] [!DNL Google Team Drive] ermöglichen es Ihnen, Dateien zu überwachen, hochzuladen, zu aktualisieren, zu kopieren, zu löschen oder abzurufen und Ordner in Ihrem [!DNL Google Shared Drive] zu erstellen.

Um [!DNL Google Team Drive] mit [!DNL Adobe Workfront Fusion] verwenden zu können, muss ein [!DNL Google Workspace] Konto vorhanden sein. Wenn Sie noch kein solches Konto haben, können Sie ein [!DNL Google Workspace] Konto bei der [[!DNL Google Workspace] Anmeldeseite“ ](https://workspace.google.com/business/signup/welcome).

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Google Team Drive] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um [!DNL Google Team Drive] Module verwenden zu können, müssen Sie über eine [!DNL Google Team Drive] verfügen.

## [!DNL Google Team Drive] Module und ihre Felder

Beim Konfigurieren [!DNL Google Team Drive] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Google Team Drive] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Die Dialogfelder für Module, die in **fett** angezeigt werden (im [!DNL Workfront Fusion] Szenario **nicht** diesem Dokumentationsartikel), sind obligatorisch.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Trigger

#### [!UICONTROL Watch Files]

Gibt Dateidetails zurück, wenn eine neue Datei im angegebenen Ordner hinzugefügt und/oder geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Team Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> Wählen Sie das freigegebene Laufwerk aus, das Sie überwachen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den Ordner im freigegebenen Laufwerk aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p> Wählen Sie den Typ der Dateien aus, die Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] Zu formatierende Dateien] </td> 
   <td> <p>Wählen Sie das Format aus, in das die überwachten [!DNL Google Documents] konvertiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Sheets] Zu formatierende Dateien] </td> 
   <td> <p>Wählen Sie das Format aus, in das die überwachten [!DNL Google Sheets] konvertiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] Zu formatierende Dateien] </td> 
   <td> <p>Wählen Sie das Format aus, in das die überwachten [!DNL Google Slides] konvertiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] Zu formatierende Dateien] </td> 
   <td> <p>Wählen Sie das Format aus, in das die überwachten [!DNL Google Drawings] konvertiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p> Wählen Sie aus, ob Sie den Ordner auf neue und geänderte Dateien oder nur auf neue Dateien überwachen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Dateien fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Upload a File]](#upload-a-file)
* [[!UICONTROL Update a File]](#update-a-file)
* [[!UICONTROL Copy a File]](#copy-a-file)
* [[!UICONTROL Delete a File]](#delete-a-file)
* [[!UICONTROL Move a File to Trash]](#move-a-file-to-trash)
* [[!UICONTROL Get a File]](#get-a-file)
* [[!UICONTROL Get a File List]](#get-a-file-list)
* [[!UICONTROL Create a Folder]](#create-a-folder)

#### [!UICONTROL Upload a File]

Lädt eine Datei auf das angegebene freigegebene Laufwerk hoch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Team Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive] </td> 
   <td> <p>Wählen Sie das freigegebene Laufwerk aus, auf das Sie eine Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den Ordner im freigegebenen Laufwerk aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Geben Sie die Datei an, die Sie auf das freigegebene Laufwerk hochladen möchten.</p> <p>Ordnen Sie die Datei zu, die Sie aus dem vorherigen Modul hochladen möchten (z. B. [!UICONTROL HTTP] &gt;[!UICONTROL Get a File] oder [!UICONTROL Dropbox] &gt;[!UICONTROL Get a file)], oder geben Sie den Dateinamen und die Dateidaten manuell ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td> <p> Geben Sie den Titel der Datei ein, die im freigegebenen Ordner angezeigt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert a File]</td> 
   <td> <p> Aktivieren Sie diese Option, um die Datei in das entsprechende Google-Format in Ihrem freigegebenen Ordner zu konvertieren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a File]

Ermöglicht das Ändern des Dateinamens und/oder des Dateiinhalts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Team Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> Wählen Sie das freigegebene Laufwerk aus, das die zu aktualisierende Datei enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den Ordner im freigegebenen Laufwerk aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> Geben Sie die ID der Datei ein, die Sie aktualisieren möchten (zuordnen).</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title] </td> 
   <td> <p>Geben Sie den neuen Titel für die aktualisierte Datei ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert a File]</td> 
   <td> <p> Aktivieren Sie diese Option, um die Datei in das entsprechende [!DNL Google] in Ihrem freigegebenen Ordner zu konvertieren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy a File]

Kopiert eine angegebene Datei in den ausgewählten Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Team Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> Wählen Sie das freigegebene Laufwerk aus, das die zu kopierende Datei enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den Zielordner aus, in den Sie die Datei kopieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> Geben Sie die ID der Datei ein, die Sie kopieren möchten (zuordnen).</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL The name of the copy file]</p> </td> 
   <td> <p>Geben Sie den neuen Dateinamen ein, wenn er am Zielspeicherort geändert werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File]

Löscht eine angegebene Datei.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Team Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> Geben Sie die ID der Datei ein, die Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File to Trash]

Verschiebt eine angegebene Datei in den Papierkorb.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Team Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> Geben Sie die ID der Datei ein, die Sie in den Papierkorb verschieben möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a File]

Ruft Details zur angegebenen Datei ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Team Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] Zu formatierende Dateien] </td> 
   <td> <p>Wählen Sie das Format aus, in das die [!DNL Google Documents] konvertiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Sheets] Zu formatierende Dateien] </td> 
   <td> <p>Wählen Sie das Format aus, in das die [!DNL Google Sheets] konvertiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] Zu formatierende Dateien] </td> 
   <td> <p>Wählen Sie das Format aus, in das die [!DNL Google Slides] konvertiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] Zu formatierende Dateien] </td> 
   <td> <p>Wählen Sie das Format aus, in das die [!DNL Google Drawings] konvertiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> Geben Sie die ID der Datei ein, die Sie abrufen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a File List]

Ruft Dateien- und/oder Ordnerdetails basierend auf dem Suchbegriff ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Team Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> Wählen Sie das freigegebene Laufwerk aus, dessen Dateien aufgelistet werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den Ordner aus, aus dem Sie Dateien auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Wählen Sie die Art der Suche aus, die Sie durchführen möchten - siehe unten.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Query]</p> </td> 
   <td> 
    <ul> 
     <li style="font-weight: bold;"> <p>[!UICONTROL Search within file names]</p> <p style="font-weight: normal;">Geben Sie den Dateinamen (einschließlich der Dateierweiterung) ein, wenn die Option [!UICONTROL Search for exact term Search] ausgewählt ist, oder geben Sie den Teil des Namens ein, wenn die Option [!UICONTROL Search for names containing the searched term] ausgewählt ist.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Fulltext search]</p> <p>Geben Sie den Suchbegriff ein, um die Dateinamen, Beschreibungen und Inhalte zu durchsuchen.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Custom search query]</p> <p>Geben Sie den [!DNL Google] Suchabfragebegriff ein. Weitere Informationen finden Sie in der [!DNL Google]-<a href="https://developers.google.com/drive/api/v2/ref-search-terms"> (Dokumentation zu Suchanfragen</a>. Beispiel: <code>fullText contains '"Hello world"'</code></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Retrieve]</td> 
   <td>Wählen Sie aus, ob Sie Dateien, Ordner oder beides abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Dateien oder Ordnern fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

Erstellt einen neuen Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Team Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> Wählen Sie das freigegebene Laufwerk aus, auf dem Sie einen Ordner erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den Ordner aus, in dem Sie einen Ordner erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the new folder]</td> 
   <td> <p> Geben Sie den Namen des neuen Ordners ein.</p> </td> 
  </tr> 
 </tbody> 
</table>
