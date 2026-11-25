---
title: Adobe Firefly Creative Production MCP-Module
description: Mit dem Adobe Firefly Creative Production MCP-Modul können Sie eine Eingabeaufforderung in natürlicher Sprache aus einem Workfront Fusion-Szenario senden und ein KI-Modell die von Ihnen ausgewählten Firefly Creative Production-Tools verwenden lassen.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: ee2719b9b3452b9203f2d0f4a550c87ff8a3b433
workflow-type: tm+mt
source-wordcount: '2087'
ht-degree: 5%
---
# Adobe Firefly Creative Production MCP-Module

Verwenden Sie den Adobe Firefly Creative Production MCP-Connector in Adobe Workfront Fusion, um Anforderungen in natürlicher Sprache mit Firefly Creative Production-Tools zu verarbeiten.

Der Connector erkennt die Tools, die über den verbundenen Firefly Model Context Protocol (MCP)-Server verfügbar sind. Sie können auswählen, welche Tools das Modul für eine Anfrage verwenden kann. Je nach den Tools, die Ihrem Adobe-Konto zur Verfügung stehen, und den Tools, die Sie im -Modul auswählen, kann eine Anfrage Folgendes bewirken:

* Entdecken Sie Workflows und Aktionen.
* Erstellen und Validieren von Workflows.
* Übermitteln von Ausführungen und Überprüfen ihres Fortschritts.
* Ausgabe-URLs abrufen.
* Speichern Sie bearbeitbare Workflow-Entwürfe, wenn sie von den Tools des Servers unterstützt werden.

Dieser Connector ist für die Firefly Creative-Produktion vorgesehen. Es handelt sich nicht um einen Firefly Boards-Connector und auch nicht um einen allgemeinen Connector für jede Creative Cloud-Anwendung.

