---
title: Adobe App Builder-Modul
description: Mit dem Adobe App Builder-Connector können Sie benutzerdefinierte Funktionen in Ihren Szenarien verwenden.
author: Becky
feature: Workfront Fusion
exl-id: 92661a0c-436b-4fbd-808a-a4fbe3cd2339
source-git-commit: 4392b9d13c49d3d64b2b694bf23cfc227ae36d02
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 26%

---

# Adobe App Builder-Modul

Im Bereich Funktionen von Fusion können Sie benutzerdefinierte Funktionen erstellen. Anschließend fügen Sie diese Funktionen in Form eines Adobe App Builder-Moduls zu Ihren Szenarien hinzu.

Da benutzerdefinierte Funktionen über Adobe App Builder funktionieren, muss Ihr Unternehmen über eine Adobe App Builder-Lizenz verfügen, um sie verwenden zu können.

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Ein beliebiges Adobe Workfront Workflow- und Adobe Workfront Automation and Integration-Paket</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p><ul><li>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li><li>Sie benötigen eine Adobe App Builder-Lizenz, um benutzerdefinierte Funktionen verwenden zu können.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Adobe App Builder-Module

### Benutzerdefinierten Codeblock ausführen

Mit diesem Modul können Sie einen Code-Block ausführen. Sie konfigurieren den Code-Block beim Einrichten des Moduls. Er wird ausgeführt, wenn das Modul während der Ausführung eines Szenarios ausgeführt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td>
   <td>Wählen Sie die Verbindung aus, die die benutzerdefinierte Funktion enthält, die Sie ausführen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Code-Block]</td> 
   <td>Geben Sie den Code-Block ein, den das Modul ausführen soll.<p>Um den Code für eine einfachere Lesbarkeit zu formatieren, klicken Sie auf das Symbol <b>Code formatieren</b>.</td> 
  </tr> 
   </tbody> 
</table>

### Benutzerdefinierte Funktion ausführen

In diesem Modul können Sie eine zuvor konfigurierte benutzerdefinierte JavaScript-Funktion verwenden, die im Bereich „Funktionen“ gespeichert ist.

Anweisungen zum Konfigurieren einer benutzerdefinierten Funktion finden Sie unter [Zuordnen von Daten mithilfe benutzerdefinierter Funktionen](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td>
   <td>Wählen Sie die Verbindung aus, die die benutzerdefinierte Funktion enthält, die Sie ausführen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aktion]</td> 
   <td>Wählen Sie die benutzerdefinierte Funktion aus, die Sie ausführen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Parameter] </td> 
   <td>Geben Sie die Werte für die Funktionsparameter ein. Die verfügbaren Parameter basieren auf den Parametern, die beim Erstellen der Funktion konfiguriert wurden.<p>Wenn ein Parameter einen Standardwert hat, wird er nicht im Feld angezeigt, Sie können ihn jedoch überschreiben, indem Sie einen Wert in das Feld eingeben oder zuordnen.</p></td> 
  </tr> 
   </tbody> 
</table>
