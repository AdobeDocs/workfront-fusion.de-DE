---
title: Slack-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die Slack verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: b5892f64c73c41524029621591e64c942c146432
workflow-type: tm+mt
source-wordcount: '4699'
ht-degree: 0%

---

# [!DNL Slack]

>[!IMPORTANT]
>
>In diesem Artikel werden die Module beschrieben, die im neuen Slack-Connector verfügbar sind, der am 14. November 2025 veröffentlicht wurde.
>
>Informationen zum alten Slack-Connector finden Sie unter [[!DNL Slack] Module (Legacy)](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/slack-modules.md).

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Slack] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
* [Dateien](#files)
* [Kanäle](#channels)
* [Reaktionen](#reactions)
* [Sterne](#stars)
* [Gespeicherte Elemente](#saved-items)
* [Nadeln](#pins)
* [Benutzende](#users)
* [Reminders](#reminders)
* [Ereignisse](#events)
* [Profil](#profile)
* [Sonstiges](#other)

### Nachrichten

+++ **[!UICONTROL Nachricht erstellen]**

Dieses Aktionsmodul erstellt eine neue Nachricht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
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
   <td role="rowheader"> <p>[!UICONTROL -Text]</p> </td> 
   <td> <p>Geben Sie den Textinhalt der Nachricht ein, die Sie erstellen möchten.</p> <p>Hinweis: Detaillierte Informationen zur Textformatierung finden Sie unter <a href="https://api.slack.com/reference/surfaces/formatting">Text für Programmoberflächen formatieren</a> in der [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Blöcke]</td> 
   <td>Blöcke sind wiederverwendbare Komponenten, mit denen Sie Ihre Nachrichten anpassen und organisieren können. Weitere Informationen zu Blöcken finden Sie unter <a href="https://api.slack.com/block-kit">Blockkit</a> in der [!DNL Slack].</td> 
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
 </tbody> 
</table>

+++

+++ **[!UICONTROL Löschen einer Nachricht]**

Dieses Aktionsmodul löscht eine angegebene Nachricht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die Kanal-ID ein oder mappen Sie sie.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID (Zeitstempel)]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, die Sie löschen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul Privaten Kanal beobachten .</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Nachricht für privaten Kanal abrufen]**

Dieses Aktionsmodul ruft die Details einer Nachricht von einem ausgewählten Kanal ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel]</p> </td> 
   <td> <p>Wählen Sie den Kanal aus, der die Nachricht enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nachrichten-ID (Zeitstempel)]</p> </td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, zu der Sie Informationen abrufen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Nachricht für öffentlichen Kanal abrufen]**

Dieses Aktionsmodul gibt eine Nachricht mit einer bestimmten ID aus einem angegebenen öffentlichen Kanal zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Wählen Sie den Kanal aus, der die Nachricht enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID (Zeitstempel)]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, zu der Sie Informationen abrufen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Antworten auflisten]**

Dieses Aktionsmodul ruft einen Thread von Nachrichten ab, die an eine Konversation gesendet wurden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, der die Nachricht enthält, für die Sie Antworten abrufen möchten, und wählen Sie dann den Kanal aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID der übergeordneten Nachricht (Zeitstempel)]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, für die Sie Antworten abrufen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Antworten ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Nach Nachricht suchen]**

Dieses Suchmodul gibt Nachrichten zurück, die mit einer Suchanfrage übereinstimmen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Abfrage]</td> 
   <td> <p>Geben Sie die Abfrage ein, nach der Sie suchen möchten. </p> <p>Informationen zum Erstellen von Formeln im Zuordnungsbereich finden Sie unter <a href="/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md" class="MCXref xref">Zuordnen von Elementen mithilfe von Funktionen in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortieren nach] </td> 
   <td> <p>Wählen Sie aus, ob die zurückgegebenen Nachrichten nach ihrem Score oder Zeitstempel sortiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Wählen Sie aus, ob Nachrichten auf- oder absteigend sortiert werden sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Aktualisieren einer Nachricht]**

