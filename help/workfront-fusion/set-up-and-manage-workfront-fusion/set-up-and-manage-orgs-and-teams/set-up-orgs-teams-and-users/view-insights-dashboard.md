---
title: Anzeigen des Insights-Dashboards für eine Organisation
description: Fusion-Administratoren können ein Dashboard anzeigen, das Ausführungsmetriken für eine Organisation anzeigt.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 069ab0fd3d72da3b67d50e4f8e62823c825ef934
workflow-type: tm+mt
source-wordcount: 849
ht-degree: 4%

---

# Anzeigen des Insights-Dashboards für eine Organisation

Mit dem Fusion Insights-Dashboard können Sie schnell feststellen, welche Szenarien am häufigsten ausgeführt werden, wo Verzögerungen auftreten und wie effektiv Ihre Worker-Pools funktionieren. Dies bietet Echtzeiteinblicke in Ausführungsvolumen, Warteschlangentiefe, Poolauslastung und Leistung auf Szenario-Ebene.

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Adobe Workfront Workflow Ultimate und Adobe Workfront Automatisierung und Integration Ultimate</p><p>Workfront Ultimate</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene</td> 
   <td> 
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Unternehmen sein.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Komponenten des Insights-Dashboards

>[!NOTE]
>
>Metriken werden nach Worker-Pool angezeigt. Um einen anderen Arbeitskraft-Pool anzuzeigen, klicken Sie auf das Feld Pool in der oberen linken Ecke des Dashboards und wählen Sie dann den Pool aus, für den Sie Metriken anzeigen möchten.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

Im Dashboard „Fusion Insights“ werden die folgenden Metriken angezeigt.

* **Protokolle zu fehlgeschlagenen Ausführungen**
In dieser Tabelle werden alle fehlgeschlagenen oder warnenden Szenarien in Ihrer Organisation aufgelistet, sodass Sie Problemausführungen finden und beheben können, ohne das Dashboard verlassen zu müssen.

* **Ausführungen warten auf die Verarbeitung**
Dieses Diagramm zeigt die Anzahl der Ausführungen, die zu einem bestimmten Zeitpunkt auf die Verarbeitung warten (auch als Ausführungsrückstand bezeichnet).

  Eine hohe Anzahl an Ausführungen, die darauf warten, verarbeitet zu werden, kann sich auf die Leistung in Ihrer Fusion-Instanz auswirken. Sie erhalten eine Benachrichtigung, wenn Ihr Ausführungsrückstand 5000 Ausführungen erreicht. Es wird empfohlen, verantwortliche Szenarien zu identifizieren und sie zu ändern oder zu deaktivieren. Wenn der hohe Ausführungsrückstand weiterhin besteht, schützt das Fusion-Team die Leistung Ihrer Fusion-Instanz, indem es die verantwortlichen Szenarien deaktiviert.
* **Poolauslastung**
Dieses Diagramm zeigt die Auslastung des Worker-Pools im Zeitverlauf. Wenn in diesem Diagramm routinemäßig die Auslastung des Workerpools angezeigt wird, sollten Sie einige Szenarien einem anderen Pool zuweisen.

  Wenn ein Pool sich der 100%igen Auslastung nähert, können andere Ressourcen, die denselben Pool verwenden, verzögert oder unterbrochen sein. In diesem Fall empfehlen wir, ein Szenario mit hoher Nutzung einem anderen Worker-Pool neu zuzuweisen oder vorhandene Szenarien zu ändern, damit sie weniger ressourcenintensiv sind.
* **Ausführungen pro Szenario**
Dieses Diagramm zeigt Ausführungen pro Szenario. Verschiedene Farben stellen verschiedene Szenarien dar. Wenn Sie den Mauszeiger über das Diagramm bewegen, wird ein Fenster angezeigt, das anzeigt, welche Farbe welches Szenario ist.

  Anhand dieses Diagramms können Sie feststellen, welche Szenarien möglicherweise einen Ausführungsrückstand oder eine hohe Auslastung des Worker-Pools verursachen.
