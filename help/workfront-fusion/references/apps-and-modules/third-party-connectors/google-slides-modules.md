---
title: Google Slides-Module
description: Mit den Adobe Workfront Fusion Google-Folien-Modulen können Sie Präsentationen erstellen, aktualisieren, auflisten und/oder löschen und Bilder in Präsentationen in Ihr Google-Folien-Konto hochladen.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 0%

---

# [!DNL Google Slides]

Mit den [!DNL Adobe Workfront Fusion] [!DNL Google Slides]-Modulen können Sie Präsentationen erstellen, aktualisieren, auflisten und/oder löschen und Bilder in Präsentationen in Ihrem [!DNL Google Slides]-Konto hochladen.

Um [!DNL Google Slides] mit [!DNL Workfront Fusion] verwenden zu können, muss ein [!DNL Google] Konto vorhanden sein. Wenn Sie noch kein [!DNL Google] Konto haben, können Sie eines auf der Hilfeseite zum [!DNL Google] Konto erstellen.

Außerdem benötigen Sie [!DNL Google Slides] in Ihrem [!DNL Google Drive].

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

Um [!DNL Google Slides]-Module verwenden zu können, müssen Sie über ein [!DNL Google]-Konto verfügen.

## Informationen zur Google Slides-API

Der Google Slides-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://slides.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.5.9</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Slides] Module und ihre Felder

