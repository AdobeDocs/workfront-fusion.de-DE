---
title: Microsoft Office 365-Kalender
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die den Microsoft Office 365-Kalender verwenden, und ihn mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: fdecf740-e735-4569-b1a2-7c25c751ba42
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2044'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Calendar]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Microsoft Office 365 Calendar] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

## Verbinden des [!DNL Office 365 Calendar]-Service mit Workfront Fusion

Anweisungen zum Verbinden Ihres [!DNL Office 365 Calendar]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung mit [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
>
>Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.

## [!DNL Microsoft Office 365 Calendar] Module und ihre Felder

Beim Konfigurieren von [!DNL Microsoft Office 365 Calendar] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Microsoft Office 365 Calendar] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ereignis](#event)
* [Kalender](#calendar)
* [Sonstiges](#other)

### Ereignis

* [[!UICONTROL Ereignis erstellen]](#create-an-event)
* [[!UICONTROL Ereignis löschen]](#delete-an-event)
* [[!UICONTROL Ereignis abrufen]](#get-an-event)
* [[!UICONTROL Ereignisse suchen]](#search-events)
* [[!UICONTROL Ereignis aktualisieren]](#update-an-event)
* [[!UICONTROL Ereignisse ansehen]](#watch-events)

#### [!UICONTROL Ereignis erstellen]

Dieses Aktionsmodul erstellt ein neues Ereignis.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Betreff]</td> 
   <td> <p>Geben Sie einen Titel für das erstellte Ereignis ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Startdatum]</td> 
   <td> Geben Sie einen einzigen Zeitpunkt ein, zu dem das Ereignis in einer kombinierten Datums- und Uhrzeitdarstellung beginnt. Verwenden Sie den <code>{date}T{time}</code> Format , z. B. <code>2017-08-29T04:00:00.0000000</code>. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enddatum]</td> 
   <td> Geben Sie einen einzigen Zeitpunkt ein, zu dem das Ereignis in einer kombinierten Datums- und Uhrzeitdarstellung endet. Verwenden Sie den <code>{date}T{time}</code> Format , z. B. <code>2017-08-29T04:00:00.0000000</code>. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL reminder on]</td> 
   <td>Wählen Sie aus, ob eine Erinnerung für dieses Ereignis aktiviert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL reminder]</td> 
   <td>Anzahl der Minuten vor Ereignisbeginn eingeben oder zuordnen, nach denen die Erinnerung Trigger werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wichtigkeit]</td> 
   <td> <p>Die Wichtigkeit dieses Ereignisses auswählen.</p> 
    <ul> 
     <li>[!UICONTROL Niedrig]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL Hoch]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>Wählen Sie die Empfindlichkeit dieses Ereignisses aus.</p> 
    <ul> 
     <li><strong>[!UICONTROL normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>Der Empfänger sieht die Nachricht "[!UICONTROL Please treat as Personal]".</p> </li> 
     <li> <p><strong>[!UICONTROL Privat]</strong> </p> <p>Der Empfänger sieht die Nachricht "[!UICONTROL Bitte als privat behandeln]". Dieses Ereignis wird von den Posteingangsregeln des Empfängers nicht weitergeleitet oder umgeleitet.</p> </li> 
     <li> <p><strong>[!UICONTROL VERTRAULICH]</strong> </p> <p>Der Empfänger sieht die Nachricht "[!UICONTROL Bitte als vertraulich behandeln]". </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hauptteil-Inhaltstyp]</td> 
   <td>Wählen Sie aus, ob der Textinhalt Nur-Text oder HTML ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hauptteilinhalt]</td> 
   <td>Geben Sie den Text der Nachricht ein, die mit dem Ereignis verknüpft ist, oder mappen Sie ihn. Sie kann im HTML- oder Textformat vorliegen (wie im Feld [!UICONTROL Hauptteil-Inhaltstyp] weiter oben angegeben).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Speicherort]</td> 
   <td> <p>Ereignisortdetails eingeben oder zuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Antwort angefordert]</td> 
   <td>Wählen Sie <strong>[!UICONTROL Yes]</strong> aus, um den Einladenden aufzufordern, eine Antwort auf die Ereigniseinladung zu senden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzeigen als]</td> 
   <td> <p>Wählen Sie aus, wie das Ereignis den Personen angezeigt werden soll, die Ihren Kalender anzeigen.</p> 
    <ul> 
     <li>[!UICONTROL FREE]</li> 
     <li>[!UICONTROL Tentative]</li> 
     <li>[!UICONTROL Besetzt]</li> 
     <li>[!UICONTROL Abwesend]</li> 
     <li>[!UICONTROL, anderswo arbeiten]</li> 
     <li>[!UICONTROL unbekannt]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attendees]</p> </td> 
   <td> <p>Klicken Sie für jeden Teilnehmer, den Sie einladen möchten, auf <b>Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Teilnehmers ein oder mappen Sie ihn.</p> </li> 
     <li> <p><strong>[!UICONTROL email]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Teilnehmers ein oder mappen Sie sie.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kategorien]</td> 
   <td>Klicken Sie für jede Kategorie, die das Ereignis wie im Kalender angezeigt werden soll, auf <b>Element hinzufügen</b> und geben Sie die Kategorie ein oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ereignis löschen]