Weitere Informationen zu MCP in Fusion-Szenarien finden Sie unter [Hinzufügen einer KI-Eingabeaufforderung zum Szenario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

<!-- BECKY CHECK ME: The request asks you to confirm the customer-facing name of the connector, its beta or release status, its availability, its access requirements, and screenshots with the product and engineering owners before publication. Confirm each item, and add a beta note at the top of the article if the connector is released as a beta. -->

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
   <p>Sie müssen auch über Zugriff auf die Adobe Firefly Creative-Produktion verfügen, wie <a href="#prerequisites">Voraussetzungen</a> in diesem Artikel beschrieben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Voraussetzungen

Bevor Sie das Adobe Firefly Creative Production MCP-Modul verwenden, benötigen Sie Folgendes:

* Zugriff auf Adobe Workfront Fusion in einer Umgebung, in der dieser Connector aktiviert ist.
* Ein Adobe-Konto mit dem Firefly Creative-Produktionszugriff und den Berechtigungen, die für die angeforderten Vorgänge erforderlich sind.
* Alle Credits oder Berechtigungen, die Sie zum Ausführen des Workflows benötigen.
* Entweder Zugriff auf Adobe Managed AI, den Ihr Fusion-Administrator konfiguriert hat, oder auf einen unterstützten LLM-Schlüssel, den Sie in den erweiterten Einstellungen des Moduls auswählen.

Die Firefly-Autorisierung und die LLM-Anmeldeinformationen dienen verschiedenen Zwecken. Durch Auswahl eines LLM-Schlüssels wird kein Zugriff auf Firefly-Tools gewährt.

## Adobe Firefly Creative Production MCP mit Workfront Fusion verbinden

1. Fügen Sie **[!UICONTROL Adobe Firefly Creative Production MCP]** > **[!UICONTROL Benutzereingabe verarbeiten]** zu Ihrem Szenario hinzu.
1. Klicken Sie **[!UICONTROL Hinzufügen]** neben dem Feld **[!UICONTROL Verbindung]**.
1. Füllen **[!UICONTROL im Fenster]** Verbindung erstellen“ die folgenden Felder aus:

   <table style="table-layout:auto">
    <col>
    <col>
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
1. Befolgen Sie den Autorisierungsfluss, melden Sie sich mit dem entsprechenden Adobe-Konto an und autorisieren Sie den Zugriff.
1. Kehren Sie zum Modul zurück und überprüfen Sie die Tools, die für die Verbindung geladen werden.

Workfront Fusion verwaltet die Client-Registrierung und Token-Verwaltung für OAuth. Sie geben kein Zugriffstoken, keine Client-ID, kein Client-Geheimnis und keinen API-Schlüssel ein. Ihr Administrator muss die Einrichtung für diesen Fluss abgeschlossen haben, bevor Sie eine Verbindung herstellen können.

Wenn die Autorisierung fehlschlägt oder Sie die erwarteten Tools nicht sehen, bestätigen Sie Ihren Zugriff und die Konfiguration Ihrer Umgebung mit Ihrem Administrator.

<!-- BECKY CHECK ME: The Environment and Type fields are described the same way as in the Adobe Fusion MCP connection. The screenshot shows only the selected values (Production and Service account). Confirm the available options for each field, and whether a personal account is supported. -->

## Adobe Firefly Creative Production MCP-Modul und seine Felder

### Benutzeraufforderung verarbeiten

Dieses Aktionsmodul verarbeitet Ihre Eingabeaufforderung mit dem ausgewählten LLM und den von Ihnen zugelassenen Firefly Creative-Produktions-Tools.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL LLM key] <i>(optional, erweitert)</i></td> 
   <td> <p>Lassen Sie dieses Feld leer, um die von Ihrem Fusion-Administrator konfigurierte Adobe Managed AI zu verwenden. Um stattdessen Ihren eigenen Schlüssel zu verwenden, wählen Sie einen vorhandenen OpenAI-, Anthropic- oder Amazon Bedrock-Schlüssel aus oder klicken Sie auf <b>[!UICONTROL Hinzufügen]</b>, um einen Schlüssel zu erstellen.</p><p>Ihre Firefly-Anmeldung ist nicht mit Ihren LLM-Anmeldedaten identisch.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Die Adobe Firefly Creative-Produktionsverbindung, die das Modul verwendet, um Tools zu finden und aufzurufen. Anweisungen finden Sie unter <a href="#connect-adobe-firefly-creative-production-mcp-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Firefly Creative Production MCP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Schreibgeschützte Tools] <i>(Optional)</i></td> 
   <td> <p>Wählen Sie die Tools aus, die der Server als schreibgeschützt kennzeichnet. Um jedes aktuell aufgelistete Tool auszuwählen, klicken Sie auf <b>Alle auswählen</b>.</p><p>Die Anzahl der aufgelisteten Tools wird im Feld angezeigt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Schreib-/Löschwerkzeuge] <i>(Optional)</i></td> 
   <td> <p>Wählen Sie die Tools aus, die der Server nicht als schreibgeschützt kennzeichnet. Mit diesen Vorgängen können Daten geändert oder Workflows ausgeführt werden. Um jedes aktuell aufgelistete Tool auszuwählen, klicken Sie auf <b>Alle auswählen</b>.</p><p>Die Anzahl der aufgelisteten Tools wird im Feld angezeigt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Other Tools (unbekannte Berechtigungen)] <i>(Optional)</i></td> 
   <td> <p>Wählen Sie Werkzeuge aus, die über keine erkannte schreibgeschützte Anmerkung verfügen. Dieses Feld wird nur angezeigt, wenn solche Tools verfügbar sind. Überprüfen Sie, wie sich diese Tools verhalten, bevor Sie sie aktivieren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Eingabeaufforderung eingeben]</td> 
   <td> <p>Beschreiben Sie die Workflow-Erkennung, -Komposition oder -Ausführung, die Sie möchten. Die maximale Länge beträgt 10.000 JavaScript-Zeichenfolgeneinheiten. Einige Charaktere, darunter viele Emojis, zählen als zwei Einheiten.</p><p>Sie müssen die Ausführung oder Veröffentlichung bei Bedarf explizit anfordern. Bei Ausführung eines Workflows können Guthaben verbraucht werden. Asynchrone Ausführungen können eine Batch-ID zurückgeben, bevor die Ausführung abgeschlossen ist.</p> </td> 
  </tr> 
 </tbody> 
