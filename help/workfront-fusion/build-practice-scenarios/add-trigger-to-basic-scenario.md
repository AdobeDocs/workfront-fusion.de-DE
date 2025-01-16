---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Hinzufügen eines Trigger-Moduls zu einem Basisszenario
description: Erfahren Sie, wie Sie ein Szenariomodul hinzufügen, damit das Trigger regelmäßig nach neuen Anfragen suchen und diese in Projekte konvertieren kann.
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
source-git-commit: 8884aef2237ad358c774110b81ac17b9efb386d4
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 1%

---

# Hinzufügen eines Trigger-Moduls zu einem Basisszenario

Trigger-Module werden am Anfang eines Szenarios platziert. Diese Module beginnen die Ausführung eines Szenarios, wenn eine Änderung in einem bestimmten Service stattgefunden hat. Bei der Änderung kann es sich um die Erstellung neuer Datensätze, das Löschen von Datensätzen, die Aktualisierung von Datensätzen usw. handeln. Sie legen die Kriterien für die Änderungen fest, die mit dem Szenario beginnen.

Abfragemodule überprüfen den Service in einem bestimmten Zeitintervall und geben Informationen zu Änderungen zurück, die während dieses Zeitintervalls aufgetreten sind. Wenn keine Änderungen vorgenommen wurden, führt der Trigger das Szenario nicht aus.

In diesem Beispiel fügen Sie ein Trigger -Modul hinzu, das alle 15 Minuten ausgeführt wird und ein Szenario startet, wenn Anforderungen an eine bestimmte Warteschlange gesendet wurden. Das Szenario konvertiert diese Anfragen dann in ein Projekt.

Dieses Beispiel ändert das in erstellte Szenario [Erstellen eines einfachen Szenarios](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

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

## Voraussetzungen

Sie müssen das unter &quot;[ eines einfachen Szenarios“ beschriebene Szenario erstellen](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) bevor Sie dieses Verfahren ausführen.

## Hinzufügen und Konfigurieren des Trigger-Moduls

### Hinzufügen des Trigger-Moduls

1. Öffnen Sie das Szenario im Szenario-Editor.
1. Klicken Sie mit der rechten Maustaste auf das erste Modul (Suche) und wählen Sie **Modul löschen**.

   Das Modul wird gelöscht, wobei ein leerer Platzhalter verbleibt.

1. Klicken Sie auf das leere Modul und wählen Sie **Adobe Workfront** aus der Liste der Apps aus.
1. Wählen Sie **Eintrag beobachten**.
1. Stellen Sie sicher, dass das Modul dieselbe Verbindung wie die übrigen Module im Szenario verwendet.
1. Wählen Sie im Feld Datensatztyp die Option **Problem** aus.
1. Wählen Sie im Feld Filter die Option **Nur neue Datensätze** aus.
1. Wählen Sie im Feld Ausgaben die Optionen `ID`, `Name` und `Project ID` aus.
1. Klicken Sie **OK**, um die Moduleinstellungen zu speichern.

   Das Fenster Start auswählen wird angezeigt.

1. Wählen Sie **Von jetzt an**.

### Planen des Trigger-Moduls

1. Klicken Sie auf die Uhr im Modul Einträge beobachten .

   Das Zeitplaneinstellungsfenster wird geöffnet.

1. Wählen Sie im Feld Ausführungsszenario die Option **In regelmäßigen Abständen** aus.

1. Klicken Sie **OK**.

### Aktualisieren des zweiten Moduls

Da das erste Modul ersetzt wurde, muss das zweite Modul dem neuen ersten Modul zugeordnet werden.

1. Öffnen Sie das Modul Objekt konvertieren .
1. Löschen Sie im Feld „Anfrage-ID“ den Block „Schwarze ID“. Der Block ist schwarz, da das Modul, von dem aus er zugeordnet wurde, nicht mehr verfügbar ist.
1. Wählen Sie den ID-Block unter dem ersten Modul (Einträge beobachten) aus, um ihn dem zweiten Modul zuzuordnen.
1. Klicken Sie **OK**.

### Testen und Aktivieren

1. Wechseln Sie zur Workfront-Umgebung, mit der sich Fusion verbindet, und fügen Sie ein Problem hinzu.
1. Klicken Sie in der linken unteren Ecke des Szenario-Editors auf **[!UICONTROL Run once]** .
1. Überprüfen Sie die Ausgabe, um sicherzustellen, dass das Szenario erwartungsgemäß ausgeführt wurde.
1. Wenn Sie sich vergewissert haben, dass das Szenario erwartungsgemäß funktioniert, klicken Sie auf **Umschalter** Planung“ unten links im Bildschirm auf **Ein**.

   Dadurch wird das Szenario aktiviert.
1. Klicken Sie [!DNL Workfront Fusion] unten links auf **[!UICONTROL Save]** , um den Fortschritt des Szenarios zu speichern.

   >[!IMPORTANT]
   >
   >Speichern Sie häufig, während Sie ein Szenario verfeinern und testen.

## Ressourcen

* Weitere Informationen zu Trigger-Modulen finden Sie unter [Trigger-Module](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) im Artikel Module - Übersicht.
