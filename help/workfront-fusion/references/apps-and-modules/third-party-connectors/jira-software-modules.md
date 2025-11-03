---
title: Jira Software-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die  [!DNL Jira] -Software verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 92cac080-d8f6-4770-a6a6-8934538c978b
source-git-commit: d4bdc4005a3b7b22d64adc8ca1d20bcf534ddfd1
workflow-type: tm+mt
source-wordcount: '2466'
ht-degree: 6%

---

# [!DNL Jira Software]

>[!NOTE]
>
>Diese Anweisungen gelten für die alten Jira Cloud- und Jira Server-Connectoren. Anweisungen zur neuen Version des Jira-Connectors, der einfach Jira heißt, finden Sie unter [Jira-Module](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md).

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Jira Software] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Diese Anweisungen gelten sowohl für Jira Cloud- als auch für Jira Server-Module.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

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

## Verbinden von [!DNL Jira Software] mit Workfront Fusion

Ihre Verbindungsmethode hängt davon ab, ob Sie [!DNL Jira Cloud] oder [!DNL Jira Server] verwenden.

* [Verbinden  [!DNL Jira Cloud]  Workfront Fusion](#connect-jira-cloud-to-workfront-fusion)
* [Verbinden  [!DNL Jira Server]  Workfront Fusion](#connect-jira-server-to-workfront-fusion)

### Verbinden von [!DNL Jira Cloud] mit Workfront Fusion

Verbinden von [!DNL Jira Cloud] mit Workfront Fusion

Um [!DNL Jira Software] mit Workfront Fusion zu verbinden, müssen Sie ein API-Token erstellen und es zusammen mit Ihrer Service-URL und Ihrem Benutzernamen in das Feld [!UICONTROL Verbindung erstellen] in Workfront Fusion einfügen.

#### Erstellen eines API-Tokens in [!DNL Jira]

1. Erstellen Sie in Jira ein API-Token.

   Für Anweisungen empfehlen wir die Suche nach „Erstellen eines API-Tokens“ in der Jira-Dokumentation.
1. Kopieren Sie das Token nach dem Erstellen an einen sicheren Speicherort.

   >[!IMPORTANT]
   >
   >Sie können das Token nach dem Schließen dieses Dialogfelds nicht mehr anzeigen.
1. Bewahren Sie das generierte Token an einem sicheren Ort auf.
1. Fahren Sie mit [Konfigurieren des  [!DNL Jira] -Tokens in Workfront Fusion](#configure-the-jira-api-token-in-workfront-fusion) fort.

#### Konfigurieren des [!DNL Jira]-API-Tokens in Workfront Fusion

1. Klicken Sie in einem beliebigen [!DNL Jira Cloud] in Workfront Fusion **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Geben Sie die folgenden Informationen an:

   * **Umgebung**
   * **Typ**
   * **[!UICONTROL Service-URL]:** Dies ist die Basis-URL, mit der Sie auf Ihr Jira-Konto zugreifen. Beispiel: `yourorganization.atlassian.net`
   * **[!UICONTROL Benutzername]**
   * **[!UICONTROL API-Token]:** Dies ist das API-Token, das Sie im Abschnitt [Erstellen eines API [!DNL Jira]](#create-an-api-token-in-jira)Tokens in diesem Artikel erstellt haben.

1. Klicken Sie [!UICONTROL Fortfahren], um die Verbindung herzustellen und zum Modul zurückzukehren.

### Verbinden von [!DNL Jira Server] mit Workfront Fusion

Um eine Verbindung zwischen Workfront Fusion und [!DNL Jira Server] zu autorisieren, benötigen Sie Ihren Kundenschlüssel, privaten Schlüssel und die Service-URL. Möglicherweise müssen Sie sich für diese Informationen an Ihren [!DNL Jira] wenden.

* [Generieren von öffentlichen und privaten Schlüsseln für  [!DNL Jira]  Verbindung](#generate-public-and-private-keys-for-your-jira-connection)
* [Konfigurieren Sie die Client-App als Verbraucher in [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)
* [Erstellen einer Verbindung zu  [!DNL Jira]  oder Jira Data Center in Workfront Fusion](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Generieren von öffentlichen und privaten Schlüsseln für Ihre [!DNL Jira]

Um einen privaten Schlüssel für Ihre [!DNL Workfront Fusion Jira]-Verbindung zu erhalten, müssen Sie öffentliche und private Schlüssel generieren. Dies erfolgt über das Terminal Ihres Computers. Sie können Ihr Terminal finden, indem Sie im Startmenü oder in der Computer-Suchleiste (nicht in der Browser-Suchleiste) nach Terminal suchen.

1. Führen Sie in Ihrem Terminal die folgenden `openssl` Befehle aus.

   * `openssl genrsa -out jira_privatekey.pem 1024`

     Dieser Befehl generiert einen privaten 1024-Bit-Schlüssel.

   * `openssl req -newkey rsa:1024 -x509 -key jira_privatekey.pem -out jira_publickey.cer -days 365`

     Dieser Befehl erstellt ein X509-Zertifikat.

   * `openssl pkcs8 -topk8 -nocrypt -in jira_privatekey.pem -out jira_privatekey.pcks8`

     Mit diesem Befehl wird der private Schlüssel (PKCS8-Format) in die `jira_privatekey.pcks8`-Datei extrahiert.

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
     >1. Kopieren Sie die Terminal-Ausgabe, einschließlich `-------BEGIN PUBLIC KEY--------` und `-------END PUBLIC KEY--------`.
     >   
     >1. Fügen Sie die Terminal-Ausgabe in eine Datei mit dem Namen `jira_publickey.pem` ein.


1. Fahren Sie fort [Konfigurieren der Client-App als Verbraucher in [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)

#### Konfigurieren der Client-App als Verbraucher in [!DNL Jira]

1. Melden Sie sich bei Ihrer [!DNL Jira] an.
1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL [!DNL Jira]Einstellungen]** ![Jira settings icon](/help/workfront-fusion/references/apps-and-modules/assets/jira-settings-icon.png) > **[!UICONTROL Applications]**> **[!UICONTROL Application links]**.
1. Geben **[!UICONTROL im Feld „URL der Anwendung eingeben, die verknüpft werden soll]** Folgendes ein

   ```
   https://app.workfrontfusion.com/oauth/cb/workfront-jiraserver-oauth1
   ```

1. Klicken Sie **[!UICONTROL Neuen Link erstellen]**. Ignorieren Sie die Fehlermeldung „Keine Antwort von der eingegebenen URL erhalten“.
1. Geben Sie im Fenster **[!UICONTROL Anwendungen verknüpfen]** Werte in die Felder **[!UICONTROL Consumer Key]** und **[!UICONTROL Shared Secret]** ein.

   Sie können die Werte für diese Felder auswählen.

1. Kopieren Sie die Werte der Felder **[!UICONTROL Consumer Key]** und **[!UICONTROL Shared Secret]** an einen sicheren Speicherort.

   Sie benötigen diese Werte später im Konfigurationsprozess.

1. Füllen Sie die URL-Felder wie folgt aus:

   | Feld | Beschreibung |
   |---|---|
   | [!UICONTROL Anfrage-Token-URL] | `<Jira base url>/plugins/servlet/oauth/request-token` |
   | [!UICONTROL Autorisierungs-URL] | `<Jira base url>/plugins/servlet/oauth/authorize` |
   | [!UICONTROL Zugriffstoken-URL] | `<Jira base url>/plugins/servlet/oauth/access-token` |

1. Aktivieren Sie das **[!UICONTROL Eingehenden Link erstellen]**.
1. Klicken Sie auf **[!UICONTROL Fortfahren]**.
1. Füllen Sie im Fenster **[!UICONTROL Anwendungen verknüpfen]** die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col data-mc-conditions=""> 
    <col data-mc-conditions=""> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Consumer key]</p> </td> 
      <td> Fügen Sie den Consumer Key ein, den Sie an einen sicheren Speicherort kopiert haben.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Kundenname]</td> 
      <td>Geben Sie einen Namen Ihrer Wahl ein. Dieser Name dient als Referenz.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Öffentlicher Schlüssel]</td> 
      <td>Fügen Sie den öffentlichen Schlüssel aus Ihrer <code>[!DNL jira_publickey.pem]</code> ein.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie auf **[!UICONTROL Fortfahren]**.
1. Fahren Sie fort [Erstellen einer Verbindung mit [!DNL Jira Server]  oder  [!DNL Jira Data Center]  Workfront Fusion](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Erstellen einer Verbindung zu [!DNL Jira Server] oder [!DNL Jira Data Center] in Workfront Fusion

>[!NOTE]
>
>Verwenden Sie die [!DNL Jira Server]-App, um eine Verbindung zu [!DNL Jira Server] oder [!DNL Jira Data Center] herzustellen.

1. Klicken Sie in einem beliebigen [!DNL Jira Server] in Workfront Fusion **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Füllen [!UICONTROL  im Bedienfeld ]Verbindung erstellen“ die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Verbindungsname]</p> </td> 
      <td> <p>Geben Sie einen Namen für die Verbindung ein.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Umgebung]</p> </td> 
      <td> <p>Wählen Sie aus, ob Sie eine Produktions- oder eine Nicht-Produktionsumgebung verwenden.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Typ]</p> </td> 
      <td> <p>Wählen Sie aus, ob Sie ein Service-Konto oder ein persönliches Konto verwenden.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Consumer key]</td> 
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

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Jira Software] Module und ihre Felder

