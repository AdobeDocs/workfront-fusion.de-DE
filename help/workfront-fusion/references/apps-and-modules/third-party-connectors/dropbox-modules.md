---
title: Dropbox-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die Dropbox verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden. Auf diese Weise können Sie Aktivitäten wie das Überwachen, Suchen, Abrufen, Auflisten, Erstellen und Bearbeiten von Dateien und Ordnern in Ihrer Dropbox automatisieren.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 29ce5940-4d71-4719-ab5e-f03c44b28c8c
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '3203'
ht-degree: 0%

---

# [!DNL Dropbox]

In einem [!DNL Adobe Workfront Fusion] können Sie Workflows automatisieren, die [!UICONTROL Dropbox] oder [!DNL Dropbox Business] verwenden, und diese mit mehreren Anwendungen und Services von Drittanbietern verbinden. Auf diese Weise können Sie Aktivitäten wie das Überwachen, Suchen, Abrufen, Auflisten, Erstellen und Bearbeiten von Dateien und Ordnern in Ihrer [!UICONTROL Dropbox] automatisieren.

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

## Voraussetzungen

* Um [!DNL Dropbox]-Module verwenden zu können, müssen Sie über ein [!DNL Dropbox]-Konto verfügen.

>[!IMPORTANT]
>
>Dropbox muss Programme mit mehr als 50 Benutzern genehmigen.
>
>Weitere Informationen finden Sie unter „Produktionsgenehmigung“ im Dropbox-Entwicklerhandbuch.

## Dropbox-API-Informationen

Der Dropbox-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.dropboxapi.com/2    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> 2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td><ul><li><p>Dropbox</p><p>v5.3.9</p></li><li><p>Dropbox Business</p><p>v1.0.12</p></li></ul></td> 
  </tr>
 </tbody> 
 </table>


## Erstellen einer Verbindung zu [!DNL Dropbox]

So erstellen Sie eine Verbindung für Ihre [!DNL Dropbox]:

1. Klicken Sie in einem beliebigen Modul **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
        <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>Wählen Sie aus, ob diese Verbindung für eine Produktions- oder Nicht-Produktionsumgebung vorgesehen ist.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</td>
        </tr>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre [!UICONTROL Dropbox] [!UICONTROL Client-ID] ein. </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihren [!DNL Dropbox] [!UICONTROL Client Secret] ein. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Kontotyp]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einem persönlichen Dropbox-Konto oder einem Geschäftskonto (Dropbox Business) herstellen möchten.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL exclude dropbox-api-path-root header]</td>
        <td>Aktivieren Sie diese Option, um die Kopfzeile „dropbox-api-path-root“ für Dropbox-Apps mit Zugriff auf den Programmordner auszuschließen</td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.## [!DNL Dropbox] Module und ihre Felder

## [!DNL Dropbox] Module und ihre Felder

