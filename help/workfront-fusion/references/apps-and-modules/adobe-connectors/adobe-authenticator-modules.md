---
title: Adobe Authenticator-Modul
description: Mit dem Adobe Authenticator-Modul können Sie über eine einzige Verbindung eine Verbindung zu jedem Adobe-Produkt mit einer API herstellen.
author: Becky
feature: Workfront Fusion
exl-id: af4da661-eeee-4033-a2bb-a2196e446a3d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 1%

---

# Adobe Authenticator-Module

Das Adobe Authenticator-Modul ermöglicht die Verbindung zu jeder Adobe-API über eine einzige Verbindung. So können Sie einfacher eine Verbindung zu Adobe-Produkten herstellen, die noch keinen dedizierten Fusion-Connector haben.

Der Vorteil gegenüber den HTTP-Modulen besteht darin, dass Sie wie in einer dedizierten App eine Verbindung erstellen können.

Eine Liste der verfügbaren Adobe-APIs finden Sie unter [Adobe-APIs](https://developer.adobe.com/apis). Sie können möglicherweise nur die APIs verwenden, denen Sie zugewiesen sind.

## Zugriffsanforderungen

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] Packstück</td>
      <td>
        <p>Neu: Beliebig</p><p>Oder</p><p>Aktuell: [!UICONTROL Pro] oder höher</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] Lizenz</td>
      <td>
        <p>Neu: Standard</p><p>Oder</p><p>Aktuell: [!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz</td>
      <td>
   <p>Aktuelle Fusion-Lizenzanforderung: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy Fusion-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung und -integration] </p>
   </td>
    </tr>
    <tr>
      <td role="rowheader">Produkt</td>
      <td>
   <p>Neuer Workfront-Plan: Wenn Sie über den [!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Adobe Workfront] verfügen, muss Ihr Unternehmen [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu nutzen. [!DNL Workfront Fusion] ist im [!UICONTROL Ultimate] [!DNL Workfront] enthalten.</p>
   <p>Oder</p>
   <p>Aktueller Workfront-Plan: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu nutzen.</p>
   </td>
    </tr>
  </tbody>
</table>

## Voraussetzungen

* Sie müssen Zugriff auf das Adobe-Produkt haben, mit dem sich das Modul verbinden soll.
* Sie müssen Zugriff auf die Adobe Developer Console haben.
* Sie müssen über ein Projekt in der Adobe Developer Console verfügen, das die API enthält, mit der sich das Modul verbinden soll. Sie können:

   * Erstellen Sie ein neues Projekt mit der -API.

     Oder
   * Fügen Sie die API zu einem vorhandenen Projekt hinzu.

  Informationen zum Erstellen oder Hinzufügen einer API zu einem Projekt in der Adobe Developer Console finden Sie unter [Erstellen eines Projekts](https://developer.adobe.com/dep/guides/dev-console/create-project/) in der Adobe-Dokumentation.

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
>Weitere Informationen zu diesen Verbindungstypen finden Sie unter [Server-zu-Server-Authentifizierung](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/) in der Adobe-Dokumentation

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
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine OAuth-Server-zu-Server-Verbindung oder eine JWT-Verbindung (Service-Konto) erstellen möchten.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Geben Sie Ihre [!DNL Adobe]-Client-ID ein. Diese finden Sie im [!UICONTROL Credentials details] Abschnitt der [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Geben Sie Ihr [!DNL Adobe]-Client-Geheimnis ein. Diese finden Sie im [!UICONTROL Credentials details] Abschnitt der [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>Wenn Sie eine OAuth-Verbindung ausgewählt haben, geben Sie die für diese Verbindung erforderlichen Bereiche ein.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Geben Sie die ID Ihres [!DNL Adobe] technischen Kontos ein. Diese finden Sie im [!UICONTROL Credentials details] Abschnitt der [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Wenn Sie eine JWT-Verbindung ausgewählt haben, geben Sie Ihre [!DNL Adobe] Organisations-ID ein. Diese finden Sie im [!UICONTROL Credentials details] Abschnitt der [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>Wenn Sie eine JWT-Verbindung ausgewählt haben, geben Sie die für diese Verbindung erforderlichen Metabereiche ein. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
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
              <p>Klicken Sie auf <b>[!UICONTROL Save]</b> , um die Datei zu extrahieren und zur Verbindungseinrichtung zurückzukehren.</p>
            </li>
          </ol>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Base URLs]</td>
        <td>Sie müssen die Basis-URLs hinzufügen, die dieser Authentifizierer zulassen soll. Wenn Sie das Modul Benutzerdefinierten API-Aufruf erstellen später im Szenario verwenden, fügen Sie der ausgewählten URL einen relativen Pfad hinzu. Durch die Eingabe von URLs hier können Sie steuern, mit was sich das Modul Benutzerdefinierte API-Aufrufe erstellen verbinden kann, was die Sicherheit erhöht.<p>Klicken Sie für jede Basis-URL, die Sie der Authentifizierung hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Basis-URL ein.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentication URL]</td>
        <td>Lassen Sie dieses Feld leer, um die standardmäßige Adobe IMS-Authentifizierungs-URL von <code>https://ims-na1.adobelogin.com</code> zu verwenden. Wenn Sie Adobe IMS nicht für die Authentifizierung verwenden, geben Sie die URL ein, die für die Authentifizierung verwendet werden soll.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</td>
      </tr>
    </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu speichern und zum Modul zurückzukehren.

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
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>Anweisungen zum Erstellen einer Verbindung zum Adobe Authenticator-Modul finden Sie unter <a href="#create-a-connection" class="MCXref xref" >Erstellen einer Verbindung</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Base URL]</p>
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
        <p>[!UICONTROL Method]</p>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt Autorisierungs-Header automatisch hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body Type]</td>
   <td> Wählen Sie den Texttyp für diese API-Anfrage:
   <ul>
   <li>application/x-www-form-urlencoded</li>
   <li>Raw</li>
   <li>multipart/form-data</li>
   </ul>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Fields]  </td>
      <td>
        <p>Klicken Sie für jede Datei, die Sie der APU-Anfrage hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie den Text der Datei (für Rohdaten) ein, oder geben Sie den <code>uploadedFile</code> ein und ordnen Sie die Daten der Datei zu.</p>
      </td>
    </tr>
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
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>Anweisungen zum Erstellen einer Verbindung zum Adobe Authenticator-Modul finden Sie unter <a href="#create-a-connection" class="MCXref xref" >Erstellen einer Verbindung</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Base URL]</p>
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
        <p>[!UICONTROL Method]</p>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt Autorisierungs-Header automatisch hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> 
     </div> </p> </td>     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Geben Sie die maximale Anzahl von Ergebnissen ein, die das Modul in einem Ausführungszyklus zurückgeben soll.</p>
      </td>
    </tr>
  </tbody>
</table>
