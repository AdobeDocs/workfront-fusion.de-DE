---
title: Verkettete Szenariobeziehungen anzeigen
description: Sie können eine Zuordnung der Beziehungen zwischen übergeordneten und untergeordneten Szenarien erstellen.
author: Becky
feature: Workfront Fusion
exl-id: 0782c6b1-42a5-48de-bfa0-3ced6ed2bf7f
source-git-commit: aee2b35919e240cce5346df6d94a610c34b26e88
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 18%

---

# Anzeigen und Verwalten verketteter Szenariobeziehungen

Sie können eine Zuordnung der Beziehungen zwischen übergeordneten und untergeordneten Szenarien erstellen. Sie können die Zuordnung auch verwenden, um zu verschiedenen Szenarien in der Kette zu springen.

Weitere Informationen zu verketteten Szenarien finden Sie unter [Verketten mehrerer Szenarien](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

Informationen zum Konfigurieren von verketteten Szenarien finden Sie unter [Kettenmodule](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md)

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

## Anzeigen einer Karte mit verketteten Beziehungen

Sie können eine Zuordnung des aktuellen Szenarios und der übergeordneten oder untergeordneten Szenarios anzeigen. Die Karte zeigt ein Diagramm des Datenflusses durch die verketteten Szenarien.

![Verkettete Szenariobeziehungen](assets/chained-scenario-relationships-2.png)

<!--get a better picture-->

So zeigen Sie die Beziehungszuordnung für ein verkettetes Szenario an:

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenario“ im linken Bereich und klicken Sie dann auf das Szenario.

   ODER

   Wenn Sie das Szenario im Szenario-Editor bearbeiten, klicken Sie auf den Pfeil nach links ![Pfeil zum Beenden der Bearbeitung](assets/exit-editing-arrow.png) in der oberen linken Ecke des Fensters.

1. Klicken Sie auf **Registerkarte** Beziehungen“.

   ![Registerkarte „Beziehungen“](assets/relations-tab.png)

1. Allgemeine Details zu den einzelnen verketteten Szenarien finden Sie unter Tags .

   Jedes Szenario verfügt über eines oder mehrere der folgenden Tags:

   * Stamm : Das Szenario beginnt an der Kette und hat kein übergeordnetes Szenario.
   * Übergeordnet : Das Szenario ist ein übergeordnetes Szenario.
   * Untergeordnet : Das Szenario ist ein untergeordnetes Szenario. Ein Szenario kann sowohl ein Elternteil als auch ein untergeordnetes Element sein.
   * Aktuell: Dies ist das Szenario, das der Benutzer derzeit anzeigt. Das heißt, dies ist das Szenario, in dem der Benutzer die Beziehungszuordnung geöffnet hat.

   ![Szenario-Tags in der Beziehungszuordnung](assets/chained-scenario-maps-tag.png)
1. (Optional) Um ein kleines Diagramm eines Szenarios anzuzeigen, bewegen Sie den Mauszeiger über das Szenario.
1. (Optional) Um direkt von der Karte zu einem anderen Szenario zu wechseln, klicken Sie auf das Szenario.

   Das angeklickte Szenario wird in einem anderen Fenster geöffnet.
1. (Optional) Um zwischen horizontaler und vertikaler Ansicht der Karte zu wechseln, klicken Sie **Horizontal** oder **Vertikal** oben rechts auf der Seite „Szenario-Details“.
1. (Optional) Um eine vereinfachte Ansicht der Karte anzuzeigen, überprüfen Sie die untere rechte Ecke der Seite.

   Dies kann praktisch sein, wenn Ihre Kettenkarte groß oder komplex ist.

   * Wenn Sie nur einen Teil der Karte anzeigen, ist dieser Teil auf der vereinfachten Karte dunkler.
   * Das aktuelle Szenario ist auf der vereinfachten Karte blau markiert.
1. Um den Ausführungsverlauf für die Kette anzuzeigen, klicken Sie auf die Registerkarte Verlauf oben in der Ansicht.

   Sie können auf einen Verlauf klicken, um die spezifischen Daten anzuzeigen, die zwischen verketteten Szenarien übergeben werden.
