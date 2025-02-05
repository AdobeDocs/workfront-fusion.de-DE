---
title: SharePoint-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die Microsoft SharePoint Online verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: 5a95b2c191d4e6d8750dc57a47923f416612b4a9
workflow-type: tm+mt
source-wordcount: '2526'
ht-degree: 0%

---

# Microsoft SharePoint Online-Module

In einem [!DNL Adobe Workfront Fusion] können Sie Workflows automatisieren, die Microsoft SharePoint Online verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um Microsoft SharePoint Online-Module verwenden zu können, müssen Sie über ein Microsoft SharePoint Online-Konto verfügen.

## SharePoint-API-Informationen

Der SharePoint-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.14.2</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion] {#connect-microsoft-sharepoint-online-to-workfront-fusion}

* [Verbinden von Microsoft SharePoint Online mit  [!DNL Workfront Fusion] mithilfe eines  [!DNL Microsoft] Kontos](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-a-microsoft-account)
* [Verbinden von Microsoft SharePoint Online mit  [!DNL Workfront Fusion] mithilfe der erweiterten Einstellungen](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-advanced-settings)

### Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion] über ein [!DNL Microsoft]

Sie können Ihr [!DNL Microsoft]-Konto verwenden, um eine Verbindung zu Microsoft SharePoint Online herzustellen. Anweisungen zum Verbinden Ihres [!DNL Sharepoint]-Kontos mit [!DNL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion]  - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion] mithilfe der erweiterten Einstellungen

Um Microsoft SharePoint Online ohne [!DNL Microsoft] mit [!DNL Workfront Fusion] zu verbinden, benötigen Sie eine Client-ID, ein Client-Geheimnis und eine Mandanten-ID.

1. Klicken Sie oben im Feld **Microsoft SharePoint Online** auf **[!UICONTROL Add]**, um das Feld **[!UICONTROL Create a connection]** zu öffnen.

1. (Optional) Ändern Sie die **[!UICONTROL Connection name]**.
1. Klicken Sie auf **[!UICONTROL Show advanced settings]**.
1. Geben Sie die Microsoft SharePoint Online-**[!UICONTROL Client ID]** und -**[!UICONTROL Client Secret]** ein.

1. Klicken Sie auf **[!UICONTROL Continue]**.
1. Geben Sie im angezeigten Anmeldefenster Ihre Anmeldedaten ein, um sich bei der App anzumelden, falls Sie dies noch nicht getan haben.
1. (Bedingt) Wenn eine **[!UICONTROL Allow]** Schaltfläche angezeigt wird, klicken Sie darauf, um die App mit [!DNL Workfront Fusion] zu verbinden.

## Microsoft SharePoint Online-Module und ihre Felder

