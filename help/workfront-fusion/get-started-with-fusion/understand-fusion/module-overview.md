---
title: Modulübersicht
description: 'Adobe Workfront Fusion unterscheidet fünf Modultypen: Aktionsmodule, Suchmodule, Trigger-Module, Aggregatoren und Iteratoren. Aggregatoren und Iteratoren sind für fortgeschrittene Szenarien geeignet.'
author: Becky
feature: Workfront Fusion
exl-id: 4c8fe028-8425-426d-a006-f0c66871b3cd
source-git-commit: 190bfe5992fb21b789a7246c4ae732a5dc7672fa
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# Modulübersicht

Adobe Workfront Fusion unterscheidet fünf Modultypen:

* Aktionsmodule
* Suchmodule
* Trigger-Module
* Aggregatoren
* Iteratoren

Aggregatoren und Iteratoren sind für fortgeschrittene Szenarien geeignet.

## Aktionsmodule

Aktionsmodule sind der häufigste Modultyp. Ein typisches Aktionsmodul führt eine Aktion aus und gibt ein einzelnes Bundle zurück, das dann zur Verarbeitung an das nächste Modul weitergegeben wird.

Im Gegensatz zu Trigger-Modulen können Aktionsmodule am Anfang, in der Mitte oder am Ende eines Szenarios platziert werden.

Szenarien können eine unbegrenzte Anzahl von Aktionsmodulen enthalten, obwohl eine große Anzahl von Modulen (150+) die Leistung beeinträchtigen kann.

>[!BEGINSHADEBOX]

**Beispiele:**

* **[!DNL Workfront]>[!UICONTROL Upload a file]** sendet eine Datei an [!DNL Workfront] und gibt deren Kennung zurück.
* **[!UICONTROL Image]>[!UICONTROL Resize]** empfängt ein Bild, ändert die Größe auf die angegebenen Abmessungen und übergibt das skalierte Bild an die nächste Aktion.

>[!ENDSHADEBOX]

Der Aktionstyp weist vier Untertypen auf:

* Erstellen
* Lesen
* Aktualisieren
* Löschen

Der Untertyp Aktualisieren umfasst die folgenden drei Vorgänge:

* **Inhalt eines Felds löschen**. Dieser Vorgang findet statt, wenn der Inhalt des Felds als `erase` Schlüsselwort ausgewertet wird (nicht zu verwechseln mit `empty`).

  ![Keyword löschen](assets/erase-content-of-field.png)

* **Lassen Sie den Inhalt eines Felds**. Dieser Vorgang findet statt, wenn das Feld leer gelassen wird oder der Inhalt des Felds als leer ausgewertet wird (in JSON durch null dargestellt).

  ![Leeres Bundle](assets/leave-content-field-unchanged.png)

* **Ersetzen Sie den Inhalt eines Felds**. Dieser Vorgang findet in allen anderen als den beiden oben beschriebenen Fällen statt.

>[!NOTE]
>
>* Wenn das Keyword `erase` im Zuordnungsbereich nicht angezeigt wird, ist das Modul kein Aktualisierungsmodul oder es wurde nicht auf die neuesten Spezifikationen für die App aktualisiert.
>* Der Inhalt des Felds wird durch `Empty` nicht geändert. Wenn das Feld gelöscht werden muss, können Sie die folgende Formel verwenden:
>
>   ![Wenn leer](assets/formula-ifempty-name-erase.png)
>
>* Ein Feld unverändert zu lassen, wenn sein Inhalt als leer ausgewertet wird, wird derzeit nicht unterstützt.

## Suchmodule

Suchmodule geben null, ein oder mehrere Bundles zurück, die dann zur Verarbeitung an das nächste Modul weitergegeben werden.

Sie können Suchmodule am Anfang, in der Mitte oder am Ende eines Szenarios platzieren.

Szenarien können eine unbegrenzte Anzahl von Suchmodulen enthalten, obwohl eine große Anzahl von Modulen (150+) die Leistung beeinträchtigen kann.

>[!BEGINSHADEBOX]

**Beispiel:**

**[!DNL Workfront]>[!UICONTROL Read Related Records]** liest Datensätze, die mit der von Ihnen angegebenen Suchabfrage in einem bestimmten übergeordneten Objekt übereinstimmen.

>[!ENDSHADEBOX]

## Trigger-Module

Trigger generieren Bundles, wenn eine Änderung in einem bestimmten Service stattgefunden hat, z. B. bei der Erstellung oder Aktualisierung eines Datensatzes.

Trigger geben null, ein oder mehrere Bundles zurück, die dann zur Verarbeitung an das nächste Modul übergeben werden.

Da Trigger dazu führen, dass Szenarien ausgeführt werden, können sie nur am Anfang eines Szenarios platziert werden.

Jedes Szenario kann nur einen Trigger enthalten.

[!DNL Workfront Fusion] werden zwei Typen von Triggern verwendet: Abfrage von Triggern und sofortige Trigger.

