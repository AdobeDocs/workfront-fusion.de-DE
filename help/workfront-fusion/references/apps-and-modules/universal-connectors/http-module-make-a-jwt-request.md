---
title: HTTP > Erstellen eines JWT-Anforderungsmoduls
description: Das Adobe Workfront Fusion-HTTP-Anforderungsmodul Erstellen einer JWT-Anforderung sendet eine HTTP(S)-Anforderung an eine URL und autorisiert sie mit einem JSON-Web-Token, das von Fusion automatisch signiert wird.
author: Becky
feature: Workfront Fusion
exl-id: 2f8c0b0d-085a-4b49-b350-4fd4cca1d0a7
TQID: 'https://experienceleague.adobe.com/'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 5e6403abee4e5767da9134529b9e88070bad5f44
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 11%
---
# [!UICONTROL HTTP] > [!UICONTROL JWT-Anfrage stellen]-Modul

Das Adobe Workfront Fusion [!UICONTROL HTTP] > [!UICONTROL Erstellen einer JWT-Anfrage]-Modul sendet eine HTTP(S)-Anfrage an eine URL und autorisiert sie mit einem JSON Web Token (JWT), das das Modul bei jedem Aufruf für Sie signiert. Die Antwort wird dann auf die gleiche Weise verarbeitet wie im standardmäßigen Modul [!UICONTROL HTTP] > [!UICONTROL Anfrage erstellen].

Dieses Modul verhält sich wie das standardmäßige Modul [!UICONTROL Anfrage stellen] mit einem Hauptunterschied: Es signiert automatisch ein JWT aus den von Ihnen angegebenen Ansprüchen und fügt es standardmäßig wie `Authorization: Bearer <token>` zur Anfrage hinzu.

Verwenden Sie dieses Modul, um jede API aufzurufen, die ein signiertes JWT für die Authentifizierung erwartet, z. B. Services, die ein kurzlebiges Bearer-Token erfordern, das mit einem gemeinsamen geheimen Schlüssel (Shared Secret, HMAC) oder einem privaten Schlüssel (RSA/ECDSA) signiert ist, ohne das Token in einem separaten Schritt zu erstellen.

Wenn die API OAuth 2.0, Standardauthentifizierung, einen API-Schlüssel oder ein Client-Zertifikat verwendet, verwenden Sie stattdessen das entsprechende dedizierte HTTP-Modul.

>[!NOTE]
>
>Wenn Sie eine Verbindung zu einem Adobe-Produkt herstellen, das derzeit über keinen dedizierten Connector verfügt, empfehlen wir die Verwendung des Adobe Authenticator-Moduls.
>
>Weitere Informationen finden Sie unter [Adobe Authenticator-Modul](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Ein beliebiges Adobe Workfront Workflow- und Adobe Workfront Automation and Integration-Paket</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: Verfügbar für Organisationen mit betriebsbasierten Lizenzen</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Erstellen einer JWT-Verbindung

Das Modul erfordert eine JWT-Verbindung. Die Verbindung speichert das Signaturmaterial, sodass der geheime oder private Schlüssel nicht im Szenario angezeigt werden muss.

### Erstellen einer JWT-Verbindung in Fusion

1. Fügen Sie das Modul [!UICONTROL HTTP] > [!UICONTROL JWT-Anfrage ]) zu Ihrem Szenario hinzu.
1. Klicken Sie **[!UICONTROL Hinzufügen]** neben dem Feld **[!UICONTROL Verbindung]**.
1. Konfigurieren Sie die Verbindungsfelder:

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader"><p>Verbindungsname</p></td>
      <td><p>Geben Sie einen Namen für die Verbindung ein.</p></td>
     </tr>
     <tr>
      <td role="rowheader"><p>Algorithmus</p></td>
      <td>
       <p>Wählen Sie den Signaturalgorithmus für die Verbindung aus.</p>
       <ul>
        <li><code>HS256</code></li>
        <li><code>HS384</code></li>
        <li><code>HS512</code></li>
        <li><code>RS256</code></li>
        <li><code>RS384</code></li>
        <li><code>RS512</code></li>
        <li><code>PS256</code></li>
        <li><code>PS384</code></li>
        <li><code>PS512</code></li>
        <li><code>ES256</code></li>
        <li><code>ES384</code></li>
        <li><code>ES512</code></li>
       </ul>
      </td>
     </tr>
     <tr>
      <td role="rowheader"><p>Geheimnis</p></td>
      <td>
       <p>Geben Sie den Signaturschlüssel ein.</p>
       <ul>
        <li>Verwenden Sie für <code>HS*</code> Algorithmen die Zeichenfolge Gemeinsamer geheimer Schlüssel .</li>
        <li>Verwenden Sie für <code>RS*</code>-, <code>PS*</code>- und <code>ES*</code>-Algorithmen den PEM-kodierten privaten Schlüssel.</li>
       </ul>
      </td>
     </tr>
    </tbody>
   </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung herzustellen und zum Modul zurückzukehren.

