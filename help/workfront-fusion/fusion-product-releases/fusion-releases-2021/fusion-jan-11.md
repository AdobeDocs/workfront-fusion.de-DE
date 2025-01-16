---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Workfront Fusion-Veröffentlichungsaktivität: Woche vom 11. Januar 2021'
description: Auf dieser Seite werden alle Verbesserungen beschrieben, die in Adobe Workfront Fusion in der Woche vom 11. Januar 2021 vorgenommen wurden.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: d5732b6c-b039-4bf7-a7e6-e59b6e8f1a63
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Workfront Fusion-Veröffentlichungsaktivität: Woche vom 11. Januar 2021

Auf dieser Seite werden alle Verbesserungen beschrieben, die in Adobe Workfront Fusion in der Woche vom 11. Januar 2021 vorgenommen wurden.

Eine Liste aller aktuellen Änderungen finden Sie unter [Adobe Workfront Fusion-Versionsaktivität](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Eine Liste der letzten Fehlerbehebungen in Workfront Fusion finden Sie auf der Seite [Workfront-Wartungs-Updates](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) und suchen Sie nach Updates mit der Bezeichnung Workfront Fusion-Wartungs-Update.

## Erweitern von Connectoren und Modulen jetzt verfügbar

Sie können jetzt Workfront Fusion verwenden, um eine Verbindung zu Ihrem Widen-Konto herzustellen. Mit den Widen-Modulen können Sie:

* Hinzufügen von Assets zu oder Entfernen von Assets aus einer Sammlung
* Dateien herunterladen oder hochladen
* Lesen oder Aktualisieren von Asset-Metadaten
* Suche nach Assets basierend auf von Ihnen angegebenen Kriterien
* Abrufen einer Liste von Assets in einer Sammlung
* Durchführen eines benutzerdefinierten API-Aufrufs.

## Datadog-Connector und -Module jetzt verfügbar

Sie können jetzt Workfront Fusion verwenden, um eine Verbindung zu Ihrem Datadog-Konto herzustellen.

Mit den Datadog-Modulen können Sie:

* Zeitreihen-Punkte posten
* Durchführen eines benutzerdefinierten API-Aufrufs

## Event-Connector und -Module jetzt verfügbar

Sie können jetzt Workfront Fusion 2.0 verwenden, um eine Verbindung zu Ihrem Cvent-Konto herzustellen.

Mit den Cvent-Modulen können Sie:

* Besprechungsanfrage erstellen
* Lesen von Datensätzen wie Kontakten, Ereignissen oder Einladungen
* Auflisten von Datensätzen basierend auf von Ihnen angegebenen Kriterien
* Registrieren oder Hinzufügen von Einladungen zu bestimmten Ereignissen
* Kontakte aktualisieren oder löschen
* Erstellen eines benutzerdefinierten API-Aufrufs


## Microsoft Dynamics 365-Connector und -Module jetzt verfügbar

Sie können jetzt Workfront Fusion 2.0 verwenden, um eine Verbindung zu Ihrem Microsoft Dynamics 365-Konto herzustellen. Mit den Microsoft Dynamics 365-Modulen können Sie:

* Trigger : Szenario, in dem Datensätze in Microsoft Dynamics 365 hinzugefügt oder aktualisiert werden
* Erstellen, Lesen, Aktualisieren oder Löschen eines Microsoft Dynamics 365-Datensatzes
* Durchführen eines benutzerdefinierten API-Aufrufs

## DocuSign-Connector und -Module jetzt verfügbar

Sie können jetzt Workfront Fusion 2.0 verwenden, um eine Verbindung zu Ihrem DocuSign-Konto herzustellen. Mit den DocuSign-Modulen können Sie:

* Trigger : Ein Szenario, in dem ein Envelope seinen Status ändert
* Erstellen eines Briefumschlags
* Lesen, Senden oder Hinzufügen eines Empfängers zu einem vorhandenen Umschlag
* Hinzufügen oder Ändern benutzerdefinierter Felder in Dokumenten
* Dokument als Feld herunterladen
* Datei in einen Briefumschlag hochladen
* Durchführen eines benutzerdefinierten API-Aufrufs

## Durchsuchen des Ausführungsverlaufs des Szenarios

Wir haben es Ihnen erleichtert, bestimmte Informationen aus früheren Szenario-Ausführungen zu finden. Die neue Volltextsuche von Fusion ermöglicht es, den Ausführungsverlauf nach allen in einem Bundle enthaltenen Daten zu durchsuchen. Um beispielsweise zu ermitteln, durch welche Ausführung eine bestimmte Aufgabe erstellt wurde, können Sie die Volltextsuche verwenden, um nach dieser Aufgaben-ID zu suchen.

Zuvor war es für das Suchen nach bestimmten Ausführungsinformationen erforderlich, jede Ausführung einzeln anzuzeigen.

## Aktualisierungen des Fusion 2.0-Datenspeichers

Um Ihnen die Anpassung Ihrer Datenspeicher zu erleichtern, haben wir einige neue Funktionen hinzugefügt. Wenn Sie jetzt einen Datenspeicher anzeigen, können Sie:

* Spalten per Drag-and-Drop neu anordnen
* Einzelne Zelle bearbeiten
* Mehrere Zeilen hinzufügen


## Erstellen einer API-Schlüsselautorisierungsanfrage über den HTTP-Connector

Um den Zugriff auf APIs flexibler zu gestalten, haben wir dem HTTP-Connector ein neues Modul hinzugefügt. Jetzt können Sie den HTTP-Connector verwenden, um eine Anfrage zu stellen, wenn der Webservice, auf den Sie zugreifen, die Verwendung eines API-Schlüssels erfordert.

## Neue Funktionen im Zuordnungsbereich verfügbar

Um Ihnen bei der Anpassung und Vereinfachung von Formeln in Ihren Modulen zu helfen, haben wir einige neue Funktionen hinzugefügt.

* Der/Die/Das

  ```
  omit
  ```

  Funktion ist eine allgemeine Funktion, die die angegebenen Schlüssel des -Objekts auslässt und den Rest zurückgibt.
* Der/Die/Das

  ```
  pick
  ```

  Funktion ist eine allgemeine Funktion, die nur die angegebenen Schlüssel aus dem Objekt auswählt.
* Der/Die/Das

  ```
  escapeMarkdown
  ```

  ist eine Zeichenfolgenfunktion, die alle Markdown-Tags in einem Text maskiert.