Beim Konfigurieren [!DNL Dropbox] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Dropbox] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger-Module](#trigger-modules)
* [Module zum Abrufen von  [!DNL Dropbox]  und Ordnern](#modules-for-getting-dropbox-files-and-folders)
* [Module zum Erstellen und Bearbeiten  [!DNL Dropbox]  Dateien und Ordnern](#modules-for-creating-and-editing-dropbox-files-and-folders)
* [Andere Module](#other-modules)

### Trigger-Module

#### [!UICONTROL Dateien ansehen]

Dieses Ordnertypmodul gibt Dateidetails zurück, wenn die Trigger in einem angegebenen Ordner geändert wird.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den Ordner aus, den Sie auf Änderungen überwachen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL auch Unterordner ansehen]</td> 
   <td> <p> Aktivieren Sie diese Option, um auch Unterordner im ausgewählten Ordner auf geänderte Dateien zu überwachen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Module zum Abrufen [!DNL Dropbox] Dateien und Ordner

* [[!UICONTROL Datei herunterladen]](#download-a-file)
* [[!UICONTROL Abrufen von Ordnermetadaten]](#get-a-folder-metadata)
* [[!UICONTROL Listet alle Dateien/Unterordner in einem Ordner auf]](#list-all-filessubfolders-in-a-folder)
* [[!UICONTROL Dateiversionen auflisten]](#list-file-revisions)
* [[!UICONTROL Dateien/Ordner suchen]](#search-filesfolders)

#### [!UICONTROL Datei herunterladen]

Dieses Aktionsmodul lädt eine Datei aus einem Ordner herunter.

Sie geben die Datei und ihren Speicherort an.

Das Modul gibt die ID der Datei und aller zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

>[!NOTE]
>
>Dieses Modul ist nützlich, um Dateien für nachfolgende Module bereitzustellen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Methode zur Auswahl von Dateien</td> 
   <td> <p> Wählen Sie aus, ob Sie den Dateipfad zuordnen möchten, oder wählen Sie die Datei manuell aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Dateipfad/Datei</p> </td> 
   <td> <p style="font-weight: bold;">Dateipfad</p> <p>Geben Sie den Zielpfad in die Datei ein oder ordnen Sie ihn zu.</p> <p style="font-weight: bold;">Datei</p> <p>Wählen Sie die Datei aus dem Menü aus.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Abrufen von Ordnermetadaten]

Dieses Aktionsmodul ruft Details zum freigegebenen Ordner ab.

Sie geben die ID des Ordners an.

Das Modul gibt die ID des Ordners und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>ID des freigegebenen Ordners</td> 
   <td> <p> Geben Sie die ID des Ordners ein, zu dem Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Listet alle Dateien/Unterordner in einem Ordner auf]

Dieses Aktionsmodul listet Dateien oder Ordner in einem bestimmten Ordner auf.

Sie geben die ID des Ordners an.

Das Modul gibt die IDs der Dateien oder Ordner und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Liste </td> 
   <td> <p>Wählen Sie aus, ob Sie Dateien oder Ordner abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Nur herunterladbare Dateien anzeigen</td> 
   <td> <p> Aktivieren Sie diese Option, um nur herunterladbare Dateien zurückzugeben. Einige Dateitypen, z. B. Google Docs, können nicht heruntergeladen werden.</p> </td> 
  </tr> 
  <tr> 
   <td>Ordner </td> 
   <td> <p>Geben Sie den Ordner ein, aus dem Sie Dateien oder Ordner abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td>Grenze </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus auflisten soll, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dateiversionen auflisten]

Dieses Aktionsmodul ruft alle Dateirevisionen (einen Versionsverlauf) einer bestimmten Datei ab.\
Sie geben die ID der Datei an.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Methode zur Auswahl von Dateien</td> 
   <td> <p> Wählen Sie aus, ob Sie den Dateipfad zuordnen möchten, oder wählen Sie die Datei manuell aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Dateipfad/Datei</p> </td> 
   <td> <p><b>Dateipfad</b></p> <p>Geben Sie den Zielpfad in die Datei ein oder ordnen Sie ihn zu.</p> <p><b>Datei</b></p> <p>Wählen Sie die Datei aus dem Menü aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Grenze</p> </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus auflisten soll, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dateien/Ordner suchen]

Dieses Suchmodul sucht in einem -Objekt nach Datensätzen, [!DNL Dropbox] mit der angegebenen Suchanfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suche] </td> 
   <td> <p>Geben Sie den Suchbegriff ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den Ordner aus, den Sie suchen möchten. Dieses Modul durchsucht das gesamte [!DNL Dropbox]Konto, wenn Sie keinen Ordner auswählen.</p> </td> 
  </tr> 
  <tr> 
   <td>Dateistatus</td> 
   <td> <p> Wählen Sie den Dateistatus aus, den Sie bei der Suche einbeziehen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Dateikategorien</td> 
   <td> <p> Wählen Sie die Dateikategorien aus, die Sie in die Suche einbeziehen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Dateierweiterungen</td> 
   <td> <p>Klicken Sie für jede Dateierweiterung, die Sie in die Suche einbeziehen möchten, auf <b>Element hinzufügen</b> und geben Sie die Dateierweiterung ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td>Grenze </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Module zum Erstellen und Bearbeiten von [!DNL Dropbox] Dateien und Ordnern

* [[!UICONTROL Ordner erstellen]](#create-a-folder)
* [[!UICONTROL Erstellen/Überschreiben einer Textdatei]](#createoverwrite-a-text-file)
* [[!UICONTROL Erstellen/Aktualisieren eines Freigabe-Links]](#createupdate-a-share-link)
* [[!UICONTROL Löschen einer Datei/eines Ordners]](#delete-a-filefolder)
* [[!UICONTROL Verschieben einer Datei/eines Ordners]](#move-a-filefolder)
* [[!UICONTROL Datei/Ordner umbenennen]](#rename-a-filefolder)
* [[!UICONTROL Datei wiederherstellen]](#restore-a-file)
* [[!UICONTROL Hochladen] einer Datei](#upload-a-file)

#### [!UICONTROL Ordner erstellen]

Dieses Aktionsmodul erstellt einen neuen Ordner.

Sie geben den Pfad und einen Namen für den Ordner an.

Das Modul gibt die ID des Ordners und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordnername] </td> 
   <td> <p>Geben Sie den Namen für den neuen Ordner ein.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-Ordner]</p> </td> 
   <td> <p>Geben Sie den Pfad ein, unter dem Sie einen neuen Ordner erstellen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis:   <p>Wenn Sie ein [!DNL Dropbox Business] <code>/</code>-Konto (mit Team-Platzierungen) verwenden, müssen Sie den Schrägstrich entfernen, oder klicken Sie nicht auf <strong>Hier klicken, um </strong> Ordner auszuwählen), um einen Team-Ordner im Stammverzeichnis zu erstellen.</p> <p>Wenn der Schrägstrich nicht entfernt wird, wird eine <code>[409] path/malformed_path/..</code> zurückgegeben.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Automatisch umbenennen]</td> 
   <td> <p> Aktivieren Sie diese Option, um den neuen Ordner umzubenennen, wenn am Zielspeicherort bereits ein Ordner mit demselben Namen vorhanden ist.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen/Überschreiben einer Textdatei]

Dieses Aktionsmodul erstellt eine DOC-Datei oder überschreibt den Inhalt einer vorhandenen.

Sie geben die Quelldatei und den Ordner an.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Auswählen, um]</td> 
   <td> <p> Wählen Sie aus, ob Sie eine DOC-Datei erstellen oder überschreiben möchten.</p><ul><li><b>Erstellen</b></p>Wählen Sie den Ordner aus, in dem Sie eine Datei erstellen möchten.</li><li><b>Überschreiben</b><p>Wählen Sie aus, wie Sie die zu überschreibende Datei auswählen möchten, ordnen Sie dann den Dateipfad zu oder wählen Sie die Datei aus. </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source-Datei]</p> </td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Inhalt der Quelldatei zu. </p> <p>Wenn Sie eine Datei erstellen, wählen Sie "<b>" </b>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen/Aktualisieren eines Freigabe-Links]

Dieses Aktionsmodul erstellt einen öffentlichen Link zu einer Datei.

Sie geben die Datei und Informationen zum Link an.

Das Modul gibt die ID des Links und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Methode zur Auswahl von Dateien]</td> 
   <td> <p> Wählen Sie aus, ob Sie den Dateipfad zuordnen oder eingeben möchten, oder wählen Sie die Datei manuell aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Dateipfad/Datei]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Dateipfad]</p> <p>Geben Sie den Pfad zur Zieldatei ein oder mappen Sie ihn.</p> <p style="font-weight: bold;">[!UICONTROL-Datei]</p> <p>Wählen Sie die Zieldatei.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL angeforderte Sichtbarkeit]</p> </td> 
   <td> <p>Wählen Sie aus, ob der Link öffentlich, für das Team oder kennworteingeschränkt ist.</p> <p><b>Hinweis:</b></p><p> [!Nur UICONTROL Team] ist nur für Dropbox Business-Konten verfügbar. [!UICONTROL Zugriff mit Passwort] ist nur für [!DNL Dropbox Pro] oder Dropbox Business-Konten verfügbar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!Ablaufdatum des UICONTROL-Links]</td> 
   <td> <p> Geben Sie Datum und Uhrzeit ein, zu der der Link abläuft und nicht mehr zugänglich ist. Wenn dieses Feld leer gelassen wird, läuft der Link nicht ab. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Typzwang</a>.</p>  </td> 
  </tr> 
  <tr> 
   <td> <p>[!Zugriffsebene des UICONTROL-Links]</p> </td> 
   <td> <p>Festlegen der Berechtigung für den Link-Empfänger.</p> <ul><li><strong>[!UICONTROL Viewer]</strong> <p>Benutzer, die den Link verwenden, können den Inhalt anzeigen und kommentieren.</p> </li><li><strong>[!UICONTROL Editor]</strong><p> Benutzer, die den Link verwenden, können den Inhalt bearbeiten, anzeigen und kommentieren. Diese Zugriffsebene ist nur für Cloud-basierte Dokumente verfügbar.</p> </li><li><strong>[!UICONTROL max]</strong> <p>Benutzer, die den Link verwenden, erhalten die maximale Zugriffsebene, auf die Sie den Link festlegen können.</p></li><ul> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Löschen einer Datei/eines Ordners]

