---
title: Häufig gestellte Fragen zur Szenarienplanung
description: Die Informationen in diesem Artikel können bei der Erstellung von Szenarien in Workfront Fusion hilfreich sein.
author: Becky
feature: Workfront Fusion
exl-id: 6a1d672d-0bd7-4a3a-b96d-6d8b4c97522d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 1%

---

# Häufig gestellte Fragen zur Szenarienplanung

Die Informationen in diesem Artikel können bei der Erstellung von Szenarien in Workfront Fusion hilfreich sein.

## Was ist ein Szenario?

### Antwort

Ein Szenario definiert eine Sequenz von Schritten, die von Adobe Workfront Fusion ausgeführt werden sollen. Für jedes Szenario geben Sie die Datenquelle an, welche Daten verwendet werden sollen und wie die Daten verarbeitet werden sollen. Mit Fusion können Sie einfache oder komplexe Szenarien erstellen, die den Anwendungsfällen für Ihr Unternehmen entsprechen.

Weitere Informationen zu Szenarien finden Sie unter [Szenario - Übersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md).

## Wie viele Module kann ich in einem Szenario verwenden?

### Antwort

Sie können in einem Szenario beliebig viele Module verwenden. Sie können Module in Routen aufteilen und festlegen, welche Daten durch die einzelnen Routen fließen sollen. Sie können auch die Ausgabe eines Moduls als Eingabe für ein anderes Modul verwenden.

Obwohl es keine Begrenzung für die Anzahl der Module in einem Szenario gibt, können mehr als 150 Module die Szenario-Performance beeinträchtigen.

Weitere Informationen zu Modulen finden Sie unter [Modulübersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md).

## Kann Workfront Fusion mit Dateien arbeiten?

### Antwort

Ja. Workfront Fusion kann Dateien empfangen, speichern, transformieren, konvertieren und verschlüsseln. Fusion bietet außerdem eine Vielzahl integrierter Funktionen, mit denen Benutzer effektiv und kreativ mit den in den Dateien enthaltenen Daten arbeiten können.

Weitere Informationen zum Arbeiten mit Dateien in Fusion finden Sie unter [Zuordnen einer Datei zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-files.md).

## Einige Trigger ermöglichen die sofortige Ausführung von Szenarien. Was bedeutet „sofort“?

### Antwort

Szenarien können in Intervallen ausgeführt werden, die dem von Ihnen angegebenen Zeitplan entsprechen, z. B. jede Stunde oder alle 5 Minuten. Es gibt spezielle Trigger, so genannte Instant-Trigger (Webhooks), die Ihr Szenario sofort starten können, nachdem sie Daten von einem bestimmten Service erhalten haben. Fusion verarbeitet die empfangenen Daten sofort, ohne auf die nächste geplante Ausführung zu warten.

Weitere Informationen zum Unterschied zwischen abgefragten und sofortigen Triggern finden Sie unter [Trigger-Module](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) im Artikel Module - Übersicht.

## Was ist ein Vorgang?

### Antwort

Ein Vorgang ist jede Aufgabe, die von einem Modul ausgeführt wird. Ein Vorgang tritt beispielsweise jedes Mal auf, wenn ein Trigger ausgeführt wird und eine Aktion eine Aufgabe ausführt.

Einige Fusion-Pläne basieren auf der Anzahl der Vorgänge, die Ihr Unternehmen verwendet.

Weitere Informationen zu Vorgängen finden Sie unter [Vorgänge](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

## Was ist eine Datenübertragung?

### Antwort

Die Datenübertragung bezieht sich auf die Datenmenge, die über Ihr Szenario übertragen wird. Beispiel: Ein Szenario ruft ein Bild mit 100 KB von Workfront ab und lädt es dann in einen Dokumentspeicheranbieter hoch. Die in diesem Szenario verwendete Datenmenge beträgt 200 KB.

## Was ist eine Verbindung?

### Antwort

Eine Verbindung ist die Verknüpfung zwischen Ihrem Workfront Fusion-Konto und dem Drittanbieterdienst, den Sie verwenden möchten. Die Verbindung kann beim Bearbeiten eines Szenarios erstellt werden.

Weitere Informationen finden Sie unter [Verbindung - Übersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

## Was sind Aggregatoren?

### Antwort

Ein [!UICONTROL Aggregator] führt Daten in einer Sammlung zusammen. Ein Beispiel dafür sind Dateien, die in ein ZIP-Archiv komprimiert und als E-Mail-Anhang gesendet werden.

Weitere Informationen finden Sie [[!UICONTROL &#x200B; Modul &#x200B;]Aggregator](/help/workfront-fusion/references/modules/aggregator-module.md).

## Was passiert, wenn ich Workfront Fusion eine E-Mail verarbeiten lasse, die mehr als einen Anhang enthält?

### Antwort

Wenn Sie das Modul [!UICONTROL E]Mail[!UICONTROL &#x200B; zum Abrufen von &#x200B;] verwenden, wird jeder Anhang einzeln über die übrigen Module im Szenario gesendet. Ähnliche Module sind auch in anderen Apps verfügbar, die mehrere Dateien gleichzeitig erhalten.
