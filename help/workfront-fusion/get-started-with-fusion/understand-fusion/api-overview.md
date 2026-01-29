---
title: Überblick über APIs
description: Über Anwendungsprogrammierschnittstellen (Application Programming Interfaces, APIs) können Anwendungen und Services miteinander kommunizieren. Fusion nutzt APIs zur Kommunikation mit der Anwendung, zu der Sie eine Verbindung herstellen. Jede Anwendung verfügt über eine separate API.
author: Becky
feature: Workfront Fusion
source-git-commit: 74308a6a43418296b29739f03683f23357d545bc
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 87%

---

# Überblick über die APIs in Fusion

<!--Add me to TOCs-->

Über Anwendungsprogrammierschnittstellen (Application Programming Interfaces, APIs) können Anwendungen und Services miteinander kommunizieren. Fusion nutzt APIs zur Kommunikation mit den Anwendungen, zu denen Sie eine Verbindung herstellen.

APIs werden von denjenigen erstellt und gesteuert, denen die Anwendung gehört. Beispielsweise gehört die Workfront-API dem Workfront-Team von Adobe und die Microsoft Graph-API Microsoft. Die Inhabenden einer API definieren, welche Aktionen über die API verfügbar sind.

>[!NOTE]
>
>Workfront Fusion verfügt über eine eigene API, mit der Sie Aktionen in Fusion automatisieren können.
>Die APIs werden schrittweise veröffentlicht und sind derzeit als experimentell gekennzeichnet. Das Fusion-Team arbeitet aktiv an der Entwicklung und Erweiterung der APIs. Sobald neue Funktionen verfügbar sind, werden Aktualisierungen veröffentlicht.
>Dokumentation zur Workfront Fusion-API finden Sie unter [Workfront Fusion-API](https://developer.adobe.com/workfront-fusion-apis/).

## Zu beachten

Die Tatsache, dass APIs inhaberseitig und nicht von Fusion definiert werden, führt zu diesen wichtigen Überlegungen:

* **Sie können Fusion verwenden, um eine Verbindung zu beliebigen Anwendungen oder Services mit einer öffentlichen API herzustellen**, unabhängig davon, ob Fusion einen dedizierten Connector zur jeweiligen Anwendung bzw. zum jeweiligen Service bietet oder nicht. Sie können die universellen Connectoren von Fusion verwenden, um diese Anwendungen oder Services in Ihre Szenarios einzubinden.

  Eine Liste der universellen Connectoren finden Sie unter [Universelle Connectoren](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

* **Änderungen, die inhaberseitig an einer Anwendungs-API vorgenommen werden, können sich auf die Fusion-Funktionalität auswirken.** Wenn die Änderungen gravierend genug sind, muss Fusion möglicherweise Module oder Verbindungstypen aktualisieren oder in Extremfällen einen neuen Connector für die Anwendung erstellen.

  Weitere Informationen zu diesen Extremsituationen, die als „Breaking Changes“ (umfassende Änderungen) bezeichnet werden, finden Sie in diesem Artikel unter [Breaking Changes](#breaking-changes).


## Breaking Changes

Eine häufige Ursache für Breaking Changes besteht darin, dass Organisationen, denen eine API gehört, die Unterstützung dafür entweder ganz oder teilweise einstellen und die API nicht mehr verfügbar ist. In diesem Fall setzt das Fusion-Team alles daran, die Fusion-Funktionalität schnell an die neue Version der Anwendungs-API anzupassen. Normalerweise erfolgt dies in Form von neuen Modulen, Verbindungstypen oder Connectoren.

Da Ihre Fusion-Szenarios mit Ihren spezifischen Daten konfiguriert sind, müssen Sie Ihre Szenarios möglicherweise aktualisieren.

* Sind die Änderungen im Zusammenhang mit der Authentifizierung oder Autorisierung erfolgt, müssen Sie die Verbindungen für diese Anwendung gegebenenfalls aktualisieren.
* Wenn die Änderungen mit einer bestimmten Aktion (einem Endpunkt) in der API im Zusammenhang stehen, müssen Sie unter Umständen jedes Modul, das sich auf diese Aktion bezieht, auf eine neue Version des Moduls aktualisieren.
* Wenn die gesamte von Fusion verwendete API-Version veraltet ist, müssen Sie möglicherweise alle Module dieses Connectors auf eine neue Version des Connectors aktualisieren.

Häufig können Sie auf die neue Version eines Moduls aktualisieren, ohne dieses Modul neu konfigurieren zu müssen.

Informationen und Anweisungen zum Aktualisieren eines Moduls finden Sie unter [Aktualisieren eines Moduls auf eine neue Version](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md).
