---
title: Trello Module
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die Trello verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 5df5cd2b-ad4c-4a02-9d0c-7cee35232f93
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '4259'
ht-degree: 0%

---

# [!UICONTROL Trello]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!UICONTROL Trello] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um [!DNL Trello]-Module verwenden zu können, müssen Sie über ein [!UICONTROL Trello]-Konto verfügen.

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

## [!UICONTROL Trello] mit [!DNL Workfront Fusion] verbinden

Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion]  - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!UICONTROL Trello] Module und ihre Felder

Beim Konfigurieren [!UICONTROL Trello] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!UICONTROL Trello] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

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

+++ **[!UICONTROL Watch Boards]**

Dieses Trigger-Modul beginnt ein Szenario, wenn eine neue Pinnwand hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Die maximale Anzahl an Boards, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Board]**

Dieses Aktionsmodul erstellt eine neue Pinnwand mit den ausgewählten Einstellungen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen Namen für die neue Pinnwand ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Geben Sie bei Bedarf die Beschreibung der Pinnwand ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>Geben Sie die ID der Organisation ein oder mappen Sie sie. Die Organisations-ID kann mit einem anderen Modul abgerufen werden, z. B. mit dem Modul Aktivitäten beobachten .</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/id-of-org.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>Die Boards haben für jede Berechtigungsstufe unterschiedliche Abstimmungs- und Kommentierungsregeln. Beispiel: Wenn Ihr Board [!UICONTROL Private] ist und Sie die Abstimmungs- und Kommentierungsregeln auf [!UICONTROL All] setzen, erhalten Sie einen Fehler. </p> <p>Abstimmungen und Kommentare sind für jede Berechtigungsstufe auf die folgenden Gruppen beschränkt:</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      —&gt;Mitglieder, Mitglieder und Beobachter</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      —&gt;Mitglieder, Mitglieder und Beobachter, Organisationsmitglieder</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      —&gt;Mitglieder, Mitglieder und Beobachter, Organisationsmitglieder, alle</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>Wählen Sie eine Option aus, um festzulegen, wer auf diesem Board stimmen darf. Siehe das Feld [!UICONTROL Permission level] für Abstimmungseinschränkungen bei Berechtigungsebenen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, wer Karten für diese Pinnwand kommentieren darf. Im Feld [!UICONTROL Permission level] finden Sie Kommentare zu Einschränkungen bei Berechtigungsebenen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Invitations]</p> </td> 
   <td> <p>Wählen Sie aus, wer andere Personen zu diesem Board einladen kann.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Self-join]</p> </td> 
   <td> <p>Wählen Sie aus, ob die Team-Mitglieder dem Board selbst beitreten können oder eingeladen werden müssen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default labels]</p> </td> 
   <td> <p>Wählen Sie aus, ob der Standardsatz von Beschriftungen für die neue Pinnwand verwendet werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default lists]</p> </td> 
   <td> <p>Wählen Sie aus, ob der Pinnwand der Standardsatz von Listen ([!UICONTROL To Do], [!UICONTROL Doing], [!UICONTROL Done]) hinzugefügt werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board source ID]</p> </td> 
   <td> <p>Wählen Sie die ID der Pinnwand aus, die Sie in die neue Pinnwand kopieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card Covers]</p> </td> 
   <td> <p>Wählen Sie <strong>[!UICONTROL Yes]</strong> aus, wenn Sie Kartenabdeckungen für die Pinnwand aktivieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Background]</p> </td> 
   <td> <p>Wählen Sie die Hintergrundfarbe oder den benutzerdefinierten Hintergrund aus.</p> <p>Hinweis: Benutzerdefinierte Hintergründe stehen nur [!UICONTROL Trello Gold and Business Class] Abonnenten zur Verfügung.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>Wählen Sie zwischen zwei Modi für die Kartenalterung. </p> 
    <ul> 
     <li><strong>[!UICONTROL Regular]</strong>: Karten werden mit zunehmendem Alter immer transparenter. </li> 
     <li><strong>[!UICONTROL Pirate]</strong>: Karten werden reißen, gelb und brechen wie eine alte Piratenkarte, während sie altern.</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Board]**

