---
title: Trello Module
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die Trello verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 5df5cd2b-ad4c-4a02-9d0c-7cee35232f93
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '5217'
ht-degree: 0%

---

# [!UICONTROL Trello]-Module

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!UICONTROL Trello] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um [!DNL Trello] Module verwenden zu können, müssen Sie über ein [!UICONTROL Trello]-Konto verfügen.

## Trello API-Informationen

Der Trello-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.trello.com/1</td>
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v4.12.37</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!UICONTROL Trello] mit [!DNL Workfront Fusion]

Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion]  - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!UICONTROL Trello]-Module und ihre Felder

Beim Konfigurieren von [!UICONTROL Trello]-Modulen zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können zusätzliche [!UICONTROL Trello]-Felder angezeigt werden, abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Pinnwände](#boards)
* [Listen](#lists)
* [Karten](#cards)
* [Abonnenten](#members)
* [Checklisten](#checklists)
* [Kennzeichnungen](#labels)
* [Kommentare](#comments)

### Pinnwände

+++ **[!UICONTROL Archivieren oder Aufheben der Archivierung einer Pinnwand]**

Dieses Aktionsmodul schließt (archiviert) oder öffnet eine angegebene Pinnwand erneut (archiviert).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Geben Sie die ID der Pinnwand ein, die Sie schließen oder erneut öffnen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archivieren oder Archivieren aufheben]</td> 
   <td> <p> Wählen Sie aus, ob Sie die Pinnwand schließen (archivieren) oder erneut öffnen (Archivierung aufheben) möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Mitglied einem Board zuweisen]**

Dieses Aktionsmodul weist einem Board, das Sie angeben, ein Mitglied zu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Wählen Sie die Pinnwand aus, der Sie ein Mitglied hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL E-Mail-Adresse]</td> 
   <td> <p> Geben Sie die E-Mail-Adresse des Mitglieds ein, das Sie der Pinnwand hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Membertyp]</p> </td> 
   <td> <p>Wählen Sie den Typ des Elements aus, das das neue Element sein soll.</p> 
    <ul> 
     <li><strong>[!UICONTROL Admin]</strong>: Ein Board-Administrator kann jede Board-Aktion ausführen.</li> 
     <li><strong>[!UICONTROL Normal]</strong>: Ein normales Mitglied ist einfach ein Mitglied des Board.</li> 
     <li><strong>[!UICONTROL Observer]</strong>: Ein Beobachter ist ein Mitglied mit schreibgeschütztem Zugriff auf das Board. <br>Beobachter stehen nur Teams mit [!UICONTROL Trello Business Class] zur Verfügung.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vollständiger Name]</td> 
   <td> <p> Geben Sie den vollständigen Namen des Benutzers ein, den Sie der Pinnwand hinzufügen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Pinnwand erstellen]**

Dieses Aktionsmodul erstellt eine neue Pinnwand mit den ausgewählten Einstellungen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen Namen für die neue Pinnwand ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td> <p>Geben Sie bei Bedarf die Beschreibung der Pinnwand ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organisations-ID]</p> </td> 
   <td> <p>Geben Sie die ID der Organisation ein oder mappen Sie sie. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Berechtigungsstufe]</p> </td> 
   <td> <p>Die Boards haben für jede Berechtigungsstufe unterschiedliche Abstimmungs- und Kommentierungsregeln. Wenn Ihr Board beispielsweise [!UICONTROL Private] ist und Sie die Abstimmungs- und Kommentar-Regeln auf [!UICONTROL All] setzen, erhalten Sie einen Fehler. </p> <p>Abstimmungen und Kommentare sind für jede Berechtigungsstufe auf die folgenden Gruppen beschränkt:</p> 
    <ul> 
     <li><strong>[!UICONTROL Privat]</strong>: 
      Mitglieder, Mitglieder und Beobachter</li> 
     <li><strong>[!UICONTROL für Organisation]</strong>: 
      Mitglieder, Mitglieder und Beobachter, Mitglieder der Organisation</li> 
     <li><strong>[!UICONTROL public]</strong>: 
      Mitglieder, Mitglieder und Beobachter, Organisationsmitglieder, Alle</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Abstimmung]</p> </td> 
   <td> <p>Wählen Sie eine Option aus, um festzulegen, wer auf diesem Board stimmen darf. Siehe das Feld [!UICONTROL Berechtigungsstufe] für Abstimmungseinschränkungen bei Berechtigungsebenen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kommentare]</p> </td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, wer Karten für diese Pinnwand kommentieren darf. Siehe das Feld [!UICONTROL Berechtigungsstufe] für Kommentare zu Einschränkungen bei Berechtigungsebenen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Einladungen]</p> </td> 
   <td> <p>Wählen Sie aus, wer andere Personen zu diesem Board einladen kann.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Self-Join]</p> </td> 
   <td> <p>Wählen Sie aus, ob die Team-Mitglieder dem Board selbst beitreten können oder eingeladen werden müssen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Standardbeschriftungen]</p> </td> 
   <td> <p>Wählen Sie aus, ob der Standardsatz von Beschriftungen für die neue Pinnwand verwendet werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Standardlisten]</p> </td> 
   <td> <p>Wählen Sie aus, ob der Pinnwand der Standardsatz von Listen ([!UICONTROL To Do], [!UICONTROL Doing], [!UICONTROL Done]) hinzugefügt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board-Quell-ID]</p> </td> 
   <td> <p>Wählen Sie die ID der Pinnwand aus, die Sie in die neue Pinnwand kopieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kartenabdeckungen]</p> </td> 
   <td> <p>Wählen Sie <strong>[!UICONTROL Yes]</strong> aus, wenn Sie Kartenabdeckungen für die Pinnwand aktivieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Hintergrund]</p> </td> 
   <td> <p>Wählen Sie die Hintergrundfarbe oder den benutzerdefinierten Hintergrund aus.</p> <p>Hinweis: Benutzerdefinierte Hintergründe stehen nur [!UICONTROL Trello Gold and Business Class]-Abonnenten zur Verfügung.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hintergrundkennung]</td> 
   <td> <p> Wenn Sie die Verwendung eines benutzerdefinierten Hintergrunds im Feld [!UICONTROL Background] ausgewählt haben, geben Sie die ID des Hintergrunds ein, den Sie verwenden möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Karte wird gealtert]</p> </td> 
   <td> <p>Wählen Sie zwischen zwei Modi für die Kartenalterung. </p> 
    <ul> 
     <li><strong>[!UICONTROL Pirate mode]</strong>: Die Karten werden reißen, gelb werden und brechen wie eine alte Piratenkarte, wenn sie altern.</li> 
     <li><strong>[!UICONTROL Regulärer Modus ]</strong>: Karten werden mit zunehmendem Alter immer transparenter. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Pinnwand bearbeiten]**

