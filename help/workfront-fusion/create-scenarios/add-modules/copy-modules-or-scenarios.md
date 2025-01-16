---
title: Module oder Szenarien kopieren
description: Sie können Module, Modulgruppen oder ganze Szenarien in Adobe Workfront Fusion kopieren. Mit dieser Funktion können Sie Szenarien oder Teile von Szenarien wiederverwenden, ohne sie erneut erstellen zu müssen.
author: Becky
feature: Workfront Fusion
exl-id: 5cece7d4-b2c7-4276-8a6f-f65bad799c7a
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---

# Module oder Szenarien kopieren

Sie können Module, Modulgruppen oder ganze Szenarien in Adobe Workfront Fusion kopieren. Mit dieser Funktion können Sie Szenarien oder Teile von Szenarien wiederverwenden, ohne sie erneut erstellen zu müssen.

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

## Voraussetzungen

Die Module müssen in einem Szenario vorhanden sein, bevor Sie sie kopieren können.

## Kopieren eines Moduls oder einer Gruppe von Modulen

Beim Kopieren eines Moduls behält die Kopie alle Feldwerte und Einstellungen des ursprünglichen Moduls bei.

Sie können das Modul oder die Module in einen anderen Bereich desselben Szenarios oder in ein anderes Szenario einfügen.

Beachten Sie beim Einfügen von Modulen in ein anderes Szenario Folgendes:

* Feldwerte, die Informationen aus einem anderen Modul abrufen, das Sie nicht kopiert haben, können nicht mehr auf diese Informationen zugreifen. Sie müssen diese Felder festlegen, um Informationen aus dem neuen Szenario abzurufen.
* Wenn Sie die Module in ein Szenario einfügen, das einem anderen Team oder einer anderen Organisation gehört, müssen alle Verbindungen zu Verbindungen aktualisiert werden, die dem Team oder der Organisation gehören, das bzw. die das neue Szenario besitzt.

### Module kopieren

Das Kopieren einer Gruppe von Modulen ähnelt dem Kopieren eines einzelnen Moduls.

1. Klicken Sie im linken Bedienfeld auf die Registerkarte **[!UICONTROL Scenarios]** .
1. Wählen Sie das Szenario aus, in das Sie ein Modul kopieren möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie mit der rechten Maustaste auf das Modul, das Sie kopieren möchten.

   >[!NOTE]
   >
   >Sie können mehrere Module auswählen, indem Sie die [!UICONTROL shift] gedrückt halten und auf die Module klicken, die Sie kopieren möchten. Beim Kopieren einer Gruppe von Modulen werden auch alle Verbindungsleitungen, Filter oder Routing-Logiken zwischen ihnen kopiert.

1. Wählen Sie **[!UICONTROL Copy module]** aus.
1. Bewegen Sie den Cursor in den Bereich des Szenarios, in dem die Kopie des Szenarios erstellt werden soll.
1. Klicken Sie mit der rechten Maustaste, und wählen Sie **[!UICONTROL Paste]**.
1. Verbinden Sie die eingefügten Module mit dem Szenario, indem Sie sie an die entsprechende Position im Szenario ziehen.

   Sie können auch Tastaturbefehle zum Kopieren und Einfügen verwenden.

## Szenario durch Klonen kopieren

Beim Klonen eines Szenarios wird eine Kopie des Szenarios erstellt, die Sie dann bearbeiten können.

1. Öffnen Sie die Seite mit den Szenario-Details:

   1. Klicken Sie im linken Bereich auf die Registerkarte **[!UICONTROL Scenario]** und dann auf ein Szenario, zu dem Sie Details anzeigen möchten.

      Oder

      Wenn Sie an dem Szenario im Szenario-Editor arbeiten, klicken Sie auf den linken Pfeil ![](assets/exit-editing-arrow.png) der oberen linken Ecke des Fensters.

