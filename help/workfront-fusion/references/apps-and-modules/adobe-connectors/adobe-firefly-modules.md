---
title: Adobe Firefly-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Adobe Firefly] verwenden, und diese mit verschiedenen Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
TQID: https://experienceleague.adobe.com/1hI4NuUl2eEAgWyXRKLHQ3-6MM9-2tFyujGbRfHSBmU
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 3886
ht-degree: 15%

---

# [!DNL Adobe Firefly]-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Adobe Firefly] verwenden, und diese mit verschiedenen Anwendungen und Services von Drittanbietern verbinden.

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
   <td> <p>Ein beliebiges Adobe Workfront Workflow- und Adobe Workfront Automation and Integration-Paket</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: keine Workfront Fusion-Lizenz erforderlich</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Bevor Sie den [!DNL Adobe Firefly]-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein aktives [!DNL Adobe Firefly] verfügen.

## Adobe Firefly-API-Informationen

Der Adobe Firefly-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.4.24</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung zu den [!DNL Adobe Firefly]

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe Firefly]-Module:

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
          <p>Geben Sie einen Namen für die Verbindung ein.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>Wählen Sie aus, ob eine Verbindung zu einem Service-Konto oder einem persönlichen Konto hergestellt werden soll.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre [!UICONTROL Adobe] [!UICONTROL Client-ID] ein. Dies finden Sie im Abschnitt mit den [!UICONTROL-Anmeldeinformationen] im [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr [!DNL Adobe]-[!UICONTROL Client-Geheimnis] ein. Dies finden Sie im Abschnitt mit den [!UICONTROL-Anmeldeinformationen] im [!DNL Adobe Developer Console].</td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Continue]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## [!DNL Adobe Firefly]-Module und ihre Felder

Beim Konfigurieren von [!DNL Adobe Firefly]-Modulen werden in Workfront Fusion die unten aufgeführten Felder angezeigt. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere [!DNL Adobe Firefly]-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Bild erweitern

Dieses Aktionsmodul erweitert ein Bild, optional mit Inhalten aus einer von Ihnen angegebenen Eingabeaufforderung.

Dieses Modul funktioniert mit der Firefly API V3 Async. Die vorherige Version dieses Moduls ist veraltet und wird in naher Zukunft entfernt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Firefly] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Firefly]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Geben Sie eine Eingabeaufforderung für den Inhalt ein, mit dem Sie das Bild erweitern möchten, oder ordnen Sie sie zu. Wenn keine Eingabeaufforderung angezeigt wird, wird das Bild mit Inhalten erweitert, die dem Originalbild entsprechen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzahl der Varianten]</td> 
   <td>Geben Sie eine Zahl zwischen 1 und 4 ein. Das Modul generiert diese Anzahl von erweiterten Bildvarianten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelle]</td> 
   <td>Wählen Sie aus, wie Sie die Quelldatei bereitstellen:<ul><li><p><b>Datei</b></p><p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Referenzbilddatei und die Referenzbilddatei der Quelldatei zu.</p></li><li><p><b>Vordefinierte URL</b></p><p>Geben Sie die URL des Quellbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Erweitertes Bildformat]</td> 
   <td>Wählen Sie das Dateiformat aus, in dem das erweiterte Bild gespeichert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL erweitern um]</td> 
   <td>  <p>Wählen Sie aus, ob Sie das Bild mithilfe der Bildplatzierung oder einer Maske erweitern möchten.</p> 
   <ul>
   <li><b>Platzierung</b><p>Geben Sie die horizontale und vertikale Ausrichtung sowie den Einzug des platzierten Bildes von den Kanten ein.</p></li>
   <li><b>Maskieren</b><p>Wählen Sie die Quelldatei für die Maske und ob die Maske invertiert werden soll.</p></li>
   </ul>
