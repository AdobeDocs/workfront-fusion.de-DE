---
title: Google Slides-Module
description: Mit den Adobe Workfront Fusion Google-Folien-Modulen können Sie Präsentationen erstellen, aktualisieren, auflisten und/oder löschen und Bilder in Präsentationen in Ihr Google-Folien-Konto hochladen.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2031'
ht-degree: 0%

---

# [!DNL Google Slides]

Mit den Adobe Workfront Fusion [!DNL Google Slides]-Modulen können Sie Präsentationen erstellen, aktualisieren, auflisten und/oder löschen und Bilder in Präsentationen in Ihrem [!DNL Google Slides]-Konto hochladen.

Um [!DNL Google Slides] mit Workfront Fusion verwenden zu können, benötigen Sie ein [!DNL Google]. Wenn Sie noch kein [!DNL Google] Konto haben, können Sie eines auf der Hilfeseite zum [!DNL Google] Konto erstellen.

Außerdem benötigen Sie [!DNL Google Slides] in Ihrem [!DNL Google Drive].

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung</p>
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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

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
* [Sonstiges](#other)

### Präsentation

* [[!UICONTROL Hinzufügen/Löschen einer Folie]](#adddelete-a-slide)
* [[!UICONTROL Erstellen einer Präsentation aus einer Vorlage]](#create-a-presentation-from-a-template)
* [[!UICONTROL Abrufen einer Seite/Miniaturansicht]](#get-a-pagethumbnail)
* [[!UICONTROL Präsentation abrufen]](#get-a-presentation)
* [[!UICONTROL Präsentationen auflisten]](#list-presentations)
* [[!UICONTROL Aktualisieren eines Diagramms]](#refresh-a-chart)
* [[!UICONTROL Laden Sie ein Bild in eine Präsentation hoch]](#upload-an-image-to-a-presentation)
* [[!UICONTROL Präsentationen ansehen]](#watch-presentations)

#### [!UICONTROL Hinzufügen/Löschen einer Folie]

Dieses Aktionsmodul erstellt eine Folie oder löscht eine vorhandene Folie in der angegebenen Präsentation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methode auswählen]</td> 
   <td> <p>Wählen Sie aus, ob Sie eine neue Folie hinzufügen oder eine Folie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Enter a Slide ID]</td> 
   <td> <p>Wenn Sie eine Folie löschen, wählen Sie aus, ob Sie die Folie-ID manuell eingeben möchten oder die Folie aus einer Liste auswählen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Presentation ID]</td> 
   <td> <p>Wählen Sie die Präsentation aus oder ordnen Sie die Präsentations-ID der Präsentation zu, für die Sie eine Folie hinzufügen oder löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Slide Object ID]</td> 
   <td> <p>Wenn Sie eine Folie löschen und die Folie manuell eingeben möchten, geben Sie die Folien-ID ein oder ordnen Sie sie zu. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL vordefinierter Layouttyp]</td> 
   <td> <p> Wählen Sie das vordefinierte Folien-Layout aus, das die hinzugefügte Folie verwenden soll. Geben Sie Werte für alle zusätzlichen Felder an (z. B. [!UICONTROL Title]).</p> 
    <ul> 
     <li>[!UICONTROL Leeres Layout, ohne Platzhalter]</li> 
     <li>[!UICONTROL Layout mit einer Beschriftung am unteren Rand]</li> 
     <li>[!UICONTROL Layout mit Titel und Untertitel]</li> 
     <li>[!UICONTROL Layout mit Titel und Textkörper]</li> 
     <li>[!UICONTROL Layout mit einem Titel und zwei Spalten]</li> 
     <li>[!UICONTROL Layout mit nur einem Titel]</li> 
     <li>[!UICONTROL Layout mit Abschnittstitel]</li> 
     <li>[!UICONTROL Layout mit Titel und Untertitel auf der einen Seite und Beschreibung auf der anderen Seite]</li> 
     <li>[!UICONTROL-Layout mit einem Titel und einem Hauptteil, in einer einzigen Spalte angeordnet]</li> 
     <li>[!UICONTROL Layout mit einem Hauptpunkt]</li> 
     <li>[!DNL Layout with a big number heading]</li> 
    </ul> <p>Dieses Feld ist verfügbar, wenn Sie eine Folie hinzufügen ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Content]</td> 
   <td> <p>Geben Sie den Textinhalt für die Folie ein oder ordnen Sie ihn zu. Felder sind je nach ausgewählter Vorlage verfügbar.</p> <p>Dieses Feld ist verfügbar, wenn Sie eine Folie hinzufügen ausgewählt haben.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen einer Präsentation aus einer Vorlage]

Dieses Aktionsmodul erstellt eine neue Präsentation, indem es eine Präsentation kopiert und alle Tags wie `{{Name}}` ersetzt, `{{Email}}` mit den bereitgestellten Daten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Titel] </td> 
   <td> <p>Geben Sie einen Namen für die neue Präsentation ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Präsentation kopieren]</td> 
   <td> <p> Wählen Sie die Option, wenn Sie eine vorhandene Präsentation kopieren:</p> 
    <ul> 
     <li>[!UICONTROL nach Zuordnung]</li> 
     <li>[!UICONTROL nach Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kopie der vorhandenen Präsentations-ID]</td> 
   <td> <p> Geben Sie den Pfad oder die Präsentations-ID einer vorhandenen Präsentation ein, die Sie kopieren möchten. Dieses Feld wird angezeigt, wenn Sie die Präsentation erstellen [!UICONTROL By Mapping].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der sich die aufzulistenden Präsentationen befinden:</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
     <li>[!UICONTROL [!DNL Google] freigegebenes Laufwerk]</li> 
    </ul> <p>Dieses Feld wird angezeigt, wenn Sie die Präsentation erstellen [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Präsentations-ID]</td> 
   <td> <p> Wählen Sie die Präsentation aus oder geben Sie die Präsentations-ID der Präsentation ein, die Sie als Vorlage verwenden möchten, oder mappen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Werte] </td> 
   <td> <p>Fügen Sie die Werte hinzu:</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong>: Geben Sie den Tag ein, den Sie in der Präsentation ersetzen möchten. Beispiel: <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[!UICONTROL Replaced Value]</strong>: Geben Sie den Wert ein, durch den das vorhandene Tag ersetzt werden soll. Wenn beispielsweise eine Zeichenfolge in der Präsentation <code>&#123;&#123;Name&#125;&#125;</code> und der ersetzte Wert Sample ist, wird die <code>&#123;&#123;Name&#125;&#125;</code> durch <code>Sample</code> ersetzt.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL neuer Laufwerkspeicherort]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der Sie die neue Präsentation speichern oder hinzufügen möchten:</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
     <li>[!UICONTROL [!DNL Google] freigegebenes Laufwerk]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Speicherort des neuen Dokuments]</p> </td> 
   <td> <p>Wählen Sie den Ordner aus, in dem Sie die Präsentation speichern oder hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Präsentation freigeben möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Freigabe für E-Mail-Adresse anderer Benutzer]</td> 
   <td> <p> Geben Sie die E-Mail-Adresse ein, mit der Sie die Präsentation teilen möchten. Wenn Sie die Option Freigegeben aktivieren, ohne eine E-Mail in dieses Feld einzugeben, kann die Präsentation für alle freigegeben werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Abrufen einer Seite/Miniaturansicht]

