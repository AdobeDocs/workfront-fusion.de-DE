---
title: Google-Laufwerkmodule
description: Mit  [!DNL Adobe Workfront Fusion Google Drive]  Modulen können Sie Ihre Dateien, Ordner oder freigegebenen Laufwerke in Ihrem überwachen, suchen, erstellen, aktualisieren, löschen und verwalten [!DNL Google Drive].
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 0%

---

# [!DNL Google Drive]

Mit den [!DNL Adobe Workfront Fusion] [!DNL Google Drive]-Modulen können Sie Ihre Dateien, Ordner oder freigegebenen Laufwerke in Ihrer [!DNL Google Drive] überwachen, suchen, erstellen, aktualisieren, löschen und verwalten.

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Ihr [!DNL Google Drive]-Konto mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Informationen zur Google Drive-API

Der Google Drive-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://www.googleapis.com/drive/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v4.1.22</td> 
  </tr>
 </tbody> 
 </table>



## Verbinden von [!DNL Google Drive] mit [!DNL Workfront Fusion]

Wenn Sie [!DNL @gmail.com] oder [!DNL @googlemail.com] Benutzer verwenden, müssen Sie einen OAuth-Client für den [!DNL Google Cloud Platform] erstellen, um Ihre [!UICONTROL Client-ID] und [!UICONTROL Client-Geheimnis] abzurufen.

Eine schrittweise Anleitung zum Erstellen des OAuth-Clients (und zum Abrufen von [!UICONTROL Client-ID] und [!UICONTROL Client-Geheimnis]) finden Sie unter [Verbinden [!DNL Adobe Workfront Fusion] mit [!DNL Google Services] Verwenden eines benutzerdefinierten OAuth-Clients](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung mit [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL Google Drive] Module und ihre Felder

Beim Konfigurieren [!DNL Google Drive] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Google Drive] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [Auslöser](#triggers)
* [Aktionen](#actions)

### Auslöser

* [[!UICONTROL Alle Dateien ansehen]](#watch-all-files)
* [[!UICONTROL Kommentare ansehen]](#watch-comments)
* [[!UICONTROL Dateien im Ordner ansehen]](#watch-files-in-folder)
* [[!UICONTROL Freigegebene Dateien ansehen]](#watch-shared-files)

#### [!UICONTROL Alle Dateien ansehen]

Dieses Dateimodul startet ein Szenario, wenn eine Trigger in Ihrem [!DNL Google Drive] hinzugefügt oder geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Welche Dateien beobachtet werden]</td> 
   <td> <p>Wählen Sie aus, welchen Dateityp Sie beobachten möchten.</p> 
    <ul> 
     <li>[!UICONTROL ALL]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL [!DNL Google Documents] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Documents] konvertieren möchten.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Spreadsheets] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Spreadsheets] konvertieren möchten.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Slides] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Slides] konvertieren möchten.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Drawings] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Drawings] konvertieren möchten.</td>
  </tr>  
  <tr> 
   <td>[!UICONTROL Uhr]</td> 
   <td>Wählen Sie aus, ob neue Dateien und alle Änderungen oder nur neue Dateien angesehen werden sollen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl heruntergeladener Dateien]</td> 
   <td>Legen Sie die maximale Anzahl von Ergebnissen fest, die [!DNL Workfront Fusion] während eines Zyklus herunterladen (die Anzahl der Wiederholungen pro Szenario-Ausführung).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kommentare ansehen]

Dieses Trigger-Modul startet ein Szenario, wenn ein Kommentar zur ausgewählten Datei hinzugefügt oder geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Datei]</td> 
   <td>Wählen Sie die Datei aus, die auf Kommentare überwacht werden soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Uhr]</td> 
   <td>Wählen Sie aus, ob Sie alle Änderungen oder nur neue Kommentare überwachen möchten</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Kommentare]</td> 
   <td>Legen Sie die maximale Anzahl von Kommentaren fest, die [!DNL Workfront Fusion] während eines Zyklus zurückgeben (die Anzahl der Wiederholungen pro Szenario-Durchgang).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dateien im Ordner ansehen]

