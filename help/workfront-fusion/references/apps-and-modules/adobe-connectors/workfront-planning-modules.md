---
title: Adobe Workfront-Planungsmodule
description: Mit den  [!DNL Adobe Workfront Planning] -Modulen können Sie ein  [!DNL Adobe Workfront Fusion]  auf der Grundlage von Ereignissen in Ihrem  [!DNL Adobe] Workfront Planning-Konto starten, Vereinbarungen und andere Datensätze erstellen, lesen oder aktualisieren, nach Datensätzen anhand der von Ihnen festgelegten Kriterien suchen und Dokumente hochladen.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: 51bb87572f16f6194f6c37bbe52ea7f27050c303
workflow-type: tm+mt
source-wordcount: '1591'
ht-degree: 0%

---

# [!DNL Adobe Workfront Planning]

Mit den [!DNL Adobe Workfront Planning]-Modulen können Sie einen Trigger erstellen, wenn in Workfront Planning Ereignisse eintreten. Sie können auch Datensätze erstellen, lesen, aktualisieren und löschen oder einen benutzerdefinierten API-Aufruf an Ihr [!DNL Adobe Workfront Planning]-Konto durchführen.

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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Für den Zugriff auf Workfront Planning sind folgende Voraussetzungen erforderlich:

* Ein neues Workfront-Paket und eine neue Lizenz. Workfront Planning ist nicht für ältere Workfront-Pakete oder -Lizenzen verfügbar.
* Ein Workfront-Planungspaket.
* Die Workfront-Instanz Ihres Unternehmens muss in das einheitliche Adobe-Erlebnis integriert werden.

## Informationen zur Adobe Workfront Planning-API

Der Adobe Workfront Planning-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://{{connection.host}}/maestro/api/{{common.maestroApiVersion}}/</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] {#create-a-connection-to-adobe-workfront-planning}

Sie können direkt aus einem [!DNL Workfront Fusion]-Modul heraus eine Verbindung zu Ihrem [!DNL Workfront Planning]-Konto herstellen.

1. Klicken Sie in einem beliebigen [!DNL Adobe Workfront Planning] auf **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

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
          <td role="rowheader">[!UICONTROL Client-ID]<p>(Optional)</p></td>
          <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL Client ID] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-Geheimnis]<p>(Optional)</p></td>
          <td>Geben Sie Ihren [!DNL Adobe] [!UICONTROL Client Secret] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL-Authentifizierungs-URL]</td>
          <td>Geben Sie die URL ein, die Ihre Workfront-Instanz zur Authentifizierung dieser Verbindung verwenden soll. <p>Der Standardwert ist <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host-Präfix]</td>
          <td>Geben Sie Ihr Host-Präfix ein.<p>Der Standardwert ist <code>origin-</code>.</p>
        </tr>
      </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## [!DNL Adobe Workfront Planning] Module und ihre Felder

