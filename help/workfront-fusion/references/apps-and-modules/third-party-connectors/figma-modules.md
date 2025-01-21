---
title: Figma-Module
description: Mit den  [!DNL Adobe Workfront Fusion] -Figma-Modulen können Sie Listen von Kommentaren, Dateien, Dateiversionen oder Projekten abrufen. Sie können auch einen Kommentar posten oder einen Aufruf an die Figma-API durchführen.
author: Becky
feature: Workfront Fusion
exl-id: 1220460b-1957-4dfc-b7c1-4c97b36ea061
source-git-commit: 200907bb8d80f874227493b489ef1ea450198dc6
workflow-type: tm+mt
source-wordcount: '2247'
ht-degree: 0%

---

# [!DNL Figma] Module

Mit den [!DNL Adobe Workfront Fusion] [!DNL Figma] können Sie Listen von Kommentaren, Dateien, Dateiversionen oder Projekten abrufen. Sie können auch einen Kommentar posten oder einen Aufruf an die [!DNL Figma]-API durchführen.

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um [!DNL Figma]-Module verwenden zu können, müssen Sie über ein [!DNL Figma]-Konto verfügen.

## Figma API-Informationen

Der Figma-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.figma.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.8.25</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung zu Figma

So erstellen Sie eine Verbindung für Ihre Figma-Module:

1. Klicken Sie in einem beliebigen Figma-Modul **[!UICONTROL Add]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p> Wählen Sie für neue Verbindungen <code>Figma</code> ohne das Legacy-Tag aus. </p><p>Die Figma änderte im Januar 2025 ihre Authentifizierungspflichten. Der <code>Figma</code> Verbindungstyp erfüllt die neuen Anforderungen. Der <code>Figma (Legacy)</code> Verbindungstyp wird in Zukunft entfernt.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Geben Sie Ihre [!UICONTROL Figme] [!UICONTROL Client ID] ein.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Geben Sie Ihre Figma-[!UICONTROL Client Secret] ein.</td>
        </tr>
        <tr>
        <td role="rowheader">Benutzerdefinierte Bereiche</td>
        <td>Geben Sie alle benutzerdefinierten Bereiche ein, die für diese Verbindung erforderlich sind.</td>
        </tr>
        <tr>
        <td role="rowheader">URL für die Überprüfung benutzerdefinierter Verbindungen</td>
        <td>Der Standardendpunkt zum Überprüfen, ob die Verbindung erfolgreich erstellt wurde, ist: <code>https://api.figma.com/v1/me</code> Wenn diese URL für den benutzerdefinierten Bereich nicht unterstützt wird, geben Sie eine benutzerdefinierte Überprüfungs-URL an.</td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu speichern und zum Modul zurückzukehren.



## [!DNL Figma] Module und ihre Felder

