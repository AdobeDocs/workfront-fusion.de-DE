---
title: Teamrollen anzeigen und verwalten
description: Jedes Team verfügt über eine Registerkarte Rollen , auf der Sie die Rollen des Teams anzeigen, eigene Rollen erstellen, die in den einzelnen Rollen enthaltenen Berechtigungen auswählen und Rollen aktualisieren oder löschen können.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: a3a6922afd713cd002cdf472c7ef62c1855b80d9
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 10%
---
# Teamrollen anzeigen und verwalten

Sie können die in einem Team verfügbaren Rollen anzeigen, eigene Rollen erstellen und auswählen, welche Berechtigungen jede Rolle enthält. Sie können Rollen auch aktualisieren und löschen.

Benutzerdefinierte Rollen bieten die folgenden Vorteile:

* Jedes Teammitglied hat nur den Zugriff, den sein Job benötigt, wodurch das Risiko versehentlicher Änderungen an kritischen Szenarien reduziert wird.
* Benutzerdefinierte Rollen können besser an die Arbeitsweise Ihres Unternehmens anpassen, anstatt Ihre Teams in die vordefinierten Rollen einzufügen.
* Sie können den Zugriff selbst verwalten, ohne sich an den Support zu wenden.

Eine Übersicht über Organisationen, Teams und die vordefinierten Team-Rollen finden Sie unter [Organisation und Team - Übersicht](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/org-and-team-overview.md). Informationen zu den in den vordefinierten Rollen enthaltenen Berechtigungen finden Sie unter [Organisations- und Team-Rollen](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Ein beliebiges Adobe Workfront Workflow- und Adobe Workfront Automation and Integration-Paket</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene</td> 
   <td> 
     <p>Sie müssen über die Berechtigung <b>[!UICONTROL Mitglieder verwalten]</b> im Team verfügen. In den vordefinierten Rollen ist diese Berechtigung in den Rollen Team-Admin und Organisationsverantwortliche enthalten.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Wer kann Teamrollen verwalten?

Jeder Benutzer mit der **[!UICONTROL Mitglieder verwalten]** Berechtigung in einem Team kann Rollen in diesem Team erstellen, aktualisieren, löschen und zuweisen.

* Organisationsverantwortliche können Rollen in allen Teams erstellen und verwalten.
* Organisations-Admins können Rollen nur in den Teams verwalten, denen sie angehören, und wo sie über die Berechtigung **[!UICONTROL Mitglieder verwalten]** verfügen.
* Team-Administratoren können Rollen in ihren Teams verwalten.

## Erstellen oder Bearbeiten einer Rolle

1. Klicken Sie in Fusion in der linken Navigation auf **Team-Übersicht**.
1. (Bedingt) Wenn Sie sich nicht auf der Seite für das Team befinden, für das Sie Rollen anzeigen möchten, klicken Sie oben auf der Seite auf **Team** Dropdown-Liste und wählen Sie das richtige Team aus.
1. Öffnen Sie die Registerkarte **[!UICONTROL Rollen]**.

   Auf der Registerkarte werden die im Team verfügbaren Rollen aufgelistet, einschließlich der vordefinierten Rollen. Für jede Rolle werden in der Liste der Name der Rolle und eine Zusammenfassung der zugehörigen Berechtigungen angezeigt, z. B. „Keine Berechtigungen“, „Mitglied“ oder „Benutzerdefiniert ・ 19 Berechtigungen“.

1. Um eine Rolle zu erstellen, klicken Sie auf **[!UICONTROL Rolle erstellen]**.

   ODER

   Um eine Rolle zu bearbeiten, klicken **[!UICONTROL in]** Zeile der Rolle, die Sie bearbeiten möchten, auf „Bearbeiten“.

   <!-- BECKY CHECK ME: The Edit button is available for the predefined roles as well as custom roles. Confirm the title of the edit page, whether you can rename the predefined roles, and what happens to users who already have the role. -->

1. Geben Sie einen Namen für die Rolle im Feld **[!UICONTROL Rollenname]** ein.
1. Wählen **[!UICONTROL in der Dropdown]** Liste Rollenvorlage die Vorlage aus, von der aus Sie beginnen möchten.

   Die Vorlage legt die anfänglichen Berechtigungen für die Rolle fest. Die Standardvorlage ist **[!UICONTROL Viewer]**.

1. Wählen Sie im Bereich **[!UICONTROL Umfangreiche]**&quot; die Berechtigungen aus, die die Rolle einschließen soll.

   Berechtigungen werden nach Bereichen gruppiert, z. B **[!UICONTROL &quot;]**&quot;, **[!UICONTROL Verbindungen]** und **[!UICONTROL Team]**. Für jeden Bereich haben Sie folgende Möglichkeiten:

   * Um alle Berechtigungen in einem Bereich gleichzeitig festzulegen, klicken Sie neben dem Namen des Bereichs auf **[!UICONTROL Kein Zugriff]**, **[!UICONTROL Nur]** oder **[!UICONTROL Vollständiger Zugriff]**.
   * Um bestimmte Berechtigungen auszuwählen, aktivieren oder deaktivieren Sie für jede Berechtigung das Kontrollkästchen.

   Eine Liste der Berechtigungen finden Sie unter [Berechtigungen, die Sie in eine Rolle einbeziehen können](#permissions-that-you-can-include-in-a-role) in diesem Artikel.

   <!-- BECKY CHECK ME: Confirm the options in the Role template dropdown and what each one selects. Confirm exactly what No access, View only, and Full access select in each area (in the screenshot, View only selects the view permissions). Confirm whether there is a Description field, and whether there are areas below Team on the page (the screenshots end at Team). -->

1. Klicken Sie auf **[!UICONTROL Speichern]**. Um die Seite ohne Speichern zu schließen, klicken Sie auf **[!UICONTROL Abbrechen]**.
1. (Optional) Um eine Rolle zu löschen, klicken **[!UICONTROL in der]** der Rolle auf der Registerkarte **[!UICONTROL Rollen]** auf „Löschen“.

   <!-- BECKY CHECK ME: Confirm why the Delete button is unavailable (dimmed) for some roles, such as Team Operator, Team Member, and Team Admin in the screenshot, whether there is a confirmation prompt, and what happens to users who have the role. Update this step and add a note, if needed. -->

Eine von Ihnen erstellte Rolle ist im Team verfügbar. Sie können sie Team-Mitgliedern zuweisen.

### Berechtigungen, die Sie in eine Rolle einbeziehen können

<table style="table-layout:auto">
 <col>
 <col>
 <thead>
  <tr>
   <th>Bereich</th>
   <th>Berechtigungen</th>
  </tr>
 </thead>
 <tbody>
 <tr>
   <td role="rowheader">[!UICONTROL Automations]</td>
   <td>Liste anzeigen, Details anzeigen, Ausführungsverlauf anzeigen, Benachrichtigungen verwalten, Statistiken zurücksetzen, Einmal ausführen, Zeitplan bearbeiten, Aktivieren, Deaktivieren, Erstellen, Bearbeiten, Veröffentlichen, Löschen</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Unvollständige Ausführungen]</td>
   <td>Anzeigen, verwalten</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Webhooks]</td>
   <td>Anzeigen, Anzeigen der Warteschlange, Erstellen, Bearbeiten, Verwalten der Warteschlange, Ändern der Priorität, Löschen</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Verbindungen]</td>
   <td>Anzeigen, Erstellen, Bearbeiten, Löschen</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL -Schlüssel]</td>
   <td>Anzeigen, Erstellen, Bearbeiten, Löschen</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Datenspeicher]</td>
   <td>Liste anzeigen, Datensätze durchsuchen, erstellen, bearbeiten, löschen</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Datenstrukturen]</td>
   <td>Anzeigen, Erstellen, Bearbeiten, Löschen</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Vorlagen]</td>
   <td>Liste anzeigen, Details anzeigen, Erstellen, Bearbeiten, Löschen</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Team]</td>
   <td>Team anzeigen, Team-Einstellungen bearbeiten, Mitglieder verwalten, Team löschen</td>
  </tr>
 </tbody>
