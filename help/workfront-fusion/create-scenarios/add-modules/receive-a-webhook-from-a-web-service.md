---
title: Webhook für einen Webservice ohne Connector konfigurieren
description: Wenn ein Webservice derzeit keinen dedizierten Connector in Workfront Fusion hat, aber das Senden von Webhooks unterstützt, können Sie den Service mit dem benutzerdefinierten Webhook-Modul als sofortigen Trigger zu einem Szenario hinzufügen.
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---

# Webhook für einen Webservice ohne Connector konfigurieren

Wenn ein Webservice derzeit keinen dedizierten Connector in Workfront Fusion hat, aber das Senden von Webhooks unterstützt, können Sie den Service mit dem benutzerdefinierten Webhook-Modul als sofortigen Trigger zu einem Szenario hinzufügen. Dieser Prozess wird als Empfang eines Webhooks bezeichnet und erfordert einige Konfigurationen auf der Seite der Anwendung, mit der Sie eine Verbindung herstellen.

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
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

## Webhook empfangen

1. Klicken Sie im linken Bedienfeld auf die Registerkarte **[!UICONTROL Scenarios]** .
1. Wählen Sie das Szenario aus, in dem Sie einen Webhook hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Fügen Sie das Modul **Webhooks > Benutzerdefinierter Webhook** hinzu, um Ihr Szenario zu starten.
1. Klicken Sie **Hinzufügen** neben dem Feld Webhook .
1. Geben Sie einen **Webhook-Namen** in das Feld ein, das angezeigt wird
1. (Optional) Konfigurieren des Webhooks.

   Anweisungen finden Sie unter [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

1. Klicken Sie auf **Speichern**.

1. Klicken Sie **Adresse in Zwischenablage kopieren** und dann auf **OK**.

1. Melden Sie sich beim -Webdienst an und führen Sie dort folgende Schritte aus:

   1. Erstellen Sie im Bereich Einstellungen für den Webdienst einen Webhook.

      Spezifische Anweisungen hängen von der Anwendung ab. Es wird empfohlen, in der Dokumentation des Programms nach „Webhook erstellen“ zu suchen.
   1. Fügen Sie die Adresse ein, die Sie in Schritt 3 in die Zwischenablage kopiert haben.
   1. Wählen Sie das Ereignis aus, durch das der Webhook Trigger wird.

1. Führen Sie das Szenario aus.

   Wenn das Ereignis oder die Ereignisse eintreten, werden die Trigger des benutzerdefinierten Webhook-Moduls ausgeführt und das Szenario wird ausgeführt.