Dieses Aktionsmodul bearbeitet die Einstellungen einer vorhandenen Pinnwand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>Geben Sie die eindeutige [!UICONTROL Trello]-ID der Pinnwand ein, die das Modul erstellen soll, oder mappen Sie sie. Sie können die Board-ID mit einem anderen Modul abrufen, z. B. dem Modul Pinnwände beobachten .</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/watch-boards.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p> Geben Sie einen neuen Namen für die Pinnwand ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New description]</td> 
   <td> <p> Geben Sie bei Bedarf eine neue Pinnwand-Beschreibung ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>Geben Sie die eindeutige [!UICONTROL Trello]-ID der Pinnwand ein, die das Modul bearbeiten soll, oder mappen Sie sie. Sie können die Pinnwand-ID mit einem anderen Modul abrufen, z. B. mit dem Modul [!DNL Watch Activities] .</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/org-id.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, ob der handelnde Benutzer das Board abonniert hat.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>Die Boards haben für jede Berechtigungsstufe unterschiedliche Abstimmungs- und Kommentierungsregeln. Beispiel: Wenn Ihr Board [!UICONTROL Private] ist und Sie die Abstimmungs- und Kommentierungsregeln auf [!UICONTROL All] setzen, erhalten Sie einen Fehler. </p> <p>Abstimmungen und Kommentare sind für jede Berechtigungsstufe auf die folgenden Gruppen beschränkt:</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      —&gt;Mitglieder, Mitglieder und Beobachter</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      —&gt;Mitglieder, Mitglieder und Beobachter, Organisationsmitglieder</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      —&gt;Mitglieder, Mitglieder und Beobachter, Organisationsmitglieder, alle</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>Wählen Sie eine Option aus, um festzulegen, wer auf diesem Board stimmen darf. Siehe das Feld [!UICONTROL Permission level] für Abstimmungseinschränkungen bei Berechtigungsebenen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, wer Karten für diese Pinnwand kommentieren darf. Im Feld [!UICONTROL Permission level] finden Sie Kommentare zu Einschränkungen bei Berechtigungsebenen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Invitations] </td> 
   <td> <p>Wählen Sie aus, wer Personen zu diesem Board einladen kann.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-join]</td> 
   <td> <p> Wählen Sie aus, ob die Team-Mitglieder dem Board selbst beitreten können oder eingeladen werden müssen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card covers]</td> 
   <td> <p> Wählen Sie aus, ob Kartenabdeckungen auf dieser Pinnwand angezeigt werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background] </td> 
   <td> <p>Wählen Sie die Hintergrundfarbe oder den benutzerdefinierten Hintergrund aus.</p> <p>Hinweis: Benutzerdefinierte Hintergründe stehen nur [!UICONTROL Trello Gold and Business Class] Abonnenten zur Verfügung.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background ID]</td> 
   <td> <p> Wenn Sie ausgewählt haben, einen benutzerdefinierten Hintergrund im Feld "[!UICONTROL Background]" zu verwenden, geben Sie die ID des Hintergrunds, den Sie verwenden möchten, ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>Wählen Sie zwischen zwei Modi für die Kartenalterung. </p> 
    <ul> 
     <li><strong>[!UICONTROL Regular]</strong>: Karten werden mit zunehmendem Alter immer transparenter. </li> 
     <li><strong>[!UICONTROL Pirate]</strong>: Karten werden reißen, gelb und brechen wie eine alte Piratenkarte, während sie altern.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar feed enabled]</td> 
   <td> <p> Wählen Sie aus, ob der Kalenderfeed aktiviert ist oder nicht.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL <Color> label name]</td> 
   <td> <p> Weisen Sie dem gewünschten Farblabel einen Namen zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, ob Sie die Pinnwand archivieren (schließen) möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Board]**