Beim Konfigurieren [!DNL Figma] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Figma] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Kommentare](#comments)

* [Projekte und Dateien](#projects-and-files)

* [Komponenten und Stile](#components-and-styles)

* [Sonstige](#other)


### Kommentare

* [Kommentar löschen](#delete-a-comment)

* [Kommentare auflisten](#list-comments)

* [Kommentar posten](#post-a-comment)


#### [!UICONTROL Delete a comment]

Dieses Aktionsmodul löscht einen einzelnen Kommentar aus einer Datei.

<table style="table-layout:auto"> 
  <col/>
  <col />
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Anweisungen zum Verbinden Ihres [!DNL Figma]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Figma</a> in diesem Artikel.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>Geben Sie die Datei-ID der Datei ein, zu der Sie einen Kommentar hinzufügen möchten, oder mappen Sie sie. </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Comment ID]</td>
      <td>Geben Sie den Text des Kommentars ein, den Sie löschen möchten.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List comments]

Dieses Suchmodul listet alle Kommentare auf, die an eine einzelne Datei in [!DNL Figma] angehängt sind.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Anweisungen zum Verbinden Ihres [!DNL Figma]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Figma</a> in diesem Artikel.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>Geben Sie die Datei-ID der Datei ein, für die Sie Kommentare abrufen möchten, oder mappen Sie sie. </p>
        <ul>
          <li>
            <p>Wenn Sie die ID nicht kennen, klicken Sie auf <b>[!UICONTROL Find Files]</b> und geben Sie die ID des Projekts, mit dem die Datei verknüpft ist, ein oder ordnen Sie sie zu. Wählen Sie dann die Datei aus.</p>
          </li>
          <li>
            <p>Wenn Sie die Projekt-ID nicht kennen, klicken Sie auf <b>[!UICONTROL Find Projects]</b> und geben Sie die ID des Teams ein, dem das Projekt gehört, dem die Datei zugeordnet ist, oder ordnen Sie sie zu. Wählen Sie dann das Projekt aus und wählen Sie die Datei aus.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td>
      <td>Geben Sie die maximale Anzahl von Kommentaren ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL Post a comment]

Dieses Aktionsmodul postet einen Kommentar in eine Figma-Datei.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Anweisungen zum Verbinden Ihres [!DNL Figma]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Figma</a> in diesem Artikel.</p>
    </tr>
    <tr>
      <td  role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>Geben Sie die Datei-ID der Datei ein, an die Sie einen Kommentar senden möchten, oder mappen Sie sie. </p>
        <ul>
          <li>
            <p>Wenn Sie die Datei-ID nicht kennen, klicken Sie auf <b>[!UICONTROL Find Files]</b> und geben Sie die ID des Projekts, mit dem die Datei verknüpft ist, ein oder ordnen Sie sie zu. Wählen Sie dann die Datei aus.</p>
          </li>
          <li>
            <p>Wenn Sie versuchen, die Datei-ID zu finden und die Projekt-ID nicht kennen, klicken Sie auf <b>[!UICONTROL Find Projects]</b> und geben Sie die ID des Teams ein, dem das Projekt gehört, dem die Datei zugeordnet ist, oder mappen Sie sie. Wählen Sie das Projekt und dann die Datei aus.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Comment]</td>
      <td>Geben Sie den Text des Kommentars ein.</td>
    </tr>
  </tbody>
</table>


### Projekte und Dateien

* [Datei oder Bild abrufen](#get-a-file-or-image)

* [Dateiversionsverlauf auflisten](#list-file-version-history)

* [Projektdateien auflisten](#list-project-files)

* [Auflisten von Projekten](#list-projects)


#### [!UICONTROL Get a file or image]

Dieses Aktionsmodul ruft eine einzelne Datei oder ein einzelnes Bild aus einer Figmabibliothek ab

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Anweisungen zum Verbinden Ihres [!DNL Figma]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Figma</a> in diesem Artikel.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>
        <p>Wählen Sie den Typ des Objekts aus, das Sie abrufen möchten.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL File]</b>
            </p>
            <p>Das -Modul gibt das Dokument zurück, auf das von [!UICONTROL Key] als JSON-Objekt verwiesen wird. Der Dateischlüssel kann aus einer beliebigen Figmadatei-URL geparst werden.</p>
            <p>Felder finden Sie unter <a href="#get-a-file-or-image-file" class="MCXref xref" >[!UICONTROL Get a file or image: File]</a>.</p>
          </li>
          <li>
            <p><b>[!UICONTROL File nodes]</b>
            </p>
            <p>Gibt die Knoten zurück, auf die von IDs als JSON-Objekt verwiesen wird. Die Knoten werden aus der [!DNL Figma] abgerufen, auf die von [!UICONTROL Key] verwiesen wird.</p>
            <p>Felder finden Sie unter <a href="#get-a-file-or-image-file-nodes" class="MCXref xref" >[!UICONTROL Get a file or image: File nodes]</a>.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Image]</b>
            </p>
            <p>Das Modul rendert Bilder aus einer -Datei.</p>
            <p>Felder finden Sie unter <a href="#get-a-file-or-image-image" class="MCXref xref" >[!UICONTROL Get a file or image: Image]</a>.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Image fills]</b>
            </p>
            <p>Das Modul gibt Download-Links für alle Bilder zurück, die in Bildausfüllungen in einem Dokument vorhanden sind. Bildfüllungen sind die Darstellungen [!DNL Figma] vom Benutzer bereitgestellten Bilder. Wenn Sie ein Bild in [!DNL Figma] ziehen, erstellt [!DNL Figma] ein Rechteck mit einer einzigen Füllung, die das Bild darstellt, und die Benutzenden können das Rechteck (und die Eigenschaften der Füllung) transformieren.</p>
            <p>Felder finden Sie unter <a href="#get-a-file-or-image-image-fills" class="MCXref xref" >[!UICONTROL Get a file or image: Image fills]</a>.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>


##### Datei oder Bild abrufen: Datei

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>Wählen Sie die Datei aus, aus der Sie JSON zurückgeben möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Version ID]</td>
      <td>Geben Sie die Version der Datei ein, die das Modul zurückgeben soll, oder ordnen Sie sie zu. Lassen Sie dieses Feld für das aktuelle Modul leer.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Node IDs]</td>
      <td>
        <p>Um nur eine Teilmenge des Dokuments zurückzugeben, geben Sie die Knoten ein, die das Modul zurückgeben soll. Das -Modul gibt die aufgelisteten Knoten, ihre untergeordneten Elemente und alles zurück, was sich zwischen dem Stammknoten und den aufgelisteten Knoten befindet.</p>
        <p>Klicken Sie für jeden Knoten, den Sie zurückgeben möchten, auf <b>[!UICONTROL Add]</b> und geben Sie den Text des Knotens ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Depth]</td>
      <td>
        <p>Geben Sie eine Ganzzahl ein, die darstellt, wie tief in der Dokumentstruktur Sie Ergebnisse zurückgeben möchten, oder ordnen Sie sie zu. </p>
        <div class="example"><span class="autonumber"><span><b>Beispiel: </b></span></span>
          <ul>
            <li>
              <p>Um nur Seiten zurückzugeben, geben Sie <code>1</code> ein.</p>
            </li>
            <li>
              <p>Um Seiten und Objekte der obersten Ebene zurückzugeben, geben Sie <code>2</code> ein.</p>
            </li>
          </ul>
        </div>
        <p>Um alle Knoten zurückzugeben, lassen Sie dieses Feld leer.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Geometry]</td>
      <td>Um Vektordaten zurückzugeben, geben Sie <code>paths</code> ein.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Plugin data]</td>
      <td>Eine kommagetrennte Liste von Plug-in-IDs und/oder die Zeichenfolge "[!UICONTROL shared]". Alle Daten, die im Dokument vorhanden sind, das von diesen Plug-ins geschrieben wurde, werden in das Ergebnis in den <code>pluginData</code>- und <code>sharedPluginData</code>-Eigenschaften aufgenommen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Branch data]</td>
      <td>Aktivieren Sie diese Option, um Metadaten der Verzweigung für die angeforderte Datei zurückzugeben. Wenn es sich bei der Datei um eine Verzweigung handelt, wird der Schlüssel der Hauptdatei in die zurückgegebene Antwort aufgenommen. Wenn die Datei Verzweigungen hat, werden deren Metadaten in die zurückgegebene Antwort aufgenommen. Standard: <code>false</code>.</td>
    </tr>
  </tbody>
