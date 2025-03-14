---
title: Bildmodule
description: Mit Adobe Workfront Fusion-Bildmodulen können Sie Informationen zu einem bestimmten Bild abrufen (Abmessungen, Typ usw.), ein Bild in ein anderes Dateiformat konvertieren und die Bildgröße direkt ändern.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---

# Bildmodule

[!DNL Adobe Workfront Fusion] [!UICONTROL Image]-Module können Sie Informationen zu einem bestimmten Bild abrufen (Abmessungen, Typ usw.), ein Bild in ein anderes Dateiformat konvertieren und die Größe des Bildes direkt ändern.

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
   <p>Keine Workfront Fusion-Lizenzanforderung</p>
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
