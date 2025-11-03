---
content-type: reference
title: Fehlertypen
description: Manchmal kann während der Ausführung eines Szenarios ein Fehler auftreten. Dies geschieht in der Regel, wenn ein Service aufgrund eines Fehlers bei der Verbindung zu einem Service nicht verfügbar ist oder wenn eine Validierung fehlschlägt. In diesem Artikel werden die häufigsten Fehler beschrieben, auf die Sie stoßen können.
author: Becky
feature: Workfront Fusion
exl-id: abf5f844-d13b-416e-a8b8-2d4ee1786262
source-git-commit: 99621f57da1eb294834a0eacfe527dcf017408e9
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 1%

---

# Fehlertypen

Manchmal kann während der Ausführung eines Szenarios ein Fehler auftreten. Dies geschieht normalerweise, wenn ein Service aufgrund eines Fehlers bei der Verbindung mit dem Service nicht verfügbar ist oder wenn eine Validierung fehlschlägt.

Adobe Workfront Fusion unterscheidet zwischen mehreren grundlegenden Fehlertypen. Der Fehlertyp bestimmt die nächsten Aktionen Ihres Fusionsszenarios.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++## Verbindungsfehler 

`ConnectionError`

Verbindungsfehler sind einer der häufigsten Fehler. Sie werden in der Regel durch die Nichtverfügbarkeit des Drittanbieterdienstes aus verschiedenen Gründen verursacht, z. B. Überlastung, Wartung oder Ausfall. Die Standardbehandlung dieses Fehlers hängt davon ab, bei welchem Modul der Fehler aufgetreten ist.

* Tritt der Fehler im ersten Modul auf, wird die Ausführung des Szenarios mit einer Warnmeldung beendet. Workfront Fusion versucht dann wiederholt, das Szenario in zunehmenden Zeitintervallen erneut auszuführen. Wenn alle Versuche fehlschlagen, deaktiviert Workfront Fusion das Szenario.
* Wenn der Verbindungsfehler auf einem anderen Modul als dem ersten auftritt, hängen die nachfolgenden Schritte von der Option Speichern unvollständiger Ausführungen zulassen in den erweiterten Einstellungen des Szenarios ab:

   * Wenn diese Option aktiviert ist, wird die Ausführung des Szenarios in den Ordner &quot;[!UICONTROL  Ausführungen“ verschoben] in dem Workfront Fusion wiederholt versucht, das Szenario in zunehmenden Zeitintervallen erneut auszuführen. Wenn alle Versuche fehlschlagen, verbleibt die Ausführung im Ordner Unvollständige Ausführungen, bis sie vom Benutzer manuell behoben wird.

     Weitere Informationen zu unvollständigen Ausführungen finden Sie unter [Anzeigen und Auflösen unvollständiger Ausführungen](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).
   * Wenn diese Option deaktiviert ist, endet die Ausführung des Szenarios mit einem Fehler und einer darauf folgenden Rollback-Phase. Workfront Fusion versucht dann wiederholt, das Szenario in zunehmenden Zeitintervallen erneut auszuführen. Wenn alle Versuche fehlschlagen, deaktiviert Workfront Fusion das Szenario.

  Weitere Informationen zur Einstellung Speichern unvollständiger Ausführungen zulassen finden Sie unter [Speichern unvollständiger Ausführungen zulassen](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions) im Artikel Konfigurieren von Szenario-Einstellungen.

### Zunehmende Zeitintervalle

Der Algorithmus zur Erhöhung der Zeitintervalle zwischen Versuchen, wenn ein Fehler auftritt, wird als exponentielles Backoff bezeichnet. Die zunehmenden Zeitintervalle werden wie folgt festgelegt:

1. 10 Minuten
1. 1 Stunde
1. 3 Stunden
1. 12 Stunden
1. 24 Stunden

Die zunehmenden Zeitintervalle verhindern, dass häufig ausgeführte Szenarien Vorgänge bei wiederholt fehlgeschlagenen Versuchen verwenden.

>[!BEGINSHADEBOX]

**Beispiel:**

Ein Szenario enthält den [!DNL Google Sheets] Trigger [!UICONTROL Zeilen ]. [!DNL Google Sheets] ist aufgrund von Wartungsarbeiten beim Starten von Workfront Fusion für 30 Minuten nicht verfügbar und kann daher keine neuen Zeilen abrufen. Das Szenario stoppt und versucht es in 10 Minuten erneut. Da [!DNL Google Sheets] immer noch nicht verfügbar ist, kann Workfront Fusion weiterhin keine Informationen zu neuen Zeilen abrufen. Die nächste Ausführung des Szenarios ist in 1 Stunde geplant. [!DNL Google Sheets] ist derzeit wieder verfügbar und das Szenario wird erfolgreich ausgeführt.

>[!ENDSHADEBOX]

## Datenfehler

`DataError`

Ein Datenfehler wird erzeugt, wenn ein Element falsch zugeordnet wird und die Validierung weder auf der Workfront Fusion-Seite noch auf der Seite des Drittanbieterdienstes erfolgreich durchläuft.

Tritt dieser Fehler auf, wird das Szenario, in dem das Modul fehlgeschlagen ist, in den Ordner „Unvollständige Ausführungen“ verschoben, wo Sie das Problem beheben können. Das Szenario stoppt jedoch nicht und wird weiterhin gemäß seinem Zeitplan ausgeführt. Um die Ausführung des Szenarios zu stoppen, wenn ein Datenfehler angezeigt wird, aktivieren Sie die Option Sequenzielle Verarbeitung im Bedienfeld „Szenario-Einstellungen“.

