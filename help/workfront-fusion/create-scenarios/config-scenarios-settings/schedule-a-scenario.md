---
content-type: reference
title: Szenario planen
description: Standardmäßig wird ein Szenario alle 15 Minuten ausgeführt. Sie können dies ändern, indem Sie festlegen, wann und wie oft ein aktiviertes Szenario ausgeführt wird. Fusionsszenarien können so geplant werden, dass sie alle 5 Minuten ausgeführt werden.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 1%

---

# Szenario planen

Standardmäßig wird ein Szenario alle 15 Minuten ausgeführt. Sie können dies ändern, indem Sie festlegen, wann und wie oft ein aktiviertes Szenario ausgeführt wird. Fusionsszenarien können so geplant werden, dass sie alle 5 Minuten ausgeführt werden.

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

## Szenario planen

1. Klicken Sie auf **Registerkarte** Szenario“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, das Sie planen möchten.
1. Klicken Sie oben rechts auf der Seite mit den Szenario-Details auf **[!UICONTROL Optionen]** > **[!UICONTROL Planung]**

   Oder

   Klicken Sie auf **[!UICONTROL Planung]**-Symbol (Uhr) im Trigger -Modul des Szenarios.

1. Geben Sie Informationen in die folgenden Felder ein:

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL-Ausführungsszenario]</td> 
      <td> <p>Wählen Sie die Häufigkeit aus, mit der Sie das Szenario ausführen möchten, und wählen Sie dann das Intervall aus.</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL in regelmäßigen Abständen]</strong> </p> <p>Geben Sie die Anzahl der Minuten zwischen den Ausführungen ein. Der Standardwert ist 15 Minuten.</p> </li> 
        <li> <p><strong>[!UICONTROL once]</strong> </p> <p>Geben Sie Datum und Uhrzeit ein, zu der das Szenario ausgeführt werden soll. Verwenden Sie den <code>MM/DD/YYYY h:mm A</code>. Beispiel: <code>06/25/2019 11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Every day]</strong> </p> <p>Geben Sie die Zeit ein, zu der das Szenario ausgeführt werden soll. Verwenden Sie den <code>h:mm A</code>. Beispiel: <code>11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Wochentage]</strong> </p> <p>Tage: Wählen Sie die Wochentage aus, an denen das Szenario ausgeführt werden soll. Sie können einen oder mehrere Tage auswählen.</p> <p>Zeit: Geben Sie die Zeit ein, zu der das Szenario an den ausgewählten Tagen ausgeführt werden soll. Verwenden Sie den <code>h:mm A</code>. Beispiel: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Tage des Monats]</strong> </p> <p>Tage: Wählen Sie die Tage des Monats aus, an denen das Szenario ausgeführt werden soll. Sie können einen oder mehrere Tage auswählen.</p> <p>Zeit: Geben Sie die Zeit ein, zu der das Szenario an den ausgewählten Tagen ausgeführt werden soll. Verwenden Sie den <code>h:mm A</code>. Beispiel: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL angegebene Daten]</strong> </p> <p>Monate: Wählen Sie die Monate aus, in denen Sie das Szenario ausführen möchten. Sie können einen oder mehrere Monate auswählen.</p> <p>Tage: Wählen Sie die Tage des Monats aus, an denen das Szenario ausgeführt werden soll. Sie können einen oder mehrere Tage auswählen.</p> <p>Zeit: Geben Sie die Zeit ein, zu der das Szenario an den ausgewählten Tagen ausgeführt werden soll. Verwenden Sie den <code>h:mm A</code>. Beispiel: <code>11:00 PM</code></p> </li> 
       </ul> <p>Hinweis: Damit ein Szenario an diesem Datum ausgeführt werden kann, muss ein Datum vorhanden sein. Beispielsweise wird ein Szenario, das nur für den 31. des Monats geplant ist, nicht im Februar, April, Juni, September oder November ausgeführt, da diese Monate keinen 31. Tag haben.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Erweiterte Planung]</td> 
      <td>Sie können bestimmte Zeitintervalle definieren, in denen Ihr Szenario ausgeführt werden soll. Sie können Tageszeitintervalle, Wochentage oder Monate angeben. Klicken Sie für jedes Intervall auf <strong>[!UICONTROL Hinzufügen]</strong> und füllen Sie die Felder wie im Feld [!UICONTROL-Ausführungsszenario] beschrieben aus.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Start]</td> 
      <td>Geben Sie Datum und Uhrzeit ein, nach denen das Szenario ausgeführt werden soll. Verwenden Sie den <code>MM/DD/YYYY h:mm A</code>. Beispiel: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL-Ende]</td> 
      <td>Geben Sie Datum und Uhrzeit ein, vor der das Szenario ausgeführt werden soll. Verwenden Sie den <code>MM/DD/YYYY h:mm A</code>. Beispiel: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **[!UICONTROL OK]**, um die Zeitplaneinstellungen zu speichern und zum Szenario zurückzukehren.