Dieses Aktionsmodul bearbeitet die Einstellungen einer vorhandenen Pinnwand.

>[!SUCCESS]
>
><table style="table-layout:auto">
<col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>Geben Sie die eindeutige [!UICONTROL Trello]-ID der Pinnwand ein, die das Modul erstellen soll, oder ordnen Sie sie zu. Sie können die Board-ID mit einem anderen Modul abrufen, z. B. dem Modul Pinnwände beobachten .</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/watch-boards.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Neuer Name]</td> 
   <td> <p> Geben Sie einen neuen Namen für die Pinnwand ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Neue Beschreibung]</td> 
   <td> <p> Eine neue Pinnwand-Beschreibung eingeben oder zuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organisations-ID]</p> </td> 
   <td> <p>Geben Sie die eindeutige [!UICONTROL Trello]-ID der Pinnwand ein, die das Modul bearbeiten soll, oder ordnen Sie sie zu.  </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL abonnieren] </td> 
   <td> <p>Wählen Sie eine Option, um anzugeben, ob der Benutzer, dem die von diesem Modul verwendete Verbindung gehört, die Pinnwand abonniert hat.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Berechtigungsstufe]</p> </td> 
   <td> <p>Die Boards haben für jede Berechtigungsstufe unterschiedliche Abstimmungs- und Kommentierungsregeln. Beispiel: Wenn Ihr Board [!UICONTROL Private] ist und Sie die Abstimmungs- und Kommentar-Regeln auf [!UICONTROL All] setzen, erhalten Sie einen Fehler. </p> <p>Abstimmungen und Kommentare sind für jede Berechtigungsstufe auf die folgenden Gruppen beschränkt:</p> 
    <ul> 
     <li><strong>[!UICONTROL Privat]</strong>: 
      Mitglieder, Mitglieder und Beobachter</li> 
     <li><strong>[!UICONTROL für Organisation]</strong>: 
      Mitglieder, Mitglieder und Beobachter, Mitglieder der Organisation</li> 
     <li><strong>[!UICONTROL public]</strong>: 
      Mitglieder, Mitglieder und Beobachter, Organisationsmitglieder, Alle</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Abstimmung]</p> </td> 
   <td> <p>Wählen Sie eine Option aus, um festzulegen, wer auf diesem Board stimmen darf. Siehe das Feld [!UICONTROL Berechtigungsstufe] für Abstimmungseinschränkungen bei Berechtigungsebenen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kommentare]</p> </td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, wer Karten für diese Pinnwand kommentieren darf. Siehe das Feld [!UICONTROL Berechtigungsstufe] für Kommentare zu Einschränkungen bei Berechtigungsebenen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Einladungen] </td> 
   <td> <p>Wählen Sie aus, wer Personen zu diesem Board einladen kann.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-Join]</td> 
   <td> <p> Wählen Sie aus, ob die Team-Mitglieder dem Board selbst beitreten können oder eingeladen werden müssen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kartenabdeckungen]</td> 
   <td> <p> Wählen Sie aus, ob Kartenabdeckungen auf dieser Pinnwand angezeigt werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Hintergrund] </td> 
   <td> <p>Wählen Sie die Hintergrundfarbe oder den benutzerdefinierten Hintergrund aus.</p> <p>Hinweis: Benutzerdefinierte Hintergründe stehen nur [!UICONTROL Trello Gold and Business Class]-Abonnenten zur Verfügung.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hintergrundkennung]</td> 
   <td> <p> Wenn Sie die Verwendung eines benutzerdefinierten Hintergrunds im Feld [!UICONTROL Background] ausgewählt haben, geben Sie die ID des Hintergrunds ein, den Sie verwenden möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Karte wird gealtert]</p> </td> 
   <td> <p>Wählen Sie zwischen zwei Modi für die Kartenalterung. </p> 
    <ul> 
     <li><strong>[!UICONTROL Pirate mode]</strong>: Die Karten werden reißen, gelb werden und brechen wie eine alte Piratenkarte, wenn sie altern.</li> 
     <li><strong>[!UICONTROL Regulärer Modus]</strong>: Karten werden mit zunehmendem Alter immer transparenter. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kalenderfeed aktiviert]</td> 
   <td> <p> Wählen Sie aus, ob der Kalenderfeed aktiviert ist oder nicht.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL &lt;color&gt; Titelname]</td> 
   <td> <p> Weisen Sie dem gewünschten Farblabel einen Namen zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Archiv] </td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, ob Sie die Pinnwand archivieren (schließen) möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **[!UICONTROL Pinnwand abrufen]**

