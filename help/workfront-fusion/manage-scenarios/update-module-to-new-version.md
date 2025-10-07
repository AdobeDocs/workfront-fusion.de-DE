---
title: Aktualisieren eines Moduls auf eine neue Version
description: Da die Anwendungen, mit denen Workfront Fusion eine Verbindung herstellt, möglicherweise aktualisiert oder neue Versionen veröffentlicht werden, ist es gelegentlich erforderlich, dass Fusion aktualisierte Module für diese Anwendungen veröffentlicht.
author: Becky
feature: Workfront Fusion
exl-id: b7f07fa5-9d81-48b3-b0ce-7a18b3b44508
source-git-commit: d0d9d7cdad993ecceaa0abf0ac69e9a9abd78b69
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 2%

---

# Aktualisieren eines Moduls auf eine neue Version

Da die Anwendungen, mit denen Workfront Fusion eine Verbindung herstellt, möglicherweise aktualisiert oder neue Versionen veröffentlicht werden, ist es gelegentlich erforderlich, dass Fusion aktualisierte Module für diese Anwendungen veröffentlicht.

Wenn in einem Szenario ein grünes Upgrade-Modulsymbol auf einem Modul angezeigt wird, hat Workfront Fusion eine neue Version dieses Moduls veröffentlicht.

![Aktualisierungssymbol](assets/update-indicator-workfront.png)

Sie können das Modul aktualisieren, ohne ein neues Szenario zu erstellen.

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
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
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
   <p>Neu:</p> <ul><li>Plan für [!UICONTROL Select] oder [!UICONTROL Prime] Workfront: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>[!UICONTROL Ultimate] Workfront-Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Unternehmen sein.</p>
     <p>Sie müssen ein Workfront Fusion-Administrator für Ihr Team sein.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Aktualisieren eines Workfront-Moduls auf eine neue Version

1. Klicken Sie auf das Symbol **Modul aktualisieren** ![Upgrade-Symbol](assets/upgrade-icon.png) auf dem Modul, das Sie auf eine neue Version aktualisieren möchten.
   ![Aktualisierungssymbol](assets/update-indicator-workfront.png)
1. Wählen Sie eine der folgenden Optionen:

   * Um ein neues Modul auszuwählen, das dieses ersetzen soll (anstatt ein Upgrade des Moduls durchzuführen), klicken Sie auf **Neue auswählen** und fahren Sie dann wie [Aktualisieren eines Nicht-Workfront-Moduls auf eine neue Version) &#x200B;](#upgrade-a-non-workfront-module-to-a-new-version).
   * Um nur dieses Modul zu aktualisieren und die Modulkonfiguration beizubehalten, klicken Sie auf **Aktualisieren**.
   * Um alle Workfront-Module im Szenario zu aktualisieren, klicken Sie auf **Alle aktualisieren**.

1. Speichern Sie das Szenario.

>[!NOTE]
>
>Wenn Sie Workfront-Module aktualisiert haben, empfehlen wir, diese zu öffnen und die Modulkonfiguration zu überprüfen.

## Aktualisieren eines Nicht-Workfront-Moduls auf eine neue Version

1. Klicken Sie auf das Symbol **Modul aktualisieren** ![Upgrade-Symbol](assets/upgrade-icon.png) auf dem Modul, das Sie auf eine neue Version aktualisieren möchten.
   ![Aktualisierungssymbol](assets/update-indicator.png)
1. Klicken Sie **Neu wählen**.
1. Wählen Sie das Modul aus, das Sie das vorherige Modul ersetzen möchten.
1. Konfigurieren Sie das Modul mit denselben Einstellungen wie das vorhandene Modul.
1. Verbinden Sie das neue Modul mit dem Szenario an derselben Stelle wie das vorhandene Modul.
1. Löschen Sie das alte Modul.
1. Speichern Sie das Szenario.
