---
title: Adobe Workfront-Module
description: Mit dem Adobe Workfront-Connector von Adobe Workfront Fusion können Sie Ihre Prozesse in Workfront automatisieren. Wenn Sie über eine Workfront Fusion for Work Automation and Integration-Lizenz verfügen, können Sie damit auch eine Verbindung zu Anwendungen und Services von Drittanbietern herstellen.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: ab12dbf0dbad25a8300eb1201fa3e0fde9148acc
workflow-type: tm+mt
source-wordcount: '7366'
ht-degree: 99%

---

# Adobe Workfront-Module

>[!IMPORTANT]
>
>Dieser Artikel enthält Anweisungen zur neuen Version des Workfront-Connectors, die am 22. Oktober 2025 veröffentlicht wurde. Dieser neue Connector spiegelt an der Workfront-API vorgenommene Änderungen wider.
>
>Der neue Connector heißt „Workfront“, der zuvor verfügbare Connector „Workfront (Legacy)“.
>
>Wir empfehlen:
>
>* die Verwendung des neuen Connectors beim Erstellen oder Aktualisieren eines Szenarios,
>* die Aktualisierung vorhandener Module auf den neuen Connector.
>
>Der Workfront-Legacy-Connector verwendet die Workfront-API-Version 20, die voraussichtlich mit der Version 28.4 (April 2028) eingestellt wird. Die Module im Legacy-Connector funktionieren bis zu diesem Zeitpunkt weiter.
>
>Anweisungen zum Aktualisieren vorhandener Module finden Sie im Artikel „Aktualisieren eines Moduls auf eine neue Version“ unter [Aktualisieren eines Workfront-Moduls auf eine neue Version](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md).
>
>Informationen dazu, warum mitunter ein neuer Connector erforderlich ist, finden Sie unter [Überblick über die APIs in Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md).

Mit dem Adobe Workfront-Connector von Adobe Workfront Fusion können Sie Ihre Prozesse in Workfront automatisieren. Sie können Workfront auch mit anderen Anwendungen und Services verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Erstellen von Szenarios: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Verbinden von Workfront mit Workfront Fusion

Der Workfront-Connector nutzt OAuth 2.0, um eine Verbindung zu Workfront herzustellen.

Sie können direkt aus einem Workfront Fusion-Modul heraus eine Verbindung zu Ihrem Workfront-Konto herstellen.

* [Herstellen einer Verbindung mit Workfront per Client-ID und Client-Geheimnis](#connect-to-workfront-using-client-id-and-client-secret)
* [Herstellen einer Verbindung mit Workfront per Server-zu-Server-Verbindung](#connect-to-workfront-using-a-server-to-server-connection)

### Herstellen einer Verbindung mit Workfront per Client-ID und Client-Geheimnis

1. Klicken Sie in einem beliebigen Adobe Workfront-Modul neben dem Feld „Verbindung“ auf **Hinzufügen**.
1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungstyp]</td>
        <td>
          <p>Wählen Sie <b>Adobe Workfront-Authentifizierungsverbindung </b> aus.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für die neue Verbindung ein. </p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre Workfront-Client-ID ein. Diese finden Sie im Workfront-Bereich „Setup“ unter „OAuth2-Programme“. Öffnen Sie die Anwendung, zu der eine Verbindung hergestellt werden soll, um die Client-ID anzuzeigen.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr Workfront-Client-Geheimnis ein. Diese finden Sie im Workfront-Bereich „Setup“ unter „OAuth2-Programme“. Wenn Sie in Workfront kein Client-Geheimnis für Ihre OAuth2-Anwendung besitzen, können Sie ein anderes generieren. Anweisungen hierzu finden Sie in der Workfront-Dokumentation.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentifizierungs-URL]</td>
        <td>Hier kann der Standardwert bleiben. Sie können aber auch die URL Ihrer Workfront-Instanz gefolgt von <code>/integrations/oauth2</code> eingeben. <p>Beispiel: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host-Präfix]</td>
        <td>In den meisten Fällen sollte dieser Wert auf <code>origin</code> gesetzt werden. 
      </tr>
    </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

   Wenn Sie nicht bei Workfront angemeldet sind, werden Sie zu einem Anmeldebildschirm weitergeleitet. Nach der Anmeldung können Sie die Verbindung zulassen.

>[!NOTE]
>
>* OAuth 2.0-Verbindungen zur Workfront-API sind nicht mehr auf API-Schlüssel angewiesen.
>* Um eine Verbindung zu einer Workfront-Sandbox-Umgebung herzustellen, müssen Sie in dieser Umgebung eine OAuth2-Anwendung erstellen und dann die Client-ID und das Client-Geheimnis, die von dieser Anwendung generiert wurden, in Ihrer Verbindung verwenden.

### Herstellen einer Verbindung mit Workfront per Server-zu-Server-Verbindung

1. Klicken Sie in einem beliebigen Adobe Workfront-Modul neben dem Feld „Verbindung“ auf **Hinzufügen**.
1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungstyp]</td>
        <td>
          <p>Wählen Sie <b>Adobe Workfront-Server-zu-Server-Verbindung</b> aus.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für die neue Verbindung ein. </p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instanzname]</td>
        <td>
          <p>Geben Sie den Namen Ihrer Instanz ein (auch als Domain bezeichnet).</p><p>Wenn Ihre URL z. B. <code>https://example.my.workfront.com</code> lautet, geben Sie <code>example</code> ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instanzen-Lane]</td>
        <td>
          <p>Geben Sie den Umgebungstyp für die Verbindung ein.</p><p>Wenn Ihre URL z. B. <code>https://example.my.workfront.com</code> lautet, geben Sie <code>my</code> ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre Workfront-Client-ID ein. Diese finden Sie im Workfront-Bereich „Setup“ unter „OAuth2-Programme“. Öffnen Sie die Anwendung, zu der eine Verbindung hergestellt werden soll, um die Client-ID anzuzeigen.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr Workfront-Client-Geheimnis ein. Diese finden Sie im Workfront-Bereich „Setup“ unter „OAuth2-Programme“. Wenn Sie in Workfront kein Client-Geheimnis für Ihre OAuth2-Anwendung besitzen, können Sie ein anderes generieren. Anweisungen hierzu finden Sie in der Workfront-Dokumentation.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Bereiche]</td>
        <td>Geben Sie alle zutreffenden Bereiche für diese Verbindung ein.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host-Präfix]</td>
        <td>In den meisten Fällen sollte dieser Wert auf <code>origin</code> gesetzt werden. 
      </tr>
    </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

   Wenn Sie nicht bei Workfront angemeldet sind, werden Sie zu einem Anmeldebildschirm weitergeleitet. Nach der Anmeldung können Sie die Verbindung zulassen.

