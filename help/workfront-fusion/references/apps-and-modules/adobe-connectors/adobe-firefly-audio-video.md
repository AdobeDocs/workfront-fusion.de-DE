---
title: Adobe Firefly Audio- und Videomodule
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Adobe Firefly-Audio und -Video verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: f54338aa35b8453ac991c9e16974f2b61fd30168
workflow-type: tm+mt
source-wordcount: '1618'
ht-degree: 14%

---

# Adobe Firefly Audio- und Videomodule

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Adobe Firefly-Audio und -Video verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Bevor Sie den Adobe Firefly-Audio- und -Video-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein aktives Adobe Firefly Audio- und Videokonto verfügen.

## Erstellen einer Verbindung zu Adobe Firefly Audio and Video

So erstellen Sie eine Verbindung für Ihre Adobe Firefly-Audio- und -Videomodule:

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


## Adobe Firefly Audio- und Videomodule und deren Felder

Beim Konfigurieren von Adobe Firefly-Audio- und -Videomodulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus werden möglicherweise zusätzliche Adobe Firefly-Audio- und -Videofelder angezeigt, abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Aktionen

* [Vorlage beschreiben](#describe-template)
* [Audio oder Video synchronisieren](#dub-audio-or-video)
* [Avatar-Video aus Text oder Audio generieren](#generate-avatar-video-from-text-or-audio)
* [Sprache aus Text generieren](#generate-speech-from-text)
* [Video umgestalten](#reframe-video)
* [Vorlage rendern](#render-template)
* [Transkribieren von Medien](#transcribe-media)

#### Vorlage beschreiben

Dieses Aktionsmodul analysiert eine MOGST-Datei (Video Template) und gibt ein Manifest von bearbeitbaren Steuerelementen, Schriftarten, Bildern, Audio, Video und anderen unterstützten Werten zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Firefly finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Firefly</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Geben Sie die vordefinierte URL ein, die auf die Eingabedatei verweist, oder ordnen Sie sie zu.</td> 
  </tr>
 </tbody> 
</table>

#### Audio oder Video synchronisieren

Dieses Aktionsmodul generiert synchronisiertes Audio oder Video. Das generierte Video kann auch eine Lippensynchronisation enthalten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Firefly finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Firefly</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Synchronisierungstyp</td> 
   <td>Wählen Sie aus, ob Sie einen Audio- oder Video-Duplikat generieren möchten.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Vordefinierte URL</td> 
   <td>Geben Sie die vordefinierte URL ein, die das Modul für die Eingabe verwenden soll, oder ordnen Sie sie zu.<p>Die folgenden Domains für die Medienspeicherung werden von Firefly Audio and Video akzeptiert</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Medientyp</td> 
   <td>Wählen Sie den Medientyp der Eingabedatei aus</td> 
  </tr>
  <tr> 
   <td role="rowheader">Lippensynchronisation</td> 
   <td>Wählen Sie aus, ob eine hochwertige zusammengesetzte Lippensynchronisation für die Videoausgabe erzeugt werden soll.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Code des Zielgebietsschemas</td> 
   <td>Klicken Sie für jeden Gebietsschema-Code, den Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und wählen Sie den Gebietsschema-Code aus.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Abschriften</td> 
   <td>Klicken Sie für jedes Transkript, das Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die vordefinierten URLs für das Transkript ein oder mappen Sie sie.</td> 
  </tr>
 </tbody> 
</table>

#### Avatar-Video aus Text oder Audio generieren

Dieses Aktionsmodul generiert ein Avatar-Video aus einem Transkript oder einer Audiodatei, die Sie bereitstellen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Firefly finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Firefly</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Geben Sie die vordefinierte URL ein, die das Modul für die Eingabe verwenden soll, oder ordnen Sie sie zu.   </td> 
  </tr>
  <tr> 
  <tr> 
   <td role="rowheader">Gebietsschema-Code</td> 
   <td>Wählen Sie den Gebietsschema-Code aus, der für die Sprache steht, die Sie im Ergebnis verwenden möchten.</td> 
  </tr>
   <td role="rowheader">Medientyp (Source)</td> 
   <td>Wählen Sie den Medientyp der Eingabedatei aus</td> 
  </tr>
  <tr> 
   <td role="rowheader">Avatar</td> 
   <td>Wählen Sie den Avatar aus, den Sie für das generierte Video verwenden möchten.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Medientyp</td> 
   <td>Auswahl des Ausgabemedientyps für das generierte Video.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Breite</td> 
   <td>Geben Sie die Breite für das generierte Video ein oder mappen Sie sie.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Höhe</td> 
   <td>Geben Sie die Höhe für das generierte Video ein oder mappen Sie sie.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Hintergrund</td> 
   <td>Wählen Sie den Hintergrundtyp aus, den Sie für das generierte Video verwenden möchten:
   <ul>
   <li><b>Video</b>: Geben Sie die URL des Hintergrundvideos ein oder mappen Sie sie.</li> 
   <li><b>Bild</b>: Geben Sie die URL des Hintergrundbilds ein oder mappen Sie sie.</li>
   <li><b>Farbe</b>: Geben Sie den Hexadezimalwert der Farbe ein, die Sie für den Videohintergrund verwenden möchten, oder mappen Sie ihn.</li> 
   </ul>
   </td>
  </tr>
 </tbody> 
</table>

#### Sprache aus Text generieren

Dieses Aktionsmodul generiert Sprache aus einem Transkript. Sie können entweder ein Nur-Text-Transkript oder eine vordefinierte URL bereitstellen. Die Antwort enthält eine Auftrags-ID und eine Status-URL zum Tracking des Auftrags.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Firefly finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Firefly</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Script</td> 
   <td>Wählen Sie den Skript-Typ aus, den Sie bereitstellen möchten.
   <ul>
   <li><b>Text</b>: Geben Sie den Quelltext in das Textfeld ein oder ordnen Sie ihn zu.</li>
   <li><b>Textdatei</b>: Geben Sie die URL der Textdatei in das URL-Feld ein oder mappen Sie sie.</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Gebietsschema-Code</td> 
   <td>Wählen Sie den Gebietsschema-Code aus, der für die Sprache steht, die Sie im Ergebnis verwenden möchten.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Medientyp</td> 
   <td>Das sollte <code>text/plain</code> werden.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Stimme</td> 
   <td>Wählen Sie die Stimme aus, die Sie verwenden möchten. Verfügbare Stimmen sind aus dem Adobe Firefly-Stimmkatalog.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Ausgabe</td> 
   <td>Das sollte <code>audio/wav</code> werden.</td> 
  </tr>
 </tbody> 
</table>

#### Video umgestalten

Dieses Modul erstellt ein neues Bild für die von Ihnen bereitgestellten Medien. Medien werden über eine vordefinierte URL bereitgestellt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Firefly finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Firefly</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vordefinierte URL</td> 
   <td>Geben Sie die vordefinierte URL ein, die das Modul für die Eingabe verwenden soll, oder ordnen Sie sie zu.<p>Die folgenden Domains für die Medienspeicherung werden von Firefly Audio and Video akzeptiert</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Erkennung von Szenen-Bearbeitungen</td> 
   <td>Wählen Sie aus, ob die Szenenediterkennung vor dem Umrahmen angewendet werden soll. </td> 
  </tr>
  <tr> 
   <td role="rowheader">Brennpunkt</td> 
   <td>Klicken Sie für jeden Fokus, den Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie oder die Keyword-Kennung für den Fokus ein.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Überlagerungen</td> 
   <td>Klicken Sie für jede Überlagerung, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Überlagerungsinformationen ein.
   <ul>
   <li><b>Source</b>: Geben Sie die URL ein, die auf die Quellmedien verweist, oder ordnen Sie sie zu.</li> 
   <li><b>Startzeit</b>: Geben Sie die Startzeit ein oder ordnen Sie sie zu.</li>
   <li><b>Dauer</b>: Geben Sie die Dauer der Überlagerung ein oder ordnen Sie sie zu.</li> 
   <li><b>Breite</b>: Geben Sie die Breite der skalierten Überlagerung ein oder ordnen Sie sie zu.</li> 
   <li><b>Höhe</b>: Geben Sie die Höhe der skalierten Überlagerung ein oder ordnen Sie sie zu.</li> 
   <li><b>Ankerpunkt</b>: Wählen Sie den Ankerpunkt für die Überlagerung aus.</li> 
   <li><b>Versatz X</b>: Geben Sie den horizontalen Versatz für die Überlagerung ein oder mappen Sie ihn.</li> 
   <li><b>Versatz Y</b>: Geben Sie den vertikalen Versatz für die Überlagerung ein oder mappen Sie ihn.</li> 
   <li><b>Wiederholen</b>: Geben Sie <code>loop</code> ein, um eine GIF-Schleife auszulösen.</li> 
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Medienformat</td> 
   <td>Wählen Sie das Format für das umgestaltete Video aus.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Seitenwagenformat</td> 
   <td>Format für zusätzliche Metadaten auswählen.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Ausgabedarstellungen</td> 
   <td>Um weitere Ausgabedarstellungen hinzuzufügen, klicken Sie auf <b>Element hinzufügen</b> und geben Sie die Ausgabedarstellungsinformationen ein.<!--add additional info--></td> 
  </tr>
 </tbody> 
</table>

#### Vorlage rendern

Dieses Modul rendert eine oder mehrere Videovarianten durch Anwenden von Überschreibungen und Exportvorgaben.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Firefly finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Firefly</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL der Eingabevorlagendatei</td> 
   <td>Geben Sie die vordefinierte URL für die Vorlage ein, die Sie rendern möchten, oder ordnen Sie sie zu.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Schriften</td> 
   <td>Klicken Sie für jede Schriftart, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den PostScript-Namen der Schriftart und die Schriftdatei-URL ein.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Wenn eine Schriftart fehlt</td> 
   <td>Wählen Sie aus, ob das Rendern fehlschlagen soll, oder verwenden Sie die Standardschriftart, wenn eine Schriftart fehlt.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Medien-Assets</td> 
   <td>Klicken Sie für jedes Medien-Asset, das Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die vordefinierte URL ein, die das Asset darstellt, oder ordnen Sie sie zu.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Vorgaben exportieren</td> 
   <td>Klicken Sie für jede Exportvorgabe, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und wählen Sie die Videovorgabe aus. Geben Sie dann die vordefinierte URL ein, die die Vorgabe darstellt, oder ordnen Sie sie zu.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Varianten</td> 
   <td>Klicken Sie für jede Variante, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie Details für die Variante ein. Sie müssen Details für mindestens eine Variante eingeben.<!--add data here--></td> 
  </tr>
  <tr> 
   <td role="rowheader">Ausgabedefinitionen</td> 
   <td>Definieren Sie die Ausgaben, indem Sie <b>Element hinzufügen</b> klicken, die hinzugefügten Varianten und Vorgaben auswählen, die Sie verwenden möchten, und einen Dateinamen hinzufügen. Varianten und Voreinstellungen werden mit 0 indiziert (das erste Element in der Variantenliste ist 0, das nächste ist 1 usw.).</td> 
  </tr>
 </tbody> 
</table>

#### Transkribieren von Medien

Dieses Modul transkribiert Audio oder Video.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu Adobe Firefly finden Sie unter <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Erstellen einer Verbindung zu Adobe Firefly</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Transkriptionstyp</td> 
   <td>Wählen Sie aus, ob Sie Audio oder Video transkribieren möchten.   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Vordefinierte URL</td> 
   <td>Geben Sie die vordefinierte URL ein, die das Modul für die Eingabe verwenden soll, oder ordnen Sie sie zu.   </td> 
  </tr>
  <tr> 
  </tr>
   <td role="rowheader">Medientyp </td> 
   <td>Wählen Sie den Medientyp der Eingabedatei aus</td> 
  </tr>
  <tr> 
   <td role="rowheader">Code des Zielgebietsschemas</td> 
   <td>Klicken Sie für jeden Gebietsschema-Code, den Sie hinzufügen möchten<b> auf „Element hinzufügen</b> und wählen Sie den Gebietsschema-Code aus, der die Sprache darstellt, die Sie im Ergebnis verwenden möchten.</td> 
  <tr> 
   <td role="rowheader">Beschriftungsformat</td> 
   <td>Geben Sie <code>SRT</code> ein, um Beschriftungen einzubeziehen, oder lassen Sie das Feld leer, wenn keine Beschriftungen gewünscht werden.</td> 
  </tr>
 </tbody> 
</table>



