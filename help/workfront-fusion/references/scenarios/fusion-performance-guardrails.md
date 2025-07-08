---
title: Leitplanken für die Fusionsleistung
description: Die Arbeitsautomatisierung erfordert eine schnelle Verarbeitung und  [!DNL Adobe Workfront Fusion]  daher für hohe Leistung. Da langwierige Szenarien die Geschwindigkeit Ihrer Arbeit verlangsamen können, haben wir  [!DNL Workfront Fusion]  leistungserhaltende Leitplanken entwickelt, die die Ausführungszeit, die Datengröße und andere Szenario-Parameter begrenzen. [!DNL Workfront Fusion] Designer sollten sich dieser Leitplanken bewusst sein und sie in ihre Designpraktiken integrieren.
author: Becky
feature: Workfront Fusion
exl-id: d142a521-edbc-4d7b-b5cd-872a9d3d2e1c
source-git-commit: 74324fd5f2f68dfbbd0dfe1286c202c246f29d43
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 0%

---

# Leitplanken für die Fusionsleistung

Die Arbeitsautomatisierung erfordert eine schnelle Verarbeitung, sodass [!DNL Adobe Workfront Fusion] für hohe Leistung entwickelt wurde. Da langwierige Szenarien die Geschwindigkeit Ihrer Arbeit verlangsamen können, haben wir [!DNL Workfront Fusion] mit leistungserhaltenden Leitplanken entwickelt, die die Ausführungszeit, die Datengröße und andere Szenario-Parameter beschränken. [!DNL Workfront Fusion] Designer sollten sich dieser Leitplanken bewusst sein und sie in ihre Entwurfsverfahren integrieren.

## Browser

* Workfront Fusion unterstützt nur Chrome-basierte Browser.

## Szenarios

* Das standardmäßige Ausführungstimeout für das Szenario beträgt **40 Minuten**. Wenn die Ausführung diese Zeitüberschreitung erreicht, unterbricht [!DNL Workfront Fusion] je nach Szenario die Ausführung des Szenarios nach dem nächsten Zyklus oder Vorgang. Dadurch wird das Szenario kurz nach Erreichen der 40-Minuten-Grenze beendet

  Verkettungsszenarien zählen nicht für die Zeitüberschreitung der Szenarioausführung. Ein übergeordnetes Szenario fällt keine Zeit an, während auf die Ausführung eines untergeordneten Szenarios gewartet wird.
* Die maximale Größe einer Szenario-Blueprint beträgt **5 MB**, wir empfehlen jedoch, die Szenario-Größe unter **3 MB** zu belassen.

  Mobile-App-Module, die Daten mit einer großen Anzahl von Feldern erstellen oder aktualisieren, können zu sehr großen Blueprints führen.

   * Achten Sie bei Verwendung der [!DNL Workfront]-App darauf, nur die Felder auszuwählen, die für Ihre Anwendungsfälle zum Erstellen oder Aktualisieren erforderlich sind.
   * Verwenden Sie bei der Verwendung anderer Programme benutzerdefinierte API-Module, um mit jedem Datensatztyp zu interagieren, der über eine große Anzahl von Feldern verfügt.

* Es gibt zwar keine Begrenzung für die Anzahl der Module in einem Szenario, aber Szenarien mit mehr als 150 Modulen beeinträchtigen die Leistung Ihres [!DNL Workfront Fusion]. Aus diesem Grund empfehlen wir nicht, Szenarien mit mehr als 150 Modulen zu erstellen.

## Vorgänge

* Das standardmäßige Zeitlimit für Vorgänge beträgt in der Regel **40 Sekunden**.

<!--
* The operation timeout for calls to Adobe Workfront is **120 seconds**.
-->

## Dateien

* Die Gesamtverarbeitungskapazität von Fusion beträgt **1 GB**. Das Limit basiert auf den Gesamtspeicherkosten. Jeder Arbeitsgang trägt zu diesen Kosten bei. Wenn eine einzelne Datei mit 400 MB heruntergeladen und hochgeladen wird, würden die Gesamtkosten für die Dateikapazität 800 MB betragen.
* Unternehmen, die den Workfront Ultimate-Plan verwenden, haben Zugriff auf eine Dateiverarbeitung, die über 1 GB hinausgeht. Die Fusion-Plattform kann einzelne Dateien mit bis zu 15 GB für eine einzelne Aktion (z. B. das Hochladen einer Datei) unterstützen, es gibt jedoch andere Faktoren, die die Datenübertragung beeinflussen. Die Dateigrößenbeschränkung einer einzelnen Aktion hängt davon ab, mit welchem Web-Service sich Fusion verbindet. Die Datenübertragung ist die Gesamtverarbeitung für eine einzelne Ausführung. Dies bedeutet, dass mehrere Aktionen in einer einzigen Ausführung zur gesamten Datenübertragung beitragen. Fusion verarbeitet Dateien, bis die Ausführungsgrenze von 40 Minuten erreicht ist.