Mit diesem Aktionsmodul können Sie eine vorhandene Nachricht bearbeiten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanalkennung oder Kanalnamen eingeben]</p> </td> 
   <td> <p>Wählen Sie aus, wie Sie die Nachricht auswählen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie im Feld <strong>[!UICONTROL Kanal-ID oder -Name]</strong> die Kanal-ID oder den Kanal, der die Nachricht enthält, ein oder ordnen Sie sie zu und geben Sie dann den <strong>[!UICONTROL Zeitstempel (Nachrichten-ID)]</strong> der Nachricht ein. .</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </li> 
     <li> <p><strong>[!UICONTROL Aus der Liste auswählen]</strong> </p> <p>Wählen Sie den Kanaltyp aus, wählen Sie dann den Kanal und dann die Nachricht aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Text]</p> </td> 
   <td> <p>Geben Sie den neuen Textinhalt der Nachricht ein, die Sie aktualisieren möchten.</p> <p>Weitere Informationen finden Sie unter <a href="https://api.slack.com/docs/formatting">Text für Programmoberflächen formatieren</a> in der [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Blöcke]</td> 
   <td>Blöcke sind wiederverwendbare Komponenten, mit denen Sie Ihre Nachrichten anpassen und organisieren können. Weitere Informationen zu Blöcken finden Sie unter <a href="https://api.slack.com/block-kit">Blockkit</a> in der [!DNL Slack].</td> 
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

+++

+++ **[!UICONTROL Direktnachrichten ansehen]**

Dieses Trigger-Modul startet das Szenario, wenn eine neue Nachricht zu einer Direktnachricht hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Wählen Sie die Direktnachrichten-Konversation aus, die Sie auf neue Nachrichten überprüfen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl an Nachrichten ein, die das Modul während jedes Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Mehrparteien-Direktnachrichten ansehen]**

Dieses Trigger-Modul startet das Szenario, wenn eine neue Nachricht zu einem Mehrparteien-Direktnachrichtenkanal hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Wählen Sie die Direktnachrichten-Konversation aus, die Sie auf neue Nachrichten überprüfen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl an Nachrichten ein, die das Modul während jedes Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Nachrichten des privaten Kanals ansehen]**

Dieses Kanalmodul startet das Trigger-Szenario, wenn eine neue Nachricht zu einem privaten Kanal (einer Gruppe) hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Privaten Kanal auswählen, der auf neue Nachrichten überwacht werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl an Nachrichten ein, die das Modul während jedes Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Nachrichten von öffentlichen Kanälen ansehen]**

Dieses Kanalmodul startet das Trigger, wenn eine neue Nachricht zu einem öffentlichen Kanal hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Wählen Sie den öffentlichen Kanal aus, den Sie auf neue Nachrichten überprüfen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl an Nachrichten ein, die das Modul während jedes Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Dateien

+++ **[!UICONTROL Erstellen Sie eine Textdatei]**

Dieses Aktionsmodul erstellt eine Textdatei.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanäle]</td> 
   <td> <p>Klicken Sie für jeden Kanal, in den Sie die Datei hochladen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und wählen Sie dann den Kanaltyp und den Kanal aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Titel]</td> 
   <td>Titel für die Datei eingeben, die hochgeladen werden soll</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thread-ID (Zeitstempel)]</td> 
   <td> <p>Wenn Sie die Datei als Antwort hochladen, geben Sie den Zeitstempel der Nachricht ein, auf die Sie antworten möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ursprünglicher Kommentar]</td> 
   <td> <p>Geben Sie den Text der Nachricht ein, mit der die Datei eingeführt wird, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Datei löschen]**

Dieses Aktionsmodul gibt den Löschvorgang für die angegebene Datei zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td> <p>Geben Sie die ID der Datei ein, die Sie löschen möchten, oder mappen Sie sie. </p> <p>Hinweis: Die Datei-ID kann mit einem anderen Modul abgerufen werden, z. B. mit dem [!DNL Watch Files].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Datei abrufen]**

Dieses Aktionsmodul gibt Details zur angegebenen Datei zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td> <p>Geben Sie die ID der Datei ein, die Sie abrufen möchten, oder mappen Sie sie. </p> <p>Hinweis: Die Datei-ID kann mit einem anderen Modul abgerufen werden, z. B. mit dem [!DNL Watch Files].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Dateien auflisten]**

