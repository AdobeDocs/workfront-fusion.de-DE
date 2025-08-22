---
title: K's Warteschlange
description: Viele Services stellen Webhooks bereit, mit denen sofortige Benachrichtigungen bereitgestellt werden können, sobald eine bestimmte Änderung im Service eintritt. Sofortige Trigger, auch als Webhooks bezeichnet, können diese Ereignisse verwenden, um Szenarien zu starten. Die Ereignisse werden in die Warteschlange des Webhooks aufgenommen, während sie auf die Verarbeitung warten, z. B. wenn das Szenario bereits ausgeführt wird. Sie können die Warteschlange des Webhooks anzeigen.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---

# Webhook-Warteschlange anzeigen

Viele Services stellen Webhooks bereit, mit denen sofortige Benachrichtigungen bereitgestellt werden können, sobald eine bestimmte Änderung im Service eintritt. Sofortige Trigger, auch als Webhooks bezeichnet, können diese Ereignisse verwenden, um Szenarien zu starten. Die Ereignisse werden in die Warteschlange des Webhooks aufgenommen, während sie auf die Verarbeitung warten, z. B. wenn das Szenario bereits ausgeführt wird. Sie können die Warteschlange des Webhooks anzeigen.

Eingehende Webhook-Daten werden immer in der Warteschlange gespeichert, unabhängig davon, wie Sie die Option „Daten sind vertraulich“ im Bedienfeld „Szenario-Einstellungen“ festgelegt haben. Nachdem die Daten in einem Szenario verarbeitet wurden, werden sie dauerhaft aus der Warteschlange gelöscht.

Weitere Informationen zu Webhooks finden Sie unter [Instant Trigger (Webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

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
