---
title: Microsoft OneDrive für Geschäftsmodule
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die  [!DNL Microsoft OneDrive for Business] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 657bea46-064e-4333-8e86-81678bb1c3bd
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---

# [!DNL Microsoft OneDrive for Business]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Microsoft OneDrive for Business] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

## Voraussetzungen

Um [!DNL Microsoft OneDrive for Business] mit [!DNL Adobe Workfront Fusion] verwenden zu können, benötigen Sie ein [!DNL Microsoft].

## Verbinden des [!DNL Microsoft OneDrive for Business]-Services mit [!DNL Workfront Fusion]

Anweisungen zum Verbinden Ihres [!DNL Microsoft OneDrive for Business]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung mit [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
>
>Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.

## [!DNL Microsoft OneDrive for Business] Module und ihre Felder

Beim Konfigurieren [!DNL Microsoft OneDrive for Business] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Microsoft OneDrive for Business] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)

### Auslöser

* [[!UICONTROL Dateien ansehen]](#watch-files)
* [[!UICONTROL Ordner ansehen]](#watch-folders)

#### [!UICONTROL Dateien ansehen]

Dieses Dateimodul wird aktiviert, wenn eine neue Trigger-Datei in einem überwachten Ordner hinzugefügt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Laufwerk-ID]</p> </td> 
   <td> <p>Wählen Sie das Laufwerk aus, das Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Ordner]</td> 
   <td> <p> Wählen Sie den Ordner aus, den Sie beobachten möchten. In einem Szenario können Sie nur einen Ordner überwachen.</p> <p>Tipp: Um mehrere Ordner anzusehen, erstellen Sie für jeden Ordner ein unabhängiges Szenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL, die ich beobachten möchte]</p> </td> 
   <td> <p>Wählen Sie aus, ob nur neue Dateien und alle Änderungen oder nur neue Dateien angezeigt werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Zeilen]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Ergebnissen fest, die das Modul während eines Zyklus zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ordner ansehen]

Dieses Ordnermodul wird aktiviert, wenn dem überwachten Trigger ein neuer Ordner hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Laufwerk-ID]</p> </td> 
   <td> <p>Wählen Sie das Laufwerk aus, das Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Ordner]</td> 
   <td> <p> Wählen Sie den Ordner aus, den Sie beobachten möchten. In einem Szenario können Sie nur einen Ordner überwachen.</p> <p>Tipp: Um mehrere Ordner zu verfolgen, erstellen Sie für jeden Ordner ein unabhängiges Szenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL, die ich beobachten möchte]</p> </td> 
   <td> <p>Wählen Sie aus, ob nur neue Ordner und alle Änderungen oder nur neue Ordner angezeigt werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Zeilen]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Ergebnissen fest, die das Modul während eines Zyklus zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Erstellen eines Ordners]](#create-a-folder)
* [[!UICONTROL Datei löschen]](#delete-a-file)
* [[!UICONTROL Löschen eines Ordners]](#delete-a-folder)
* [[!UICONTROL Datei abrufen]](#get-a-file)
* [[!UICONTROL Erhalten Sie einen Freigabe-Link]](#get-a-sharing-link)
* [[!UICONTROL Datei hochladen]](#upload-a-file)

#### [!UICONTROL Erstellen eines Ordners]

Erstellt einen Ordner im angegebenen übergeordneten Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><strong>[!UICONTROL-Verbindung]</strong> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Laufwerk-ID]</strong> </td> 
   <td> <p>Wählen Sie das Laufwerk aus, auf dem Sie einen neuen Ordner erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL-Ordner]</strong> </td> 
   <td> <p>Wählen Sie den Ordner aus, in dem Sie einen neuen Ordner erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Ordnername]</strong> </td> 
   <td>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei löschen]

Dieses Aktionsmodul verschiebt die angegebene Datei in den Papierkorb.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, von dem Sie eine Datei löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datei-ID]</td> 
   <td> <p>Geben Sie die ID der Datei ein, die Sie löschen möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Löschen eines Ordners]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, von dem Sie eine Datei löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordner-ID]</td> 
   <td> <p>Geben Sie die ID des Ordners ein, den Sie löschen möchten, oder ordnen Sie sie zu. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei abrufen]

Dieses Aktionsmodul ruft die Datei mit der angegebenen ID ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, von dem Sie eine Datei abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datei-ID]</td> 
   <td> <p>Geben Sie die ID der Datei ein, die Sie abrufen möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erhalten Sie einen Freigabe-Link]

Dieses Modul ruft einen Link ab, den Sie freigeben können, um Zugriff auf die angegebene Datei zu gewähren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, auf das Sie eine Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL EINGABETASTE]</td> 
   <td> <p>Wählen Sie aus, ob Sie eine Datei anhand der Datei-ID oder des Dateipfads auswählen möchten. Geben Sie die Datei-ID oder den Pfad in das Feld ein, das angezeigt wird.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Berechtigungstyp]</p> </td> 
   <td> <p>Wählen Sie aus, ob Personen, die den Link erhalten, Lese-/Schreibberechtigungen oder Leseberechtigungen erhalten sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Umfang]</td> 
   <td> <p> Wählen Sie aus, ob die Datei für alle Personen zugänglich sein soll, die über den Link verfügen, oder nur für Mitglieder Ihres Unternehmens.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei hochladen]

Dieses Aktionsmodul lädt eine Binär- oder Textdatei in einen angegebenen Ordner hoch

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Laufwerk-ID]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, auf das Sie eine Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den Ordner im Laufwerk aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source-Datei]</p> </td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Wenn die gleichnamige Datei existiert]</td> 
   <td> <p> Wählen Sie aus, was Sie tun möchten, wenn bereits eine Datei mit demselben Namen wie die Datei vorhanden ist, die Sie hochladen möchten.</p> 
    <ul> 
     <li>[!UICONTROL Vorhandene Datei ersetzen]</li> 
     <li>[!UICONTROL Neue Datei umbenennen]</li> 
     <li>[!UICONTROL Mit Fehler beenden]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
