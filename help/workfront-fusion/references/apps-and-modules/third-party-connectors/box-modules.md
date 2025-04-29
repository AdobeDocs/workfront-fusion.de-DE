---
title: Box-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die Box verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden. Überwacht einen angegebenen Ordner, um auf Dateiänderungen zu prüfen, vorhandene Dateien zu ändern und zu löschen oder neue Dateien in einen Ordner hochzuladen.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: f02c4df01c7fad6bb9cdf4911512eef97e71c82b
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 1%

---

# Box-Module

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Box] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden. Überwacht einen angegebenen Ordner, um auf Dateiänderungen zu prüfen, vorhandene Dateien zu ändern und zu löschen oder neue Dateien in einen Ordner hochzuladen.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Voraussetzungen

Um [!DNL Box]-Module verwenden zu können, müssen Sie über ein [!DNL Box]-Konto verfügen.

## Box-API-Informationen

Der Box-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box] Module und ihre Felder

Beim Konfigurieren [!DNL Box] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Box] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)

### Auslöser

* [[!UICONTROL Neues Ereignis]](#new-event)
* [[!UICONTROL Dateien ansehen]](#watch-files)

#### [!UICONTROL Neues Ereignis]

Dieses Instant Trigger-Modul startet ein Szenario, in dem eine Datei hinzugefügt, verschoben, kopiert, gelöscht, gesperrt oder entsperrt wird.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Wählen Sie den Webhook aus, mit dem Sie ausgehende Nachrichten beobachten möchten. Um einen Webhook hinzuzufügen, klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie den Namen und die Verbindung des Webhooks ein.</p> <p> Anweisungen zum Verbinden Ihres [!UICONTROL Box]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung mit einem Dienst herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Ereignisse]</p> </td> 
   <td> <p>Geben Sie die höchste Anzahl von Ereignissen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dateien ansehen]

Dieses Dateimodul startet ein Szenario, wenn eine neue Trigger hinzugefügt oder eine vorhandene Datei in einem überwachten Ordner aktualisiert wird.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  <tr> 
   <td role="rowheader">Ordner</td> 
   <td> <p>Wählen Sie den Ordner aus, den Sie beobachten möchten. Ein Szenario kann einen einzelnen Ordner überwachen.</p> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beobachten</td> 
   <td> <p>Wählen Sie den Typ der Dateien aus, die Sie beobachten möchten.</p> 
    <ul> 
     <li> <p><strong>Nur neue Dateien</strong> </p> <p>Das Szenario beginnt, wenn eine neue Datei hinzugefügt wird.</p> </li> 
     <li> <p><strong>Neue Dateien und alle Änderungen</strong> </p> <p>Das Szenario beginnt, wenn eine Datei hinzugefügt wird oder wenn der Dateiinhalt oder ein Dateiattribut (z. B. der Name) geändert wird.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Maximale Anzahl heruntergeladener Dateien</p> </td> 
   <td> <p>Geben Sie die höchste Anzahl von Dateien ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Datei löschen]](#delete-a-file)
* [[!UICONTROL Datei abrufen]](#get-a-file)
* [[!UICONTROL Datei aktualisieren]](#update-a-file)
* [[!UICONTROL Hochladen] einer Datei](#upload-a-file)

#### [!UICONTROL Datei löschen]

Dieses Aktionsmodul löscht eine Datei.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td>Geben Sie die eindeutige ID der Datei ein, die das Modul löschen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei abrufen]

Dieses Aktionsmodul lädt eine Datei herunter.

Sie geben die ID der Datei an.

>[!NOTE]
>
>Dieses Modul ist nützlich, um Dateien für nachfolgende Module bereitzustellen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td>Geben Sie die eindeutige ID der Datei ein, die das Modul abrufen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei aktualisieren]

Dieses Aktionsmodul aktualisiert eine Datei.

Sie geben die ID der Datei an.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td>Geben Sie die eindeutige ID der Datei ein, die das Modul aktualisieren soll, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei hochladen]

Dieses Aktionsmodul lädt eine Datei hoch.

Sie geben die Datei an. Sie können auch einen neuen Dateinamen für die Datei angeben.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Ordner]</td> 
   <td> <p>Wählen Sie den Ordner aus, in den Sie die Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Wenn dieses Modul nicht erfolgreich ist, sollten Sie Folgendes beachten:
>
>* Die Größe der Datei kann die maximale Dateigröße für Ihren [!DNL Box] überschreiten oder Sie haben möglicherweise das Speicherkontingent Ihres [!DNL Box]-Kontos ausgeschöpft. Um mehr Speicherplatz zu erhalten, löschen Sie vorhandene Dateien aus [!DNL Box] oder aktualisieren Sie Ihr [!DNL Box].
>* [!DNL Box] lädt nicht mehr als eine Datei mit demselben Namen in einen einzelnen Ordner hoch. Wenn der Zielordner eine Datei mit demselben Namen wie die hochgeladene Datei enthält, wird die Ausführung des Szenarios mit einem Fehler beendet. Um dies zu vermeiden, benennen Sie die Datei um. Wenn Sie die Datei aktualisieren möchten, verwenden Sie das Modul **[!UICONTROL Datei aktualisieren]**.
