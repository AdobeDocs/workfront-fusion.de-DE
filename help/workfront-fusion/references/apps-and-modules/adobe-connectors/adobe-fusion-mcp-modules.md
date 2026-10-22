---
title: Adobe Fusion MCP-Module
description: Mit dem MCP-Modul von Adobe Fusion können Sie eine Eingabeaufforderung in englischer Sprache an den MCP-Server von Adobe Fusion senden und die Anfrage von einem KI-Modell ausführen lassen.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 06ba1c54288fff09f866bffa5c3fce7381c71ad2
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 14%
---
# Adobe Fusion MCP-Module

Der Adobe Fusion MCP-Connector sendet eine Eingabeaufforderung in englischer Sprache an den Adobe Fusion Model Context Protocol (MCP)-Server. Ein KI-Modell interpretiert Ihre Anfrage und ruft die dafür erforderlichen Fusion-Tools auf.

Der Connector funktioniert nur mit dem gehosteten Adobe Fusion MCP-Server. Sie können nicht auf einen anderen MCP-Server zeigen.

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
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Verbinden von Adobe Fusion MCP mit Workfront Fusion

Sie können eine Verbindung direkt aus dem Adobe Fusion MCP-Modul heraus erstellen.

1. Klicken Sie im MCP-Modul von Adobe Fusion **[!UICONTROL dem Feld]** Verbindung **auf „Hinzufügen**.
1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto">
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">Verbindungsname</td>
        <td>
          <p>Geben Sie einen Namen für die Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Umgebung</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Typ</td>
        <td>
          <p>Wählen Sie aus, ob eine Verbindung zu einem Service-Konto oder einem persönlichen Konto hergestellt werden soll.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Klicken Sie auf **[!UICONTROL Fortfahren]**.

Sie werden zur Anmeldeseite von Adobe weitergeleitet. Melden Sie sich mit Ihrem Adobe-Konto an und genehmigen Sie den Zugriff. Sie werden zurück zu Workfront Fusion weitergeleitet, und die neue Verbindung ist im -Modul verfügbar.

## Adobe Fusion MCP-Modul und seine Felder

### Benutzeraufforderung verarbeiten

Dieses Aktionsmodul sendet eine Eingabeaufforderung in englischer Sprache an den Adobe Fusion MCP-Server. Ein KI-Modell interpretiert die Eingabeaufforderung, ruft die für den Abschluss erforderlichen Fusion-Tools auf und gibt das Ergebnis zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>LLM-<i> (optional, erweitert)</i></td> 
   <td> <p>Standardmäßig verarbeitet dieses Modul Ihre Eingabeaufforderung mit Adobe Managed AI, sodass Sie keinen Schlüssel auswählen müssen.</p> <p>Um stattdessen Ihren eigenen KI-Anbieter zu verwenden, wählen Sie einen vorhandenen LLM-Schlüssel aus oder erstellen Sie einen neuen, indem Sie auf <b>Hinzufügen</b> klicken und die folgenden Informationen eingeben:</p>
     <ul>
       <li><b>Schlüsselname</b>: Geben Sie einen Namen für den neuen Schlüssel ein.</li>
       <li><b>LLM</b>: Wählen Sie das große Sprachmodell aus, mit dem dieser Schlüssel verknüpft ist. Unterstützte Anbieter sind OpenAI, Anthropic und Amazon Bedrock.</li>
       <li><b>Schlüssel</b>: Geben Sie den API-Schlüssel für den ausgewählten Anbieter ein oder ordnen Sie ihn zu.</li>
       <li><b>Modell</b>: Wählen Sie das LLM-Modell aus, das der Schlüssel verwenden soll.</li>
       <li><b>Andere Felder</b>: Geben Sie Werte für alle anderen Felder ein, die für Ihr LLM erforderlich sind.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden von Adobe Fusion MCP mit Workfront Fusion finden Sie unter <a href="#connect-adobe-fusion-mcp-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Fusion MCP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Schreibgeschützte Tools <i>(optional)</i></td> 
   <td> <p>Wählen Sie bestimmte schreibgeschützte Tools aus, um die KI einzuschränken. Wenn keine ausgewählt sind, sind alle schreibgeschützten Tools in dieser Kategorie zulässig.</p> </td> 
  </tr> 
  <tr> 
   <td>Schreib-/Löschwerkzeuge <i>(optional)</i></td> 
   <td> <p>Wählen Sie bestimmte Schreib- oder Löschwerkzeuge aus, um die KI einzuschränken. Wenn keine ausgewählt sind, sind alle Schreib- und Löschwerkzeuge in dieser Kategorie zulässig.</p> <p>Um sicherzustellen, dass ein unbeaufsichtigtes Szenario niemals eine destruktive Aktion ausführt, empfehlen wir, dieses Feld, das auf eine absichtlich leere Auswahl eingestellt ist, nicht unbeschränkt zu lassen.</p> </td> 
  </tr> 
  <tr> 
   <td>Eingabeaufforderung eingeben</td> 
   <td> <p>Geben Sie die Anweisung ein, die die KI ausführen soll, oder kartieren Sie sie in einfachem Englisch.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Beschränken Sie die Tools, die die KI aufrufen kann

Sie können einschränken, welche Fusion-Tools die KI aufrufen kann, indem Sie Tools in den Feldern Schreibgeschützte Tools und Schreib-/Löschtools auswählen.

* Wenn Sie ein Feld leer lassen, kann die KI jedes Tool in dieser Kategorie aufrufen.
* Wenn Sie beide Felder leer lassen, kann die KI jedes Tool auf dem Fusion MCP-Server aufrufen.

Um zu verhindern, dass ein unbeaufsichtigtes Szenario eine Schreib- oder Löschaktion ausführt, wählen Sie im Feld Schreibgeschützte Tools nur die Tools aus, die Sie zulassen möchten, und wählen Sie im Feld Schreib-/Löschtools mindestens ein Tool aus, das mit dem Aufruf der KI vertraut ist.

Die Toolnamen in den Listen stammen vom Fusion MCP-Server.

#### Verarbeitung der Eingabeaufforderung durch das Modul

* Das Modul hat keine Folgedrehung. Wenn Ihre Eingabeaufforderung unklar ist, geht die KI von einer vernünftigen Annahme aus und gibt sie in der Antwort an, anstatt Ihnen eine Frage zu stellen.
* Die KI überprüft Informationen, die sich mithilfe der Tools ändern können.
* Die KI führt keine Schreib- oder Löschaktionen durch, die über die von Ihrer Eingabeaufforderung angeforderten hinausgehen.
* Für das Modul ist eine gültige Verbindung erforderlich. Ohne läuft es nicht.

#### Ausgabe

Das -Modul gibt die folgenden Informationen zurück, die Sie in nachfolgenden Modulen im Szenario zuordnen können:

* **Antwort**: Die endgültige Antwort der KI als Text.
* **Audit-Protokoll**: Ein Datensatz der Sitzung, einschließlich der aufgerufenen Tools, ihrer Argumente und Ergebnisse und der Timings.
* **Zusammenfassung**: Gesamtwerte für die Sitzung, einschließlich der Anzahl erfolgreicher Tool-Aufrufe und des endgültigen Status.