</td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Größe]</td> 
   <td>Wählen Sie die Höhe und Breite aus, die das erweiterte Bild sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Klicken Sie für jedes Bild, das das Modul generiert, auf <b>Element hinzufügen</b> und geben Sie eine Ganzzahl ein oder mappen Sie sie. Sie können denselben Startwert in einem anderen Modul zum Erweitern eines Bildes verwenden, um ein ähnliches Bild mit verschiedenen Stilen zu generieren. Die Anzahl der hinzugefügten Testadressen muss der Anzahl der Varianten im Feld entsprechen.</td> 
  </tr> 
 </tbody> 
</table>

### Ein Bild erweitern (veraltet)

Dieses Modul ist veraltet und wird in naher Zukunft entfernt. Verwenden Sie stattdessen das Modul Bild erweitern .

### Bild ausfüllen

Dieses Aktionsmodul füllt den maskierten Bereich eines Bildes aus, optional mit Inhalten aus einer von Ihnen angegebenen Eingabeaufforderung.

Dieses Modul funktioniert mit der Firefly API V3 Async. Die vorherige Version dieses Moduls ist veraltet und wird in naher Zukunft entfernt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Firefly] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Firefly]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL image &gt; Source]</td> 
   <td>Wählen Sie aus, wie Sie die Bildquelldatei bereitstellen:<ul><li><p><b>Datei</b></p><p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Referenzbilddatei und die Referenzbilddatei der Quelldatei zu.</p></li><li><p><b>Vordefinierte URL</b></p><p>Geben Sie die URL des Quellbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mask &gt; Source]</td> 
   <td>Wählen Sie aus, wie Sie die Maskenquelldatei bereitstellen:<ul><li><p><b>Datei</b></p><p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Referenzbilddatei und die Referenzbilddatei der Quelldatei zu.</p></li><li><p><b>Vordefinierte URL</b></p><p>Geben Sie die URL des Quellbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Geben Sie eine Eingabeaufforderung für den Inhalt ein, mit dem Sie das Bild ausfüllen möchten, oder mappen Sie sie. Wenn keine Eingabeaufforderung angezeigt wird, wird das Bild mit Inhalten gefüllt, die dem Originalbild entsprechen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzahl der Varianten]</td> 
   <td>Geben Sie eine Zahl zwischen 1 und 4 ein. Das Modul generiert diese Anzahl von ausgefüllten Bildvarianten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Gefülltes Bildformat]</td> 
   <td>Wählen Sie das Dateiformat aus, in dem das ausgefüllte Bild gespeichert werden soll.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Klicken Sie für jedes Bild, das das Modul generiert, auf <b>Element hinzufügen</b> und geben Sie eine Ganzzahl ein oder mappen Sie sie. Sie können denselben Startwert in einem anderen Modul zum Erweitern eines Bildes verwenden, um ein ähnliches Bild mit verschiedenen Stilen zu generieren. Die Anzahl der hinzugefügten Testadressen muss der Anzahl der Varianten im Feld entsprechen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Größe]</td> 
   <td>Wählen Sie die Größe aus, in der das Bild ausgefüllt werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>Wenn ein Gebietsschema bereitgestellt wird, generiert das Modul Inhalte, die für das angegebene Gebietsschema relevanter sind. <p>Das Gebietsschema muss im ISO-639-1-Sprachcode und in der ISO-3166-1-Region angegeben werden.</p><p> Beispiel: <code>en-US</code></p></td> 
  </tr> 
 </tbody> 
</table>

### Bild ausfüllen (veraltet)

Dieses Modul ist veraltet und wird in naher Zukunft entfernt. Verwenden Sie stattdessen das Modul Bild ausfüllen .

### Generieren eines adaptiven Composite

