---
title: K's Warteschlange
description: Viele Services stellen Webhooks bereit, mit denen sofortige Benachrichtigungen bereitgestellt werden können, sobald eine bestimmte Änderung im Service eintritt. Sofortige Trigger, auch als Webhooks bezeichnet, können diese Ereignisse verwenden, um Szenarien zu starten. Die Ereignisse werden in die Warteschlange des Webhooks aufgenommen, während sie auf die Verarbeitung warten, z. B. wenn das Szenario bereits ausgeführt wird. Sie können die Warteschlange des Webhooks anzeigen.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
TQID: https://experienceleague.adobe.com/FtTjoNtYNM9kuPDMaHa4883m13pLO2MRat5ohnjXuAM
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 29%

---

# Webhook-Warteschlange anzeigen

Viele Services stellen Webhooks bereit, mit denen sofortige Benachrichtigungen bereitgestellt werden können, sobald eine bestimmte Änderung im Service eintritt. Sofortige Trigger, auch als Webhooks bezeichnet, können diese Ereignisse verwenden, um Szenarien zu starten. Die Ereignisse werden in die Warteschlange des Webhooks aufgenommen, während sie auf die Verarbeitung warten, z. B. wenn das Szenario bereits ausgeführt wird. Sie können die Warteschlange des Webhooks anzeigen.

Eingehende Webhook-Daten werden immer in der Warteschlange gespeichert, unabhängig davon, wie Sie die Option „Daten sind vertraulich“ im Bedienfeld „Szenario-Einstellungen“ festgelegt haben. Nachdem die Daten in einem Szenario verarbeitet wurden, werden sie dauerhaft aus der Warteschlange gelöscht.

Weitere Informationen zu Webhooks finden Sie unter [Instant-Auslöser (Webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

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

## Webhook-Warteschlange anzeigen

Alle Nachrichten von eingehenden Webhooks werden in der Warteschlange des Webhooks gespeichert.

Wenn ein Szenario derzeit über eine Warteschlange verfügt, wird in diesem Szenario ein Banner angezeigt:

![Warteschlangen-Banner](assets/queue-banner.png)

So zeigen Sie die Warteschlange eines Webhooks an:

1. Klicken Sie **[!UICONTROL Menü]** links auf „Webhooks“.
1. Suchen Sie den Webhook, für den Sie die Warteschlange anzeigen möchten.
1. Suchen Sie die Anzahl der Ereignisse in der Schaltfläche Empfangene Ereignisse .

   ![Webhook-Warteschlange](assets/webhook-queue.png)

1. Klicken Sie auf die Schaltfläche, um Details zu den Ereignissen in der Warteschlange anzuzeigen.