</table>

Das Feld **[!UICONTROL LLM key]** wird angezeigt, wenn Sie **[!UICONTROL Erweiterte Einstellungen anzeigen]** auswählen.

<!-- BECKY CHECK ME: The screenshot does not show the Other tools (unknown permissions) field, because it appears only when the server returns tools without a read-only annotation. Confirm its label, and confirm the order of the fields. Also confirm that the tool lists are not required. -->

Die Toollisten variieren je nach Verfügbarkeit des Servers und dem Zugriff auf Ihr Konto. Die Anzahl der Tools wird in der Beschriftung der einzelnen Selektoren angezeigt.

#### Wählen Sie die Werkzeuge aus, die das Modul verwenden kann

* Das Modul kann nur die von Ihnen ausgewählten Werkzeuge verwenden.
* Wenn Sie eine Kategorie leer lassen, kann das Modul keine Tools aus dieser Kategorie verwenden.
* Wenn Sie alle Kategorien leer lassen, verarbeitet das Modul die Eingabeaufforderung ohne Werkzeuge. Es hat nicht Zugriff auf jedes Tool.
* **[!UICONTROL Alle auswählen]** wählt jedes Tool aus, das derzeit in dieser Kategorie aufgeführt ist. Es enthält nicht automatisch Tools, die später hinzugefügt werden.
* Wenn ein ausgewähltes Tool nicht mehr verfügbar ist oder in eine andere Kategorie verschoben wird, öffnen Sie das Modul erneut und überprüfen Sie Ihre Auswahl.

>[!NOTE]
>
>Die Anmerkungen des Servers helfen, Tools zu kategorisieren, sie gewährleisten jedoch keine Berechtigungen. Aktivieren Sie nur die Tools, die für Ihr Szenario erforderlich sind.

#### Ausgabe