Beim Konfigurieren von [!DNL Jira Software] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Jira Software] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Trigger

#### [!UICONTROL Auf Datensätze achten]

Dieses Trigger-Modul startet ein Szenario, wenn ein Datensatz hinzugefügt, aktualisiert oder gelöscht wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Wählen Sie den Webhook aus, den Sie auf Datensätze überwachen möchten. </p> <p>So fügen Sie einen neuen Webhook hinzu:</p> 
    <ol> 
     <li value="1">Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong></li> 
     <li value="2">Geben Sie einen Namen für den Webhook ein.</li> 
     <li value="3"> <p>Wählen Sie die Verbindung aus, die Sie für Ihren Webhook verwenden möchten. </p> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit Workfront Fusion</a> in diesem Artikel.</p> </li> 
     <li value="4"> <p>Wählen Sie den Datensatztyp aus, auf den die Software achten soll:</p> 
      <ul> 
       <li>[!UICONTROL-Kommentar] </li> 
       <li>[!UICONTROL Problem]</li> 
       <li>[!UICONTROL-Projekt] </li> 
       <li>[!UICONTROL Sprint]</li> 
      </ul> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Problem zum Sprint hinzufügen]](#add-issue-to-sprint)
* [[!UICONTROL Datensatz erstellen]](#create-a-record)
* [[!UICONTROL Benutzerdefinierter API-Aufruf]](#custom-api-call)
* [[!UICONTROL Löschen eines Datensatzes]](#delete-a-record)
* [[!UICONTROL Anlage herunterladen]](#download-an-attachment)
* [[!UICONTROL Eintrag lesen]](#read-a-record)
* [[!UICONTROL Aktualisieren eines Datensatzes]](#update-a-record)

#### [!UICONTROL Problem zum Sprint hinzufügen]

Dieses Aktionsmodul fügt einem Sprint ein oder mehrere Probleme hinzu.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sprint-ID]</td> 
   <td>Geben Sie die Sprint-ID des Sprints ein, dem Sie ein Problem hinzufügen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Problem-ID oder Schlüssel]</td> 
   <td>Klicken Sie für jedes Problem oder jeden Schlüssel, das/den Sie anzeigen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie die Problem-ID oder den Schlüssel ein. Sie können bis zu 50 in einem Modul eingeben.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datensatz erstellen]

Dieses Aktionsmodul erstellt einen neuen Datensatz in Jira.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den das Modul erstellen soll, und füllen Sie dann die anderen Felder aus, die für diesen Datensatztyp spezifisch sind und im Modul angezeigt werden.</p> 
    <ul> 
     <li>[!UICONTROL-Anhang]</li> 
     <li>[!UICONTROL-Kommentar]</li> 
     <li>[!UICONTROL Problem]</li> 
     <li>[!UICONTROL-Projekt]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Arbeitsprotokoll]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Jira Software]-API durchführen. Verwenden Sie dieses Modul, um eine Datenflussautomatisierung zu erstellen, die von den anderen [!DNL Jira Software] nicht durchgeführt werden kann.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Pfad eingeben für<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Löschen eines Datensatzes]

Dieses Aktionsmodul löscht den angegebenen Datensatz.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den das Modul löschen soll. </p> 
    <ul> 
     <li>[!UICONTROL-Anhang]</li> 
     <li>[!UICONTROL-Kommentar]</li> 
     <li>[!UICONTROL Problem]</li> 
     <li>[!UICONTROL-Projekt]</li> 
     <li>[!UICONTROL Sprint] </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID oder Schlüssel]</td> 
   <td>Geben Sie die ID oder den Schlüssel des Datensatzes ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Anlage herunterladen]

