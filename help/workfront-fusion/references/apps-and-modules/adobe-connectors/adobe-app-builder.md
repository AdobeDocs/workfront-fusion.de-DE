---
title: Adobe App Builder-Modul
description: Mit dem Adobe App Builder-Connector können Sie benutzerdefinierte Funktionen in Ihren Szenarien verwenden.
author: Becky
feature: Workfront Fusion
source-git-commit: 8250d4fdad8ed7ffe63cd003f6e0cb325cbbfa8d
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 31%

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

## Adobe App Builder-Modul

Das einzige derzeit verfügbare Adobe App Builder-Modul ist die Aktion „Ausführen“, mit der Sie eine zuvor konfigurierte benutzerdefinierte JavaScript-Funktion verwenden können.

Anweisungen zum Konfigurieren einer benutzerdefinierten Funktion finden Sie unter [Zuordnen von Daten mithilfe benutzerdefinierter Funktionen](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

### Ausführen einer Aktion

Dieses Modul führt eine zuvor konfigurierte benutzerdefinierte Funktion aus.

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
   <td role="rowheader">[!UICONTROL-Parameter] </td> 
   <td>Geben Sie die Werte für die Funktionsparameter ein. Die verfügbaren Parameter basieren auf den Parametern, die beim Erstellen der Funktion konfiguriert wurden.<p>Wenn ein Parameter einen Standardwert hat, wird er nicht im Feld angezeigt, Sie können ihn jedoch überschreiben, indem Sie einen Wert in das Feld eingeben oder zuordnen.</p></td> 
  </tr> 
   </tbody> 
</table>


