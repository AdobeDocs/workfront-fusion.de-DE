---
title: Mehrere Szenarien verketten
description: Sie können Szenarien miteinander verketten, sodass ein Szenario ein Trigger zum anderen durchführt, und die vom zweiten Szenario ausgegebenen Daten an das erste zurückgeben.
author: Becky
feature: Workfront Fusion
exl-id: def8d4c1-fc20-4b93-b1fd-be2f60300464
source-git-commit: 7f73007e219714c38dd0cf29d2a1e3a4c8f6f3cc
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# Verketten mehrerer Szenarien

>[!NOTE]
>
>Diese Funktion befindet sich derzeit in Beta.

Sie können Szenarien miteinander verketten, sodass ein Szenario ein Trigger zum anderen durchführt, und die vom zweiten Szenario ausgegebenen Daten an das erste zurückgeben. Dies ermöglicht eine modularere Szenarioerstellung, bei der Sie Szenarioabschnitte in mehreren Szenarien nicht duplizieren müssen.

Sie können mehrere untergeordnete Szenarien aus einem übergeordneten Szenario aufrufen und Sie können ein untergeordnetes Szenario aus mehreren übergeordneten Szenarien aufrufen. Sie können auch untergeordnete Szenarien verschachteln und eines von einem anderen aufrufen.

Wenn ein übergeordnetes Szenario darauf wartet, dass ein untergeordnetes Szenario Daten zurückgibt, wird diese Zeit nicht mit der maximalen Wartezeit des übergeordneten Szenarios verrechnet. Ein übergeordnetes Szenario ruft beispielsweise fünf untergeordnete Szenarien auf, deren Ausführung jeweils 10 Minuten dauert, d. h. insgesamt 50 Minuten. Die Ausführung der Module im übergeordneten Szenario selbst dauert 15 Minuten. Das übergeordnete Szenario überschreitet keine Zeitüberschreitung, obwohl insgesamt 65 Minuten vergangen sind. Dies ist die Zeitüberschreitung von 40 Minuten.

Weitere Informationen zu den Leistungs-Schutzmechanismen von Fusion, einschließlich Zeitüberschreitungen, finden Sie unter [Leistungs-Schutzmechanismen von Fusion](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md).

