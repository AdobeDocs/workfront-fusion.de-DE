---
title: HTTP &gt; Andere Module
description: Die  [!DNL Adobe Workfront Fusion] -HTTP-App bietet verschiedene Module für die Kommunikation auf der Grundlage des Hypertext Transfer Protocol (HTTP). HTTP ist die Grundlage der Datenkommunikation für das World Wide Web. Sie können die Module verwenden, um Web-Seiten und -Dateien herunterzuladen, Webhooks und API-Endpunkte aufzurufen usw.
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# HTTP > Andere Module

>[!NOTE]
>
>[!UICONTROL Adobe Workfront Fusion] benötigt zusätzlich zu einer [!UICONTROL Adobe Workfront] eine [!UICONTROL Adobe Workfront Fusion].

Die [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] App bietet verschiedene Module für die Kommunikation auf der Grundlage des Hypertext Transfer Protocol (HTTP). HTTP ist die Grundlage der Datenkommunikation für das World Wide Web. Sie können die Module verwenden, um Web-Seiten und -Dateien herunterzuladen, Webhooks und API-Endpunkte aufzurufen usw.

Die richtige Auswahl des Moduls hängt vom Authentifizierungs-/Autorisierungsmechanismus der Ressource ab, auf die Sie zugreifen möchten. Im Folgenden finden Sie Beispiele für -Module

* Anfrage stellen: Das universelle Modul ist hauptsächlich für Ressourcen bestimmt, die keine Art von Authentifizierung/Autorisierung verwenden
* Eine einfache Authentifizierungsanfrage stellen: für Ressourcen, die [!DNL HTTP] Standardauthentifizierung (BA) verwenden
* Erstellen einer OAuth 2.0-Anfrage: für Ressourcen, die das OAuth 2.0-Autorisierungsprotokoll verwenden
* Erstellen einer Client-Zertifikat-Authentifizierungsanfrage: für Ressourcen, die ein Autorisierungsprotokoll verwenden, das ein Client-seitiges Zertifikat erfordert.
* Erstellen einer API-Schlüsselautorisierungsanfrage: für Ressourcen, die API-Schlüssel zur Autorisierung verwenden.

>[!NOTE]
>
>Wenn Sie eine Verbindung zu einem Adobe-Produkt herstellen, das derzeit über keinen dedizierten Connector verfügt, empfehlen wir die Verwendung des Adobe Authenticator-Moduls.
>
>Weitere Informationen finden Sie unter [Adobe Authenticator-Modul](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

## Anforderungsmodule

Spezifische Anweisungen für das Anforderungsmodul finden Sie in den folgenden Artikeln:

* [[!UICONTROL HTTP] > [!UICONTROL Make a request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make a Basic Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make a Client Certificate Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an API Key Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## Andere Aktionsmodule

* [[!UICONTROL Get a File]](#get-a-file)
* [[!UICONTROL Resolve a target URL]](#resolve-a-target-url)

### [!UICONTROL Get a File]

Dieses Aktionsmodul lädt eine Datei von der angegebenen URL herunter. Nachdem die Datei heruntergeladen wurde, können Sie die Datei mit anderen Modulen im Szenario weiter verarbeiten (die Dateidaten zuordnen).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Geben Sie die URL der Datei ein, die Sie herunterladen möchten, oder mappen Sie sie. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Resolve a target URL]

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
   <td role="rowheader">[!UICONTROL Method] </td> 
   <td> <p>Wählen Sie aus, ob Sie die [!UICONTROL HEAD]- oder die [!UICONTROL GET] verwenden möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Iterator-Module

### [!UICONTROL Retrieve headers]

Dieses Modul gibt jede Kopfzeile (Name und Wert) des angegebenen HTTP-Moduls in einem separaten Bundle zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
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
