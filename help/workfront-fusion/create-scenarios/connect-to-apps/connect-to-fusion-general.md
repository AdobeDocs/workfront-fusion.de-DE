---
title: Erstellen einer Verbindung - Grundlegende Anweisungen
description: Viele  [!DNL Adobe Workfront Fusion]  erfordern beim Erstellen einer Verbindung keine benutzerdefinierte Konfiguration. In diesem Artikel wird der Standardprozess zur Erstellung von Verbindungen beschrieben.
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Erstellen einer Verbindung - Grundlegende Anweisungen

Viele [!DNL Adobe Workfront Fusion]-Connectoren erfordern beim Erstellen einer Verbindung keine benutzerdefinierte Konfiguration. In diesem Artikel wird der Standardprozess zur Erstellung von Verbindungen beschrieben.

>[!NOTE]
>
>
>Wenn Adobe Workfront Fusion keine App für den Webservice anbietet, den Sie in Ihrem Szenario verwenden möchten, können Sie eine Verbindung zum Webservice mithilfe [!DNL Workfront Fusion] HTTP- und Webhooks-Modulen herstellen, wie in den folgenden Artikeln erläutert:
>
>* [Verbinden Sie Adobe Workfront Fusion mit einem Webservice, der die API-Token-Autorisierung verwendet](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [Webhook für einen Webservice ohne Connector konfigurieren](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

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

## Erstellen einer Verbindung

So erstellen Sie eine Verbindung innerhalb eines [!DNL Workfront Fusion]:

1. Klicken Sie auf **[!UICONTROL Add]** neben dem Feld [!UICONTROL Connection] , um das **[!UICONTROL Create a connection]** zu öffnen.
1. (Optional) Ändern Sie die **[!UICONTROL Connection name]**.
1. (Bedingt) Wenn für die App erweiterte Verbindungseinstellungen wie eine ID, ein Schlüssel oder eine [!UICONTROL secret] erforderlich sind, geben Sie diese Informationen ein.

   Möglicherweise müssen Sie auf **[!UICONTROL Show advanced settings]** klicken, um die Felder anzuzeigen, in die Sie diese Art von Informationen eingeben können.

1. Klicken Sie auf **[!UICONTROL Continue]**.
1. Geben Sie im angezeigten Anmeldefenster Ihre Anmeldedaten ein, um sich bei der App anzumelden, falls Sie dies noch nicht getan haben.
1. (Bedingt) Wenn eine **[!UICONTROL Allow]** Schaltfläche angezeigt wird, untersuchen Sie die Aktionen, die der Connector ausführen kann, und klicken Sie dann auf die Schaltfläche, um die App mit [!DNL Workfront Fusion] zu verbinden.

   >[!NOTE]
   >
   >Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
   >
   >Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.
