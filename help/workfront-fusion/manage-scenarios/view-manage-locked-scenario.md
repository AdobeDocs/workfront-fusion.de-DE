---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Gesperrte Szenarien verwalten
description: Verwalten gesperrter Szenarien in [!DNL Adobe Workfront Fusion]
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# Gesperrte Szenarien verwalten

In einigen Fällen kann ein Szenario vorübergehend in [!DNL Workfront Fusion] gesperrt sein. Gesperrte Szenarien werden innerhalb von 2-4 Stunden automatisch entsperrt. Sie können Szenarien manuell entsperren. Dies wird jedoch im Allgemeinen nicht empfohlen.

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
   <td role="rowheader">[!DNL Adobe Workfront] Packstück</td> 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz</td> 
   <td> <p>Neu: [!UICONTROL Standard]</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuell: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>[!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Workfront]: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein [!DNL Workfront Fusion]-Administrator für Ihre Organisation sein.</p>
     <p>Sie müssen [!DNL Workfront Fusion] für Ihr Team sein.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++


## Entsperren eines gesperrten Szenarios

Gesperrte Szenarien werden 2-4 Stunden nach dem Zeitpunkt entsperrt, zu dem sie gesperrt wurden. Sie können ein Szenario manuell entsperren, bevor es so geplant ist, dass es automatisch entsperrt wird.

>[!WARNING]
>
>Das manuelle Entsperren eines Szenarios kann zu Fehlern bei der Ausführung eines Szenarios führen. Es wird empfohlen, Szenarien nur manuell zu entsperren, wenn ein Szenario gesperrt ist, da Ausführungen ausgeführt und gestoppt werden. Dies ist Teil des Entwurfs des Szenarios. In anderen Fällen empfehlen wir, zu warten, bis das Szenario automatisch entsperrt wird.


So entsperren Sie ein gesperrtes Szenario manuell:

1. Gehen Sie zur Seite mit den Szenario-Details des gesperrten Szenarios.
1. Klicken Sie oben rechts im Bildschirm auf **[!UICONTROL Options]** .
1. Wählen Sie **[!UICONTROL Unlock execution]** aus.
1. Klicken Sie auf **[!UICONTROL Unlock]**.
   ![](assets/unlock-scenario.png)
