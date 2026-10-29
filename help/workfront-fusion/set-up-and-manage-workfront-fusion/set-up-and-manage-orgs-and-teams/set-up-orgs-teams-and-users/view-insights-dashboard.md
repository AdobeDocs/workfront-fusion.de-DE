---
title: Anzeigen des Insights-Dashboards für eine Organisation
description: Fusion-Administratoren können ein Dashboard anzeigen, das Ausführungsmetriken für eine Organisation anzeigt.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: 'https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 45c755a2f6152b6e230864e4c840d0334705bd22
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 3%
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
* **Organisationsvorgänge**
In diesem Diagramm können Sie die Anzahl der in Ihrer Organisation verwendeten Vorgänge anzeigen. Sie können bestimmte Teams oder Szenarien auswählen und Vorgänge in der letzten Woche, im letzten Monat oder im letzten Jahr anzeigen.
* **Top-Szenarien nach Vorgängen**
In diesem Diagramm können Sie sehen, welche Szenarien die meisten Vorgänge verwenden. Sie können bestimmte Teams auswählen oder Daten des letzten Tages, der letzten Woche oder des letzten Monats anzeigen.

<!--

* **Executions waiting to be processed**
   This chart shows the number of executions waiting to be processed (also known as the execution backlog) at a given point in time. 

   A high number of executions waiting to be processed may affect performance in your Fusion instance. You will receive a notification if your execution backlog reaches 5000 executions. We recommend identifying responsible scenarios and modifying or disabling them. If the high execution backlog persists, the Fusion team will protect the performance of your Fusion instance by disabling the responsible scenarios.
* **Pool Utilization**
   This chart shows worker pool utilization over time. If this chart routinely shows worker pool utilization, you may want to assign some scenarios to another pool.

   If a pool is nearing 100% utilization, other resources that use the same pool may be delayed or disrupted. If this occurs, we recommend reassigning a high-usage scenario to another worker pool, or modifying existing scenarios to be less resource intensive.
* **Executions per scenario**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify which scenarios may be causing an execution backlog or high worker pool utilization. 
* **Duration of executions**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify scenarios that are taking longer than usual, including those affected by issues with a connected app or service.

-->

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

## Anpassen des Insights-Dashboards

Sie können auswählen, welche Widgets in welcher Reihenfolge im Insights-Dashboard angezeigt werden.

### Widgets hinzufügen, entfernen oder neu anordnen

1. Klicken Sie in der linken Navigation auf **Insights** ![Insights-Symbol](assets/insights-icon.png).
1. Klicken Sie **[!UICONTROL der Insights]** Kopfzeile auf „Anpassen“.

   Ein Seitenbereich wird geöffnet. Sie listet jedes Widget als Karte auf, die eine Vorschau, den Widget-Namen und eine Beschreibung anzeigt.

1. Um ein Widget ein- oder auszublenden, klicken Sie auf seine Karte oder auf die Schaltfläche **[!UICONTROL Widget hinzufügen]** oder **[!UICONTROL Widget entfernen]** auf der Karte.

   Angezeigte Widgets sind mit einem Häkchen versehen.
1. Um Widgets neu anzuordnen, ziehen Sie eine Widget-Karte an eine neue Position im Bedienfeld.

   Ein gestrichelter Platzhalter und eine Ablageleiste zeigen an, wo die Karte landen wird.

Ihre Auswahl wird pro Browser gespeichert. Widgets, die in späteren Versionen hinzugefügt werden, werden automatisch im Bedienfeld angezeigt.

Wenn Sie alle Widgets entfernen, zeigt die Seite die Meldung „Keine Widgets auf dieser Seite“ an.

## Aktualisieren des Insights-Dashboards

Um die Daten jedes Widgets neu zu laden, klicken Sie auf **[!UICONTROL Aktualisieren]** neben **[!UICONTROL Anpassen]**.

* Jedes Widget behält seine Filter bei.
* Die Schaltfläche **[!UICONTROL Aktualisieren]** zeigt den Status „Ausstehend“ an, bis alle Widgets vollständig geladen sind.
* Diagramme behalten das vorherige Diagramm unter einem Ladeschleuderrad, und das Ausführungsprotokoll dimmt seine Tabelle unter einem Schleuderrad, während die Daten neu geladen werden.
* Wenn eine Aktualisierung fehlschlägt, behalten Widgets ihre letzten guten Daten bei.

