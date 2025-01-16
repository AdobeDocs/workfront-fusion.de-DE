---
title: Adobe Creative Cloud-Bibliotheksmodule
description: Mit den  [!DNL Adobe Workfront Fusion Adobe Creative Cloud] -Bibliotheksmodulen können Sie ein Szenario starten, wenn ein Element oder eine Bibliothek erstellt oder aktualisiert wird. Sie können Elemente auch hochladen, abrufen, archivieren oder auflisten oder die API  [!DNL Adobe Creative Cloud Libraries] .
author: Becky
feature: Workfront Fusion
exl-id: 85607e4e-538a-427f-8a99-a0ab65a75ac2
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 0%

---

# Adobe Creative Cloud-Bibliotheksmodule

Mit den [!DNL Adobe Workfront Fusion] [!DNL Adobe Creative Cloud Libraries] können Sie ein Szenario starten, wenn ein Element oder eine Bibliothek erstellt oder aktualisiert wird. Sie können auch Elemente hochladen, abrufen, archivieren oder auflisten oder die [!DNL Adobe Creative Cloud Libraries]-API aufrufen.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

>[!IMPORTANT]
>
>Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.

## Zugriffsanforderungen

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
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td>
      <td>
   <p>Aktuelle Lizenzanforderung: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung und -integration] </p>
   </td>
    </tr>
    <tr>
      <td role="rowheader">Produkt</td>
      <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den [!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Adobe Workfront] verfügen, muss Ihr Unternehmen [!DNL Adobe Workfront Fusion] kaufen und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden. [!DNL Workfront Fusion] ist im [!UICONTROL Ultimate] [!DNL Workfront] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden.</p>
   </td>
    </tr>
  </tbody>
</table>


Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Voraussetzungen

Um [!DNL Adobe Creative Cloud Libraries] Module verwenden zu können, müssen Sie über ein [!UICONTROL Adobe Creative Cloud]-Konto verfügen.

## Informationen zur Adobe Creative Cloud Libraries-API

Der Adobe Creative Cloud Libraries-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://cc-libraries.adobe.io/api/v1</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.1.7</td> 
  </tr>
 </tbody> 
 </table>

## [!UICONTROL Adobe Creative Cloud Libraries] Module und ihre Felder

Beim Konfigurieren [!UICONTROL Adobe Creative Cloud Libraries] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Adobe Creative Cloud Libraries] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Elemente](#elements)

* [Bibliotheken](#libraries)

* [Sonstige](#other)


### Elemente

* [[!UICONTROL Archive an Element]](#archive-an-element)

* [[!UICONTROL Get an Element]](#get-an-element)

* [[!UICONTROL List Elements]](#list-elements)

* [[!UICONTROL Upload an Element]](#upload-an-element)

* [!UICONTROL [Neues Element in Bibliothek ansehen]](#watch-new-element-in-library)

* [[!UICONTROL Watch Updated Elements]](#watch-updated-elements)


#### [!UICONTROL Archive an Element]

Dieses Aktionsmodul archiviert ein Element aus einer Bibliothek.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Wählen Sie die Bibliothek aus, die das zu archivierende Element enthält.</td>
    </tr>
    <tr>
      <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-LightGray" role="rowheader">[!UICONTROL Element ID]</td>
      <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-LightGray">Wählen Sie das Element aus, das Sie archivieren möchten.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an Element]

Dieses Aktionsmodul gibt ein einzelnes Element aus einer Bibliothek zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Wählen Sie die Bibliothek aus, die das abzurufende Element enthält.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Element ID]</td>
      <td>Geben Sie die ID des Elements ein, das Sie abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selector]</td>
      <td>
        <p>Wählen Sie den Typ der Informationen aus, die das Modul zurückgibt. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL Default]</b>
            </p>
            <p>Basisdaten</p>
          </li>
          <li>
            <p><b>[!UICONTROL Details]</b>
            </p>
            <p>Alle verfügbaren Daten</p>
          </li>
          <li>
            <p><b>[!UICONTROL Representations]</b>
            </p>
            <p>Eine reduzierte Liste von Assets, die mit dem Bibliothekselement verknüpft sind</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Elements]

Dieses Aktionsmodul ruft eine Liste von Elementen in einer Bibliothek ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Wählen Sie die Bibliothek aus, aus der Sie Elemente auflisten möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Order by]</td>
      <td>Wählen Sie aus, ob die Ergebnisse nach Namen oder nach dem letzten Änderungsdatum des Elements sortiert werden sollen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Type]</td>
      <td >Geben Sie einen MIME-Typ ein, um die Ergebnisse auf Elemente zu beschränken, die mit dem angegebenen MIME-Typ identifiziert werden. Beispiel: <code>string</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selector]</td>
      <td>
        <p>Wählen Sie den Typ der Informationen aus, die das Modul zurückgibt. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL Default]</b>
            </p>
            <p>Basisdaten</p>
          </li>
          <li>
            <p><b>[!UICONTROL Details]</b>
            </p>
            <p>Alle verfügbaren Daten</p>
          </li>
          <li>
            <p><b>[!UICONTROL Representations]</b>
            </p>
            <p>Eine reduzierte Liste von Assets, die mit dem Bibliothekselement verknüpft sind</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Upload an Element]

