---
title: Leistungsleitlinien für Fusion
description: Die Arbeitsautomatisierung erfordert eine schnelle Verarbeitung, weshalb Adobe Workfront Fusion auf hohe Leistung ausgelegt ist. Da lang laufende Szenarios das Arbeitstempo verlangsamen können, wurde Workfront Fusion unter Berücksichtigung von Leistungsleitlinien entwickelt, durch die die Ausführungszeit, die Datengröße und andere Szenarioparameter begrenzt werden. Die Designerinnen und Designer sollten sich dieser Leitlinien bewusst sein und sie in ihre Design-Praktiken integrieren.
author: Becky
feature: Workfront Fusion
exl-id: d142a521-edbc-4d7b-b5cd-872a9d3d2e1c
source-git-commit: 3a05e5df36bf9b1aacd0611fdad0240c8c52368d
workflow-type: ht
source-wordcount: '1092'
ht-degree: 100%

---

# Leistungsleitlinien für Fusion

Die Arbeitsautomatisierung erfordert eine schnelle Verarbeitung, weshalb Adobe Workfront Fusion auf hohe Leistung ausgelegt ist. Da lang laufende Szenarios das Arbeitstempo verlangsamen können, wurde Workfront Fusion unter Berücksichtigung von Leistungsleitlinien entwickelt, durch die die Ausführungszeit, die Datengröße und andere Szenarioparameter begrenzt werden. Die Designerinnen und Designer sollten sich dieser Leitlinien bewusst sein und sie in ihre Design-Praktiken integrieren.

## Browser

* Workfront Fusion unterstützt nur Chrome-basierte Browser.

## Szenarios

* Der standardmäßige Timeout für Szenario-Ausführungen beträgt **40 Minuten**. Wird bei der Ausführung dieser Timeout erreicht, unterbricht Workfront Fusion je nach Szenario die Szenario-Ausführung nach dem nächsten Zyklus bzw. Vorgang. Dadurch wird das Szenario kurz nach Erreichen des 40-Minuten-Limits beendet.

  Verkettungsszenarios zählen nicht für den Timeout bei Szenario-Ausführungen. Ein übergeordnetes Szenario baut keine Zeit auf, während auf die Ausführung eines untergeordneten Szenarios gewartet wird.
* Die maximale Größe einer Szenario-Blueprint beträgt **5 MB**. Wir empfehlen jedoch, die Szenariogröße bei unter **3 MB** zu belassen.

  Anwendungsmodule, die Daten mit einer großen Anzahl von Feldern erstellen oder aktualisieren, können zu sehr großen Blueprints führen.

   * Achten Sie bei Verwendung der Workfront-Anwendung darauf, nur die Felder auszuwählen, die für Ihre Anwendungsfälle zum Erstellen oder Aktualisieren erforderlich sind.
   * Nutzen Sie bei Verwendung anderer Anwendungen benutzerdefinierte API-Module, um mit jedem Eintragstyp zu interagieren, der über eine große Anzahl von Feldern verfügt.

* Es gibt zwar keine Begrenzung für die Anzahl der Module in einem Szenario, aber Szenarios mit mehr als 150 Modulen beeinträchtigen die Leistung Ihres Workfront Fusion-Systems. Aus diesem Grund raten wir davon ab, Szenarios mit mehr als 150 Modulen zu erstellen.

## Vorgänge

* Der standardmäßige Timeout für Vorgänge beträgt in der Regel **40 Sekunden**.

<!--
* The operation timeout for calls to Adobe Workfront is **120 seconds**.
-->

## Dateien

* Die Gesamtverarbeitungskapazität von Fusion für Dateien beträgt **1 GB**. Das Limit basiert auf dem Gesamtspeicherbedarf. Jeder Vorgang trägt zu diesem Bedarf bei. Wenn eine einzelne Datei mit 400 MB heruntergeladen und hochgeladen wird, würde der Speicherbedarf für die Datei insgesamt bei 800 MB liegen.
* Unternehmen mit Workfront Ultimate-Plan steht eine erhöhte Dateiverarbeitungskapazität von mehr als 1 GB zur Verfügung. Es gibt jedoch noch weitere Faktoren, die sich auf die Datenübertragung auswirken. Der Service, mit dem Fusion eine Verbindung herstellt, kann die Dateigröße begrenzen, was sich auf alle Dateien auswirken würde, die von diesem Service verarbeitet werden. Darüber hinaus können große Dateien die Ausführungszeit des Szenarios beeinträchtigen. Fusion verarbeitet Dateien, bis das Ausführungs-Limit von 40 Minuten erreicht ist, woraufhin die Ausführung fehlschlägt.
* Wenn eine Datei mit einem Modul heruntergeladen wird, das große Dateien unterstützt, und dann an ein Modul übergeben wird, das große Dateien nicht unterstützt, kann dieses Modul die Datei nicht erfolgreich verarbeiten. Große Dateien müssen während des gesamten Workflows ausschließlich mit unterstützten Modulen verarbeitet werden.
* Module, die keine großen Dateien unterstützen, können Dateien mit einer Größe von bis zu **200 MB** verarbeiten.

