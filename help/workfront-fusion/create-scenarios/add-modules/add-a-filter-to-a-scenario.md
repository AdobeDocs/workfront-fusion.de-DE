---
title: Hinzufügen eines Filters zu einem Szenario
description: In einigen Szenarien müssen Sie nur mit Bundles arbeiten, die bestimmte Kriterien erfüllen. Mit Filtern können Sie diese Bundles auswählen.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
TQID: 'https://experienceleague.adobe.com/YMoeIdlzd7omGJoEFHUPTYl3eKayIp0LfbqkohVEXjs'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 11%
---
# Hinzufügen eines Filters zu einem Szenario

In einigen Szenarien müssen Sie nur mit Bundles arbeiten, die bestimmte Kriterien erfüllen. Mit Filtern können Sie diese Bundles auswählen.

Sie können beispielsweise ein Szenario mit dem Trigger [!UICONTROL Datensätze überwachen] für Workfront erstellen, um nur Aufgaben zu erfassen, die einem bestimmten Benutzer zugewiesen sind.

Sie können einen Filter zwischen zwei Modulen hinzufügen und überprüfen, ob die von den vorherigen Modulen empfangenen Pakete bestimmte Filterbedingungen erfüllen:

* Wenn dies der Fall ist, werden die Bundles an das nächste Modul im Szenario weitergegeben.
* Ist dies nicht der Fall, wird die Verarbeitung für die Bundles beendet.

>[!NOTE]
>
>Workfront Fusion stellt den Szenario-Editor auf ein neues Erlebnis um. Während dieser Umstellung sind sowohl die klassischen als auch die neuen Erlebnisse verfügbar und Sie können jederzeit zwischen ihnen wechseln. Es wird empfohlen, die neue -Version zu verwenden. Weitere Informationen finden Sie unter [Neue und klassische Erlebnisse](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) im Artikel Szenario-Editor.

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
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Voraussetzungen

Sie müssen beide Module zu einem Szenario hinzufügen, bevor Sie einen Filter zwischen ihnen hinzufügen können.

## Hinzufügen eines Filters zwischen zwei Modulen

