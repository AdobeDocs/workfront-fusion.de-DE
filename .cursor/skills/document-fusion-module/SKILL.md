---
name: document-fusion-module
description: Dokumentieren Sie ein neues Adobe Workfront Fusion-Connector-Modul, indem Sie es dem entsprechenden Connector-Artikel unter help/workfront-fusion/references/apps-and-modules/ hinzufügen. Verwenden Sie diese Option, wenn Benutzende ein neues Fusion-Modul hinzufügen, dokumentieren oder beschreiben möchten oder Screenshots eines Bedienfelds zur Fusion-Modul-Konfiguration bereitstellen und den entsprechenden Artikel aktualisieren möchten.
source-git-commit: 976db79104d226a16a35dc04e8c8cb111eb745db
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 0%

---


# Dokumentieren eines Fusion-Connector-Moduls

Verwenden Sie diese Fähigkeit, um einem Workfront Fusion-Connector-Artikel ein oder mehrere neue Module hinzuzufügen (z. B. `adobe-firefly-modules.md`, `adobe-photoshop-modules.md`, `azure-dev-ops.md`).

## Erforderliche Eingänge (pro Modul)

Bevor Sie die Felder eines Moduls ausfüllen, **der Benutzer** Folgendes bereitstellen. Wenn etwas fehlt, stoppen und fragen Sie danach, bevor Sie fortfahren.

1. **Der Modulname** - genau so, wie er in der Fusion-Benutzeroberfläche angezeigt wird (z. B. `Generate adaptive composite`).
2. **Der Connector-Artikelpfad** - Der Agent findet diesen und bestätigt dies beim Benutzer (siehe Phase 1).
3. **Die API-URL** für den zugrunde liegenden API-Vorgang. Dies ist erforderlich, damit der Zweck jedes Felds mit der API-Spezifikation abgeglichen werden kann.
4. **Screenshot des Konfigurationsbereichs des Moduls in der Standardansicht** (`Show advanced settings` **deaktiviert**)
5. **Screenshot des Konfigurationsbereichs des Moduls in der erweiterten Ansicht** (`Show advanced settings` **aktiviert**) oder eine explizite Anweisung, dass das Modul keine erweiterten Felder hat.

## Workflow

Dies ist ein mehrphasiger Prozess. Das Tempo ist wichtig — arbeiten Sie *mit* dem Benutzer, nicht vor ihm. Den Fortschritt an jeder Phasengrenze bestätigen und jederzeit für Korrekturen offen bleiben.

### Phase 1 — Umfang der Arbeiten

1. **Frage, ob es sich um ein oder mehrere Module handelt**: *„Fügen Sie einem Connector-Artikel ein einzelnes Modul oder mehrere Module hinzu?“*

2. **Sammeln Sie jeden Modulnamen im Voraus** basierend auf der Antwort:
   - **Einzelnes Modul**: Fragen Sie nach dem genauen Namen, wie er in der Fusion-Benutzeroberfläche angezeigt wird.
   - **Mehrere Module**: Fragen Sie nach allen Namen gleichzeitig, ODER fragen Sie nach einem Screenshot des Connectors, der sie auflistet (z. B. der Bildschirm Connector-Übersicht in Fusion , der die Kachelbezeichnungen für jedes Modul anzeigt). In beiden Fällen schließen Sie diesen Schritt mit einer bestätigten Liste aller neu hinzuzufügenden Module ab.

3. **Finden Sie den Connector-Artikel selbst** indem Sie `help/workfront-fusion/references/apps-and-modules/` nach dem Connector-Namen suchen, der von den Modulen impliziert wird. Verwenden Sie die `Glob` oder `Grep`.

4. **Bestätigen Sie den Artikelpfad mit dem Benutzer**: *„Basierend auf dem/den Modulnamen sollte dies in `help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-firefly-modules.md` gehen. Ist das korrekt?“*

5. **Lesen Sie den Connector-Artikel** um mehr über seine vorhandene Struktur und Konventionen zu erfahren. Achten Sie auf:
   - Überschriftenstil (typischerweise `### Module name` Satzfall)
   - Sortierung vorhandener Module (normalerweise alphabetisch)
   - Wortwahl `Connection` Zeilen
   - Schreiben verschachtelter Felder (z. B. `Image > Source`)
   - Vorhandene Konventionen für Fußnoten oder Anmerkungen

