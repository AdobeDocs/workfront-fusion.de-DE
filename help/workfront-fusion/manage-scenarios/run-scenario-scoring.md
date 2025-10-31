---
title: Ausführen des Szenario-Scoring-Experten
description: Der Szenario-Scoring-Experte kann Ihnen dabei helfen sicherzustellen, dass Ihr Szenario so konfiguriert ist, dass es den Best Practices entspricht. Er prüft Ihr Szenario und gibt Empfehlungen für dessen Struktur und Organisation.
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Ausführen des Szenario-Scoring-Experten

>[!IMPORTANT]
>
>Der Experte für Szenario-Bewertung wurde vorübergehend deaktiviert.

Der Szenario-Scoring-Experte kann Ihnen dabei helfen sicherzustellen, dass Ihr Szenario so konfiguriert ist, dass es den Best Practices entspricht. Er prüft Ihr Szenario und gibt Empfehlungen für dessen Struktur und Organisation.

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

## Ausführen des Szenario-Scoring-Experten

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie den Szenario-Scoring-Experten ausführen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf das Symbol „Szenario![Bewertungsexperte](assets/scoring-expert-icon.png) unten im Bildschirm.

   Das Expertengremium für Szenario-Bewertung wird geöffnet.
1. Klicken Sie **Auswerten**.

Der Szenario-Scoring-Experte gibt einen Score von 10 zurück und zeigt an, welche Prüfungen bestanden oder fehlgeschlagen sind. Wenn eine Prüfung fehlgeschlagen ist, gibt der Szenario-Scoring-Experte Empfehlungen, wie sichergestellt werden kann, dass das Szenario diese Prüfungen erfüllt.

![Szenario-Bewertung](assets/scenario-score.png)

## Szenario-Scoring-Prüfungen

Der Szenario-Scoring-Experte verwendet die folgenden Prüfungen:

* Das Szenario muss benannt werden.
* Alle Module müssen beschriftet sein.
* Das Szenario muss nach einem festgelegten Zeitplan ausgeführt werden.

  Anweisungen finden Sie unter [Planen eines Szenarios](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
* Die Größe des Szenario-Blueprints muss unter 5 MB liegen.

  Weitere Informationen finden Sie unter [Leistungs-Schutzmechanismen von Fusion](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#scenarios).
* Wenn ein Workfront Instant Trigger-Modul verwendet wird, muss es gefiltert werden.

  Anweisungen finden Sie unter [Ereignisabonnementfilter im Modul Workfront > [!UICONTROL Ereignisse ]](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules).
