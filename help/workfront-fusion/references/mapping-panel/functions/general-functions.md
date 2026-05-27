---
title: Allgemeine Funktionen
description: Die folgenden allgemeinen Funktionen sind im Bedienfeld "Adobe Workfront Fusion-Zuordnung“ verfügbar.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
TQID: https://experienceleague.adobe.com/1IX25ZtrWVizi5gZJfFw-acnW5eIuXpGgcXgXW0T-Hw
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 478
ht-degree: 8%

---

# Allgemeine Funktionen

## Variablen

Sie können die folgenden allgemeinen Variablen verwenden, um Details zu einer Ausführung anzugeben:

* `executionID`: die ID dieser Szenarioausführung
* `triggerTimestamp`: Der Zeitpunkt, zu dem diese Ausführung ausgelöst wurde
* `scenarioID`: Die ID des derzeit geöffneten Szenarios
* `scenarioName`: Der Name des aktuell ausgeführten Szenarios
* `operationsConsumed`: Die Anzahl der zu diesem Zeitpunkt im Szenario verwendeten Vorgänge.

## [!UICONTROL GET (Objekt oder Array; Pfad)]

Gibt den Wertpfad eines Objekts oder Arrays zurück. Verwenden Sie Punktnotation, um auf verschachtelte Objekte zuzugreifen. Das erste Element in einem Array ist Index 1.

>[!BEGINSHADEBOX]

**Beispiele:**

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if (Ausdruck; Wert1; Wert2)]

Gibt die `value1` zurück, wenn der Ausdruck als „true“ ausgewertet wird. Andernfalls wird die `value2` zurückgegeben.

Um eine if-Anweisung zu erstellen, die einen Wert nur dann zurückgibt, wenn zwei oder mehr Ausdrücke als „true“ ausgewertet werden, verwenden Sie das `and`-Schlüsselwort.

Um `if` Anweisungen zu kombinieren, verwenden Sie die Operatoren `and` und `or` .

![UND-Operator](assets/and-in-if-statement.png)

>[!BEGINSHADEBOX]

**Beispiele:**

* `if( 1 = 1 ; A ; B )`

  Gibt einen

* `if( 1 = 2 ; A ; B )`

  Gibt B zurück

* `if( 1 = 2 and 1 = 2 ; A ; B )`

  Gibt B zurück

>[!ENDSHADEBOX]

## [!UICONTROL IfEmpty (value1; value2)]

Gibt den `value1` zurück, wenn dieser Wert nicht leer ist. Andernfalls wird der `value2` zurückgegeben.

>[!BEGINSHADEBOX]

**Beispiele:**

* `ifempty(` `A` `;` `B` )

  Gibt einen

* `ifempty(` `unknown` `;` `B` )

  Gibt B zurück

* `ifempty(` `""` `;` `B` )

  Gibt B zurück

>[!ENDSHADEBOX]

## [!UICONTROL switch (Ausdruck; Wert1; Ergebnis1; [Wert2; Ergebnis2; …]; [else])]

Wertet einen Wert (den Ausdruck) anhand einer Werteliste aus und gibt das Ergebnis zurück, das dem ersten übereinstimmenden Wert entspricht. Um einen `else` Wert einzuschließen, fügen Sie ihn nach dem endgültigen Ausdruck oder Wert hinzu.

>[!BEGINSHADEBOX]

**Beispiele:**

* `switch( B ; A ; 1 ; B ; 2 ; C ; 3 )`

  Gibt 2 zurück

* `switch( C ; A ; 1 ; B ; 2 ; C ; 3 )`

  Gibt 3 zurück

* `switch( X ; A ; 1 ; B ; 2 ; C ; 3 ; 4 )`

  Gibt 4 zurück

  In dieser Funktion ist 4 der Wert, der zurückgegeben werden soll, wenn keine Ausdrücke gelten (der `else`).

>[!ENDSHADEBOX]

## [!UICONTROL OMIT(Objekt; Schlüssel1; [Schlüssel2; …])]

Lässt die angegebenen Schlüssel des -Objekts aus und gibt den Rest zurück.

>[!BEGINSHADEBOX]

**Beispiel:**

