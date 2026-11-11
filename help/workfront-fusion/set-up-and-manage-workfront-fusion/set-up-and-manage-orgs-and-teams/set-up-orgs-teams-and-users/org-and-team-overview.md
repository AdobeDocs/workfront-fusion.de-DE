---
title: Übersicht über Fusion-Organisationen und -Teams
description: Die Organisations- und Team-Funktionen von Adobe Workfront Fusion ermöglichen es Unternehmen, den Zugriff auf Szenarien und andere Funktionen innerhalb von Fusion zu steuern.
author: Becky
feature: Workfront Fusion
exl-id: 44e6de2a-b2d3-410d-abc3-10facd258495
TQID: 'https://experienceleague.adobe.com/rWg9TitUlX092UIFTY1LUZsR7UlmWwE5dItl6wnlBMA'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: f9cdbcf936fc6b022f6513f47b9b377424731419
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%
---
# Übersicht über Adobe Workfront Fusion-Organisationen und -Teams

Die Organisations- und Team-Funktionen von Adobe Workfront Fusion ermöglichen es Unternehmen, den Zugriff auf Szenarien und andere Funktionen innerhalb von Fusion zu steuern.

Eine Organisation ist die größte Entität in Adobe Workfront Fusion. Beispielsweise kann Ihre Fusion-Organisation das Fusion-Konto für Ihr gesamtes Unternehmen repräsentieren.

Teams sind kleinere Gruppen innerhalb der Organisation und teilen Fusion-Ressourcen wie Szenarien, Verbindungen und Vorlagen.

Anweisungen zum Erstellen eines Teams finden Sie unter [Erstellen eines Teams](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/create-a-team.md).

## Organisationen

Workfront Fusion-Benutzer gehören einer Organisation an.

Benutzer müssen einer Organisation hinzugefügt werden, bevor sie einem Team hinzugefügt werden.

### Organisationsressourcen

Die folgenden Ressourcen wirken sich auf die gesamte Fusion-Organisation aus und werden daher auf Organisationsebene verwaltet:

* **Worker-Pools:** Ein Worker-Pool ist eine Menge von Workfront Fusion-Verarbeitungsressourcen, die einer bestimmten Organisation zugewiesen sind.

  Weitere Informationen finden Sie unter [Arbeitspools](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/worker-pools.md).

