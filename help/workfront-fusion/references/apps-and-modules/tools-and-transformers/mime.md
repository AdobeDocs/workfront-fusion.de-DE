---
title: MIME-Module
description: Sie können MIME-Typen in Adobe Workfront Fusion verwenden. MIME-Typen (Multipurpose Internet Mail Extension) sind Bezeichnungen, mit denen Software verschiedene Arten von im Internet freigegebenen Daten identifizieren kann. Webserver und Browser verwenden den MIME-Typ, um zu bestimmen, was mit einer Datei getan werden soll. Beispielsweise wird eine Datei mit dem MIME-Typ text/html in einem Browser anders verarbeitet als eine Datei mit dem MIME-Typ image/jpeg. MIME-Typen funktionieren unabhängig von Betriebssystem und Hardware.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# [!UICONTROL MIME] Module

Sie können MIME-Typen in Adobe Workfront Fusion verwenden. MIME-Typen (Multipurpose Internet Mail Extension) sind Bezeichnungen, mit denen Software verschiedene Arten von im Internet freigegebenen Daten identifizieren kann. Webserver und Browser verwenden den MIME-Typ, um zu bestimmen, was mit einer Datei getan werden soll. Beispielsweise wird eine Datei mit dem MIME-Typ `text/html` in einem Browser anders verarbeitet als eine Datei mit dem MIME-Typ `image/jpeg`. MIME-Typen funktionieren unabhängig von Betriebssystem und Hardware.

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



## [!UICONTROL MIME]-Module und ihre Felder

* [Abrufen einer Dateierweiterung](#get-a-file-extension)
* [Abrufen eines MIME-Typs](#get-a-mime-type)

### [!UICONTROL Dateierweiterung abrufen]

Dieses Transformatormodul gibt die ursprüngliche Dateierweiterung für einen bestimmten MIME-Typ zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME-Typ]</td> 
   <td> <p>Geben Sie den MIME-Typ ein, für den Sie die Dateierweiterung bestimmen möchten, oder ordnen Sie ihn zu. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Abrufen eines MIME-Typs]

Dieses Transformatormodul gibt den MIME-Typ zurück, der mit einem bestimmten Dateinamen, Pfad oder einer bestimmten Erweiterung verknüpft ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Datei]</td> 
   <td> <p>Geben Sie die Datei ein, für die Sie den MIME-Typ bestimmen möchten, oder ordnen Sie sie zu. </p> <p>Sie können die Datei wie folgt eingeben:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Dateipfad]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>[!UICONTROL Dateiname]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>image.jpeg</p> </li> 
     <li><strong>[!UICONTROL-Dateierweiterung]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
