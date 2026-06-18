---
title: Adobe Photoshop-Module
description: Mit den Adobe Photoshop-Modulen können Sie ein Adobe Workfront Fusion-Szenario auf der Grundlage von Ereignissen in Ihrem Adobe Photoshop-Konto starten, Vereinbarungen erstellen, lesen oder aktualisieren und andere Datensätze suchen, anhand der von Ihnen festgelegten Kriterien nach Datensätzen suchen und Dokumente hochladen.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
TQID: https://experienceleague.adobe.com/RratZmko93V0LMxJ6qTy6cNvRqgPNvNgHTflRngE6BI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ce3fb5604ac4ed85af1bcc51143732499dfb0404
workflow-type: tm+mt
source-wordcount: 7285
ht-degree: 12%

---

# [!DNL Adobe Photoshop]-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Adobe Photoshop] verwenden, und diese mit verschiedenen Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

>[!IMPORTANT]
>
>Adobe Photoshop hat einige Elemente seiner API verworfen, die Fusion verwendet, um Aktionen in Photoshop durchzuführen.
>
>**Daher werden einige der vorhandenen Photoshop-Module nach dem 30. Juli 2026 nicht mehr funktionieren.**
>
>Es wird empfohlen, alle Szenarien, die diese Module verwenden, so bald wie möglich auf die aktualisierten Module zu aktualisieren.
>
>Eine Liste der betroffenen Module finden Sie unter [Aktualisierungen der Einstellung von Adobe Photoshop-API](#adobe-photoshop-api-deprecation-updates).
>
>Eine Erläuterung der Auswirkungen von API-Änderungen auf Workfront Fusion finden Sie unter [Übersicht über APIs in Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md).

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

Bevor Sie den [!DNL Adobe Photoshop]-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein aktives [!DNL Adobe Photoshop] verfügen.
* Sie müssen über eine Firefly Services-Lizenz verfügen.
* Sie müssen über eine Client-ID und ein Client-Geheimnis verfügen. Sie können diese von der Adobe Developer Console beziehen.

## Aktualisierungen der Einstellung von Adobe Photoshop-APIs

Adobe Photoshop hat einige Elemente seiner API verworfen, die Fusion verwendet, um Aktionen in Photoshop durchzuführen.

**Daher werden einige der vorhandenen Photoshop-Module nach dem 30. Juli 2026 nicht mehr funktionieren.**

In dieser Tabelle wird dokumentiert, welche Module von dieser Einstellung betroffen sind und auf welches Modul Sie aktualisieren sollten.

| Veraltetes Modul | Auf neues Modul aktualisieren |
|---|---|
| PSD-Bearbeitungen anwenden | Erstellen oder Bearbeiten eines Composite |
| Bildformat konvertieren | Erstellen oder Bearbeiten eines Composite |
| Erstellen von zusammengesetzten Elementen | Erstellen oder Bearbeiten eines Composite |
| Erstellen einer neuen PSD | Erstellen oder Bearbeiten eines Composite |
| Ausgabedarstellungen erstellen | Erstellen oder Bearbeiten eines Composite |
| Bearbeiten von Textebenen | Ausführen von Photoshop-Aktionen, -Skripten und -Transformationen |
| Bearbeiten von Textebenen 2 | Ausführen von Photoshop-Aktionen, -Skripten und -Transformationen |
| Ausführen einer JSON-Aktion | Ausführen von Photoshop-Aktionen, -Skripten und -Transformationen |
| Tiefenunschärfe ausführen | (Nicht verfügbar) |
| Ausführen von Photoshop-Aktionen | Ausführen von Photoshop-Aktionen, -Skripten und -Transformationen |
| Ausführen eines Produktzuschnitts | Ausführen von Photoshop-Aktionen, -Skripten und -Transformationen |
| Abrufen von Ebeneninformationen | Manifest erzeugen |
| Ändern der Bildgröße | Erstellen oder Bearbeiten eines Composite |
| Smart-Objekt ersetzen | Erstellen oder Bearbeiten eines Composite |
| Smart-Objekt 2 ersetzen | Erstellen oder Bearbeiten eines Composite |
| Drehen von Bildern | Ausführen von Photoshop-Aktionen, -Skripten und -Transformationen |
| Wasserzeichen für ein Bild | Erstellen oder Bearbeiten eines Composite |

## Adobe Photoshop-API-Informationen

Der Adobe Photoshop-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://image.adobe.io/pie/psdService</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.12.31</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe Photoshop]-Module:

1. Klicken Sie in einem beliebigen Modul **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Verbindungstyp]</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine JWT- oder eine Server-zu-Server-Verbindung verwenden möchten.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für die Verbindung ein.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre [!UICONTROL Adobe] [!UICONTROL Client-ID] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr [!DNL Adobe]-[!UICONTROL Client-Geheimnis] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID des technischen Kontos]</td>
        <td>Wenn Sie eine JWT-Verbindung verwenden, geben Sie Ihre [!DNL Adobe] [!UICONTROL Technical Account ID] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Organisations-ID]</td>
        <td>Wenn Sie eine JWT-Verbindung verwenden, geben Sie Ihre [!DNL Adobe] [!UICONTROL Organisations-ID] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Privater Schlüssel]</td>
        <td>
          <p>Wenn Sie eine JWT-Verbindung verwenden, geben Sie den privaten Schlüssel ein, der beim Erstellen Ihrer Anmeldeinformationen im [!DNL Adobe Developer Console] generiert wurde. </p>
          <p>So extrahieren Sie Ihren privaten Schlüssel oder Ihr Zertifikat:</p>
          <ol>
            <li value="1">
              <p>Klicken Sie auf <b>[!UICONTROL Extrahieren]</b>.</p>
            </li>
            <li value="2">
              <p>Wählen Sie den zu extrahierenden Dateityp aus.</p>
            </li>
            <li value="3">
              <p>Wählen Sie die Datei aus, die den privaten Schlüssel oder das Zertifikat enthält.</p>
            </li>
            <li value="4">
              <p>Geben Sie das Kennwort für die Datei ein.</p>
            </li>
            <li value="5">
              <p>Klicken Sie <b>Speichern</b>, um die Datei zu extrahieren und zur Verbindungseinrichtung zurückzukehren.</p>
            </li>
          </ol>
        </td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Continue]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## [!DNL Adobe Photoshop]-Module und ihre Felder

