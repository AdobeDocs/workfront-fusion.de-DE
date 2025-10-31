---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Gesperrte Szenarien verwalten
description: Verwalten gesperrter Szenarien in Adobe Workfront Fusion
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# Gesperrte Szenarien verwalten

In einigen Fällen kann ein Szenario vorübergehend in Workfront Fusion gesperrt sein. Gesperrte Szenarien werden innerhalb von 2-4 Stunden automatisch entsperrt. Sie können Szenarien manuell entsperren. Dies wird jedoch im Allgemeinen nicht empfohlen.

Szenarien können aus verschiedenen Gründen gesperrt werden:

* Workfront Fusion unterstützt keine parallele Verarbeitung geplanter Szenarien. Diese Szenarien werden zu Beginn der Szenarioausführung gesperrt und nach Abschluss entsperrt. Wenn die Ausführung unterbrochen wird, kann es sein, dass sich das Szenario nicht entsperrt. Dies kann vorkommen, wenn ein Benutzer das Szenario manuell forciert oder wenn ein Systemproblem vorliegt.

* Das Entwicklungsteam von Workfront Fusion kann ein Szenario sperren, da es Leistungs- oder andere Probleme verursacht.

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

## Entsperren eines gesperrten Szenarios

Gesperrte Szenarien werden 2-4 Stunden nach dem Zeitpunkt entsperrt, zu dem sie gesperrt wurden. Sie können ein Szenario manuell entsperren, bevor es so geplant ist, dass es automatisch entsperrt wird.

>[!WARNING]
>
>Das manuelle Entsperren eines Szenarios kann zu Fehlern bei der Ausführung eines Szenarios führen. Es wird empfohlen, Szenarien nur manuell zu entsperren, wenn ein Szenario gesperrt ist, da Ausführungen ausgeführt und gestoppt werden. Dies ist Teil des Entwurfs des Szenarios. In anderen Fällen empfehlen wir, zu warten, bis das Szenario automatisch entsperrt wird.


So entsperren Sie ein gesperrtes Szenario manuell:

1. Gehen Sie zur Seite mit den Szenario-Details des gesperrten Szenarios.
1. Klicken Sie **[!UICONTROL Optionen]** in der oberen rechten Ecke des Bildschirms.
1. Wählen Sie **[!UICONTROL Ausführung entsperren]**.
1. Klicken Sie **[!UICONTROL Entsperren]**.
   ![Szenario entsperren](assets/unlock-scenario.png)
