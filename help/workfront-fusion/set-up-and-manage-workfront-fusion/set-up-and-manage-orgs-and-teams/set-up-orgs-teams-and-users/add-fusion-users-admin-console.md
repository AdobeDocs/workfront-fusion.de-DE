---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Hinzufügen von Benutzern zu Adobe Workfront Fusion über die Adobe Admin Console
description: Sie können einen Benutzer zur Adobe Admin Console hinzufügen und ihn Adobe Workfront Fusion zuweisen, oder Sie können einen vorhandenen Benutzer in der Adobe Admin Console Workfront Fusion zuweisen.
author: Becky
feature: Workfront Fusion
exl-id: 7cb1c1a7-3c7a-459a-818f-d9cefcb9988b
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---

# Hinzufügen von Benutzern zu Adobe Workfront Fusion über die Adobe Admin Console

Sie können einen Benutzer zum [!DNL Adobe Admin Console] hinzufügen und ihn [!DNL Adobe Workfront Fusion] zuweisen oder einen vorhandenen Benutzer im [!DNL Adobe Admin Console] zum [!DNL Workfront Fusion] zuweisen.

Ein Video, das [!DNL Workfront Fusion] in der [!DNL Adobe Admin Console] beschreibt, einschließlich der Hinzufügung von Benutzern, finden Sie unter [[!DNL Fusion] auf Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.



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
   <tr> 
   <td role="rowheader">[!DNL Adobe] Administratorrechte</td> 
   <td>Sie müssen eine [!UICONTROL Product Configuration Administrator] von [!DNL Adobe] Produkten für Ihr Unternehmen sein.</td> 
  </tr>
  </tbody> 
</table>

&#42;Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

&#42;&#42;Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Packstück</td> 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz</td> 
   <td> <p>Neu: [!UICONTROL Standard]</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuell: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>[!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Workfront]: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein [!DNL Workfront Fusion]-Administrator für Ihre Organisation sein.</p>
     <p>Sie müssen [!DNL Workfront Fusion] für Ihr Team sein.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++


## Voraussetzungen

Bevor Sie den [!DNL Admin Console] für die [!DNL Workfront] verwenden, sollten Sie eine E-Mail erhalten, in der Sie zur Konsole eingeladen werden.

1. Wenn Sie [!DNL Adobe] noch nicht kennen und eine E-Mail erhalten haben, in der Sie darauf hingewiesen werden, dass Sie jetzt über Administratorrechte für die Verwaltung [!DNL Adobe] Software und Services für Ihr Unternehmen verfügen, klicken Sie auf die Schaltfläche in der E-Mail, um ein [!DNL Adobe] Konto zu erstellen, und öffnen Sie die [!DNL Admin Console].

   Oder

   Wenn Sie bereits über ein Adobe-Konto verfügen, gehen Sie zur [[!DNL Adobe Admin Console] Seite](https://adminconsole.adobe.com).


## Hinzufügen eines neuen Benutzers zur [!DNL Adobe Admin Console] und [!DNL Workfront Fusion]

1. Wählen [[!DNL Adobe Admin Console]  auf der ](https://adminconsole.adobe.com/) die Registerkarte **[!UICONTROL Products]** in der oberen Navigationsleiste und klicken Sie dann auf die Kachel Produkt **[!DNL Workfront Fusion]** .

   ![Fusion in der Admin Console ](assets/fusion-product-admin-console.png)

1. Wählen Sie in der angezeigten Liste die Organisation aus, der Sie einen Benutzer hinzufügen möchten.

   ![Fusion-Instanz in Admin Console](assets/fusion-instances-admin-console.png)

1. Klicken Sie in der angezeigten Liste bei ausgewählter Registerkarte **[!UICONTROL Product Profiles]** auf den Namen des Links [!DNL Workfront Fusion] [!UICONTROL Product Profile] .

   >[!IMPORTANT]
   >
   > Nehmen Sie keine Änderungen am [!UICONTROL Product Profile] selbst vor.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Users]** , die über der Liste ausgewählt ist, und dann auf **[!UICONTROL Add User]**.

1. Geben Sie im **[!UICONTROL Add users to this product profile]** die E-Mail-Adresse oder den Namen eines Benutzers ein, den Sie hinzufügen möchten, und wählen Sie dann den Benutzer in der angezeigten Liste aus.

1. Klicken Sie auf **[!UICONTROL Save]**.

   Der Benutzer wird in [!DNL Workfront Fusion] erstellt.

1. (Optional) Fahren Sie mit [Ändern der Zugriffsebene von Benutzenden in fort [!DNL Workfront Fusion]](#change-a-users-access-level-in-workfront-fusion)

## Ändern der Zugriffsebene von Benutzenden in Workfront Fusion

* [Benutzerrolle in „Admin“ ändern](#change-a-users-role-to-admin)
* [Rolle eines Benutzers in „Mitglied“, „Buchhalter“ oder „App-Entwickler“ ändern](#change-a-users-role-to-member-accountant-or-app-developer)

### Benutzerrolle in „Admin“ ändern

Die Zuweisung einer Administratorrolle an einen Benutzer muss in der [!DNL Adobe Admin Console] erfolgen.

1. Wählen Sie auf der Seite [!DNL Workfront Fusion]-[!UICONTROL Product Profile], auf der Sie den Benutzer hinzugefügt haben, die Registerkarte **[!UICONTROL Admins]** aus.

1. Klicken Sie auf **[!UICONTROL Add Admin]**.

1. Geben Sie in das **[!UICONTROL Add product profile administrators]** die E-Mail-Adresse oder den Namen des Benutzers ein, der Administrator werden soll, und wählen Sie dann den Benutzer in der angezeigten Liste aus.

1. Klicken Sie auf **[!UICONTROL Save]**.

   Der Benutzer ist jetzt Administrator in [!DNL Workfront Fusion].

### Rolle eines Benutzers in „Mitglied“, „Buchhalter“ oder „App-Entwickler“ ändern

Die Rollen „Mitglied“, „Buchhalter“ und „App-Entwickler“ werden in Workfront Fusion verwaltet.

Anweisungen finden Sie unter [Anzeigen oder Bearbeiten von Benutzerrollen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md).

## Zuweisen eines vorhandenen Benutzers in der [!DNL Adobe Admin Console] zu [!DNL Workfront Fusion]

Sie können einen vorhandenen Benutzer zu einem Team in Fusion hinzufügen. Dies wird innerhalb von Fusion gehandhabt.

Anweisungen finden Sie unter [Hinzufügen eines Benutzers zu einem Team](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md).
