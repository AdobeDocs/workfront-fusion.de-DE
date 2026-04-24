---
title: MCP-Module (Model Context Protocol)
description: Mit dem Modul „Model Context Protocol“ (MCP) können Sie eine Benutzeraufforderung mithilfe von MCP verarbeiten.
author: Becky
feature: Workfront Fusion
hide: true
exl-id: 748055ad-d305-4513-9a5c-9c970b74a96e
source-git-commit: 80f2d078cd624424f23bd007e852f49643fec7f3
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 18%

---

# MCP Agent-Modul

<!--SET UP REDIRECTS-->

Das Model Context Protocol (MCP) ist eine Möglichkeit, KI-Sprachmodelle sicher mit anderen Anwendungen zu verbinden. Sie konfigurieren MCP-Server, die dem KI-Modell den Zugriff auf die Anwendung ermöglichen. Sie können dann eine Eingabeaufforderung an das KI-Modell senden und es kann Informationen aus der Anwendung zurückgeben.

Sie können beispielsweise einen MCP-Server konfigurieren, um ein KI-Modell mit Gmail zu verbinden. Wenn Sie die Eingabeaufforderung „Give me my last 5 emails from Gmail“ (Gib mir meine letzten 5 E-Mails von Gmail) senden, kann sie auf Gmail zugreifen und die E-Mails zurücksenden.

Mit dem Modul „Model Context Protocol“ (MCP) können Sie eine Benutzeraufforderung mit einem Sprachmodell und MCP-Servern verarbeiten.

Weitere Informationen zu MCP in Fusion-Szenarien finden Sie unter [Hinzufügen einer KI-Eingabeaufforderung zum Szenario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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

## Voraussetzungen

* Sie müssen alle MCP-Server konfiguriert haben, mit denen Sie eine Verbindung herstellen möchten.
* Zum ausgewählten LLM (Large Language Model) muss ein LLM-Schlüssel vorhanden sein.

## Modul für Modellkontext-Protokoll und seine Felder

### Eingabeaufforderung verarbeiten

Dieses Aktionsmodul verarbeitet eine Eingabeaufforderung mit dem von Ihnen angegebenen Sprachmodell und MCP-Servern.

>[!NOTE]
>
>Dieses Modul muss ein -Objekt zurückgeben. Es wird keine Ausgabe wie Zeichenfolgen oder Zahlen zurückgegeben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>LLM-Schlüssel</td> 
   <td> Wählen Sie einen vorhandenen LLM-Schlüssel aus oder erstellen Sie einen neuen, indem Sie auf <b>Hinzufügen</b> klicken und die folgenden Informationen eingeben: 
     <ul>
       <li><b>Schlüsselname</b>: Geben Sie einen Namen für den neuen Schlüssel ein.</li>
       <li><b>LLM</b>: Wählen Sie das große Sprachmodell aus, mit dem dieser Schlüssel verknüpft ist.</li>
       <li><b>Schlüssel</b>: Geben Sie den API-Schlüssel für das ausgewählte Modell ein oder ordnen Sie ihn zu.</li>
       <li><b>Modell</b>: Wählen Sie das LLM-Modell aus, das der Schlüssel verwenden soll.</li>
       <li><b>Max Tokens</b>: Geben Sie die maximale Anzahl von Token ein, die das LLM in seiner Antwort generieren kann, oder ordnen Sie sie zu.<p>Ein Token entspricht in der Regel vier Zeichen oder 0,75 eines Wortes im Englischen. „Hello world“ entspricht zwei Token und „Authentication“ entspricht einem Token zu zwei Token.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>MCP-Server</td> 
   <td> <p>Klicken Sie für jeden MCP-Server, mit dem Sie eine Verbindung herstellen möchten<b> auf „Hinzufügen</b> und geben Sie die folgenden Informationen ein: </p> 
     <ul>
       <li><b>Verbindung</b>: Wählen Sie die Verbindung aus, die Fusion für die Verbindung mit dem MCP-Server verwenden wird.</li>
       <li><b>MCP Server Host</b>: Geben Sie die URL des MCP-Servers ein.</li>
       <li><b>MCP Server Name</b>: Geben Sie einen Namen für diesen MCP-Server ein oder ordnen Sie ihn zu.</li>
       <li><b>Headers</b>: Fügen Sie alle anwendbaren Header hinzu.</li>
       <li><b>MCP Server Type</b>: Wählen Sie den Server Type.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>Eingabeaufforderung eingeben </td> 
   <td> <p>Geben Sie die Eingabeaufforderung ein, die Sie verarbeiten möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>