Dieses Aktionsmodul ruft die Details einer Pinnwand ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>Geben Sie die ID der Pinnwand ein, zu der Sie Informationen abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!DNL Search for Boards]**

Dieses Suchmodul ruft Informationen zu einer Pinnwand ab, die Sie angeben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Abfrage] </td> 
   <td> <p>Geben Sie den Namen (oder einen Teil des Namens) der Pinnwand ein, zu der Sie Informationen erhalten möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl zurückgegebener Pinnwände]</td> 
   <td> <p> Geben Sie die maximale Anzahl an Pinnwänden ein, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben möchten. Dieser Wert muss kleiner oder gleich 1.000 sein.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Partial] </p> </td> 
   <td> <p>Standardmäßig durchsucht dieses Modul den Mitgliederinhalt nach exakten Übereinstimmungen der einzelnen Wörter in Ihrer Abfrage. Wenn [!UICONTROL Partial] aktiviert ist, sucht das Modul nach Inhalten, die mit einem beliebigen Wort in der Abfrage beginnen.</p> <p> Wenn Sie beispielsweise das Wort „Entwicklung“ verwenden, um nach einer Pinnwand mit dem Titel „Mein Entwicklungsstatusbericht“ zu suchen, müssen Sie standardmäßig nach dem gesamten Wort suchen. Wenn Sie [!UICONTROL Partial] aktiviert haben, können Sie nach „dev“, aber nicht nach „development“ suchen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pinnwände] </td> 
   <td> <p>Geben Sie „meine“ ein oder ordnen Sie eine kommagetrennte Liste von Board-IDs zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Zuweisung eines Mitglieds zu einem Board aufheben]**

Dieses Aktionsmodul entfernt ein Mitglied aus einer Pinnwand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Geben Sie die ID der Pinnwand ein (zuordnen oder auswählen), aus der Sie den Benutzer entfernen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Member] </td> 
   <td> <p>Wählen Sie das Mitglied aus, das Sie aus der Pinnwand entfernen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Pinnwände ansehen]**

Dieses Trigger-Modul beginnt ein Szenario, wenn eine neue Pinnwand hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Pinnwänden ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Listen

+++ **[!UICONTROL Liste erstellen]**

Dieses Aktionsmodul erstellt eine Liste auf einer Pinnwand, für die Sie angeben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Geben Sie die ID der Pinnwand ein, auf der Sie eine Liste erstellen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen Namen für die neue Liste ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Position] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Liste oben hinzufügen oder unten auf der Karte anhängen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Liste kopieren]</td> 
   <td> <p> Wenn Sie eine Liste kopieren, wählen Sie aus, wie Sie die ID der zu kopierenden Liste eingeben möchten.</p> 
    <ul> 
     <li> <p><strong>Manuell eingeben</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL List ID]</strong> die ID der Liste ein, die Sie kopieren möchten, oder ordnen Sie sie zu.<br></p> </li> 
     <li> <p><strong>Auswählen</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Liste enthält, die Sie kopieren möchten, und klicken Sie dann auf die Liste.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Liste bearbeiten]**