* **Dauer der Ausführungen**
Dieses Diagramm zeigt Ausführungen pro Szenario. Verschiedene Farben stellen verschiedene Szenarien dar. Wenn Sie den Mauszeiger über das Diagramm bewegen, wird ein Fenster angezeigt, das anzeigt, welche Farbe welches Szenario ist.

  Sie können dieses Diagramm verwenden, um Szenarien zu identifizieren, die länger als üblich dauern, einschließlich der Szenarien, die von Problemen mit einer verbundenen App oder einem Service betroffen sind.

## Anzeigen des Fusion Insights-Dashboards

1. Klicken Sie in Fusion **linken** auf „Insights“.

   Das Dashboard wird geöffnet.

1. Um Daten für einen bestimmten Zeitpunkt anzuzeigen, bewegen Sie den Mauszeiger über ein Dashboard und passen Sie Ihren Cursor an den Zeitpunkt an, den Sie anzeigen möchten.

   In allen Diagrammen wird zu diesem Zeitpunkt eine Linie angezeigt, und in jedem Diagramm wird ein Fenster mit den Daten für diese Zeit angezeigt.
1. Um Daten für ein bestimmtes Szenario im Diagramm Ausführungen pro Szenario oder im Diagramm Dauer der Ausführungen anzuzeigen, klicken Sie auf einen Balken mit der Farbe für das Szenario, für das Sie Daten anzeigen möchten. Um zur Ansicht mit allen Szenarien zurückzukehren, klicken Sie erneut auf das Diagramm.
1. Um zu einem bestimmten Szenario zu wechseln, das im Diagramm Ausführungen pro Szenario oder im Diagramm Dauer der Ausführungen angezeigt wird, klicken Sie mit der rechten Maustaste auf einen Balken in der Farbe für das Szenario und wählen Sie **Szenario in neuer Registerkarte öffnen**.
1. Um ein Diagramm zu erweitern, klicken Sie auf **Erweitern** Symbol ![Erweitern](assets/expand-icon.png) in der rechten oberen Ecke des Diagramms.
1. Um den Zeitbereich des Dashboards zu ändern, klicken Sie in das Feld Zeitbereich in der oberen rechten Ecke des Dashboards und wählen Sie dann einen neuen Zeitrahmen aus. Der längste verfügbare Zeitraum beträgt 24 Stunden, der kürzeste 15 Minuten.
1. Um die Diagramme zu aktualisieren, klicken Sie auf das Aktualisierungssymbol oben rechts im Dashboard.
1. Um einen anderen Pool anzuzeigen, klicken Sie auf das Feld Pool in der oberen linken Ecke des Dashboards und wählen Sie dann den Pool aus, den Sie anzeigen möchten.

## Filtern und Speichern von Ausführungen im Ausführungsprotokoll

Verwenden Sie das Ausführungsprotokoll, um Szenario-Ausführungen zu finden, bei denen ein Fehler aufgetreten ist oder in Ihrer Organisation eine Warnung zurückgegeben wurde, und reaktivieren Sie alle Szenarien, die nach wiederholten Fehlern automatisch deaktiviert wurden.

1. Filtern Sie im Ausführungsprotokoll Ausführungen nach einem der folgenden Kriterien:

   * [!UICONTROL Team]
   * [!UICONTROL Szenario]
   * [!UICONTROL Ausführungstyp]
   * [!UICONTROL Datumsbereich]
   * [!UICONTROL Deaktivierungsstatus]
   * [!UICONTROL Fehlermeldung]

   Bei den meisten Filtern können Sie festlegen, dass nur die ausgewählten Werte oder alles außer ihnen übereinstimmen sollen.

1. Klicken Sie auf eine Ausführung, um weitere Details zu ihrem Fehler anzuzeigen.
1. Um ein oder mehrere Szenarien, die nach wiederholten Fehlern automatisch deaktiviert wurden, erneut zu aktivieren, wählen Sie die Ausführungen aus und klicken Sie dann auf **Aktivieren**.

   >[!NOTE]
   >
   >Untersuchen Sie vor der Reaktivierung eines Szenarios die Ursache der Fehler, z. B. abgelaufene Anmeldeinformationen oder ein Connector-Problem, damit das Szenario nicht sofort wieder fehlschlägt.