Das -Modul gibt die folgenden Informationen unter &quot;**[!UICONTROL &quot;]**. Sie können sie in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Antwort] (<code>data.response</code>)</td> 
   <td> <p>Die endgültige Textantwort. Ihr Inhalt hängt von der Eingabeaufforderung und den Ergebnissen des Tools ab. Es wird nicht garantiert, dass es sich um eine URL oder ein strukturiertes JSON handelt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Audit-Protokoll] (<code>data.auditTrail</code>)</td> 
   <td> <p>Details zur Verarbeitung der Eingabeaufforderung und der Tool-Aufrufe, einschließlich der Argumente, Ergebnisse, Timing und Erfolgsinformationen. Verarbeiten Sie diese Details entsprechend den Anforderungen Ihres Unternehmens an die Datenverarbeitung.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zusammenfassung] (<code>data.summary</code>)</td> 
   <td> <p>Anzahl der Tool-Aufrufe, Verarbeitungszeit und Ausführungsstatus. Überprüfen Sie die Zusammenfassung zusammen mit der Antwort und dem Audit-Protokoll, einschließlich aller <code>partial_success</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL LLM-Nutzung] (<code>data.usage</code>)</td> 
   <td> <p>Optional. Die gesamte Token-Nutzung aus den festgestellten LLM-Antworten. Hierbei handelt es sich nicht um die Anbieterfakturierung, die Firefly-Kreditnutzung oder die LLM-Aktivität innerhalb des Firefly-Servers, die von Fusion nicht beobachtet werden kann.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### LLM-Nutzungsfelder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>status</code></td> 
   <td> <p>Eine der folgenden Möglichkeiten:</p><ul><li><code>complete</code>: Jede beobachtete Anfrage wird von allen Haupt-Token-Zählungen abgedeckt.</li><li><code>partial</code>: Einige Nutzungsinformationen fehlen.</li><li><code>unavailable</code>: Es wurden Anfragen beobachtet, aber es wurde keine verwendbare Nutzung gemeldet.</li><li><code>not_applicable</code>: Es wurden keine LLM-Anfragen beobachtet.</li></ul> </td> 
  </tr> 
  <tr> 
   <td><code>llmRequests</code></td> 
   <td> <p>Die Anzahl der LLM-Anfragen, die die Laufzeit beobachtet hat.</p> </td> 
  </tr> 
  <tr> 
   <td><code>requestsWithUsage</code></td> 
   <td> <p>Die Anzahl der beobachteten Anfragen mit nutzbaren Token-Nutzungsinformationen.</p> </td> 
  </tr> 
  <tr> 
   <td><code>inputTokens</code>, <code>outputTokens</code>, <code>totalTokens</code></td> 
   <td> <p>Die Gesamtzahl zählt. Jede Zählung wird <code>null</code>, wenn eine beobachtete Anfrage diese Zählung nicht meldet oder wenn keine Anfragen beobachtet wurden. Eine gemeldete Null bleibt gleich null.</p> </td> 
  </tr> 
  <tr> 
   <td><code>cacheReadInputTokens</code>, <code>cacheWriteInputTokens</code></td> 
   <td> <p>Optionale Zählungen für zwischengespeicherte Token. Diese Felder werden ausgelassen, wenn keine Anfrage jemals eine Zahl meldet. Sie sind <code>null</code>, wenn nur einige Anfragen eine Zahl melden, und nur numerisch, wenn jede Anfrage eine Zahl meldet. Addieren Sie diese Zahlen nicht zu den Gesamtwerten.</p> </td> 
  </tr> 
 </tbody> 
</table>

Der Hauptverwendungsstatus kann `complete` werden, während ein Cache-Feld `null` wird. Der Nutzungsstatus ist unabhängig vom Ausführungsstatus. Wenn die Laufzeit keine Nutzungsinformationen bereitstellt, fehlt die Nutzungssammlung, anstatt eine Null anzuzeigen.

## Ausführung des Moduls

* **Einige Vorgänge sind asynchron.** Eine Anfrage kann eine Batch-ID zurückgeben, bevor die Ausgabe verfügbar ist. Bei längeren Aufträgen verwenden Sie separate Ausführungen, um die Anfrage zu senden und später ihren Status zu überprüfen und die Batch-ID zwischen ihnen zu speichern. Verlassen Sie sich nicht auf eine Antwort, die nur eine URL für dieses Design enthält.
* **Fehler erzeugen Modulfehler.** Bei Autorisierung, Validierung und fehlgeschlagener Laufzeitverarbeitung können Modulfehler anstelle eines Ausgabepakets auftreten. Verwenden Sie eine Route zur Fehlerbehandlung in Fusion.
* **Eine Antwort ist nicht erfolgreich.** Das Modul kann eine Antwort zurückgeben, selbst wenn einige Vorgänge fehlgeschlagen sind. Überprüfen Sie die Zusammenfassung, das Audit-Protokoll und die Ergebnisse des Tools, bevor Sie sich auf die Antwort verlassen.
* **Eine Ausgabe-URL ist keine heruntergeladene Datei.** Der Connector gibt Text- und Tool-Ergebnisse zurück, keine Binärdatei. Um die Datei in Fusion zu importieren, fügen Sie ein HTTP-Modul hinzu, das die URL herunterlädt.
* **Beim Ausführen eines Workflows können Credits verwendet werden.** Bildgenerierung und Workflow-Ausführung können Credits verbrauchen. Bestätigen Sie die Nutzung und die Berechtigungen, die für Ihr Konto gelten. Die Verwendung des LLM-Tokens ist kein Abrechnungs- oder Kreditbericht für Firefly.
* **Eingabeaufforderungsanweisungen garantieren keinen einzigen Durchlauf.** Eine Anweisung in der Eingabeaufforderung, z. B. die Übermittlung nur eines Batches, garantiert nicht, dass eine Anfrage genau einmal verarbeitet wird. Steuern Sie weitere Zustellversuche und doppelte Anfragen in Ihrem Szenario.
* **Die Verarbeitung hat Grenzen.** Bei der Verarbeitung gibt es zusätzlich zu den Ausführungsbeschränkungen des Szenarios Längenbeschränkungen für Tools, Iterationen und Ausgaben. Gehen Sie nicht davon aus, dass das Modul unbegrenzt abfragt.

