---
title: HTTP > Erstellen eines einfachen Autorisierungsanforderungsmoduls
description: Adobe Workfront Fusion erfordert zusätzlich zu einer Adobe Workfront-Lizenz eine Adobe Workfront Fusion-Lizenz.
author: Becky
feature: Workfront Fusion
exl-id: e544768e-7023-473f-8d51-631b04183743
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 1%

---

# [!UICONTROL HTTP] > [!UICONTROL Erstellen einer einfachen Autorisierungsanfrage]-Modul

Mit diesem [!DNL Adobe Workfront Fusion] können Sie eine HTTP-Anfrage mit HTTP-Standardautorisierung konfigurieren und an einen Server senden. Die empfangene HTTP-Antwort ist dann im Ausgabepaket enthalten.

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

## [!UICONTROL HTTP] > [!UICONTROL Erstellen einer einfachen Autorisierungsanfrage] Modulkonfiguration

Wenn Sie das Modul [!UICONTROL HTTP] > [!UICONTROL Einfache Autorisierungsanfrage erstellen] konfigurieren, zeigt [!DNL Adobe Workfront Fusion] die unten aufgeführten Felder an. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zu einem anderen Modul in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL]</td> 
   <td> <p>Wählen Sie den Schlüssel aus, der Ihre grundlegenden Authentifizierungsdaten enthält, oder klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong>, um Ihre Anmeldeinformationen einem neuen Schlüssel hinzuzufügen. </p> <p>Hinweis: Sie können weitere Anmeldeinformationen hinzufügen, um einfach zwischen den einzelnen Verbindungen zu wechseln.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Alle Status als Fehler auswerten (außer 2xx und 3xx )] </td> 
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
     <li> <p><strong>[!UICONTROL application/x-www-form-urlencoded]</strong> </p> <p>Dieser Hauptteiltyp wird verwendet, um [!UICONTROL POST]-Daten mithilfe von <code>application/x-www-form-urlencoded</code> zu speichern.</p> <p><code>[!UICONTROL application/x-www-form-urlencoded]</code> besteht der Text der an den Server gesendeten HTTP-Nachricht im Wesentlichen aus einer Abfragezeichenfolge. Schlüssel und Werte werden in Schlüssel-Wert-Paaren codiert, die durch <code>&amp;</code> getrennt sind, wobei zwischen Schlüssel und Wert ein <code>=</code> besteht. </p> <p>Verwenden Sie für Binärdaten stattdessen <code>[!UICONTROL multipart/form-data]</code> .</p> <p>Klicken Sie für jedes Schlüssel-Wert-Paar, das Sie hinzufügen möchten, im Feld Felder auf <b>Element hinzufügen</b> und geben Sie den Schlüssel und den Wert ein.</p>
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>Beispiel: </b></span></span> 
       <p>Beispiel für das daraus resultierende HTTP-Anfrageformat:</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL Multipart/form-data] ist eine mehrteilige HTTP-Anfrage zum Senden von Dateien und Daten. Es wird häufig verwendet, um Dateien auf den Server hochzuladen.</p> <p>Fügen Sie Felder hinzu, die in der Anfrage gesendet werden sollen. Jedes Feld muss ein Schlüssel-Wert-Paar enthalten.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL text]</strong> </p> <p>Geben Sie den Schlüssel und den Wert ein, die innerhalb des Anfragetexts gesendet werden sollen.</p> </li> 
       <li> <p><strong>[!UICONTROL-Datei]</strong> </p> <p>Geben Sie den Schlüssel und anschließend die Quelldatei ein, die Sie im Anfrageinhalt senden möchten. Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Datei zu.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um Antworten automatisch zu parsen und JSON- und XML-Antworten zu konvertieren, sodass Sie keine [!UICONTROL JSON] &gt; [!UICONTROL Parse JSON]- oder [!UICONTROL XML] &gt; [!UICONTROL Parse XML]-Module verwenden müssen.</p> <p>Bevor Sie geparste JSON- oder XML-Inhalte verwenden können, führen Sie das Modul einmal manuell aus, damit das Modul den Antwortinhalt erkennen und in nachfolgenden Modulen zuordnen kann.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zeitüberschreitung] </td> 
   <td> <p>Angeben des Zeitlimits für Anfragen in Sekunden (1-300). Der Standardwert ist 40 Sekunden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Cookies für andere HTTP-Module freigeben]</td> 
   <td> <p> Aktivieren Sie diese Option, um Cookies vom Server für alle HTTP-Module in Ihrem Szenario freizugeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selbstsigniertes Zertifikat]</td> 
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
              <p>Klicken Sie auf <b>[!UICONTROL Speichern]</b>, um die Datei zu extrahieren und zum Modul-Setup zurückzukehren.</p>
            </li>
          </ol>
</p> </td> 
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
   <td> <p> Aktivieren Sie diese Option, um eine komprimierte Version der Website anzufordern.</p> <p>Fügt eine <code>[!UICONTROL Accept-Encoding]</code>-Kopfzeile hinzu, um komprimierten Inhalt anzufordern.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Gegenseitige TLS verwenden]</td> 
   <td> <p>Aktivieren Sie diese Option, um gegenseitiges TLS in der HTTP-Anfrage zu verwenden.</p> <p>Weitere Informationen zu gegenseitigen TLS finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">Verwenden von gegenseitigen TLS in HTTP-Modulen</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
