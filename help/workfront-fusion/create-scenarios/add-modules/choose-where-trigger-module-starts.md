---
title: Startseite eines Trigger-Moduls auswählen
description: Bei einigen Trigger-Modulen können Sie das erste Bundle auswählen, von dem aus das Abrufen von Bundles beginnen soll.
author: Becky
feature: Workfront Fusion
exl-id: 83628fa5-82e2-4f67-bfed-70a4c3c19f7f
source-git-commit: 9ec972ef7677874965d6b4cb646e87c0b2240214
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%

---

# Startseite eines Trigger-Moduls auswählen

Bei einigen Trigger-Modulen können Sie das erste Bundle auswählen, von dem aus das Abrufen von Bundles beginnen soll.

Sie können auch angeben, ob Sie alle Bundles oder nur die Bundles von nach einem bestimmten Datum abrufen möchten.

Weitere Informationen zu Trigger-Modulen finden Sie im Abschnitt [Trigger-Module](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) im Artikel Module - Übersicht.

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
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Startseite eines Trigger-Moduls auswählen

1. Klicken Sie im linken Bedienfeld auf die Registerkarte **[!UICONTROL Scenarios]** .
1. Wählen Sie das Szenario aus, in dem Sie den Startpunkt des Triggers auswählen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Konfigurieren und speichern Sie ein Trigger-Modul.

   Oder

   Klicken Sie mit der rechten Maustaste auf das Symbol für das Modul Trigger und wählen Sie **Startpunkt auswählen**.

   ![](assets/choose-where-to-start.png)

1. Wählen Sie im angezeigten **[!UICONTROL Choose where to start]** eine Option aus.

   Die angezeigten Optionen hängen von den Möglichkeiten eines bestimmten Service ab. Sie können Folgendes umfassen:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody>
    <tr>
    <td>[!UICONTROL From now on] (Standard)</td>
    <td>Ruft alle hinzugefügten oder aktualisierten Bundles (abhängig von Einstellungen) ab, nachdem diese Option ausgewählt wurde</td>
    </tr>
     <tr>
    <td>[!UICONTROL Since specific date]</td>
    <td>Ruft alle hinzugefügten oder aktualisierten Bundles (je nach Einstellungen) nach einem bestimmten Datum und zu einer bestimmten Uhrzeit ab</td>
      </tr>
      <tr>
    <td>[!UICONTROL All]</td>
    <td>Ruft alle verfügbaren Bundles ab</td>
     </tr>
      <tr>
    <td>[!UICONTROL Choose manually]</td>
    <td>Ermöglicht die Auswahl des ersten Bundles, von dem aus der Abruf der Bundles beginnen soll</td>
     </tr>
     </tbody>
   </table>



   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Einen Namen für die neue [!DNL DocuSign] eingeben</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Account type]</td> 
      <td>Wählen Sie aus, ob das Konto, mit dem Sie eine Verbindung herstellen möchten, ein Produktionskonto oder ein Demokonto ist.</td> 
     </tr> 
    </tbody> 
   </table>