Dieses Ordnermodul startet ein Trigger-Szenario, wenn eine Datei im angegebenen Ordner hinzugefügt oder geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL-Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Wählen Sie den zu überwachenden Ordner aus]</td>
    <td >Wählen Sie den Ordner auf Ihrem Laufwerk aus, in dem die Dateien überwacht werden sollen.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Welche Dateien beobachtet werden]</td>
   <td> <p>Wählen Sie aus, welchen Dateityp Sie beobachten möchten.</p> 
    <ul> 
     <li>[!UICONTROL ALL]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL [!DNL Google Documents] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Documents] konvertieren möchten.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Spreadsheets] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Spreadsheets] konvertieren möchten.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Slides] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Slides] konvertieren möchten.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Drawings] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Drawings] konvertieren möchten.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Uhr]</td>
    <td>Wählen Sie aus, ob neue Dateien und alle Änderungen oder nur neue Dateien angesehen werden sollen.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Maximale Anzahl heruntergeladener Dateien]</td>
    <td>Legen Sie die maximale Anzahl von Ergebnissen fest, die [!DNL Workfront Fusion] während eines Zyklus herunterladen (die Anzahl der Wiederholungen pro Szenario-Ausführung).</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Freigegebene Dateien ansehen]

Trigger, wenn eine neue Datei für Sie freigegeben oder eine vorhandene freigegebene Datei aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Wählen Sie den zu überwachenden Ordner aus]</td> 
   <td>Wählen Sie den freigegebenen Ordner aus, in dem die Dateien überwacht werden sollen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Welche Dateien beobachtet werden]</td> 
   <td> <p>Wählen Sie aus, welchen Dateityp Sie beobachten möchten.</p> 
    <ul> 
     <li>[!UICONTROL ALL]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL [!DNL Google Documents] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Documents] konvertieren möchten.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Spreadsheets] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Spreadsheets] konvertieren möchten.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Slides] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Slides] konvertieren möchten.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Drawings] Dateien ins Format konvertieren]</td>
    <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Drawings] konvertieren möchten.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Uhr]</td> 
   <td>Wählen Sie aus, ob neue Dateien und alle Änderungen oder nur neue Dateien angesehen werden sollen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl heruntergeladener Dateien]</td> 
   <td>Legen Sie die maximale Anzahl von Ergebnissen fest, die [!DNL Workfront Fusion] während eines Zyklus herunterladen (die Anzahl der Wiederholungen pro Szenario-Ausführung).</td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Kopieren einer Datei]](#copy-a-file)
* [[!UICONTROL Erstellen eines fFolder]](#create-a-folder)
* [[!UICONTROL Datei löschen]](#delete-a-file)
* [[!UICONTROL Datei abrufen]](#get-a-file)
* [[!UICONTROL Link freigeben]](#get-a-share-link)
* [[!UICONTROL Verschieben einer Datei in den Papierkorb]](#move-a-filefolder-to-trash)
* [[!UICONTROL Suchen nach Dateien/Ordnern]](#search-for-filesfolders)
* [[!UICONTROL Aktualisieren einer Datei]](#update-a-file)
* [[!UICONTROL Datei hochladen]](#upload-a-file)

#### [!UICONTROL Kopieren einer Datei]

Dieses Aktionsmodul kopiert eine Datei an den neuen Speicherort.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ziel]</td> 
   <td> <p>Wählen Sie das Ziel aus, in das Sie eine Datei kopieren möchten.</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zielordner]</td> 
   <td>Wählen Sie den Ordner aus, der die Datei enthält, die Sie kopieren möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datei-ID]</td> 
   <td>Ordnen Sie die ID der Datei zu, die Sie kopieren möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Der Name der Kopie]</td> 
   <td>Geben Sie einen Titel für die neue Datei ein. Lassen Sie dieses Feld leer, wenn Sie den ursprünglichen Dateinamen nicht ändern möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen eines Ordners]

Dieses Aktionsmodul erstellt einen Ordner am angegebenen Speicherort.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ziel]</td> 
   <td> <p>Wählen Sie das Ziel aus, an dem Sie einen Ordner erstellen möchten.</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Speicherort des neuen Ordners]</td> 
   <td>Navigieren Sie zu der Position, an der Sie einen neuen Ordner erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Der Name des neuen Ordners]</td> 
   <td>Geben Sie einen Namen für den Ordner ein, den Sie erstellen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Freigabeordner]</td> 
   <td>Wählen Sie diese Option aus, wenn Sie den Ordner für alle mit dem Link [!UICONTROL Share] freigeben möchten. Andernfalls ist der Freigabe-Link nur für den Eigentümer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei löschen]

