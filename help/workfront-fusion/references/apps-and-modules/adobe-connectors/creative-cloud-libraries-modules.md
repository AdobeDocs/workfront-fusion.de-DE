---
title: Adobe Creative Cloud-Bibliotheksmodule
description: Mit den  [!DNL Adobe Workfront Fusion Adobe Creative Cloud] -Bibliotheksmodulen können Sie ein Szenario starten, wenn ein Element oder eine Bibliothek erstellt oder aktualisiert wird. Sie können Elemente auch hochladen, abrufen, archivieren oder auflisten oder die API  [!DNL Adobe Creative Cloud Libraries] .
author: Becky
feature: Workfront Fusion
exl-id: 85607e4e-538a-427f-8a99-a0ab65a75ac2
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1404'
ht-degree: 1%

---

# Adobe Creative Cloud-Bibliotheksmodule

Mit den Adobe Workfront Fusion [!DNL Adobe Creative Cloud Libraries]-Modulen können Sie ein Szenario starten, wenn ein Element oder eine Bibliothek erstellt oder aktualisiert wird. Sie können auch Elemente hochladen, abrufen, archivieren oder auflisten oder die [!DNL Adobe Creative Cloud Libraries]-API aufrufen.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

>[!IMPORTANT]
>
>Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.

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

Um [!DNL Adobe Creative Cloud Libraries]-Module verwenden zu können, müssen Sie über ein [!UICONTROL Adobe Creative Cloud]-Konto verfügen.

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

## [!UICONTROL Adobe Creative Cloud-], -Module und ihre Felder

Beim Konfigurieren von [!UICONTROL Adobe Creative Cloud Libraries]-Modulen zeigt Workfront Fusion die folgenden Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Adobe Creative Cloud Libraries] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Elementen](#elements)

* [Bibliotheken](#libraries)

* [Sonstiges](#other)


### Elementen

* [[!UICONTROL Element archivieren]](#archive-an-element)

* [[!UICONTROL Element abrufen]](#get-an-element)

* [[!UICONTROL Listenelemente]](#list-elements)

* [[!UICONTROL Element hochladen]](#upload-an-element)

* [!UICONTROL [Neues Element in Bibliothek ansehen]](#watch-new-element-in-library)

* [[!UICONTROL Aktualisierte Elemente ansehen]](#watch-updated-elements)


#### [!UICONTROL Element archivieren]

Dieses Aktionsmodul archiviert ein Element aus einer Bibliothek.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Bibliotheks-ID]</td>
      <td >Wählen Sie die Bibliothek aus, die das zu archivierende Element enthält, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Element-ID]</td>
      <td>Wählen Sie das Element aus, das Sie archivieren möchten, oder ordnen Sie es zu.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Element abrufen]

Dieses Aktionsmodul gibt ein einzelnes Element aus einer Bibliothek zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Bibliotheks-ID]</td>
      <td>Wählen Sie die Bibliothek aus, die das abzurufende Element enthält, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Element-ID]</td>
      <td>Geben Sie die ID des Elements ein, das Sie abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL-Auswahl]</td>
      <td>
        <p>Wählen Sie den Typ der Informationen aus, die das Modul zurückgibt. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL Standard]</b>
            </p>
            <p>Basisdaten</p>
          </li>
          <li>
            <p><b>[!UICONTROL Details]</b>
            </p>
            <p>Alle verfügbaren Daten</p>
          </li>
          <li>
            <p><b>[!UICONTROL-Darstellungen]</b>
            </p>
            <p>Eine reduzierte Liste von Assets, die mit dem Bibliothekselement verknüpft sind</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Listenelemente]

Dieses Aktionsmodul ruft eine Liste von Elementen in einer Bibliothek ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Bibliotheks-ID]</td>
      <td >Wählen Sie die Bibliothek aus, aus der Sie Elemente auflisten möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Sortieren nach]</td>
      <td>Wählen Sie aus, ob die Ergebnisse nach Namen oder nach dem letzten Änderungsdatum des Elements sortiert werden sollen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Typ]</td>
      <td >Geben Sie einen MIME-Typ ein oder ordnen Sie ihn zu, um die Ergebnisse auf Elemente zu beschränken, die mit dem angegebenen MIME-Typ identifiziert werden. Beispiel: <code>string</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL-Auswahl]</td>
      <td>
        <p>Wählen Sie den Typ der Informationen aus, die das Modul zurückgibt. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL Standard]</b>
            </p>
            <p>Basisdaten</p>
          </li>
          <li>
            <p><b>[!UICONTROL Details]</b>
            </p>
            <p>Alle verfügbaren Daten</p>
          </li>
          <li>
            <p><b>[!UICONTROL-Darstellungen]</b>
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