>[!NOTE]
>
>* OAuth 2.0-Verbindungen zur Workfront-API sind nicht mehr auf API-Schlüssel angewiesen.
>* Um eine Verbindung zu einer Workfront-Sandbox-Umgebung herzustellen, müssen Sie in dieser Umgebung eine OAuth2-Anwendung erstellen und dann die Client-ID und das Client-Geheimnis, die von dieser Anwendung generiert wurden, in Ihrer Verbindung verwenden.

## Workfront-Module und ihre Felder

Beim Konfigurieren von Workfront-Modulen werden in Workfront Fusion die unten aufgeführten Felder angezeigt. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere Workfront-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Wenn in einem Workfront-Modul nicht die aktuellen Felder angezeigt werden, kann dies an Caching-Problemen liegen. Warten Sie in einem solchen Fall eine Stunde und versuchen Sie es dann erneut.
>* Ein Status-Code „HTTP 429“ von Adobe Workfront sollte zu keinen Deaktivierungen führen, sondern vielmehr eine kurze Ausführungspause im Szenario auslösen.

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL Ereignisse überwachen]**

Dieses Auslösermodul führt ein Szenario in Echtzeit aus, wenn Objekte eines bestimmten Typs in Workfront hinzugefügt, aktualisiert oder gelöscht werden.

Das Modul zeigt alle Ereignisabonnements an, die mit dem Webhook verbunden sind. Dazu gehören Ereignisabonnements, die über Fusion erstellt wurden, sowie Ereignisabonnements, die direkt über die API erstellt wurden. Diese Ereignisabonnementansicht ist in der Legacy-Version des Moduls „Ereignisse überwachen“ nicht verfügbar.

Das Modul gibt alle Standardfelder zurück, die mit dem Eintrag verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

1. Klicken Sie rechts neben dem Feld **Webhook** auf **[!UICONTROL Hinzufügen]**.

1. Konfigurieren Sie den Webhook im angezeigten Feld **[!UICONTROL Hook hinzufügen]**.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Webhook-Name]</td> 
      <td>Geben Sie einen Namen für den Webhook ein.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Verbindung]</td> 
      <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Eintragstyp]</td> 
      <td>Wählen Sie den Typ des Workfront-Eintrags aus, der vom Modul überwacht werden soll.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Status]</td> 
      <td>Wählen Sie aus, ob der alte oder der neue Status überwacht werden soll.<ul><li><p><b>[!UICONTROL Neuer Status]</b></p><p>Lösen Sie ein Szenario aus, wenn sich der Eintrag <b>in</b> einen bestimmten Wert ändert.</p><p>Wenn beispielsweise der Status auf „[!UICONTROL Neuer Status]“ und der Filter auf „[!UICONTROL Status] [!UICONTROL gleich] [!UICONTROL In Arbeit]“ gesetzt ist, löst der Webhook beim Wechsel des [!UICONTROL Status] zu „[!UICONTROL In Arbeit]“ ein Szenario aus. Dies gilt unabhängig vom vorherigen Status. </p></li><li><p><b>[!UICONTROL Alter Status]</b></p><p>Lösen Sie ein Szenario aus, wenn sich der Eintrag <b>von</b> einem bestimmten Wert ändert.</p><p>Wenn beispielsweise der Status auf „[!UICONTROL Alter Status]“ und der Filter auf „[!UICONTROL Status] [!UICONTROL gleich] [!UICONTROL In Arbeit]“ gesetzt ist, löst der Webhook beim Wechsel eines [!UICONTROL Status] vom Typ „[!UICONTROL In Arbeit]“ zu einem anderen Status ein Szenario aus. </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Ereignisfilter]</p> </td> 
      <td> <p>Sie können Filter festlegen, um nur auf Einträge zu achten, die die von Ihnen ausgewählten Kriterien erfüllen.</p> <p>Geben Sie für jeden Filter Folgendes an: das Feld, das vom Filter ausgewertet werden soll, den Operator und den Wert, den der Filter zulassen soll. Sie können mehr als einen Filter verwenden, indem Sie UND-Regeln hinzufügen.</p> <p><b>HINWEIS</b>: Filter in vorhandenen Workfront-Webhooks können nicht bearbeitet werden. Um verschiedene Filter für Workfront-Ereignisabonnements einzurichten, entfernen Sie den aktuellen Webhook und erstellen Sie einen neuen.</p> <p>Weitere Informationen zu Ereignisfiltern finden Sie in diesem Artikel unter <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Ereignisabonnementfilter in den Modulen unter „Workfront“ &gt; „[!UICONTROL Ereignisse überwachen]“</a>.</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>Von dieser Verbindung stammende Ereignisse ausschließen</td> 
      <td>Aktivieren Sie diese Option, um Ereignisse auszuschließen, die mit dem von diesem Auslösermodul verwendeten Connector erstellt oder aktualisiert wurden. Dadurch lassen sich Situationen verhindern, in denen ein Szenario von sich selbst ausgelöst und in einer Endlosschleife wiederholt wird.<p><b>HINWEIS</b>: Der Eintragstyp „Zuweisung“ umfasst diese Option nicht.</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Eintragsursprung]</td> 
      <td>
       <p>Wählen Sie aus, ob das Szenario eine Überwachung anhand der Option „[!UICONTROL Nur neue Einträge]“, „[!UICONTROL Nur aktualisierte Einträge]“, „[!UICONTROL Neue und aktualisierte Einträge]“ oder „[!DNL Deleted Records Only]“ durchführen soll.</p>
       <p><b>HINWEIS</b>: Wenn Sie die Option „[!UICONTROL Neue und aktualisierte Einträge]“ auswählen, werden im Rahmen der Webhook-Erstellung zwei Ereignisabonnements (für dieselbe Webhook-Adresse) erstellt.</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

Nachdem der Webhook erstellt wurde, können Sie die Adresse des Endpunkts anzeigen, an den Ereignisse gesendet werden.

Weitere Informationen finden Sie in der Workfront-Dokumentation im Artikel „Ereignisabonnement-API“ unter [Beispiele für Ereignis-Payloads](https://experienceleague.adobe.com/de/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads).

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Feld überwachen]**

