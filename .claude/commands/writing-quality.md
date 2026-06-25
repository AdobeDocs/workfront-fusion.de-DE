---
name: writing-quality
description: Überprüfen und verbessern Sie die technische Schreibqualität für Workfront-Artikel mit Anleitungen und die allgemeine Dokumentation. wendet das Workfront-Dokumentationshandbuch und die Grundsätze aus der Entwicklung technischer Qualitätsinformationen an. Wird beim Bearbeiten, Überprüfen oder Schreiben von Anleitungsartikeln, Übersichtsartikeln, Referenzartikeln oder allgemeiner Dokumentation verwendet. Für Versionshinweise nicht verwenden - Verwenden Sie stattdessen die Qualifikation zum Formatieren von Versionshinweisen .
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 1%

---


# Schreibqualität

Prüft und verbessert die Workfront-Dokumentation mithilfe des Workfront-Dokumentationsstilhandbuchs und der DQTI-Prinzipien.

## Workflow

Bei der Überprüfung oder Bearbeitung von Inhalten:

1. Zieldatei lesen
2. Wenden Sie die folgenden Regeln an - beheben Sie Probleme direkt oder markieren Sie sie
3. Bewahren Sie die Absicht und technische Genauigkeit des Autors auf
4. Ausführliche Regeln zu Terminologie, Zeichensetzung und Verfahren finden Sie unter .claude/commands/_writing-quality-reference.md

## Stimme und Standpunkt

- Verwenden Sie **zweite Person** („Sie können…„) Adressierung des Lesers
- Kontraktionen für einen Gesprächston verwenden (nicht, nicht, nicht, es ist, sie sind)
- Verwenden Sie „Wir empfehlen“ für Best Practices - nicht „Es wird empfohlen“ oder „Sie sollten“.
- Wenn Sie für eine Benutzergruppe schreiben, verweisen Sie auf andere Rollen in der dritten Person („Sie können… Der Workfront-Administrator kann jedoch einschränken…„)
- Benutze nie geschlechtsspezifische Pronomina - strukturiere den Satz um oder verwende „sie“
- Kein Schrägstrich für Auswahlmöglichkeiten - verwenden Sie „oder“ („er oder sie“ oder nicht „er/sie„)

## Klarheit (DQTI)

- Eine Idee pro Satz
- Sätze nach Möglichkeit unter ~25 Wörtern speichern
- Mit der Aktion oder dem Ergebnis führen, nicht mit dem Hintergrundkontext
- Verwenden Sie das einfachste Wort, das die Bedeutung vermittelt („Verwenden“ nicht „Nutzen“, „Starten“ nicht „Initiieren“, „Über“ nicht „Belangen„).
- Nominalisierungen vermeiden („create“ statt „the creation of“, „configure“ statt „the configuration of„)
- Spezifische, konkrete Sprache verwenden - vage Begriffe („mehrere“, „verschiedene“, „einige„) vermeiden
- Vermeidung doppelter Negative
- Optionale Pronomina („that“, „who„) benutzen, um die Satzstruktur klarer zu machen

## Konkretheit (DQTI)

- Verwenden spezifischer Beispiele anstelle abstrakter Beschreibungen
- Realistische Werte in Beispiele aufnehmen
- Benennen Sie die genauen Elemente, Felder und Bereiche der Benutzeroberfläche

## Aufgabenausrichtung (DQTI)

- Konzentrieren Sie sich darauf, was der Benutzer tun **, nicht darauf, was das System *ist*
- Lead-Prozeduren mit Verben des Typs „Aufgabe erstellen“, „Benachrichtigungen konfigurieren“
- Bieten Sie genügend Kontext, damit der Benutzer handeln kann, aber nicht mehr
- Fügen Sie einen Link zu einer detaillierten Hilfe hinzu („Weitere Informationen finden Sie [ „Artikel].„)

## Großschreibung

- **Überschriften**: Der Satz ist immer groß („Aufgabe erstellen“ statt „Aufgabe erstellen„).
- **Workfront-Begriffe**: Wird nur großgeschrieben, wenn direkt auf ein Benutzeroberflächenelement verwiesen wird
   - Direkter Verweis: „Füllen Sie das Feld Geplantes Abschlussdatum aus.“
   - Indirekte Referenz: „Jede Aufgabe muss ein geplantes Abschlussdatum haben.“
   - Tipp: Wenn Sie „the“ oder „a“ vor den Begriff setzen können, sollte dieser in der Regel kleingeschrieben sein
