---
title: Allgemeine Funktionen
description: Die folgenden allgemeinen Funktionen sind im Bedienfeld "Adobe Workfront Fusion-Zuordnung“ verfügbar.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
source-git-commit: 2c732659f3f3e81e13b7b12a5df5bde19c0e0928
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Allgemeine Funktionen

## [!UICONTROL get (object or array; path)]

Gibt den Wertpfad eines Objekts oder Arrays zurück. Verwenden Sie Punktnotation, um auf verschachtelte Objekte zuzugreifen. Das erste Element in einem Array ist Index 1.

>[!BEGINSHADEBOX]

**Beispiele:**

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if (expression; value1; value2)]

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

## [!UICONTROL ifempty (value1; value2)]

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

## [!UICONTROL switch (expression; value1; result1; [value2; result2; ...]; [else])]

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

## [!UICONTROL omit(object; key1; [key2; ...])]

Lässt die angegebenen Schlüssel des -Objekts aus und gibt den Rest zurück.

>[!BEGINSHADEBOX]

**Beispiel:**

`omit(` Benutzer `;` Passwort `)`

Gibt eine Sammlung der Benutzerinformationen zurück, mit Ausnahme des Kennworts.

>[!ENDSHADEBOX]

## [!UICONTROL pick(object; key1; [key2; ...])]

Wählt nur die angegebenen Schlüssel aus dem Objekt aus.

>[!BEGINSHADEBOX]

**Beispiel:**

`pick(` Benutzer `;` Passwort `;` E-Mail-`)`

Gibt nur eine Sammlung von Passwort und E-Mail-Adresse der Benutzenden zurück.

>[!ENDSHADEBOX]

## mergeCollections(collection1;collection2)

Führt zwei Sammlungen durch Kombinieren ihrer Schlüssel-Wert-Paare zusammen. Wenn beide Sammlungen denselben Schlüssel enthalten, überschreibt der Wert aus der zweiten Sammlung diesen Wert aus der ersten Sammlung.