>[!IMPORTANT]
>
>Eine JWT-Verbindung signiert nur mit einem Algorithmus. Wenn für Ihr Szenario mehr als ein Signaturalgorithmus erforderlich ist, erstellen Sie für jeden Algorithmus eine separate Verbindung. Dies entspricht dem vorhandenen Verhalten der eigenständigen JWT-App.

## [!UICONTROL HTTP] > [!UICONTROL Erstellen einer JWT-Anfrage] Modul und seine Felder

Wenn Sie das Modul [!UICONTROL HTTP] > [!UICONTROL JWT-Anfrage ]) konfigurieren, zeigt Adobe Workfront Fusion die unten aufgeführten Felder in der gleichen Reihenfolge an, in der sie in der Modulbenutzeroberfläche angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld. Als erweitert markierte Felder werden ausgeblendet, es sei denn, Sie wählen **[!UICONTROL Erweiterte Einstellungen anzeigen]** aus.

<table style="table-layout:auto">
 <col>
 <col>
 <tbody>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Verbindung]</p></td>
   <td><p>Wählen Sie eine vorhandene JWT-Verbindung aus oder erstellen Sie eine neue.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL URL]</p></td>
   <td><p>Die Ziel-URL für die Anfrage.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Methode]</p></td>
   <td><p>HTTP-Methode wie GET, POST, PUT, PATCH oder DELETE.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Header]</p></td>
   <td><p>Benutzerdefinierte Anfragekopfzeilen im Schlüssel/Wert-Format.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Abfragezeichenfolge]</p></td>
   <td><p>Parameter der Abfragezeichenfolge im Schlüssel/Wert-Format.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Texttyp]</p></td>
   <td><p>Kodierung des Anfragetexts. Die Optionen umfassen Raw, application/x-www-form-urlencoded und multipart/form-data.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Parse response]</p></td>
   <td><p>Wenn diese Option aktiviert ist, analysiert Fusion den Antworttext anhand des Inhaltstyps der Antwort.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL JWT-Payload (Ansprüche)]</p></td>
   <td><p>Schlüssel/Wert-Paare, die als Ansprüche in der JWT-Payload enthalten sind. Die reservierten Ansprüche <code>exp</code>, <code>iat</code> und <code>nbf</code> müssen ein NumericDate sein - eine Anzahl von Sekunden seit der Unix-Epoche. Anspruchswerte behalten ihren JSON-Typ bei, sodass Zahlen Zahlen Zahlen und Boolesche Werte bleiben.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Timeout] (erweitert)</p></td>
   <td><p>Angeben des Zeitlimits für Anfragen in Sekunden (1-300). Der Standardwert ist 40 Sekunden.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Wiederholungsanzahl] (erweitert)</p></td>
   <td><p>Geben Sie an, wie oft die Anfrage erneut versucht werden soll, wenn die Anfrage aufgrund eines wiederholbaren Fehlers fehlschlägt.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Zusätzliche Wiederholungsstatus-Codes] (erweitert)</p></td>
   <td><p>Geben Sie zusätzliche HTTP-Status-Codes an, die als wiederholbar behandelt werden sollen.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Cookies für andere HTTP-Module freigeben] (erweitert)</p></td>
   <td><p>Aktivieren Sie diese Option, um Cookies vom Server für alle HTTP-Module in Ihrem Szenario freizugeben.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Selbstsigniertes Zertifikat] (erweitert)</p></td>
   <td><p>Laden Sie Ihr Zertifikat hoch, wenn Sie TLS mit Ihrem selbstsignierten Zertifikat verwenden möchten.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL lehnen Verbindungen ab, die nicht verifizierte (selbstsignierte) Zertifikate verwenden] (erweitert)</p></td>
   <td><p>Aktivieren Sie diese Option, um Verbindungen abzulehnen, die nicht verifizierte TLS-Zertifikate verwenden.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Weiterleitung folgen] (erweitert)</p></td>
   <td><p>Aktivieren Sie diese Option, um den URL-Umleitungen mit 3xx-Antworten zu folgen.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Serialisierung mehrerer derselben Abfragezeichenfolgen-Schlüssel als Arrays deaktivieren] (erweitert)</p></td>
   <td><p>Standardmäßig verarbeitet Workfront Fusion mehrere Werte für denselben URL-Abfragezeichenfolgen-Parameterschlüssel wie Arrays. Beispielsweise wird <code>www.test.com?foo=bar&amp;foo=baz</code> in <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code> konvertiert. Aktivieren Sie diese Option, um diese Funktion zu deaktivieren.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Komprimierten Inhalt anfordern] (erweitert)</p></td>
   <td><p>Aktivieren Sie diese Option, um eine komprimierte Version der Website anzufordern. Fügt eine <code>[!UICONTROL Accept-Encoding]</code>-Kopfzeile hinzu, um komprimierten Inhalt anzufordern.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Use Mutual TLS] (erweitert)</p></td>
   <td><p>Aktivieren Sie diese Option, um gegenseitiges TLS in der HTTP-Anfrage zu verwenden.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Sign Options] (Erweitert)</p></td>
   <td><p>Klicken Sie für jede Vorzeichenoption, die Sie der Anfrage hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Namen und Wert des Parameters ein.</p><p>Zusätzliche an den JWT-Signierer übergebene Optionen, z. B. <code>expiresIn</code>, <code>issuer</code>, <code>audience</code>, <code>subject</code> und <code>keyid</code>. Dauerwerte wie <code>expiresIn</code> werden von der <code>jsonwebtoken</code>-Bibliothek interpretiert. Eine einfache Zahl wird als Millisekunden behandelt. Verwenden Sie daher eine Einheitszeichenfolge wie <code>"1h"</code> oder <code>"3600s"</code>, um explizit zu sein. Der Algorithmus wird aus der Verbindung übernommen und kann hier nicht überschrieben werden.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Header Name] (erweitert)</p></td>
   <td><p>Geben Sie den Namen des Anfrage-Headers ein, der das signierte JWT erhält, oder ordnen Sie ihn zu. Standard: <code>Authorization</code>. Der Kopfzeilenname darf keinen Punkt enthalten (<code>.</code>), da gepunktete Namen abgelehnt werden und nicht in Anfrageprotokollen maskiert werden können.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Token-Typ] (erweitert)</p></td>
   <td><p>Geben Sie das Authentifizierungsschema ein, das vor dem Token platziert wurde, z. B. <code>Bearer</code>, oder ordnen Sie es zu. Lassen Sie dieses Feld leer, um das rohe Token ohne Präfix zu senden.</p></td>
  </tr>
 </tbody>