Dieses Aktionsmodul löscht eine Datei oder einen Ordner.

Sie geben die Datei oder den Ordner an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Methode zur Auswahl von Dateien]</td> 
   <td> <p> Wählen Sie aus, ob Sie den Dateipfad zuordnen oder eingeben möchten, oder wählen Sie die Datei manuell aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-Datei oder Ordnerpfad] / [!UICONTROL-Datei oder Ordner]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Datei-/Ordnerpfad]</p> <p>Geben Sie den Zielpfad für die Datei oder den Ordner ein oder ordnen Sie ihn zu.</p> <p style="font-weight: bold;">[!UICONTROL Datei/Ordner]</p> <p>Wählen Sie die Datei oder den Ordner aus dem Menü aus.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Verschieben einer Datei/eines Ordners]

Dieses Aktionsmodul verschiebt eine Datei oder einen Ordner an einen anderen Speicherort.

Sie legen die Datei oder den Ordner sowie die Art und Weise und den Ort des Verschiebens fest.

Das Modul gibt die ID der Datei oder des Ordners und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Methode zur Auswahl von Dateien/Ordnern] </td> 
   <td> <p>Wählen Sie aus, ob Sie den Datei- oder Ordnerpfad zuordnen oder eingeben möchten, oder wählen Sie die Datei oder den Ordner manuell aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Datei / Ordnerpfad] /</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Datei-/Ordnerpfad]</p> <p>Geben Sie den Zielpfad für die Datei oder den Ordner ein oder ordnen Sie ihn zu.</p> <p style="font-weight: bold;">[!UICONTROL Datei/Ordner]</p> <p>Wählen Sie aus, ob Sie eine Datei oder einen Ordner verschieben, und wählen Sie dann die Datei oder den Ordner aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL zu Ordner]</p> </td> 
   <td> <p>Geben Sie den Zielspeicherort für die Datei oder den Ordner ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Neuer Name]</p> </td> 
   <td> <p>Geben Sie den neuen Namen für die Datei oder den Ordner am neuen Speicherort ein.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Automatisch umbenennen]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um sicherzustellen, dass das Modul die neue Datei oder den neuen Ordner umbenennt, wenn eine Datei oder ein Ordner mit demselben Namen vorhanden ist, indem ([!UICONTROL NUMBER]) nach dem Datei- oder Ordnernamen hinzugefügt wird. Andernfalls wird die Datei bzw. der Ordner am Zielspeicherort überschrieben.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Eigentumsübertragung zulassen]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um Verschiebungen nach Inhaber zuzulassen, auch wenn dies zu einer Übertragung der Eigentümerschaft für den verschobenen Inhalt führen würde.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei/Ordner umbenennen]

