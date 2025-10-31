---
title: Verbinden von Adobe Workfront Fusion mit Google Services mithilfe eines benutzerdefinierten OAuth-Clients
description: Sie können Adobe Workfront Fusion verwenden, um mithilfe eines benutzerdefinierten OAuth-Clients eine Verbindung zu Google Services herzustellen. Für dieses Verfahren ist ein bestehendes Google-Konto erforderlich.
author: Becky
feature: Workfront Fusion
exl-id: 2f0bc289-4ecf-4a31-9d7b-641bbca6fc95
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 1%

---

# Verbinden von Adobe Workfront Fusion mit Google Services mithilfe eines benutzerdefinierten OAuth-Clients

Sie können Adobe Workfront Fusion verwenden, um mithilfe eines benutzerdefinierten OAuth-Clients eine Verbindung zu Google Services herzustellen. Für dieses Verfahren ist ein bestehendes Google-Konto erforderlich.

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

Sie benötigen ein bestehendes Google-Konto, um diese Verbindung herzustellen.

## Verbinden von Fusion mit Google-Services mithilfe eines benutzerdefinierten OAuth-Clients

Um diese Verbindung zu erstellen, müssen Sie ein Projekt auf Google Cloud Platform erstellen und konfigurieren und dann die Verbindung in Fusion basierend auf diesem Projekt konfigurieren.

>[!NOTE]
>
>Dieses Verfahren ist für Folgendes gedacht:
>
>* Persönlicher Gebrauch (`@gmail.com` und `@googlemail.com`)
>* Interne Verwendung (Google Workspace-Benutzende, die einen benutzerdefinierten OAuth-Client bevorzugen)

