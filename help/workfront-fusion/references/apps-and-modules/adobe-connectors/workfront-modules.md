---
title: Adobe Workfront-Module
description: Sie können den Adobe Workfront Fusion Adobe Workfront-Connector verwenden, um Ihre Prozesse in Workfront zu automatisieren. Wenn Sie über eine Lizenz für Workfront Fusion for Work Automation und Integration verfügen, können Sie damit auch eine Verbindung zu Apps und Services von Drittanbietern herstellen.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '8067'
ht-degree: 7%

---

# Adobe Workfront-Module

Sie können den Adobe Workfront Fusion Adobe Workfront-Connector verwenden, um Ihre Prozesse in Workfront zu automatisieren. Sie können Workfront auch mit anderen Programmen und Services verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Legacy: Beliebig </p>
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


>[!NOTE]
>
>* Wenn Ihr Unternehmen das veraltete Lizenzierungspaket (basierend auf Connectoren) verwendet, muss es über eine Workfront Fusion for Work Automation- und Integrationslizenz verfügen, um eine Verbindung zu Apps und Services von Drittanbietern herzustellen. Der Workfront-Connector wird nicht auf die Anzahl der aktiven Apps angerechnet, die für Ihr Unternehmen verfügbar sind. Alle Szenarien werden mit der Gesamtanzahl des Szenarios Ihres Unternehmens verrechnet, auch wenn sie nur die Workfront-App verwenden.

+++

## Verbinden von Workfront mit Workfront Fusion

Der Workfront-Connector verwendet OAuth 2.0, um eine Verbindung zu Workfront herzustellen.

Sie können direkt aus einem Workfront Fusion-Modul heraus eine Verbindung zu Ihrem Workfront-Konto herstellen.

1. Klicken Sie in einem beliebigen Adobe Workfront **Modul** Hinzufügen) neben dem Feld Verbindung .
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
          <p>Geben Sie einen Namen für die neue Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>
          <p>Wählen Sie aus, ob eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung hergestellt werden soll.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungstyp]</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre Workfront-Client-ID ein. Diese finden Sie im Bereich OAuth2-Anwendungen des Bereichs Setup in Workfront. Öffnen Sie das spezifische Programm, mit dem Sie eine Verbindung herstellen, um die Client-ID anzuzeigen.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr Workfront-Client-Geheimnis ein. Diese finden Sie im Bereich OAuth2-Anwendungen des Bereichs Setup in Workfront. Wenn Sie in Workfront kein Client-Geheimnis für Ihr OAuth2-Programm haben, können Sie ein anderes generieren. Anweisungen hierzu finden Sie in der Dokumentation zu Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL-Authentifizierungs-URL]</td>
        <td>Dies kann der Standardwert bleiben oder Sie können die URL Ihrer Workfront-Instanz gefolgt von <code>/integrations/oauth2</code> eingeben. <p>Beispiel: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host-Präfix]</td>
        <td>In den meisten Fällen sollte dieser Wert <code>origin</code> werden.
      </tr>
    </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

   Wenn Sie nicht bei Workfront angemeldet sind, werden Sie zu einem Anmeldebildschirm weitergeleitet. Nach der Anmeldung können Sie die Verbindung zulassen.

>[!NOTE]
>
>* OAuth 2.0-Verbindungen zur Workfront-API sind nicht mehr auf API-Schlüssel angewiesen.
>* Um eine Verbindung zu einer Workfront Sandbox-Umgebung herzustellen, müssen Sie in dieser Umgebung eine OAuth2-Anwendung erstellen und dann die von dieser Anwendung generierte Client-ID und den geheimen Client-Schlüssel in Ihrer Verbindung verwenden.

## Workfront-Module und ihre Felder

Beim Konfigurieren von Workfront-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service können zusätzlich dazu weitere Workfront-Felder angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Wenn in einem Workfront-Modul nicht die aktuellsten Felder angezeigt werden, kann dies an Problemen mit der Zwischenspeicherung liegen. Eine Stunde warten und erneut versuchen.
>* HTTP 429-Status-Codes von Adobe Workfront sollten keine Deaktivierungen verursachen, sondern stattdessen eine kurze Ausführungspause im Trigger verursachen.

* [Triggers](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Trigger

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL Ereignisse ansehen]**

Dieses Trigger-Modul führt ein Szenario in Echtzeit aus, wenn Objekte eines bestimmten Typs in Workfront hinzugefügt, aktualisiert oder gelöscht werden

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

1. Klicken **[!UICONTROL rechts neben dem Feld]** Webhook **auf „Hinzufügen**.

1. Konfigurieren Sie den Webhook im Feld **[!UICONTROL Hook hinzufügen]** das angezeigt wird.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Webhook-Name]</td> 
      <td>Einen Namen für den Webhook eingeben</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL-Verbindung]</td> 
      <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Datensatztyp]</td> 
      <td>Wählen Sie den Typ des Workfront-Datensatzes aus, den das Modul überwachen soll.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL-Status]</td> 
      <td>Wählen Sie aus, ob der alte oder der neue Status überwacht werden soll.<ul><li><p><b>[!UICONTROL Neuer Status]</b></p><p>Trigger : Ein Szenario, in dem sich der Datensatz <b> einem </b> Wert ändert.</p><p>Wenn beispielsweise der Status auf [!UICONTROL Neuer Status] festgelegt ist und der Filter auf [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress] festgelegt ist, gibt der Webhook einem Szenario einen Trigger, wenn der [!UICONTROL Status] zu [!UICONTROL In Progress] wechselt, unabhängig davon, welcher Status zuvor war. </p></li><li><p><b>[!UICONTROL Alter Status]</b></p><p>Trigger : Ein Szenario, in dem sich der Datensatz <b> einem </b> Wert ändert.</p><p>Wenn beispielsweise der Status auf [!UICONTROL Alter Status] festgelegt ist und der Filter auf [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress] festgelegt ist, gibt der Webhook einem Szenario einen Trigger, wenn ein [!UICONTROL Status], der derzeit [!UICONTROL In Progress] ist, zu einem anderen Status wechselt. </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Ereignisfilter]</p> </td> 
      <td> <p>Sie können Filter festlegen, um nur nach Datensätzen zu suchen, die die von Ihnen ausgewählten Kriterien erfüllen.</p> <p>Geben Sie für jeden Filter das Feld ein, das vom Filter ausgewertet werden soll, den Operator und den Wert, den der Filter zulassen soll. Sie können mehr als einen Filter verwenden, indem Sie AND-Regeln hinzufügen.</p> <p><b>HINWEIS</b>: Filter in vorhandenen Workfront-Webhooks können nicht bearbeitet werden. Um verschiedene Filter für Workfront-Ereignisabonnements einzurichten, entfernen Sie den aktuellen Webhook und erstellen Sie einen neuen.</p> <p>Weitere Informationen zu Ereignisfiltern finden Sie unter <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Ereignisabonnementfilter in den Modulen Workfront &gt; [!UICONTROL Ereignisse </a>] in diesem Artikel.</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>Ausschließen von Ereignissen, die von dieser Verbindung stammen</td> 
      <td>Aktivieren Sie diese Option, um Ereignisse auszuschließen, die mit demselben Connector erstellt oder aktualisiert wurden, den dieses Trigger-Modul verwendet. Dadurch können Situationen verhindert werden, in denen ein Szenario sich selbst in Trigger versetzt und in einer Endlosschleife wiederholt wird.<p><b>HINWEIS</b>: Der Datensatztyp „Zuweisung“ umfasst diese Option nicht.</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Record Origin]</td> 
      <td>
       <p>Wählen Sie aus, ob das Szenario [!UICONTROL Nur neue Datensätze], [!UICONTROL Nur aktualisierte Datensätze], [!UICONTROL Neue und aktualisierte Datensätze] oder [!DNL Deleted Records Only] ansehen soll.</p>
       <p><b>HINWEIS</b>: Wenn Sie die Option [!UICONTROL Neue und aktualisierte Datensätze] auswählen, erstellt die Webhook-Erstellung zwei Ereignisabonnements (für dieselbe Webhook-Adresse).</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

