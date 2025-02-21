---
title: GitHub-Module
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die GitHub verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: d9e6c26c-8770-40bc-a83a-8c05f86e4a3f
source-git-commit: e11c73482a3844bbc96c8d08f8e50a53bc302513
workflow-type: tm+mt
source-wordcount: '1519'
ht-degree: 0%

---

# [!DNL GitHub]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!UICONTROL GitHub] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
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

Um [!DNL GitHub] Module verwenden zu können, müssen Sie über ein [!DNL GitHub] Konto verfügen.

## [!DNL GitHub] mit [!DNL Workfront Fusion] verbinden

Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung zu [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL GitHub] Module und ihre Felder.

Beim Konfigurieren [!DNL GitHub] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL GitHub] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)

### Auslöser

* [[!UICONTROL Watch Comments]](#watch-comments)
* [[!UICONTROL Watch Forks]](#watch-forks)
* [[!UICONTROL Watch Issues]](#watch-issues)
* [[!UICONTROL Watch Pull Requests]](#watch-pull-requests)
* [[!UICONTROL Watch Repositories]](#watch-repositories)

#### [!UICONTROL Watch Comments]

Dieses Kommentarmodul startet ein Trigger, wenn ein neuer Kommentar hinzugefügt oder ein bestehender Kommentar geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, das Sie überwachen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue number]</td> 
   <td>Wenn Sie die Suche einschränken möchten, indem Sie nur nach neuen Kommentaren zu einem bestimmten Problem suchen, geben Sie die Problemnummer ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Kommentaren fest, die [!DNL Workfront Fusion] während eines Zyklus zurückgibt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Wählen Sie aus, ob nur nach neuen Kommentaren oder Kommentaren und allen Änderungen gesucht werden soll.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Forks]

Dieses Trigger-Modul startet ein Szenario, wenn eine neue Verzweigung erstellt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, auf das Sie Formulare überwachen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned forks]</td> 
    <td>Geben Sie die maximale Anzahl der Verzweigungen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Issues]

Dieses Trigger-Modul startet ein Szenario, wenn ein neues Problem hinzugefügt oder ein vorhandenes Problem geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL I want to watch]</td> 
   <td>Wählen Sie aus, ob alle Repositorys, die mit diesem Konto verknüpft sind, oder nur ein Repository überwacht werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wenn Sie ausgewählt haben, dass Probleme nur in einem Repository überwacht werden sollen, wählen Sie das Repository aus, das überwacht werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Problemen fest, die [!DNL Workfront Fusion] während eines Zyklus zurückgibt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Wählen Sie aus, ob nur auf neue Probleme oder auf neue Probleme und alle Änderungen geachtet werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Sie können die Probleme, die Sie im Auge behalten möchten, nach ihrer Zuordnung filtern.</p> 
    <ul> 
     <li>[!UICONTROL All issues]</li> 
     <li>[!UICONTROL Only issues assigned to me]</li> 
     <li>[!UICONTROL Only issues created by me]</li> 
     <li>[!UICONTROL Only issues mentioning me]</li> 
     <li>[!UICONTROL Only issues I'm subscribed to updates for]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Wählen Sie aus, ob nur offene oder nur geschlossene Anfragen angezeigt werden sollen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Klicken Sie für jedes Tag, das Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie das Tag ein. Das Modul überwacht Probleme mit diesen Tags.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Pull Requests]

Dieses Modul wird Trigger, wenn eine neue Pull-Anforderung hinzugefügt oder eine vorhandene Pull-Anforderung geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, das Sie überwachen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned pull requests]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Pull-Anforderungen fest, die [!DNL Workfront Fusion] während eines Zyklus zurückgibt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Wählen Sie aus, ob Sie [!UICONTROL only open pull], [!UICONTROL only closed ones] oder alle Pull-Anforderungen beobachten möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Wählen Sie aus, ob Sie nur auf neue Pull-Anforderungen oder neue Pull-Anforderungen und alle Änderungen achten möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Repositories]