Dieses Aktionsmodul setzt ein Betreffbild nahtlos in ein Hintergrundbild an einer maskierten Position zusammen. Sie können steuern, wie stark Schatten angewendet werden, wie die Beleuchtung und Farbe des Objekts mit dem Hintergrund harmonisiert werden und ob die ursprünglichen Hintergrunddetails im maskierten Bereich erhalten bleiben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Firefly] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Firefly]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hintergrund &gt; Bild &gt; Source]</td> 
   <td>Wählen Sie aus, wie Sie das Hintergrundbild bereitstellen. Das Hintergrundbild ist die Zielszene, in der das Objekt zusammengestellt wird.<ul><li><p><b>Bild hochladen</b></p><p>Laden Sie das Hintergrundbild hoch oder ordnen Sie die Bilddatei aus einem vorherigen Modul zu.</p></li><li><p><b>Bild-URL</b></p><p>Geben Sie die URL des Hintergrundbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hintergrund &gt; Füllbereichsmaske &gt; Source]</td> 
   <td>Wählen Sie aus, wie Sie die Füllbereichsmaske bereitstellen. Die Füllbereichsmaske gibt den Bereich des Hintergrunds an, in dem das Objekt platziert wird.<ul><li><p><b>Bild hochladen</b></p><p>Laden Sie das Bild mit der Füllbereichsmaske hoch oder ordnen Sie die Bilddatei aus einem vorherigen Modul zu.</p></li><li><p><b>Bild-URL</b></p><p>Geben Sie die URL des Füllbereichsmaskenbildes ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objekt &gt; Bild &gt; Source]</td> 
   <td>Wählen Sie aus, wie Sie das Objektbild bereitstellen. Das Objektbild ist das Quellbild des Objekts, das in den Hintergrund eingefügt werden soll.<ul><li><p><b>Bild hochladen</b></p><p>Laden Sie das Objektbild hoch oder ordnen Sie die Bilddatei aus einem vorherigen Modul zu.</p></li><li><p><b>Bild-URL</b></p><p>Geben Sie die URL des Objektbildes ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objekt &gt; Maske &gt; Source]</td> 
   <td>Wählen Sie aus, wie Sie die Objektmaske bereitstellen. Die Objektmaske ist die Segmentierungsmaske für das Objekt.<ul><li><p><b>Bild hochladen</b></p><p>Laden Sie das Objektmaskenbild hoch oder ordnen Sie die Bilddatei aus einem vorherigen Modul zu.</p></li><li><p><b>Bild-URL</b></p><p>Geben Sie die URL des Objektmaskenbildes ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzahl der Varianten]</td> 
   <td>Geben Sie eine Zahl zwischen 1 und 3 ein. Das Modul generiert diese Anzahl von zusammengesetzten Varianten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]*</td> 
   <td>Klicken Sie <b>Element hinzufügen</b>, um einen Seed-Wert hinzuzufügen, und geben Sie dann eine Ganzzahl ein oder ordnen Sie sie zu. Verwenden Sie pro Variante einen Seed. Die Anzahl der Seed-Werte muss mit dem Wert von [!UICONTROL Anzahl der Varianten] übereinstimmen, wenn beide angegeben werden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Harmonisierung]*</td> 
   <td>Geben Sie eine Zahl zwischen 0 und 1 ein, um zu steuern, wie stark die Farben und die Beleuchtung des Objekts an den Hintergrund angepasst werden. <code>0.0</code> gilt für minimale Harmonisierung und <code>1.0</code> für maximale Harmonisierung.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Schattenintensität]*</td> 
   <td>Geben Sie eine Zahl zwischen 0 und 1 ein, um die Schattenintensität im zusammengesetzten Ergebnis zu steuern. Niedrigere Werte reduzieren den Schatten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hintergrund beibehalten]*</td> 
   <td>Wählen Sie aus, ob die ursprünglichen Hintergrunddetails beim Erstellen im maskierten Bereich beibehalten werden sollen. <ul><li><b>Ja</b><p>Die ursprünglichen Hintergrunddetails innerhalb des maskierten Bereichs bleiben beim Zusammensetzen erhalten.</p></li><li><b>Nein</b><p>Die ursprünglichen Hintergrunddetails innerhalb des maskierten Bereichs bleiben beim Zusammensetzen nicht erhalten.</p></li><li><b>Nicht definiert</b><p>Verwenden Sie das Standardverhalten für diese Option.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Ausgabe &gt; Medientyp]*</td> 
   <td>Wählen Sie das Dateiformat aus, in dem der generierte Verbund gespeichert werden soll.</td> 
  </tr> 
 </tbody> 
