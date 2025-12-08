---
title: Überblick über Zuordnungen
description: Beim Zuordnen werden die Ausgaben eines Moduls (in Elemente strukturiert) den Eingabefeldern eines anderen Moduls zugewiesen.
author: Becky
feature: Workfront Fusion
exl-id: 9208ce20-0757-427a-9669-ce4274d05522
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: ht
source-wordcount: '435'
ht-degree: 100%

---

# Überblick über Zuordnungen

Beim Zuordnen werden die Ausgaben eines Moduls den Eingabefeldern eines anderen Moduls zugewiesen.

Bei Verwendung eines Moduls werden kein, ein oder mehrere Pakete als Ausgabe erzeugt. Ein Paket besteht aus einem oder mehreren Elementen.

Sie können diese Elemente Feldern in späteren Modulen zuordnen.

Wenn Sie auf ein Feld klicken, in das ein Wert eingefügt werden kann, der von einem vorherigen Modul in einem Szenario ausgegeben wurde, wird das Zuordnungs-Panel angezeigt. Hier können Sie das Element auswählen, das zugeordnet werden soll. Eine Zuordnung kann eines oder mehrere der folgenden Objekte umfassen:

* ein einziges Element
* mehrere Elemente
* statischen Text
* Funktionen

>[!BEGINSHADEBOX]

**Beispiele**:

Ein einziges Element

![Ein einziges Element zuordnen](assets/map-single.png)

Mehrere Elemente mit Text

![Mehrere Elemente zuordnen](assets/map-multiple-with-text.png)

Funktion mit mehreren Elementen und Text

![Formel mit Text zuordnen](assets/map-formula-with-text.png)


>[!ENDSHADEBOX]


Anweisungen zum Zuordnen finden Sie in den Artikeln unter [Zuordnen von Daten: Artikelindex](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md).

>[!NOTE]
>
>Auf Ausgaben von Modulen, die zwischen [!UICONTROL Iterator] und [!UICONTROL Aggregator] eingeschlossen sind, kann nur über das Modul [!UICONTROL Aggregator] zugegriffen werden.

## Das Zuordnungs-Panel

Wenn Sie in ein Feld klicken, in dem Sie Daten zuordnen können, wird das Zuordnungs-Panel geöffnet.

Auf der ersten Registerkarte ![Aus anderen Modulen zuordnen](assets/toolbar-icon-functions-you-map-from-other-modules.png) werden die Elemente angezeigt, die aus anderen Modulen zugeordnet werden können.

Die anderen Registerkarten umfassen Funktionen, Operatoren und Keywords, mit denen Sie Formeln erstellen können. Diese sind je nach Datentyp in verschiedene Registerkarten unterteilt.

![Zuordnungs-Panel](assets/mapping-panel-blank.png)


Weitere Informationen zu Funktionsregisterkarten finden Sie unter [Überblick über Funktionen](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md).

Weitere Informationen zum Zuordnen von Elementen mithilfe von Funktionen finden Sie unter [Zuordnen von Elementen mithilfe von Funktionen](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

## Sammlungen

Elemente können mehrere Werte verschiedener Typen enthalten. Dies sind Elemente vom Typ „Sammlung“.

Pakete vom Typ „Sammlung“ `(Collection)` werden in der Modulausgabe neben dem Paket-Label angezeigt.

![Sammlung](assets/collection.png)

In den meisten Fällen ordnen Sie die Elemente der Sammlung zu und nicht das Element, das für die gesamte Sammlung steht.

Um das Element einer Sammlung im Zuordnungs-Panel zu finden, klicken Sie auf den Pfeil neben der Sammlung.

![Sammlungs-Dropdown](assets/collection-dropdown.png)

Weitere Informationen zu Sammlungen finden Sie unter [Elementdatentypen](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

Anweisungen zum Zuordnen von Sammlungen finden Sie unter [Zuordnen eines Elements](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md#map-an-item) im Artikel „Zuordnen von Informationen zwischen Modulen“.

## Arrays

Elemente können mehrere Werte desselben Typs enthalten. Dies sind Elemente vom Typ „Array“.

Pakete vom Typ „Array“ `(Array)` werden in der Modulausgabe neben dem Paket-Label angezeigt.

Im Zuordnungs-Panel werden Arrays mit eckigen Klammern angezeigt. Ein Element vom Typ „Array“ lässt sich anhand der eckigen Klammern am Ende des Element-Labels erkennen. Um ein bestimmtes Array-Element im Zuordnungs-Panel zu finden, klicken Sie auf den Pfeil neben dem Array.

![Array](assets/array.png)

Informationen und Anweisungen zum Zuordnen von Arrays und Array-Elementen finden Sie unter [Zuordnen von Arrays und Array-Elementen](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).
