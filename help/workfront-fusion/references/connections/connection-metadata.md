---
title: Verbindungsmetadaten
description: Fusion verwendet Metadaten, um wichtige Attribute einer Verbindung zu identifizieren.
author: Becky
feature: Workfront Fusion
exl-id: b41fbe8c-30fa-49d0-8a24-3535642b97ae
TQID: https://experienceleague.adobe.com/95OLgw45L7WeFuTtNYYD1lVYf916pkSNVVw0O8eZ9y8
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 5%

---

# Verbindungsmetadaten

Fusion verwendet Metadaten, um wichtige Attribute einer Verbindung zu identifizieren.

Verbindungsmetadaten können beim Erstellen einer neuen Verbindung festgelegt werden. Diese Attribute befinden sich im selben Dialogfeld, das zum Einrichten einer Verbindung verwendet wird:

![Verbindungsmetadaten](assets/connection-metadata-setup.png)

Fusion-Benutzer können Verbindungen im Bereich Verbindungen anzeigen und bearbeiten. Sie können den Bereich Verbindungen erreichen, indem Sie im linken Navigationsbereich auf Verbindungen klicken.

![Bereich „Verbindungen“ in der linken Navigation](assets/connections-in-left-nav.png)

<!--![Connection metadata in Connections area](assets/connections-area-metadata.png)-->

## Umgebungstyp

Fusion-Verbindungen können sowohl von Produktions- als auch von Nicht-Produktionssystemen verwendet werden. Sie können den Umgebungstyp markieren, mit dem eine Verbindung hergestellt wird, was zum Schutz der Produktionsumgebungen beiträgt.

Der Umgebungstyp wird wie andere Verbindungsmetadaten nur zu Informationszwecken verwendet. Benutzer sind dafür verantwortlich, dieses Attribut genau festzulegen und in einem Szenario eine Verbindung mit der richtigen Umgebung zu verwenden.

## Authentifizierungstyp

Fusion-Verbindungen können sowohl für Service-Konten als auch für persönliche Konten verwendet werden. Service-Konten werden für die Authentifizierung verwendet, wenn ein Szenario als Fusion automatisiert wird. Personenbezogene Konten sind Authentifizierungen, die auf einer bestimmten Person basieren. Welcher Authentifizierungstyp verwendet wird, hängt von den Anforderungen des Szenarios ab. Für automatisierte Benutzeraktionen sollten persönliche Konten verwendet werden. Wenn beispielsweise ein Fusion-Szenario die Genehmigung durch eine bestimmte Person automatisiert, sollte der Authentifizierungstyp für diese Person sein. Andernfalls fungiert Fusion als Fusion, und der Typ sollte Service Account sein.

Der Authentifizierungstyp wird wie andere Verbindungsmetadaten nur zu Informationszwecken verwendet. Benutzer sind dafür verantwortlich, dieses Attribut genau festzulegen und den richtigen Verbindungstyp in einem Szenario zu verwenden.

Weitere Informationen zu Authentifizierungstypen finden Sie unter [Authentifizierung](https://developer.adobe.com/developer-console/docs/guides/authentication/) im Authentifizierungshandbuch von Adobe.

## Ressourcen

* Anweisungen zum Verwalten von Verbindungsmetadaten finden Sie unter [Verbindungen verwalten](/help/workfront-fusion/create-scenarios/connect-to-apps/manage-connections.md).
