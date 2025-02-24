---
title: Google-Kalendermodule
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die den Google-Kalender verwenden, und ihn mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: 160e503adeca5404e18fd0cba9f475fee8510a48
workflow-type: tm+mt
source-wordcount: '2315'
ht-degree: 0%

---

# [!DNL Google Calendar]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!UICONTROL Google Calendar] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Plan*</td>
  <td> <p>[!UICONTROL Pro] oder höher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
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

Um [!DNL Google Calendar]-Module verwenden zu können, müssen Sie über ein [!DNL Google]-Konto verfügen.

## Google Calendar-API-Informationen

Der Google-Kalender-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://www.googleapis.com/calendar/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v5.4.5</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Calendar] Module und ihre Felder

Beim Konfigurieren [!DNL Google Calendar] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Google Calendar] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Iteratoren](#iterators)

### Auslöser

* [Ereignisse ansehen](#watch-events)
* [Ereignisse ansehen (Sofort)](#watch-events-instant)

#### Ereignisse ansehen

Dieses Kalendermodul führt ein Trigger aus, wenn ein neues Ereignis in dem von Ihnen angegebenen Kalender hinzugefügt, aktualisiert, gelöscht, gestartet oder beendet wird. Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz oder den Datensätzen verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Calendar]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Wählen Sie den Kalender aus, mit dem das Modul arbeiten soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Wählen Sie aus, ob nur neue Ereignisse oder neue Ereignisse und alle Änderungen angesehen werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>Aktivieren Sie diese Option, um gelöschte Ereignisse einzuschließen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>Geben Sie den Text ein, für den Sie Ergebnisse zurückgeben möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Ereignissen fest, mit denen [!DNL Workfront Fusion] während eines Zyklus arbeitet (die Anzahl der Wiederholungen pro Szenario-Ausführung). Wenn der Wert zu hoch eingestellt ist, kann die Verbindung auf der Seite des angegebenen Drittanbieterdienstes unterbrochen werden (Zeitüberschreitung). [!DNL Workfront Fusion] hat darauf keinen Einfluss. Es wird empfohlen, einen niedrigeren Wert festzulegen und entweder einen höheren Wert für die maximale Anzahl an Zyklen zu definieren oder das Szenario häufiger auszuführen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Ereignisse ansehen (Sofort)

Dieses Ereignismodul verwendet einen Mailhook, um eine E-Mail-Trigger zu erstellen, den Sie als Ereigniseinladung verwenden können. Das Modul startet ein Szenario basierend auf Ereignissen, zu denen die E-Mail-Adresse eingeladen wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Mailhook] </td> 
   <td> <p>Wählen Sie den Mailhook aus, den Sie für dieses Modul verwenden möchten. Um einen neuen Mailhook zu erstellen, klicken Sie auf <b>Hinzufügen</b> und geben Sie die Verbindung ein, die Sie für den Mailhook verwenden möchten.</p><p>Anweisungen zum Verbinden Ihres [!DNL Google Calendar]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Ereignissen fest, mit denen [!DNL Workfront Fusion] während eines Zyklus arbeitet (die Anzahl der Wiederholungen pro Szenario-Ausführung). Wenn der Wert zu hoch eingestellt ist, kann die Verbindung auf der Seite des angegebenen Drittanbieterdienstes unterbrochen werden (Zeitüberschreitung). [!DNL Workfront Fusion] hat darauf keinen Einfluss. Es wird empfohlen, einen niedrigeren Wert festzulegen und entweder einen höheren Wert für die maximale Anzahl an Zyklen zu definieren oder das Szenario häufiger auszuführen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [Kalender erstellen](#create-a-calendar)
* [Ereignis erstellen](#create-an-event)
* [Ereignis löschen](#delete-an-event)
* [Ereignisse abrufen](#get-events)
* [Aktualisieren eines Ereignisses](#update-an-event)

#### Kalender erstellen

Dieses Aktionsmodul erstellt einen Kalender, der mit dem Konto verknüpft ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Calendar]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color] </td> 
   <td> <p>Farbe auswählen, die mit dem Kalender verknüpft werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name] </td> 
   <td> <p>Geben Sie einen Namen für den neuen Kalender ein oder mappen Sie ihn.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an event]

Dieses Aktionsmodul erstellt ein Ereignis.

Sie geben den Kalender und die Parameter für das Ereignis an.

Das Modul gibt die ID des Ereignisses und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL Google Calendar]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Wählen Sie den Kalender aus, in dem das Ereignis angezeigt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color]</td> 
   <td>Wählen Sie die Farbe aus, die das Ereignis im Kalender anzeigt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Geben Sie einen Namen für das Ereignis ein oder mappen Sie ihn. </p> <p>Hinweis: Wenn Sie [!UICONTROL Quick add] im Feld [!UICONTROL Create an event] ausgewählt haben, können Sie Datum und Uhrzeit des Ereignisses einbeziehen und [!DNL Workfront Fusion] das Ereignis für dieses Datum und diese Uhrzeit erstellen. Beispiel: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Wenn Sie [!UICONTROL Quick add] ausgewählt haben, aber kein Datum und keine Uhrzeit in den Ereignisnamen aufnehmen, wird das Ereignis aus der aktuellen Zeit erstellt und dauert eine Stunde.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Aktivieren Sie diese Option, wenn das Ereignis ein ganztägiges Ereignis ist (keine Start- und Endzeiten erfordert).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Geben Sie das Startdatum und die Uhrzeit des Ereignisses ein oder ordnen Sie sie zu. </p> <p>Eine Liste der unterstützten Datumsformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Geben Sie das Enddatum und die Endzeit des Ereignisses ein oder mappen Sie sie. </p> <p>Eine Liste der unterstützten Datumsformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Geben Sie eine Beschreibung für das Ereignis ein oder mappen Sie sie. Dieses Feld unterstützt HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Geben Sie einen Ort für das Ereignis im Textformular ein.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Aktivieren Sie diese Option, um die standardmäßigen Erinnerungseinstellungen zu verwenden. Wenn Sie eine benutzerdefinierte Erinnerung im Feld [!UICONTROL Reminder] festlegen, wird dieser Wert auf Nein festgelegt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Erinnerung für das Ereignis hinzufügen. Klicken Sie für jede Erinnerung, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und wählen Sie dann die Methode aus, mit der Sie erinnert werden möchten, und legen Sie fest, wie lange (in Minuten) das Ereignis dauern soll, bevor Sie erinnert werden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Fügen Sie die Teilnehmer zum Ereignis hinzu. Klicken Sie für jeden Teilnehmer auf <b>Teilnehmer hinzufügen</b> und geben Sie dann seinen Namen und seine E-Mail-Adresse ein oder mappen Sie diese.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Wählen Sie aus, ob Personen, die Ihren Kalender anzeigen, Sie während dieses Ereignisses als beschäftigt oder verfügbar anzeigen sollen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Sichtbarkeit dieses Ereignisses auswählen. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>Das Ereignis hat die Sichtbarkeit, die Sie in Ihren Kalendereinstellungen festgelegt haben.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Jeder, für den der Kalender freigegeben ist, kann dieses Ereignis sehen.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Nur Teilnehmer können diese Veranstaltung sehen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Wählen Sie aus, ob Benachrichtigungen über die Erstellung eines neuen Ereignisses an alle Gäste, nicht [!DNL Google Calendar] Gäste oder an niemanden gesendet werden sollen.</p> <p>Tipp: Es wird empfohlen, die Option [!UICONTROL None] nur für Anwendungsfälle der Migration zu verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Aktivieren Sie diese Option, wenn Gäste dieses Ereignis ändern können sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Fügen Sie alle Wiederholungsregeln hinzu, die Sie auf dieses Ereignis anwenden möchten. Für jede Regel ist eine Liste mit [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] und [!UICONTROL EXDATE] für ein wiederkehrendes Ereignis erforderlich. Beachten Sie, dass [!UICONTROL DTSTART] und [!UICONTROL DTEND] Zeilen in diesem Feld nicht zulässig sind. Ereignisstart- und -endzeiten werden in den Feldern Beginn und Ende angegeben. Dieses Feld wird für einzelne Ereignisse oder Instanzen wiederkehrender Ereignisse weggelassen. Weitere Informationen finden Sie unter <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an event]

