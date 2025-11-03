---
title: Verschlüsseler
description: Mit Adobe Workfront Fusion Encryptor-Modulen können Sie beliebige Textdaten verschlüsseln. Sie unterstützen derzeit die Nachrichtenverschlüsselung über AES256 und PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---

# Verschlüsseler

Mit Adobe Workfront Fusion [!UICONTROL Encryptor]-Modulen können Sie beliebige Textdaten verschlüsseln. Sie unterstützen derzeit die Nachrichtenverschlüsselung über AES256 und PGP ([!UICONTROL OpenPGP]).

Diese Module müssen mit Verschlüsselungsprozessen vertraut sein.

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
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Nachrichtenverschlüsselung und -entschlüsselung mit PGP

Beim Ver- und Entschlüsseln mit PGP muss ein Schlüsselbund verwendet und ein privater oder öffentlicher Schlüssel (oder beides) erstellt werden.

Weitere Informationen zu öffentlichen und privaten Schlüsseln finden Sie im [Glossar zu Adobe Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md).

Weitere Informationen zu Schlüsseln finden Sie unter [Schlüssel](/help/workfront-fusion/references/modules/keys.md).

## [!UICONTROL Encryptor]-Module und ihre Felder

Beim Konfigurieren von [!UICONTROL Encryptor]-Modulen werden die folgenden Felder angezeigt. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

### AES-Entschlüsselung (erweitert)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL-Schlüssel]</td>
        <td>Wählen Sie den Schlüssel aus, den das Modul verwenden soll. Um einen Schlüssel zu erstellen, klicken Sie <b>Hinzufügen</b> und geben Sie den Namen, den Schlüssel und den Kodierungstyp des Schlüssels ein.</td>
    </tr>
    <tr>
        <td>Bits</td>
        <td>Wählen Sie aus, ob das Modul 128-Bit- oder 256-Bit-Verschlüsselung verwenden soll.</td>
    </tr>
    <tr>
        <td>Eingabekodierung</td>
        <td>Wählen Sie den Typ der Eingabekodierung aus, den Sie verwenden möchten:
        <ul>
        <li>Binär</li>
        <li>Basis 64</li>
        <li>hexadezimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Daten</td>
        <td>Geben Sie die Daten ein, die Sie entschlüsseln möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
        <td>Ausgabekodierung</td>
        <td>Wählen Sie den Typ der Ausgabekodierung aus, den Sie verwenden möchten:
        <ul>
        <li>ASCII</li>
        <li>Binär</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Verschlüsselungsalgorithmus</td>
        <td>Wählen Sie den Chiffrier-Algorithmus aus, den Sie verwenden möchten:
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Kodierung des Initialisierungsvektors</td>
        <td>Wählen Sie die zu verwendende Initialisierungsvektorcodierung aus:
        <ul>
        <li>UTF-8</li>
        <li>Binär</li>
        <li>Basis 64</li>
        <li>hexadezimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Authentifizierungs-Tag-Kodierung</td>
        <td>Wählen Sie die Authentifizierungs-Tag-Codierung aus, die Sie verwenden möchten:
        <ul>
        <li>UTF-8</li>
        <li>Binär</li>
        <li>Basis 64</li>
        <li>hexadezimal</li>
        </ul>
        </td>
    </tr>
</table>

### AES-Entschlüsselung (einfach)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL-Schlüssel]</td>
        <td>Wählen Sie den Schlüssel aus, den das Modul verwenden soll. Um einen Schlüssel zu erstellen, klicken Sie <b>Hinzufügen</b> und geben Sie den Namen, den Schlüssel und den Kodierungstyp des Schlüssels ein.</td>
    </tr>
   <tr>
        <td>Eingabekodierung</td>
        <td>Wählen Sie den Typ der Eingabekodierung aus, den Sie verwenden möchten:
        <ul>
        <li>Binär</li>
        <li>Basis 64</li>
        <li>hexadezimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Daten</td>
        <td>Geben Sie die Daten ein, die Sie entschlüsseln möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
        <td>Ausgabekodierung</td>
        <td>Wählen Sie den Typ der Ausgabekodierung aus, den Sie verwenden möchten:
        <ul>
        <li>ASCII</li>
        <li>Binär</li>
        <li>UTF-8</li>
        </ul>
        </td>
     </tr>
    <tr>
        <td>Geheimer Schlüssel</td>
        <td>Geben Sie den geheimen Schlüssel ein, den Sie verwenden möchten, oder ordnen Sie ihn zu.</td>
    </tr>
</table>