Dieses Aktionsmodul ruft die Details einer Pinnwand ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Geben Sie den Namen (oder einen Teil des Namens) der Pinnwand ein, zu der Sie Informationen erhalten möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned boards]</td> 
   <td> <p> Geben Sie die maximale Anzahl an Pinnwänden ein, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben möchten. Dieser Wert muss kleiner oder gleich 1.000 sein.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Partial] </p> </td> 
   <td> <p>Standardmäßig durchsucht dieses Modul den Mitgliederinhalt nach exakten Übereinstimmungen der einzelnen Wörter in Ihrer Abfrage. Wenn [!UICONTROL Partial] aktiviert ist, sucht das Modul nach Inhalten, die mit einem beliebigen Wort in Ihrer Abfrage beginnen.</p> <p> Wenn Sie beispielsweise das Wort „Entwicklung“ verwenden, um nach einer Pinnwand mit dem Titel „Mein Entwicklungsstatusbericht“ zu suchen, müssen Sie standardmäßig nach dem gesamten Wort suchen. Wenn Sie [!UICONTROL Partial] aktiviert haben, können Sie nach „dev“ suchen, aber nicht nach „development“.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Boards] </td> 
   <td> <p>Geben Sie „meine“ ein oder ordnen Sie eine kommagetrennte Liste von Board-IDs zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archive or Unarchive a Board]**

Dieses Aktionsmodul schließt eine von Ihnen angegebene Pinnwand oder öffnet sie erneut.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Geben Sie die ID der Pinnwand ein, die Sie schließen oder erneut öffnen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> Wählen Sie aus, ob Sie die Pinnwand schließen (archivieren) oder erneut öffnen (Archivierung aufheben) möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assign a Member to a Board]**

Dieses Aktionsmodul weist einem Board, das Sie angeben, ein Mitglied zu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Wählen Sie die Pinnwand aus, der Sie ein Mitglied hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email address]</td> 
   <td> <p> Geben Sie die E-Mail-Adresse des Mitglieds ein, das Sie der Pinnwand hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Member type]</p> </td> 
   <td> <p>Wählen Sie den Typ des Mitglieds aus, das Sie der Pinnwand hinzufügen möchten.</p> 
    <ul> 
     <li><strong>[!UICONTROL Admin]</strong>: Ein Board-Administrator kann jede Board-Aktion ausführen.</li> 
     <li><strong>[!UICONTROL Normal]</strong>: Ein normales Mitglied ist einfach ein Mitglied des Board.</li> 
     <li><strong>[!UICONTROL Observer]</strong>: Ein Beobachter ist ein Mitglied mit schreibgeschütztem Zugriff auf das Board. <br>Beobachter stehen nur Teams mit [!UICONTROL Trello Business Class] zur Verfügung.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Full name]</td> 
   <td> <p> Geben Sie den vollständigen Namen des Benutzers ein, den Sie der Pinnwand hinzufügen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

Dieses Aktionsmodul entfernt ein Mitglied aus einer Pinnwand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Geben Sie die ID der Pinnwand ein (zuordnen oder auswählen), aus der Sie den Benutzer entfernen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Member] </td> 
   <td> <p>Wählen Sie das Mitglied aus, das Sie aus der Pinnwand entfernen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Listen

+++ **[!UICONTROL Watch cards moved to a list]**

Dieses Kartenmodul wird aktiviert, wenn eine Trigger in eine bestimmte Liste verschoben wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board]</td> 
   <td>Wählen Sie die Pinnwand aus, die die Liste enthält, die Sie auf Karten überprüfen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List]</td> 
   <td>Wählen Sie die Liste aus, die Sie auf Karten überwachen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Die maximale Anzahl an Karten, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p>  </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a List]**

Dieses Aktionsmodul erstellt eine Liste auf einer Pinnwand, für die Sie angeben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Liste oben hinzufügen oder unten auf der Karte anhängen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy list]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der zu kopierenden Liste eingeben möchten.</p> 
    <ul> 
     <li> <p><strong>Manuell eingeben</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL List ID]</strong> die ID der Liste ein, die Sie kopieren möchten, oder mappen Sie sie zu.<br></p> </li> 
     <li> <p><strong>Auswählen</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Liste enthält, die Sie kopieren möchten, und klicken Sie dann auf die Liste.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a List]**

Dieses Aktionsmodul bearbeitet eine vorhandene Liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
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
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Liste oben hinzufügen oder unten auf der Karte anhängen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribed]</td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie das aktive Mitglied der Liste abonnieren möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a List]**

Dieses Aktionsmodul ruft Details zu einer bestimmten Liste ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL List ID]</p> </td> 
   <td> <p>Geben Sie die ID der Liste ein, zu der Sie Informationen abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Karten

+++ **[!UICONTROL Watch cards]**

