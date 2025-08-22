---
title: Microsoft OneDrive-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die OneDrive verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: d21eafad-9c67-4f42-b718-0aa4223846e6
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '4159'
ht-degree: 0%

---

# [!DNL Microsoft OneDrive]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL OneDrive] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um [!DNL OneDrive]-Module verwenden zu können, müssen Sie über ein [!DNL Microsoft OneDrive]-Konto verfügen.



## OneDrive-API-Informationen

Der OneDrive-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://graph.microsoft.com/v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>


## Verbinden des [!DNL OneDrive]-Service mit Workfront Fusion

Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung mit [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
>
>Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.

## [!DNL Microsoft OneDrive] Module und ihre Felder

Beim Konfigurieren von [!DNL OneDrive] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL OneDrive] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Datei/Ordner](#filefolder)
* [Sonstiges](#other)

### Datei/Ordner

* [[!UICONTROL Kopieren einer Datei]](#copy-a-file)
* [[!UICONTROL Erstellen eines Ordners]](#create-a-folder)
* [[!UICONTROL Löschen einer Datei/eines Ordners]](#delete-a-filefolder)
* [[!UICONTROL Datei herunterladen]](#download-a-file)
* [[!UICONTROL Datei abrufen]](#get-a-file)
* [[!UICONTROL Link freigeben]](#get-a-share-link)
* [[!UICONTROL Verschieben einer Datei/eines Ordners]](#move-a-filefolder)
* [[!UICONTROL Dateien/Ordner suchen]](#search-filesfolders)
* [[!UICONTROL Datei hochladen]](#upload-a-file)
* [[!UICONTROL Dateien/Ordner ansehen]](#watch-filesfolders)

#### [!UICONTROL Kopieren einer Datei]

Dieses Aktionsmodul kopiert eine Datei an einen neuen Speicherort

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (Datei-ID und Dateipfad)]</td> 
   <td>Wählen Sie aus, ob die Datei anhand der Datei-ID oder anhand des Dateipfads identifiziert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID eingeben] / [!UICONTROL Dateipfad]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Datei-ID oder den Dateipfad eingeben möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Manuell eingeben]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie die ID oder den Pfad direkt eingeben oder sie von einem vorherigen Modul aus zuordnen möchten.</p> </li> 
     <li> <p><b>[!UICONTROL Aus einer Liste auswählen]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie aus einer Liste der verfügbaren Dateien oder Pfade auswählen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den Speicherort aus, der die Datei enthält, die Sie kopieren möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Geben Sie die ID des Laufwerks ein, das die Datei oder den Ordner enthält, die bzw. den Sie kopieren möchten.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die SharePoint-Site aus, die die zu verschiebende Datei enthält. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, deren Laufwerk die zu kopierende Datei enthält.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das die zu kopierende Datei enthält, oder ordnen Sie es zu. Dieses Feld ist nicht verfügbar, wenn Sie im Feld [!UICONTROL Aktivieren, um eine Laufwerk-ID einzugeben] [!UICONTROL Nein] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL -Datei] / [!UICONTROL -Datei-ID] / [!UICONTROL -Dateipfad]</p> </td> 
   <td> <p>Wenn Sie [!UICONTROL Manuell eingeben] ausgewählt haben, geben Sie die ID oder den Pfad der Datei ein, die Sie kopieren möchten, oder ordnen Sie sie zu.</p> <p>Wenn Sie in der Liste Auswählen ausgewählt haben, wählen Sie die Datei aus, die Sie kopieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Neuen Ordnerspeicherort eingeben]</td> 
   <td> <p>Wählen Sie aus, wohin Sie den Speicherort eingeben möchten, in den Sie die Datei kopieren möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Manuell eingeben]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie die ID oder den Pfad direkt eingeben oder sie von einem vorherigen Modul aus zuordnen möchten.</p> </li> 
     <li> <p><b>[!UICONTROL Aus einer Liste auswählen]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie aus einer Liste der verfügbaren Ordner auswählen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL neuer OneDrive-Speicherort]</td> 
   <td> <p>Wählen Sie den Speicherort aus, an den Sie den Filter kopieren möchten. Diese Option ist verfügbar, wenn Sie den neuen Ordnerspeicherort aus einer Liste ausgewählt haben.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Geben Sie die ID des Laufwerks ein, auf das Sie die Datei kopieren möchten.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die [!DNL SharePoint] Site aus, in die Sie die Datei kopieren möchten. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, auf deren Laufwerk Sie die Datei kopieren möchten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das den Ordner enthält, in den Sie die Datei kopieren möchten, oder ordnen Sie es zu. Dieses Feld ist nicht verfügbar, wenn Sie im Feld [!UICONTROL Aktivieren, um eine Laufwerk-ID einzugeben] [!UICONTROL Nein] ausgewählt haben.</p> <p>Wenn Sie dieses Feld leer lassen, kann die Datei oder der Ordner nur innerhalb desselben [!UICONTROL OneDrive] kopiert werden.</p> <p>Sie können Dateien und Ordner von [!UICONTROL My Drive] in das Laufwerk einer [!UICONTROL Site] oder das Laufwerk einer [!UICONTROL Group] kopieren. </p> <p>Sie können Dateien aus dem Laufwerk einer [!UICONTROL Site] nur auf dasselbe Laufwerk derselben Site kopieren.</p> <p>Sie können Dateien aus dem Laufwerk einer [!UICONTROL Group] nur auf dasselbe Laufwerk derselben Gruppe kopieren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td>Geben Sie den Ordner ein, in den Sie die Kopie oder den Ordner verschieben möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Neuer kopierter Dateiname]</td> 
   <td> <p>Geben Sie einen Namen für die neue Kopie der Datei ein oder ordnen Sie ihn zu. Sie können dieses Feld leer lassen, wenn Sie den ursprünglichen Dateinamen nicht ändern möchten.</p> <p>Der Name muss die Dateierweiterung enthalten. Beispiel: <code>file.txt</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen eines Ordners]

Dieses Aktionsmodul erstellt einen neuen Ordner im angegebenen Laufwerk.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den Speicherort aus, an dem Sie einen Ordner erstellen möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Wählen Sie das Laufwerk aus, auf dem Sie einen Ordner erstellen möchten.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die [!DNL SharePoint] Site aus, in der Sie einen Ordner erstellen möchten. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, der das Laufwerk gehört, auf dem Sie einen Ordner erstellen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, auf dem Sie einen Ordner erstellen möchten. Dieses Feld ist nicht verfügbar, wenn Sie im Feld [!UICONTROL Aktivieren, um eine Laufwerk-ID einzugeben] [!UICONTROL Nein] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td>Wenn der neue Ordner ein Unterordner sein soll, navigieren Sie zu dem Ordner, in dem er ein Unterordner sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Neuer Ordnername]</td> 
   <td> <p>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wenn der gleichnamige Ordner bereits vorhanden ist]</td> 
   <td>Wählen Sie aus, wie vorgegangen werden soll, wenn bereits eine Datei mit demselben Namen vorhanden ist.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Löschen einer Datei/eines Ordners]

