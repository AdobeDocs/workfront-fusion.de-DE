---
title: Übersicht über die Zuordnung
description: Bei der Zuordnung werden die Ausgaben eines Moduls, strukturiert in Elemente, den Eingabefeldern eines anderen Moduls zugewiesen.
author: Becky
feature: Workfront Fusion
exl-id: 9208ce20-0757-427a-9669-ce4274d05522
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Übersicht über die Zuordnung

Beim Mapping werden die Ausgaben eines Moduls den Eingabefeldern eines anderen Moduls zugewiesen.

Der Betrieb eines Moduls erzeugt null, ein oder mehrere Bundles als Ausgabe. Ein Bundle besteht aus einem oder mehreren Elementen.

Sie können diese Elemente Feldern in späteren Modulen zuordnen.

Wenn Sie auf ein Feld klicken, in das Sie einen Wert einfügen können, der von einem vorherigen Modul in einem Szenario ausgegeben wurde, wird das Zuordnungsbedienfeld angezeigt. Hier können Sie das Element auswählen, das Sie zuordnen möchten. Eine Zuordnung kann eine oder mehrere der folgenden Optionen enthalten:

* Ein einzelnes Element
* Mehrere Elemente
* Statischer Text
* Funktionen

>[!BEGINSHADEBOX]

**Beispiele**:

Einzelnes Element

![Einzelnes Element zuordnen](assets/map-single.png)

Mehrere Elemente mit Text

![Mehrere Elemente zuordnen](assets/map-multiple-with-text.png)

Funktion mit mehreren Elementen und Text

![Formel mit Text zuordnen](assets/map-formula-with-text.png)


>[!ENDSHADEBOX]


Anweisungen zum Zuordnen finden Sie in den Artikeln unter [Zuordnungsdaten: Artikelindex](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md).

>[!NOTE]
>
>Die Ausgaben von Modulen, die zwischen einem [!UICONTROL Iterator] und [!UICONTROL Aggregator] eingeschlossen sind, sind über das [!UICONTROL Aggregator] Modul hinaus nicht zugänglich.

## Das Zuordnungsbedienfeld

Wenn Sie in ein Feld klicken, in dem Sie Daten zuordnen können, wird das Zuordnungsbedienfeld geöffnet.

Auf der ersten Registerkarte ![Aus anderen Modulen zuordnen](assets/toolbar-icon-functions-you-map-from-other-modules.png) werden die Elemente angezeigt, die Sie aus anderen Modulen zuordnen können.

Die anderen Registerkarten umfassen Funktionen, Operatoren und Schlüsselwörter, die Sie zum Erstellen von Formeln verwenden können. Diese sind je nach Datentyp in verschiedene Registerkarten unterteilt.

![Zuordnungsbereich](assets/mapping-panel-blank.png)


Weitere Informationen zu Funktionsregisterkarten finden Sie unter [Funktionsübersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md).

Weitere Informationen zum Zuordnen von Elementen mithilfe von Funktionen finden Sie unter [Zuordnen von Elementen mithilfe von Funktionen](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

## Sammlungen

Elemente können mehrere Werte verschiedener Typen enthalten. Hierbei handelt es sich um Elemente vom Typ Sammlung.

Bundles vom Typ Sammlung werden in der Modulausgabe `(Collection)` neben der Bundle-Beschriftung angezeigt.

![Sammlung](assets/collection.png)

In den meisten Fällen ordnen Sie die Elemente der Sammlung zu, anstatt das Element zuzuordnen, das die gesamte Sammlung darstellt.

Um das Element einer Sammlung im Zuordnungsbereich zu finden, klicken Sie auf den Pfeil neben der Sammlung.

![Sammlungs-Dropdown](assets/collection-dropdown.png)

Weitere Informationen zu Sammlungen finden Sie unter [Elementdatentypen](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

Anweisungen zum Zuordnen von Sammlungen finden Sie unter [Zuordnen eines Elements](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md#map-an-item) im Artikel Zuordnungsinformationen von einem Modul zu einem anderen.

## Arrays

Elemente können mehrere Werte desselben Typs enthalten. Dies sind Elemente vom Typ Array.

Bundles vom Typ Array werden `(Array)` neben der Bundle-Beschriftung in der Modulausgabe angezeigt.

Im Zuordnungsbereich werden Arrays mit eckigen Klammern angezeigt. Ein Element vom Typ Array kann durch die eckigen Klammern am Ende der Beschriftung des Elements identifiziert werden. Um ein bestimmtes Array-Element im Zuordnungsbereich zu finden, klicken Sie auf den Pfeil neben dem Array.

![Array](assets/array.png)

Informationen und Anweisungen zum Zuordnen von Arrays und Array-Elementen finden Sie unter [Zuordnen von Arrays und Array-Elementen](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).