Nachdem der Webhook erstellt wurde, können Sie die Adresse des Endpunkts anzeigen, an den Ereignisse gesendet werden.

Weitere Informationen finden Sie im Abschnitt [Beispiele für Ereignis-Payloads](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads) im Artikel Ereignisabonnement-API in der Dokumentation zu Workfront.

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Feld beobachten]**

Dieses Feldmodul führt ein Trigger aus, wenn ein von Ihnen angegebenes Feld aktualisiert wird. Das Modul gibt sowohl den alten als auch den neuen Wert des angegebenen Felds zurück. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Datensatzes aus, den das Modul überwachen soll.</p> <p>Wählen Sie beispielsweise [!UICONTROL Task] aus, wenn Sie die Ausführung des Szenarios jedes Mal starten möchten, wenn ein Datensatzfeld in einer Aufgabe aktualisiert wird.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Feld]</td> 
   <td>Wählen Sie das Feld aus, das das Modul auf Aktualisierungen überwachen soll. Diese Felder spiegeln die Felder wider, die Ihr Workfront-Administrator für das Tracking eingerichtet hat.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Objektfelder aus, die Sie in das Ausgabepaket für dieses Modul aufnehmen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Aufzeichnung ansehen]**

Dieses Trigger-Modul führt ein Szenario aus, in dem Objekte eines bestimmten Typs hinzugefügt, aktualisiert oder beides werden. Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz oder den Datensätzen verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

In der Ausgabe gibt das Modul an, ob jeder Datensatz neu oder aktualisiert ist.

Datensätze, die seit der letzten Ausführung des Szenarios hinzugefügt und aktualisiert wurden, werden als neue Datensätze zurückgegeben.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL filter]</td> 
   <td> <p>Wählen Sie aus, ob das Szenario [!UICONTROL Nur neue Datensätze], [!UICONTROL Nur aktualisierte Datensätze] oder [!UICONTROL Neue und aktualisierte Datensätze] ansehen soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Datensatzes aus, den das Modul überwachen soll.</p> <p>Wenn Sie beispielsweise das Szenario jedes Mal starten möchten, wenn ein neues Projekt erstellt wird, wählen Sie [!UICONTROL Project] aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Referenz]</td> 
   <td> <p>Wählen Sie die Referenzfelder aus, die Sie in das Ausgabepaket für dieses Modul aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Sammlungsfelder aus, die Sie in das Ausgabepaket für dieses Modul aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optionaler Filter]</td> 
   <td> <p>(Erweitert) Geben Sie eine API-Code-Zeichenfolge ein, um zusätzliche Parameter oder Code zu definieren, die Ihre Kriterien verfeinern. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

+++


### Aktionen

<!--
* [Convert object](#convert-object) 
* [Create a record (attaching custom forms)](#create-a-record-attaching-custom-forms) 
* [Create a record](#create-a-record) 
* [Custom API Call](#custom-api-call) 
* [Delete Record](#delete-record) 
* [Download Document](#download-document) 
* [Misc Action](#misc-action) 
* [Read a Record](#read-a-record) 
* [Update Record](#update-record) 
* [Upload Document](#upload-document)
-->

+++ **[!UICONTROL Objekt konvertieren]**

Dieses Aktionsmodul führt eine der folgenden Konvertierungen durch:

* Anfrage in Projekt konvertieren
* Anfrage in Aufgabe konvertieren
* Aufgabe in Projekt konvertieren

>[!NOTE]
>
>Seit Juli 2024 können benutzerdefinierte Formulare beim Konvertieren eines -Objekts einbezogen werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Objekttyp]</td> 
   <td> <p>Wählen Sie den Typ des Objekts aus, das Sie konvertieren möchten. Dies ist der Typ, den das Objekt vor der Konvertierung hat.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL nach] konvertieren</td> 
   <td>Wählen Sie das Objekt aus, in das Sie es konvertieren möchten. Dies ist der Typ, den das Objekt nach der Konvertierung hat.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL &lt;Objekt&gt;-ID]</td> 
   <td> <p>Geben Sie die ID des Objekts ein. </p> <p>Hinweis: Bei der Eingabe der ID eines Objekts können Sie mit der Eingabe des Namens des Objekts beginnen und es dann aus der Liste auswählen. Das Modul gibt dann die entsprechende ID in das Feld ein.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Vorlagenkennung]</td> 
   <td> <p>Wenn Sie in ein Projekt konvertieren, wählen Sie die Vorlagen-ID aus, die Sie für das Projekt verwenden möchten.</p> <p>Hinweis: Bei der Eingabe der ID eines Objekts können Sie mit der Eingabe des Namens des Objekts beginnen und es dann aus der Liste auswählen. Das Modul gibt dann die entsprechende ID in das Feld ein.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Benutzerdefinierte Formulare]</td> 
   <td>Wählen Sie alle benutzerdefinierten Formulare aus, die Sie dem neu konvertierten -Objekt hinzufügen möchten, und geben Sie dann Werte für die Felder des benutzerdefinierten Formulars ein.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL-Optionen]</td> 
   <td> <p>Aktivieren Sie beim Konvertieren des -Objekts alle gewünschten Optionen. Je nachdem, in welches Objekt Sie konvertieren oder aus welchem Sie konvertieren, sind Optionen verfügbar.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Native Felder kopieren]</td> 
   <td> <p>Aktivieren Sie diese Option, um alle nativen Felder aus dem ursprünglichen Objekt in das neue Objekt zu kopieren.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Benutzerdefinierte Formulare kopieren]</td> 
   <td> <p>Aktivieren Sie diese Option, um alle nativen Felder aus dem ursprünglichen Objekt in das neue Objekt zu kopieren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Datensatz erstellen]** 

Dieses Aktionsmodul erstellt ein Objekt, z. B. ein Projekt, eine Aufgabe oder ein Problem in Workfront und ermöglicht das Hinzufügen eines benutzerdefinierten Formulars zum neuen Objekt. Mit dem Modul können Sie auswählen, welche der Objektfelder im Modul verfügbar sind.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Stellen Sie sicher, dass Sie die Mindestanzahl von Eingabefeldern angeben. Wenn Sie beispielsweise ein Problem erstellen möchten, müssen Sie im Feld „Projekt-ID“ eine gültige übergeordnete Projekt-ID angeben, um anzugeben, wo das Problem in Workfront auftreten soll. Sie können das Zuordnungsbedienfeld verwenden, um diese Informationen einem anderen Modul in Ihrem Szenario zuzuordnen, oder Sie können sie manuell eingeben, indem Sie den Namen eingeben und ihn dann aus der Liste auswählen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Datensatzes aus, den das Modul erstellen soll.</p> <p>Wenn Sie beispielsweise ein Projekt erstellen möchten, wählen Sie [!UICONTROL Project] aus der Dropdown-Liste aus.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Felder zum Zuordnen auswählen]</td> 
   <td> <p>Wählen Sie die Felder aus, die für die Dateneingabe verfügbar sein sollen. Auf diese Weise können Sie diese Felder verwenden, ohne die nicht benötigten Felder durchscrollen zu müssen. Anschließend können Sie Daten in diese Felder eingeben oder zuordnen.</p> <p>Verwenden Sie für Felder in benutzerdefinierten Formularen das Feld <b>[!UICONTROL Benutzerdefiniertes Formular anhängen]</b>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Benutzerdefiniertes Formular anhängen]</td> 
   <td>Wählen Sie alle benutzerdefinierten Formulare aus, die Sie dem neuen Objekt hinzufügen möchten, und geben Sie dann Werte für diese Felder ein oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Wenn Sie die ID eines Objekts eingeben, können Sie mit der Eingabe des Namens des Objekts beginnen und es dann aus der Liste auswählen. Das Modul gibt dann die entsprechende ID in das Feld ein.
