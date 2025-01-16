---
content-type: reference
title: Szenario planen
description: Standardmäßig wird ein Szenario alle 15 Minuten ausgeführt. Sie können dies ändern, indem Sie festlegen, wann und wie oft ein aktiviertes Szenario ausgeführt wird. Fusionsszenarien können so geplant werden, dass sie alle 5 Minuten ausgeführt werden.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Szenario planen

Standardmäßig wird ein Szenario alle 15 Minuten ausgeführt. Sie können dies ändern, indem Sie festlegen, wann und wie oft ein aktiviertes Szenario ausgeführt wird. Fusionsszenarien können so geplant werden, dass sie alle 5 Minuten ausgeführt werden.

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
   <p>Neu:</p> <ul><li>[!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Workfront] Plan: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] ist enthalten.</li></ul>
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

## Szenario planen

1. Klicken Sie auf **Registerkarte** Szenario“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, das Sie planen möchten.
1. Klicken Sie oben rechts auf der Seite mit den Szenario-Details auf **[!UICONTROL Options]** > **[!UICONTROL Scheduling]**

   Oder

   Klicken Sie auf das **[!UICONTROL Scheduling]** (Uhr) im Trigger-Modul des Szenarios.

1. Geben Sie Informationen in die folgenden Felder ein:

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Run scenario]</td> 
      <td> <p>Wählen Sie die Häufigkeit aus, mit der Sie das Szenario ausführen möchten, und wählen Sie dann das Intervall aus.</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL At regular intervals]</strong> </p> <p>Geben Sie die Anzahl der Minuten zwischen den Ausführungen ein. Der Standardwert ist 15 Minuten.</p> </li> 
        <li> <p><strong>[!UICONTROL Once]</strong> </p> <p>Geben Sie Datum und Uhrzeit ein, zu der das Szenario ausgeführt werden soll. Verwenden Sie den <code>MM/DD/YYYY h:mm A</code>. Beispiel: <code>06/25/2019 11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Every day]</strong> </p> <p>Geben Sie die Zeit ein, zu der das Szenario ausgeführt werden soll. Verwenden Sie den <code>h:mm A</code>. Beispiel: <code>11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Days of the week]</strong> </p> <p>Tage: Wählen Sie die Wochentage aus, an denen das Szenario ausgeführt werden soll. Sie können einen oder mehrere Tage auswählen.</p> <p>Zeit: Geben Sie die Zeit ein, zu der das Szenario an den ausgewählten Tagen ausgeführt werden soll. Verwenden Sie den <code>h:mm A</code>. Beispiel: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Days of the month]</strong> </p> <p>Tage: Wählen Sie die Tage des Monats aus, an denen das Szenario ausgeführt werden soll. Sie können einen oder mehrere Tage auswählen.</p> <p>Zeit: Geben Sie die Zeit ein, zu der das Szenario an den ausgewählten Tagen ausgeführt werden soll. Verwenden Sie den <code>h:mm A</code>. Beispiel: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Specified dates]</strong> </p> <p>Monate: Wählen Sie die Monate aus, in denen Sie das Szenario ausführen möchten. Sie können einen oder mehrere Monate auswählen.</p> <p>Tage: Wählen Sie die Tage des Monats aus, an denen das Szenario ausgeführt werden soll. Sie können einen oder mehrere Tage auswählen.</p> <p>Zeit: Geben Sie die Zeit ein, zu der das Szenario an den ausgewählten Tagen ausgeführt werden soll. Verwenden Sie den <code>h:mm A</code>. Beispiel: <code>11:00 PM</code></p> </li> 
       </ul> <p>Hinweis: Damit ein Szenario an diesem Datum ausgeführt werden kann, muss ein Datum vorhanden sein. Beispielsweise wird ein Szenario, das nur für den 31. des Monats geplant ist, nicht im Februar, April, Juni, September oder November ausgeführt, da diese Monate keinen 31. Tag haben.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Advanced scheduling]</td> 
      <td>Sie können bestimmte Zeitintervalle definieren, in denen Ihr Szenario ausgeführt werden soll. Sie können Tageszeitintervalle, Wochentage oder Monate angeben. Klicken Sie für jedes Intervall auf <strong>[!UICONTROL Add]</strong> und füllen Sie die Felder wie im Feld [!UICONTROL Run scenario] beschrieben aus.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Start]</td> 
      <td>Geben Sie Datum und Uhrzeit ein, nach denen das Szenario ausgeführt werden soll. Verwenden Sie den <code>MM/DD/YYYY h:mm A</code>. Beispiel: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL End]</td> 
      <td>Geben Sie Datum und Uhrzeit ein, vor der das Szenario ausgeführt werden soll. Verwenden Sie den <code>MM/DD/YYYY h:mm A</code>. Beispiel: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie auf **[!UICONTROL OK]** , um die Zeitplaneinstellungen zu speichern und zum Szenario zurückzukehren.