Dieses Aktionsmodul ruft die neueste Version der angegebenen Seite oder der Miniaturansicht einer Seite in der Präsentation ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Eine Präsentation und Seiten-ID eingeben]</td> 
   <td> <p> Wählen Sie aus, ob Sie eine Präsentation und Seiten-ID manuell eingeben möchten, oder wählen Sie sie aus einer Liste aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Präsentations-ID]</td> 
   <td> <p> Wählen Sie die Präsentations-ID aus, die Sie abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seitenobjekt-ID]</td> 
   <td> <p> Wählen Sie die Folie aus, für die Sie die Details des Seitenobjekts anzeigen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seitenminiaturansicht anzeigen]</td> 
   <td> <p> Aktivieren Sie das Kontrollkästchen, wenn Sie die Informationen über die Miniaturansicht der Seite anzeigen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Präsentation abrufen]

Dieses Aktionsmodul ruft die neueste Version einer angegebenen Präsentation ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der sich die aufzulistenden Präsentationen befinden:</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
     <li>[!UICONTROL [!DNL Google] freigegebenes Laufwerk]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Präsentations-ID]</td> 
   <td> <p> Wählen Sie die Präsentation aus, die Sie abrufen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Präsentationen auflisten]

Dieses Modul ruft eine Liste aller Präsentationen am angegebenen Ort ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Speicherort des Laufwerks auswählen]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der sich die aufzulistenden Präsentationen befinden:</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
     <li>[!UICONTROL [!DNL Google] freigegebenes Laufwerk]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID]</td> 
   <td> <p>Wählen Sie den Ordnerspeicherort der Präsentationen aus, die Sie auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Präsentationen ein, die das Modul während eines Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren eines Diagramms]

Dieses Aktionsmodul aktualisiert die Diagrammdaten, die in einer durch die ID angegebenen Präsentation gespeichert sind.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Präsentations-ID eingeben]</td> 
   <td> <p> Wählen Sie aus, ob Sie eine Präsentations-ID manuell eingeben oder aus einer Liste auswählen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wenn Sie die Präsentation aus einer Liste auswählen, wählen Sie die [!DNL Google Drive] aus, in der sich die Präsentationen befinden, die Sie auflisten möchten:</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
     <li>[!UICONTROL [!DNL Google] freigegebenes Laufwerk]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Präsentations-ID]</td> 
   <td> <p>Wählen Sie die Präsentation aus oder geben Sie die Präsentations-ID der Präsentation ein bzw. mappen Sie sie, die das Diagramm enthält, das Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Diagrammobjekt-ID]</td> 
   <td> <p> Wenn Sie Daten manuell eingeben, geben Sie die ID des Diagramms ein, das Sie aktualisieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Laden Sie ein Bild in eine Präsentation hoch]

