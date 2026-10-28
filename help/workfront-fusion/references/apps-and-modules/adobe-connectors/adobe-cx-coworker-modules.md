---
title: Adobe CX Enterprise Coworker-Module
description: Verwenden Sie den Adobe CX Enterprise Coworker-Connector in Adobe Workfront Fusion, um eine Eingabeaufforderung in natürlicher Sprache an einen Kollegen zu senden und seine Antwort in einem Szenario zu verwenden.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 6efe84af0487893a3c33ba2bf6e3db5200f25446
workflow-type: tm+mt
source-wordcount: '1974'
ht-degree: 7%
---
# Adobe CX Enterprise Coworker-Module

Verwenden Sie den Adobe CX Enterprise Coworker-Connector in Adobe Workfront Fusion, um eine Eingabeaufforderung in natürlicher Sprache an einen Kollegen zu senden und seine Antwort in einem Szenario zu verwenden. Ein Mitarbeiter interpretiert Ihre Anfrage und kann die Ihrem Konto zur Verfügung stehenden Tools verwenden, um die Arbeit auszuführen.

Der Connector bietet zwei Module:

* **[!UICONTROL Eingabeaufforderung ausführen]** startet eine neue Anfrage und wartet standardmäßig auf das Ergebnis.
* **[!UICONTROL Ausführungsstatus abrufen]** prüft eine Anfrage, die Sie zuvor gestartet haben.

## Zugriffsanforderungen

<!-- BECKY CHECK ME: This table is copied from other Fusion connector articles. The source material does not list access requirements, but says you need an Adobe account that has access to Coworker. Confirm the requirements and whether Coworker needs its own license or entitlement. -->

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

## Voraussetzungen

Sie müssen über ein Adobe-Konto verfügen, das Zugriff auf Adobe CX Enterprise Coworker hat.

## Verbinden von Adobe CX Enterprise Coworker mit Workfront Fusion

Melden Sie sich mit einem Adobe-Konto an, das Zugriff auf Coworker und alle Services hat, die für Ihre Anfrage benötigt werden.

So erstellen Sie eine Verbindung:

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
      <tr>
        <td role="rowheader">Client-ID</td>
        <td>
          <p>Geben Sie eine optionale Überschreibung für diese Verbindung ein oder ordnen Sie sie zu. Verwenden Sie andernfalls die plattformverwaltete Client-ID dieses Kontotyps. Registrieren Sie die angezeigte Fusion-Callback-URL für das dedizierte Coworker-Konto.</p>
        </td>
      <tr>
        <td role="rowheader">Client-Geheimnis</td>
        <td>
          <p>Geben Sie eine optionale Überschreibung für diese Verbindung ein oder ordnen Sie sie zu. Verwenden Sie andernfalls das plattformverwaltete ClientSecret dieses Kontotyps. Verwenden Sie die für die konfigurierte IMS-Umgebung ausgestellten Anmeldeinformationen.</p>
        </td>
    </tbody>
   </table>

1. Klicken Sie auf **[!UICONTROL Fortfahren]**.

Wenn Sie sich nicht anmelden oder einen erforderlichen Dienst nicht verwenden können, wenden Sie sich an Ihren Administrator.

## Adobe CX Enterprise Coworker-Module und ihre Felder

>[!WARNING]
>
>Geben Sie in einer Eingabeaufforderung niemals Kennwörter oder andere Anmeldeinformationen ein.

### Ausführungsstatus abrufen

Dieses Aktionsmodul überprüft den aktuellen Status einer von (**[!UICONTROL einer Eingabeaufforderung)]** Aufgabe.

Dieses Modul überprüft die Aufgabe einmal. Sie startet keine neue Aufgabe und überprüft sie erst, wenn die Aufgabe abgeschlossen ist. Wenn das Ergebnis noch aussteht, überprüfen Sie es später erneut.