Beim Konfigurieren von Workfront-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service können zusätzlich dazu weitere Workfront-Felder angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)
* [Nicht kategorisiert](#uncategorized)

### Auslöser

#### Ereignisse ansehen

Dieses Trigger-Modul startet ein Szenario, wenn ein Datensatz, ein Datensatztyp oder ein Arbeitsbereich in Workfront Planning erstellt, aktualisiert oder gelöscht wird.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Wählen Sie den Webhook aus, den Sie verwenden möchten, oder klicken Sie auf Hinzufügen , um einen neuen zu erstellen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] finden Sie unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objekttyp]</td>
      <td>Wählen Sie aus, ob Datensätze, Datensatztypen oder Arbeitsbereiche überwacht werden sollen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL-Status]</td>
      <td>Wählen Sie aus, ob der alte oder der neue Status überwacht werden soll.<ul><li><p><b>[!UICONTROL Neuer Status]</b></p><p>Trigger : Ein Szenario, in dem sich der Datensatz <b> einem </b> Wert ändert.</p></li><li><p><b>[!UICONTROL Alter Status]</b></p><p>Trigger : Ein Szenario, in dem sich der Datensatz <b> einem </b> Wert ändert.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Wenn Sie Datensätze beobachten, wählen Sie die Workspace aus, die Sie auf Datensätze überwachen möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datensatztyp]</td>
      <td>Wählen Sie beim Überwachen von Datensätzen den Typ des Datensatzes aus, auf den Sie achten möchten.</td>
    </tr>
    </tr>
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Ereignisfilter]</p> </td> 
      <td> <p>Sie können Filter festlegen, um nur nach Datensätzen zu suchen, die die von Ihnen ausgewählten Kriterien erfüllen.</p> <p>Geben Sie für jeden Filter das Feld ein, das vom Filter ausgewertet werden soll, den Operator und den Wert, den der Filter zulassen soll. Sie können mehr als einen Filter verwenden, indem Sie AND-Regeln hinzufügen.</p> <p>Hinweis: Filter in vorhandenen [!DNL Workfront]-Webhooks können nicht bearbeitet werden. Um verschiedene Filter für [!DNL Workfront] Ereignisabonnements einzurichten, entfernen Sie den aktuellen Webhook und erstellen Sie einen neuen.</p> <p>Weitere Informationen zu Ereignisfiltern finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Ereignisabonnementfilter in den Modulen [!DNL Workfront] &gt; [!UICONTROL Ereignisse beobachten</a> im Artikel Workfront-Module .</p> </td> 
     </tr> 
    <tr>
      <td role="rowheader">[!UICONTROL zu überwachende Objekte]</td>
      <td>Wählen Sie aus, ob Sie auf neue Nachrichten achten möchten. Aktualisierte, neue und aktualisierte oder gelöschte Datensätze.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Von dieser Verbindung vorgenommene Aktualisierungen ausschließen]</p>
      </td>
      <td>Aktivieren Sie diese Option, um zu verhindern, dass das Szenario ausgelöst wird, wenn eine Änderung durch die von diesem Modul verwendete Verbindung vorgenommen wird. Dadurch wird verhindert, dass eine weitere Instanz des Szenarios ausgelöst wird, wenn dieses Szenario eine auslösende Aktion ausführt.</td> 
      </tr>
  </tbody>
</table>

### Aktionen

* [Datensatztyp löschen](#delete-a-record-type)
* [Erstellen eines benutzerdefinierten KI-Aufrufs](#make-a-custom-api-call)

#### Datensatztyp löschen

Dieses Aktionsmodul löscht einen einzelnen Datensatztyp in Workfront Planning anhand seiner ID.

>[!WARNING]
>
>Durch das Löschen eines Datensatztyps in Workfront Planning werden auch alle Datensätze in der Datensatztyptabelle gelöscht.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] finden Sie unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning]</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatztyp-ID]</p>
      </td>
      <td>Geben Sie die ID des Datensatztyps ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
  </tbody>
</table>

#### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Modul führt einen benutzerdefinierten API-Aufruf an die [!DNL Adobe Workfront Planning]-API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] finden Sie unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning]</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Pfad eingeben für <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
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
        <p>Klicken Sie für jedes Schlüssel/Wert-Paar, das Sie der Abfragezeichenfolge hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Schlüssel und den Wert ein.</p>
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


### Suchvorgänge

#### Datensätze suchen

Dieses Aktionsmodul ruft eine Liste von Datensätzen basierend auf von Ihnen angegebenen Kriterien ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] finden Sie unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning]</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>Geben Sie die Workspace ein, die die zu durchsuchenden Datensätze enthält, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatztyp]</p>
      </td>
      <td>Wählen Sie den Datensatztyp aus, den Sie suchen möchten.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatzfelder]</p>
      </td>
      <td>Suchen Sie für jedes Feld, das Sie bei der Suche verwenden möchten, dieses Feld, wählen Sie den Operator aus und geben Sie den Wert ein, nach dem Sie suchen möchten, oder mappen Sie ihn. Felder sind je nach ausgewähltem Datensatztyp verfügbar.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL-Bedingung für Filter]</p>
      </td>
      <td>Bedingung für die Filter auswählen:<ul><li><b>UND</b><p>Das Modul gibt Datensätze zurück, <b> (alle</b> der von Ihnen ausgewählten Feldwerte erfüllen.</p></li><li><b>ODER</b><p>Das Modul gibt Datensätze zurück, <b> (beliebige</b> der ausgewählten Feldwerte erfüllen.</p></li></ul></td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Limit]</p>
      </td>
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
      </tr>
  </tbody>
</table>


### Nicht kategorisiert


#### Erstellen eines Datensatzes

Diese Aktion erstellt in Workfront Planning einen einzigen Datensatz.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] finden Sie unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning]</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatztyp-ID]</p>
      </td>
      <td>Geben Sie den Typ des Datensatzes ein, den Sie erstellen möchten, oder ordnen Sie ihn zu. Die verfügbaren Datensatztypen basieren auf Ihrem Workfront Planning-Konto.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Andere Felder</p>
      </td>
      <td>Geben Sie die Werte ein, die der neue Datensatz haben soll. Diese Felder basieren auf dem von Ihnen ausgewählten Datensatztyp.</td> 
      </tr>
     <tr>
  </tbody>