</table>

<!-- BECKY CHECK ME: Confirm that this list is complete, and add a description of what each permission allows, if needed. The list is taken from the Create role page, which may have more areas below Team. -->

## Rollen in ein anderes Team klonen

Sie können die Rollen in einem Team in ein anderes Team kopieren, sodass Sie nicht dieselben Rollen in jedem Team neu erstellen müssen.

1. Öffnen Sie die Registerkarte **[!UICONTROL Rollen]** des Teams, wie in [Erstellen oder Bearbeiten einer Rolle](#create-or-edit-a-role) in diesem Artikel beschrieben.
1. Klicken Sie **[!UICONTROL Zum Team klonen]**.

   Die Seite **[!UICONTROL Rollen in ein anderes Team klonen]** wird geöffnet.

1. Wählen **[!UICONTROL in der Dropdown]** Liste „Target-Team“ das Team aus, dem Sie die Rollen klonen möchten.

   Es wird eine Tabelle angezeigt, in der die Rollen im aktuellen Team aufgeführt sind.

1. Überprüfen und legen Sie für jede Rolle in der Tabelle Folgendes fest:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Source-Rolle]</td> 
      <td> <p>Die Rolle im aktuellen Team mit einer Zusammenfassung seiner Berechtigungen.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Aktion]</td> 
      <td> <p>Was ist mit der Rolle zu tun? Beispielsweise kopiert <b>[!UICONTROL Copy into existing role]</b> die Berechtigungen der Quellrolle in eine Rolle, die bereits im Zielteam vorhanden ist.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Target]</td> 
      <td> <p>Die Rolle im Zielteam, in die die Quellrolle kopiert wird.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL -Änderungen]</td> 
      <td> <p>Ob sich die Zielrolle von der Quellrolle unterscheidet. <b>[!UICONTROL Already in sync]</b> bedeutet beispielsweise, dass die Zielrolle bereits über dieselben Berechtigungen wie die Quellrolle verfügt.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Benutzende]</td> 
      <td> <p>Informationen zu Benutzern, die die Rolle haben. <b>[!UICONTROL No match users]</b> bedeutet beispielsweise, dass keine einzuschließenden Benutzer vorhanden sind.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Status]</td> 
      <td> <p>Das Ergebnis für die Rolle nach dem Klonen.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **[!UICONTROL Klonen]**. Um die Seite ohne Klonen zu schließen, klicken Sie auf **[!UICONTROL Abbrechen]**.

