---
title: MCP-Module (Model Context Protocol)
description: Mit dem Modul „Model Context Protocol“ (MCP) können Sie eine Benutzeraufforderung mithilfe von MCP verarbeiten.
author: Becky
feature: Workfront Fusion
source-git-commit: d8ae176db714d2b9f041b74a62e8276171745c4b
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---

# MCP-Module (Model Context Protocol)

Das Model Context Protocol (MCP) ist eine Möglichkeit, KI-Sprachmodelle sicher mit anderen Anwendungen zu verbinden. Sie konfigurieren MCP-Server, die dem KI-Modell den Zugriff auf die Anwendung ermöglichen. Sie können dann eine Eingabeaufforderung an das KI-Modell senden und es kann Informationen aus der Anwendung zurückgeben.

Sie können beispielsweise einen MCP-Server konfigurieren, um ein KI-Modell mit Gmail zu verbinden. Wenn Sie die Eingabeaufforderung „Give me my last 5 emails from Gmail“ (Gib mir meine letzten 5 E-Mails von Gmail) senden, kann sie auf Gmail zugreifen und die E-Mails zurücksenden.

Mit dem Modul „Model Context Protocol“ (MCP) können Sie eine Benutzeraufforderung mit einem Sprachmodell und MCP-Servern verarbeiten.

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Oder</p>
   <p>Legacy: Workfront Fusion für Arbeitsautomatisierung und -integration </p>
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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Modul für Modellkontext-Protokoll und seine Felder

Beim Konfigurieren des MCP-Moduls zeigt [!DNL Adobe Workfront Fusion] die unten aufgeführten Felder an. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

### Eingabeaufforderung verarbeiten

Dieses Aktionsmodul verarbeitet eine Eingabeaufforderung mit dem von Ihnen angegebenen Sprachmodell und MCP-Servern.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Schlüssel für großes Sprachmodell (LLM)]</td> 
   <td> <p>Geben Sie den API-Schlüssel für das große Sprachmodell ein, das Sie für diese Eingabeaufforderung verwenden möchten, oder ordnen Sie ihn zu. </p> <p>Derzeit wird nur der anthropische API-Schlüssel unterstützt.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MCP-Server]</td> 
   <td> <p>Klicken Sie für jeden MCP-Server, den Sie für diese Eingabeaufforderung bereitstellen möchten, auf <b>Element hinzufügen</b> und geben Sie den Servernamen und den Host ein. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eingabeaufforderung eingeben]</td> 
   <td> <p>Geben Sie die Eingabeaufforderung für das große Sprachmodell ein oder ordnen Sie sie zu. </p> </td> 
  </tr> 
 </tbody> 
</table>