</table>

* Diese Felder sind erweiterte Felder und werden nur angezeigt, wenn Sie **[!UICONTROL Erweiterte Einstellungen anzeigen]** auswählen.

### Bild erzeugen

Dieses Aktionsmodul generiert ein - und -Bild basierend auf einer von Ihnen angegebenen Eingabeaufforderung. Sie können auch ein optionales Referenzbild angeben. Das generierte Bild entspricht dem Stil des Referenzbilds.

Dieses Modul funktioniert mit der Firefly API V3 Async. Die vorherige Version dieses Moduls ist veraltet und wird in naher Zukunft entfernt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Firefly] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Firefly]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Geben Sie eine Eingabeaufforderung für das Bild ein, das Sie generieren möchten, oder ordnen Sie sie zu. Weitere Details in der Eingabeaufforderung ermöglichen Ihnen mehr Kontrolle darüber, was im Bild angezeigt wird.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modellversion]</td> 
   <td>Wählen Sie die Firefly-Modellversion aus, die Sie zum Generieren des Bildes verwenden möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzahl der Varianten]</td> 
   <td>Geben Sie eine Zahl zwischen 1 und 4 ein. Das Modul generiert diese Anzahl von Bildvarianten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generiertes Bildformat]</td> 
   <td>Wählen Sie das Dateiformat aus, in dem das erweiterte Bild gespeichert werden soll. Wenn Sie Standard auswählen, lautet das Dateiformat JPEG , wenn kein Referenzbild angegeben wird. Wenn ein Referenzbild bereitgestellt wird, ist das Dateiformat des generierten Bildes mit dem Referenzbild identisch.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure &gt; Image Reference]</td> 
    <td>Wählen Sie aus, wie Sie die Quelldatei für die Struktur des neuen Bildes bereitstellen:<ul><li><p><b>Datei</b></p><p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Referenzbilddatei und die Referenzbilddatei der Quelldatei zu.</p></li><li><p><b>Vordefinierte URL</b></p><p>Geben Sie die URL des Quellbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Struktur &gt; Stärke]</td> 
    <td>Geben Sie eine Zahl zwischen 0 und 100 ein, um zu steuern, wie streng Firefly der Struktur des Quellbilds folgt. Höhere Zahlen bedeuten, dass Firefly dem Bild genauer folgt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Image Reference]</td> 
    <td>Wählen Sie aus, wie Sie die Quelldatei für den Stil des neuen Bildes bereitstellen:<ul><li><p><b>Datei</b></p><p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Referenzbilddatei und die Referenzbilddatei der Quelldatei zu.</p></li><li><p><b>Vordefinierte URL</b></p><p>Geben Sie die URL des Quellbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Struktur &gt; Stärke]</td> 
    <td>Geben Sie eine Zahl zwischen 0 und 100 ein, um zu steuern, wie streng Firefly dem Stil des Quellbilds folgt. Höhere Zahlen bedeuten, dass Firefly dem Bild genauer folgt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Stil &gt; Vorgaben]</td> 
   <td>Wenn Sie einen Vorgabestil verwenden möchten, klicken Sie auf Element hinzufügen und geben Sie den gewünschten Stil ein, oder ordnen Sie ihn zu.<p>Eine Liste der Vorgabenstile finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Bildmodellstile</a> in der Entwicklerdokumentation für Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Negative Eingabeaufforderung]</td> 
   <td>Geben Sie die Wörter ein, die Sie im generierten Inhalt vermeiden möchten, oder ordnen Sie sie zu. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inhaltsklasse]</td> 
   <td>Wählen Sie aus, ob das generierte Bild mehr wie ein Foto oder eher wie erstellte Kunst aussehen soll. <ul><li><b>Foto</b><p>Geben Sie Werte für Blende, Verschlusszeit (in Sekunden) und Sichtfeld (in Millimetern) ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL seed]</td> 
   <td>Klicken Sie für jedes Bild, das das Modul generiert, auf <b>Element hinzufügen</b> und geben Sie eine Ganzzahl ein oder mappen Sie sie. Sie können denselben Startwert in einem anderen Modul zum Erweitern eines Bildes verwenden, um ein ähnliches Bild mit verschiedenen Stilen zu generieren. Die Anzahl der hinzugefügten Testadressen muss der Anzahl der Varianten im Feld entsprechen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Größe]</td> 
   <td>Wählen Sie die Größe aus, in der das generierte Bild angezeigt werden soll.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Sehstärke]</td> 
   <td>Geben Sie eine Ganzzahl ein, die die Gesamtintensität der vorhandenen visuellen Eigenschaften des Fotos darstellt, oder mappen Sie sie. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>Wenn ein Gebietsschema bereitgestellt wird, generiert das Modul Inhalte, die für das angegebene Gebietsschema relevanter sind. <p>Das Gebietsschema muss im ISO-639-1-Sprachcode und in der ISO-3166-1-Region angegeben werden.</p><p> Beispiel: <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kachel]</td> 
   <td>Aktivieren Sie diese Einstellung, um ein Bild zu erstellen, das beliebig oft wiederholt werden kann.</td> 
  </tr> 
 </tbody> 