Dieses Aktionsmodul gibt eine Liste von Dateien basierend auf dem angegebenen Filter zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Typ] </td> 
   <td> <p>Wählen Sie die Dateitypen aus, die Sie abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanaltyp]</p> </td> 
   <td> <p>Wählen Sie den Kanaltyp aus, der für den Kanal steht, dessen Dateien aufgelistet werden sollen, und wählen Sie dann den Kanal aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Erstellt von]</td> 
   <td> <p>Wählen Sie einen Benutzer aus, um nur die vom angegebenen Benutzer erstellten Dateien zurückzugeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datum von]</td> 
   <td>Geben Sie das früheste Datum ein, ab dem Sie Dateien zurückgeben möchten. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datum bis]</td> 
   <td>Geben Sie das letzte Datum ein, ab dem Sie Dateien zurückgeben möchten. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Dateien ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Download a File]**

This action module downloads a file from a URL. It must follow the [!UICONTROL Slack] >[!UICONTROL Get a File] module in a scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL private download]</td> 
   <td> <p>Map the <b>[!UICONTROL URL Private download]</b> value from the [!DNL Slack] >[!UICONTROL Get a File] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL Datei hochladen]**

Dieses Aktionsmodul erstellt oder lädt eine Datei in [!DNL Slack] hoch

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanäle]</td> 
   <td> <p>Klicken Sie für jeden Kanal, in den Sie die Datei hochladen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und wählen Sie dann den Kanaltyp und den Kanal aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Titel]</td> 
   <td>Titel für die Datei eingeben, die hochgeladen werden soll</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thread-ID (Zeitstempel)]</td> 
   <td> <p>Wenn Sie die Datei als Antwort hochladen, geben Sie den Zeitstempel der Nachricht ein, auf die Sie antworten möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ursprünglicher Kommentar]</td> 
   <td> <p>Geben Sie den Text der Nachricht ein, mit der die Datei eingeführt wird, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Dateien ansehen]**

Dieses Dateimodul startet ein Trigger, wenn eine neue Datei hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Typ]</td> 
   <td>Wählen Sie den Dateityp aus, den das Modul überwachen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td> <p>Wählen Sie den Kanaltyp aus, der auf Dateien überwacht werden soll, und wählen Sie dann den Kanal aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Erstellt von]</td> 
   <td> <p>Wählen Sie einen Benutzer aus, um nur die vom angegebenen Benutzer erstellten Dateien zurückzugeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl von Dateien ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Kanäle

+++ **[!UICONTROL Archivieren eines Kanals]**

Dieses Aktionsmodul archiviert einen Kanal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Kanals ein, den Sie archivieren möchten, oder mappen Sie sie.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Erstellen eines Kanals]**

Dieses Aktionsmodul erstellt einen neuen Kanal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Name]</p> </td> 
   <td> <p>Geben Sie einen Namen für den neuen Kanal ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ist privat]</td> 
   <td>Aktivieren Sie diese Option, um den neuen Kanal als privat festzulegen.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Kanal abrufen]**

Dieses Aktionsmodul gibt Informationen zu einem Arbeitsbereichskanal zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Kanals ein, über den Sie Informationen abrufen möchten, oder ordnen Sie sie zu.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Einem Kanal beitreten]**

Dieses Aktionsmodul fügt den Benutzer einem Kanal hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Kanals ein, den Sie beitreten möchten, oder mappen Sie sie.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Einen Kanal verlassen]**

Dieses Aktionsmodul entfernt den Benutzer aus einem Kanal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Kanals ein, den Sie verlassen möchten, oder ordnen Sie sie zu.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Kanäle auflisten]**

Dieses Suchmodul gibt eine Liste aller Kanäle in einem Arbeitsbereich zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
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
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl an Kanälen fest, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Mitglieder im Kanal auflisten]**

Dieses Suchmodul gibt eine Liste der Benutzer im ausgewählten Kanal zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, der die Mitglieder enthält, die Sie auflisten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privater Kanal]</td> 
   <td>Wählen Sie den Kanal aus, dessen Mitglieder Sie auflisten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Mitgliedern fest, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Legen Sie den Zweck eines Kanals fest]**