#### [!UICONTROL Neues Element in Bibliothek ansehen]

Dieses Trigger-Modul startet ein Szenario, wenn ein Element zu einer Bibliothek hinzugefügt wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Bibliotheks-ID]</td>
      <td >Wählen Sie die Bibliothek aus, die Sie auf aktualisierte Elemente überwachen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL Aktualisierte Elemente ansehen]

Dieses Trigger-Modul startet ein Szenario, wenn ein Element in einer Bibliothek aktualisiert wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Bibliotheks-ID]</td>
      <td >Wählen Sie die Bibliothek aus, die Sie auf neue Elemente überwachen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>

### Bibliotheken

* [[!UICONTROL Neue Bibliotheken ansehen]](#watch-new-libraries)

* [[!UICONTROL Aktualisierte Bibliotheken ansehen]](#watch-updated-libraries)


#### [!UICONTROL Neue Bibliotheken ansehen]

Dieses Bibliotheksmodul startet ein Trigger, wenn eine neue Bibliothek erstellt wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Aktualisierte Bibliotheken ansehen]

Dieses Bibliotheksmodul startet ein Trigger, wenn eine vorhandene Bibliothek aktualisiert wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
    </tr>
  </tbody>
</table>

### Sonstiges

* [Durchführen eines API-Aufrufs](#make-an-api-call)
* [Asset hochladen](#upload-an-asset)

#### [!UICONTROL Erstellen eines API-Aufrufs]

Dieses Modul führt einen benutzerdefinierten API-Aufruf an die [!DNL Adobe Creative Cloud Libraries]-API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td> <p>Anweisungen zum Verbinden Ihres Adobe Creative Cloud-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen.</a></p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://cc-libraries.adobe.io/api</code> ein.</p>
    <p>Beispiel <code>/v1/libraries</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL API-Version]</td>
      <td>
        <p>Wählen Sie die Version der [!DNL Adobe Analytics]-API aus, mit der Sie eine Verbindung herstellen möchten.</p>
      </td>
    </tr>    <tr>
      <td role="rowheader">[!UICONTROL-Methode]</td>
      <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL-Kopfzeilen]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td>
      <td>
        <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"name":"something-urgent"}</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL body]</td>
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
       <tr>
      <td role="rowheader">[!UICONTROL Vorübergehendes Dokument hochladen]</td>
      <td>
      <p>Wenn Sie ein vorübergehendes Dokument hochladen möchten, geben Sie die Quelldatei für das Dokument ein, das Sie hochladen möchten.</p>
      <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p>
    </td>
    </tr>
</tbody>
</table>


#### [!UICONTROL Asset hochladen]

Dieses Aktionsmodul lädt ein kleines Datei-Asset in eine vorhandene Bibliothek hoch. Die maximale Dateigröße beträgt 1 GB.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Eine bestehende Creative Cloud Libraries-Verbindung auswählen. Die Verbindungserstellung ist derzeit nicht im Creative Cloud Libraries-Connector verfügbar. Vorhandene Verbindungen funktionieren erwartungsgemäß.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Bibliotheks-ID]</td>
      <td >Wählen Sie die Bibliothek aus, in die Sie ein Asset hochladen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Aufrufmodus]</td>
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
      <td role="rowheader">[!UICONTROL Elementtyp]</td>
      <td >Wählen Sie den Typ des Elements aus, das Sie hochladen möchten</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dateityp]</td>
      <td >Geben Sie den MIME-Typ der hochgeladenen Datei ein oder ordnen Sie ihn zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Source-Datei]</td>
      <td>
        <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p>
      </td>
    </tr>
  </tbody>
</table>





