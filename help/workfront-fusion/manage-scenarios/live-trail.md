---
title: Verwenden des Live-Protokolls zur Überprüfung einer Szenarioausführung
description: Das Live-Protokoll zeigt ein unmittelbar ausgeführtes Szenario, in dem Modulanfragen und Ausführungsaktivitäten in einer Liste kombiniert werden. Sie können die Anfrage- und Antwortdetails für jeden Vorgang öffnen.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 17%
---

# Verwenden des Live-Protokolls zur Überprüfung einer Szenarioausführung

Der Live-Trail zeigt ein laufendes Szenario. Es kombiniert Modulanfragen und Ausführungsaktivität in einer chronologischen Liste, sodass Sie eine Ausführung im Szenario-Editor verfolgen und sehen können, was schiefgelaufen ist, ohne die Arbeitsfläche zu verlassen.

>[!NOTE]
>
>Diese Funktion ist nur in der neuen Version des Szenario-Editors verfügbar. Weitere Informationen finden Sie unter [Neue und klassische Erlebnisse](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) im Artikel Szenario-Editor.

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Ein beliebiges Adobe Workfront Workflow- und Adobe Workfront Automation and Integration-Paket</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Live-Spur öffnen

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, das Sie überprüfen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Starten Sie eine Ausführung des Szenarios, z. B. durch Klicken auf &quot;**ausführen**.



Der Live-Pfad wird im Bedienfeld auf der rechten Seite der Arbeitsfläche geöffnet. Wenn Sie das Bedienfeld während eines Durchgangs schließen, können Sie es über eine kleine Registerkarte auf der rechten Seite des Bildschirms erneut öffnen, ohne die erfassten Ereignisse zu verlieren.

## Überprüfen von Ereignissen im Live-Protokoll

Das Live-Protokoll listet Modulanfragen auf und führt Aktivitäten in der Reihenfolge aus, in der sie auftreten. Sie haben folgende Möglichkeiten:

* Durchsuchen Sie die Liste.
* Filtern Sie die Liste nach Status.
* Folgt dem neuesten Ereignis während der Ausführung.
* Löscht die aktuelle Spur.

## Anfrage- und Antwortdetails anzeigen

1. Klicken Sie im Live-Protokoll auf die Anfrage, für die Sie Details anzeigen möchten.

   Das Modul, das die Anfrage gestellt hat, wird auf der Arbeitsfläche angezeigt, und die Anfrage- und Antwortdetails werden im Bedienfeld geöffnet.

1. Überprüfen Sie die Details. Die Detailansicht umfasst:

   * Navigation zwischen den Vorgängen des Moduls
   * Header und Hauptteil der Anfrage
   * Antwort-Header und Hauptteil

1. (Optional) Kopieren Sie die Details, um sie an anderer Stelle zu verwenden, indem Sie auf **Roh kopieren** oder **cURL kopieren** klicken:

   * Kopieren Sie einen Rohbericht der Anfrage und der Antwort.
   * Kopieren Sie einen cURL-Befehl für die Anfrage.

1. Um zur Liste zurückzukehren, klicken Sie auf den Rückwärtspfeil links oben im Bedienfeld.

## Stellen Sie sicher, dass Anfrage- und Antwortdetails verfügbar sind

Anfrage- und Antwortdetails werden nicht für jede geplante oder ausgelöste Ausführung gespeichert, da sie viel Speicher benötigen.

* Einmal ausführen speichert immer Anfrage- und Antwortdetails.
* Aktivieren Sie für die regulären Ausführungen eines Szenarios in den Szenario-Einstellungen temporäre Debug-Protokolle, bevor die Ausführungen ausgeführt werden, die Sie überprüfen möchten. Weitere Informationen finden Sie unter [Temporäre Debug-Protokolle](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs) im Artikel Konfigurieren von Szenario-Einstellungen.

Wenn Sie einen Durchlauf aus dem Ausführungsverlauf öffnen und der Bereich für Anfragen und Antworten keine Daten enthält, werden Sie zum Bereich für temporäre Debugging-Protokolle weitergeleitet.
