---
title: Mathematische Funktionen
description: Die folgenden mathematischen Funktionen sind im Zuordnungsbereich von Adobe Workfront Fusion verfügbar.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Mathematische Funktionen

## [!UICONTROL average ([array of values]) average(value1; [value2], ...)]

Gibt den Durchschnittswert der numerischen Werte in einem bestimmten Array oder den Durchschnittswert einzeln eingegebener numerischer Werte zurück.

## [!UICONTROL ceil (number)]

Gibt die kleinste Ganzzahl zurück, die größer oder gleich einer angegebenen Zahl ist.

>[!BEGINSHADEBOX]

**Beispiele:**

* `ceil(` `1.2` `)`

  Gibt 2 zurück

* `ceil(` `4` `)`

  Gibt 4 zurück

>[!ENDSHADEBOX]

## [!UICONTROL floor (number)]

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

## [!UICONTROL max ([array of values]), max(value1;value2; ...)]

Gibt die größte Zahl in einem angegebenen Array oder die größte Zahl einzeln eingegebener Zahlen zurück.

## [!UICONTROL min ([array of values]), min(value1; value2; ...)]

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

## [!UICONTROL sum ([array of values]), sum(value1; value2; ...)]

Gibt die Summe der Werte in einem angegebenen Array oder die Summe der einzeln eingegebenen Zahlen zurück.

## [!UICONTROL parseNumber (number; decimal separator)]

Analysiert eine Zeichenfolge mit einer Zahl und gibt die Zahl zurück. Beispiel: parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (number; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

Gibt eine Zahl im angeforderten Format zurück. Standardmäßig ist der Dezimalpunkt ein Komma (,) und das Tausendertrennzeichen ein Punkt (.).

>[!BEGINSHADEBOX]

**Beispiel:**

`formatNumber( 123456789 ; 3 ; , ; . )`

Gibt 123.456.789.000 zurück

>[!ENDSHADEBOX]
