---
title: Überblick über Module
description: 'Adobe Workfront Fusion unterscheidet fünf Modultypen: Aktionsmodule, Suchmodule, Auslösermodule, Aggregatoren und Iteratoren. Aggregatoren und Iteratoren werden für fortgeschrittene Szenarios verwendet.'
author: Becky
feature: Workfront Fusion
exl-id: 4c8fe028-8425-426d-a006-f0c66871b3cd
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: ht
source-wordcount: '917'
ht-degree: 100%

---

# Überblick über Module

Adobe Workfront Fusion unterscheidet fünf Modultypen:

* Aktionsmodule
* Suchmodule
* Auslösermodule
* Aggregatoren
* Iteratoren

Aggregatoren und Iteratoren werden für fortgeschrittene Szenarios verwendet.

## Aktionsmodule

Aktionsmodule sind der am häufigsten verwendete Modultyp. Ein typisches Aktionsmodul führt eine Aktion aus und gibt ein einzelnes Paket zurück, das dann zur Verarbeitung an das nächste Modul weitergegeben wird.

Im Gegensatz zu Auslösermodulen können Aktionsmodule am Anfang, in der Mitte oder am Ende eines Szenarios platziert werden.

Szenarios können eine unbegrenzte Anzahl von Aktionsmodulen enthalten. Allerdings kann eine große Anzahl von Modulen (mehr als 150) die Leistung beeinträchtigen.

>[!BEGINSHADEBOX]

**Beispiele:**

* **Workfront > [!UICONTROL Datei hochladen]**: Sendet eine Datei an Workfront und gibt die zugehörige Kennung zurück.
* **[!UICONTROL Bild] > [!UICONTROL Größe ändern]**: Empfängt ein Bild, ändert es den angegebenen Abmessungen entsprechend und übergibt das angepasste Bild an die nächste Aktion.

>[!ENDSHADEBOX]

Der Aktionstyp weist vier Untertypen auf:

* Erstellen
* Lesen
* Aktualisieren
* Löschen

Der Untertyp „Aktualisieren“ umfasst die drei folgenden Vorgänge:

* **Inhalt eines Felds löschen**. Dieser Vorgang erfolgt, wenn der Inhalt des Felds als Keyword `erase` ausgewertet wird (nicht zu verwechseln mit `empty`).

  ![Keyword löschen](assets/erase-content-of-field.png)

* **Inhalt eines Felds unverändert lassen**. Dieser Vorgang erfolgt, wenn das Feld leer gelassen oder der Inhalt des Felds als leer ausgewertet wird (in JSON durch null dargestellt).

  ![Leeres Paket](assets/leave-content-field-unchanged.png)

* **Inhalt eines Felds ersetzen**. Dieser Vorgang erfolgt in allen anderen als den beiden oben beschriebenen Fällen.

>[!NOTE]
>
>* Wenn das Keyword `erase` im Zuordnungs-Panel nicht angezeigt wird, ist das Modul kein Aktualisierungsmodul oder es wurde nicht auf die neuesten Spezifikationen für die Anwendung aktualisiert.
>* Der Inhalt des Felds wird durch `Empty` nicht geändert. Wenn das Feld gelöscht werden muss, können Sie die folgende Formel verwenden:
>
>   ![Wenn leer](assets/formula-ifempty-name-erase.png)
>
>* Ein Feld unverändert zu lassen, wenn sein Inhalt als leer ausgewertet wird, wird derzeit nicht unterstützt.

## Suchmodule

Suchmodule geben kein, ein oder mehrere Pakete zurück, die dann zur Verarbeitung an das nächste Modul weitergegeben werden.

Sie können Suchmodule am Anfang, in der Mitte oder am Ende eines Szenarios platzieren.

Szenarios können eine unbegrenzte Anzahl von Suchmodulen enthalten. Allerdings kann eine große Anzahl von Modulen (mehr als 150) die Leistung beeinträchtigen.

>[!BEGINSHADEBOX]

**Beispiel:**

**Workfront > [!UICONTROL Verwandte Einträge lesen]**: Liest Einträge, die Ihrer Suchanfrage in einem bestimmten übergeordneten Objekt übereinstimmen.

>[!ENDSHADEBOX]

## Auslösermodule

Auslöser generieren Pakete, wenn eine Änderung in einem bestimmten Service erfolgt ist, z. B. durch die Erstellung oder Aktualisierung eines Eintrags.

Auslöser geben kein, ein oder mehrere Pakete zurück, die dann zur Verarbeitung an das nächste Modul übergeben werden.

Da Auslöser zur Ausführung eines Szenarios führen, können sie nur am Anfang eines Szenarios platziert werden.

Jedes Szenario kann nur einen Auslöser enthalten.

Workfront Fusion verwendet zwei Typen von Auslösern: Auslöser, die auf Abruf oder sofort ausgeführt werden.

### Abrufauslöser