## Beispiele

### Workflows erkennen, ohne einen auszuführen

Wählen Sie die schreibgeschützten Tools aus, die Sie zur Erkennung von Workflows benötigen, und geben Sie dann eine Eingabeaufforderung wie die folgende ein:

```text
List the Firefly Creative Production workflows available to my account.
Summarize what each workflow does and what inputs it requires.
Do not create, modify, submit, or publish anything.
```

### Ein Bild anfordern

Wählen Sie die Tools aus, die Sie für die Erstellung oder Auswahl eines Workflows benötigen, validieren Sie ihn, senden Sie ihn, überprüfen Sie seinen Fortschritt und rufen Sie die Ausgaben ab. Die Toolnamen und die Verfügbarkeit können variieren. Geben Sie dann eine Eingabeaufforderung wie die folgende ein:

```text
Generate one photorealistic image of a black dog on a sunny windowsill.
Submit one generation batch only and check that same batch for completion
within the available execution limits. Do not publish or submit another
generation.

On success, return only the actual downloadable image URL as plain text,
without Markdown, quotes, labels, or explanation. Never invent a URL or
return a workflow or status-page URL instead.

If the run fails or times out, report the failure honestly instead of
returning a URL. Do not generate another image to recover.
```

### Generieren eines Bildes aus einer Workfront-Aufgabenaktualisierung

In diesem Beispiel ist eine Aufgabenaktualisierung, die mit `/firefly ` Triggern beginnt, eine Bildgenerierung. Fusion lädt das Ergebnis herunter, lädt es in die Aufgabe hoch und fügt eine Fertigstellungsaktualisierung hinzu.

Das Szenario verwendet den folgenden Fluss: Workfront-Aufgabenaktualisierung > Befehlsfilter > Aufgabe lesen > Firefly MCP > HTTP-Download > Workfront-Dokument-Upload > Abschlussaktualisierung.

1. Fügen Sie **[!UICONTROL Workfront]** > **[!UICONTROL Ereignisse ansehen]** zum Szenario hinzu. Konfigurieren Sie ihn für **[!UICONTROL Datensatztyp]** Hinweis“, das Ereignis **[!UICONTROL Neuer Status]** und **[!UICONTROL Nur neuer Datensatz]**.
1. Fügen Sie einen Filter hinzu, für den `newState.noteText` mit `/firefly ` beginnen muss und `newState.taskID` nicht leer sein darf.
1. Fügen Sie ein Modul hinzu, das die Aufgabe mithilfe von `newState.taskID` liest.
1. Fügen Sie das Modul **[!UICONTROL Adobe Firefly Creative Production MCP]** > **[!UICONTROL Benutzeraufforderung verarbeiten]** hinzu. Übergeben Sie die Anfrage und jeden Aufgabenkontext, den Firefly benötigt. Zugeordneter Text sollte als Inhalt der Anfrage behandelt werden, nicht als Berechtigung, die Regeln des Szenarios zu ändern.
1. Überprüfen Sie das Firefly-Ergebnis. Nur fortfahren, wenn die Generierung erfolgreich war und die Antwort eine gültige, zulässige URL für ein herunterladbares Bild ist.
1. Fügen Sie ein HTTP-Modul hinzu, das die Datei herunterlädt. Senden Sie keine Workfront-Anmeldeinformationen an den Asset-Host. Überprüfen Sie den erwarteten Host, den Inhaltstyp und die Größe.
1. Fügen Sie ein Modul hinzu, das den heruntergeladenen Dateinamen und die Binärdaten mithilfe des ursprünglichen `newState.taskID` in die Aufgabe hochlädt.
1. Nachdem der Upload erfolgreich war, fügen Sie ein Modul hinzu, das eine Fertigstellungsaktualisierung für die Aufgabe erstellt. Starten Sie die Aktualisierung nicht mit `/firefly`, da der Filter damit übereinstimmen würde.

