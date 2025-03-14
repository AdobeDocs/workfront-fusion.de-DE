---
title: HTTP > Erstellen eines OAuth 2.0-Anfragemoduls
description: Um eine HTTP [!DNL Adobe Workfront Fusion] S-Anfrage an Server zu senden, für die eine OAuth 2.0-Autorisierung erforderlich ist, müssen Sie zunächst eine OAuth-Verbindung erstellen. [!DNL Adobe Workfront Fusion] Stellt sicher, dass alle Aufrufe, die mit dieser Verbindung getätigt werden, über die entsprechenden Autorisierungskopfzeilen verfügen und die zugehörigen Token bei Bedarf automatisch aktualisieren.
author: Becky
feature: Workfront Fusion
exl-id: a302a1d4-fddf-4a71-adda-6b87ff7dba4b
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2256'
ht-degree: 0%

---

# [!UICONTROL HTTP] > [!UICONTROL OAuth 2.0-Anfrage stellen] Modul

>[!NOTE]
>
>[!DNL Adobe Workfront Fusion] benötigt zusätzlich zu einer [!DNL Adobe Workfront] eine [!DNL Adobe Workfront Fusion].

Um eine [!DNL Adobe Workfront Fusion] HTTP(S)-Anfrage an Server zu senden, für die eine OAuth 2.0-Autorisierung erforderlich ist, müssen Sie zunächst eine OAuth-Verbindung erstellen. [!DNL Adobe Workfront Fusion] stellt sicher, dass alle Aufrufe, die mit dieser Verbindung getätigt werden, über die entsprechenden Autorisierungskopfzeilen verfügen und die zugehörigen Token bei Bedarf automatisch aktualisieren.

[!DNL Workfront Fusion] unterstützt die folgenden OAuth 2.0-Authentifizierungsflüsse:

* Autorisierungs-Code-Fluss
* impliziter Fluss

Andere Flüsse, z. B. Fluss der Anmeldeinformationen des Ressourcenbesitzers und Fluss der Client-Anmeldeinformationen, werden über dieses Modul nicht automatisch unterstützt.

