---
title: JSONata-Module
description: Der Adobe Workfront Fusion JSONata-Connector bietet ein Modul zur Verarbeitung von Daten im JSON-Format, damit Adobe Workfront Fusion weiter mit dem Dateninhalt arbeiten kann.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# [!UICONTROL JSONata]-Module

Mit dem Adobe Workfront Fusion [!UICONTROL JSONata]-Connector können Sie JSON-Objekte abfragen. Dieses Modul erfordert keine Verbindung.

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



## JSONata-Module und ihre Felder

### Evaluate

Dieses Aktionsmodul fragt ein JSON-Objekt ab und gibt ein Array zurück.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Ausdruck]</td> 
   <td>Geben Sie den Ausdruck ein, den Sie zum Auswerten des JSON-Objekts verwenden möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Daten] </td> 
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
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
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