</table>

## So wird das Token erstellt

1. Das Modul erfasst die Ansprüche im Feld [!UICONTROL JWT-Payload (Ansprüche].
1. Reservierte Ansprüche wie <code>exp</code>, <code>iat</code>, und <code>nbf</code> werden in numerische Datumswerte konvertiert.
1. Das Modul wendet die [!UICONTROL Signaturoptionen] an und signiert das Token mit dem Algorithmus aus der Verbindung.
1. Das signierte Token wird in der Anfrage-Kopfzeile platziert, die durch [!UICONTROL Kopfzeilenname) definiert ].
1. Wenn [!UICONTROL Token Type] festgelegt ist, fügt das Modul das Präfix vor dem Token hinzu. Beispiel: <code>Bearer eyJ…</code>.
1. Die Anfrage wird gesendet und die Antwort wird auf die gleiche Weise verarbeitet wie das standardmäßige Modul [!UICONTROL HTTP] > [!UICONTROL Anfrage erstellen].

Das signierte Token wird automatisch in Debug- und Fehlerprotokollen maskiert, sodass es nie offen gelegt wird.

## Beispiel

### Verbindung

- Algorithmus: `HS256`
- Geheim: `my-shared-secret`

### Moduleinstellungen

- URL: `https://api.example.com/v1/orders`
- Methode: `GET`
- JWT-Payload (Ansprüche):
  - `sub` = `service-account-42`
  - `iss` = `make-integration`
