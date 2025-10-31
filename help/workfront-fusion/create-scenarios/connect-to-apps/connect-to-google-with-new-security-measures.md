---
title: Verbinden von Adobe Workfront Fusion mit Google Services mit aktualisierten Sicherheitsmaßnahmen
description: Google hat Einschränkungen für die Verwendung seiner API eingeführt. In diesem Artikel wird beschrieben, wie Sie Adobe Workfront Fusion mit Google verbinden, wobei diese Sicherheitsmaßnahmen für die Aktualisierung berücksichtigt werden.
author: Becky
feature: Workfront Fusion
exl-id: eac7ba26-664e-464c-b05c-8c2ebf407fb3
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Verbinden von Adobe Workfront Fusion mit Google Services mit aktualisierten Sicherheitsmaßnahmen

Google hat Einschränkungen für die Verwendung seiner API eingeführt. In diesem Artikel wird beschrieben, wie Sie Adobe Workfront Fusion mit Google verbinden, wobei diese Sicherheitsmaßnahmen für die Aktualisierung berücksichtigt werden.

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

## Einschränkungen bei Google Services

Google hat ab dem 1. Juni 2020 Einschränkungen für die Verwendung seiner API eingeführt. Diese Sicherheitsmaßnahmen schützen Google-Benutzer vor unbeabsichtigten oder missbräuchlichen Verwendungen ihrer personenbezogenen Daten in Google.

Diese Einschränkungen beziehen sich auf die Apps Gmail und Google Drive.

Weitere Informationen zu diesen Einschränkungen finden Sie unter „Zusätzliche Anforderungen für bestimmte API-Bereiche“ in der [Benutzerdatenrichtlinie für Google-API-Services](https://developers.google.com/terms/api-services-user-data-policy#additional_requirements_for_specific_api_scopes)

Um auf eingeschränkte Bereiche zugreifen zu können, muss der verbundene Dienst (Adobe Workfront Fusion oder jeder andere Dienst, der über die API auf die Daten des Benutzers zugreift) überprüft werden. Außerdem muss er über ein Bewertungsschreiben verfügen, um nachzuweisen, dass der Dienst bei der Verwendung der Daten sicher und transparent ist. Workfront Fusion erfüllt alle Google-Anforderungen für den Zugriff auf eingeschränkte Bereiche. Allerdings verfügen die meisten der mit Workfront Fusion verbundenen Services von Drittanbietern nicht über das Beurteilungsschreiben und erfüllen daher nicht die Google-Bedingungen. Aus diesem Grund ist es Workfront Fusion nicht gestattet, Daten an diese Services zu senden.

## Ausnahmen von den Google Services-Einschränkungen

Es gibt einige Ausnahmen, die es ermöglichen, Daten an einen nicht genehmigten Drittanbieterdienst zu senden, der nicht über das Begutachtungsschreiben verfügt, ohne die neuen Einschränkungen zu verletzen. Sie unterscheiden sich je nach Google Workspace mit dem Workfront Fusion OAuth-Client, Google Workspace mit einem anderen OAuth-Client oder @gmail.com und @googlemail.com.

* [Google Workspace mit Workfront Fusion OAuth-Client](#google-workspace-with-workfront-fusion-oauth-client)
* [Google Workspace mit einem anderen OAuth-Client](#google-workspace-with-another-oauth-client)
* [@gmail.com und @googlemail.com](#gmailcom-and-googlemailcom)

### Google Workspace mit Workfront Fusion OAuth-Client

Workfront Fusion verwendet die Domain-weite Installationsausnahme. Die Domain-weite Installation ist für Benutzende von Google Workspace geeignet und ermöglicht es Benutzenden, nicht genehmigte Services ohne Einschränkungen zu integrieren. Wenn Sie ein Google Workspace-Benutzer sind, müssen Sie keine zusätzlichen Schritte ausführen und können direkt eine Verbindung zu nicht genehmigten Services herstellen.

### Google Workspace mit einem anderen OAuth-Client

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

* Zu Google Workspace wechseln

  oder

* Erstellen Sie einen benutzerdefinierten OAuth-Client. Diese Option ist für fortgeschrittene Benutzer gedacht.

  Anweisungen finden Sie unter [Verbinden von Adobe Workfront Fusion mit Google Services mithilfe eines benutzerdefinierten OAuth-Clients](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Wenn Sie einen anderen Service als Google Drive oder Gmail integrieren möchten, gelten diese Einschränkungen nicht.

### Was sollte ich tun, wenn ich Google Workspace verwende? {#what-should-i-do-if-im-a-g-suite-user}

Es ist keine Aktion erforderlich.
