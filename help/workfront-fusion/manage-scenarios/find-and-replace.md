---
title: Suchen und Ersetzen von Variablen, Quellen und Verbindungen in einem Szenario
description: Verwenden Sie Suchen und Ersetzen , um eine zugeordnete Variable zu ersetzen, Verweise von einem Quellmodul einem anderen neu zuzuordnen oder eine Verbindung in andere Module in Ihrem Szenario zu kopieren.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 15%
---

# Suchen und Ersetzen von Variablen, Quellen und Verbindungen in einem Szenario

>[!NOTE]
>
>Diese Funktion ist nur in der neuen Version des Szenario-Editors verfügbar. Weitere Informationen finden Sie unter [Neue und klassische Erlebnisse](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) im Artikel Szenario-Editor.

Mit Suchen und Ersetzen können Sie dieselbe Änderung in vielen Modulen gleichzeitig vornehmen. Sie haben folgende Möglichkeiten:

* Ersetzen Sie eine zugeordnete Variable im gesamten Szenario oder in einem Modul.
* Ordnen Sie Verweise von einem Quellmodul einem anderen neu zu.
* Kopieren Sie eine Verbindung zu einem oder allen kompatiblen Modulen aus derselben App.

Bevor eine Änderung vorgenommen wird, zeigt Suchen und Ersetzen eine Vorschau der betroffenen Module an.

In der klassischen -Version können Sie die Tools Swap-Variable, Neuzuordnung der Quelle und Swap-Verbindung im DevTool verwenden, um diese Aufgaben auszuführen. Weitere Informationen finden Sie unter [Debuggen eines Szenarios](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md).

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
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Suchen und Ersetzen öffnen

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie Änderungen vornehmen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf **Symbol** Suchen und Ersetzen![ im Bereich Steuerelemente ](assets/find-replace-icon.png)Suchen und Ersetzen“.

   Möglicherweise müssen Sie auf das Dreipunkt-Symbol im Bereich Steuerelemente klicken, um das Symbol „Suchen und Ersetzen“ anzuzeigen.

Öffnungen im Bedienfeld auf der rechten Seite der Arbeitsfläche suchen und ersetzen.

## Ersetzen einer Variablen

Verwenden Sie die **Variable**, um eine zugeordnete Variable zu ersetzen.

1. Öffnen Sie Suchen und Ersetzen und klicken Sie dann auf die Registerkarte **Variable**.
1. Fügen Sie im Feld Variable suchen die Variable ein, die Sie ersetzen möchten.
1. Fügen Sie im Feld Ersetzen durch die Variable ein, die die vorherige Variable ersetzen wird.
1. Wählen Sie im Feld Modul das Modul aus, auf das die Änderung angewendet werden soll, oder wählen Sie **Ganzes Szenario**, um die Änderung auf alle betroffenen Module im Szenario anzuwenden.
1. Klicken Sie auf **Ersetzen**
1. Überprüfen Sie die Vorschau der betroffenen Module. Um zu einem Modul auf der Arbeitsfläche zu wechseln, wählen Sie seine Zeile in der Vorschau aus.
1. Klicken Sie auf **Übernehmen**.

## Quelle neu zuordnen

Verwenden Sie die Registerkarte **Source**, um zu ändern, auf welches Modul die Zuordnungen in anderen Modulen verweisen.

1. Öffnen Sie Suchen und Ersetzen und klicken Sie dann auf die Registerkarte **Source**.
1. Wählen Sie im Feld Source-Modul das Quellmodul aus, auf das die Zuordnungen derzeit verweisen.
1. Wählen Sie in den Feldern des Zielmoduls das Modul aus, auf das sie stattdessen verweisen sollen.
1. Wählen Sie im Feld Modul das Modul aus, auf das die Änderung angewendet werden soll, oder wählen Sie **Ganzes Szenario**, um die Änderung auf alle betroffenen Module im Szenario anzuwenden.
1. Klicken Sie auf **Ersetzen**
1. Überprüfen Sie die Vorschau der betroffenen Module. Um zu einem Modul auf der Arbeitsfläche zu wechseln, wählen Sie seine Zeile in der Vorschau aus.
1. Klicken Sie auf **Übernehmen**.

## Kopieren einer Verbindung zu anderen Modulen

Verwenden Sie die **Verbindung**, um dieselbe Verbindung in mehr als einem Modul derselben App zu verwenden.

1. Öffnen Sie Suchen und Ersetzen und klicken Sie dann auf die Registerkarte **Verbindung** .
1. Wählen Sie im Feld Verbindung von ein Modul aus, das derzeit über die Verbindung verfügt, die Sie für andere Module verwenden möchten.
1. Wählen Sie im Feld Anwenden auf das Modul aus, für das die Änderung gelten soll, oder ob die Änderung auf alle kompatiblen Module im Szenario angewendet werden soll.
1. Klicken Sie auf **Übernehmen**.
