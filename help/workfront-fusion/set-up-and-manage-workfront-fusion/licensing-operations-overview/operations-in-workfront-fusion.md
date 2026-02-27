---
title: Vorgänge
description: Ein Vorgang in Adobe Workfront Fusion ist eine Aufgabe, die von einem Modul ausgeführt wird. Zu Tracking-Zwecken ist jede erfolgreiche Aktion, die von einem Modul ausgeführt wird, ein Vorgang.
author: Becky
feature: Workfront Fusion
exl-id: c14e2bb2-1cce-48ff-8bea-acc9829d3cf2
source-git-commit: d630251ec01f5e11bad0305a2f49fb447bf1dd1e
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 1%

---

# Vorgänge

Ein Vorgang in Adobe Workfront Fusion ist eine Aufgabe, die von einem Modul ausgeführt wird. Zu Tracking-Zwecken ist jede erfolgreiche Aktion, die von einem Modul ausgeführt wird, ein Vorgang.

## Überlegungen beim Zählen der Anzahl der Vorgänge

* Im Allgemeinen wird jede erfolgreiche Ausführung von Aktionsschritten als Vorgang betrachtet.
* Das erste Modul in einem Szenario wird nur einmal ausgeführt und immer als ein Vorgang gezählt, auch wenn kein Bundle zurückgegeben wird.
* Wie oft die übrigen Module ausgeführt werden, hängt von der Anzahl der Bundles ab, die sie verarbeiten müssen.  Ein Durchgang eines Moduls für ein Bundle ist ein Vorgang. Eine Ausnahme bildet das Aggregator-Modul, das als ein Vorgang pro Satz von Bundles gezählt wird, die verarbeitet werden.
* Der Wert von Vorgängen kann abweichen. Einige werden kleiner und einfacher sein, andere werden komplexer sein. Vorgänge werden für Ihre Gesamtleistung angerechnet, unabhängig davon, wie einfach oder komplex sie sein mögen.
* Vorgänge werden bei der [!UICONTROL Finalisierung] einer Szenarioausführung gezählt.
* Folgende Vorgänge werden **nicht** gezählt:
   * Alle Filterschritte.
   * Jede Aktion, die einen Fehler verursacht oder angehalten wird.
   * Alle Routen, die nicht ausgeführt werden, weil die Regeln der Route nicht eingehalten wurden, z. B. Ausweich- oder deaktivierte Routen.
   * Jede Aktion, die nicht ausgeführt wird, entweder weil ein Filter keine Daten durchlässt oder weil das Szenario aufgrund eines Fehlers angehalten wurde.

>[!NOTE]
>
>Wenn Ihr Unternehmen routinemäßig versucht, mehr Vorgänge zu verwenden, als das Workfront Fusion-Paket zulässt, empfehlen wir, ein Upgrade auf das Ultimate-Paket für Automatisierung und Integration in Erwägung zu ziehen.

## Limits für Operationen

In Ihrem Unternehmen gibt es möglicherweise ein monatliches Betriebslimit. Dies basiert auf dem von Ihrem Unternehmen erworbenen Workfront-Plan. Der Plan [!UICONTROL Ultimate] Workfront bietet unbegrenzte Operationen.

Wenn für Ihr Unternehmen ein monatliches Limit gilt, werden Sie benachrichtigt, wenn Ihr Unternehmen das Limit fast erreicht hat. Wenn Ihr Unternehmen das Limit überschreitet, setzt sich Workfront mit Ihrem Unternehmen in Verbindung, um sicherzustellen, dass Ihr Plan Ihren Anforderungen entspricht.

Workfront Fusion sendet eine Benachrichtigung, wenn Ihr Unternehmen die folgenden Prozentsätze des monatlichen Limits für das Unternehmen erreicht:

* 50 %
* 75 %
* 90 %
* 100%

## Anzahl der in den letzten 30 Tagen durchgeführten Vorgänge anzeigen

Sie können ein Diagramm sehen, das die Anzahl der ausgeführten Vorgänge anzeigt. Diese Diagramme sind an den folgenden Speicherorten verfügbar:

* **Organisations-Dashboard**: Von der gesamten Organisation verwendete Vorgänge
* **Team-Dashboard**: Vorgänge, die von Szenarien verwendet werden, die diesem Team gehören
* **Seite mit Szenariodetails**: Von diesem Szenario verwendete Vorgänge
