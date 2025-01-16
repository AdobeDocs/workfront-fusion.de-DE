---
content-type: reference
title: Vorlagen genehmigen oder ablehnen
description: In diesem Artikel wird beschrieben, wie Sie Fusion-Vorlagen genehmigen oder ablehnen.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: dafecd8b-96e5-46da-9ab6-15f0bc9b52a4
source-git-commit: 23e9f383b25c7b3789c413e557b94418e48a636b
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 1%

---

# Vorlagen für die Registerkarte „Öffentlich“ genehmigen oder nicht genehmigen

Adobe Workfront Fusion-Vorlagen sind vorgefertigte Szenarien zur Automatisierung und Optimierung verschiedener Workflows. Diese Vorlagen können Benutzenden dabei helfen, schnell Integrationen und Automatisierungen einzurichten, ohne alles von Grund auf neu erstellen zu müssen.

Als Admin können Sie festlegen, ob bestimmte Vorlagen für die gesamte Organisation auf der Registerkarte Öffentliche Vorlagen freigegeben werden sollen.

Benutzer können von ihnen erstellte Vorlagen zur Genehmigung senden, die auf der Seite „Öffentliche Vorlagen“ freigegeben werden. <!--do the have to be requested or can an admin just choose to approve?-->

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] Plan</td>
      <td><p>Beliebig</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">[!DNL Adobe Workfront] Lizenz</td>
      <td><p>Neu: [!UICONTROL Standard]</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td>
      <td>
        <p>Aktuell: Keine [!DNL Workfront Fusion].</p>
        <p>Oder</p>
        <p>Legacy: Beliebig</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Produkt</td>
      <td>
        <p>Neu:</p>
        <ul>
          <li>[!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Workfront] Plan: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</li>
          <li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] ist enthalten.</li>
        </ul>
        <p>Oder</p>
        <p>Aktuell: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->

+++

## [!DNL Workfront Fusion] genehmigen oder ablehnen

Wenn Sie eine Vorlage validieren, wird sie auf der Registerkarte [!UICONTROL Public templates] angezeigt und steht allen Benutzern zur Verfügung.

Wenn Sie eine Vorlage ablehnen, wird sie aus der Registerkarte [!UICONTROL Public templates] entfernt und nur für das Team verfügbar gemacht, das sie erstellt hat.

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Administration]** , um den [!UICONTROL Administration] zu öffnen.
1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Templates]** .
1. Wenn Sie eine Vorlage genehmigen möchten, klicken Sie auf **[!UICONTROL Approve]** rechts neben der Vorlage.
1. Wenn Sie eine Vorlage nicht genehmigen möchten, klicken Sie auf **[!UICONTROL Disapprove]** rechts neben der Vorlage.

>[!NOTE]
>
>Wenn Sie die zuvor genehmigte und dann bearbeitete Vorlage genehmigen, überschreibt Ihre zweite Genehmigung die ursprüngliche Vorlage.


## Vorlagenstatus

Sie können den Status auf der Vorlagenseite unter dem Vorlagennamen überprüfen.

Die folgenden Status sind verfügbar:

* **[!UICONTROL Private]**: Diese Vorlage ist nur für den Vorlagenautor und sein Team sichtbar.
* **[!UICONTROL Published]**: Diese Vorlage ist nur für den Vorlagenautor und sein Team sichtbar. Nach der Veröffentlichung können Sie die Vorlage bei Bedarf zur Genehmigung senden. Sie können auch einen freigabefähigen Link kopieren.
* **[!UICONTROL Approved]**: Diese Vorlage ist für alle Workfront Fusion-Benutzenden auf der Registerkarte [!UICONTROL Public templates] sichtbar. Sie können einen freigabefähigen Link auch kopieren, indem Sie in der oberen rechten Ecke des Bildschirms auf [!UICONTROL Options] klicken.

Sie können den Status auch über die Registerkarte [!UICONTROL Team templates] überprüfen. Wenn eine Vorlage veröffentlicht wird, wird rechts neben dem Vorlagennamen ein Symbol angezeigt.

* **Augensymbol**: Die Vorlage wird veröffentlicht, ist nur für das Team sichtbar und es wurde keine Genehmigungsanfrage gesendet.
* **Gelbes Häkchensymbol**: Die Vorlage wird veröffentlicht, ist nur für das Team sichtbar und wartet auf Genehmigung, um zur Registerkarte Öffentliche Vorlagen hinzugefügt zu werden.
* **Grünes Häkchensymbol**: Die Vorlage ist auf der Registerkarte Öffentliche Vorlagen verfügbar und für jeden Workfront Fusion-Benutzer sichtbar. Er wird auch weiterhin auf der Registerkarte [!UICONTROL Team templates] angezeigt. Der Vorlagenautor oder sein Teammitglied kann sie weiterhin bearbeiten.

Vorlagen ohne Symbole haben [!UICONTROL Private] Status. Sie werden nicht veröffentlicht und sind nur für das Team sichtbar.


<!--

## Questions about how this works

Editing

1. If an admin edits a template, do they have to publish again? ... Do they have to approve again?
1. What does publishing actually do?
1. Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
1. What is the admin approving? Does a user have to submit it for approval? 



What does "Publishing" mean?
What does "Approving" mean?
If an admin edits a template, do they have to publish again? ... Do they have to approve again?
Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
What is the admin approving? Does a user have to submit it for approval?

-->
