---
title: Adobe Marketo Engage MCP-Modul
description: Mit dem Adobe Marketo Engage MCP-Modul können Sie eine Eingabeaufforderung in natürlicher Sprache an den MCP-Server (Model Context Protocol) von Adobe Marketo Engage senden.
author: Becky
feature: Workfront Fusion
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
    internal-label: APIs
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
  - id: e14a7f57-c82c-4874-a495-5d036cbbdc3d
    internal-label: Resource management
subfeature_v2:
  - id: b70a979b-965d-47a9-a360-e7ec2a19b8c1
    internal-label: Digital content and documents
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 9e08c421a53c7ca499715fa8e32be6c10fbde1d9
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 10%
---
# Adobe Marketo Engage MCP-Modul

Mit dem Adobe Marketo Engage MCP-Modul können Sie eine Aufforderung in natürlicher Sprache an den MCP-Server (Model Context Protocol) von Adobe Marketo Engage senden, indem Sie ein KI-Modell verwenden, um die Anfrage zu interpretieren, und Marketos eigene Tools aufrufen, um sie zu erfüllen. Im Gegensatz zu einem herkömmlichen Marketo-Connector, bei dem jedes Modul eine feste Aktion ausführt, z. B. „Lead erstellen“, verfügt dieser Connector über ein einziges Modul, das eine offene Anweisung in einfachem Englisch akzeptiert und es der KI ermöglicht, zu entscheiden, welche Marketo-Vorgänge erforderlich sind, um sie zu erfüllen.

Dieser Connector ist speziell für Marketo Engages eigenen MCP-Server

Informationen zum Verbinden mit MCPs für andere Anwendungen finden Sie unter [Hinzufügen einer KI-Eingabeaufforderung zu Ihrem Szenario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: Verfügbar für Organisationen mit betriebsbasierten Lizenzen</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

* Sie müssen über ein Adobe Marketo Engage-Konto und eine gültige Marketo-Instanz verfügen.

## Adobe Marketo Engage MCP mit Workfront Fusion verbinden {#connect-adobe-marketo-engage-mcp-to-workfront-fusion}

Sie können direkt aus dem Adobe Marketo Engage-MCP-Modul heraus eine Verbindung zu Ihrer Marketo-Instanz herstellen.

1. Klicken Sie im MCP-Modul von Adobe Marketo Engage **Hinzufügen** neben dem Feld **Verbindung**.
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
          <p>Geben Sie einen Namen für die neue Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>
          <p>Wählen Sie aus, ob eine Verbindung zu einem Service-Konto oder einem persönlichen Konto hergestellt werden soll.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>
          <p>Geben Sie die Client-ID für Ihren Marketo REST-API-Service ein, wie in Marketo LaunchPoint erstellt.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>
          <p>Geben Sie das Client-Geheimnis für Ihren Marketo REST-API-Service ein, wie in Marketo LaunchPoint erstellt.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Munchkin ID]</td>
        <td>
          <p>Geben Sie die Munchkin-ID Ihrer Marketo-Instanz ein (z. B. `123-ABC-456`). Die Munchkin-ID wird in Marketo unter <b>Admin → Munchkin</b> angezeigt.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Klicken Sie **Fortfahren**, um die Verbindung herzustellen und zum Modul zurückzukehren.

>[!IMPORTANT]
>
> * Verwenden Sie einen dedizierten Marketo-Benutzer, der nur über eine API verfügt, mit den Mindestrollen und -berechtigungen, die für das Szenario erforderlich sind, anstatt ein Administratorkonto wiederzuverwenden.
> * Beim Erstellen der Verbindung werden die Anmeldeinformationen nicht überprüft. Fusion speichert sie ohne Testaufruf, sodass die Verbindung erfolgreich erstellt werden kann, selbst wenn ein Wert falsch eingegeben oder falsch eingegeben wurde. Wenn eine Berechtigung falsch ist, tritt der Fehler normalerweise erst später auf, wenn das Modul zum ersten Mal versucht, Marketo zu erreichen, oder wenn die Tool-Listen nicht geladen werden können.