Dieses Trigger-Modul startet ein Szenario, wenn ein Repository erstellt oder geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned repositories]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Repositorys fest, die [!DNL Workfront Fusion] in einem Zyklus zurückgibt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Wählen Sie aus, ob Sie auf neue Repositorys und alle Änderungen oder nur auf neue Repositorys achten möchten.</td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Add assignees]](#add-assignees)
* [[!UICONTROL Add labels to an issue]](#add-labels-to-an-issue)
* [[!UICONTROL Create a comment]](#create-a-comment)
* [[!UICONTROL Create an issue]](#create-an-issue)
* [[!UICONTROL Get an issue]](#get-an-issue)
* [[!UICONTROL List comments]](#list-comments)
* [[!UICONTROL Remove a label from an issue]](#remove-a-label-from-an-issue)
* [[!UICONTROL Remove assignees]](#remove-assignees)
* [[!UICONTROL Search for an issue]](#search-for-an-issue)
* [[!UICONTROL Update an issue]](#update-an-issue)

#### [!UICONTROL Add assignees]

Dieses Modul fügt dem angegebenen Problem Verantwortliche hinzu

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, das das Problem enthält, dem Sie Verantwortliche hinzufügen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Wählen Sie die Personen aus, die Sie dem Problem zuweisen möchten. Zu den verfügbaren Bevollmächtigten gehören alle mit Schreibberechtigungen für das Repository sowie Organisationsmitglieder mit Leseberechtigungen für das Repository. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Geben Sie die Problemnummer des Problems ein, dem Sie Bevollmächtigte hinzufügen möchten, oder ordnen Sie sie zu. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add labels to an issue]

Dieses Modul fügt einem Problem Kennzeichnungen hinzu. Kennzeichnungen werden auf Repository-Ebene definiert und können nur von einer Person mit Schreibzugriff auf das Repository erstellt werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, das das Problem enthält, dem Sie Kennzeichnungen hinzufügen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Wählen Sie die Kennzeichnungen aus, die Sie dem Problem hinzufügen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Geben Sie die Problemnummer des Problems ein, dem Sie Kennzeichnungen hinzufügen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a comment]

Dieses Modul erstellt einen Kommentar zum angegebenen Problem.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, das das Problem enthält, zu dem Sie einen Kommentar erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Geben Sie die Problemnummer des Problems ein, zu dem Sie einen Kommentar erstellen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Geben Sie den Inhalt des Kommentars ein oder mappen Sie ihn.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an issue]

Dieses Modul erstellt ein neues Problem im ausgewählten Repository.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, in dem Sie ein Problem erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Wählen Sie die Personen aus, die Sie dem Problem zuweisen möchten. Zu den verfügbaren Bevollmächtigten gehören alle Personen mit Schreibberechtigungen für das Repository sowie Organisationsmitglieder mit Leseberechtigungen für das Repository. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Milestone]</td> 
   <td>Wählen Sie den Meilenstein aus, den Sie mit dem neuen Problem verknüpfen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Wählen Sie alle Kennzeichnungen aus, die Sie auf das neue Problem anwenden möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Geben Sie einen Titel für die neue Anfrage ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Geben Sie den Hauptteil des Problems ein, z. B. eine Beschreibung oder zusätzliche Informationen, oder ordnen Sie ihn zu</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an issue]

Dieses Modul ruft Details zum angegebenen Problem ab

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, das das Problem enthält, zu dem Sie Details abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Geben Sie die Anfragenummer des Problems ein, zu dem Sie Details abrufen möchten, oder ordnen Sie sie zu. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List comments]

Dieses Modul listet alle Kommentare zum angegebenen Problem auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, das das Problem enthält, aus dem Sie Kommentare auflisten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Geben Sie die Problemnummer des Problems ein, zu dem Sie Kommentare auflisten möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since]</td> 
   <td>Das Modul gibt die Kommentare zurück, die nach diesem Datum erstellt wurden. Eine Liste der unterstützten Datumsformate finden Sie unter "<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> in [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Kommentaren fest, die [!DNL Workfront Fusion] während eines Zyklus zurückgibt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a label from an issue]

Dieses Modul entfernt eine einzelne Kennzeichnung aus einem Problem.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, das das Problem enthält, aus dem Sie eine Kennzeichnung entfernen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Wählen Sie die Bezeichnung aus, die Sie aus dem Problem entfernen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Geben Sie die Problemnummer des Problems ein, von dem Sie einen Titel entfernen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assignees]

Dieses Modul entfernt Verantwortliche aus dem angegebenen Problem.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, das das Problem enthält, aus dem Sie die Zugewiesenen entfernen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Wählen Sie die Personen aus, die Sie aus dem Problem entfernen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Geben Sie die Problemnummer des Problems ein, aus dem Sie Zugewiesene entfernen möchten, oder ordnen Sie sie zu. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for an issue]

Dieses Modul sucht nach Problemen, die Ihren Suchkriterien entsprechen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Problemen fest, die [!DNL Workfront Fusion] während eines Zyklus zurückgibt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Wählen Sie aus, wie die Suchergebnisse sortiert werden sollen.</p> 
    <ul> 
     <li> <p>[!UICONTROL Best match] </p> </li> 
     <li>[!UICONTROL Date created]</li> 
     <li>[!UICONTROL Date updated]</li> 
     <li>[!UICONTROL Number of comments]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort direction]</td> 
   <td> <p>Aufsteigend oder absteigend auswählen. </p> <p>Bei Datumsangaben wird bei Auswahl von <strong>[!UICONTROL descending]</strong> zuerst das neueste Datum zurückgegeben. </p> <p>Wenn Sie [!UICONTROL number of comments] "<strong>[!UICONTROL descending]</strong>" auswählen, wird das Problem mit der höchsten Anzahl an Kommentaren zuerst zurückgegeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>Geben Sie Ihre Suchanfrage ein oder ordnen Sie sie zu. Eine ausführliche Beschreibung der Suchoptionen finden Sie unter <a href="https://docs.github.com/en/github/searching-for-information-on-github/searching-issues-and-pull-requests">Suchen von Problemen und Pull-</a> auf der [!DNL GitHub]-Hilfeseite.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an issue]

Dieses Modul aktualisiert ein vorhandenes [!DNL GitHub].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL GitHub]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Wählen Sie das Repository aus, in dem Sie ein Problem aktualisieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Wählen Sie die Personen aus, die Sie dem Problem zuweisen möchten. Zu den verfügbaren Bevollmächtigten gehören alle mit Schreibberechtigungen für das Repository sowie Organisationsmitglieder mit Leseberechtigungen für das Repository. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Milestone]</td> 
   <td>Wählen Sie den Meilenstein aus, den Sie mit dem Problem verknüpfen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Wählen Sie alle Kennzeichnungen aus, die Sie auf das Problem anwenden möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Geben Sie die Anfragenummer des Problems ein, das Sie aktualisieren möchten, oder mappen Sie sie. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Wählen Sie den Status aus, auf den Sie das Problem aktualisieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Geben Sie einen neuen Titel für das Problem ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Geben Sie einen neuen Text für das Problem ein, z. B. eine Beschreibung oder zusätzliche Informationen, oder ordnen Sie ihn zu</td> 
  </tr> 
 </tbody> 
</table>
