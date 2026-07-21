---
name: fusion-release-notes
description: Erstellen Sie eine neue wöchentliche Versionshinweisseite für Workfront Fusion und fügen Sie sie in die Übersichtsseite zur Versionsaktivität und in das Inhaltsverzeichnis ein. Verwenden Sie diese Option, wenn Benutzende neue Versionshinweise zu Fusion oder eine wöchentliche Versionsseite schreiben, hinzufügen oder entwerfen möchten oder darum bitten, neue Fusion-Funktionen für eine Version zu dokumentieren. Verwenden Sie nicht für Workfront (Quicksilver)-Versionshinweise in Produktankündigungen/Produktversionen - verwenden Sie für diese Versionshinweise Release-Formatter.
source-git-commit: 59a8d8ee83906bc16fc627bd348accc4e588cf9b
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 1%

---


# Versionshinweise zu Fusion

Erstellt in `help/workfront-fusion/fusion-product-releases/` eine neue wöchentliche Versionshinweisseite für Adobe Workfront **Fusion** und verknüpft sie mit den beiden Stellen, an denen sie auffindbar ist: der Übersichtsseite zur Versionsaktivität und der `help/workfront-fusion/TOC.md`.

Dies ist ein anderes System als die Quicksilver (Core Workfront)-Versionshinweise, die von den `release-notes-formatter` verarbeitet werden:

| | Versionshinweise zu Fusion (diese Fähigkeit) | Quicksilver - Versionshinweise (`release-notes-formatter`) |
|---|---|---|
| Kadenz | Wöchentlich | Vierteljährlich |
| Verzeichnis | `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/` | `help/quicksilver/product-announcements/product-releases/` |
| Datumsbeschriftung für einzelne Funktion | Nein - der Seitentitel trägt die Woche | Ja - `>[!NOTE]` Block pro Funktion |
| Seite indizieren | `fusion-release-activity.md` (nach Jahr/Monat) | `{YY}-q{N}-release-overview.md` (nach Quartal) |

## Schritt 1: Zusammenstellen der Funktionen

Fragen Sie den Benutzer (falls noch nicht angegeben) nach der Liste der Funktionen/Änderungen des Dokuments für die Woche und für jede Woche:

- Ein kurzer Funktionstitel
- Eine klare Beschreibung dessen, was sich geändert hat und warum es wichtig ist
- Die Hilfeartikel, auf die er verweist (Überprüfen Sie, ob der Pfad vorhanden ist - raten Sie nicht)
- Ob eine Benutzer-/Admin-Aktion erforderlich ist oder ob es sich um eine Einstellung handelt (`>[!IMPORTANT]` Legende erforderlich)

## Schritt 2: Dateinamen und Datum bestimmen

- Finden Sie den Montag (oder das Veröffentlichungsdatum) für die Woche, die dokumentiert wird, und bestätigen Sie dies mit dem Benutzer, wenn es nicht eindeutig ist.
- Dateipfad: `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md`
  - `{M}` und `{D}` haben **keine führenden Nullen**: `fusion-2026-7-20.md`, nicht `fusion-2026-07-20.md`.
  - Wenn der Jahresordner noch nicht vorhanden ist, erstellen Sie ihn.
- Überprüfen Sie, ob für diese Woche bereits eine Seite vorhanden ist, bevor Sie eine neue erstellen.

## Schritt 3: Seite schreiben

### Titelei

```yaml
---
title: Workfront Fusion release activity Week of {Month} {Day}, {Year}
description: Workfront Fusion release activity Week of {Month} {Day}, {Year}
author: {Author}
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
```

Regeln:
- `title` und `description` sind identisch.
- Setzen Sie immer das Komma in das Datum (`July 20, 2026`), auch wenn es auf einigen älteren Seiten weggelassen wird. Kopieren Sie diese Inkonsistenz nicht.
- **Verwenden Sie `hidefromtoc: true` für jede neue Seite. Fügen Sie keine `exl-id` oder `TQID` hinzu.** Diese werden nach der Veröffentlichung der Seite später zugewiesen. Die Erfindung einer solchen ist falsch. (Ab Mitte 2026 folgen alle Seiten diesem Muster - siehe `_fusion-release-notes-reference.md`, wenn Sie ein Beispiel überprüfen müssen.)

### Textkörper

```markdown
# Workfront Fusion release activity: Week of {Month} {Day}, {Year}

This page describes all enhancements made in Adobe Workfront Fusion the week of {Month} {Day}, {Year}.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/de/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## {Feature title}

Feature description paragraph(s) — what changed, why, and how it affects existing scenarios/configurations if relevant.

For more information, see [{Help article title}](/help/workfront-fusion/{path-to-article}.md).

## {Next feature title}

...
```