Anweisungen zum Konfigurieren von Kettenmodulen finden Sie unter [Kettenmodule](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

## Übergeordnete und untergeordnete Szenarien

* Das **übergeordnete** Szenario ruft mithilfe des Moduls **Kette** > **Untergeordnetes Szenario aufrufen** ein anderes Szenario auf. Sie erhält die Ausgabe des untergeordneten Szenarios, das sie in späteren Szenario-Modulen verarbeiten kann.
* Das **untergeordnete** Szenario wird vom übergeordneten Szenario aufgerufen. Ihr Trigger-Modul empfängt Daten aus dem übergeordneten Szenario und gibt die Ausgabe an das übergeordnete Szenario zurück.

Das übergeordnete Szenario erfordert eine Antwort vom untergeordneten Szenario. Untergeordnete Szenarien, die keine Daten zurückgeben, werden derzeit nicht unterstützt.

## Datenstrukturen in verketteten Szenarien

Workfront Fusion verwendet Datenstrukturen, um Informationen vom übergeordneten Szenario zum untergeordneten Szenario zu übertragen. Die Datenstruktur wird im untergeordneten Szenario konfiguriert. Wenn das untergeordnete Szenario aus dem übergeordneten Szenario ausgewählt wird, werden die Felder für die Datenstruktur, die als Eingabe für das untergeordnete Szenario verwendet wird, im übergeordneten Szenario angezeigt. Sie können diesen Feldern Werte zuordnen, die beim Auslösen an das untergeordnete Szenario übergeben werden.

Informationen zu den Modulen, die in den übergeordneten und untergeordneten Szenarien konfiguriert werden müssen, finden Sie unter [Kettenmodule](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

Informationen zu Datenstrukturen finden Sie unter [Datenstrukturen](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

## Datenfluss

1. Daten fließen durch das übergeordnete Szenario.
1. Daten erreichen das Modul Untergeordnetes Szenario aufrufen . Daten werden den Feldern im Szenario „Untergeordnetes Aufrufen“ zugeordnet, die mit den Feldern in der Datenstruktur übereinstimmen, die im Trigger-Modul des untergeordneten Szenarios verwendet wird.
1. Daten aus dem Szenario Untergeordnetes Element aufrufen werden an das untergeordnete Szenario übergeben.
1. Das untergeordnete Szenario verarbeitet Daten und führt Aktionen durch.
1. Das untergeordnete Szenario endet mit der Antwort an das übergeordnete Modul zurückgeben.
1. Die Ausgabe der Rückgabeantwort an das übergeordnete Modul wird an das übergeordnete Szenario übergeben.
1. Die Ausgabe des Szenarios „Untergeordnetes Element aufrufen“ ist die Ausgabe des untergeordneten Szenarios. Diese Ausgabe kann später im übergeordneten Szenario verarbeitet werden.

## Anwendungsszenarien

Betrachten Sie die folgenden Beispielanwendungsfälle für Verkettungsszenarien:

* **Wiederverwendbare Logik**: Sie können ein Szenario für wiederholte Aktionen verketten, die in mehreren Szenarien verwendet werden. Wenn Sie beispielsweise über mehrere Szenarien zur Archivierung von Inhalten verfügen, können Sie ein einziges untergeordnetes Szenario mit dem Namen „Inhalt archivieren“ erstellen, das Sie dann als untergeordnetes Szenario für alle Workflows verwenden können, die Inhalte archivieren.

* **Fehlerbehandlung**: Unternehmen nutzen häufig dieselben Aktionen zur Fehlerbehandlung in mehreren Szenarien, z. B. eine Route zur Fehlerbehandlung, die ein Fehlerprotokoll an einen Datenspeicher sendet und eine Slack-Benachrichtigung erstellt. Sie können mit diesen Aktionen ein untergeordnetes Szenario erstellen und dieses Szenario in Fehlerbehandlungsrouten in mehreren Szenarien verketten.

* **Verlängerung der**: Sie können Verkettungen für große Batch-Vorgänge mit lang laufenden Aktionen verwenden, z. B. wenn Sie Dateien exportieren und importieren möchten. Dieser Vorgang dauert einige Zeit, wenn viele Dateien vorhanden sind. Da untergeordnete Szenarien nicht mit der maximalen Wartezeit des übergeordneten Szenarios verrechnet werden, können Sie die Ausführungszeit überschreiten, indem Sie mehrere untergeordnete Szenarien zum Exportieren oder Importieren der Dateien verwenden.

* **Ersetzen von Iteratoren** Durch Ersetzen von Iteratoren durch untergeordnete Szenarien kann die Speichernutzung reduziert werden, z. B. bei komplexen Vorgängen in einer Iteration, die zu einem Fehler wegen zu wenig Arbeitsspeicher führt. Sie können ein separates Szenario für den komplexen Vorgang erstellen und den Iterator durch das Modul Untergeordnetes Szenario aufrufen ersetzen

* **Datensatz suchen und erstellen**: Sie können beispielsweise ein Szenario erstellen, in dem nach einem Benutzer gesucht wird. Wenn sie vorhanden sind, werden sie als genehmigende Person hinzugefügt, deren Zugriff überprüft und genehmigt werden muss. Wenn sie nicht vorhanden sind, erstellt das Szenario eine Anfrage, in die der Administrator einen neuen Benutzer aufnehmen kann.

## Anzeigen des Ausführungsverlaufs für verkettete Szenarien

Sie können den Ausführungsverlauf für verkettete Szenarien anzeigen, indem Sie den Verlauf jedes Szenarios in der Kette anzeigen. Beispielsweise würde der Ausführungsverlauf des übergeordneten Szenarios Informationen über Module und Daten enthalten, die direkt im übergeordneten Szenario verarbeitet werden. Um den Ausführungsverlauf für Module und Daten, die in einem untergeordneten Szenario verarbeitet werden, anzuzeigen, öffnen Sie das untergeordnete Szenario und zeigen Sie dort den Ausführungsverlauf an.

Es wird empfohlen, die Schaltfläche **Zum untergeordneten Szenario wechseln** im Modul Untergeordnetes Szenario aufrufen zu verwenden, um schnell zum untergeordneten Szenario zu wechseln, in dem Sie den Ausführungsverlauf anzeigen können. Das untergeordnete Szenario wird in einem anderen Browser-Fenster geöffnet, sodass übergeordnete und untergeordnete Szenarien gleichzeitig angezeigt werden.

![Wechseln Sie zur Schaltfläche für das untergeordnete Szenario](assets/go-to-the-child-button.png)

## Fehler und unvollständige Ausführungen

### Umgang mit Fehlern

Wenn das untergeordnete Szenario einen Fehler aufweist, kann dies dazu führen, dass Daten an das übergeordnete Element zurückgegeben werden.

Es wird empfohlen, die Fehlerbehandlung im untergeordneten Szenario zu konfigurieren, um sicherzustellen, dass das übergeordnete Szenario nicht auf die Antwort des untergeordneten Szenarios wartet, wenn im untergeordneten Szenario ein Fehler auftritt.

## Best Practices

Beachten Sie beim Verketten eines Szenarios die folgenden Best Practices.

### Vermeiden von Rekursionen bei der Verkettung von Szenarien

Rekursionen treten auf, wenn in einem Szenario eine neue Ausführung von sich selbst in Trigger gesetzt wird, wodurch eine neue Ausführung in einer Endlosschleife Trigger wird usw.

Rekursionen können Leistungsprobleme sowohl für die Organisation, der das rekursive Szenario gehört, als auch für andere Organisationen verursachen.

Gehen Sie beim Verketten von Szenarien wie folgt vor, um Rekursionen zu vermeiden:

* Stellen Sie sicher **dass das übergeordnete Szenario nicht durch untergeordnete Szenarien Trigger werden kann**. Wenn beispielsweise ein übergeordnetes Szenario ausgelöst wird, wenn eine Anfrage erstellt wird, stellen Sie sicher, dass die untergeordneten Szenarien keine Anfragen erstellen.
* Stellen Sie sicher **dass sich untergeordnete Szenarien nicht gegenseitig**. Wenn beispielsweise untergeordnetes Szenario A untergeordnetes Szenario B aufruft, stellen Sie sicher, dass untergeordnetes Szenario B nicht untergeordnetes Szenario A aufruft.
* Stellen Sie sicher **dass ein Szenario sich nicht selbst aufrufen**. Beispielsweise wird ein Szenario ausgelöst, wenn eine Aufgabe erstellt wird, und dieses Szenario erstellt zwei Aufgaben. Bei den neu erstellten Aufgaben wird das Szenario erneut Trigger, sodass vier neue Aufgaben erstellt werden. Bei jeder Erstellung einer Aufgabe wird das Szenario ausgelöst und bei jeder Ausführung des Szenarios verdoppelt sich die Anzahl der Aufgaben. Die Anzahl der Aufgaben steigt exponentiell.

>[!IMPORTANT]
>
>* **Wenn ein Szenario eine Rekursion verursacht, wird es vom Fusion Engineering-Team deaktiviert, um weitere Leistungsprobleme zu vermeiden.**
>* Da die Rekursion ein Ergebnis des Szenario-Designs ist, müssen Sie Ihre Szenarien so entwerfen, dass das Szenario keine das Szenario Trigger Aktionen enthält.

### Verwenden der Fehlerbehandlung, um eine Antwort sicherzustellen

Da das übergeordnete Szenario auf eine Antwort des untergeordneten Szenarios wartet, bevor es fortgesetzt werden kann, müssen Sie sicherstellen, dass das untergeordnete Szenario so aufgebaut ist, dass es eine Antwort bereitstellt, selbst wenn ein Fehler auftritt.
