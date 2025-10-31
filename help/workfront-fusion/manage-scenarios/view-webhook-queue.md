---
title: K's Warteschlange
description: Viele Services stellen Webhooks bereit, mit denen sofortige Benachrichtigungen bereitgestellt werden können, sobald eine bestimmte Änderung im Service eintritt. Sofortige Trigger, auch als Webhooks bezeichnet, können diese Ereignisse verwenden, um Szenarien zu starten. Die Ereignisse werden in die Warteschlange des Webhooks aufgenommen, während sie auf die Verarbeitung warten, z. B. wenn das Szenario bereits ausgeführt wird. Sie können die Warteschlange des Webhooks anzeigen.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Webhook-Warteschlange anzeigen

Viele Services stellen Webhooks bereit, mit denen sofortige Benachrichtigungen bereitgestellt werden können, sobald eine bestimmte Änderung im Service eintritt. Sofortige Trigger, auch als Webhooks bezeichnet, können diese Ereignisse verwenden, um Szenarien zu starten. Die Ereignisse werden in die Warteschlange des Webhooks aufgenommen, während sie auf die Verarbeitung warten, z. B. wenn das Szenario bereits ausgeführt wird. Sie können die Warteschlange des Webhooks anzeigen.

Eingehende Webhook-Daten werden immer in der Warteschlange gespeichert, unabhängig davon, wie Sie die Option „Daten sind vertraulich“ im Bedienfeld „Szenario-Einstellungen“ festgelegt haben. Nachdem die Daten in einem Szenario verarbeitet wurden, werden sie dauerhaft aus der Warteschlange gelöscht.

Weitere Informationen zu Webhooks finden Sie unter [Instant Trigger (Webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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
