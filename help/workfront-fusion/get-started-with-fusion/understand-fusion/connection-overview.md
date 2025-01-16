---
title: Verbindungsübersicht
description: Für die meisten Apps ist es erforderlich, eine Verbindung zu erstellen, über  [!DNL Adobe Workfront Fusion]  mit dem angegebenen Drittanbieterdienst entsprechend den Einstellungen des spezifischen Szenarios kommunizieren kann.
author: Becky
feature: Workfront Fusion
exl-id: 01132df7-4cc0-4ff3-b4d7-607a06558735
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Verbindungsübersicht

Für Workfront Fusion ist für die meisten Anwendungen eine Verbindung erforderlich.  Sie verwendet diese Verbindung für die Kommunikation mit dem angegebenen Drittanbieterdienst.

Wenn Sie beispielsweise ein Szenario erstellen möchten, das Informationen aus [!DNL Workfront] abruft, müssen Sie [!DNL Workfront Fusion] die Berechtigung erteilen, auf Ihr [!DNL Workfront]-Konto zuzugreifen.

Eine Verbindung stellt die Autorisierung und Berechtigungen dar, die Fusion für den Zugriff auf das Programm verwendet. Sie können für jede in Ihren Szenarien verwendete Anwendung eine oder mehrere Verbindungen erstellen und dieselbe Verbindung in mehreren Modulen oder Szenarien verwenden.

Die meisten Verbindungen werden nur für eine einzige Anwendung verwendet. Beispielsweise kann eine [!DNL Workfront]-Verbindung nicht in einem [!UICONTROL Salesforce] verwendet werden. Einige [!DNL Adobe] Anwendungen können Verbindungen gemeinsam nutzen. Weitere Informationen finden Sie in den Artikeln zu diesen Anwendungen, die unter [Fusion-Anwendungen und ihre Modulverweise: Artikelindex“ aufgeführt ](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

Verbindungen gehören Teams. Alle Mitglieder eines Teams haben Zugriff auf die Verbindungen des Teams, und Benutzer außerhalb eines Teams haben keinen Zugriff auf die Verbindungen des Teams.

## Zugriffsberechtigungen

Für jede Verbindung benötigt [!DNL Workfront Fusion] nur die Zugriffsrechte, die für den erfolgreichen Abschluss eines bestimmten Szenarios erforderlich sind. Wenn Sie beispielsweise ein Szenario erstellen, um ein Dokument aus [!DNL Workfront] herunterzuladen, fragt [!DNL Workfront Fusion] nicht nach der Berechtigung zum Erstellen eines neuen Projekts. Wenn Sie später feststellen, dass Sie ein Projekt erstellen müssen, können Sie die Verbindung aktualisieren oder eine neue erstellen, die Projekte erstellen kann.

Nicht alle Services ermöglichen es Ihnen, den Zugriff auf bestimmte Aufgaben zu beschränken. In diesen Fällen müssen [!DNL Workfront Fusion] vollständige Zugriffsrechte benötigen. Weitere Informationen dazu, wie Sie [!DNL Workfront Fusion] Zugriff auf Ihr registriertes -Konto auf diese Services beschränken können, finden Sie in der programmspezifischen Dokumentation unter [Fusion-Programme und deren Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
