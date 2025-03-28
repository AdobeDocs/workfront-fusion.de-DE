---
title: Adobe Photoshop-Module
description: Mit den Adobe Photoshop-Modulen können Sie ein Adobe Workfront Fusion-Szenario auf der Grundlage von Ereignissen in Ihrem Adobe Photoshop-Konto starten, Vereinbarungen erstellen, lesen oder aktualisieren und andere Datensätze suchen, anhand der von Ihnen festgelegten Kriterien nach Datensätzen suchen und Dokumente hochladen.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
source-git-commit: db1d6f5bf29063b069681395c6ff6d3554c67dc3
workflow-type: tm+mt
source-wordcount: '4359'
ht-degree: 0%

---

# [!DNL Adobe Photoshop]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Adobe Photoshop] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.


Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

+++**Erweitern Sie , um die Zugriffsanforderungen für die Funktion in diesem Artikel anzuzeigen.**

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] Plan*</td>
      <td>
        <p>[!UICONTROL Pro] oder höher</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td>
      <td>
        <p>[!UICONTROL-Plan], [!UICONTROL-Arbeit]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td>
      <td >
        <p>[!UICONTROL Workfront Fusion for Work Automation and Integration]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Produkt</td>
      <td>Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu nutzen.</td>
    </tr>
    </tr>
  </tbody>
</table>


&#42;Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

&#42;&#42;Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [!DNL [Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Bevor Sie den [!DNL Adobe Photoshop]-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein aktives [!DNL Adobe Photoshop] verfügen.
* Sie müssen über eine Firefly Services-Lizenz verfügen.
* Sie müssen über eine Client-ID und ein Client-Geheimnis verfügen. Sie können diese von der Adobe Developer Console beziehen.

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

## Erstellen einer Verbindung zu [!DNL Adobe Photoshop]

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe Photoshop]:

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
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre [!UICONTROL Adobe] [!UICONTROL Client-ID] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihren [!DNL Adobe] [!UICONTROL Client Secret] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID des technischen Kontos]</td>
        <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL ID des technischen Kontos] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Organisations-ID]</td>
        <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL Organisations-ID] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Privater Schlüssel]</td>
        <td>
          <p>Geben Sie den privaten Schlüssel ein, der bei der Erstellung Ihrer Anmeldeinformationen im [!DNL Adobe Developer Console] generiert wurde. </p>
          <p>So extrahieren Sie Ihren privaten Schlüssel oder Ihr Zertifikat:</p>
          <ol>
            <li value="1">
              <p>Klicken Sie auf <b>[!UICONTROL Extract]</b>.</p>
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

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## [!DNL Adobe Photoshop] Module und ihre Felder

