---
content-type: reference
title: Vorlagen bearbeiten
description: In diesem Artikel wird beschrieben, wie Sie Fusion-Vorlagen bearbeiten.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 473dba8b-faa4-432f-9357-c2146e86b261
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '766'
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
      <td role="rowheader">Adobe Workfront-Plan</td>
      <td><p>Beliebig</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">Adobe Workfront-Lizenz</td>
      <td><p>Neu: Standard</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p></td>
    </tr>
    <tr>
      <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td>
      <td>
        <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
        <p>Oder</p>
        <p>Legacy: Beliebig</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Produkt</td>
      <td>
        <p>Neu:</p>
        <ul>
          <li>[!UICONTROL Select] oder [!UICONTROL Prime] Workfront-Plan: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li>
          <li>[!UICONTROL Ultimate] Workfront-Plan: Workfront Fusion ist enthalten.</li>
        </ul>
        <p>Oder</p>
        <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md). -->

+++

## Bearbeiten von Workfront Fusion-Vorlagen als Admin

1. Klicken Sie **[!UICONTROL linken]** auf „Administration“, um den Bereich [!UICONTROL Administration] zu öffnen.
1. Klicken Sie **[!UICONTROL linken Navigationsbereich auf]** Alle Vorlagen“.
1. Klicken **[!UICONTROL rechts neben]** Vorlage, die Sie bearbeiten möchten, auf „Detail“.
1. (Optional) Benennen Sie die Vorlage um, indem Sie **Optionen** in der oberen rechten Ecke klicken und **Umbenennen** auswählen.
1. (Optional) Um die Sprache Ihrer Vorlage zu ändern, klicken Sie auf **[!UICONTROL Neue Vorlage erstellen]** ![Symbol Szenarioeinstellungen](assets/fusion-scenario-settings-icon.png) und wählen Sie die Sprache aus der Dropdown-Liste Sprache aus.

   >[!IMPORTANT]
   >
   >Die Sprachauswahl entspricht den in den Systemeinstellungen verfügbaren Sprachen und betrifft nur den Namen der öffentlichen Vorlage und deren Beschreibung. Sie können eine Vorlagensprache nicht mehr ändern, nachdem die Vorlage gespeichert wurde.

1. (Optional) Um die Vorlagenbeschreibung zu bearbeiten, klicken Sie auf **[!UICONTROL Vorlage einrichten]** ![Symbol „Szenarioeinstellungen“](assets/fusion-scenario-settings-icon.png) und geben Sie die Beschreibung ein.
1. Fügen Sie Apps, Module und Tools auf die gleiche Weise hinzu oder bearbeiten Sie sie wie beim Erstellen eines Standardszenarios.

   Informationen zum Hinzufügen von kontextueller Hilfe zu den Modulen finden Sie unter [Einrichten [!UICONTROL Assistent]-Funktionalität](#set-up-wizard-functionality) in diesem Artikel.

   <!--For more information on building a scenario, see [Create a scenario in Adobe Workfront Fusion](../../../workfront-fusion/scenarios/create-a-scenario.md).-->

   >[!NOTE]
   >
   >Wenn Ihre Vorlage Module enthält, für die das Hinzufügen der Verbindung, der Anmeldeinformationen oder anderer vertraulicher Informationen zum Datenschutz erforderlich ist, werden diese Informationen nicht für die Vorlagenbenutzer freigegeben.

1. (Optional) Klicken Sie auf **[!UICONTROL Einmal ausführen]** um die Vorlage zu testen.
1. Klicken Sie auf **[!UICONTROL Speichern]**-Symbol ![Speichern](assets/save-icon.png).


## Einrichten der [!UICONTROL Wizard]-Funktion

Mit [!DNL Workfront Fusion template] [!UICONTROL Assistent] können Sie zukünftigen Benutzern Ihrer Vorlage Anweisungen oder Informationen zu den spezifischen Feldern bereitstellen, die in -Modulen verwendet werden.

1. Klicken Sie auf das Modul, das der Vorlage hinzugefügt wurde, um die Felder des Moduls anzuzeigen.
1. Suchen Sie das Feld, in dem Sie [!UICONTROL Wizard]-Informationen hinzufügen möchten, und aktivieren Sie **[!UICONTROL Verwenden im Assistenten]** unterhalb dieses Felds.
1. Geben Sie die Informationen, die für die Benutzer sichtbar sein sollen, in das Feld [!UICONTROL Hilfe] ein.
1. (Optional) Damit Benutzer diesen Text bei Verwendung der Vorlage sehen können, aktivieren Sie **[!UICONTROL Als Standardwert verwenden]**.
1. Wiederholen Sie die Schritte 2-4 für jedes Feld, für das Sie Informationen bereitstellen möchten.
1. Klicken Sie auf **[!UICONTROL OK]**, um die Änderungen zu speichern und das Modul zu schließen.

Der Veröffentlichungsprozess ist derselbe wie bei einem Standardbenutzer. Weitere Informationen finden Sie [ Abschnitt ](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md)Veröffentlichen und Freigeben von Vorlagen“.

## Vorlagenstatus

Sie können den Status auf der Vorlagenseite unter dem Vorlagennamen überprüfen.

Die folgenden Status sind verfügbar:

* **[!UICONTROL Privat]**: Diese Vorlage ist nur für den Vorlagenautor und dessen Team sichtbar.
* **[!UICONTROL Veröffentlicht]**: Diese Vorlage ist nur für den Vorlagenautor und dessen Team sichtbar. Nach der Veröffentlichung können Sie die Vorlage bei Bedarf zur Genehmigung senden. Sie können auch einen freigabefähigen Link kopieren.
* **[!UICONTROL Genehmigt]**: Diese Vorlage ist für alle Workfront Fusion-Benutzenden auf der Registerkarte [!UICONTROL Öffentliche Vorlagen] sichtbar. Sie können einen freigabefähigen Link auch kopieren, indem [!UICONTROL Optionen] in der oberen rechten Ecke des Bildschirms klicken.

Sie können den Status auch über die Registerkarte [!UICONTROL Teamvorlagen] überprüfen. Wenn eine Vorlage veröffentlicht wird, wird rechts neben dem Vorlagennamen ein Symbol angezeigt.

* **Augensymbol**: Die Vorlage wird veröffentlicht. Sie ist für das Team sichtbar.
* **Gelbes Häkchensymbol**: Die Vorlage wird veröffentlicht, ist nur für das Team sichtbar und wartet auf Genehmigung, um zur Registerkarte Öffentliche Vorlagen hinzugefügt zu werden.
* **Grünes Häkchensymbol**: Die Vorlage ist auf der Registerkarte Öffentliche Vorlagen verfügbar und für jeden Workfront Fusion-Benutzer sichtbar. Sie ist weiterhin auf der Registerkarte [!UICONTROL Teamvorlagen] sichtbar. Der Vorlagenautor oder sein Teammitglied kann sie weiterhin bearbeiten.

Vorlagen ohne Symbole haben den [!UICONTROL Privat]. Sie werden nicht veröffentlicht und sind nur für das Team sichtbar.

## Suchen der SVG-Informationen einer Vorlage

1. Klicken Sie **[!UICONTROL linken]** auf „Administration“, um den Bereich [!UICONTROL Administration] zu öffnen.
1. Klicken **[!UICONTROL im linken]** auf „Vorlagen“.
1. Klicken Sie auf die Vorlage, für die Sie Informationen suchen möchten.
1. Klicken **oben** auf „Optionen“.
1. *SVG-Diagramm auswählen*.

Hier können Sie das SVG-Diagramm und den SVG-Code anzeigen.
