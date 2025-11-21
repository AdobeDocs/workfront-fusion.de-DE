---
title: Adobe Substance-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die verwenden [!DNL Adobe Substance] und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
source-git-commit: 2e44c89d487100b3245b40f6927185a0ff12ef2f
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 25%

---

# [!DNL Adobe Substance] Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Adobe Substance] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Paket für Adobe Workfront Workflow und Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: keine Workfront Fusion-Lizenz erforderlich</p>
   <p>Connector-basiert (alt): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Adobe Workfront Fusion erworben werden.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Angaben in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Bevor Sie den [!DNL Adobe Substance]-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein aktives [!DNL Adobe Substance] verfügen.



## [!DNL Adobe Substance]-Module und ihre Felder

Beim Konfigurieren von [!DNL Adobe Substance]-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Dienst weitere [!DNL Adobe Substance]-Felder angezeigt werden. Ein Sternchen neben dem Feldnamen in einem Modul zeigt ein erforderliches Feld an.

Wenn die Schaltfläche für Zuordnung über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Verbundwerkstoffe](#composites)
* [Szenen](#scenes)
* [Leerzeichen](#spaces)

### Verbundwerkstoffe

#### 3D-Objekt-Composite generieren

Dieses Aktionsmodul generiert Inhalte für ein 3D-Composite, das das ausgewählte Hero-Asset enthält.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Substance]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Andere Felder</td> 
   <td>Konfigurieren Sie weitere Felder nach Bedarf. Weitere Informationen zu Feldern finden Sie in der <a href="https://s3d.adobe.io/docs#/operations/v1/composites/compose">Adobe Substance API-Dokumentation</a>.</td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">Camera name</td> 
   <td>Enter or map the name of an existing camera that has been previously defined in the source 3D file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Content class</td> 
   <td>Select whether you want the composite to have the style of art or of a photo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enable ground plane</td> 
   <td>Enable this to enable the auto-generated ground plane under the hero asset. This is useful if the 3D scene contains only a hero asset, without additional elements.</td> 
  </tr> -->
 </tbody> 
</table>

### Szenen

* [Konvertieren von 3D-Dateien](#convert-3d-files)
* [3D-Szene erstellen](#create-3d-scene)
* [3D-Szene beschreiben](#describe-3d-scene)
* [3D-Objekt rendern](#render-3d-object)
* [3D-Objekt rendern (Basisversion)](#render-3d-object-basic-version)

#### Konvertieren von 3D-Dateien

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Substance]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Format</td> 
   <td>Wählen Sie das Format aus, in das Sie die Datei konvertieren möchten.</td> 
  </tr> 
<tr> 
   <td role="rowheader">Modelleinstiegspunkt</td> 
   <td>Die Konvertierung erfolgt in der Regel anhand der ersten Datei, die als gültiges 3D-Modell gilt. Definieren Sie diesen Einstiegspunkt, um mehrere Optionen zu unterscheiden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Quellen</td> 
   <td>Klicken Sie für jede Datei, die Sie konvertieren möchten, auf <b> Element hinzufügen </b> geben Sie die Dateiinformationen ein.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D-Szene erstellen

Dieses Aktionsmodul erstellt eine Szene mit den von Ihnen angegebenen Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Substance]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Codierung</td> 
   <td>Wählen Sie den Dateityp für die Szene.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dateiname</td> 
   <td>Geben Sie einen Namen für die Ausgabedatei ein oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Andere Felder</td> 
   <td>Konfigurieren Sie weitere Felder nach Bedarf. Weitere Informationen zu Feldern finden Sie in der <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/assemble">Adobe Substance API-Dokumentation</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Quellen</td> 
   <td>Klicken Sie für jede Datei, die Sie verwenden möchten, auf <b> Element hinzufügen </b> geben Sie die Dateiinformationen ein.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D-Szene beschreiben

Dieses Aktionsmodul ruft Informationen über 3D-Szeneninhalte ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Substance]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Szenendatei</td> 
   <td>Geben Sie den Pfad zur Szenendatei ein, die Sie beschreiben möchten, oder mappen Sie ihn.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Quellen</td> 
   <td>Klicken Sie für jede Datei, die Sie beschreiben möchten, auf <b> Element hinzufügen </b> geben Sie die Dateiinformationen ein.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D-Objekt rendern

Dieses Aktionsmodul rendert ein Bild einer Szene.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Substance]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
   <td role="rowheader">Andere Felder</td> 
   <td>Konfigurieren Sie weitere Felder nach Bedarf. Weitere Informationen zu Feldern finden Sie in der <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render">Adobe Substance API-Dokumentation</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Quellen</td> 
   <td>Klicken Sie für jede Datei, die Sie verwenden möchten, auf <b> Element hinzufügen </b> geben Sie die Dateiinformationen ein.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D-Objekt rendern (Basisversion)

Dieses Aktionsmodul rendert ein Bild einer Szene, hat jedoch weniger Optionen als das Modul 3D-Objekt rendern .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Substance]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
   <td role="rowheader">Andere Felder</td> 
   <td>Konfigurieren Sie weitere Felder nach Bedarf. Weitere Informationen zu Feldern finden Sie in der <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render-basic">Adobe Substance API-Dokumentation</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Quellen</td> 
   <td>Klicken Sie für jede Datei, die Sie verwenden möchten, auf <b> Element hinzufügen </b> geben Sie die Dateiinformationen ein.</td> 
  </tr> 
 </tbody> 
</table>

### Leerzeichen

#### Platz erstellen

Mit diesem Aktionsmodul können Sie Dateien hochladen und vorübergehend speichern.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Substance]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Dateiname</td> 
   <td>Geben Sie den Namen der Datei ein, die hochgeladen wird, oder ordnen Sie ihn zu.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Dateidaten</td> 
   <td>Binärdaten der Datei eingeben oder zuordnen.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name</td> 
   <td>Geben Sie einen Namen für den mehrteiligen Formularwert ein oder mappen Sie ihn.</td> 
  </tr> 
 </tbody> 
</table>