## Das Modul: „Benutzeraufforderung verarbeiten“

Dies ist das einzige Modul, das der Connector bereitstellt. In einem Szenario wird sie verwendet, indem Folgendes bereitgestellt wird:

1. **Connection** - die oben erstellte Marketo-Verbindung.
2. **Geben Sie Ihre Eingabeaufforderung ein** - die Anweisung in einfachem Englisch (z. B. „Finden Sie jeden Lead, der in der letzten Woche zur Liste der Webinare im Frühjahr hinzugefügt wurde, und teilen Sie mir mit, für welchen der Firmennamen nicht festgelegt wurde„).
3. **Tools** (optional) — siehe unten. Diese Felder werden nur angezeigt, wenn eine Verbindung ausgewählt ist.
4. **LLM-Schlüssel** (optional, erweitert) — unten beschrieben.

Die endgültige Antwort der KI wird als Text zurückgegeben, plus ein vollständiges Audit-Protokoll darüber, was bei der Erstellung dieser Antwort passiert ist.

## Adobe Marketo Engage MCP-Modul und seine Felder

### Benutzeraufforderung verarbeiten

Dieses Aktionsmodul sendet eine englischsprachige Anweisung an den MCP-Server von Adobe Marketo Engage und gibt die Antwort der KI zurück.

<table style="table-layout:auto"> 
 <col/>
 <col/>
 <tbody>
  <tr>
   <td role="rowheader">LLM-<i> (optional, erweitert)</i></td>
   <td><p>Standardmäßig verarbeitet dieses Modul Ihre Eingabeaufforderung mit dem eigenen KI-Service von Adobe und Sie müssen keinen Schlüssel auswählen.</p><p>Um stattdessen Ihren eigenen KI-Anbieter zu verwenden, wählen Sie einen vorhandenen LLM-Schlüssel aus oder erstellen Sie einen neuen, indem Sie auf <b>Hinzufügen</b> klicken und die folgenden Informationen eingeben:</p>
    <ul>
     <li><b>Schlüsselname</b>: Geben Sie einen Namen für den neuen Schlüssel ein.</li>
     <li><b>LLM</b>: Wählen Sie das große Sprachmodell aus, mit dem dieser Schlüssel verknüpft ist. Unterstützte Anbieter sind OpenAI, Anthropic Claude und Amazon Bedrock.</li>
     <li><b>Schlüssel</b>: Geben Sie den API-Schlüssel für den ausgewählten Anbieter ein oder ordnen Sie ihn zu.</li>
     <li><b>Modell</b>: Wählen Sie das LLM-Modell aus, das der Schlüssel verwenden soll.</li>
     <li><b>Andere Felder</b>: Geben Sie Werte für alle anderen Felder ein, die für Ihr LLM erforderlich sind.</li>
    </ul>
   </td>
  </tr>
  <tr>
   <td role="rowheader">Verbindung</td>
   <td><p>Anweisungen zum Verbinden Ihres Marketo-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-marketo-engage-mcp-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Marketo Engage MCP mit Workfront Fusion</a> in diesem Artikel.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Benutzeraufforderung</td>
   <td><p>Geben Sie die Anweisung ein, die die KI ausführen soll, oder kartieren Sie sie in einfachem Englisch.</p><p>Beispiel: <i>Finden Sie alle Leads, die in den letzten 7 Tagen zur Liste der Frühjahrs-Webinare hinzugefügt wurden, und fassen Sie zusammen, welche Branchen am häufigsten vorkommen.</i></p></td>
  </tr>
 </tbody>
</table>

### Modulausgabe

Die Ausgabe ist ein einzelnes Bundle, das Folgendes enthält:

* Antwort: Die endgültige Antwort der KI als Text. Sie können diese Daten nachfolgenden Modulen zuordnen.
* Audit-Protokoll: Der detaillierte Datensatz des Durchgangs, einschließlich Sitzungs-ID, ursprünglicher Eingabeaufforderung, Start- und Endzeiten, Gesamtdauer, Gesamtstatus, endgültiger Antwort und einer Tool-Aufrufliste. In jedem Tool-Aufrufeintrag wird aufgezeichnet, welches Marketo-Tool ausgeführt wurde, welche Argumente verwendet wurden, welche Ausgabe ausgegeben wurde, welche Start- und Endzeit und -dauer ausgeführt wurde, ob der Aufruf erfolgreich war und welche Reihenfolge der Aufruf in der Sequenz vorgenommen wurde.
* Zusammenfassung: Derselbe Durchgang verkürzt sich auf Zahlen: Gesamtzahl der Tool-Aufrufe, erfolgreiche Aufrufe, fehlgeschlagene Aufrufe, Verarbeitungszeit und Status.

### KI-Modelle

Standardmäßig verwendet das Modul automatisch den eigenen verwalteten KI-Service von Adobe, ohne dass Schlüssel oder Anmeldeinformationen eingegeben werden müssen.

Sie können stattdessen einen bestimmten LLM-Schlüssel auswählen, um OpenAI, Anthropic Claude oder Amazon Bedrock zu verwenden, wenn Ihr Unternehmen über ein Konto mit einem dieser Schlüssel verfügt.

### Auswählen, welche Marketo-Aktionen die KI ausführen darf

Nachdem eine Verbindung ausgewählt wurde, fragt das Modul den Marketo-MCP-Server, welche Tools es anbietet, und präsentiert diese als Mehrfachauswahllisten, die jeweils zeigen, wie viele Tools es enthält:

* Schreibgeschützte Tools: Aktionen, die nur etwas nachschlagen und nichts ändern, z. B. einen Lead finden, Kampagnenmitglieder auflisten oder die Details eines Programms lesen.
* Tools zum Schreiben/Löschen: Aktionen, die etwas ändern, z. B. das Erstellen oder Aktualisieren eines Leads, das Hinzufügen einer Person zu einer Liste, das Aktivieren einer Kampagne oder das Genehmigen oder Senden einer E-Mail.
* Andere Tools: Eine dritte Liste, die nur angezeigt wird, wenn der Marketo-Server Tools anbietet, die nicht als schreibgeschützt gekennzeichnet sind. Diese werden separat angezeigt und nicht als sicher oder unsicher angenommen. Wenn der Server alles kennzeichnet, wird diese Liste nicht angezeigt.

Wenn keine Tools ausgewählt sind, kann die KI sie alle verwenden. Sie können eine Liste auf bestimmte Aktionen beschränken. Wenn Sie beispielsweise nur zwei bestimmte „write“-Aktionen auswählen und „read-only“ belassen, kann die KI frei nachschlagen, was sie benötigt, aber nur diese zwei spezifischen Arten von Änderungen vornehmen. Wenn Sie eine Liste leer lassen, sind alle Aktionen in dieser Kategorie zulässig. Um die KI einzuschränken, müssen Sie aktiv auswählen, welche spezifischen Aktionen in dieser Kategorie zulässig sind. Auf diese Weise können Sie sicherstellen, dass die KI keine unerwarteten destruktiven Maßnahmen gegen Live-Marketing-Daten ergreift, während sie ihr weiterhin die Möglichkeit gibt, Informationen frei zu sammeln.

Da die Listen live vom Marketo-Server gelesen werden, können sich die exakten angezeigten Tools ändern, wenn Adobe diesen Server aktualisiert.

### Kein persistenter Gesprächsverlauf

Jede Ausführung dieses Moduls ist eine einzelne, in sich abgeschlossene Ausführung. Die KI kann keine Folgefrage stellen und auf eine Antwort warten. Stattdessen muss sie ihr bestes Urteil fällen und in einem Schritt eine vollständige, endgültige Antwort geben. Wenn eine Anfrage mehrdeutig ist, geht die KI von einer vernünftigen Annahme aus, gibt diese Annahme als Teil ihrer Antwort an und fährt fort. Er wird nicht anhalten und den Benutzer bitten, dies zu klären, da es keine Möglichkeit gibt, eine Antwort innerhalb eines Durchgangs zu erhalten.

