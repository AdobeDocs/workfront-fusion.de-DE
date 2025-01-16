---
title: Verbinden von Adobe Workfront Fusion mit einem Webservice, der die API-Token-Autorisierung verwendet
description: Einige Services lassen keine Integrationslösungen wie Adobe Workfront Fusion zu, um eine App zu erstellen, die Sie in Ihrem Szenario einfach verwenden können.
author: Becky
feature: Workfront Fusion
exl-id: 4a8ac816-52de-41e8-96d7-1c8cde2ebe32
source-git-commit: 362952ec85b0df2306ba117ba530e95201330cca
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 1%

---

# Verbinden von Adobe Workfront Fusion mit einem Webservice, der die API-Token-Autorisierung verwendet

Einige Services lassen keine Integrationslösungen wie Adobe Workfront Fusion zu, um eine App zu erstellen, die Sie in Ihrem Szenario einfach verwenden können.

Um diese Situation zu umgehen, verbinden Sie den gewünschten Service (die App) mit Workfront Fusion über das HTTP-Modul > Anfrage stellen .

In diesem Artikel wird erläutert, wie Sie mithilfe eines API-Schlüssels/API-Tokens nahezu jeden Webservice mit Workfront Fusion verbinden.

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

## Herstellen einer Verbindung zu einem Webdienst, der ein API-Token verwendet

Die Vorgehensweise beim Verbinden des Service über ein API-Token ist bei den meisten Web-Services ähnlich.