>* Bei der Eingabe von Text für ein benutzerdefiniertes Feld oder ein [!UICONTROL Hinweis]-Objekt (Kommentar oder Antwort) können Sie HTML-Tags im Feld [!UICONTROL Notizentext] verwenden, um Rich-Text zu erstellen, z. B. fett oder kursiv gedruckten Text.
>



>[!NOTE]
>
>Benutzende werden im Status Deaktiviert und Ausstehende Genehmigung erstellt. Wenn Ihr Unternehmen in die Adobe Admin Console migriert wurde und das Abzeichen Ausstehende Genehmigung nicht innerhalb weniger Minuten entfernt wird, können Sie den Benutzer genehmigen.
>
>* **Auflösen einzelner Benutzer**
>
>      In der Benutzerliste können Sie Probleme bei einzelnen Benutzenden lösen.
>
>      1. Wählen Sie die Benutzenden in der Benutzerliste aus.
>      1. Klicken Sie auf das Dreipunkt-Menü in der Listenüberschrift.
>      1. Wählen Sie **Genehmigen** aus.
>      1. Aktualisieren Sie die Seite nach einigen Minuten.
>
>* **Auflösen von Benutzenden, die in einem großen Batch hinzugefügt wurden**
>
>   Um Probleme bei Benutzenden zu lösen, die in großer Anzahl hinzugefügt wurden, können Sie den Batch von Benutzenden direkt in der Adobe Admin Console hinzufügen.
>
>   Anweisungen finden Sie unter [Verwalten mehrerer Benutzender | CSV-Massen-Upload](https://helpx.adobe.com/de/enterprise/using/bulk-upload-users.html) in der Adobe-Dokumentation.

+++

+++ **[!UICONTROL Datensatz erstellen (veraltet)]**

>[!IMPORTANT]
>
>Dieses Modul wurde durch das Modul Datensatz erstellen ersetzt. Es wird empfohlen, dieses Modul in neuen Szenarien zu verwenden.
>>Vorhandene Szenarien, die dieses Modul verwenden, funktionieren weiterhin erwartungsgemäß. Dieses Modul wird im Mai 2025 aus der Modulauswahl entfernt.

Dieses Aktionsmodul erstellt ein Objekt, z. B. ein Projekt, eine Aufgabe oder ein Problem in Workfront. Mit dem Modul können Sie auswählen, welche der Objektfelder im Modul verfügbar sind.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Stellen Sie sicher, dass Sie die Mindestanzahl von Eingabefeldern angeben. Wenn Sie beispielsweise ein Problem erstellen möchten, müssen Sie im Feld „Projekt-ID“ eine gültige übergeordnete Projekt-ID angeben, um anzugeben, wo das Problem in Workfront auftreten soll. Sie können das Zuordnungsbedienfeld verwenden, um diese Informationen einem anderen Modul in Ihrem Szenario zuzuordnen, oder Sie können sie manuell eingeben, indem Sie den Namen eingeben und ihn dann aus der Liste auswählen.

Dieses Modul hängt beim Erstellen des -Objekts keine benutzerdefinierten Formulare an. Um benutzerdefinierte Formulare beim Erstellen eines -Objekts anzuhängen, verwenden Sie das Modul [!UICONTROL Erstellen eines Datensatzes (Anhängen benutzerdefinierter Formulare].

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Datensatzes aus, den das Modul erstellen soll.</p> <p>Wenn Sie beispielsweise ein Projekt erstellen möchten, wählen Sie [!UICONTROL Project] aus der Dropdown-Liste aus.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Felder zum Zuordnen auswählen]</td> 
   <td>Wählen Sie die Felder aus, die für die Dateneingabe verfügbar sein sollen. Auf diese Weise können Sie diese Felder verwenden, ohne die nicht benötigten Felder durchscrollen zu müssen.</td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Wenn Sie die ID eines Objekts eingeben, können Sie mit der Eingabe des Namens des Objekts beginnen und es dann aus der Liste auswählen. Das Modul gibt dann die entsprechende ID in das Feld ein.
>* Bei der Eingabe von Text für ein benutzerdefiniertes Feld oder ein [!UICONTROL Hinweis]-Objekt (Kommentar oder Antwort) können Sie HTML-Tags im Feld [!UICONTROL Notizentext] verwenden, um Rich-Text zu erstellen, z. B. fett oder kursiv gedruckten Text.

+++

+++ **[!UICONTROL Benutzerdefinierter API-Aufruf]**

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die Workfront-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen Workfront-Modulen nicht durchgeführt werden kann.

Das -Modul gibt die folgenden Informationen zurück:

* **[!UICONTROL Status-Code]** (Zahl): Dies zeigt den Erfolg oder Misserfolg Ihrer HTTP-Anfrage an. Dies sind Standardcodes, die Sie im Internet nachschlagen können.
* **[!UICONTROL Headers]** (Objekt): Ein detaillierterer Kontext für die Antwort/den Status-Code, der sich nicht auf den Ausgabetext bezieht. Nicht alle Kopfzeilen, die in einer Antwort-Kopfzeile angezeigt werden, sind Antwort-Kopfzeilen, sodass einige möglicherweise nicht für Sie nützlich sind.

  Die Antwort-Header hängen von der HTTP-Anfrage ab, die Sie beim Konfigurieren des Moduls ausgewählt haben.

* **[!UICONTROL body]** (Objekt): Je nach der HTTP-Anfrage, die Sie beim Konfigurieren des Moduls ausgewählt haben, erhalten Sie möglicherweise einige Daten zurück. Diese Daten, z. B. die Daten aus einer GET-Anfrage, sind in diesem Objekt enthalten.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Geben Sie einen Pfad relativ zu ein<code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API-Version]</td> 
   <td>Wählen Sie die Version der Workfront-API aus, die das Modul verwenden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden in Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Dadurch wird der Inhaltstyp der Anfrage bestimmt.</p> <p>Beispiel:<code> {"Content-type":"application/json"}</code></p> <p>Hinweis: Wenn Fehler auftreten und es schwierig ist, deren Ursprung zu ermitteln, sollten Sie die Kopfzeilen basierend auf der Workfront-Dokumentation ändern. Wenn Ihr benutzerdefinierter API-Aufruf einen 422-HTTP-Anfragefehler zurückgibt, versuchen Sie es mit einer <code>"Content-Type":"text/plain"</code>-Kopfzeile.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> <p>Tipp: Es wird empfohlen, Informationen über den JSON-Text und nicht als Abfrageparameter zu senden.</p> </td> 
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

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Datensatz löschen]**