Dieses Aktionsmodul benennt eine Datei oder einen Ordner um.

Geben Sie die Datei bzw. den Ordner und den neuen Namen an.

Das Modul gibt die ID der Datei oder des Ordners und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Methode zur Auswahl von Dateien</td> 
   <td> <p> Wählen Sie aus, ob Sie den Dateipfad zuordnen oder eingeben möchten, oder wählen Sie die Datei manuell aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Datei/Ordnerpfad/Datei/Ordner</p> </td> 
   <td> <p style="font-weight: bold;">Datei-/Ordnerpfad</p> <p>Geben Sie den Zielpfad für die Datei oder den Ordner ein oder ordnen Sie ihn zu.</p> <p style="font-weight: bold;">Datei/Ordner</p> <p>Wählen Sie aus, ob Sie eine Datei oder einen Ordner verschieben, und wählen Sie dann die Datei oder den Ordner aus.</p> </td> 
  </tr> 
  <tr> 
   <td>Umbenennen </td> 
   <td> <p>Geben Sie den neuen Namen für die Datei ein, einschließlich der Dateierweiterung.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Datei wiederherstellen]

Dieses Aktionsmodul stellt eine frühere Version einer Datei wieder her.

Sie geben die Datei und die Nummer der Revision an, die Sie benötigen.