Dieses Aktionsmodul löscht ein Ereignis.

Kalender und Ereignis-ID angeben.

Das Modul gibt die ID des Ereignisses und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Calendar]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Wählen Sie den Kalender aus, der das Ereignis enthält, das Sie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> Geben Sie die Ereignis-ID aus einem zuvor erstellten [!DNL Google Calendar] ein, das Sie löschen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get events]

Dieses Modul ruft Informationen zu Ereignissen im ausgewählten Kalender basierend auf den von Ihnen angegebenen Kriterien ab.

Sie geben den Kalender und die Parameter der Suche an.

Das Modul gibt die ID der Ereignisse und aller zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL Google Calendar]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Wählen Sie den Kalender aus, für den Sie Ereignisse abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> Datum des Starts des Ereignisses eingeben oder zuordnen. Dieses Modul ruft auch Ereignisse ab, die vor diesem Datum beginnen und noch am eingegebenen Startdatum auftreten. </p> <p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Datum eingeben oder zuordnen, an dem das Ereignis endet. </p> <p> Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Single events]</td> 
   <td> <p> Aktivieren Sie diese Option, um wiederkehrende Ereignisse als einzelne Instanzen zu behandeln. Wenn Sie beispielsweise eine wöchentliche Besprechung haben und diese Option aktiviert ist, gibt das Modul jede wöchentliche Besprechung als separates Ereignis zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>Geben Sie den Suchbegriff ein, nach dem Sie suchen möchten, oder ordnen Sie ihn zu. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td> <p>Auswahl der Reihenfolge der im Ergebnis zurückgegebenen Ereignisse.</p> 
    <ul> 
     <li><strong>[!UICONTROL Start Time]</strong>: Sortieren nach Startdatum und -zeit (aufsteigend). Dies ist nur bei der Abfrage einzelner Ereignisse verfügbar.</li> 
     <li><strong>[!UICONTROL Updated Time]</strong>: Sortieren nach der Zeit der letzten Änderung (aufsteigend).</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mazimum number of returned events]</td> 
   <td> <p>Legen Sie die maximale Anzahl von Ereignissen fest, [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgegeben werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an event]

