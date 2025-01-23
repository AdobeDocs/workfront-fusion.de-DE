---
title: Microsoft Office 365-Kalender
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die den Microsoft Office 365-Kalender verwenden, und ihn mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: fdecf740-e735-4569-b1a2-7c25c751ba42
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Calendar]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Microsoft Office 365 Calendar] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Um [!DNL Office 365 Calendar] mit [!DNL Adobe Workfront Fusion] verwenden zu können, muss ein [!DNL Office 365 Excel] Konto vorhanden sein. Sie können einen unter [www.office.com](https://www.office.com/) erstellen.

Anweisungen zum Verbinden Ihres Office 365-Kontos mit [!DNL Workfront Fusion] finden Sie unter [Verbindung zum Adobe herstellen [!DNL Workfront Fusion]  - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

Nachdem Sie Ihr Einverständnis erteilt haben, werden Sie zurück zur Seite &quot;[!UICONTROL Workfront Fusion]-Administration“ weitergeleitet, auf der Sie mit der Erstellung Ihres Szenarios fortfahren können.

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

Um [!DNL Microsoft Office 365 Calendar]-Module verwenden zu können, müssen Sie über ein [!DNL Microsoft Office 365 Calendar]-Konto verfügen.

## Informationen zur Microsoft Office 365-Kalender-API

Der Microsoft Office 365-Kalender-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden des [!DNL Office 365 Calendar]-Services mit [!DNL Workfront Fusion]

Anweisungen zum Verbinden Ihres [!DNL Office 365 Calendar]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung zu [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
>
>Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.

## [!DNL Microsoft Office 365 Calendar] Module und ihre Felder

Beim Konfigurieren [!DNL Microsoft Office 365 Calendar] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Microsoft Office 365 Calendar] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ereignis](#event)
* [Kalender](#calendar)
* [Sonstige](#other)

### Ereignis

* [[!UICONTROL Watch Events]](#watch-events)
* [[!UICONTROL Search Events]](#search-events)
* [[!UICONTROL Get an Event]](#get-an-event)
* [[!UICONTROL Create an Event]](#create-an-event)
* [[!UICONTROL Update an Event]](#update-an-event)
* [[!UICONTROL Delete an Event]](#delete-an-event)

#### [!UICONTROL Watch Events]

Dieses Kalendermodul ruft Details zu einem Trigger ab, wenn das Ereignis im ausgewählten Kalender erstellt, aktualisiert, gelöscht, gestartet oder beendet wird.

>[!NOTE]
>
>Um nach gelöschten Vorkommen einer Ereignisreihe zu suchen, wählen Sie [!UICONTROL By Updated Time] im Feld [!UICONTROL Watch events] aus. Dieses Modul überwacht nicht auf gelöschte einzelne Ereignisse oder gelöschte Ereignisreihen.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch events]</td> 
   <td> <p>Wählen Sie aus, wie Sie Ereignisse ansehen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL By Created Time]</strong> </p> <p>Achten Sie auf neue Ereignisse.</p> </li> 
     <li> <p><strong>[!UICONTROL By Updated Time]</strong> </p> <p>Auf aktualisierte Ereignisse achten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Wählen Sie die [!UICONTROL calendar group] aus, die den Kalender enthält, in dem Sie Ereignisse beobachten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>Wählen Sie den spezifischen Kalender aus, den Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Filterbedingungen festlegen, um Ergebnisse nach Betreff, Ereignis-ID oder Hauptteil zu filtern.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl an Nachrichten ein, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Events]

Dieses Suchmodul ruft Details zu einem Ereignis ab, wenn das Ereignis im ausgewählten Kalender erstellt, aktualisiert, gelöscht, gestartet oder beendet wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Wählen Sie die [!UICONTROL calendar group] aus, die den Kalender enthält, in dem Sie Ereignisse beobachten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>Wählen Sie den spezifischen Kalender aus, den Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Filterbedingungen festlegen, um Ergebnisse zu filtern. Sie können nach den folgenden Eigenschaften filtern:</p> 
    <ul> 
     <li>[!UICONTROL Subject]</li> 
     <li>[!UICONTROL Event ID]</li> 
     <li>[!UICONTROL Created Date Time]</li> 
     <li>[!UICONTROL Last Modified Date Time]</li> 
     <li>[!UICONTROL Body Preview]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Ergebnisse sortieren möchten.</p> 
    <ul> 
     <li><strong>[!UICONTROL Subject]</strong>, aufsteigend oder absteigend</li> 
     <li><strong>[!UICONTROL Created Date Time]</strong>, aufsteigend oder absteigend</li> 
     <li><strong>[!UICONTROL Last Modified Date Time]</strong>, aufsteigend oder absteigend</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl an Ereignissen ein, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben sollen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Event]

Dieses Aktionsmodul ruft Details des angegebenen Ereignisses ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Geben Sie die ID des Ereignisses ein, zu dem Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an Event]

Dieses Aktionsmodul erstellt ein neues Ereignis.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Geben Sie einen Titel für das erstellte Ereignis ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start date]</td> 
   <td> Geben Sie einen einzigen Zeitpunkt ein, zu dem das Ereignis in einer kombinierten Datums- und Uhrzeitdarstellung beginnt. Verwenden Sie den <code>({date}T{time}</code> Format , z. B. <code>2017-08-29T04:00:00.0000000</code>. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End date]</td> 
   <td> Geben Sie einen einzigen Zeitpunkt ein, zu dem das Ereignis in einer kombinierten Datums- und Uhrzeitdarstellung endet. Verwenden Sie den <code>{date}T{time}</code> Format , z. B. <code>2017-08-29T04:00:00.0000000</code>. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder on]</td> 
   <td>Wählen Sie aus, ob eine Erinnerung für dieses Ereignis aktiviert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder]</td> 
   <td>Anzahl der Minuten vor Ereignisbeginn eingeben oder zuordnen, nach denen die Erinnerung Trigger werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Die Wichtigkeit dieses Ereignisses auswählen.</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>Wählen Sie die Empfindlichkeit dieses Ereignisses aus.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>Der Empfänger sieht eine "[!UICONTROL Please treat this as Personal]"-Nachricht.</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>Der Empfänger sieht eine "[!UICONTROL Please treat this as Private]"-Nachricht. Dieses Ereignis wird von den Posteingangsregeln des Empfängers nicht weitergeleitet oder umgeleitet.</p> </li> 
     <li> <p><strong>[!UICONTROL Confidential]</strong> </p> <p>Der Empfänger sieht eine "[!UICONTROL Please treat this as Confidential]"-Nachricht. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content type]</td> 
   <td>Wählen Sie aus, ob der Textinhalt Nur-Text oder HTML ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td>Geben Sie den Text der Nachricht ein, die mit dem Ereignis verknüpft ist, oder mappen Sie ihn. Es kann im HTML- oder Textformat vorliegen (wie im Feld [!UICONTROL Body Content Type] oben angegeben).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Location]</td> 
   <td> <p>Details zum Veranstaltungsort eingeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Response requested]</td> 
   <td>Wählen Sie <strong>[!UICONTROL Yes]</strong> aus, um den Einladenden aufzufordern, eine Antwort auf die Ereigniseinladung zu senden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show as]</td> 
   <td> <p>Wählen Sie aus, wie das Ereignis den Personen angezeigt werden soll, die Ihren Kalender anzeigen.</p> 
    <ul> 
     <li>[!UICONTROL Free]</li> 
     <li>[!UICONTROL Tentative]</li> 
     <li>[!UICONTROL Busy]</li> 
     <li>[!UICONTROL Out of office]</li> 
     <li>[!UICONTROL Working elsewhere]</li> 
     <li>[!UICONTROL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attendees]</p> </td> 
   <td> <p>Fügen Sie Teilnehmer der Veranstaltung hinzu.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Geben Sie den Namen des Teilnehmers ein.</p> </li> 
     <li> <p><strong>[!UICONTROL Email]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Teilnehmers ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>Geben Sie die Kategorien ein, die das Ereignis wie im Kalender angezeigt werden soll, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an Event]