Dieses Kartenmodul wird aktiviert, wenn eine neue Trigger hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Wählen Sie den Ort aus, an dem Sie auf Karten achten möchten.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards]</strong> </li> 
     <li> <p><strong>Karten auf einer bestimmten Pinnwand</strong> </p> <p>Wählen Sie die Pinnwand aus, die Sie auf Karten überwachen möchten</p> </li> 
     <li> <p><strong>[!UICONTROL Cards on specific list]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Liste enthält, die Sie auf Karten überprüfen möchten, und wählen Sie dann die Liste aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Die maximale Anzahl an Karten, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a card]**

Dieses Aktionsmodul erstellt eine Karte in einer ausgewählten Liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a list ID]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Liste eingeben möchten, der Sie eine Karte hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL List ID]</strong> die ID der Liste ein, der Sie eine Karte hinzufügen möchten, oder mappen Sie sie.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Liste enthält, die Sie kopieren möchten, und klicken Sie dann auf die Liste.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>Geben Sie für jeden Titel, den Sie der Karte hinzufügen möchten, die ID des Titels ein. Die ID kann z. B. mithilfe des [!UICONTROL Retrieve Labels] abgerufen werden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members]</td> 
   <td>Geben Sie für jedes Mitglied, das Sie der Karte hinzufügen möchten, die ID des Mitglieds ein. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen Namen für die neue Karte ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Description]</p> </td> 
   <td> <p>Geben Sie eine Beschreibung für die Karte ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Karte oben hinzufügen oder unten in der Liste [!UICONTROL append] möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> Geben Sie ein Fälligkeitsdatum für die Karte ein. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Aktivieren Sie diese Option, um die Karte am Fälligkeitsdatum als abgeschlossen zu markieren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td> <p>Geben Sie die URL einer Datei ein, die Sie der Karte als Anhang hinzufügen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Source file]</p> </td> 
   <td> <p>Geben Sie Informationen zu einer Datei ein, die Sie der Karte als Anhang hinzufügen möchten, oder ordnen Sie sie zu.</p> 
    <ul> 
     <li>[!UICONTROL File name]: Geben Sie den Dateinamen einschließlich der Dateierweiterung ein oder ordnen Sie ihn zu.</li> 
     <li> 
     <p>Wählen Sie eine Datei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Datei zu</p> 
     <p>Hinweis: Pro Anhang gibt es eine Beschränkung von 10 MB für Datei-Uploads. [!UICONTROL Business Class]- und [!UICONTROL Trello Gold]-Mitglieder haben jedoch eine Dateiuploadbegrenzung von 250 MB pro Anhang.</p> 
     </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy card]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der zu kopierenden Karte eingeben möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, die Sie kopieren möchten, oder mappen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, die Sie kopieren möchten, und klicken Sie auf die Liste mit der Karte. Wählen Sie dann die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Card]**

Dieses Aktionsmodul bearbeitet eine vorhandene Karte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Card ID]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, die Sie bearbeiten möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, die Sie bearbeiten möchten, oder mappen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, die Sie bearbeiten möchten, wählen Sie dann die Liste mit der Karte aus und klicken Sie auf die Karte.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p>Geben Sie einen neuen Namen für die Karte ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New description]</p> </td> 
   <td> <p>Geben Sie eine neue Beschreibung für die Karte ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Move a card]</p> </td> 
   <td> <p>Wählen Sie die Pinnwand oder die Pinnwand aus und geben Sie an, wohin die Karte verschoben werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>Fügen Sie die IDs aller Kennzeichnungen hinzu, die Sie der Karte hinzufügen möchten. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Karte oben hinzufügen oder unten in der Liste [!UICONTROL append] möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> Geben Sie ein Fälligkeitsdatum für die Karte ein. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Wenn diese Option aktiviert ist, wird die Karte am Fälligkeitsdatum als abgeschlossen markiert.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members] </td> 
   <td> <p>Fügen Sie die ID aller Mitglieder hinzu, die Sie der Karte hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment cover ID]</p> </td> 
   <td> <p>Geben Sie die ID des Bildanhangs ein, den die Karte als Cover verwenden soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>Wählen Sie aus, ob das Mitglied die Karte abonnieren soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, ob Sie die Karte archivieren (schließen) möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Card]**

