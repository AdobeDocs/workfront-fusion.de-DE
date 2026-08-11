---
title: Benachrichtigungsoptionen festlegen
description: Die Optionen für E-Mail-Benachrichtigungen werden auf Team-Ebene festgelegt.
author: Becky
feature: Workfront Fusion
exl-id: 570a09fc-01a9-4952-8a2b-8bfdd86d0bd8
TQID: https://experienceleague.adobe.com/-HytP4gfrhiiSn-dg5ndg1YC6NTMC-NURYzSFgO5kIo
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 90a58033e240271b88d01b9daef9763f38264056
workflow-type: tm+mt
source-wordcount: 665
ht-degree: 13%

---

# Benachrichtigungsoptionen festlegen

Wenn Ihr Unternehmen die Adobe Unified Shell verwendet, erhalten Sie Benachrichtigungen über den Bereich Adobe-Benachrichtigungen .

Wenn Ihre Organisation nicht zur Adobe Unified Shell migriert wurde, können Sie die Benachrichtigungen auswählen, die ein Team erhält. Benachrichtigungen werden auf Team-Ebene festgelegt.

Sie können steuern, für welche Situationen Benachrichtigungen gesendet werden:

* Bei Warnung benachrichtigen: Fusion sendet eine Benachrichtigung, wenn eine Szenarioausführung eine Warnung protokolliert.
* Bei Fehler benachrichtigen: Fusion sendet eine Benachrichtigung, wenn die Ausführung eines Szenarios fehlschlägt.
* Benachrichtigen, wenn das Szenario deaktiviert ist: Fusion sendet eine Benachrichtigung, wenn ein Szenario automatisch deaktiviert wird, z. B. nach zu vielen aufeinander folgenden Fehlern.

Sie können Benachrichtigungen auf Team- oder Szenario-Ebene festlegen. Benachrichtigungen auf Szenario-Ebene setzen Benachrichtigungen außer Kraft, die auf Team-Ebene festgelegt wurden. Das heißt, wenn eine Szenario-Einstellung direkt im Widerspruch zu einer Team-Einstellung steht, wird die Szenario-Einstellung befolgt. Die Team-Benachrichtigungseinstellungen zeigen an, ob es für diese Einstellung Überschreibungen gibt.

Standardmäßig sind alle Benachrichtigungstypen in Workfront Fusion aktiviert.

>[!IMPORTANT]
>
>Um Benachrichtigungen von Workfront Fusion zu erhalten, müssen in den Adobe CX Enterprise-Benachrichtigungseinstellungen Fusion-Benachrichtigungen aktiviert sein. Sie können auf diese Einstellungen zugreifen, indem Sie auf die Benachrichtigungsglocke in der rechten oberen Ecke des Bildschirms und auf das Symbol „Einstellungen“ klicken.

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
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Rolle</td> 
   <td> 
     <p>Sie müssen Mitglied der Fusion-Organisation und des -Teams sein, für die Sie Benachrichtigungseinstellungen anpassen.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Anzeigen und Verwalten der Benachrichtigungseinstellungen auf Team-Ebene

1. Klicken Sie in Workfront Fusion **der linken** auf „Team-Übersicht“.
1. Klicken Sie auf **Registerkarte** Benachrichtigungsoptionen“.

   Die Liste Benachrichtigungsoptionen wird geöffnet. Wenn es Überschreibungen gibt, wird die Anzahl der Überschreibungen neben dieser Einstellung angezeigt.

1. (Bedingt) Wenn es Überschreibungen gibt, zeigen Sie an, welche Szenarien die Team-Benachrichtigungseinstellung überschreiben. Klicken Sie dazu auf das Dreipunkt-Menü.

   Sie können in diesem Menü auf ein Szenario klicken, um direkt zu diesem Szenario zu gelangen.

   ![Menü „Szenario überschreiben“](assets/view-notification-override.png)

1. Informationen zum Wiederherstellen der Standardeinstellungen für einen Benachrichtigungstyp finden Sie unter [Wiederherstellen der ](#restore-notification-defaults)) in diesem Artikel.

Änderungen an der Liste der Benachrichtigungsoptionen werden automatisch gespeichert.

## Festlegen von Benachrichtigungseinstellungen auf Szenario-Ebene

Die Benachrichtigungseinstellungen für einzelne Szenarien werden im Bedienfeld „Szenario-Einstellungen“ für dieses Szenario festgelegt.

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Filter hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf [!UICONTROL Szenario]-Symbol ![Szenario-Einstellungen](assets/scenario-settings-icon.png) am unteren Rand Ihres Szenarios.
1. Klicken Sie im Bedienfeld Szenario-Einstellungen **unten** Bedienfeld auf „Erweiterte Einstellungen anzeigen“.
1. Passen Sie die Einstellungen **Bei** benachrichtigen **„Bei Fehler benachrichtigen** und **Bei deaktiviertem Szenario benachrichtigen** nach Bedarf an.
1. Klicken Sie auf **OK**, um die Szenario-Einstellungen zu speichern und zu beenden.

## Standardeinstellungen für Benachrichtigungen wiederherstellen

Sie können eine Team-Benachrichtigungseinstellung auf der Registerkarte Benachrichtigungsoptionen auf die Standardeinstellung zurücksetzen. Dadurch wird die Benachrichtigungsoption auf „Aktiviert“ gesetzt und es werden alle Szenario-Benachrichtigungsüberschreibungen für diesen Benachrichtigungstyp entfernt.

Wenn für den Benachrichtigungstyp derzeit der Standardwert festgelegt ist, wird das Symbol **Auf Standard wiederherstellen** nicht angezeigt.

1. Klicken Sie in Workfront Fusion **der linken** auf „Team-Übersicht“.
1. Klicken Sie auf **Registerkarte** Benachrichtigungsoptionen“.

   Die Liste Benachrichtigungsoptionen wird geöffnet. Wenn für einen Benachrichtigungstyp derzeit nicht der Standard festgelegt ist, wird für diesen Benachrichtigungstyp das Symbol „In Standard wiederherstellen“ angezeigt.

   ![Auf Standard zurücksetzen sichtbar](assets/restore-notification-defaults.png)

1. Um die Standardeinstellungen für diesen Benachrichtigungstyp wiederherzustellen, einschließlich etwaiger Szenarioüberschreibungen, klicken Sie auf das Symbol **Auf Standard zurücksetzen** ![Auf Standard zurücksetzen](assets/restore-default-icon.png) für diesen Benachrichtigungstyp.

Änderungen an der Liste der Benachrichtigungsoptionen werden automatisch gespeichert.

<!--

## Set notification options

If your organization is not on the Adobe Unified Shell, you can set notification settings directly in Fusion.

Email notification options are set on the team level.

1. In the left navigation panel, click **[!UICONTROL Team]**
1. Select the **[!UICONTROL Notification Options]** tab.
1. Enable the notifications that you want the team to receive.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">'[!UICONTROL Warning in scenario run]'</td> 
      <td> <p>Receive an email when there is a warning in a scenario run</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Errors in scenario run]</td> 
      <td>Receive an email when there is an error in a scenario run.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Scenario deactivation]</p> </td> 
      <td><p>Receive an email when a scenario deactivates.</p><p>In some cases, a scenario might be deactivated by the Workfront Fusion engineering team because the scenario is causing performance or other issues. In these cases, you do not receive notifications in Workfront Fusion. </p></td>

</tr>
</tbody>
</table>

Changes to notification options save automatically.

-->