### Phase 2 - Platzieren von Platzhaltern für jedes Modul im Voraus

Selbst wenn es nur ein neues Modul gibt, gibt dies dem Benutzer eine klare visuelle Roadmap. Wenn mehrere neue Module vorhanden sind, platzieren Sie diese jetzt alle.

Fügen Sie für jedes neue Modul einen Platzhalterabschnitt an der alphabetischen Position ein:

```markdown
### Module name

<!-- PLACEHOLDER: Add description of the Module name module here. -->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Connector Name], see <a href="#create-a-connection-to-connector-name" class="MCXref xref" >Create a connection to [!DNL Connector Name]</a> in this article.</td> 
  </tr> 
  <!-- PLACEHOLDER: Add field rows for the Module name module here. -->
 </tbody> 
</table>
```

Zeigen Sie dem Benutzer die Liste der hinzugefügten Platzhalter an (z. B. „Hinzugefügte Platzhalter für: Adaptiven Verbund generieren, Bilder mit Bild5 generieren, Präzise Verbund generieren, Video generieren„). Fragen Sie dann, womit Sie beginnen sollen: *„Mit wem möchten Sie beginnen?“*

### Phase 3 — Dokumentationsschleife pro Modul

Führen Sie für jedes Modul diese Schleife vollständig aus, bevor Sie zum nächsten Modul übergehen:

#### 3a. Abrufen der API-URL

Fragen Sie den Benutzer nach der API-URL: *„Bitte geben Sie die API-URL für den zugrunde liegenden API-Vorgang von `<module name>` frei.“*

Wenn Sie es haben:
- Versuchen Sie es `WebFetch` mit der URL.
- Wenn die Seite leer/JS-gerendert ist (wie bei Adobe Developer-Dokumenten üblich), suchen Sie nach einer zugehörigen Feature Guide-Seite - in der Regel unter einer `.../guides/how-tos/...`-URL - und rufen Sie diese stattdessen ab.
- Wenn Sie immer noch kein Glück haben, wenden Sie sich für den Vorgangsnamen an `WebSearch`.

Verwenden Sie alles, was Sie lernen, später als Hintergrundkontext für Feldbeschreibungen. Entladen Sie es nicht dem Benutzer, sondern bestätigen Sie es nur kurz: *Ich habe den API-Kontext - bereit für den Standard-Screenshot der Ansicht.“*

#### 3b. Abrufen des Standardansichts-Screenshots

Fragen Sie: *„Bitte teilen Sie einen Screenshot des Konfigurationsbereichs des Moduls mit `Show advanced settings`**deaktiviert**. Nachdem wir die Standardfelder durchgearbeitet haben, frage ich nach der erweiterten Ansicht, sende diese aber noch nicht.“*

#### 3c. Dokumentieren der Standardfelder

Erfassen Sie beim Arbeiten mit dem Screenshot der Standardansicht jedes sichtbare Feld von oben nach unten. Für jedes Feld:

1. Verwenden Sie die genaue UI-Beschriftung des Felds als Zeilenüberschrift. Für gruppierte Felder verbinden Sie sich mit ` > `:

   ```
   [!UICONTROL Background > Image > Source]
   ```

2. Lesen Sie den Hilfetext unter dem Feld im Screenshot (graue/gelbe Beschriftung). Verwenden Sie sie als Grundlage für die Beschreibung.
3. Verweisen Sie mit dem API-Kontext aus Schritt 3a, um zu identifizieren, was das Feld darstellt (z. B. `background.fillAreaMask` ist „der Bereich des Hintergrunds, in dem das Objekt platziert werden wird„).
4. Schreiben Sie die Beschreibung, indem Sie **Was das Feld ist** (über die API) mit **Wie Sie es bereitstellen** (über den Text und Feldtyp des UI-Helpers) kombinieren.

Überspringen Sie alle Felder, die im Screenshot nicht sichtbar sind, selbst wenn sie von der API unterstützt werden. Erfinde keine Felder.

Nachdem die Standardfelder eingerichtet wurden, diese kurz für den Benutzer zusammenfassen (z. B. „Hinzugefügte Standardfelder: Verbindung, Eingabeaufforderung, Seitenverhältnis, …„), und dann mit Schritt 3d fortfahren.

#### 3D. Abrufen des Screenshots der erweiterten Ansicht