Dieses Aktionsmodul löscht die ausgewählte Datei oder den ausgewählten Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (Datei-/Ordner-ID und Pfad)]</td> 
   <td>Wählen Sie aus, ob die Datei anhand der Datei-ID oder anhand des Dateipfads identifiziert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-/Ordner-ID eingeben /Datei-/Ordnerpfad eingeben]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Datei-ID oder den Dateipfad eingeben möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Manuell eingeben]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie die ID oder den Pfad direkt eingeben oder sie von einem vorherigen Modul aus zuordnen möchten.</p> </li> 
     <li> <p><b>[!UICONTROL Aus einer Liste auswählen]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie aus einer Liste der verfügbaren Dateien oder Pfade auswählen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den Ort aus, den Sie suchen möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Geben Sie die ID des Laufwerks ein, auf dem sich die zu löschende Datei bzw. der zu löschende Ordner befindet.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die [!DNL SharePoint] Site aus, die die Datei oder den Ordner enthält, die bzw. den Sie löschen möchten. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, deren Laufwerk die zu löschende Datei oder den zu löschenden Ordner enthält.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das die zu löschende Datei oder den zu löschenden Ordner enthält, oder ordnen Sie es zu. Dieses Feld ist nicht verfügbar, wenn Sie im Feld [!UICONTROL Aktivieren, um eine Laufwerk-ID einzugeben] [!UICONTROL Nein] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei/Ordner] auswählen</td> 
   <td>Wählen Sie aus, ob Sie eine Datei oder einen Ordner löschen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Datei] / [!UICONTROL -Datei-ID] / [!UICONTROL -Dateipfad]</td>
   <td> <p>Wenn Sie [!UICONTROL Manuell eingeben] ausgewählt haben, geben Sie die Datei-ID oder den Pfad der Datei, die Sie löschen möchten, ein oder mappen Sie sie.</p> <p>Wenn Sie [!UICONTROL Select] aus der Liste ausgewählt haben, wählen Sie die Datei aus, die Sie löschen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei herunterladen]