Dieses Aktionsmodul löscht ein Objekt, z. B. ein Projekt, eine Aufgabe oder ein Problem in Workfront.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Löschen erzwingen]</td> 
   <td>Aktivieren Sie diese Option, um sicherzustellen, dass der Datensatz gelöscht wird, auch wenn die Workfront-Benutzeroberfläche eine Löschbestätigung anfordern würde.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Async delete]</td> 
   <td>Aktivieren Sie diese Option, damit das Modul asynchron gelöscht werden kann.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>Geben Sie die eindeutige Workfront-ID des Datensatzes ein, den Sie löschen möchten.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=". Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Typ des Workfront-Eintrags aus, den das Modul löschen soll.</td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>Wir empfehlen die folgende Szenariokonfiguration, um zu vermeiden, dass Datensätze aufgrund asynchroner Vorgänge nicht gelöscht werden.
>
>1. Datensatz synchron löschen.
>1. Fügen Sie die Fehlerbehandlung zum Modul Datensatz löschen hinzu, um den Fehler zu ignorieren, der durch die Zeitüberschreitung nach 40 Sekunden verursacht wird.


+++

+++ **[!UICONTROL Dokument herunterladen]**

Dieses Aktionsmodul lädt ein Dokument von Workfront herunter.

Sie geben die ID des Datensatzes an.

Das Modul gibt den Inhalt, den Dateinamen, die Dateierweiterung und die Dateigröße des Dokuments zurück. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dokument-ID]</td> 
   <td> <p>Ordnen Sie die eindeutige Workfront-ID des Dokuments zu, das das Modul herunterladen soll, oder geben Sie sie manuell ein.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=". Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Misc-Aktion]**

Mit diesem Aktionsmodul können Sie Aktionen für die API durchführen.

>[!NOTE]
>
>Seit Juli 2024 umfasst die `convertToProject` die `copyCategories`. Bei Festlegung auf `TRUE` werden alle benutzerdefinierten Formulare in das Projekt aufgenommen, in das das Problem konvertiert wird.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Datensatzes aus, mit dem das Modul interagieren soll.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL-Aktion]</td> 
   <td> <p>Wählen Sie die Aktion aus, die das Modul ausführen soll.</p> <p>Je nach ausgewähltem [!UICONTROL-Datensatztyp] und [!UICONTROL-Aktion] müssen Sie möglicherweise zusätzliche Felder ausfüllen. Einige Kombinationen dieser beiden Einstellungen erfordern möglicherweise nur eine Datensatz-ID, während andere (wie Project für den <strong>[!UICONTROL Record Type]</strong> und [!UICONTROL Attach Template] für den <strong>[!UICONTROL Action]</strong>) zusätzliche Informationen erfordern (wie eine Objekt-ID und eine Vorlagen-ID).</p><p>Die für einige Aktionen verfügbaren Optionen finden Sie unter <a href="#misc-action-options" class="MCXref xref">Sonstige Aktionsoptionen</a> in diesem Artikel.</p> <p>Detaillierte Informationen zu den einzelnen Feldern finden Sie in der <a href="http://developer.workfront.com/">Workfront-Entwicklerdokumentation</a>. <p><strong>Hinweis</strong>: Die Site mit der Entwicklerdokumentation enthält Informationen nur über API-Version 14, enthält jedoch weiterhin wertvolle Informationen für API-Aufrufe. </p> 
    <ol> 
     <li value="1"> <p>Wählen Sie in der linken Navigationsleiste der Workfront Developer-Dokumentationsseite den Datensatztyp aus. Die folgenden Typen verfügen über eigene Seiten:</p> 
      <ul> 
       <li> <p>[!UICONTROL-Projekte]</p> </li> 
       <li> <p>[!UICONTROL Aufgaben]</p> </li> 
       <li> <p>[!UICONTROL Probleme]</p> </li> 
       <li> <p>[!UICONTROL Benutzer]</p> </li> 
       <li> <p>[!UICONTROL-Dokumente]</p> </li> 
      </ul> <p>Wählen Sie für alle anderen Datensatztypen <b>[!UICONTROL Andere Objekte und Endpunkte]</b> aus und suchen Sie den Datensatztyp auf den alphabetisch sortierten Seiten.</p> </li> 
     <li value="2"> <p>Suchen Sie auf der Seite des entsprechenden Datensatztyps (Strg+F bzw. Befehl+F) nach der Aktion.</p> </li> 
     <li value="3"> <p>Anzeigen von Beschreibungen für verfügbare Felder unter der ausgewählten Aktion.</p> </li> 
    </ol> <p>Hinweis:  <p>Beim Erstellen eines Korrekturabzugs über das Modul [!UICONTROL Misc Action] von Workfront empfiehlt es sich, einen Korrekturabzug ohne erweiterte Optionen zu erstellen und dann den Korrekturabzug mithilfe der [!DNL Workfront Proof] SOAP-API zu aktualisieren.</p><p>Weitere Informationen zum Erstellen eines Korrekturabzugs mit der Workfront-API (die dieses Modul verwendet) finden Sie unter <a href="https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">Hinzufügen erweiterter Proofing-Optionen beim Erstellen eines Korrekturabzugs über die Adobe Workfront-API</a></p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>Geben Sie die eindeutige Workfront-ID des Datensatzes ein, mit dem das Modul interagieren soll, oder mappen Sie sie.<p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=". Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

