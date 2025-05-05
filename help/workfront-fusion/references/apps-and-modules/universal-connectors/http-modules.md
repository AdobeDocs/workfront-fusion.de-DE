---
title: HTTP > Andere Module
description: Die  [!DNL Adobe Workfront Fusion] -HTTP-App bietet verschiedene Module für die Kommunikation auf der Grundlage des Hypertext Transfer Protocol (HTTP). HTTP ist die Grundlage der Datenkommunikation für das World Wide Web. Sie können die Module verwenden, um Web-Seiten und -Dateien herunterzuladen, Webhooks und API-Endpunkte aufzurufen usw.
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# HTTP > Andere Module

Die [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP]-App bietet verschiedene Module für die Kommunikation auf der Grundlage des Hypertext Transfer Protocol (HTTP)-Protokolls. HTTP ist die Grundlage der Datenkommunikation für das World Wide Web. Sie können die Module verwenden, um Web-Seiten und -Dateien herunterzuladen, Webhooks und API-Endpunkte aufzurufen usw.

Die richtige Auswahl des Moduls hängt vom Authentifizierungs-/Autorisierungsmechanismus der Ressource ab, auf die Sie zugreifen möchten. Im Folgenden finden Sie Beispiele für -Module

* **Anfrage stellen**: Hauptsächlich für Ressourcen bestimmt, die keine Art von Authentifizierung oder Autorisierung verwenden
* **Eine einfache Authentifizierungsanfrage stellen**: Für Ressourcen, die [!DNL HTTP] Standardauthentifizierung (BA) verwenden
* **Erstellen einer OAuth 2.0-Anfrage**: Für Ressourcen, die das OAuth 2.0-Autorisierungsprotokoll verwenden
* **Erstellen einer Client-Zertifikat-Authentifizierungsanfrage**: Für Ressourcen mit einem Autorisierungsprotokoll, für das ein Client-seitiges Zertifikat erforderlich ist
* **Erstellen einer API-Schlüssel-Autorisierungsanfrage**: Für Ressourcen, die API-Schlüssel für die Autorisierung verwenden

>[!NOTE]
>
>Wenn Sie eine Verbindung zu einem Adobe-Produkt herstellen, das derzeit über keinen dedizierten Connector verfügt, empfehlen wir die Verwendung des Adobe Authenticator-Moduls.
>
>Weitere Informationen finden Sie unter [Adobe Authenticator-Modul](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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

## Anforderungsmodule

Spezifische Anweisungen für das Anforderungsmodul finden Sie in den folgenden Artikeln:

* [[!UICONTROL HTTP] > [!UICONTROL Anfrage stellen] Modul](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Erstellen einer einfachen Autorisierungsanfrage]-Modul](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL OAuth 2.0-Anfrage stellen] Modul](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Erstellen einer Client-Zertifikatautorisierungsanfrage] Modul](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Erstellen einer API-Schlüssel-Autorisierungsanfrage]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## Andere Aktionsmodule

* [[!UICONTROL Datei abrufen]](#get-a-file)
* [[!UICONTROL Auflösen einer Ziel-URL]](#resolve-a-target-url)

### [!UICONTROL Datei abrufen]

Dieses Aktionsmodul lädt eine Datei von der angegebenen URL herunter. Nachdem die Datei heruntergeladen wurde, können Sie die Datei mit anderen Modulen im Szenario weiter verarbeiten (die Dateidaten zuordnen).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Alle Status als Fehler auswerten (außer 2xx und 3xx )] </td> 
   <td> <p>Mit dieser Option können Sie die Fehlerbehandlung einrichten.</p> <p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Fehlerbehandlung in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Geben Sie die URL der Datei ein, die Sie herunterladen möchten, oder mappen Sie sie. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Cookies für andere HTTP-Module freigeben] </td> 
   <td> <p>Aktivieren Sie diese Option, wenn die Cookies für diese Website für andere Module verfügbar sein sollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Auflösen einer Ziel-URL]

Dieses Aktionsmodul löst eine Kette von HTTP-Umleitungen auf und gibt eine Ziel-URL zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Geben Sie die URL ein, die Sie auflösen möchten, oder ordnen Sie sie zu, z. B. eine [!DNL bit.ly] URL.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Methode] </td> 
   <td> <p>Wählen Sie aus, ob Sie die Methode [!UICONTROL HEAD] oder die Methode [!UICONTROL GET] verwenden möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Iterator-Module

### [!UICONTROL Kopfzeilen abrufen]

Dieses Modul gibt jede Kopfzeile (Name und Wert) des angegebenen HTTP-Moduls in einem separaten Bundle zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Modul]</td> 
   <td> <p> Wählen Sie das Modul aus, aus dem Sie die Kopfzeilen abrufen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Generieren von JSON Web Token (JWT)

Es ist möglich, mithilfe integrierter Funktionen ein JWT-Token zu generieren:

Kopfzeile:

![JWT-Header](/help/workfront-fusion/references/apps-and-modules/assets/jwt-header-350x19.png)

Code zum Kopieren und Einfügen:

```
{{replace(replace(replace(base64("{""alg"":""HS256"",""typ"":""JWT""}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Payload:

![JWT-Payload](/help/workfront-fusion/references/apps-and-modules/assets/jwt-payload-350x17.png)

Code zum Kopieren und Einfügen:

```
{{replace(replace(replace(base64("{""iss"":""key"",""exp"":" + (timestamp + 60) + "}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Token:

![JWT-Token](/help/workfront-fusion/references/apps-and-modules/assets/jwt-token-350x15.png)

Code zum Kopieren und Einfügen:

```
{{1.value}}.{{2.value}}.{{replace(replace(replace(sha256(1.value + "." + 2.value; "base64"; "secret"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```