Beim Konfigurieren von Microsoft SharePoint Online-Modulen zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service werden möglicherweise auch zusätzliche Microsoft SharePoint Online-Felder angezeigt. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Laufwerkselement](#drive-item)
* [Element](#item)
* [Liste](#list)
* [Seite (Beta)](#page-beta)
* [Site](#site)
* [Sonstige](#other)

### Laufwerkselement

* [Erstellen einer Datei](#create-a-file)
* [Erstellen eines Ordners](#create-a-folder)
* [Datei abrufen](#get-a-file)
* [Überwachen von Ordnerelementen](#watch-folder-items)

#### Erstellen einer Datei

Dieses Modul gibt Änderungen zurück, die in SharePoint vorgenommen wurden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Wählen Sie aus, wie Sie den Speicherort des Ordners identifizieren möchten, in dem Sie Änderungen abrufen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie den <strong>[!UICONTROL Site ID]</strong>, die <strong>[!UICONTROL Drive ID]</strong> und den <strong>[!UICONTROL Folder ID]</strong> des Speicherorts ein, an dem Sie die Datei erstellen möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Wählen Sie den Speicherort aus, an dem Sie die Datei erstellen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
      <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p>
  </tr>  </tbody> 
</table>

#### Erstellen eines Ordners

Dieses Aktionsmodul erstellt einen neuen Ordner in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Wählen Sie aus, wie Sie den Speicherort des zu erstellenden Ordners identifizieren möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie den <strong>[!UICONTROL Site ID]</strong>, die <strong>[!UICONTROL Drive ID]</strong> und die <strong>[!UICONTROL Folder ID]</strong> des Speicherorts ein, an dem Sie den Ordner erstellen möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Wählen Sie den Speicherort aus, an dem Sie den Ordner erstellen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder name]</td> 
   <td>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie ihn zu.</td> 
  </tr>
  </tbody> 
</table>

#### Datei abrufen

Dieses Aktionsmodul ruft die angegebene SharePoint-Datei ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Wählen Sie aus, wie Sie den Speicherort der Datei identifizieren möchten, die Sie erhalten möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> und <strong>[!UICONTROL File ID]</strong> für die Datei ein, die Sie abrufen möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Speicherort der Datei auswählen. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Überwachen von Ordnerelementen

Dieses Ordnermodul startet ein Trigger, wenn ein Element in einem ausgewählten Ordner aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Wählen Sie aus, wie Sie den Speicherort der Datei identifizieren möchten, die Sie erhalten möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> und <strong>[!UICONTROL folder ID]</strong> in die angezeigten Felder ein oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Wählen Sie den Speicherort des Ordners aus, den Sie überwachen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl an Elementen ein, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben sollen.</td> 
  <tr>
  </tr>
</tbody> 
</table>

### Element

* [[!UICONTROL Copy an item]](#copy-an-item)
* [[!UICONTROL Create an item]](#create-an-item)
* [[!UICONTROL Delete an item]](#delete-an-item)
* [[!UICONTROL Get an Item]](#get-an-item)
* [[!UICONTROL List Items]](#list-items)
* [[!UICONTROL Move Item]](#move-an-item)
* [[!UICONTROL Update an item]](#update-an-item)
* [[!UICONTROL Watch Items] (geplant)](#watch-items-scheduled)


#### [!UICONTROL Copy an Item]

Dieses Aktionsmodul kopiert ein vorhandenes Element in eine SharePoint-Liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Site-, Laufwerk- und Ordner-IDs eingeben</td> 
   <td> <p>Wählen Sie aus, wie Sie die Site und das Laufwerk identifizieren möchten, die das zu kopierende Element enthalten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong> und <strong>[!UICONTROL Item ID]</strong> des zu kopierenden Elements ein oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>Wählen Sie im Feld Elementtyp aus, ob Sie ein Feld oder einen Ordner verschieben möchten.  Wählen Sie die Site aus, die das zu kopierende Element enthält, klicken Sie dann auf die Liste und wählen Sie das Element aus. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> Geben Sie die ID des Ordners ein, in den Sie das Element kopieren möchten, oder ordnen Sie sie zu. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>Geben Sie einen Namen für die neue Kopie des Elements ein oder ordnen Sie ihn zu. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an item]

Dieses Aktionsmodul erstellt ein neues Element in einer SharePoint-Liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Create an Item]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Site identifizieren und steuern möchten, wo Sie ein Element erstellen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong> und <strong>[!UICONTROL List ID]</strong> ein, in denen Sie das Element erstellen möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Site aus, die die Liste enthält, in der Sie ein Element erstellen möchten, und wählen Sie dann die Liste aus. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Klicken Sie für jedes Feld, das Sie für das neue Element festlegen möchten, auf <b>Element hinzufügen</b> und geben Sie den Schlüssel des Felds (der das Feld identifiziert) und den Wert ein, den das neue Element für dieses Feld haben soll.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an item]

Dieses Aktionsmodul löscht ein vorhandenes Element in einer SharePoint-Liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Site und Liste identifizieren möchten, die das zu löschende Element enthalten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> und <strong>[!UICONTROL Item ID]</strong> des Elements ein, das Sie löschen möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Site aus, die das zu löschende Element enthält, wählen Sie dann die Liste aus und wählen Sie das Element aus. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Item]

Dieses Aktionsmodul gibt die Daten eines angegebenen Elements zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get an Item]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Site und Liste identifizieren möchten, die das zu abrufende Element enthalten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> und <strong>[!UICONTROL Item ID]</strong> des Elements ein, für das Sie Daten zurückgeben möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Site aus, die die Liste enthält, aus der Sie ein Element abrufen möchten, wählen Sie dann die Liste aus und wählen Sie dann das Element aus. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Items]

Dieses Aktionsmodul ruft eine Liste aller Elemente in einer angegebenen Liste ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Items]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Liste identifizieren möchten, aus der Sie Elemente abrufen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong> und <strong>[!UICONTROL List ID]</strong> für die Liste ein, für die Sie Elemente auflisten möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Site aus, die die Liste enthält, von der Sie Elemente abrufen möchten, und wählen Sie dann die Liste aus. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Elementen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Item]

Dieses Aktionsmodul kopiert ein vorhandenes Element in eine SharePoint-Liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Site-, Laufwerk- und Ordner-IDs eingeben</td> 
   <td> <p>Wählen Sie aus, wie Sie die Site und Liste identifizieren möchten, die das zu verschiebende Element enthalten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> und <strong>[!UICONTROL Item ID]</strong> für das Element ein, das Sie verschieben möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>Wählen Sie im Feld Elementtyp aus, ob Sie ein Feld oder einen Ordner verschieben möchten. Wählen Sie die Site aus, die das zu kopierende Element enthält, klicken Sie dann auf die Liste und wählen Sie das Element aus. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> Geben Sie die ID des Ordners ein, in den Sie das Element verschieben möchten, oder ordnen Sie sie zu. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>Geben Sie einen Namen für das verschobene Element ein oder ordnen Sie ihn zu. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an item]

Dieses Aktionsmodul aktualisiert ein vorhandenes Element in einer SharePoint-Liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Site und Liste identifizieren möchten, die das zu aktualisierende Element enthalten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> und <strong>[!UICONTROL Item ID]</strong> des Elements ein, das Sie aktualisieren möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Site aus, die das zu aktualisierende Element enthält, wählen Sie dann die Liste aus und wählen Sie das Element aus. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Klicken Sie für jedes Feld, das Sie für das neue Element aktualisieren möchten, auf <b>Element hinzufügen</b> und geben Sie den Schlüssel des Felds (der das Feld identifiziert) und den neuen Wert ein, den das Element für dieses Feld haben soll.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Items] (geplant)

Dieses Trigger-Modul startet ein Szenario, wenn ein Element erstellt oder geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Wählen Sie aus, ob Listen nach Erstellungszeit (neue Elemente) oder nach Änderungszeit (aktualisierte Elemente) angezeigt werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Website und die Liste identifizieren möchten, die Sie überwachen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong> und <strong>[!UICONTROL List ID]</strong> ein, die Sie beobachten möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Wählen Sie die Website aus, die Sie beobachten möchten, und klicken Sie dann auf die Liste. Mit diesen Dropdown-Listen werden nur die folgenden Sites abgerufen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Elementen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Liste

* [[!UICONTROL Create a List]](#create-a-list)
* [[!UICONTROL Get a List]](#get-a-list)
* [[!UICONTROL List Lists]](#list-lists)
* [[!UICONTROL Watch Lists]](#watch-lists)

#### [!UICONTROL Create a List]

Dieses Aktionsmodul erstellt eine neue Liste in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Site ID]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Site identifizieren möchten, auf der Sie eine Liste erstellen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong> ein, in der Sie eine Liste erstellen möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Website aus, auf der Sie eine Liste erstellen möchten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display Name]</td> 
   <td>Geben Sie einen Namen für die neue Liste ein oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Geben Sie eine Beschreibung für die neue Liste ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Add Columns]</td> 
   <td>Klicken Sie für jede Spalte, die Sie für die neue Liste festlegen möchten, auf <b>Element hinzufügen </b> geben Sie einen <strong>[!UICONTROL Name]</strong> für das Feld ein und wählen Sie die <strong>[!UICONTROL Type]</strong> aus, die die neue Spalte haben soll.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a List]

Dieses Aktionsmodul gibt die Daten einer angegebenen Liste zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a List]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Site und Liste identifizieren möchten, die das zu abrufende Element enthalten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong> und (<strong>-ID) ein</strong> die Sie zurückgeben möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Site aus, die die Liste enthält, die Sie abrufen möchten, und wählen Sie dann die Liste aus. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Lists]

Dieses Aktionsmodul ruft eine Liste aller Elemente in einer angegebenen Site ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Lists]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Website identifizieren möchten, von der Sie Listen abrufen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong> ein, die die Listen enthält, die Sie zurückgeben möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Site aus, die die Listen enthält, die Sie abrufen möchten. Mit der Dropdown-Liste werden nur die Websites abgerufen, denen Sie folgen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Listen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Lists]

Dieses Trigger-Modul startet ein Szenario, wenn eine Liste erstellt oder geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Wählen Sie aus, ob Listen nach Erstellungszeit (neue Elemente) oder nach Änderungszeit (aktualisierte Elemente) angezeigt werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site ID]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Website identifizieren möchten, die Sie auf Listen überwachen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong> ein, für die Sie Listen anzeigen möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Wählen Sie die Website aus, die Sie beobachten möchten. Mit der Dropdown-Liste wird nur die Site abgerufen, der Sie folgen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Listen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Seite (Beta)

>[!NOTE]
>
>APIs in der `beta` Version in [!DNL Microsoft Graph] können sich ändern. Die Verwendung dieser APIs in Produktionsanwendungen wird nicht unterstützt.

#### [!UICONTROL Get a Page]

Dieses Aktionsmodul gibt die Daten einer angegebenen Seite zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Page]</td> 
   <td> <p>Wählen Sie aus, wie Sie die abzurufende Seite identifizieren möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Page ID]</strong> und <strong>[!UICONTROL Site ID]</strong> ein oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Site aus, die die abzurufende Seite enthält, und wählen Sie dann die Seite aus.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Site