</table>

### Erstellen eines Bildes (veraltet)

Dieses Modul ist veraltet und wird in naher Zukunft entfernt. Verwenden Sie stattdessen das Modul Bild erzeugen .

### Zusammengesetztes Objekt erzeugen

Dieses Aktionsmodul kombiniert von Firefly generierte Bilder, um eine Bildkomposition zu erstellen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Firefly] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Firefly]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Geben Sie eine Eingabeaufforderung für das Bild ein, das Sie generieren möchten, oder ordnen Sie sie zu. Weitere Details in der Eingabeaufforderung ermöglichen Ihnen mehr Kontrolle darüber, was im Bild angezeigt wird.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzahl der Varianten]</td> 
   <td>Geben Sie eine Zahl zwischen 1 und 4 ein. Das Modul generiert diese Anzahl von Bildvarianten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inhaltsklasse]</td> 
   <td>Wählen Sie aus, ob das generierte Bild eher einem Foto oder einer Kunst ähneln soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL image &gt; Source]</td> 
    <td>Wählen Sie aus, wie Sie die Quelldatei für die Struktur des neuen Bildes bereitstellen:<ul><li><p><b>Datei</b></p><p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Referenzbilddatei und die Referenzbilddatei der Quelldatei zu.</p></li><li><p><b>Vordefinierte URL</b></p><p>Geben Sie die URL des Quellbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generiertes Bildformat]</td> 
   <td>Wählen Sie das Dateiformat aus, in dem das erweiterte Bild gespeichert werden soll. Wenn Sie Standard auswählen, lautet das Dateiformat JPEG , wenn kein Referenzbild angegeben wird. Wenn ein Referenzbild bereitgestellt wird, ist das Dateiformat des generierten Bildes mit dem Referenzbild identisch.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Image Reference]</td> 
    <td>Wählen Sie aus, wie Sie die Quelldatei für den Stil des neuen Bildes bereitstellen:<ul><li><p><b>Datei</b></p><p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Referenzbilddatei und die Referenzbilddatei der Quelldatei zu.</p></li><li><p><b>Vordefinierte URL</b></p><p>Geben Sie die URL des Quellbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Struktur &gt; Stärke]</td> 
    <td>Geben Sie eine Zahl zwischen 0 und 100 ein, um zu steuern, wie streng Firefly dem Stil des Quellbilds folgt. Höhere Zahlen bedeuten, dass Firefly dem Bild genauer folgt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Stil &gt; Vorgaben]</td> 
   <td>Wenn Sie einen Vorgabestil verwenden möchten, klicken Sie auf Element hinzufügen und geben Sie den gewünschten Stil ein, oder ordnen Sie ihn zu.<p>Eine Liste der Vorgabenstile finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Bildmodellstile</a> in der Entwicklerdokumentation für Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Größe]</td> 
   <td>Wählen Sie die Größe aus, die der generierte Verbund sein soll. </td> 
  </tr> 
 </tbody> 