Das Modul gibt die ID der Version und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Methode zur Auswahl von Dateien]</td> 
   <td> <p> Wählen Sie aus, ob Sie den Dateipfad zuordnen oder eingeben möchten, oder wählen Sie die Datei manuell aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-Dateipfad] / [!UICONTROL-Datei]</p> </td> 
   <td> <p><strong>[!UICONTROL Dateipfad]</strong> </p> <p>Geben Sie den Zielpfad in die Datei ein oder ordnen Sie ihn zu.</p> <p><strong>[!UICONTROL-Datei]</strong> </p> <p>Wählen Sie die Datei aus dem Menü aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-Revision]</p> </td> 
   <td> <p>Geben Sie die Revisionsnummer der Revision ein, die Sie wiederherstellen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei hochladen]

Dieses Aktionsmodul lädt eine Datei in einen Ordner hoch.

Sie geben Informationen wie den Speicherort für die Datei, die Datei, die Sie hochladen möchten, und einen optionalen neuen Namen für die Datei an.

Das Modul gibt die ID der Datei und aller zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner]</td> 
   <td> <p> Wählen Sie den Ordner Ihrer [!DNL Dropbox] aus, in den Sie die Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source-Datei]</p> </td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> <p><b>Hinweis:</b></p><p> Die maximale Größe der hochgeladenen Datei beträgt 150 MB.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Vorhandene Datei überschreiben]</td> 
   <td> <p> Aktivieren Sie diese Option, um die vorhandene Datei durch die neue Datei zu ersetzen. Wenn diese Option deaktiviert bleibt, wird die hochgeladene Datei umbenannt.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Andere Module

