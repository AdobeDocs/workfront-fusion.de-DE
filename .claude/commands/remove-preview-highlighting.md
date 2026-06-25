---
name: remove-preview-highlighting
description: ""
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---


# Entfernen der Vorschau-Hervorhebung (Workfront)

## Umfang

Nur anwenden, wenn **alle** wahr sind:

1. Der Benutzer hat diesen Workflow aufgerufen (z. B. **„Hervorhebung der Vorschau entfernen“** oder eindeutig dieselbe Absicht).
2. Der Pfad der Markdown-Datei **nicht** enthält **`product-announcements`** (schließen Sie die gesamte Ordnerstruktur aus, z. B. Versionshinweise, Betas, Ankündigungen unter `help/quicksilver/product-announcements/`).
3. Die Markdown-Datei wird **nicht** unten unter **[Ausgeschlossene Pfade](#excluded-paths)** aufgeführt.
4. Die Markdown-Datei wird in `git log` mit Vorschauinhalten angezeigt **die vom aktuellen Git-Benutzer innerhalb** benutzerdefinierten Datumsbereichs hinzugefügt oder geändert wurden (siehe Schritt „Inventar„).
5. Der Artikel **(mindestens eine** von:
   - Vorschau-Umgebung **Sprache in Textprosa- oder echten Snippet-Absätzen** (typische Muster: „hervorgehobene Informationen“, „Vorschau-Umgebung“, „noch nicht allgemein verfügbar“, Schnellversionshinweise) - **nicht** Übereinstimmung aus **Link-Text allein** auf einer Inhaltsverzeichnis-/Indexseite (siehe unten); oder
   - alle HTML-Elemente mit **`class="preview"`** (z. B. `<span class="preview">`, `<div class="preview">`) oder
   - Ein Vorschau-Snippet **Variable** wie **`{{highlighted-preview}}`** oder **`{{highlighted-preview-article-level}}`**.

Wenn der Umfang unklar ist, bestätigen Sie ihn vor der Bearbeitung.

**INHALTSVERZEICHNIS-/INDEXSEITEN - Immer diesen Fall überspringen:** **Nie** Legen Sie eine Datei in das Inventar ein, wenn der **nur** vorschaubezogene Wortlaut **innerhalb** Anzeigetext eines Markdown-Links auf **einen anderen** Artikel verweist (z. B. *Senden eines Berichts in der Sandbox-Vorschau-Umgebung&#x200B;**&#x200B;*** no`class="preview"`, **noSnippet-Variablen und**&#x200B;**&#x200B;** **noPreview Boilerplate in**&#x200B;**prose außerhalb von Links**. Dies ist keine Vorschauhervorhebung auf dieser Seite - es ist nur eine Inhaltsverzeichniserwähnung. Gilt für jeden Index/Inhaltsverzeichnis, nicht nur für eine Datei.

### Ausgeschlossene Pfade

Fügen Sie diese niemals zum Inventar hinzu oder bearbeiten Sie sie in diesem Workflow, es sei denn, der Benutzer überschreibt explizit:

- `help/quicksilver/documents/adobe-workfront-for-experience-manager-assets-essentials/send-to-aem.md` - Parallele Vorschau vs. Produktionsbeschränkungen erfordern eine bewusste redaktionelle Entscheidung außerhalb der Automatisierung.
- `help/quicksilver/reports-and-dashboards/reports/creating-and-managing-reports/create-manage-reports.md` - meldet das Inhaltsverzeichnis; das einzige „preview“-Signal ist der Link zum Artikel Sandbox-Versand in der Vorschau.

## Erforderlicher Workflow (menschlicher Workflow)

Repository **nicht** ohne Genehmigung stapelweise bearbeiten.

1. **Bestand**\
   a. **Fragen Sie den Benutzer, für welche vierteljährliche Version** die Vorschau-Hervorhebung entfernt wird (z. B. „Q3 2026“ oder „2026.07„).\
   B. **Abrufen des Veröffentlichungskalenders** aus `https://wiki.corp.adobe.com/spaces/AWF/pages/3631617814/2026+Monthly+Release+Calendar` mithilfe des Adobe-Wiki MCP-Tools. Suchen:
   - Das **Produktionsveröffentlichungsdatum** der **vorherigen** vierteljährlichen Veröffentlichung → `--since`.
   - Das **Produktionsveröffentlichungsdatum** der vierteljährlichen **target**-Veröffentlichung → `--until`.
   - Vierteljährliche Versionen werden durch die Spalte „Quartalsname der Version“ gekennzeichnet (z. B. 2026.01, 2026.04, 2026.07, 2026.10).
   - **Wenn das aktuelle Datum im 4. Quartal (Oktober-Dezember) liegt:** Bitten Sie den Benutzer nach dem Abrufen des Kalenders des aktuellen Jahres, die URL für den Veröffentlichungskalender des nächsten Jahres anzugeben, und rufen Sie diese dann ebenfalls ab, damit alle erforderlichen vierteljährlichen Produktionstermine verfügbar sind.
c. Bestimmen Sie den aktuellen Git-Benutzer und führen Sie dann Folgendes anhand der Produktionsversionstermine aus Schritt b aus:

   ```bash
   GIT_USER=$(git config user.name)
   git log --since="YYYY-MM-DD" --until="YYYY-MM-DD" \
     --author="$GIT_USER" --name-only --pretty=format: \
     -- "help/quicksilver/**/*.md" | sort -u | grep -v '^$'
   ```

   d. Filtern Sie aus **Ergebnissen nach Dateien, bei denen die Übertragungen des aktuellen Benutzers im Datumsbereich tatsächlich Vorschauinhalte hinzugefügt oder geändert**. Überprüfen Sie für jede Kandidatendatei, ob die vom Benutzer übergebenen eingeführten Vorschaumarken:

   ```bash
   git log --since="YYYY-MM-DD" --until="YYYY-MM-DD" \
     --author="$GIT_USER" -p -- "<file>" | \
   grep -q '^\+.*class="preview"\|^\+.*{{highlighted-preview\|^\+.*highlighted information\|^\+.*not yet generally available'
   ```

   Schließen Sie die Datei nur ein, wenn dieses Grep übereinstimmt (Exitcode 0). Dadurch werden falsch-positive Ergebnisse vermieden, bei denen ein Benutzer eine Datei, deren Vorschau-Hervorhebung von einer anderen Person hinzugefügt wurde, unabhängig bearbeitet hat.

   E. **Auslassen** alle Pfade unter **`product-announcements`**, alle **[ausgeschlossenen Pfade](#excluded-paths)** und alle **TOC/Index** Seiten gemäß der obigen Inhaltsverzeichnisregel.\
   F. Zeigen Sie die resultierende sortierte Liste an. Wenn der/die Benutzende sagt, dass eine aufgelistete Datei keine Vorschau-Hervorhebung hat, entfernen Sie sie aus der Ausführung und verschärfen Sie die Kriterien, anstatt Bearbeitungen zu erzwingen.

2. **Starten**\
   Fragen Sie, ob mit dem **ersten** Artikel in der Liste (oder einem Pfad mit den Benutzernamen) begonnen werden soll.

3. **Pro Artikel - zuerst anzeigen, nach OK bearbeiten**
   - Lies die Datei!
   - Änderungsvorschläge klar: **vor/nach Ausschnitten** oder eine fokussierte Beschreibung der Änderungen.
   - **Warten** auf eine explizite Genehmigung (z. B. „okay“, „anwenden“, „ja„), bevor die Datei geschrieben wird.

4. **Nach jeder Datei**\
   Frage, ob zum Artikel **Weiter** (oder STOP/SKIP) übergegangen werden soll.

## Inhaltsregeln (GA: Vorschau des Inhalts wird zum Dokument)

Beim Entfernen der Vorschau-Hervorhebung für **allgemeine Verfügbarkeit** lautet das Ziel: **Behalten Sie das für die Vorschau dokumentierte Verhalten bei**, **Sie „veraltete Verzweigungen in Produktion“/im alten** ab, und **Entfernen Sie dann nur für die Vorschau verwendete Beschriftungen und Wrapper** sodass das Thema für alle Kunden als aktuell liest.

### Parallele Schritte

- Wenn der Artikel einen Schritt (oder ein nummeriertes Element) **eingerahmt als „in der Produktion“** (oder gleichwertig: aktuelle Produktion / vorhandenes Produktionsverhalten) **und** einen **parallelen** Schritt eingerahmt als **„in der Vorschau“** (oder Vorschau-Umgebung):
   - **Entfernen** Sie den Produktionsschritt (den alten Pfad).
   - **Behalten** Sie den **Inhalt** des In-Vorschau-Schritts bei, **jedoch umformulieren** sodass er **nicht** Vorschauspezifisch ist (entfernen Sie „in der Vorschau“, „Vorschauumgebung“ usw.). Passen Sie die Nummerierung an, damit die Liste konsistent bleibt.

Wenn die Struktur mehrdeutig ist (keine klare Parallele), **stop** und zeigen Sie beide Kandidaten; fragen Sie den Benutzer, welcher Block beibehalten werden soll.

### Parallele Abschnitte

- Wenn ein **Abschnitt** (Überschrift + Hauptteil) **über „in der Produktionsumgebung“** und es einen **parallelen Abschnitt** **über „in der Vorschauumgebung“**:
   - **Entfernen** Sie den Abschnitt „Produktionsumgebung“ (der ersetzte Inhalt).
   - **Ersetzen** durch den Inhalt des Vorschauabschnitts, dann **Entfernen** den Wortlaut der Vorschauumgebung und alle **`class="preview"`** Wrapper, sodass der Abschnitt neutral (GA-fähig) ist.

### Hinweise zu Snippets und Top-of-Article

- Entfernen Sie **Nur-Vorschau-Textbausteine** (Bereiche/Div-Bereiche oder Absätze, die nur erklären, dass der hervorgehobene Inhalt nur die Vorschau ist, schnelle Freigabe, Sandbox usw.). sobald die Funktion allgemein verfügbar ist.
- Links oder Sätze entfernen, deren **(**) Vorschauverfügbarkeit ist, es sei denn, der Benutzer sagt, er möchte eine andere Mitteilung beibehalten.

### HTML `class="preview"`

- Entfernen Sie die **öffnenden und schließenden Tags** für Elemente, die **`class="preview"`** verwenden, **inneren Inhalt beibehalten** (Markdown/HTML innerhalb des Tags).
- Behandeln Sie sowohl **`<span class="preview">`** als auch **`<div class="preview">`** und dasselbe Muster für andere Tags (z. B. **`<p class="preview">`**, **`<li class="preview">`**), wenn sie im **sichtbaren** (nicht kommentierten) Hauptteilinhalt angezeigt werden.
- Listen-/Tabellenstruktur beibehalten; fehlerhafte Listen oder fehlerhafte Leerzeichen nach dem Entpacken beheben.

### Auskommentierte Abschnitte (HTML-Kommentare)

- **Löschen** Entpacken oder anderweitig **Ändern** von Inhalten in **`<!-- … -->`** HTML-Kommentaren nicht möglich **es sei denn, der Benutzer gibt explizit an,** was zu tun ist (z. B. den gesamten Kommentar löschen, Vorschauklassen nur innerhalb des Kommentars entfernen, Kommentar für allgemeine Verfügbarkeit aufheben).
- Wenn vorschaubezogene Inhalte oder **`class="preview"`** (nur **)** Kommentaren angezeigt werden, **nennen Sie dies**, wenn Sie den Artikel lesen: Sagen Sie, was im Kommentar ist, und **fragen** was zu tun ist. **Standard: kommentierte Abschnitte bleiben unverändert.**

### Was nicht tun

- Diesen Workflow nicht für Pfade unter **`product-announcements`** (Versionshinweise und zugehörige Links) ausführen. Der Bestand muss diese Pfade ausschließen.
- Inventarisieren oder bearbeiten Sie keine Pfade, die unter **[Ausgeschlossene Pfade](#excluded-paths)** aufgeführt sind, es sei denn, der Benutzer fragt ausdrücklich danach.
- **Nicht** automatisch entfernen oder bearbeiten Sie **auskommentierte** (`<!-- … -->`) Blöcke. Befolgen Sie **auskommentierte Abschnitte** oben.
- Entfernen Sie „Vorschau“ nicht, wenn es **nicht** um dieses Funktionsverfügbarkeitsmuster geht (z. B. [Vorschau der Sandbox-Umgebung] (·) als **Produktname** in einem anderen Kontext) - Urteilsvermögen verwenden und fragen Sie, ob Sie sich nicht sicher sind.
- Ändern Sie keine `author:` oder nicht verwandte Schriftart, es sei denn, der Benutzer fragt.
- Überspringen Sie nicht den Schritt **Anzeigen → Genehmigen**.

## Qualitätsprüfungen vor der Präsentation von Bearbeitungen

- Keine weiteren **`class="preview"`** über den vereinbarten Umfang der Änderung.
- Keine verwaisten doppelten Überschriften oder fehlerhaften Schrittnummern.
- Einführung liest sich korrekt **ohne** zu widersprechen (nicht „nur in der Vorschau“ für ausgelieferte Funktionen).

## Referenzen

- Übereinstimmung mit den **[Workfront](https://experienceleague.adobe.com/de?lang=de)** Dokumentationsstilen und Repo-Konventionen (Commit-/PR-Regeln, wenn der Benutzer einen Commit ausführt).
