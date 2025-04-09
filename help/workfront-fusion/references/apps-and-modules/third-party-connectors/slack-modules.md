---
title: Slack-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die Slack verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: c9c68a4c-f592-42d1-b15f-a525b9aa3944
source-git-commit: eb0518ba0d1a0c758cb547e362c722f4be3674c7
workflow-type: tm+mt
source-wordcount: '1954'
ht-degree: 0%

---

# [!DNL Slack] Module

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows, die [!DNL Slack]verwenden, automatisieren und mit mehreren Anwendungen und Diensten von Drittanbietern verbinden.

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

Um [!DNL Slack]-Module verwenden zu können, müssen Sie über ein [!DNL Slack]-Konto verfügen.

## Slack-API-Informationen

Der Slack-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>{{IfEmpty(parameters.domain, 'https://slack.com/api/')}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v4.0.15</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Slack] Module und ihre Felder

Beim Konfigurieren [!DNL Slack] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Slack] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Nachrichten](#messages)
* [Unterhaltungen](#channels)
* [Sonstige](#other)

### Nachrichten

* [Erstellen einer Nachricht](#create-a-message)
* [Löschen einer Nachricht](#delete-a-message)
* [Private Kanal Nachricht abrufen](#get-a-private-channel-message)
* [Abrufen einer Nachricht für einen öffentlichen Kanal](#get-a-public-channel-message)
* [Aktualisieren einer Nachricht](#update-a-message)
* [Nachrichten des privaten Kanals ansehen](#watch-private-channel-messages)
* [Nachrichten öffentlicher Kanäle ansehen](#watch-public-channel-messages)

### [!UICONTROL Nachricht erstellen]

Dieses Aktionsmodul erstellt eine neue Nachricht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanalkennung oder Kanalnamen eingeben]</p> </td> 
   <td> <p>Wählen Sie aus, wie Sie den Kanal auswählen möchten, in dem Sie eine Nachricht erstellen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Kanal-ID oder -Name]</strong> die Kanal-ID oder den Namen des Kanals ein, in dem Sie die Nachricht posten möchten, oder ordnen Sie sie zu.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </li> 
     <li> <p><strong>[!UICONTROL Aus der Liste auswählen]</strong> </p> <p>Wählen Sie den Kanaltyp und dann den Kanal aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[! UICONTROL Text]</p> </td> 
   <td> <p>Geben Sie den Text Inhalte der Nachricht ein, die Sie erstellen möchten.</p> <p>Hinweis: Detaillierte Informationen zur Textformatierung finden Sie unter <a href="https://api.slack.com/reference/surfaces/formatting">Text für Programmoberflächen formatieren</a> in der [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL als Benutzer]</td> 
   <td>Aktivieren Sie diese Option, um die Nachricht als die Person zu posten, der die von der Verbindung für dieses Modul verwendeten Anmeldeinformationen gehören.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thread-Nachrichten-ID (Zeitstempel)]</td> 
   <td>Wenn es sich bei der neuen Nachricht um eine Antwort handelt, geben Sie den Zeitstempel der Nachricht ein, auf die Sie antworten möchten. Geben Sie keinen Zeitstempel einer Nachricht ein, die bereits eine Antwort ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Antwort senden]</td> 
   <td> <p>Wählen Sie <strong>[!UICONTROL Yes]</strong> aus, wenn beide der folgenden Bedingungen zutreffen:</p> 
    <ul> 
     <li> <p>Die neue Nachricht ist eine Antwort auf eine andere Nachricht</p> </li> 
     <li> <p>Die neue Nachricht soll für alle Personen im Kanal sichtbar sein</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anlagen]</td> 
   <td>Klicken Sie für jedes Element, das Sie an die Nachricht anhängen möchten, auf <b>Element hinzufügen</b> und geben Sie die Details des Elements ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL icon emoji]</td> 
   <td>Geben Sie das Emoji, das als Symbol für diese Nachricht verwendet werden soll, im <code>:icon-name:</code> Format ein oder ordnen Sie es zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Icon URL]</td> 
   <td>Geben Sie die URL des Bildes ein, das als Symbol für diese Nachricht verwendet werden soll, oder mappen Sie sie. </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Link-Namen]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, damit Namen und Kanäle das <code>@username</code>- oder <code>#channel</code> Format verwenden können. </p> <p>Weitere Informationen finden Sie unter <a href="https://api.slack.com/docs/formatting">Text für Programmoberflächen formatieren</a> in der [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nachrichtentext analysieren]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um automatisches Parsen zu ermöglichen. </p> <p>Weitere Informationen finden Sie unter <a href="https://api.slack.com/docs/formatting">Text für Programmoberflächen formatieren</a> in der [!DNL Slack].</p> <p>Hinweis: Wenn Sie die Optionen [!UICONTROL Link names] oder [!UICONTROL Parse message text] in der ursprünglichen Nachricht verwendet haben, sollten Sie sie auch beim Ausführen des Moduls [!UICONTROL Nachricht aktualisieren] angeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Markdown verwenden]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, damit [!DNL Slack] Markdown im Text verwenden können.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Entfalten Sie hauptsächlich textbasierten Inhalt]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um das Entfalten von hauptsächlich textbasiertem Inhalt zu ermöglichen. </p> <p>Weitere Informationen zum Entfalten in [!DNL Slack] finden Sie unter <a href="https://api.slack.com/reference/messaging/link-unfurling">Entfalten von Links in Nachrichten</a> in der [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Medieninhalte entpacken]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um das Entfalten von Medieninhalten zu ermöglichen. </p> <p>Weitere Informationen zum Entfalten in [!DNL Slack] finden Sie unter <a href="https://api.slack.com/reference/messaging/link-unfurling">Entfalten von Links in Nachrichten</a> in der [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Benutzername]</td> 
   <td>Geben Sie den Benutzernamen an, der zum Posten der Nachricht verwendet wird. Wenn kein Benutzername angegeben wird, wird der Name „Bot“ verwendet.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Löschen einer Nachricht]

Mit dieser Aktion wird eine angegebene Meldung Modul gelöscht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die Kanal-ID ein oder mappen Sie sie.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, die Sie löschen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul Nachrichten für privaten Kanal ansehen .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL als Benutzer]</td> 
   <td> <p> Aktivieren Sie diese Option, um die Nachricht als Benutzer mit den in der Verbindung verwendeten Anmeldeinformationen zu löschen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Nachricht für privaten Kanal abrufen]

