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
source-git-commit: f7c1d5b1de74cc0c59e3a00938bed14b489500db
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 1%

---

# Hinzufügen von Benutzern zu Adobe Workfront Fusion über die Adobe Admin Console

Sie können einen Benutzer zum [!DNL Adobe Admin Console] hinzufügen und ihn Adobe Workfront Fusion zuweisen, oder einen vorhandenen Benutzer im [!DNL Adobe Admin Console] Workfront Fusion zuweisen.

Ein Video, in dem Workfront Fusion in der [!DNL Adobe Admin Console] beschrieben wird, einschließlich der Vorgehensweise beim Hinzufügen von Benutzern, finden Sie unter [[!DNL Fusion] auf Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.

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
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene</td> 
   <td> 
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Unternehmen sein.</p>
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Team sein.</p>
   </td> 
  </tr> 
  </tr>
   <tr> 
   <td role="rowheader">Konfigurationen der Zugriffsebene</td> 
   <td>Sie müssen Produktkonfigurations-Administrator von Adobe-Produkten für Ihr Unternehmen sein.</td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Voraussetzungen

Bevor Sie den [!DNL Admin Console] für Workfront verwenden, sollten Sie eine E-Mail erhalten, in der Sie zur -Konsole eingeladen werden.

1. Wenn Sie [!DNL Adobe] noch nicht kennen und eine E-Mail erhalten haben, in der Sie darauf hingewiesen werden, dass Sie jetzt über Administratorrechte für die Verwaltung [!DNL Adobe] Software und Services für Ihr Unternehmen verfügen, klicken Sie auf die Schaltfläche in der E-Mail, um ein [!DNL Adobe] Konto zu erstellen, und öffnen Sie die [!DNL Admin Console].

   Oder

   Wenn Sie bereits über ein Adobe-Konto verfügen, gehen Sie zur [[!DNL Adobe Admin Console] Seite](https://adminconsole.adobe.com).


## Hinzufügen eines neuen Benutzers zu [!DNL Adobe Admin Console] und Workfront Fusion

1. Wählen Sie auf [[!DNL Adobe Admin Console] Seite](https://adminconsole.adobe.com/) die Registerkarte **[!UICONTROL Produkte]** in der oberen Navigationsleiste und wählen Sie dann die Produktkachel **Workfront**.

   ![Fusion in Admin Console](assets/fusion-product-admin-console.png)

1. Wählen Sie in der angezeigten Liste die Organisation aus, der Sie einen Benutzer hinzufügen möchten.

   ![Fusion-Instanz in Admin Console](assets/fusion-instances-admin-console.png)

1. Klicken Sie in der angezeigten Liste bei **[!UICONTROL ausgewählten Registerkarte]** Produktprofile“ auf den Namen des Links Workfront [!UICONTROL Produktprofil].

   >[!IMPORTANT]
   >
   > Nehmen Sie keine Änderungen am [!UICONTROL Produktprofil] vor.

1. Klicken Sie **[!UICONTROL der]** „Benutzer“ oberhalb der Liste auf **[!UICONTROL Benutzer hinzufügen]**.

1. Geben **[!UICONTROL im Feld „Benutzer zu diesem Produktprofil hinzufügen]** die E-Mail-Adresse oder den Namen eines Benutzers ein, den Sie hinzufügen möchten, und wählen Sie dann den Benutzer in der angezeigten Liste aus.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Die Benutzerin bzw. der Benutzer wird in Workfront Fusion erstellt.

1. (Optional) Fahren Sie mit [Ändern der Zugriffsebene von Benutzenden in Workfront Fusion fort](#change-a-users-access-level-in-workfront-fusion)

## Ändern der Zugriffsebene von Benutzenden in Workfront Fusion

* [Benutzerrolle in „Admin“ ändern](#change-a-users-role-to-admin)
* [Rolle eines Benutzers in „Mitglied“, „Buchhalter“ oder „App-Entwickler“ ändern](#change-a-users-role-to-member-accountant-or-app-developer)

### Benutzerrolle in „Admin“ ändern

Die Zuweisung einer Administratorrolle an einen Benutzer muss in der [!DNL Adobe Admin Console] erfolgen.

1. Wählen Sie auf der Seite [!UICONTROL Produktprofil] von Workfront Fusion, auf der Sie den Benutzer hinzugefügt haben, die Registerkarte **[!UICONTROL Administratoren]** aus.

1. Klicken Sie **[!UICONTROL Admin hinzufügen]**.

1. Geben **[!UICONTROL im Feld „Produktprofil-]** hinzufügen“ die E-Mail-Adresse oder den Namen des Benutzers ein, der Administrator werden soll, und wählen Sie dann den Benutzer in der angezeigten Liste aus.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Der Benutzer ist jetzt Administrator in Workfront Fusion.

### Rolle eines Benutzers in „Mitglied“, „Buchhalter“ oder „App-Entwickler“ ändern

Die Rollen „Mitglied“, „Buchhalter“ und „App-Entwickler“ werden in Workfront Fusion verwaltet.

Anweisungen finden Sie unter [Anzeigen oder Bearbeiten von Benutzerrollen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md).

## Zuweisen eines bestehenden Benutzers in der [!DNL Adobe Admin Console] zu Workfront Fusion

Sie können einen vorhandenen Benutzer zu einem Team in Fusion hinzufügen. Dies wird innerhalb von Fusion gehandhabt.

Anweisungen finden Sie unter [Hinzufügen eines Benutzers zu einem Team](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md).