</table>

##### Datei oder Bild abrufen: Dateiknoten

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>Wählen Sie die Datei aus, aus der Sie JSON zurückgeben möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Node IDs]</td>
      <td>
        <p>Geben Sie die Knoten ein, die das Modul zurückgeben und konvertieren soll</p>
        <p>Klicken Sie für jeden Knoten, den Sie zurückgeben möchten, auf <b>[!UICONTROL Add]</b> und geben Sie den Text des Knotens ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Version ID]</td>
      <td>Geben Sie die Version der Datei ein, die das Modul zurückgeben soll, oder ordnen Sie sie zu. Lassen Sie dieses Feld für das aktuelle Modul leer.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Depth]</td>
      <td>
        <p>Geben Sie eine Ganzzahl ein, die darstellt, wie tief in der Dokumentstruktur Sie Ergebnisse zurückgeben möchten, oder ordnen Sie sie zu. </p>
        <div class="example"><span class="autonumber"><span><b>Beispiel: </b></span></span>
          <ul>
            <li>
              <p>Um nur Seiten zurückzugeben, geben Sie <code>1</code> ein.</p>
            </li>
            <li>
              <p>Um Seiten und Objekte der obersten Ebene zurückzugeben, geben Sie <code>2</code> ein.</p>
            </li>
          </ul>
        </div>
        <p>Um alle Knoten zurückzugeben, lassen Sie dieses Feld leer.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Geometry]</td>
      <td>Um Vektordaten zurückzugeben, geben Sie <code>paths</code> ein.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Plugin data]</td>
      <td>Eine kommagetrennte Liste von Plug-in-IDs und/oder die Zeichenfolge „shared“. Alle Daten, die im Dokument vorhanden sind, das von diesen Plug-ins geschrieben wurde, werden in das Ergebnis in den Eigenschaften pluginData und sharedPluginData aufgenommen.</td>
    </tr>
  </tbody>
</table>