### Trigger werden abgerufen

Trigger fragen regelmäßig einen bestimmten Service ab, auch wenn sich seit der Ausführung des vorherigen Szenarios nichts geändert hat. Es wird empfohlen, ein Szenario mit einem Abrufintervall so zu planen, dass es in regelmäßigen Triggern ausgeführt wird. Wenn es eine Änderung gibt, die mit der Konfiguration des Triggers übereinstimmt, gibt der Trigger Bundles zurück, die Informationen über die Änderung enthalten. Wenn keine Änderung vorliegt, die mit der Konfiguration übereinstimmt, gibt der Trigger keine Pakete aus.

Anweisungen zum Planen eines Szenarios finden Sie unter [Planen eines Szenarios](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Mit Abruf-Triggern können Sie das erste Bundle auswählen, das über ein Bedienfeld ausgegeben werden soll, das nach dem Speichern eines Triggers oder Ändern der Trigger-Einstellungen automatisch angezeigt wird. Diese Auswahl betrifft nur die erste Ausführung des Moduls. Nachdem das Modul einmal ausgeführt wurde, überwachen nachfolgende Ausführungen nur noch die Änderungen, die nach der letzten Ausführung vorgenommen wurden.

Weitere Informationen finden Sie unter [Wählen, wo ein Trigger-Modul beginnt](/help/workfront-fusion/create-scenarios/add-modules/choose-where-trigger-module-starts.md).

>[!BEGINSHADEBOX]

**Beispiele:**

* **[!DNL Workfront]>[!UICONTROL Watch records]** gibt Datensätze zurück, die nach der letzten Ausführung des Szenarios neu hinzugefügt wurden.

* **[!DNL Google Sheets]>[!UICONTROL Watch Rows]** gibt neue Zeilen zurück, die nach der letzten Ausführung des Szenarios hinzugefügt wurden.

>[!ENDSHADEBOX]

### Sofortige Trigger

Sofortige Trigger ermöglichen es einem Service, [!DNL Workfront Fusion] sofort nach einer Änderung über eine Änderung zu informieren. Es wird empfohlen, ein Szenario mit einem sofortigen Trigger zu planen, der sofort ausgeführt werden soll.

Anweisungen finden Sie unter [Planen eines Szenarios](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Weitere Informationen zum Umgang mit eingehenden Daten durch einen Instant Trigger finden Sie unter [Instant Trigger (Webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

>[!BEGINSHADEBOX]

**Beispiele:**

* **[!DNL Workfront]>[!UICONTROL Watch Events]** gibt Informationen zurück, wenn ein bestimmter Ereignistyp in Workfront auftritt, z. B. bei der Erstellung einer Aufgabe.
* **[!DNL Google Sheets]>[!UICONTROL Watch Changes]** gibt Informationen zurück, wenn eine Zelle aktualisiert wird.

>[!ENDSHADEBOX]

## Aggregatoren

Ein Aggregator-Modul sammelt mehrere Bundles in einem Bundle.

Aggregatoren geben nur ein Bundle zurück, das dann zur weiteren Verarbeitung an das nächste Modul übergeben wird.

Aggregatoren können nur in der Mitte eines Szenarios platziert werden.

Szenarien können eine unbegrenzte Anzahl von Aggregatoren enthalten, obwohl sich eine große Anzahl von Modulen (150+) auf die Leistung auswirken kann.

>[!BEGINSHADEBOX]

**Beispiele:**

* **[!UICONTROL Archive]>[!UICONTROL Create an archive]** komprimiert mehrere Dateien in ein ZIP-Archiv.
* **[!UICONTROL CSV]>[!UICONTROL Aggregate to CSV]** führt mehrere Zeichenfolgen aus einer CSV-Datei in einer Zeile zusammen.
* **[!UICONTROL Tools]>[!UICONTROL Text aggregator]** kombiniert mehrere Zeichenfolgen zu einer einzigen Zeichenfolge.

>[!ENDSHADEBOX]

Weitere Informationen finden Sie unter [Aggregator-Modul](/help/workfront-fusion/references/modules/aggregator-module.md).

## Iteratoren

Ein Iterator ist ein Modultyp, der Arrays in separate Bundles aufteilt.

Iteratoren geben ein oder mehrere Bundles zurück, die dann zur Verarbeitung an das nächste Modul weitergegeben werden.

Iteratoren können nur in der Mitte eines Szenarios platziert werden.

Szenarien können eine unbegrenzte Anzahl von Iteratoren enthalten, obwohl eine große Anzahl von Modulen (150+) die Leistung beeinträchtigen kann.

>[!BEGINSHADEBOX]

**Beispiel:**

**[!UICONTROL Email]>[!UICONTROL Retrieve attachments]** unterteilt ein Array von Anlagen in separate Bundles.

>[!ENDSHADEBOX]

Weitere Informationen finden Sie unter [Iteratormodul](/help/workfront-fusion/references/modules/iterator-module.md) und [Array zuordnen](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).