Dieses Aktionsmodul lädt die angegebene Datei herunter.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (Datei-ID und Dateipfad)]</td> 
   <td>Wählen Sie aus, ob die Datei anhand der Datei-ID oder anhand des Dateipfads identifiziert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Datei-ID/Dateipfad eingeben</td> 
   <td> <p>Wählen Sie aus, wie Sie die Datei-ID oder den Dateipfad eingeben möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Manuell eingeben]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie die ID oder den Pfad direkt eingeben oder sie von einem vorherigen Modul aus zuordnen möchten.</p> </li> 
     <li> <p><b>[!UICONTROL Aus einer Liste auswählen]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie aus einer Liste der verfügbaren Dateien oder Pfade auswählen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den gewünschten Speicherort aus, der die Datei enthält, die Sie herunterladen möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Geben Sie die ID des Laufwerks ein, das die herunterzuladende Datei enthält.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die SharePoint-Site aus, die die Datei enthält, die Sie herunterladen möchten. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, deren Laufwerk die Datei enthält, die Sie herunterladen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das die Datei enthält, die Sie herunterladen möchten, oder ordnen Sie es zu. Dieses Feld ist nicht verfügbar, wenn Sie im Feld [!UICONTROL Aktivieren, um eine Laufwerk-ID einzugeben] [!UICONTROL Nein] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Datei] / [!UICONTROL -Datei-ID] / [!UICONTROL -Dateipfad]</td>
   <td> <p>Wenn Sie [!UICONTROL Manuell eingeben] ausgewählt haben, geben Sie die Datei-ID oder den Pfad der Datei, die Sie herunterladen möchten, ein oder mappen Sie sie.</p> <p>Wenn Sie [!UICONTROL Auswählen aus der Liste] ausgewählt haben, wählen Sie die Datei, die Sie herunterladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nach PDF konvertieren]</td> 
   <td> <p>Aktivieren Sie diese Option, um die Datei in eine PDF-Datei zu konvertieren. Sie können aus den folgenden Dateitypen konvertieren:</p> 
    <table style="table-layout:auto"> 
     <col> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td> 
        <ul> 
         <li> <p> <p>CSV</p> </p> </li> 
         <li> <p> <p>DOC</p> </p> </li> 
         <li> <p> <p>DOCX</p> </p> </li> 
         <li> <p> <p>ODP</p> </p> </li> 
         <li> <p> <p>ODS</p> </p> </li> 
         <li> <p> <p>ODT</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p> <p>TOPF</p> </p> </li> 
         <li> <p> <p>POTM</p> </p> </li> 
         <li> <p> <p>POTX</p> </p> </li> 
         <li> <p> <p>PPS</p> </p> </li> 
         <li> <p> <p>PPSX</p> </p> </li> 
         <li> <p> <p>PPSXM</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p>PPT</p> </li> 
         <li> <p>PPTM</p> </li> 
         <li> <p>PPTX</p> </li> 
         <li> <p>RTF</p> </li> 
         <li> <p>XLS</p> </li> 
         <li> <p>XLSX</p> </li> 
        </ul> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei abrufen]

Dieses Aktionsmodul ruft die Metadaten einer angegebenen Datei ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (Datei-ID und Dateipfad)]</td> 
   <td>Wählen Sie aus, ob die Datei anhand der Datei-ID oder anhand des Dateipfads identifiziert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID eingeben] / [!UICONTROL Dateipfad]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Datei-ID oder den Dateipfad eingeben möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Manuell eingeben]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie die ID oder den Pfad direkt eingeben oder sie von einem vorherigen Modul aus zuordnen möchten.</p> </li> 
     <li> <p><b>[!UICONTROL Aus einer Liste auswählen]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie aus einer Liste der verfügbaren Dateien oder Pfade auswählen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den Ort aus, den Sie suchen möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Geben Sie die ID des Laufwerks ein, das die Datei enthält, die Sie abrufen möchten.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die SharePoint-Site aus, die die Datei enthält, die Sie erhalten möchten. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, deren Laufwerk die Datei enthält, die Sie erhalten möchten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das die Datei enthält, die Sie abrufen möchten, oder ordnen Sie es zu. Dieses Feld ist nicht verfügbar, wenn Sie im Feld [!UICONTROL Aktivieren, um eine Laufwerk-ID einzugeben] [!UICONTROL Nein] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Datei] / [!UICONTROL -Datei-ID] / [!UICONTROL -Dateipfad]</td> 
   <td> <p>Wenn Sie [!UICONTROL Manuell eingeben] ausgewählt haben, geben Sie die Datei-ID oder den Pfad der Datei, die Sie abrufen möchten, ein oder mappen Sie sie.</p> <p>Wenn Sie [!UICONTROL Auswählen aus der Liste] ausgewählt haben, wählen Sie die Datei, die Sie erhalten möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Link freigeben]

