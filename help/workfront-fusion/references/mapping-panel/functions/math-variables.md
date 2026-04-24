---
title: Mathematische Variablen
description: Die folgenden mathematischen Variablen sind im - [!DNL Adobe Workfront Fusion mapping]  verfügbar.
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
source-git-commit: 72abd9b5aa73d54edd73dc16f7695d2b01cc8624
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 13%

---

# Mathematische Variablen

## pi

Stellt das mathematische Symbol $\pi$ dar.

## [!UICONTROL random]

Gibt eine pseudo-zufällige Gleitkommazahl im Bereich [`0`,`1`] zurück (einschließlich `0`, aber nicht `1`).

Verwenden Sie die folgende Formel, um eine ganzzahlige pseudo-zufällige Zahl im Bereich [`min`,`max`] zu generieren (einschließlich sowohl `min` als auch `max`):

![Random](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
