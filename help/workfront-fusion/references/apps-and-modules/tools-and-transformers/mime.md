---
title: MIME-Module
description: Sie können MIME-Typen in Adobe Workfront Fusion verwenden. MIME-Typen (Multipurpose Internet Mail Extension) sind Bezeichnungen, mit denen Software verschiedene Arten von im Internet freigegebenen Daten identifizieren kann. Webserver und Browser verwenden den MIME-Typ, um zu bestimmen, was mit einer Datei getan werden soll. Beispielsweise wird eine Datei mit dem MIME-Typ text/html in einem Browser anders verarbeitet als eine Datei mit dem MIME-Typ image/jpeg. MIME-Typen funktionieren unabhängig von Betriebssystem und Hardware.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# [!UICONTROL MIME]

Sie können MIME-Typen in Adobe Workfront Fusion verwenden. MIME-Typen (Multipurpose Internet Mail Extension) sind Bezeichnungen, mit denen Software verschiedene Arten von im Internet freigegebenen Daten identifizieren kann. Webserver und Browser verwenden den MIME-Typ, um zu bestimmen, was mit einer Datei getan werden soll. Beispielsweise wird eine Datei mit dem MIME-Typ `text/html` in einem Browser anders verarbeitet als eine Datei mit dem MIME-Typ `image/jpeg`. MIME-Typen funktionieren unabhängig von Betriebssystem und Hardware.

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Plan*</td>
  <td> <p>[!UICONTROL Pro] oder höher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung und -integration], [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den [!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Adobe Workfront] verfügen, muss Ihr Unternehmen [!DNL Adobe Workfront Fusion] kaufen und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden. [!DNL Workfront Fusion] ist im [!UICONTROL Ultimate] [!DNL Workfront] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## [!UICONTROL MIME] Module und ihre Felder

### [!UICONTROL Get a MIME type]

Dieses Transformatormodul gibt den MIME-Typ zurück, der mit einem bestimmten Namen, Pfad oder einer bestimmten Erweiterung verknüpft ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL File]</td> 
   <td> <p>Geben Sie die Datei ein, für die Sie den MIME-Typ bestimmen möchten, oder ordnen Sie sie zu. </p> <p>Sie können die Datei wie folgt eingeben:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File path]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>[!UICONTROL File name]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>image.jpeg</p> </li> 
     <li><strong>[!UICONTROL File extension]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get a file extension]

Dieses Transformatormodul gibt die ursprüngliche Dateierweiterung für einen bestimmten MIME-Typ zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME type]</td> 
   <td> <p>Geben Sie den MIME-Typ ein, für den Sie die Dateierweiterung bestimmen möchten, oder ordnen Sie ihn zu. </p> </td> 
  </tr> 
 </tbody> 
</table>
