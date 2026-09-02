---
name: fusion-doc-request
description: Handhabung einer Fusion-Dokumentationsanfrage über die
source-git-commit: e354c51f13bd4f15172de068cac9720bd097eb8d
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---


# Fusion-Dokumentationsanfrage

Behandelt das im `#fusion-documentation` Slack-Kanal veröffentlichte Muster „Neue Dokumentationsanfrage von {person}&quot;: Lesen Sie die Anfrage, aktualisieren Sie die Dokumente und erstellen Sie dann eine Tracking-Aufgabe mit demselben benutzerdefinierten Workfront-Formular, das für jede vorherige Anfrage dieser Art verwendet wird.

Dies ist ein anderer Workflow als die `fusion-release-notes`. Diese Qualifikation aktualisiert einen Referenzartikel und erstellt eine Workfront-Aufgabe. Sie erstellt oder aktualisiert keine wöchentliche Versionshinweisseite für Fusion in diesem Repository, selbst wenn in der Anfrage „Ankündigung erforderlich: Ja“ steht. Verwenden Sie `fusion-release-notes` nur, wenn der Benutzer separat nach einem wöchentlichen Versionshinweis fragt.

## Schritt 1: Anforderungsdetails abrufen

Wenn ein Slack-Link angegeben ist, analysieren Sie die `channel_id` und `message_ts` aus der URL und rufen Sie den Thread ab (`slack_get_thread_replies` oder `slack_read_thread`, je nachdem, welches Slack MCP-Tool verbunden ist - versuchen Sie beide, wenn einer fehlschlägt). Behalten Sie den Permalink/die URL des Threads bei - er wird in Schritt 3 benötigt.

Slack-Verbindungen in dieser Umgebung sind fehlerhaft (abgelaufene Token, trennt die Verbindung zur Sitzungsmitte). Wenn ein Abruf fehlschlägt:
- Einmal versuchen.
- Wenn der Abruf immer noch fehlschlägt, teilen Sie dem Benutzer einfach mit, dass der Abruf fehlgeschlagen ist, und bitten Sie ihn, den Anfrageinhalt direkt einzufügen. Raten Sie nicht über den Inhalt und geben Sie nicht leise auf, ohne es zu sagen.

Die Anfragevorlage enthält die folgenden Felder: „Jedes extrahieren“:

&#x200B;* **Funktionstitel**
&#x200B;* **Beschreibung**
&#x200B;* **Punkte, die der Dokumentation hinzugefügt werden müssen** *(manchmal vorhanden - spezifische Abschnitte/Details, die der Antragsteller abdecken möchte; behandeln Sie diese nach Bedarf, nicht optional, falls angegeben)*
&#x200B;* **Voraussichtliches Veröffentlichungsdatum**
&#x200B;* **Ankündigung erforderlich** *(Ja/Nein - nur zur Information; siehe oben stehenden Hinweis. Aktion für dieses Feld nicht ausführen.)*

Wenn die Anfrage mit der vollständigen Spezifikation auf eine Confluence-Wiki-Seite verweist, rufen Sie sie ab (`get_wiki_content`), bevor Sie die Dokumentation schreiben. Verlassen Sie sich nicht nur auf die Slack-Zusammenfassung für technische Details (exakte Feldnamen, Schritte, Benutzeroberflächen-Kennzeichnungen) - rufen Sie diese aus der Wiki-Spezifikation ab, wenn eine verknüpft ist.

## Schritt 2: Dokumentation aktualisieren

Suchen Sie die relevanten vorhandenen Artikel in diesem Repository (Grep für zugehörige Modulnamen, Benutzeroberflächen-Bezeichnungen oder Einstellungsnamen - raten Sie nicht auf die Datei). Aktualisieren Sie sie, um die Änderung widerzuspiegeln, wobei Sie der vorhandenen Struktur, Überschriftenebene und dem Hausstil dieses Artikels folgen.

&#x200B;* Erfinden Sie keine technischen Details (exakte Feldnamen, Berechtigungsumfänge, Konfigurationsschritte), die nicht in der Slack-Anfrage oder verknüpften Wiki-Spezifikation enthalten sind. Wenn etwas nicht bestätigt ist, kennzeichnen Sie es inline als HTML-Kommentar (z. B. `<!-- BECKY CHECK ME: confirm the exact permission scope before publishing -->`), anstatt es zu erraten - nie als sichtbarer Hinweis. Er darf nicht auf der veröffentlichten Seite gerendert werden.
&#x200B;* Wenn dies eine brandneue Artikeldatei erfordert (nicht nur eine Änderung an einer bestehenden), folgen Sie den ständigen Konventionen dieses Repositorys: keine fabrizierten `exl-id`/`TQID` in der Frontseite, verkabeln Sie die neue Seite in das entsprechende Inhaltsverzeichnis und konvertieren Sie die Datei nach der Erstellung in CRLF/no-BOM (das `Write`-Tool verwendet standardmäßig LF).

