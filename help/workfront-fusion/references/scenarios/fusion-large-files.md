---
title: Arbeiten mit großen Dateien
description: Unterstützung für große Dateien ist derzeit für die Workfront- und HTTP-Connectoren verfügbar.
author: Becky
feature: Workfront Fusion
exl-id: 6df81943-e70c-42b3-aa44-d82343598a51
source-git-commit: 4422a0d9236c4fe783b3b8d2757a86c91bcca748
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 0%

---

# Arbeiten mit großen Dateien

>[!IMPORTANT]
>
>Die Funktion für große Dateien steht nur Kunden von Workfront Ultimate zur Verfügung und umfasst einen schrittweisen Rollout. Alle Fusion-Organisationen mit einem Workfront Ultimate-Plan verfügen ab Januar 2025 über umfangreiche Dateifunktionen.

Erweiterte Datenübertragungsfunktionen sind jetzt in Workfront Fusion verfügbar, sodass in Szenarien deutlich größere Dateien verarbeitet werden können.

Um größere Dateien zu verarbeiten, müssen Ihre Szenarien aktualisiert werden.

>[!NOTE]
>
>Diese Funktion steht nur Benutzenden des Ultimate Workfront-Pakets zur Verfügung.

## Connectoren, die große Dateien unterstützen

Für die erste Version unterstützen die folgenden Connectoren große Dateien.

* Workfront > Dokument hochladen
* Adobe Experience Manager Assets > Dokument hochladen
* Workfront Proof > Datei hochladen
* Adobe Authenticator > Erstellen eines benutzerdefinierten API-Aufrufs
* HTTP

In zukünftigen Versionen werden weitere Connectoren unterstützt.

## Aktualisieren von Szenarien zur Verarbeitung großer Dateien

Das Modul Workfront > Dokument hochladen wurde geändert, um größere Dateien zu verarbeiten. Die frühere Version dieses Moduls zeigt jetzt `(Legacy)` an, die an den Modulnamen angehängt ist. In den meisten Fällen funktioniert das alte Modul weiterhin.

Wenn Sie mit größeren Dateien arbeiten möchten, empfehlen wir, das alte Modul durch das neue Modul Dokument hochladen zu ersetzen. Das neue Modul Dokument hochladen verhindert Zeitüberschreitungen und andere Fehler.

![Dokument hochladen](assets/new-upload-document.png)

## FAQs

### Was ist die neue Dateigrößenbeschränkung?

Benutzer können jetzt Dateien verarbeiten, die die vorherige 1 GB-Grenze überschreiten, was die Effizienz und Produktivität verbessert.  Obwohl die Plattform einzelne Dateien mit bis zu 15 GB für eine einzelne Aktion (z. B. das Hochladen einer Datei) unterstützen kann, gibt es andere Faktoren, die die Datenübertragung beeinflussen. Die Dateigrößenbeschränkung einer einzelnen Aktion hängt letztendlich von dem Web-Service ab, mit dem sich Fusion verbindet. Die Datenübertragung ist die Gesamtverarbeitung für eine einzelne Ausführung. Dies bedeutet, dass mehrere Aktionen in einer einzigen Ausführung zur gesamten Datenübertragung beitragen.

Fusion verarbeitet Dateien, bis die Ausführungsgrenze von 40 Minuten erreicht ist. Das Hochladen, Herunterladen oder Verarbeiten großer Dateien in Ihrem Fusion-Szenario kann einige Zeit dauern. Die Größe einzelner Dateien ist zwar nicht beschränkt, die Ausführungszeit eines Szenarios ist jedoch auf 40 Minuten begrenzt. Wenn große Dateien dazu führen, dass die Ausführung länger als 40 Minuten dauert, schlägt das Szenario daher fehl. Die Ausführungszeit des Szenarios kann auch von der Größe des Szenarios, der Komplexität der Module und der Netzwerkgeschwindigkeit beeinflusst werden. Daher empfehlen wir, diese Aspekte Ihrer Szenarien bei der Verwendung großer Dateien zu berücksichtigen.

### Wie funktioniert die neue Dateiübertragung von Fusion?

Wenn Fusion Dateien verarbeitet, werden größere Dateien zum persistenten Speicher hinzugefügt (S3 Bucket oder Azure Blob Storage). Wenn ein Fusion-Modul eine Dateiaktion wie das Hochladen oder Herunterladen ausführt, verwendet Fusion die Datei im persistenten Speicher als Quelle anstelle des aktiven Speichers.

### Kann ich mit größeren Dateien arbeiten, die unvollständige Ausführungen verwenden?

Ja, Fusion unterstützt unvollständige Ausführungen mit größeren Dateien. Beachten Sie, dass unvollständige Ausführungen für eine Organisation begrenzt sind und aktiv verwaltet werden sollten.

### Kann ich größere Dateien mit einem beliebigen Connector verwenden?

Jeder Fusion-Connector muss aktualisiert werden, um größere Dateien zu unterstützen. Zu den unterstützten Connectoren gehören Workfront, HTTP und AEM Assets. Fusion-Connectoren sind weiterhin durch die vom Webservice unterstützte Dateigröße begrenzt. Dateigrößenbeschränkungen sind normalerweise in der API-Dokumentation für Webservice-Endpunkte enthalten, die Dateien herunterladen und hochladen.

### Wirkt sich dies auf Vorgänge aus?

Nein, die Anzahl der von einem Modul ausgeführten Vorgänge ist gleich.

### Wann wird die Benutzeroberfläche von Fusion aktualisiert, um Dateiübertragungsdaten anzuzeigen?

Wir arbeiten aktiv an Aktualisierungen der Benutzeroberfläche von Fusion für die Dateiübertragung auf der Detailseite für das Dashboard und die Ausführung des Szenarios mit einer geplanten Veröffentlichung im 1. Quartal 2025.