>[!NOTE]
>
>Konvertieren Sie die Aufgaben-ID nicht in eine Zahl, runden Sie sie nicht oder formatieren Sie sie nicht neu. Wenn ein Kollege die ursprüngliche Eingabeaufforderung sofort ohne Aufgaben-ID beantwortet hat, müssen Sie den Status nicht überprüfen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Rohergebnis einschließen] <i>(Optional, erweitert)</i></td> 
   <td> <p>Diese Option ist standardmäßig deaktiviert. Schließen Sie die vollständige Antwort des Kollegen in die Ausgabe ein. Die Antwort kann vertrauliche Informationen enthalten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie dieselbe Verbindung aus, die Sie in der ursprünglichen <b>[!UICONTROL Run a Prompt]</b>-Ausführung verwendet haben.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Aufgaben-ID]</td> 
   <td> <p>Ordnen Sie die von <b>[!UICONTROL Run a Prompt] zurückgegebene Aufgaben-ID </b>. Behalten Sie den Text genau so bei, wie er zurückgegeben wurde.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Eingabeaufforderung ausführen

Dieses Aktionsmodul sendet eine Anweisung an einen Kollegen, z. B. die Zusammenfassung von Text oder die Erfassung von Informationen mithilfe von Tools, die für Ihr Konto verfügbar sind.

Bei jedem Durchgang wird die Eingabeaufforderung einmal gesendet und eine neue Konversation gestartet. Sie müssen kein KI-Modell auswählen oder einen separaten KI-Provider-Schlüssel angeben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindung]</td> 
   <td> <p>Wählen Sie Ihre Verbindung mit Kollegen aus. Anweisungen finden Sie unter <a href="#connect-adobe-cx-coworker-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe CX Enterprise Coworker mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Benutzeraufforderung]</td> 
   <td> <p>Geben Sie Ihre Anweisung ein. Sie können mehrere Zeilen verwenden und Informationen aus früheren Modulen zuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Auf Abschluss warten] <i>(Optional, erweitert)</i></td> 
   <td> <p>Diese Option ist standardmäßig aktiviert. Aktivieren Sie diese Option, wenn das Modul auf den Abschluss der Aufgabe warten soll oder Aufmerksamkeit benötigt wird. Ausschalten, um das ursprüngliche Ergebnis sofort zurückzugeben.</p><p>Weitere Informationen finden Sie unter <a href="#wait-for-completion">Auf Abschluss warten</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Rohergebnis einschließen] <i>(Optional, erweitert)</i></td> 
   <td> <p>Diese Option ist standardmäßig deaktiviert. Aktivieren Sie diese Option, wenn das Modul die vollständige Antwort des Kollegen in die Ausgabe aufnehmen soll. Die Antwort kann vertrauliche Informationen enthalten.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
> Wir empfehlen, **[!UICONTROL Rohergebnis einbeziehen]** deaktiviert zu lassen, es sei denn, Sie benötigen die vollständige Antwort für einen bestimmten Zweck. Rohdaten können vertrauliche Informationen enthalten, und es wird nicht garantiert, dass jede Aktion vollständig aufgezeichnet wird. Überprüfen Sie, was ein Rohergebnis enthält, bevor Sie es speichern, freigeben oder an einen anderen Service übergeben.

#### Auf Abschluss warten

Wenn **[!UICONTROL Auf Abschluss warten]** aktiviert ist, prüft das Modul die Aufgabe nach einer Wartezeit von fünf Sekunden. Wenn die Aufgabe noch aussteht, wartet das Modul weitere fünf Sekunden, bevor es die Überprüfung erneut durchführt. Jede Prüfung benötigt auch Zeit, um eine Antwort zu erhalten. Durch das Überprüfen des Status wird die Eingabeaufforderung nicht erneut gesendet.

Warten stoppt, wenn die Aufgabe abgeschlossen wird, fehlschlägt, abgebrochen oder abgelehnt wird oder Ihre Eingabe oder Autorisierung benötigt wird. Wenn ein Mitarbeiter eine sofortige Antwort bereitstellt, gibt das Modul diese ohne weitere Prüfungen zurück.

Wenn **[!UICONTROL Auf Abschluss warten]** deaktiviert ist, gibt das Modul das erste Ergebnis zurück, ohne auf den Abschluss der Aufgabe zu warten. Überprüfen Sie **[!UICONTROL Status]**, **[!UICONTROL Abgeschlossen]** und **[!UICONTROL Erfordert Aufmerksamkeit]**, um zu entscheiden, was als Nächstes getan werden soll. Eine Aufgabe kann bereits abgeschlossen werden, wenn das erste Ergebnis vorliegt.

Das Warten unterliegt dem Fusion-Modul-Timeout. Wenn das Modul eine Zeitüberschreitung aufweist oder beendet wird, funktioniert der -Mitarbeiter möglicherweise weiter. In diesem Fall erhalten Sie möglicherweise keine Ausgabe- oder Aufgaben-ID.

