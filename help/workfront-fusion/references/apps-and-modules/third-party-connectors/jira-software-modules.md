---
title: Jira Software-Module
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die  [!DNL Jira] -Software verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 92cac080-d8f6-4770-a6a6-8934538c978b
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1809'
ht-degree: 1%

---

# [!DNL Jira Software]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Jira Software] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

<!-- Bob Fix this compared to original -->

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
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung und -integration] </p>
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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Voraussetzungen

Um [!DNL Jira] Module verwenden zu können, benötigen Sie ein [!DNL Jira].

## Jira-API-Informationen

Der Jira-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"></td> 
   <td> Jira Cloud</td> 
   <td> Jira-Server</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersion</td> 
   <td> 2</td> 
   <td> 2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersionAgile</td> 
   <td> 1,0 </td> 
   <td> 1,0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>1.7.29</td> 
   <td>1,0,19</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Jira Software] mit [!DNL Workfront Fusion] verbinden

Ihre Verbindungsmethode hängt davon ab, ob Sie [!DNL Jira Cloud] oder [!DNL Jira Server] verwenden.

* [Verbinden  [!DNL Jira Cloud]  Workfront Fusion](#connect-jira-cloud-to-workfront-fusion)
* [Verbinden [!DNL Jira Server] mit [!DNL Workfront Fusion]](#connect-jira-server-to-workfront-fusion)

### [!DNL Jira Cloud] mit [!DNL Workfront Fusion] verbinden

[!DNL Jira Cloud] mit [!DNL Workfront Fusion] verbinden

Um [!DNL Jira Software] mit [!DNL Workfront Fusion] zu verbinden, müssen Sie ein API-Token erstellen und es zusammen mit Ihrer Service-URL und Ihrem Benutzernamen in das Feld [!UICONTROL Create a connection] in [!DNL Workfront Fusion] einfügen.

#### Erstellen eines API-Tokens in [!DNL Jira]

1. Wechseln Sie zu [https://id.atlassian.com/manage/api-tokens](https://id.atlassian.com/manage/api-tokens) und melden Sie sich an.
1. Klicken Sie auf **[!UICONTROL Create API token]**.
1. Geben Sie einen Namen für das Token ein, z. B. *Workfront Fusion*.
1. Kopieren Sie das Token mithilfe der Schaltfläche **[!UICONTROL Copy to clipboard]** .

   >[!IMPORTANT]
   >
   >Sie können das Token nach dem Schließen dieses Dialogfelds nicht mehr anzeigen.
1. Bewahren Sie das generierte Token an einem sicheren Ort auf.
1. Fahren Sie fort mit [Konfigurieren des  [!DNL Jira] -API-Tokens in [!DNL Workfront Fusion]](#configure-the-jira-api-token-in-workfront-fusion).

#### Konfigurieren des [!DNL Jira]-API-Tokens in [!DNL Workfront Fusion]

1. Fügen Sie [!DNL Workfront Fusion] einem Szenario ein [!DNL Jira] hinzu, um das **[!UICONTROL Create a connection]** zu öffnen.
1. Geben Sie die folgenden Informationen an:

   * **[!UICONTROL Service URL]:** Dies ist die Basis-URL, mit der Sie auf Ihr Jira-Konto zugreifen. Beispiel: `yourorganization.atlassian.net`
   * **[!UICONTROL Username]**
   * **[!UICONTROL API token]:** Dies ist das API-Token, das Sie im Abschnitt [Erstellen eines API-Tokens [!DNL Jira]](#create-an-api-token-in-jira) dieses Artikels erstellt haben.

1. Klicken Sie auf [!UICONTROL Continue] , um die Verbindung zu erstellen und zum Modul zurückzukehren.

### [!DNL Jira Server] mit [!DNL Workfront Fusion] verbinden

<!--
<p style="color: #ff1493;">Becky: Find out and document how to find these things</p>
-->

Um eine Verbindung zwischen [!DNL Workfront Fusion] und [!DNL Jira Server] zu autorisieren, benötigen Sie Ihren Consumer Key, den privaten Schlüssel und die Service-URL. Möglicherweise müssen Sie sich für diese Informationen an Ihren [!DNL Jira] wenden.

* [Generieren von öffentlichen und privaten Schlüsseln für  [!DNL Jira]  Verbindung](#generate-public-and-private-keys-for-your-jira-connection)
* [Konfigurieren Sie die Client-App als Verbraucher in [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)
* [Erstellen einer Verbindung zu  [!DNL Jira]  oder Jira Data Center in [!DNL Workfront Fusion]](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Generieren von öffentlichen und privaten Schlüsseln für Ihre [!DNL Jira]

Um einen privaten Schlüssel für Ihre [!DNL Workfront Fusion Jira]-Verbindung zu erhalten, müssen Sie öffentliche und private Schlüssel generieren.

1. Führen Sie in Ihrem Terminal die folgenden `openssl` Befehle aus.

   * `openssl genrsa -out jira_privatekey.pem 1024`

     Dieser Befehl generiert einen privaten 1024-Bit-Schlüssel.

   * `openssl req -newkey rsa:1024 -x509 -key jira_privatekey.pem -out jira_publickey.cer -days 365`

     Dieser Befehl erstellt ein X509-Zertifikat.

   * `openssl pkcs8 -topk8 -nocrypt -in jira_privatekey.pem -out jira_privatekey.pcks8`

     Dieser Befehl extrahiert den privaten Schlüssel (PKCS8-Format) in die `jira_privatekey.pcks8`
-Datei.

   * `openssl x509 -pubkey -noout -in jira_publickey.cer  > jira_publickey.pem`

     Mit diesem Befehl wird der öffentliche Schlüssel aus dem Zertifikat in die `jira_publickey.pem`-Datei extrahiert.

     >[!NOTE]
     >
     >Wenn Sie Windows verwenden, müssen Sie den öffentlichen Schlüssel in der `jira_publickey.pem` möglicherweise manuell speichern:
     >
     >1. Führen Sie in Ihrem Terminal den folgenden Befehl aus:
     >   
     >   `openssl x509 -pubkey -noout -in jira_publickey.cer`
     >   
     >1. Terminal-Ausgabe kopieren (einschließlich `-------BEGIN PUBLIC KEY--------` und `-------END PUBLIC KEY--------`
     >   
     >1. Fügen Sie die Terminal-Ausgabe in eine Datei mit dem Namen `jira_publickey.pem` ein.


1. Fahren Sie fort [Konfigurieren der Client-App als Verbraucher in [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)

#### Konfigurieren der Client-App als Verbraucher in [!DNL Jira]

1. Melden Sie sich bei Ihrer [!DNL Jira] an.
1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL [!DNL Jira] Settings]** ![](/help/workfront-fusion/references/apps-and-modules/assets/jira-settings-icon.png) > **[!UICONTROL Applications]** > **[!UICONTROL Application links]**.
1. Geben Sie in das Feld **[!UICONTROL Enter the URL of the application you want to link]** ein.

   ```
   https://app.workfrontfusion.com/oauth/cb/workfront-jiraserver-oauth1
   ```

1. Klicken Sie auf **[!UICONTROL Create new link]**. Ignorieren Sie die Fehlermeldung „Keine Antwort von der eingegebenen URL erhalten“.
1. Geben Sie im **[!UICONTROL Link applications]**-Fenster Werte in die Felder **[!UICONTROL Consumer key]** und **[!UICONTROL Shared secret]** ein.

   Sie können die Werte für diese Felder auswählen.

1. Kopieren Sie die Werte der **[!UICONTROL Consumer key]**- und **[!UICONTROL Shared secret]** an einen sicheren Speicherort.

   Sie benötigen diese Werte später im Konfigurationsprozess.

1. Füllen Sie die URL-Felder wie folgt aus:

   | Feld | Beschreibung |
   |---|---|
   | [!UICONTROL Request Token URL] | `<Jira base url>/plugins/servlet/oauth/request-token` |
   | [!UICONTROL Authorization URL] | `<Jira base url>/plugins/servlet/oauth/authorize` |
   | [!UICONTROL Access Token URL] | `<Jira base url>/plugins/servlet/oauth/access-token` |

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL Create incoming link]** .
1. Klicken Sie auf **[!UICONTROL Continue]**.
1. Füllen Sie im **[!UICONTROL Link applications]** die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col data-mc-conditions=""> 
    <col data-mc-conditions=""> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Consumer Key]</p> </td> 
      <td> Fügen Sie den Consumer Key ein, den Sie an einen sicheren Speicherort kopiert haben.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Consumer name]</td> 
      <td>Geben Sie einen Namen Ihrer Wahl ein. Dieser Name dient als Referenz.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Public key]</td> 
      <td>Fügen Sie den öffentlichen Schlüssel aus Ihrer <code>[!DNL jira_publickey.pem]</code> ein.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie auf **[!UICONTROL Continue]**.
1. Fahren Sie fort [Erstellen einer Verbindung mit [!DNL Jira Server] oder [!DNL Jira Data Center] in [!DNL Workfront Fusion]](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Erstellen einer Verbindung zu [!DNL Jira Server] oder [!DNL Jira Data Center] in [!DNL Workfront Fusion]

>[!NOTE]
>
>Verwenden Sie die [!DNL Jira Server]-App, um eine Verbindung zu [!DNL Jira Server] oder [!DNL Jira Data Center] herzustellen.

1. Klicken Sie in einem [!DNL Jira Server] Modul in [!DNL Workfront Fusion] auf **[!UICONTROL Add]** neben dem Feld [!UICONTROL connection] .
1. Füllen Sie im Bedienfeld [!UICONTROL Create a connection] die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Einen Namen für die Verbindung eingeben</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Consumer Key]</td> 
      <td>Fügen Sie den Kundenschlüssel ein, den Sie an einen sicheren Speicherort in kopiert haben <a href="#configure-the-client-app-as-a-consumer-in-jira" class="MCXref xref">Konfigurieren Sie die Client-Anwendung als Verbraucher in [!DNL Jira]</a></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Private Key]</td> 
      <td>Fügen Sie den privaten Schlüssel aus der <code>[!DNL jira_privatekey.pcks8]</code> ein, die Sie in erstellt haben <a href="#generate-public-and-private-keys-for-your-jira-connection" class="MCXref xref">Generieren Sie öffentliche und private Schlüssel für Ihre [!DNL Jira] Verbindung</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Service URL]</td> 
      <td>Geben Sie Ihre [!DNL Jira]-Instanz-URL ein. Beispiel: <code>yourorganization.atlassian.net</code></td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Jira Software] Module und ihre Felder

Beim Konfigurieren [!DNL Jira Software] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Jira Software] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Trigger

#### [!UICONTROL Watch for records]

Dieses Trigger-Modul startet ein Szenario, wenn ein Datensatz hinzugefügt, aktualisiert oder gelöscht wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Wählen Sie den Webhook aus, den Sie auf Datensätze überwachen möchten. </p> <p>So fügen Sie einen neuen Webhook hinzu:</p> 
    <ol> 
     <li value="1">Klicken <strong>[!UICONTROL Add]</strong></li> 
     <li value="2">Geben Sie einen Namen für den Webhook ein.</li> 
     <li value="3"> <p>Wählen Sie die Verbindung aus, die Sie für Ihren Webhook verwenden möchten. </p> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </li> 
     <li value="4"> <p>Wählen Sie den Datensatztyp aus, auf den die Software achten soll:</p> 
      <ul> 
       <li>[!UICONTROL Comment] </li> 
       <li>[!UICONTROL Issue]</li> 
       <li>[!UICONTROL Project] </li> 
       <li>[!UICONTROL Sprint]</li> 
      </ul> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Add issue to sprint]](#add-issue-to-sprint)
* [[!UICONTROL Create a Record]](#create-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Delete a record]](#delete-a-record)
* [[!UICONTROL Download an attachment]](#download-an-attachment)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Update a record]](#update-a-record)

#### [!UICONTROL Add issue to sprint]

Dieses Aktionsmodul fügt einem Sprint ein oder mehrere Probleme hinzu.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sprint ID]</td> 
   <td>Geben Sie die Sprint-ID des Sprints ein, dem Sie ein Problem hinzufügen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID or Keys]</td> 
   <td>Fügen Sie für jedes Problem, das Sie dem Sprint hinzufügen möchten, eine Problem-ID oder einen Schlüssel hinzu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Record]

