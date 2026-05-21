---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Workfront Fusion-Veröffentlichungen: Woche vom 3. Mai 2021'
description: Auf dieser Seite werden alle Verbesserungen beschrieben, die in Adobe Workfront Fusion in der Woche vom Dienstag, 3. Mai 2021 vorgenommen wurden.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 8858fc79-5eda-4938-9bb5-c05be38f02bc
TQID: https://experienceleague.adobe.com/GZ5W-9Q1Y9M-cCVN1CupZVs8GuQPy4Dusifz-5sxJm8
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 273
ht-degree: 35%

---

# Workfront Fusion-Veröffentlichungen: Woche vom 3. Mai 2021

Auf dieser Seite werden alle Verbesserungen beschrieben, die in Adobe Workfront Fusion in der Woche vom Dienstag, 3. Mai 2021 vorgenommen wurden.

Eine Liste aller aktuellen Änderungen finden Sie unter [Adobe Workfront Fusion-Veröffentlichungen](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Eine Liste der letzten Fehlerbehebungen in Workfront Fusion finden Sie auf der Seite [Wartungs-Updates für Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=de). Suchen Sie nach Updates mit der Bezeichnung „Workfront Fusion-Wartungs-Update“.

## Salesforce-Connector kann jetzt mit SOQL suchen

Das Modul Salesforce > Suche nach Datensätzen bietet jetzt die Möglichkeit, mit SOQL (Salesforce Object Query Language) zu suchen. Sie können auch mit den zuvor verfügbaren Optionen suchen (SOSL und einfache Suchen).

## Neuer Verbindungstyp im Azure DevOps-Connector erfordert weniger Bereiche

Zur Verbesserung der Sicherheit haben wir dem Workfront Fusion Azure DevOps-Connector einen neuen Connector-Typ hinzugefügt. Wenn Sie jetzt eine Verbindung in einem Azure DevOps-Modul erstellen, können Sie aus zwei Verbindungstypen auswählen:

* Azure DevOps

  Dieser neue Verbindungstyp beschränkt die Bereiche auf die, die speziell von Workfront Fusion benötigt werden.

* Azure DevOps (alle Bereiche anfordern)

  Hierbei handelt es sich um den Legacy-Verbindungstyp, bei dem alle in einer Verbindung mit Azure DevOps verfügbaren Bereiche angefordert werden.

Es wird empfohlen, den Azure DevOps-Verbindungstyp in allen neuen Szenarien zu verwenden, in denen Azure DevOps verwendet wird. Es wird außerdem empfohlen, alle Azure DevOps-Module in Ihren bestehenden Szenarien so zu ändern, dass sie den neuen Verbindungstyp verwenden. Der alte Azure-DevOps-Verbindungstyp (alle Bereiche anfordern) wird in naher Zukunft nicht mehr unterstützt.