Deaktivieren Sie für längere Arbeiten das Warten und speichern Sie die anfängliche **[!UICONTROL Aufgaben-ID]**, damit Sie die Aufgabe später überprüfen können. Die Eingabeaufforderung nach einer Zeitüberschreitung nicht automatisch erneut ausführen. Die erste Anfrage ist möglicherweise bereits in Bearbeitung und eine Wiederholung kann Änderungen duplizieren.


## Modulausgabe

Beide Module geben die folgenden Informationen zurück, wenn sie ohne Fehler abgeschlossen werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aufgaben-ID]</td> 
   <td> <p>Identifiziert die Aufgabe. Dies ist leer, wenn ein Mitarbeiter eine sofortige Antwort bereitstellt, ohne eine Aufgabe zu erstellen. Verwenden Sie diesen Wert mit <b>[!UICONTROL Get Execution Status]</b>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kontext-ID]</td> 
   <td> <p>Identifiziert das Gespräch. Es ist kein Input für die Fortsetzung des Gesprächs.</p><p>Weitere Informationen finden Sie unter <a href="#use-previous-answers">Verwenden früherer Antworten</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
   <td> <p>Der aktuelle Aufgabenstatus. Siehe <a href="#task-states" class="MCXref xref">Aufgabenstatus</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL abgeschlossen]</td> 
   <td> <p>„True“, wenn die Aufgabe abgeschlossen ist oder „Mitarbeiter“ eine sofortige Antwort bereitstellt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL erfordert Aufmerksamkeit]</td> 
   <td> <p>True, wenn ein Mitarbeiter eine Eingabe oder Autorisierung benötigt.</p><p>Weitere Informationen finden Sie unter <a href="#requests-that-need-attention">Anforderungen, die Aufmerksamkeit erfordern</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text des endgültigen Assistenten]</td> 
   <td> <p>Die endgültige Antwort, wenn die Aufgabe abgeschlossen ist. Dies ist leer, solange die Aufgabe aussteht oder bearbeitet werden muss. Eine abgeschlossene Antwort kann auch keinen Antworttext enthalten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text-Artefakte (können Zwischentext enthalten)]</td> 
   <td> <p>Bei der Arbeit ausgegebener Text Jedes Element kann eine Artefakt-ID, einen Namen und einen Text enthalten. Diese Punkte sind nicht unbedingt endgültige Antworten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rohergebnis (Opt-in)]</td> 
   <td> <p>Die vollständige Antwort. Dies ist nur enthalten, wenn <b>[!UICONTROL Rohergebnis einschließen]</b> aktiviert ist.</p> </td> 
  </tr> 
 </tbody> 
</table>

Verwenden Sie **[!UICONTROL Abschließender Assistententext]** für die Antwort, anstatt alle Textartefakte zu kombinieren. Artefakte können Fortschrittsbeschreibungen oder anderen Zwischentext enthalten.

### Anfragen, die Aufmerksamkeit erfordern

Die Mitarbeiter benötigen möglicherweise weitere Informationen oder Autorisierungen, bevor der Vorgang fortgesetzt werden kann. In diesem Fall ist **[!UICONTROL Erfordert Aufmerksamkeit]** wahr und **[!UICONTROL Abgeschlossen]** ist falsch. Das Ergebnis an eine Person weiterleiten, anstatt es als abgeschlossene Arbeit zu behandeln.

Diese Module können keine Folgefragen beantworten oder eine Aktion in Ihrem Namen genehmigen. **[!UICONTROL Ausführungsstatus abrufen]** kann überprüfen, ob sich der Status der Aufgabe geändert hat, löst jedoch die Eingabe- oder Autorisierungsanfrage nicht auf.

### Frühere Antworten verwenden

Mit jeder **[!UICONTROL Ausführen einer Eingabeaufforderung]** wird eine neue Konversation gestartet. Wenn Sie auf eine frühere Antwort verweisen möchten, fügen Sie in Ihrer neuen Eingabeaufforderung die entsprechende Frage und Antwort als Text ein. Dadurch erhalten die Mitarbeiter Kontext, aber die vorherige Konversation wird nicht fortgesetzt.

**[!UICONTROL Kontext-ID]** identifiziert die Konversation, die mit dem Ergebnis verknüpft ist. Sie können es diesen Modulen nicht bereitstellen, um ein Gespräch fortzusetzen.

