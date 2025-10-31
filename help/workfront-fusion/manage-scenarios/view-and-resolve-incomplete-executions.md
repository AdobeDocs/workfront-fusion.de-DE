---
title: Anzeigen und Auflösen unvollständiger Ausführungen
description: Der Ordner [!UICONTROL Unvollständige Ausführungen] speichert Szenario-Ausführungen, die aufgrund eines Fehlers nicht erfolgreich abgeschlossen wurden. Jede gespeicherte unvollständige Ausführung kann entweder manuell oder automatisch aufgelöst werden.
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 5%

---

# Anzeigen und Auflösen unvollständiger Ausführungen

Der Ordner [!UICONTROL Unvollständige Ausführungen] speichert Szenario-Ausführungen, die aufgrund eines Fehlers nicht erfolgreich abgeschlossen wurden. Jede gespeicherte unvollständige Ausführung kann entweder manuell oder automatisch aufgelöst werden.

>[!NOTE]
>
>Standardmäßig ist das Speichern unvollständiger Ausführungen deaktiviert. Um sie zu aktivieren, aktivieren Sie die Option [!UICONTROL Speichern unvollständiger Ausführungen zulassen] in den erweiterten Einstellungen des Szenarios.
>
>Weitere Informationen zu Szenario-Einstellungen finden Sie unter [Konfigurieren von Szenario-Einstellungen](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Vorschau für vollständigen Artikel hervorgehoben {#highlighted-preview-article-level}

<span class="preview">Die Informationen auf dieser Seite beziehen sich auf Funktionen, die noch nicht allgemein verfügbar sind. Sie ist nur in der Sandbox-Vorschau -Umgebung verfügbar.</span>## Anzeigen unvollständiger Ausführungen

Wenn bei einem Modul während seines Vorgangs ein Fehler auftritt, wird eine neue unvollständige Ausführung zum Ordner Unvollständige Ausführungen hinzugefügt. Jede unvollständige Ausführung enthält den Blueprint des Szenarios und alle Bundles, die dem fehlgeschlagenen Modul zugeordnet werden können. Die Liste der unvollständigen Ausführungen kann durch Klicken auf die Registerkarte [!UICONTROL Unvollständige Ausführungen] auf der Seite mit den Szenario-Details geöffnet werden.

<!--

![Incomplete executions tab](assets/incomplete-executions-tab-350x102.png)

-->

Weitere Informationen finden Sie unter [Fehler, die zu unvollständigen Ausführungen führen](#errors-resulting-into-incomplete-executions) in diesem Artikel.

>[!NOTE]
>
>Die aktuelle Größenbeschränkung des nicht aufgelösten Ordners „Unvollständige Ausführungen“ pro Szenario beträgt 10 MB. Wenn Ihr Szenario diesen Grenzwert überschreitet, wird möglicherweise der folgende Fehler angezeigt:
>
>`DLQ limit per scenario has been exceeded`
>
>Teams sind auf insgesamt 500 MB für alle nicht aufgelösten unvollständigen Ausführungen beschränkt.
>
>Weitere Informationen finden Sie unter [Datenverlust aktivieren](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) im Artikel Konfigurieren von Szenario-Einstellungen.


## Beheben von unvollständigen Ausführungen über die Registerkarte Unvollständige Ausführungen

Wenn eine neue unvollständige Ausführung gespeichert wird, können Sie sie wie folgt auflösen:

1. Öffnen Sie das betroffene Szenario.
1. Klicken Sie auf die **[!UICONTROL Unvollständige Ausführungen]**.
1. Suchen Sie die unvollständige Ausführung, die Sie auflösen möchten, und klicken Sie auf **[!UICONTROL Details]**.
1. Öffnen Sie das Protokoll des Moduls, in dem alle Vorgänge des Moduls angezeigt werden.
1. Suchen Sie den fehlgeschlagenen Vorgang und klicken Sie auf **[!UICONTROL Auflösen]**:

   ![Schaltfläche „Auflösen](assets/resolve-btn-350x188.png)



## Beheben von unvollständigen Ausführungen über die Registerkarte Verlauf

Wenn Sie das Protokoll aller Modulvorgänge anzeigen möchten, bevor Sie versuchen, die unvollständige Ausführung aufzulösen, können Sie die unvollständige Ausführung über den Ordner [!UICONTROL Verlauf] auflösen:

1. Öffnen Sie das betroffene Szenario.
1. Klicken Sie auf die **[!UICONTROL Verlauf]**.
1. Suchen Sie nach der fehlgeschlagenen Ausführung des Szenarios und klicken Sie auf **[!UICONTROL Details]**.
1. Öffnen Sie das Protokoll des Moduls, in dem alle Vorgänge des Moduls angezeigt werden.
1. Suchen Sie den fehlgeschlagenen Vorgang und klicken Sie auf **[!UICONTROL Auflösen]**:

   ![Schaltfläche „Auflösen](assets/resolve-btn-350x188.png)

## Optionen im Zusammenhang mit unvollständigen Ausführungen

Die folgenden Optionen im Bedienfeld [!UICONTROL Szenarioeinstellungen] bestimmen, ob und wie die unvollständigen Ausführungen gespeichert werden:

* Speichern unvollständiger Ausführungen zulassen
* Sequenzielle Verarbeitung
* Datenverlust aktivieren

Weitere Informationen zu diesen Optionen finden Sie unter [Szenarioeinstellungen konfigurieren](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Fehler führen zu unvollständigen Ausführungen

Es gibt verschiedene Kategorien von Fehlern, die zur Speicherung unvollständiger Ausführungen führen. Dazu können gehören:

* Validierungsfehler, die aus unvollständigen oder fehlerhaften Daten resultieren, hauptsächlich aufgrund eines fehlenden Elements, das erwartet wird, um alle Daten, die ein Modul durchlaufen, erfolgreich zu verarbeiten.
* Fehler, die durch die Nichtverfügbarkeit des endgültigen Ziels aufgrund eines temporären oder langfristigen Verbindungsfehlers auftreten (z. B. während der Verbindung zu einem E-Mail- oder FTP-Remote-Server).

Tritt beim ersten Modul des Szenarios ein Fehler auf, wird die Ausführung sofort gestoppt und keine unvollständige Ausführung gespeichert.

Wenn ein Fehler bei einem anderen Modul auftritt und keine Fehler-Handler-Route angehängt ist, tritt einer der folgenden Fälle auf:

* Für die folgenden Fehlertypen wird ein unvollständiger Ausführungseintrag mit automatischem Wiederholungsversuch gespeichert:

   * `ConnectionError`
   * `RateLimitError`
   * `OutOfSpaceError`
   * `ModuleTimeoutError`

* Für die folgenden Fehlertypen wird ein unvollständiger Ausführungseintrag ohne automatische Wiederholung gespeichert:

   * `DataError`
   * `InvalidConfigurationError`
   * `InvalidAccessTokenError`
   * `UnexpectedError`
   * `MaxFileSizeExceededError`
   * `MaxResultsExceededError`

* Bei allen anderen als den oben genannten Fehlertypen schlägt die Ausführung fehl.
