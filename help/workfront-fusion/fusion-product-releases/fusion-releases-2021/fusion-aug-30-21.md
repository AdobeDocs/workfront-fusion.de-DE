---
title: Workfront Fusion-Versionsaktivität:&nbsp;Woche vom 30. August 2021
description: Workfront Fusion-Versionsaktivität:&nbsp;Woche vom 30. August 2021
author: Luke
draft: Probably
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: cac11147-5b3d-477b-869b-e255528c4bec
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Workfront Fusion-Veröffentlichungsaktivität: Woche vom 30. August 2021

Auf dieser Seite werden alle Verbesserungen beschrieben, die in Adobe Workfront Fusion in der Woche vom 30. August 2021 vorgenommen wurden.

Eine Liste aller aktuellen Änderungen finden Sie unter [Adobe Workfront Fusion-Versionsaktivität](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Eine Liste der letzten Fehlerbehebungen in Workfront Fusion finden Sie auf der Seite [Workfront-Wartungs-Updates](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) und suchen Sie nach Updates mit der Bezeichnung Workfront Fusion-Wartungs-Update.

## Filtern von Ereignissen mit Trigger im Modul Workfront > Ereignisse beobachten

1. Richten Sie einen benutzerdefinierten Filter für Ereignisse ein, die Trigger des Moduls &quot;Workfront&quot; > „Ereignisse beobachten“ sind.

   Um die Anzahl unnötiger Szenario-Ausführungen zu reduzieren, haben wir das Modul Workfront > Datensätze überwachen aktualisiert, um die Ereignisfilterung zu aktivieren. Jetzt können Sie beim Erstellen eines Webhooks einen Filter festlegen. Dadurch kann das Szenario nur dann einen Trigger erhalten, wenn das Ereignis bestimmte Kriterien erfüllt.

   Der Ereignisfilter bietet derzeit die folgenden Vorgänge:

   * Gleich: Ein Trigger wird nur durchgeführt, wenn ein Ereignis den Filterbedingungen entspricht. Sie können beispielsweise einen Filter einrichten, der ein Szenario nur dann Trigger, wenn das Ereignis in einem bestimmten Projekt auftritt.
   * Ungleich : Ein Trigger wird nur dann erstellt, wenn ein Ereignis nicht den Filterbedingungen entspricht. Sie können beispielsweise einen Trigger erstellen, der ein Szenario nur dann filtert, wenn das Problem, in dem ein Ereignis auftritt, nicht den Status „Geschlossen“ hat.

   Zuvor ruft das Modul Datensätze beobachten alle Datensätze ab. Benutzende konnten nur filtern, indem sie später im Szenario Filter eingerichtet haben.

   Um die Ereignisfilterung zu nutzen, erstellen Sie einen neuen Webhook im Modul Ereignisse beobachten . Es ist derzeit nicht möglich, vorhandene Webhooks zu bearbeiten, um diese Funktion einzuschließen. Es wird dringend empfohlen, neue Webhooks mit Ereignisfiltern für Ihre vorhandenen Szenarien zu erstellen.

1. Durch die aktuelle Verbindung ausgelöste Ereignisse herausfiltern.

   Um die Einrichtung Ihrer Webhooks für das Modul Workfront > Ereignisse beobachten zu vereinfachen, haben wir den gängigsten Ereignisfilter hinzugefügt. Jetzt bietet der Webhook eine Option, alle Änderungen herauszufiltern, die von -Modulen vorgenommen wurden, indem die für das Modul Ereignisse beobachten angegebene Verbindung verwendet wird. Mit anderen Worten: Bei aktiviertem Filter können alle Änderungen, die der mit dieser Verbindung verknüpfte Workfront-Benutzer vornimmt, das Szenario nicht in Trigger bringen.

   Zuvor war dieser Filter nicht verfügbar. Daher war es einfacher, in Workfront-Modulen vorgenommene Änderungen an Trigger-Szenarien vorzunehmen, die diese Module enthalten, was möglicherweise dazu führte, dass sich Szenarien in einer Endlosschleife selbst Trigger machten.