#### Sonstige Aktionsoptionen

##### Aufgabe

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Aktion</th> 
   <th>Optionen</th> 
  </tr> 
  <tr> 
   <td>Kopieren</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>Zuweisungen löschen</li>
   <li>clearConstraints</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Löscht die Finanzdaten</p></li>
   <li>clearPermissions</li>
   <li>clearVorgänger</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Löscht Erinnerungsnachrichten</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Verschieben</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>Zuweisungen löschen</li>
   <li>clearDocuments</li>
   <li>clearConstraints</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Löscht die Finanzdaten</p></li>
   <li>clearPermissions</li>
   <li>clearVorgänger</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Löscht Erinnerungsnachrichten</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

##### Problem

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Aktion</th> 
   <th>Optionen</th> 
  </tr> 
  <tr> 
   <td>Kopieren</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>Zuweisungen löschen</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearPermissions</li>
   <li>clearProgress</li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>In Aufgabe umwandeln</td> 
   <td>
   <ul>
   <li>Anfrage aufbewahren<p>Ursprüngliche Anfrage aufbewahren und deren Lösung mit dieser Aufgabe verknüpfen</p></li>
   <li>preservePrimaryContact<p>Dem primären Kontakt der Anfrage Zugriff auf diese Aufgabe erteilen</p></li>
   <li>preserveCompletionDate<p>Geplantes Abschlussdatum der Anfrage beibehalten</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>In Projekt konvertieren</td> 
   <td>
   <ul>
   <li>Anfrage aufbewahren<p>Ursprüngliche Anfrage aufbewahren und deren Lösung mit dieser Aufgabe verknüpfen</p></li>
   <li>preservePrimaryContact<p>Dem primären Kontakt der Anfrage Zugriff auf diese Aufgabe erteilen</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



##### Projekt

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Aktion</th> 
   <th>Optionen</th> 
  </tr> 
  <tr> 
   <td>Kopieren</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>Zuweisungen löschen</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Löscht die Finanzdaten</p></li>
   <li>clearPermissions</li>
   <li>clearVorgänger</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Löscht Erinnerungsnachrichten</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Vorlage anfügen / als Vorlage speichern</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>Zuweisungen löschen</li>
   <li>clearBillingRates</li>
   <li>clearConstraints</li>
   <li>clearDeliverables<p>Löscht Ziele</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Löscht die Finanzdaten</p></li>
   <li>clearHourTypes</li>
   <li>clearIssueSetup<p>Löscht die Warteschlangeneigenschaften und das Problem-Setup</p></li>
   <li>clearVorgänger</li>
   <li>Risiken löschen</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>Löscht Erinnerungsnachrichten</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL Datensatz lesen]**

Dieses Aktionsmodul ruft Daten aus einem einzelnen Datensatz ab.

Sie geben die ID des Datensatzes an. Sie können auch angeben, welche verwandten Datensätze das Modul lesen soll.

Wenn es sich bei dem Datensatz, den das Modul liest, beispielsweise um ein Projekt handelt, können Sie angeben, dass die Aufgaben des Projekts gelesen werden sollen.

Das -Modul gibt ein Array von Daten aus den von Ihnen angegebenen Ausgabefeldern zurück.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL-Verbindung]</td>
    <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Datensatztyp]</td>

<td>Wählen Sie den Workfront-Objekttyp aus, den das Modul lesen soll.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Ausgaben]</td>

<td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Ausgabe Benutzerdefiniertes Formular]</td>
     <td> <p>Wählen Sie die benutzerdefinierten Formulare aus, die Sie in das Ausgabepaket für dieses Modul aufnehmen möchten, und wählen Sie dann die spezifischen Felder aus den benutzerdefinierten Formularen aus, die Sie in die Ausgabe aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL-Verweise]</td>
   <td>Wählen Sie alle Referenzfelder aus, die Sie in die Ausgabe aufnehmen möchten.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL-Sammlungen]</td>
   <td>Wählen Sie alle Referenzfelder aus, die Sie in die Ausgabe aufnehmen möchten.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Geben Sie die eindeutige Workfront-ID des Datensatzes ein, den das Modul lesen soll.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=". Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Datensatz lesen (veraltet)]**

>[!IMPORTANT]
>
>Dieses Modul wurde durch das Modul Datensatz lesen ersetzt. Es wird empfohlen, dieses Modul in neuen Szenarien zu verwenden.
>>Vorhandene Szenarien, die dieses Modul verwenden, funktionieren weiterhin erwartungsgemäß. Dieses Modul wird im Mai 2025 aus der Modulauswahl entfernt.

Dieses Aktionsmodul ruft Daten aus einem einzelnen Datensatz ab.

Sie geben die ID des Datensatzes an. Sie können auch angeben, welche verwandten Datensätze das Modul lesen soll.

Wenn es sich bei dem Datensatz, den das Modul liest, beispielsweise um ein Projekt handelt, können Sie angeben, dass die Aufgaben des Projekts gelesen werden sollen.

Das -Modul gibt ein Array von Daten aus den von Ihnen angegebenen Ausgabefeldern zurück.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL-Verbindung]</td>
    <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Datensatztyp]</td>

<td>Wählen Sie den Workfront-Objekttyp aus, den das Modul lesen soll.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Ausgaben]</td>

<td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL-Verweise]</td>
   <td>Wählen Sie alle Referenzfelder aus, die Sie in die Ausgabe aufnehmen möchten.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL-Sammlungen]</td>
   <td>Wählen Sie alle Referenzfelder aus, die Sie in die Ausgabe aufnehmen möchten.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Geben Sie die eindeutige Workfront-ID des Datensatzes ein, den das Modul lesen soll.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=". Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **Payload-Version für Ereignisse aktualisieren**

Workfront hat kürzlich eine neue Version seines Ereignisabonnement-Services veröffentlicht. Die neue Version ist keine Änderung der Workfront-API, sondern eine Änderung der Ereignisabonnementfunktion. Dieses Aktionsmodul aktualisiert die für dieses Szenario verwendete Ereignis-Payload-Version.

Weitere Informationen zur neuen Ereignisabonnementversion finden Sie unter [Ereignisabonnementversion](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) in der Workfront-Dokumentation

Ressourcen zum Beibehalten Ihrer Workfront Fusion-Szenarien während des Ereignisabonnement-Upgrades, einschließlich einer Webinar-Aufzeichnung, finden Sie unter [Beibehalten Ihrer Fusion-Szenarien während des Ereignissabonnement-Upgrades V2](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Version]</td> 
   <td> Wählen Sie die Version des Ereignisabonnements aus, die Sie für diese Payload verwenden möchten. </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **Aktualisieren eines Datensatzes**