Dieses Aktionsmodul löscht ein vorhandenes Ereignis.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ereignis-ID]</td> 
   <td> <p>Geben Sie die ID des Ereignisses ein, das Sie löschen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ereignis abrufen]

Dieses Aktionsmodul ruft Details des angegebenen Ereignisses ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ereignis-ID]</td> 
   <td> <p>Geben Sie die ID des Ereignisses ein, zu dem Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ereignisse suchen]

Dieses Suchmodul ruft Details zu einem Ereignis ab, wenn das Ereignis im ausgewählten Kalender erstellt, aktualisiert, gelöscht, gestartet oder beendet wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kalendergruppen-ID]</td> 
   <td>Wählen Sie die [!UICONTROL Kalendergruppe] aus, die den Kalender enthält, in dem Sie Ereignisse beobachten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kalender]</td> 
   <td> <p>Wählen Sie den spezifischen Kalender aus, den Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL filter]</td> 
   <td> <p>Filterbedingungen festlegen, um Ergebnisse zu filtern. Sie können nach den folgenden Eigenschaften filtern:</p> 
    <ul> 
     <li>[!UICONTROL Betreff]</li> 
     <li>[!UICONTROL Ereignis-ID]</li> 
     <li>[!UICONTROL Erstellungsdatum Uhrzeit]</li> 
     <li>[!UICONTROL Datum der letzten Änderung]</li> 
     <li>[!UICONTROL Textvorschau]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortieren nach]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Ergebnisse sortieren möchten.</p> 
    <ul> 
     <li><strong>[!UICONTROL subject]</strong>, aufsteigend oder absteigend</li> 
     <li><strong>[!UICONTROL Erstellungsdatum Uhrzeit]</strong>, aufsteigend oder absteigend</li> 
     <li><strong>[!UICONTROL Datum der letzten Änderung]</strong>, aufsteigend oder absteigend</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Ereignissen ein, die Workfront Fusion während eines Szenario-Ausführungszyklus zurückgeben soll.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ereignis aktualisieren]

Dieses Aktionsmodul aktualisiert ein vorhandenes Ereignis.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ereignis-ID]</td> 
   <td>Geben Sie die ID des Ereignisses ein, das Sie aktualisieren möchten, ordnen Sie sie zu oder wählen Sie sie aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Betreff]</td> 
   <td> <p>Geben Sie einen neuen Titel für das Ereignis ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Startdatum]</td> 
   <td> Geben Sie einen einzigen Zeitpunkt ein, zu dem das Ereignis in einer kombinierten Datums- und Uhrzeitdarstellung beginnt. Verwenden Sie den <code>{date}T{time}</code> Format , z. B. <code>2017-08-29T04:00:00.0000000</code>. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enddatum]</td> 
   <td> Geben Sie einen einzigen Zeitpunkt ein, zu dem das Ereignis in einer kombinierten Datums- und Uhrzeitdarstellung endet. Verwenden Sie den <code>({date}T{time}</code> Format , z. B. <code>2017-08-29T04:00:00.0000000</code>. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL reminder on]</td> 
   <td>Wählen Sie aus, ob eine Erinnerung für dieses Ereignis aktiviert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL reminder]</td> 
   <td>Anzahl der Minuten vor Ereignisbeginn eingeben oder zuordnen, nach denen die Erinnerung Trigger werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wichtigkeit]</td> 
   <td> <p>Die Wichtigkeit dieses Ereignisses auswählen.</p> 
    <ul> 
     <li>[!UICONTROL Niedrig]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL Hoch]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>Wählen Sie die Empfindlichkeit dieses Ereignisses aus.</p> 
    <ul> 
     <li><strong>[!UICONTROL normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>Der Empfänger sieht die Nachricht "[!UICONTROL Please treat as Personal]".</p> </li> 
     <li> <p><strong>[!UICONTROL Privat]</strong> </p> <p>Der Empfänger sieht die Nachricht "[!UICONTROL Bitte als privat behandeln]". Dieses Ereignis wird von den Posteingangsregeln des Empfängers nicht weitergeleitet oder umgeleitet.</p> </li> 
     <li> <p><strong>[!UICONTROL VERTRAULICH]</strong> </p> <p>Der Empfänger sieht die Nachricht "[!UICONTROL Bitte als vertraulich behandeln]". </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hauptteil-Inhaltstyp]</td> 
   <td>Wählen Sie aus, ob der Textinhalt der mit dem Ereignis verknüpften Nachricht Nur-Text oder HTML ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hauptteilinhalt]</td> 
   <td>Geben Sie den Text der Nachricht ein, die mit dem Ereignis verknüpft ist, oder mappen Sie ihn. Sie kann im HTML- oder Textformat vorliegen (wie im Feld [!UICONTROL Hauptteil-Inhaltstyp] weiter oben angegeben).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Speicherort]</td> 
   <td> <p>Details zum Veranstaltungsort eingeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Antwort angefordert]</td> 
   <td>Wählen Sie <strong>[!UICONTROL Yes]</strong> aus, um den Einladenden aufzufordern, eine Antwort auf die Ereigniseinladung zu senden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzeigen als]</td> 
   <td> <p>Wählen Sie aus, wie das Ereignis den Personen angezeigt werden soll, die Ihren Kalender anzeigen.</p> 
    <ul> 
     <li>[!UICONTROL FREE]</li> 
     <li>[!UICONTROL Tentative]</li> 
     <li>[!UICONTROL Besetzt]</li> 
     <li>[!UICONTROL Abwesend]</li> 
     <li>[!UICONTROL, anderswo arbeiten]</li> 
     <li>[!DNL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attendees]</p> </td> 
   <td> <p>Fügen Sie Teilnehmer der Veranstaltung hinzu.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Teilnehmers ein.</p> </li> 
     <li> <p><strong>[!UICONTROL email]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Teilnehmers ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kategorie]</td> 
   <td>Geben Sie die Kategorien ein, die das Ereignis wie im Kalender angezeigt werden soll, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ereignisse ansehen]