Dieses Auslösermodul führt ein Szenario aus, wenn ein von Ihnen angegebenes Feld aktualisiert wird. Das Modul gibt sowohl den alten als auch den neuen Wert des angegebenen Felds zurück. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Eintrags aus, der vom Modul überwacht werden soll.</p> <p>Wählen Sie beispielsweise „[!UICONTROL Aufgabe]“ aus, wenn die Ausführung des Szenarios bei jeder Aktualisierung eines Eintragsfelds in einer Aufgabe gestartet werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Feld]</td> 
   <td>Wählen Sie das Feld aus, das vom Modul auf Aktualisierungen überwacht werden soll. Diese Felder spiegeln die Felder wider, die von der Workfront-Administration zum Tracking eingerichtet wurden.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Objektfelder aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Beschränkung]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Eintrag überwachen]**

Dieses Auslösermodul führt ein Szenario aus, wenn Objekte eines bestimmten Typs hinzugefügt und/oder aktualisiert werden. Das Modul gibt alle Standardfelder zurück, die mit dem Eintrag bzw. den Einträgen verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

In der Ausgabe gibt das Modul an, ob es sich jeweils um einen neuen oder aktualisierten Eintrag handelt.

Einträge, die seit der letzten Szenario-Ausführung hinzugefügt und aktualisiert wurden, werden als neue Einträge zurückgegeben.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Wählen Sie aus, ob das Szenario eine Überwachung anhand der Option „[!UICONTROL Nur neue Einträge]“, „[!UICONTROL Nur aktualisierte Einträge]“ oder „[!UICONTROL Neue und aktualisierte Einträge]“ durchführen soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Eintrags aus, der vom Modul überwacht werden soll.</p> <p>Wenn das Szenario beispielsweise bei jeder Erstellung eines neuen Projekts starten soll, wählen Sie „[!UICONTROL Projekt]“ aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Referenz]</td> 
   <td> <p>Wählen Sie die Referenzfelder aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Sammlungsfelder aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optionaler Filter]</td> 
   <td> <p>(Fortgeschritten) Geben Sie eine API-Code-Zeichenfolge ein, um zusätzliche Parameter oder zusätzlichen Code zum Verfeinern Ihrer Kriterien zu definieren. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschränkung]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

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

* Problem in Projekt konvertieren
* Problem in Aufgabe konvertieren
* Aufgabe in Projekt konvertieren

>[!NOTE]
>
>Seit Juli 2024 können benutzerdefinierte Formulare beim Konvertieren eines Objekts einbezogen werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Objekttyp]</td> 
   <td> <p>Wählen Sie den Typ des Objekts aus, das konvertiert werden soll. Dies entspricht dem Objekttyp vor der Konvertierung.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Konvertieren in]</td> 
   <td>Wählen Sie das Objekt aus, in das konvertiert werden soll. Dies entspricht dem Objekttyp nach der Konvertierung.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL &lt;Object&gt;-ID]</td> 
   <td> <p>Geben Sie die ID des Objekts ein. </p> <p>Hinweis: Bei der Eingabe der ID eines Objekts können Sie mit der Eingabe des Namens des Objekts beginnen und es dann aus der Liste auswählen. Das Modul trägt daraufhin die entsprechende ID in das Feld ein.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Vorlagen-ID]</td> 
   <td> <p>Wenn Sie in ein Projekt konvertieren, wählen Sie die Vorlagen-ID aus, die für das Projekt verwendet werden soll.</p> <p>Hinweis: Bei der Eingabe der ID eines Objekts können Sie mit der Eingabe des Namens des Objekts beginnen und es dann aus der Liste auswählen. Das Modul trägt daraufhin die entsprechende ID in das Feld ein.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Benutzerdefinierte Formulare]</td> 
   <td>Wählen Sie alle benutzerdefinierten Formulare aus, die dem neu konvertierten Objekt hinzugefügt werden sollen, und geben Sie dann Werte für die Felder der benutzerdefinierten Formulare ein.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Optionen]</td> 
   <td> <p>Aktivieren Sie beim Konvertieren des Objekts alle gewünschten Optionen. Je nachdem, in welches Objekt bzw. von welchem Objekt konvertiert werden soll, sind unterschiedliche Optionen verfügbar.</p> </td> 
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

+++ **[!UICONTROL Eintrag erstellen]** 

Dieses Aktionsmodul erstellt ein Objekt, z. B. ein Projekt, eine Aufgabe oder ein Problem in Workfront, und ermöglicht das Hinzufügen eines benutzerdefinierten Formulars zum neuen Objekt. Mit dem Modul können Sie auswählen, welche Objektfelder im Modul verfügbar sind.

Geben Sie die ID des Eintrags an.

Das Modul gibt daraufhin die ID des Eintrags und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Achten Sie darauf, die Mindestanzahl von Eingabefeldern anzugeben. Beim Erstellen eines Problems müssen Sie beispielsweise im Feld „Projekt-ID“ eine gültige übergeordnete Projekt-ID angeben, um die Problemstelle in Workfront anzugeben. Sie können das Zuordnungs-Panel verwenden, um diese Informationen aus einem anderen Modul in Ihrem Szenario zuzuordnen. Eine manuelle Eingabe ist ebenfalls möglich. Geben Sie hierzu den Namen ein und wählen Sie dann diesen aus der Liste aus.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Eintrags aus, der vom Modul erstellt werden soll.</p> <p>Wenn Sie beispielsweise ein Projekt erstellen möchten, wählen Sie in der Dropdown-Liste die Option „[!UICONTROL Projekt]“ aus.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Felder zum Zuordnen auswählen]</td> 
   <td> <p>Wählen Sie die Felder aus, die zur Dateneingabe verfügbar sein sollen. Auf diese Weise können Sie diese Felder verwenden, ohne durch nicht benötigte Felder scrollen zu müssen. Anschließend können Sie Daten in diese Felder eingeben oder darin zuordnen.</p> <p>Verwenden Sie für Felder in benutzerdefinierten Formularen das Feld <b>[!UICONTROL Benutzerdefiniertes Formular anfügen]</b>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Benutzerdefiniertes Formular anfügen]</td> 
   <td>Wählen Sie alle benutzerdefinierten Formulare aus, die dem neuen Objekt hinzugefügt werden sollen, wählen Sie die Felder für die Eingabe von Werten aus und geben Sie dann Werte für diese Felder ein bzw. ordnen Sie diese zu.</td> 
  </tr> 
 </tbody> 