Dieses Aktionsmodul ruft die Details einer ausgewählten Karte ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p>Geben Sie die ID der Pinnwand ein, die die Karte enthält, zu der Sie Details abrufen möchten. Auf diese Weise können Sie die Namen der benutzerdefinierten Felder der Pinnwand anzeigen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, zu der Sie Details abrufen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, zu der Sie Details abrufen möchten, oder mappen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, auf der sich die Karte befindet, zu der Sie Details abrufen möchten, wählen Sie dann die Liste aus, auf der sich die Karte befindet, und wählen Sie dann die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search for Cards]**

Dieses Aktionsmodul gibt Karten zurück, die mit der Suchanfrage übereinstimmen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board] </td> 
   <td> <p>Wählen Sie die Pinnwände aus, die Sie durchsuchen möchten. Wenn keine Pinnwand ausgewählt ist, werden alle Pinnwände durchsucht.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Query]</p> </td> 
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
     <li><code><strong>description:</strong>, <strong>checklist:</strong>, <strong>comment:</strong>, and <strong>name:</strong></code> <p>Gibt Karten zurück, die mit dem Text der Kartenbeschreibungen, Checklisten, Kommentare oder Namen übereinstimmen. Beispielsweise gibt comment:„FIX IT“ Karten mit „FIX IT“ in einem Kommentar zurück.</p> </li> 
     <li><code><strong>is:open</strong> and <strong>is:archived</strong></code> <p>Gibt offene oder archivierte Karten zurück. Wenn keines von beiden angegeben ist, gibt [!UICONTROL Trello] beide Typen zurück.</p> </li> 
     <li><code><strong>is:starred</strong> </code> <p>Enthält nur Karten auf mit Sternen versehenen Pinnwänden.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned cards]</td> 
   <td> <p> Die maximale Anzahl an Karten, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben. Dieser Wert muss kleiner oder gleich 1.000 sein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>Standardmäßig durchsucht dieses Modul den Mitgliederinhalt nach exakten Übereinstimmungen der einzelnen Wörter in Ihrer Abfrage. Wenn [!UICONTROL Partial] aktiviert ist, sucht das Modul nach Inhalten, die mit einem beliebigen Wort in Ihrer Abfrage beginnen.</p> <p> Wenn Sie beispielsweise das Wort „Entwicklung“ verwenden, um nach einer Pinnwand mit dem Titel „Mein Entwicklungsstatusbericht“ zu suchen, müssen Sie standardmäßig nach dem gesamten Wort suchen. Wenn Sie [!UICONTROL Partial] aktiviert haben, können Sie nach „dev“ suchen, aber nicht nach „development“.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cards] </td> 
   <td> <p>Fügen Sie alle Karten hinzu, nach denen Sie gezielt suchen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archive or Unarchive a Card]**

Dieses Aktionsmodul archiviert oder sendet eine Karte zurück an die Pinnwand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card ID]</td> 
   <td> <p> Geben Sie die ID der Karte ein, die Sie archivieren oder an die Pinnwand zurücksenden möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> Wählen Sie aus, ob Sie die Karte schließen (Archiv) oder an die Pinnwand zurücksenden möchten (Archivierung aufheben).</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Add an Attachment]**

Dieses Aktionsmodul fügt der ausgewählten Karte einen Anhang hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, zu der Sie Details abrufen möchten.</p> 
    <ul> 
     <li> <p><strong>Manuell eingeben</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, zu der Sie Details abrufen möchten, oder mappen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, auf der sich die Karte befindet, zu der Sie Details abrufen möchten, wählen Sie dann die Liste aus, auf der sich die Karte befindet, und wählen Sie dann die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment type]</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie die Datei direkt hochladen oder eine URL zur Datei angeben möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </li> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Geben Sie die URL zur Datei und einen Namen für den Anhang an.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Abonnenten

+++ **[!UICONTROL Assign a Member to a Board]**