Dieses Aktionsmodul aktualisiert ein Objekt, z. B. ein Projekt, eine Aufgabe oder ein Problem. Mit dem Modul können Sie auswählen, welche der Objektfelder im Modul verfügbar sind.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des -Objekts und alle zugehörigen Felder zusammen mit allen benutzerdefinierten Feldern und Werten zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Geben Sie die eindeutige Workfront-ID des Datensatzes ein, den Sie aktualisieren möchten.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=". Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Eintrags aus, den das Modul aktualisieren soll.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Wählen Sie die Felder aus, die für die Dateneingabe verfügbar sein sollen. Auf diese Weise können Sie diese Felder verwenden, ohne die nicht benötigten Felder durchscrollen zu müssen. Anschließend können Sie Daten in diese Felder eingeben oder zuordnen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>Wählen Sie die benutzerdefinierten Formulare aus, für die Sie Feldwerte für den neuen Datensatz angeben möchten. Nachdem Sie das Formular ausgewählt haben, geben Sie die Daten für die Felder in diesem Formular ein.<p> Um Feldwerte für ein Formular anzugeben, das Sie in diesem Modul anhängen, fügen Sie die benutzerdefinierte Formular-ID in den Abschnitt Zuzuordnende Felder ein.</td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
> Bei der Eingabe von Text für ein benutzerdefiniertes Feld oder ein [!UICONTROL Hinweis]-Objekt (Kommentar oder Antwort) können Sie HTML-Tags im Feld [!UICONTROL Notizentext] verwenden, um Rich-Text zu erstellen, z. B. fett oder kursiv gedruckten Text.


+++

+++ **[!UICONTROL Eintrag aktualisieren (alt)]**

>[!IMPORTANT]
>
>Dieses Modul wurde durch das Modul Aktualisieren eines Datensatzes ersetzt. Es wird empfohlen, dieses Modul in neuen Szenarien zu verwenden.
>>Vorhandene Szenarien, die dieses Modul verwenden, funktionieren weiterhin erwartungsgemäß. Dieses Modul wird im Mai 2025 aus der Modulauswahl entfernt.

Dieses Aktionsmodul aktualisiert ein Objekt, z. B. ein Projekt, eine Aufgabe oder ein Problem. Mit dem Modul können Sie auswählen, welche der Objektfelder im Modul verfügbar sind.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des -Objekts und alle zugehörigen Felder zusammen mit allen benutzerdefinierten Feldern und Werten zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Geben Sie die eindeutige Workfront-ID des Datensatzes ein, den Sie aktualisieren möchten.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=". Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Eintrags aus, den das Modul aktualisieren soll.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Wählen Sie die Felder aus, die für die Dateneingabe verfügbar sein sollen. Auf diese Weise können Sie diese Felder verwenden, ohne die nicht benötigten Felder durchscrollen zu müssen. Anschließend können Sie Daten in diese Felder eingeben oder zuordnen.</td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Wenn Sie die ID eines Objekts eingeben, können Sie mit der Eingabe des Namens des Objekts beginnen und es dann aus der Liste auswählen. Das Modul gibt dann die entsprechende ID in das Feld ein.
>* Bei der Eingabe von Text für ein benutzerdefiniertes Feld oder ein [!UICONTROL Hinweis]-Objekt (Kommentar oder Antwort) können Sie HTML-Tags im Feld [!UICONTROL Notizentext] verwenden, um Rich-Text zu erstellen, z. B. fett oder kursiv gedruckten Text.

+++

+++ **[!UICONTROL Dokument hochladen]**

Dieses Aktionsmodul lädt ein Dokument in ein Workfront-Objekt, z. B. ein Projekt, eine Aufgabe oder ein Problem. Dieses Modul lädt das Dokument in Blöcken hoch, was den Upload-Prozess für Workfront reibungsloser macht.

Dieses Modul kann größere Dateien als das alte Modul verarbeiten und ist Teil eines schrittweisen Rollouts an Unternehmen mit einem Ultimate Workfront-Paket.

Sie geben den Speicherort für das Dokument, die Datei, die Sie hochladen möchten, und einen optionalen neuen Namen für die Datei an.

Das Modul gibt die ID des Dokuments und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID des zugehörigen Eintrags]</td> 
   <td>Geben Sie die eindeutige Workfront-ID des Datensatzes ein, in den Sie das Dokument hochladen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Verwandter Datensatztyp]</td> 
   <td>Wählen Sie den Typ des Workfront-Datensatzes aus, in den das Modul das Dokument hochladen soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordner-ID]</td> 
   <td>Je nach Typ des zugehörigen Datensatzes müssen Sie möglicherweise eine Ordner-ID eingeben oder zuordnen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Dokument hochladen (alt)]**

Dieses Aktionsmodul lädt ein Dokument in ein Workfront-Objekt, z. B. ein Projekt, eine Aufgabe oder ein Problem. Dadurch wird das gesamte Dokument gleichzeitig hochgeladen.

Sie geben den Speicherort für das Dokument, die Datei, die Sie hochladen möchten, und einen optionalen neuen Namen für die Datei an.

Das Modul gibt die ID des Dokuments und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID des zugehörigen Eintrags]</td> 
   <td>Geben Sie die eindeutige Workfront-ID des Datensatzes ein, in den Sie das Dokument hochladen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Verwandter Datensatztyp]</td> 
   <td>Wählen Sie den Typ des Workfront-Datensatzes aus, in den das Modul das Dokument hochladen soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordner-ID]</td> 
   <td>Je nach Typ des zugehörigen Datensatzes müssen Sie möglicherweise eine Ordner-ID eingeben oder zuordnen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

Hier finden Sie eine Liste der Workfront-Objekttypen, für die Sie dieses Modul in [Workfront-Objekttypen verwenden können, die für jedes Workfront-Modul verfügbar sind](#workfront-object-types-available-for-each-workfront-module).

+++

### Suchvorgänge

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL Lesen verwandter Datensätze]**

Dieses Suchmodul liest Datensätze, die mit der von Ihnen angegebenen Suchabfrage in einem bestimmten übergeordneten Objekt übereinstimmen.

Sie legen fest, welche Felder in der Ausgabe enthalten sein sollen. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des übergeordneten Datensatzes (Workfront-Objekt) aus, dessen verknüpfte Datensätze Sie lesen möchten.</p> <p>Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie in <a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">Workfront-Objekttypen, die für jedes Workfront-Modul verfügbar sind</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID des übergeordneten Eintrags]</td> 
   <td> <p>Geben Sie die ID des übergeordneten Datensatzes ein, dessen verknüpfte Datensätze Sie lesen möchten, oder ordnen Sie sie zu.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=". Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL-Sammlungen]</td> 
   <td>Wählen Sie den Typ des untergeordneten Datensatzes aus, den das Modul lesen soll, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Suche]**

