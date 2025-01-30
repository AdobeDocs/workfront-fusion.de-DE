---
title: Anzeigen und Auflösen unvollständiger Ausführungen
description: Der Ordner [!UICONTROL Incomplete executions] speichert Szenario-Ausführungen, die aufgrund eines Fehlers nicht erfolgreich abgeschlossen wurden. Jede gespeicherte unvollständige Ausführung kann entweder manuell oder automatisch aufgelöst werden.
author: Becky
feature: Workfront Fusion
exl-id: 974b32b4-d86a-48cd-a8d4-1ae2cf309b9b
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Anzeigen des Ausführungsverlaufs eines Szenarios

Sie können Informationen zu den Ereignissen oder Ausführungen eines Szenarios anzeigen oder alle Ausführungen des Szenarios nach bestimmten Daten durchsuchen.

Eine Szenario-Ausführung stellt eine einzelne Ausführung des Szenarios dar.

Ein Szenarioereignis ist eine Änderung des Szenarios, z. B. das Bearbeiten, Aktivieren oder Deaktivieren.

>[!NOTE]
>
>Im Verlauf eines Szenarios werden alle Ereignisse und Ausführungen eines Szenarios in den letzten 30 Tagen angezeigt.

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

## Szenarioverlauf anzeigen


### Szenarioverlauf auf der Registerkarte Verlauf anzeigen

Die Registerkarte [!UICONTROL History] zeigt mehr Details an, als auf der Seite [!UICONTROL Scenario detail] verfügbar sind. Sie können die Ausführungen auch auf der Registerkarte [!UICONTROL History] filtern und sortieren.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Scenario]** im linken Bereich und dann auf das Szenario.

   Oder

   Wenn Sie das Szenario im Szenario-Editor bearbeiten, klicken Sie auf den Pfeil nach links ![Pfeil zum Beenden der Bearbeitung](assets/exit-editing-arrow.png) in der oberen linken Ecke des Fensters.

1. Klicken Sie **Verlauf** neben dem Namen des Szenarios.
   ![Registerkarte „Verlauf“](assets/history-tab.png)

   Die folgenden Details werden für jede Ausführung des Szenarios aufgelistet:

   * Datum, an dem der Durchgang **[!UICONTROL Started]** wurde
   * Ausführungs-ID
   * **[!UICONTROL Status]** (Erfolg oder Fehlgeschlagen)
   * **[!UICONTROL Duration]** ausführen
   * Anzahl **[!UICONTROL Operations]**
   * Größe der **[!UICONTROL Data Transfer]**

   >[!NOTE]
   >
   >Der Szenarioverlauf zeigt neben **kürzlich ausgeführten Szenarien** Badge Verarbeitung an, während die Ausführungsdetails in den Speicher geschrieben werden. Die Verarbeitung erfolgt unmittelbar nach der Ausführung des Szenarios. und sollte nicht länger als ein paar Minuten dauern. Details zur Szenario-Ausführung sind während der Ausführung möglicherweise nicht sichtbar.

1. Um Details für eine bestimmte Szenario-Ausführung anzuzeigen, klicken Sie **ganz** auf „Details“. Der [!UICONTROL details] Link ist nur sichtbar, wenn für die Ausführung Details verfügbar sind.
1. Um Ereignisse anzuzeigen, schalten Sie **Ereignisse anzeigen** ein.


### Anzeigen des Szenario-Verlaufs auf der Seite mit den Szenario-Details


1. Klicken Sie auf die Registerkarte **[!UICONTROL Scenario]** im linken Bereich und dann auf das Szenario.

   Oder

   Wenn Sie das Szenario im Szenario-Editor bearbeiten, klicken Sie auf den Pfeil nach links ![Pfeil zum Beenden der Bearbeitung](assets/exit-editing-arrow.png) in der oberen linken Ecke des Fensters.

1. Klicken Sie auf die Registerkarte **[!UICONTROL History]** im rechten Bedienfeld.
1. (Optional) Klicken Sie auf die Ausführung im rechten Bedienfeld, um detaillierte Informationen zu einer ausgewählten Szenario-Ausführung zu erhalten.

   Weitere Informationen zur Verarbeitung von Bundles finden Sie unter [Ausführungsablauf für Szenarien](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)

   >[!NOTE]
   >
   >* Der Szenarioverlauf zeigt neben Szenarien **die kürzlich ausgeführt wurden,** Badge „Verarbeitungsverlauf“ an, während die Ausführungsdetails in den Speicher geschrieben werden. Die Verarbeitung erfolgt unmittelbar nach der Ausführung des Szenarios. und sollte nicht länger als ein paar Minuten dauern. Details zur Szenario-Ausführung sind während der Ausführung möglicherweise nicht sichtbar.

