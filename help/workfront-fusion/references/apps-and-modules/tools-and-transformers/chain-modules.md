---
title: Kettenmodule
description: Mithilfe dieser Module können Sie Szenarien verketten und einen Aufruf ausführen.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
exl-id: 21429f94-fe4c-4ccc-a8c0-d7573657fecc
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 1%

---

# Kettenmodule

Mithilfe der Kettenmodule können Sie ein Szenario mit einem anderen verbinden.

<!--This article will be about the specific module configuration-->

Anweisungen zum Planen von verketteten Szenarien finden Sie unter [Verketten mehrerer Szenarien](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).


## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Kettenmodule und ihre Felder

### Trigger

#### Daten von übergeordneter Seite empfangen

Dieses Trigger ist das Modulmodul im untergeordneten Szenario und wird durch das Modul „Untergeordnetes Szenario aufrufen“ im übergeordneten Szenario ausgelöst. Es empfängt Daten vom übergeordneten Szenario, die im untergeordneten Szenario verarbeitet werden können.

So konfigurieren Sie den Empfang von Daten aus dem übergeordneten Modul:

1. Um eine vorhandene Datenstruktur zu verwenden, wählen Sie im Feld Datenstruktur die Datenstruktur aus, die für die Eingabedaten des Szenarios verwendet werden soll.

   Oder

   Um eine neue Datenstruktur zu erstellen, die als Eingabedaten des Szenarios verwendet werden soll, klicken Sie auf **Hinzufügen** neben dem Feld „Datenstruktur“ und erstellen Sie die Datenstruktur.

   Anweisungen zum Erstellen einer Datenstruktur finden Sie unter [Datenstrukturen](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Klicken Sie **OK**, um das Modul zu speichern.

### Aktionen

#### Untergeordnetes Szenario aufrufen

Dieses Modul befindet sich im übergeordneten Szenario. Die Felder spiegeln die Datenstruktur wider, die im untergeordneten Szenario im Feld Daten vom übergeordneten Modul empfangen festgelegt ist.

>[!NOTE]
>
>* Sie können über dieses Modul ein vorhandenes untergeordnetes Szenario auswählen oder ein neues erstellen.
>* Sie können die Datenstruktur beim Erstellen eines untergeordneten Szenarios erstellen.

So konfigurieren Sie das Modul „Untergeordnetes Szenario aufrufen“

1. Fügen Sie Ihrem Szenario das Modul Untergeordnetes Szenario aufrufen hinzu.
1. Um ein vorhandenes untergeordnetes Szenario zu verwenden, wählen Sie im Feld Kette das untergeordnete Szenario aus, das Sie aufrufen möchten.

   Oder

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

Wenn Ihr untergeordnetes Szenario mehrere Routen hat, empfehlen wir, dieses Modul zu einer Route hinzuzufügen, die immer nach einer anderen Route ausgeführt wird.

So konfigurieren Sie das Modul Responder hinzufügen:

1. Um eine vorhandene Datenstruktur zu verwenden, wählen Sie im Feld Datenstruktur die Datenstruktur aus, die für die Daten verwendet wird, die das untergeordnete Szenario an das übergeordnete Szenario zurückgibt.

   Oder

   Um eine neue Datenstruktur für die Daten zu erstellen, klicken Sie **Hinzufügen** neben dem Feld Datenstruktur und erstellen Sie die Datenstruktur.

   Anweisungen zum Erstellen einer Datenstruktur finden Sie unter [Datenstrukturen](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Klicken Sie **OK**, um das Modul zu speichern.