</table>

### Erzeugen von Bildern mit Image5

Dieses Aktionsmodul generiert ein Bild mit dem [!DNL Adobe Firefly] Image5-Modell. Sie stellen eine Textaufforderung und optional ein Referenzbild bereit, um die Generierung zu leiten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Firefly] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Firefly]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Geben Sie eine Beschreibung des Bildes ein, das Sie generieren möchten, oder mappen Sie sie. Die Eingabeaufforderung muss zwischen 1 und 1500 Zeichen lang sein. Mehr Details in der Eingabeaufforderung ermöglichen Ihnen mehr Kontrolle darüber, was im Bild angezeigt wird.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seitenverhältnis]</td> 
   <td>Wählen Sie die Form des generierten Bildes aus. Wenn ein Referenzbild bereitgestellt wird, wählen Sie <b>Auto</b>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Auflösung]</td> 
   <td>Wählen Sie die Auflösung des erzeugten Bildes aus. Die Generierung höherer Auflösungen dauert länger.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Referenzbild]</td> 
   <td>Geben Sie optional ein Referenzbild an, um die Generierung zu leiten. Klicken Sie <b>Element hinzufügen</b> und geben Sie das Bild ein. Wenn Sie ein Referenzbild verwenden, setzen Sie [!UICONTROL Seitenverhältnis] auf <b>Auto</b>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]*</td> 
   <td>Klicken Sie <b>Element hinzufügen</b> und geben Sie eine Ganzzahl ein, um ein bestimmtes Generierungsergebnis zu reproduzieren. Leer lassen, um ein zufälliges Ergebnis zu erzeugen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ursachenaufforderung]*</td> 
   <td>Wählen Sie die Strategie zur umgehenden Argumentation aus, die bei der Generierung verwendet wird.<ul><li><p><b>Qualität : Erzeugt eine Bildbeschreibung</b></p><p>Erzeugt eine Bildbeschreibung in der Ausgabe des Moduls.</p></li><li><p><b>Geschwindigkeit - Schnellere Generierung, keine Beschreibung</b></p><p>Erzeugt das Bild schneller, lässt aber die Bildbeschreibung leer.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]*</td> 
   <td>Geben Sie einen Sprach- und Regionscode ein oder mappen Sie ihn, um den generierten Inhalt auf ein bestimmtes Land und eine bestimmte Sprache anzupassen. <p>Das Gebietsschema muss im ISO-639-1-Sprachcode und in der ISO-3166-1-Region angegeben werden.</p><p>Beispiel: <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzahl der Varianten]*</td> 
   <td>Geben Sie die Anzahl der Bilder ein, die pro Anfrage generiert werden sollen. Derzeit wird nur 1 unterstützt. Um mehrere Bilder zu generieren, senden Sie separate Anfragen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Modell]*</td> 
   <td>Wählen Sie das [!DNL Firefly] aus, das Sie zum Generieren des Bildes verwenden möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschränkung]</td> 
   <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während eines Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

*Diese Felder sind erweitert und werden nur angezeigt, wenn Sie **[!UICONTROL Erweiterte Einstellungen anzeigen]** auswählen.

### Präzise Komposition generieren

