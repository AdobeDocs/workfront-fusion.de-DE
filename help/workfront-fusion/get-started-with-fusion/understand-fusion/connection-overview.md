---
title: Verbindungsübersicht
description: Für die meisten Apps ist es erforderlich, eine Verbindung zu erstellen, über die Adobe Workfront Fusion mit dem angegebenen Drittanbieterdienst entsprechend den Einstellungen des jeweiligen Szenarios kommunizieren kann.
author: Becky
feature: Workfront Fusion
exl-id: 01132df7-4cc0-4ff3-b4d7-607a06558735
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Verbindungsübersicht

Für Workfront Fusion ist für die meisten Anwendungen eine Verbindung erforderlich.  Sie verwendet diese Verbindung für die Kommunikation mit dem angegebenen Drittanbieterdienst.

Wenn Sie beispielsweise ein Szenario erstellen möchten, das Informationen aus Workfront abruft, müssen Sie Workfront Fusion die Berechtigung erteilen, auf Ihr Workfront-Konto zuzugreifen.

Eine Verbindung stellt die Autorisierung und Berechtigungen dar, die Fusion für den Zugriff auf das Programm verwendet. Sie können für jede in Ihren Szenarien verwendete Anwendung eine oder mehrere Verbindungen erstellen und dieselbe Verbindung in mehreren Modulen oder Szenarien verwenden.

Die meisten Verbindungen werden nur für eine einzige Anwendung verwendet. Beispielsweise kann eine Workfront-Verbindung nicht in einem [!UICONTROL Salesforce]-Modul verwendet werden. Einige [!DNL Adobe] Anwendungen können Verbindungen gemeinsam nutzen. Weitere Informationen finden Sie in den Artikeln zu diesen Anwendungen, die unter [Fusion-Anwendungen und ihre Modulverweise: Artikelindex“ aufgeführt ](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

Verbindungen gehören Teams. Alle Mitglieder eines Teams haben Zugriff auf die Verbindungen des Teams, und Benutzer außerhalb eines Teams haben keinen Zugriff auf die Verbindungen des Teams.

## Zugriffsberechtigungen

Workfront Fusion benötigt für jede Verbindung nur die Zugriffsrechte, die für den erfolgreichen Abschluss eines bestimmten Szenarios erforderlich sind. Wenn Sie beispielsweise ein Szenario erstellen, um ein Dokument aus Workfront herunterzuladen, fordert Workfront Fusion nicht die Berechtigung zum Erstellen eines neuen Projekts an. Wenn Sie später feststellen, dass Sie ein Projekt erstellen müssen, können Sie die Verbindung aktualisieren oder eine neue erstellen, die Projekte erstellen kann.

Nicht alle Services ermöglichen es Ihnen, den Zugriff auf bestimmte Aufgaben zu beschränken. In diesen Fällen müssen für Workfront Fusion vollständige Zugriffsrechte erforderlich sein. Weitere Informationen dazu, wie Sie den Workfront Fusion-Zugriff auf Ihr -Konto einschränken können, das für diese Services registriert ist, finden Sie in der programmspezifischen Dokumentation unter [Fusion-Programme und deren Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