</table>

### Löschen eines Datensatzes

Dieses Aktionsmodul löscht den angegebenen Datensatz in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] finden Sie unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning]</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatz-ID]</p>
      </td>
      <td>Geben Sie die ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

### Datensatz abrufen

Dieses Aktionsmodul ruft einen einzelnen Datensatz aus [!DNL Adobe Workfront Planning] ab, angegeben durch die Kennung.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] finden Sie unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datensatz-ID]</td>
      <td>Geben Sie die ID des Datensatzes ein, den Sie abrufen möchten, oder ordnen Sie sie zu.</td>
    </tr>
  </tbody>
</table>

### Datensätze nach Datensatztyp abrufen

Dieses Aktionsmodul ruft alle Datensätze des angegebenen Typs ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] finden Sie unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Wählen Sie den Arbeitsbereich aus, der die abzurufenden Datensätze enthält, oder ordnen Sie ihn zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datensatztyp]</td>
      <td>Wählen Sie den Typ des Datensatzes aus, den Sie abrufen möchten.</td>
    </tr>
     <!--<tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> -->
  </tbody>
</table>

### Datensatztypen abrufen

Dieses Aktionsmodul ruft eine Liste von Datensatztypen in einem [!DNL Adobe Workfront Planning] ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] finden Sie unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Wählen Sie den Arbeitsbereich aus, der die Datensatztypen enthält, die Sie abrufen möchten, oder ordnen Sie ihn zu.</td>
    </tr>
  </tbody>
</table>

### Eintrag aktualisieren

Diese Aktion aktualisiert einen einzelnen Datensatz in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL-Verbindung]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning] finden Sie unter <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Workfront Planning]</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Datensatz-ID]</p>
      </td>
      <td>Geben Sie den Typ des Datensatzes ein, den Sie aktualisieren möchten, oder ordnen Sie ihn zu. Die verfügbaren Datensatztypen basieren auf Ihrem Workfront Planning-Konto.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Andere Felder</p>
      </td>
      <td>Geben Sie die neuen Werte ein, die der Datensatz haben soll. Diese Felder basieren auf dem von Ihnen ausgewählten Datensatztyp.</td> 
      </tr>
     <tr>
  </tbody>
</table>


## Verwenden von JSONata für eine lesbare Aufschlüsselung der `record-types`

Der folgende JSONata-Ausdruck erstellt eine für Menschen lesbare Ausgabe der Planning-Abfrage, die Ihnen die Aufschlüsselung der Datensatztypen liefert. Dadurch können der Name des Datensatztyps, die Feldnamen und gegebenenfalls die Feldoptionennamen anhand eines Namens für Menschen lesbar gemacht werden, während der Rest der Struktur intakt bleibt.

```
(
    $s0 := ({"data":$ ~> | fields | {"options":(options){name:$}} |});
    $s1 := ({"data":$s0.data ~> | **.fields | {"options_name":(options.*){displayName:$}} | });
    $s2 := $s1 ~> | data | {"fields":(fields){displayName:$}} |; 
    $s2.data{displayName:$}
)
```

Informationen zur Verwendung von JSONata-Modulen finden Sie unter [JSONata-Module](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/jsonata-module.md).