Dieses Aktionsmodul ändert ein vorhandenes Ereignis.

Kalender und Ereignis-ID angeben.

Das Modul gibt die ID des Ereignisses und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Calendar]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu Adobe [!DNL Workfront Fusion] - Grundanweisungen</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Wählen Sie den Kalender aus, mit dem Sie arbeiten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>Geben Sie die Ereignis-ID aus dem zuvor erstellten [!DNL Google Calendar] ein, das Sie aktualisieren möchten.</p> </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Geben Sie einen Namen für das Ereignis ein oder mappen Sie ihn. </p> <p>Hinweis: Wenn Sie [!UICONTROL Quick add] im Feld [!UICONTROL Create an event] ausgewählt haben, können Sie Datum und Uhrzeit des Ereignisses einbeziehen und [!DNL Workfront Fusion] das Ereignis für dieses Datum und diese Uhrzeit erstellen. Beispiel: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Wenn Sie [!UICONTROL Quick add] ausgewählt haben, aber kein Datum und keine Uhrzeit in den Ereignisnamen aufnehmen, wird das Ereignis aus der aktuellen Zeit erstellt und dauert eine Stunde.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Aktivieren Sie diese Option, wenn das Ereignis ein ganztägiges Ereignis ist (keine Start- und Endzeiten erfordert).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Geben Sie das Startdatum und die Uhrzeit des Ereignisses ein oder ordnen Sie sie zu. </p> <p>Eine Liste der unterstützten Datumsformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Geben Sie das Enddatum und die Endzeit des Ereignisses ein oder mappen Sie sie. </p> <p>Eine Liste der unterstützten Datumsformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Geben Sie eine Beschreibung für das Ereignis ein oder mappen Sie sie. Dieses Feld unterstützt HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Geben Sie einen Ort für das Ereignis im Textformular ein.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Aktivieren Sie diese Option, um die standardmäßigen Erinnerungseinstellungen zu verwenden. Wenn Sie eine benutzerdefinierte Erinnerung im Feld [!UICONTROL Reminder] festlegen, wird dieser Wert auf Nein festgelegt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Erinnerung für das Ereignis hinzufügen. Klicken Sie für jede Erinnerung, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und wählen Sie dann die Methode aus, mit der Sie erinnert werden möchten, und legen Sie fest, wie lange (in Minuten) das Ereignis dauern soll, bevor Sie erinnert werden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Fügen Sie die Teilnehmer zum Ereignis hinzu. Klicken Sie für jeden Teilnehmer auf <b>Teilnehmer hinzufügen</b> und geben Sie dann seinen Namen und seine E-Mail-Adresse ein oder mappen Sie diese.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Wählen Sie aus, ob Personen, die Ihren Kalender anzeigen, Sie während dieses Ereignisses als beschäftigt oder verfügbar anzeigen sollen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Sichtbarkeit dieses Ereignisses auswählen. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>Das Ereignis hat die Sichtbarkeit, die Sie in Ihren Kalendereinstellungen festgelegt haben.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Jeder, für den der Kalender freigegeben ist, kann dieses Ereignis sehen.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Nur Teilnehmer können diese Veranstaltung sehen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Wählen Sie aus, ob Benachrichtigungen über die Erstellung eines neuen Ereignisses an alle Gäste, nicht [!DNL Google Calendar] Gäste oder an niemanden gesendet werden sollen.</p> <p>Tipp: Es wird empfohlen, die Option [!UICONTROL None] nur für Anwendungsfälle der Migration zu verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Aktivieren Sie diese Option, wenn Gäste dieses Ereignis ändern können sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Fügen Sie alle Wiederholungsregeln hinzu, die Sie auf dieses Ereignis anwenden möchten. Für jede Regel ist eine Liste mit [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] und [!UICONTROL EXDATE] für ein wiederkehrendes Ereignis erforderlich. Beachten Sie, dass [!UICONTROL DTSTART] und [!UICONTROL DTEND] Zeilen in diesem Feld nicht zulässig sind. Ereignisstart- und -endzeiten werden in den Feldern Beginn und Ende angegeben. Dieses Feld wird für einzelne Ereignisse oder Instanzen wiederkehrender Ereignisse weggelassen. Weitere Informationen finden Sie unter <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr>