1. Um Ereignisse anzuzeigen, klicken Sie auf die Registerkarte **Ereignisse**.

## Filtern des Ausführungsverlaufs des Szenarios

Sie können den Ausführungsverlauf filtern, um nur Ausführungen mit den angegebenen Werten anzuzeigen.

1. Öffnen Sie den vollständigen Seitenverlauf für ein Szenario, wie in [Szenario-Ausführungsverlauf auf der Registerkarte [!UICONTROL History] anzeigen](#view-scenario-history-on-the-history-tab) in diesem Artikel beschrieben.
1. Klicken Sie in der Kopfzeile der Spalte![ nach ](assets/fusion-scenario-filter-icon.png) Sie filtern möchten, auf das [!UICONTROL filter]-Symbol (Szenariofiltersymbol).
1. Geben Sie im Dialogfeld [!UICONTROL filter] die Werte ein, nach denen Sie filtern möchten.
1. Klicken Sie auf **[!UICONTROL Save]**.

Das Filtersymbol ist in Spalten mit einem aktiven Filter orange.

<!-- don't see how to do this
## Sort the scenario execution history

You can sort the scenario execution history.

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-execution-history-on-the-history-tab) in this article.
1. Click the [!UICONTROL Sort] icon in the header of the column you want to filter by.
1. Optional: To reverse the order of the sort, click the [!UICONTROL Sort] icon again.
-->

## Alle Ausführungen eines Szenarios durchsuchen

1. Öffnen Sie den vollständigen Seitenverlauf für ein Szenario, wie in [Szenario-Ausführungsverlauf auf der Registerkarte [!UICONTROL History] anzeigen](#view-scenario-history-on-the-history-tab) in diesem Artikel beschrieben.
1. Klicken Sie oben in der Liste der Ausführungen auf **[!UICONTROL Fulltext search]** .

   Oder

   Geben Sie **Strg+Umschalt+F** (Windows) oder **Befehl+Umschalt+F** (Mac) ein
Das [!UICONTROL Search in history] wird geöffnet.

1. (Optional) Um nach Ausführungen zu suchen, die bestimmten Text enthalten, geben Sie den Text in der Suchleiste des **[!UICONTROL Search in history]** ein.

   Um nach exaktem Text zu suchen, setzen Sie den Text in Anführungszeichen („Beispiel„).

   >[!INFO]
   >
   >**Beispiel:** Wenn Sie die Ausführung finden möchten, mit der ein bestimmtes Projekt erstellt wurde, geben Sie die Projekt-ID in die [!UICONTROL Fulltext search] ein.
   >
   >„625ef2ef0006036bd1794b6e52d737c5“

1. (Optional) Um die Suche nach Datumsbereich zu beschränken, wählen Sie das Anfangs- und Enddatum der gewünschten Suche im [!UICONTROL By date range] aus.

   >[!NOTE]
   >
   >* Ausführungen sind nur für die letzten 30 Tage verfügbar.
   >
   >* [!DNL Workfront Fusion] speichert Webhook-Payloads 30 Tage lang. Der Zugriff auf eine Webhook-Payload mehr als 30 Tage nach der Erstellung führt zum Fehler &quot;[!UICONTROL Failed to read file from storage.]&quot;


1. (Optional) Um die Suche nach Status zu begrenzen, wählen Sie den gewünschten Status in der Dropdown-Liste **[!UICONTROL By status]** aus.


   Verfügbare Status sind:

   * [!UICONTROL All]

   * [!UICONTROL Error]

   * [!UICONTROL Warning]

   * [!UICONTROL Success]

1. (Optional) Ändern Sie die Reihenfolge, in der die Ergebnisse im Dropdown-Menü **[!UICONTROL Sort by dates]** angezeigt werden.

1. (Optional) Um eine Szenario-Ausführungs-ID zu kopieren, klicken Sie auf das Symbol **[!UICONTROL Copy execution ID]** . <img src="assets/copy-fusion-execution-id-icon.png"> in der Zeile der gewünschten Ausführung.

1. (Optional) Klicken Sie auf ein Ergebnis der [!UICONTROL Fulltext search], um das Ausgabebundle des Szenario-Moduls zu untersuchen, das die Informationen enthält.
