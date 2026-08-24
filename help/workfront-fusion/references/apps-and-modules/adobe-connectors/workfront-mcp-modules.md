---
title: Adobe Workfront MCP-Module
description: Mit dem Adobe Workfront MCP-Modul können Sie eine Eingabeaufforderung in englischer Sprache an den MCP-Server von Adobe Workfront senden und die Anforderung von einem KI-Modell ausführen lassen.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 88515edc81bafe2d1a81df627fd51dd4ed674c02
workflow-type: tm+mt
source-wordcount: 884
ht-degree: 16%

---

# Adobe Workfront MCP-Module

Der Adobe Workfront MCP-Connector ist eine dedizierte Fusion-Integration für Adobe Workfronts eigenen MCP-Server (Model Context Protocol). Im Gegensatz zu einem typischen Connector, bei dem jedes Modul eine feste Aktion ausführt, verfügt dieser Connector über ein einziges Modul, das eine offene, englischsprachige Anweisung akzeptiert und es einem KI-Modell ermöglicht, zu entscheiden, welche Workfront-Vorgänge erforderlich sind, um diese auszuführen.

Sie können beispielsweise die Eingabeaufforderung „Alle meine aktiven Projekte im Verzug finden und ihren Status zusammenfassen“ eingeben und das Modul gibt eine zusammenfassende Antwort zurück, anstatt mehrere GET- und FILTER-Module verketten zu müssen.

Sie können einschränken, welche Workfront-Aktionen die KI durchführen darf, sodass selbst ein unbeaufsichtigtes Szenario garantieren kann, dass keine unerwarteten destruktiven Aktionen durchgeführt werden.

Standardmäßig verwendet dieses Modul Adobe Managed AI mit dem `claude-sonnet-5`. Sie können das Modul mithilfe eines Schlüssels und anderer von Ihnen bereitgestellter Anmeldeinformationen für die Verwendung eines anderen LLM konfigurieren.

>[!NOTE]
>
>Die Nutzung von Adobe Managed AI ist auf 25 USD pro Organisation und Monat beschränkt.

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

## Adobe Workfront MCP mit Workfront Fusion verbinden

Der Adobe Workfront MCP-Connector verwendet OAuth 2.0, um eine Verbindung zu Workfront herzustellen. Im Gegensatz zu anderen Workfront-Connectoren gibt es keine manuellen Verbindungsfelder, wie z. B. einen Host, eine Client-ID oder einen geheimen Client-Schlüssel, die ausgefüllt werden müssen.

So erstellen Sie eine Verbindung:

1. Klicken Sie im MCP-Modul von Adobe Workfront **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .
1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für die Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>Wählen Sie aus, ob eine Verbindung zu einem Service-Konto oder einem persönlichen Konto hergestellt werden soll.</td>
      </tr>
    </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

   Wenn Sie nicht bei Workfront angemeldet sind, werden Sie zu einem Anmeldebildschirm weitergeleitet. Anmelden und Zugriff genehmigen.

Sie werden zurück zu Workfront Fusion weitergeleitet, und die neue Verbindung ist im -Modul verfügbar.

>[!NOTE]
>
>Bei der ersten Verwendung registriert sich die Verbindung automatisch beim MCP-Server von Workfront und verwendet diese Registrierung für jede nachfolgende Verbindung, die Sie erstellen.

## Adobe Workfront MCP-Modul und seine Felder

### Benutzeraufforderung verarbeiten

Dieses Aktionsmodul verarbeitet unter Verwendung des von Ihnen angegebenen Sprachmodells eine Eingabeaufforderung in englischer Sprache gegenüber dem MCP-Server von Workfront und gibt die Antwort der KI zurück.

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
  </tr>   <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-adobe-workfront-mcp-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Workfront MCP mit Workfront </a>) in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>Schreibgeschützte Tools <i>(optional)</i></td> 
   <td> <p>Beschränken Sie, welche schreibgeschützten Workfront-Aktionen die KI aufrufen darf. Wenn keine Tools ausgewählt sind, sind alle schreibgeschützten Tools zulässig.</p> </td> 
  </tr> 
  <tr> 
   <td>Schreib-/Löschwerkzeuge <i>(optional)</i></td> 
   <td> <p>Geben Sie die Schreib- oder Löschaktionen für Workfront ein, die die KI aufrufen darf. Wenn Sie dieses Feld leer lassen, sind alle Schreib- und Löschwerkzeuge zulässig.</p> <p>Um sicherzustellen, dass ein unbeaufsichtigtes Szenario niemals eine destruktive Aktion ausführt, empfehlen wir, dieses Feld, das auf eine absichtlich leere Auswahl eingestellt ist, nicht unbeschränkt zu lassen.</p> </td> 
  </tr> 
  <tr> 
   <td>Eingabeaufforderung eingeben</td> 
   <td> <p>Geben Sie die Anweisung ein, die die KI ausführen soll, oder kartieren Sie sie in einfachem Englisch.</p> <p>Beispiel: <i>Alle mir zugewiesenen Projekte finden, die sich im Verzug befinden.</i></p> </td> 
  </tr>  </tbody> 
</table>

Eine Liste der Tools, die Sie für die Felder Schreibgeschützte Tools und Schreib-/Löschtools auswählen können, finden Sie unter [Adobe Workfront MCP Server Tools](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-tools) in der Dokumentation zu Workfront.

Das -Modul gibt die folgenden Informationen zurück, die Sie in nachfolgenden Modulen im Szenario zuordnen können:

* **Antwort**: Die endgültige Antwort der KI als Text.
* **Audit-Protokoll**: Ein Datensatz der Sitzung, einschließlich der ursprünglichen Eingabeaufforderung, Start- und Endzeit und Details zu jedem von der KI durchgeführten Tool-Aufruf, wie z. B. der Tool-Name, die Argumente, ob der Aufruf erfolgreich war, die Dauer und die Ausgabe.
* **Zusammenfassung**: Gesamtwerte für die Sitzung, einschließlich der Anzahl der versuchten Tool-Aufrufe, der Anzahl der erfolgreichen oder fehlgeschlagenen Aufrufe, der Gesamtverarbeitungszeit und des Gesamtstatus.
