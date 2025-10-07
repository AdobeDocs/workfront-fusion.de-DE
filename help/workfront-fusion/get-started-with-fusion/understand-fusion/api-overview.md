---
title: API-Übersicht
description: Anwendungsprogrammierschnittstellen (APIs) bieten eine Möglichkeit für Anwendungen und Dienste, miteinander zu kommunizieren. Fusion verwendet APIs zur Kommunikation mit dem Programm, mit dem Sie eine Verbindung herstellen. Jedes Programm verfügt über eine separate API.
author: Becky
feature: Workfront Fusion
source-git-commit: 1ee32ad1faa8c105142f85e83f1b522548fc7f93
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Übersicht über APIs in Fusion

<!--Add me to TOCs-->

Anwendungsprogrammierschnittstellen (APIs) bieten eine Möglichkeit für Anwendungen und Dienste, miteinander zu kommunizieren. Fusion verwendet APIs zur Kommunikation mit den Anwendungen, mit denen Sie eine Verbindung herstellen.

APIs werden von den Inhabern der Anwendung erstellt und gesteuert. Beispielsweise gehört die Workfront-API dem Workfront-Team von Adobe und die Microsoft-Graph-API Microsoft. Der Inhaber der API definiert, welche Aktionen über die API verfügbar sind.

## Zu beachten

Die Tatsache, dass APIs von ihren Besitzern und nicht von Fusion definiert werden, führt zu einigen wichtigen Überlegungen:

* **Sie können Fusion verwenden, um eine Verbindung zu jeder App oder jedem Service herzustellen, die über eine öffentliche API**, unabhängig davon, ob Fusion einen dedizierten Connector zu dieser App oder diesem Service anbietet oder nicht. Sie können die universellen Connectoren von Fusion verwenden, um diese Apps oder Services in Ihre Szenarien zu bringen.

  Eine Liste der universellen Connectoren finden Sie unter [Universelle Connectoren](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)

* **Änderungen, die der Eigentümer einer Anwendung an der API vornimmt, können sich auf die Fusion-Funktionalität auswirken.** Wenn die Änderungen schwerwiegend genug sind, muss Fusion möglicherweise Module oder Verbindungstypen aktualisieren oder in Extremfällen einen neuen Connector für die Anwendung erstellen.

  Weitere Informationen zu diesen Extremsituationen, die als „grundlegende Änderungen“ bezeichnet werden, finden Sie unter [Umfassende Änderungen](#breaking-changes) in diesem Artikel.


## Umfassende Änderungen

Eine häufige Ursache für grundlegende Änderungen ist die Einstellung, wenn ein API-Verantwortlicher eine API ganz oder teilweise aus der Verfügbarkeit entfernt. In diesem Fall unternimmt das Fusion-Team alle Anstrengungen, um die Fusion-Funktionalität schnell an die neue Version der API des Programms anzupassen. Normalerweise erfolgt dies in Form von neuen Modulen, Verbindungstypen oder Connectoren.

Da Ihre Fusion-Szenarien mit Ihren spezifischen Daten konfiguriert sind, müssen Sie Ihre Szenarien möglicherweise aktualisieren.

* Wenn die Änderungen mit der Authentifizierung oder Autorisierung in Zusammenhang standen, müssen Sie möglicherweise die Verbindungen für diese Anwendung aktualisieren.
* Wenn sich die Änderungen auf eine bestimmte Aktion (Endpunkt) in der API bezogen, müssen Sie die Module zu dieser Aktion möglicherweise auf eine neue Version des Moduls aktualisieren.
* Wenn die gesamte von Fusion verwendete API-Version veraltet ist, müssen Sie möglicherweise alle Module dieses Connectors auf eine neue Version eines Connectors aktualisieren.

In vielen Fällen können Sie auf die neue Version eines Moduls aktualisieren, ohne dieses Modul neu konfigurieren zu müssen.

Informationen und Anweisungen zum Aktualisieren eines Moduls finden Sie unter [Aktualisieren eines Moduls auf eine neue Version](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md).
