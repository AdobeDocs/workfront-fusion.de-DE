---
title: Adobe I/O Events-Module
description: Mit den Adobe I/O Events-Modulen können Sie ein Adobe Workfront Fusion-Szenario starten, das auf Ereignissen in Ihren Adobe-Programmen basiert.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: b2229f3e-a2a7-4b07-8ead-a37d193c2ec7
source-git-commit: 9cea5de748873720247db39161cea12c7e9c7186
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 1%

---

# Adobe I/O Events-Module

Mit den Adobe I/O Events-Modulen können Sie ein Adobe Workfront Fusion-Szenario starten, das auf Ereignissen in Adobe-Konten und -Services basiert, die keinen dedizierten Workfront Fusion-Connector haben.

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

Bevor Sie den Adobe I/O Events-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein gültiges Adobe-Konto verfügen.

## Adobe I/O Events-API-Informationen

Der Adobe I/O Events-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://api.adobe.io/events</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.6.7</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung mit Adobe I/O Events

So erstellen Sie eine Verbindung für Ihre Adobe I/O Events-Module:

1. Klicken Sie neben dem Feld Verbindung auf Hinzufügen .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">Name der Verbindung</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Typ</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Zusätzliche Bereiche</td>
        <td>Um weitere Bereiche hinzuzufügen, klicken Sie auf <b>Element hinzufügen</b> und geben Sie den Bereich ein.</td>
      </tr>
      <tr>
        <td role="rowheader">Client-ID</td>
        <td>Geben Sie Ihre Adobe-Client-ID ein. Diese finden Sie im Abschnitt Anmeldedaten des Adobe Developer Console</td>
      </tr>
      <tr>
        <td role="rowheader">Geheimer Client-Schlüssel</td>
        <td>Geben Sie Ihr Adobe-Client-Geheimnis ein. Diese finden Sie im Abschnitt Anmeldedaten des Adobe Developer Console</td>
      </tr>
      </tr>
        <tr>
        <td role="rowheader">Verbrauchenorg-ID</td>
        <td>Geben Sie Ihre Verbrauchenorg-ID ein. Diese finden Sie in der Berechtigungs-URL des Projekts: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">Berechtigungs-ID</td>
        <td>Geben Sie Ihre Berechtigungs-ID ein. Diese finden Sie in der Berechtigungs-URL des Projekts: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">IMS-Organisations-ID</td>
        <td>Geben Sie Ihre Adobe-Organisations-ID ein. Diese finden Sie im Abschnitt Anmeldedaten des Adobe Developer Console</td>
      </tr>
        <tr>
        <td role="rowheader">Projekt-ID</td>
        <td>Geben Sie Ihre Projekt-ID ein. Diese finden Sie in der Berechtigungs-URL des Projekts: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">WORKSPACE ID</td>
        <td>Um die Workspace-ID Ihres Projekts anzuzeigen, laden Sie Ihre Projektdetails von der Projektübersichtsseite in Adobe Developer Console herunter. </td>
      </tr>
    </tbody>
    </table>

1. Klicken Sie **Fortfahren**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## Adobe I/O Events-Module und ihre Felder

Beim Konfigurieren [!DNL Adobe I/O Events] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Adobe I/O Events] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

#### Erstellen einer Ereignisregistrierung

Dieses Aktionsmodul verwendet einen Webhook, um eine Ereignisbeschreibung zu erstellen. Hier können Sie einen Webhook konfigurieren. Wenn Sie einen vorhandenen Webhook verwenden, sind die Felder in diesem Modul schreibgeschützt.

So erstellen Sie einen Webhook:

1. Klicken Sie **Hinzufügen** neben dem Feld Webhook .
1. Füllen Sie die folgenden Felder aus:

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Webhook name]</td>
        <td>Einen Namen für diesen Webhook eingeben.</td>
       </tr>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe I/O Events] finden Sie unter <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe I/O Events]</a> in diesem Artikel.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Webhook description]
         </td>
         <td>
           Beschreibung für diesen Webhook eingeben.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event provider]
         </td>
         <td>
           Wählen Sie das Produkt oder Konto aus, aus dem Sie Ereignisse erstellen möchten.
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event type]
         </td>
         <td>
           Wählen Sie die Ereignisse aus, die der Webhook überwachen soll. Das Szenario tritt bei diesen Ereignissen im Trigger auf.
         </td>
       </tr>
     </tbody>
   </table>

1. Klicken Sie auf Speichern , um den Webhook zu speichern und zum Modul zurückzukehren.

### Aktionen

#### Alle Ereignisse aus einem Protokoll abrufen

Dieses Suchmodul ruft alle Ereignisse für eine Registrierung aus einem Journal ab.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe I/O Events] finden Sie unter <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe I/O Events]</a> in diesem Artikel.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Registration ID]
         </td>
         <td>
           Wählen Sie die Registrierung aus, für die Sie Ereignisse abrufen möchten.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Maximum number of returned records]
         </td>
         <td>
              Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie. 
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Return events that occur after]
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Seek]
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Latest]
         </td>
         <td>
         Aktivieren Sie diese Option, um das neueste Ereignis zurückzugeben.
         </td>
       </tr>
     </tbody>
   </table>

#### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt einen benutzerdefinierten API-Aufruf an die [!DNL Adobe I/O Events]-API durch

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe I/O Events] finden Sie unter <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe I/O Events]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Pfad eingeben für <code>https://api.adobe.io/events</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
      <td>
  <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p>  
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt automatisch Autorisierungs- und X-API-Schlüssel-Header hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
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

### Suchvorgänge

#### Provider- und Ereignis-IDs abrufen

Dieses Suchmodul ruft die Adobe I/O Events-IDs für den angegebenen Anbieter und die angegebenen Ereignisse ab.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe I/O Events] finden Sie unter <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe I/O Events]</a> in diesem Artikel.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event provider]
         </td>
         <td>
           Wählen Sie den Provider aus, für den Sie die ID abrufen möchten.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event type]
         </td>
         <td>
              Wählen Sie die Ereignisse aus, für die Sie IDs angeben möchten. Ereignisse sind je nach Ereignisanbieter verfügbar. 
         </td>
       </tr>
     </tbody>
   </table>

<!--

Watch Events

This trigger module starts a scenario when an event occurs in the chosen Adobe product or service.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">Webhook</td> 
   <td><p>Select the webhook that you want to use for this trigger, or add a new webhook. </p><p>To add a new webhook, <ol><li>Click <b>Add</b> next to the webhook field.</li><li>Enter the following: <ul><li>A name for the webhook</li><li>The connection that you want to use for this webhook</li><li>The source of the events you want to watch</li></ul></li><li>Click <b>Save</b> to save the webhook and return to the module. </td> 
   </tr> 
   </tbody> 
</table>

-->