Beim Konfigurieren von [!DNL Adobe Photoshop]-Modulen werden in Workfront Fusion die unten aufgeführten Felder angezeigt. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere [!DNL Adobe Photoshop]-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Aktionen

* [HEX in RGB konvertieren](#convert-hex-to-rgb)
* [Erstellen einer Zeichenfläche](#create-an-artboard)
* [Erstellen oder Bearbeiten eines Composite](#create-or-edit-a-composite)
* [Bearbeiten eines Bildes mit verschiedenen Anpassungen](#edit-an-image-with-various-adjustments)
* [Ausführen von Photoshop-Aktionen, -Skripten und -Transformationen](#execute-photoshop-actions-scripts-and-transformations)
* [Manifest erzeugen](#generate-a-manifest)
* [Hintergrund entfernen](#remove-background)

#### HEX in RGB konvertieren

Dieses Modul konvertiert einen HEX-Farbcode in RGB-Farbe.



Dieses Modul nimmt Bildanpassungen im Lightroom-Stil vor.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL HEX]</td>
      <td>Geben Sie den HEX-Code ein, den Sie in RGB konvertieren möchten, oder ordnen Sie ihn zu.</td>
    </tr>
    </tbody>
</table>

#### Erstellen einer Zeichenfläche

Dieses Modul erstellt eine neue Zeichenfläche in Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Images]</td>
      <td>
        <p>Klicken Sie für jedes Bild, das Sie dieser Zeichenfläche hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Quelltyp und den Speicherort des Bildes ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Zeichenflächen-Abstand]</p>
      </td>
   <td>Geben Sie den Abstand in Pixel ein, den Sie zwischen den einzelnen Zeichenflächen haben möchten, oder mappen Sie ihn zu.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede konvertierte Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie den Speicherort, den Speicherort und andere Optionen wie aufgeführt ein.</p>
      </td>
    </tr>
    </tbody>
</table>

#### Erstellen oder Bearbeiten eines Composite

Dieses Modul erstellt oder bearbeitet einen Verbund in Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Images]</td>
      <td>
        <p>Klicken Sie für jedes Bild, das Sie dieser Zeichenfläche hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Quelltyp und den Speicherort des Bildes ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Breite]</p>
      </td>
   <td>Wenn Sie ein Bild erstellen, geben Sie die Bildbreite in Pixel ein.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Höhe]</td>
      <td>
        <p>Wenn Sie ein Bild erstellen, geben Sie die Bildhöhe in Pixel ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -Modus]</td>
      <td>
        <p>Wählen Sie den Farbmodus für dieses Bild.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fill]</td>
      <td>
        <p>Wählen Sie den Füllungstyp für die Hintergrundebene aus.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>
        <p>Geben Sie einen Namen für das neue Bild ein oder mappen Sie ihn.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Pixel-Skalierungsfaktor]</td>
      <td>
        <p>Geben Sie den Pixelskalierungsfaktor ein oder mappen Sie ihn. Dies muss eine Zahl zwischen 0,1 und 1 sein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -Auflösung]</td>
      <td>
        <p>Geben <b> im Feld </b> den Wert der Auflösung in Dichteeinheiten (Pixel pro Zoll) ein. Der Standardwert ist 72.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Profiltyp]</td>
      <td>
        <p>Wenn Sie das Standardfarbprofil überschreiben möchten, wählen Sie einen Profiltyp aus und geben Sie die Details wie aufgeführt ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Zuschneiden &gt; Oben / Links / Unten / Rechts]</td>
      <td>
        <p>Geben Sie die Grenzen ein, auf die Sie das Bild zuschneiden möchten.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ausblenden]</td>
      <td>
        <p>Wählen Sie Ja , um Pixel außerhalb der Zuschnittgrenzen auszublenden. Wenn dies auf „false“ gesetzt ist, werden Pixel außerhalb der Zuschnittgrenzen gelöscht. Der Standardwert lautet „false“.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Größe ändern &gt; Breite]</td>
      <td>
        <p>Wählen Sie die Einheit aus, die Sie für die Breite verwenden möchten, und wählen Sie dann den Wert aus, der die gewünschte Breite darstellt. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Größe ändern &gt; Höhe]</td>
      <td>
        <p>Wählen Sie die Einheit aus, die Sie für die Höhe verwenden möchten, und wählen Sie dann den Wert aus, der für die gewünschte Höhe steht. </p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL -Auflösung]</td>
      <td>
        <p>Wählen Sie die Einheit aus, die Sie für die Auflösung verwenden möchten, und wählen Sie dann den Wert für die gewünschte Auflösung aus.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Resample]</td>
      <td>
        <p>Wählen Sie die beim Ändern der Größe zu verwendende Resampling-Methode aus.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Proportionen beschränken]</td>
      <td>
        <p>Wählen Sie Ja , um das Seitenverhältnis zwischen Breite und Höhe beizubehalten. Wählen Sie Nein , um eine unabhängige Einstellung der Breite und Höhe zu ermöglichen.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Rastern]</td>
      <td>
        <p>Wählen Sie aus, ob das Bild gerastert werden soll.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL scale styles]</td>
      <td>
        <p>Wählen Sie aus, ob beim Ändern der Bildgröße eine Skalierung auf Stile angewendet werden soll.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Beschneiden nach]</td>
      <td>
        <p>Wählen Sie aus, ob transparente Pixel gekürzt werden sollen.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL -Ebenen]</td>
      <td>
        <p>Klicken Sie für jede weitere hinzuzufügende Ebene auf <b>Element hinzufügen</b> und geben Sie Ebenendetails ein. </p><p>Weitere Informationen finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/createComposite">Erstellen oder Bearbeiten eines Composite</a> in der Adobe-Dokumentation.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Standardschriftart PostScript Name]</td>
      <td>
        <p>Geben Sie den PostScript-Namen der Standardschriftart ein, die Sie verwenden möchten, oder ordnen Sie ihn zu.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL fehlende Schriftstrategie]</td>
      <td>
        <p>Wählen Sie aus, ob bei der Erstellung oder Bearbeitung ein Fehler auftreten soll oder ob die Standardschriftart verwendet werden soll, wenn keine Schriftart verfügbar ist.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Zusätzliche Schriftarten]</td>
      <td>
        <p>Klicken Sie für jede Schriftart, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Quell-URL der Schriftart ein. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede bearbeitete Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie die Ausgabedetails ein. </p><p>Weitere Informationen finden Sie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/createComposite">Erstellen oder Bearbeiten eines Composite</a> in der Dokumentation zu Adobe.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Maximale Anzahl an Ergebnissen]</td>
      <td>
        <p>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während eines Ausführungszyklus arbeiten soll, oder mappen Sie sie.</p>
      </td>
      </tr>
      </tbody>
