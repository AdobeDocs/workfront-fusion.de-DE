---
title: Aufrufen der MS Graph REST-API
description: Aufrufen der MS Graph REST API über das Adobe Workfront Fusion HTTP &> Erstellen eines OAuth 2.0-Anfragemoduls
author: Becky
feature: Workfront Fusion
exl-id: f411c807-955d-44fe-98b1-3ebba3fe0861
source-git-commit: a7ee3e751b75523c4da62cea71e59a63f98b95e0
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 2%

---

# Aufrufen der MS Graph REST-API

Viele Microsoft-Web-Services sind über die Microsoft Graph-API zugänglich. Sie können eine Verbindung zur Microsoft Graph-API herstellen, indem Sie das Workfront Fusion-HTTP > OAuth 2.0-Anfragemodul erstellen.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz</td> 
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Prime oder Workfront-Plan auswählen: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>Ultimate Workfront Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Registrieren von Workfront Fusion im Microsoft Application Registration Portal

Um eine Verbindung zur Microsoft Graph REST API herzustellen, müssen Sie zunächst Adobe Workfront Fusion registrieren.

1. Beginnen Sie mit der Registrierung einer neuen Anwendung, wie unter [Registrieren einer Anwendung bei der Microsoft Identity Platform](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) in der Dokumentation zu Microsoft beschrieben.

   Im Rahmen der Registrierung benötigt Microsoft die folgenden Informationen:

   <table style="table-layout:auto">
      <tr>
        <td>Anwendungsname</td>
        <td>Geben Sie einen Namen für das Programm ein, z. B. „Mein Workfront Fusion-Programm“.</td>
      </tr>
      <tr>
        <td>Redirect URL</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/oauth2</code></td>
      </tr>
    </table>

1. Notieren Sie sich die Anwendungs-ID, wenn Sie die App-Registrierung abgeschlossen haben.

   >[!IMPORTANT]
   >
   >Sie benötigen die Anwendungs-ID, um Ihre Verbindung in Workfront Fusion einzurichten.

1. Generieren Sie ein Client-Geheimnis. Notieren Sie sich dieses Geheimnis.

   Anweisungen finden Sie unter [Registrieren einer Anwendung bei der Microsoft Identity Platform](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) in der Dokumentation zu Microsoft.

   >[!IMPORTANT]
   >
   >Sie benötigen das Client-Geheimnis, um Ihre Verbindung in Workfront Fusion einzurichten.

1. Konfigurieren Sie die Berechtigungen für Ihr Programm.

   Einzelheiten zum Auffinden und Konfigurieren dieser Felder finden Sie im Abschnitt „Konfigurieren von Berechtigungen für Microsoft-Diagramme“ in [Zugriff ohne Benutzer erhalten](https://docs.microsoft.com/en-us/graph/auth-v2-service) der Dokumentation zu Microsoft.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Welche Art von Berechtigungen benötigt Ihre Anwendung?</td> 
      <td>Wählen Sie <code>Delegated permissions</code> aus.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Berechtigungen auswählen</td> 
      <td> <p>Wählen Sie die folgenden Berechtigungen aus:</p> 
       <ul> 
        <li> <p><code>offline_access</code> </p> </li> 
        <li> <p><code>openid</code> </p> </li> 
        <li> <p>Alle anderen für Ihre Integrationen erforderlichen Berechtigungen (Beispiel: <code>User.Read</code>)</p> </li> 
       </ul> <p><b>Wichtig</b>: Sie benötigen die ausgewählten Berechtigungen, um Ihre Verbindung in Workfront Fusion einzurichten.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Fahren Sie [Konfigurieren Ihrer MS Graph API-Verbindung in Workfront Fusion](#configure-your-ms-graph-api-connection-in-workfront-fusion) fort.

## Konfigurieren der MS Graph API-Verbindung in Workfront Fusion

Nach der Registrierung von Workfront Fusion wie unter [Registrieren von Workfront Fusion im Microsoft Application Registration Portal](#register-workfront-fusion-in-the-microsoft-application-registration-portal) beschrieben, können Sie Ihre Verbindung im HTTP > Erstellen einer OAuth 2.0-Anfrage-Modul konfigurieren.

1. Fügen Sie Ihrem Szenario ein HTTP > OAuth 2.0-Aufrufmodul hinzu.
1. Klicken Sie **Hinzufügen** neben dem Feld Verbindung .
1. Konfigurieren Sie die Verbindungsfelder wie folgt:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Name der Verbindung</td> 
      <td>Geben Sie einen Namen für die Verbindung ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Umgebung</p> </td> 
      <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Produktions- oder Nicht-Produktionskonto herstellen. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Typ</p> </td> 
      <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Flusstyp</p> </td> 
      <td>Wählen Sie <code>Authorization Code</code> aus. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Autorisierungs-URI</td> 
      <td><code>https://login.microsoftonline.com/common/oauth2/v2.0/authorize</code> eingeben. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token-URI</td> 
      <td><code>https://login.microsoftonline.com/common/oauth2/v2.0/token</code> eingeben. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Umfang</td> 
      <td> <p>Geben Sie die Berechtigungen ein, die Sie bei der Registrierung ausgewählt haben, wie unter <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Registrieren von Workfront Fusion im Microsoft-</a> beschrieben.</p> <p>Klicken Sie für jeden Bereich auf <b>Hinzufügen</b> und geben Sie die Berechtigung ein.</p> <p>Beispiel: <code>offline_access</code>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Bereichstrennzeichen</td> 
      <td>Wählen Sie <code>SPACE</code> aus. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Client-ID</td> 
      <td>Geben Sie die Anwendungs-ID aus Schritt 2 in <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Registrieren von Workfront Fusion im Microsoft-</a> ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Geheimer Client-Schlüssel</td> 
      <td>Geben Sie das Client-Geheimnis ein, das Sie in Schritt 3 unter <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Registrieren von Workfront Fusion im Microsoft-</a> generiert haben.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Parameter zulassen</td> 
      <td> <p>Fügen Sie die folgenden Autorisierungsparameter hinzu. Klicken Sie für jeden Parameter, den Sie hinzufügen<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein: </p> 
       <ul> 
        <li> <p>Schlüssel:<code> response_mode</code> Wert: <code>query</code></p> </li> 
        <li> <p>Schlüssel: <code>prompt </code>Wert: <code>consent</code></p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Zugriffstoken-Parameter</td> 
      <td>Sie müssen in dieses Feld nichts eingeben.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token-Parameter aktualisieren</td> 
      <td> 
       <ol> 
        <li value="1"> <p>Klicken Sie <b>Element hinzufügen</b>.</p> </li> 
        <li value="2"> <p>Geben Sie <b> Feld </b>Schlüssel“ <code>scope</code> ein.</p> </li> 
        <li value="3"> <p>Geben <b> im Feld </b> alle Bereiche ein, die Sie in das Feld Umfang eingegeben haben, getrennt durch Leerzeichen.</p> <p>Beispiel: <code>offline_access openid User.Read</code></p> </li> 
       </ol> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Benutzerdefinierte Kopfzeilen</td> 
      <td>Sie müssen in dieses Feld nichts eingeben.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token-Platzierung</td> 
      <td><code>In the header</code> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **Weiter**.
1. Klicken Sie im eingeblendeten Fenster auf **Akzeptieren**, um die Verbindung herzustellen und zum Modul zurückzukehren.
