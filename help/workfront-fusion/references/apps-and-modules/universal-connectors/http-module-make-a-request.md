---
title: HTTP &gt; Erstellen eines Anforderungsmoduls
description: Das Adobe Workfront Fusion HTTP &gt; Make a Request-Modul ist ein universelles Modul, mit dem Sie eine HTTP-Anfrage konfigurieren und an einen Server senden können. Die empfangene HTTP-Antwort ist dann im Ausgabepaket enthalten.
author: Becky
feature: Workfront Fusion
exl-id: 42f6176e-86e0-489e-868b-66823a932daf
source-git-commit: 5a95b2c191d4e6d8750dc57a47923f416612b4a9
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 1%

---

# [!UICONTROL HTTP] > [!UICONTROL Make a request]

Der [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] > [!UICONTROL Make a request module] ist ein universelles Modul, mit dem Sie eine HTTP-Anfrage konfigurieren und an einen Server senden können. Die empfangene HTTP-Antwort ist dann im Ausgabepaket enthalten.

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
   <p>Keine Workfront Fusion-Lizenzanforderung.</p>
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

## [!UICONTROL HTTP] > Konfiguration des [!UICONTROL Make a request]

Beim Konfigurieren des Moduls [!UICONTROL HTTP] > [!UICONTROL Make a request] zeigt [!DNL Adobe Workfront Fusion] die unten aufgeführten Felder an. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx)] </td> 
   <td> <p>Mit dieser Option können Sie die Fehlerbehandlung einrichten.</p> <p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Fehlerbehandlung hinzufügen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Geben Sie die URL ein, an die Sie eine Anfrage senden möchten, z. B. einen API-Endpunkt oder eine Website.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Beispiel: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Geben Sie die gewünschten Schlüssel-Wert-Paare für die Abfrage ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Body type]</p> </td> 
   <td> <p>Der HTTP-Hauptteil sind die Datenbytes, die in einer HTTP-Transaktionsnachricht unmittelbar nach den -Headern übertragen werden, falls welche verwendet werden sollen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>Der Rohtexttyp ist im Allgemeinen für die meisten HTTP-Textkörperanforderungen geeignet, selbst in Situationen, in denen in der Entwicklerdokumentation keine zu sendenden Daten angegeben sind.</p> <p>Geben Sie ein Formular zum Analysieren der Daten im Feld [!UICONTROL Content type] an.</p> <p>Trotz des ausgewählten Inhaltstyps werden Daten in jedem Format eingegeben, das in der Entwicklerdokumentation festgelegt oder erforderlich ist.</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>Dieser Texttyp dient zum [!UICONTROL POST] von Daten mithilfe von <code>[!UICONTROL application/x-www-form-urlencoded]</code>.</p> <p><code>application/x-www-form-urlencoded</code> besteht der Text der an den Server gesendeten HTTP-Nachricht im Wesentlichen aus einer Abfragezeichenfolge. Schlüssel und Werte werden in Schlüssel-Wert-Paaren codiert, die durch <code>&amp;</code> getrennt sind, wobei zwischen Schlüssel und Wert ein <code>=</code> besteht. </p> <p>Verwenden Sie für Binärdaten stattdessen <code>[!UICONTROL multipart/form-data]</code> .</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>Beispiel: </b></span></span> 
       <p>Beispiel für das daraus resultierende HTTP-Anfrageformat:</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>Die [!UICONTROL  Multipart/form-data] ist eine mehrteilige HTTP-Anfrage, die zum Senden von Dateien und Daten verwendet wird. Es wird häufig verwendet, um Dateien auf den Server hochzuladen.</p> <p>Fügen Sie Felder hinzu, die in der Anfrage gesendet werden sollen. Jedes Feld muss ein Schlüssel-Wert-Paar enthalten.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>Geben Sie den Schlüssel und den Wert ein, die innerhalb des Anfragetexts gesendet werden sollen.</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Geben Sie den Schlüssel und anschließend die Quelldatei ein, die Sie im Anfrageinhalt senden möchten.</p> <p>Ordnen Sie die Datei zu, die Sie aus dem vorherigen Modul hochladen möchten (z. B. [!UICONTROL HTTP] &gt; [!UICONTROL Get a File] oder [!UICONTROL Google Drive] &gt; Datei herunterladen), oder geben Sie den Dateinamen und die Dateidaten manuell ein.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um Antworten automatisch zu analysieren und JSON- und XML-Antworten zu konvertieren.</p> <p>Bevor Sie geparste JSON- oder XML-Inhalte verwenden können, führen Sie das Modul einmal manuell aus, damit das Modul den Antwortinhalt erkennen und in nachfolgenden Modulen zuordnen kann.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL User name]</p> </td> 
   <td> <p> Geben Sie den Benutzernamen ein, wenn Sie eine Anfrage mit einfacher Autorisierung senden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password] </td> 
   <td> <p>Geben Sie das Passwort ein, wenn Sie eine Anfrage mit einfacher Autorisierung senden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>Angeben des Zeitlimits für Anfragen in Sekunden (1-300). Der Standardwert ist 40 Sekunden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> Aktivieren Sie diese Option, um Cookies vom Server für alle HTTP-Module in Ihrem Szenario freizugeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p>So fügen Sie ein selbstsigniertes Zertifikat hinzu:</p>
          <ol>
            <li value="1">
              <p>Klicken Sie auf <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Wählen Sie den zu extrahierenden Dateityp aus.</p>
            </li>
            <li value="3">
              <p>Wählen Sie die Datei aus, die das - oder -Zertifikat enthält.</p>
            </li>
            <li value="4">
              <p>Geben Sie das Kennwort für die Datei ein.</p>
            </li>
            <li value="5">
              <p>Klicken Sie auf <b>[!UICONTROL Save]</b> , um die Datei zu extrahieren und zur Moduleinrichtung zurückzukehren.</p>
            </li>
          </ol>