</table>

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Bei der Eingabe der ID eines Objekts können Sie mit der Eingabe des Namens des Objekts beginnen und es dann aus der Liste auswählen. Das Modul trägt daraufhin die entsprechende ID in das Feld ein.
>* Bei der Eingabe von Text für ein benutzerdefiniertes Feld oder ein Objekt vom Typ [!UICONTROL Notiz] (Kommentar oder Antwort) können Sie mithilfe von HTML-Tags im Feld [!UICONTROL Notizentext] Rich-Text erstellen, z. B. fett oder kursiv formatierten Text.
>



>[!NOTE]
>
>Benutzende werden im Status „Deaktiviert“ und „Ausstehende Genehmigungen“ erstellt. Wenn Ihre Organisation zur Adobe Admin Console migriert wurde und das Zeichen „Ausstehende Genehmigungen“ nicht innerhalb weniger Minuten verschwindet, können Sie die entsprechende Person genehmigen.
>
>* **Lösen von Problemen bei einzelnen Benutzenden**
>
>      In der Benutzerliste können Sie Probleme bei einzelnen Benutzenden lösen.
>
>      1. Wählen Sie die Benutzenden in der Benutzerliste aus.
>      1. Klicken Sie auf das Dreipunkt-Menü in der Listenüberschrift.
>      1. Wählen Sie **Genehmigen** aus.
>      1. Aktualisieren Sie die Seite nach einigen Minuten.
>
>* **Lösen von Problemen bei Benutzenden, die in großer Anzahl hinzugefügt wurden**
>
>   Um Probleme bei Benutzenden zu lösen, die in großer Anzahl hinzugefügt wurden, können Sie den Batch von Benutzenden direkt in der Adobe Admin Console hinzufügen.
>
>   Anweisungen finden Sie unter [Verwalten mehrerer Benutzender | CSV-Massen-Upload](https://helpx.adobe.com/de/enterprise/using/bulk-upload-users.html) in der Adobe-Dokumentation.

+++

<!--

+++ **[!UICONTROL Create Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Create a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module creates an object, such as a project, task, or issue in Workfront. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

Make sure you provide the minimum number of input fields. For example, if you want to create an issue, you need to provide a valid parent project ID in the Project ID field to indicate where the issue should live in Workfront. You can use the mapping panel to map this information from another module in your scenario, or you can enter it manually by typing in the name and then selecting it from the list.

This module does not attach custom forms when creating the object. To attach custom forms while creating an object, use the [!UICONTROL Create a record (attaching custom forms)] module.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to create.</p> <p>For example, if you want to create a Project, select [!UICONTROL Project] from the dropdown list.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL Benutzerdefinierter API-Aufruf]**

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die Workfront-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, was über die anderen Workfront-Module nicht möglich ist.

Das Modul enthält folgende Informationen:

* **[!UICONTROL Status-Code]** (Zahl): Gibt den Erfolg oder Misserfolg Ihrer HTTP-Anfrage an. Hierbei handelt es sich um Standard-Codes, die Sie im Internet recherchieren können.
* **[!UICONTROL Header]** (Objekt): Ein ausführlicherer Kontext für die Antwort/den Status-Code, der sich nicht auf den Ausgabetext bezieht. Nicht alle Header, die in einem Antwort-Header angezeigt werden, sind Antwort-Header. Einige sind also möglicherweise nicht nützlich für Sie.

  Die Antwort-Header hängen von der beim Konfigurieren des Moduls ausgewählten HTTP-Anfrage ab.

* **[!UICONTROL Text]** (Objekt): Je nach HTTP-Anfrage, die Sie beim Konfigurieren des Moduls ausgewählt haben, erhalten Sie möglicherweise bestimmte Daten zurück. Diese Daten, etwa die Daten aus einer GET-Anfrage, sind in diesem Objekt enthalten.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Geben Sie einen Pfad relativ zu<code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code> ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API-Version]</td> 
   <td>Wählen Sie die Version der Workfront-API aus, die vom Modul verwendet werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden in Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Header]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Dadurch wird der Content-Typ der Anfrage bestimmt.</p> <p>Beispiel:<code> {"Content-type":"application/json"}</code></p> <p>Hinweis: Wenn Fehler auftreten und es schwierig ist, deren Ursprung zu ermitteln, sollten Sie die Header anhand der Workfront-Dokumentation ändern. Wenn Ihr benutzerdefinierter API-Aufruf einen 422-HTTP-Anfragefehler zurückgibt, versuchen Sie es dem Header <code>"Content-Type":"text/plain"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> <p>Tipp: Es wird empfohlen, Informationen mittels JSON-Text und nicht als Abfrageparameter zu senden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p>Fügen Sie den Textinhalt für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrem JSON-Objekt verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Eintrag löschen]**

Dieses Aktionsmodul löscht ein Objekt, z. B. ein Projekt, eine Aufgabe oder ein Problem in Workfront.

Geben Sie die ID des Eintrags an.

Das Modul gibt daraufhin die ID des Eintrags und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Löschen erzwingen]</td> 
   <td>Aktivieren Sie diese Option, um sicherzustellen, dass der Eintrag gelöscht wird, selbst wenn die Workfront-Benutzeroberfläche eine Löschbestätigung anfordert.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Asynchron löschen]</td> 
   <td>Aktivieren Sie diese Option, um asynchrone Löschvorgänge durch das Modul zuzulassen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>Geben Sie die eindeutige Workfront-ID des zu löschenden Eintrags ein.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=“. Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Eintragstyp]</td> 
   <td>Wählen Sie den Typ des Workfront-Eintrags aus, der vom Modul gelöscht werden soll.</td> 
  </tr> 
 </tbody> 
</table>

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>Wir empfehlen die folgende Szenariokonfiguration, um zu verhindern, dass Einträge aufgrund asynchroner Vorgänge nicht gelöscht werden.
>
>1. Löschen Sie den Eintrag synchron.
>1. Fügen Sie dem Modul „Eintrag löschen“ Anweisungen zur Fehlerbehandlung hinzu, um den Fehler zu ignorieren, der durch den Timeout nach 40 Sekunden verursacht wird.


+++

+++ **[!UICONTROL Dokument herunterladen]**

Dieses Aktionsmodul lädt ein Dokument von Workfront herunter.

Geben Sie die ID des Eintrags an.

Das Modul gibt den Inhalt, den Dateinamen, die Dateierweiterung und die Dateigröße des Dokuments zurück. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dokument-ID]</td> 
   <td> <p>Ordnen Sie die eindeutige Workfront-ID des Dokuments zu, das vom Modul heruntergeladen werden soll, oder geben Sie diese manuell ein.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=“. Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

+++

### **Vorsignierte Datei-URL abrufen**