Dieses Aktionsmodul löscht dauerhaft eine Datei oder einen Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datei-ID]</td> 
   <td>Ordnen Sie die ID der Datei zu, die Sie löschen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei abrufen]

Dieses Aktionsmodul ruft die Datei mit der angegebenen ID ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Documents] Dateien ins Format konvertieren]</td> 
   <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Documents] konvertieren möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Spreadsheets] Dateien ins Format konvertieren]</td> 
   <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Spreadsheets] konvertieren möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Slides] Dateien ins Format konvertieren]</td> 
   <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Slides] konvertieren möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Drawings] Dateien ins Format konvertieren]</td> 
   <td>Wählen Sie das Dateiformat aus, in das Sie [!DNL Google Drawings] konvertieren möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datei-ID]</td> 
   <td>Ordnen Sie die ID der Datei zu, die Sie abrufen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Link freigeben]

Dieses Aktionsmodul ruft den Freigabe-Link für eine Datei in Google Drive ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datei-ID]</td> 
   <td>Ordnen Sie die ID der Datei zu, für die Sie den Freigabe-Link abrufen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Verschieben einer Datei in den Papierkorb]

Dieses Aktionsmodul verschiebt eine Datei oder einen Ordner in den Papierkorb.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datei-ID]</td> 
   <td>Ordnen Sie die ID der Datei zu, die Sie in den Papierkorb verschieben möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Suchen nach Dateien/Ordnern]

Dieses Suchmodul sucht anhand von Suchkriterien nach Dateien oder Ordnern.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ziel]</td> 
   <td> <p>Wählen Sie das zu durchsuchende Ziellaufwerk aus.</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordner auflisten]</td> 
   <td>Navigieren Sie zu dem Ordner, in dem Sie nach den Dateien oder Ordnern suchen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL abrufen]</td> 
   <td> <p> Wählen Sie aus, ob Sie nach Dateien, Ordnern oder beidem suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Suche]</p> </td> 
   <td> <p>Wählen Sie den Typ der Suche aus, die Sie durchführen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Suche innerhalb von Datei-/Ordnernamen]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL-Abfrage]</strong> </p> <p>Geben Sie einen Teil des Dateinamens oder des vollständigen Dateinamens (einschließlich des Suffix) ein, nach dem gesucht werden soll.</p> </li> 
       <li> <p><strong>[!UICONTROL Suchoptionen]</strong> </p> <p>Wählen Sie aus, ob Sie nach dem genauen Begriff suchen möchten oder ob Sie nach Namen suchen möchten, die den Suchbegriff enthalten.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Volltext]-Suche</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL-Abfrage]</strong> </p> <p>Geben Sie einen beliebigen Suchbegriff ein, den Sie in Ihrem [!DNL Google Drive] suchen möchten.</p> </li> 
      </ul> </li> 
     <li> <p><strong>Benutzerdefinierte Suchanfrage eingeben</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL-Abfrage]</strong> </p> <p>Geben Sie die benutzerdefinierte Suchabfrage ein. Weitere Informationen finden Sie im Abschnitt [!UICONTROL Nach Dateien suchen] dieses Artikels.</p> </li> 
       <li> <p><strong>Fügen Sie den oben ausgewählten Ordner zur Abfrage hinzu</strong> </p> <p>Sucht in der übergeordneten Sammlung nach dem Ordner. Dadurch werden alle Dateien und Ordner gefunden, die sich direkt in dem oben ausgewählten Ordner befinden.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</td> 
   <td>Legen Sie die maximale Anzahl von Dateien oder Ordnern fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Die Routenausführung auch dann fortsetzen, wenn das Modul keine Ergebnisse zurückgibt]</td> 
   <td>Aktivieren Sie diese Option, um sicherzustellen, dass das Szenario nicht angehalten wird, wenn das Modul keine Ergebnisse zurückgibt.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren einer Datei]