Dieses Suchmodul sucht in einem Objekt in Workfront nach Datensätzen, die mit der angegebenen Suchanfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Datensatzes aus, nach dem das Modul suchen soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Benutzerdefinierte Formularliste]</td> 
   <td> <p>Wählen Sie mindestens ein benutzerdefiniertes Formular aus. Felder aus diesen benutzerdefinierten Formularen stehen für die Suchabfrage zur Verfügung.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ergebnissatz]</td> 
   <td>Wählen Sie eine Option aus, um anzugeben, ob das Modul das erste Ergebnis erhalten soll, das Ihren Suchkriterien entspricht, oder alle Ergebnisse, die damit übereinstimmen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suchkriterienfelder]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie für Ihre Suchkriterien verwenden möchten. Diese Felder sind dann im Dropdown-Menü Suchkriterien verfügbar.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suchkriterien]</td> 
   <td> <p>Geben Sie das Feld ein, nach dem Sie suchen möchten, den Operator, den Sie in Ihrer Abfrage verwenden möchten, und den Wert, nach dem Sie in dem Feld suchen.</p> <p>Hinweis: Verwenden Sie <code>username </code>in Ihren Suchkriterien nicht. Wenn <code>username </code> in eine API-Abfrage an Workfront aufgenommen wird, wird der Benutzer bei Workfront protokolliert und die Suche ist nicht erfolgreich.</p> <p>Hinweis: <code>In</code> und <code>NotIn</code>Arbeiten mit Arrays. Die Eingaben sollten im Array-Format vorliegen.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die in die Ausgabe für dieses Modul aufgenommen werden sollen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL-Verweise]</td> 
   <td>Wählen Sie alle Referenzfelder aus, die Sie in die Suche einbeziehen möchten.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL-Sammlungen]</td> 
   <td>Wählen Sie alle Sammlungen aus, die Sie der Suche hinzufügen möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Suche (veraltet)]**

>[!IMPORTANT]
>
>Dieses Modul wurde durch das Modul Datensätze suchen ersetzt. Es wird empfohlen, dieses Modul in neuen Szenarien zu verwenden.
>>Vorhandene Szenarien, die dieses Modul verwenden, funktionieren weiterhin erwartungsgemäß. Dieses Modul wird im Mai 2025 aus der Modulauswahl entfernt.

Dieses Suchmodul sucht in einem Objekt in Workfront nach Datensätzen, die mit der angegebenen Suchanfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Datensatzes aus, nach dem das Modul suchen soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ergebnissatz]</td> 
   <td>Wählen Sie eine Option aus, um anzugeben, ob das Modul das erste Ergebnis erhalten soll, das Ihren Suchkriterien entspricht, oder alle Ergebnisse, die damit übereinstimmen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suchkriterienfelder]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie für Ihre Suchkriterien verwenden möchten. Diese Felder sind dann im Dropdown-Menü Suchkriterien verfügbar.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suchkriterien]</td> 
   <td> <p>Geben Sie das Feld ein, nach dem Sie suchen möchten, den Operator, den Sie in Ihrer Abfrage verwenden möchten, und den Wert, nach dem Sie in dem Feld suchen.</p> <p>Hinweis: Verwenden Sie <code>username </code>in Ihren Suchkriterien nicht. Wenn <code>username </code> in eine API-Abfrage an Workfront aufgenommen wird, wird der Benutzer bei Workfront protokolliert und die Suche ist nicht erfolgreich.</p> <p>Hinweis: <code>In</code> und <code>NotIn</code>Arbeiten mit Arrays. Die Eingaben sollten im Array-Format vorliegen.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die in die Ausgabe für dieses Modul aufgenommen werden sollen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL-Verweise]</td> 
   <td>Wählen Sie alle Referenzfelder aus, die Sie in die Suche einbeziehen möchten.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL-Sammlungen]</td> 
   <td>Wählen Sie alle Sammlungen aus, die Sie der Suche hinzufügen möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--not visible Jan 6, 2025

+++ **[!UICONTROL Search (Legacy)]**

This search module looks for records in an object in Workfront that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Select an option to specify whether you want the module to get the first result that matches your search criteria or all the results that match it.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the output for this module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Select any reference fields that you want to include in the search.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Select any collections that you want to add to the search.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++-->

## Für jedes Workfront-Modul verfügbare Workfront-Objekttypen

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**Für jedes Workfront-Trigger-Modul verfügbare Objekttypen**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Überwachungseintrag]</th> 
   <th>[!UICONTROL Überwachungsfeld]</th> 
   <th>[!UICONTROL Ereignisse beobachten]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Genehmigungsprozess</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Zuweisung</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Ausgangsbasis</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Abrechnungseintrag </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Abrechnungssatz</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Firma</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dashboard</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dokument</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dokumentenordner</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Dokumentanforderung</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Dokumentversion</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Ausgabe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Ausgabentyp</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Gruppe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Hour</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Stundentyp</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problem</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Wiederholung</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aufgabengebiet</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Journaleintrag</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Meilenstein</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Meilensteinpfad</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Hinweis</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Notiz-Tag</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programm</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projekt</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projektbenutzer</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Korrekturabzug-Genehmigung</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Reservierte Zeit* </td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Bericht</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Risiko</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risikotyp</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Genehmigende Person für Schritt</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aufgabe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Team</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Vorlage</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Vorlagenaufgabe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Arbeitszeittabelle</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Benutzerin bzw. Benutzer</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Update</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Für jedes Workfront-Aktionsmodul verfügbare Objekttypen**

>[!NOTE]
>
>Das [!UICONTROL Dokument herunterladen]-Modul ist nicht in dieser Tabelle enthalten, da Workfront-Objekttypen nicht Teil seiner Konfiguration sind.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Datensatz erstellen]</th> 
   <th>[!UICONTROL Datensatz aktualisieren]</th> 
   <th>[!UICONTROL Datensatz löschen]</th> 
   <th>[!UICONTROL Dokument hochladen]</th> 
   <th>[!UICONTROL Datensatz lesen]</th> 
   <th>[!UICONTROL Benutzerdefinierter API-Aufruf]</th> 
   <th>[!UICONTROL Misc-Aktion]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Genehmigungsprozess</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Zuweisung</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Ausgangsbasis</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
   <tr> 
   <td>Abrechnungseintrag</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Abrechnungssatz</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Firma</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dokument</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dokumentenordner</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dokumentversion</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Wechselkurs</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Ausgabe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Ausgabentyp</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Externes Dokument</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Gruppe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Hour</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Stundentyp</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problem</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Wiederholung</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aufgabengebiet</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Journaleintrag</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Meilenstein</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Meilensteinpfad</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Hinweis</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Notiz-Tag</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programm</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projekt</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projektbenutzer</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Reservierte Zeit* </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risiko</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risikotyp</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Genehmigende Person für Schritt</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aufgabe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Team</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Vorlage</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Vorlagenaufgabe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Arbeitszeittabelle</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Benutzerin bzw. Benutzer</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Update</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Für jedes Workfront-Suchmodul verfügbare Objekttypen**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Suche]</th> 
   <th>[!UICONTROL Verwandte Einträge lesen]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Genehmigungsprozess</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Zuweisung</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Abrechnungseintrag</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Abrechnungssatz</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Firma</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dokument</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dokumentenordner</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dokumentversion</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Ausgabe</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Ausgabentyp</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Gruppe</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Hour</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Stundentyp</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problem</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Wiederholung</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aufgabengebiet</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Journaleintrag</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Meilenstein</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Meilensteinpfad</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Hinweis</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Notiz-Tag</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programm</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Projekt</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projektbenutzer</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Reservierte Zeit* </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risiko</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risikotyp</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Genehmigende Person für Schritt</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Aufgabe</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Team</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Vorlage</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Vorlagenaufgabe</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Arbeitszeittabelle</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Benutzerin bzw. Benutzer</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Benutzerdelegierung</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

