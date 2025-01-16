---
title: Elementdatentypen
description: Ihre  [!DNL Adobe Workfront Fusion]  können die unten aufgeführten Elementtypen in einem Bundle enthalten.
author: Becky
feature: Workfront Fusion
exl-id: 3ad65959-5c19-4727-bc9d-4ff1d238ad8b
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Elementdatentypen

Sie können die unten aufgeführten Elementtypen in einem Bundle enthalten.

Informationen dazu, welche Elementtypen [!DNL Workfront Fusion] Konvertierungen untereinander ermöglichen, finden Sie unter [Typzwang](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Text</p> </td> 
   <td> <p>Der häufigste Elementtyp. Bei einigen Textelementen prüft [!DNL Adobe Workfront Fusion], ob die maximal oder minimal zulässige Länge erreicht wird oder ob das Element eine Formatvalidierung (E-Mail, URL oder Dateiname) durchführt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Zahl</p> </td> 
   <td> <p>Bei einigen numerischen Elementen können [!DNL Workfront Fusion] die Eingabe für einen bestimmten Bereich (den minimal oder maximal zulässigen Wert) überprüfen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Boolesch (ja/nein)</p> </td> 
   <td> <p>Dieser Typ wird für Elemente mit nur zwei möglichen Werten verwendet: true oder false. </p> <p>Beim Festlegen von Modulen kann der boolesche Typ in zwei verschiedenen Formen angezeigt werden:</p> 
    <ul> 
     <li> <p>Das Kontrollkästchen Pflichtfeld wird angezeigt, wenn das Feld Pflichtfeld ist und ausgefüllt werden muss.</p> <p> <img src="assets/boolean-checkbox-350x158.jpg" style="width: 350;height: 158;"> </p> </li> 
     <li> <p>Optionale Felder, die leer gelassen werden können, werden als Auswahlfeld angezeigt, sodass aus drei Werten ausgewählt werden kann: <code>Yes</code>, <code>No</code> und <code>Not defined</code> (Standard).</p> <p> <img src="assets/boolean-convert-file-350x129.jpg" style="width: 350;height: 129;"> </p> </li> 
    </ul> <p>Sie können auf <strong>[!UICONTROL Map]</strong> klicken, wenn Sie den Wert einem Element aus einem anderen Modul zuordnen müssen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Datum</p> </td> 
   <td> <p>Datumsangaben werden im ISO 8601-Datumsformat eingegeben, z. B. <code>2015-09-18T11:58Z</code>. Sie können die Zeitzone in Ihren Profileinstellungen ändern. </p> <p>Wenn Sie auf ein Feld klicken, für das ein Datum erforderlich ist, wird in den Moduleinstellungen ein Popup-Kalender angezeigt. Bei einigen Elementen ist keine Zeit erforderlich.</p> <p>Die Werte von Datumselementen werden mithilfe der in Ihrem Profil ausgewählten lokalen Zeitzone und Web-Zeitzone formatiert. Sie können die ISO 8601-Version des Werts eines Datumselements anzeigen, indem Sie den Mauszeiger über das Element bewegen.</p> <p>Hinweis: Wenn der ISO-Wert nicht angezeigt wird, ist das Element wahrscheinlich Text, kein Datum.</p> <p>Die Uhrzeit wird im <code>hours:minutes:seconds</code> Format eingegeben, z. B. <code>14:03:52</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Puffer (Binärdaten)</p> </td> 
   <td> <p>Dateiinhalte werden normalerweise als Inhalte vom Typ „Puffer“ gesendet (Bildinhalte, Videodateien und andere). In einigen Fällen sind in diesem Typ Textdaten enthalten (z. B. eine Textdatei). [!DNL Workfront Fusion] ist in der Lage, Textdaten im Binärcode automatisch in Text und Text in Textdaten im Binärcode zu konvertieren. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/map-data/map-files.md" class="MCXref xref">Zuordnungsdateien</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Sammlung</p> </td> 
   <td> <p>Eine Sammlung ist ein Element, das aus mehreren Unterelementen besteht. Das Absenderelement in einer E-Mail-Nachricht ist ein Beispiel für eine Sammlung: Es enthält den Absendernamen (Texttyp) und die Absender-E-Mail-Adresse (Texttyp).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Auswählen (Menü)</p> </td> 
   <td> <p>Bei der Konfiguration der Moduleinstellungen können Sie aus mehreren Elementen desselben Typs auswählen. Ein Beispiel hierfür ist das Menü Ordnerauswahl in den Einstellungen für die [!DNL Dropbox]. </p> <p>Beim Festlegen von Modulen kann das Auswahlmenü in zwei Formen angezeigt werden:</p> <p> <p>Wenn die Mehrfachauswahl möglich ist, werden mehrere Elemente mit Kontrollkästchen angezeigt.</p> <p> <img src="assets/image-kb-type-list-multi-350x232.jpg" style="width: 350;height: 232;"> </p> </p> <p>Wenn nur eine Option möglich ist, wird ein Dropdown-Menü angezeigt.</p> <p> <img src="assets/select-menu-dropdown-350x130.jpg" style="width: 350;height: 130;"> </p> <p>Wenn Sie ein Element aus einem anderen Modul zuordnen müssen, verwenden Sie die Schaltfläche <strong>Map</strong>. Mit dieser Schaltfläche wird ein Textfeld anstelle des Auswahlmenüs geöffnet. Weitere Informationen zur Zuordnung finden Sie unter <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md" class="MCXref xref">Zuordnungsübersicht</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Array</p> </td> 
   <td> <p>Sie können den Array-Typ verwenden, um mit mehreren Werten desselben Typs zu arbeiten, einschließlich Sammlungen. Ein Beispiel sind die [!UICONTROL Email]: Sie geben ein Array von Anlagen zurück und jede Anlage enthält Namen, Inhalt, Größe usw. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/map-data/map-an-array.md" class="MCXref xref">Zuordnen eines Arrays oder Array-Elements</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Validierung</p> </td> 
   <td> <p>[!DNL Workfront Fusion] kann für jeden Elementtyp eine Validierung durchführen. Wenn ein Element die Validierung nicht besteht, stoppt das Modul die Verarbeitung aufgrund eines Datenfehlers. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/errors/error-processing.md" class="MCXref xref">Fehlertypen </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
