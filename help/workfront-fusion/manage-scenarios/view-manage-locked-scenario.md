---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Gesperrte Szenarien verwalten
description: Verwalten gesperrter Szenarien in Adobe Workfront Fusion
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 1%

---

# Gesperrte Szenarien verwalten

In einigen Fällen kann ein Szenario vorübergehend in Workfront Fusion gesperrt sein. Gesperrte Szenarien werden innerhalb von 2-4 Stunden automatisch entsperrt. Sie können Szenarien manuell entsperren. Dies wird jedoch im Allgemeinen nicht empfohlen.

Szenarien können aus verschiedenen Gründen gesperrt werden:

* Workfront Fusion unterstützt keine parallele Verarbeitung geplanter Szenarien. Diese Szenarien werden zu Beginn der Szenarioausführung gesperrt und nach Abschluss entsperrt. Wenn die Ausführung unterbrochen wird, kann es sein, dass sich das Szenario nicht entsperrt. Dies kann vorkommen, wenn ein Benutzer das Szenario manuell forciert oder wenn ein Systemproblem vorliegt.

* Das Entwicklungsteam von Workfront Fusion kann ein Szenario sperren, da es Leistungs- oder andere Probleme verursacht.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz</td> 
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Plan für [!UICONTROL Select] oder [!UICONTROL Prime] Workfront: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>[!UICONTROL Ultimate] Workfront-Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Unternehmen sein.</p>
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Team sein.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
