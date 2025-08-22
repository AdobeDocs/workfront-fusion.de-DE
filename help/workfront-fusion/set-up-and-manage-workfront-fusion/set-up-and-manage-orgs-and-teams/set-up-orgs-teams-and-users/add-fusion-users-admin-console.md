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
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 2%

---

# Hinzufügen von Benutzern zu Adobe Workfront Fusion über die Adobe Admin Console

Sie können einen Benutzer zum [!DNL Adobe Admin Console] hinzufügen und ihn Adobe Workfront Fusion zuweisen, oder einen vorhandenen Benutzer im [!DNL Adobe Admin Console] Workfront Fusion zuweisen.

Ein Video, in dem Workfront Fusion in der [!DNL Adobe Admin Console] beschrieben wird, einschließlich der Vorgehensweise beim Hinzufügen von Benutzern, finden Sie unter [[!DNL Fusion] auf Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.



Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Plan*</td> 
   <td> <p>[!UICONTROL Pro] oder höher</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz*</td> 
   <td> <p>[!UICONTROL -Plan], [!UICONTROL -Arbeit]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den Plan [!UICONTROL Select] oder [!UICONTROL Prime] Adobe Workfront verfügen, muss Ihr Unternehmen Adobe Workfront Fusion sowie Adobe Workfront erwerben, um die in diesem Artikel beschriebenen Funktionen nutzen zu können. Workfront Fusion ist im Workfront-Plan [!UICONTROL Ultimate] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss Adobe Workfront Fusion sowie Adobe Workfront erwerben, um die in diesem Artikel beschriebenen Funktionen nutzen zu können.</p>
   </td> 
  </tr>
   <tr> 
   <td role="rowheader">[!DNL Adobe] Administratorrechte</td> 
   <td>Sie müssen [!UICONTROL Product Configuration Administrator] für [!DNL Adobe] Produkte für Ihre Organisation sein.</td> 
  </tr>
  </tbody> 
</table>

&#42;Wenden Sie sich an Ihren Workfront-Administrator, um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

&#42;&#42;Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



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
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Plan für [!UICONTROL Select] oder [!UICONTROL Prime] Workfront: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>[!UICONTROL Ultimate] Workfront-Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Unternehmen sein.</p>
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Team sein.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