Wenn Sie die Option [!UICONTROL Speichern unvollständiger Ausführungen zulassen] in den Szenario-Einstellungen nicht aktiviert haben, wird die Ausführung des Szenarios mit dem Fehler beendet und ein Rollback durchgeführt.

## Fehler beim Duplizieren von Daten

`DuplicateDataError`

Wenn Workfront Fusion versucht, dasselbe Bundle zweimal in einen Service einzufügen, der keine doppelten Daten zulässt, wird ein Fehler mit doppelten Daten erzeugt. Tritt dieser Fehler auf, wird die Verarbeitung von Workfront Fusion auf die gleiche Weise durchgeführt wie bei dem Datenfehler.

Weitere Informationen finden Sie unter [Datenfehler](#data-error) in diesem Artikel.


## Fehler wegen ungültigem Zugriffs-Token

`InvalidAccessTokenError`

Ein Fehler mit einem ungültigen Zugriffstoken tritt auf, wenn Workfront Fusion nicht auf Ihr bei einem Drittanbieterdienst registriertes Konto zugreifen kann. Dies geschieht normalerweise, wenn Sie Zugriffsrechte für Workfront Fusion bei der Verwaltung eines bestimmten Services widerrufen. Szenarien, die diesen Service verwenden, werden jedoch weiterhin gemäß dem Zeitplan ausgeführt.

Wenn dieser Fehler auftritt, wird die Ausführung des Szenarios sofort gestoppt. Der Rest des Szenarios, das mit dem Modul beginnt, in dem der Fehler aufgetreten ist, wechselt zum Ordner „Unvollständige Ausführungen“.

## Fehler bei der Ratenbegrenzung

`RateLimitError`

Wenn ein von einem bestimmten Service festgelegtes Limit überschritten wird, wird ein Fehler bei der Ratenbeschränkung generiert. Tritt dieser Fehler auf, wird Workfront Fusion auf die gleiche Weise wie beim Verbindungsfehler fortgesetzt.

Weitere Informationen finden Sie unter [Verbindungsfehler](#connection-error) in diesem Artikel.

## Unvollständiger Datenfehler

`IncompleteDataError`

Ein unvollständiger Datenfehler tritt nur bei Triggern auf. Dieser Fehler wird generiert, wenn ein Trigger die erforderlichen Daten nicht von einem bestimmten Service herunterladen kann.

Wenn ein Szenario mit dem `IncompleteDataError` beendet wird, hängt sein weiteres Verhalten von der Einstellung [!UICONTROL Maximale Anzahl aufeinander folgender Fehler] ab.

Weitere Informationen finden Sie unter [Anzahl aufeinander folgender Fehler](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors) im Artikel Konfigurieren von Szenarioeinstellungen.

>[!BEGINSHADEBOX]

**Beispiel:**

In einem Szenario ist der Workfront-Trigger [!UICONTROL Datensatz ]) so eingestellt, dass auf Dokumente geachtet wird. Das Szenario wird ausgeführt, während Sie ein großes Dokument hochladen, z. B. ein langes Video. Da [!UICONTROL Workfront Fusion] versucht, das Video herunterzuladen, während es noch auf Workfront hochgeladen wird, endet das Szenario mit der `IncompleteDataError`.

>[!ENDSHADEBOX]

## Laufzeitfehler

`RuntimeError`

Fehler, die während der Ausführung des Szenarios auftreten und nicht zu diesen Fehlertypen gehören, werden als `RunTimeError` gemeldet.

Wenn ein Szenario mit dem `RuntimeError` beendet wird, hängt sein weiteres Verhalten von der Einstellung [!UICONTROL Maximale Anzahl aufeinander folgender Fehler] ab.

Weitere Informationen finden Sie unter [Anzahl aufeinander folgender Fehler](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors) im Artikel Konfigurieren von Szenarioeinstellungen.


>[!NOTE]
>
>Wenn ein Szenario mit einem sofortigen Trigger beginnt und auf diesen Fehler stößt, wird die Einstellung [!UICONTROL Maximale Anzahl aufeinander folgender Fehler] ignoriert und das Szenario wird sofort deaktiviert.
>>Weitere Informationen finden Sie unter [Instant Trigger](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers) im Artikel Module - Übersicht.

## Inkonsistenzfehler

`InconsistencyError`

Wenn einer dieser Fehler während der Commit- oder Rollback-Phase auftritt, wird das Szenario mit einem Inkonsistenzfehler beendet.

Wenn dieser Fehler in einem Szenario auftritt, wird die Ausführung des Szenarios sofort angehalten.

## Warnung

Während der Ausführung eines Szenarios erhalten Sie möglicherweise eine Warnung, die Sie über ein Problem informiert. Eine Warnung verhindert nicht, dass das Szenario erfolgreich abgeschlossen wird.

Beispielsweise kann eine Warnung angezeigt werden, wenn die maximal zulässige Dateigröße überschritten wird und die Option [!UICONTROL Datenverlust aktivieren] deaktiviert ist.

## Ressourcen

Weitere Informationen zur Zuordnung finden Sie unter [Zuordnungsübersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).

Informationen zu unvollständigen Ausführungen finden Sie unter [Anzeigen und Auflösen unvollständiger Ausführungen](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Weitere Informationen zum Bedienfeld „Szenarioeinstellungen“ finden Sie unter [Konfigurieren von Szenarioeinstellungen](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

Weitere Informationen zu Zeitplänen finden Sie unter [Planen eines Szenarios](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Informationen zu Szenario-Phasen finden Sie [Szenario-Ausführung, -Zyklen und -Phasen](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

Informationen zur Option Datenverlust aktivieren finden Sie unter [Datenverlust aktivieren](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) im Artikel Konfigurieren von Szenario-Einstellungen.