Abrufauslöser rufen regelmäßig Informationen von einem bestimmten Service ab, auch wenn sich seit der vorherigen Szenario-Ausführung nichts geändert hat. Es wird empfohlen, ein Szenario mit einem Abrufauslöser so zu planen, dass es regelmäßig ausgeführt wird. Wenn es eine Änderung gibt, die mit der Konfiguration des Auslösers übereinstimmt, gibt der Auslöser Pakete zurück, die Informationen zur Änderung enthalten. Wenn keine Änderung vorliegt, die der Konfiguration entspricht, gibt der Auslöser keine Pakete aus.

Anweisungen zum Planen eines Szenarios finden Sie unter [Planen eines Szenarios](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Mit Abrufauslösern können Sie das erste Paket auswählen, das über ein Panel ausgegeben werden soll, das nach dem Speichern eines Auslösers oder Ändern der Auslösereinstellungen automatisch angezeigt wird. Diese Auswahl betrifft nur die erste Ausführung des Moduls. Nachdem das Modul einmal ausgeführt wurde, achten nachfolgende Ausführungen nur noch auf die Änderungen, die nach der letzten Ausführung vorgenommen wurden.

Weitere Informationen finden Sie unter [Wählen des Ausgangspunkts eines Auslösermoduls](/help/workfront-fusion/create-scenarios/add-modules/choose-where-trigger-module-starts.md).

>[!BEGINSHADEBOX]

**Beispiele:**

* **Workfront > [!UICONTROL Einträge überwachen]**: Gibt Einträge zurück, die nach der letzten Ausführung des Szenarios neu hinzugefügt wurden.

* **[!DNL Google Sheets]> [!UICONTROL Zeilen überwachen]**: Gibt neue Zeilen zurück, die nach der letzten Ausführung des Szenarios hinzugefügt wurden.

>[!ENDSHADEBOX]

### Instant-Auslöser

Instant-Auslöser ermöglichen es einem Service, Workfront Fusion bei Auftreten einer Änderung sofort darüber zu informieren. Es wird empfohlen, ein Szenario mit einem Instant-Auslöser so zu planen, dass es sofort ausgeführt wird.

Anweisungen finden Sie unter [Planen eines Szenarios](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Weitere Informationen zum Umgang mit eingehenden Daten durch einen Instant-Auslöser finden Sie unter [Instant-Auslöser (Webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

>[!BEGINSHADEBOX]

**Beispiele:**

* **Workfront > [!UICONTROL Ereignisse überwachen]**: Gibt Informationen zurück, wenn ein bestimmter Ereignistyp in Workfront auftritt, z. B. die Erstellung einer Aufgabe.
* **[!DNL Google Sheets]> [!UICONTROL Änderungen überwachen]**: Gibt Informationen zurück, sobald eine Zelle aktualisiert wird.

>[!ENDSHADEBOX]

## Aggregatoren

Ein Aggregatormodul führt mehrere Pakete zu einem Paket zusammen.

Aggregatoren geben nur ein Paket zurück, das dann zur weiteren Verarbeitung an das nächste Modul übergeben wird.

Aggregatoren können nur in der Mitte eines Szenarios platziert werden.

Szenarios können eine unbegrenzte Anzahl von Aggregatoren enthalten. Allerdings kann eine große Anzahl Aggregatoren (mehr als 150) die Leistung beeinträchtigen.

>[!BEGINSHADEBOX]

**Beispiele:**

* **[!UICONTROL Archivieren] > [!UICONTROL Archiv erstellen]**: Komprimiert mehrere Dateien in ein ZIP-Archiv.
* **[!UICONTROL CSV] > [!UICONTROL In CSV aggregieren]**: Führt mehrere Zeichenfolgen aus einer CSV-Datei in einer Zeile zusammen.
* **[!UICONTROL Tools] > [!UICONTROL Textaggregator]**: Kombiniert mehrere Zeichenfolgen zu einer einzigen Zeichenfolge.

>[!ENDSHADEBOX]

Weitere Informationen finden Sie unter [Aggregatormodul](/help/workfront-fusion/references/modules/aggregator-module.md).

## Iteratoren

Ein Iterator ist ein Modultyp, der Arrays in separate Pakete aufteilt.

Iteratoren geben ein oder mehrere Pakete zurück, die dann zur Verarbeitung an das nächste Modul weitergegeben werden.

Iteratoren können nur in der Mitte eines Szenarios platziert werden.

Szenarios können eine unbegrenzte Anzahl von Iteratoren enthalten. Allerdings kann eine große Anzahl Iteratoren (mehr als 150) die Leistung beeinträchtigen.

>[!BEGINSHADEBOX]

**Beispiel:**

**[!UICONTROL E-Mail] > [!UICONTROL Anhänge abrufen]**: Teilt ein Array von Anhängen in separate Pakete auf.

>[!ENDSHADEBOX]

Weitere Informationen finden Sie unter [Iteratormodul](/help/workfront-fusion/references/modules/iterator-module.md) und [Zuordnen eines Arrays](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).
