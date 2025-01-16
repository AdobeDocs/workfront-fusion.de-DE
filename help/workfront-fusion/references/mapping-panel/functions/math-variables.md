---
title: Mathematische Variablen
description: Die folgenden mathematischen Variablen sind im - [!DNL Adobe Workfront Fusion mapping]  verfügbar.
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 0%

---

# Mathematische Variablen

## Pi

Stellt das mathematische Symbol $\pi$ dar.

## [!UICONTROL random]

Gibt eine pseudo-zufällige Gleitkommazahl im Bereich [`0`,`1`] zurück (einschließlich `0`, aber nicht `1`).

Verwenden Sie die folgende Formel, um eine ganzzahlige pseudo-zufällige Zahl im Bereich [`min`,`max`] zu generieren (einschließlich sowohl `min` als auch `max`):

![](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