Dieses Aktionsmodul erstellt einen neuen Datensatz in Jira.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den das Modul erstellen soll. Wenn Sie einen Datensatztyp auswählen, werden im Modul andere für diesen Datensatztyp spezifische Felder angezeigt.</p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Worklog]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Jira Software]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Jira Software] nicht durchgeführt werden kann.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Pfad eingeben für<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a record]

Dieses Aktionsmodul löscht einen bestimmten Datensatz.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den das Modul löschen soll. </p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID or Key]</td> 
   <td>Geben Sie die ID oder den Schlüssel des Datensatzes ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download an attachment]

Dieses Aktionsmodul lädt eine bestimmte Anlage herunter.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Anhangs ein, den Sie herunterladen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Dieses Aktionsmodul liest Daten aus einem einzelnen Datensatz in [!DNL Jira Software].

Sie geben die ID des Datensatzes an.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Wählen Sie den Typ [!DNL Jira] Datensatzes aus, den das Modul lesen soll.</p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL User]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Wählen Sie die Ausgaben aus, die Sie empfangen möchten. Je nach dem im Feld "[!UICONTROL Record Type]" ausgewählten Datensatztyp stehen Ausgabeoptionen zur Verfügung.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Geben Sie die eindeutige [!DNL Jira Software]-ID des Datensatzes ein, den das Modul lesen soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

