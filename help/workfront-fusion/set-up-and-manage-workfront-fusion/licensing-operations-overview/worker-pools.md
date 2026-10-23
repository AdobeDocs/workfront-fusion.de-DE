---
title: Arbeitspools
description: Ein Worker-Pool ist eine Menge an Workfront Fusion-Verarbeitungsressourcen, die einer oder mehreren bestimmten Organisationen zugewiesen ist. Alle Fusion-Vorgänge und -Verarbeitungen erfolgen im Kontext des zugewiesenen Worker-Pools einer Organisation.
author: Becky
feature: Workfront Fusion
exl-id: 8bf508a8-d1f9-455f-af89-62f688289137
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: b800142d824927e5765eed50a831731e6b5d9925
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 19%
---
# Arbeitskräftepools

Ein Worker-Pool ist eine Menge an Workfront Fusion-Verarbeitungsressourcen, die einer bestimmten Organisation zugewiesen ist. Alle Fusion-Vorgänge und -Verarbeitungen erfolgen im Kontext des zugewiesenen Worker-Pools einer Organisation.

Worker-Pools ermöglichen eine effizientere Ausführung Ihrer Szenarien und verhindern die Möglichkeit, mit anderen Organisationen um die Verarbeitungskapazität von Fusion zu konkurrieren.

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

## Übersicht über den Worker-Pool

Ein Worker-Pool ist eine Möglichkeit, Szenario-Ausführungen parallel zu verarbeiten. Jeder Worker-Pool ist verknüpft mit:

* Eine Reihe von Arbeitnehmern.
* Eine Ausführungswarteschlange.

Wenn ein Szenario ausgeführt wird, wird es in die Ausführungswarteschlange des Arbeitspools übergeben. Worker im Pool rufen Aufgaben kontinuierlich aus dem Ausführungspool ab und verarbeiten sie parallel.

Wenn die Ausführungswarteschlangentiefe zunimmt und alle vorhandenen Sekundäre verwendet werden, skaliert Workfront Fusion den Pool automatisch, indem weitere Sekundäre hinzugefügt werden. Diese Skalierung ist dynamisch und ereignisgesteuert, d. h. die Kapazität entspricht exakten oder Verträgen, die auf Echtzeitlasten basieren, ohne dass Sie oder Ihr Unternehmen Maßnahmen ergreifen.

Das Workfront Fusion-Team überwacht kontinuierlich die Nutzung und das Skalierungsverhalten von Pools und kann Schwellenwerte oder Muster überprüfen, um eine konsistente Leistung bei wachsender Nutzung sicherzustellen.

## Umbenennen eines Worker-Pools

Organisationsverantwortliche und -administrierende können die ihrer Organisation zugewiesenen Worker-Pools umbenennen. Jeder Pool zeigt standardmäßig einen vom System generierten Namen an. Sie können einem Pool einen benutzerdefinierten Namen geben, z. B. `Marketing EU` oder `High-volume integrations`, und ihn bei Bedarf ändern.

Das Umbenennen eines Pools ändert nur die Beschriftung. Szenarien, Ausführungen und Pool-Kapazität sind davon nicht betroffen. Der neue Name wird überall dort angezeigt, wo der Pool angezeigt wird, z. B. wenn Sie einem Pool Szenarien zuweisen.

>[!NOTE]
>
>Die **[!UICONTROL Worker-Pools]** wird nur angezeigt, wenn Ihrer Organisation mehr als ein Worker-Pool zugewiesen ist. Wenn Ihr Unternehmen über einen einzigen Worker-Pool verfügt oder den gemeinsamen Pool verwendet, wird die Registerkarte nicht angezeigt.

So benennen Sie einen Worker-Pool um:

1. Klicken Sie in der linken Navigation auf **Organisationsübersicht**
1. Klicken Sie auf **[!UICONTROL Registerkarte]** Worker-Pools“ oben auf der Seite.

   Auf der Registerkarte werden die einzelnen Pools aufgelistet und angezeigt, wie viele Szenarien ihnen zugewiesen sind.

1. Klicken Sie **[!UICONTROL Umbenennen]** neben dem Pool, den Sie umbenennen möchten.
1. Geben Sie in dem sich öffnenden Bedienfeld den neuen Namen ein.
1. Klicken Sie auf **Speichern**.