Dieses Aktionsmodul ruft die Details einer Nachricht von einem ausgewählten Kanal ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die Kanal-ID ein (zuordnen).</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nachrichten-ID (Zeitstempel)]</p> </td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, zu der Sie Informationen abrufen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einer anderen Modul abgerufen werden, z. B. mit dem [! UICONTROL Ansehen private Kanal Nachrichten] Modul.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Nachricht für öffentlichen Kanal abrufen]**

Dieses Aktionsmodul gibt eine Nachricht mit einer bestimmten ID aus einem angegebenen öffentlichen Kanal zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die Kanal-ID ein oder mappen Sie sie.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID (Zeitstempel)]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, zu der Sie Informationen abrufen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Public Channel Messages].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren einer Nachricht]

Mit diesem Aktionsmodul können Sie eine vorhandene Nachricht bearbeiten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choose how you want to select the message you want to .</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Channel ID or name]</strong> field, enter or map the Channel ID or of the channel that contains the message, then enter the <strong>[!UICONTROL Time Stamp (Message ID)]</strong> of the message.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the type of channel, then select the channel, then select the message.</p> </li> 
    </ul> </td> 
  </tr> -->
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Kanals ein, der die zu aktualisierende Nachricht enthält, oder ordnen Sie sie zu.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nachrichten-ID (Zeitstempel)]</p> </td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, zu der Sie Informationen abrufen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Public Channel Messages].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Text]</p> </td> 
   <td> <p>Geben Sie den neuen Textinhalt der Nachricht ein, die Sie aktualisieren möchten.</p> <p>Weitere Informationen finden Sie unter <a href="https://api.slack.com/docs/formatting">Text für Programmoberflächen formatieren</a> in der [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL als Benutzer]</td> 
   <td>Aktivieren Sie diese Option, um die Nachricht als die User zu aktualisieren, die die Anmeldeinformationen besitzt, die von der Verbindung für diese Modul verwendet werden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL-Anlagen]</td> 
   <td>Klicken Sie für jedes Element, das Sie an die Nachricht anhängen möchten, auf <b>Element hinzufügen</b> und geben Sie die Details des Elements ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Link-Namen]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, damit Namen und Kanäle das <code>@username</code>- oder <code>#channel</code> Format verwenden können. </p> <p>Weitere Informationen finden Sie unter <a href="https://api.slack.com/docs/formatting">Text für Programmoberflächen formatieren</a> in der [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nachrichtentext analysieren]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um automatisches Parsen zu ermöglichen. </p> <p> Weitere Informationen finden Sie unter <a href="https://api.slack.com/docs/formatting">Text für Programmoberflächen formatieren</a> in der [!DNL Slack].</p> <p>Hinweis: Wenn Sie die Optionen [!UICONTROL Link names] oder [!UICONTROL Parse message text] in der ursprünglichen Nachricht verwendet haben, sollten Sie sie auch beim Ausführen des Moduls Nachricht aktualisieren angeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Nachrichten des privaten Kanals ansehen]