Dieses Aktionsmodul ändert den Zweck eines Kanals

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, für den Sie den Zweck ändern möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privat] / Benutzer / [!UICONTROL Mehrere IM-Kanäle]</td> 
   <td>Wählen Sie den Kanal oder den Benutzer aus, für den bzw. den Sie den Zweck ändern möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zweck]</td> 
   <td>Geben Sie den neuen Zweck des Kanals ein oder mappen Sie ihn. Dieses Feld unterstützt keine Formatierung oder Links.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Legen Sie das Thema eines Kanals fest]**

Dieses Aktionsmodul ändert das Thema eines Kanals

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, für den Sie das Thema ändern möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privat] / [!UICONTROL Benutzer] / [!UICONTROL Mehrere IM-Kanäle]</td> 
   <td>Wählen Sie den Kanal oder den Benutzer aus, für den bzw. den Sie das Thema ändern möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Topic]</td> 
   <td>Geben Sie das neue Thema des Kanals ein oder ordnen Sie es zu. Dieses Feld unterstützt keine Formatierung oder Links.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archivierung eines Kanals aufheben]**

Dieses Aktionsmodul hebt die Archivierung eines Kanals auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kanal-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Kanals ein, dessen Archivierung Sie aufheben möchten, oder mappen Sie sie.</p> <p>Hinweis: Die Kanal-ID kann mit dem Modul [!UICONTROL List Channels] abgerufen werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Reaktionen

+++ **[!UICONTROL Reaktion hinzufügen]**

Dieses Aktionsmodul fügt einem Element eine Reaktion hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, dem Sie eine Reaktion hinzufügen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privat] / [!UICONTROL Benutzer] / [!UICONTROL Mehrere IM-Kanäle]</td> 
   <td>Wählen Sie den Kanal oder Benutzer aus, dem Sie eine Reaktion hinzufügen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID (Zeitstempel)]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, der eine Reaktion hinzugefügt werden soll, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name der-Reaktion (Emoji)]</td> 
   <td>Geben Sie den Namen des Emojis ein, das Sie für eine Reaktion verwenden möchten, oder mappen Sie ihn. Beispiel: <code>thumbsup</code>. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Reaktionen auflisten]**

Dieses Aktionsmodul gibt von einem Benutzer durchgeführte Reaktionen zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Benutzer]</p> </td> 
   <td> <p>Wählen Sie den Benutzer aus, der die Reaktionen erstellt hat, die Sie auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl an Reaktionen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Entfernen einer Reaktion]**

Dieses Aktionsmodul entfernt eine Reaktion aus einem Element.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, aus dem Sie eine Reaktion entfernen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privat] / [!UICONTROL Benutzer] / [!UICONTROL Mehrere IM-Kanäle]</td> 
   <td>Wählen Sie den Kanal oder den Benutzer aus, aus dem bzw. dem Sie eine Reaktion entfernen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, aus der Sie eine Reaktion entfernen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name der-Reaktion (Emoji)]</td> 
   <td>Geben Sie den Namen des Emojis ein, das Sie aus der Nachricht entfernen möchten, oder ordnen Sie ihn zu. Beispiel: <code>thumbsup</code>. </td> 
  </tr> 
 </tbody> 
</table>

+++

### Sterne

+++ **[!UICONTROL Stern hinzufügen]**

Dieses Aktionsmodul macht einen Kanal zu einem Startkanal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, dem Sie einen Stern hinzufügen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privat] / [!UICONTROL Benutzer] / [!UICONTROL Mehrere IM-Kanäle]</td> 
   <td>Wählen Sie den Kanal oder Benutzer aus, dem Sie einen Stern hinzufügen möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Entferne einen Stern]**

Dieses Aktionsmodul entfernt den Stern aus einem gestarteten Kanal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, dem Sie einen Stern hinzufügen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privat] / [!UICONTROL Benutzer] / [!UICONTROL Mehrere IM-Kanäle]</td> 
   <td>Wählen Sie den Kanal oder Benutzer aus, dem Sie einen Stern hinzufügen möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Gespeicherte Elemente