* [Erstellen eines Projekts in Google Cloud Platform](#create-a-project-on-google-cloud-platform)
* [Konfigurieren der OAuth-Einverständniseinstellungen](#configure-oauth-consent-settings)
* [OAuth-Anmeldedaten erstellen](#create-oauth-credentials)
* [Verbinden mit Google in Workfront Fusion](#connect-to-google-in-workfront-fusion)

### Erstellen eines Projekts in Google Cloud Platform

So erstellen Sie ein Projekt in Google Cloud Platform:

1. Beginnen Sie mit der Erstellung eines Projekts auf Google Cloud Platform.

   Anweisungen finden Sie unter [Erstellen eines Google Cloud-Projekts](https://developers.google.com/workspace/guides/create-project) in der Dokumentation zu Google.
1. Beim Aktivieren von APIs müssen Sie die Google Drive-API sowie die API aller Google-Apps aktivieren, die Sie verwenden möchten (z. B. die Google Sheets-API).
1. Erstellen Sie das Projekt fertig.
1. Fahren Sie mit dem Abschnitt [Konfigurieren der OAuth-](#configure-oauth-consent-settings)&quot; in diesem Artikel fort.

### Konfigurieren der OAuth-Einverständniseinstellungen

1. Konfigurieren von OAuth für Ihr Projekt

   Anweisungen finden Sie unter [Konfigurieren des OAuth-Einverständnisbildschirms und Auswählen von Bereichen](https://developers.google.com/workspace/guides/configure-oauth-consent) in der Dokumentation zu Google.
1. Wählen Sie **Extern** aus und klicken Sie dann auf **Erstellen**.

   >[!NOTE]
   >
   >Bei Auswahl dieser Option fallen keine Gebühren an. Weitere Informationen finden Sie in den Google-Informationen zu Ausnahmen von den Prüfanforderungen.

1. Füllen Sie die erforderlichen Felder wie folgt aus:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>App-Name</p> </td> 
      <td> <p>Geben Sie den Namen der App ein, die um Zustimmung bittet.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>Adobe Workfront Fusion </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Support-E-Mail</td> 
      <td>Geben Sie eine E-Mail-Adresse ein, an die sich Benutzer bei Fragen zu ihrem Einverständnis wenden können, wenn sie eine Verbindung zu dieser App herstellen.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">E-Mail-Adressen</td> 
      <td>Geben Sie eine oder mehrere E-Mail-Adressen ein, die Google verwenden kann, um Sie über Änderungen an Ihrem Projekt zu informieren.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie unter Autorisierte Domains auf **Domain hinzufügen** und geben Sie `workfrontfusion.com` ein.
1. Fügen Sie die folgenden Bereiche hinzu:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Service/API</th> 
      <th>Erforderliche Bereiche</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td> <p>Gmail</p> </td> 
      <td> <p>https://mail.google.com/</p> <p>https://www.googleapis.com/auth/gmail.labels</p> <p>https://www.googleapis.com/auth/gmail.send</p> <p>https://www.googleapis.com/auth/gmail.readonly</p> <p>https://www.googleapis.com/auth/gmail.compose</p> <p>https://www.googleapis.com/auth/gmail.insert</p> <p>https://www.googleapis.com/auth/gmail.modify</p> <p>https://www.googleapis.com/auth/gmail.metadata</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Google Drive</p> </td> 
      <td> <p>https://www.googleapis.com/auth/drive</p> <p>https://www.googleapis.com/auth/drive.readonly</p> </td> 
     </tr> 
    </tbody> 
   </table>

   Möglicherweise müssen Sie die Liste erweitern oder zur nächsten Seite der Liste gehen, um alle Einträge anzuzeigen.

1. (Optional) Fügen Sie dem Projekt Testbenutzer hinzu.
1. Überprüfen Sie Ihre Informationen auf Genauigkeit und klicken Sie dann auf **Zurück zum Dashboard**.

   >[!NOTE]
   >
   >Sie müssen Ihren Einverständnisbildschirm und Ihren Antrag nicht zur Verifizierung durch Google einreichen.

1. Fahren Sie fort [OAuth-Anmeldeinformationen erstellen](#create-oauth-credentials).

### OAuth-Anmeldedaten erstellen

1. Erstellen Sie die OAuth Client-ID-Anmeldeinformationen.

   Anweisungen finden Sie unter [Erstellen von Zugriffsberechtigungen](https://developers.google.com/workspace/guides/create-credentials) in der Dokumentation zu Google.

   >[!NOTE]
   >
   >Wenn dies nicht die erste API oder der erste Service (Gmail oder Google Drive) ist, die bzw. den Sie aktiviert haben, müssen Sie keine neuen Anmeldeinformationen erstellen.

1. Füllen Sie die erforderlichen Felder wie folgt aus:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Anwendungstyp</td> 
      <td> <p> Web-Anwendung</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Name</td> 
      <td>Workfront Fusion </td> 
     </tr> 
    </tbody> 
   </table>

1. Geben Sie unter Autorisierte Umleitungs-URIs **einen** folgenden Werte ein:

   * Für Gmail oder Google Drive: `https://app.workfrontfusion.com/oauth/cb/google-restricted`

   * Für andere Google-Apps: `https://app.workfrontfusion.com/oauth/cb/google`

1. Klicken Sie auf **Erstellen**.

   Die Client-ID und das Client-Geheimnis werden angezeigt.

1. Kopieren Sie die Client-ID und den geheimen Client-Schlüssel an einen sicheren Speicherort. Sie werden sie verwenden, um eine Verbindung in Workfront Fusion herzustellen.
1. Fahren Sie [Verbindung zu Google in Workfront Fusion herstellen](#connect-to-google-in-workfront-fusion) fort.

### Verbinden mit Google in Workfront Fusion

Der Prozess der Verbindungsherstellung zu Google unterscheidet sich, je nachdem, ob Sie ein Modul aus einem Google-Service (z. B. Google Sheets oder Google Docs) verwenden oder ob Sie über das HTTP > OAuth2.0-Anfragemodul eine Verbindung zu Google herstellen.

* [Herstellen einer Verbindung zu Google in einem Google-Service](#connect-to-google-in-a-google-service)
* [Stellen Sie im HTTP > OAuth2.0-Anforderungsmodul eine Verbindung zu Google her.](#connect-to-google-in-the-http--make-an-oauth20-request-module)

#### Herstellen einer Verbindung zu Google in einem Google-Service

1. Suchen Sie in Workfront Fusion das Google-Modul, für das Sie eine Verbindung erstellen müssen.
1. Klicken Sie **Verbindung erstellen** und anschließend auf **Erweiterte Einstellungen anzeigen**.
1. Füllen Sie je nach Bedarf die Felder „Verbindungsname“, „Umgebung“ und „Typ“ aus.
1. Geben Sie die Client-ID und das Client-Geheimnis, die Sie unter [OAuth-Anmeldeinformationen erstellen](#create-oauth-credentials) abgerufen haben, in die entsprechenden Felder ein und klicken Sie dann auf **Weiter**.

1. Melden Sie sich mit Ihrem Google-Konto an.

   Das Fenster **Diese App ist nicht verifiziert** wird angezeigt. Beachten Sie, dass die im Fenstertitel erwähnte „App“ der OAuth-Client ist, den Sie oben erstellt haben.

1. Klicken Sie auf **Erweitert** und dann auf **Wechseln zu Workfront Fusion (unsicher)**, um den Zugriff mithilfe Ihres benutzerdefinierten OAuth-Clients zuzulassen.

1. Klicken Sie **Zulassen**, um Workfront Fusion die Berechtigung zu erteilen.
1. Klicken Sie im angezeigten Fenster erneut auf **Zulassen**, um Ihre Auswahl zu bestätigen.

   Die Verbindung zum gewünschten Google-Service mithilfe eines benutzerdefinierten OAuth-Clients wird hergestellt.

#### Stellen Sie im HTTP > OAuth2.0-Anforderungsmodul eine Verbindung zu Google her. {#connect-to-google-in-the-http--make-an-oauth20-request-module}

Anweisungen zum Herstellen einer Verbindung zu Google im HTTP > Erstellen einer OAuth2.0-Anfrage-Modul finden Sie unter [Anweisungen zum Erstellen einer Verbindung zu Google im HTTP > Erstellen eines OAuth 2.0-Anfrage-Moduls](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module) im Artikel HTTP > Erstellen eines OAuth 2.0-Anfrage-Moduls.

## Mögliche Fehlermeldung: [403 Zugriff nicht konfiguriert]

Wenn die `403 Access Not Configured` Fehlermeldung angezeigt wird, müssen Sie die entsprechende API in Ihrer Google Cloud-Plattform aktivieren. Um die API zu aktivieren, führen Sie die Schritte im Abschnitt [Erstellen eines Projekts auf der Google Cloud Platform](#create-a-project-on-google-cloud-platform) in diesem Artikel aus.