Fragen Sie: *„Bitte teilen Sie jetzt einen Screenshot des Konfigurationsbereichs des Moduls mit `Show advanced settings`**aktiviert**. Wenn das Modul keine erweiterten Felder enthält, sagen Sie es so und wir fahren fort.“*

#### 3e. Dokumentieren der erweiterten Felder

Arbeiten mit dem Screenshot der erweiterten Ansicht:

1. Identifizieren Sie die Felder *die* bereits in der Standardansicht sind. Dies sind die erweiterten Felder.
2. Folgen Sie für jedes erweiterte Feld demselben Beschreibungsvorgang aus Schritt 3c.
3. Hängen Sie `*` an den Feldnamen in der `<td role="rowheader">` an:

   ```html
   <td role="rowheader">[!UICONTROL Seeds]*</td>
   ```

4. Fügen Sie nach dem `</table>` diese Fußnote in einer eigenen Zeile hinzu:

   ```markdown
   * These fields are advanced fields, and do not display unless you select **[!UICONTROL Show advanced settings]**.
   ```

Wenn der Benutzer angegeben hat, dass das Modul keine erweiterten Felder enthält, überspringen Sie die Schritte 3d und 3e vollständig.

#### 3f. Entwurf der Modulbeschreibung

Ersetzen Sie jetzt (nicht früher) den Platzhalter Beschreibung oben im Abschnitt durch einen Entwurf mit einem Satz, der auf dem API-Kontext und den Auswirkungen der Felder basiert. Bieten Sie sie immer als Entwurf zur Überprüfung durch den Benutzer an:

> *„Ich habe diese Beschreibung entworfen: &#39;…&#39;. Möchten Sie sie verwenden, bearbeiten oder ersetzen?“*

#### 3 g. Einzelmodul-Zusammenfassung

Geben Sie dem Benutzer eine abschließende Zusammenfassung der dokumentierten Felder des Moduls (Standard + Erweitert) und stellen Sie alle offenen Fragen:

- Wurden in den Screenshots Felder abgeschnitten?
- Ist die Modulbeschreibung zulässig?
- Sollte irgendetwas als veraltet oder bemerkenswert gekennzeichnet werden?

Warten Sie auf Bestätigung, bevor Sie sagen, dass das Modul abgeschlossen ist. Dann fragen Sie: *„Bereit zum nächsten Modul?“* (oder „Wir sind alle mit diesem Connector-Artikel fertig.„)

### Phase 4 — Endprüfung

Nachdem alle Module dokumentiert sind, führen Sie diese Checkliste für jedes Modul durch:

- [ ] Überschrift des Moduls ist `### ` (H3) und verwendet die Groß-/Kleinschreibung.
- [ ] Modul wird in alphabetischer Reihenfolge relativ zu den gleichrangigen Modulen angezeigt.
- [ ] erste Zeile ist `Connection` und verwendet den standardmäßigen Verbindungs-Link-Wortlaut.
- [ ] Jedes dokumentierte Feld ist in den Screenshots des Benutzers sichtbar.
- [ ] erweiterten Felder sind mit `*` gekennzeichnet, und unter der Tabelle befindet sich eine einzige Fußnote.
- [ ] Keine Felder, die nur über die API erfunden wurden.
- [ ] Dropdown-Beschreibungen in Source verwenden die exakten Beschriftungen der UI-Optionen (siehe &quot;Source-Feldkonvention“ unten).
- [ ] Modulbeschreibung ist eine Zusammenfassung aus einem Satz, die beschreibt, was das Modul tut.

## Source Field Convention

Bildquellenfelder in Fusion-Connectoren bieten in der Regel eine Dropdown-Liste mit zwei Optionen. **Verwenden Sie die exakten Beschriftungen, die im Screenshot des Benutzers angezeigt werden** - verschiedene Generationen von Modulen verwenden unterschiedliche Formulierungen:

| Wenn das Dropdown-Menü Folgendes anzeigt… | Dieses Format verwenden |
|---|---|
| **Bild hochladen** und **Bild-URL** (neuere Module) | `<ul><li><b>Upload Image</b><p>Upload the image, or map the image file from a previous module.</p></li><li><b>Image URL</b><p>Enter or map the URL of the image.</p></li></ul>` |
| **Datei** und **Vordefinierte URL** (ältere Module) | `<ul><li><b>File</b><p>Select a source file from a previous module, or map the source file's reference image file name and reference image file.</p></li><li><b>Presigned URL</b><p>Enter or map the URL of the source image.</p></li></ul>` |