Hinweise:
- Ein H2 pro Funktion in der Reihenfolge, in der der Benutzer sie sortiert hat (keine erzwungene Erstbestellung innerhalb der Seite - es dauert eine Woche).
- Keine `>[!NOTE]` Datumsbeschriftung pro Funktion - der Seitentitel enthält bereits das Datum.
- Wenn für eine Funktion eine Aktion erforderlich ist oder es sich um eine grundlegende Änderung/Einstellung handelt, fügen Sie direkt unter der H2 vor der Beschreibung einen `>[!IMPORTANT]` hinzu:

  ```markdown
  ## {Feature title}
  
  >[!IMPORTANT]
  >
  >**Action Required: {short summary of what the user must do and by when}**
  >
  >{Details of the requirement.}
  
  {Regular description paragraph(s).}
  ```

- Jede Funktion sollte mit „Weitere Informationen finden Sie unter […]&quot; enden. Link zum entsprechenden Hilfeartikel. Überprüfen Sie, ob das Verknüpfungsziel im Repository vorhanden ist.

## Schritt 4: Hinzufügen der Seite zum Übersichtsindex

`help/workfront-fusion/fusion-product-releases/fusion-release-activity.md` bearbeiten:

- Suchen Sie den `## Fusion releases in {current year}` Abschnitt (er ist **nicht** in einen `+++` ausblendbaren Block eingeschlossen - nur die letzten Jahre werden ausgeblendet).
- Suchen oder erstellen Sie die `### {Month} {Year}` Überschrift für den Monat der Veröffentlichung, direkt unter der Überschrift Jahr .
  - Wenn die Monatsüberschrift noch nicht vorhanden ist, fügen Sie sie **über** dem Vormonat (neuer Monat zuerst) hinzu.
- Fügen Sie die neue Seite als **erstes** Aufzählungszeichen unter der Überschrift „Monat“ hinzu (neueste Woche zuerst):

  ```markdown
  * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```

- Wenn dies die erste Version eines neuen Jahres ist, fügen Sie eine neue `## Fusion releases in {YYYY}` Überschrift über der Überschrift des Vorjahres hinzu und verpacken Sie den Abschnitt *Vorjahr* in einem `+++ **Click to open**` / `+++` ausblendbaren Block, falls er noch nicht vorhanden ist (nur das aktuelle Jahr bleibt erweitert).

## Schritt 5: Hinzufügen der Seite zum Inhaltsverzeichnis

`help/workfront-fusion/TOC.md` bearbeiten:

- Suchen Sie `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}` für das aktuelle Jahr, verschachtelt unter `* Fusion release activity {#fusion-release-activity}`.
- Fügen Sie die neue Seite als **ersten** Eintrag unter dieser Überschrift hinzu (neueste zuerst), wobei Sie vorhandene Einzüge (8 Leerzeichen) berücksichtigen:

  ```markdown
        * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```

- Wenn die Überschrift des aktuellen Jahres noch nicht vorhanden ist, fügen Sie `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}` über der Überschrift des Vorjahres hinzu.
- **Fügen Sie** das `{hide-from-toc}`-Präfix neuen Einträgen hinzu - das wird nur für ältere Einträge verwendet, wenn sie außerhalb des sichtbaren Navigationsbereichs liegen (siehe Bekannte Inkonsistenzen unten).

### Bekannte Inkonsistenzen, die überwacht werden müssen (nicht replizieren)

- Mehrere Inhaltsverzeichniseinträge von Anfang 2026 sind versehentlich unter der Überschrift `Fusion releases - 2025` verschachtelt, obwohl die Seiten selbst Versionen von 2026 sind. Wenn Sie einen neuen Eintrag hinzufügen, überprüfen Sie immer, ob er unter der Überschrift &quot;**Jahr“ landet** und nicht an der Stelle, an der der vorherige Eintrag liegt.
- Bei einigen älteren Seitentiteln/H1s wird das Komma vor dem Jahr weggelassen (`July 13 2026` statt `July 13, 2026`). Verwenden Sie auf neuen Seiten immer das Komma .

## Schritt 6: Endgültige Checkliste

- [ ] Datei im richtigen Pfad ohne vorangestellte Nullen im Datum erstellt
- [ ] Frontmatter verwendet `hidefromtoc: true`, keine erfundenen `exl-id`/`TQID`
- [ ] Titel-/Beschreibungsübereinstimmung, Datum enthält Kommas
- [ ] Jede Funktion verfügt über eine Beschreibung und einen verifizierten Link „Für weitere Informationen“
- [ ] Funktionen für die erforderliche Aktion/Einstellung haben einen `>[!IMPORTANT]`
- [ ] Neue Seite wurde als neuester Eintrag in `fusion-release-activity.md` unter dem richtigen Jahr/Monat hinzugefügt
- [ ] Neue Seite wurde als neuester Eintrag in `TOC.md` unter der korrekten Jahresüberschrift hinzugefügt
- [ ] Neujahr/Monat-Überschriften werden bei Bedarf erstellt, wobei das Vorjahr in `fusion-release-activity.md` ausgeblendet wird

## Weitere Ressourcen

Vollständig bearbeitete Beispiele (eine einfache Woche mit mehreren Funktionen und eine mit einem `>[!IMPORTANT]` Aktionsaufruf) finden Sie unter `.claude/commands/_fusion-release-notes-reference.md`.