Dieses Aktionsmodul lädt eine bestimmte Anlage herunter.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Anhangs ein, den Sie herunterladen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eintrag lesen]

Dieses Aktionsmodul liest Daten aus einem einzelnen Datensatz in [!DNL Jira Software].

Sie geben die ID des Datensatzes an.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ [!DNL Jira] Datensatzes aus, den das Modul lesen soll.</p> 
    <ul> 
     <li>[!UICONTROL-Anhang]</li> 
     <li>[!UICONTROL Problem]</li> 
     <li>[!UICONTROL-Projekt]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL-Benutzer]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Ausgaben aus, die Sie empfangen möchten. Die Ausgabeoptionen sind je nach dem im Feld "[!UICONTROL Record Type]" ausgewählten Datensatztyp verfügbar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Geben Sie die eindeutige [!DNL Jira Software]-ID des Datensatzes ein, den das Modul lesen soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren eines Datensatzes]

Dieses Aktionsmodul aktualisiert einen vorhandenen Datensatz, z. B. ein Problem oder Projekt.

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den das Modul aktualisieren soll. Wenn Sie einen Datensatztyp auswählen, werden im Modul andere für diesen Datensatztyp spezifische Felder angezeigt.</p> 
    <ul> 
     <li>[!UICONTROL-Kommentar]</li> 
     <li>[!UICONTROL Problem]</li> 
     <li>[!UICONTROL-Projekt]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Problem beim Übergang]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID oder Schlüssel]</td> 
   <td>Geben Sie die ID oder den Schlüssel des Datensatzes, den Sie aktualisieren möchten, ein oder ordnen Sie ihn zu und füllen Sie dann die anderen Felder aus, die für diesen Datensatztyp spezifisch sind und im Modul angezeigt werden.</td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL Einträge auflisten]](#list-records)
* [[!UICONTROL Suche nach Datensätzen]](#search-for-records)

>[!IMPORTANT]
>
>Das vom alten Jira-Connector verwendete Suchmodul kann zu folgendem Fehler führen:
>
>`[410] The requested API has been removed. Please migrate to the /rest/api/3/search/jql API. A full migration guideline is available at https://developer.atlassian.com/changelog/#CHANGE-2046`
>
>Dies ist auf eine Funktionseinstellung aufseiten von Jira zurückzuführen.
>
>Wenn dieser Fehler auftritt, können Sie das Suchmodul des alten Jira-Connectors durch das Suchmodul des neuen Connectors ersetzen. Beachten Sie, dass Sie beim neuen Connector die verwendete API-Version auswählen können. Achten Sie darauf, beim Erstellen der Verbindung V3 auszuwählen.
>
> ![API-Versionsoption im neuen Jira-Connector](/help/workfront-fusion/references/apps-and-modules/assets/jira-version-option.png)
>
>Hinweis:
>
>* Betroffen ist nur das Suchmodul. Derzeit sind andere vom Fusion-Connector verwendete Jira-API-Endpunkte hiervon nicht betroffen.
>
>* Der geografische Rollout kann zu Inkonsistenzen führen. Atlassian führt diese Änderung regional ein, was bedeutet, dass einige Jira-Cloud-Instanzen ggf. noch vorübergehend ältere Endpunkte unterstützen. Dies kann in allen Umgebungen zu inkonsistentem Verhalten führen.

#### [!UICONTROL Einträge auflisten]

Dieses Suchmodul ruft alle Elemente eines bestimmten Typs ab, die Ihrer Suchanfrage entsprechen

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Datensatztyp aus, den das Modul auflisten soll. Wenn Sie einen Datensatztyp auswählen, werden im Modul andere für diesen Datensatztyp spezifische Felder angezeigt.</p> 
    <ul> 
     <li>[!UICONTROL-Kommentar]</li> 
     <li>[!UICONTROL Problem]</li> 
     <li>[!UICONTROL-Projekt]</li> 
     <li>[!UICONTROL Sprint-Problem]</li> 
     <li>[!UICONTROL Arbeitsprotokoll]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Max. Ergebnisse]</p> </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus abrufen soll, oder mappen Sie sie.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Enter or map the ID of the first item you want to retrieve details for. This is a way to paginate the records. If you enter the 5000th item as the offset, the module would return items 5000-9999.</td> 
   </tr>
  --> 
 </tbody> 
</table>

#### [!UICONTROL Suche nach Datensätzen]

Dieses Suchmodul sucht in einem -Objekt nach Datensätzen, [!DNL Jira Software] mit der angegebenen Suchanfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Jira Software]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von [!DNL Jira Software] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, nach dem das Modul suchen soll. Wenn Sie einen Datensatztyp auswählen, werden im Modul andere für diesen Datensatztyp spezifische Felder angezeigt.</p> 
    <ul> 
     <li>[!UICONTROL Probleme]</li> 
     <li> <p>[!UICONTROL Probleme nach JQL (Jira-Abfragesprache)] </p> <p>Weitere Informationen zu JQL finden Sie unter <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a> auf der Atlassian-Hilfeseite. </p> </li> 
     <li>[!UICONTROL-Projekt]</li> 
     <li>[!UICONTROL Projekt nach Problem]</li> 
     <li>[!UICONTROL-Benutzer]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
