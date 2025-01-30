---
content-type: reference
title: Vorlagen bearbeiten
description: In diesem Artikel wird beschrieben, wie Sie Fusion-Vorlagen bearbeiten.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 473dba8b-faa4-432f-9357-c2146e86b261
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---

# Vorlagen bearbeiten

Adobe Workfront Fusion-Vorlagen sind vorgefertigte Szenarien zur Automatisierung und Optimierung verschiedener Workflows. Mit diesen Vorlagen können Sie Integrationen und Automatisierungen schnell einrichten, ohne alles von Grund auf neu erstellen zu müssen.

Als Administrator sind Sie berechtigt, von anderen erstellte Vorlagen anzuzeigen, zu ändern, umzubenennen, zu veröffentlichen, zu genehmigen und zu löschen.

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

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md). -->

+++

## Bearbeiten [!DNL Workfront Fusion] Vorlagen als Admin

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Administration]** , um den [!UICONTROL Administration] zu öffnen.
1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL All Templates]** .
1. Klicken Sie rechts neben der Vorlage, die Sie bearbeiten möchten, auf **[!UICONTROL Detail]** .
1. (Optional) Benennen Sie die Vorlage um, indem Sie **Optionen** in der oberen rechten Ecke klicken und **Umbenennen** auswählen.
1. (Optional) Um die Sprache Ihrer Vorlage zu ändern, klicken Sie auf **[!UICONTROL Create a new template]** ![Symbol Szenario-Einstellungen](assets/fusion-scenario-settings-icon.png) und wählen Sie die Sprache aus der Dropdownliste Sprache aus.

   >[!IMPORTANT]
   >
   >Die Sprachauswahl entspricht den in den Systemeinstellungen verfügbaren Sprachen und betrifft nur den Namen der öffentlichen Vorlage und deren Beschreibung. Sie können eine Vorlagensprache nicht mehr ändern, nachdem die Vorlage gespeichert wurde.

1. (Optional) Um die Vorlagenbeschreibung zu bearbeiten, klicken Sie auf **[!UICONTROL Set up a template]** ![Symbol Szenario-Einstellungen](assets/fusion-scenario-settings-icon.png) und geben Sie die Beschreibung ein.
1. Fügen Sie Apps, Module und Tools auf die gleiche Weise hinzu oder bearbeiten Sie sie wie beim Erstellen eines Standardszenarios.

   Informationen zum Hinzufügen von kontextueller Hilfe zu den Modulen finden Sie unter [Einrichten [!UICONTROL Wizard] Funktionen](#set-up-wizard-functionality) in diesem Artikel.

   <!--For more information on building a scenario, see [Create a scenario in [!DNL Adobe Workfront Fusion]](../../../workfront-fusion/scenarios/create-a-scenario.md).-->

   >[!NOTE]
   >
   >Wenn Ihre Vorlage Module enthält, für die das Hinzufügen der Verbindung, der Anmeldeinformationen oder anderer vertraulicher Informationen zum Datenschutz erforderlich ist, werden diese Informationen nicht für die Vorlagenbenutzer freigegeben.

1. (Optional) Klicken Sie auf **[!UICONTROL Run once]** , um die Vorlage zu testen.
1. Klicken Sie auf das **[!UICONTROL Save]**-Symbol ![Speichersymbol](assets/save-icon.png).


## Einrichten [!UICONTROL Wizard] Funktionen

Mit der [!DNL Workfront Fusion template] [!UICONTROL Wizard] können Sie zukünftigen Benutzern Ihrer Vorlage Anweisungen oder Informationen zu den spezifischen Feldern bereitstellen, die in -Modulen verwendet werden.

1. Klicken Sie auf das Modul, das der Vorlage hinzugefügt wurde, um die Felder des Moduls anzuzeigen.
1. Suchen Sie das Feld, in dem Sie [!UICONTROL Wizard] Informationen hinzufügen möchten, und aktivieren Sie **[!UICONTROL Use in Wizard]** unter diesem Feld.
1. Geben Sie die Informationen, die für die Benutzer sichtbar sein sollen, in das Feld [!UICONTROL Help] ein.
1. (Optional) Damit Benutzer diesen Text bei Verwendung der Vorlage sehen können, aktivieren Sie **[!UICONTROL Use as default value]**.
1. Wiederholen Sie die Schritte 2-4 für jedes Feld, für das Sie Informationen bereitstellen möchten.
1. Klicken Sie auf **[!UICONTROL OK]** , um die Änderungen zu speichern und das Modul zu schließen.

Der Veröffentlichungsprozess ist derselbe wie bei einem Standardbenutzer. Weitere Informationen finden Sie im Abschnitt [Publish- und Freigabevorlagen](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md) .

## Vorlagenstatus

Sie können den Status auf der Vorlagenseite unter dem Vorlagennamen überprüfen.

Die folgenden Status sind verfügbar:

* **[!UICONTROL Private]**: Diese Vorlage ist nur für den Vorlagenautor und sein Team sichtbar.
* **[!UICONTROL Published]**: Diese Vorlage ist nur für den Vorlagenautor und sein Team sichtbar. Nach der Veröffentlichung können Sie die Vorlage bei Bedarf zur Genehmigung senden. Sie können auch einen freigabefähigen Link kopieren.
* **[!UICONTROL Approved]**: Diese Vorlage ist für alle Workfront Fusion-Benutzenden auf der Registerkarte [!UICONTROL Public templates] sichtbar. Sie können einen freigabefähigen Link auch kopieren, indem Sie in der oberen rechten Ecke des Bildschirms auf [!UICONTROL Options] klicken.

Sie können den Status auch über die Registerkarte [!UICONTROL Team templates] überprüfen. Wenn eine Vorlage veröffentlicht wird, wird rechts neben dem Vorlagennamen ein Symbol angezeigt.

* **Augensymbol**: Die Vorlage wird veröffentlicht. Sie ist für das Team sichtbar.
* **Gelbes Häkchensymbol**: Die Vorlage wird veröffentlicht, ist nur für das Team sichtbar und wartet auf Genehmigung, um zur Registerkarte Öffentliche Vorlagen hinzugefügt zu werden.
* **Grünes Häkchensymbol**: Die Vorlage ist auf der Registerkarte Öffentliche Vorlagen verfügbar und für jeden Workfront Fusion-Benutzer sichtbar. Er wird auch weiterhin auf der Registerkarte [!UICONTROL Team templates] angezeigt. Der Vorlagenautor oder sein Teammitglied kann sie weiterhin bearbeiten.

Vorlagen ohne Symbole haben [!UICONTROL Private] Status. Sie werden nicht veröffentlicht und sind nur für das Team sichtbar.

## Suchen der SVG-Informationen einer Vorlage

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Administration]** , um den [!UICONTROL Administration] zu öffnen.
1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Templates]** .
1. Klicken Sie auf die Vorlage, für die Sie Informationen suchen möchten.
1. Klicken **oben** auf „Optionen“.
1. *SVG-Diagramm*.

Hier sehen Sie das SVG-Diagramm und den SVG-Code.
