---
title: JSONata-Module
description: Der Adobe Workfront Fusion JSONata-Connector bietet ein Modul zur Verarbeitung von Daten im JSON-Format, damit Adobe Workfront Fusion weiter mit dem Dateninhalt arbeiten kann.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---

# [!UICONTROL JSONata]-Module

Mit dem Adobe Workfront Fusion [!UICONTROL JSONata]-Connector können Sie JSON-Objekte abfragen. Dieses Modul erfordert keine Verbindung.

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
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Plan für [!UICONTROL Select] oder [!UICONTROL Prime] Workfront: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>[!UICONTROL Ultimate] Workfront-Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
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
