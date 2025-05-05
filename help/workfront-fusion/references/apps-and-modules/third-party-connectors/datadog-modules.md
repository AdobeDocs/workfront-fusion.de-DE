---
title: Datadog-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die Datadog verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
source-git-commit: 8a4e54a4c1783e4bc679778c6fcf21dcb4d3d537
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 1%

---

# [!DNL Datadog]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Datadog] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um [!DNL Datadog]-Module verwenden zu können, müssen Sie über ein [!DNL Datadog]-Konto verfügen.

## Datadog-API-Informationen

Der Datadog-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>1,0,11</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Datadog] mit [!DNL Workfront Fusion] verbinden {#connect-datadog-to-workfront-fusion}

### Abrufen Ihres API-Schlüssels und Anwendungsschlüssels {#retrieve-your-api-key-and-application-key}

Um Ihr [!DNL Datadog]-Konto mit [!DNL Workfront Fusion] zu verbinden, müssen Sie einen API-Schlüssel und einen Anwendungsschlüssel aus Ihrem [!DNL Datadog]-Konto abrufen.

1. Melden Sie sich bei Ihrem [!DNL Datadog] an.
1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Integrationen]** und dann auf **[!UICONTROL APIs]**.
1. Klicken Sie im Hauptbildschirm auf **[!UICONTROL API-Schlüssel]**.
1. Bewegen Sie den Mauszeiger über die violette Leiste, um den API-Schlüssel anzuzeigen.
1. Kopieren Sie den API-Schlüssel an einen sicheren Speicherort.
1. Klicken Sie im Hauptbildschirm auf **[!UICONTROL Anwendungsschlüssel]**.
1. Bewegen Sie den Mauszeiger über die violette Leiste, um den Anwendungsschlüssel anzuzeigen.
1. Kopieren Sie den Anwendungsschlüssel an einen sicheren Speicherort.

### Erstellen einer Verbindung zu [!DNL Datadog] in [!DNL Workfront Fusion]

Sie können eine Verbindung zu Ihrem [!DNL Datadog]-Konto direkt aus einem [!UICONTROL Datadog]-Modul erstellen.

1. Klicken Sie in einem [!UICONTROL Datadog]-Modul **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Füllen Sie die Felder des Moduls wie folgt aus:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Verbindungsname]</td> 
      <td> <p> Geben Sie einen Namen für die Verbindung ein.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>Wählen Sie aus, ob diese Verbindung für eine Produktions- oder Nicht-Produktionsumgebung vorgesehen ist.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Domain] </td> 
      <td> <p>Wählen Sie die Domain aus, zu der Sie eine Verbindung herstellen möchten (USA oder EU).</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API-Schlüsselspeicherort] </td> 
      <td> <p>Wählen Sie aus, ob der API-Schlüssel in die Kopfzeile oder in die Abfragezeichenfolge aufgenommen werden soll.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API-Schlüssel]</td> 
      <td> <p> Geben Sie Ihren [!DNL Datadog] API-Schlüssel ein. </p> <p>Anweisungen zum Abrufen des API-Schlüssels finden Sie unter <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">Abrufen Ihres API-Schlüssels und </a>) in diesem Artikel.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Datadog] Module und ihre Felder

Beim Konfigurieren [!DNL Datadog] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Datadog] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Aktionen

* [[!UICONTROL Erstellen eines API-Aufrufs]](#make-an-api-call)
* [[!UICONTROL Zeitreihen-Punkte posten]](#post-timeseries-points)

#### [!UICONTROL Erstellen eines API-Aufrufs]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Datadog]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Datadog] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dedizierte Domain verwenden]</td> 
   <td>Einige Datadog-API-Endpunkte, die viel eingehenden Traffic erwarten, werden auf ihren dedizierten Domains ausgeführt. Aktivieren Sie dieses Kontrollkästchen, um die dedizierte Domain für Ihren API-Aufruf zu verwenden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://api.datadoghq.com/api/</code> ein. Beispiel: <code> /v1/org</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel:** Der folgende API-Aufruf gibt alle Dashboards in Ihrem [!DNL Datadog]-Konto zurück:

URL: `/v1/dashboard`

Methode: `GET`

![Beispiel für einen Datadog-API-Aufruf](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-example.png)

Das Ergebnis finden Sie in der Modulausgabe unter Bundle > Hauptteil > Dashboards.

In unserem Beispiel wurden drei Dashboards zurückgegeben:

![Datadog-API-Antwort](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-response-example.png)

#### [!UICONTROL Zeitreihen-Punkte posten]

Mit dem Modul können Sie Zeitreihendaten posten, die in [!DNL Datadog] Dashboards grafisch dargestellt werden können.

Der Grenzwert für komprimierte Payloads beträgt 3,2 Megabyte (3200000) und 62 Megabyte (62914560) für dekomprimierte Payloads.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Datadog]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Datadog] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Typ]</td> 
   <td> Wählen Sie den Typ der Metrik aus, den Sie verwenden möchten. 
   <ul>
   <li>Tachometer</li>
   <li>Rate</li>
   <li>Count</li>
   </ul>
   </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL Interval]</td> 
   <td> Wenn der Typ der Metrik „Rate“ oder „Anzahl“ lautet, definieren Sie das entsprechende Intervall.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Points]</td> 
   <td><p>Fügen Sie Punkte hinzu, die sich auf eine Metrik beziehen.</p> <p>Dies ist ein JSON-Array von Punkten. Jeder Punkt hat das folgende Format: <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>Hinweis:  <p>Der Zeitstempel muss in Sekunden angegeben werden.</p> <p>Der Zeitstempel muss aktuell sein. Aktuell ist definiert als nicht mehr als 10 Minuten in der Zukunft oder als mehr als 1 Stunde in der Vergangenheit.</p> <p> Das numerische Wertformat sollte ein Fließwert sein.</p> </p> <p>Dieses Feld muss mindestens 1 Element enthalten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Host]</td> 
   <td>Geben Sie den Namen des Hosts ein, der die Metrik erzeugt hat. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> Klicken Sie für jedes Tag, das Sie der Metrik hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie den Wert des Tags ein.</td> 
  </tr> 
 </tbody> 
</table>