* **Vorgänge**: Ein Vorgang in Adobe Workfront Fusion ist eine Aufgabe, die von einem Modul ausgeführt wird.

  Weitere Informationen finden Sie unter [Vorgänge](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

### Organisationsrollen

Ein Benutzer hat in einer Organisation eine der folgenden Rollen:

* **[!UICONTROL Inhaber]**: Der/die Verantwortliche verfügt über alle in der Organisation verfügbaren Berechtigungen.
* **[!UICONTROL Admin]**: Administratoren können Benutzende auf der Adobe Admin Console verwalten, wenn das Unternehmen für Adobe Identity Management System (IMS) aktiviert ist, oder neue Benutzende für Organisationen einladen, die nicht auf IMS arbeiten. Sie können auch Vorlagen genehmigen.
* **[!UICONTROL Mitglied]**: Mitglieder können Workfront Fusion verwenden, aber keine organisatorischen Änderungen vornehmen.
* **[!UICONTROL Buchhalter]**: Buchhalter können Lizenzinformationen im Organisations-Dashboard anzeigen, jedoch keine Aktionen ausführen.
* **[!UICONTROL App-]**: Die Funktionalität für diese Rolle ist derzeit nicht verfügbar und wird in naher Zukunft verfügbar gemacht. Es wird derzeit nicht empfohlen, dieser Rolle Benutzer zuzuweisen.

Informationen zu bestimmten Aktionen, die Benutzern in den einzelnen Organisationsrollen zur Verfügung stehen, finden Sie unter [Organisation und Teamrollen](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

## Teams

Teams sind Benutzergruppen, die den Zugriff auf bestimmte Ressourcen gemeinsam nutzen. Diese Ressourcen können Folgendes umfassen:

* Szenarios
* Verbindungen
* Webhooks
* Schlüssel
* Datenspeicher
* Datenstrukturen
* E-Mail-Benachrichtigungseinstellungen

>[!NOTE]
>
>Da Teams Ressourcen gemeinsam nutzen, ist es manchmal nützlich, wenn ein Team nur ein Mitglied hat. Beispielsweise können Benutzende, die an Schulungen teilnehmen, Verbindungen zu ihren jeweiligen Workfront-Konten erstellen. Alle Teammitglieder können sich auch mit dem jeweiligen Workfront-Konto verbinden. In diesem Fall empfehlen wir, dass der Benutzer das einzige Mitglied eines Schulungsteams ist.

Organisationen können so viele Teams haben, wie sie benötigen, und Benutzer können zu einem oder mehreren Teams gehören.

Benutzer können ihr Team aus der Dropdown-Liste im linken Navigationsbereich auswählen. Benutzende sehen nur Teams, denen sie angehören. Die Auswahl eines Teams ermöglicht einem Benutzer den Zugriff auf die Ressourcen dieses Teams.

### Teamfunktionen

Benutzende haben in jedem ihrer Teams eine der folgenden Rollen:

* **[!UICONTROL Team-]**: Administratoren können die Rolle eines Team-Mitglieds hinzufügen, entfernen oder ändern. Sie können auch alle Aktionen ausführen, die für die anderen Teamfunktionen verfügbar sind.
* **[!UICONTROL Teammitglied]**: Die Rolle „Teammitglied“ ermöglicht Benutzern das Erstellen und Ausführen von Szenarien.
* **[!UICONTROL Team-Überwachung]**: Die Rolle [!UICONTROL Überwachung] ermöglicht Benutzern den Zugriff auf Ausführungsinformationen für Szenarien, sie können jedoch keine Szenarien entwerfen oder ihren „aktiven“ Status ändern.
* **[!UICONTROL Teamoperator]**: Die Rolle [!UICONTROL Operator] ermöglicht es Benutzern, Ausführungsdaten anzuzeigen und den Status „Aktiv“ von Szenarien zu ändern.
* **[!UICONTROL Team Eingeschränktes Mitglied]**: Die Funktionalität für diese Rolle ist derzeit nicht verfügbar und wird in naher Zukunft verfügbar gemacht. Es wird derzeit nicht empfohlen, dieser Rolle Benutzer zuzuweisen.

Informationen zu bestimmten Aktionen, die Benutzern in den einzelnen Team-Rollen zur Verfügung stehen, finden Sie unter [Organisation und Team-Rollen](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

### Benutzerdefinierte Team-Rollen

<!-- BECKY CHECK ME: The source material (the Slack announcement) says flexible permissions are live in QA and for internal customers, with a limited pilot with paid customers next, then general availability. Confirm availability at the 2026-11-12 release before publishing, and whether this section should say that the feature is available only to some organizations. -->

Zusätzlich zu den vordefinierten Team-Rollen verfügt jedes Team über die Registerkarte **[!UICONTROL Rollen]** , auf der Sie Ihre eigenen Rollen erstellen können. Sie können Rollen erstellen, aktualisieren und löschen sowie genau auswählen, welche Berechtigungen jede Rolle enthält. Sie sind nicht mehr auf einen festen Satz von Rollen beschränkt.

Anweisungen finden Sie unter [Teamrollen anzeigen und verwalten](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-and-manage-team-roles.md).

Mit benutzerdefinierten Rollen können Sie:

* Gewähren Sie jeder Person nur den Zugriff, den ihre Arbeit benötigt, wodurch das Risiko versehentlicher Änderungen an kritischen Szenarien reduziert wird.
* Richten Sie den Zugriff so ein, dass er der Funktionsweise Ihres Unternehmens entspricht, anstatt Ihre Teams in die vordefinierten Rollen einzufügen.
* Verwalten Sie den Zugriff selbst, ohne sich an den Support zu wenden.

Jeder Benutzer mit der **[!UICONTROL Mitglieder verwalten]** Berechtigung in einem Team kann Rollen in diesem Team erstellen, aktualisieren, löschen und zuweisen. In den vordefinierten Rollen ist diese Berechtigung in den Rollen Team-Admin und Organisationsverantwortliche enthalten.

* Organisationsverantwortliche können Rollen in allen Teams erstellen und verwalten.
* Organisations-Admins können Rollen nur in den Teams verwalten, denen sie angehören, und wo sie über die Berechtigung **[!UICONTROL Mitglieder verwalten]** verfügen.
* Team-Administratoren können Rollen in ihren Teams verwalten.

<!-- BECKY CHECK ME: The source does not describe the steps in the Roles tab, the list of permissions that you can choose from, or whether you can edit or delete the predefined roles. Add the steps and permissions list once confirmed. Also confirm that Team Admins can manage roles (the source says the Manage members permission was previously given to Team Admin and Org Owner roles, and that team and org admins can create roles only in the teams where they are admins). -->