Wenn der Screenshot die geöffneten Dropdown-Optionen nicht anzeigt, bitten Sie den Benutzer, sie freizugeben.

## Stil der Feldbeschreibung

- Stimmen und Struktur vorhandener Moduleinträge im selben Artikel abgleichen.
- Beschreibungen kurz halten: Ein oder zwei Sätze pro Feld reichen in der Regel aus.
- Verwenden Sie `[!UICONTROL ...]` Markup für jeden Feldnamen der Benutzeroberfläche, der von einem anderen Feld referenziert wird.
- Verwenden Sie `<code>...</code>` für Literalwerte (`<code>en-US</code>`, `<code>0.0</code>`).
- Geben Sie bei numerischen Bereichsfeldern den zulässigen Bereich explizit an: *„Geben Sie eine Zahl zwischen 0 und 1 ein…*.
- Auflisten Sie Dropdown-Listen mit diskreten Optionen als `<ul>` mit `<b>Option</b>` gefolgt von `<p>` Beschreibung.

## Häufige Felder und empfohlene Beschreibungen

Wiederverwenden dieser Komponenten für Konsistenz über Module hinweg:

**Seeds** (wenn das Feld mehrere Seed-Werte über Element hinzufügen zulässt):
> Klicken Sie **Element hinzufügen**, um einen Seed-Wert hinzuzufügen, und geben Sie dann eine Ganzzahl ein oder ordnen Sie sie zu. Verwenden Sie pro Variante einen Seed. Die Anzahl der Seed-Werte muss mit dem Wert **Number of Variations** übereinstimmen, wenn beide angegeben sind.

**Anzahl der Varianten** (ersetzen Sie den Bereich durch den tatsächlichen Bereich aus dem Screenshot):
> Geben Sie eine Zahl zwischen &quot;[&quot; ] &quot;[&quot; ]. Das Modul generiert diese Anzahl von [Ausgabetyp]-Varianten.

**Limit** (der standardmäßige Ausführungszyklus-Grenzwert von Fusion; nur einschließen, wenn im Screenshot sichtbar):
> Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während eines Ausführungszyklus arbeiten soll, oder mappen Sie sie.

**Gebietsschema**:
> Geben Sie einen Sprach- und Regionscode ein oder mappen Sie ihn, um den generierten Inhalt auf ein bestimmtes Land und eine bestimmte Sprache anzupassen. Das Gebietsschema muss im ISO-639-1-Sprachcode und in der ISO-3166-1-Region angegeben werden. Beispiel: `en-US`

## Sie können jederzeit Korrekturen vornehmen

Der/die Benutzende kann frühere Arbeiten in der Mitte des Flusses korrigieren - Seeds-Formulierung, Dropdown-Beschriftungen, Feldpositionierung, erweiterte/standardmäßige Aufteilung usw. Behandeln Sie jede Korrektur als autorisierend und aktualisieren Sie sie ohne Push-back. Nach der Korrektur kurz zusammenfassen, was geändert wurde.

Wenn der/die Benutzende eine neue Mid-Flow-Konvention einführt (z. B. „Markieren wir erweiterte Felder mit `*` und fügen wir eine Fußnote hinzu„), übernehmen Sie sie für den Rest der Sitzung und wenden Sie sie rückwirkend auf alle bereits dokumentierten Module an.

## Vorgehensweise bei widersprüchlichen Informationen

Wenn die API-Spezifikation und die Benutzeroberfläche nicht übereinstimmen (dies geschieht häufig):

1. **Vertrauen Sie der Benutzeroberfläche** denn das ist es, was der Benutzer tatsächlich in Fusion sieht.
2. **Beachten Sie die Diskrepanz** in Ihrer Antwort an den Benutzer, damit er entscheiden kann, ob er weitere Untersuchungen durchführen möchte.
3. **Erfinde keine Erklärung** im Artikelinhalt - behalte es für das, was in der Benutzeroberfläche steht.

Wenn sich zwei Screenshots des Benutzers widersprechen (z. B. zeigt ein Screenshot `Blend`, ein anderer zeigt `Harmonization` für dasselbe Modul), stoppen und fragen Sie vor dem Schreiben, welcher richtig ist. Ermitteln Sie durch Querverweise auf die API-Spezifikation, welcher Screenshot wahrscheinlich zu einem anderen Modul gehört.
