---
title: Adobe Authenticator-Modul
description: Mit dem Adobe Authenticator-Modul können Sie über eine einzige Verbindung eine Verbindung zu jedem Adobe-Produkt mit einer API herstellen.
author: Becky
feature: Workfront Fusion
exl-id: af4da661-eeee-4033-a2bb-a2196e446a3d
source-git-commit: 983ce043afbcc44ee8af2dfcd46738f170a2b257
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 1%

---

# Adobe Authenticator-Module

Mit dem Adobe Authenticator-Modul können Sie über eine einzige Verbindung eine Verbindung zu jeder Adobe-API herstellen. Dadurch können Sie einfacher eine Verbindung zu Adobe-Produkten herstellen, die noch keinen dedizierten Fusion-Connector haben.

Der Vorteil gegenüber den HTTP-Modulen besteht darin, dass Sie wie in einer dedizierten App eine Verbindung erstellen können.

Eine Liste der verfügbaren Adobe-APIs finden Sie unter [Adobe-APIs](https://developer.adobe.com/apis). Sie können möglicherweise nur die APIs verwenden, denen Sie zugewiesen sind.

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

## Voraussetzungen

* Sie müssen Zugriff auf das Adobe-Produkt haben, mit dem sich das Modul verbinden soll.
* Sie müssen Zugriff auf die Adobe Developer Console haben.
* Sie müssen über ein Projekt in der Adobe Developer Console verfügen, das die API enthält, mit der sich das Modul verbinden soll. Sie können:

   * Erstellen Sie ein neues Projekt mit der -API.

     Oder
   * Fügen Sie die API zu einem vorhandenen Projekt hinzu.

  Informationen zum Erstellen oder Hinzufügen einer API zu einem Projekt in der Adobe Developer Console finden Sie unter [Erstellen eines Projekts](https://developer.adobe.com/dep/guides/dev-console/create-project/) in der Dokumentation zu Adobe.

## Adobe Authenticator-API-Informationen

Der Adobe Authenticator-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung

Eine Adobe Authenticator-Verbindung stellt eine Verbindung zu einem einzelnen Projekt in Adobe Developer Console her. Um dieselbe Verbindung für mehr als eine Adobe-API zu verwenden, fügen Sie die APIs zum selben Projekt hinzu und erstellen Sie eine Verbindung zu diesem Projekt.

Sie können separate Verbindungen zu separaten Projekten erstellen, aber Sie können keine Verbindung verwenden, um auf eine API zuzugreifen, die nicht zu dem in dieser Verbindung angegebenen Projekt gehört.

>[!IMPORTANT]
>
>Mit dem Adobe Authenticator-Connector haben Sie die Wahl zwischen einer OAuth-Server-zu-Server-Verbindung oder einer JWT-Verbindung (Service Account). Adobe hat veraltete JWT-Anmeldeinformationen, die nach dem 1. Januar 2025 nicht mehr funktionieren. **Daher empfehlen wir dringend, OAuth-Verbindungen zu erstellen.**
>
>Weitere Informationen zu diesen Verbindungstypen finden Sie unter [Server-zu-Server](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/) in der Dokumentation zu Adobe

So erstellen Sie eine Verbindung:

1. Klicken Sie in einem beliebigen Adobe Authenticator **Modul** Hinzufügen) neben dem Feld Verbindung .
1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungstyp]</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine OAuth-Server-zu-Server-Verbindung oder eine JWT-Verbindung (Service-Konto) erstellen möchten. Es wird dringend empfohlen, OAuth-Verbindungen zu erstellen.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre [!DNL Adobe]-Client-ID ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr [!DNL Adobe]-Client-Geheimnis ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL -Bereiche]</td>
        <td>Wenn Sie eine OAuth-Verbindung ausgewählt haben, geben Sie die für diese Verbindung erforderlichen Bereiche ein.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID des technischen Kontos]</td>
        <td>Wenn Sie eine JWT-Verbindung ausgewählt haben, geben Sie Ihre [!DNL Adobe] ID des technischen Kontos ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organisations-ID]</td>
        <td>Wenn Sie eine JWT-Verbindung ausgewählt haben, geben Sie Ihre [!DNL Adobe] Organisations-ID ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>Wenn Sie eine JWT-Verbindung ausgewählt haben, geben Sie die für diese Verbindung erforderlichen Metabereiche ein. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Privater Schlüssel]</td>
        <td>
          <p>Wenn Sie eine JWT-Verbindung ausgewählt haben, geben Sie den privaten Schlüssel ein, der beim Erstellen Ihrer Anmeldeinformationen im [!DNL Adobe Developer Console] generiert wurde. </p>
          <p>So extrahieren Sie Ihren privaten Schlüssel oder Ihr Zertifikat:</p>
          <ol>
            <li value="1">
              <p>Klicken Sie auf <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Wählen Sie den zu extrahierenden Dateityp aus.</p>
            </li>
            <li value="3">
              <p>Wählen Sie die Datei aus, die den privaten Schlüssel oder das Zertifikat enthält.</p>
            </li>
            <li value="4">
              <p>Geben Sie das Kennwort für die Datei ein.</p>
            </li>
            <li value="5">
              <p>Klicken Sie auf <b>[!UICONTROL Speichern]</b>, um die Datei zu extrahieren und zur Verbindungseinrichtung zurückzukehren.</p>
            </li>
          </ol>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Basis-URLs]</td>
        <td>Sie müssen die Basis-URLs hinzufügen, die dieser Authentifizierer zulassen soll. Wenn Sie das Modul Benutzerdefinierten API-Aufruf erstellen später im Szenario verwenden, fügen Sie der ausgewählten URL einen relativen Pfad hinzu. Durch die Eingabe von URLs hier können Sie steuern, mit was sich das Modul Benutzerdefinierte API-Aufrufe erstellen verbinden kann, was die Sicherheit erhöht.<p>Klicken Sie für jede Basis-URL, die Sie der Authentifizierung hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Basis-URL ein.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL -Authentifizierungs-URL]</td>
        <td>Lassen Sie dieses Feld leer, um die standardmäßige Adobe IMS-Authentifizierungs-URL von <code>https://ims-na1.adobelogin.com</code> zu verwenden. Wenn Sie Adobe IMS nicht für die Authentifizierung verwenden, geben Sie die URL ein, die für die Authentifizierung verwendet werden soll.</td>
      </tr>
    </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## Module

