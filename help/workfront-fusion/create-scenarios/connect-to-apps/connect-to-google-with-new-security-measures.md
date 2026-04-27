---
title: Verbinden von Adobe Workfront Fusion mit Google Services mit aktualisierten Sicherheitsmaßnahmen
description: Google has introduced restrictions on how users can use their API. This article describes how to connect Adobe Workfront Fusion to Google, accounting for these update security measures.
author: Becky
feature: Workfront Fusion
exl-id: eac7ba26-664e-464c-b05c-8c2ebf407fb3
source-git-commit: bbd1ec27e52127c8814188612a1e8d5cfab0cd25
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 18%

---

# Verbinden von Adobe Workfront Fusion mit Google Services mit aktualisierten Sicherheitsmaßnahmen

Google has introduced restrictions on how users can use their API. This article describes how to connect Adobe Workfront Fusion to Google, accounting for these update security measures.

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
   <p>Betriebsbasiert: keine Workfront Fusion-Lizenz erforderlich</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Google Services restrictions

Google introduced restrictions on how users can use their API as of June 1st, 2020. These security measures protect Google users from leakage or misuse of their personal data on Google.

These restrictions are related to the Gmail and Google Drive apps.

For more information about these restrictions, see &quot;Additional Requirements for Specific API Scopes&quot; in the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy#additional_requirements_for_specific_api_scopes)

To access restricted scopes, the connected service (Adobe Workfront Fusion or any other service that accesses the user&#39;s data via the API) must be verified, and must have a Letter of Assessment to prove that the service is secure and transparent about how they use the data. Workfront Fusion complies with all of Google&#39;s requirements for access to restricted scopes. However, most of the third-party connected services in Workfront Fusion don&#39;t have the Letter of Assessment, and therefore don&#39;t comply with Google terms. Because of that, Workfront Fusion is not permitted to send data to these services.

## Exceptions to Google Services restrictions

There are a few exceptions that make it possible to send data to an unapproved third-party service that doesn&#39;t have the Letter of Assessment without violating any of the new restrictions. They differ based on Google Workspace with the Workfront Fusion OAuth client, Google Workspace with another OAuth client, or @gmail.com and @googlemail.com.

* [Google Workspace with Workfront Fusion OAuth client](#google-workspace-with-workfront-fusion-oauth-client)
* [Google Workspace with another OAuth client](#google-workspace-with-another-oauth-client)
* [@gmail.com and @googlemail.com](#gmailcom-and-googlemailcom)

### Google Workspace with Workfront Fusion OAuth client

Workfront Fusion uses the Domain-wide Installation exception. Domain-wide Installation is suited for Google Workspace users, and allows users to integrate unapproved services without any limitations. If you are a Google Workspace user, you don&#39;t have to perform any additional steps and can directly connect to unapproved services.

### Google Workspace with another OAuth client

Google Workspace-Benutzende, die lieber ihren eigenen OAuth-Client statt des Workfront Fusion-OAuth-Clients verwenden, können sich über den Internal Use-Ansatz mit Google Services verbinden. Diese Option ist für fortgeschrittene Benutzer gedacht. Anweisungen finden Sie unter [Verbinden von Adobe Workfront Fusion mit Google Services mithilfe eines benutzerdefinierten OAuth-Clients](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

### @gmail.com und @googlemail.com {#gmailcom-and-googlemailcom}

Benutzende, die über @gmail.com oder @googlemail.com auf Google-Services zugreifen, können über den Ansatz der persönlichen Nutzung eine Verbindung zu Google-Services herstellen. Diese Option ist für fortgeschrittene Benutzer gedacht. Anweisungen finden Sie unter [Verbinden von Adobe Workfront Fusion mit Google Services mithilfe eines benutzerdefinierten OAuth-Clients](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## Häufig gestellte Fragen

* [Welche Apps in Adobe Workfront Fusion sind betroffen?](#what-apps-in-adobe-workfront-fusion-are-affected)
* [Habe ich ein Google Workspace-Konto?](#do-i-have-a-g-suite-account)
* [Was sollte ich tun, wenn ich @gmail.com oder @googlemail.com verwende?](#what-should-i-do-if-im-gmailcom-or-googlemailcom-user)
* [Was sollte ich tun, wenn ich Google Workspace verwende?](#what-should-i-do-if-im-a-g-suite-user)

### Welche Apps in Adobe Workfront Fusion sind betroffen? {#what-apps-in-adobe-workfront-fusion-are-affected}

Google Drive, Gmail und E-Mail (mit dem Gmail-Konto verbunden).

### Habe ich ein Google Workspace-Konto? {#do-i-have-a-g-suite-account}

Wenn Ihre E-Mail-Adresse mit @gmail.com oder @googlemail.com endet, ist Ihr Konto kein Google Workspace-Konto. Wenn Ihr Google-Konto mit einer benutzerdefinierten Domain wie @my-company.com endet, ist es ein Google Workspace-Konto.

### Was sollte ich tun, wenn ich @gmail.com oder @googlemail.com user bin? {#what-should-i-do-if-im-gmailcom-or-googlemailcom-user}

Diese neuen Einschränkungen gelten nur, wenn Sie Google Drive oder Gmail integrieren. Wenn Sie eine Verbindung zu Google Drive oder Gmail herstellen möchten, können Sie

* Wechseln Sie zu Google Workspace.

  oder

* Erstellen Sie einen benutzerdefinierten OAuth-Client. Diese Option ist für fortgeschrittene Benutzer gedacht.

  Anweisungen finden Sie unter [Verbinden von Adobe Workfront Fusion mit Google Services mithilfe eines benutzerdefinierten OAuth-Clients](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Wenn Sie einen anderen Service als Google Drive oder Gmail integrieren möchten, gelten diese Einschränkungen nicht.

### Was sollte ich tun, wenn ich Google Workspace verwende? {#what-should-i-do-if-im-a-g-suite-user}

Es ist keine Aktion erforderlich.