Dieses Aktionsmodul aktualisiert die Metadaten oder Inhalte einer Datei.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ziel]</td> 
   <td> <p>Wählen Sie das Ziel aus, das die Datei enthält, die Sie aktualisieren möchten.</p> 
    <ul> 
     <li>[!UICONTROL Mein Laufwerk]</li> 
     <li>[!UICONTROL für mich freigegeben]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL In Ordner verschieben]</td> 
   <td>Wenn Sie die Datei in einen bestimmten Ordner verschieben möchten, wählen Sie den Ordner aus, in den Sie die Datei verschieben möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datei-ID]</td> 
   <td>Ordnen Sie die ID der Datei zu, die Sie aktualisieren möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Titel]</td> 
   <td>Geben Sie einen Titel für die aktualisierte Datei ein.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dateiinhalt ändern]</td> 
   <td>Wählen Sie aus, ob Sie den Inhalt der Datei ersetzen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source-Datei]</td> 
   <td>Wenn Sie den Inhalt ersetzen, wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datei konvertieren]</td> 
   <td>Aktivieren Sie diese Option, um die Datei in das entsprechende Google-Dateiformat zu konvertieren.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei hochladen]

Lädt eine Datei in Ihr [!DNL Google Drive] hoch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Drive]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Google Drive] mit [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Destination]</td> 
   <td> <p>Wählen Sie das Ziel aus, an das Sie eine Datei hochladen möchten.</p> 
    <ul> 
     <li>[!DNL My Drive]</li> 
     <li>[!DNL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zielordner]</td> 
   <td>Wählen Sie den Ordner aus, in den Sie eine Datei hochladen möchten. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source-Datei]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Titel]</td> 
   <td>Geben Sie einen Titel für die neue Datei ein.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datei konvertieren]</td> 
   <td>Wenn diese Option aktiviert ist, kann das Modul Dateien in das entsprechende [!DNL Google] konvertieren.</td> 
  </tr> 
 </tbody> 
</table>

## Fehlerbehebung

### Datei kann nicht hochgeladen oder aktualisiert werden

Das Hochladen oder Aktualisieren einer Datei schlägt aus verschiedenen Gründen fehl:

* Die hochgeladene Datei ist zu groß und überschreitet die maximale Dateigröße, die für Ihren [!DNL Google Drive] zulässig ist, oder Sie haben Ihr [!DNL Google Drive] Speicherlimit überschritten. Sie können entweder Ihren Speicherplan aktualisieren oder vorhandene Dateien aus dem [!DNL Google Drive]-Service löschen.
* Der ausgewählte Ordner, in den die Datei hochgeladen werden soll, existiert nicht mehr. In diesem Fall stoppt das Szenario und Sie müssen einen anderen Zielordner im Modul auswählen.

<!-- Not present February 2025

## Search for files

In the module List files in a folder you can use your own query which consists of these parts:

* **[!UICONTROL Field]** - Attribute of the file that is being searched, for example, the attribute `name` of the file.

* **[!UICONTROL Operator]** - Test that is performed on the data to provide a match, for example, `contains`.

* **[!UICONTROL Value]** - The content of the attribute that is tested, for example, the name of the file `My cool document`.

Combine clauses with the conjunctions `and` or `or`, and negate the query with `not`.

