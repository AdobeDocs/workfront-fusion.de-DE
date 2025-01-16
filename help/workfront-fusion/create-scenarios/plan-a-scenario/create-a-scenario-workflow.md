---
title: Workflow zum Erstellen eines Szenarios
description: Diesem allgemeinen Workflow folgen, um ein Szenario zu erstellen
author: Becky
feature: Workfront Fusion
exl-id: 49f8edd7-e29a-4ead-9134-a9f0d1cc244d
source-git-commit: f190217891c1d583e49cacb820e2076b995f6a3d
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Workflow zum Erstellen eines Szenarios

Szenarien werden entsprechend den Anforderungen Ihres Unternehmens erstellt, mit Programmen und Modulen, die auf Ihre Anwendungsfälle zugeschnitten sind. Das Erstellen eines Szenarios folgt jedoch unabhängig vom Anwendungsfall demselben grundlegenden Workflow. In diesem Artikel wird der grundlegende Prozess der Erstellung eines Szenarios beschrieben.


* [Szenario erstellen und benennen](#create-and-name-the-scenario)
* [Hinzufügen und Konfigurieren des ersten Moduls](#configure-the-first-module)
* [Erstellen von Verbindungen](#create-connections)
* [Hinzufügen und Konfigurieren zusätzlicher Module](#add-and-configure-additional-modules)
* [Zuordnen von Daten zwischen Modulen](#map-data-between-modules)
* [Routing konfigurieren](#configure-routing)
* [Konfigurieren der Fehlerbehandlung](#configure-error-handling)
* [Szenarioeinstellungen konfigurieren](#onfigure-scenario-settings)
* [Testen und Überarbeiten](#test-and-revise)
* [Aktivieren des Szenarios](#activate-the-scenario)

Tastaturbefehle



## Szenario erstellen und benennen

1. Melden Sie sich bei Ihrem [!DNL Workfront Fusion] Konto an.
1. Klicken Sie im linken Bedienfeld auf **[!UICONTROL Scenarios]** ![](assets/scenarios-icon.png) .

   >[!NOTE]
   >
   >Wenn der linke Navigationsbereich oder dessen Symbole nicht angezeigt werden, klicken Sie auf das Symbol Menü ![Menü](assets/main-menu-icon-left-nav.png) .

1. (Optional) Klicken Sie im [!UICONTROL **Ordner**]-Bedienfeld auf das **[!UICONTROL Add folder]**-Symbol ![](assets/add-folder-icon.png) geben Sie dann einen Namen wie „Übungsszenarien“ für Ihren ersten Ordner ein.

1. (Optional) Öffnen Sie den Ordner und klicken Sie dann oben rechts auf der Seite auf **[!UICONTROL Create a new scenario]** .

1. Wählen Sie oben links den **[!UICONTROL New scenario]** Platzhalternamen aus und geben Sie dann einen Namen wie „Übungsszenario 1“ ein.

   ![](assets/name-the-scenario.png)

1. Fahren Sie mit [Verbinden des ersten Moduls](#2-connect-the-first-module) unten fort.

## Hinzufügen und Konfigurieren des ersten Moduls

Das erste Modul für Ihr Szenario ist ein Trigger-Modul, das das Szenario startet, wenn bestimmte Bedingungen erfüllt sind.

Anweisungen zum Hinzufügen des ersten Moduls zu einem Szenario finden Sie unter [Hinzufügen des ersten Moduls zu einem Szenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-basic.md#add-the-first-module-to-a-scenario) im Artikel Hinzufügen eines Moduls zu einem Szenario.

Anweisungen zum Konfigurieren eines Moduls finden Sie unter [Konfigurieren eines Moduls](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)

## Erstellen von Verbindungen

Beim Konfigurieren eines Moduls müssen Sie eine Verbindung eingeben oder erstellen. Das Modul verwendet diese Verbindung und die darin enthaltenen Berechtigungen für den Zugriff auf das Datum in der Anwendung.

Grundlegende Anweisungen zum Erstellen einer Verbindung finden Sie unter [Verbindung erstellen - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

Spezifische Anwendungsfälle, die Google, Microsoft oder Programme ohne dedizierte Connectoren betreffen, finden Sie in den anderen Artikeln unter [Mit Programmen verbinden: Artikelindex](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-apps-toc.md).

## Hinzufügen und Konfigurieren zusätzlicher Module

Fahren Sie mit dem Hinzufügen und Konfigurieren zusätzlicher Module fort.

Anweisungen zum Hinzufügen von Modulen finden Sie in den Artikeln, die unter [Module hinzufügen: Artikelindex](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md) aufgeführt sind.

## Zuordnen von Daten zwischen Modulen

Sie können die Ausgabe aus vorherigen Modulen als Eingabe in nachfolgenden Modulen verwenden. Sie können beispielsweise ein Workfront-Projekt in einem Modul erstellen und ein Dokument in dieses Modul in einem nachfolgenden Modul hochladen.

Anweisungen finden Sie in den Artikeln unter [Zuordnungsdaten: Artikelindex](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md).

## Routing konfigurieren

Das Routing ermöglicht es dem Szenario, basierend auf Datenwerten verschiedene Aktionen auszuführen.

Anweisungen finden Sie unter [Router-Modul hinzufügen und Routen konfigurieren](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Konfigurieren der Fehlerbehandlung

Durch die Fehlerbehandlung kann das Szenario von Fehlern wiederhergestellt werden. Sie können auswählen, wie das Szenario in verschiedenen Fehlersituationen reagieren soll.

Anweisungen finden Sie unter [Fehlerbehandlung hinzufügen](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md).

## Szenarioeinstellungen konfigurieren

Sie können Einstellungen für Ihr gesamtes Szenario konfigurieren, z. B. das Planen eines Szenarios, das Erstellen von Notizen oder das Bestimmen, wie Daten gespeichert werden.

Anweisungen finden Sie in den Artikeln unter [Szenarioeinstellungen konfigurieren: Artikelindex](/help/workfront-fusion/create-scenarios/config-scenarios-settings/config-scenario-settings-toc.md).

## Testen und Überarbeiten

Durch das Testen Ihres Szenarios können Sie feststellen, ob Ihr Szenario wie beabsichtigt funktioniert. Anschließend können Sie das Szenario auf der Grundlage Ihrer Ergebnisse überarbeiten und dann erneut testen.

1. Klicken Sie in der linken unteren Ecke des Szenario-Editors auf **[!UICONTROL Run once]** .
1. Klicken Sie nach Abschluss der Ausführung des Szenarios auf die Blase „Execution Inspector“ über jedem Modul, um die Eingabe von Informationen und die Ausgabe dieses Moduls anzuzeigen.

   * Allgemeine Informationen zum Lesen von Informationen zur Szenarioausführung finden Sie unter [Szenarioausführungsfluss](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Informationen zu verarbeiteten Bundles finden Sie unter [Szenarioausführung, Zyklen und Phasen in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. Klicken Sie [!DNL Workfront Fusion] auf **[!UICONTROL Save]** ![](assets/save-icon.png) in der linken unteren Ecke, um den Fortschritt des Szenarios zu speichern.

   >[!IMPORTANT]
   >
   >Speichern Sie häufig, während Sie ein Szenario verfeinern und testen.

## Aktivieren des Szenarios

Dieses Beispielszenario hat kein Trigger-Modul. Wenn dies ein Szenario wäre, das Sie für echte Daten verwenden würden, würde es mit einem Trigger-Modul beginnen, und das letzte, was Sie tun würden, wäre, es zu aktivieren. Nachdem Sie ein Szenario aktiviert haben, wird es standardmäßig alle 15 Minuten ausgeführt. Sie können dies ändern, indem Sie festlegen, wann und wie oft die Ausführung erfolgen soll.

Weitere Informationen zum Aktivieren von Szenarien finden Sie unter [Aktivieren oder Deaktivieren eines Szenarios](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).

Weitere Informationen zu Zeitplänen finden Sie unter [Planen eines Szenarios](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Tastaturbefehle für das Workfront Fusion-Szenario

Beim Erstellen oder Bearbeiten eines Szenarios können die folgenden Tastaturbefehle verwendet werden:

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <thead> 
  <tr> 
   <th> <p>Aktion</p> </th> 
   <th>[!DNL Windows]</th> 
   <th> <p>[!DNL MacOS]</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save] </td> 
   <td>Strg+Umschalt+S</td> 
   <td><span style="font-weight: normal;">Befehl+Umschalt+S</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Run Once]</td> 
   <td>Strg+Umschalt+Eingabe</td> 
   <td><span style="font-weight: normal;">Befehl+Umschalt+Eingabe</span> </td> 
  </tr> 
 </tbody> 
</table>



