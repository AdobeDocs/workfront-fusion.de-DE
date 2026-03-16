---
title: Verwalten von Adobe Workfront Fusion-Benutzern in Ihrer Organisation
description: Verwalten von Adobe Workfront Fusion-Benutzern in Ihrer Organisation
author: Becky
feature: Workfront Fusion
exl-id: 32c221fa-856b-4921-9fa6-5e60f2aa08cd
source-git-commit: 3f9390d8947ef2666336c1a4cc6eab8d174849d5
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 18%

---

# Anzeigen oder Bearbeiten von Benutzerrollen

Adobe Workfront Fusion-Administratoren können Benutzerrollen in Workfront Fusion verwalten.


>[!NOTE]
>
>Wenn Ihr Unternehmen derzeit zur Adobe Admin Console wechselt, können Sie in Workfront keine Benutzenden verwalten (Benutzende hinzufügen oder löschen). Sie können diese Aktionen nach Abschluss der Migration in der Adobe Admin Console ausführen.

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
   <td role="rowheader">Konfigurationen der Zugriffsebene</td> 
   <td> 
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Unternehmen sein.</p>
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Team sein.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Anzeigen oder Bearbeiten von Benutzerrollen für eine Organisation

Adobe Workfront Fusion-Administratoren können Benutzerrollen für ein Unternehmen anzeigen und aktualisieren.

1. Wählen Sie, während Sie als Workfront Fusion-Administrator angemeldet sind **[!UICONTROL im linken Navigationsbereich]** Alle Benutzer“ aus.
1. Klicken Sie **[!UICONTROL Details]** in der Zeile des Benutzers, den Sie anzeigen möchten.
1. (Optional) Um die Rolle des Benutzers in einer Organisation zu aktualisieren, klicken Sie auf das Dropdown-Menü in der Spalte **[!DNL Role]** in der Zeile der Organisation, in der Sie die Rolle des Benutzers ändern möchten, und wählen Sie dann die neue Rolle aus.

### Überlegungen beim Hinzufügen oder Ändern von Organisationseigentümern

Ihr Unternehmen kann über mehr als einen Eigentümer verfügen.

Beachten Sie beim Zuweisen eines Benutzers zu oder von einer Eigentümerrolle Folgendes.

* Nur ein Inhaber kann die Rolle „Inhaber“ zuweisen oder einem aktuellen Inhaber eine andere Rolle zuweisen.
* Nur Administratoren können ein Upgrade auf Inhaber durchführen.
* Wenn es nur einen Eigentümer gibt, kann diese Eigentümerrolle nicht geändert oder entfernt werden.
* Wenn nur ein Eigentümer vorhanden ist, kann dieser nicht gelöscht werden, wenn andere Benutzer in der Organisation vorhanden sind.
* Wenn Admins die Rolle „Eigentümer“ zugewiesen wird, werden sie automatisch zu Admins in allen Teams innerhalb der Organisation.
* Wenn ein Eigentümer einer anderen Rolle zugewiesen wird, wird dieser Benutzer automatisch in allen Teams zum Team-Mitglied.
* Wenn ein neues Team erstellt wird, werden alle Eigentümer automatisch als Team-Admins zugewiesen.

## Anzeigen oder Bearbeiten von Benutzerrollen für ein Team

Adobe Workfront Fusion-Administratoren und Team-Administratoren können Benutzerrollen anzeigen und aktualisieren.

1. Wählen Sie, während Sie als Workfront Fusion-Administrator angemeldet sind **[!UICONTROL im linken Navigationsbereich]** Alle Benutzer“ aus.
1. Klicken Sie **[!UICONTROL Details]** in der Zeile des Benutzers, den Sie anzeigen möchten.
1. Klicken Sie auf das Symbol Teams in der Spalte **[!DNL Role]** in der Zeile der Organisation, die das Team enthält, in dem Sie die Rolle des Benutzers anzeigen oder bearbeiten möchten.
1. (Optional) Um die Rolle des Benutzers in einem Team zu aktualisieren, klicken Sie auf das Dropdown-Menü in der Spalte **[!DNL Role]** in der Zeile des Teams, in der Sie die Rolle des Benutzers ändern möchten, und wählen Sie dann die neue Rolle aus.