Beim Konfigurieren [!DNL Adobe Photoshop] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Adobe Photoshop] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [PSD-Bearbeitungen anwenden](#apply-psd-edits)
* [Automatische Farbkorrektur eines Bildes](#auto-color-correct-an-image)
* [Bildformat konvertieren](#convert-image-format)
* [Erstellen einer Maske](#create-a-mask)
* [Erstellen einer neuen PSD](#create-a-new-psd)
* [Bearbeiten von Textebenen](#edit-text-layers)
* [Tiefenunschärfe ausführen](#execute-depth-blur)
* [Ausführen von Photoshop-Aktionen](#execute-photoshop-actions)
* [Ausführen von Photoshop-Aktionen (JSON)](#execute-photoshop-actions-json)
* [Ausführen eines Produktzuschnitts](#execute-product-crop)
* [Abrufen von Ebeneninformationen](#get-layer-info)
* [Erstellen eines benutzerdefinierten API-Aufrufs](#make-a-custom-api-call)
* [Hintergrund entfernen](#remove-background)
* [Ersetzen eines Smart-Objekts](#replace-a-smart-object)
* [Ändern der Bildgröße](#resize-an-image)
* [Wasserzeichen für ein Bild](#watermark-an-image)

### PSD-Bearbeitungen anwenden

Dieses Aktionsmodul wendet eine Vielzahl von Bearbeitungen auf Dokument- und Ebenenebene an.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
   <td> Auswahl der Aktion, die ausgeführt werden soll, wenn im Dokument eine oder mehrere Schriftarten fehlen. <ul><li><code>fail</code>: Der Vorgang ist nicht erfolgreich und der Status wird auf „Fehlgeschlagen“ gesetzt, wobei die Details zum Fehler im Detailabschnitt des Status angegeben werden.</li><li><code>useDefault</code>: Der Vorgang ist erfolgreich, aber standardmäßig werden alle fehlenden Schriftarten durch ArialMT ersetzt.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Optionen)-Ebenen]</p>
      </td>
   <td> Klicken Sie für jede Ebene, die Sie hinzufügen möchten, auf Element hinzufügen und füllen Sie die Ebenendetails aus. <p>Weitere Informationen zu Ebenenoptionen finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_applyPsdEdits/">PSD-Bearbeitungen anwenden</a> in der Dokumentation zu Adobe Photoshop.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede konvertierte Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie den Speicherort, den Speicherort und den Typ wie in dieser Tabelle aufgeführt ein.</p>
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
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</p>
      </td>
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
    </tbody>
</table>



### Automatische Farbkorrektur eines Bildes

Dieses Aktionsmodul korrigiert automatisch das angegebene Bild.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</p>
      </td>
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
    </tbody>
</table>


### Bildformat konvertieren

Dieses Aktionsmodul konvertiert eine Datei in JPEG, PNG, PSD oder TIFF.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
        <p>Klicken Sie für jede konvertierte Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie den Speicherort, den Speicherort und den Typ wie in dieser Tabelle aufgeführt ein.</p>
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
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</p>
      </td>
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
    </tbody>
</table>



### Erstellen einer Maske

Dieses Aktionsmodul gibt eine PNG-Datei mit einem Mast um das Subjekt herum zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
   <td></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>Der Standardwert ist 4.0</td> 
    </tr> 
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</p>
      </td>
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
    </tbody>
</table>

### Erstellen einer neuen PSD

Dieses Aktionsmodul erstellt eine neue PSD mit optionalen Ebenen und generiert Ausgabedarstellungen oder speichert sie als PSD.

Felder, die sich auf dieses Modul beziehen, finden Sie [Erstellen einer neuen PSD](https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/documentCreate) in der Dokumentation zu Adobe Photoshop.

### Bearbeiten von Textebenen

Dieses Aktionsmodul bearbeitet Textebenen in einer Photoshop-Datei.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
      <td role="rowheader">[!UICONTROL-Ebenen]</td>
   <td> <p>Weitere Informationen zu Ebenenoptionen finden Sie unter <a href="https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/text">Textebene bearbeiten</a> in der Adobe Photoshop-Dokumentation.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL der Ausgabedatei]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ausgabedateityp]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Komprimierung]</p>
      </td>
   <td> Wählen Sie den Komprimierungsgrad für die Ausgabedatei. </td> 
    </tr>
  </tbody>
</table>



### Ausführen von Photoshop-Aktionen (JSON)

Dieses Aktionsmodul führt Photoshop-Aktionen mithilfe von JSON-Befehlen aus.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
      <td role="rowheader">[!UICONTROL Ausgabe Dateispeicherung]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p><p>Wenn Sie Fusion Internal Storage auswählen, wird die Datei für spätere Module verfügbar, aber nicht außerhalb des Szenarios.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL der Ausgabedatei]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie.  Dies ist nur erforderlich, wenn Sie für den Ausgabespeicher keinen internen Fusion-Speicher ausgewählt haben.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ausgabedateityp]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Komprimierung]</p>
      </td>
   <td> Wählen Sie den Komprimierungsgrad für die Ausgabedatei. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgaben]</td>
      <td>
        <p>Klicken Sie für jede konvertierte Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie den Speicherort, den Speicherort und den Typ wie in dieser Tabelle aufgeführt ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Ausgabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die neue Datei gespeichert werden soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Ausgabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die neue Datei gespeichert werden soll, oder mappen Sie sie. </td> 
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
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</p>
      </td>
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
      </tbody>
</table>

### Tiefenunschärfe ausführen

Dieses Aktionsmodul führt „Tiefenunschärfe“ für die ausgewählte Datei aus.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
      <td role="rowheader">[!UICONTROL Ausgabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL der Ausgabedatei]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ausgabedateityp]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Andere Felder]</td>
      <td>
        <p>Weitere Informationen zu anderen Optionen für Tiefenunschärfe finden Sie unter <a href="https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/depthBlur">Tiefenunschärfe ausführen</a> in der Adobe Photoshop-API-Dokumentation.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Komprimierung]</p>
      </td>
   <td> Wählen Sie den Komprimierungsgrad für die Ausgabedatei. </td> 
    </tr>
  </tbody>
</table>

### Ausführen von Photoshop-Aktionen

Dieses Aktionsmodul führt eine Photoshop-Aktion für das ausgewählte Bild aus.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
      <td role="rowheader">[!UICONTROL Ausgabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL der Ausgabedatei]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ausgabedateityp]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Komprimierung]</p>
      </td>
   <td> Wählen Sie den Komprimierungsgrad für die Ausgabedatei. </td> 
    </tr>
  </tbody>
</table>

### Ausführen eines Produktzuschnitts

Dieses Aktionsmodul führt das Produktzuschneiden für das ausgewählte Bild aus.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
      <td role="rowheader">[!UICONTROL Ausgabedateispeicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die bearbeitete Datei gespeichert werden soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL der Ausgabedatei]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad ein, unter dem die bearbeitete Datei gespeichert wird, oder mappen Sie sie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ausgabedateityp]</p>
      </td>
   <td> Dateityp für die bearbeitete Datei auswählen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL überschreiben]</td>
      <td>
        <p>Wählen Sie aus, ob die neu bearbeitete Datei alle bereits vorhandenen Ausgabedateien überschreiben soll.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Komprimierung]</p>
      </td>
   <td> Wählen Sie den Komprimierungsgrad für die Ausgabedatei. </td> 
    </tr>
  </tbody>