Weitere Informationen zur OAuth 2.0-Authentifizierung finden Sie unter [OAuth 2.0-Autorisierungs-Framework](https://tools.ietf.org/html/rfc6749).

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

## Erstellen einer Verbindung für eine [!DNL OAuth]

* [Allgemeine Anweisungen zum Erstellen einer Verbindung im HTTP > Erstellen eines OAuth 2.0-Anfragemoduls](#general-instructions-for-creating-a-connection-in-the-http--make-an-oauth-20-request-module)
* [Anweisungen zum Erstellen einer Verbindung zu Google finden Sie unter http > [!UICONTROL Erstellen] eines OAuth 2.0-Anfragemoduls](#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module)
* [Anleitung zum Herstellen einer Verbindung zur Microsoft Graph API über HTTP > Erstellen einer OAuth 2.0-Anfrage](#instructions-for-connecting-to-microsoft-graph-api-via-the-http--make-an-oauth-20-request-module)

### Allgemeine Anweisungen zum Erstellen einer Verbindung im Modul [!UICONTROL HTTP] > [!UICONTROL OAuth 2.0-Anfrage]

1. Erstellen Sie im [!DNL target] einen OAuth-Client, mit dem Sie kommunizieren [!DNL Adobe Workfront Fusion]. Diese Option befindet sich höchstwahrscheinlich im Abschnitt [!UICONTROL Entwickler] des angegebenen Service.

   1. Geben Sie beim Erstellen eines Clients die entsprechende URL in das Feld `[!UICONTROL Redirect URL]` oder `[!UICONTROL Callback URL]` ein:

      | Nord- und Südamerika/APAC | `https://app.workfrontfusion.com/oauth/cb/oauth2` |
      |---|---|
      | **EMEA** | `https://app-eu.workfrontfusion.com/oauth/cb/oauth2` |

   1. Nachdem Sie den Client erstellt haben, zeigt der angegebene Dienst zwei Schlüssel an: `[!UICONTROL Client ID]` und `[!UICONTROL Client Secret]`. Einige Dienste nennen diese `[!UICONTROL App Key]` und `[!UICONTROL App Secret]`. Speichern Sie den Schlüssel und die geheimen Daten an einem sicheren Speicherort, damit Sie sie beim Erstellen der Verbindung in Workfront Fusion bereitstellen können.

1. Die `[!UICONTROL Authorize URI]` und `[!UICONTROL Token URI]` finden Sie in der API-Dokumentation des jeweiligen Service. Dies sind URL-Adressen, über die [!DNL Workfront Fusion] mit dem [!DNL target]-Service kommuniziert. Die Adressen dienen zur OAuth-Autorisierung.

   >[!NOTE]
   >
   >Wenn der Service den impliziten Fluss verwendet, benötigen Sie nur die `[!UICONTROL Authorize URI]` .

1. (Bedingt) Wenn der Ziel-Service Bereiche (Zugriffsrechte) verwendet, überprüfen Sie, wie der Service einzelne Bereiche trennt, und stellen Sie sicher, dass Sie das Trennzeichen in den erweiterten Einstellungen entsprechend festlegen. Wenn das Trennzeichen nicht richtig festgelegt ist, kann [!DNL Workfront Fusion] die Verbindung nicht erstellen, und es wird ein Fehler wegen ungültigem Bereich angezeigt.
1. Nachdem Sie die oben genannten Schritte ausgeführt haben, können Sie in [!DNL Workfront Fusion] mit der Erstellung der OAuth-Verbindung beginnen. Fügen Sie Ihrem Szenario das Modul HTTP > OAuth 2-Anfrage erstellen hinzu.
1. Klicken Sie im Feld Verbindung des Moduls auf **[!UICONTROL Hinzufügen]**.

1. Füllen Sie die folgenden Felder aus, um eine Verbindung zu erstellen:

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Verbindungsname] </td> 
      <td> <p>Geben Sie den Namen der Verbindung ein.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Umgebung] </td> 
      <td> <p>Wählen Sie aus, ob Sie eine Produktions- oder Nicht-Produktionsumgebung verwenden.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Typ] </td> 
      <td> <p>Wählen Sie aus, ob Sie ein Service-Konto oder ein persönliches Konto verwenden.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL-Flusstyp]</p> </td> 
      <td> <p>Fluss zum Abrufen von Token auswählen.</p> 
       <ul> 
        <li><strong>[!UICONTROL Autorisierungs-Code]</strong>: Geben Sie die <code>[!UICONTROL Authorize URI]</code> und <code>[!UICONTROL Token URI]</code> aus der API-Dokumentation des Services ein.</li> 
        <li><strong>[!UICONTROL implicit]</strong>: Geben Sie den <code>[!UICONTROL Authorize URI]</code> aus der API-Dokumentation des Services ein.</li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL-Umfang] </td> 
      <td> <p>Individuelle Bereiche hinzufügen. Diese Informationen finden Sie in der Entwicklerdokumentation (API) des jeweiligen Services.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL-Bereichstrennzeichen] </td> 
      <td> <p>Wählen Sie aus, durch welche Bereiche oben getrennt werden soll. Diese Informationen finden Sie in der Entwicklerdokumentation (API) des jeweiligen Services.</p> <p>Warnung: Wenn das Trennzeichen nicht richtig festgelegt ist, kann [!DNL Workfront Fusion] die Verbindung nicht erstellen und Sie erhalten einen Fehler wegen ungültigem Bereich.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client-ID] </td> 
      <td> <p>Geben Sie die Client-ID ein. Sie haben die Client-ID erhalten, als Sie einen OAuth-Client in dem Service erstellt haben, den Sie verbinden möchten.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client-Geheimnis]</td> 
      <td> <p> Geben Sie den geheimen Client-Schlüssel ein. Sie haben das Client-Geheimnis erhalten, als Sie einen OAuth-Client in dem Service erstellt haben, zu dem Sie eine Verbindung herstellen möchten.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Parameter autorisieren]</p> </td> 
      <td> <p>Fügen Sie alle Parameter hinzu, die Sie in den Autorisierungsaufruf aufnehmen möchten. Die folgenden Standardparameter werden immer automatisch eingefügt und müssen nicht hinzugefügt werden.</p> <p>Standardparameter:</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL response_type]</strong> </p> <p> <code>code </code>für [!UICONTROL Authorization Code Flow] und <code>token </code>für [!UICONTROL Implicit Flow]</p> </li> 
        <li> <p><strong>[!UICONTROL redirect_uri]</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">Nord- und Südamerika/APAC</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong> </p> <p> Die Client-ID, die Sie beim Erstellen des Kontos erhalten haben</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Zugriffstokenparameter]</p> </td> 
      <td> <p>Fügen Sie alle Parameter hinzu, die Sie in den Token-Aufruf aufnehmen möchten. Die folgenden Standardparameter werden immer automatisch eingefügt und müssen nicht hinzugefügt werden.</p> <p>Standardparameter:</p> 
       <ul> 
        <li><strong>[!UICONTROL grant_type]</strong>: <code>authorization_code</code></li> 
        <li> <p><strong>[!UICONTROL redirect_uri]:</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">Nord- und Südamerika/APAC</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li><strong>[!UICONTROL client_id]</strong>: Die Client-ID, die Sie beim Erstellen des Kontos erhalten haben, wird automatisch in den Anfragetext aufgenommen</li> 
        <li><strong>client_secret</strong>: Das Client-Geheimnis, das Sie beim Erstellen des Kontos erhalten haben, wird automatisch im Anfrageinhalt enthalten</li> 
        <li><strong>code</strong>: Der von der Autorisierungsanfrage zurückgegebene Code</li> 
       </ul> <p>Hinweis:  <p>Der OAuth 2.0-Standard unterstützt in diesem Schritt mindestens zwei Methoden der Client-Authentifizierung (<code>[!UICONTROL client_secret_basic]</code> und <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] sendet die angegebene Client-ID und das angegebene Geheimnis automatisch über die <code>[!UICONTROL client_secret_post]</code>. Daher werden diese Parameter automatisch als Teil des Textkörpers der Token-Anfrage einbezogen. </p> <p>Weitere Informationen zur OAuth 2.0-Authentifizierung finden Sie unter <a href="https://tools.ietf.org/html/rfc6749">OAuth 2.0-Autorisierungs-Framework</a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Token-Parameter aktualisieren]</p> </td> 
      <td> <p>Fügen Sie alle Parameter hinzu, die Sie in den Token-Aufruf aufnehmen möchten. Die folgenden Standardparameter werden immer automatisch eingefügt und müssen nicht hinzugefügt werden.</p> <p>Standardparameter:</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL grant_type]</strong>: <code>refresh_token</code></p> </li> 
        <li> <p><strong>[!UICONTROL refresh_token]</strong>: Das letzte Aktualisierungstoken, das von dem Service erhalten wurde, mit dem Sie eine Verbindung herstellen</p> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong>: Die Client-ID, die Sie beim Erstellen des Kontos erhalten haben, wird automatisch in den Anfragetext aufgenommen</p> </li> 
        <li> <p><strong>[!UICONTROL client_secret]</strong>: Das Client-Geheimnis, das Sie beim Erstellen des Kontos erhalten haben, wird automatisch im Anfrageinhalt enthalten</p> </li> 
       </ul> <p>Hinweis:  <p>Der OAuth 2.0-Standard unterstützt in diesem Schritt mindestens zwei Methoden der Client-Authentifizierung (<code>[!UICONTROL client_secret_basic]</code> und <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] sendet die angegebene Client-ID und das angegebene Geheimnis automatisch über die <code>[!UICONTROL client_secret_post]</code>. Daher werden diese Parameter automatisch als Teil des Textkörpers der Token-Anfrage einbezogen. </p> <p>Weitere Informationen zur OAuth 2.0-Authentifizierung finden Sie unter <a href="https://tools.ietf.org/html/rfc6749">OAuth 2.0-Autorisierungs-Framework</a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Benutzerdefinierte Kopfzeilen]</p> </td> 
      <td> <p>Geben Sie alle zusätzlichen Schlüssel und Werte an, die in die Kopfzeile der Schritte [!UICONTROL Token] und [!UICONTROL Aktualisierungstoken] aufgenommen werden sollen.</p> <p>Hinweis:  <p>Der OAuth 2.0-Standard unterstützt in diesem Schritt mindestens zwei Methoden der Client-Authentifizierung (<code>[!UICONTROL client_secret_basic]</code> und <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] unterstützt die <code>[!UICONTROL client_secret_basic]</code> nicht automatisch. Wenn der Service, mit dem Sie eine Verbindung herstellen, erwartet, dass die Client-ID und das Client-Geheimnis in einer einzigen Zeichenfolge kombiniert und dann base64 in der Autorisierungs-Kopfzeile codiert werden, sollten Sie diese Kopfzeile und diesen Schlüsselwert hier hinzufügen.</p> <p> Weitere Informationen zur OAuth 2.0-Authentifizierung finden Sie unter <a href="https://tools.ietf.org/html/rfc6749">OAuth 2.0-Autorisierungs-Framework</a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Token-Platzierung]</p> </td> 
      <td> <p>Wählen Sie aus, ob das Token beim Herstellen einer Verbindung zur angegebenen URL im [!UICONTROL-Header], [!UICONTROL-Abfragezeichenfolge] oder in beiden gesendet werden soll.</p> <p>Token werden am häufigsten im Anfrage-Header gesendet.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Header Token Name] </td> 
      <td> <p>Geben Sie den Namen des Autorisierungs-Tokens in die Kopfzeile ein. Standard: <code>[!UICONTROL Bearer]</code>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Abfragezeichenfolgen-Parametername] </td> 
      <td> <p>Geben Sie den Namen des Autorisierungs-Tokens in der Abfragezeichenfolge ein. Standard: <code>[!UICONTROL access_token]</code>.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.