Siehe &quot;[!UICONTROL Assign a Member to a Board]&quot; unter [Pinnwände](#boards).

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

Siehe &quot;[!UICONTROL Unassign a Member from a Board]&quot; unter [Pinnwände](#boards).

+++

+++ **[!UICONTROL Add a Member to a Card]**

Dieses Aktionsmodul fügt das angegebene Mitglied zur angegebenen Karte hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter card ID and member ID]</p> </td> 
   <td> <p>Wählen Sie aus, wie Sie die Karten-ID und die Mitglieds-ID eingeben möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie die <strong>[!UICONTROL Card ID]</strong> und die <strong>[!UICONTROL Member ID]</strong> ein oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, der Sie ein Mitglied hinzufügen möchten, und wählen Sie dann die Liste aus, die die Karte, die Karte selbst und das Mitglied enthält, das Sie der Karte hinzufügen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search for Members]**

Dieses Aktionsmodul ruft Informationen zu [!UICONTROL Trello] Mitgliedern ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Geben Sie den vollständigen Namen oder Benutzernamen des Benutzers ein, den Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>Standardmäßig durchsucht dieses Modul den Mitgliederinhalt nach exakten Übereinstimmungen der einzelnen Wörter in Ihrer Abfrage. Wenn [!UICONTROL Partial] aktiviert ist, sucht das Modul nach Inhalten, die mit einem beliebigen Wort in Ihrer Abfrage beginnen.</p> <p> Wenn Sie beispielsweise das Wort „Entwicklung“ verwenden, um nach einer Pinnwand mit dem Titel „Mein Entwicklungsstatusbericht“ zu suchen, müssen Sie standardmäßig nach dem gesamten Wort suchen. Wenn Sie [!UICONTROL Partial] aktiviert haben, können Sie nach „dev“ suchen, aber nicht nach „development“.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned members]</td> 
   <td> <p> Die maximale Anzahl an Mitgliedern, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Checklisten

+++ **[!UICONTROL Create a Checklist]**

Dieses Aktionsmodul erstellt eine Checkliste für die ausgewählte Karte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, der Sie eine Checkliste hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, der Sie eine Checkliste hinzufügen möchten, oder mappen Sie diese.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, auf der sich die Karte befindet, der Sie eine Checkliste hinzufügen möchten, wählen Sie dann die Liste aus, auf der sich die Karte befindet, und wählen Sie die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen Namen für die Checkliste ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Checkliste oben oder [!UICONTROL append the] Checkliste unten auf der Karte hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter checklist ID]</p> </td> 
   <td> <p>Geben Sie die ID einer Quell-Checkliste ein, die Sie in die neue kopieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Checklist Item]**

Dieses Aktionsmodul fügt ein Element zu einer bestimmten Checkliste hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter checklist ID]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Checkliste eingeben möchten, der Sie ein Element hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Checklist ID]</strong> die ID der Karte ein, der Sie eine Checkliste hinzufügen möchten, oder mappen Sie diese.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, der Sie eine Checkliste hinzufügen möchten, wählen Sie dann die Liste aus, die die Karte enthält, wählen Sie dann die Karte aus und klicken Sie auf die Checkliste.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>Geben Sie einen Namen für das neue Element ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie das Element oben oder [!UICONTROL append] unten in der Checkliste hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Checked]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie das Element wie bereits aktiviert hinzufügen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Checklist Item]**

Dieses Aktionsmodul bearbeitet eine vorhandene Checkliste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Card ID and Checklist Item ID]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte und die Checkliste eingeben möchten, in der Sie ein Element bearbeiten möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Checklist ID]</strong> die ID der Karte ein, der Sie eine Checkliste hinzufügen möchten, oder mappen Sie diese.</p> <p>Geben Sie im Feld <strong>[!UICONTROL Checklist Item ID]</strong> die ID der Checkliste ein oder mappen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, der Sie eine Checkliste hinzufügen möchten, wählen Sie dann die Liste aus, die die Karte enthält, wählen Sie dann die Karte aus und klicken Sie auf die Checkliste.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Checklist ID]</td> 
   <td>Wählen Sie die Checkliste aus, in die Sie das Checklisten-Element verschieben möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>Geben Sie einen Namen für das neue Element ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie das Element oben hinzufügen oder am Ende der Checkliste anhängen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL State]</p> </td> 
   <td> <p>Auswählen, ob das Checklisten-Element vollständig oder unvollständig ist.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Kennzeichnungen

+++ **[!UICONTROL Add a Label to a Card]**

