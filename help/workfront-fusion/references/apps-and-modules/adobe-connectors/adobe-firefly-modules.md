---
title: Adobe Firefly-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die verwenden [!DNL Adobe Firefly] und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2482'
ht-degree: 1%

---

# [!DNL Adobe Firefly]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Adobe Firefly] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

## Erstellen einer Verbindung zu [!DNL Adobe Firefly]

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe Firefly]:

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
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre [!UICONTROL Adobe] [!UICONTROL Client-ID] ein. Dies finden Sie im Abschnitt mit den [!UICONTROL -Anmeldeinformationen] im [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihren [!DNL Adobe] [!UICONTROL Client Secret] ein. Dies finden Sie im Abschnitt mit den [!UICONTROL -Anmeldeinformationen] im [!DNL Adobe Developer Console].</td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## [!DNL Adobe Firefly] Module und ihre Felder

Beim Konfigurieren von [!DNL Adobe Firefly] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Adobe Firefly] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Bild erweitern

Dieses Aktionsmodul erweitert ein Bild, optional mit Inhalten aus einer von Ihnen angegebenen Eingabeaufforderung.

Dieses Modul funktioniert mit der Firefly API V3 Async. Die vorherige Version dieses Moduls ist veraltet und wird in naher Zukunft entfernt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Firefly]</a> in diesem Artikel.</td> 
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
   <td role="rowheader">[!UICONTROL Source]</td> 
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
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Firefly]</a> in diesem Artikel.</td> 
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

### Bild erzeugen

Dieses Aktionsmodul generiert ein - und -Bild basierend auf einer von Ihnen angegebenen Eingabeaufforderung. Sie können auch ein optionales Referenzbild angeben. Das generierte Bild entspricht dem Stil des Referenzbilds.

Dieses Modul funktioniert mit der Firefly API V3 Async. Die vorherige Version dieses Moduls ist veraltet und wird in naher Zukunft entfernt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Firefly]</a> in diesem Artikel.</td> 
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
   <td role="rowheader">[!UICONTROL -Stil &gt; Vorgaben]</td> 
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
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Firefly]</a> in diesem Artikel.</td> 
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
   <td role="rowheader">[!UICONTROL -Stil &gt; Vorgaben]</td> 
   <td>Wenn Sie einen Vorgabestil verwenden möchten, klicken Sie auf Element hinzufügen und geben Sie den gewünschten Stil ein, oder ordnen Sie ihn zu.<p>Eine Liste der Vorgabenstile finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Bildmodellstile</a> in der Entwicklerdokumentation für Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Größe]</td> 
   <td>Wählen Sie die Größe aus, die der generierte Verbund sein soll. </td> 
  </tr> 
 </tbody> 
</table>

### Erzeugen ähnlicher Bilder

Dieses Aktionsmodul generiert Bilder, die dem von Ihnen angegebenen Quellbild ähneln.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Firefly]</a> in diesem Artikel.</td> 
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


### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt einen benutzerdefinierten Aufruf an die Firefly-API durch.

Spezifische verfügbare APIs finden Sie unter [Adobe Firefly-API](https://developer.adobe.com/firefly-services/docs/firefly-api/) in der Dokumentation zu Adobe Developer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL -Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Firefly] finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Firefly]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://firefly-api.adobe.io/</code> ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL -Methode]</p>
      </td>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -Kopfzeilen]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt Autorisierungs-Header automatisch hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL body]</td>
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