Dieses Aktionsmodul bearbeitet eine vorhandene Liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listen-ID]</td> 
   <td> <p> Geben Sie die ID der Liste ein, die Sie aktualisieren möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen neuen Namen für die Liste ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Ordnen Sie die Pinnwand zu, auf die Sie die Liste verschieben möchten, oder wählen Sie sie aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Position] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Liste oben hinzufügen oder unten auf der Karte anhängen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL abonniert]</td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie das aktive Mitglied der Liste abonnieren möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Liste abrufen]**

Dieses Aktionsmodul ruft Details zu einer bestimmten Liste ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Listen-ID]</p> </td> 
   <td> <p>Geben Sie die ID der Liste ein, zu der Sie Informationen abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Karten ansehen, die in eine Liste verschoben werden]**

Dieses Kartenmodul wird aktiviert, wenn eine Trigger in eine bestimmte Liste verschoben wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Pinnwand]</td> 
   <td>Wählen Sie die Pinnwand aus, die die Liste enthält, die Sie auf Karten überprüfen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Liste]</td> 
   <td>Wählen Sie die Liste aus, die Sie auf Karten überwachen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Karten

+++ **[!UICONTROL Anlage hinzufügen]**

Dieses Aktionsmodul fügt der ausgewählten Karte einen Anhang hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Karten-ID eingeben]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, der Sie einen Anhang hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>Manuell eingeben</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, der Sie einen Anhang hinzufügen möchten, oder ordnen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, auf der sich die Karte befindet, der Sie eine Anlage hinzufügen möchten, wählen Sie dann die Liste mit der Karte aus und klicken Sie auf die Karte.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anlagentyp]</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie die Datei direkt hochladen oder eine URL zur Datei angeben möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL-Datei]</strong> </p> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </li> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Geben Sie die URL zur Datei und einen Namen für den Anhang an.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archivieren oder Aufheben der Archivierung einer Karte]**

Dieses Aktionsmodul archiviert oder sendet eine Karte zurück an die Pinnwand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kartenkennung]</td> 
   <td> <p> Geben Sie die ID der Karte ein, die Sie archivieren oder an die Pinnwand zurücksenden möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archivieren oder Archivieren aufheben]</td> 
   <td> <p> Wählen Sie aus, ob Sie die Karte schließen (Archiv) oder an die Pinnwand zurücksenden möchten (Archivierung aufheben).</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Karte erstellen]**

Dieses Aktionsmodul erstellt eine Karte in einer ausgewählten Liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listenkennung eingeben]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Liste eingeben möchten, der Sie eine Karte hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL List ID]</strong> die ID der Liste ein, der Sie eine Karte hinzufügen möchten, oder ordnen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Liste enthält, der Sie eine Karte hinzufügen möchten, und wählen Sie dann die Liste aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kennzeichnungen] </td> 
   <td> <p>Klicken Sie für jede Beschriftung, die Sie der Karte hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die ID der Beschriftung ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Member]</td> 
   <td>Klicken Sie für jedes Mitglied, das Sie der Karte hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die ID des Mitglieds ein. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen Namen für die neue Karte ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Beschreibung]</p> </td> 
   <td> <p>Geben Sie eine Beschreibung für die Karte ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Position] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Karte oben hinzufügen möchten oder ob Sie die Karte am Ende der Liste anhängen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fälligkeitsdatum]</td> 
   <td> <p> Geben Sie ein Fälligkeitsdatum für die Karte ein. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Aktivieren Sie diese Option, um die Karte am Fälligkeitsdatum als abgeschlossen zu markieren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei URL]</td> 
   <td> <p>Geben Sie die URL einer Datei ein, die Sie der Karte als Anhang hinzufügen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Source-Datei]</p> </td> 
   <td> <p>Geben Sie Informationen zu einer Datei ein, die Sie der Karte als Anhang hinzufügen möchten, oder ordnen Sie sie zu. Wählen Sie eine Datei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Datei zu</p> 
     <p>Hinweis: Pro Anhang gibt es eine Beschränkung von 10 MB für Datei-Uploads. Die [!UICONTROL Business Class]- und [!UICONTROL Trello Gold]-Mitglieder haben jedoch eine Dateiuploadbegrenzung von 250 MB pro Anhang.</p> 
     </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Karte kopieren]</td> 
   <td> <p> Wenn Sie eine neue Karte als Kopie einer vorhandenen Karte erstellen, wählen Sie aus, wie Sie die ID der Karte eingeben möchten, die Sie kopieren möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, die Sie kopieren möchten, oder ordnen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, die Sie kopieren möchten, und klicken Sie auf die Liste mit der Karte. Wählen Sie dann die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Karte bearbeiten]**