`omit(` Benutzer `;` Passwort `)`

Gibt eine Sammlung der Benutzerinformationen zurück, mit Ausnahme des Kennworts.

>[!ENDSHADEBOX]

## [!UICONTROL PICK(Objekt; Schlüssel1; [Schlüssel2; …])]

Wählt nur die angegebenen Schlüssel aus dem Objekt aus.

>[!BEGINSHADEBOX]

**Beispiel:**

`pick(` Benutzer `;` Passwort `;` E-Mail-`)`

Gibt nur eine Sammlung von Passwort und E-Mail-Adresse der Benutzenden zurück.

>[!ENDSHADEBOX]

## mergeCollections(collection1;collection2)

Führt zwei Sammlungen durch Kombinieren ihrer Schlüssel-Wert-Paare zusammen. Wenn beide Sammlungen denselben Schlüssel enthalten, überschreibt der Wert aus der zweiten Sammlung diesen Wert aus der ersten Sammlung.

### [!UICONTROL isBlank(value)]

Gibt `true` zurück, wenn der Wert `null` oder eine leere Zeichenfolge ist, andernfalls gibt `false` zurück. Im Gegensatz zu `ifEmpty` behandelt diese Funktion die Zeichenfolge `0` oder nur Leerzeichen nicht als leer.

>[!BEGINSHADEBOX]

**Beispiel:**

* `isBlank("")     `

  Gibt „true“ zurück
* `isBlank(null)   `

  Gibt „true“ zurück
* `isBlank("Hello")`

  Gibt „false“ zurück
* `isBlank(0)      `

  Gibt „false“ zurück
* `isBlank(" ")    `

  Gibt „false“ zurück

>[!ENDSHADEBOX]


### [!UICONTROL IN(Wert;Wert1;Wert2; …)]

Gibt &quot;`true`&quot; zurück, wenn der Wert einem der angegebenen Werte entspricht (strikte Gleichheit, keine Typenzwang).

>[!BEGINSHADEBOX]

**Beispiel:**

* `in("B"; "A"; "B"; "C")`

  Gibt „true“ zurück
* `in("D"; "A"; "B"; "C")`

  Gibt „false“ zurück
* `in(2; 1; 2; 3)        `

  Gibt „true“ zurück
* `in("2"; 1; 2; 3)      `

  Gibt „false“ zurück

>[!ENDSHADEBOX]

### [!UICONTROL ifin(Wert;Wert1;Wert2; …; trueExpression; falseExpression)]

Gibt `trueExpression` zurück, wenn der Wert mit einem der angegebenen Übereinstimmungswerte übereinstimmt. Gibt andernfalls `falseExpression` zurück. Erfordert mindestens 3 Argumente (Wert, ein Übereinstimmungswert und trueExpression + falseExpression).

>[!BEGINSHADEBOX]

**Beispiel:**

* `ifin("B"; "A"; "B"; "yes"; "no")`

  Gibt ja zurück
* `ifin("D"; "A"; "B"; "yes"; "no")`

  Gibt keine zurück.
* `ifin("X"; "X"; "found"; "not found")`

  Rückgaben gefunden

>[!ENDSHADEBOX]

### [!UICONTROL case(indexNumber; value1; value2; …)]

Gibt den Wert an der durch die Indexnummer angegebenen Position zurück (1-basiert). Gibt `null` zurück, wenn der Index außerhalb des Bereichs liegt oder 0 ist.

>[!BEGINSHADEBOX]

**Beispiel:**

* `case(1; "Sun"; "Mon"; "Tue")`

  Gibt Sun zurück
* `case(2; "Sun"; "Mon"; "Tue")`

  Gibt Mon zurück
* `case(3; "Sun"; "Mon"; "Tue")`

  Gibt „true“ zurück
* `case(5; "a"; "b")           `

  Gibt null zurück

>[!NOTE]
>
>Es wird empfohlen, dies zu verwenden, um den Tagesnamen von einem Datum abzurufen:
>`case(dayOfWeek(date); "Sun"; "Mon"; "Tue"; "Wed"; "Thu"; "Fri"; "Sat")`

>[!ENDSHADEBOX]

