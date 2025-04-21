---
title: Array-Funktionen
description: Die folgenden Array-Funktionen sind im Bedienfeld "Adobe Workfront Fusion-Zuordnung“ verfügbar.
author: Becky
feature: Workfront Fusion
exl-id: 16c3915c-add1-4aab-a0e1-75fc590c42a6
source-git-commit: d141738a7e013ed817cb657b883fc5e1061e2165
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# Array-Funktionen

## [!UICONTROL Join (Array;Trennzeichen)]

Verkettet alle Elemente eines Arrays in einer Zeichenfolge, wobei zwischen den einzelnen Elementen das angegebene Trennzeichen verwendet wird.

## [!UICONTROL length (Array)]

Gibt die Anzahl der Elemente in einem Array zurück.

## [!UICONTROL keys (Objekt)]

Gibt ein Array der Eigenschaften eines bestimmten Objekts oder Arrays zurück.

## [!UICONTROL slice (Array; Start; [end])]

Gibt ein neues Array zurück, das nur ausgewählte Elemente enthält.

## [!UICONTROL Zusammenführen (Array1; Array2; …)]

Führt ein oder mehrere Arrays in einem Array zusammen.

## [!UICONTROL Enthält (Array; Wert)]

Prüft, ob ein Array den Wert enthält.

## [!UICONTROL Entfernen (Array; Wert1; Wert2; …)]

Entfernt die in den Parametern eines Arrays angegebenen Werte. Diese Funktion ist nur bei primitiven Text- oder Zahlenfeldern wirksam.

## [!UICONTROL add (Array; Wert1; Wert2; …)]

Fügt die in den Parametern angegebenen Werte zu einem Array hinzu und gibt dieses Array zurück.

## [!UICONTROL Map (komplexes Array; Schlüssel; [Schlüssel zum Filtern]; [mögliche Werte zum Filtern])]

Gibt ein primitives Array mit Werten eines komplexen Arrays zurück. Diese Funktion ermöglicht das Filtern von Werten. Verwenden Sie unformatierte Variablennamen für Schlüssel.

>[!BEGINSHADEBOX]

**Beispiele:**

* `map(Emails[];email)`

  Gibt ein primitives Array mit E-Mails zurück.

* `map(Emails[];email;label;work;home)`

  Gibt ein primitives Array mit E-Mails mit einer Kennzeichnung wie Arbeit oder Startseite zurück.

>[!ENDSHADEBOX]

Weitere Informationen finden Sie unter [Zuordnen eines Arrays oder Array-Elements](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).

## schlurfen

## [!UICONTROL sort (Array; [order]; [key])]

Sortiert die Werte eines Arrays. Die gültigen Werte des `order` sind:

* `asc`

  (Standard) - aufsteigende Reihenfolge: 1, 2, 3, … für Typ Nummer. A, B, C, a, b, c, … für den Typ Text

* `desc`

  Absteigende Reihenfolge: …, 3, 2, 1 für Typ Nummer. …, c, b, a, C, B, A für den Typ Text.

* `asc ci`

  Aufsteigende Reihenfolge ohne Unterscheidung der Groß- und Kleinschreibung: A, a, B, b, C, c, … für den Typ Text.

* `desc ci`

  Groß-/Kleinschreibung wird nicht in absteigender Reihenfolge beachtet: …, C, c, B, b, A, a für Typ Text.

Verwenden Sie den `key`-Parameter, um auf Eigenschaften in komplexen Objekten zuzugreifen.

Verwenden Sie unformatierte Variablennamen für Schlüssel.

Verwenden Sie Punktnotation, um auf verschachtelte Eigenschaften zuzugreifen.

Das erste Element in einem Array ist Index 1.

>[!BEGINSHADEBOX]

**Beispiele:**

* `sort(Contacts[];name)`

  Sortiert ein Array von Kontakten nach der Eigenschaft „name“ in aufsteigender Standardreihenfolge.

* `sort(Contacts[];desc;name)`

  Sortiert ein Array von Kontakten nach der Eigenschaft „name“ in absteigender Reihenfolge

