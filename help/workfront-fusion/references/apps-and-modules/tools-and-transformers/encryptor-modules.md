---
title: Verschlüsseler
description: Mit Adobe Workfront Fusion Encryptor-Modulen können Sie beliebige Textdaten verschlüsseln. Sie unterstützen derzeit die Nachrichtenverschlüsselung über AES256 und PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---

# Verschlüsseler

[!DNL Adobe Workfront Fusion] [!UICONTROL Encryptor] können Sie beliebige Textdaten verschlüsseln. Sie unterstützen derzeit die Nachrichtenverschlüsselung über AES256 und PGP ([!UICONTROL OpenPGP]).

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Plan*</td>
  <td> <p>[!UICONTROL Pro] oder höher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung und -integration], [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den [!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Adobe Workfront] verfügen, muss Ihr Unternehmen [!DNL Adobe Workfront Fusion] kaufen und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden. [!DNL Workfront Fusion] ist im [!UICONTROL Ultimate] [!DNL Workfront] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Nachrichtenverschlüsselung und -entschlüsselung mit PGP

Beim Ver- und Entschlüsseln mit PGP muss ein Schlüsselbund verwendet und ein privater oder öffentlicher Schlüssel (oder beides) erstellt werden.

Weitere Informationen zu öffentlichen und privaten Schlüsseln finden Sie im [Adobe Workfront Fusion-Glossar](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md). <!--For more information on keychains, see [Keys in [!DNL Adobe Workfront Fusion]]().-->

## [!UICONTROL Encryptor] Module und ihre Felder

Beim Konfigurieren von [!UICONTROL Encryptor]-Modulen werden die folgenden Felder angezeigt. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

### Verschlüsseln einer PGP-Nachricht

Dieses Modul ermöglicht die Verschlüsselung von Nachrichten mit öffentlichen und privaten Schlüsseln.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Geben Sie den privaten Schlüssel des Absenders ein. Dadurch kann die Identität des Absenders authentifiziert werden.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Geben Sie den öffentlichen Schlüssel des Empfängers ein.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Geben Sie die Nachricht ein, die Sie verschlüsseln möchten.</td>
    </tr>

### Entschlüsseln einer PGP-Nachricht

Mit diesem Modul können Sie eine Nachricht mit öffentlichen und privaten Schlüsseln entschlüsseln.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Geben Sie den privaten Schlüssel des Empfängers ein.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Geben Sie den öffentlichen Schlüssel des Empfängers ein. Dadurch kann die Identität des Absenders authentifiziert werden.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Ordnen Sie die Nachricht zu, die Sie entschlüsseln möchten.</td>
    </tr>
</table>
