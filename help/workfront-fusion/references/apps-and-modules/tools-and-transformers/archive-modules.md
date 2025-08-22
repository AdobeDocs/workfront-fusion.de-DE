---
title: Archivierungsmodule
description: In einem Adobe Workfront Fusion-Szenario können Sie ein Archiv, z. B. eine ZIP-Datei, mit mehreren Anwendungen und Services von Drittanbietern verbinden. Sie können beispielsweise ein Szenario konfigurieren, das
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%

---

# [!UICONTROL Archivieren] Module

In einem Adobe Workfront Fusion-Szenario können Sie ein Archiv, z. B. eine ZIP-Datei, in Ihrem Szenario verwenden, sodass Sie es in Ihren Automatisierungen oder Integrationen verwenden können.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## [!UICONTROL Archivieren] Module und ihre Felder

Beim Konfigurieren von [!UICONTROL Archiv]-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können zusätzliche [!UICONTROL Archivieren]-Felder angezeigt werden, abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktionen](#actions)
* [Aggregatoren](#aggregators)
* [Transformatoren](#transformers)

## Aktionen

### [!UICONTROL Entpacken Sie ein Archiv]

Dieses Aktionsmodul extrahiert eine identifizierte Datei aus einem Archiv.

Das Modul gibt die ID der Datei und aller zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source-Datei]</td> 
   <td> <p>  <p>Quelldatei aus einem vorherigen Modul auswählen oder die Quelldaten zuordnen.</p></p>  </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Beispiel** Rufen Sie die ZIP-Datei aus dem definierten [!DNL Dropbox]-Ordner ab (z. B. „Archive„), extrahieren Sie sie mithilfe des [!UICONTROL Archive]-Moduls und senden Sie die extrahierten Dateien als Anhänge mit dem [!UICONTROL Email]- oder [!DNL Gmail]-Modul an die gewünschte E-Mail-Adresse.

![Beispiel für Dropbox](/help/workfront-fusion/references/apps-and-modules/assets/example-dropbox-350x134.png)

>[!ENDSHADEBOX]

## Aggregatoren

### [!UICONTROL Erstellen eines Archivs]

Dieses Aggregator-Modul fügt die gewünschten Dateien zu einem [!UICONTROL ZIP], GZIP oder [!UICONTROL TAR]-Archiv hinzu.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source-Modul]</td> 
   <td> <p> Wählen Sie das Modul aus, von dem Sie die Dateien abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Typ] </td> 
   <td> <p>Wählen Sie aus, ob Sie Dateien zu einem [!UICONTROL ZIP]-, GZIP- oder einem [!UICONTROL TAR]-Archiv hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Kommentar]</td> 
   <td>Geben Sie einen Kommentar ein, den Sie dem Archiv hinzufügen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Gruppieren nach]</td> 
   <td> <p>Definieren Sie einen Ausdruck, nach dem die aggregierte Ausgabe gruppiert werden soll. Dieser Ausdruck kann ein oder mehrere zugeordnete Elemente enthalten. Die aggregierten Daten werden dann mithilfe des Werts dieses Ausdrucks in Gruppen aufgeteilt. Jede Gruppe gibt als separates Bundle mit einem Schlüssel (dem ausgewerteten Ausdruck) und einem Wert (dem aggregierten Text) aus. Sie können den Schlüssel als Filter in nachfolgenden Modulen verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Verarbeitung nach einer leeren Aggregation anhalten]</td> 
   <td>Wählen Sie diese Option, um das Szenario anzuhalten, wenn keine Ergebnisse vorliegen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Archivname]</td> 
   <td> <p> Geben Sie einen Namen für das erstellte Archiv ein. Keine Erweiterung hinzufügen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Beispiel:** eingehende E-Mails mit dem Modul [!DNL Gmail] > [!UICONTROL E-Mails &#x200B;]. Wenn eine E-Mail empfangen wird, werden ihre Anhänge in einzelne Bundles iteriert, dann in der [!DNL ZIP] archiviert und im definierten Dropbox-Ordner gespeichert.

![Beispiel für Gmail](/help/workfront-fusion/references/apps-and-modules/assets/example-gmail-350x102.png)

>[!ENDSHADEBOX]

## Transformatoren

* [[!UICONTROL Entlüften]](#deflate)
* [[!UICONTROL aufblasen]](#inflate)

### [!UICONTROL Entlüften]

Dieses Transformatormodul komprimiert Binärdaten mit einem Deflationsalgorithmus.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Daten] </td> 
   <td> <p>Geben Sie die Daten, die Sie komprimieren möchten, mit der Deflate-Funktion ein oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL aufblasen]

Dieses Transformatormodul dekomprimiert Binärdaten mithilfe eines Inflationsalgorithmus.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Daten] </td> 
   <td> <p>Geben Sie die Daten, die Sie dekomprimieren möchten, mithilfe der Inflate-Funktion ein oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>
