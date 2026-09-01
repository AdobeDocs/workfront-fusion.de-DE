---
title: Anzeigen und Verwalten von Speicher in Workfront Fusion
description: Im Speicherbereich werden die verfügbaren Repositorys aufgelistet. Außerdem können Sie dort Ordner und Dateien durchsuchen.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 330
ht-degree: 1%

---

# Anzeigen und Verwalten von Speicher in Workfront Fusion

Der Speicherbereich in Workfront Fusion ermöglicht Ihnen die Anzeige von und die Interaktion mit Repositorys in Ihrem Adobe Cloud-Speicher.

Einen Überblick über Speicher finden Sie unter [Speicherübersicht](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

>[!TIP]
>
>Der Speicher muss initialisiert werden, bevor Sie Repositorys sehen können. Anweisungen finden Sie unter [Initialisieren von Speicher](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md).

## Anzeigen von Repositorys, Ordnern und Dateien

1. Klicken Sie in Workfront Fusion **linken** auf „Speicher“.
Eine Liste der Repositorys wird geöffnet.

   Wenn nur ein Repository verfügbar ist, wird das Repository direkt geöffnet.

1. Klicken Sie **einem** Repository auf „Öffnen“, um dessen Inhalt zu durchsuchen.

   Beim Öffnen eines Repositorys werden Ordner im Repository angezeigt.
1. Klicken Sie auf einen Ordner, um ihn zu öffnen und seine Dateien anzuzeigen.
1. Um zurück durch die Ordnerstruktur zu navigieren, klicken Sie auf die Breadcrumbs.


>[!NOTE]
>
>Ein leerer Ordner zeigt die Meldung an: *„Dieser Ordner ist leer“*

## Verwalten mehrerer Speicherverbindungen

Ein Team kann über mehrere Adobe-Speicherverbindungen verfügen.

1. Klicken Sie in Workfront Fusion **linken** auf „Speicher“.
Wenn mehrere Verbindungen vorhanden sind, werden Registerkarten oben auf der Speicherseite angezeigt, die mit dem Namen jeder Verbindung beschriftet sind.
1. Um zu den Repositorys einer anderen Verbindung zu wechseln, klicken Sie auf die Registerkarte für diese Verbindung.

Wenn eine Verbindung ungültig wird, z. B. wenn ihr Token abgelaufen ist und nicht aktualisiert werden konnte, wird sie automatisch herausgefiltert und wird nicht als Registerkarte angezeigt. Die geplante Token-Aktualisierung von Fusion sorgt dafür, dass die Verbindungen automatisch gültig bleiben.

## Dateiinformationen

Jede Datei in der Tabelle zeigt:

| Spalte | Beschreibung |
| -------- | ------------- |
| **Name** | Dateiname mit einem Dokument-Symbol. |
| **Typ** | Dateierweiterungs-Badge wie PNG, PDF oder JPG. |
| **size** | Dateigröße. Zeigt *„Wird verarbeitet…* an, ob die Datei kürzlich hochgeladen wurde und das Backend sie noch verarbeitet. |
| **Erstellt** | Erstellungsdatum. |

Dateien zeigen auch ein **Versionsabzeichen** (z. B. `v2`, `v3`), wenn mehrere Versionen vorhanden sind.

## Tabellen-Steuerelemente

* **Suche/Filter**: Filtern Sie Dateien anhand des Namens mithilfe der globalen Suchleiste.
* **Sortierung**: Klicken Sie zum Sortieren auf Spaltenüberschriften.
* **Paginierung**: Wählen Sie 10, 25, 50 oder 100 Elemente pro Seite aus. Der Standardwert lautet 25.
