---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Hinzufügen eines Webhooks zu einem Basisszenario
description: Webhooks, auch als Instant Trigger bezeichnet, sind eine spezielle Art von Szenariomodul, das ein Trigger starten kann, wenn eine Änderung vorgenommen wird, anstatt nach einem bestimmten Zeitplan.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 1%

---

# Hinzufügen eines Webhooks zu einem Basisszenario

Webhooks, auch als Instant Trigger bezeichnet, sind eine spezielle Art von Szenariomodul, das ein Trigger starten kann, wenn eine Änderung vorgenommen wird, anstatt nach einem bestimmten Zeitplan.

In diesem Beispiel fügen Sie einen Webhook hinzu, um ein Szenario zu starten, sobald Anforderungen an eine bestimmte Anfragewarteschlange gesendet wurden. Das Szenario konvertiert diese Anfragen dann in ein Projekt.

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

## Webhook hinzufügen und konfigurieren


### Webhook-Modul hinzufügen

1. Öffnen Sie das Szenario im Szenario-Editor.
1. Klicken Sie mit der rechten Maustaste auf das erste Modul und wählen Sie **Modul löschen**.

   Das Modul wird gelöscht, wobei ein leerer Platzhalter verbleibt.

1. Klicken Sie auf das leere Modul und wählen Sie **Adobe Workfront** aus der Liste der Apps aus.
1. Wählen Sie **Ereignisse ansehen** aus.
1. Klicken Sie **Hinzufügen** neben dem Feld Webhook .
1. Wählen Sie im Feld Datensatztyp die Option **Problem** aus, damit das Modul einen Trigger für Änderungen bei Problemen durchführt.
1. Wählen Sie im Feld Status die Option **Neuer Status**. Dies ist ein Pflichtfeld, das für den Filter verwendet wird, der in diesem Beispiel nicht abgedeckt wird.
1. Wählen Sie im Feld Datensatzherkunft die Option **Nur neuer Datensatz**. Dadurch kann das Szenario einen Trigger auslösen, wenn ein Problem hinzugefügt wird, und nicht, wenn ein Problem aktualisiert oder gelöscht wird.
1. Klicken Sie **Speichern**, um die Modulkonfiguration zu speichern.

## Aktualisieren des zweiten Moduls

1. Öffnen Sie das Szenario.
1. Klicken Sie auf **Objekt konvertieren**-Modul, um es zu öffnen.
1. Löschen Sie im Feld „Anfrage-ID“ den Block „Schwarze ID“. Der Block ist schwarz, da das Modul, von dem aus er zugeordnet wurde, nicht mehr verfügbar ist.
1. Wählen Sie den ID-Block unter dem ersten Modul (Ereignisse beobachten) aus, um ihn dem zweiten Modul zuzuordnen.
1. Klicken Sie **OK**.



### Testen und Aktivieren

1. Klicken Sie in der linken unteren Ecke des Szenario-Editors auf **[!UICONTROL Run once]** .

   Das Szenario muss ausgeführt werden, um auf die neue Anfrage warten zu können.
1. Wechseln Sie zur Workfront-Umgebung, mit der sich Fusion verbindet, und fügen Sie ein Problem hinzu.

   Das Szenario sollte ausgeführt werden.
1. Überprüfen Sie die Ausgabe, um sicherzustellen, dass das Szenario erwartungsgemäß ausgeführt wurde.
1. Wenn Sie sich vergewissert haben, dass das Szenario erwartungsgemäß funktioniert, klicken Sie auf **Umschalter** Planung“ unten links im Bildschirm auf **Ein**.

   Dadurch wird das Szenario aktiviert.
1. Klicken Sie [!DNL Workfront Fusion] unten links auf **[!UICONTROL Save]** , um den Fortschritt des Szenarios zu speichern.