Dieses Aktionsmodul bearbeitet eine vorhandene Karte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kartenkennung eingeben]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, die Sie bearbeiten möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, die Sie bearbeiten möchten, oder ordnen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, die Sie bearbeiten möchten, wählen Sie dann die Liste mit der Karte aus und klicken Sie auf die Karte.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Neuer Name]</td> 
   <td> <p>Geben Sie einen neuen Namen für die Karte ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Neue Beschreibung]</p> </td> 
   <td> <p>Geben Sie eine neue Beschreibung für die Karte ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Karte verschieben]</p> </td> 
   <td> <p>Wählen Sie die Pinnwand oder die Pinnwand aus und geben Sie an, wohin die Karte verschoben werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kennzeichnungen] </td> 
   <td> <p>Klicken Sie für jede Beschriftung, die Sie der Karte hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die ID der Beschriftung ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Position] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Karte oben hinzufügen möchten oder [!UICONTROL hängen] Sie die Karte am Ende der Liste an.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fälligkeitsdatum]</td> 
   <td> <p> Geben Sie ein Fälligkeitsdatum für die Karte ein. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Aktivieren Sie diese Option, um die Karte am Fälligkeitsdatum als abgeschlossen zu markieren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Member] </td> 
   <td> <p>Klicken Sie für jedes Mitglied, das Sie der Karte hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die ID des Mitglieds ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anlagenabdeckung-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Bildanhangs ein, den die Karte als Cover verwenden soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL abonnieren] </td> 
   <td> <p>Wählen Sie aus, ob das Mitglied die Karte abonnieren soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Archiv] </td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, ob Sie die Karte archivieren (schließen) möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Erhalte eine Karte]**

Dieses Aktionsmodul ruft die Details einer ausgewählten Karte ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p>Geben Sie die ID der Pinnwand ein, die die Karte enthält, zu der Sie Details abrufen möchten. Auf diese Weise können Sie die Namen der benutzerdefinierten Felder der Pinnwand anzeigen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Karten-ID eingeben]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, zu der Sie Details abrufen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, zu der Sie Details abrufen möchten, oder ordnen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, auf der sich die Karte befindet, zu der Sie Details abrufen möchten, wählen Sie dann die Liste aus, auf der sich die Karte befindet, und wählen Sie dann die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Nach Karten suchen]**