</tbody> 
</table>

### Iteratoren

#### Anlagen iterieren

Dieses Aktionsmodul durchläuft Anlagen zu einem Ereignis und gibt jede Anlage in einem separaten Bundle aus.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> Wählen Sie in diesem Szenario das Modul aus, das das Ereignis ausgibt, das die Anlagen enthält, die Sie iterieren möchten. </td> 
  </tr> 
 </tbody> 
</table>

#### Iterieren von Teilnehmern

Dieses Aktionsmodul durchläuft die Teilnehmer für ein Ereignis und gibt jeden Teilnehmer in einem separaten Bundle aus.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> Wählen Sie in diesem Szenario das Modul aus, das das Ereignis ausgibt, das die Teilnehmer enthält, die Sie iterieren möchten. </td> 
  </tr> 
 </tbody> 
</table>





## Trigger eines Szenarios vor einem Ereignis

Sie können ein Szenario zu einer bestimmten Zeit vor einem Ereignis mithilfe von standardmäßigen [!DNL Google Calendar]-E-Mail-Erinnerungen und dem Modul [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] in einen Trigger umwandeln.

1. Verwenden Sie das Modul [!UICONTROL Google Calendar] >[!UICONTROL Update an event] , um eine E-Mail-Erinnerung zu Ihrem Ereignis hinzuzufügen:

   ![Ereignisszenario vor Trigger ](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

1. Erstellen Sie ein neues Szenario, das mit dem Modul [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] beginnt.

   1. Kopieren Sie die E-Mail-Adresse des Postfachs.
   1. Speichern Sie das Szenario und führen Sie es aus.

1. Leiten Sie [!DNL Gmail] die E-Mail-Erinnerungen an die E-Mail-Adresse des E-Mail-Hooks [!DNL Google Calendar]:

   1. Öffnen Sie Ihre **[!UICONTROL [!DNL Gmail] settings]**.
   1. Öffnen Sie die Registerkarte **[!UICONTROL Forwarding and POP/IMAP]** .
   1. Klicken Sie auf **[!UICONTROL Add a forwarding address].**
   1. Fügen Sie die kopierte E-Mail-Adresse der Mailhooks ein&#x200B; klicken Sie auf **[!UICONTROL Next]**, bestätigen Sie den Vorgang durch Drücken von **[!UICONTROL Proceed]** im Popup-Fenster und klicken Sie dann auf **[!UICONTROL OK]**.

   1. Wechseln Sie [!DNL Workfront Fusion] zu dem neuen Szenario, das seine Ausführung abschließen soll, indem Sie die Bestätigungs-E-Mail erhalten.
   1. Klicken Sie auf die Blase über dem Modul, um die Ausgabe des Moduls zu überprüfen.
   1. Erweitern Sie das `Text` und kopieren Sie den Bestätigungs-Code:

      ![Bestätigungs-Code](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. Fügen Sie in Gmail den Bestätigungs-Code in das Bearbeitungsfeld ein und klicken Sie auf&#x200B;**[!UICONTROL Verify]**:

      ![Code einfügen](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. Öffnen Sie die Registerkarte **[!UICONTROL Filters and Blocked Addresses]** .
   1. Klicken Sie auf **[!UICONTROL Create a new filter]**.
   1. Richten Sie einen Filter für alle E-Mails aus `     calendar-notification@google.com` ein und klicken Sie auf&#x200B;**[!UICONTROL Create a filter]**:
   1. Wählen Sie **[!UICONTROL Forward it to]** und danach die E-Mail-Adresse der Mailhooks aus der Liste aus.
   1. Klicken Sie auf **[!UICONTROL Create filter]** , um den Filter zu erstellen.

1. (Optional) Fügen Sie [!DNL Workfront Fusion] das Modul [!UICONTROL Text parser] > [!UICONTROL Match pattern] nach dem Modul [!UICONTROL Webhooks] > [!UICONTROL Custom mailhook] hinzu, um den HTML-Code der E-Mail zu analysieren und alle benötigten Informationen zu erhalten.

   Sie können beispielsweise das Modul wie folgt konfigurieren, um die Ereignis-ID abzurufen:

   *Muster*: `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *Text*: Das vom [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] Modul ausgegebene `HTML content`.