##### Datei oder Bild abrufen: Bild

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>Wählen Sie die Datei aus, aus der Sie JSON zurückgeben möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Node IDs]</td>
      <td>
        <p>Geben Sie die Knoten ein, die das Modul rendern soll.</p>
        <p>Klicken Sie für jeden Knoten, den Sie rendern möchten, auf <b>[!UICONTROL Add]</b> und geben Sie den Text des Knotens ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Scale]</td>
      <td>Um das Bild zu skalieren, geben Sie den Skalierungsfaktor ein oder mappen Sie ihn. Diese Zahl muss zwischen 0,01 und 4 liegen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Format]</td>
      <td>
        <p>Wählen Sie das Format für die Bildausgabe aus.</p>
        <ul>
          <li>
            <p>JPG</p>
          </li>
          <li>
            <p>PNG</p>
          </li>
          <li>
            <p>SVG</p>
          </li>
          <li>
            <p>PDF</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SVG - Include ID]</td>
      <td>Aktivieren Sie diese Option, um ID-Attribute für alle SVG-Elemente einzuschließen. Standard: [!UICONTROL false].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SVG - Simplify Stroke]</td>
      <td>Aktivieren Sie diese Option, um innere/äußere Konturen zu vereinfachen und wenn möglich das Konturattribut anstelle von &lt;Maske&gt; zu verwenden. Standard: [!UICONTROL true].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Use absolute bounds]</td>
      <td>Aktivieren Sie diese Option, um die vollständigen Abmessungen des Knotens zu verwenden, unabhängig davon, ob er abgeschnitten wird oder ob der Raum um ihn herum leer ist. Hiermit können Sie Textknoten ohne Zuschnitt exportieren. Standard: [!UICONTROL false].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Version]</td>
      <td>Geben Sie die Version der Datei ein, die das Modul zurückgeben soll, oder ordnen Sie sie zu. Lassen Sie dieses Feld für das aktuelle Modul leer.</td>
    </tr>
  </tbody>
</table>

##### Datei oder Bild abrufen: Bilddateien

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>Wählen Sie die Datei aus, aus der Sie JSON zurückgeben möchten.</td>
    </tr>
  </tbody>
</table>

### [!UICONTROL List file version history]

Dieses Suchmodul gibt den Versionsverlauf einer einzelnen Datei in [!UICONTROL Figma] zurück.
<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Anweisungen zum Verbinden Ihres [!DNL Figma]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Figma</a> in diesem Artikel.</p>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>Geben Sie die Datei-ID der Datei ein, für die Sie den Versionsverlauf abrufen möchten, oder ordnen Sie sie zu. </p>
        <ul>
          <li>
            <p>Wenn Sie die Datei-ID nicht kennen, klicken Sie auf <b>[!UICONTROL Find Files]</b> und geben Sie die ID des Projekts, mit dem die Datei verknüpft ist, ein oder ordnen Sie sie zu. Wählen Sie dann die Datei aus.</p>
          </li>
          <li>
            <p>Wenn Sie versuchen, die Datei-ID zu finden und die Projekt-ID nicht kennen, klicken Sie auf <b>[!UICONTROL Find Projects]</b> und geben Sie die ID des Teams ein, dem das Projekt gehört, dem die Datei zugeordnet ist, oder mappen Sie sie. Wählen Sie das Projekt und dann die Datei aus.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned files]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List project files]

Dieses Suchmodul gibt eine Liste aller Dateien im angegebenen Projekt zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Anweisungen zum Verbinden Ihres [!DNL Figma]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Figma</a> in diesem Artikel.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>Geben Sie die Projekt-ID für das Projekt ein, für das Sie Dateien abrufen möchten, oder ordnen Sie sie zu. </p>
        <ul>
          <li>
            <p>Wenn Sie die Projekt-ID nicht kennen, klicken Sie auf <b>[!UICONTROL Find Projects]</b> und geben Sie die ID des Teams ein, dem das Projekt zugeordnet ist, oder ordnen Sie sie zu. Wählen Sie dann das Projekt aus.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned files]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List projects]

Dieses Suchmodul gibt eine Liste aller Projekte innerhalb des angegebenen Teams zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Anweisungen zum Verbinden Ihres [!DNL Figma]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Figma</a> in diesem Artikel.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Team ID]</td>
      <td>Geben Sie die Projekt-ID des Projekts ein, für das Sie Dateien abrufen möchten, oder ordnen Sie sie zu. Die Team-ID finden Sie in der URL der Team-Seite in Figma</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned projects]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>


### Komponenten und Stile

#### [!UICONTROL Get a style or component]