Dieses Kanalmodul startet das Trigger-Szenario, wenn eine neue Nachricht zu einem privaten Kanal (einer Gruppe) hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! UICONTROL Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL Kanal] </td> 
   <td> <p>Privaten Kanal auswählen, der auf neue Nachrichten überwacht werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL-Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl an Nachrichten fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Nachrichten von öffentlichen Kanälen ansehen]

Dieses Kanalmodul startet das Trigger, wenn eine neue Nachricht zu einem öffentlichen Kanal hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL Kanal] </td> 
   <td> <p>Wählen Sie den öffentlichen Kanal aus, den Sie auf neue Nachrichten überprüfen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl an Nachrichten fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Unterhaltungen

* [Kanal abrufen](#get-a-channel)
* [Kanäle auflisten](#list-channels)
* [Mitglieder im Kanal auflisten](#list-members-in-channel)

#### [!UICONTROL Kanal abrufen]

Dieses Aktionsmodul gibt Informationen zu einem Arbeitsbereichskanal zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! UICONTROL Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack] Konto mit [!DNL Workfront Fusion]finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen eine Verbindung zu [!DNL Adobe Workfront Fusion] – Standard Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Kanals ein, über den Sie Informationen abrufen möchten, oder ordnen Sie sie zu.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </td> 
  </tr> 
 </tbody>

#### [!UICONTROL Kanäle auflisten]

Dieses Suchmodul gibt eine Liste aller Kanäle in einem Arbeitsbereich zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Ausschließen archiviert]</p> </td> 
   <td> <p>Wählen Sie [!UICONTROL Yes] aus, um archivierte Kanäle in den Ergebnissen auszuschließen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Typ] </td> 
   <td> <p>Wählen Sie die Kanaltypen aus, die Sie abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL-Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl an Kanälen fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Mitglieder im Kanal auflisten]

Diese suchen Modul eine Liste der Benutzer im ausgewählten Kanal zurückgibt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! UICONTROL Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack] Konto mit [!DNL Workfront Fusion]finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen eine Verbindung zu [!DNL Adobe Workfront Fusion] – Standard Anweisungen</a>.</p> </td> 
  </tr> 
<tr> 
   <td role="rowheader"> <p>[! UICONTROL Geben Sie eine Kanal ID oder einen Namen ein]</p> </td> 
   <td> <p>Wählen Sie aus, wie Sie die Nachricht auswählen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Kanal-ID oder -Name]</strong> die Kanal-ID oder den Kanal, aus dem Sie die Benutzer auflisten möchten, ein oder ordnen Sie sie zu.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </li> 
     <li> <p><strong>[! UICONTROL Wählen Sie aus dem Liste]</strong> </p> <p>Wählen Sie den Typ der Kanal und anschließend die Kanal aus.</p> </li> 
    </ul> </td> 
  </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Festlegen wird die maximale Anzahl von Mitgliedern [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgegeben.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Sonstige

#### [!UICONTROL Einen API-Aufruf ausführen]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Slack]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Slack] nicht durchgeführt werden kann.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://slack.com/api/</code> ein. Beispiel: <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL-Header]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Basis-URL]</td> 
   <td>Wählen Sie die Basis-URL aus, die Sie für den API-Aufruf verwenden möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zugriffstoken senden]</td> 
   <td>Wählen Sie aus, ob das Zugriffstoken als Kopfzeile oder als Abfrageparameter gesendet werden soll.</td> 
  </tr> 
 </tbody> 
</table>

## Terminologie

Die folgende Terminologie kann bei der Konfiguration [!DNL Slack] Module nützlich sein:

* **DM**: [!UICONTROL Direct Message]
* **[!UICONTROL IM:** Sofortnachricht]
* **Privater Kanal**: früher [!UICONTROL Gruppe]
* **Direktnachricht**: früher [!UICONTROL IM]
* **Kanal**: [!UICONTROL Konversation] in der API-Dokumentation, [!UICONTROL Kanal] in der [!DNL Slack] App.