Dieses Aktionsmodul gibt einen Freigabe-Link für die angegebene Datei zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (Datei-ID und Dateipfad)]</td> 
   <td>Wählen Sie aus, ob die Datei anhand der Datei-ID oder anhand des Dateipfads identifiziert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID eingeben] / [!UICONTROL Dateipfad]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Datei-ID oder den Dateipfad eingeben möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Manuell eingeben]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie die ID oder den Pfad direkt eingeben oder sie von einem vorherigen Modul aus zuordnen möchten.</p> </li> 
     <li> <p><b>[!UICONTROL Aus einer Liste auswählen]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie aus einer Liste der verfügbaren Dateien oder Pfade auswählen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den Speicherort aus, für den Sie einen Freigabe-Link abrufen möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Geben Sie die ID des Laufwerks ein, das die Datei enthält, für die Sie einen Freigabe-Link abrufen möchten.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die SharePoint-Site aus, die die Datei enthält, für die Sie einen Freigabe-Link abrufen möchten. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, deren Laufwerk die Datei enthält, für die Sie einen Freigabe-Link abrufen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das die Datei enthält, für die Sie einen Freigabe-Link abrufen möchten, oder ordnen Sie es zu. Dieses Feld ist nicht verfügbar, wenn Sie im Feld [!UICONTROL Aktivieren, um eine Laufwerk-ID einzugeben] [!UICONTROL Nein] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Datei] / [!UICONTROL -Datei-ID] / [!UICONTROL -Dateipfad]</td> 
   <td> <p>Wenn Sie [!UICONTROL Manuell eingeben] ausgewählt haben, geben Sie die Datei-ID oder den Pfad der Datei, für die Sie einen Freigabe-Link abrufen möchten, ein oder mappen Sie sie.</p> <p>Wenn Sie [!UICONTROL Select] aus der Liste ausgewählt haben, wählen Sie die Datei aus, für die Sie einen Freigabe-Link abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Berechtigungstyp]</td> 
   <td> <p>Wählen Sie aus, ob Personen mit diesem Link die Datei lesen und schreiben oder nur lesen können sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Umfang]</td> 
   <td>Wählen Sie aus, ob die Datei für alle Personen mit dem Link oder nur für Mitglieder Ihrer Organisation verfügbar sein soll, die den Link besitzen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Verschieben einer Datei/eines Ordners]