>[!IMPORTANT]
>
>**[!UICONTROL Abgeschlossen]** garantiert nicht, dass die angeforderte Geschäftsaktion erfolgreich war. Beispielsweise könnte ein Kollege abschließen, indem er erklärt, dass ein erforderliches Tool nicht verfügbar war. Überprüfen Sie die Antwort und überprüfen Sie alle erforderlichen Ergebnisse, bevor Sie die nächste Aktion durchführen.

### Aufgabenstatus

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"><code>submitted</code>, <code>working</code></td> 
   <td> <p>Die Aufgabe steht aus. <b>[!UICONTROL Completed]</b> ist false. <b>[!UICONTROL Run a Prompt]</b> wartet weiter, wenn der Wartevorgang eingeschaltet ist. Andernfalls speichern Sie die Aufgaben-ID und überprüfen Sie es später.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>completed</code></td> 
   <td> <p><b>[!UICONTROL Completed]</b> ist wahr. Überprüfen Sie <b>[!UICONTROL Final Assistant Text]</b> und das erwartete Ergebnis.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>input-required</code>, <code>auth-required</code></td> 
   <td> <p>Die Aufgabe erfordert Aufmerksamkeit. <b>[!UICONTROL Completed]</b> ist „false“ und <b>[!UICONTROL erfordert Aufmerksamkeit]</b> ist „true“. Wartezeit stoppt. Verlegen Sie das Ergebnis zur menschlichen Überprüfung.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>failed</code>, <code>canceled</code>, <code>rejected</code></td> 
   <td> <p>Das Modul meldet einen Fehler anstelle eines normalen Ergebnisses.</p> </td> 
  </tr> 
 </tbody> 
</table>

Ein ausstehendes Ergebnis oder ein Ergebnis, das bearbeitet werden muss, ist kein erfolgreicher Abschluss, auch wenn das Modul ohne Fehler zurückgibt.

## Beispiele

### Zusammenfassen einer Aktualisierung

1. Fügen Sie **[!UICONTROL Eingabeaufforderung ausführen]** hinzu und wählen Sie Ihre Verbindung aus.
1. Geben Sie Folgendes in das Feld **[!UICONTROL Benutzeraufforderung]** ein:

   ```text
   Summarize the following project update in three bullet points.
   Use only the supplied text; do not call tools or change any records.
   
   The planning workshop is complete. Two dependencies need confirmation.
   The team will review the delivery estimate on Friday.
   ```

1. Lassen Sie **[!UICONTROL Auf Abschluss warten]** aktiviert und **[!UICONTROL Rohergebnis einbeziehen]** deaktiviert.
1. Wenn **[!UICONTROL Erfordert Aufmerksamkeit]** wahr ist, leiten Sie das Ergebnis zur menschlichen Überprüfung weiter. Wenn **[!UICONTROL Abgeschlossen]** wahr ist, ordnen Sie **[!UICONTROL endgültigen Assistententext]** Ihrem nächsten Schritt zu.

KI-generierte Formulierungen können variieren. Überprüfen Sie die Ergebnisse, wenn Genauigkeit wichtig ist.

### Später eine längere Aufgabe überprüfen

1. Fügen Sie **[!UICONTROL Eingabeaufforderung ausführen]**, wählen Sie Ihre Verbindung aus und geben Sie Ihre Anweisung ein.
1. Deaktivieren **[!UICONTROL Auf Abschluss warten]**.
1. Überprüfen Sie das Anfangsergebnis.

   * Wenn die Aufgabe abgeschlossen ist, das Ergebnis verarbeiten.
   * Wenn die Aufgabe Aufmerksamkeit erfordert, leiten Sie das Ergebnis zur Überprüfung weiter.
   * Wenn die Aufgabe aussteht, speichern Sie die **[!UICONTROL Aufgaben-ID]** als Text und notieren Sie, welche Verbindung Sie verwendet haben.

1. Verwenden Sie später **[!UICONTROL Ausführungsstatus abrufen]** mit dieser Verbindung und Aufgaben-ID.
1. Wenn die Aufgabe noch aussteht, arrangieren Sie eine weitere Prüfung innerhalb der Grenzen Ihres Szenarios. Verarbeiten Sie das Ergebnis einmal nach Abschluss und behandeln Sie Aufmerksamkeit oder Fehler separat.

