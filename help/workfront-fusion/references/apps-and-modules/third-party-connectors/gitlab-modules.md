---
title: GitLab-Module
description: Adobe Workfront Fusion erfordert zusätzlich zu einer Adobe Workfront-Lizenz eine Adobe Workfront Fusion-Lizenz.
author: Becky
feature: Workfront Fusion
exl-id: fabbadce-5669-4363-834e-6d7428520f62
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '3554'
ht-degree: 0%

---

# [!UICONTROL GitLab]

Adobe Workfront Fusion erfordert zusätzlich zu einer Adobe Workfront-Lizenz eine Adobe Workfront Fusion-Lizenz.

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!UICONTROL GitLab] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

>[!NOTE]
>
>Dieser Artikel erwartet eine gewisse Vertrautheit mit der API-Dokumentation und [!DNL GitLab] Funktionalität im Allgemeinen.

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

## [!DNL GitLab] mit [!DNL Workfront Fusion] verbinden {#connect-gitlab-to-workfront-fusion}

1. Klicken Sie in einem [!DNL Workfront Fusion] [!DNL Gitlab] auf **[!UICONTROL Add]** neben dem Feld Verbindung .
1. Konfigurieren Sie die folgenden Felder:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name]</td> 
      <td> <p>Geben Sie einen Namen für die Verbindung ein.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL [!DNL GitLab] URL]</td> 
      <td>Geben Sie die URL Ihrer [!DNL GitLab] ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Access Token]</td> 
      <td><p>Geben Sie Ihre [!UICONTROL Private Token] oder [!UICONTROL Personal Access Token] ein.</p><p>Informationen zum Suchen oder Erstellen eines persönlichen Zugriffstokens in [!DNL GitLab] finden Sie unter „Erstellen eines persönlichen Zugriffstokens“ in <a href="https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html">Persönliche Zugriffstoken</a> in der [!DNL GitLab].</p></td> 
     </tr> 
    </tbody> 
   </table>


1. Klicken Sie auf **[!UICONTROL Continue]**.
1. Klicken Sie auf **[!UICONTROL Authorize]** , um die Verbindung zu erstellen und zum Modul zurückzukehren.

## [!DNL GitLab] Module und ihre Felder

Beim Konfigurieren [!DNL GitLab] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL GitLab] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Trigger

+++**[!UICONTROL Watch build status]**

Dieses Instant Trigger-Modul startet ein Szenario, wenn sich der Status eines Builds ändert.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Änderungen des Build-Status überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch commit/MR/issue/snippet comments]**

Dieses Instant Trigger-Modul startet ein Szenario, wenn ein Commit für einen Commit, eine Zusammenführungsanfrage, ein Problem oder ein Codefragment ausgeführt wird.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Kommentare überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch commits (pushes)]**

Dieses Instant Trigger-Modul startet ein Szenario, wenn ein Commit an ein Repository gesendet wird. Dieses Modul startet kein Szenario, wenn ein Tag gesendet wird.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Commits überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch issue comment]**

Dieses Instant Trigger-Modul startet ein Szenario, wenn ein Problem kommentiert wird.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Problemkommentare überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch issues]**

Dieses [!UICONTROL instant trigger]-Modul startet ein Szenario, wenn ein Problem erstellt wird oder wenn ein vorhandenes Problem aktualisiert, geschlossen oder erneut geöffnet wird.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Probleme überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch merge requests]**

Dieses Instant Trigger-Modul startet ein Szenario, wenn eine der folgenden Situationen eintritt:

* Eine neue Zusammenführungsanfrage wird erstellt
* Eine vorhandene Zusammenführungsanfrage wird aktualisiert, zusammengeführt oder geschlossen
* Ein Commit wird in der Quellverzweigung hinzugefügt


<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Zusammenführungsanfragen überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch merge request comments]**

Dieses Instant Trigger-Modul startet ein Szenario, wenn ein Kommentar zu einer Zusammenführungsanfrage abgegeben wird.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Kommentare zu Zusammenführungsanfragen überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch pipeline status]**

Dieses Instant Trigger-Modul startet ein Szenario, wenn sich der Status einer Pipeline ändert.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Pipeline-Statusänderungen überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch projects]**

