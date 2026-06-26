---
name: add-mini-tocs
description: ""
source-git-commit: 4ec81401b5a76edd620b9779414ee578966b4315
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Mini-Inhaltsverzeichnisse hinzufügen

Scannt eine Markdown-Datei und fügt unter jeder qualifizierten Überschrift, die direkte Unterüberschriften hat, ein Minitabelle mit Inhalten ein.

## Workflow

1. Lies die Zieldatei.
2. Identifizieren Sie jede Überschrift auf `##` oder tieferen Ebene, die mindestens eine direkte untergeordnete Überschrift hat (eine `#` tiefer).
3. Erstellen Sie für jede dieser übergeordneten Überschriften eine Liste mit Aufzählungszeichen, die nur Links zu den direkt untergeordneten Elementen enthält.
4. Fügen Sie die Liste unmittelbar vor der ersten untergeordneten Überschrift nach einem Einführungstext ein, der auf die übergeordnete Überschrift folgt.
5. Wenn an dieser Position bereits ein Mini-Inhaltsverzeichnis vorhanden ist, vergleichen Sie es mit den aktuellen untergeordneten Überschriften in diesem Abschnitt. Wenn die Liste veraltet ist (fehlende Einträge, zusätzliche Einträge oder falsche Links), ersetzen Sie sie durch die aktualisierte Liste. Wenn er bereits übereinstimmt, überspringen Sie.
6. Schreiben Sie die aktualisierte Datei.

## Umfang

- **Erstellen Sie** Mini-Inhaltsverzeichnis unter dem `#` Artikeltitel. Mini-Inhaltsverzeichnisse werden nur unter `##` Überschriften und tiefer hinzugefügt.
- Eine `##` erhält eine Liste der `###` direkt untergeordneten Elemente.
- Eine `###` erhält eine Liste der `####` direkt untergeordneten Elemente.
- Und so weiter für tiefere Ebenen.

## Link-Format

Jeder Eintrag in der Liste verwendet genau dieses Format:

```
* [Heading text](#anchor)
```

### Regeln zur Ankergenerierung

Konvertieren Sie den Überschrifttext wie folgt in einen Anker:

1. Gesamten Text in Kleinbuchstaben schreiben.
2. Entfernen Sie alle Zeichen, die keine Buchstaben, Zahlen, Leerzeichen oder Bindestriche sind.
3. Ersetzen Sie Leerzeichen durch Bindestriche.
4. Entfernen Sie alle Code-Formatierungen, die in Backtick eingeschlossen sind (behalten Sie den Text darin).

Beispiel: `### Create or edit a function` → `#create-or-edit-a-function`

## Verschachtelungsregeln

- Nur Link **direkte untergeordnete Elemente** (eine Ebene tiefer als das übergeordnete Element) in jeder Liste.
- Schließen Sie keine Enkelkinder oder tieferen Überschriften in dieselbe Liste ein.
- Wenn diese untergeordneten Überschriften selbst untergeordnete Elemente haben, wird ein eigenes kleines Inhaltsverzeichnis unter ihnen eingefügt.

**Beispielstruktur:**

```
## Manage a package          ← parent: gets a list of ### headings
### Functions                ← child of ##, parent of ####: gets a list of #### headings
#### Create a function       ← child of ###
#### Delete a function       ← child of ###
### Variables                ← child of ##
### History                  ← child of ##
```

Ergebnisse in:

Unter `## Manage a package`:

```
* [Functions](#functions)
* [Variables](#variables)
* [History](#history)
```

Unter `### Functions`:

```
* [Create a function](#create-a-function)
* [Delete a function](#delete-a-function)
```

## Platzierung

Fügen Sie die Mini-Inhaltsverzeichnisliste unmittelbar vor der ersten untergeordneten Überschrift ein. Wenn zwischen der übergeordneten Überschrift und der ersten untergeordneten Überschrift ein Einführungstext vorhanden ist, wird die Liste nach diesem Text direkt über der ersten untergeordneten Überschrift eingefügt. Fügen Sie vor und nach der Mini-Inhaltsverzeichnisliste immer eine leere Zeile ein.

## Überspringen

- `#` Überschriften (Artikeltitel): Fügen Sie hier niemals ein Mini-Inhaltsverzeichnis hinzu.
- Übergeordnete Überschriften mit nur einem direkt untergeordneten Element: Überspringen - Eine Liste mit einem Element fügt keinen Navigationswert hinzu.
- Abschnitte ohne untergeordnete Überschriften: Überspringen.
