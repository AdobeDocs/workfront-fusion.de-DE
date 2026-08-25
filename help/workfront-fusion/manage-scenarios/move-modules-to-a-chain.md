---
title: Module in eine Kette verschieben
description: Sie können eine Gruppe von Modulen in einem Szenario auswählen und sie in ein neues verkettetes Szenario verschieben, ohne Zuordnungen oder Datenstrukturen manuell neu zu erstellen.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: f1a80f64edc410ae76bfbba1280df7232e2d09c5
workflow-type: tm+mt
source-wordcount: 513
ht-degree: 17%

---

# Module in eine Kette verschieben

>[!IMPORTANT]
>
>Diese Funktion befindet sich in Beta und wird für geschäftskritische Produktions-Workflows nicht empfohlen. Als Beta-Funktion kann sich das Verhalten ändern, und Sonderfälle können möglicherweise nicht vollständig verarbeitet werden.

Sie können eine Gruppe von Modulen in einem Szenario auswählen und sie in ein neues verkettetes Szenario verschieben, ohne Zuordnungen oder Datenstrukturen manuell neu zu erstellen. Dies bietet eine einfache Möglichkeit, große Szenarien zu modularisieren.

Wenn Sie eine Gruppe von Modulen in eine Kette verschieben, führt Workfront Fusion Folgendes aus:

* Verschiebt die ausgewählten Module in eine neu erstellte Vorlage.
* Öffnet das neue Szenario in einem separaten Browser-Fenster.
* Ersetzt die ausgewählten Module im ursprünglichen Szenario durch ein Modul Kette > Untergeordnetes Szenario aufrufen .
* erstellt automatisch die Eingabe- und Ausgabedatenstrukturen, die für das neue untergeordnete Szenario erforderlich sind.
* behält das vorhandene Szenario-Verhalten bei, sodass das Szenario weiterhin auf die gleiche Weise ausgeführt wird wie vor dem Verschieben der Module.
* Aktualisiert automatisch Zuordnungen:
  * Module, die in das untergeordnete Szenario verschoben werden, empfangen Daten über die Kette > Daten von den Eingaben des übergeordneten Moduls.
  * Die Ausgaben des untergeordneten Szenarios werden automatisch dem übergeordneten Szenario zurückgegeben.
  * Vorhandene Zuordnungen im Blueprint werden an die neue Struktur angepasst.

Informationen zur Planung von verketteten Szenarien finden Sie unter [Verketten mehrerer Szenarien](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

Anweisungen zum Konfigurieren von Kettenmodulen finden Sie unter [Kettenmodule](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

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

## Voraussetzungen

Die Module, die Sie in eine Kette verschieben möchten, müssen bereits in einem Szenario vorhanden sein, und Sie müssen mehr als ein Modul auswählen.

## Einschränkungen

In den folgenden Situationen können Sie eine Auswahl von Modulen nicht in eine Kette verschieben:

* Die ausgewählten Module sind nicht Teil eines einzigen, ununterbrochenen Flusses. Sie können beispielsweise nicht gleichzeitig Module aus zwei verschiedenen, nicht verbundenen Routen auswählen.
* Die Auswahl enthält ein Webhook-Modul.
* Die Auswahl umfasst ein weiteres Kettenmodul.
* Die Auswahl umfasst ein Router-Modul, und Sie haben nicht alle Routen dieses Routers ausgewählt.
* Ein ausgewähltes Modul hat eine Fehler-Handler-Route, und Sie haben diese Route nicht ebenfalls ausgewählt.

## Module in eine Kette verschieben

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, das die Module enthält, die Sie verschieben möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Wählen Sie die Module aus, die Sie in eine Kette verschieben möchten, indem Sie [!UICONTROL Umschalt] gedrückt halten und auf die Module klicken, die Sie verschieben möchten.
1. Klicken Sie mit der rechten Maustaste auf eines der ausgewählten Module.
1. Wählen Sie **[!UICONTROL In Kette verschieben]** aus.