Dieses Aktionsmodul fügt einer ausgewählten Karte einen Titel hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, der Sie eine Checkliste hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, der Sie eine Checkliste hinzufügen möchten, oder mappen Sie diese. Geben Sie <strong>[!UICONTROL Label ID]</strong> Feld die ID der Beschriftung ein, die Sie hinzufügen möchten, oder mappen Sie sie zu.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, auf der sich die Karte befindet, der Sie eine Checkliste hinzufügen möchten, wählen Sie dann die Liste aus, auf der sich die Karte befindet, und wählen Sie die Karte aus. </p> <p>Wählen Sie den Titel aus, den Sie der Karte hinzufügen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Kommentare

+++ **[!UICONTROL Watch Comments]**

Ruft Kommentardetails ab, wenn ein neuer Kommentar an einer angegebenen Position vorhanden ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Wählen Sie den Ort aus, auf den Sie nach Kommentaren achten möchten.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards] überall</strong> </li> 
     <li> <p><strong>[!UICONTROL Board]</strong> </p> <p>Pinnwand auswählen, auf der Kommentare angezeigt werden sollen</p> </li> 
     <li> <p><strong>[!UICONTROL List]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Liste enthält, die Sie auf Kommentare überwachen möchten, und wählen Sie dann die Liste aus.</p> </li> 
     <li><strong>[!UICONTROL Card]</strong> </li> 
     <li>Wählen Sie die Pinnwand aus, die die Karte enthält, die Sie auf Kommentare überwachen möchten, wählen Sie dann die Liste aus, die die Karte enthält, und wählen Sie dann die Karte aus.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Die maximale Anzahl von Kommentaren, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Comment in a Card]**

Dieses Aktionsmodul fügt einen Kommentar zu einer ausgewählten Karte hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, zu der Sie einen Kommentar hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, zu der Sie einen Kommentar hinzufügen möchten, oder mappen Sie sie.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, zu der Sie einen Kommentar hinzufügen möchten, wählen Sie dann die Liste aus, die die Karte enthält, und wählen Sie dann die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment] </td> 
   <td> <p>Geben Sie den Kommentar ein, den Sie der ausgewählten Karte hinzufügen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Comments in a Card]**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!UICONTROL Trello]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Wählen Sie aus, wie Sie die ID der Karte eingeben möchten, zu der Sie einen Kommentar hinzufügen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Card ID]</strong> die ID der Karte ein, zu der Sie einen Kommentar hinzufügen möchten, oder mappen Sie sie.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Wählen Sie die Pinnwand aus, die die Karte enthält, zu der Sie einen Kommentar hinzufügen möchten, wählen Sie dann die Liste aus, die die Karte enthält, und wählen Sie dann die Karte aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td> 
   <td> <p> Geben Sie die maximale Anzahl an Kommentaren ein, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since] </td> 
   <td> <p>Legen Sie das Startdatum des Zeitraums fest, in dem der Kommentar erstellt wurde. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before] </td> 
   <td> <p>Legen Sie das Enddatum des Zeitraums fest, in dem der Kommentar erstellt wurde. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

## [!UICONTROL Trello] Objektkennungen

* [So finden Sie die ID oder den Shortlink einer Karte in [!DNL Trello]](#how-to-find-the-id-or-the-shortlink-of-a-card-in-trello)
* [So finden Sie IDs anderer Objekte in [!DNL Trello]](#how-to-find-ids-of-other-objects-in-trello)

### So finden Sie die ID oder den Shortlink einer Karte in [!DNL Trello]

Wenn Sie eine Karte bearbeiten oder einen neuen Kommentar erstellen möchten, müssen Sie die ID der Karte oder deren Shortlink kennen. Diese Informationen können Sie der Ausgabe des [!UICONTROL New Card]-Triggers entnehmen. Den Shortlink für eine Karte erhalten Sie auch, indem Sie die Karte öffnen und auf die Schaltfläche [!UICONTROL Share] klicken. Der Shortlink befindet sich im [!UICONTROL Link to this card] am Ende der URL nach dem `https://trello.com/c/`.

![Freigeben und mehr](/help/workfront-fusion/references/apps-and-modules/assets/share-and-more-350x575.png)

### So finden Sie IDs anderer Objekte in [!DNL Trello]

Pinnwand-, Listen- und Kommentar-IDs können nur über Trigger abgerufen werden. Auf der [!DNL trello.com]-Website werden diese IDs nicht angezeigt.
