---
title: Webhooks bearbeiten
description: Sie können bestehende Webhooks für die Workfront- und Workfront Planning-Connectoren bearbeiten.
author: Becky
feature: Workfront Fusion
source-git-commit: 2561c911b9b542a7b143fae745baf4e1de45be38
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 4%

---

# Webhooks bearbeiten

Sie können vorhandene Webhooks bearbeiten. In Szenarien, in denen diese Webhooks verwendet werden, wird künftig die neue Konfiguration verwendet, sodass kein neuer Webhook mehr erstellt werden muss und er nicht mehr allen betroffenen Szenarien manuell zugewiesen werden muss.

Webhooks können nur für die folgenden Connectoren bearbeitet werden:

* Workfront
* Workfront Planning

>[!IMPORTANT]
>
>Beachten Sie beim Aktualisieren eines Webhooks Folgendes:
>
>* Der bearbeitete Webhook wird von Workfront-Ereignisabonnements als neues Abonnement behandelt. Der Verlauf der Ereignisabonnements wird für die vorherige Webhook-Konfiguration nicht beibehalten, da dies als separates Ereignisabonnement betrachtet wird.
>* Der Wechsel vom alten zum neuen Ereignisabonnement ist möglicherweise nicht perfekt synchronisiert. Es ist daher möglich, ein Ereignis zweimal zu erhalten (wenn das neue Abonnement vor dem alten abläuft) oder ein Ereignis zu verpassen (wenn das alte Abonnement vor dem Start des neuen abläuft).

## Webhook bearbeiten

Sie können Webhooks über ein Szenario oder die Webhooks-Liste bearbeiten.

### Webhook in einem Szenario bearbeiten

>[!NOTE]
>
>Diese Funktion ist nur für Szenarien mit einem Workfront- oder Workfront Planning Instant Trigger-Modul verfügbar.

1. Wechseln Sie zu dem Szenario, das den Webhook enthält, den Sie bearbeiten möchten.
1. Klicken Sie im Trigger-Modul des Szenarios auf das Dropdown-Menü neben dem Feld Webhook und wählen Sie **Element bearbeiten**.

   Das Konfigurationsfenster des Webhooks wird geöffnet und mit der vorhandenen Konfiguration gefüllt.

1. Nehmen Sie die gewünschten Änderungen am Webhook vor.
1. Klicken Sie auf **Speichern**, um den Webhook zu speichern und zu dem Modul zurückzukehren.

### Bearbeiten eines Webhooks über die Liste Webhooks

1. Wählen Sie in der linken Navigation **Webhooks** ![Webhooks-Symbol](assets/webhooks-icon.png).
1. Aktivieren Sie das Kontrollkästchen neben dem Webhook, den Sie bearbeiten möchten.
1. Klicken Sie im blauen Banner unten auf dem Bildschirm auf **Bearbeiten**.
1. Nehmen Sie die gewünschten Änderungen am Webhook vor.
1. Klicken Sie auf **Speichern**, um den Webhook zu speichern und zur Liste Webhooks zurückzukehren.