Dieses Aktionsmodul ruft vorsignierte Datei-URLs ab, die später von anderen APIs verwendet werden können.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dokument-ID]</td> 
   <td> <p>Ordnen Sie die eindeutige Workfront-ID des Dokuments zu, für das eine vorsignierte URL abgerufen werden soll, oder geben Sie diese manuell ein.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=“. Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zeit bis URL-Ablauf]</td> 
   <td> <p>Geben Sie die Anzahl der Minuten ein, die diese URL existiert, bevor sie abläuft, oder ordnen Sie diesen Wert zu. Der Standardwert ist 1 Minute.</p><p>Um diesen Wert zu ändern, muss der entsprechende Parameter vom Workfront Fusion-Team aktiviert werden. Ist er nicht aktiviert, bleibt der Wert unabhängig von der eingegebenen Zahl 1 Minute.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++ **[!UICONTROL Sonstige Aktion]**

Mit diesem Aktionsmodul können Sie Aktionen für die API durchführen.

>[!NOTE]
>
>Ab Juli 2024 umfasst die Aktion `convertToProject` das Feld `copyCategories`. Beim Festlegen von `TRUE` werden alle benutzerdefinierten Formulare in das Projekt eingeschlossen, in das das Problem konvertiert wird.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Eintrags aus, mit dem das Modul interagieren soll.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Aktion]</td> 
   <td> <p>Wählen Sie die Aktion aus, die vom Modul ausgeführt werden soll.</p> <p>Abhängig von Ihrer Auswahl unter „[!UICONTROL Eintragstyp]“ und „[!UICONTROL Aktion]“ müssen Sie möglicherweise zusätzliche Felder ausfüllen. Bei bestimmten Kombinationen dieser beiden Einstellungen muss unter Umständen nur eine Eintrags-ID angegeben werden, während für andere (z. B. die Option „Projekt“ unter <strong>[!UICONTROL Eintragstyp]</strong> und die Option „[!UICONTROL Vorlage anfügen]“ unter <strong>[!UICONTROL Aktion]</strong>) zusätzliche Informationen (wie eine Objekt-ID und eine Vorlagen-ID) erforderlich sind.</p><p>Die für einige Aktionen verfügbaren Optionen finden Sie in diesem Artikel unter <a href="#misc-action-options" class="MCXref xref">Sonstige Aktionsoptionen</a>.</p> <p>Weitere Informationen zu den einzelnen Feldern finden Sie in der <a href="http://developer.workfront.com/">Workfront-Entwicklerdokumentation</a>. <p><strong>Hinweis</strong>: Die Site mit der Entwicklerdokumentation enthält nur Informationen bis zur API-Version 14, sie liefert aber dennoch wertvolle Informationen für API-Aufrufe. </p> 
    <ol> 
     <li value="1"> <p>Wählen Sie im linken Navigationsbereich der Workfront-Entwicklerdokumentation den Eintragstyp aus. Für folgende Typen sind eigene Seiten vorhanden:</p> 
      <ul> 
       <li> <p>[!UICONTROL Projekte]</p> </li> 
       <li> <p>[!UICONTROL Aufgaben]</p> </li> 
       <li> <p>[!UICONTROL Probleme]</p> </li> 
       <li> <p>[!UICONTROL Benutzende]</p> </li> 
       <li> <p>[!UICONTROL Dokumente]</p> </li> 
      </ul> <p>Wählen Sie für alle anderen Eintragstypen das unterste Thema zu <b>[!UICONTROL anderen Objekten und Endpunkten]</b> aus und suchen Sie den Eintragstyp auf den alphabetisch sortierten Seiten.</p> </li> 
     <li value="2"> <p>Suchen Sie (über den Tastaturbefehl Strg+F bzw. Befehlstaste+F) auf der Seite des entsprechenden Eintragstyps nach der Aktion.</p> </li> 
     <li value="3"> <p>Lassen Sie sich Beschreibungen für die verfügbaren Felder unter der ausgewählten Aktion anzeigen.</p> </li> 
    </ol> <p>Hinweis:  <p>Beim Erstellen eines Korrekturabzugs über das Workfront-Modul „[!UICONTROL Sonstige Aktion]“ empfiehlt es sich, einen Korrekturabzug ohne erweiterte Optionen zu erstellen und dann den Korrekturabzug mithilfe der [!DNL Workfront Proof]-SOAP-API zu aktualisieren.</p><p>Weitere Informationen zum Erstellen eines Korrekturabzugs mit der Workfront-API (die dieses Modul verwendet) finden Sie unter <a href="https://experienceleague.adobe.com/de/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">Hinzufügen erweiterter Proofing-Optionen beim Erstellen eines Korrekturabzugs über die Adobe Workfront-API</a>.</p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>Geben Sie die eindeutige Workfront-ID des Eintrags ein, mit dem das Modul interagieren soll, oder ordnen Sie diese zu.<p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=“. Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

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
   <li>clearAssignments</li>
   <li>clearConstraints</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Finanzielle Informationen löschen</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Erinnerungsnachrichten löschen</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Verschieben</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearDocuments</li>
   <li>clearConstraints</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Finanzielle Informationen löschen</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Erinnerungsnachrichten löschen</p></li>
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
   <li>clearAssignments</li>
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
   <li>preserveIssue<p>Ursprüngliches Problem beibehalten und Lösung hiermit verknüpfen: Aufgabe</p></li>
   <li>preservePrimaryContact<p>Zugriff auf diese Aufgabe durch den primären Kontakt für das Problem zulassen</p></li>
   <li>preserveCompletionDate<p>Das geplante Abschlussdatum des Problems beibehalten</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>In Projekt konvertieren</td> 
   <td>
   <ul>
   <li>preserveIssue<p>Ursprüngliches Problem beibehalten und Lösung hiermit verknüpfen: Aufgabe</p></li>
   <li>preservePrimaryContact<p>Zugriff auf diese Aufgabe durch den primären Kontakt für das Problem zulassen</p></li>
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
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Finanzielle Informationen löschen</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Erinnerungsnachrichten löschen</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Vorlage anfügen/Als Vorlage speichern</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearBillingRates</li>
   <li>clearConstraints</li>
   <li>clearDeliverables<p>Ziele löschen</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Finanzielle Informationen löschen</p></li>
   <li>clearHourTypes</li>
   <li>clearIssueSetup<p>Warteschlangeneigenschaften und Problem-Setup löschen</p></li>
   <li>clearPredecessors</li>
   <li>clearRisks</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>Erinnerungsnachrichten löschen</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL Eintrag lesen]**

