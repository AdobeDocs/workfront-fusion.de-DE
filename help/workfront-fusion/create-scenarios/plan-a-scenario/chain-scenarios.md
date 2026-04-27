---
title: Mehrere Szenarien verketten
description: Sie können Szenarien miteinander verketten, sodass ein Szenario ein Trigger zum anderen durchführt, und die vom zweiten Szenario ausgegebenen Daten an das erste zurückgeben.
author: Becky
feature: Workfront Fusion
exl-id: def8d4c1-fc20-4b93-b1fd-be2f60300464
source-git-commit: 0390bb875eb10278967d7d1c9cd61e5243e5f37e
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 12%

---

# Verketten mehrerer Szenarios

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

* **Verlängerung der**: Sie können Verkettungen für große Batch-Vorgänge mit lang laufenden Aktionen verwenden, z. B. beim Exportieren und Importieren von Dateien. Dieser Vorgang dauert einige Zeit, wenn viele Dateien vorhanden sind. Da untergeordnete Szenarien nicht mit der maximalen Wartezeit des übergeordneten Szenarios verrechnet werden, können Sie die Ausführungszeit überschreiten, indem Sie mehrere untergeordnete Szenarien zum Exportieren oder Importieren der Dateien verwenden.

* **Ersetzen von Iteratoren** Durch Ersetzen von Iteratoren durch untergeordnete Szenarien kann die Speichernutzung reduziert werden, z. B. bei komplexen Vorgängen in einer Iteration, die zu einem Fehler wegen zu wenig Arbeitsspeicher führt. Sie können ein separates Szenario für den komplexen Vorgang erstellen und den Iterator durch das Modul Untergeordnetes Szenario aufrufen ersetzen

* **Datensatz suchen und erstellen**: Sie können beispielsweise ein Szenario erstellen, in dem nach einem Benutzer gesucht wird. Wenn sie vorhanden sind, werden sie als genehmigende Person hinzugefügt, deren Zugriff überprüft und genehmigt werden muss. Wenn sie nicht vorhanden sind, erstellt das Szenario eine Anfrage, in die der Administrator einen neuen Benutzer aufnehmen kann.

## Viewing execution history for chained scenarios

You can view execution history for chained scenarios by viewing the history of each scenario included in the chain. For example, the parent scenario&#39;s execution history would include information about modules and data processed directly in the parent scenario. To view execution history for modules and data processed in a child scenario, open the child scenario and view the execution history there.

We recommend using the **Go to the child scenario** button in the Call a child scenario module to quickly go to the child scenario, where you can view its execution history. The child scenario opens in another browser window, allowing you to see parent and child scenarios at the same time.

![Go to the child scenario button](assets/go-to-the-child-button.png)

## Errors and incomplete executions

### Umgang mit Fehlern

If the child scenario errors out, that may affect getting data back to your parent.

We recommend configuring error handling in the child scenario to ensure that if something goes wrong in the child scenario, the parent scenario is not stuck waiting for the response from the child scenario.

## Best Practices

Consider the following best practices when chaining a scenario.

### Avoid recursion when chaining scenarios

Rekursionen treten auf, wenn ein Szenario sich selbst neu auslöst, wodurch eine neue Ausführung in einer Endlosschleife ausgelöst wird.

Rekursionen können Leistungsprobleme sowohl für die Organisation, der das rekursive Szenario gehört, als auch für andere Organisationen verursachen.

When chaining scenarios, follow these practices to avoid recursion:

* Ensure that **child scenarios cannot trigger the parent scenario**. For example, if a parent scenario is triggered when a request is created, ensure that the child scenarios do not create requests.
* Ensure that **child scenarios do not call each other**. For example, If child scenario A calls child scenario B, ensure that child scenario B does not call child scenario A.
* Ensure that **a scenario cannot call itself**. Beispielsweise wird ein Szenario ausgelöst, wenn eine Aufgabe erstellt wird und dieses Szenario zwei Aufgaben erstellt. Bei den neu erstellten Aufgaben wird das Szenario erneut ausgelöst, sodass vier neue Aufgaben erstellt werden. Bei jeder Erstellung einer Aufgabe wird das Szenario ausgelöst und bei jeder Ausführung des Szenarios verdoppelt sich die Anzahl der Aufgaben. Die Anzahl der Aufgaben steigt exponentiell.

>[!IMPORTANT]
>
>* **Wenn ein Szenario eine Rekursion verursacht, wird es vom Fusion-Engineering-Team deaktiviert, um weitere Leistungsprobleme zu verhindern.**
>* Da die Rekursion ein Ergebnis des Szenario-Designs ist, müssen Sie Ihre Szenarios so entwerfen, dass das Szenario keine Aktionen umfasst, die das Szenario auslösen.
>* You can view a diagram of the relationships between parent and child scenarios.
>   For instructions, see [View chained scenario relationships](/help/workfront-fusion/manage-scenarios/view-chained-scenario-relationships.md).

### Use error handling to ensure a response

Because the parent scenario is waiting for a response from the child scenario before it can continue, you must ensure that the child scenario is built so that it will provide a response even if it encounters an error.
