---
title: Arbeitspools
description: Ein Worker-Pool ist eine Menge an Workfront Fusion-Verarbeitungsressourcen, die einer oder mehreren bestimmten Organisationen zugewiesen ist. Alle Fusion-Vorgänge und -Verarbeitungen erfolgen im Kontext des zugewiesenen Worker-Pools einer Organisation.
author: Becky
feature: Workfront Fusion
exl-id: 8bf508a8-d1f9-455f-af89-62f688289137
source-git-commit: b95974d19c3dcb2fea0d6323c2b747665216a2e7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%
---
# Arbeitskräftepools

Ein Worker-Pool ist eine Menge an Workfront Fusion-Verarbeitungsressourcen, die einer bestimmten Organisation zugewiesen ist. Alle Fusion-Vorgänge und -Verarbeitungen erfolgen im Kontext des zugewiesenen Worker-Pools einer Organisation.

Worker-Pools ermöglichen eine effizientere Ausführung Ihrer Szenarien und verhindern die Möglichkeit, mit anderen Organisationen um die Verarbeitungskapazität von Fusion zu konkurrieren.

## Übersicht über den Worker-Pool

Ein Worker-Pool ist eine Möglichkeit, Szenario-Ausführungen parallel zu verarbeiten. Jeder Worker-Pool ist verknüpft mit:

* Eine Reihe von Arbeitnehmern.
* Eine Ausführungswarteschlange.

Wenn ein Szenario ausgeführt wird, wird es in die Ausführungswarteschlange des Arbeitspools übergeben. Worker im Pool rufen Aufgaben kontinuierlich aus dem Ausführungspool ab und verarbeiten sie parallel.

Wenn die Ausführungswarteschlangentiefe zunimmt und alle vorhandenen Sekundäre verwendet werden, skaliert Workfront Fusion den Pool automatisch, indem weitere Sekundäre hinzugefügt werden. Diese Skalierung ist dynamisch und ereignisgesteuert, d. h. die Kapazität entspricht exakten oder Verträgen, die auf Echtzeitlasten basieren, ohne dass Sie oder Ihr Unternehmen Maßnahmen ergreifen.

Das Workfront Fusion-Team überwacht kontinuierlich die Nutzung und das Skalierungsverhalten von Pools und kann Schwellenwerte oder Muster überprüfen, um eine konsistente Leistung bei wachsender Nutzung sicherzustellen.
