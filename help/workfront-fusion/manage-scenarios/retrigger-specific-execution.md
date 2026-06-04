---
title: Erneutes Auslösen einer bestimmten Szenarioausführung
description: Sie können eine bestimmte Szenario-Ausführung erneut auslösen, um die Daten mithilfe eines aktualisierten Szenario-Blueprints zu verarbeiten oder ihren Datenfluss anzuzeigen.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 9c05aa1111fd571ea6f0ff86943b2849a39e4973
workflow-type: tm+mt
source-wordcount: 523
ht-degree: 18%

---

# Erneutes Auslösen einer bestimmten Szenarioausführung

Sie können eine bestimmte Szenario-Ausführung erneut auslösen, um die Daten mithilfe eines aktualisierten Szenario-Blueprints zu verarbeiten oder ihren Datenfluss anzuzeigen. Wenn Sie eine Ausführung erneut auslösen, wird das Szenario mit den Daten dieser Ausführung ausgeführt.

Wenn Sie beispielsweise ein Szenario aktualisieren, um eine Aktion hinzuzufügen, z. B. ein Problem zu erstellen, können Sie eine Ausführung, die vor dem Update stattgefunden hat, erneut auslösen. Das aktualisierte Szenario wird unter Verwendung des auslösenden Ereignisses des ursprünglichen Szenarios ausgeführt, aber es enthält auch die aktualisierte Aktion. In diesem Beispiel erstellt das Szenario ein Problem im Rahmen der neuen Ausführung.

Eine erneute Auslösung ist für Szenarien mit Webhook-Triggern und für untergeordnete Szenarien verfügbar.

Beim erneuten Auslösen eines Szenarios, das einen Webhook verwendet, kann das ursprüngliche Webhook-Ereignis erneut verwendet werden, sodass Sie das Ereignis nicht neu erstellen müssen, um das Szenario erneut auszulösen.

Bei Verwendung verketteter Szenarien kann die erneute Auslösung auch auf ein untergeordnetes Szenario angewendet werden. Das untergeordnete Szenario kann mithilfe der Daten, die in der ursprünglichen Ausführung vom übergeordneten Szenario gesendet wurden, erneut ausgelöst werden, ohne dass das übergeordnete Szenario erneut ausgelöst wird.

Weitere Informationen zu Webhooks finden Sie unter [Instant-Auslöser (Webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

Weitere Informationen zu Verkettungsszenarien finden Sie unter [Verketten mehrerer Szenarien](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

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

## Erneutes Auslösen einer Ausführung

Sie können eine Szenarioausführung erneut über das Diagramm des Szenarios, den Verlaufsbereich des Szenarios oder die Seite der spezifischen Szenarioausführung auslösen.

### Erneutes Auslösen einer Ausführung aus dem Szenariodiagramm

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, das die Ausführung ausgeführt hat, die Sie erneut auslösen möchten.

   Das Diagramm des Szenarios wird geöffnet.
1. Suchen Sie die Ausführung, die Sie erneut auslösen möchten, in der Liste Ausführungen rechts auf der Seite.
1. Klicken Sie **diesem Szenario** Erneut auslösen“.

![Aus Diagramm erneut auslösen](assets/retrigger-from-diagram.png)

### Auslösen einer Ausführung aus dem Szenarioverlauf

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, das die Ausführung ausgeführt hat, die Sie erneut auslösen möchten.

   Das Diagramm des Szenarios wird geöffnet.

1. Klicken Sie auf **Registerkarte** Verlauf“ direkt unter dem Szenarionamen.
1. Suchen Sie die Ausführung, die Sie erneut auslösen möchten. Sie können die Volltextsuche verwenden, um sie bei Bedarf zu finden.
1. Klicken Sie **diesem Szenario** Erneut auslösen“.

![Aus dem Verlauf auslösen](assets/retrigger-from-history.png)

### Auslösen eines Szenarios von der Ausführungsseite des Szenarios

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, das die Ausführung ausgeführt hat, die Sie erneut auslösen möchten.

   Das Diagramm des Szenarios wird geöffnet.
1. Suchen Sie die Ausführung, die Sie erneut auslösen möchten, in der Liste Ausführungen rechts auf der Seite.
1. Klicken Sie auf die Ausführung, um sie zu öffnen.
1. Klicken Sie auf der Ausführungsseite auf **Erneut auslösen**.


![Aus Ausführung auslösen](assets/retrigger-from-execution.png)