+++ **[!UICONTROL Gespeichertes Element entfernen]**

Dieses Aktionsmodul entfernt ein Element aus gespeicherten Elementen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID (Zeitstempel)]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, die Sie aus gespeicherten Elementen entfernen möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td> <p>Geben Sie die Datei ein, die Sie aus gespeicherten Elementen entfernen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Element speichern]**

Dieses Aktionsmodul fügt ein Element zu gespeicherten Elementen hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID (Zeitstempel)]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, die Sie speichern möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td> <p>Geben Sie die Datei ein, die Sie speichern möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Nadeln

+++ **[!UICONTROL Element anheften]**

Dieses Aktionsmodul heftet ein Element an einen Kanal an.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, an den Sie ein Element anheften möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privat] / [!UICONTROL Mehrere IM-Kanäle] / [!UICONTROL Benutzer]</td> 
   <td>Wählen Sie den Kanal oder Benutzer aus, an den Sie ein Element anheften möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, die Sie anheften möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Fixierung eines Elements aufheben]**

Dieses Aktionsmodul hebt die Anheftung eines Elements aus einem Kanal auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, von dem Sie ein Element entfernen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privat] / [!UICONTROL Mehrere IM-Kanäle] / [!UICONTROL Benutzer]</td> 
   <td>Wählen Sie den Kanal oder den Benutzer aus, von dem bzw. dem Sie ein angeheftetes Element entfernen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID]</td> 
   <td> <p> Geben Sie den Zeitstempel der Nachricht ein, deren Anheftung Sie aufheben möchten, oder ordnen Sie ihn zu.</p> <p>Hinweis: Der Zeitstempel kann mit einem anderen Modul abgerufen werden, z. B. dem Modul [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Benutzende

+++ **[!UICONTROL Benutzer abrufen]**

Dieses Aktionsmodul ruft Details zu einem Mitglied eines Arbeitsbereichs ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Benutzer-ID]</p> </td> 
   <td> <p>Geben Sie die Benutzer-ID des Benutzers ein, für den Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> <p>Hinweis: Die Benutzer-ID kann mit einem anderen Modul abgerufen werden, z. B. mit dem Modul [!DNL List Users] .</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Benutzer einladen]**

Dieses Aktionsmodul lädt 1-30 Benutzer zu einem öffentlichen oder privaten Kanal ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, zu dem Sie Benutzer einladen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privater Kanal]</td> 
   <td>Wählen Sie den Kanal aus, zu dem Sie Benutzer einladen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Benutzer]</td> 
   <td> <p>Wählen Sie die Benutzer aus, die Sie zum Kanal hinzufügen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Benutzer treten]**

Dieses Aktionsmodul entfernt einen Benutzer aus einem Kanal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kanaltyp]</td> 
   <td>Wählen Sie den Kanaltyp aus, aus dem ein Benutzer entfernt werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Öffentlich] / [!UICONTROL Privater Kanal]</td> 
   <td>Wählen Sie den Kanal aus, aus dem Sie eine Benutzerin oder einen Benutzer entfernen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Benutzer]</td> 
   <td> <p>Wählen Sie den Benutzer aus, den Sie aus dem Kanal entfernen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Benutzer auflisten]**

Dieses Aktionsmodul gibt eine Liste aller Benutzer in einem Arbeitsbereich zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Limit]</p> </td> 
   <td> <p>Geben Sie die maximale Anzahl an Benutzern ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Nach Benutzer suchen]**

Dieses Aktionsmodul ruft Details zu einem einzelnen Benutzer mithilfe seiner E-Mail-Adresse ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL E-Mail] </p> </td> 
   <td> <p>Geben Sie die E-Mail-Adresse des Benutzers ein, zu dem Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Benutzer beobachten]**

Dieses Benutzermodul startet das Trigger, wenn ein neuer Benutzer zum Arbeitsbereich [!DNL Slack] hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Benutzern fest, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Reminders

<!--

+++ **[!UICONTROL List Reminders]**