### Welche Denkansätze gibt es für die neuen Dateiverarbeitungsbeschränkungen, die mir beim Entwerfen von Szenarien helfen?

Es kann kompliziert erscheinen, ein Szenario zu entwerfen, das innerhalb der Ausführungsfrist von 40 Minuten funktioniert. Beim Entwerfen eines Szenarios wird empfohlen, Folgendes zu beachten:

* **Verstehen Sie Ihre Geschäftsanforderungen für die Ausführungszeit**: Die Platform-Grenze von Fusion für die Ausführungszeit beträgt 40 Minuten, aber die meisten Geschäftsprozess-Automatisierungen werden voraussichtlich viel schneller ausgeführt. Beispielsweise wird erwartet, dass benutzerinitiierte Automatisierungen mit ergebnisabhängiger Fortsetzung deutlich unter dem 40-Minuten-Limit abgeschlossen werden.
* **Beim Entwerfen die Ausführungszeit berücksichtigen**: Beim Entwerfen des Szenarios ist es wichtig, die Ausführungszeit des Moduls für einzelne Dateiaktionen wie Uploads und Downloads zu verstehen. Dieses Wissen hilft Ihnen bei der Planung von Szenarien, die mehrere Dateiaktionen umfassen.  Um Genauigkeit in Ihrem Design zu gewährleisten, empfehlen wir, die Ausführungszeit des Moduls auf einen Puffer aufzurunden.
Wenn beispielsweise Fusion ein Dokument in 144 Sekunden (2,4 Minuten) herunterlädt, können Sie davon ausgehen, dass eine einzelne Ausführung ähnliche Aktionen mehrmals ausführen kann. In diesem Beispiel dauert die Ausführung des Moduls 144 Sekunden und Sie sollten für den Download eine Ausführungszeit von 3 Minuten einplanen. Wenn Ihre Anforderungen sowohl einen Upload als auch einen Download umfassen, beträgt die erwartete Ausführungszeit ca. 6 Minuten. Beachten Sie, dass die Ausführungszeiten von Fusion auf 40 Minuten begrenzt sind.

* **Dateiaktionen konsolidieren**: Das häufigste Beispiel für Dateiaktionen in einem Fusion-Szenario ist ein Download und ein Upload. Die meisten Szenarien mit nur diesen beiden Aktionen werden in wenigen Minuten ausgeführt. Nach Möglichkeit sollten Fusion-Designer ihre Szenarien auf einen Download und einen Upload beschränken.

* **Berechnen der Größe mithilfe des**: Workfront und andere Webservices schließen die Dateigröße einer Datei in die Ausgabe des Download-Moduls ein. Sie können diese Daten verwenden, um Dateien herauszufiltern, die für einen Modul-Upload zu groß oder für die Ausführungszeit des Szenarios zu groß sind.

* **Isolieren von Dateiaktionen in ihrem eigenen Szenario bei der Arbeit mit mehreren Dateien**: Fusion-Designer sollten die Isolierung von Dateiaktionen in separaten Szenarien in Betracht ziehen. Beispielsweise muss ein Fusionsszenario, das durch eine neue Workfront-Anfrage mit mehreren angehängten Dateien ausgelöst wird, möglicherweise bis zu 30 Dateien aufnehmen. Da das Hochladen und Herunterladen jeder Datei bis zu 3 Minuten dauern kann, würde die Verarbeitung aller Dateien in einer einzigen Ausführung die 40-Minuten-Ausführungsgrenze von Fusion überschreiten. Die Lösung besteht darin, ein Szenario für Dateiaktionen zu erstellen, das dem Hochladen und Herunterladen einzelner Dateien gewidmet ist. Das durch eine Anfrage ausgelöste Szenario durchläuft die angehängten Dateien und ruft das Dateiaktionsszenario für jede Datei mithilfe des HTTP-Moduls auf. Dieser Ansatz stellt sicher, dass jede Datei innerhalb der Ausführungsfristen verarbeitet wird.

<!--
## Connectors that do not support large files

Some Fusion connectors do not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

The following connectors do **not** support large files. 

* Archive
* Box
* Convert
* CSV
* Datastores
* Flow control
* FTP
* JSON
* JWT
* Markdown
* Math
* Microsoft Word templates
* MIME
* Microsoft SQL
* SFTP
* Adobe Acrobat Sign
* SOAP
* Tools
* XML

If a connector is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.-->






<!--## Connectors that support large files

The following connectors support large files.

Workfront
HTTP
Webhooks
Salesforce
Microsoft Email
Workfront Proof
AEM Assets
Email
Slack
Jira
Microsoft Excel
SharePoint
Frame.io
Adobe PDF Services
Marketo
Azure Devops 
Google Email
Jira Server
Google Sheets
Microsoft OneDrive
ServiceNow 
AWS S3
Bynder
OneDrive Business
Adobe Authenticator
Google Drive
Microsoft Dynamics
Google Docs
NetSuite
Airtable
Azure AD
QuickBase 
Adobe Target
Adobe Campaign Classic
Microsoft Calendar
Workfront Planning
HubSpot CRM  
DropBox
Cloud Convert
Egnyte
Adobe Firefly
OpenAI / Chat GPT
Allocadia
Cvent
GitLab 
Google Team Drive
Google Calendar
Workfront SDL Managed Translation
Widen
Workfront Boards
Google Slides
Qualtrics
Microsoft Power BI
Adobe Photoshop
Anaplan
DocuSign 
MariaDB
Adobe Creative Cloud Libraries
Figma
AEM Forms
Datadog
GitHub 
Google Forms
Adobe I/O Events
Trello
Workday
Adobe Journey Optimizer
Adobe Lightroom


If a file is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

-->