### AES Encrypt (erweitert)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL-Schlüssel]</td>
        <td>Wählen Sie den Schlüssel aus, den das Modul verwenden soll. Um einen Schlüssel zu erstellen, klicken Sie <b>Hinzufügen</b> und geben Sie den Namen, den Schlüssel und den Kodierungstyp des Schlüssels ein.</td>
    </tr>
    <tr>
        <td>Bits</td>
        <td>Wählen Sie aus, ob das Modul 128-Bit- oder 256-Bit-Verschlüsselung verwenden soll.</td>
    </tr>
    <tr>
        <td>Eingabekodierung</td>
        <td>Wählen Sie den Typ der Eingabekodierung aus, den Sie verwenden möchten:
        <ul>
        <li>Binär</li>
        <li>ASCII</li>
        <li>hexadezimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Daten</td>
        <td>Geben Sie die Daten ein, die Sie verschlüsseln möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
        <td>Ausgabekodierung</td>
        <td>Wählen Sie den Typ der Ausgabekodierung aus, den Sie verwenden möchten:
        <ul>
        <li>ASCII</li>
        <li>Binär</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Verschlüsselungsalgorithmus</td>
        <td>Wählen Sie den Chiffrier-Algorithmus aus, den Sie verwenden möchten:
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Kodierung des Initialisierungsvektors</td>
        <td>Wählen Sie die Authentifizierungs-Tag-Codierung aus, die Sie verwenden möchten:
        <ul>
        <li>UTF-8</li>
        <li>Binär</li>
        <li>Basis 64</li>
        <li>hexadezimal</li>
        </ul>
        </td>
    </tr>
</table>

### AES-Verschlüsselung (einfach)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL-Schlüssel]</td>
        <td>Wählen Sie den Schlüssel aus, den das Modul verwenden soll. Um einen Schlüssel zu erstellen, klicken Sie <b>Hinzufügen</b> und geben Sie den Namen, den Schlüssel und den Kodierungstyp des Schlüssels ein.</td>
    </tr>
   <tr>
        <td>Eingabekodierung</td>
        <td>Wählen Sie den Typ der Eingabekodierung aus, den Sie verwenden möchten:
        <ul>
        <li>Binär</li>
        <li>ASCII</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Daten</td>
        <td>Geben Sie die Daten ein, die Sie verschlüsseln möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
        <td>Ausgabekodierung</td>
        <td>Wählen Sie den Typ der Ausgabekodierung aus, den Sie verwenden möchten:
        <ul>
        <li>Basis 64</li>
        <li>Binär</li>
        <li>hexadezimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Geheimer Schlüssel</td>
        <td>Geben Sie den geheimen Schlüssel ein, den Sie verwenden möchten, oder ordnen Sie ihn zu.</td>
    </tr>
</table>


### Digitale Signatur erstellen

Mit diesem Modul können Sie eine Nachricht mit öffentlichen und privaten Schlüsseln entschlüsseln.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Privater Schlüssel]</td>
        <td>Privaten Schlüssel auswählen, der für diese Signatur verwendet werden soll. Um einen privaten Schlüssel hinzuzufügen, klicken Sie auf <b>Hinzufügen</b> und geben Sie den Namen des Schlüssels, den Schlüsseltext und die Passphrase ein.</td>
    </tr>
    <tr>
        <td>Algorithmus </td>
        <td>Wählen Sie aus, ob Sie RSA-SHA1 oder RSA-SHA256 verwenden möchten. </td>
    </tr>
   <tr>
        <td>Eingabekodierung</td>
        <td>Wählen Sie den Typ der Eingabekodierung aus, den Sie verwenden möchten:
        <ul>
        <li>ASCII</li>
        <li>Binär</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Ausgabekodierung</td>
        <td>Wählen Sie den Typ der Ausgabekodierung aus, den Sie verwenden möchten:
        <ul>
        <li>Basis 64</li>
        <li>hexadezimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Daten</td>
        <td>Geben Sie die Daten ein, aus denen Sie die Signatur erstellen möchten, oder ordnen Sie sie zu.</td>
    </tr>
</table>

### Entschlüsseln einer PGP-Nachricht

Mit diesem Modul können Sie eine Nachricht mit öffentlichen und privaten Schlüsseln entschlüsseln.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Privater Schlüssel]</td>
        <td>Privaten Schlüssel des Empfängers auswählen, der für diese Nachricht verwendet werden soll. Um einen privaten Schlüssel hinzuzufügen, klicken Sie auf <b>Hinzufügen</b> und geben Sie den Namen des Schlüssels, den Schlüsseltext und die Passphrase ein.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Öffentlicher Schlüssel]</td>
        <td>Geben Sie den öffentlichen Schlüssel des Absenders ein. Dadurch kann die Identität des Absenders authentifiziert werden.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Nachricht]</td>
        <td>Ordnen Sie die Nachricht zu, die Sie entschlüsseln möchten.</td>
    </tr>
</table>

### Verschlüsseln einer PGP-Nachricht

Dieses Modul ermöglicht die Verschlüsselung von Nachrichten mit öffentlichen und privaten Schlüsseln.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Privater Schlüssel]</td>
        <td>Geben Sie den privaten Schlüssel des Absenders ein. Dadurch kann die Identität des Absenders authentifiziert werden.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Öffentlicher Schlüssel]</td>
        <td>Geben Sie den öffentlichen Schlüssel des Empfängers ein.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Nachricht]</td>
        <td>Geben Sie die Nachricht ein, die Sie verschlüsseln möchten.</td>
    </tr>
    </table>