Dieses Aktionsmodul ruft Daten aus einem einzelnen Eintrag ab.

Geben Sie die ID des Eintrags an. Sie können auch angeben, welche verwandten Einträge vom Modul gelesen werden sollen.

Wenn es sich bei dem Eintrag, den das Modul liest, beispielsweise um ein Projekt handelt, können Sie angeben, dass die Aufgaben des Projekts gelesen werden sollen.

Das Modul gibt ein Array von Daten aus den von Ihnen angegebenen Ausgabefeldern zurück.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Verbindung]</td>
    <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Eintragstyp]</td>

<td>Wählen Sie den Workfront-Objekttyp aus, der vom Modul gelesen werden soll.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Ausgaben]</td>

<td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Benutzerdefiniertes Ausgabeformular]</td>
     <td> <p>Wählen Sie die benutzerdefinierten Formulare aus, die in das Ausgabepaket für dieses Modul eingeschlossen werden sollen, und dann die Felder aus den benutzerdefinierten Formularen, die Sie in die Ausgabe aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Verweise]</td>
   <td>Wählen Sie alle Referenzfelder aus, die in die Ausgabe eingeschlossen werden sollen.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Sammlungen]</td>
   <td>Wählen Sie alle Referenzfelder aus, die in die Ausgabe eingeschlossen werden sollen.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Geben Sie die eindeutige Workfront-ID des Eintrags ein, der vom Modul gelesen werden soll.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=“. Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

+++

<!--

+++ **[!UICONTROL Read a Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Read a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module retrieves data from a single record.

You specify the ID of the record. You can also specify which related records you want the module to read.

For example, if the record that the module is reading is a project, you can specify that you want the project's tasks read.

The module returns an array of data from the output fields you specified.

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
  
   <td>Choose the Workfront object type that you want the module to read.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
  
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Enter the unique Workfront ID of the record that you want the module to read.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++

-->

+++ **Ereignis-Payload-Version aktualisieren**

Workfront hat kürzlich eine neue Version seines Ereignisabonnement-Services veröffentlicht. Die neue Version bewirkt keine Änderung der Workfront-API, sondern der Ereignisabonnementfunktion. Dieses Aktionsmodul aktualisiert die für dieses Szenario verwendete Ereignis-Payload-Version.

Weitere Informationen zur neuen Ereignisabonnementversion finden Sie in der Workfront-Dokumentation unter [Ereignisabonnement-Versionierung](https://experienceleague.adobe.com/de/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning).

Ressourcen zum Beibehalten Ihrer Workfront Fusion-Szenarios während des Ereignisabonnement-Upgrades, einschließlich einer Webinar-Aufzeichnung, finden Sie unter [Beibehalten Ihrer Fusion-Szenarios beim Upgrade auf Ereignisabonnements V2](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=de).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Version]</td> 
   <td> Wählen Sie die Version des Ereignisabonnements aus, das für diese Payload verwendet werden soll. </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **Eintrag aktualisieren**


Dieses Aktionsmodul aktualisiert ein Objekt, z. B. ein Projekt, eine Aufgabe oder ein Problem. Mit dem Modul können Sie auswählen, welche Objektfelder im Modul verfügbar sind.

Geben Sie die ID des Eintrags an.

Das Modul gibt daraufhin die ID des Objekts und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Geben Sie die eindeutige Workfront-ID des Eintrags ein, der vom Modul aktualisiert werden soll.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=“. Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Eintrags aus, der vom Modul aktualisiert werden soll.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Wählen Sie die Felder aus, die zur Dateneingabe verfügbar sein sollen. Auf diese Weise können Sie diese Felder verwenden, ohne durch nicht benötigte Felder scrollen zu müssen. Anschließend können Sie Daten in diese Felder eingeben oder darin zuordnen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>Wählen Sie die benutzerdefinierten Formulare aus, für die Sie Feldwerte zum neuen Eintrag angeben möchten. Nachdem Sie das Formular ausgewählt haben, geben Sie die Daten für die Felder in diesem Formular ein.<p> Um Feldwerte für ein Formular anzugeben, das Sie in diesem Modul anfügen, schließen Sie die benutzerdefinierte Formular-ID in den Abschnitt mit den zuzuordnenden Feldern ein.</td> 
  </tr> 
 </tbody> 
</table>

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
> Bei der Eingabe von Text für ein benutzerdefiniertes Feld oder ein Objekt vom Typ [!UICONTROL Notiz] (Kommentar oder Antwort) können Sie mithilfe von HTML-Tags im Feld [!UICONTROL Notizentext] Rich-Text erstellen, z. B. fett oder kursiv formatierten Text.


+++

<!--

+++ **[!UICONTROL Update Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Update a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module updates an object, such as a project, task, or issue. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  object and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Enter the unique Workfront ID of the record that you want the module to update.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to update.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need. You can then enter or map data into these fields.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL Dokument hochladen]**

Dieses Aktionsmodul lädt ein Dokument in ein Workfront-Objekt hoch, z. B. in ein Projekt, eine Aufgabe oder ein Problem. Mit diesem Modul wird das Dokument in Blöcken hochgeladen, was einen reibungsloseren Upload-Prozess in Workfront ermöglicht.

Dieses Modul kann größere Dateien als das Legacy-Modul verarbeiten und wird schrittweise an Organisationen mit Workfront-Ultimate-Paket ausgerollt.

Geben Sie den Speicherort für das Dokument, die hochzuladende Datei und einen optionalen neuen Namen für die Datei an.

Das Modul gibt daraufhin die ID des Dokuments und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID des verwandten Eintrags]</td> 
   <td>Geben Sie die eindeutige Workfront-ID des Eintrags ein, in den das Dokument hochgeladen werden soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Typ des verwandten Eintrags]</td> 
   <td>Wählen Sie den Typ des Workfront-Eintrags aus, in den das Dokument vom Modul hochgeladen werden soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordner-ID]</td> 
   <td>Je nach Typ des verwandten Eintrags müssen Sie möglicherweise eine Ordner-ID eingeben oder diese zuordnen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Quelldatei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie unter [Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen](#workfront-object-types-available-for-each-workfront-module).

+++

<!--

+++ **[!UICONTROL Upload Document (Legacy)]**

This action module uploads a document to a Workfront object, such as a project, task, or issue. It uploads the entire document at once. 

You specify the location for the document, the file you want to upload, and an optional new name for the file.

The module returns the ID of the document and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Enter the unique Workfront ID of the record to which you want to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Select the type of Workfront record where you want the module to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Depending on the type of related record, you may need to enter or map a folder ID.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).


