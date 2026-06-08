---
title: Kettenmodule
description: Mithilfe dieser Module können Sie Szenarien verketten und einen Aufruf ausführen.
author: Becky
feature: Workfront Fusion
exl-id: 21429f94-fe4c-4ccc-a8c0-d7573657fecc
TQID: https://experienceleague.adobe.com/AlHUrliXikCc3OVHiBTjLNQFndCf5qLzOLuBvnDTUfA
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 81d1dfcdb5c15f6a93e2793f9a0e41821b65c7e3
workflow-type: tm+mt
source-wordcount: 883
ht-degree: 10%

---

# Kettenmodule

>[!IMPORTANT]
>
>Diese Funktion befindet sich in Beta und wird für geschäftskritische Produktions-Workflows nicht empfohlen. Als Beta-Funktion kann sich das Verhalten ändern, und Sonderfälle können möglicherweise nicht vollständig verarbeitet werden.
>
>Für stabile Integrationen sollten Sie erwägen, ein zweites Szenario über einen Webhook mit einem HTTP-Anfrage-Modul auszulösen. Dieses Muster verwendet vollständig unterstützte Primitive und bietet jedem Szenario eine unabhängige Ausführungskontrolle.
>
>Wenn Sie verkettete Szenarien verwenden möchten, lesen Sie [Verketten mehrerer Szenarien miteinander](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md) um Entwurfsanleitungen zu erhalten.

Mithilfe der Kettenmodule können Sie ein Szenario mit einem anderen verbinden.

<!--This article will be about the specific module configuration-->

Anweisungen zum Planen von verketteten Szenarien finden Sie unter [Verketten mehrerer Szenarien](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).


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
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Kettenmodule und ihre Felder

### Auslöser

#### Daten von übergeordneter Seite empfangen

Dieses Trigger ist das Modulmodul im untergeordneten Szenario und wird durch das Modul „Untergeordnetes Szenario aufrufen“ im übergeordneten Szenario ausgelöst. Es empfängt Daten vom übergeordneten Szenario, die im untergeordneten Szenario verarbeitet werden können.

So konfigurieren Sie den Empfang von Daten aus dem übergeordneten Modul:

1. Um eine vorhandene Datenstruktur zu verwenden, wählen Sie im Feld Datenstruktur die Datenstruktur aus, die für die Eingabedaten des Szenarios verwendet werden soll.

   ODER

   Um eine neue Datenstruktur zu erstellen, die als Eingabedaten des Szenarios verwendet werden soll, klicken Sie auf **Hinzufügen** neben dem Feld „Datenstruktur“ und erstellen Sie die Datenstruktur.

   Anweisungen zum Erstellen einer Datenstruktur finden Sie unter [Datenstrukturen](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Klicken Sie **OK**, um das Modul zu speichern.

### Aktionen

#### Untergeordnetes Szenario aufrufen

Dieses Modul befindet sich im übergeordneten Szenario. Die Felder spiegeln die Datenstruktur wider, die im untergeordneten Szenario im Feld Daten vom übergeordneten Modul empfangen festgelegt ist.

>[!IMPORTANT]
>
> Überprüfen Sie Folgendes, bevor Sie dieses Modul in einem Produktionsszenario konfigurieren:
>
> * **Aktivieren Sie in diesem Szenario nicht &quot;Trigger zuletzt übertragen (CTL**, wenn „Auslösen und vergessen“ deaktiviert ist. Die CTL versucht es erneut, wenn sie auf eine untergeordnete Antwort wartet, wodurch eine unbegrenzte Wiederholungsschleife entsteht.
> * **Verwenden Sie beim Platzieren dieses Moduls in einem Iterator Vorsicht.** Wenn Sie in einem großen Iterator für jedes Element ein untergeordnetes Szenario bereitstellen, wird die Plattform erheblich ausgelastet. Erwägen Sie, die Logik des untergeordneten Szenarios einzubinden oder freigegebene Suchen außerhalb des Iterators vorab zu berechnen.
> * **Feuer und Vergessen** bedeutet, dass das Elternteil keine Sicht darauf hat, ob das Kind gelaufen ist oder erfolgreich war. Verwenden Sie diese Option nur, wenn Kinderfehler unabhängig überwacht werden.
>
> Eine vollständige Entwurfsanleitung finden Sie unter [Verketten mehrerer Szenarien](https://experienceleague.adobe.com/en/docs/workfront-fusion/using/create-scenarios/plan-a-scenario/chain-scenarios).

>[!NOTE]
>
>* Sie können über dieses Modul ein vorhandenes untergeordnetes Szenario auswählen oder ein neues erstellen.
>* Sie können die Datenstruktur beim Erstellen eines untergeordneten Szenarios erstellen.

So konfigurieren Sie das Modul „Untergeordnetes Szenario aufrufen“

1. Fügen Sie Ihrem Szenario das Modul Untergeordnetes Szenario aufrufen hinzu.
1. Um ein vorhandenes untergeordnetes Szenario zu verwenden, wählen Sie im Feld Kette das untergeordnete Szenario aus, das Sie aufrufen möchten.

   ODER

   Um ein neues untergeordnetes Szenario zu erstellen, klicken Sie auf Hinzufügen neben dem Feld Kette . Das untergeordnete Szenario wird in einem separaten Fenster angezeigt, in dem die Empfängerdaten von übergeordneten Modulen und die Rückgabeantwort von übergeordneten Modulen vorhanden sind.

   Die im Trigger -Modul des untergeordneten Szenarios konfigurierten Felder werden im Modul „Untergeordnetes Szenario aufrufen“ angezeigt.

1. Geben Sie die Informationen, die an das untergeordnete Szenario übergeben werden sollen, in das Modul „Untergeordnetes Szenario aufrufen“ ein oder mappen Sie es.
1. (Bedingt) Wenn Sie möchten, dass das übergeordnete Szenario seine Ausführung fortsetzt, ohne auf eine Antwort des untergeordneten Szenarios zu warten, aktivieren Sie die Option **Auslösen und vergessen** .
1. Klicken Sie **OK**, um das Modul zu speichern.

>[!NOTE]
>
>Wenn Sie ein neues untergeordnetes Szenario für dieses Modul erstellen, wird das untergeordnete Szenario in einem separaten Browser-Fenster geöffnet, in dem Sie sowohl das übergeordnete als auch das untergeordnete Szenario gleichzeitig anzeigen und konfigurieren können.

#### Antwort an übergeordnetes Element zurückgeben

Dies ist das untergeordnete Szenario und sendet Daten in der ausgewählten Struktur an das übergeordnete Szenario. Sie können diese Daten in späteren Modulen im übergeordneten Szenario zuordnen.

>[!IMPORTANT]
>
> Wenn Ihr untergeordnetes Szenario mehrere Routen hat, müssen **sicherstellen** dass die Antwort an das übergeordnete Modul von jedem Ausführungspfad aus erreichbar ist. Wenn sich das Modul Antwort zurückgeben auf einer Route befindet, die übersprungen oder nicht ausgeführt wird, wartet das übergeordnete Szenario auf unbestimmte Zeit auf eine Antwort, die nie eintrifft.
>
> Fügen Sie die Antwort zum Zurückkehren zum übergeordneten Modul nach dem Router auf einer Route hinzu, die unabhängig vom Ergebnis des Routers immer ausgeführt wird, oder fügen Sie Fehlerbehandlung hinzu, um sicherzustellen, dass eine Antwort immer zurückgegeben wird, auch wenn ein Fehler auftritt.

So konfigurieren Sie das Modul Responder hinzufügen:

1. Um eine vorhandene Datenstruktur zu verwenden, wählen Sie im Feld Datenstruktur die Datenstruktur aus, die für die Daten verwendet wird, die das untergeordnete Szenario an das übergeordnete Szenario zurückgibt.

   ODER

   Um eine neue Datenstruktur für die Daten zu erstellen, klicken Sie **Hinzufügen** neben dem Feld Datenstruktur und erstellen Sie die Datenstruktur.

   Anweisungen zum Erstellen einer Datenstruktur finden Sie unter [Datenstrukturen](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Klicken Sie **OK**, um das Modul zu speichern.
