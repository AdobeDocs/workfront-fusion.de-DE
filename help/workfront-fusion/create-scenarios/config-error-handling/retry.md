---
title: Konfigurieren einer Problemumgehung für die Verarbeitung von Wiederholungsfehlern
description: Manchmal ist es nützlich, ein fehlerhaftes Modul erneut auszuführen, wenn die Chance besteht, dass der Grund für den Fehler schnell behoben wird.
author: Becky
feature: Workfront Fusion
exl-id: 08e19a1a-7ca9-4c79-a165-f200048a5cda
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Problemumgehung für `retry` Fehlerbehandlung konfigurieren

Manchmal ist es nützlich, ein fehlerhaftes Modul erneut auszuführen, wenn die Chance besteht, dass der Grund für den Fehler schnell behoben wird.

Adobe Workfront Fusion bietet derzeit nicht die `retry`-Fehlerbehandlungsdirektive, es stehen jedoch zwei Problemumgehungen zur Verfügung, um die `retry`-Funktionalität nachzuahmen.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz</td> 
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Prime oder Workfront-Plan auswählen: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>Ultimate Workfront Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Problemumgehungen für die [!UICONTROL Wiederholen]-Fehlerbehandlungsanweisung

Workfront Fusion bietet derzeit nicht die `retry` Fehlerbehandlungsanweisung. Verwenden Sie eine der folgenden Problemumgehungen, um die Funktionalität für weitere Zustellversuche zu imitieren.

Anweisungen finden Sie unter [Anweisungen für die Fehlerbehandlung](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

* [Verwenden der Break-Direktive](#use-the-break-directive)
* [Verwenden des Repeater-Moduls](#use-the-repeater-module)

### Verwenden der Break-Direktive

Wenn die Break-Direktive ausgeführt wird, wird der Status der Szenario-Ausführung in der Warteschlange der unvollständigen Ausführungen gespeichert. In diesem Fall können Sie die unvollständige Ausführung manuell beheben.

Anweisungen finden Sie [Beheben von Fehlern, die von der Break-Direktive behandelt werden](/help/workfront-fusion/create-scenarios/config-error-handling/resolve-error-from-break-directive.md)

Anweisungen zum Beheben unvollständiger Ausführungen finden Sie unter [Anzeigen und Auflösen unvollständiger Ausführungen](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

#### Nachteile

* Das Mindestintervall für weitere Zustellversuche beträgt eine Minute.
* Wenn das Modul mehrere Bundles verarbeitet und die Verarbeitung eines Bundles fehlschlägt, wird die partielle Ausführung (nur das Bundle, das den Fehler verursacht hat) in den Ordner „Unvollständige Ausführungen“ verschoben und für weitere Zustellversuche gemäß den Einstellungen der [!UICONTROL break]-Anweisung geplant. Die aktuelle Ausführung wird jedoch fortgesetzt und das Modul verarbeitet weiterhin die nachfolgenden Bundles.

  Um zu verhindern, dass das Szenario erneut ausgeführt wird, bis die im Ordner „Unvollständige Ausführungen“ gespeicherte Ausführung erfolgreich aufgelöst wurde, aktivieren Sie die Option &quot;[!UICONTROL Sequenzielle Verarbeitung]&quot; in den [!UICONTROL Szenario-Einstellungen].

Weitere Informationen zu unvollständigen Ausführungen finden Sie unter [Anzeigen und Auflösen unvollständiger Ausführungen](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

### Verwenden des Repeater-Moduls

Die Problemumgehung für das Repeater-Modul ist komplexer, kann aber besser angepasst werden.

#### Konfigurieren der Fehler-Handler-Route

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie die Problemumgehung hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf das **Flusssteuerung**-Symbol ![Flusssteuerung](assets/flow-control-icon.png) und wählen Sie **Repeater** aus.
1. Legen Sie im Repeater-Modul für das **[!UICONTROL Wiederholungen]** die maximale Anzahl der Wiederholungen für das Szenario fest.
1. Schließen Sie das potenziell fehlerhafte Modul nach dem **[!UICONTROL Repeater]** an.
1. Hängen Sie eine Fehler-Handler-Route an das Modul mit dem potenziellen Fehler an.

   Anweisungen finden Sie unter [Fehlerbehandlung hinzufügen](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md).
1. Fügen Sie das Modul **[!UICONTROL Tools] > [!UICONTROL Sleep]** zur Fehler-Handler-Route hinzu und legen Sie **[!UICONTROL Feld Verzögerung]** auf die Anzahl der Sekunden zwischen den Wiederholungsversuchen fest.

1. Fügen Sie die Direktive **[!UICONTROL Ignore]** nach dem Modul **[!UICONTROL Tools] > [!UICONTROL Sleep]** hinzu.
1. Fahren Sie [Konfigurieren der Standardroute](#configure-the-default-route) fort.

#### Konfigurieren der Standardroute

1. Fügen Sie das Modul **[!UICONTROL Tools] > [!UICONTROL Variable festlegen]** in einer separaten Route (kein Fehler-Handler) nach dem potenziell fehlerhaften Modul hinzu und konfigurieren Sie es so, dass das Ergebnis des Moduls in einer Variablen namens gespeichert wird, z. B. `Result`.

1. Fügen Sie das Modul **[!UICONTROL Array]** nach **[!UICONTROL Tools] > [!UICONTROL Variable festlegen]** hinzu und wählen Sie das Modul **[!DNL Repeater]** in seinem Feld Source-Modul aus.

1. Fügen Sie das Modul **[!UICONTROL Tools] > [!UICONTROL Variable abrufen]** nach dem Modul **[!UICONTROL Array-Aggregator]** hinzu und ordnen Sie ihm den Wert der `Result`-Variablen zu.

1. Fügen Sie das Modul **[!UICONTROL Tools] > [!UICONTROL GET variable]** zwischen dem **[!UICONTROL Repeater]**-Modul und dem möglicherweise fehlerhaften Modul ein und ordnen Sie ihm den Wert der `Result`-Variable zu.

1. Fügen Sie einen Filter zwischen diesem Modul **[!UICONTROL Tools] > [!UICONTROL Variable abrufen]** und dem Modul ein, das möglicherweise fehlschlägt, und fahren Sie nur fort, wenn die `Result` nicht vorhanden ist.

>[!BEGINSHADEBOX]

**Beispiel:**

In diesem Beispielszenario stellt das Modul [!UICONTROL HTTP] > [!UICONTROL Anfrage stellen] das Modul dar, das möglicherweise fehlschlägt:

![HTTP-Anfrage stellen](assets/http-make-request.png)

>[!ENDSHADEBOX]

Wenn das Ergebnis des potenziell fehlschlagenden Moduls zu komplex ist, um in einer einfachen Variablen gespeichert zu werden, können Sie einen Datenspeicher verwenden, um das Ergebnis zu speichern und abzurufen. Der Datenspeicher würde nur einen Datensatz enthalten. Der Schlüssel des Datensatzes kann beispielsweise `Result` sein.

Weitere Informationen zu Datenspeichern finden Sie unter [Datenspeicher](/help/workfront-fusion/create-scenarios/map-data/data-stores.md).

#### Nachteile

* Diese Problemumgehung ist komplexer.
* Diese Problemumgehung erfordert mehr Vorgänge.

## Ressourcen

* Weitere Informationen zu Repeater-Modulen und Break-Anweisungen finden Sie unter [Flusskontrolle](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/flow-control.md).
* Weitere Informationen zum Abrufen von Variablenmodulen finden Sie unter [Tools](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/tools-modules.md).
