---
title: JWT-Module
description: Die  [!DNL Adobe Workfront Fusion] [!UICONTROL JWT]-App bietet ein Modul, das JWT-Token basierend auf dem bereitgestellten Algorithmus erstellt.
author: Becky
feature: Workfront Fusion
exl-id: 380f60db-b2ec-411a-86ee-0d5699f19b41
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# [!UICONTROL JWT]-Modul

Die [!DNL Adobe Workfront Fusion] [!UICONTROL JWT]-App bietet ein Modul, das JWT-Token basierend auf dem bereitgestellten Algorithmus erstellt.

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
   <p>Keine Workfront Fusion-Lizenzanforderung</p>
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

## JWT-API-Informationen

Der JWT-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
   <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.1.5</td> 
  </tr>
 </tbody> 
 </table>

## JWT-Modul und seine Felder

### JWT generieren

Dieses Modul generiert ein JWT basierend auf dem ausgewählten Algorithmus.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Algorithmus]</td> 
   <td> <p>Wählen Sie den Algorithmus aus, mit dem Sie den JWT generieren möchten.</p> <ul>
   <li><b>HS256</b>: HMAC mit SHA-256-Hash-Algorithmus</li>
   <li><b>HS384</b>: HMAC mit SHA-384-Hash-Algorithmus</li>
   <li><b>HS512</b>: HMAC mit SHA-512-Hash-Algorithmus</li>
   <li><b>RS256</b>: RSASSA-PKCS1-v1_5 mit SHA-256-Hash-Algorithmus</li>
   <li><b>RS384</b>: RSASSA-PKCS1-v1_5 mit SHA-384-Hash-Algorithmus</li>
   <li><b>RS512</b>: RSASSA-PKCS1-v1_5 mit SHA-512-Hash-Algorithmus</li>
   <li><b>PS256</b>: RSASSA-PSS mit SHA-256-Hash-Algorithmus (nur Knoten ^6.12.0 ODER &gt;=8.0.0)</li>
   <li><b>PS384</b>: RSASSA-PSS mit SHA-384-Hash-Algorithmus (nur Knoten ^6.12.0 ODER &gt;=8.0.0)</li>
   <li><b>PS512</b>: RSASSA-PSS mit SHA-512-Hash-Algorithmus (nur Knoten ^6.12.0 ODER &gt;=8.0.0)</li>
   <li><b>ES256</b>: ECDSA unter Verwendung der P-256-Kurve und des SHA-256-Hash-Algorithmus</li>
   <li><b>ES384</b>: ECDSA unter Verwendung der P-384-Kurve und des SHA-384-Hash-Algorithmus</li>
   <li><b>ES512</b>: ECDSA unter Verwendung der P-521-Kurve und des SHA-512-Hash-Algorithmus</li>
   </ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload] </td> 
   <td> <p>Klicken Sie für jedes Payload-Element, das Sie hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie den Schlüssel und den Wert des Elements ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Optionen] </td> 
   <td> <p>Klicken Sie für jedes Optionselement, das Sie hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie den Schlüssel und den Wert des Elements ein.</p> <p>Die folgenden Schlüssel sind verfügbar:
   <ul>
   <li><b>Algorithmus</b>: (Standard: RS256)</li>
   <li><b>expiresIn</b>: In Sekunden oder einer Zeichenfolge, die eine Zeitspanne beschreibt (z. B. 2 Tage, 10h, 7d). Ein numerischer Wert wird als Anzahl von Sekunden interpretiert. Wenn Sie eine Zeichenfolge verwenden, stellen Sie sicher, dass Sie die Zeiteinheiten (Tage, Stunden usw.) angeben, andernfalls wird standardmäßig die Millisekunden-Einheit verwendet (120 ist gleich 120 ms).</li>
   <li><b>notBefore</b>: Wird in Sekunden oder in einer Zeichenfolge angegeben, die eine Zeitspanne beschreibt (z. B. 2 Tage, 10h, 7d). Ein numerischer Wert wird als Anzahl von Sekunden interpretiert. Wenn Sie eine Zeichenfolge verwenden, stellen Sie sicher, dass Sie die Zeiteinheiten (Tage, Stunden usw.) angeben, andernfalls wird standardmäßig die Millisekunden-Einheit verwendet (120 ist gleich 120 ms).
</li>
   <li><b>Zielgruppe</b></li>
   <li><b>Aussteller</b></li>
   <li><b>jwtid</b></li>
   <li><b>Subjekt</b></li>
   <li><b>noTimestamp</b></li>
   <li><b>Kopfzeile</b></li>
   <li><b>keyId</b></li>
   <li><b>mutatePayload</b>: Wenn <code>true</code>, ändert die Sign-Funktion das Payload-Objekt direkt. Dies ist nützlich, wenn Sie einen Rohverweis auf die Payload benötigen, nachdem Ansprüche darauf angewendet wurden, aber bevor sie in ein Token codiert wurde.</li>
   <li><b>allowInsecureKeySizes</b>: Wenn <code>true</code>, ermöglicht die Verwendung privater Schlüssel mit einem Modul unter 2048 für RSA.</li>
   <li><b>allowInvalidAsymmetricKeyTypes</b>: Wenn <code>true</code>, lässt asymmetrische Schlüssel zu, die nicht mit dem angegebenen Algorithmus übereinstimmen. Diese Option dient nur der Abwärtskompatibilität und sollte vermieden werden.</li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>
