---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Erstellen eines Basisszenarios
description: Erfahren Sie, wie Sie mit Adobe Workfront Fusion ein einfaches Automatisierungsszenario erstellen. Automatisierungsszenarien automatisieren Workfront-Prozesse, einschließlich Datenmanipulationen und -umwandlungen. Dieses Beispiel führt Sie durch den Prozess der Erstellung eines Szenarios, das in Workfront nach einer  [!DNL Workfront]  sucht und sie dann in ein Projekt konvertiert.
author: Becky
feature: Workfront Fusion
exl-id: 5284dee1-e890-4357-a28d-29e09ac02822
source-git-commit: 8884aef2237ad358c774110b81ac17b9efb386d4
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 1%

---

# Erstellen eines Basisszenarios

Die Rolle von [!DNL Adobe Workfront Fusion] besteht darin, Ihre Prozesse zu automatisieren, damit Sie sich auf neue Aufgaben konzentrieren können, anstatt dieselben Aufgaben immer wieder zu wiederholen. Es funktioniert durch die Verknüpfung von Aktionen innerhalb und zwischen Apps und Services, um ein Szenario zu erstellen, das Ihre Daten automatisch überträgt und transformiert. Das Szenario, in dem Sie Daten in einer App oder einem Service erstellen, überwacht und verarbeitet diese Daten, um das gewünschte Ergebnis zu liefern.

In diesem Beispiel wird erläutert, wie Sie ein Szenario erstellen, in dem in Workfront nach einer Anfrage gesucht und diese in ein Projekt konvertiert wird.

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
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++



## Erstellen eines Übungsszenarios

### Erstellen des Szenarios

1. Klicken Sie **Bereich &quot;**&quot; auf **Neues Szenario erstellen**.

   Informationen zum Auffinden des Bereichs „Szenarien“ finden Sie unter [Navigieren in Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/navigate-workfront-fusion.md).

   Der Szenario-Editor wird angezeigt, wobei in der Mitte ein leeres Modul enthalten ist.