Dieses Aktionsmodul gibt Karten zurück, die mit der Suchanfrage übereinstimmen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Pinnwand] </td> 
   <td> <p>Wählen Sie die Pinnwände aus, die Sie durchsuchen möchten. Wenn keine Pinnwand ausgewählt ist, werden alle Pinnwände durchsucht.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Abfrage]</p> </td> 
   <td> <p>Geben Sie die Suchanfrage ein. Sie können Ihre Suche mithilfe der folgenden Suchoperatoren verfeinern:</p> 
    <ul> 
     <li><code><strong>-operator</strong></code> <p>Sie können "-" zu jedem Operator hinzufügen, um eine negative Suche durchzuführen, z. B. <code>[!UICONTROL -has:members]</code> nach Karten zu suchen, ohne dass ein Mitglied zugewiesen ist.</p> </li> 
     <li><code><strong>@name</strong></code> <p>Gibt Karten zurück, die einem Mitglied zugewiesen wurden. Sie können auch <code>member:</code> verwenden. Verwenden Sie <code>@me</code>, um nur Ihre Karten einzubeziehen.</p> </li> 
     <li><code><strong>#label</strong></code> <p>Gibt beschriftete Karten zurück. Sie können auch <code>label:</code> verwenden. Beispielsweise gibt <code>label:"FIX IT"</code> Karten mit der Bezeichnung „FEHLERBEHEBUNG“ zurück.</p> </li> 
     <li><code><strong>board:id</strong></code> <p>Gibt Karten innerhalb einer bestimmten Pinnwand zurück. Beispielsweise gibt <code>board:Trello</code> Karten auf Pinnwänden mit [!UICONTROL Trello] im Namen der Pinnwand zurück.</p> </li> 
     <li><code><strong>list:name</strong></code> <p>Gibt Karten in der Liste mit dem Namen „name“ zurück.</p> </li> 
     <li><code><strong>has:attachments</strong></code> <p>Gibt Karten mit Anhängen zurück. Der Operator <code>has</code>: kann auch mit anderen Attributen verwendet werden, z. B. <code>has:description</code>, <code>has:cover</code>, <code>has:members</code> oder <code>has:stickers</code>.</p> </li> 
     <li><code><strong>due:day</strong></code> <p>Gibt Karten zurück, die innerhalb von 24 Stunden fällig sind. Der <code>due:</code>-Operator kann auch mit anderen Zeitrahmen verwendet werden, z. B. <code>due:week</code>, <code>due:month</code> oder <code>due:overdue</code>. Sie können auch nach einem bestimmten Tagesbereich suchen. Das Hinzufügen von <code>due:14</code> zur Suche umfasst beispielsweise Karten, die in den nächsten 14 Tagen fällig sind.</p> </li> 
     <li><code><strong>created:day</strong></code> <p>Gibt Karten zurück, die in den letzten 24 Stunden erstellt wurden. Der <code> created:</code>Operator kann auch mit anderen Zeitrahmen wie <code>created:week</code> oder <code>created:month</code> verwendet werden. Sie können auch nach einem bestimmten Tagesbereich suchen. Wenn Sie beispielsweise <code>created:14</code> zur Suche hinzufügen, werden auch die Karten einbezogen, die in den letzten 14 Tagen erstellt wurden.</p> </li> 
     <li><code><strong>edited:day</strong></code> <p>Gibt die Karten zurück, die in den letzten 24 Stunden bearbeitet wurden. Der <code>edited:</code> Operator kann auch mit anderen Zeitrahmen verwendet werden, z. B. <code>edited:week</code> oder <code>edited:month</code>. Sie können auch nach einem bestimmten Tagesbereich suchen. Wenn Sie beispielsweise der Suche <code>edited:21</code> hinzufügen, werden die Karten berücksichtigt, die in den letzten 21 Tagen bearbeitet wurden.</p> </li> 
     <li><code><strong>description:</strong>, <strong>checklist:</strong>, <strong>comment:</strong>, and <strong>name:</strong></code> <p>Gibt Karten zurück, die mit dem Text der Kartenbeschreibungen, Checklisten, Kommentare oder Namen übereinstimmen. Beispielsweise gibt <code>comment:"FIX IT"</code> in einem Kommentar Karten mit „FEHLERBEHEBUNG“ zurück.</p> </li> 
     <li><code><strong>is:open</strong> and <strong>is:archived</strong></code> <p>Gibt offene oder archivierte Karten zurück. Wenn keiner der Typen angegeben ist, gibt [!UICONTROL Trello] beide Typen zurück.</p> </li> 
     <li><code><strong>is:starred</strong> </code> <p>Enthält nur Karten auf mit Sternen versehenen Pinnwänden.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl zurückgegebener Karten]</td> 
   <td> <p> Geben Sie die maximale Anzahl an Karten ein, die Sie während eines Ausführungszyklus zurückgeben [!DNL Workfront Fusion], oder mappen Sie sie. Dieser Wert muss kleiner oder gleich 1.000 sein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>Standardmäßig durchsucht dieses Modul den Mitgliederinhalt nach exakten Übereinstimmungen der einzelnen Wörter in Ihrer Abfrage. Wenn [!UICONTROL Partial] aktiviert ist, sucht das Modul nach Inhalten, die mit einem beliebigen Wort in der Abfrage beginnen.</p> <p> Wenn Sie beispielsweise das Wort „Entwicklung“ verwenden, um nach einer Pinnwand mit dem Titel „Mein Entwicklungsstatusbericht“ zu suchen, müssen Sie standardmäßig nach dem gesamten Wort suchen. Wenn Sie [!UICONTROL Partial] aktiviert haben, können Sie nach „dev“, aber nicht nach „development“ suchen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Karten] </td> 
   <td> <p>Um nach bestimmten Karten zu suchen<b> klicken Sie auf </b>Element hinzufügen“ und fügen Sie die ID der Karte hinzu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Karten ansehen]**

Dieses Kartenmodul startet ein Trigger, wenn eine neue Karte hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Überwachtes Objekt]</td> 
   <td> <p>Wählen Sie den Ort aus, an dem Sie auf Karten achten möchten.</p> 
    <ul> 
     <li><strong>[!UICONTROL Alle Karten]</strong> </li> 
     <li> <p><strong>Karten auf einer bestimmten Pinnwand</strong> </p> <p>Wählen Sie die Pinnwand aus, die Sie auf Karten überwachen möchten</p> </li> 
     <li> <p><strong>[!UICONTROL Karten auf einer bestimmten Liste]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Liste enthält, die Sie auf Karten überprüfen möchten, und wählen Sie dann die Liste aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Abonnenten

+++ **[!UICONTROL Mitglied zu einer Karte hinzufügen]**