Dieses Aktionsmodul platziert ein Objekt im maskierten Bereich eines Hintergrundbildes und wendet generative Harmonisierung an, sodass das Objekt sich natürlich mit dem Hintergrund vermischt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Firefly] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Firefly]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hintergrund &gt; Bild &gt; Source]</td> 
   <td>Wählen Sie aus, wie Sie das Hintergrundbild bereitstellen. Das Hintergrundbild ist die Zielszene, in der das Objekt zusammengestellt wird.<ul><li><p><b>Bild hochladen</b></p><p>Laden Sie das Hintergrundbild hoch oder ordnen Sie die Bilddatei aus einem vorherigen Modul zu.</p></li><li><p><b>Bild-URL</b></p><p>Geben Sie die URL des Hintergrundbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hintergrund &gt; Füllbereichsmaske &gt; Source]</td> 
   <td>Wählen Sie aus, wie Sie die Füllbereichsmaske bereitstellen. Die Füllbereichsmaske gibt den Bereich des Hintergrunds an, in dem das Objekt platziert wird.<ul><li><p><b>Bild hochladen</b></p><p>Laden Sie das Bild mit der Füllbereichsmaske hoch oder ordnen Sie die Bilddatei aus einem vorherigen Modul zu.</p></li><li><p><b>Bild-URL</b></p><p>Geben Sie die URL des Füllbereichsmaskenbildes ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objekt &gt; Bild &gt; Source]</td> 
   <td>Wählen Sie aus, wie Sie das Objektbild bereitstellen. Das Objektbild ist das Quellbild des Objekts, das in den Hintergrund eingefügt werden soll.<ul><li><p><b>Bild hochladen</b></p><p>Laden Sie das Objektbild hoch oder ordnen Sie die Bilddatei aus einem vorherigen Modul zu.</p></li><li><p><b>Bild-URL</b></p><p>Geben Sie die URL des Objektbildes ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzahl der Varianten]</td> 
   <td>Geben Sie eine Zahl zwischen 1 und 3 ein. Das Modul generiert diese Anzahl von zusammengesetzten Varianten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]*</td> 
   <td>Klicken Sie <b>Element hinzufügen</b>, um einen Seed-Wert hinzuzufügen, und geben Sie dann eine Ganzzahl ein oder ordnen Sie sie zu. Verwenden Sie pro Variante einen Seed. Die Anzahl der Seed-Werte muss mit dem Wert von [!UICONTROL Anzahl der Varianten] übereinstimmen, wenn beide angegeben werden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blend]*</td> 
   <td>Geben Sie eine Zahl zwischen 0 und 1 ein, um die Mischung zwischen dem harmonischen und ursprünglichen Erscheinungsbild des Objekts zu steuern. <code>0.0</code> wendet eine vollständige Harmonisierung an, wobei <code>1.0</code> das Erscheinungsbild des ursprünglichen Objekts beibehalten wird.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Ausgabe &gt; Medientyp]*</td> 
   <td>Wählen Sie das Dateiformat aus, in dem der generierte Verbund gespeichert werden soll.</td> 
  </tr> 
 </tbody> 
</table>

* Diese Felder sind erweiterte Felder und werden nur angezeigt, wenn Sie **[!UICONTROL Erweiterte Einstellungen anzeigen]** auswählen.

### Erzeugen ähnlicher Bilder