Führen Sie die ursprüngliche Eingabeaufforderung nicht erneut aus, nur um den Fortschritt zu überprüfen.

## Überlegungen zur Verwendung

* Mitarbeiter können Tools verwenden und Aktionen durchführen, die von Ihrem Konto zugelassen sind, einschließlich Änderungen an Datensätzen. Verwenden Sie vertrauenswürdige Eingabeaufforderungen und ein Konto mit geeignetem Zugriff.
* Diese Module bieten keine Möglichkeit, einzelne Tools einzuschränken. Anweisungen wie „nichts ändern“ beschreiben Ihre Absicht, sind aber nicht erzwungen und schreibgeschützt.
* Die verfügbaren Tools und Fähigkeiten variieren je nach Konto. Der Connector bietet keine Auswahl für Kenntnisse und garantiert keine bestimmte Aktion, z. B. das Erstellen einer Journey oder das Aktualisieren eines Projekts. Gehen Sie nicht davon aus, dass Genehmigungsanfragen unbeaufsichtigt abgeschlossen werden.
* Der Connector startet und überprüft die Anforderungen der Arbeitskraft. Projektänderungen werden nicht überwacht und Antworten werden nicht automatisch in einer anderen Anwendung gespeichert. Fügen Sie Ihrem Szenario nach Bedarf die entsprechenden Trigger-, Speicher- und Folgemodule hinzu.
* KI-generierte Antworten können unvollständig oder ungenau sein. Validieren Sie wichtige Ergebnisse, bevor Sie sie für Änderungen oder Entscheidungen verwenden.
* Der Connector versucht eine fehlgeschlagene Anfrage nicht automatisch erneut. Stellen Sie sicher, dass die Fehlerbehandlung in Ihrem Szenario keine Eingabeaufforderung wiederholt, deren Ergebnis unsicher ist.

## Fehlerbehebung

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Ein erforderliches Feld fehlt</td> 
   <td> <p>Wählen Sie eine Verbindung aus und geben Sie die erforderliche Eingabeaufforderung oder Aufgaben-ID ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Die Anmeldung schlägt fehl oder der Zugriff wird verweigert</td> 
   <td> <p>Melden Sie sich erneut an und stellen Sie sicher, dass Ihr Adobe-Konto Zugriff auf Coworker und die erforderlichen Services hat. Wenden Sie sich bei Bedarf an Ihren Administrator.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aufgabe nicht gefunden</td> 
   <td> <p>Vergewissern Sie sich, dass die Aufgaben-ID unverändert ist und dass Sie die ursprüngliche Verbindung verwenden. Eine neue Aufgabe ist möglicherweise nicht sofort sichtbar. Überprüfen Sie den Status später, anstatt die Eingabeaufforderung erneut zu senden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eine Statusprüfung schlägt fehl</td> 
   <td> <p>Wenn der Fehler die Kennung der akzeptierten Aufgabe enthält, untersuchen Sie diese Aufgabe mithilfe von <b>[!UICONTROL Get Execution Status]</b>. Starten Sie die Eingabeaufforderung nicht automatisch neu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zeitüberschreitung bei Ausführung einer Eingabeaufforderung oder Verlust der Antwort</td> 
   <td> <p>Die Aufgabe wurde möglicherweise gestartet, auch wenn Sie die Kennung nicht erhalten haben. Untersuchen Sie dies, bevor Sie die Anfrage wiederholen, um doppelte Arbeit zu vermeiden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zeitüberschreitung bei Fusion beim Warten</td> 
   <td> <p>Kollege arbeitet vielleicht noch. Überprüfen Sie die Aufgabe, ob Sie ihre ID haben. Deaktivieren Sie für zukünftige lange Aufgaben das Warten und speichern Sie zuerst die anfängliche ID.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Mitarbeiter oder ein erforderlicher Dienst ist nicht verfügbar</td> 
   <td> <p>Teilen Sie den angezeigten Fehler mit Ihrem Administrator, ohne Anmeldeinformationen oder vertraulichen Ergebnisinhalt.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- BECKY CHECK ME: Confirm the exact module and field labels in the UI (Run a Prompt, Get Execution Status, User prompt, Wait for completion, Include raw result, Task ID, and the output item names). Also confirm that the module is listed under "Adobe CX Enterprise Coworker" in the app picker. -->