1. Klicken Sie mit der rechten Maustaste oben rechts auf der Seite auf **[!UICONTROL Options]**.
1. Wählen Sie **[!UICONTROL Clone]** aus.
1. (Optional) Geben Sie einen Namen für das neue Szenario ein.
1. (Optional) Aktivieren Sie **[!UICONTROL Keep the states of any new modules the same as those being duplicated]**, um sicherzustellen, dass das kopierte Szenario auch Informationen zu den letzten Datensätzen enthält, die vom ursprünglichen Szenario verarbeitet wurden.
1. Klicken Sie auf **[!UICONTROL Save]** , um das Szenario zu erstellen.

## Kopieren eines Szenarios mithilfe von Blueprints

Szenario-Blueprints stellen die Anordnung, Zuordnung und Feldwerte eines bestimmten Szenarios zu einem bestimmten Zeitpunkt dar. Sie können einen Szenario-Blueprint in eine JSON-Datei auf Ihrem Computer exportieren und sie dann beim Erstellen eines neuen Szenarios importieren. Aus einem Szenario-Blueprint importierte Szenarien können bearbeitet werden.

Ein Szenario-Blueprint stellt das gesamte Szenario dar. Wenn Sie nur bestimmte Module aus einem Szenario kopieren möchten, finden Sie weitere Informationen unter [Kopieren eines Moduls oder einer Gruppe von Modulen](#copy-a-module-or-a-group-of-modules) in diesem Artikel.

### Szenario-Blueprint exportieren

1. Klicken Sie im linken Bedienfeld auf die Registerkarte **[!UICONTROL Scenarios]** .
1. Wählen Sie das Szenario aus, in das Sie eine Blueprint exportieren möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie im Szenario auf das Menü **[!UICONTROL More]** im Bereich Szenario-Einstellungen .
1. Klicken Sie auf **[!UICONTROL Export Blueprint]**.

   Eine JSON-Datei wird erstellt und auf Ihren Computer heruntergeladen. Sie können diese Datei in Ihrem [!DNL Downloads] Ordner finden.

### Blueprint importieren

>[!IMPORTANT]
>
>Wenn Sie eine Blueprint in ein vorhandenes Szenario importieren, ersetzt die Szenario-Blueprint das vorhandene Szenario. Sie können keine Blueprint an ein vorhandenes Szenario anhängen.

1. Beginnen Sie mit der Erstellung eines neuen Szenarios.
1. Klicken Sie im Szenario auf das Menü **[!UICONTROL More]** im Bereich Szenario-Einstellungen .
1. Klicken Sie auf **[!UICONTROL Import Blueprint]**.
1. Klicken Sie im angezeigten Dialogfeld auf **[!UICONTROL Browse]**
1. Navigieren Sie zu der Blueprint, die Sie importieren möchten, und klicken Sie auf **[!UICONTROL Open]**.
1. Klicken Sie auf **[!UICONTROL Save]**.

   Eine JSON-Datei wird erstellt und auf Ihren Computer heruntergeladen. Sie können diese Datei in Ihrem [!UICONTROL Downloads] Ordner finden.

## Kopieren und Wiederverwenden von Szenarien mithilfe von Vorlagen

Sie können Vorlagen als Ausgangspunkt für Ihre [!DNL Workfront Fusion] erstellen. Wenn Sie ein Szenario aus einer Vorlage erstellen, können Sie das Szenario ändern, ohne die Vorlage zu ändern. Feldwerte werden nicht in Vorlagen gespeichert.

Weitere Informationen zum Erstellen eines Szenarios mithilfe einer Vorlage finden Sie unter [Erstellen von Szenarios mit Vorlagen](/help/workfront-fusion/create-scenarios/add-modules/create-scenarios-with-fusion-templates.md).

## Fehlerbehebung

Wenn Sie Module kopieren und einfügen, wie in [Kopieren eines Moduls oder einer Gruppe von Modulen](#copy-a-module-or-a-group-of-modules) beschrieben, und beim Einfügen nichts angezeigt wird, überprüfen Sie die Site-Einstellungen Ihres Browsers, um sicherzustellen, dass das Einfügen aus der Zwischenablage zulässig ist.
