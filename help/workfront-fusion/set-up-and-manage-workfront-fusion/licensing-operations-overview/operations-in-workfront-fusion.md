---
title: Vorgänge
description: Ein Vorgang in Adobe Workfront Fusion ist eine Aufgabe, die von einem Modul ausgeführt wird. Zu Tracking-Zwecken ist jede erfolgreiche Aktion, die von einem Modul ausgeführt wird, ein Vorgang.
author: Becky
feature: Workfront Fusion
exl-id: c14e2bb2-1cce-48ff-8bea-acc9829d3cf2
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Vorgänge

Ein Vorgang in Adobe Workfront Fusion ist eine Aufgabe, die von einem Modul ausgeführt wird. Zu Tracking-Zwecken ist jede erfolgreiche Aktion, die von einem Modul ausgeführt wird, ein Vorgang.

## Überlegungen beim Zählen der Anzahl der Vorgänge

* Im Allgemeinen wird jede erfolgreiche Ausführung von Aktionsschritten als Vorgang betrachtet.
* Das erste Modul in einem Szenario wird nur einmal ausgeführt und immer als ein Vorgang gezählt, auch wenn kein Bundle zurückgegeben wird.
* Wie oft die übrigen Module ausgeführt werden, hängt von der Anzahl der Bundles ab, die sie verarbeiten müssen.  Ein Durchgang eines Moduls für ein Bundle ist ein Vorgang. Eine Ausnahme bildet das Aggregator-Modul, das als ein Vorgang pro Satz von Bundles gezählt wird, die verarbeitet werden.
* Vorgänge werden in der [!UICONTROL Finalization] Phase der Ausführung eines Szenarios gezählt.
* Folgende Vorgänge werden **nicht** gezählt:
   * Alle Filterschritte.
   * Jede Aktion, die einen Fehler verursacht oder angehalten wird.
   * Alle Routen, die nicht ausgeführt werden, weil die Regeln der Route nicht eingehalten wurden, z. B. Ausweich- oder deaktivierte Routen.
   * Jede Aktion, die nicht ausgeführt wird, entweder weil ein Filter keine Daten durchlässt oder weil das Szenario aufgrund eines Fehlers angehalten wurde.

## Limits für Operationen

In Ihrem Unternehmen gibt es möglicherweise ein monatliches Betriebslimit. Dies basiert auf dem [!DNL Workfront], den Ihr Unternehmen erworben hat. Der [!UICONTROL Ultimate] [!DNL Workfront] bietet unbegrenzten Betrieb.

Wenn für Ihr Unternehmen ein monatliches Limit gilt, werden Sie benachrichtigt, wenn Ihr Unternehmen das Limit fast erreicht hat. Wenn Ihre Organisation das Limit überschreitet, kontaktieren [!DNL Workfront] Ihre Organisation, um sicherzustellen, dass Ihr Plan Ihren Anforderungen entspricht.

## Anzahl der in den letzten 30 Tagen durchgeführten Vorgänge anzeigen

Sie können ein Diagramm sehen, das die Anzahl der ausgeführten Vorgänge anzeigt. Diese Diagramme sind an den folgenden Speicherorten verfügbar:

* **Organisations-Dashboard**: Von der gesamten Organisation verwendete Vorgänge
* **Team-Dashboard**: Vorgänge, die von Szenarien verwendet werden, die diesem Team gehören
* **Seite mit Szenariodetails**: Von diesem Szenario verwendete Vorgänge
