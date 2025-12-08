---
title: Überblick über Verbindungen
description: Bei den meisten Anwendungen ist es erforderlich, eine Verbindung zu erstellen, über die Adobe Workfront Fusion mit dem angegebenen Drittanbieter-Service entsprechend den Einstellungen des jeweiligen Szenarios kommunizieren kann.
author: Becky
feature: Workfront Fusion
exl-id: 01132df7-4cc0-4ff3-b4d7-607a06558735
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: ht
source-wordcount: '315'
ht-degree: 100%

---

# Überblick über Verbindungen

Workfront Fusion benötigt für die meisten Anwendungen eine Verbindung.  Diese Verbindung dient zur Kommunikation mit dem jeweiligen Drittanbieter-Service.

Wenn Sie beispielsweise ein Szenario erstellen möchten, das Informationen aus Workfront abruft, müssen Sie Workfront Fusion die Berechtigung zum Zugreifen auf Ihr Workfront-Konto erteilen.

Eine Verbindung stellt die Autorisierung und Berechtigungen dar, die Fusion für den Zugriff auf die Anwendung verwendet. Sie können für jede in Ihren Szenarios verwendete Anwendung eine oder mehrere Verbindungen erstellen und dieselbe Verbindung in mehreren Modulen oder Szenarios nutzen.

Die meisten Verbindungen werden nur für eine einzige Anwendung verwendet. Beispielsweise kann eine Workfront-Verbindung nicht in einem [!UICONTROL Salesforce]-Modul eingesetzt werden. Einige [!DNL Adobe]-Anwendungen ermöglichen es, Verbindungen gemeinsam zu nutzen. Weitere Informationen finden Sie in den Artikeln zu diesen Anwendungen unter [Referenzen zu Fusion-Anwendungen und ihren Modulen: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

Verbindungen gehören Teams. Alle Mitglieder eines Teams haben Zugriff auf die Verbindungen des Teams, Benutzende außerhalb eines Teams jedoch nicht.

## Zugriffsberechtigungen

Workfront Fusion benötigt für jede Verbindung nur die Zugriffsrechte, die für den erfolgreichen Abschluss eines bestimmten Szenarios erforderlich sind. Wenn Sie beispielsweise ein Szenario erstellen, um ein Dokument aus Workfront herunterzuladen, fordert Workfront Fusion nicht die Berechtigung zum Erstellen eines neuen Projekts an. Wenn Sie später ein Projekt erstellen müssen, können Sie die Verbindung aktualisieren oder eine neue Verbindung erstellen, die eine Projekterstellung ermöglicht.

Nicht alle Services lassen es zu, dass Sie den Zugriff auf bestimmte Aufgaben beschränken. In diesen Fällen ist Workfront Fusion auf Vollzugriff angewiesen. Weitere Informationen dazu, wie Sie den Workfront Fusion-Zugriff auf Ihr für diese Services registriertes Konto beschränken können, finden Sie in der anwendungsspezifischen Dokumentation unter [Referenzen zu Fusion-Anwendungen und ihren Modulen: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