1. Erstellen Sie eine Anwendung auf der Website des Webservices, wie im Abschnitt [Erstellen einer neuen Anwendung und Abrufen des API-Tokens](#create-a-new-application-and-obtain-the-api-token) in diesem Artikel erläutert.
1. Abrufen des API-Schlüssels oder API-Tokens.
1. Fügen Sie das HTTP-Modul > Anfrage erstellen von Workfront Fusion zu Ihrem Szenario hinzu.
1. Richten Sie das Modul gemäß der API-Dokumentation des Web-Services ein und führen Sie das Szenario aus, wie in Abschnitt [Einrichten des HTTP-Moduls](#set-up-the-http-module) in diesem Artikel beschrieben.

>[!NOTE]
>
>Dieses Beispiel stellt eine Verbindung zum Pushover-Benachrichtigungs-Service her.

## Erstellen eines neuen Programms und Abrufen des API-Tokens

>[!NOTE]
>
>Es gibt viele verschiedene Möglichkeiten, wie Web-Services API-Schlüssel oder API-Token erstellen und verteilen. Anweisungen zum Abrufen eines API-Schlüssels und eines Tokens für Ihren gewünschten Webservice finden Sie auf der Website des Services nach „API-Schlüssel“ oder „API-Token“.
>
>Wir enthalten Anweisungen zum Abrufen eines Pushover-API-Schlüssels nur als Beispiel für das, was Sie möglicherweise finden.

1. Melden Sie sich bei Ihrem Pushover-Konto an.
1. Klicken **unten auf der Seite auf &quot;**/API-Token erstellen“.
1. Füllen Sie die Informationen aus und klicken Sie auf **Anwendung erstellen**.
1. Bewahren Sie das bereitgestellte API-Token an einem sicheren Ort auf. Sie benötigen es für das Workfront Fusion-HTTP > Erstellen eines Anfragemoduls , um eine Verbindung zum gewünschten Webservice herzustellen (in diesem Fall Pushover).

## Einrichten des HTTP-Moduls

Um einen Webservice mit Ihrem Workfront Fusion-Szenario zu verbinden, müssen Sie das HTTP-Modul > Anfrage stellen im Szenario verwenden und das Modul gemäß der API-Dokumentation des Webservices einrichten.

1. Fügen Sie das Modul HTTP > Anfrage stellen zu Ihrem Szenario hinzu.
1. Um eine Nachricht mithilfe von Workfront Fusion zu pushen, richten Sie das HTTP-Modul wie folgt ein.

   >[!NOTE]
   >
   >Diese Moduleinstellungen entsprechen der Pushover-Webservice-API-Dokumentation. Die Einstellungen für andere Webdienste können sich unterscheiden. Beispielsweise kann das API-Token in die Kopfzeile und nicht in das Feld Hauptteil eingefügt werden.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> URL</td> 
      <td> <p><code>https://api.pushover.net/1/messages.json</code> </p> <p>Das URL-Feld enthält den Endpunkt, den Sie in der API-Dokumentation des Webservices finden.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> Methode</td> 
      <td> <p><code>POST</code> </p> <p>Die verwendete Methode hängt vom entsprechenden Endpunkt ab. Der Pushover-Endpunkt für das Pushen von Nachrichten verwendet die POST -Methode.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Kopfzeilen</p> </td> 
      <td> <p>Einige Webdienste verwenden möglicherweise Kopfzeilen, um das API-Token oder andere Parameter für die Authentifizierung anzugeben. Dies ist in unserem Beispiel nicht der Fall, da der Endpunkt des Pushover für das Pushen von Nachrichten den Hauptteil (siehe unten) für alle Anfragetypen verwendet.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Abfragezeichenfolge</p> </td> 
      <td> <p>Einige Webdienste verwenden möglicherweise eine Abfragezeichenfolge, um andere Parameter anzugeben. Dies ist in unserem Beispiel nicht der Fall, da der Pushover-Webservice Body (siehe unten) für alle Anfragetypen verwendet.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Textkörper</p> </td> 
      <td> <p><code>Raw</code> </p> <p>Mit dieser Einstellung können Sie den JSON-Inhaltstyp im Feld Inhaltstyp unten auswählen.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Inhaltstyp</p> </td> 
      <td> <p><code>JSON (application/json)</code> </p> <p>JSON ist der erforderliche Inhaltstyp der Pushover-App. Dies kann sich von anderen Web-Services unterscheiden.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Inhalt anfordern</p> </td> 
      <td> <p>Geben Sie den Inhalt der Hauptteilanfrage im JSON-Format ein. Sie können das Modul JSON &gt; JSON erstellen verwenden, wie in <a href="#map-the-json-body-using-the-json--create-json-module" class="MCXref xref">Zuordnen des JSON-Bodys mithilfe des Moduls JSON &gt; JSON erstellen</a> in diesem Artikel erläutert. Sie können den JSON-Inhalt auch manuell eingeben, wie in <a href="#enter-the-json-body-manually" class="MCXref xref">JSON-Text manuell eingeben</a> in diesem Artikel beschrieben.</p> <p>Die erforderlichen Parameter für diesen Webdienst finden Sie in der API-Dokumentation des Webdienstes.</p> </td>

   </tr> 
    </tbody> 
   </table>

## JSON-Text manuell eingeben

Geben Sie Parameter und Werte im JSON-Format an.

>[!BEGINSHADEBOX]

**Beispiel:**

```
{"user":"12345c2ecu1hq42ypqzhswbyam34",
"token":"123459evz8aepwtxydndydgyumbfx",
"message":"Hello World!",
"title":"The Push Notification"}
```

>[!ENDSHADEBOX]

Dieses Beispiel enthält die folgenden Informationen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p> Benutzer</p> </td> 
   <td> <p>Ihr USER_KEY. Dies finden Sie in Ihrem Pushover-Dashboard.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> Token </td> 
   <td> <p>Ihr API-Token/API-Schlüssel, der generiert wurde, als Sie Ihre Pushover-App erstellt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> Nachricht </td> 
   <td> <p>Der Textinhalt der Push-Benachrichtigung, die an das/die Gerät(e) gesendet wird.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> Anrede </td> 
   <td> <p>(Optional) Der Titel Ihrer Nachricht. Wenn kein Wert eingegeben wird, wird der Name Ihrer App verwendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ordnen Sie den JSON-Text mithilfe des JSON- > JSON erstellen -Moduls zu

Das Modul JSON erstellen erleichtert die Angabe von JSON. Außerdem haben Sie die Möglichkeit, Werte dynamisch zu definieren.

Weitere Informationen zu den JSON-Modulen finden Sie unter [JSON-](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/json-modules.md).

1. Geben Sie die Werte ein, aus denen Sie JSON erstellen möchten, oder ordnen Sie sie zu.

   ![](/help/workfront-fusion/create-scenarios/connect-to-apps/assets/json-values-350x288.png)

1. Verbinden Sie das Modul JSON > JSON erstellen mit dem Modul HTTP > Anfrage stellen .
1. Ordnen Sie die JSON-Zeichenfolge aus dem Modul JSON erstellen dem Inhaltsfeld Anfrage im Feld HTTP > Modul Anfrage erstellen zu.

Wenn Sie das Szenario ausführen, wird die Push-Benachrichtigung an das Gerät gesendet, das in Ihrem PushOver-Konto registriert wurde.