</table>

### Abrufen von Ebeneninformationen

Dieses Aktionsmodul ruft Ebeneninformationen aus der angegebenen PSD-Datei ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
   <td> </td> 
    </tr>
  </tbody>
</table>

### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt einen benutzerdefinierten Aufruf an die Photoshop-API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://image.adobe.io/pie/psdService</code> ein. Beispiel: <code>/photoshopActions</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL-Methode]</p>
      </td>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL-Kopfzeilen]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Abfragezeichenfolge]  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
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

### Hintergrund entfernen

Dieses Aktionsmodul identifiziert das Hauptsubjekt Ihres Bildes und entfernt den Hintergrund.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
   <td></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>Der Standardwert ist 4.0</td> 
    </tr> 
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</p>
      </td>
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
    </tbody>
</table>



### Ersetzen eines Smart-Objekts

Dieses Aktionsmodul ersetzt ein Smart-Objekt in einer PSD-Ebene und generiert neue Ausgabedarstellungen.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
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
        <p>[!UICONTROL-Ebenen]</p>
      </td>
   <td>Klicken Sie für jede Ebene, die Sie dem Smart-Objekt hinzufügen möchten, auf Element hinzufügen und geben Sie den Namen oder die ID des Objekts, den Datei-Service, in dem das Smart-Objekt gespeichert ist, und die URL oder den Pfad der Ebene ein.<p>Beschreibungen der erweiterten Einstellungen in diesem Bereich finden Sie unter <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_replaceSmartObject/">Ersetzen eines Smart-Objekts</a> in der Dokumentation zur Photoshop-API </td> 
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
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</p>
      </td>
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
    </tbody>
</table>



### Ändern der Bildgröße

Mit dieser Aktion wird die Größe eines Bildes geändert, wobei dasselbe Seitenverhältnis verwendet wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL-Speicher]</td>
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
        <p>Klicken Sie für jede konvertierte Datei, die Sie erstellen möchten, auf Element hinzufügen und geben Sie die Speicher-, Speicherort- und anderen Optionen wie in dieser Tabelle aufgeführt ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Typ]</p>
      </td>
   <td>Wählen Sie den Dateityp aus, in den Sie die Datei konvertieren möchten. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Breite]</p>
      </td>
   <td>Geben Sie eine Zahl ein, die die Breite des skalierten Bildes in Pixel darstellt. Das Seitenverhältnis wird beibehalten.</td> 
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

### Wasserzeichen für ein Bild

Dieses Aktionsmodul fügt dem ausgewählten Bild ein Wasserzeichen hinzu.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Photoshop] finden Sie unter <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Photoshop]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Basis-/Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem die Datei gespeichert wird, der Sie ein Wasserzeichen hinzufügen möchten.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Basis/Eingabe)-Dateispeicherort]</p>
      </td>
   <td> Geben Sie die URL oder den Pfad der Datei ein, der Sie ein Wasserzeichen hinzufügen möchten, oder ordnen Sie sie zu. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Wasserzeichen/Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem das hinzuzufügende Wasserzeichen gespeichert wird.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Wasserzeichen/Eingabe)-Speicher]</td>
      <td>
        <p>Wählen Sie den Datei-Service aus, in dem das hinzuzufügende Wasserzeichen gespeichert wird.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Wasserzeichen/Grenzen) Höhe]</p>
      </td>
   <td>Geben Sie die gewünschte Höhe des Wasserzeichens in Pixel ein oder mappen Sie sie.</td> 
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Wasserzeichen/Grenzen) Breite]</p>
      </td>
   <td> Geben Sie die gewünschte Breite des Wasserzeichens in Pixel ein oder mappen Sie sie. </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Wasserzeichen/Grenzen) links]</p>
      </td>
   <td> Geben Sie den Abstand in Pixeln von der linken Seite des Bildes ein, in dem das Wasserzeichen sein soll, oder mappen Sie ihn.</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Wasserzeichen/Grenzen) oben]</p>
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
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</p>
      </td>
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
    </tr>
    </tbody>
</table>