Dieses Aktionsmodul verschiebt eine Datei oder einen Ordner an einen neuen Speicherort

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (Datei-ID und Dateipfad)]</td> 
   <td>Wählen Sie aus, ob die Datei anhand der Datei-ID oder anhand des Dateipfads identifiziert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID/Dateipfad eingeben]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Datei-ID oder den Dateipfad eingeben möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Manuell eingeben]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie die ID oder den Pfad direkt eingeben oder sie von einem vorherigen Modul aus zuordnen möchten.</p> </li> 
     <li> <p><b>[!UICONTROL Aus einer Liste auswählen]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie aus einer Liste der verfügbaren Dateien oder Pfade auswählen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den Speicherort aus, der die Datei oder den Ordner enthält, die bzw. den Sie verschieben möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Geben Sie die ID des Laufwerks ein, das die zu verschiebende Datei oder den zu verschiebenden Ordner enthält.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die [!DNL SharePoint] Site aus, die die zu verschiebende Datei oder den zu verschiebenden Ordner enthält. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, deren Laufwerk die zu verschiebende Datei oder den zu verschiebenden Ordner enthält.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das die zu verschiebende Datei oder den zu verschiebenden Ordner enthält, oder ordnen Sie es zu. Dieses Feld ist nicht verfügbar, wenn Sie im Feld [!UICONTROL Aktivieren, um eine Laufwerk-ID einzugeben] [!UICONTROL Nein] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei/Ordner] auswählen</td> 
   <td>Wählen Sie aus, ob Sie eine Datei oder einen Ordner verschieben möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL -Datei] / [!UICONTROL -Datei-ID] / [!UICONTROL -Dateipfad]</p> <p role="rowheader">[!UICONTROL -Ordner] / [!UICONTROL -Ordner-ID] / [!UICONTROL -Ordnerpfad]</p> </td> 
   <td> <p>Wenn Sie [!UICONTROL Manuell eingeben] ausgewählt haben, geben Sie die ID oder den Pfad der Datei oder des Ordners ein, die bzw. den Sie verschieben möchten, oder ordnen Sie sie zu.</p> <p>Wenn Sie [!UICONTROL Select] aus der Liste ausgewählt haben, wählen Sie die Datei oder den Ordner aus, die bzw. den Sie verschieben möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Neuen Ordnerspeicherort eingeben]</td> 
   <td> <p>Wählen Sie aus, wie Sie den Speicherort eingeben möchten, an den Sie die Datei oder den Ordner verschieben möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Manuell eingeben]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie die ID oder den Pfad direkt eingeben oder sie von einem vorherigen Modul aus zuordnen möchten.</p> </li> 
     <li> <p><b>[!UICONTROL Aus einer Liste auswählen]</b> </p> <p>Wählen Sie diese Option aus, wenn Sie aus einer Liste der verfügbaren Dateien oder Pfade auswählen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den Speicherort aus, an den Sie die Datei oder den Ordner verschieben möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Geben Sie die ID des Laufwerks ein, in das Sie die Datei oder den Ordner verschieben möchten.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die [!DNL SharePoint] Site aus, in die Sie die Datei oder den Ordner verschieben möchten. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, zu deren Laufwerk Sie die Datei oder den Ordner verschieben möchten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das den Ordner enthält, in den Sie die Datei oder den Ordner verschieben möchten, oder ordnen Sie es zu. Dieses Feld ist nicht verfügbar, wenn Sie im Feld [!UICONTROL Aktivieren, um eine Laufwerk-ID einzugeben] [!UICONTROL Nein] ausgewählt haben.</p> <p>Wenn Sie dieses Feld leer lassen, kann die Datei bzw. der Ordner nur innerhalb derselben [!DNL OneDrive] verschoben werden.</p> <p>Sie können Dateien und Ordner von [!UICONTROL My Drive] auf das Laufwerk einer [!UICONTROL Site] oder das Laufwerk einer [!UICONTROL Group] verschieben. </p> <p>Sie können Dateien vom Laufwerk einer [!UICONTROL Site] nur auf dasselbe Laufwerk in derselben Site verschieben.</p> <p>Sie können Dateien vom Laufwerk einer [!UICONTROL Group] nur auf dasselbe Laufwerk derselben Gruppe verschieben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td>Geben Sie den Ordner ein, in den Sie die Datei oder den Ordner verschieben möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dateien/Ordner suchen]

Dieses Suchmodul gibt Dateien und Ordner basierend auf den von Ihnen festgelegten Kriterien zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den Ort aus, den Sie suchen möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Geben Sie die ID des Laufwerks ein, nach dem das Modul suchen soll.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> <p>Navigieren Sie zu dem Ordner, den das Modul durchsuchen soll. Sie können auch eine Abfrage eingeben, um die zurückgegebenen Ergebnisse zu filtern.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL für mich freigegeben]</b> </p> <p>Das Modul sucht nach Dateien, die für den Eigentümer des Laufwerks freigegeben wurden.</p> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die [!DNL SharePoint] Site aus, nach der das Modul suchen soll. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, nach deren Laufwerk das Modul suchen soll.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elementtyp auswählen]</td> 
   <td> <p>Wählen Sie aus, ob Sie nach Dateien, Ordnern oder beidem suchen möchten.</p> <p>Hinweis: Sie können in einem Laufwerk vom Typ [!UICONTROL Shared With Me] nicht nach Ordnern suchen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei hochladen]

