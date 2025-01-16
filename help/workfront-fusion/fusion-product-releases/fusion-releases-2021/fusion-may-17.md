---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Workfront Fusion-Veröffentlichungsaktivität: Woche vom 17. Mai 2021'
description: Auf dieser Seite werden alle Verbesserungen beschrieben, die in Adobe Workfront Fusion in der Woche vom 17. Mai 2021 vorgenommen wurden.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 2ea57c69-8db7-4500-9157-e2c2d8c74938
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Workfront Fusion-Veröffentlichungsaktivität: Woche vom 17. Mai 2021

Auf dieser Seite werden alle Verbesserungen beschrieben, die in Adobe Workfront Fusion in der Woche vom 17. Mai 2021 vorgenommen wurden.

Eine Liste aller aktuellen Änderungen finden Sie unter [Adobe Workfront Fusion-Versionsaktivität](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Eine Liste der letzten Fehlerbehebungen in Workfront Fusion finden Sie auf der Seite [Workfront-Wartungs-Updates](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) und suchen Sie nach Updates mit der Bezeichnung Workfront Fusion-Wartungs-Update.

## Kopieren von Modulen in Workfront Fusion-Szenarien

Um die Arbeit mit Ihren Workfront Fusion-Szenarien zu vereinfachen, haben wir das Kopieren und Einfügen von Modulen ermöglicht. Jetzt können Sie ein Modul oder eine Gruppe von Modulen kopieren und in dasselbe oder ein anderes Szenario einfügen. Beim Kopieren von Modulen werden die Feldwerte in diesem Modul beibehalten.


## Auswahl mehrerer Module in einem Workfront Fusion-Szenario

Beim Bearbeiten eines Szenarios können jetzt mehrere Module gleichzeitig ausgewählt werden. Sie können dann Massenaktionen für die ausgewählten Module durchführen.

* Kopieren
* Verschieben
* Löschen

Beim Kopieren und Verschieben von Modulen werden die Modulwerte und alle Leitungen, die die Module verbinden, beibehalten.


## Module behalten jetzt nicht gespeicherte Informationen bei

Um die Erstellung von Szenarien zu vereinfachen, haben wir es Modulen ermöglicht, Feldwerte beizubehalten, wenn sie nicht im Fokus sind. Wenn Sie nun ein Modul verlassen, ohne es zu speichern, und zu ihm zurückkehren, zeigen die Felder die zuvor eingegebenen Werte an. Wenn das Modul geschlossen ist, wird ein Indikator angezeigt, dass es nicht gespeicherte Felder gibt.

## Der Azure AD-Connector verarbeitet jetzt neue und aktualisierte Datensätze separat

Neue Datensätze und Aktualisierungen vorhandener Datensätze werden jetzt von separaten Modulen verarbeitet.

* Trigger Um nach neuen Datensätzen zu suchen, können Sie das Modul Datensätze überwachen verwenden. Dieses Modul sucht nicht mehr nach aktualisierten Datensätzen.
* Um aktualisierte Datensätze zu erhalten, können Sie das neue Delta-Modul „Benutzer/Gruppen suchen“ verwenden. Dieses Modul gibt neue, aktualisierte und gelöschte Datensätze zurück.