</table>

#### Bearbeiten eines Bildes mit verschiedenen Anpassungen

Dieses Modul nimmt Bildanpassungen im Lightroom-Stil vor.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Images]</td>
      <td>
        <p>Geben Sie den Quelltyp und den Speicherort des Bildes ein oder ordnen Sie ihn zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Andere Felder]</p>
      </td>
   <td><p>Weitere Informationen finden Sie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/edit">Bearbeiten eines Bildes mit verschiedenen Anpassungen</a> in der Dokumentation zu Adobe.</p></td> 
    </tr>
    </tbody>
</table>

#### Ausführen von Photoshop-Aktionen, -Skripten und -Transformationen

Dieses Modul führt Aktionen, Skripte und Umwandlungen aus, die in der Firefly Photoshop-API verfügbar sind.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Images]</td>
      <td>
        <p>Geben Sie den Quelltyp und den Speicherort des Bildes ein oder ordnen Sie ihn zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Aktionen]</p>
      </td>
   <td><p>Klicken Sie für jede Aktion, die Sie hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie die Quelle, URL und den Namen der Aktion ein.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL UXP-Quelle]</p>
      </td>
   <td><p>Wenn Sie ein UDP-Skript verwenden, wählen Sie aus, ob Sie eine URL oder Inline-Inhalte bereitstellen, geben Sie dann die URL oder den Inhalt ein oder mappen Sie ihn.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Zusätzliche Inhalte]</p>
      </td>
   <td><p>Fügen Sie bis zu 25 Dateien hinzu, die von der Aktion oder UXP referenziert werden.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede bearbeitete Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie das Format, das Ziel und das Ausgabemuster ein.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Maximale Anzahl an Ergebnissen]</td>
      <td>
        <p>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während eines Ausführungszyklus arbeiten soll, oder mappen Sie sie.</p>
      </td>
      </tr>
    </tbody>
</table>

#### Manifest erzeugen

Dieses Modul generiert ein PSD-Manifest für das angegebene Eingabebild.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Quelle]</td>
      <td>
        <p>Geben Sie den Quelltyp und den Speicherort des Bildes ein oder ordnen Sie ihn zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede bearbeitete Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie die Zieldetails ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ebenenminiaturansichten einschließen]</p>
      </td>
   <td><p>Wählen Sie Ja aus, wenn Sie das Modul zum Generieren einer Miniaturansicht für jede Ebene im Manifest verwenden möchten.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Tiefe der Miniaturansichten]</p>
      </td>
   <td><p>Geben Sie die maximale Tiefe für Miniatur-Ausgabedarstellungen ein oder mappen Sie sie. Geben Sie für keine maximale Tiefe <code>0</code> ein.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Layer-Miniaturansichtsformat]</p>
      </td>
   <td><p>Wählen Sie aus, ob die Miniaturen im JPEG- oder PNG-Format vorliegen sollen.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Smart-Objektdaten extrahieren]</td>
      <td>
        <p>Wählen Sie aus, ob eingebettete Smart-Objekte extrahiert und eine vordefinierte URL in das Manifest aufgenommen werden sollen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auf Transparenz trimmen]</td>
      <td>
        <p>Wählen Sie aus, ob die Miniaturansichten der Ebenen gekürzt werden sollen, um transparente Pixel zu entfernen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximale Anzahl an Ergebnissen]</td>
      <td>
        <p>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während eines Ausführungszyklus arbeiten soll, oder mappen Sie sie.</p>
      </td>
      </tr>
    </tbody>
</table>

#### Hintergrund entfernen

