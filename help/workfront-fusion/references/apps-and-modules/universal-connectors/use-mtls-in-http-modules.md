---
title: Verwenden von gegenseitigem TLS in HTTP-Modulen in Adobe Workfront Fusion
description: Sie können Mutual TLS in Ihren Adobe Workfront Fusion-HTTP-Modulen verwenden, sodass beide Seiten der Informationstransaktion die Identität der anderen überprüfen können.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 89017451c8e0b821616adda861222127e100a08d
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Verwenden von gegenseitigem TLS in HTTP-Modulen in [!DNL Adobe Workfront Fusion]

## Gegenseitige TLS - Übersicht

Wenn Sie Daten über das Internet senden, müssen Sie sicherstellen, dass sie an den richtigen Ort gesendet werden oder von dort stammen und dass nur die vorgesehene Empfängerin oder der vorgesehene Empfänger sie lesen kann. Bei aktiviertem TLS verwendet der Client (Computer, der Informationen anfordert) Zertifikate, um die Identität des Servers zu überprüfen (Computer, der Informationen bereitstellt). Dadurch werden sichere HTTP-Verbindungen hergestellt.

Das gegenseitige TLS ermöglicht es, dass diese Identitätsbestätigung in beide Richtungen funktioniert. Wenn der Server sein Zertifikat sendet, um seine Identität zum Client zu überprüfen, fordert er auch das Zertifikat des Clients an. Dadurch wird sichergestellt, dass der Server keine Informationen an eine Website oder einen Benutzer sendet, die bzw. der sie missbrauchen würde.

>[!INFO]
>
>**Beispiel:**
>
>* **TLS**: Wenn eine Person „MyGreatBank.com“ in einen Browser eingibt, möchte sie sicherstellen, dass sie zu „My Great Bank“ geht und nicht zu einer Website, die ihre Bankinformationen missbrauchen oder verkaufen könnte. Sie möchten auch sicherstellen, dass ihre Bankkontoinformationen verschlüsselt sind.
>
>   Wenn der Browser (der Client) eine Verbindung zu MyGreatBank.com (dem Server) herstellt, erfordert TLS ein Zertifikat von MyGreatBank.com, um seine Identität zu überprüfen. Das Zertifikat wird von einer Zertifizierungsstelle wie [!DNL DigiCert] oder [!DNL Thawte] bereitgestellt. Da der Browser der Zertifizierungsstelle vertraut, lässt er die Verbindung zu.
>
>* **Mutual TLS**: MySoftware.com ist ein Software-Client, der Informationen von der MyGreatBank.com API benötigt. MyGreatBank erlaubt nur vertrauenswürdigen Kunden eine Verbindung zu ihren Servern herzustellen. Zusätzlich zum regulären TLS, das die Identität von MyGreatBank.com überprüft, überprüft der Prozess für TLS-/Zertifizierungsstellen auch die Anfrage von MySoftware.com.

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
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Oder</p>
   <p>Legacy: Workfront Fusion für Arbeitsautomatisierung und -integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Prime oder Workfront auswählen: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>Ultimate Workfront-Paket: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Bereitstellen Ihres [!DNL Workfront Fusion] öffentlichen Zertifikats

Wenn Sie über eine HTTP-Anfrage eine Verbindung zu einem Webdienst herstellen, benötigt der Webdienst in der Regel ein [!DNL Workfront Fusion] öffentliches Zertifikat zur Überprüfung. Auf diese Weise kann der Webdienst das in der HTTP-Anfrage dargestellte Zertifikat mit dem in der Datei enthaltenen vergleichen, um sicherzustellen, dass sich das Zertifikat auf der Zulassungsliste des Webdienstes befindet.

Anweisungen zum Hochladen des [!DNL Adobe Workfront Fusion] öffentlichen Zertifikats auf einen Webdienst finden Sie in der Dokumentation zum Webdienst.

>[!NOTE]
>
>Zusätzlich zum Zertifikat müssen Sie möglicherweise weitere Informationen angeben. Informationen dazu, was für einen Webdienst erforderlich ist, finden Sie in der API-Dokumentation des Webdienstes.

Sie können die folgenden Links verwenden, um die öffentlichen Workfront Fusion-Zertifikate herunterzuladen. Informationen zum Auffinden Ihres Rechenzentrums finden Sie unter [Identifizieren Ihres Rechenzentrums](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md) im Artikel Konfigurieren von IP-Adressen für Fusion in der -Zulassungsliste Ihres Unternehmens.

### Zertifikate für 2025

>[!IMPORTANT]
>
>* Diese [!DNL Workfront Fusion] öffentlichen Zertifikate laufen am **4. April 2026** (USA und EU) oder **25. November** (Azure) ab. Nach Ablauf Ihres müssen Sie ein neues Zertifikat in den Webservice hochladen. Wir empfehlen Ihnen Folgendes:
>
>   * Notieren Sie sich das Ablaufdatum und legen Sie eine Erinnerung fest, damit Sie das Zertifikat in Ihren Webservice hochladen können.
>   * Setzen Sie ein Lesezeichen für diese Seite, um die neuen Zertifikate leicht zu finden.
>
>* Hierbei handelt es sich um Nicht-Platzhalter-TLS-Zertifikate.

| Rechenzentrum | Downloadlink | Gültige Daten |
|---|---|---|
| US-Rechenzentrum | [Download [!DNL Workfront Fusion] US-Zertifikat 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-us-mtls-certificate.pem) | 3. März 2025 bis 4. April 2026 |
| EU-Rechenzentrum | [Download [!DNL Workfront Fusion] EU-Zertifikat 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-eu-mtls-certificate.pem) | 3. März 2025 bis 4. April 2026 |
| Azure-Cluster | [Download [!DNL Workfront Fusion] Azure-Zertifikat 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-az-mtls-certificate.pem) | 24. Oktober 2024 bis 25. November 2025 |

<!--

### Certificates for 2024

>[!IMPORTANT]
>
>* We recommend installing the certificates for 2025, available above.
>* These [!DNL Workfront Fusion] public certificates expire on **May 7, 2025**. After yours expires you will need to upload a new certificate to the web service. We recommend that you:
>
>   * Make note of the expiration date and set a reminder for yourself to upload the certificate to your web service.
>   * Bookmark this page to easily find the new certificates.
>
>* These are non-wildcard mTLS certificates.

| Datacenter | Download link | Dates valid |
|---|---|---|
| US Datacenter | [Download [!DNL Workfront Fusion] Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |
| EU Datacenter | [Download [!DNL Workfront Fusion] EU Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |

-->

## Aktivieren von gegenseitigem TLS in [!DNL Workfront Fusion] HTTP-Modulen

Alle [!DNL Workfront Fusion] [!UICONTROL HTTP]-Anfragemodule haben die Möglichkeit, gegenseitiges TLS zu aktivieren.

So aktivieren Sie gegenseitiges TLS in einem [!UICONTROL HTTP]-Anfragemodul:

1. Fügen Sie Ihrem [!UICONTROL  ein ]HTTP“-Anfragemodul hinzu.
1. Starten Sie die Konfiguration des Moduls.

   Anweisungen zum Konfigurieren eines [!UICONTROL HTTP]-Anfragemoduls finden Sie im entsprechenden Artikel unter [Universelle Connectoren](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

1. Aktivieren Sie **[!UICONTROL Erweiterte Einstellungen anzeigen]** unten im Modul.
1. Aktivieren **[!UICONTROL Gegenseitige TLS verwenden]**.
