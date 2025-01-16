---
title: Anzeigen und Auflösen unvollständiger Ausführungen
description: Der Ordner [!UICONTROL Incomplete executions] speichert Szenario-Ausführungen, die aufgrund eines Fehlers nicht erfolgreich abgeschlossen wurden. Jede gespeicherte unvollständige Ausführung kann entweder manuell oder automatisch aufgelöst werden.
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
source-git-commit: 3d06958b6f706f4f974230853fb6553232656fd3
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 6%

---

# Anzeigen und Auflösen unvollständiger Ausführungen

Der Ordner [!UICONTROL Incomplete executions] speichert Szenario-Ausführungen, die aufgrund eines Fehlers nicht erfolgreich abgeschlossen wurden. Jede gespeicherte unvollständige Ausführung kann entweder manuell oder automatisch aufgelöst werden.

>[!NOTE]
>
>Standardmäßig ist das Speichern unvollständiger Ausführungen deaktiviert. Um sie zu aktivieren, aktivieren Sie die Option [!UICONTROL Allow storing incomplete executions] in den erweiterten Einstellungen des Szenarios.
>
>Weitere Informationen zu Szenario-Einstellungen finden Sie unter [Konfigurieren von Szenario-Einstellungen](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Packstück</td> 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz</td> 
   <td> <p>Neu: [!UICONTROL Standard]</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuell: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>[!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Workfront]: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein [!DNL Workfront Fusion]-Administrator für Ihre Organisation sein.</p>
     <p>Sie müssen [!DNL Workfront Fusion] für Ihr Team sein.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Anzeigen unvollständiger Ausführungen

Wenn bei einem Modul während seines Vorgangs ein Fehler auftritt, wird eine neue unvollständige Ausführung zum Ordner Unvollständige Ausführungen hinzugefügt. Jede unvollständige Ausführung enthält den Blueprint des Szenarios und alle Bundles, die dem fehlgeschlagenen Modul zugeordnet werden können. Die Liste der unvollständigen Ausführungen kann durch Klicken auf die Registerkarte [!UICONTROL Incomplete Executions] auf der Seite mit den Szenario-Details geöffnet werden.

<!--

![](assets/incomplete-executions-tab-350x102.png)

-->

Weitere Informationen finden Sie unter [Fehler, die zu unvollständigen Ausführungen führen](#errors-resulting-into-incomplete-executions) in diesem Artikel.

>[!NOTE]
>
>Die aktuelle Größenbeschränkung des nicht aufgelösten Ordners „Unvollständige Ausführungen“ pro Organisation beträgt 500 MB. Wenn Ihre Organisation dieses Limit überschreitet, wird möglicherweise der folgende Fehler angezeigt:
>
>`"There is NOT ENOUGH SPACE to add a bundle to the IEQ. The reason is: Too many incomplete executions."`
>
>Weitere Informationen finden Sie unter [Datenverlust aktivieren](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) im Artikel Konfigurieren von Szenario-Einstellungen.


## Beheben von unvollständigen Ausführungen über die Registerkarte Unvollständige Ausführungen

Wenn eine neue unvollständige Ausführung gespeichert wird, können Sie sie wie folgt auflösen:

1. Öffnen Sie das betroffene Szenario.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Incomplete Executions]** .
1. Suchen Sie die unvollständige Ausführung, die Sie auflösen möchten, und klicken Sie auf **[!UICONTROL Details]**.


## Beheben von unvollständigen Ausführungen über die Registerkarte Verlauf

Wenn Sie das Protokoll aller Modulvorgänge anzeigen möchten, bevor Sie versuchen, die unvollständige Ausführung zu beheben, können Sie die unvollständige Ausführung über den [!UICONTROL History] Ordner auflösen:

1. Öffnen Sie das betroffene Szenario.
1. Klicken Sie auf die Registerkarte **[!UICONTROL History]** .
1. Suchen Sie nach der fehlgeschlagenen Ausführung des Szenarios und klicken Sie auf **[!UICONTROL Details]**.
1. Öffnen Sie das Protokoll des Moduls, in dem alle Vorgänge des Moduls angezeigt werden.
1. Suchen Sie den fehlgeschlagenen Vorgang und klicken Sie auf **[!UICONTROL Resolve]**:

   ![](assets/resolve-btn-350x188.png)

## Optionen im Zusammenhang mit unvollständigen Ausführungen

Die folgenden Optionen im [!UICONTROL Scenario settings] bestimmen, ob und wie die unvollständigen Ausführungen gespeichert werden:

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

* Wenn der Fehlertyp `ConnectionError`, `RateLimitError`, `OutOfSpaceError` oder `ModuleTimeoutError` ist, wird ein unvollständiger Ausführungseintrag mit automatischem Wiederholungsversuch gespeichert.
* Wenn der Fehlertyp `DataError`, `InvalidConfigurationError`, `InvalidAccessTokenError`, `UnexpectedError`, `MaxFileSizeExceededError` oder `MaxResultsExceededError` lautet, wird ein unvollständiger Ausführungsdatensatz ohne automatische Wiederholung gespeichert.
* Bei allen anderen als den oben genannten Fehlertypen schlägt die Ausführung fehl.
