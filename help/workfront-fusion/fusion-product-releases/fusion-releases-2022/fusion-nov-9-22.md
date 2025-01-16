---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Workfront Fusion-Veröffentlichungsaktivität: Woche vom 7. November 2022'
description: Auf dieser Seite werden alle Verbesserungen beschrieben, die in Adobe Workfront Fusion in der Woche vom 7. November 2022 vorgenommen wurden.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 9d58abd0-1fe7-43c8-a1ea-2fadea738590
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Workfront Fusion-Veröffentlichungsaktivität: Woche vom 7. November 2022

**Webhook-Warteschlangen-Optimierung**

Die Webhook-Warteschlange von Fusion wurde mit dieser Version optimiert. Der Service, der Webhooks akzeptiert, ist jetzt von Warteschlangen- und anderen Prozessen getrennt. Diese Änderung ermöglicht es Fusion, Webhook-Warteschlangen schneller und konsistenter zu verarbeiten.

Während der Implementierung dieser Änderung konnten wir die erwartete Protokollverarbeitungszeit für Webhook-Ereignisse in der Warteschlange besser verstehen. Es wird erwartet, dass die Webhook-Viewer-Seite von Fusion nicht älter als 1 Minute ist.

Um die aktuell in der Warteschlange befindlichen Webhook-Ereignisse anzuzeigen, navigieren Sie in der linken Navigationsleiste zu Webhooks . LKW-Symbole mit einer Zahl im Zähler zeigen Warteschlangenereignisse für diesen Webhook an. Klicken Sie auf das LKW-Symbol, um die Ereignisse in der Warteschlange anzuzeigen.


**Nicht verwendete Webhooks werden jetzt deaktiviert oder gelöscht**

An der Art und Weise, wie Workfront Fusion mit nicht verwendeten Webhooks umgeht, haben wir einige Änderungen vorgenommen. Jetzt werden Webhooks automatisch deaktiviert, wenn einer der folgenden Punkte zutrifft:

* Der Webhook wurde seit mehr als 5 Tagen mit keinem Szenario verbunden.
* Der Webhook wird nur in inaktiven Szenarien verwendet, die seit mehr als 30 Tagen inaktiv sind.

Deaktivierte Webhooks werden automatisch gelöscht und von der Registrierung entfernt, wenn sie mit keinem Szenario verbunden sind und sich seit mehr als 30 Tagen im Status Deaktiviert befinden.
