---
title: JSONata-Module
description: Der Adobe Workfront Fusion JSONata-Connector bietet ein Modul zur Verarbeitung von Daten im JSON-Format, damit Adobe Workfront Fusion weiter mit dem Dateninhalt arbeiten kann.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
TQID: https://experienceleague.adobe.com/luvZBccaWY5-8muR71o8C82qVROYJvcuAqt3Ol2LZac
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 329
ht-degree: 28%

---

# [!UICONTROL JSONata]-Module

Mit dem Adobe Workfront Fusion [!UICONTROL JSONata]-Connector können Sie JSON-Objekte abfragen. Dieses Modul erfordert keine Verbindung.

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
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## JSONata-Module und ihre Felder

### Evaluate

Dieses Aktionsmodul fragt ein JSON-Objekt ab und gibt ein Array zurück.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ausdruck]</td> 
   <td>Geben Sie den Ausdruck ein, den Sie zum Auswerten des JSON-Objekts verwenden möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Daten] </td> 
   <td> Geben Sie das zu überprüfende JSON-Objekt ein.  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringify-Ausgabe] </td> 
   <td> Aktivieren Sie diese Option, um die Ausgabe in eine Zeichenfolge zu konvertieren.  </td> 
  </tr> 
  </tbody>
  </table>

>[!BEGINSHADEBOX]

**Beispiel**:

Das Ziel besteht darin, ein Array von Namen aus dem folgenden JSON-Objekt zurückzugeben:

```JSON
{
  "people": [
    { "name": "Alice", "age": 30 },
    { "name": "Bob", "age": 25 },
    { "name": "Charlie", "age": 35 }
  ]
}
```

1. Geben Sie im Ausdrucksfeld `people.name` ein.
1. Geben Sie im Datenfeld das JSON-Objekt ein.

Das -Modul gibt ein Array von Namen zurück, die aus dem JSON-Objekt abgerufen wurden.

>[!ENDSHADEBOX]



### JSONata MCP

Dieses Aktionsmodul generiert JSONata-Ausdrücke durch Analyse der angegebenen Eingabe- und Ausgabeschemata. Sie stellen die Schemata bereit, die das Model Context Protocol (MCP) verwendet, um den Ausdruck zu generieren, der die Eingabe in die Ausgabe umwandelt.




<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie die Verbindung aus, die Sie für die Verbindung mit dem Large Language Model (LLM) verwenden möchten, das Sie für dieses Modul verwenden möchten.</p> <p>Derzeit wird nur der anthropische API-Schlüssel unterstützt.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eingabeschema]</td> 
   <td> <p>Eingabeschema eingeben oder zuordnen, das für diesen Ausdruck verwendet werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabeschema]</td> 
   <td> <p>Geben Sie das Ausgabeschema ein, das für diesen Ausdruck verwendet werden soll, oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>
