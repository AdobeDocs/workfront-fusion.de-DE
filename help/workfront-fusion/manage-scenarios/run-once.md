---
title: Einmalige Ausführung verwenden, um ein Szenario zu testen
description: Sie können ein Szenario ohne externen Trigger testen, indem Sie die Schaltfläche Einmal ausführen verwenden.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 74faab448149276b8d769dfde0260c96d4b0712a
workflow-type: tm+mt
source-wordcount: 332
ht-degree: 0%

---

# Einmalige Ausführung verwenden, um ein Szenario zu testen

Beim Erstellen, Aktualisieren oder Verfeinern eines Szenarios können Sie die Schaltfläche „Einmal ausführen“ verwenden, um das Szenario bei Bedarf Trigger. Auf diese Weise können Sie das Szenario testen, ohne auf die zugehörige Ereignislogik zu warten, z. B. auf bestimmte Trigger oder Abrufintervalle.

Sie können ein Szenario auch einmal ausführen, um Datenstrukturen zu konfigurieren

>[!TIP]
>
>Es wird empfohlen, beim Erstellen und Verfeinern von Szenarien häufig zu testen.

## Verwenden der Funktion „Einmal ausführen“

Die Funktion „Einmal ausführen“ befindet sich im Szenario-Editor.

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie den Szenario-Scoring-Experten ausführen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken **unten links** Szenario-Editor auf „Einmal ausführen“.
1. (Bedingt) Wenn das Szenario durch einen Webhook ausgelöst wird oder ein untergeordnetes Szenario ist, wählen Sie die Eingabe für den Testlauf aus.

   * **Auf einen externen Webhook-Aufruf warten**: Das Szenario beginnt mit der Überwachung auf einen eingehenden Webhook-Aufruf. Sie müssen den Webhook vom externen System aus Trigger herstellen, um den Webhook bereitzustellen.

     Wenn der Webhook beispielsweise auf eine neue Anfrage in Workfront wartet, müssen Sie eine neue Anfrage in Workfront erstellen, um Trigger für die Funktion „Einmal ausführen“ zu erhalten.

     >[!NOTE]
     >
     >Diese Option ist nur für Webhook-Szenarien verfügbar.

   * **Verwenden Sie eine frühere Ausführungseingabe**: Sie müssen eine frühere Ausführung auswählen. Die Ausführung „Einmal ausführen“ verwendet die Eingabedaten, die die ausgewählte Ausführung ausgelöst haben.

     Um eine frühere Ausführung auszuwählen, wählen Sie die Ausführung aus und klicken Sie auf **Ausführen**.

     Um die Eingabedaten aus der Ausführung zu überprüfen, bevor Sie sie auswählen, klicken Sie auf **Vorschau der Eingabe** für diese Ausführung.

     >[!NOTE]
     >
     >Das Szenario muss frühere Ausführungen abgeschlossen haben, bevor diese Option verfügbar ist.

   * **Manuelle Eingabe**: Sie müssen die Webhook-Payload für die Szenario-Eingabe angeben. Dieser muss im JSON-Format vorliegen.

     Geben Sie zum Bereitstellen der Eingabe den Text in das Feld **Webhook-Payload** ein und klicken Sie auf **Ausführen**.



