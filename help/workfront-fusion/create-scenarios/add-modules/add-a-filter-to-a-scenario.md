---
title: Hinzufügen eines Filters zu einem Szenario
description: In einigen Szenarien müssen Sie nur mit Bundles arbeiten, die bestimmte Kriterien erfüllen. Mit Filtern können Sie diese Bundles auswählen.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 1%

---

# Hinzufügen eines Filters zu einem Szenario

In einigen Szenarien müssen Sie nur mit Bundles arbeiten, die bestimmte Kriterien erfüllen. Mit Filtern können Sie diese Bundles auswählen.

Sie können beispielsweise ein Szenario mit dem Trigger [!UICONTROL Datensätze überwachen] für Workfront erstellen, um nur Aufgaben zu erfassen, die einem bestimmten Benutzer zugewiesen sind.

Sie können einen Filter zwischen zwei Modulen hinzufügen und überprüfen, ob die von den vorherigen Modulen empfangenen Pakete bestimmte Filterbedingungen erfüllen:

* Wenn dies der Fall ist, werden die Bundles an das nächste Modul im Szenario weitergegeben.
* Ist dies nicht der Fall, wird die Verarbeitung für die Bundles beendet.

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
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Sie müssen beide Module zu einem Szenario hinzufügen, bevor Sie einen Filter zwischen ihnen hinzufügen können.

## Fügen Sie einen Filter zwischen zwei Modulen hinzu:

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

   Wenn der Filter beispielsweise Dateien in Adobe Workfront übergeben soll, die mit XML enden, geben Sie **[!UICONTROL Dateinamen]** in das erste Feld ein und .**[!UICONTROL xml]** im zweiten Feld an. Im Dropdown-Menü zwischen ihnen wählen Sie **[!UICONTROL Endet mit (Groß-/Kleinschreibung wird nicht beachtet)]**. Dieser Filter würde für eingehende Bundles des ersten Moduls (Workfront) gelten. Nur Bundles mit XML-Dateien würden an das nächste Modul weitergegeben.

   ![Filter einrichten](assets/set-up-filter-box.png)

1. Klicken Sie auf **[!DNL OK]**.

## Kopieren von Filtern

Derzeit enthält der Szenario-Editor keine Funktion zum Kopieren eines Filters.

>[!NOTE]
>
>Wenn Sie die Module auf beiden Seiten des Filters kopieren, wird der Filter ebenfalls kopiert.
>
>Weitere Informationen zum Kopieren von Modulen finden Sie unter [Module oder Szenarien in Adobe Workfront Fusion kopieren](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

Um einen Filter zu kopieren, ohne Module zu kopieren, können Sie das Fusion DevTool verwenden

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Filter hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Öffnen Sie Fusion DevTool, indem Sie auf das DevTool![Symbol (DevTool](assets/debugger-icon.png) unten auf dem Bildschirm klicken.

   Wenn das DevTool-Symbol nicht angezeigt wird, finden Sie unter [Debuggen eines Szenarios](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) Anweisungen zum Öffnen des DevTools.

1. Klicken Sie auf **[!UICONTROL Tools]**-Symbol ![DevTool-](assets/devtools-tools-icon.png)) in der linken Seitenleiste.

1. Klicken Sie **[!UICONTROL Filter kopieren]** und konfigurieren Sie dann das **[!UICONTROL Filter kopieren]**-Tool im rechten Seitenbereich:

   1. Legen Sie das **[!UICONTROL Source]** Modul direkt nach dem Filter, den Sie kopieren möchten, als Modul fest.
   1. Legen Sie das **[!UICONTROL Target-Modul]** als das Modul fest, nach dem Sie den Filter direkt platzieren möchten.

1. Klicken Sie auf **[!UICONTROL Ausführen]**.