+++
-->

### Suchvorgänge

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL Verwandte Einträge lesen]**

Dieses Suchmodul liest Einträge, die mit Ihrer Suchanfrage in einem bestimmten übergeordneten Objekt übereinstimmen.

Legen Sie fest, welche Felder in der Ausgabe enthalten sein sollen. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des übergeordneten Eintrags (Workfront-Objekts) aus, dessen verknüpfte Einträge Sie lesen möchten.</p> <p>Eine Liste der Workfront-Objekttypen, für die Sie dieses Modul verwenden können, finden Sie in diesem Artikel unter <a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID des übergeordneten Eintrags]</td> 
   <td> <p>Geben Sie die ID des übergeordneten Eintrags ein, dessen verknüpfte Einträge Sie lesen möchten, oder ordnen Sie diese zu.</p> <p>Um die ID abzurufen, öffnen Sie das Workfront-Objekt in Ihrem Browser und kopieren Sie den Text am Ende der URL nach „ID=“. Beispiel: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sammlungen]</td> 
   <td>Wählen Sie den Typ des untergeordneten Eintrags aus, der vom Modul gelesen werden soll, oder ordnen Sie diesen zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Suche]**

Dieses Suchmodul sucht in einem Objekt in Workfront nach Einträgen, die mit Ihrer Suchanfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Eintrags aus, nach dem vom Modul gesucht werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Liste benutzerdefinierter Formulare]</td> 
   <td> <p>Wählen Sie mindestens ein benutzerdefiniertes Formular aus. Felder aus diesen benutzerdefinierten Formularen stehen für die Suchanfrage zur Verfügung.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ergebnissatz]</td> 
   <td>Wählen Sie eine Option aus, um anzugeben, ob das Modul das erste Ergebnis erhalten soll, das Ihren Suchkriterien entspricht, oder alle Ergebnisse, die damit übereinstimmen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suchkriterienfelder]</td> 
   <td> <p>Wählen Sie die Felder aus, die für Ihre Suchkriterien verwendet werden sollen. Diese Felder sind dann im Dropdown „Suchkriterien“ verfügbar.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suchkriterien]</td> 
   <td> <p>Geben Sie das Feld ein, nach dem gesucht werden soll, den gewünschten Operator für die Abfrage und den Wert, nach dem im Feld gesucht werden soll.</p> <p>Hinweis: Verwenden Sie nicht <code>username </code>in Ihren Suchkriterien. Ist <code>username </code>in einer API-Abfrage an Workfront enthalten, wird die bzw. der Benutzende bei Workfront angemeldet und die Suche ist nicht erfolgreich.</p> <p>Hinweis: <code>In</code> und <code>NotIn</code>arbeiten mit Arrays. Die Eingaben sollten im Array-Format erfolgen.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die in die Ausgabe für dieses Modul eingeschlossen werden sollen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Verweise]</td> 
   <td>Wählen Sie alle Referenzfelder aus, die in die Suche eingeschlossen werden sollen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sammlungen]</td> 
   <td>Wählen Sie alle Sammlungen aus, die der Suche hinzugefügt werden sollen.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Suchen (Legacy)]**

>[!IMPORTANT]
>
>Dieses Modul wurde durch das Modul „Einträge suchen“ ersetzt. Es wird empfohlen, dieses Modul in neuen Szenarios zu verwenden.
>Vorhandene Szenarios, die dieses Modul nutzen, funktionieren weiterhin erwartungsgemäß. Dieses Modul wurde im Mai 2025 aus der Modulauswahl entfernt.

Dieses Suchmodul sucht in einem Objekt in Workfront nach Einträgen, die mit Ihrer Suchanfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-Anwendung mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Workfront-Eintrags aus, nach dem vom Modul gesucht werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ergebnissatz]</td> 
   <td>Wählen Sie eine Option aus, um anzugeben, ob das Modul das erste Ergebnis erhalten soll, das Ihren Suchkriterien entspricht, oder alle Ergebnisse, die damit übereinstimmen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suchkriterienfelder]</td> 
   <td> <p>Wählen Sie die Felder aus, die für Ihre Suchkriterien verwendet werden sollen. Diese Felder sind dann im Dropdown „Suchkriterien“ verfügbar.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suchkriterien]</td> 
   <td> <p>Geben Sie das Feld ein, nach dem gesucht werden soll, den gewünschten Operator für die Abfrage und den Wert, nach dem im Feld gesucht werden soll.</p> <p>Hinweis: Verwenden Sie nicht <code>username </code>in Ihren Suchkriterien. Ist <code>username </code>in einer API-Abfrage an Workfront enthalten, wird die bzw. der Benutzende bei Workfront angemeldet und die Suche ist nicht erfolgreich.</p> <p>Hinweis: <code>In</code> und <code>NotIn</code>arbeiten mit Arrays. Die Eingaben sollten im Array-Format erfolgen.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die in die Ausgabe für dieses Modul eingeschlossen werden sollen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Verweise]</td> 
   <td>Wählen Sie alle Referenzfelder aus, die in die Suche eingeschlossen werden sollen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sammlungen]</td> 
   <td>Wählen Sie alle Sammlungen aus, die der Suche hinzugefügt werden sollen.</td> 
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

## Für die einzelnen Workfront-Module verfügbare Workfront-Objekttypen

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**Für die einzelnen Workfront-Auslösermodule verfügbare Objekttypen**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Eintrag überwachen]</th> 
   <th>[!UICONTROL Feld überwachen]</th> 
   <th>[!UICONTROL Ereignisse überwachen]</th> 
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
   <td>Stunde</td> 
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
   <td>Notiz</td> 
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
   <td>Projektbenutzerin bzw. -benutzer</td> 
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
   <td>Benutzerin oder Benutzer</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Aktualisieren</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Für die einzelnen Workfront-Aktionsmodule verfügbare Objekttypen**

>[!NOTE]
>
>Das Modul [!UICONTROL Dokument herunterladen] ist nicht in dieser Tabelle enthalten, da Workfront-Objekttypen nicht Teil der zugehörigen Konfiguration sind.

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
   <th>[!UICONTROL Eintrag erstellen]</th> 
   <th>[!UICONTROL Eintrag aktualisieren]</th> 
   <th>[!UICONTROL Eintrag löschen]</th> 
   <th>[!UICONTROL Dokument hochladen]</th> 
   <th>[!UICONTROL Eintrag lesen]</th> 
   <th>[!UICONTROL Benutzerdefinierter API-Aufruf]</th> 
   <th>[!UICONTROL Sonstige Aktion]</th> 
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
   <td>Stunde</td> 
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
   <td>Notiz</td> 
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
   <td>Projektbenutzerin bzw. -benutzer</td> 
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
   <td>Benutzerin oder Benutzer</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Aktualisieren</td> 
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