Lädt ein Bild mit den bereitgestellten Daten hoch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Präsentation wählen]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Präsentation auswählen möchten, in die Sie ein Bild hochladen.</p> 
    <ul> 
     <li>[!UICONTROL nach Zuordnung]</li> 
     <li>[!DNL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wenn Sie aus einem Dropdown-Menü auswählen, wählen Sie die [!DNL Google Drive] aus, in der sich die Präsentation befindet, der Sie ein Bild hinzufügen möchten:</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
     <li>[!UICONTROL [!DNL Google] freigegebenes Laufwerk]</li> 
    </ul>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Präsentations-ID]</td> 
   <td> <p> Wählen Sie die Präsentations-ID der Präsentation aus, in die Sie ein Bild hochladen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methode auswählen]</td> 
   <td> <p> Wählen Sie aus, wie Sie das Bild ersetzen möchten.</p>
   <ul>
   <li><p><b>Laden Sie ein Bild hoch, indem Sie das Text-Tag ersetzen</b></p><p>Klicken Sie im Feld Werte für jedes Bild, das Sie hochladen möchten, auf <b>Element hinzufügen</b> und geben Sie den Tag des Bildes und die URL des neuen Bildes ein.</p></li>
   <li><p><b>Bild durch Ersetzen hochladen</b></p><p>Klicken Sie im Feld Werte für jedes Bild, das Sie hochladen möchten, auf <b>Element hinzufügen</b> und geben Sie die Objekt-ID, die Ersetzungsmethode und die URL des neuen Bildes ein.</p></li>
   </ul>
  <p>Hinweis: Die Bilder müssen kleiner als 50 MB sein, dürfen 25 Megapixel nicht überschreiten und müssen im PNG-, JPEG- oder GIF-Format vorliegen.</p>   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Präsentationen ansehen]

Dieses Trigger-Modul startet ein Szenario, wenn eine neue Präsentation erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Uhr] </td> 
   <td> <p>Wählen Sie die Option aus, um die Präsentationen anzusehen:</p> 
    <ul> 
     <li> <p>[!UICONTROL Erstellungsdatum]</p> </li> 
     <li> <p>[!UICONTROL Änderungsdatum]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Präsentationen ein, die Workfront Fusion während eines Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

* [[!UICONTROL Einfügen von Links in eine Präsentation]](#insert-links-in-a-presentation)
* [[!UICONTROL Erstellen eines API-Aufrufs]](#make-an-api-call)

#### [!UICONTROL Einfügen von Links in eine Präsentation]

Dieses Modul macht alle Links in einer Präsentation klickbar oder fügt einen Link in alle passenden Eingabetexte ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Präsentation wählen]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Präsentation auswählen möchten, in die Sie ein Bild hochladen.</p> 
    <ul> 
     <li>[!UICONTROL nach Zuordnung]</li> 
     <li>[!UICONTROL nach Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie die [!DNL Google Drive] aus, in der sich die aufzulistenden Präsentationen befinden:</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
     <li>[!UICONTROL [!DNL Google] freigegebenes Laufwerk]</li> 
    </ul> <p>Dieses Feld wird angezeigt, wenn Sie die Präsentation erstellen [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Präsentations-ID]</td> 
   <td> <p>Wählen Sie den Ordnerspeicherort der Präsentationen aus, die Sie auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL select]</td> 
   <td> <p>Wählen Sie aus, ob alle Links in einer Präsentation klickbar sein sollen oder ob Sie einen Link in alle Übereinstimmungseingabetexte einfügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Texteingaben]</td> 
   <td>Wenn Sie einen Link einfügen, klicken Sie für jedes Textelement, für das Sie einen Link hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Text und den zugehörigen Link ein. Jedes Mal, wenn das Element in der Präsentation angezeigt wird, wird es automatisch mit der angegebenen Site verknüpft.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen eines API-Aufrufs]

Führt einen beliebigen autorisierten API-Aufruf aus.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Slides]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://developers.google.com/slides/</code> ein. z. B. Präsentation.</p> <p>Eine Liste der verfügbaren Endpunkte finden Sie in der <a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides] API-Dokumentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Geben Sie die gewünschten Anfrage-Header ein. Sie müssen keine Autorisierungskopfzeilen hinzufügen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p> Geben Sie die Abfragezeichenfolge der Anfrage ein.</p> </td> 
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

>[!BEGINSHADEBOX]

**Beispiel** Mithilfe eines API-Aufrufs können Sie die Präsentationsdetails für die eingegebene Präsentations-ID abrufen. Die Präsentations-ID finden Sie in der URL, wenn Sie die Präsentation in [!DNL Google Slides] öffnen.

![Beispiel für einen API-Aufruf](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)

Der folgende API-Aufruf gibt die Präsentationsdetails zurück:

![Präsentationsdetails](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)

Treffer der Suche finden Sie in der Modulausgabe unter [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL presentationId].

In unserem Beispiel wurden die angeforderten Präsentationsdetails zurückgegeben:

![Präsentationsdetails](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

>[!ENDSHADEBOX]
