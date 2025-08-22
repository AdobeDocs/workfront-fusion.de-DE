---
content-type: reference
title: Anweisungen für die Fehlerbehandlung
description: In diesem Artikel werden Anweisungen beschrieben, die Sie für die Fehlerbehandlung in Ihren Adobe Workfront Fusion-Szenarien verwenden können.
author: Becky
feature: Workfront Fusion
exl-id: d7b0141f-d99d-4ab7-a60f-ed552a76f05d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 15%

---

# Anweisungen für die Fehlerbehandlung

Mithilfe von Anweisungen zur Fehlerbehebung können Sie festlegen, was beim Auftreten eines Fehlers in einem Szenario geschieht.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz</td> 
   <td> Neu: Standard<p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion]-Lizenz</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Plan für [!UICONTROL Select] oder [!UICONTROL Prime] Workfront: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>[!UICONTROL Ultimate] Workfront-Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>


Wenden Sie sich an Ihren Workfront-Administrator, um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu Adobe Workfront Adobe Workfront Fusion finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Anweisungen für die Fehlerbehandlung

Die folgenden Anweisungen zur Fehlerbehandlung sind in Workfront Fusion verfügbar.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Rollback</p> <p> <img src="assets/rollback.png"> </p> </td> 
   <td> <ul><li><p>Die Ausführung des Szenarios wird sofort angehalten.</li><li>Eine Rollback-Phase wird für alle Module gestartet, um sie alle in den Ausgangszustand zurückzuversetzen. </li><li>Nachfolgende Module werden nicht verarbeitet.</p></li><li> <p>In den meisten Fällen wird das Szenario nach der Anzahl aufeinander folgender Fehler, die in den Szenario-Einstellungen angegeben sind, deaktiviert. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors" class="MCXref xref">Anzahl aufeinander folgender Fehler</a>.</p> </li><li><p>Der Ausführungsstatus des Szenarios wird als „Fehler“ markiert.</p></li></ul> <p><b>Hinweis</b>: Dies ist das Standardverhalten, wenn dem Modul keine Fehler-Handler-Route angehängt ist und die Einstellung <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions" class="MCXref xref">Speichern unvollständiger Ausführungen zulassen</a>Speichern unvollständiger Ausführungen zulassen unter [!UICONTROL Szenario-Einstellungen] nicht aktiviert ist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Zusichern</p> <p> <img src="assets/commit.png"> </p> </td> 
   <td> <ul><li><p>Die Ausführung des Szenarios wird sofort angehalten.</li><li>Eine Commit-Phase wird für alle Module gestartet. </li><li>Nachfolgende Module werden nicht verarbeitet.</p></li><li> <p>Alle nicht verarbeiteten Pakete werden ignoriert.</p> </li><li><p>Der Status der Szenarioausführung wird als „erfolgreich“ gekennzeichnet. </p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Wieder aufnehmen</p> <p> <img src="assets/resume.png"> </p> </td> 
   <td> <ul><li><p>Es wird eine Ersatzausgabe angegeben und an das Modul geliefert, bei dem ein Fehler auftritt.</p> </li><li><p>Nachfolgende Module werden verarbeitet.</p></li><li> <p>Der Status der Szenarioausführung wird als „erfolgreich“ gekennzeichnet.</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Ignorieren</p> <p> <img src="assets/ignore.png"> </p> </td> 
   <td><ul><li> <p>Der Fehler wird ignoriert.</li><li> Nachfolgende Module werden nicht verarbeitet.</p> </li><li><p>Wenn unbearbeitete Bündel vorhanden sind, wird die Ausführung des Szenarios normal fortgesetzt.</p> </li><li><p>Der Status der Szenarioausführung wird als „erfolgreich“ gekennzeichnet.</p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Unterbrechen</p> <p> <img src="assets/break.png"> </p> </td> 
   <td><ul><li> <p>Der Zustand der Szenarioausführung wird in der Warteschlange für unvollständige Ausführungen gespeichert, wo der Fehler manuell behoben werden kann. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md" class="MCXref xref">Anzeigen und Auflösen unvollständiger Ausführungen</a>.</p> <p>Es gibt jedoch einige Ausnahmen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow" class="MCXref xref">Speichern unvollständiger Ausführungen zulassen</a> im Artikel Konfigurieren von Szenario-Einstellungen</a>.</p></li><li> <p>Nachfolgende Module werden nicht verarbeitet.</p></li><li> <p>Wenn unbearbeitete Bündel vorhanden sind, wird die Ausführung des Szenarios normal fortgesetzt.</p> </li><li><p>Der Ausführungsstatus des Szenarios wird als „Warnung“ markiert, wenn die Option [!UICONTROL Ausführung automatisch abschließen] deaktiviert ist.</p></li></ul> <p>Weitere Informationen finden Sie im Abschnitt <a href="#break" class="MCXref xref">[!UICONTROL Break]</a> in diesem Artikel</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Erneut versuchen</p> <p> <img src="assets/retry.png"> </p> </td> 
   <td> <p>In einigen Fällen kann es nützlich sein, ein fehlerhaftes Modul erneut auszuführen, wenn die Wahrscheinlichkeit besteht, dass der Grund für den Fehler im Laufe der Zeit vergeht.</p> <p>Workfront Fusion bietet derzeit keine Wiederholungsrichtlinie an, obwohl mehrere Problemumgehungen verwendet werden können, um die Funktionalität nachzuahmen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/config-error-handling/retry.md" class="MCXref xref">Fehlerbehandlung bei erneuten Zustellversuchen</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Anweisungen zum Umgang mit Fehlern können nicht außerhalb einer Route zum Umgang mit Fehlern verwendet werden.
>* Workfront Fusion bietet derzeit kein Throw-Modul, mit dem Sie einfach bedingte Fehler (Throw-Fehler) erzeugen können, obwohl eine Problemumgehung eingesetzt werden kann, um seine Funktionalität nachzuahmen.
>
>  Weitere Informationen finden Sie unter [Konfigurieren `throw` Fehlerumgehung](/help/workfront-fusion/create-scenarios/config-error-handling/throw.md).

## Ressourcen

* Informationen zum Rollback und zur Rollback-Phase finden Sie unter [Rollback](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) im Artikel Szenario, Ausführungszyklen und Phasen .
* Informationen zur Commit-Phase finden Sie [Commit](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#commit) im Artikel Szenario, Ausführungszyklen und Phasen .
