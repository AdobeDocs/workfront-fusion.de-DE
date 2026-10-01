---
title: Adobe Workfront Fusion MCP-Server-Tools
description: Referenzliste der Tools, die der Adobe Workfront Fusion-MCP-Server für KI-Agentenplattformen und -Mitarbeiter bereitstellt.
source-git-commit: 322a34df48a5218bc045e6cac6a5a8b3837e8c2e
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 7%
---

# Adobe Workfront Fusion MCP-Server-Tools


In diesem Artikel werden die Tools aufgelistet, die der Adobe Workfront Fusion MCP-Server einem verbundenen KI-Agenten bereitstellt. Der Agent ruft diese Tools in Ihrem Namen auf, wenn Sie ihn bitten, Fusion-Elemente zu finden, zu überprüfen, zu erstellen, auszuführen, zu aktualisieren oder zu löschen.

Die gleichen Tools stehen in jeder unterstützten Oberfläche zur Verfügung: benutzerdefinierte MCP-Verbindungen in Claude, ChatGPT, Copilot oder Ihrem eigenen Agenten und Coworker, sowohl eigenständig als auch in der rechten Leiste von Fusion. Informationen zum Setup finden Sie unter [Konfigurieren des Adobe Workfront Fusion MCP-Servers](configure-fusion-mcp-server.md).

Der Agent agiert in Fusion mithilfe Ihrer Adobe ID-, Fusion-Organisationsrolle und Teamrollen. Ein Tool funktioniert nur, wenn Sie über die entsprechende Berechtigung in Fusion verfügen. Adobe übernimmt keine Verantwortung für Änderungen, die der Agent an Ihren Fusion-Daten vornimmt.

## Lese- und Schreibaktionen

Jedes Tool ist wie folgt klassifiziert:

* **Lesen**: Ruft Informationen ab, ohne etwas zu ändern, z. B. Listenszenarien oder eine Ausführung zu erhalten.
* **Write**: Erstellt, ändert, führt Fusion-Daten aus oder löscht sie, z. B. durch Klonen eines Szenarios oder Löschen einer Webhook-Warteschlange.

## Organisations-Tools

Die aktive Organisation gilt für alle anderen Tools in der aktuellen Sitzung.

| Tool | Name | Aktion | Beschreibung |
| --- | --- | --- | --- |
| Organisationen auflisten | `fusion_orgs_list` | Lesen | Listet die Fusion-Organisationen auf, auf die Sie zugreifen können, mit ID, Region (Zone) und Bezeichnung. |
| Aktive Organisation festlegen | `fusion_orgs_set` | Session | Wechselt die aktive Organisation für die aktuelle Sitzung. Ändert keine Fusion-Daten. |

## Szenario-Tools

### Szenarios

| Tool | Name | Aktion | Beschreibung |
| --- | --- | --- | --- |
| Auflisten von Szenarien | `fusion_scenarios_list` | Lesen | Listet Szenarien in der Organisation auf. |
| Szenario abrufen | `fusion_scenarios_get` | Lesen | Gibt ein Szenario zurück, einschließlich der vollständigen Blueprint. |
| Szenario-Abhängigkeiten abrufen | `fusion_scenarios_getDependencies` | Lesen | Gibt die Verbindungen, Schlüssel, Datenspeicher, Datenstrukturen und Webhooks der Blueprint-Referenzen des Szenarios zurück. |
| Abhängige Szenarien suchen | `fusion_scenarios_dependents` | Lesen | Sucht Szenarien, die auf einen bestimmten Webhook, Datenspeicher, eine Datenstruktur, eine Verbindung, einen Schlüssel oder ein Szenario verweisen. Nützlich für Auswirkungsanalysen, bevor eine Ressource geändert oder gelöscht wird. |
| Blueprint validieren | `fusion_scenarios_validate_blueprint` | Lesen | Validiert einen Blueprint strukturell anhand eines Teams (Modulverweise, Verbindungen, erforderliche Felder), ohne etwas zu speichern. |
| Szenario erstellen | `fusion_scenarios_create` | Schreiben | Erstellt in einem Team ein Szenario aus einer Blueprint mit optionalem Namen, optionaler Beschreibung, Ordner, Zeitplan und sequenzieller Verarbeitung. |
| Klonen-Szenario | `fusion_scenarios_clone` | Schreiben | Klonen Sie ein Szenario in dasselbe oder ein anderes Team. Beim Klonen über Teams hinweg ordnen Sie jede Verbindung, jeden Webhook, jeden Datenspeicher, jede Datenstruktur und jeden Schlüssel einer Zielressource zu. Optional ab dem zuletzt verarbeiteten Datensatz. |
| Szenario aktualisieren | `fusion_scenarios_update` | Schreiben | Ändert den Namen, die Beschreibung, den Ordner, die Planung oder den aktiven Status (aktivieren/deaktivieren). Kann auch ein gelöschtes Szenario wiederherstellen. |
| Szenario einmal ausführen | `fusion_scenarios_execute` | Schreiben | Führt ein Szenario einmal aus und wartet (bis zu einer maximalen Wartezeit) auf das Ergebnis, gibt den Status und alle Fehlermeldungen zurück. Wird für sofortige Szenarien (Webhook-ausgelöst) nicht unterstützt. |
| Szenario löschen | `fusion_scenarios_delete` | Schreiben | Löscht ein Szenario. Gelöschte Szenarien können mit &quot;**-Szenario“ wiederhergestellt**. |