Dieses Aktionsmodul aktualisiert ein vorhandenes Ereignis.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td>Geben Sie die ID des Ereignisses ein, das Sie aktualisieren möchten, ordnen Sie sie zu oder wählen Sie sie aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Geben Sie einen Titel für das erstellte Ereignis ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start date]</td> 
   <td> Geben Sie einen einzigen Zeitpunkt ein, zu dem das Ereignis in einer kombinierten Datums- und Uhrzeitdarstellung beginnt. Verwenden Sie den <code>{date}T{time}</code> Format , z. B. <code>2017-08-29T04:00:00.0000000</code>. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End date]</td> 
   <td> Geben Sie einen einzigen Zeitpunkt ein, zu dem das Ereignis in einer kombinierten Datums- und Uhrzeitdarstellung endet. Verwenden Sie den <code>({date}T{time}</code> Format , z. B. <code>2017-08-29T04:00:00.0000000</code>. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder on]</td> 
   <td>Wählen Sie aus, ob eine Erinnerung für dieses Ereignis aktiviert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder]</td> 
   <td>Anzahl der Minuten vor Ereignisbeginn eingeben oder zuordnen, nach denen die Erinnerung Trigger werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Die Wichtigkeit dieses Ereignisses auswählen.</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>Wählen Sie die Empfindlichkeit dieses Ereignisses aus.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>Der Empfänger sieht eine "[!UICONTROL Please treat this as Personal]"-Nachricht.</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>Der Empfänger sieht eine "[!UICONTROL Please treat this as Private]"-Nachricht. Dieses Ereignis wird von den Posteingangsregeln des Empfängers nicht weitergeleitet oder umgeleitet.</p> </li> 
     <li> <p><strong>[!UICONTROL Confidential]</strong> </p> <p>Der Empfänger sieht eine "[!UICONTROL Please treat this as Confidential]"-Nachricht. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content type]</td> 
   <td>Wählen Sie aus, ob der Hauptteil der Nachricht, die mit dem Ereignis verknüpft ist, Nur-Text oder HTML ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td>Geben Sie den Text der Nachricht ein, die mit dem Ereignis verknüpft ist, oder mappen Sie ihn. Es kann im HTML- oder Textformat vorliegen (wie im Feld [!UICONTROL Body Content Type] oben angegeben).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Location]</td> 
   <td> <p>Details zum Veranstaltungsort eingeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Response requested]</td> 
   <td>Wählen Sie <strong>[!UICONTROL Yes]</strong> aus, um den Einladenden aufzufordern, eine Antwort auf die Ereigniseinladung zu senden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show as]</td> 
   <td> <p>Wählen Sie aus, wie das Ereignis den Personen angezeigt werden soll, die Ihren Kalender anzeigen.</p> 
    <ul> 
     <li>[!UICONTROL Free]</li> 
     <li>[!UICONTROL Tentative]</li> 
     <li>[!UICONTROL Busy]</li> 
     <li>[!UICONTROL Out of office]</li> 
     <li>[!UICONTROL Working elsewhere]</li> 
     <li>[!DNL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attendees]</p> </td> 
   <td> <p>Fügen Sie Teilnehmer der Veranstaltung hinzu.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Geben Sie den Namen des Teilnehmers ein.</p> </li> 
     <li> <p><strong>[!UICONTROL Email]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Teilnehmers ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>Geben Sie die Kategorien ein, die das Ereignis wie im Kalender angezeigt werden soll, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Event]