<!-- BECKY CHECK ME: The screenshot shows the Clone roles to another team page after a target team is selected. Confirm the options in the Action dropdown (for example, whether you can create a new role in the target team), the options in the Target dropdown, what the checkbox in the Users column does (for example, whether it also assigns the role to matching users in the target team) and what "matching users" means, what the Changes column shows when the roles differ, and what the Status column shows before and after you clone. -->

<!-- BECKY CHECK ME: Confirm whether the Target team dropdown lists all teams or only the teams that you can manage, and whether the Clone to team button is visible to everyone who can manage roles. -->

## Einem Benutzer eine Rolle zuweisen

Eine benutzerdefinierte Rolle wird auf die gleiche Weise zugewiesen wie eine vordefinierte Rolle. Anweisungen finden Sie unter [Benutzer zu einem Team hinzufügen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md) und [Benutzerrollen anzeigen oder bearbeiten](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md#view-or-edit-user-roles-for-a-team).

<!-- BECKY CHECK ME: Confirm that custom roles appear in the role dropdowns in both of these procedures. -->

## Zu beachten

* Kaskadierte Organisationsberechtigungen. Um jemandem Zugriff auf die Durchführung einer Aktion in allen Teams zu gewähren, weisen Sie eine Organisationsrolle zu, anstatt eine Teamrolle zu erstellen. Weitere Informationen finden Sie unter [Organisations- und Teamrollen](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).
* Die von Ihnen erstellten Rollen gehören zu einem Team.

<!-- BECKY CHECK ME: The Slack thread says that defining a role that is available in all teams was out of scope for the initial release. Confirm that a role belongs to a single team, and that you clone it to use it in another team. -->