- Unterschriftsoptionen:
  - `expiresIn` = `1h`
- Kopfzeilenname: `Authorization`
- Token-Typ: `Bearer`

### Ergebnis

Das -Modul sendet die Anfrage mit einer -Kopfzeile, die ähnlich sieht:

```text
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

## Häufig gestellte Fragen/Gotchas

### Warum ist mein Token so schnell abgelaufen?

Sie haben wahrscheinlich eine reine Zahl für `expiresIn` wie `3600` eingegeben. Die `jsonwebtoken`-Bibliothek interpretiert einfache Zahlen als Millisekunden. Verwenden Sie stattdessen eine Einheitenzeichenfolge wie `"1h"` oder `"3600s"`.

### Wann wird das Token erstellt?

Das Modul signiert jedes Mal ein neues JWT, wenn das Modul ausgeführt wird, nicht beim Erstellen der Verbindung. Die Verbindung speichert nur das Signaturmaterial und den Algorithmus, sodass Ansprüche wie `iat` und `exp` den Zeitpunkt des Moduldurchgangs widerspiegeln.

Wenn die Anfrage innerhalb derselben Modulausführung erneut versucht wird, verwendet Fusion für diese Wiederholungsversuche dasselbe signierte Token, anstatt für jeden Versuch ein neues Token zu signieren. Aus diesem Grund kann ein sehr kurzer `expiresIn` ablaufen, bevor ein erneuter Versuch stattfindet, was dazu führen kann, dass ein bereits abgelaufenes Token erneut gesendet wird. Um dies zu vermeiden, verwenden Sie eine klare Einheitenzeichenfolge wie `"1h"` oder `"3600s"` und vermeiden Sie zu kurze Token-Lebensdauern.

### Kann ich den Algorithmus pro Anfrage ändern?

Nein. Der Algorithmus wird durch die -Verbindung festgelegt. Wenn Sie einen anderen Algorithmus benötigen, erstellen Sie eine andere JWT-Verbindung.

### Kann ich das Token in einer benutzerdefinierten Kopfzeile senden?

Ja. Legen Sie [!UICONTROL  Feld &quot;]&quot; auf einen benutzerdefinierten Namen fest, es darf jedoch keinen Punkt (`.`) enthalten.

### Kann ich das Roh-Token ohne `Bearer` senden?

Ja. Lassen Sie [!UICONTROL Token-]&quot; leer.

### Ist das Token in Protokollen sichtbar?

Nein. Das signierte Token wird automatisch in Debug- und Fehlerprotokollen maskiert.


>[!NOTE]
>
>Technischer Hinweis: Beim Signieren wird die `jsonwebtoken`-Bibliothek verwendet und das Signierverhalten der eigenständigen JWT-App gespiegelt, sodass dieselben Eingaben dasselbe Token erzeugen wie die eigenständige JWT-App.
