---
title: Bildmodule
description: Mit Adobe Workfront Fusion-Bildmodulen können Sie Informationen zu einem bestimmten Bild abrufen (Abmessungen, Typ usw.), ein Bild in ein anderes Dateiformat konvertieren und die Bildgröße direkt ändern.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Bildmodule

Mit [!UICONTROL  (Image]-Modulen von Adobe Workfront Fusion können Sie Informationen zu einem bestimmten Bild abrufen (Abmessungen, Typ usw.), ein Bild in ein anderes Dateiformat konvertieren und die Bildgröße direkt ändern.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## [!UICONTROL Image]-Module und ihre Felder

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

* [[!UICONTROL Format konvertieren]](#convert-a-format)
* [[!UICONTROL Extrahieren von Metadaten]](#extract-metadata)
* [[!UICONTROL Größe ändern]](#resize)

### [!UICONTROL Format konvertieren]

Dieses Transformatormodul ändert das Format einer Bilddatei. Dieses Modul ist mit den folgenden Formaten kompatibel:

* PNG
* JPG
* GIF
* BMP

Sowohl die Quelldatei als auch die Ausgabe müssen in einem der folgenden Formate vorliegen. Beispielsweise kann das Modul [!UICONTROL Bild] > [!UICONTROL Format konvertieren] eine PNG-Datei in eine BMP-Datei oder eine BMP in eine JPG-Datei umwandeln.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabeformat]</td> 
   <td>Wählen Sie das Format aus, in das das Modul die Quelldatei konvertieren soll. </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Extrahieren von Metadaten]

Dieses Transformatormodul gibt grundlegende Informationen über ein Modul zurück.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Größe ändern]

Dieses Transformatormodul ändert die Höhe und Breite eines Bildes entsprechend den von Ihnen angegebenen Kriterien.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ich möchte]</td> 
   <td>Wählen Sie aus, ob Sie das Verhältnis Höhe/Breite beibehalten oder die Bemaßungen auf eine bestimmte Höhe und Breite ändern möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL nach]</td> 
   <td> <p>Wählen Sie aus, wie das Modul die neue Bildgröße bestimmen soll. Dieses Feld wird angezeigt, wenn Sie ausgewählt haben, dass das Verhältnis von Höhe zu Breite im Feld Ich möchte beibehalten werden soll. Andere Felder werden je nach Auswahl in diesem Feld angezeigt.</p> 
    <ul> 
     <li> <p>[!UICONTROL Maximale Breite]</p> <p>Reduziert ein Bild auf eine angegebene Breite. Die Höhe wird automatisch berechnet.</p> </li> 
     <li> <p>[!UICONTROL Maximale Höhe]</p> <p>Reduziert ein Bild auf eine angegebene Höhe. Die Breite wird automatisch berechnet.</p> </li> 
     <li> <p>[!UICONTROL Maximale Höhe oder Breite]</p> <p>Verringert ein Bild so, dass seine Höhe und Breite die angegebenen Werte nicht überschreiten. Da diese Option das Verhältnis von Höhe zu Breite beibehält, kann eine der Bemaßungen kleiner als angegeben sein. Wenn beispielsweise Höhe und Breite als 40 angegeben sind, wird ein Bild mit einer Größe von 400 x 300 auf 40 x 30 reduziert.</p> </li> 
     <li> <p>[!UICONTROL Mindestbreite]</p> <p>Vergrößert ein Bild auf die angegebene Breite. Die Höhe wird automatisch berechnet.</p> </li> 
     <li> <p>[!UICONTROL Mindesthöhe]</p> <p>Vergrößert ein Bild auf eine angegebene Höhe. Die Breite wird automatisch berechnet.</p> </li> 
     <li> <p>[!UICONTROL Mindesthöhe oder -breite]</p> <p>Vergrößert ein Bild so, dass seine Höhe und Breite nicht kleiner sind als die angegebenen Werte. Da diese Option das Verhältnis von Höhe zu Breite beibehält, kann eine der Bemaßungen größer als angegeben sein. Wenn beispielsweise Höhe und Breite als 300 angegeben sind, wird ein Bild im Format 40x30 auf 400x300 vergrößert.</p> </li> 
     <li> <p>[!UICONTROL Prozent]</p> <p>Ändert die Bildgröße um einen Prozentsatz basierend auf dem von Ihnen angegebenen Wert. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Breite]</td> 
   <td>Geben Sie die gewünschte Breite des skalierten Bildes in Pixel ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Höhe]</td> 
   <td>Geben Sie die gewünschte Höhe des skalierten Bildes in Pixel ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Änderung nach Prozentsatz]</td> 
   <td>Wenn Sie das Bild nach Prozentsatz ändern möchten, geben Sie den Prozentsatz ein, nach dem Sie das Bild ändern möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

## Fehlerbehebung

### Aktion mit Fehler beendet

Eine Aktion kann aus einem der folgenden Gründe mit einem Fehler beendet werden:

* Die empfangenen Daten liegen nicht im Format JPG/GIF/PNG/BMP vor
* Die maximale Breite/Höhe wurde beim Ändern der Bildabmessungen überschritten. Die Bildgröße darf 3840 Pixel Breite und 2160 Pixel Höhe nicht überschreiten
* Die maximal zulässige Größe eines Bildes wurde beim Ändern der Abmessungen oder des Formats des Bildes überschritten.