Beispiel-Eingabeaufforderungen:

* _Welche aktiven Szenarien im Marketing-Team wurden in den letzten sechs Monaten nicht bearbeitet?_
* _Welche Verbindungen verwendet das Szenario „Synchronisierung von Salesforce → Workfront&quot;_
* _Klonen Sie die „Lead-Aufnahme“ in das Sales-Team und tauschen Sie die Sales Salesforce-Verbindung aus._
* _Validieren Sie diese Blueprint, bevor ich sie importiere._
* _Führen Sie „Nightly Report“ einmal aus und sagen Sie mir, ob es erfolgreich ist._

### Szenario-Versionen

| Tool | Name | Aktion | Beschreibung |
| --- | --- | --- | --- |
| Auflisten von Szenario-Versionen | `fusion_scenario_versions_list` | Lesen | Listet gespeicherte Versionen eines Szenarios auf. Filtern Sie nach `version`, `createdAt`, `comment`. |
| Szenario-Version abrufen | `fusion_scenario_versions_get` | Lesen | Gibt den Blueprint und die Metadaten für eine bestimmte Version zurück. |

Beispiel-Eingabeaufforderungen:

* _Was hat sich zwischen Version 12 und Version 14 dieses Szenarios geändert?_

### Ordner

| Tool | Name | Aktion | Beschreibung |
| --- | --- | --- | --- |
| Ordner auflisten | `fusion_folders_list` | Lesen | Listet Szenario-Ordner mit Szenario-Anzahl auf. |
| Ordner erstellen | `fusion_folders_create` | Schreiben | Erstellt einen Ordner in einem Team. |
| Ordner umbenennen | `fusion_folders_update` | Schreiben | Benennt einen Ordner um. |
| Ordner löschen | `fusion_folders_delete` | Schreiben | Löscht einen Ordner. |

## Ausführungs-Tools

| Tool | Name | Aktion | Beschreibung |
| --- | --- | --- | --- |
| Ausführungen auflisten | `fusion_executions_list` | Lesen | Führt Ausführungen für ein Szenario oder für eine unvollständige Ausführung auf. Filtern Sie nach `status` (z. B. `status==3` auf Fehler, `status==2` auf Warnungen), `timestamp`, `duration`, `bundles`, `operations`, `transfer`. Optional umfasst Prüfläufe. |
| Ausführung abrufen | `fusion_executions_get` | Lesen | Gibt eine einzelne Ausführung und Metadaten zu ihrem Szenario oder einer unvollständigen Ausführung zurück. |

Beispiel-Eingabeaufforderungen:

* _Fehlgeschlagene Ausführungen von „Rechnungssynchronisierung“ von gestern anzeigen und Fehler zusammenfassen._
* _Welche Ausführung dieses Szenarios hat die meisten Vorgänge in dieser Woche verwendet?_

## Vorgänge (Verwendung)-Tools

| Tool | Name | Aktion | Beschreibung |
| --- | --- | --- | --- |
| Abrufen von Vorgängen | `fusion_operations_get` | Lesen | Gibt eine Vorgangszeitreihe (nach Tag oder Monat) für einen Datumsbereich von bis zu 1 Jahr zurück. Nach Team, Szenario oder Paket filtern; nach Modul, Paket, Szenario oder Team gruppieren. |
| Zusammenfassung der Vorgänge abrufen | `fusion_operations_summary_by_org` | Lesen | Gibt die Gesamtzahl der Vorgänge pro Szenario und Team für einen Datumsbereich plus die Gesamtsumme zurück. |

Beispiel-Eingabeaufforderungen:

* _Die 10 wichtigsten Szenarien nach Vorgängen im letzten Monat._
* _Wie viele Vorgänge hat die Salesforce-App im 3. Quartal verwendet?_

## Verbindung und wichtige Tools

Diese Tools geben nur Metadaten zurück. Sie geben keine Anmeldeinformationen, Token oder geheimen Werte zurück.

| Tool | Name | Aktion | Beschreibung |
| --- | --- | --- | --- |
| Verbindungen suchen | `fusion_connections_search` | Lesen | Listet Verbindungen auf. Filtern Sie nach `name`, `accountName`, `accountType`, `expire`, `teamId`, `scopesCount`, `editable`, `environmentType`, `authenticationType`. |
| Verbindung abrufen | `fusion_connections_get` | Lesen | Gibt Details für eine einzelne Verbindung zurück. |
| Suchschlüssel | `fusion_keys_search` | Lesen | Führt Schlüssel auf. Filtern Sie nach `name`, `typeName`, `teamId`. |
| Schlüssel abrufen | `fusion_keys_get` | Lesen | Gibt Details für einen einzelnen Schlüssel zurück. |

Beispiel-Eingabeaufforderungen:

* _Welche Verbindungen laufen in den nächsten 30 Tagen ab, und in welchen Szenarien werden sie verwendet?_

## Webhook-Tools

### Webhooks

| Tool | Name | Aktion | Beschreibung |
| --- | --- | --- | --- |
| Webhooks auflisten | `fusion_hooks_list` | Lesen | Listet Webhooks auf. Filtern Sie nach `name`, `teamId`, `type`, `enabled`, `gone`, `typeName`, `scenarioId`, `priority`, `detached` und mehr. |
| Webhook abrufen | `fusion_hooks_get` | Lesen | Gibt die Konfiguration eines Webhooks, die Besitzerbindung und externe Referenzen zurück. |
| Abhängige Webhooks suchen | `fusion_hooks_dependents` | Lesen | Sucht Webhooks, die auf eine bestimmte Verbindung verweisen. |

### Webhook-Warteschlange

| Tool | Name | Aktion | Beschreibung |
| --- | --- | -------- | --- |
| Warteschlangenstatus abrufen | `fusion_queue_stats` | Lesen | Gibt die Anzahl an Ereignissen in der Warteschlange, die Warteschlangenbegrenzung und die Aktivierung des Webhooks zurück. |
| Listenwarteschlange | `fusion_queue_list` | Lesen | Listet empfangene Webhook-Ereignisse auf, die darauf warten, verarbeitet zu werden. |
| Warteschlangenelement abrufen | `fusion_queue_get` | Lesen | Gibt ein einzelnes Ereignis in der Warteschlange zurück, einschließlich der decodierten Payload. |
| Warteschlangenelemente löschen | `fusion_queue_delete` | Schreiben | Löscht bestimmte Ereignisse in der Warteschlange (bis zu 50) oder löscht die Warteschlange, wobei optional einige Ereignisse ausgeschlossen werden. Derzeit verarbeitete Ereignisse können nicht gelöscht werden. |

Beispiel-Eingabeaufforderungen:

* _Wird der Webhook „Formularübermittlungen“ gesichert?_
* _Anzeige der Payload des ältesten Ereignisses in der Warteschlange._

## Tools für Datenspeicher und Datenstruktur

| Tool | Name | Aktion | Beschreibung |
| --- | --- | --- | --- |
| Auflisten von Datenspeichern | `fusion_datastores_list` | Lesen | Listet Datenspeicher mit der Anzahl, Größe und Maximalgröße der Datensätze auf. |
| Datenspeicher abrufen | `fusion_datastores_get` | Lesen | Gibt die Metadaten und die Verwendung eines Datenspeichers, die verknüpfte Datenstruktur und die strikte Validierungseinstellung zurück. |
| Auflisten von Datenspeicherdatensätzen | `fusion_data_list` | Lesen | Liest Datensätze (Schlüssel + JSON-Daten) aus einem Datenspeicher mit Offset-Paging. |
| Suchen nach abhängigen Datenspeichern | `fusion_datastores_dependents` | Lesen | Sucht Datenspeicher, die eine bestimmte Datenstruktur verwenden. |
| Datenstrukturen suchen | `fusion_data_structures_search` | Lesen | Listet Datenstrukturen auf. Filtern Sie nach `name`, `strict`, `teamId`. |
| Datenstruktur abrufen | `fusion_data_structures_get` | Lesen | Gibt eine Datenstruktur einschließlich der vollständigen Feldspezifikation zurück. |

Beispiel-Eingabeaufforderungen:

* _Welche Datenspeicher sind zu über 80 % ausgelastet?_
* _Zeigen Sie mir die ersten 20 Datensätze im Datenspeicher „Kundenkarte“._

## Aktivitätsprotokoll-Tools

| Tool | Name | Aktion | Beschreibung |
| --- | --- | --- | --- |
| Aktivitätsprotokolle auflisten | `fusion_activity_logs_list` | Lesen | Listet Audit-Ereignisse für die Organisation auf (wer was getan hat, zu welcher Entität wann). Filtern Sie nach `entity` (z. B. `scenario`, `connection`, `webhook`, `data store`, `user`), `action` (z. B. `created`, `deleted`, `updated`, `transferred ownership`), Benutzer, Team und Zeitstempel. |
| Aktivitätsprotokolle exportieren | `fusion_activity_logs_export` | Lesen | Exportiert Aktivitätsprotokolle als CSV- oder XLSX-Dateien und verwendet dabei dieselben Filter. |

Beispiel-Eingabeaufforderungen:

* _Wer hat Szenarien in den letzten 7 Tagen gelöscht?_
* _Exportieren Sie alle Verbindungsänderungen in diesem Quartal nach Excel._

## Kollegin

Alle Tools in diesem Artikel sind in Coworker verfügbar, sowohl eigenständig als auch in der rechten Leiste von Fusion, vorbehaltlich derselben Lese-/Schreibeinstellungen und Ihrer Berechtigungen.

## So werden Tools aktualisiert

Wenn Adobe eine neue Version des Fusion MCP-Servers veröffentlicht, übernehmen Connected Agents automatisch den aktualisierten Toolsatz. Sie müssen die Verbindung nicht wiederherstellen.