## Schritt 3: Workfront-Aufgabe erstellen

Projekt: **Produktdokumentationsaufgaben - für Entwicklungsprobleme, die Messaging erfordern**. Lösen Sie seine ID mit `insights_find_id_by_name` (Entität `project`) auf anstatt sie hartcodiert zu haben, falls sie sich jemals ändert - siehe Bekannte Werte unten für die letzte aufgelöste ID.

Aufgabenfelder:

| Feld | Wert |
|---|---|
| `name` | `Becky - {Feature Title}` |
| `projectID` | Von der obigen Projektsuche |
| `assignedToID` | Der aktuelle Benutzer von `insights_get_current_user` |
| `categoryID` | die benutzerdefinierte Formular-ID der Produktdokumentation - siehe Bekannte Werte unten. Wenn es jemals unklar ist, fragen Sie zur Bestätigung `task.task_categoryID` nach einer kürzlich durchgeführten gleichrangigen Aufgabe in diesem Projekt ab. |
| `description` | den **vollständigen Slack-Nachrichtentext** (alle Felder aus der Anfragevorlage, keine Umschreibung), gefolgt von einem Link zur Slack-Konversation |
| `DE:Release notes` | Ein formatierter Versionshinweis, siehe Format unten |
| `DE:Preview Date Known` | `Yes`, standardmäßig |
| `DE:Preview Date` | das **erwartete Veröffentlichungsdatum) der Anfrage** |
| Produkt/Bereich | Wählen Sie `Fusion` aus (ein Aufzählungsfeld im Produktdokumentationsformular; bestätigen Sie den genauen Feldnamen mit `insights_search_fields`, falls er unklar ist). |

Legen Sie die Felder für das Vorschaudatum als Teil desselben Erstellungsaufrufs fest - lassen Sie sie nicht zu einem späteren Zeitpunkt liegen oder warten Sie, bis Sie gefragt werden. Wenn der/die Benutzende später ein anderes Datum angibt oder sagt, dass das Datum noch nicht wirklich bekannt ist, aktualisiert dies entsprechend, füllt es aber standardmäßig jedes Mal aus.

Format der Versionshinweise für das `DE:Release notes` Feld. Beginnen Sie immer mit `***FUSION***` in einer eigenen Zeile, dann mit einer leeren Zeile, dann mit dem Titel - dadurch wird die Anmerkung auf einen Blick als zu Fusion gehörend (im Gegensatz zu Core Workfront) markiert:

```markdown
***FUSION***

## {Feature Title}

{Description of what changed and why it matters, in second person. A sentence or two is enough for a simple change - use multiple paragraphs and/or a bulleted list for anything with several parts or steps, the same way a full weekly release note would.}

For more information, see [{Article title}](/help/workfront-fusion/{path-to-article}.md).
```

Rufen Sie vor dem Aufruf „create“ `read_workflow_docs` mit `workfront://tools/create-any-object` auf. Dieser Aufruf legt benutzerdefinierte Felder und einen Aufzählungswert (`DE:Preview Date Known`) fest, wofür er gemäß den Regeln des MCP-Servers erforderlich ist.

## Schritt 4: Zurück an den Benutzer bestätigen

Klarer Bericht:

&#x200B;* Welche DOC-Datei(en) Sie geändert haben und was Sie hinzugefügt haben.
&#x200B;* Aufgabenname und URL.
&#x200B;* Die genauen Feldwerte, die Sie festgelegt haben, einschließlich der Felder für das Vorschaudatum.
&#x200B;* Alles, worauf man nicht ganz vertrauen konnte - z.B. Slack war nicht erreichbar und man arbeitete nur aus eingefügtem Text, der Zielartikel war mehrdeutig oder ein technisches Detail war nicht im Quellmaterial vorhanden und wurde markiert, anstatt geraten zu werden.

## Bekannte Werte (aus früheren Ausführungen)

Bestätigen Sie, dass diese immer noch aufgelöst werden, anstatt davon auszugehen, dass sie dauerhaft sind:

&#x200B;* Projekt „Produktdokumentationsaufgaben - für Entwicklungsprobleme, die Messaging erfordern“ ist der ID `5e69583f00236b9f767c3e3944100ee4` zugeordnet
&#x200B;* Benutzerdefiniertes Formular für die Produktdokumentation (`categoryID`) ist `5d7275b9000514604bd969d418725843`
&#x200B;* Benutzerdefinierte Felder: `DE:Release notes`, `DE:Preview Date Known`, `DE:Preview Date`