Dieses Aktionsmodul generiert Bilder, die dem von Ihnen angegebenen Quellbild ähneln.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Firefly] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Firefly]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzahl der Varianten]</td> 
   <td>Geben Sie eine Zahl zwischen 1 und 4 ein. Das Modul generiert diese Anzahl von Bildvarianten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modellversion]</td> 
   <td>Wählen Sie die Firefly-Modellversion aus, die Sie zum Generieren der Bilder verwenden möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generiertes Bildformat]</td> 
   <td>Wählen Sie das Dateiformat aus, in dem das erweiterte Bild gespeichert werden soll. Wenn Sie Standard auswählen, lautet das Dateiformat JPEG , wenn kein Referenzbild angegeben wird. Wenn ein Referenzbild bereitgestellt wird, ist das Dateiformat des generierten Bildes mit dem Referenzbild identisch.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL image &gt; Source]</td> 
    <td>Wählen Sie aus, wie Sie die Quelldatei für die Struktur des neuen Bildes bereitstellen:<ul><li><p><b>Datei</b></p><p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Referenzbilddatei und die Referenzbilddatei der Quelldatei zu.</p></li><li><p><b>Vordefinierte URL</b></p><p>Geben Sie die URL des Quellbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Image Reference]</td> 
    <td>Wählen Sie aus, wie Sie die Quelldatei für den Stil des neuen Bildes bereitstellen:<ul><li><p><b>Datei</b></p><p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen der Referenzbilddatei und die Referenzbilddatei der Quelldatei zu.</p></li><li><p><b>Vordefinierte URL</b></p><p>Geben Sie die URL des Quellbilds ein oder mappen Sie sie.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Größe]</td> 
   <td>Wählen Sie die Größe aus, die der generierte Verbund sein soll. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Klicken Sie für jedes Bild, das das Modul generiert, auf <b>Element hinzufügen</b> und geben Sie eine Ganzzahl ein oder mappen Sie sie. Sie können denselben Startwert in einem anderen Modul zum Erweitern eines Bildes verwenden, um ein ähnliches Bild mit verschiedenen Stilen zu generieren. Die Anzahl der hinzugefügten Testadressen muss der Anzahl der Varianten im Feld entsprechen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kachel]</td> 
   <td>Aktivieren Sie diese Einstellung, um ein Bild zu erstellen, das beliebig oft wiederholt werden kann.</td> 
  </tr> 
 </tbody> 
</table>


### Video generieren

Dieses Aktionsmodul generiert ein Video aus einer Textaufforderung. Sie können auch ein oder mehrere Referenzbilder bereitstellen, die die Videogenerierung leiten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Firefly] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Firefly]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Geben Sie eine Beschreibung des Videos ein, das Sie generieren möchten, oder mappen Sie sie. Mehr Details in der Eingabeaufforderung ermöglichen Ihnen mehr Kontrolle darüber, was im Video angezeigt wird.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bild &gt; Bedingungen]</td> 
   <td>Geben Sie optional ein oder mehrere Referenzbilder an, die die Videogenerierung leiten sollen. Klicken <b> für jedes </b> auf „Element hinzufügen“.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL sizeS]</td> 
   <td>Klicken Sie <b>Element hinzufügen</b> und geben Sie die Dimensionen des generierten Videos ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bitratenfaktor]*</td> 
   <td>Geben Sie eine Zahl zwischen 0 und 63 ein, um den Bitratenfaktor für das generierte Video festzulegen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Videoeinstellungen &gt; Kamerabewegung]*</td> 
   <td>Wählen Sie die Kamerabewegung aus, die Sie im erzeugten Video verwenden möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Videoeinstellungen &gt; Eingabeaufforderungsstil]*</td> 
   <td>Wählen Sie den Eingabeaufforderungsstil aus, den Sie für das generierte Video verwenden möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Videoeinstellungen &gt; Aufnahmewinkel]*</td> 
   <td>Wählen Sie den Aufnahmewinkel aus, den Sie im erzeugten Video verwenden möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Videoeinstellungen &gt; Aufnahmegröße]*</td> 
   <td>Wählen Sie die Aufnahmegröße aus, die Sie im generierten Video verwenden möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschränkung]</td> 
   <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während eines Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

* Diese Felder sind erweiterte Felder und werden nur angezeigt, wenn Sie **[!UICONTROL Erweiterte Einstellungen anzeigen]** auswählen.

### Benutzerdefinierten API-Aufruf erstellen

Dieses Aktionsmodul führt einen benutzerdefinierten Aufruf an die Firefly-API durch.

Spezifische verfügbare APIs finden Sie unter [Adobe Firefly-API](https://developer.adobe.com/firefly-services/docs/firefly-api/) in der Dokumentation zu Adobe Developer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Firefly] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Firefly]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://firefly-api.adobe.io/</code> ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Methode]</p>
      </td>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Header]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt automatisch Autorisierungs-Header hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Text]</td>
   <td> <p>Fügen Sie den Textinhalt für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrem JSON-Objekt verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

