---
title: K's Warteschlange
description: Viele Services stellen Webhooks bereit, mit denen sofortige Benachrichtigungen bereitgestellt werden können, sobald eine bestimmte Änderung im Service eintritt. Sofortige Trigger, auch als Webhooks bezeichnet, können diese Ereignisse verwenden, um Szenarien zu starten. Die Ereignisse werden in die Warteschlange des Webhooks aufgenommen, während sie auf die Verarbeitung warten, z. B. wenn das Szenario bereits ausgeführt wird. Sie können die Warteschlange des Webhooks anzeigen.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
TQID: 'https://experienceleague.adobe.com/FtTjoNtYNM9kuPDMaHa4883m13pLO2MRat5ohnjXuAM'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 1c28e4007e3e9d6503618482002e506f9393ee57
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 16%
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

Die Warteschlangenseite des Webhooks weist dasselbe Layout auf wie die Listen **[!UICONTROL Szenarien]** und **[!UICONTROL Webhooks]**.

>[!NOTE]
>
>Suchen und Sortieren gelten nur für die Ereignisse, die derzeit in der Tabelle geladen sind, nicht für die gesamte Warteschlange. Um weitere Ereignisse einzubeziehen, laden Sie zuerst zusätzliche Ereignisse.

So zeigen Sie die Warteschlange eines Webhooks an und verwalten sie:

1. Klicken Sie **[!UICONTROL Menü]** links auf „Webhooks“.
1. Suchen Sie den Webhook, für den Sie die Warteschlange anzeigen möchten.
1. Suchen Sie die Spalte Anzahl der Ereignisse in der vollständigen Warteschlange.

   ![Webhook-Warteschlange](assets/webhook-queue.png)

1. Klicken Sie auf **Vorgänge**, um Details zu den Ereignissen in der Warteschlange anzuzeigen.

   Die Seite Warteschlange des Webhooks wird geöffnet. Auf der Seite werden die Ereignisse in der Warteschlange in einer Tabelle mit den folgenden Spalten aufgelistet **[!UICONTROL ID]**, **[!UICONTROL Erstellt in]**, **[!UICONTROL Size]** und **[!UICONTROL Details]**.

1. (Optional) Um die Ereignisse in der Tabelle zu filtern, geben Sie Text in das Feld **[!UICONTROL Suche]** über der Tabelle ein.
1. (Optional) Um die Ereignisse zu sortieren, klicken Sie auf die Spaltenüberschrift **[!UICONTROL ID]**, **[!UICONTROL Erstellt um]** oder **[!UICONTROL Size]**.
1. (Optional) Um die Anzahl der Ereignisse zu ändern, die auf jeder Seite angezeigt werden, wählen Sie eine Zahl in der **[!UICONTROL Anzeigen]** Dropdown-Liste unten auf der Seite aus.
1. (Optional) Um zwischen den Ereignisseiten zu wechseln, klicken **[!UICONTROL unten auf]** Seite auf **[!UICONTROL Erste]**, **[!UICONTROL Weiter]** oder **[!UICONTROL Letzte]**.

   Diese Schaltflächen sind nicht verfügbar, wenn die Warteschlange nur eine Ereignisseite hat.

1. (Optional) Um die Payload eines Ereignisses anzuzeigen, klicken Sie auf **[!UICONTROL Details]** in der Zeile für das Ereignis.

   Das Dialogfeld Details wird geöffnet und zeigt die Payload des Ereignisses an.

1. (Optional) So löschen Sie Ereignisse:

   1. Wählen Sie die Ereignisse aus, die Sie löschen möchten, indem Sie einen der folgenden Schritte ausführen:

      * Aktivieren Sie das Kontrollkästchen neben jedem Ereignis, das Sie auswählen möchten.
      * Aktivieren Sie das **[!UICONTROL Alle auswählen]**, um die gesamte Warteschlange auszuwählen, nicht nur die gerade geladenen Ereignisse. Anschließend können Sie das Kontrollkästchen für alle Ereignisse deaktivieren, die Sie aus der Auswahl ausschließen möchten.

   1. Klicken Sie in der Leiste am unteren Bildschirmrand auf **Löschen**.