- **Schaltflächen**: Folgen Sie der Groß-/Kleinschreibung der Benutzeroberfläche, mit Ausnahme von Schaltflächen → Großbuchstaben
- **Roles**: „Systemadministrator“ für die Rolle in der Benutzeroberfläche; &quot;Workfront-Administrator“ für die Person

## Überschriften

- Verwenden des Befehls „Imperative“ im Satzfall („Aufgabe erstellen“, „Zugriffsebenen konfigurieren„)
- Die Überschriften sollten aufgabenbasiert sein und beschreiben, was der Benutzer erreichen wird
- Übersichtsartikel enden mit „Overview“ („Projects overview„)
- Lange Abschnitte in mehrere Überschriften mit klaren Unterzielen unterteilen

## Querverweise und Links

Verwenden Sie diese exakten Muster:

| Situation | Format |
|-----------|--------|
| Link nach der Angabe von Informationen | „Weitere Informationen finden Sie unter [Artikelname].“ |
| Link ohne vorherige Info | „Weitere Informationen finden Sie unter [Artikelname].“ |
| Link zu einem Abschnitt in einem anderen Artikel | „Weitere Informationen finden Sie unter [Abschnittsname] in [Artikelname].“ |
| Link zu einem Abschnitt im selben Artikel | „Weitere Informationen finden Sie unter [Abschnittsname] in diesem Artikel.“ |

- In einem Absatz: Inline mit dem Text
- In einem Verfahrensschritt: In einer neuen Zeile nach dem Schritt
- Mehrere Links: Aufzählungsliste verwenden
- „obere rechte Ecke“ / „obere linke Ecke“ für Bildschirmpositionen verwenden

## Fett und Kursiv

- **Fett** klickbare Aktionen und Benutzeroberflächenelemente nur in Verfahrensschritten
- Fett gedruckte UI-Elemente außerhalb von Verfahrensschritten nicht verwenden
- Keine fett gedruckten Dialogfeldnamen, Seitennamen, Symbolnamen oder Menünamen außerhalb von Schritten
- Verwenden *kursiv* für Text, den der Benutzer eingeben soll (“*my.workfront.com* in das URL-Feld eingeben„)
- Verwenden Sie niemals Kursiv für die Hervorhebung - strukturieren Sie stattdessen den Satz um

## Hinweise, Tipps und Warnungen

Sparsam benutzen - Überbeanspruchung macht sie für die Leser unsichtbar.

- Maximal ein Hinweis/Tipp/Warnhinweis pro Abschnitt
- Nie mehrere Notizen stapeln
- Verknüpfte Notizen zu einer Notiz mit Aufzählungsliste kombinieren
- Verwenden Sie keine Notizen, um neue Funktionen anzukündigen - überarbeiten Sie stattdessen den Artikeltext

| Typ | Zweck |
|------|---------|
| `>[!NOTE]` | Informationen, die nicht zum Absatz passen; Frustration vermeiden; Versionierung/Kompatibilität |
| `>[!TIP]` | Nice-to-have Vorschläge, die dem Benutzer das Leben erleichtern |
| `>[!IMPORTANT]` | Wichtige Informationen für den Schritt oder das Verfahren |
| `>[!WARNING]` | Benutzer auf möglichen Datenverlust hinweisen |

## Vorgänge

- Verwenden von Befehlsüberschriften (im Folgenden „Aufgabe erstellen„)
- Einführung nur, wenn nötig — die Überschrift sollte ausreichen
- Bevorzugtes Intro-Format: Infinitiv-Satz + Doppelpunkt („So erstellen Sie ein temporäres Kennwort:„)
- Für einstufige Vorgänge wird weiterhin eine nummerierte Liste verwendet
- „Typ“ oder „Auswählen“ verwenden - vage Wörter wie „festlegen“ oder „angeben“ vermeiden.
- Bedingte Schritte: „(Bedingt) Wenn Sie Mitglied mehrerer Teams sind, wählen Sie …“
- Optionale Schritte: „(Optional) Um ein Emoji hinzuzufügen, klicken Sie auf …“
- Die Systemantwort vor oder unmittelbar nach ihrem Auftreten beschreiben
- Mehrere Methoden: Dokumentieren Sie zunächst den einfachsten Weg und verwenden Sie dann „Oder“