* `sort(Contacts[];asc ci;name)`

  Sortiert ein Array von Kontakten nach der Eigenschaft „name“ in aufsteigender Reihenfolge ohne Berücksichtigung der Groß-/Kleinschreibung

* `sort(Emails[];sender.name)`

  Sortiert ein Array von E-Mails nach der Eigenschaft „sender.name“

>[!ENDSHADEBOX]

## [!UICONTROL reverse (Array)]

Das erste Element des Arrays wird zum letzten Element, das zweite zum vorletzten Element usw.

## [!UICONTROL reduzieren (Array)]

Erstellt ein neues Array, in dem alle Unterarray-Elemente rekursiv bis zur angegebenen Tiefe verkettet sind.

## [!UICONTROL distinct (Array; [key])]

Entfernt Duplikate innerhalb eines Arrays. Verwenden Sie das [!UICONTROL key]-Argument, um auf Eigenschaften in komplexen Objekten zuzugreifen. Verwenden Sie Punktnotation, um auf verschachtelte Eigenschaften zuzugreifen. Das erste Element in einem Array ist Index 1.

>[!BEGINSHADEBOX]

**Beispiel:** `distinct(Contacts[];name)`

Entfernt Duplikate innerhalb eines Arrays von Kontakten, indem die Eigenschaft „name“ verglichen wird.

>[!ENDSHADEBOX]

## toCollection

* Diese Funktion wandelt ein Array, das Schlüssel-Wert-Paare enthält, in eine Sammlung um. Die Funktion umfasst drei Argumente:

* (Array) enthält Schlüssel-Wert-Paare
* (String) Der Name des als Schlüssel zu verwendenden Felds
* (Zeichenfolge) Der Name des als Wert zu verwendenden Felds

>[!BEGINSHADEBOX]

Beispiel:

Ein Array erhalten:

```
[{"name":"Bob", "age":22}, {"name":"Tim", "age":23}]
```

und Argumente

```
{{toCollection(6.array; "name"; "age")}}
```

Die Funktion gibt zurück

```
{
    "Bob": 22,
    "Tim": 23
}
```

>[!ENDSHADEBOX]

## toArray

Diese Funktion wandelt eine Sammlung in ein Array von Schlüssel-Wert-Paaren um.

>[!BEGINSHADEBOX]

**Beispiele:**

Angegeben an die Sammlung

`{ key1: "value1", key2: "value2:}`

Die Funktion

`toArray({ key1: "value1", key2: "value2:})`

Gibt das Array von Schlüssel-Wert-Paaren zurück.

`[{ key1: "value1"}, { key2: "value2"}]`

>[!ENDSHADEBOX]

## [!UICONTROL arrayDifference [array1, array2, mode]]

Gibt die Differenz zwischen zwei Arrays zurück.

Geben Sie einen der folgenden Werte für den `mode` ein.

* `classic`: Gibt ein neues Array zurück, das alle Elemente der `array1` enthält, die nicht in `array2` vorhanden sind.

* `symmetric`: Gibt ein Array von Elementen zurück, die nicht in beiden Arrays enthalten sind.

  Mit anderen Worten: Die Funktion gibt ein -Array zurück, das alle Elemente von `array1` enthält, die nicht in `array2` vorhanden sind, sowie alle Elemente von `array2`, die nicht in `array1` vorhanden sind.

>[!BEGINSHADEBOX]

**Beispiele:**

Bei den folgenden Arrays:

```
myArray = [1,2,3,4,5]
```

```
yourArray = [3,4,5,6,7]
```

* `arrayDifference [myArray, yourArray, classic]`

  Gibt `[1,2]`

* `arrayDifference [yourArray, myArray, classic]`

  Gibt `[6,7]`

* `arrayDifference [myArray, yourArray, symmetric]`

  Gibt `[1,2,6,7]`

>[!ENDSHADEBOX]

## deduplizieren

## Schlüsselwörter

## emptyarray