* [Erstellen eines benutzerdefinierten API-Aufrufs](#make-a-custom-api-call)
* [Erstellen eines benutzerdefinierten API-Aufrufs (veraltet)](#make-a-custom-api-call-legacy)

### Erstellen eines benutzerdefinierten API-Aufrufs

Mit diesem Aktionsmodul können Sie eine beliebige Adobe-API aufrufen. Es werden große Dateien anstelle von reinen Textkörpern unterstützt.

Dieses Modul wurde am 14. November 2024 zur Verfügung gestellt. Jedes Adobe Authenticator-Modul > Erstellen eines benutzerdefinierten API-Aufrufs, der vor diesem Datum konfiguriert wurde, verarbeitet keine großen Dateien und wird jetzt als Modul Erstellen eines benutzerdefinierten API-Aufrufs (Legacy) betrachtet.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL -Verbindung]</td>
     <td>Anweisungen zum Erstellen einer Verbindung zum Adobe Authenticator-Modul finden Sie unter <a href="#create-a-connection" class="MCXref xref" >Erstellen einer Verbindung</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Basis-URL]</p>
      </td>
      <td>
        <p>Geben Sie die Basis-URL des API-Punkts ein, mit dem Sie eine Verbindung herstellen möchten.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Geben Sie den Pfad relativ zur Basis-URL ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL -Methode]</p>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -Kopfzeilen]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt Autorisierungs-Header automatisch hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Abfragezeichenfolge]  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Texttyp]</td>
   <td> Wählen Sie den Texttyp für diese API-Anfrage:
   <ul>
   <li>Raw</li>
   <li>application/x-www-form-urlencoded</li>
   <li>multipart/form-data</li>
   </ul>
      </td>
      </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ausgabetyp]  </td>
      <td>
        <p>Wählen Sie den Datentyp aus, den das Modul ausgeben soll. Wenn Sie keinen Typ auswählen, wählt das Modul automatisch einen Typ aus.</p>
      </td>
    </tr>
  </tbody>
</table>

### Erstellen eines benutzerdefinierten API-Aufrufs (veraltet)

Mit diesem Aktionsmodul können Sie eine beliebige Adobe-API aufrufen.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL -Verbindung]</td>
     <td>Anweisungen zum Erstellen einer Verbindung zum Adobe Authenticator-Modul finden Sie unter <a href="#create-a-connection" class="MCXref xref" >Erstellen einer Verbindung</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Basis-URL]</p>
      </td>
      <td>
        <p>Geben Sie die Basis-URL des API-Punkts ein, mit dem Sie eine Verbindung herstellen möchten.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Geben Sie den Pfad relativ zur Basis-URL ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL -Methode]</p>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -Kopfzeilen]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt Autorisierungs-Header automatisch hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Abfragezeichenfolge]  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL body]</td>
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