1. Fahren Sie fort mit [Konfigurieren des OAuth 2.0-Anforderungsmoduls](#configure-the-make-an-oauth-20-request-module).

### Anweisungen zum Erstellen einer Verbindung zu [!DNL Google] finden Sie unter [!UICONTROL HTTP] > [!UICONTROL Erstellen einer OAuth 2.0-Anfrage]

Im folgenden Beispiel wird gezeigt, wie das Anforderungsmodul [!UICONTROL HTTP] > [!UICONTROL Erstellen einer OAuth 2.0] für die Verbindung mit [!DNL Google] verwendet wird.

1. Stellen Sie sicher, dass Sie ein Projekt erstellt, OAuth-Einstellungen konfiguriert und Ihre Anmeldeinformationen generiert haben, wie in Artikel [Verbinden [!DNL Adobe Workfront Fusion] mit [!DNL Google Services]  unter Verwendung eines benutzerdefinierten OAuth-Clients ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).
1. Öffnen Sie das Modul [!UICONTROL HTTP] > [!UICONTROL OAuth 2.0-Anfrage ].
1. Klicken Sie in einem beliebigen Modul **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .
1. Geben Sie die folgenden Werte ein:

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Verbindungsname] </td> 
      <td> <p>Geben Sie einen Namen für die Verbindung ein.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Umgebung] </td> 
      <td> <p>Wählen Sie aus, ob Sie eine Produktions- oder Nicht-Produktionsumgebung verwenden.</p> </td> 
     </tr> 
      <tr> 
      <td role="rowheader">[!UICONTROL Typ] </td> 
      <td> <p>Wählen Sie aus, ob Sie ein Service-Konto oder ein persönliches Konto verwenden.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL-Flusstyp]</p> </td> 
      <td> <p>[!UICONTROL Autorisierungs-Code]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL URI autorisieren]</td> 
      <td><code>https://accounts.google.com/o/oauth2/v2/auth</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Token-URI]</td> 
      <td><code>https://www.googleapis.com/oauth2/v4/token</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL-Umfang] </td> 
      <td> <p>Individuelle Bereiche hinzufügen. Weitere Informationen zu Bereichen finden Sie unter <a href="https://developers.google.com/identity/protocols/oauth2/scopes">OAuth 2.O-Bereiche für [!DNL Google] APIs</a> in der [!DNL Google].</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL-Bereichstrennzeichen] </td> 
      <td> <p>[!UICONTROL LEERZEICHEN]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client-ID] </td> 
      <td> <p>Geben Sie Ihre [!DNL Google]-Client-ID ein. </p> <p>Informationen zum Erstellen einer Client-ID finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create-oauth-credentials" class="MCXref xref">Erstellen von OAuth</a> im Artikel [!DNL Connect Adobe Workfront Fusion] zum [!DNL Google Services] mit einem benutzerdefinierten OAuth-Client</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client-Geheimnis]</td> 
      <td> <p>Geben Sie Ihr [!DNL Google]-Client-Geheimnis ein. </p> <p>Informationen zum Erstellen geheimer Client-Daten finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create-oauth-credentials" class="MCXref xref">Erstellen von OAuth</a> im Artikel [!DNL Connect Adobe Workfront Fusion] zu [!DNL Google] Services mithilfe eines benutzerdefinierten OAuth-Clients</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Parameter autorisieren]</p> </td> 
      <td> <p>Fügen Sie <code>[!UICONTROL access_type]</code> - <code>[!UICONTROL offline] </code>Schlüssel-Wert-Paar hinzu.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/google-authentication-http.png"> </p> <p>Hinweis: Wenn Authentifizierungsprobleme auftreten, z. B. bei der Token-Aktualisierung, versuchen Sie, das <code>[!UICONTROL prompt] </code>-/<code>[!UICONTROL consent] </code>-Wertpaar hinzuzufügen.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindungseinstellungen zu speichern.