Weitere Informationen finden Sie unter [Arbeiten mit großen Dateien](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

## Server-Speichernutzung

* Die Server-Speichernutzung für eine einzelne Ausführung ist auf **1 GB** beschränkt.

  Zahlreiche Faktoren, z. B. große Dateien oder komplexe Module, können die Server-Speichernutzung auf eine Weise beeinflussen, die schwer vorherzusagen oder zu steuern ist. Aus diesem Grund kann Ihre Szenario-Ausführung das 1-GB-Speicher-Limit überschreiten, auch wenn das Szenario allen anderen Leistungsleitlinien folgt. Wenn Sie das Speicher-Limit überschreiten, schlägt die Ausführung fehl.

## Webhooks

* Die standardmäßige Maximalgröße einer Payload beträgt **5 MB**.
* Webhooks sind auf **100 Anfragen pro Sekunde** beschränkt. Wenn dieses Limit erreicht ist, sendet Workfront Fusion den Status 429 ([!UICONTROL Zu viele Anfragen]).
* Workfront Fusion speichert Webhook-Payloads 30 Tage lang. Der Zugriff auf eine Webhook-Payload mehr als 30 Tage nach dem Empfang führt zum Fehler [!UICONTROL Fehler beim Lesen der Datei aus dem Speicher].
* Webhooks werden automatisch deaktiviert, wenn einer der folgenden Punkte zutrifft:

   * Der Webhook wurde seit mehr als 5 Tagen mit keinem Szenario verbunden.
   * Der Webhook wird nur in inaktiven Szenarios verwendet, die seit mehr als 30 Tagen inaktiv sind.

* Deaktivierte Webhooks werden automatisch gelöscht und ihre Registrierung wird aufgehoben, wenn sie mit keinem Szenario verbunden sind und seit mehr als 30 Tagen einen deaktivierten Status aufweisen.
* Der Timeout für eine Webhook-Antwort erfolgt nach 5 Minuten.

## Ausführungsverlauf

* Ausführungsverlaufsprotokolle sind auf eine Größe von **100 MB** beschränkt. Wenn der Ausführungsverlauf diese Größe überschreitet, werden nur die ersten 100 MB angezeigt.
* Wenn ein Szenario mehrere gleichzeitige Ausführungen aufweist, werden auf der Detailseite des Szenarios im Bereich „Ausführungen“ nur 5 Ausführungen angezeigt. Dies gilt auch bei mehr als 5 aktiven Ausführungen.

## Unvollständige Ausführungen

* Unvollständige Ausführungen sind auf eine Gesamtgröße von **10 MB** pro Szenario beschränkt. Wenn das Limit von 10 MB erreicht wird, werden für dieses Szenario keine weiteren unvollständigen Ausführungen gespeichert.
* Unvollständige Ausführungen sind auf eine Gesamtgröße von **500 MB** pro Team beschränkt. Wenn das Limit von 500 MB erreicht wird, werden für dieses Team keine unvollständigen Ausführungen mehr gespeichert.
* Workfront Fusion lässt bis zu 5 fehlgeschlagene Vorgänge pro Minute zu.

## Weitere Versuche

* Wenn bei Verwendung des Unterbrechungsmoduls und Angabe der Anweisung „Erneut versuchen“ ein Szenario innerhalb eines Zeitraums von 2 Minuten 10-mal nacheinander fehlschlägt, wird das Szenario automatisch deaktiviert.

## Rekursion

Rekursionen treten auf, wenn ein Szenario sich selbst neu auslöst, wodurch eine neue Ausführung in einer Endlosschleife ausgelöst wird.

Beispielsweise wird ein Szenario ausgelöst, wenn eine Aufgabe erstellt wird und dieses Szenario zwei Aufgaben erstellt. Bei den neu erstellten Aufgaben wird das Szenario erneut ausgelöst, sodass vier neue Aufgaben erstellt werden. Bei jeder Erstellung einer Aufgabe wird das Szenario ausgelöst und bei jeder Ausführung des Szenarios verdoppelt sich die Anzahl der Aufgaben. Die Anzahl der Aufgaben steigt exponentiell.

Rekursionen können Leistungsprobleme sowohl für die Organisation, der das rekursive Szenario gehört, als auch für andere Organisationen verursachen.

Beachten Sie Folgendes im Hinblick auf Rekursionen:

* **Wenn ein Szenario eine Rekursion verursacht, wird es vom Fusion-Engineering-Team deaktiviert, um weitere Leistungsprobleme zu verhindern.**
* Da die Rekursion ein Ergebnis des Szenario-Designs ist, müssen Sie Ihre Szenarios so entwerfen, dass das Szenario keine Aktionen umfasst, die das Szenario auslösen.

## TLS

* Fusion unterstützt derzeit standardmäßig TLS 1.2.
* Fusion kann TLS 1.3 für ausgehende HTTPS-Anfragen verwenden, wenn TLS 1.3 für den Ziel-Service aktiviert ist.
* Fusion unterstützt sowohl TLS 1.2 als auch TLS 1.3 für eingehende HTTPS-Anfragen an Webhooks.
* Organisationen können anfordern, dass TLS 1.3 für ihre Fusion-Instanz aktiviert wird.

>[!NOTE]
>
> Wenn Sie eine Verbindung zu Workfront herstellen, beachten Sie, dass diese TLS-Funktion in Workfront für Aufrufe an Domains mit dem Format `https://<domain>.my.workfront.com` aktiviert ist.
