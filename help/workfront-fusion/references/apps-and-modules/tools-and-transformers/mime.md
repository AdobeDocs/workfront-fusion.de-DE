---
title: MIME-Module
description: Sie können MIME-Typen in Adobe Workfront Fusion verwenden. MIME-Typen (Multipurpose Internet Mail Extension) sind Bezeichnungen, mit denen Software verschiedene Arten von im Internet freigegebenen Daten identifizieren kann. Webserver und Browser verwenden den MIME-Typ, um zu bestimmen, was mit einer Datei getan werden soll. Beispielsweise wird eine Datei mit dem MIME-Typ text/html in einem Browser anders verarbeitet als eine Datei mit dem MIME-Typ image/jpeg. MIME-Typen funktionieren unabhängig von Betriebssystem und Hardware.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# [!UICONTROL MIME] Module

Sie können MIME-Typen in Adobe Workfront Fusion verwenden. MIME-Typen (Multipurpose Internet Mail Extension) sind Bezeichnungen, mit denen Software verschiedene Arten von im Internet freigegebenen Daten identifizieren kann. Webserver und Browser verwenden den MIME-Typ, um zu bestimmen, was mit einer Datei getan werden soll. Beispielsweise wird eine Datei mit dem MIME-Typ `text/html` in einem Browser anders verarbeitet als eine Datei mit dem MIME-Typ `image/jpeg`. MIME-Typen funktionieren unabhängig von Betriebssystem und Hardware.

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
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Keine Workfront Fusion-Lizenzanforderung</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Prime oder Workfront auswählen: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>Ultimate Workfront-Paket: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
   <td role="rowheader">[!UICONTROL -Datei]</td> 
   <td> <p>Geben Sie die Datei ein, für die Sie den MIME-Typ bestimmen möchten, oder ordnen Sie sie zu. </p> <p>Sie können die Datei wie folgt eingeben:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Dateipfad]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>[!UICONTROL Dateiname]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>image.jpeg</p> </li> 
     <li><strong>[!UICONTROL -Dateierweiterung]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