</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reject connections that are using unverified (self-signed) certificates] </td> 
   <td> <p>Aktivieren Sie diese Option, um Verbindungen abzulehnen, die nicht verifizierte TLS-Zertifikate verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow redirect]</td> 
   <td> <p> Aktivieren Sie diese Option, um den URL-Umleitungen mit 3xx-Antworten zu folgen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow all redirects] </td> 
   <td> <p>Aktivieren Sie diese Option, um den URL-Umleitungen mit allen Antwort-Codes zu folgen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Disable serialization of multiple same query string keys as arrays]</p> </td> 
   <td> <p>Standardmäßig verarbeitet [!DNL Workfront Fusion] mehrere Werte für denselben URL-Abfragezeichenfolgen-Parameterschlüssel wie Arrays. Beispielsweise wird <code>www.test.com?foo=bar&amp;foo=baz</code> in <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code> konvertiert. Aktivieren Sie diese Option, um diese Funktion zu deaktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request compressed content]</td> 
   <td> <p> Aktivieren Sie diese Option, um eine komprimierte Version der Website anzufordern.</p> <p>Fügt eine <code>[!UICONTROL Accept-Encoding]</code>-Kopfzeile hinzu, um komprimierten Inhalt anzufordern.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Mutual TLS]</td> 
   <td> <p>Aktivieren Sie diese Option, um gegenseitiges TLS in der HTTP-Anfrage zu verwenden.</p> <p>Weitere Informationen zu gegenseitigen TLS finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">Verwenden von gegenseitigen TLS in HTTP-Modulen</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Beispiel:** Dieses Beispiel zeigt, wie Sie das Modul so einrichten, dass es eine [!UICONTROL POST]-Anfrage mit JSON-Payload sendet:

![Beispiel für eine Anfrage](/help/workfront-fusion/references/apps-and-modules/assets/make-a-request-example-350x522.png)

Es wird nicht empfohlen, JSON-Elemente mit Ausdrücken und Elementen direkt im [!UICONTROL Request content]-Feld zu mischen, da dies zu ungültigem JSON führen kann.

>[!ENDSHADEBOX]