* [[!UICONTROL Get a Site]](#get-a-site)
* [[!UICONTROL Search Sites]](#search-sites)

#### [!UICONTROL Get a Site]

Dieses Aktionsmodul gibt die Daten einer angegebenen Site zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Site]</td> 
   <td> <p>Wählen Sie aus, wie Sie die abzurufende Seite identifizieren möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong> ein oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Site aus, die Sie abrufen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Sites]

Dieses Aktionsmodul sucht nach Sites anhand eines von Ihnen angegebenen Parameters.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword of Display Name]</td> 
   <td> <p>Geben Sie den Suchbegriff ein, nach dem Sie die Sites suchen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Sites ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstige

* [Änderungen abrufen](#get-changes)
* [Durchführen eines API-Aufrufs](#make-an-api-call)
* [Ereignisse ansehen](#watch-events)

#### Änderungen abrufen

Dieses Modul ruft Ergänzungen, Aktualisierungen und Löschungen ab, die im SharePoint-Ordner vorgenommen wurden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Site und das Laufwerk identifizieren möchten, die das zu aktualisierende Element enthalten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong> und <strong>[!UICONTROL Folder ID]</strong> in die angezeigten Felder ein oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Wählen Sie die Site aus, die das zu aktualisierende Element enthält, wählen Sie dann das Laufwerk und dann den Ordner aus. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> Das Token gibt an, ab welchem Punkt das Modul mit dem Abrufen von Änderungen beginnen soll.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Mit diesem Modul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft SharePoint Online-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Microsoft SharePoint Online mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://graph.microsoft.com</code> ein. Beispiel:<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Beispiel: <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Wählen Sie den Datentyp aus, den Sie in Ihrem API-Aufruf senden möchten.</td> 
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

#### Ereignisse ansehen

Dieses Instant-Trigger-Modul startet ein Szenario, wenn ein Element in SharePoint hinzugefügt, aktualisiert oder gelöscht wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
  <!--
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Wählen Sie einen vorhandenen Webhook aus oder klicken Sie auf Hinzufügen und geben Sie die Verbindung ein, um einen neuen Webhook zu erstellen.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