1. Fahren Sie fort mit [Konfigurieren des OAuth 2.0-Anforderungsmoduls](#configure-the-make-an-oauth-20-request-module).

## Konfigurieren des OAuth 2.0-Anforderungsmoduls

Nachdem Sie eine OAuth 2.0-Verbindung hergestellt haben, fahren Sie mit dem Einrichten des Moduls wie gewünscht fort. Alle Autorisierungs-Token sind automatisch in dieser Anfrage und in jeder anderen Anfrage enthalten, die dieselbe Verbindung verwendet.

Wenn Sie das Modul [!UICONTROL HTTP] > [!UICONTROL OAuth 2.0-Anfrage ]) konfigurieren, zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zu einem anderen Modul in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto">  
 <col> 
 <col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Informationen zum Einrichten einer Verbindung finden Sie unter <a href="#create-a-connection-for-an-oauth-request" class="MCXref xref">Erstellen einer Verbindung für eine OAuth</a>Anfrage in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Alle Status als Fehler auswerten (außer 2xx und 3xx)] </td> 
   <td> <p>Mit dieser Option können Sie die Fehlerbehandlung einrichten.</p> <p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Fehlerbehandlung</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Geben Sie die URL ein, an die Sie eine Anfrage senden möchten, z. B. einen API-Endpunkt, eine Website usw.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Methode]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen] </td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Beispiel: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p> Geben Sie die gewünschten Schlüssel-Wert-Paare für die Abfrage ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Texttyp]</p> </td> 
   <td> <p>Der HTTP-Hauptteil sind die Datenbytes, die in einer HTTP-Transaktionsnachricht unmittelbar nach den -Headern übertragen werden, falls welche verwendet werden sollen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL RAW]</strong> </p> <p>Der Rohtexttyp ist im Allgemeinen für die meisten HTTP-Textkörperanforderungen geeignet, selbst in Situationen, in denen in der Entwicklerdokumentation keine zu sendenden Daten angegeben sind.</p> <p>Geben Sie ein Formular zum Analysieren der Daten im Feld [!UICONTROL Content-Typ] an.</p> <p>Trotz des ausgewählten Inhaltstyps werden Daten in jedem Format eingegeben, das in der Entwicklerdokumentation festgelegt oder erforderlich ist.</p> </li> 
     <li> <p><strong>[!UICONTROL application/x-www-form-urlencoded]</strong> </p> <p>Dieser Hauptteiltyp wird verwendet, um Daten mit <code>[!UICONTROL application/x-www-form-urlencoded]</code> zu posten.</p> <p><code>[!UICONTROL application/x-www-form-urlencoded]</code> besteht der Text der an den Server gesendeten HTTP-Nachricht im Wesentlichen aus einer Abfragezeichenfolge. Schlüssel und Werte werden in Schlüssel-Wert-Paaren codiert, die durch <code>&amp;</code> getrennt sind, wobei zwischen Schlüssel und Wert ein <code>=</code> besteht. </p> <p>Für Binärdaten <code>use [!UICONTROL multipart/form-data]</code> Sie stattdessen .</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>Beispiel: </b></span></span> 
       <p>Beispiel für das daraus resultierende HTTP-Anfrageformat:</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL Multipart/form-data] ist eine mehrteilige HTTP-Anfrage zum Senden von Dateien und Daten. Es wird häufig verwendet, um Dateien auf den Server hochzuladen.</p> <p>Fügen Sie Felder hinzu, die in der Anfrage gesendet werden sollen. Jedes Feld muss ein Schlüssel-Wert-Paar enthalten.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL text]</strong> </p> <p>Geben Sie den Schlüssel und den Wert ein, die innerhalb des Anfragetexts gesendet werden sollen.</p> </li> 
       <li> <p><strong>[!UICONTROL-Datei]</strong> </p> <p>Geben Sie den Schlüssel und anschließend die Quelldatei ein, die Sie im Anfrageinhalt senden möchten.</p> <p>Ordnen Sie die Datei zu, die Sie aus dem vorherigen Modul hochladen möchten (z. B. [!UICONTROL HTTP] &gt; [!UICONTROL Datei abrufen]), oder geben Sie den Dateinamen und die Dateidaten manuell ein.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um Antworten automatisch zu parsen und JSON- und XML-Antworten zu konvertieren, sodass Sie keine [!UICONTROL JSON] &gt; [!UICONTROL Parse JSON]- oder [!UICONTROL XML] &gt; [!UICONTROL Parse XML]-Module verwenden müssen.</p> <p>Bevor Sie geparste JSON- oder XML-Inhalte verwenden können, führen Sie das Modul einmal manuell aus, damit das Modul den Antwortinhalt erkennen und in nachfolgenden Modulen zuordnen kann.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zeitüberschreitung] </td> 
   <td> <p>Geben Sie die Zeitüberschreitung der Anfrage in Sekunden (1-300) ein. Der Standardwert ist 40 Sekunden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Cookies für andere HTTP-Module freigeben]</td> 
   <td> <p> Aktivieren Sie diese Option, um Cookies vom Server für alle HTTP-Module in Ihrem Szenario freizugeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selbstsigniertes Zertifikat]</td> 
   <td> <p>Um ein selbstsigniertes Zertifikat oder einen privaten Schlüssel für TLS zu verwenden, klicken Sie auf <b>Extrahieren</b> und geben Sie die Datei und das Kennwort des Zertifikats oder des privaten Schlüssels an.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL lehnen Verbindungen ab, die nicht verifizierte (selbstsignierte) Zertifikate verwenden] </td> 
   <td> <p>Aktivieren Sie diese Option, um Verbindungen abzulehnen, die nicht verifizierte TLS-Zertifikate verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Weiterleitung folgen]</td> 
   <td> <p> Aktivieren Sie diese Option, um den URL-Umleitungen mit 3xx-Antworten zu folgen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Alle Weiterleitungen verfolgen] </td> 
   <td> <p>Aktivieren Sie diese Option, um den URL-Umleitungen mit allen Antwort-Codes zu folgen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Serialisierung mehrerer derselben Abfragezeichenfolgen-Schlüssel als Arrays deaktivieren]</p> </td> 
   <td> <p>Standardmäßig verarbeitet [!DNL Workfront Fusion] mehrere Werte für denselben URL-Abfragezeichenfolgen-Parameterschlüssel wie Arrays. Beispielsweise wird <code>www.test.com?foo=bar&amp;foo=baz</code> in <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code> konvertiert. Aktivieren Sie diese Option, um diese Funktion zu deaktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Komprimierten Inhalt anfordern]</td> 
   <td> <p> Aktivieren Sie diese Option, um eine komprimierte Version der Website anzufordern.</p> <p>Dadurch wird eine <code>[!UICONTROL Accept-Encoding]</code>-Kopfzeile hinzugefügt, um komprimierten Inhalt anzufordern.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Gegenseitige TLS verwenden]</td> 
   <td> <p>Aktivieren Sie diese Option, um gegenseitiges TLS in der HTTP-Anfrage zu verwenden.</p> <p>Weitere Informationen zu gegenseitigem TLS finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">Verwenden von gegenseitigem TLS in HTTP-Modulen in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