Die KI wird auch angewiesen, Fakten mit einem Tool-Aufruf zu überprüfen, anstatt sich auf den Arbeitsspeicher zu verlassen, da sich die Marketo-Daten möglicherweise seit der vorherigen Ausführung geändert haben.

Die KI führt nur dann eine Schreib-, Aktualisierungs- oder Löschaktion durch, wenn bei der Eingabeaufforderung tatsächlich nach einer Aktion gefragt wurde. Es führt keine Aktion aus, die nicht angefordert wurde, einschließlich des Aktivierens oder Deaktivieren von Kampagnen, des Erstellens oder Löschens von Leads und Listen und des Genehmigens oder Sendens von E-Mails, selbst in der gleichen Ausführung, in der es etwas Anderes tut, worum der Benutzer gebeten hat.

Da jede Ausführung unabhängig ist, hat die KI keinen Speicher einer vorherigen Ausführung allein. Ein Szenario, das ein Chat-ähnliches Erlebnis mit mehreren Umdrehungen möchte, muss diesen Verlauf explizit als Teil der neuen Eingabeaufforderung bereitstellen, z. B. indem die vorherige Frage und Antwort im Datenspeicher von Fusion gespeichert oder zwischen Modulen übergeben wird und sie zu Beginn der neuen Eingabeaufforderung als Text eingeschlossen wird, gefolgt von der neuen Frage. Es gibt keine Sitzungs- oder Konversations-ID, die sich automatisch vorherige Ausführungen merkt.

## Beispiel-Prompts

Sie können Eingabeaufforderungen wie die folgenden verwenden:

* *Listen Sie die Leads auf, die in den letzten sieben Tagen am Programm „Produkteinführung im 3. Quartal“ teilgenommen haben, und fassen Sie zusammen, aus welchen Branchen sie stammen.*
* *Überprüfen Sie, ob die intelligente Kampagne „Willkommensreihe“ derzeit aktiv ist, und sagen Sie mir, wie viele Personen daran beteiligt sind.*
* *Finden Sie das Formular auf unserer Preisseite und sagen Sie mir, welche Felder als Pflichtfelder markiert sind.*
* *Fügen Sie den Lead mit E-Mail-`jane@example.com` zur statischen Liste &quot;VIP-Kunden“ hinzu.*
* *Fassen Sie die Leistung jeder E-Mail im Programm „Frühling-Newsletter“ zusammen.*

<!--

## What a content writer should NOT claim

* Connection form: Do not describe the connection as an OAuth or "sign in with Adobe" flow. It is not one. It is three credential fields that the user copies out of Marketo's LaunchPoint and Munchkin admin pages. Screenshots or steps borrowed from the AEM MCP connector docs would be wrong here.
* Credential validation: Do not imply that the connection form validates the credentials. It saves them without testing them.
* Module scope: This is not a substitute for individual Marketo action modules. It is a single, flexible AI-driven module, not a set of deterministic single-purpose modules.
* Reliability: Results are AI-generated and can occasionally be imperfect, even with every safeguard above in place. This is appropriate for automation where a human is not reviewing every single run in real time, but it is not a guarantee of 100% deterministic behavior the way a traditional Marketo module is. This deserves extra emphasis for Marketo specifically, because a write action here can email real customers or alter real lead records.
* Tool restrictions: The read/write tool split limits what categories of Marketo actions the AI can take. It is not a way to sandbox or limit what the AI is capable of reasoning about or discussing in its answer text.
* Tool naming: Do not name specific Marketo MCP tools or actions unless they are verified against the live tool list. This document intentionally describes capability areas, such as leads, lists, campaigns, programs, emails, forms, snippets, and bulk operations, rather than exact tool names, since the server's exact tool set may evolve.
* API limits: Do not state Marketo API rate limits, quotas, or daily call caps as if this connector defines them. Any such limit comes from the user's own Marketo subscription and REST API allowance; verify with the Marketo team before publishing numbers.

## Reference links used while compiling this

* Adobe Marketo Engage MCP server (developer documentation):
  https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server

  -->