Dieses Aktionsmodul identifiziert das Hauptsubjekt Ihres Bildes und entfernt den Hintergrund.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Datei gespeichert wird, aus der der Hintergrund entfernt werden soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Eingabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, aus der bzw. dem Sie den Hintergrund entfernen möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die neue Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die neue Datei gespeichert werden soll, oder mappen Sie sie.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll. Dies gilt nur für Dateien im Adobe-Speicher.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Farbraum]</p>
      </td>
   <td>Wählen Sie aus, ob das Ausgabebild RGB- oder RGBA-Farbe verwenden soll. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maskenformat]</p>
      </td>
   <td>Wählen Sie aus, ob die Kanten des Bildes weich (gefedert) oder binär sein sollen. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL optimieren]</p>
      </td>
   <td>Wählen Sie Leistung aus, um die Geschwindigkeit zu optimieren, oder Batch, um Wartezeiten zuzulassen. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nachbearbeitungsprozess]</p>
      </td>
   <td>Wählen Sie aus, ob die Nachbearbeitung aktiviert werden soll.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>Der Standardwert ist 4.0</td> 
    </tr> 
    </tbody>
</table>


### Legacy

* [Anwenden von PSD-Bearbeitungen (veraltet)](#apply-psd-edits-legacy)
* [Automatische Farbkorrektur eines Bildes (veraltet)](#auto-color-correct-an-image-legacy)
* [Bildformat konvertieren (veraltet)](#convert-image-format-legacy)
* [Erstellen einer Maske (veraltet)](#create-a-mask-legacy)
* [Erstellen einer neuen PSD (veraltet)](#create-a-new-psd-legacy)
* [Erstellen von Ausgabedarstellungen (veraltet)](#create-renditions-legacy)
* [Bearbeiten von Textebenen (alt)](#edit-text-layers-legacy)
* [Bearbeiten von Textebenen 2 (alt)](#edit-text-layers-2-legacy)
* [Ausführen einer JSON-Aktion (alt)](#execute-an-action-json-legacy)
* [Tiefenunschärfe ausführen (alt)](#execute-depth-blur-legacy)
* [Ausführen von Photoshop-Aktionen (veraltet)](#execute-photoshop-actions-legacy)
* [Ausführen eines Produktzuschnitts (veraltet)](#execute-product-crop-legacy)
* [Abrufen von Ebeneninformationen (veraltet)](#get-layer-info-legacy)
* [Erstellen eines benutzerdefinierten API-Aufrufs (veraltet)](#make-a-custom-api-call-legacy)
* [Hintergrund entfernen (veraltet)](#remove-background-legacy)
* [Ersetzen eines Smart-Objekts (alt)](#replace-a-smart-object-legacy)
* [Ersetzen eines Smart-Objekts 2 (alt)](#replace-a-smart-object-2-legacy)
* [Größe eines Bildes ändern (veraltet)](#resize-an-image-legacy)
* [Wasserzeichen für ein Bild (veraltet)](#watermark-an-image-legacy)

#### Anwenden von PSD-Bearbeitungen (veraltet)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Erstellen oder Bearbeiten eines zusammengesetzten &#x200B;](#create-or-edit-a-composite)&quot;.

Dieses Aktionsmodul wendet eine Vielzahl von Bearbeitungen auf Dokument- und Ebenenebene an.

Dieses Modul unterstützt große Dateien. Weitere Informationen zu großen Dateien finden Sie unter [Arbeiten mit großen Dateien](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die zu bearbeitende Datei gespeichert ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Eingabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie bearbeiten möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument &gt; Bildgröße) Höhe]</p>
      </td>
      <td> Geben Sie die Höhe des Bildes in Pixel ein oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument &gt; Bildgröße) Breite]</p>
      </td>
      <td> Geben Sie die Breite des Bildes in Pixel ein oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument &gt; Arbeitsflächengröße) oben]</p>
      </td>
   <td> Geben Sie die y-Koordinate der linken oberen Ecke des Dokuments in Pixeln ein oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument &gt; Arbeitsflächengröße) unten]</p>
      </td>
   <td> Geben Sie die y-Koordinate der unteren rechten Ecke des Dokuments in Pixeln ein oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument &gt; Arbeitsflächengröße) links]</p>
      </td>
   <td> Geben Sie die x-Koordinate der linken oberen Ecke des Dokuments in Pixeln ein oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument &gt; Arbeitsflächengröße) rechts]</p>
      </td>
   <td> Geben Sie die x-Koordinate der unteren rechten Ecke des Dokuments in Pixeln ein oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument) kürzen]</p>
      </td>
   <td> Wählen Sie Transparente Pixel aus, damit die Kürzung auf transparenten Pixeln im Bild basiert. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen) Standardschriftart]</p>
      </td>
   <td> Geben Sie den vollständigen PostScript-Namen der Schriftart ein, die als globaler Standard für das Dokument verwendet werden soll. Diese Schriftart wird für alle Textebenen verwendet, in denen die Schriftart fehlt, und es wurde keine andere Schriftart speziell für diese Ebene angegeben. Wenn diese Schriftart fehlt, wird die unter Fehlende Schriftarten verwalten angegebene Option wirksam. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen) Schriftarten]</p>
      </td>
   <td> Klicken Sie für jede Schriftart, die das Dokument benötigt, auf Element hinzufügen und geben Sie den Speicherort und den Dateispeicherort der Schriftart ein. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen): fehlende Schriftarten verwalten]</p>
      </td>
   <td> Auswahl der Aktion, die ausgeführt werden soll, wenn im Dokument eine oder mehrere Schriftarten fehlen. <ul><li><code>fail</code>: Der Vorgang ist nicht erfolgreich und der Status wird auf „Fehlgeschlagen“ gesetzt, wobei die Details zum Fehler im Detailabschnitt des Status angegeben werden.</li><li><code>useDefault</code>: Der Vorgang wird erfolgreich sein und alle fehlenden Schriftarten werden durch ArialMT ersetzt.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen)-Ebenen]</p>
      </td>
   <td> Klicken Sie für jede Ebene, die Sie hinzufügen möchten, auf Element hinzufügen und füllen Sie die Ebenendetails aus. <p>Weitere Informationen zu Ebenenoptionen finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/modifyDocumentAsync">PSD-Bearbeitungen anwenden</a> in der Dokumentation zu Adobe Photoshop.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede bearbeitete Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie den Speicherort, den Speicherort und den Typ wie aufgeführt ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die neue Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die neue Datei gespeichert werden soll, oder mappen Sie sie. Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Typ]</p>
      </td>
   <td>Wählen Sie den Dateityp aus, in den Sie die Datei konvertieren möchten. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll. Dies gilt nur für Dateien im Adobe-Speicher.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe) Auf Arbeitsfläche zuschneiden]</p>
      </td>
   <td>Wählen Sie aus, ob die Ausgabedarstellungen die Größe der Arbeitsfläche aufweisen sollen. Mit True werden die Ausgabedarstellungen auf die Arbeitsfläche gekürzt, während mit False die Größe der Ausgabedarstellungsebene festgelegt wird</td> 
    </tr>
    </tbody>