Dieses Aktionsmodul aktualisiert einen vorhandenen Datensatz, z. B. ein Problem oder Projekt.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den das Modul aktualisieren soll. Wenn Sie einen Datensatztyp auswählen, werden im Modul andere für diesen Datensatztyp spezifische Felder angezeigt.</p> 
    <ul> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Transition issue]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID or Key]</td> 
   <td>Geben Sie die ID oder den Schlüssel des Datensatzes ein, den Sie aktualisieren möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL List records]](#list-records)
* [[!UICONTROL Search for records]](#search-for-records)

#### [!UICONTROL List records]

Dieses Suchmodul ruft alle Elemente eines bestimmten Typs ab, die Ihrer Suchanfrage entsprechen

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Wählen Sie den Datensatztyp aus, den das Modul auflisten soll. Wenn Sie einen Datensatztyp auswählen, werden im Modul andere für diesen Datensatztyp spezifische Felder angezeigt.</p> 
    <ul> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint issue]</li> 
     <li>[!UICONTROL Worklog]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Max Results]</p> </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus abrufen soll, oder mappen Sie sie.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Enter or map the ID of the first item you want to retrieve details for. This is a way to paginate the records. If you enter the 5000th item as the offset, the module would return items 5000-9999.</td> 
   </tr>
  --> 
 </tbody> 
</table>

#### [!UICONTROL Search for records]

Dieses Suchmodul sucht in einem -Objekt nach Datensätzen, [!DNL Jira Software] mit der angegebenen Suchanfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, nach dem das Modul suchen soll. Wenn Sie einen Datensatztyp auswählen, werden im Modul andere für diesen Datensatztyp spezifische Felder angezeigt.</p> 
    <ul> 
     <li>[!UICONTROL Issues]</li> 
     <li> <p>[!UICONTROL Issues by JQL (Jira Query Lanuguage)] </p> <p>Weitere Informationen zu JQL finden Sie unter <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a> auf der Atlassian-Hilfeseite. </p> </li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Project by issue]</li> 
     <li>[!UICONTROL User]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