Dieses Aktionsmodul lädt eine Datei in den angegebenen Ordner hoch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enter (Folder Location ID &amp; Path)</td> 
   <td>Wählen Sie aus, ob Sie den Zielordner durch eine ID oder einen Pfad identifizieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den Speicherort aus, an den Sie eine Datei hochladen möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Wählen Sie das Laufwerk aus, das die Datei enthält, die Sie erhalten möchten.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die [!DNL SharePoint] Site aus, die den Ordner enthält, in den Sie eine Datei hochladen möchten. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, deren Laufwerk den Ordner enthält, in den Sie eine Datei hochladen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das den Ordner enthält, in den Sie eine Datei hochladen möchten. Dieses Feld ist nicht verfügbar, wenn Sie im Feld [!UICONTROL Aktivieren, um eine Laufwerk-ID einzugeben] [!UICONTROL Nein] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wenn die gleichnamige Datei existiert]</td> 
   <td>Wählen Sie aus, wie vorgegangen werden soll, wenn bereits eine Datei mit demselben Namen vorhanden ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td>Hinzufügen einer Beschreibung zur hochgeladenen Datei.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dateien/Ordner ansehen]

Dieses Ordnermodul startet ein Trigger-Szenario, wenn eine Datei oder ein Ordner erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Dateien/Ordner beobachten]</td> 
   <td> <p>Wählen Sie aus, wie Dateien oder Ordner überwacht werden sollen:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL nach Erstellungszeit]</b> </p> <p>Auf neue Dateien oder Ordner achten.</p> </li> 
     <li> <p><b>[!UICONTROL nach Aktualisierungszeit]</b> </p> <p>Suchen Sie nach aktualisierten Dateien oder Ordnern.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL [!DNL OneDrive] auswählen]</td> 
   <td> <p>Wählen Sie den Ort aus, den Sie beobachten möchten:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Wählen Sie aus, ob das Modul zur Eingabe einer Laufwerk-ID aktiviert werden soll.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Geben Sie die ID des Laufwerks ein, das vom Modul überwacht werden soll.</p> </li> 
       <li> <p><b>[!UICONTROL Nein]</b> </p> <p>Navigieren Sie zu dem Ordner, den das Modul überwachen soll. Sie können auch eine Abfrage eingeben, um die zurückgegebenen Ergebnisse zu filtern.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL für mich freigegeben]</b> </p> <p>Das Modul überwacht Dateien, die für den Eigentümer des Laufwerks freigegeben wurden.</p> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Wählen Sie die SharePoint-Site aus, die das Modul überwachen soll. Verfügbare Sites sind Sites , gefolgt vom angemeldeten Benutzer.</p> </li> 
     <li> <p><b>[!UICONTROL Laufwerk der-Gruppe]</b> </p> <p>Wählen Sie die Gruppe aus, deren Laufwerk vom Modul überwacht werden soll.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elementtyp auswählen]</td> 
   <td> <p>Wählen Sie aus, ob Dateien, Ordner oder beides überwacht werden soll.</p> <p>Hinweis: Sie können in einem Laufwerk vom Typ [!UICONTROL Shared With Me] nicht nach Ordnern suchen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Sonstiges

#### [!UICONTROL Erstellen eines API-Aufrufs]

Dieses Modul führt einen benutzerdefinierten API-Aufruf aus.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL OneDrive]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://graph.microsoft.com</code> ein. Beispiel:<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
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



## Wenn Sie eine Datei nicht hochladen oder aktualisieren können

Es gibt mehrere mögliche Probleme, wenn das Hochladen oder Aktualisieren einer Datei fehlschlägt:

* Die hochgeladene Datei ist zu groß und überschreitet die maximale Dateigröße für Ihren [!DNL OneDrive] oder Sie haben das Speicherkontingent Ihres [!DNL OneDrive]-Kontos vollständig genutzt. Um mehr Speicherplatz zu erhalten, löschen Sie vorhandene Dateien aus [!DNL OneDrive] oder aktualisieren Sie Ihr [!DNL OneDrive].
* OneDrive erlaubt es nicht, zwei Dateien mit demselben Namen in einen einzelnen Ordner hochzuladen. Wenn der Zielordner eine Datei mit demselben Namen wie die hochgeladene Datei enthält, wird die Ausführung des Szenarios mit einem Fehler beendet. Die Lösung besteht darin, die hochgeladene Datei einfach umzubenennen. Wenn Sie eine Datei aktualisieren möchten, verwenden Sie die Aktion [!UICONTROL Datei aktualisieren].
* Der zuvor ausgewählte Ordner, in den die Datei hochgeladen wird, existiert nicht mehr. Das Szenario wird angehalten und Sie müssen den Zielordner erneut auswählen.