Dieses Modul für geplante Trigger startet ein Szenario, wenn ein neues Projekt hinzugefügt wird, bei dem der authentifizierte Benutzer Mitglied ist.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL GitLab]-Kontos mit [!DNL Workfront] Fusion finden Sie unter <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL GitLab] mit [!DNL Workfront] Fusion</a> in diesem Artikel.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Max Ergebnisse</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus überwachen soll, oder mappen Sie sie.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch repository branches]**

Dieses Modul für geplante Trigger startet ein Szenario, wenn eine neue Verzweigung zu einem Repository hinzugefügt wird.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL GitLab]-Kontos mit [!DNL Workfront] Fusion finden Sie unter <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL GitLab] mit [!DNL Workfront] Fusion</a> in diesem Artikel.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Max Ergebnisse</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus überwachen soll, oder mappen Sie sie.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch repository tags]**

Dieses Instant Trigger-Modul startet ein Szenario, wenn ein Tag in einem Repository erstellt oder gelöscht wird.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Tags überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch snippet comments]**

Dieses Instant Trigger-Modul startet ein Szenario, wenn ein Snippet neu kommentiert wird.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Kommentare überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch todos]**

Dieses Modul für geplante Trigger startet ein Szenario, wenn eine neue Aufgabe hinzugefügt wird. Wenn kein Filter angewendet wird, wird der Trigger ausgeführt, wenn eine neue ausstehende Aufgabe hinzugefügt wird.

Informationen zu Feldern finden Sie unter [Abrufen einer Liste von Aufgaben](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) in der [!DNL GitLab].

+++

+++**[!UICONTROL Watch wiki page]**

Dieses Instant Trigger-Modul startet ein Szenario, wenn eine Wiki-Seite erstellt oder bearbeitet wird.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Wählen Sie den Webhook aus, den Sie für diesen Trigger verwenden möchten, oder fügen Sie einen neuen Webhook hinzu. </p><p>Um einen neuen Webhook hinzuzufügen, <ol><li>Klicken Sie <b>[!UICONTROL Add]</b> neben dem Feld [!UICONTROL webhook] .</li><li>Geben Sie Folgendes ein: <ul><li>Ein Name für den Webhook</li><li>Die Verbindung, die Sie für diesen Webhook verwenden möchten</li><li>Das Projekt, das der Webhook auf Wiki-Seiten überwachen soll</li></ul></li><li>Klicken Sie auf <b>[!UICONTROL Save]</b> , um den Webhook zu speichern und zum Modul zurückzukehren. </td> 
   </tr> 
   </tbody> 
</table>

+++

### Aktionen

+++**[!UICONTROL Accept merge request]**

Dieses Aktionsmodul führt gesendete Änderungen mit der angegebenen Zusammenführungsanfrage zusammen.

Informationen zu Feldern finden Sie unter [Zusammenführungsanfrage akzeptieren](https://docs.gitlab.com/ee/api/merge_requests.html#accept-mr) in der [!DNL GitLab].

+++

+++**[!UICONTROL Cancel a build]**

Dieses Aktionsmodul hebt einen einzelnen Build eines Projekts auf.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL GitLab]-Kontos mit [!DNL Workfront] Fusion finden Sie unter <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL GitLab] mit [!DNL Workfront] Fusion</a> in diesem Artikel.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Wählen Sie das Projekt aus, das den Build enthält, den Sie abbrechen möchten, oder ordnen Sie es zu.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td>Wählen Sie den Build aus, den Sie abbrechen möchten, oder ordnen Sie ihn zu.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Merge commit message]</td> 
   <td> Geben Sie eine Commit-Nachricht für die Zusammenführung ein oder ordnen Sie sie zu.
    </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Should remove source branch]</td> 
   <td>Wählen Sie aus, ob die Quellverzweigung nach Abschluss der Zusammenführung entfernt werden soll.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Merge when build succeeds]</td> 
   <td>Wählen Sie aus, ob die Zusammenführungsanfrage zusammengeführt werden soll, sobald der Build abgeschlossen ist.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL SHA]</td> 
   <td>Falls vorhanden, muss diese SHA mit der HEAD der Quellverzweigung übereinstimmen. Wenn sie nicht übereinstimmt, schlägt die Zusammenführung fehl.</td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Cancel a pipeline's builds]**

Dieses Aktionsmodul hebt die Builds für eine einzelne Pipeline auf.

