---
title: Webhook für einen Webservice ohne Connector konfigurieren
description: Wenn ein Webservice derzeit keinen dedizierten Connector in Workfront Fusion hat, aber das Senden von Webhooks unterstützt, können Sie den Service mit dem benutzerdefinierten Webhook-Modul als sofortigen Trigger zu einem Szenario hinzufügen.
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
TQID: https://experienceleague.adobe.com/Ux37ZShkz3kxnJg3Guwqvqt8TISuzV0kAVZ-kKfy0zI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 354
ht-degree: 27%

---

# Webhook für einen Webservice ohne Connector konfigurieren

Wenn ein Webservice derzeit keinen dedizierten Connector in Workfront Fusion hat, aber das Senden von Webhooks unterstützt, können Sie den Service mit dem benutzerdefinierten Webhook-Modul als sofortigen Trigger zu einem Szenario hinzufügen. Dieser Prozess wird als Empfang eines Webhooks bezeichnet und erfordert einige Konfigurationen auf der Seite der Anwendung, mit der Sie eine Verbindung herstellen.

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Ein beliebiges Adobe Workfront Workflow- und Adobe Workfront Automation and Integration-Paket</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Webhook empfangen

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Webhook hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Fügen Sie das Modul **Webhooks > Benutzerdefinierter Webhook** hinzu, um Ihr Szenario zu starten.
1. Klicken Sie neben dem Feld „Webhook“ auf **Hinzufügen**.
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