* [Fields](#fields)
* [Value types](#value-types)
* [Operators](#operators)
* [Examples](#examples)

### Fields 

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Field </th> 
   <th>Value Type </th> 
   <th>Operators</th> 
   <th> <p> Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>string</td> 
   <td><code>contains</code><sup>1</sup>, <code>=</code>, <code>!=</code></td> 
   <td> <p> Name of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>string </td> 
   <td><code>contains</code><sup>2, 3</sup> </td> 
   <td> <p> Full text of the file including name, description, content, and indexable text.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> string</td> 
   <td><code>contains</code>, <code>=</code>, <code>!=</code></td> 
   <td> <p> MIME type of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code> &lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date of the last modification to the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code>&lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date that the user last viewed a file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Whether the file is in the trash or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>Whether the file is starred or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Whether the [!UICONTROL parents] collection contains the specified ID.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who own the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to modify the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to read the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Files that are in the user's "Shared with me" collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>collection</td> 
   <td><code>has </code> </td> 
   <td> <p> Public custom file properties.</p> </td> 
  </tr> 
 </tbody> 
</table>

Consider the following about operators in these fields:

* The `contains` operator only performs prefix matching for a `title`.

   For example, the title "HelloWorld" matches for `title contains 'Hello'` but not for `title contains 'World'`.

* The `contains` operator only performs matching on entire string tokens for `fullText`.

   For example, if the full text of a doc contains the string "HelloWorld" only the query `fullText contains 'HelloWorld'` returns a result. Queries such as `fullText contains 'Hello'` would not return results in this scenario.

* The `contains` operator matches on an exact alphanumeric phrase if it is surrounded by double quotes.

   For example, if the `fullText` of a doc contains the string "Hello there world", then the query `fullText contains '"Hello there"'` returns a result, but the query `fullText contains '"Hello world"'` does not.

   Furthermore, because the search is alphanumeric, if the `fullText` of a doc contains the string "Hello_world", then the query `fullText contains '"Hello world"'` returns a result.

* Fields of `type` date are currently not comparable to each other, only to constant dates.

### Value types

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Value Type</th> 
   <th> <p> Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>String </td> 
   <td> <p>Surround with single quotes '. Escape single quotes in queries with <code>\'</code>, e.g.,<code> 'Valentine\'s Day'</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolean </td> 
   <td> <p><code>true </code>or <code>false</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td> <p>RFC 3339 format, default timezone is UTC, e.g., <code>2012-06-04T12:00:00-08:00</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Operators

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Operator </th> 
   <th> <p>Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>The content of one string is present in the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> The content of a string or boolean is equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> The content of a string or boolean is not equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> A date is earlier than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> A date is earlier than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> A date is later than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> A date is later than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>An element is contained within a collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>Return files that match both clauses.</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>Return files that match either clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>Negates a search clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>A collection contains an element matching the parameters.</p> </td> 
  </tr> 
 </tbody> 
</table>

For compound clauses, you can use parentheses to group clauses together. For example:
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')` This search returns all files with an image or video MIME type that their last modification was after June 4, 2012. Because `and` and `or` operators are evaluated from left to right, without parentheses, the above example would return only images modified after June 4, 2012, but would return all videos, even those before June 4, 2012.

### Examples 

All examples on this page show the unencoded `<q>q</q>` parameter, where `title = 'hello'` is encoded as `title+%3d+%27hello%27`. Client libraries handle this encoding automatically.

* Search for files with the name "hello"
   <pre>title = 'hello'</pre>
* Search for folders using the folder-specific MIME type
   <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* Search for files that are not folders
   <pre>mimeType != 'application/vnd.google-apps.folder'</pre>
* Search for files with a name containing the words "hello" and "goodbye"
   <pre>title contains 'hello' and [!UICONTROL name] contains 'goodbye'</pre>
* Search for files with a name that does not contain the word "hello"
   <pre>not title contains 'hello'</pre>
* Search for files containing the word "hello" in the content
   <pre>fullText contains 'hello'</pre>
* Search for files not containing the word "hello" in the content
   <pre>not fullText contains 'hello'</pre>
* Search for files containing the exact phrase "hello world" in the content
   <pre>fullText contains '"hello world"'fullText contains '"hello_world"'</pre>
* Search for files with a query containing the "\" character (e.g., "\authors")
   <pre>fullText contains '\\authors'</pre>
* Search for files writeable by the user `test@example.org`
   <pre>'test@example.org' in [!DNL writers]</pre>
* Search for the ID `1234567` in the `parents` collection. This finds all files and folders located directly in the folder whose ID is `1234567`.
   <pre>'1234567' in [!UICONTROL parents]</pre>
* Search for the alias ID `appDataFolder` in the `parents` collection. This finds all files and folders located directly under the [Application Data folder](https://developers.google.com/drive/api/v2/appdata).
   <pre>'appDataFolder' in parents</pre>
* Search for files writeable by the users `test@example.org` and `test2@example.org`
   <pre>'test@example.org' in writers and 'test2@example.org' in writers</pre>
* Search for files containing the text "important" which are in the trash
   <pre>fullText contains 'important' and trashed = true</pre>
* Search for files modified after June 4th 2012
   <pre>modifiedDate > '2012-06-04T12:00:00' // default time zone is UTC</pre><pre>modifiedDate > '2012-06-04T12:00:00-08:00'</pre>
* Search for files shared with the authorized user with "hello" in the name
   <pre>sharedWithMe and title contains 'hello'</pre>
* Search for files with a [custom file property](https://developers.google.com/drive/api/v2/properties) named `additionalID` with the value `8e8aceg2af2ge72e78`.
   <pre>properties has { key='additionalID' and value='8e8aceg2af2ge72e78' and visibility='PRIVATE' }</pre>

Source of this guide is [[!DNL Google Drive] documentation](https://developers.google.com/drive/api/v2/search-shareddrives).

-->