#### [!UICONTROL Erstellen eines API-Aufrufs]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Dropbox]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Dropbox] nicht durchgeführt werden kann.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Dropbox]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-dropbox" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Dropbox]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen relativen Pfad ein, um einen relativen Pfad zum <code>https://api.dropboxapi.com</code> einzugeben. Beispiel: <code>/2/files/list_folder</code></p>  </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-Methode]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Kopfzeilen] </td> 
   <td> <p>Geben Sie die gewünschten Anfrage-Header ein. [!DNL Workfront Fusion] fügt Autorisierungskopfzeilen automatisch hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p> Geben Sie die Abfragezeichenfolge der Anfrage ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL body] </td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:   <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Beispiel:**

Der folgende API-Aufruf gibt die ersten 10 Dateien aus dem [!DNL /Text files] Ordner in Ihrem [!DNL Dropbox]-Konto zurück:

URL: `/2/files/list_folder`

Textkörper:

```
{
"path": "/Text files",
"limit": 10,
"recursive": false,
"include_deleted": false
}
```

Treffer der Suche finden Sie in der Modulausgabe unter [!UICONTROL Bundle] > [!UICONTROL Body] > Einträge.

In unserem Beispiel wurden 10 Tickets zurückgegeben.

>[!ENDSHADEBOX]

## Häufige Probleme

* [Datei kann nicht hochgeladen oder aktualisiert werden](#unable-to-upload-or-update-a-file)
* [Über einen freigegebenen Link referenziertes Bild wird nicht gerendert](#image-referenced-via-a-shared-link-does-not-render)

### Datei kann nicht hochgeladen oder aktualisiert werden

Das Hochladen oder Aktualisieren einer Datei kann aus folgenden Gründen fehlschlagen:

* Die hochgeladene Datei ist zu groß und überschreitet die für Ihren [!DNL Dropbox] maximal zulässige Dateigröße. Andernfalls haben Sie das Speicherkontingent Ihres [!DNL Dropbox]-Kontos vollständig ausgeschöpft. Sie müssen vorhandene Dateien aus Ihrem [!DNL Dropbox] löschen oder Ihren Plan aktualisieren.
* Der zuvor ausgewählte Ordner, in den die Datei hochgeladen wird, existiert nicht mehr. Das Szenario stoppt und Sie müssen den Zielordner erneut auswählen.

### Über einen freigegebenen Link referenziertes Bild wird nicht gerendert

Die von [!UICONTROL Dropbox] >[!UICONTROL Freigegebenen Link erstellen] zurückgegebene URL verweist nicht direkt auf ein Bild, sondern auf eine [!DNL Dropbox]. Um das Herunterladen des Bildes zu erzwingen, ersetzen Sie die nachfolgende `?dl=0` durch `?dl=1`. Um das Rendern des Bildes zu erzwingen (z. B. in einem Webbrowser oder in Facebook Messenger), hängen Sie `&raw=1` an die URL an.

Wenn Sie den direkten oder unbearbeiteten Link Ihres Bildes für Ihre Website oder für andere [!DNL Workfront Fusion]-Module abrufen müssen, müssen Sie die anfängliche freigegebene URL wie folgt ändern:

Ursprüngliche URL:

`https://www.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png?dl=0`

1. `www` durch `dl` ersetzen.
1. `?dl=0` entfernen.

Endgültige URL:

`https://dl.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png`

Um die URL automatisch zu ändern, können Sie die Funktion `replace()` zweimal verwenden:

* Ersetzen Sie www durch dl

  ![Ersetzen Sie www durch dl](/help/workfront-fusion/references/apps-and-modules/assets/www-to-dl-350x32.png)

* Und ?dl=0 entfernen

  ![DL entfernen](/help/workfront-fusion/references/apps-and-modules/assets/remove-dl0-350x33.png)

Um dies in einem Schritt zu tun, kombinieren Sie diese Funktionen:

![Beide ersetzen](/help/workfront-fusion/references/apps-and-modules/assets/replace-both-350x47.png)

Sie können sie auch kopieren und in das Feld einfügen. Ersetzen Sie `1.url` durch die URL .

```
{{replace(replace(1.url; "?dl=0"; ""); "www"; "dl")}}
```
