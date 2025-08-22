---
title: Qualtrics-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Qualtrics verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 80b441b7-c808-4c4f-b9ff-d614650dbb73
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---

# Qualtrics-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Qualtrics] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Plan*</td>
  <td> <p>[!UICONTROL Pro] oder höher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz*</td>
   <td> <p>[!UICONTROL-Plan], [!UICONTROL-Arbeit]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den Plan [!UICONTROL Select] oder [!UICONTROL Prime] Adobe Workfront verfügen, muss Ihr Unternehmen Adobe Workfront Fusion sowie Adobe Workfront erwerben, um die in diesem Artikel beschriebenen Funktionen nutzen zu können. Workfront Fusion ist im Workfront-Plan [!UICONTROL Ultimate] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss Adobe Workfront Fusion sowie Adobe Workfront erwerben, um die in diesem Artikel beschriebenen Funktionen nutzen zu können.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Wenden Sie sich an Ihren Workfront-Administrator, um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Voraussetzungen

Um [!DNL Qualtrics] Module verwenden zu können, müssen Sie über ein [!UICONTROL Qualtrics]-Konto verfügen.

## Qualtrics-API-Informationen

Der Qualtrics-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://{{connection.dataCenterCode}}.qualtrics.com/API/v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.1.1</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL Qualtrics] mit Workfront Fusion

Sie können eine Verbindung zu Ihrem [!DNL Qualtrics]-Konto direkt aus einem [!UICONTROL Qualtrics]-Modul heraus erstellen.

1. Klicken Sie in einem [!UICONTROL Qualtrics]-Modul **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Geben Sie die folgenden Informationen ein:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Verbindungsname]</p> </td> 
      <td> <p>Geben Sie einen Namen für die neue Verbindung ein.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Rechenzentrum-ID] </td> 
      <td>Verwenden Sie den <code>&lt;Data Center ID>.qualtrics.com</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API-Schlüssel]</td> 
      <td>Informationen zum Auffinden Ihres API-Schlüssels finden Sie in der [!DNL Qualtrics].</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Qualtrics] Module und ihre Felder

Die folgenden Module sind für den [!DNL Qualtrics]-Connector verfügbar:

* [!UICONTROL Neue Umfrageantwort ansehen]
* [!UICONTROL Erstellen eines Verzeichniskontakts]
* [!UICONTROL Löschen eines Verzeichniskontakts]
* [!UICONTROL Verzeichniskontakt abrufen]
* [!UICONTROL Aktualisieren eines Verzeichniskontakts]
* [!UICONTROL Erstellen einer neuen Umfrageverteilung per SMS]
* [!UICONTROL Verteilen einer Umfrage per E-Mail]
* [!UICONTROL Erstellen eines API-Aufrufs]
* [!UICONTROL Verzeichniskontakte auflisten]