</table>

#### Automatische Farbkorrektur eines Bildes (veraltet)

Dieses Aktionsmodul korrigiert automatisch das angegebene Bild.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Datei gespeichert ist, die Sie farblich korrigieren möchten.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Eingabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie farblich korrigieren möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die neue Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die neue Datei gespeichert werden soll, oder mappen Sie sie. Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Typ]</p>
      </td>
   <td>Wählen Sie den Dateityp aus, in den Sie die Datei konvertieren möchten. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll. Dies gilt nur für Dateien im Adobe-Speicher.</p>
      </td>
    </tr>
    </tbody>
</table>

#### Bildformat konvertieren (veraltet)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Erstellen oder Bearbeiten eines zusammengesetzten &#x200B;](#create-or-edit-a-composite)&quot;.

Dieses Aktionsmodul konvertiert eine Datei in JPEG, PNG, PSD oder TIFF.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Datei gespeichert wird, aus der der Hintergrund entfernt werden soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Eingabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, aus der bzw. dem Sie den Hintergrund entfernen möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede konvertierte Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie den Speicherort, den Speicherort und den Typ wie aufgeführt ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die neue Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die neue Datei gespeichert werden soll, oder mappen Sie sie. Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Typ]</p>
      </td>
   <td>Wählen Sie den Dateityp aus, in den Sie die Datei konvertieren möchten. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll. Dies gilt nur für Dateien im Adobe-Speicher.</p>
      </td>
    </tr>
    </tbody>
</table>

#### Erstellen einer Maske (veraltet)

Dieses Aktionsmodul gibt eine PNG-Datei mit einer Maske zurück, die um das Subjekt herum angewendet wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Datei gespeichert wird, aus der Sie eine Maske erstellen möchten.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Eingabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, aus der Sie eine Maske erstellen möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Maskendatei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die Maskendatei gespeichert werden soll, oder mappen Sie diese. Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll. Dies gilt nur für Dateien im Adobe-Speicher.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Farbraum]</p>
      </td>
   <td>Wählen Sie aus, ob das Ausgabebild RGB- oder RGBA-Farbe verwenden soll. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maskenformat]</p>
      </td>
   <td>Wählen Sie aus, ob die Maske weich (gefedert) oder binär sein soll. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL optimieren]</p>
      </td>
   <td>Wählen Sie Leistung aus, um die Geschwindigkeit zu optimieren, oder Batch, um Wartezeiten zuzulassen. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nachbearbeitungsprozess]</p>
      </td>
   <td>Wählen Sie aus, ob die Nachbearbeitung aktiviert werden soll.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>Der Standardwert ist 4.0</td> 
    </tr> 
    </tbody>
</table>

#### Erstellen einer neuen PSD (veraltet)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Erstellen oder Bearbeiten eines zusammengesetzten &#x200B;](#create-or-edit-a-composite)&quot;.

Dieses Aktionsmodul erstellt eine neue PSD mit optionalen Ebenen und generiert Ausgabedarstellungen oder speichert sie als PSD.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument &gt; Bildgröße) Höhe]</p>
      </td>
      <td> Geben Sie die Höhe des Bildes in Pixel ein oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument &gt; Bildgröße) Breite]</p>
      </td>
      <td> Geben Sie die Breite des Bildes in Pixel ein oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument)-Auflösung]</p>
      </td>
   <td> Geben Sie die Auflösung für das Bild in Pixeln pro Zoll ein oder mappen Sie sie. Dieser muss zwischen 72 und 300 liegen. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokumentmodus)]</p>
      </td>
   <td> Wählen Sie den Modus für das Bild aus. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokument) ausfüllen]</p>
      </td>
   <td> Wählen Sie aus, ob die Füllung für die Hintergrundebene transparent, weiß oder die Hintergrundfarbe des Bildes sein soll. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen &gt; Dokumenttiefe)]</p>
      </td>
   <td> Wählen Sie die Bittiefe des Bildes aus. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen)-Ebenen]</p>
      </td>
   <td> Klicken Sie für jede Ebene, die Sie hinzufügen möchten, auf Element hinzufügen und füllen Sie die Ebenendetails aus. <p>Weitere Informationen zu Ebenenoptionen finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync">PSD erstellen</a> in der Adobe Photoshop-Dokumentation.  </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen), globale Schriftart]</p>
      </td>
   <td> Geben Sie den vollständigen PostScript-Namen der Schriftart ein, die als globaler Standard für das Dokument verwendet werden soll. Diese Schriftart wird für alle Textebenen verwendet, in denen die Schriftart fehlt, und es wurde keine andere Schriftart speziell für diese Ebene angegeben. Wenn diese Schriftart fehlt, wird die unter Fehlende Schriftarten verwalten angegebene Option wirksam. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen) Schriftarten]</p>
      </td>
   <td> Klicken Sie für jede Schriftart, die das Dokument benötigt, auf Element hinzufügen und geben Sie den Speicherort und den Dateispeicherort der Schriftart ein. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen): fehlende Schriftarten verwalten]</p>
      </td>
   <td> Auswahl der Aktion, die ausgeführt werden soll, wenn im Dokument eine oder mehrere Schriftarten fehlen. <ul><li><code>fail</code>: Der Vorgang ist nicht erfolgreich und der Status wird auf „Fehlgeschlagen“ gesetzt, wobei die Details zum Fehler im Detailabschnitt des Status angegeben werden.</li><li><code>useDefault</code>: Der Vorgang wird erfolgreich sein und alle fehlenden Schriftarten werden durch ArialMT ersetzt.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie den Speicherort, den Speicherort und den Typ wie aufgeführt ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die neue Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die neue Datei gespeichert werden soll, oder mappen Sie sie. Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Typ]</p>
      </td>
   <td>Wählen Sie den Dateityp aus, in den Sie die Datei konvertieren möchten. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe) Andere Felder]</td>
      <td>
        <p><p>Weitere Informationen zu Ausgabeoptionen finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync">PSD erstellen</a> in der Dokumentation zu Adobe Photoshop.  </p>
      </td>
    </tr>
    </tbody>