Dieses Aktionsmodul fügt das angegebene Mitglied zur angegebenen Karte hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Karten-ID und Mitglieder-ID eingeben]</p> </td> 
   <td> <p>Wählen Sie aus, wie Sie die Karten-ID und die Mitglieds-ID eingeben möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Card ID]</strong> und die <strong>[!UICONTROL Member ID]</strong> ein oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, der Sie ein Mitglied hinzufügen möchten, und wählen Sie dann die Liste aus, die die Karte, die Karte selbst und das Mitglied enthält, das Sie der Karte hinzufügen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Mitglied einem Board zuweisen]**

Siehe [!UICONTROL Zuweisen eines Mitglieds zu einem ]&quot; unter [Pinnwände](#boards).

+++

+++ **[!UICONTROL Mitglieder suchen]**

Dieses Aktionsmodul ruft Informationen über [!UICONTROL Trello]-Mitglieder ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Abfrage] </td> 
   <td> <p>Geben Sie den Namen oder Benutzernamen des Benutzers ein, den Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>Standardmäßig durchsucht dieses Modul den Mitgliederinhalt nach exakten Übereinstimmungen der einzelnen Wörter in Ihrer Abfrage. Wenn [!UICONTROL Partial] aktiviert ist, sucht das Modul nach Inhalten, die mit einem beliebigen Wort in der Abfrage beginnen.</p> <p> Wenn Sie beispielsweise das Wort „Entwicklung“ verwenden, um nach einer Pinnwand mit dem Titel „Mein Entwicklungsstatusbericht“ zu suchen, müssen Sie standardmäßig nach dem gesamten Wort suchen. Wenn Sie [!UICONTROL Partial] aktiviert haben, können Sie nach „dev“, aber nicht nach „development“ suchen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Member]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Zuweisung eines Mitglieds zu einem Board aufheben]**

Siehe [!UICONTROL Zuweisung eines Mitglieds zu einem Board aufheben] unter [Boards](#boards).

+++

### Checklisten

+++ **[!UICONTROL Erstellen einer Checkliste]**

Dieses Aktionsmodul erstellt eine Checkliste für die ausgewählte Karte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kartenkennung eingeben]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, der Sie eine Checkliste hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, der Sie eine Checkliste hinzufügen möchten, oder ordnen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, auf der sich die Karte befindet, der Sie eine Checkliste hinzufügen möchten, wählen Sie dann die Liste aus, auf der sich die Karte befindet, und wählen Sie die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen Namen für die Checkliste ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Position] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Checkliste oben hinzufügen möchten oder ob Sie die Checkliste am unteren Rand der Karte anhängen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Checklisten-ID eingeben]</p> </td> 
   <td> <p>Wenn Sie die Checkliste durch Kopieren einer vorhandenen Checkliste erstellen, geben Sie die ID einer Quell-Checkliste, die Sie kopieren möchten, in die neue ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Erstellen eines Checklisten-Elements]**

Dieses Aktionsmodul fügt ein Element zu einer bestimmten Checkliste hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Checklisten-ID eingeben]</td> 
   <td> <p> Wenn Sie eine neue Checkliste durch Kopieren einer vorhandenen Checkliste erstellen, wählen Sie aus, wie Sie die ID der Checkliste eingeben möchten, der Sie ein Element hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Checklist ID]</strong> die ID der Karte ein, der Sie eine Checkliste hinzufügen möchten, oder ordnen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, der Sie eine Checkliste hinzufügen möchten, wählen Sie dann die Liste aus, die die Karte enthält, wählen Sie dann die Karte aus und klicken Sie auf die Checkliste.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Elementname]</p> </td> 
   <td> <p>Geben Sie einen Namen für das neue Element ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Position]</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie das Element oben oder [!UICONTROL append] unten in der Checkliste hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL aktiviert]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie das Element wie bereits aktiviert hinzufügen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Checklisten-Element bearbeiten]**

Dieses Aktionsmodul bearbeitet eine vorhandene Checkliste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Karten-ID und Checklisten-Element-ID eingeben]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte und die Checkliste eingeben möchten, in der Sie ein Element bearbeiten möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Checklist ID]</strong> die ID der Karte ein, der Sie eine Checkliste hinzufügen möchten, oder ordnen Sie sie zu.</p> <p>Geben Sie im Feld <strong>[!UICONTROL Checklist Item ID]</strong> die ID der Checkliste ein oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, der Sie eine Checkliste hinzufügen möchten, wählen Sie dann die Liste aus, die die Karte enthält, wählen Sie dann die Karte aus und klicken Sie auf die Checkliste.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Checklist ID]</td> 
   <td>Wählen Sie die Checkliste aus, in die Sie das Checklisten-Element verschieben möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Elementname]</p> </td> 
   <td> <p>Geben Sie einen Namen für das neue Element ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Position]</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie das Element oben hinzufügen oder am Ende der Checkliste anhängen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Status]</p> </td> 
   <td> <p>Auswählen, ob das Checklisten-Element vollständig oder unvollständig ist.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Kennzeichnungen