+++**Für die einzelnen Workfront-Suchmodule verfügbare Objekttypen**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Suchen]</th> 
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
   <td>Stunde</td> 
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
   <td>Notiz</td> 
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
   <td>Projektbenutzerin bzw. -benutzer</td> 
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
   <td>Benutzerin oder Benutzer</td> 
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

Sie sollten überprüfen, ob alles erwartungsgemäß funktioniert.

+++

## Ereignisabonnementfilter in den Workfront-Modulen [!UICONTROL Ereignisse überwachen]

>[!NOTE]
>
>* Es wird ausdrücklich empfohlen, Ereignisabonnementfilter in den Modulen [!UICONTROL Ereignisse überwachen] zu verwenden.
>
>* Workfront hat kürzlich eine neue Version seines Ereignisabonnement-Services veröffentlicht. Die neue Version bewirkt keine Änderung der Workfront-API, sondern der Ereignisabonnementfunktion. Dieses Aktionsmodul aktualisiert die für dieses Szenario verwendete Ereignis-Payload-Version.
>
>   Weitere Informationen zur neuen Ereignisabonnementversion finden Sie in der Workfront-Dokumentation unter [Ereignisabonnement-Versionierung](https://experienceleague.adobe.com/de/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning).
>
>   Ressourcen zum Beibehalten Ihrer Workfront Fusion-Szenarios während des Ereignisabonnement-Upgrades, einschließlich einer Webinar-Aufzeichnung, finden Sie unter [Beibehalten Ihrer Fusion-Szenarios beim Upgrade auf Ereignisabonnements V2(https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=de)].

Das Workfront-Modul [!UICONTROL Ereignisse überwachen] löst Szenarios auf Basis eines Webhooks aus, der ein Ereignisabonnement in der Workfront-API erstellt. Das Ereignisabonnement ist ein Satz von Daten, der bestimmt, welche Ereignisse an den Webhook gesendet werden. Wenn Sie beispielsweise ein Modul [!UICONTROL Ereignisse überwachen] einrichten, das auf Probleme achtet, sendet das Ereignisabonnement ausschließlich Ereignisse, die mit Problemen in Zusammenhang stehen.

Durch Verwendung von Ereignisabonnementfiltern können Fusion-Benutzende Ereignisabonnements erstellen, die für ihre Anwendungsfälle besser geeignet sind. Sie können z. B. ein Ereignisabonnement in der Workfront-API einrichten, um nur Probleme in einem bestimmten Projekt an den Webhook zu senden und so sicherzustellen, dass das Modul [!UICONTROL Ereignisse überwachen] Szenarios nur für Probleme in diesem Projekt auslöst. Die Möglichkeit, genauer definierte Auslöser zu erstellen, verbessert das Szenario-Design, indem die Anzahl irrelevanter Auslöser reduziert wird.

Dies unterscheidet sich vom Einrichten eines Filters im Workfront Fusion-Szenario. Ohne einen Ereignisabonnementfilter erhält Ihr Webhook alle Ereignisse, die mit dem ausgewählten Objekttyp zusammenhängen. Die meisten dieser Ereignisse sind für das Szenario irrelevant und müssen herausgefiltert werden, bevor das Szenario fortgesetzt werden kann.

Die folgenden Operatoren sind im Filter unter „Workfront“ > „Ereignisse überwachen“ verfügbar:

* Gleich
* Ungleich
* Größer als
* Kleiner als
* Größer oder gleich
* Kleiner oder gleich
* Enthält
* Vorhanden
   * Dieser Operator benötigt keinen Wert und das Wertfeld ist nicht vorhanden.
* Existiert nicht
   * Dieser Operator benötigt keinen Wert und das Wertfeld ist nicht vorhanden.
* Geändert
   * Dieser Operator benötigt keinen Wert und das Wertfeld ist nicht vorhanden.
   * Dieser Operator ignoriert das Feld „Status“.
   * Wählen Sie bei Verwendung von `Changed` im Feld **Eintragsursprung** die Option **Nur aktualisierte Ereignisse** aus.

>[!IMPORTANT]
>
>Filter in vorhandenen Workfront-Webhooks können nicht bearbeitet werden. Um verschiedene Filter für Workfront-Ereignisabonnements einzurichten, entfernen Sie den aktuellen Webhook und erstellen Sie einen neuen.

>[!INFO]
>
>**Beispiel:** Nehmen wir ein Szenario an, bei dem neue Probleme verarbeitet werden, die der Benutzerin Ana zugewiesen sind.
>
>### Filtern von Ereignissen mithilfe eines Ereignisabonnementfilters (empfohlen)
>
>Mit dem Ereignisfilter können Sie den Webhook so einrichten, dass das Szenario ausgelöst wird, wenn ein Problem während der Problemerstellung Ana zugewiesen wird. Ana hat die Benutzer-ID b378489d8f7cd3cee0539260720a84b7.
>
>![Ereignisfilter](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>Wenn an einem Tag 100 Probleme erstellt werden, aber nur zwei davon Ana zugewiesen sind, wird das Szenario zweimal ausgeführt.
>
>### Filtern von Ereignissen innerhalb des Szenarios (nicht empfohlen)
>
>Um Ereignisse so zu filtern, dass nur die Probleme verarbeitet werden, die Ana zugewiesen sind, können Sie nach dem Modul [!UICONTROL Ereignisse überwachen] einen Filter erstellen.
>
>![Ohne Ereignisfilter](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>Wenn an einem Tag 100 Probleme erstellt werden, aber nur zwei davon Ana zugewiesen sind, wird das Szenario 100-mal ausgeführt. 98 der Ausführungen würden beim Filter anhalten, aber das Auslösermodul verbraucht trotzdem Daten und führt Vorgänge bei allen Ausführungen aus.

Weitere Informationen zu Workfront-Ereignisabonnements finden Sie unter [Häufig gestellte Fragen – Ereignisabonnements](https://experienceleague.adobe.com/de/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq).

Weitere Informationen zu Webhooks finden Sie unter [Instant-Auslöser (Webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/references/modules/webhooks-reference.md).

Weitere Informationen zu Filtern in Szenarios finden Sie unter [Hinzufügen eines Filters zu einem Szenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).