</table>

#### Erstellen von Ausgabedarstellungen (veraltet)

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die zu bearbeitende Datei gespeichert ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Eingabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie bearbeiten möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie die Speicher-, Speicherort-, Typ- und Überschreibungsoption wie aufgeführt ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgänge)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe) Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output)-Typ]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgänge) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
      </tbody>
</table>

#### Bearbeiten von Textebenen (alt)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Ausführen von Photoshop-Aktionen, -Skripten und -](#execute-photoshop-actions-scripts-and-transformations)&quot;.

Dieses Aktionsmodul bearbeitet Textebenen in einer Photoshop-Datei. Sie können separate Bearbeitungsdetails für mehrere Ebenen in derselben Datei eingeben.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Eingabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die zu bearbeitende Datei gespeichert ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eingabedatei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie bearbeiten möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL fehlende Schriftarten verwalten]</td>
      <td>
        <p>Auswahl der Aktion, die ausgeführt werden soll, wenn im Dokument eine oder mehrere Schriftarten fehlen. Wenn die Schriftart nicht angegeben ist, verwendet das Modul die Standardschriftart.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Standardschriftart]  </td>
      <td>
        <p>Geben Sie den vollständigen PostScript-Namen der Schriftart ein, die als globaler Standard für das Dokument verwendet werden soll. Diese Schriftart wird für alle Textebenen verwendet, in denen die Schriftart fehlt, und es wurde keine andere Schriftart speziell für diese Ebene angegeben. Wenn diese Schriftart fehlt, wird die unter Fehlende Schriftarten verwalten angegebene Option wirksam.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen) Schriftarten]</p>
      </td>
   <td> Geben Sie den Speicherort und den Dateispeicherort der Schriftart ein. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -Ebenen]</td>
   <td> <p>Klicken Sie für jede Textebene, die Sie bearbeiten möchten, auf <b>Element hinzufügen</b> und geben Sie die Ebenenoptionen ein.<p>Weitere Informationen zu Ebenenoptionen finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync">Text bearbeiten</a> in der Adobe Photoshop-Dokumentation.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Typ]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Bearbeiten von Textebenen 2 (alt)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Ausführen von Photoshop-Aktionen, -Skripten und -](#execute-photoshop-actions-scripts-and-transformations)&quot;.

Dieses Aktionsmodul bearbeitet eine Textebene in einer Photoshop-Datei.

Um mehrere Ebenen zu bearbeiten, verwenden Sie das Modul [Textebenen bearbeiten](#edit-text-layers) .

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Eingabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die zu bearbeitende Datei gespeichert ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eingabedatei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie bearbeiten möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL fehlende Schriftarten verwalten]</td>
      <td>
        <p>Auswahl der Aktion, die ausgeführt werden soll, wenn im Dokument eine oder mehrere Schriftarten fehlen. Wenn die Schriftart nicht angegeben ist, verwendet das Modul die Standardschriftart.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Standardschriftart]  </td>
      <td>
        <p>Geben Sie den vollständigen PostScript-Namen der Schriftart ein, die als globaler Standard für das Dokument verwendet werden soll. Diese Schriftart wird für alle Textebenen verwendet, in denen die Schriftart fehlt, und es wurde keine andere Schriftart speziell für diese Ebene angegeben. Wenn diese Schriftart fehlt, wird die unter Fehlende Schriftarten verwalten angegebene Option wirksam.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen) Schriftarten]</p>
      </td>
   <td> Geben Sie den Speicherort und den Dateispeicherort der Schriftart ein. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -Ebenen]</td>
   <td> <p>Weitere Informationen zu Ebenenoptionen finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync">Textebene bearbeiten</a> in der Adobe Photoshop-Dokumentation.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Typ]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
  </tbody>
</table>


#### Ausführen einer JSON-Aktion (alt)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Ausführen von Photoshop-Aktionen, -Skripten und -](#execute-photoshop-actions-scripts-and-transformations)&quot;.

Dieses Aktionsmodul führt Photoshop-Aktionen mithilfe von JSON-Befehlen aus.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die zu bearbeitende Datei gespeichert ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Eingabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie bearbeiten möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Aktion JSON]</td>
      <td>
        <p>Geben Sie den JSON-Befehl für die Aktion ein, die Sie ausführen möchten.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Schriftarten / Muster / Pinsel / Zusätzliche Bilder]</td>
      <td>
        <p>Klicken Sie für jede Schriftart, jedes Muster, jeden Pinsel oder jedes zusätzliche Bild, das Sie in dieser Aktion verwenden möchten, auf Element hinzufügen und geben Sie den Speicherort und den Dateispeicherort des Elements ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Schriftart/Muster/Pinseldatei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie verwenden möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie die Speicher-, Speicherort-, Typ- und Überschreibungsoption wie aufgeführt ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgänge)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe) Datei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output)-Typ]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgänge) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
      </tbody>