* [Hinzufügen eines Filters zwischen zwei Modulen in der neuen -Version (empfohlen)](#add-a-filter-between-two-modules-in-the-new-experience-recommended)
* [Hinzufügen eines Filters zwischen zwei Modulen im klassischen Erlebnis](#add-a-filter-between-two-modules-in-the-classic-experience)

### Hinzufügen eines Filters zwischen zwei Modulen in der neuen -Version (empfohlen)

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Filter hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie mit der linken Maustaste auf den Pfad zwischen den Modulen, denen Sie einen Filter hinzufügen möchten.

   Das **[!UICONTROL Filter einrichten]** wird direkt geöffnet. (Durch Klicken mit der rechten Maustaste auf den Pfad wird stattdessen ein anderes Menü geöffnet.)

1. Geben Sie im angezeigten Feld einen **[!UICONTROL Titel]** für den Filter ein.
1. Definieren Sie den Filter **[!UICONTROL Bedingung]**.

   Geben Sie im ersten Feld das Feld ein, nach dem Sie filtern möchten, den Operator und (bei Bedarf) den Wert, mit dem Sie das Feld vergleichen möchten.

   >[!TIP]
   >
   >Sie können Werte über das Zuordnungsbedienfeld in Filterfelder eingeben
   >Weitere Informationen zur Zuordnung finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   Wenn der Filter beispielsweise Dateien in Adobe Workfront übergeben soll, die mit XML enden, geben Sie **[!UICONTROL Dateiname]** in das erste Feld und .**[!UICONTROL xml]** in das zweite Feld ein. Im Dropdown-Menü zwischen ihnen wählen Sie **[!UICONTROL Endet mit (Groß-/Kleinschreibung wird nicht beachtet)]**. Dieser Filter würde für eingehende Bundles des ersten Moduls (Workfront) gelten. Nur Bundles mit XML-Dateien würden an das nächste Modul weitergegeben.

   ![Filter einrichten](assets/new-filter-setup-xml-example.png)

1. Klicken Sie auf **[!DNL OK]**.

### Hinzufügen eines Filters zwischen zwei Modulen im klassischen Erlebnis

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Filter hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf das Schraubenschlüsselsymbol ![Schraubenschlüsselsymbol](assets/wrench-icon.png) zwischen den Modulen, in denen Sie einen Filter hinzufügen möchten, und wählen Sie **Filter einrichten** aus.
1. Geben Sie im angezeigten Feld einen **[!UICONTROL Titel]** für den Filter ein.
1. Definieren Sie den Filter **[!UICONTROL Bedingung]**.

   Geben Sie im ersten Feld das Feld ein, nach dem Sie filtern möchten, den Operator und (bei Bedarf) den Wert, mit dem Sie das Feld vergleichen möchten.

   >[!TIP]
   >
   >Sie können Werte über das Zuordnungsbedienfeld in Filterfelder eingeben
   >Weitere Informationen zur Zuordnung finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   Wenn der Filter beispielsweise Dateien in Adobe Workfront übergeben soll, die mit XML enden, geben Sie **[!UICONTROL Dateiname]** in das erste Feld und .**[!UICONTROL xml]** in das zweite Feld ein. Im Dropdown-Menü zwischen ihnen wählen Sie **[!UICONTROL Endet mit (Groß-/Kleinschreibung wird nicht beachtet)]**. Dieser Filter würde für eingehende Bundles des ersten Moduls (Workfront) gelten. Nur Bundles mit XML-Dateien würden an das nächste Modul weitergegeben.

   ![Filter einrichten](assets/set-up-filter-box.png)

1. Klicken Sie auf **[!DNL OK]**.

## Kopieren von Filtern

Sie können einen vorhandenen Filter kopieren und an einer anderen Stelle im Szenario einfügen.

* [Kopieren eines Filters in die neue -Version (empfohlen)](#copy-a-filter-in-the-new-experience-recommended)
* [Kopieren eines Filters in der klassischen Benutzeroberfläche](#copy-a-filter-in-the-classic-experience)

### Kopieren eines Filters in die neue -Version (empfohlen)

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Filter hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie mit der rechten Maustaste auf den Pfad zwischen den Modulen, in denen sich der Filter befindet.
1. Wählen Sie **Filter kopieren** aus.
1. Klicken Sie mit der rechten Maustaste auf den Pfad zwischen den Modulen, in die Sie den Filter einfügen möchten.
1. Wählen Sie **Filter einfügen** aus.
1. (Optional) Um den Filter anzupassen, klicken Sie auf das Filtersymbol oder die Kennzeichnung und geben Sie Werte ein, wie in [Hinzufügen eines Filters zwischen zwei Modulen in der neuen -Version](#add-a-filter-between-two-modules-in-the-new-experience-recommended) in diesem Artikel beschrieben.

### Kopieren eines Filters in der klassischen Benutzeroberfläche

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Filter hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie mit der rechten Maustaste auf die Verbindungspunkte zwischen den Modulen, in denen sich der Filter befindet.
1. Wählen Sie **Filter kopieren** aus.
1. Klicken Sie mit der rechten Maustaste auf die Verbindungspunkte zwischen Modulen, in die Sie den Filter einfügen möchten.
1. Filter **Einfügen** auswählen
1. (Optional) Um den Filter anzupassen, klicken Sie auf das Filtersymbol oder die Kennzeichnung und geben Sie Werte ein, wie in [Hinzufügen eines Filters zwischen zwei Modulen im klassischen Erlebnis](#add-a-filter-between-two-modules-in-the-classic-experience) in diesem Artikel beschrieben.




<!--

Currently, the scenario editor does include a feature for copying a filter.

>[!NOTE]
>
>If you copy the modules on either side of the filter, the filter is also copied.
>
>For more information on copying modules, see [Copy modules or scenarios in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

To copy a filter without copying modules, you can use the Fusion DevTool

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a filter.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Open the Fusion DevTool by clicking on the DevTool icon ![DevTool icon](assets/debugger-icon.png) near the bottom of the screen.
   
   If you do not see the DevTool icon, see [Debug a scenario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) for instructions on opening the DevTool.
   
1. Click the **[!UICONTROL Tools]** icon ![DevTool tools](assets/devtools-tools-icon.png) in the left side bar.

1. Click **[!UICONTROL Copy Filter]**, then configure the **[!UICONTROL Copy Filter]** tool in the right side panel:

   1. Set the **[!UICONTROL Source Module]** as the module directly after the filter you want to copy.
   1. Set the **[!UICONTROL Target Module]** as the module that you want to place the filter directly after.

1. Click **[!UICONTROL Run]**.

-->