Beim Konfigurieren von [!DNL Google Slides] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Google Slides] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Präsentation](#presentation)
* [Sonstige](#other)

### Präsentation

* [[!UICONTROL Watch Presentations]](#watch-presentations)
* [[!UICONTROL List Presentations]](#list-presentations)
* [[!UICONTROL Get a Presentation]](#get-a-presentation)
* [[!UICONTROL Get a Page/Thumbnail]](#get-a-pagethumbnail)
* [[!UICONTROL Create a Presentation From a Template]](#create-a-presentation-from-a-template)
* [[!UICONTROL Upload an Image To a Presentation]](#upload-an-image-to-a-presentation)
* [[!UICONTROL Refresh a Chart]](#refresh-a-chart)
* [[!UICONTROL Add/Delete a Slide]](#adddelete-a-slide)

#### [!UICONTROL Watch Presentations]

Trigger beim Erstellen oder Aktualisieren einer neuen Präsentation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch] </td> 
   <td> <p>Wählen Sie die Option aus, um die Präsentationen anzusehen:</p> 
    <ul> 
     <li> <p>[!UICONTROL Created Date]</p> </li> 
     <li> <p>[!UICONTROL Modified Date]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Die maximale Anzahl von Präsentationen, die Workfront Fusion während eines Szenario-Ausführungszyklus zurückgeben sollte.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Presentations]

Ruft eine Liste aller Präsentationen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive location]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der sich die aufzulistenden Präsentationen befinden:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Freigegebenes Laufwerk</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p>Wählen Sie den Ordnerspeicherort der Präsentationen aus, die Sie auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Die maximale Anzahl von Präsentationen, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben sollten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Presentation]

Ruft die neueste Version einer angegebenen Präsentation ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der sich die aufzulistenden Präsentationen befinden:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Freigegebenes Laufwerk</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Wählen Sie die Präsentation aus, die Sie abrufen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Page/Thumbnail]

Ruft die neueste Version der angegebenen Seite oder der Miniaturansicht einer Seite in der Präsentation ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Wählen Sie die Präsentations-ID aus, die Sie abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page Object ID]</td> 
   <td> <p> Wählen Sie die Folie aus, für die Sie die Details des Seitenobjekts anzeigen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Page Thumbnail]</td> 
   <td> <p> Aktivieren Sie das Kontrollkästchen, wenn Sie die Informationen über die Miniaturansicht der Seite anzeigen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Presentation From a Template]

Erstellt eine neue Präsentation, indem alle Tags wie `{{Name}}`, `{{Email}}` in einer Vorlage, durch die bereitgestellten Daten ersetzt werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>Geben Sie einen Namen für die neue Präsentation ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy a Presentation]</td> 
   <td> <p> Wählen Sie die Option, wenn Sie eine vorhandene Präsentation kopieren:</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy of Existing Presentation ID]</td> 
   <td> <p> Geben Sie den Pfad oder die Präsentations-ID einer vorhandenen Präsentation ein, die Sie kopieren möchten. Dieses Feld wird angezeigt, wenn Sie die [!UICONTROL By Mapping] erstellen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der sich die aufzulistenden Präsentationen befinden:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Freigegebenes Laufwerk</li> 
    </ul> <p>Dieses Feld wird angezeigt, wenn Sie die [!UICONTROL By Dropdown] erstellen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Wählen Sie die Präsentations-ID der Präsentation aus, die Sie als Vorlage verwenden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values] </td> 
   <td> <p>Fügen Sie die Werte hinzu:</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong>: Geben Sie das Tag ein, das Sie in der Präsentation ersetzen möchten. Beispiel: <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[!UICONTROL Replaced Value]</strong>: Geben Sie den Wert ein, durch den das vorhandene Tag ersetzt werden soll. Beispiel: Wenn eine Zeichenfolge <tr><ul><tr><tr><tr><code>&#123;&#123;Name&#125;&#125;/code> in the presentation and the replaced value is Sample, then the <code>&#123;&#123;Name&#125;&#125;</code> will be replaced by <code>Sample</code>.</li> 
    </ul> </td> 
  </tr> 
   
   <td role="rowheader">[!UICONTROL New Drive Location]</td> 
   <td> <p>Select the [!DNL Google Drive] where you want to store or add the new presentation:</p> 
     
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Shared Drive]</li> 
    </ul> </td> 
  </tr> 
   
   <td role="rowheader"> <p>[!UICONTROL New Document's Location]</p> </td> 
   <td> <p>Select the folder where you want to store or add the presentation.</p> </td> 
  </tr> 
   
   <td role="rowheader">[!UICONTROL Shared] </td> 
   <td> <p>Select if you want to share the presentation.</p> </td> 
  </tr> 
   
   <td role="rowheader">[!UICONTROL Sharing with Other's Email Address]</td> 
   <td> <p> Enter the email address with whom you want to share the presentation. If you are not entering an email address and selecting only shared field, the presentation is shareable to anyone.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an Image To a Presentation]

Lädt ein Bild mit den bereitgestellten Daten hoch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Presentation]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Präsentation auswählen möchten, in die Sie ein Bild hochladen.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!DNL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der sich die aufzulistenden Präsentationen befinden:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Freigegebenes Laufwerk</li> 
    </ul> <p>Dieses Feld wird angezeigt, wenn Sie die [!UICONTROL By Dropdown] erstellen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Wählen Sie die Präsentations-ID der Präsentation aus, in die Sie ein Bild hochladen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>Werte Fügen Sie die Werte hinzu:</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong>: Geben Sie das Tag ein, dem Sie die URL hinzufügen möchten.</li> 
     <li><strong>[!UICONTROL Image URL]</strong>: Geben Sie den Pfad oder die URL für das Bild ein, das Sie hochladen möchten.</li> 
    </ul> <p>Hinweis: Die Bilder müssen kleiner als 50 MB sein, dürfen 25 Megapixel nicht überschreiten und müssen im PNG-, JPEG- oder GIF-Format vorliegen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Refresh a Chart]

Aktualisiert die Diagrammdaten, die in einer durch die ID festgelegten Präsentation gespeichert sind

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der sich die aufzulistenden Präsentationen befinden:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Freigegebenes Laufwerk</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Wählen Sie die Präsentations-ID der Präsentation aus, die das Diagramm enthält, das Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Chart Object ID]</td> 
   <td> <p> Wählen Sie das Diagramm aus, das Sie aktualisieren möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add/Delete a Slide]