</table>

#### Tiefenunschärfe ausführen (alt)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.

Dieses Aktionsmodul führt „Tiefenunschärfe“ für die ausgewählte Datei aus.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Eingabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die zu bearbeitende Datei gespeichert ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eingabedatei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie bearbeiten möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgänge)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe) Datei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output)-Typ]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgänge) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Andere Felder]</td>
      <td>
        <p>Weitere Informationen zu anderen Optionen für Tiefenunschärfe finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Tiefenunschärfe ausführen</a> in der Adobe Photoshop-API-Dokumentation.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Ausführen von Photoshop-Aktionen (veraltet)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Ausführen von Photoshop-Aktionen, -Skripten und -](#execute-photoshop-actions-scripts-and-transformations)&quot;.

Dieses Aktionsmodul führt eine Photoshop-Aktion für das ausgewählte Bild aus.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Eingabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die zu bearbeitende Datei gespeichert ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eingabedatei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie bearbeiten möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Actions Dateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Aktionsdatei gespeichert wird.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Aktionsdatei URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Aktionsdatei ein oder mappen Sie ihn. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Aktionsname]</p>
      </td>
   <td> Wenn Sie nur eine bestimmte Aktion ausführen möchten, können Sie aus dem ActionSet angeben, welche Aktion wiedergegeben werden soll. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Schriftart/Muster/Pinselspeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die zu verwendende Datei gespeichert ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Schriftart/Muster/Pinseldatei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie verwenden möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgänge)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe) Datei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output)-Typ]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgänge) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Andere Felder]</td>
      <td>
        <p>Weitere Informationen zu anderen Optionen für Tiefenunschärfe finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Tiefenunschärfe ausführen</a> in der Adobe Photoshop-API-Dokumentation.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Ausführen eines Produktzuschnitts (veraltet)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Ausführen von Photoshop-Aktionen, -Skripten und -](#execute-photoshop-actions-scripts-and-transformations)&quot;.

Dieses Aktionsmodul führt das Produktzuschneiden für das ausgewählte Bild aus.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Eingabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Datei gespeichert wird, die Sie zuschneiden möchten.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eingabedatei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, die Sie zuschneiden möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL UNIT]</p>
      </td>
   <td> Wählen Sie aus, ob die Höhen- und Breiteneinstellung in Pixel oder als Prozentsatz beschrieben werden soll. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Breite]</p>
      </td>
   <td> Geben Sie den Betrag des Breitenabstands ein, den Sie hinzufügen möchten, oder ordnen Sie ihn zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Höhe]</p>
      </td>
   <td> Geben Sie den Betrag des Höhenabstands ein, den Sie hinzufügen möchten, oder ordnen Sie ihn zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgänge)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe) Datei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output)-Typ]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgänge) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Andere Felder]</td>
      <td>
        <p>Weitere Informationen zu anderen Optionen für Tiefenunschärfe finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Tiefenunschärfe ausführen</a> in der Adobe Photoshop-API-Dokumentation.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Abrufen von Ebeneninformationen (veraltet)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Manifest &#x200B;](#generate-a-manifest)generieren.

Dieses Aktionsmodul ruft Ebeneninformationen aus der angegebenen PSD-Datei ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Eingabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Datei gespeichert ist, von der Ebeneninformationen abgerufen werden sollen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Eingabedatei-URL]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, von der Ebeneninformationen abgerufen werden sollen, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Miniaturansichten]</p>
      </td>
   <td> Wählen Sie den Dateityp aus, in dem die Miniaturen gespeichert werden sollen. Miniaturansichten sind kleine Vorschauen für jede renderbare Ebene.</td> 
    </tr>
  </tbody>
</table>

#### Benutzerdefinierten API-Aufruf erstellen

Dieses Aktionsmodul führt einen benutzerdefinierten Aufruf an die Photoshop-API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://image.adobe.io/pie/psdService</code> ein. Beispiel: <code>/photoshopActions</code></p>
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
      <td role="rowheader">[!UICONTROL Abfragezeichenfolge]  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
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

#### Ersetzen eines Smart-Objekts (alt)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Erstellen oder Bearbeiten eines zusammengesetzten &#x200B;](#create-or-edit-a-composite)&quot;.

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Erstellen oder Bearbeiten eines zusammengesetzten &#x200B;](#create-or-edit-a-composite)&quot;.

Dieses Aktionsmodul ersetzt ein Smart-Objekt in einer PSD-Ebene und generiert neue Ausgabedarstellungen.

Dieses Modul verwendet die Smart Object API Version 2.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem das Smart-Objekt gespeichert ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Eingabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad des Smart-Objekts ein oder ordnen Sie ihn zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL -Ebenen]</p>
      </td>
   <td>Klicken Sie für jede Ebene, die Sie dem Smart-Objekt hinzufügen möchten, auf Element hinzufügen und geben Sie den Namen oder die ID des Objekts, den Datei-Service, in dem das Smart-Objekt gespeichert ist, und die URL oder den Pfad der Ebene ein.<p>Beschreibungen der erweiterten Einstellungen in diesem Bereich finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync">Ersetzen eines Smart-Objekts</a> in der Dokumentation zur Photoshop-API </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Größe des Bildes während der Platzierung ändern]</p>
      </td>
   <td> Wählen Sie aus, ob die Bildgröße geändert werden soll.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede neue Ausgabedarstellung, die das Modul erstellen soll, auf Element hinzufügen und füllen Sie die folgenden Felder aus. Sie können maximal 25 Ausgabedateien haben.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die neue Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die neue Datei gespeichert werden soll, oder mappen Sie sie.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output)-Typ]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
     </tbody>