Dieses Kalendermodul ruft Details zu einem Trigger ab, wenn das Ereignis im ausgewählten Kalender erstellt, aktualisiert, gelöscht, gestartet oder beendet wird.

>[!NOTE]
>
>Um nach gelöschten Vorkommen einer Ereignisreihe zu suchen, wählen Sie [!UICONTROL Nach Aktualisierungszeit] im Feld [!UICONTROL Ereignisse ]. Dieses Modul überwacht nicht auf gelöschte einzelne Ereignisse oder gelöschte Ereignisreihen.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ereignisse beobachten]</td> 
   <td> <p>Wählen Sie aus, wie Sie Ereignisse ansehen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL nach Erstellungszeit]</strong> </p> <p>Achten Sie auf neue Ereignisse.</p> </li> 
     <li> <p><strong>[!UICONTROL nach Aktualisierungszeit]</strong> </p> <p>Auf aktualisierte Ereignisse achten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kalendergruppen-ID]</td> 
   <td>Wählen Sie die [!UICONTROL Kalendergruppe] aus, die den Kalender enthält, in dem Sie Ereignisse beobachten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kalender]</td> 
   <td> <p>Wählen Sie den spezifischen Kalender aus, den Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL filter]</td> 
   <td>Filterbedingungen festlegen, um Ergebnisse nach Betreff, Ereignis-ID oder Hauptteil zu filtern.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl an Nachrichten ein, die Workfront Fusion während eines Szenario-Ausführungszyklus zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Kalender

* [[!UICONTROL Kalender erstellen]](#create-a-calendar)
* [[!UICONTROL Löschen eines Kalenders]](#delete-a-calendar)
* [[!UICONTROL Kalender abrufen]](#get-a-calendar)
* [[!UICONTROL Kalender auflisten]](#list-calendars)
* [[!UICONTROL Aktualisieren eines Kalenders]](#update-a-calendar)



#### [!UICONTROL Kalender erstellen]

Dieses Aktionsmodul erstellt einen neuen Kalender in Ihrem Office 365-Konto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kalendername]</td> 
   <td> <p>Geben Sie einen Namen für den neuen Kalender ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Löschen eines Kalenders]

Dieses Aktionsmodul löscht einen vorhandenen Kalender.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kalenderkennung]</td> 
   <td>Geben Sie die [!UICONTROL Calendar]-ID für den Kalender ein, den Sie löschen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kalender abrufen]

Dieses Aktionsmodul ruft Details zu einem einzelnen Kalender ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kalenderkennung]</td> 
   <td> <p>Geben Sie die ID des Kalenders ein, zu dem Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kalender auflisten]

Dieses Suchmodul ruft eine Liste aller Kalender der authentifizierten Benutzenden ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kalendergruppen-ID]</td> 
   <td>Wählen Sie die [!UICONTROL Kalendergruppe] aus, die die Kalender enthält, die Sie auflisten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Kalendern ein, die Workfront Fusion während eines Szenario-Ausführungszyklus zurückgeben soll.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren eines Kalenders]

Dieses Aktionsmodul bearbeitet einen vorhandenen Kalender.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kalenderkennung]</td> 
   <td>Geben Sie die [!UICONTROL Kalender-ID] für den Kalender ein, den Sie aktualisieren möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Neuer Kalendername]</td> 
   <td> <p>Geben Sie einen neuen Namen für den Kalender ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

#### [!UICONTROL Erstellen eines API-Aufrufs]

Mit diesem Modul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://graph.microsoft.com</code> ein. Beispiel:<code> /v1.0/me/events</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Methode]</p> </td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Beispiel: <code>{"Content-type":"application/json"}</code>. Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p> Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:   <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
