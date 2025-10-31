---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: connections-annd-webhooks
title: Verwalten von Verbindungen
description: Für die meisten Apps ist es erforderlich, eine Verbindung zu erstellen, über die Adobe Workfront Fusion mit dem angegebenen Drittanbieterdienst entsprechend den Einstellungen des jeweiligen Szenarios kommunizieren kann.
author: Becky
feature: Workfront Fusion
exl-id: 26d7caad-8e12-4f04-ac7c-f71686c90ee6
source-git-commit: 93d06cb917680f9cabc1bad6be0f9cd843449d07
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 1%

---

# Verwalten von Verbindungen

Eine Verbindung stellt die Autorisierung und Berechtigungen dar, die Fusion für den Zugriff auf das Programm verwendet. Sie können für jede Anwendung eine oder mehrere Verbindungen erstellen und dieselbe Verbindung in mehreren Modulen oder Szenarien verwenden.

Sie können diese Verbindungen im Bereich Verbindungen verwalten.

Weitere Informationen zu Verbindungen finden Sie unter [Verbindung - Übersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

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
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Connector-basiert (veraltet): Um eine Verbindung zu Anwendungen außerhalb der Workfront-Produktfamilie herzustellen, benötigen Sie Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Anzeigen und Verwalten von Verbindungen

Sie können alle Verbindungen über den Bereich Verbindungen verwalten.

>[!NOTE]
>
>Verbindungen gehören Teams. Wenn Sie die gesuchte Verbindung nicht finden können, überprüfen Sie, ob Sie das richtige Team anzeigen.
>
>Um ein neues Team auszuwählen, klicken Sie im linken Navigationsbereich auf den Namen des Teams und wählen Sie ein neues Team aus.

1. Um den Bereich Verbindungen zu öffnen, klicken Sie **Verbindungen** ![Verbindungssymbol](assets/connections-icon.png) in der linken Navigationsleiste.
1. Suchen Sie die Verbindung, die Sie verwalten möchten, und führen Sie dann einen oder mehrere der folgenden Schritte in der Zeile für diese Verbindung aus.
1. (Optional) Weisen Sie eine Umgebung und einen Verbindungstyp zu, indem Sie auf die **Umgebung** und **Typ** Dropdown-Listen klicken und eine Option auswählen.
1. (Optional) Um anzuzeigen, welche Berechtigungen Workfront Fusion für die Verbindung erteilt wurden, klicken Sie auf das Symbol Anzeigen ![Verbindungsberechtigungen anzeigen](assets/view-connection-permissions.png) für diese Verbindung.
1. (Optional) Um eine Verbindung umzubenennen, markieren Sie den Verbindungsnamen und geben Sie den neuen Namen ein.
1. (Optional) Um eine Verbindung erneut zu autorisieren, aktivieren Sie das Kontrollkästchen neben der Verbindung und klicken Sie **unten** Bildschirm auf „Erneut genehmigen“.
1. (Optional) Um eine Verbindung zu löschen, aktivieren Sie das Kontrollkästchen neben der Verbindung, klicken Sie **Löschen** unten auf dem Bildschirm und dann auf **Wirklich?**.
1. (Optional) Um sicherzustellen, dass die Verbindung zum Service erfolgreich hergestellt wurde, aktivieren Sie das Kontrollkästchen neben der Verbindung und klicken Sie **unten** Bildschirm auf „Überprüfen“.
1. (Optional) Um aktive Szenarien anzuzeigen, die diese Verbindung verwenden, aktivieren Sie das Kontrollkästchen neben der Verbindung und klicken dann auf **Aktive Szenarien abrufen**. Sie können dann in der Liste Aktive Szenarien auf ein Szenario klicken, um zu diesem Szenario zu wechseln.

## Erneuern einer Verbindung

Workfront Fusion erhält in der Regel für unbegrenzte Zeit Zugriffsrechte für einen bestimmten Dienst. Bei einigen Anwendungen muss die Zugriffsberechtigung nach einer bestimmten Zeit erneuert werden. In diesen Fällen werden Sie von Workfront Fusion kurz vor Ablauf der Zugriffsrechte per E-Mail benachrichtigt.

So erneuern Sie eine Verbindung:

1. Um den Bereich Verbindungen zu öffnen, klicken Sie **Verbindungen** ![Verbindungssymbol](assets/connections-icon.png) in der linken Navigationsleiste.
1. Suchen Sie die Verbindung, die Sie erneuern möchten.
1. Aktivieren Sie in der Zeile für diese Verbindung das Kontrollkästchen neben der Verbindung und klicken Sie dann unten **Bildschirm auf** Erneut genehmigen“.

## Ressourcen

* Weitere Informationen zu Verbindungsmetadaten, z. B. Umgebung und Typ, finden Sie unter [Verbindungsmetadaten](/help/workfront-fusion/references/connections/connection-metadata.md).