Dieses Aktionsmodul ruft einen einzelnen Stil, eine einzelne Komponente oder einen Satz von Stilen oder Komponenten ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Anweisungen zum Verbinden Ihres [!DNL Figma]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Figma</a> in diesem Artikel.</p>
    </tr>
    <tr>
      <td role="rowheader">Objekt&gt; Typ</td>
      <td>Wählen Sie den Typ des Objekts aus, das Sie abrufen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">&lt;[!UICONTROL Object> key]</td>
      <td>Geben Sie den Schlüssel (eindeutige Kennung) des Objekts ein, das Sie abrufen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Team ID]</td>
      <td>Beim Abrufen einer Team-Komponente oder eines Team-Komponentensatzes geben Sie die ID des Teams ein, mit dem der Datensatz oder die Datensätze verknüpft sind, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Page Size]</td>
      <td>Beim Abrufen einer Team-Komponente oder eines Team-Komponentensatzes geben Sie die Zahl oder die Ergebnisse ein, die pro Seite zurückgegeben werden sollen, oder ordnen Sie sie zu. Standardwert: 30.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL After]</td>
      <td>
        <p>Beim Abrufen einer Team-Komponente oder eines Team-Komponentensatzes geben Sie die Nummer des Ergebnisses ein, nach der das Abrufen der Ergebnisse beginnen soll, oder mappen Sie diese. Dies kann mit dem Feld [!UICONTROL Page Size] kombiniert werden, um Ergebnisse zu paginieren.</p>
        <p>Dieser Wert entspricht nicht den Objekt-IDs.</p>
        <p>Dieses Feld kann nicht in Kombination mit dem [!UICONTROL Before] Feld verwendet werden.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Before]</td>
      <td>
        <p>Beim Abrufen einer Team-Komponente oder eines Team-Komponentensatzes geben Sie die Nummer des Ergebnisses ein, vor der das Abrufen der Ergebnisse beginnen soll, oder mappen Sie sie. Dies kann mit dem Feld [!UICONTROL Page Size] kombiniert werden, um Ergebnisse zu paginieren.</p>
        <p>Dieser Wert entspricht nicht den Objekt-IDs.</p>
        <p>Dieses Feld kann nicht in Kombination mit dem [!UICONTROL After] Feld verwendet werden.</p>
      </td>
    </tr>
  </tbody>
</table>


### Sonstige

* [Durchführen eines API-Aufrufs](#make-an-api-call)

* [Ereignisse ansehen](#watch-events)


#### [!UICONTROL Make an API call]

Mit diesem Aktionsmodul können Sie die Figma-API benutzerdefiniert authentifiziert aufrufen, ohne die Authentifizierung durchdenken zu müssen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen Figma-Modulen nicht durchgeführt werden kann.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Anweisungen zum Verbinden Ihres [!DNL Figma]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Figma</a> in diesem Artikel.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://api.figma.com/v1/</code> ein.</p>
        <p>Beispiel: <code>[!DNL files/7179110/comments]</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Method]</td>
      <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Fügt die Autorisierungskopfzeilen für Sie hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]</td>
      <td>
        <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"name":"something-urgent"}</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### [!UICONTROL Watch events]

Dieses Teammodul startet ein Szenario, wenn eines der folgenden Trigger für ein bestimmtes Team in Ihrem [!DNL Figma] Teambereich eintritt:

* Dateiaktualisierung

* Dateiversionsaktualisierung

* Datei löschen

* Bibliothek veröffentlichen

* Dateikommentar

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>
        <p>Wählen Sie den Webhook aus, den das Modul überwacht.</p>
        <p>So fügen Sie einen neuen Webhook hinzu:</p>
        <ol>
          <li>
            <p>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL Webhook] .</p>
          </li>
          <li>
            <p>Geben Sie einen Namen für den Webhook ein.</p>
          </li>
          <li>
            <p>Wählen Sie die Verbindung aus, die Sie für diesen Webhook verwenden möchten. Anweisungen zum Verbinden Ihres [!DNL Figma]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen.</a></p>
          </li>
          <li>
            <p>Wählen Sie den Ereignistyp aus, den das Modul überwachen soll.</p>
          </li>
          <li>
            <p>Geben Sie die ID des Teams ein, dessen Ereignisse der Webhook überwachen soll.</p>
          </li>
          <li>
            <p>Wählen Sie aus, ob der Webhook aktiv oder angehalten sein soll.</p>
          </li>
          <li>
            <p>Geben Sie eine Beschreibung für den Webhook ein.</p>
          </li>
          <li>
            <p>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren.</p>
          </li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>