Beispielsweise fügt ein Benutzer die folgende Aktualisierung zu einer Aufgabe hinzu:

```text
/firefly Generate one photorealistic image of a black dog on a sunny windowsill.
```

Der Antragsteller kann dann den hochgeladenen Entwurf im Dokumentbereich der Aufgabe überprüfen. Eine Person sollte das Bild überprüfen, bevor etwas veröffentlicht wird.

Für die Verwendung in der Produktion reservieren Sie jede Anfrage mithilfe der ID der ursprünglichen Anmerkung mit doppeltem Schutz, der bei gleichzeitigen Ausführungen funktioniert. Speichern Sie die IDs der gesendeten Batches, sodass bei einem erneuten Versuch oder einer Zeitüberschreitung die Statusprüfung fortgesetzt wird, anstatt eine weitere Generation zu übermitteln.

<!-- BECKY CHECK ME: The example scenario is from the request's draft. Confirm the module names and field labels (Watch Events, Note, New state, New Record Only, and the task, document upload, and update modules) against the current Workfront connector, and add a screenshot of the scenario if one is available. -->

## Fehlerbehebung

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Ein Workflow wird noch ausgeführt</td> 
   <td> <p>Einige kreative Vorgänge sind asynchron. Bei längeren Aufträgen senden Sie die Anfrage in einem Durchgang und überprüfen Sie den Status in einem späteren Durchgang. Speichern Sie die Batch-ID zwischen den Ausführungen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Das Modul meldet einen Fehler</td> 
   <td> <p>Autorisierung, Validierung und fehlgeschlagene Laufzeitverarbeitung können zu Modulfehlern führen. Fügen Sie eine Route zur Fehlerbehandlung in Fusion zu Ihrem Szenario hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Das Modul gibt eine Antwort zurück, aber einige Vorgänge sind fehlgeschlagen</td> 
   <td> <p>Überprüfen Sie die Zusammenfassung, das Audit-Protokoll und die Ergebnisse des Tools. Eine Antwort allein zeigt nicht an, dass das Bild generiert oder hochgeladen wurde.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Es gibt eine URL, aber keine Datei in Fusion</td> 
   <td> <p>Der Connector lädt keine Dateien herunter. Fügen Sie ein HTTP-Modul hinzu, das die URL herunterlädt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ein ausgewähltes Tool ist nicht verfügbar</td> 
   <td> <p>Öffnen Sie das -Modul, aktualisieren Sie die verfügbaren Tools und aktualisieren Sie Ihre Auswahl.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Der Workflow dauert länger als eine Modulausführung</td> 
   <td> <p>Bei der Verarbeitung gibt es zusätzlich zu den Ausführungsbeschränkungen des Szenarios Längenbeschränkungen für Tools, Iterationen und Ausgaben. Teilen Sie die Arbeit auf mehrere Ausführungen auf und speichern Sie die Batch-ID.</p> </td> 
  </tr> 
 </tbody> 
</table>