This action module returns a list of all reminders created by or given to the currently authenticated user.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Limit]</p> </td> 
   <td> <p>Enter or map the maximum number of reminders you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Reminder]**

This action module retrieves details about a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to retrieve details for.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL Erinnerung erstellen]**

Dieses Aktionsmodul erstellt eine Erinnerung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Text]</td> 
   <td>Inhalt der Erinnerung eingeben oder zuordnen</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Time]</td> 
   <td> <p>Datum und Uhrzeit eingeben oder zuordnen, zu der diese Erinnerung erfolgen soll. Geben Sie einen der folgenden Werte ein: </p> 
    <ul> 
     <li> <p>Der Unix-Zeitstempel (in bis zu fünf Jahren)</p> </li> 
     <li> <p>Die Anzahl der Sekunden bis zur Erinnerung (falls innerhalb von 24 Stunden) </p> </li> 
     <li> <p>Eine Beschreibung in natürlicher Sprache (Beispiele: „in 15 Minuten“ oder „jeden Donnerstag„)</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Benutzer] </p> </td> 
   <td> <p>Wählen Sie den Benutzer aus, der die Erinnerung erhält.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Complete a Reminder]**

This action module completes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to complete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Delete a Reminder]**

This action module deletes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to delete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

### Ereignisse

+++ **[!UICONTROL Neues Ereignis]**

Dieser sofortige Trigger startet ein Szenario, wenn eine neue Nachricht oder ein anderes Ereignis erstellt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Wählen Sie den Webhook aus, den Sie verwenden möchten.</p> <p>Oder</p> <p>Erstellen Sie einen neuen Webhook.</p> 
    <ol> 
     <li value="1"> <p>Klicken Sie auf <b>[!UICONTROL Hinzufügen]</b>.</p> </li> 
     <li value="2"> <p>Wählen Sie den Ereignistyp.</p> </li> 
     <li value="3"> <p>Wählen Sie eine Verbindung aus oder fügen Sie sie hinzu. Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung mit [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen</a></p> </li> 
     <li value="4"> <p>Wählen Sie bei Aufforderung den Kanal aus, den Sie beobachten möchten.</p> </li> 
     <li value="5"> <p>Klicken Sie auf <b>[!UICONTROL Speichern]</b>, um den Webhook zu speichern und zum Modul zurückzukehren.</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Profil

+++ **[!UICONTROL Status festlegen]**

Dieses Aktionsmodul aktualisiert den aktuellen Status eines Benutzers.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Statustext]</p> </td> 
   <td> <p>Geben Sie den Statustext ein oder ordnen Sie ihn zu. Beachten Sie Folgendes:</p> 
    <ul> 
     <li> <p>Sie können bis zu 100 Zeichen eingeben.</p> </li> 
     <li> <p>Sie können Markup oder andere Formatierungen verwenden, z. B. Benutzerbeschriftungen.</p> </li> 
     <li> <p>Sie können Emojis in den Statustext einfügen, indem Sie das <code>:emojiname:</code> Format verwenden.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status Emoji]</td> 
   <td> <p>Geben Sie das Emoji ein, das Sie zur Darstellung Ihres Status verwenden möchten, oder ordnen Sie es zu. Verwenden Sie den <code>:emojiname:</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status Expiration]</td> 
   <td>Geben Sie das Datum und die Uhrzeit ein, zu der der Status ablaufen soll, oder ordnen Sie sie zu. Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Typzwang</a>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Sonstiges

+++ **[!UICONTROL Erstellen eines API-Aufrufs]**

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Slack]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Slack] nicht durchgeführt werden kann.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Slack]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://slack.com/api/</code> ein. Beispiel: <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Methode]</td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
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
 </tbody> 
</table>

+++

## Terminologie

Die folgende Terminologie kann bei der Konfiguration [!DNL Slack] Module nützlich sein:

* **DM**: [!UICONTROL Direct Message]
* **IM**: [!UICONTROL Instant Message]
* **Privater Kanal**: früher [!UICONTROL Gruppe]
* **Direktnachricht**: früher [!UICONTROL IM]
* **channel**: [!UICONTROL Konversation] in der API-Dokumentation, [!UICONTROL channel] in der [!DNL Slack] App.