+++ **[!UICONTROL Fügen Sie einer Karte einen Titel hinzu]**

Dieses Aktionsmodul fügt einer ausgewählten Karte einen Titel hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Karten-ID eingeben]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, der Sie eine Checkliste hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, der Sie eine Checkliste hinzufügen möchten, oder ordnen Sie sie zu. Geben <strong> im Feld[!UICONTROL Label ID]</strong> die ID der Beschriftung ein, die Sie hinzufügen möchten, oder ordnen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, auf der sich die Karte befindet, der Sie eine Checkliste hinzufügen möchten, wählen Sie dann die Liste aus, auf der sich die Karte befindet, und wählen Sie die Karte aus. </p> <p>Wählen Sie den Titel aus, den Sie der Karte hinzufügen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Kommentare

+++ **[!UICONTROL Kommentar in einer Karte erstellen]**

Dieses Aktionsmodul fügt einen Kommentar zu einer ausgewählten Karte hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kartenkennung eingeben]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, zu der Sie einen Kommentar hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, zu der Sie einen Kommentar hinzufügen möchten, oder mappen Sie sie ihr zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, zu der Sie einen Kommentar hinzufügen möchten, wählen Sie dann die Liste aus, die die Karte enthält, und wählen Sie dann die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kommentar] </td> 
   <td> <p>Geben Sie den Kommentar ein, den Sie der ausgewählten Karte hinzufügen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Kommentare in einer Karte auflisten]**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kartenkennung eingeben]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, zu der Sie einen Kommentar hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, zu der Sie einen Kommentar hinzufügen möchten, oder mappen Sie sie ihr zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, zu der Sie einen Kommentar hinzufügen möchten, wählen Sie dann die Liste aus, die die Karte enthält, und wählen Sie dann die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Kommentare]</td> 
   <td> <p> Geben Sie die maximale Anzahl an Kommentaren ein, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL seit] </td> 
   <td> <p>Legen Sie das Startdatum des Zeitraums fest, in dem der Kommentar erstellt wurde. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL davor] </td> 
   <td> <p>Legen Sie das Enddatum des Zeitraums fest, in dem der Kommentar erstellt wurde. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Kommentare ansehen]**

Dieses Trigger-Modul startet ein Szenario, wenn ein Kommentar hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Überwachtes Objekt]</td> 
   <td> <p>Wählen Sie den Ort aus, auf den Sie nach Kommentaren achten möchten.</p> 
    <ul> 
     <li><strong>[!UICONTROL Alle Karten] überall</strong> </li> 
     <li> <p><strong>[!UICONTROL Board]</strong> </p> <p>Pinnwand auswählen, auf der Kommentare angezeigt werden sollen</p> </li> 
     <li> <p><strong>[!UICONTROL-Liste]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Liste enthält, die Sie auf Kommentare überwachen möchten, und wählen Sie dann die Liste aus.</p> </li> 
     <li><strong>[!UICONTROL-Karte]</strong> </li> 
     <li>Wählen Sie die Pinnwand aus, die die Karte enthält, die Sie auf Kommentare überwachen möchten, wählen Sie dann die Liste aus, die die Karte enthält, und wählen Sie dann die Karte aus.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Kommentaren ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

## [!UICONTROL trello] Objekt-IDs

* [So finden Sie die ID oder den Shortlink einer Karte in [!DNL Trello]](#how-to-find-the-id-or-the-shortlink-of-a-card-in-trello)
* [So finden Sie IDs anderer Objekte in [!DNL Trello]](#how-to-find-ids-of-other-objects-in-trello)

### So finden Sie die ID oder den Shortlink einer Karte in [!DNL Trello]

Wenn Sie eine Karte bearbeiten oder einen neuen Kommentar erstellen möchten, müssen Sie die ID der Karte oder deren Shortlink kennen. Diese Information können Sie der Ausgabe des Triggers [!UICONTROL Neue Karte] entnehmen. Der Shortlink für eine Karte kann auch durch Öffnen der Karte und Klicken auf die Schaltfläche [!UICONTROL Freigeben] abgerufen werden. Den Shortlink finden Sie im Feld [!UICONTROL Link zu dieser Karte] am Ende der URL nach der `https://trello.com/c/`.

![Freigeben und mehr](/help/workfront-fusion/references/apps-and-modules/assets/share-and-more-350x575.png)

### So finden Sie IDs anderer Objekte in [!DNL Trello]

Pinnwand-, Listen- und Kommentar-IDs können nur über Trigger abgerufen werden. Auf der [!DNL `trello.com`]-Website werden diese IDs nicht angezeigt.
