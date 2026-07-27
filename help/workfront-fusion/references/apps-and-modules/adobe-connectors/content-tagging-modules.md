---
title: Adobe Content Tagger-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Adobe Content Tagger verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: 737e9b07237960d5833cd21e110ef573ddd0a72c
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 21%

---

# Adobe Content Tagger-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Adobe Content Tagger verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

## Erstellen einer Verbindung mit Adobe Content Tagger

So erstellen Sie eine Verbindung für Ihre Adobe Content Tagger-Module:

1. Klicken Sie in einem beliebigen Modul **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Verbindungsname</td>
        <td>
          <p>Geben Sie einen Namen für die Verbindung ein.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Umgebung</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td>
        </tr>
        <tr>
        <td role="rowheader">Typ</td>
        <td>Wählen Sie aus, ob eine Verbindung zu einem Service-Konto oder einem persönlichen Konto hergestellt werden soll.</td>
        </tr>
        <tr>
        <td role="rowheader">Client-ID</td>
        <td>Geben Sie Ihre Adobe-Client-ID ein. Diese finden Sie im Abschnitt Anmeldedaten des Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Client-Geheimnis</td>
        <td>Geben Sie Ihr Adobe-Client-Geheimnis ein. Diese finden Sie im Abschnitt Anmeldedaten des Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Verbindung zu speichern und zum Modul zurückzukehren.


## Adobe Content Tagger-Module und ihre Felder

Beim Konfigurieren von Adobe Content Tagger-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können zusätzliche Adobe Content Tagger-Felder angezeigt werden, abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Aktionen

* [Tag-Farben](#tag-colors)
* [Tag-Schlüsselwörter](#tag-keywords)
* [Tag-Text in einem Bild](#tag-text-in-an-image)

#### Tag-Farben

Dieses Modul gibt den Prozentsatz eines Bildes zurück, das von verschiedenen Pixelfarben abgedeckt wird, sortiert in 40 Farbkategorien.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Content Tagger finden Sie unter <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Content Tagger</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name der Bilddatei</td> 
   <td>Geben Sie den Dateinamen des Bildes ein, für das Sie Farben taggen möchten, oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bilddaten</td> 
   <td>Geben Sie die Dateidaten des Bildes ein, für das Sie Farben taggen möchten, oder mappen Sie sie.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Bildformat</td> 
    <td>Wählen Sie den Bildtyp für das Bild aus, für das Sie Farben taggen möchten.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Anzahl Farben</td> 
    <td>Geben Sie die Anzahl der zurückzugebenden Farben ein oder mappen Sie sie. Um alle Ergebnisse zurückzugeben, geben Sie 0 ein.</p></td> 
  </tr> 
 <tr> 
   <td role="rowheader">Mindestdeckung</td> 
   <td>Geben Sie die Mindestabdeckung ein, für die Sie Farben taggen möchten, oder mappen Sie sie. Es werden nur Farben zurückgegeben, die mindestens diese Bildmenge abdecken. Ein Wert von 1 entspricht 100 % des Bildes und ein Wert von .5 entspricht 50 % des Bildes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ändern Sie die Bildgröße vor der Extraktion.</td> 
   <td>Wählen Sie Ja , um die Bildgröße auf 320 x 320 zu ändern, bevor Sie die Farben extrahieren. Wählen Sie Nein , um Farben aus dem Bild in voller Größe zu extrahieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vordergrund-/Hintergrundmaske aktivieren</td> 
   <td>Wählen Sie Ja , wenn Sie Farben für das Gesamtbild, den Vordergrund und den Hintergrund separat auswerten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Töne abrufen</td> 
   <td>Wählen Sie Ja , wenn Sie zusätzlich zu den Farben Daten zu warmen, neutralen und kühlen Tönen abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Farben</td> 
   <td>Geben Sie die maximale Anzahl von Farben ein, die das Modul für einen Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>



#### Tag-Schlüsselwörter

Dieses Modul extrahiert Schlüsselwörter oder Schlüsselbegriffe, die das Thema des Dokuments am besten beschreiben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Content Tagger finden Sie unter <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Content Tagger</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name der Dokumentdatei</td> 
   <td>Geben Sie den Dateinamen des Dokuments ein, aus dem Sie Schlüsselwörter extrahieren möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bilddaten</td> 
   <td>Geben Sie die Dateidaten des Dokuments ein, aus dem Sie Schlüsselwörter extrahieren möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Bildformat</td> 
    <td>Wählen Sie das Format des Dokuments aus, aus dem Sie Schlüsselwörter extrahieren möchten.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Anwendungs-ID</td> 
   <td>Geben Sie die Anwendungs-ID für das Dokument ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Anzahl der Schlüsselbegriffe</td> 
   <td>Geben Sie die Anzahl der Schlüsselsätze ein, die das Modul zurückgeben soll, oder mappen Sie sie. Um alle Ergebnisse zurückzugeben, geben Sie 0 ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Minimale Relevanz</td> 
   <td>Geben Sie den Schwellenwert für die Bewertung ein, unterhalb dessen keine Ergebnisse zurückgegeben werden, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Minimale Länge des Schlüsselsatzes (Wörter)</td> 
   <td>Geben Sie die Mindestanzahl von Wörtern ein, die in Schlüsselbegriffen erforderlich sind, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Länge des Schlüsselsatzes (Wörter)</td> 
   <td>Geben Sie die maximale Anzahl von Wörtern ein, die in Schlüsselbegriffen erforderlich sind, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tiefe der semantischen Einheit</td> 
   <td>Wählen Sie aus, wie tief die hierarchischen Antworten gehen sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Entitätstypen</td> 
   <td>Klicken Sie für jeden Entitätstyp, auf den Sie die Schlüsselbegriffe beschränken möchten, auf <b>Element hinzufügen</b> und geben Sie die Informationen für den Entitätstyp ein.</td> 
  </tr> 
 </tbody> 
</table>

#### Tag-Text in einem Bild

Dieses Modul gibt an, ob Text in einem Bild vorhanden ist, und gibt den Text zurück, falls vorhanden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Content Tagger finden Sie unter <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Content Tagger</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name der Bilddatei</td> 
   <td>Geben Sie den Dateinamen des Dokuments ein, aus dem Sie Text extrahieren möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bilddaten</td> 
   <td>Geben Sie die Dateidaten des Dokuments ein, aus dem Sie Text extrahieren möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Bildformat</td> 
    <td>Wählen Sie das Format des Dokuments aus, aus dem Sie Text extrahieren möchten.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Mit Wörterbuch filtern</td> 
   <td>Wählen Sie aus, ob nur Wörter zurückgegeben werden sollen, die sich im englischen Wörterbuch befinden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Minimale Wahrscheinlichkeit</td> 
   <td>Geben Sie die Mindestwahrscheinlichkeit ein, mit der das Modul nur Wörter zurückgibt, die mit mindestens dieser Wahrscheinlichkeit erkannt werden, oder mappen Sie sie. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Minimale Relevanz</td> 
   <td>Geben Sie den minimalen Prozentsatz des Bildes ein, den der zurückgegebene Text abdecken soll. Die Relevanz wird als Bruchteil des Bereichs des Begrenzungsrahmens des extrahierten Textes im Vergleich zum vollständigen Bild berechnet. 0,01 würde in einen Text übersetzt werden, der mindestens 1 % des Bildes einnimmt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Ergebnissen ein, die das Modul für einen Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>