Erstellt eine leere Folie oder löscht eine vorhandene Folie in der angegebenen Präsentation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the method]</td> 
   <td> <p>Wählen Sie aus, ob Sie eine neue Folie hinzufügen oder eine Folie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Presentation ID]</td> 
   <td> <p>Wählen Sie die Präsentations-ID der Präsentation aus, für die Sie eine Folie hinzufügen oder löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Predefined layout type]</td> 
   <td> <p> Wählen Sie das vordefinierte Folien-Layout aus, das die hinzugefügte Folie verwenden soll. Geben Sie Werte für alle zusätzlichen Felder an (z. B. [!UICONTROL Title]).</p> 
    <ul> 
     <li>[!UICONTROL Blank layout, with no placeholders]</li> 
     <li>[!UICONTROL Layout with a caption at the bottom]</li> 
     <li>[!UICONTROL Layout with a title and subtitle]</li> 
     <li>[!UICONTROL Layout with a title and body]</li> 
     <li>[!UICONTROL Layout with a title and two columns]</li> 
     <li>[!UICONTROL Layout with only a title]</li> 
     <li>[!UICONTROL Layout with a section title]</li> 
     <li>[!UICONTROL Layout with a title and subtitle on one side and description on the other]</li> 
     <li>[!UICONTROL Layout with one title and one body, arranged in a single column]</li> 
     <li>[!UICONTROL Layout with a main point]</li> 
     <li>[!DNL Layout with a big number heading]</li> 
    </ul> <p>Dieses Feld ist verfügbar, wenn Sie eine Folie hinzufügen ausgewählt haben.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstige

* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Insert Links in a Presentation]](#insert-links-in-a-presentation)

#### [!UICONTROL Make an API Call]

Führt einen beliebigen autorisierten API-Aufruf aus.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Geben Sie einen Pfad relativ zu https://developers.google.com/slides/ ein. z. B. Präsentation.</p> <p>Eine Liste der verfügbaren Endpunkte finden Sie in der <a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides] API-Dokumentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Geben Sie die gewünschten Anfrage-Header ein. Sie müssen keine Autorisierungskopfzeilen hinzufügen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Geben Sie die Abfragezeichenfolge der Anfrage ein.</p> </td> 
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

>[!INFO]
>
>**Beispiel** Mithilfe eines API-Aufrufs können Sie die Präsentationsdetails für die eingegebene Präsentations-ID abrufen. Die Präsentations-ID finden Sie in der URL, wenn Sie die Präsentation in [!DNL Google Slides] öffnen.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)
>
>Der folgende API-Aufruf gibt die Präsentationsdetails zurück:
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)
>
>Treffer der Suche finden Sie in der Modulausgabe unter [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL presentationId].
>
>In unserem Beispiel wurden die angeforderten Präsentationsdetails zurückgegeben:
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

#### [!UICONTROL Insert Links in a Presentation]

Dieses Modul macht alle Links in einer Präsentation klickbar oder fügt einen Link in alle passenden Eingabetexte ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Presentation]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Präsentation auswählen möchten, in die Sie ein Bild hochladen.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der sich die aufzulistenden Präsentationen befinden:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Freigegebenes Laufwerk</li> 
    </ul> <p>Dieses Feld wird angezeigt, wenn Sie die [!UICONTROL By Dropdown] erstellen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Wählen Sie den Ordnerspeicherort der Präsentationen aus, die Sie auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select]</td> 
   <td> <p>Wählen Sie aus, ob alle Links in einer Präsentation klickbar sein sollen oder ob Sie einen Link in alle Übereinstimmungseingabetexte einfügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text Inputs]</td> 
   <td>Fügen Sie für jedes Textelement, für das Sie einen Link hinzufügen möchten, das Element sowie den zugehörigen Link zur Liste hinzu. Jedes Mal, wenn das Element in der Präsentation angezeigt wird, wird es automatisch mit der angegebenen Site verknüpft.</td> 
  </tr> 
 </tbody> 
</table>