Dieses Aktionsmodul löscht ein vorhandenes Ereignis.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Geben Sie die ID des Ereignisses ein, das Sie löschen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Kalender

* [[!UICONTROL List Calendars]](#list-calendars)
* [[!UICONTROL Get a Calendar]](#get-a-calendar)
* [[!UICONTROL Create a Calendar]](#create-a-calendar)
* [[!UICONTROL Update a Calendar]](#update-a-calendar)
* [[!UICONTROL Delete a Calendar]](#delete-a-calendar)

#### [!UICONTROL List Calendars]

Dieses Suchmodul ruft eine Liste aller Kalender der authentifizierten Benutzenden ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Wählen Sie die [!UICONTROL calendar group] aus, die die Kalender enthält, die Sie auflisten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl an Kalendern ein, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben sollen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Calendar]

Dieses Aktionsmodul ruft Details zu einem einzelnen Kalender ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Geben Sie die ID des Kalenders ein, zu dem Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Calendar]

Dieses Aktionsmodul erstellt einen neuen Kalender in Ihrem Google-Konto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar name]</td> 
   <td> <p>Geben Sie einen Namen für den neuen Kalender ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Calendar]

Dieses Aktionsmodul bearbeitet einen vorhandenen Kalender.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td>Geben Sie die [!UICONTROL Calendar ID] für den Kalender ein, den Sie aktualisieren möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Calendar name]</td> 
   <td> <p>Geben Sie einen Namen für den neuen Kalender ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Calendar]

Dieses Aktionsmodul löscht einen vorhandenen Kalender.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td>Geben Sie die [!UICONTROL Calendar]-ID für den Kalender ein, den Sie löschen möchten.</td> 
  </tr> 
 </tbody> 
</table>

### Sonstige

#### [!UICONTROL Make an API Call]

Mit diesem Modul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://graph.microsoft.com</code> ein. Beispiel:<code> /v1.0/me/events</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu, z. B. <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:   <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