Informationen zu Feldern finden Sie unter [Abbrechen von Pipeline-Aufträgen](https://docs.gitlab.com/ee/api/pipelines.html#cancel-a-pipelines-jobs) in der [!DNL GitLab].

+++

+++**[!UICONTROL Cancel merge when pipeline succeeds]**

Wenn eine Zusammenführungsanfrage auf Zusammenführen eingestellt ist, wenn eine Pipeline erfolgreich ausgeführt wird, hebt dieses Aktionsmodul diese Aktion auf.

Informationen zu Feldern finden Sie unter [Zusammenführung bei erfolgreicher Pipeline abbrechen](https://docs.gitlab.com/ee/api/merge_requests.html) in der [!DNL GitLab].

+++

+++**[!UICONTROL Cherry pick a commit]**

Dieses Aktionsmodul wählt einen Commit für eine bestimmte Verzweigung aus.

Informationen zu Feldern finden Sie unter [Kirsche einen Commit auswählen](https://docs.gitlab.com/ee/api/commits.html#cherry-pick-a-commit) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create a new label]**

Dieses Aktionsmodul erstellt eine neue Beschriftung für das angegebene Repository.

Informationen zu Feldern finden Sie unter [Erstellen einer neuen Beschriftung](https://docs.gitlab.com/ee/api/labels.html#create-a-new-label) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create a new pipeline]**

Dieses Aktionsmodul erstellt eine neue Pipeline für das angegebene Projekt.

Informationen zu Feldern finden Sie unter [Erstellen einer neuen Pipeline](https://docs.gitlab.com/ee/api/pipelines.html#create-a-new-pipeline) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create a new release]**

Dieses Aktionsmodul fügt Versionshinweise zum vorhandenen Git-Tag hinzu.

Informationen zu Feldern finden Sie unter [Erstellen einer Version](https://docs.gitlab.com/ee/api/releases/#create-a-release) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create a new tag]**

Dieses Aktionsmodul erstellt ein neues Tag im Repository, das auf die angegebene Referenz verweist.

Informationen zu Feldern finden Sie unter [Erstellen eines neuen Tags](https://docs.gitlab.com/ee/api/tags.html#create-a-new-tag) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create a todo]**

Dieses Aktionsmodul erstellt für den aktuellen Benutzer eine Aufgabe für das ausgewählte Problem. Der aktuelle Benutzer ist der Benutzer, der durch die Anmeldeinformationen für die für dieses Modul verwendete Verbindung identifiziert wird.

Informationen zu Feldern finden Sie unter [Erstellen einer Aufgabe](https://docs.gitlab.com/ee/api/issues.html#create-a-todo) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create a todo on a merge request]**

Dieses Aktionsmodul erstellt eine Aufgabe für den aktuellen Benutzer in der ausgewählten Zusammenführungsanfrage. Der aktuelle Benutzer ist der Benutzer, der durch die Anmeldeinformationen für die für dieses Modul verwendete Verbindung identifiziert wird.

Informationen zu Feldern finden [ unter „Erstellen einer ](https://docs.gitlab.com/ee/api/merge_requests.html#create-a-todo)&quot; in der [!DNL GitLab].

+++

+++**[!UICONTROL Create merge request]**

Dieses Aktionsmodul erstellt eine neue Zusammenführungsanfrage für ein Projekt.

Informationen zu Feldern finden Sie unter [Zusammenführungsanfrage erstellen](https://docs.gitlab.com/ee/api/merge_requests.html#create-mr) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create new file in repository]**

Dieses Aktionsmodul erstellt eine neue Datei im ausgewählten Repository.

Informationen zu Feldern finden Sie unter [Erstellen einer neuen Datei im Repository](https://docs.gitlab.com/ee/api/repository_files.html#create-new-file-in-repository) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create new issue note]**

Dieses Aktionsmodul erstellt eine Problemnotiz für ein einzelnes Projektproblem.

Informationen zu Feldern finden Sie [Hinweis zu „Neues Problem erstellen](https://docs.gitlab.com/ee/api/notes.html#create-new-issue-note) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create new merge request note]**

Dieses Aktionsmodul erstellt Notizen für eine einzelne Zusammenführungsanfrage.

Informationen zu Feldern finden Sie [Hinweis für neue Zusammenführungsanfragen erstellen](https://docs.gitlab.com/ee/api/notes.html#create-new-merge-request-note) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create a new milestone]**

Dieses Aktionsmodul erstellt einen neuen Meilenstein für ein Projekt.

Informationen zu Feldern finden Sie unter [Neuen Meilenstein erstellen](https://docs.gitlab.com/ee/api/milestones.html#create-new-milestone) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create new snippet note]**

Dieses Aktionsmodul erstellt eine neue Anmerkung für ein einzelnes Snippet. Snippet Notes sind Kommentare, die Benutzer in einem Snippet posten können.

Informationen zu Feldern finden Sie unter [Neuen Code-Ausschnitt erstellen](https://docs.gitlab.com/ee/api/notes.html#create-new-snippet-note) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create repository branch]**

Dieses Aktionsmodul erstellt eine einzige Repository-Verzweigung.

Informationen zu Feldern finden Sie unter [Repository-Verzweigung erstellen](https://docs.gitlab.com/ee/api/branches.html#create-repository-branch) in der [!DNL GitLab].

+++

+++**[!UICONTROL Create build variable]**

Dieses Aktionsmodul erstellt eine neue Build-Variable.

Informationen zu Feldern finden Sie unter [Variable erstellen](https://docs.gitlab.com/ee/api/project_level_variables.html#create-variable) in der [!DNL GitLab].

+++

+++**[!UICONTROL Delete a merge request]**

Dieses Aktionsmodul ist nur für Administratoren und Projektbesitzer. Dadurch wird die betreffende Zusammenführungsanfrage gelöscht

Informationen zu Feldern finden Sie unter [Löschen einer Zusammenführungsanfrage](https://docs.gitlab.com/ee/api/merge_requests.html#delete-a-merge-request) in der [!DNL GitLab].

+++

+++**[!UICONTROL Delete existing file in repository]**

Dieses Aktionsmodul löscht eine vorhandene Datei aus dem Repository.

Informationen zu Feldern finden Sie unter [Löschen einer vorhandenen Datei im Repository](https://docs.gitlab.com/ee/api/repository_files.html#delete-existing-file-in-repository) in der [!DNL GitLab].

+++

+++**[!UICONTROL Delete repository branch]**

Dieses Aktionsmodul löscht eine Verzweigung aus dem Repository.

Informationen zu Feldern finden Sie unter [Repository-Verzweigung löschen](https://docs.gitlab.com/ee/api/branches.html#delete-repository-branch) in der [!DNL GitLab].

+++

+++**[!UICONTROL Edit issue]**

Dieses Aktionsmodul aktualisiert ein vorhandenes Projektproblem. Dieser Aufruf wird auch verwendet, um ein Problem als geschlossen zu markieren.

Informationen zu Feldern finden Sie unter [Problem bearbeiten](https://docs.gitlab.com/ee/api/issues.html#edit-issue) in der [!DNL GitLab].

+++

+++**[!UICONTROL Edit Milestone]**
Dieses Aktionsmodul aktualisiert einen vorhandenen Projekt-Meilenstein.

Informationen zu Feldern finden Sie unter [Meilenstein bearbeiten](https://docs.gitlab.com/ee/api/milestones.html#edit-milestone) in der [!DNL GitLab].

+++

+++**[!UICONTROL Erase a build]**

Dieses Aktionsmodul löscht einen Build eines Projekts (entfernt Vorgangsartefakte und Vorgangslog).

Informationen zu Feldern finden Sie unter [Auftrag löschen](https://docs.gitlab.com/ee/api/jobs.html#erase-a-job) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get a list of todos]**

Dieses Suchmodul ruft eine Liste von Aufgaben ab.

Informationen zu Feldern finden Sie unter [Abrufen einer Liste von Aufgaben](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get a single build]**

Dieses Aktionsmodul ruft einen einzelnen Auftrag eines Projekts ab.

Informationen zu Feldern finden Sie unter [Abrufen eines einzelnen Auftrags](https://docs.gitlab.com/ee/api/jobs.html#get-a-single-job) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get a single repository tag]**

Dieses Aktionsmodul ruft ein bestimmtes Repository-Tag ab, das durch seinen Namen bestimmt wird.

Informationen zu Feldern finden Sie unter [Abrufen eines einzelnen Repository-Tags](https://docs.gitlab.com/ee/api/tags.html#get-a-single-repository-tag) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get a specific deployment]**

Dieses Aktionsmodul ruft eine bestimmte Bereitstellung ab.

Informationen zu Feldern finden Sie unter [Abrufen einer bestimmten Bereitstellung](https://docs.gitlab.com/ee/api/deployments.html#get-a-specific-deployment) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get all issues assigned to a single milestone]**

Dieses Suchmodul ruft alle Probleme ab, die einem einzelnen Projekt-Milestone zugewiesen sind.

Informationen zu Feldern finden Sie unter [Alle Probleme abrufen, die einem einzelnen Meilenstein zugewiesen sind](https://docs.gitlab.com/ee/api/milestones.html#get-all-issues-assigned-to-a-single-milestone) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get file from repository]**

Dieses Aktionsmodul ruft Informationen über eine Datei im Repository ab, z. B. Name, Größe oder Inhalt.

Informationen zu Feldern finden Sie unter [Datei aus Repository abrufen](https://docs.gitlab.com/ee/api/repository_files.html#get-file-from-repository) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get project users]**

Dieses Suchmodul ruft die Benutzer des Projekts ab.

Informationen zu Feldern finden Sie unter [Abrufen von Projektbenutzenden](https://docs.gitlab.com/ee/api/projects.html#get-project-users) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get a single issue]**

Dieses Aktionsmodul ruft Problemdetails ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Informationen zum Erstellen einer neuen Verbindung finden Sie unter <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">Connect [!DNL GitLab] zu Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td> <p>Wählen Sie das Projekt aus, das das Problem enthält, zu dem Sie Details abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID]</td> 
   <td> <p>Geben Sie den Namen des Problems ein, zu dem Sie Details abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Get single issue note]**

Dieses Aktionsmodul ruft eine einzelne Notiz für ein bestimmtes Projektproblem ab.

Informationen zu Feldern finden Sie unter [Abrufen einer einzelnen Problemnotiz](https://docs.gitlab.com/ee/api/notes.html#get-single-issue-note) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request]**

Dieses Aktionsmodul ruft Informationen über eine einzelne Zusammenführungsanfrage ab.

Informationen zu Feldern finden Sie unter [Einzelne Zusammenführungsanfrage abrufen](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request changes]**

Dieses Suchmodul ruft Informationen zur Zusammenführungsanfrage ab, einschließlich der Dateien und Änderungen.

Informationen zu Feldern finden Sie unter [Änderungen an einzelnen Zusammenführungsanfragen abrufen](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-changes) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request commits]**

Dieses Aktionsmodul ruft eine Liste von Commits für Zusammenführungsanfragen ab.

Informationen zu Feldern finden Sie unter [Abrufen einzelner Commits für Zusammenführungsanfragen](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-commits) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request note]**

Dieses Aktionsmodul gibt für eine gegebene Zusammenführungsanfrage eine einzelne Notiz zurück.

Informationen zu Feldern finden Sie [Hinweis zum Abrufen einer einzelnen Zusammenführungsanfrage](https://docs.gitlab.com/ee/api/notes.html#get-single-merge-request-note) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get a Milestone]**

Dieses Aktionsmodul ruft Meilensteindetails ab.

Informationen zu Feldern finden Sie unter [Abrufen eines einzelnen Meilensteins](https://docs.gitlab.com/ee/api/milestones.html#get-single-milestone) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get single project]**

Dieses Aktionsmodul ruft Projektdetails ab.

Informationen zu Feldern finden Sie unter [Einzelnes Projekt abrufen](https://docs.gitlab.com/ee/api/projects.html#get-single-project) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get single repository branch]**

Dieses Aktionsmodul ruft Details zur Repository-Verzweigung ab.

Informationen zu Feldern finden Sie unter [Einzelne Repository-Verzweigung abrufen](https://docs.gitlab.com/ee/api/branches.html#get-single-repository-branch) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get snippet note]**

Dieses Modul ruft eine einzelne Notiz für einen bestimmten Ausschnitt ab.

Informationen zu Feldern finden Sie unter [Abrufen eines einzelnen Ausschnitts](https://docs.gitlab.com/ee/api/notes.html#get-single-snippet-note) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get the comments of a commit]**

Dieses Suchmodul ruft Kommentare eines Commits in einem Projekt ab.

Informationen zu Feldern finden Sie [Abrufen der Kommentare eines Commits](https://docs.gitlab.com/ee/api/commits.html#get-the-comments-of-a-commit) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get the diff of a commit]**

Dieses Aktionsmodul ruft die Differenz eines Commits in einem Projekt ab.

Informationen zu Feldern finden Sie [Abrufen des Unterschieds eines Commits](https://docs.gitlab.com/ee/api/commits.html#get-the-diff-of-a-commit) in der [!DNL GitLab].

+++

+++**[!UICONTROL Keep artifacts]**

Verhindert, dass Artefakte gelöscht werden, wenn die Gültigkeit festgelegt ist.

Informationen zu Feldern finden Sie unter [Artefakte beibehalten](https://docs.gitlab.com/ee/api/job_artifacts.html#keep-artifacts) in der [!DNL GitLab].

+++

+++**[!UICONTROL List all merge request notes]**

Dieses Suchmodul ruft eine Liste aller Notizen für eine einzelne Zusammenführungsanfrage ab.

Informationen zu Feldern finden Sie unter [Auflisten aller Mergeanforderungshinweise](https://docs.gitlab.com/ee/api/notes.html#list-all-merge-request-notes) in der [!DNL GitLab].

+++

+++**[!UICONTROL List all snippet notes]**

Dieses Modul erhält eine Liste aller Notizen für ein einzelnes Snippet. Snippet Notes sind Kommentare, die Benutzer in einem Snippet posten können.

Informationen zu Feldern finden Sie unter [??](https://docs.gitlab.com/ee/api/notes.html#list-all-snippet-notes) in der [!DNL GitLab].

+++

+++**[!UICONTROL List commit builds]**

Dieses Suchmodul gibt eine Liste von Builds für einen bestimmten Commit in einem Projekt zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Informationen zum Erstellen einer neuen Verbindung finden Sie unter <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">Connect [!DNL GitLab] zu Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Wählen Sie das Projekt aus, das den Commit enthält, für den Sie Builds auflisten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> Um die Suche auf einen bestimmten Status zu beschränken, wählen Sie den Status aus. Wenn Sie dieses Feld leer lassen, werden alle Builds des Commits zurückgegeben.  </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL List issues]**

Dieses Suchmodul gibt alle Probleme entsprechend den angegebenen Filtereinstellungen zurück.

Informationen zu Feldern finden Sie unter [Probleme auflisten](https://docs.gitlab.com/ee/api/issues.html#list-issues) in der [!DNL GitLab].

+++

+++**[!UICONTROL List Issues That Close on Merge]**

Dieses Suchmodul ruft alle Probleme ab, die durch Zusammenführen der angegebenen Zusammenführungsanfrage geschlossen werden würden.

Informationen zu Feldern finden Sie unter [Probleme auflisten, die bei der Zusammenführung geschlossen werden](https://docs.gitlab.com/ee/api/merge_requests.html#list-issues-that-will-close-on-merge) in der [!DNL GitLab].

+++

+++**[!UICONTROL List Labels]**

Dieses Suchmodul ruft alle Bezeichnungen im Projekt ab.

Informationen zu Feldern finden Sie unter [Beschriftungen auflisten](https://docs.gitlab.com/ee/api/labels.html#list-labels) in der [!DNL GitLab].

+++

+++**[!UICONTROL List merge requests]**

Dieses Suchmodul ruft alle Zusammenführungsanfragen anhand der Filtereinstellungen ab.

Informationen zu Feldern finden Sie unter [Auflisten von Zusammenführungsanfragen](https://docs.gitlab.com/ee/api/merge_requests.html#list-merge-requests) in der [!DNL GitLab].

+++

+++**[!UICONTROL List Owned Projects]**

Dieses Suchmodul ruft Projekte ab, bei denen der authentifizierte Benutzer als Eigentümer festgelegt ist.

Informationen zu Feldern finden Sie unter [Benutzerprojekte auflisten](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) in der [!DNL GitLab].

+++

+++**[!UICONTROL List project builds]**

Dieses Suchmodul ruft eine Liste von Builds in einem Projekt ab.

Informationen zu Feldern finden Sie unter [Projektaufträge auflisten](https://docs.gitlab.com/ee/api/jobs.html#list-project-jobs) in der [!DNL GitLab].

+++

+++**[!UICONTROL List project deployments]**

Dieses Suchmodul ruft eine Liste der Bereitstellungen in einem Projekt ab.

Informationen zu Feldern finden Sie unter [Auflisten von Projektbereitstellungen](https://docs.gitlab.com/ee/api/deployments.html#list-project-deployments) in der [!DNL GitLab].

+++

+++**[!UICONTROL List project issue notes]**

Dieses Suchmodul ruft eine Liste aller Hinweise für ein einzelnes Problem ab.

Informationen zu Feldern finden Sie unter [Projektproblemnotizen auflisten](https://docs.gitlab.com/ee/api/notes.html#list-project-issue-notes) in der [!DNL GitLab].

+++

+++**[!UICONTROL List project issues]**

Dieses Suchmodul gibt alle Probleme in einem angegebenen Projekt zurück.

Informationen zu Feldern finden Sie unter [Auflisten von ](https://docs.gitlab.com/ee/api/issues.html#list-project-issues) in der [!DNL GitLab].

+++

+++**[!UICONTROL List project milestones]**

Dieses Suchmodul ruft alle Meilensteine im Projekt ab.

Informationen zu Feldern finden Sie [Projektmeilensteine auflisten](https://docs.gitlab.com/ee/api/milestones.html#list-project-milestones) in der [!DNL GitLab].

+++

+++**[!UICONTROL List project pipelines]**

Dieses Suchmodul ruft alle Pipelines für das Projekt ab.

Informationen zu Feldern finden Sie unter [Auflisten von Projekt](https://docs.gitlab.com/ee/api/pipelines.html#list-project-pipelines)Pipelines in der [!DNL GitLab].

+++

+++**[!UICONTROL List project repository tags]**

Dieses Suchmodul ruft eine Liste von Repository-Tags aus einem Projekt ab, sortiert nach Namen in umgekehrter alphabetischer Reihenfolge.

Informationen zu Feldern finden Sie unter [Projekt-Repository-Tags auflisten](https://docs.gitlab.com/ee/api/tags.html#list-project-repository-tags) in der [!DNL GitLab].

+++

+++**[!UICONTROL List project variables]**

Dieses Suchmodul ruft eine Liste der Variablen eines Projekts ab.

Informationen zu Feldern finden Sie unter [Projektvariablen auflisten](https://docs.gitlab.com/ee/api/project_level_variables.html#list-project-variables) in der [!DNL GitLab].

+++

+++**[!UICONTROL List projects]**

Dieses Suchmodul ruft alle Projekte ab, bei denen der authentifizierte Benutzer Mitglied ist.

Informationen zu Feldern finden Sie unter [Alle Projekte auflisten](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) in der [!DNL GitLab].

+++

+++**[!UICONTROL List repository branches]**

Dieses Modul sucht anhand des Suchbegriffs nach Repository-Verzweigungen.

Informationen zu Feldern finden Sie unter [Repository-Verzweigungen auflisten](https://docs.gitlab.com/ee/api/branches.html#list-repository-branches) in der [!DNL GitLab].

+++

+++**[!UICONTROL List repository commits]**

Dieses Suchmodul ruft eine Liste von Repository-Commits in einem Projekt ab.

Informationen zu Feldern finden Sie unter [Listen-Repository-Commits](https://docs.gitlab.com/ee/api/commits.html#list-repository-commits) in der [!DNL GitLab].

+++

+++**[!UICONTROL List repository contributors]**

Dieses Suchmodul ruft eine Repository-Liste der Mitwirkenden ab.

Informationen zu Feldern finden Sie unter [Mitwirkende](https://docs.gitlab.com/ee/api/repositories.html#contributors) in der [!DNL GitLab].

+++

+++**[!UICONTROL List repository tree]**

Dieses Suchmodul ruft eine Liste von Repository-Dateien und Verzeichnissen in einem Projekt ab.

Informationen zu Feldern finden Sie unter [Repository-Baumstruktur auflisten](https://docs.gitlab.com/ee/api/repositories.html#list-repository-tree) in der [!DNL GitLab].

+++

+++**[!UICONTROL Mark a todo as done]**

Dieses Aktionsmodul kennzeichnet ein einzelnes ausstehendes Aufgabenelement, das durch seine ID als „Erledigt“ für den aktuellen Benutzer angegeben ist.

Informationen zu Feldern finden Sie unter [Markieren eines Aufgabenelements als erledigt](https://docs.gitlab.com/ee/api/todos.html#mark-a-todo-as-done) in der [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing issue note]**

Ändert eine vorhandene Anmerkung eines Problems.

Informationen zu Feldern finden Sie [Hinweis zu vorhandenen Problemen ändern](https://docs.gitlab.com/ee/api/notes.html#modify-existing-issue-note) in der [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing merge request note]**

Ändert die vorhandene Notiz einer Zusammenführungsanfrage.

Informationen zu Feldern finden Sie unter [Notiz zu vorhandenen Zusammenführungsanfragen ändern](https://docs.gitlab.com/ee/api/notes.html#modify-existing-merge-request-note) in der [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing snippet note]**

Dieses Aktionsmodul ändert eine vorhandene Notiz eines Snippets.

Informationen zu Feldern finden Sie unter [Ändern vorhandener Snippets](https://docs.gitlab.com/ee/api/notes.html#modify-existing-snippet-note) in der [!DNL GitLab].

+++

+++**[!UICONTROL New issue]**

Dieses Aktionsmodul erstellt ein neues Projektproblem.

Informationen zu Feldern finden Sie unter [Neues Problem](https://www.integromat.com/en/help/app/gitlab) in der [!DNL GitLab].

+++

+++**[!UICONTROL Play a build]**

Dieses Aktionsmodul Trigger eine manuelle Aktion, um einen Auftrag zu starten.

Informationen zu Feldern finden Sie unter [Wiedergeben eines Auftrags](https://docs.gitlab.com/ee/api/jobs.html#play-a-job) in der [!DNL GitLab].

+++

+++**[!UICONTROL Post comment to commit]**

Dieses Aktionsmodul fügt einen Kommentar zu einem Commit hinzu.

Informationen zu Feldern finden Sie unter [Post comment to commit](https://docs.gitlab.com/ee/api/commits.html#post-comment-to-commit) in der [!DNL GitLab].

+++

+++**[!UICONTROL Remove variable]**

Dieses Aktionsmodul entfernt die Variable eines Projekts.

Informationen zu Feldern finden Sie unter [Variable entfernen](https://docs.gitlab.com/ee/api/project_level_variables.html#remove-variable) in der [!DNL GitLab].

+++

+++**[!UICONTROL Retry a build]**

Dieses Aktionsmodul versucht einen einzelnen Build in einem Commit erneut.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Informationen zum Erstellen einer neuen Verbindung finden Sie unter <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">Connect [!DNL GitLab] zu Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Wählen Sie das Projekt aus, das den Build enthält, den Sie erneut versuchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td> Wählen Sie den Build aus, den Sie erneut versuchen möchten. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Retry Failed Jobs in a Pipeline]**

Dieses Aktionsmodul versucht fehlgeschlagene Builds in einer Pipeline erneut.

Informationen zu Feldern finden Sie unter [Wiederholen von Aufträgen in einer Pipeline](https://docs.gitlab.com/ee/api/pipelines.html#retry-jobs-in-a-pipeline) in der [!DNL GitLab].

+++

+++**[!UICONTROL Get a Variable]**

Dieses Modul ruft Details zur spezifischen Variablen eines Projekts ab.

Informationen zu Feldern finden Sie unter [Variablendetails anzeigen](https://docs.gitlab.com/ee/api/project_level_variables.html#show-variable-details) in der [!DNL GitLab].

+++

+++**[!UICONTROL Update a release]**

Dieses Aktionsmodul aktualisiert eine Version.

Informationen zu Feldern finden Sie unter [Aktualisieren einer Version](https://docs.gitlab.com/ee/api/releases/#update-a-release) in der [!DNL GitLab].

+++

+++**[!UICONTROL Update merge request]**

Dieses Aktionsmodul aktualisiert eine vorhandene Zusammenführungsanfrage. Sie können die Zielverzweigung oder den Titel ändern oder sogar die MR schließen.

Informationen zu Feldern finden Sie unter [Aktualisieren einer Zusammenführungsanfrage](https://docs.gitlab.com/ee/api/merge_requests.html#update-mr) in der [!DNL GitLab].

+++

+++**[!UICONTROL Update a Variable]**

Dieses Aktionsmodul aktualisiert die Variable eines Projekts.

Informationen zu Feldern finden Sie unter [Variable aktualisieren](https://docs.gitlab.com/ee/api/project_level_variables.html#update-variable) in der [!DNL GitLab].

+++
