---
title: Erstellen von Verbindungen
description: Eine Verbindung muss den Anforderungen entsprechen, die von der API der App oder des Webservices festgelegt werden, mit der bzw. dem sie eine Verbindung herstellt. Aus diesem Grund variieren die Anweisungen zum Einrichten einer Verbindung je nach App oder Webservice. Dieser Artikel hilft Ihnen, die Anweisungen zum Verbinden von Adobe Workfront Fusion mit der ausgewählten App oder dem ausgewählten Webservice zu identifizieren und zu finden.
author: Becky
feature: Workfront Fusion
exl-id: 281403a6-6f88-4976-8a10-1d0848ef9b35
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 1%

---

# Erstellen von Verbindungen

Eine Verbindung muss den Anforderungen entsprechen, die von der API der App oder des Webservices festgelegt werden, mit der bzw. dem sie eine Verbindung herstellt. Aus diesem Grund variieren die Anweisungen zum Einrichten einer Verbindung je nach App oder Webservice. Dieser Artikel hilft Ihnen, die Anweisungen zum Verbinden von Adobe Workfront Fusion mit der ausgewählten App oder dem ausgewählten Webservice zu identifizieren und zu finden.

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

## Herstellen einer Verbindung zu einer Anwendung oder einem Webdienst, für die/den keine Konfiguration erforderlich ist

In den meisten Fällen können Sie das Modul verwenden, um eine Verbindung mit wenigen oder keinen zusätzlichen Informationen zu erstellen. Workfront Fusion verarbeitet die Authentifizierung automatisch.

Anweisungen zum Erstellen einer Verbindung ohne besondere Überlegungen finden Sie unter [Verbindung erstellen - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

## Herstellen einer Verbindung mit einer Adobe-App oder einem Service

Um eine Verbindung zu einer Adobe-App oder einem Service herzustellen, benötigen Sie möglicherweise Informationen aus der Adobe Admin Console, z. B. Ihre Organisations-ID oder die ID des technischen Kontos.

Sie können auch das Adobe Authenticator-Modul verwenden, um über eine einzige Verbindung eine Verbindung zu einer beliebigen Adobe-API herzustellen. Dadurch können Sie einfacher eine Verbindung zu Adobe-Produkten herstellen, die noch keinen dedizierten Fusion-Connector haben.

Spezifische Anweisungen finden Sie [im Artikel zum -Connector](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-adobe-products).

## Herstellen einer Verbindung zu einer [!DNL Microsoft] App oder einem Webdienst

Die meisten [!DNL Microsoft]-Apps in Workfront Fusion ermöglichen es Ihnen, eine Verbindung ohne zusätzliche Informationen zu erstellen.

Die folgenden Umstände erfordern zusätzliche Schritte beim Erstellen einer Verbindung:

* Verwendung von Microsoft Dynamics 365-Modulen.

  Anweisungen finden Sie unter [Microsoft Dynamics 365-Module](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).

* Herstellen einer Verbindung zur Microsoft Graph-API mithilfe eines HTTP-Moduls

  Anweisungen finden Sie unter [Aufrufen der MS Graph REST-API](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md).

## Herstellen einer Verbindung zu einer [!DNL Google] App oder einem Webdienst

Der Prozess zum Herstellen einer Verbindung zu [!DNL Google] Apps kann je nach Art des von Ihnen verwendeten [!DNL Google]-Kontos unterschiedlich sein. Darüber hinaus müssen [!DNL Google] Sicherheitsmaßnahmen möglicherweise zusätzlich konfiguriert werden, wenn Sie eine Verbindung zu Workfront Fusion herstellen.

Weitere Informationen finden Sie unter:

* [Verbinden von Adobe Workfront Fusion mit Google Services mithilfe eines benutzerdefinierten OAuth-Clients](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)
* [Verbinden von Adobe Workfront Fusion mit Google Services mit aktualisierten Sicherheitsmaßnahmen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-google-with-new-security-measures.md)

## Andere Apps, für die eine zusätzliche Konfiguration erforderlich ist

Einige Apps und Services folgen nicht der Grundkonfiguration für Workfront Fusion-Verbindungen. Anweisungen zum Verbinden dieser Apps finden Sie im Artikel zu dieser App.

Spezifische Anweisungen finden Sie [im Artikel zum -Connector](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-third-party-applications).
