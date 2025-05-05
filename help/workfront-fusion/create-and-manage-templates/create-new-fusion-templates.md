---
title: Erstellen neuer Vorlagen
description: Sie können neue Szenariovorlagen in  [!DNL Adobe] Workfront Fusion erstellen.
author: Becky
feature: Workfront Fusion
exl-id: 9cb9bd04-e9ae-4162-a1b9-d71566582b7a
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Erstellen neuer Vorlagen

Sie können in [!DNL Adobe] Workfront Fusion neue Szenariovorlagen erstellen.

>[!TIP]
>
>Bevor Sie eine neue Vorlage erstellen, können Sie die Registerkarte [!UICONTROL Public templates] überprüfen, um sicherzustellen, dass die Vorlage, die Sie erstellen möchten, nicht bereits verfügbar ist.

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
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Erstellen einer neuen Vorlage

Sie können eine Vorlage in einem Prozess erstellen, der dem Erstellen eines Szenarios ähnelt. Fusion-Administratoren können auch Vorlagen aus vorhandenen Szenarien erstellen.

* [Erstellen einer Vorlage](#build-a-template)
* [Erstellen einer Vorlage aus einem Szenario](#create-a-template-from-a-scenario)

### Erstellen einer Vorlage

1. Klicken Sie **[!UICONTROL Templates]** linken ![&#128279;](assets/templates-icon.png) auf Vorlagensymbol).
1. Klicken Sie oben rechts auf **[!UICONTROL Create a new template]** .
1. (Optional) Benennen Sie die Vorlage um, indem Sie die **[!UICONTROL New template name]** in der oberen linken Ecke ersetzen.
1. (Optional) Um die Sprache Ihrer Vorlage zu ändern, klicken Sie auf **[!UICONTROL Set up a template]** ![Symbol Szenarioeinstellungen](assets/scenario-settings-icon.png) und wählen Sie die Sprache aus der Dropdown-Liste Sprache aus.

   >[!IMPORTANT]
   >
   >Die Sprachauswahl entspricht den in den Systemeinstellungen verfügbaren Sprachen und betrifft nur den Namen der öffentlichen Vorlage und deren Beschreibung. Sie können eine Vorlagensprache nicht mehr ändern, nachdem die Vorlage gespeichert wurde.

1. (Optional) Um eine Beschreibung der Vorlage einzugeben, klicken Sie auf **[!UICONTROL Set up a template]** ![Symbol Szenario-Einstellungen](assets/scenario-settings-icon.png) und geben Sie die Beschreibung ein.
1. Fügen Sie Apps, Module und Tools hinzu, wobei dieselben Prozesse verwendet werden wie beim Hinzufügen von Modulen zu einem Szenario.

   Anweisungen finden Sie in den Artikeln unter [Module hinzufügen](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Informationen zum Hinzufügen von kontextueller Hilfe zu den Modulen finden Sie unter [Einrichten von Assistenten](#set-up-wizard-functionality) in diesem Artikel.

   Weitere Informationen zum Erstellen eines Szenarios finden Sie unter [Workflow zum Erstellen eines Szenarios](/help/workfront-fusion/create-scenarios/plan-a-scenario/create-a-scenario-workflow.md).

   >[!NOTE]
   >
   >Wenn Ihre Vorlage Module enthält, für die das Hinzufügen der Verbindung, der Anmeldeinformationen oder anderer vertraulicher Informationen zum Datenschutz erforderlich ist, werden diese Informationen nicht für die Vorlagenbenutzer freigegeben.

1. (Optional) Klicken Sie auf **[!UICONTROL Run once]** , um Ihre Vorlage zu testen.
1. Klicken Sie auf das **[!UICONTROL Save]**-Symbol ![Speichersymbol](assets/save-icon.png), um die Vorlage zu speichern.

Wenn Sie Ihre Vorlage speichern, wird sie für Ihre Team-Mitglieder sichtbar. Wenn Sie möchten, dass Ihre Vorlage außerhalb Ihres Teams zugänglich ist, müssen Sie eine Anfrage einreichen, um sie genehmigen und veröffentlichen zu lassen. Die Anfrage wird zur Genehmigung an das Adobe Workfront Fusion-Team gesendet. Nach der Genehmigung ist die Vorlage für andere Benutzer außerhalb Ihres Teams zugänglich.

Informationen zum Veröffentlichen von Vorlagen finden Sie unter [Publish und Freigabe [!DNL Adobe Workfront Fusion] Vorlagen](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md).

### Erstellen einer Vorlage aus einem Szenario

>[!NOTE]
>
>Sie müssen ein Fusion-Administrator sein, um eine Vorlage aus einem Szenario erstellen zu können.

1. Klicken Sie im linken Bedienfeld auf die Registerkarte **[!UICONTROL Scenarios]** .
1. Wählen Sie das Szenario aus, aus dem Sie eine Vorlage erstellen möchten.
1. Klicken Sie auf **Admin**-Dropdown in der oberen rechten Ecke der Seite.
1. Wählen Sie **Als Vorlage klonen** aus.

   Das Szenario wird in eine neue Vorlagenseite kopiert.
1. (Optional) Benennen Sie die Vorlage um, indem Sie die **[!UICONTROL New template name]** in der oberen linken Ecke ersetzen.
1. (Optional) Um die Sprache Ihrer Vorlage zu ändern, klicken Sie auf **[!UICONTROL Set up a template]** ![Symbol Szenarioeinstellungen](assets/scenario-settings-icon.png) und wählen Sie die Sprache aus der Dropdown-Liste Sprache aus.

   >[!IMPORTANT]
   >
   >Die Sprachauswahl entspricht den in den Systemeinstellungen verfügbaren Sprachen und betrifft nur den Namen der öffentlichen Vorlage und deren Beschreibung. Sie können eine Vorlagensprache nicht mehr ändern, nachdem die Vorlage gespeichert wurde.

1. (Optional) Um eine Beschreibung der Vorlage einzugeben, klicken Sie auf **[!UICONTROL Set up a template]** ![Symbol Szenario-Einstellungen](assets/scenario-settings-icon.png) und geben Sie die Beschreibung ein.
1. Bearbeiten Sie Apps, Module und Tools nach Bedarf, indem Sie dieselben Prozesse verwenden wie beim Hinzufügen von Modulen zu einem Szenario.

   Anweisungen finden Sie in den Artikeln unter [Module hinzufügen](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Informationen zum Hinzufügen von kontextueller Hilfe zu den Modulen finden Sie unter [Einrichten [!UICONTROL Wizard] Funktionen](#set-up-wizard-functionality) in diesem Artikel.

   >[!NOTE]
   >
   >Wenn Ihre Vorlage Module enthält, für die das Hinzufügen der Verbindung, der Anmeldeinformationen oder anderer vertraulicher Informationen zum Datenschutz erforderlich ist, werden diese Informationen nicht für die Vorlagenbenutzer freigegeben.

1. (Optional) Klicken Sie auf **[!UICONTROL Run once]** , um Ihre Vorlage zu testen.
1. Klicken Sie auf das **[!UICONTROL Save]**-Symbol ![Speichersymbol](assets/save-icon.png).

## Einrichten [!UICONTROL Wizard] Funktionen {#set-up-wizard-functionality}

Mit der [!DNL Workfront Fusion template] [!UICONTROL Wizard] können Sie zukünftigen Benutzern Ihrer Vorlage Anweisungen oder Informationen zu den spezifischen Feldern bereitstellen, die in -Modulen verwendet werden.

1. Klicken Sie beim Erstellen einer Vorlage auf ein Modul, das der Vorlage hinzugefügt wurde, um die Felder des Moduls anzuzeigen.
1. Suchen Sie das Feld, in dem Sie [!UICONTROL Wizard] Informationen hinzufügen möchten, und aktivieren Sie **[!UICONTROL Use in Wizard]** für dieses Feld.
1. Geben Sie die Informationen, die für die Benutzer sichtbar sein sollen, in das Feld [!UICONTROL Help] ein.
1. (Optional) Damit Benutzer diesen Text bei Verwendung der Vorlage sehen können, aktivieren Sie **[!UICONTROL Use as default value]**.
1. Wiederholen Sie die Schritte 2-4 für jedes Feld, für das Sie Informationen bereitstellen möchten.
1. Klicken Sie auf **[!UICONTROL OK]** , um die Änderungen zu speichern und das Modul zu schließen.
