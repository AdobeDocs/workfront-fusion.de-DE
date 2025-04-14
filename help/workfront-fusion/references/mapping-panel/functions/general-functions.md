---
title: Allgemeine Funktionen
description: The following general functions are available in the Adobe Workfront Fusion mapping panel.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
source-git-commit: 295004ab7536b85124bc366d6832c08365338d08
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Allgemeine Funktionen

## Variablen

There are two general variables that you can use to identify details about an execution:

* `executionID`: the ID of this scenario execution
* `triggerTimestamp`: The time at which this execution was triggered

## [!UICONTROL get (object or array; path)]

Returns the value path of an object or array. To access nested objects, use dot notation. The first item in an array is index 1.

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

Returns the `value1` if this value is not empty; otherwise it returns the `value2`.

>[!BEGINSHADEBOX]

**Examples:**

* `ifempty(` `A` `;` `B` )

  Returns A

* `ifempty(` `unknown` `;` `B` )

  Gibt B zurück

* `ifempty(` `""` `;` `B` )

  Returns B

>[!ENDSHADEBOX]

## [!UICONTROL switch (expression; value1; result1; [value2; result2; ...]; [else])]

Evaluates one value (called the expression) against a list of values; returns the result corresponding to the first matching value. To include an  `else` value, add it after the final expression or value.

>[!BEGINSHADEBOX]

**Examples:**

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

`pick(` User `;` password `;` email `)`

Returns a collection of only the user&#39;s password and email address.

>[!ENDSHADEBOX]

## mergeCollections(collection1; collection2)

Führt zwei Sammlungen durch Kombinieren ihrer Schlüssel-Wert-Paare zusammen. Wenn beide Sammlungen denselben Schlüssel enthalten, überschreibt der Wert aus der zweiten Sammlung diesen Wert aus der ersten Sammlung.