Es wird empfohlen, dies zu überprüfen, um sicherzustellen, dass es so funktioniert, wie Sie es erwarten würden.

+++

## Filter für Ereignisabonnements in den Modulen Workfront [!UICONTROL Ereignisse beobachten]

>[!NOTE]
>
>* Es wird dringend empfohlen, Ereignisabonnementfilter in Ihren Modulen [!UICONTROL Ereignisse beobachten] zu verwenden.
>
>* Workfront hat kürzlich eine neue Version seines Ereignisabonnement-Services veröffentlicht. Die neue Version ist keine Änderung der Workfront-API, sondern eine Änderung der Ereignisabonnementfunktion. Dieses Aktionsmodul aktualisiert die für dieses Szenario verwendete Ereignis-Payload-Version.
>
>   Weitere Informationen zur neuen Ereignisabonnementversion finden Sie unter [Ereignisabonnementversion](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) in der Workfront-Dokumentation
>
>   Ressourcen zum Beibehalten Ihrer Workfront Fusion-Szenarien während des Ereignisabonnement-Upgrades, einschließlich einer Webinar-Aufzeichnung, finden Sie unter [Beibehalten Ihrer Fusion-Szenarien während des Ereignissabonnement-Upgrades v2(https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182)].

Das Workfront-Modul [!UICONTROL Ereignisse beobachten] erstellt Trigger, die auf einem Webhook basieren, der ein Ereignisabonnement in der Workfront-API erstellt. Das Ereignisabonnement ist ein Datensatz, der bestimmt, welche Ereignisse an den Webhook gesendet werden. Wenn Sie beispielsweise ein Modul [!UICONTROL Ereignisse beobachten] einrichten, das auf Probleme überwacht, sendet das Ereignisabonnement nur Ereignisse, die mit Problemen in Zusammenhang stehen.

Durch die Verwendung von Ereignisabonnementfiltern können Fusion-Benutzer Ereignisabonnements erstellen, die besser für ihre Anwendungsfälle geeignet sind. Sie können beispielsweise ein Ereignisabonnement in der Workfront-API einrichten, um nur Probleme, die sich in einem bestimmten Projekt befinden, an den Webhook zu senden, um sicherzustellen, dass das Modul [!UICONTROL Ereignisse beobachten] nur für Probleme in diesem Projekt Trigger erstellt. Die Möglichkeit, engere Trigger zu erstellen, verbessert das Szenario-Design, indem die Anzahl der irrelevanten Trigger reduziert wird.

Dies unterscheidet sich vom Einrichten eines Filters im Workfront Fusion-Szenario. Ohne einen Ereignisabonnementfilter erhält Ihr Webhook alle Ereignisse, die mit dem ausgewählten Objekttyp zusammenhängen. Die meisten dieser Ereignisse wären für das Szenario irrelevant und müssen herausgefiltert werden, bevor das Szenario fortgesetzt werden kann.

Die folgenden Operatoren sind im Filter Workfront > Ereignisse beobachten verfügbar:

* Gleich
* Ungleich
* Größer als
* Kleiner als
* Größer oder gleich
* Kleiner oder gleich
* Enthält
* Vorhanden
   * Dieser Operator benötigt keinen Wert, und das Wertfeld ist nicht vorhanden.
* existiert nicht
   * Dieser Operator benötigt keinen Wert, und das Wertfeld ist nicht vorhanden.
* Geändert
   * Dieser Operator benötigt keinen Wert, und das Wertfeld ist nicht vorhanden.
   * Dieser Operator ignoriert das Feld Status .
   * Wählen Sie bei Verwendung von `Changed` **Nur aktualisierte Ereignisse** im Feld **Herkunft**.

>[!IMPORTANT]
>
>Filter in vorhandenen Workfront-Webhooks können nicht bearbeitet werden. Um verschiedene Filter für Workfront-Ereignisabonnements einzurichten, entfernen Sie den aktuellen Webhook und erstellen Sie einen neuen.

>[!INFO]
>
>**Beispiel** Nehmen wir ein Szenario an, in dem neue Probleme verarbeitet werden, die einem bestimmten Benutzer, Ana, zugewiesen sind.
>
>### Filtern von Ereignissen mithilfe eines Ereignisabonnement-Filters (empfohlen)
>
>Mit dem Ereignisfilter können Sie den Webhook so einrichten, dass der Trigger für das Szenario erstellt wird, wenn ein Problem Ana zugewiesen wird, wenn das Problem erstellt wird. Ana hat die userID b378489d8f7cd3cee0539260720a84b7.
>
>![Ereignisfilter](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>Wenn an einem Tag 100 Probleme erstellt werden, aber nur zwei davon Ana zugewiesen sind, wird das Szenario zweimal ausgeführt.
>
>### Filtern von Ereignissen innerhalb des Szenarios (nicht empfohlen)
>
>Um Ereignisse so zu filtern, dass nur Ana zugewiesene Probleme verarbeitet werden, können Sie nach dem Modul [!UICONTROL Ereignisse beobachten] einen Filter erstellen.
>
>![Ohne Ereignisfilter](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>Wenn an einem Tag 100 Probleme erstellt werden, aber nur zwei davon Ana zugewiesen sind, wird das Szenario 100-mal ausgeführt. 98 der Ausführungen würden am Trigger anhalten, aber das Filtermodul verbraucht weiterhin Daten und führt Vorgänge in allen Ausführungen aus.

Weitere Informationen zu Workfront-Ereignisabonnements finden Sie unter [FAQs - Ereignisabonnements](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq).

Weitere Informationen zu Webhooks finden Sie unter [Instant Trigger (Webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/references/modules/webhooks-reference.md)

Weitere Informationen zu Filtern in Szenarien finden Sie unter [Hinzufügen eines Filters zu einem Szenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).