Dieses Aktionsmodul lädt ein kleines Datei-Asset in eine vorhandene Bibliothek hoch. Die maximale Dateigröße beträgt 1 GB.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Wählen Sie die Bibliothek aus, aus der Sie Elemente auflisten möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Invocation Mode]</td>
      <td>
        <p>Wählen Sie den Verarbeitungsmodus aus, mit dem dieser Anforderungsprozess aufgerufen werden soll.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL sync]</b>
            </p>
            <p>Der API-Aufruf wird synchron verarbeitet. Die Antwort wird bereitgestellt, wenn die Verarbeitung abgeschlossen ist (es sei denn, der Aufruf überschreitet das Zeitlimit.)</p>
          </li>
          <li>
            <p><b>[!UICONTROL async]</b>
            </p>
            <p>Die Antwort des asynchronen Monitors wird sofort zurückgegeben, und die Anforderungsverarbeitung erfolgt asynchron. Der aufrufende Benutzer ist dafür verantwortlich, den Endpunkt bis zum Abschluss abzufragen.</p>
          </li>
          <li>
            <p><b>[!UICONTROL sync,async]</b> (Standard)</p>
            <p>Es wird versucht, die Anfrage synchron zu verarbeiten. Wenn die Verarbeitung mehr als 5000 ms dauert, wird die Antwort des asynchronen Monitors zurückgegeben. Die Monitor-URL sollte abgefragt werden, bis die Anfrage abgeschlossen ist.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Type File]</td>
      <td >Geben Sie den MIME-Typ der hochgeladenen Datei ein oder ordnen Sie ihn zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Source File]</td>
      <td>
        <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Watch New Element in Library]

Dieses Trigger-Modul startet ein Szenario, wenn ein Element zu einer Bibliothek hinzugefügt wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Wählen Sie die Bibliothek aus, die Sie auf aktualisierte Elemente überwachen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL Watch Updated Elements]

Dieses Trigger-Modul startet ein Szenario, wenn ein Element in einer Bibliothek aktualisiert wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Library ID]</td>
      <td >Wählen Sie die Bibliothek aus, die Sie auf neue Elemente überwachen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>

### Bibliotheken

* [[!UICONTROL Watch New Libraries]](#watch-new-libraries)

* [[!UICONTROL Watch Updated Libraries]](#watch-updated-libraries)


#### [!UICONTROL Watch New Libraries]

Dieses Bibliotheksmodul startet ein Trigger, wenn eine neue Bibliothek erstellt wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Watch Updated Libraries]

Dieses Bibliotheksmodul startet ein Trigger, wenn eine vorhandene Bibliothek aktualisiert wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>

### Sonstige

#### [!UICONTROL Make an API Call]

Dieses Modul führt einen benutzerdefinierten API-Aufruf an die [!DNL Adobe Creative Cloud Libraries]-API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Anweisungen zum Verbinden Ihres Adobe Creative Cloud-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen.</a></p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://cc-libraries.adobe.io/api</code> ein.</p>
    <p>Beispiel: <code>/v1/libraries</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL API version]</td>
      <td>
        <p>Wählen Sie die Version der [!DNL Adobe Analytics]-API aus, mit der Sie eine Verbindung herstellen möchten.</p>
      </td>
    </tr>    <tr>
      <td role="rowheader">[!UICONTROL Method]</td>
      <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p>
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
       <tr>
      <td role="rowheader">[!UICONTROL Upload a transient document]</td>
      <td>
      <p>Wenn Sie ein vorübergehendes Dokument hochladen möchten, geben Sie die Quelldatei für das Dokument ein, das Sie hochladen möchten.</p>
      <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p>
    </td>
    </tr>

</tbody>
</table>