Weitere Informationen finden Sie unter [Arbeiten mit großen Dateien](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

## Speicherauslastung des Servers

* Die Speichernutzung des Servers für eine einzelne Ausführung ist auf **1 GB** beschränkt.

  Viele Faktoren, wie z. B. große Dateien oder komplexe Module, können die Speichernutzung des Servers auf eine Weise beeinflussen, die schwer vorherzusagen oder zu steuern ist. Aus diesem Grund kann Ihre Szenarioausführung das 1 GB-Speicherlimit überschreiten, auch wenn das Szenario allen anderen Leistungs-Schutzmechanismen folgt. Wenn Sie die Speicherbegrenzung überschreiten, schlägt die Ausführung fehl.

## Webhooks

* Die standardmäßige Maximalgröße einer Payload beträgt **5 MB**.
* Webhooks sind auf **100 Anfragen pro Sekunde beschränkt**. Wenn dieses Limit erreicht ist, sendet Workfront Fusion den Status 429 ([!UICONTROL Zu viele Anfragen]).
* [!DNL Workfront Fusion] speichert Webhook-Payloads 30 Tage lang. Der Zugriff auf eine Webhook-Payload mehr als 30 Tage nach dem Empfang führt zu dem Fehler &quot;[!UICONTROL Fehler beim Lesen der Datei aus dem Speicher.]&quot;
* Webhooks werden automatisch deaktiviert, wenn einer der folgenden Punkte zutrifft:

   * Der Webhook wurde seit mehr als 5 Tagen mit keinem Szenario verbunden
   * Der Webhook wird nur in inaktiven Szenarien verwendet, die seit mehr als 30 Tagen inaktiv sind.

* Deaktivierte Webhooks werden automatisch gelöscht und von der Registrierung entfernt, wenn sie mit keinem Szenario verbunden sind und sich seit mehr als 30 Tagen im Status Deaktiviert befinden.

## Ausführungsverlauf

* Die Ausführungsverlaufsprotokolle sind auf eine Größe von **100 MB)**. Wenn der Ausführungsverlauf diese Größe überschreitet, werden nur die ersten 100 MB angezeigt.
* Wenn ein Szenario mehrere gleichzeitige Ausführungen hat. Nur 5 Ausführungen werden im Bereich Ausführungen auf der Seite mit den Szenario-Details angezeigt. Dies gilt auch, wenn mehr als 5 Ausführungen laufen.

## Unvollständige Ausführungen

* Unvollständige Ausführungen sind auf eine Gesamtgröße von **500 MB** beschränkt. Wenn das Limit von 500 MB erreicht wird, werden keine unvollständigen Ausführungen mehr gespeichert.

## Weitere Zustellversuche

* Wenn bei Verwendung des Break-Moduls und Angabe der Wiederholungsanweisung ein Szenario innerhalb eines Zeitrahmens von 2 Minuten 10-mal nacheinander fehlschlägt, wird das Szenario automatisch deaktiviert.

## Rekursion

Rekursionen treten auf, wenn in einem Szenario eine neue Ausführung von sich selbst in Trigger gesetzt wird, wodurch eine neue Ausführung in einer Endlosschleife Trigger wird usw.

Beispielsweise wird ein Szenario ausgelöst, wenn eine Aufgabe erstellt wird, und dieses Szenario erstellt zwei Aufgaben. Bei den neu erstellten Aufgaben wird das Szenario erneut Trigger, sodass vier neue Aufgaben erstellt werden. Bei jeder Erstellung einer Aufgabe wird das Szenario ausgelöst und bei jeder Ausführung des Szenarios verdoppelt sich die Anzahl der Aufgaben. Die Anzahl der Aufgaben steigt exponentiell.

Rekursionen können Leistungsprobleme sowohl für die Organisation, der das rekursive Szenario gehört, als auch für andere Organisationen verursachen.

Beachten Sie Folgendes bezüglich der Rekursion:

* **Wenn ein Szenario eine Rekursion verursacht, wird es vom Fusion Engineering-Team deaktiviert, um weitere Leistungsprobleme zu vermeiden.**
* Da die Rekursion ein Ergebnis des Szenario-Designs ist, müssen Sie Ihre Szenarien so entwerfen, dass das Szenario keine das Szenario Trigger Aktionen enthält.

## TLS

* Fusion unterstützt derzeit standardmäßig TLS Version 1.2.
* Fusion kann TLS 1.3 für ausgehende HTTPS-Anfragen verwenden, wenn TLS 1.3 für den Ziel-Service aktiviert ist.
* Fusion unterstützt sowohl TLS 1.2 als auch TLS 1.3 für eingehende HTTPS-Anfragen an Webhooks.
* Unternehmen können anfordern, dass TLS Version 1.3 für ihre Fusion-Instanz aktiviert wird.

>[!NOTE]
>
> Wenn Sie eine Verbindung zu Workfront herstellen, beachten Sie, dass diese TLS-Funktion in Workfront für Aufrufe an Domains mit dem Format `https://<domain>.my.workfront.com` aktiviert ist.
