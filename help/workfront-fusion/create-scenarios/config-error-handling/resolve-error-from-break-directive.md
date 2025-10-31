---
title: Beheben von Fehlern, die von der Break-Direktive behandelt werden
description: Manchmal ist es nützlich, ein fehlerhaftes Modul erneut auszuführen, wenn die Chance besteht, dass der Grund für den Fehler schnell behoben wird.
author: Becky
feature: Workfront Fusion
exl-id: d568942c-2cd5-430c-bdbf-e1496da25b50
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Beheben von Fehlern, die von der Break-Direktive behandelt werden

Wenn ein Fehler von der Break-Direktive verarbeitet wird, wird im Ordner Unvollständige Ausführungen ein Datensatz erstellt. Dieser Datensatz speichert den Status der Szenario-Ausführung zusammen mit Daten aus den vorherigen Modulen. Der Datensatz verweist auf das Modul, von dem der Fehler stammt, und enthält Informationen zu den Daten, die vom Modul als Eingabe empfangen wurden. Für jedes Datenbündel, das den Fehler verursacht, wird ein separater Datensatz erstellt.

Weitere Informationen finden Sie unter [Anzeigen und Auflösen unvollständiger Ausführungen](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

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

+++

## Beheben von Fehlern, die sich aus der Break-Direktive ergeben

Sie können den Fehler manuell beheben, indem Sie das Szenario (falls erforderlich) aktualisieren und es einmal ausführen.

Sie können das Szenario auch so konfigurieren, dass eine unvollständige Ausführung automatisch verarbeitet wird, indem Sie das Szenario erneut ausführen. So konfigurieren Sie das Modul für die Verarbeitung unvollständiger Ausführungen:

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie die Problemumgehung hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf das **Fluss**-Symbol ![Fluss](assets/flow-control-icon.png) und wählen Sie **Break** aus.
1. Aktivieren Sie innerhalb des Moduls break die Option [!UICONTROL **Ausführung automatisch abschließen**].
1. Geben **im Feld „Anzahl der**&quot; die maximale Anzahl der Versuche ein, für die das Modul die Ausführung wiederholen soll, oder mappen Sie sie

   Diese Zahl muss zwischen 1 und 100 liegen.
1. Geben **im Feld „Intervall zwischen**&quot; die Anzahl der Minuten zwischen den einzelnen Wiederholungsversuchen ein oder mappen Sie sie.

Wenn diese Option aktiviert ist, wird bei einem Fehler die unvollständige Ausführung abgerufen (nach der im Feld [!UICONTROL Intervall zwischen Versuchen] angegebenen Zeit) und mit den ursprünglichen Eingabedaten ausgeführt. Dies wird wiederholt, bis die Ausführung des Moduls fehlerfrei abgeschlossen wird oder die angegebene Anzahl von Versuchen erreicht ist.

>[!NOTE]
>
>Wenn der erste Wiederholungsversuch fehlschlägt, erhöht sich das Intervall zwischen den Wiederholungsversuchen exponentiell bei jedem zweiten Versuch.


Wenn die Option Ausführung automatisch abschließen aktiviert ist, wird die Ausführung des Szenarios als „Erfolg“ markiert, da der automatische Wiederholungsversuch des Fehler-Handlers das Problem automatisch behebt. In diesem Fall erhalten Benutzerinnen und Benutzer keine E-Mail über die fehlgeschlagene Ausführung.

Wenn die Option Automatische Ausführung abschließen deaktiviert ist, wird der Durchlauf als „Warnung“ markiert.

Es gibt einige Ausnahmen davon, dass Ausführungen unter Unvollständige Ausführungen gespeichert werden. Bei einigen Fehlertypen ist der automatische erneute Versuch einer Szenarioausführung nicht möglich.

## Ressourcen

Weitere Informationen finden Sie unter [Speichern unvollständiger Ausführungen zulassen](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions) im Artikel Konfigurieren von Szenario-Einstellungen.
