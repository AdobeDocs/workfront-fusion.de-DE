---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Verwalten gesperrter Szenarios
description: Verwalten gesperrter Szenarien in Adobe Workfront Fusion
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
TQID: https://experienceleague.adobe.com/1eVGWr4SwutYzNmCKB62CCWbQ6ExdXtpjC5BORh-kxo
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 29%

---

# Verwalten gesperrter Szenarios

In einigen Fällen kann ein Szenario vorübergehend in Workfront Fusion gesperrt sein. Gesperrte Szenarien werden innerhalb von 2-4 Stunden automatisch entsperrt. Sie können Szenarien manuell entsperren. Dies wird jedoch im Allgemeinen nicht empfohlen.

Szenarien können aus verschiedenen Gründen gesperrt werden:

* Workfront Fusion unterstützt keine parallele Verarbeitung geplanter Szenarien. Diese Szenarien werden zu Beginn der Szenarioausführung gesperrt und nach Abschluss entsperrt. Wenn die Ausführung unterbrochen wird, kann es sein, dass sich das Szenario nicht entsperrt. Dies kann vorkommen, wenn ein Benutzer das Szenario manuell forciert oder wenn ein Systemproblem vorliegt.

* Das Entwicklungsteam von Workfront Fusion kann ein Szenario sperren, da es Leistungs- oder andere Probleme verursacht.

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