1. Wählen Sie oben links den **[!UICONTROL New scenario]** Platzhalternamen aus und geben Sie dann einen Namen ein.
1. Fahren Sie mit [Hinzufügen und konfigurieren Sie das erste Modul](#add-and-configure-the-first-module) fort.

### Hinzufügen und Konfigurieren des ersten Moduls

1. Klicken Sie auf das leere Modul, um die App auszuwählen, aus der Sie ein Modul auswählen möchten.

   Rechts neben dem Modul wird eine Liste mit Apps angezeigt.

1. Wählen Sie **[!DNL Adobe Workfront]** aus. Wenn es nicht sichtbar ist, klicken Sie unten in der Liste auf die Suchleiste, geben Sie &quot;Workfront&quot; ein und wählen Sie es aus, wenn es in der Liste angezeigt wird.

   Die Liste ändert sich und zeigt alle [!DNL Workfront] Module an, die Sie verwenden können.

1. Klicken Sie auf das **[!UICONTROL Search]**.

   Das Fenster für die Modulkonfiguration wird geöffnet.

1. Wählen Sie im [!UICONTROL Connection] Ihre Workfront-Verbindung aus.

   Wenn Sie keine Workfront-Verbindung haben, lesen Sie [Verbindung erstellen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)
1. Wählen Sie im [!UICONTROL Record Type] die Option **[!UICONTROL Issue]** aus. Dadurch wird das Modul so eingerichtet, dass nur Probleme gesucht werden, darunter auch Anfragen.

   Sie finden **[!UICONTROL Issue]** in der Liste, wenn Sie mit der Eingabe des Wortes &quot;[!UICONTROL Issue]&quot; beginnen.

1. Wählen Sie im **[!UICONTROL Result Set]** die Option **[!UICONTROL First Matching Record]** aus.

   Dadurch wird das Modul so eingestellt, dass nur der erste gefundene Datensatz zurückgegeben wird, der die Kriterien erfüllt.
1. Konfigurieren Sie im Bereich **[!UICONTROL Search criteria]** die Kriterien, um die spezifische Aufgabe zurückzugeben.

   1. Wählen Sie im ersten Feld unter [!UICONTROL Search Criteria] das Feld aus, das Sie in Ihre Suche einbeziehen möchten. Wählen Sie für dieses Beispiel **[!UICONTROL Name]** aus.

      Sie finden **[!UICONTROL Name]** in der Liste, wenn Sie mit der Eingabe des Wortes &quot;[!UICONTROL name]&quot; beginnen.
   1. Klicken Sie für den -Operator auf den Dropdown-Pfeil neben **Vorhanden** und ändern Sie ihn in [!UICONTROL **Enthält (ignoriert Groß-/Kleinschreibung)**].

      Auf diese Weise kann das Modul Projekte mit den ausgewählten Wörtern im Namen finden, auch wenn Sie nicht den gesamten Namen oder nur die falsche Groß-/Kleinschreibung (z. B. alle Großbuchstaben) eingeben.
   1. Geben Sie im letzten Feld unter [!UICONTROL Search Criteria] ein Wort oder eine Phrase ein, von dem bzw. der Sie wissen, dass es/sie im Namen der Aufgabe ist, nach der Sie suchen.

1. Wählen Sie in der Liste **[!UICONTROL Outputs]** die Felder aus, die vom Modul ausgegeben werden sollen. Wählen Sie für dieses Beispiel die Felder **[!UICONTROL ID]** und **[!UICONTROL Name]** aus.

   >[!TIP]
   >
   >Sie können **Befehlstaste+F** ([!DNL Mac] OS) oder **Strg+F** ([!DNL Windows] OS) verwenden, um ein Feld schnell zu finden.

1. Klicken Sie auf **[!UICONTROL OK]** , um die Modulkonfiguration zu speichern.

1. Klicken Sie mit der rechten Maustaste auf das Modul, klicken Sie auf **[!UICONTROL Rename]**, geben Sie dann einen Namen ein, der beschreibt, was das Modul tun soll (z. B. „Nach Anfragen suchen„), und klicken Sie dann auf **[!UICONTROL OK]**.

   Der Name wird direkt unter dem Modul angezeigt. Darunter finden Sie [!DNL Workfront Fusion] kurze Beschreibung der Art der Aktion, die vom Modul ausgeführt wird.

   ![](assets/module-renamed-wf.png)

1. Fahren Sie mit [Hinzufügen und konfigurieren Sie das zweite Modul](#add-and-configure-the-second-module) fort.

## Hinzufügen und Konfigurieren des zweiten Moduls

1. Bewegen Sie den Mauszeiger über den Teilkreis rechts neben dem Modul und klicken Sie dann auf **[!UICONTROL Add another module]**.
1. Wählen Sie [!DNL Adobe Workfront] aus der Liste der Programme und dann die **[!UICONTROL Convert object]** aus.
1. Wählen Sie im Feld [!UICONTROL Connection] dieselbe Workfront-Verbindung aus, die Sie im vorherigen Modul verwendet haben.
1. Wählen Sie im Feld **[!UICONTROL Record type]** die Option **[!UICONTROL issue]** aus, da das Modul ein Problem konvertieren wird.
1. Wählen Sie im Feld **[!UICONTROL Convert to]** die Option **Projekt** aus.
1. Klicken Sie neben dem Feld Aufgaben-ID auf den Umschalter Zuordnung , um es zu aktivieren.

   Der Umschalter wird blau, wenn er aktiviert ist. Auf diese Weise können Sie die Aufgaben-ID aus dem vorherigen Modul zuordnen.

   ![Umschalter für Zuordnung](assets/map-toggle.png)
1. Klicken Sie auf das Feld **[!UICONTROL Task ID]** .

   Es öffnet sich ein Bedienfeld, in dem Sie auswählen können, was als ID der Aufgabe verwendet werden soll, die Sie in ein Projekt konvertieren möchten. Da Sie die Zuordnung aktiviert haben, enthält das Bedienfeld Ausgaben aus allen vorherigen Modulen. Sie haben ID als Ausgabe des vorherigen Moduls ausgewählt, sodass es jetzt im Bedienfeld verfügbar ist.

   Dieses Bedienfeld wird als Zuordnungs-Bedienfeld bezeichnet. Weitere Informationen zum Zuordnungsbereich finden Sie unter [Zuordnungsübersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).
1. Wählen **ID** im Zuordnungsbereich aus.

   Im Feld ID wird ein ID-Block angezeigt. Es zeigt die Nummer des Moduls, dem es zugeordnet ist, und das Feld, das zugeordnet ist.

   ![Map ID](assets/map-id.png)

1. Klicken Sie auf das **Vorlagen** ID), geben Sie den Namen der Workfront-Vorlage ein, die Sie für dieses Projekt verwenden möchten, und wählen Sie sie aus, wenn sie in der Liste angezeigt wird.
1. Klicken Sie auf **[!UICONTROL OK]** , um die Modulkonfiguration zu speichern.

1. Klicken Sie mit der rechten Maustaste auf das Modul, klicken Sie auf **[!UICONTROL Rename]**, geben Sie dann einen Namen ein, der beschreibt, was das Modul tun soll (z. B. „In Projekt konvertieren„), und klicken Sie dann auf **[!UICONTROL OK]**.

1. Fahren Sie mit [Testen des Szenarios](#test-the-scenario) fort.

## Testen des Szenarios

Bevor Sie Ihr Szenario aktivieren, müssen Sie es testen, indem Sie es mindestens einmal ausführen und die Ergebnisse anzeigen. Auf diese Weise können Sie verstehen, wie Daten durch das Szenario fließen, und Fehler finden.

Bei diesem Szenario würde ein erfolgreicher Test dazu führen, dass die Anfrage gefunden und in ein Projekt konvertiert wird.

1. Klicken Sie in der linken unteren Ecke des Szenario-Editors auf **[!UICONTROL Run once]** .
1. Klicken Sie nach der Ausführung des Szenarios auf die Blase über dem ersten Modul, um Informationen über das vom Modul verarbeitete Datenpaket anzuzeigen, einschließlich der Daten, die aus der vom Modul zurückgegebenen Anfrage abgerufen wurden.

1. Klicken Sie auf die Blase „Ausführungs-Inspektor“ über dem zweiten Modul, um die Eingabe (die Anfrage) und die Ausgabe (das konvertierte Projekt) anzuzeigen.

   Weitere Informationen zu den Daten in den Inspektionsblasen finden Sie unter:

   * Allgemeine Informationen finden Sie unter [Ausführungsfluss von Szenarien](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Informationen zu verarbeiteten Bundles finden Sie unter [Szenarioausführung, Zyklen und Phasen](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. Klicken Sie [!DNL Workfront Fusion] unten links auf **[!UICONTROL Save]** , um den Fortschritt des Szenarios zu speichern.

   >[!IMPORTANT]
   >
   >Speichern Sie häufig, während Sie ein Szenario verfeinern und testen.

>[!TIP]
>
>Wir empfehlen die optionale, aber nützliche Vorgehensweise, Hinweise zu jedem Modul hinzuzufügen.
>
>1. Klicken Sie mit der rechten Maustaste auf ein Modul und wählen Sie **[!UICONTROL Add a note]**.
>1. Geben Sie in der angezeigten Anmerkung eine Übersicht für das Modul ein.
>
>    Sie können mehrere Notizen für ein Modul hinzufügen.
>
>1. Schließen Sie den **[!UICONTROL Notes]**.
>
>     Nachdem Sie einem Szenario eine Anmerkung hinzugefügt haben, wird auf dem **[!UICONTROL Notes]** unten im Szenario-Editor ein orangefarbener Punkt ![](assets/notes-icon-w-dot.png).
>
>1. Klicken Sie auf das **[!UICONTROL Notes]** Symbol ![](assets/notes-icon-w-dot.png) , um Ihre Notizen anzuzeigen.
>

## Aktivieren des Szenarios

Der letzte Schritt beim Erstellen eines Szenarios besteht darin, es zu aktivieren.

Da dieses Szenario nach einem bestimmten Problem sucht, ist es nicht erforderlich, es zu aktivieren. Durch die Aktivierung eines Szenarios wird es nach einem Zeitplan ausgeführt oder wenn eine bestimmte Aktion in einem Programm stattfindet. Nachdem Sie ein Szenario aktiviert haben, wird es standardmäßig alle 15 Minuten ausgeführt. Sie können dies ändern, indem Sie festlegen, wann und wie oft die Ausführung erfolgen soll.

Weitere Informationen zum Aktivieren von Szenarien finden Sie unter [Aktivieren oder Deaktivieren eines Szenarios](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).

Weitere Informationen zu Zeitplänen finden Sie unter [Planen eines Szenarios](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Nächste Schritte

* [Ein Trigger-Modul hinzufügen](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md), damit das Szenario regelmäßig nach neuen Anfragen suchen und sie in Projekte konvertieren kann.
* [Webhook hinzufügen](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) damit das Szenario jedes Mal ausgeführt werden kann, wenn eine Anfrage eingegeben wird.
* [Filter hinzufügen](/help/workfront-fusion/build-practice-scenarios/add-filter-basic-scenario.md) um sicherzustellen, dass nur bestimmte Anfragen in Projekte konvertiert werden.
* [Funktion hinzufügen](/help/workfront-fusion/build-practice-scenarios/use-function-to-build-practice-scenario.md) die den Namen des neuen Projekts anpasst.