</table>

#### Ersetzen eines Smart-Objekts 2 (alt)

Dieses Aktionsmodul ersetzt ein Smart-Objekt in einer PSD-Ebene und generiert neue Ausgabedarstellungen.

Dieses Modul verwendet die Legacy-Version von Smart-Objekten.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem das Smart-Objekt gespeichert ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Eingabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad des Smart-Objekts ein oder ordnen Sie ihn zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL -Ebenen]</p>
      </td>
   <td>Klicken Sie für jede Ebene, die Sie dem Smart-Objekt hinzufügen möchten, auf Element hinzufügen und geben Sie den Namen oder die ID des Objekts, den Datei-Service, in dem das Smart-Objekt gespeichert ist, und die URL oder den Pfad der Ebene ein.<p>Beschreibungen der erweiterten Einstellungen in diesem Bereich finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync">Ersetzen eines Smart-Objekts</a> in der Dokumentation zur Photoshop-API </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede neue Ausgabedarstellung, die das Modul erstellen soll, auf Element hinzufügen und füllen Sie die folgenden Felder aus. Sie können maximal 25 Ausgabedateien haben.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die neue Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die neue Datei gespeichert werden soll, oder mappen Sie sie.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe) Breite]</p>
      </td>
   <td> Die Breite der Ausgabedatei in Pixel. Das Modul behält das ursprüngliche Seitenverhältnis bei. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll. Dies gilt nur für Dateien im Adobe-Speicher.</p>
      </td>
    </tbody>
</table>

#### Größe eines Bildes ändern (veraltet)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Erstellen oder Bearbeiten eines zusammengesetzten &#x200B;](#create-or-edit-a-composite)&quot;.

Mit dieser Aktion wird die Größe eines Bildes geändert, wobei dasselbe Seitenverhältnis verwendet wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Datei gespeichert wird, deren Größe geändert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, deren Größe Sie ändern möchten, oder ordnen Sie sie zu.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede konvertierte Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie den Speicherort, den Speicherort und andere Optionen wie aufgeführt ein.</p>
      </td>
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL -Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die neue Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die neue Datei gespeichert werden soll, oder mappen Sie sie.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Breite]</p>
      </td>
   <td> Die Breite der Ausgabedatei in Pixel. Das Modul behält das ursprüngliche Seitenverhältnis bei. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Max. Breite]</p>
      </td>
   <td>Wenn die Breite 0 ist, kann Max. mit bereitgestellt werden, um die Größe abzurufen. Die maximale Breite hat Vorrang, da sie kleiner ist als die Dokumentbreite.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll. Dies gilt nur für Dateien im Adobe-Speicher.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Auf Arbeitsfläche zuschneiden]</p>
      </td>
   <td>Wählen Sie Ja , um die Ausgabedarstellungen auf die Arbeitsflächengröße zu kürzen, oder Nein , um die Größe der Ausgabedarstellungsebene festzulegen.</td> 
    </tr>
    </tbody>
</table>

#### Wasserzeichen für ein Bild (veraltet)

>[!NOTE]
>
>Dieses Modul wird nicht mehr unterstützt und funktioniert nach dem 30. Juli 2026 nicht mehr.
>Aktualisieren Sie dieses Modul zum Modul [Erstellen oder Bearbeiten eines zusammengesetzten &#x200B;](#create-or-edit-a-composite)&quot;.

Dieses Aktionsmodul fügt dem ausgewählten Bild ein Wasserzeichen hinzu.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu den [!DNL Adobe Photoshop] finden Sie in diesem Artikel unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu den [!DNL Adobe Photoshop]</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Basis &gt; Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Datei gespeichert wird, der Sie ein Wasserzeichen hinzufügen möchten.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Basis &gt; Eingabe) Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, der Sie ein Wasserzeichen hinzufügen möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Wasserzeichen &gt; Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem das hinzuzufügende Wasserzeichen gespeichert wird.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Wasserzeichen &gt; Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem das hinzuzufügende Wasserzeichen gespeichert wird.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Wasserzeichen &gt; Grenzen) Höhe]</p>
      </td>
   <td>Geben Sie die gewünschte Höhe des Wasserzeichens in Pixel ein oder mappen Sie sie.</td> 
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Wasserzeichen &gt; Grenzen) Breite]</p>
      </td>
   <td> Geben Sie die gewünschte Breite des Wasserzeichens in Pixel ein oder mappen Sie sie. </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Wasserzeichen &gt; Grenzen) links]</p>
      </td>
   <td> Geben Sie den Abstand in Pixeln von der linken Seite des Bildes ein, in dem das Wasserzeichen sein soll, oder mappen Sie ihn.</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Wasserzeichen &gt; Grenzen) oben]</p>
      </td>
   <td> Geben Sie den Abstand in Pixeln vom oberen Rand des Bildes ein, in dem das Wasserzeichen sein soll, oder mappen Sie ihn.</td> 
    </tr>  
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die mit Wasserzeichen versehene Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die mit Wasserzeichen versehene Datei gespeichert werden soll, oder mappen Sie diese. Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Typ]</p>
      </td>
   <td>Wählen Sie den Dateityp aus, in den Sie die Datei konvertieren möchten. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe) Breite]</p>
      </td>
   <td> Die Breite der Ausgabedatei in Pixel. Das Modul behält das ursprüngliche Seitenverhältnis bei. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe) überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll. Dies gilt nur für Dateien im Adobe-Speicher.</p>
      </td>
    </tbody>
</table>
