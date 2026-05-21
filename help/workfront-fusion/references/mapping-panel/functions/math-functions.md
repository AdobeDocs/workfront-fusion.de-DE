---
title: Mathematische Funktionen
description: Die folgenden mathematischen Funktionen sind im Zuordnungsbereich von Adobe Workfront Fusion verfügbar.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
TQID: https://experienceleague.adobe.com/a0WYFvPFBnXOvKS9ndQ-TD5xSvJz2bCbUbDY5VnXW0w
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 404
ht-degree: 14%

---

# Mathematische Funktionen

## [!UICONTROL average ([Array von Werten]) average(Wert1; [Wert2], …)]

Gibt den Durchschnittswert der numerischen Werte in einem bestimmten Array oder den Durchschnittswert einzeln eingegebener numerischer Werte zurück.

## [!UICONTROL CELL (Zahl)]

Gibt die kleinste Ganzzahl zurück, die größer oder gleich einer angegebenen Zahl ist.

>[!BEGINSHADEBOX]

**Beispiele:**

* `ceil(` `1.2` `)`

  Gibt 2 zurück

* `ceil(` `4` `)`

  Gibt 4 zurück

>[!ENDSHADEBOX]

## [!UICONTROL FLOOR (number)]

Gibt die größte Ganzzahl zurück, die kleiner oder gleich einer angegebenen Zahl ist.

>[!BEGINSHADEBOX]

**Beispiele:**

* `floor(` `1.2` `)`

  Gibt 1 zurück

* `floor(` `1.9` `)`

  Gibt 1 zurück

* `floor(` `4` `)`

  Gibt 4 zurück

>[!ENDSHADEBOX]

## [!UICONTROL max ([Array von Werten]), max(Wert1;Wert2; …)]

Gibt die größte Zahl in einem angegebenen Array oder die größte Zahl einzeln eingegebener Zahlen zurück.

## [!UICONTROL min ([Array von Werten]), min(Wert1; Wert2; …)]

Gibt die kleinste Zahl in einem angegebenen Array oder die kleinste Zahl unter einzeln eingegebenen Zahlen zurück.

## [!UICONTROL round (number)]

Rundet einen numerischen Wert auf die nächste Ganzzahl.

>[!BEGINSHADEBOX]

**Beispiele:**

* `round(` `1.2` `)`

  Gibt 1 zurück

* `round(` `1.5` `)`

  Gibt 2 zurück

* `round(` `1.7` `)`

  Gibt 2 zurück

* `round(` `2` `)`

  Gibt 2 zurück

>[!ENDSHADEBOX]

## [!UICONTROL SUM ([Array von Werten]), SUM(Wert1; Wert2; …)]

Gibt die Summe der Werte in einem angegebenen Array oder die Summe der einzeln eingegebenen Zahlen zurück.

## [!UICONTROL parseNumber (Zahl; Dezimaltrennzeichen)]

Analysiert eine Zeichenfolge mit einer Zahl und gibt die Zahl zurück. Beispiel: parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (Zahl; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

Gibt eine Zahl im angeforderten Format zurück. Standardmäßig ist der Dezimalpunkt ein Komma (,) und das Tausendertrennzeichen ein Punkt (.).

>[!BEGINSHADEBOX]

**Beispiel:**

`formatNumber( 123456789 ; 3 ; , ; . )`

Gibt 123.456.789,000 zurück

>[!ENDSHADEBOX]

### [!UICONTROL ABS(Zahl)]

[!BADGE Neu!]{type=Informative}

Gibt den absoluten Wert einer Zahl zurück.

>[!BEGINSHADEBOX]

**Beispiel:**

* `abs(-3.14)`

  Gibt 3.14 zurück
* `abs(3.14)`

  Gibt 3.14 zurück


### [!UICONTROL DIV(Zahl1; Zahl2; …)]

[!BADGE Neu!]{type=Informative}

Dividiert alle Zahlen in der vorgegebenen Reihenfolge.

>[!BEGINSHADEBOX]

**Beispiel:**

* `div(10; 2)`

  Gibt 5 zurück
* `div(100; 5; 4)`

  Gibt 5 zurück


### [!UICONTROL ln(Zahl)]

[!BADGE Neu!]{type=Informative}

Gibt den natürlichen Logarithmus der Zahl zurück.


>[!BEGINSHADEBOX]

**Beispiel:**

* `ln(1)`

  Gibt 0 zurück
* `ln(2.718281828)`

  Gibt 1 zurück


### [!UICONTROL LOG(Zahl1; Zahl2)]

[!BADGE Neu!]{type=Informative}

Gibt den Logarithmus der `number2` zum `number1` zurück.

>[!BEGINSHADEBOX]

**Beispiel:**

* `log(10; 100)`

  Gibt 2 zurück
* `log(2; 8)`

  Gibt 3 zurück


### [!UICONTROL number(string)]

[!BADGE Neu!]{type=Informative}

Konvertiert eine Zeichenfolge in eine Zahl.

>[!BEGINSHADEBOX]

**Beispiel:**

* `number("3.14")`

  Gibt 3.14 zurück
* `number("42")`

  Gibt 42 zurück


### [!UICONTROL POWER(Zahl;Leistung)]

[!BADGE Neu!]{type=Informative}

Gibt eine Zahl zurück, die die angegebene Potenz erreicht.

>[!BEGINSHADEBOX]

**Beispiel:**

* `power(2; 3)`

  Gibt 8 zurück
* `power(4; 0.5)`

  Gibt 2 zurück


### [!UICONTROL PROD(Zahl1; Zahl2; …)]

[!BADGE Neu!]{type=Informative}

Multipliziert alle angegebenen Zahlen.

>[!BEGINSHADEBOX]

**Beispiel:**

* `prod(2; 3; 4)`

  Gibt 24 zurück
* `prod(5; 5)`

  Gibt 25 zurück


### [!UICONTROL sortAscNum(Zahl1; Zahl2; …)]

[!BADGE Neu!]{type=Informative}

Gibt die angegebenen Zahlen in aufsteigender Reihenfolge zurück.

>[!BEGINSHADEBOX]

**Beispiel:**

* `sortAscNum(3; 1; 2)`

  Gibt \[1, 2, 3] zurück
* `sortAscNum(5; 3; 4)`

  Gibt \[3, 4, 5] zurück


### [!UICONTROL sortDescNum(Zahl1; Zahl2; …)]

[!BADGE Neu!]{type=Informative}

Gibt die angegebenen Zahlen in absteigender Reihenfolge zurück.

>[!BEGINSHADEBOX]

**Beispiel:**

* `sortDescNum(3; 1; 2)`

  Gibt \[3, 2, 1] zurück
* `sortDescNum(5; 3; 4)`

  Gibt \[5, 4, 3] zurück


### [!UICONTROL SQRT(Zahl)]

[!BADGE Neu!]{type=Informative}

Gibt die Quadratwurzel einer Zahl zurück.

>[!BEGINSHADEBOX]

**Beispiel:**

* `sqrt(9)`

  Gibt 3 zurück
* `sqrt(4)`

  Gibt 2 zurück


### [!UICONTROL SUB(Zahl1; Zahl2; …)]

[!BADGE Neu!]{type=Informative}

Subtrahiert alle Zahlen in der angegebenen Reihenfolge.

>[!BEGINSHADEBOX]

**Beispiel:**

* `sub(10; 3; 2)`

  Gibt 5 zurück
* `sub(20; 5)`

  Gibt 15 zurück