## Take the Insights-Tour

Beim ersten Öffnen des Insights-Dashboards erhalten Sie über ein Begrüßungsdialogfeld die Möglichkeit, eine Tour zu starten oder zu überspringen.

Die Tour zeigt die einzelnen Widgets in Ihrer gespeicherten Reihenfolge sowie die Schaltfläche **[!UICONTROL Anpassen]** und das Bedienfeld, die Schaltfläche **[!UICONTROL Aktualisieren]** und die Schaltfläche **[!UICONTROL Wiederholen]** in der Titelleiste.

Um die Tour jederzeit neu zu starten, klicken Sie auf das Informationssymbol ![Informationssymbol](assets/insights-tour-information.png) in der Titelleiste.

Die Tour beginnt nicht, wenn Sie das Insights-Dashboard über einen Link in einem Szenario öffnen. Weitere Informationen finden Sie unter [Öffnen des Insights-Dashboards aus einem Szenario](#open-the-insights-dashboard-from-a-scenario) in diesem Artikel.

## Nach Szenarien und Teams anhand der ID suchen

In den Widgets **[!UICONTROL Organisationsvorgänge]** und **[!UICONTROL Top-Szenarien nach]**) entsprechen die Felder **[!UICONTROL Szenario]** und **[!UICONTROL Team]** in Bezug auf die ID sowie den Namen. Jede Option zeigt ihre ID unter dem Namen an, z. B. „ID 123“.

* In den Listen werden die ersten 500 Szenarien und die ersten 200 Teams geladen. Wenn Sie eine ID eingeben, die sich nicht in der geladenen Liste befindet, sucht Fusion diese nach kurzer Verzögerung automatisch.
* Wenn Sie ein Szenario löschen, wird auch das Team gelöscht, das automatisch für dieses Szenario ausgefüllt wurde.

>[!NOTE]
>
>Der Szenariofilter im Ausführungsprotokoll stimmt nicht mit der ID überein.

## Öffnen des Insights-Dashboards aus einem Szenario heraus

Sie können das Insights-Dashboard mit dem Widget **[!UICONTROL Organisationsvorgänge]** öffnen, das nach einem bestimmten Szenario und Team gefiltert wurde.

So gehen Sie von einem Szenario aus zur Insights-Seite:

1. Öffnen Sie die Seite mit den Szenario-Details:

   1. Klicken Sie **[!UICONTROL linken Panel auf]** Registerkarte „Szenario“ und dann auf ein Szenario, zu dem Sie Details anzeigen möchten.

      ODER

      Wenn Sie an dem Szenario im Szenario-Editor arbeiten, klicken Sie auf den Pfeil nach links ![Beenden der Bearbeitung](assets/exit-editing-arrow.png) in der oberen linken Ecke des Fensters.
      1. Klicken Sie auf **Registerkarte** Berichte“ oben auf der Seite.

* Das Widget **[!UICONTROL Organisationsvorgänge]** wird gefiltert für dieses Szenario und Team geöffnet und die Seite scrollt zum Widget.
* Wenn Sie das Widget von der Seite entfernt haben, wird stattdessen eine Warnung mit der Schaltfläche **[!UICONTROL Widget hinzufügen]** angezeigt.

## Verwenden des dunklen Modus

Das Insights-Dashboard und seine Widgets folgen automatisch Ihrer Einstellung für den Dunkelmodus. Wenn Sie die Einstellung ändern, wird die Seite sofort aktualisiert, ohne dass sie neu geladen wird, und der aktuelle Status bleibt erhalten. Der Lichtmodus bleibt unverändert.

## Zugriff auf Leistungs-Widgets

Das **[!UICONTROL Performance]**-Widget wird nur Benutzern angezeigt, die über eine der folgenden Berechtigungen verfügen:

* Organisation in der aktiven Organisation bearbeiten
* Organisationsansicht auf der Admin-Seite

Das Widget wird auf der Seite und im Bedienfeld **[!UICONTROL Anpassen]** für andere Benutzer ausgeblendet. Wenn Benutzenden später Zugriff gewährt wird, kehrt das Widget an seiner gespeicherten Position zurück. Das direkte Öffnen der Insights-URL umgeht diese Prüfung nicht.

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