### Eckige Klammern in Verfahren

- Verwenden Sie `>`, um die Menü-/Registerkartennavigation anzuzeigen: „Klicken Sie auf **E** > **Benachrichtigungen**&quot;
- Fettgedruckte Schaltflächennamen, nicht die Klammern
- Leerzeichen um Klammern einschließen
- Keine Klammern für die Navigation im Hauptmenü verwenden - Hauptmenüausschnitt verwenden

## Interpunktion-Kurzreferenz

| Regel | Beispiel |
|------|---------|
| Oxford-Komma immer | „Motiv, Mittel und Chance“ |
| Komma vor „then“ in Prozeduren | „Klicken Sie auf Setup und dann auf Schnittstelle.“ |
| Komma nach Jahr in einer Datummitte | „Die Ausgabe vom 2. Januar 2016…“ |
| Kein Komma, nur für Monat und Jahr | „Januar 2016“ |
| Doppelpunkt vor einer Liste, Kleinbuchstaben nach | „Wählen Sie eine der folgenden Optionen aus: Option A“ |
| Kein Doppelpunkt nach den Verfahrensüberschriften | „Aufgabe erstellen“ (nicht „Aufgabe erstellen:„) |
| Em stricht sparsam | Strukturieren Sie den Satz nach Möglichkeit um |
| Punkte in Dateierweiterungen | „PDF-Datei hochladen“ |

Vollständige Satzzeichen und Terminologieregeln finden Sie unter .claude/commands/_writing-quality-reference.md.

## Vollständigkeit (DATI)

- Alle Informationen enthalten, die der Benutzer benötigt, um zu verstehen und zu handeln
- Geben Sie keine Informationen ein, die der Benutzer nicht benötigt
- Geben Sie immer einen Link „Für weitere Informationen“ zu einer detaillierten Dokumentation an
- Document System-Standardwerte: „(Standard)“ in Listen oder im Satz beschreiben

## Organisation (DQTI)

- Logische Struktur mit progressiver Offenlegung (Übersicht → Details → Referenz)
- Neuester Inhalt zuerst für zeitgesteuerte Seiten (z. B. Versionshinweise)
- Ein Thema pro Abschnitt
- Listen für mehr als 3 parallele Elemente verwenden
- Verwenden von Tabellen für strukturierte Vergleiche oder Feldbeschreibungen
- Vermeiden Sie Textwandabsätze - unterteilen Sie sie in verdauliche Abschnitte.

## Artikeltypen

| Typ | Zweck | Titelübereinkommen |
|------|---------|-----------------|
| Überblick | Kontext, Diagramme, wie Dinge funktionieren — keine Verfahren | Endet mit „overview“ |
| Anleitung | Spezifische Aufgabe mit klaren Schritten | Verb „Imperativ“ |
| Erste Schritte | Setup-Info + Links für neue Benutzer | „Erste Schritte mit…“ |
| Referenz | Beschreibung der Felder in Tabellen | Beschreibender Substantivsatz |

## Validierungs-Checkliste

Überprüfen Sie nach der Bearbeitung Folgendes:

- [ ] Zweite Person in ganz („Sie„), Kontraktionen verwendet
- [ Groß-/Kleinschreibung ] alle Überschriften
- [ ] Workfront-Begriffe korrekt großgeschrieben (direkte oder indirekte Referenz)
- [ Nur bei anklickbaren Aktionen innerhalb von Verfahrensschritten fett ]
- [ ] Querverweise verwenden das Standardformat („Weitere Informationen finden Sie unter…„)
- [ ] Anmerkungen/Tipps/Warnungen nicht gestapelt, maximal eine pro Abschnitt
- [ ] Oxford-Komma wird durchgängig verwendet
- [ ] Verfahrensschritte verwenden bestimmte Verben (Typ, Auswahl, Klick - nicht „festlegen“ oder „angeben„)
- [ ] bedingte/optionale Schritte, die korrekt gekennzeichnet sind
- [ ] Keine Geschlechtspronomen
- [ ] Sätze sind klar, konkret und aufgabenorientiert
