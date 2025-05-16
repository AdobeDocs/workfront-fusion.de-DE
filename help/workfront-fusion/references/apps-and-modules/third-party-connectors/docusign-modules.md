---
title: DocuSign-Module
description: Mit  [!DNL Adobe Workfront Fusion DocuSign]  Modulen können Sie den Umschlagstatus überwachen und abrufen, Umschläge suchen und abrufen oder ein Dokument herunterladen und senden, um sich bei Ihrem  [!DNL DocuSign]  anzumelden.
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
source-git-commit: 2b2030d062b5ec8c81476a8950fee3b15f96dcd2
workflow-type: tm+mt
source-wordcount: '2200'
ht-degree: 0%

---

# DocuSign-Module

Mit den [!DNL Adobe Workfront Fusion] [!DNL DocuSign]-Modulen können Sie den Umschlagstatus überwachen und abrufen, Umschläge suchen und abrufen oder ein Dokument herunterladen und senden, um sich bei Ihrem [!DNL DocuSign]-Konto anzumelden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

Um [!DNL DocuSign]-Module verwenden zu können, müssen Sie über ein [!DNL DocuSign]-Konto verfügen.

## DocuSign-API-Informationen

Der DocuSign-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>1.18.11</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL DocuSign] mit [!DNL Workfront Fusion] verbinden {#connect-docusign-to-workfront-fusion}

So erstellen Sie eine Verbindung für Ihre [!DNL DocuSign]:

1. Klicken Sie **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung], wenn Sie mit der Konfiguration des ersten [!DNL DocuSign] beginnen.
1. Geben Sie Folgendes ein:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Verbindungsname]</p> </td> 
      <td>Geben Sie einen Namen für die neue [!DNL DocuSign] ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Umgebung]</p> </td> 
      <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktionsumgebung in einer produktionsfremden Umgebung herstellen möchten.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Verbindungsname]</p> </td> 
      <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Kontotyp]</td> 
      <td>Wählen Sie aus, ob das Konto, mit dem Sie eine Verbindung herstellen möchten, ein Produktionskonto oder ein Demokonto ist.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **Fortfahren**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## [!DNL DocuSign] Module und ihre Felder

Beim Konfigurieren [!DNL DocuSign] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL DocuSign] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)

### Auslöser

#### [!UICONTROL Briefumschläge ansehen]

Dieses Trigger-Modul startet ein Szenario, in dem ein Umschlag gesendet, zugestellt, signiert, abgeschlossen oder abgelehnt wird.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von DocuSign mit Workfront </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Konto] </td> 
   <td> <p>Wählen Sie das Konto aus, das die Datensätze enthält, die Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ereignistyp]</td> 
   <td> <p> Wählen Sie den Ereignistyp aus, den Sie beobachten möchten.</p> 
    <ul> 
     <li>[!UICONTROL Dokument abgeschlossen]</li> 
     <li>[!UICONTROL Dokument abgelehnt]</li> 
     <li>[!UICONTROL Dokument gesendet]</li> 
     <li>[!UICONTROL Dokument signiert]</li> 
     <li>[!UICONTROL Neues Dokument im Posteingang]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Ausgaben]</p> </td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Modulausgabe aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Benutzerdefiniertes Feld hinzufügen]](#add-a-custom-field)
* [[!UICONTROL Empfänger zu Umschlag hinzufügen]](#add-recipient-to-envelope)
* [[!UICONTROL Erstellen Sie einen neuen Umschlag]](#create-a-new-envelope)
* [[!UICONTROL Benutzerdefinierter API-Aufruf]](#custom-api-call)
* [[!UICONTROL Dokument herunterladen]](#download-a-document)
* [[!UICONTROL Benutzerdefiniertes Feld ändern]](#modify-custom-field)
* [[!UICONTROL Einen Umschlag lesen]](#read-an-envelope)
* [[!UICONTROL Briefumschlag senden]](#send-envelope)
* [[!UICONTROL Datei in einen Briefumschlag hochladen]](#upload-a-file-to-an-envelope)

#### [!UICONTROL Benutzerdefiniertes Feld hinzufügen]

Dieses Aktionsmodul fügt dem Dokument ein benutzerdefiniertes Feld hinzu

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Konto] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Dokument enthält, dem Sie ein benutzerdefiniertes Feld hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die ID des Umschlags ein, der das Dokument enthält, dem Sie ein benutzerdefiniertes Feld hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Feldname]</td> 
   <td>Geben Sie einen Namen für das neue Feld ein, das Sie hinzufügen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL erforderlich]</td> 
   <td>Aktivieren Sie diese Option, wenn das hinzugefügte Feld ein erforderliches Feld sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Feld anzeigen]</td> 
   <td>Aktivieren Sie diese Option, wenn das Feld sichtbar sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Wert]</td> 
   <td>Geben Sie den Wert (Inhalt) des hinzugefügten Felds ein oder ordnen Sie ihn zu. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Empfänger zu Umschlag hinzufügen]

Dieses Aktionsmodul fügt einen oder mehrere Empfänger zu einem vorhandenen Umschlag hinzu. Wenn der Umschlag bereits gesendet wurde, wird dem Empfänger eine E-Mail gesendet. Dieses Modul gilt nicht für Umschläge, die bereits abgeschlossen wurden.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres DocuSign-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL -Konto] </td>
   <td> <p>Wählen Sie das Konto aus, das den Umschlag enthält, dem Sie Empfänger hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Envelope ID]</td>
    <td>Wählen Sie die Zuordnung oder die ID des Umschlags aus, dem Sie den Empfänger hinzufügen möchten.</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[!UICONTROL Empfängertyp]</td>
   <td> <p> Wählen Sie den Empfängertyp aus, den Sie dem Umschlag hinzufügen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agent]</p> </li> 
     <li> <p>[!UICONTROL Carbon Copy]</p> </li> 
     <li> <p>[!UICONTROL Zertifizierter Versand]</p> </li> 
     <li> <p>[!UICONTROL in-person-signer]</p> </li> 
     <li> <p>[!UICONTROL Intermediär]</p> </li> 
     <li> <p>[!UICONTROL -Signierer]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL E-Mail]</td>
   <td> <p>Geben Sie die E-Mail-Adresse des Empfängers ein, den Sie zum Umschlag hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Name]</td>
   <td>Geben Sie den Namen des Empfängers ein, den Sie dem Umschlag hinzufügen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Routing-Reihenfolge]</td>
   <td> <p>Routingnummer des Empfängers eingeben oder zuordnen. Die Routing-Nummer bestimmt die Reihenfolge, in der Empfänger Ihre Dokumente erhalten und signieren.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL E-Mail-Text]</td>
   <td>Geben Sie den Text (Inhalt) der E-Mail ein, die an den Empfänger gesendet wird, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL E-Mail-Betreff]</td>
   <td>Geben Sie den Betreff der E-Mail ein, die an den Empfänger gesendet wird, oder ordnen Sie ihn zu.</td> 
  </tr> 
    <td role="rowheader">[!UICONTROL Private Nachricht]</td>
   <td> Wenn Sie eine private Nachricht an den Empfänger senden möchten, geben Sie den Text der Nachricht ein oder ordnen Sie ihn zu. <p>Nur der ausgewählte Empfänger sieht die private Nachricht sowie die allgemeine Nachricht. Die private Nachricht ist auf 1.000 Zeichen begrenzt.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Authentifizierung]</td> 
   <td> <p>Wählen Sie die Authentifizierungsmethode aus, mit der Sie die Identität des Empfängers bestätigen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL None]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL -Zugriffscode]</strong> </p> <p>Geben Sie den Zugriffscode ein oder ordnen Sie ihn zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Phone]</strong> </p> <p>Geben Sie die Telefonnummer ein oder mappen Sie sie.</p> </li> 
     <li> <p><strong>[!UICONTROL SMS]</strong> </p> <p>Geben Sie die Telefonnummer ein oder mappen Sie sie.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen Sie einen neuen Umschlag]

Dieses Aktionsmodul erstellt aus einer Vorlage einen neuen Umschlag. Gibt die ID des neuen Envelopes sowie den Status des neuen Envelopes zurück.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL -Verbindung] </td>

<td> <p>Anweisungen zum Verbinden Ihres DocuSign-Kontos mit Workfront Fusion finden Sie in den Artikeln unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL -Konto] </td>
   <td> <p>Wählen Sie das Konto aus, das den Umschlag enthält, in den Sie eine Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL -Vorlage]</td>
   <td> <p> Wählen Sie die Vorlage aus, aus der Sie den neuen Umschlag erstellen möchten. Vorlagen sind basierend auf dem ausgewählten [!UICONTROL -Konto] verfügbar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL nach der Erstellung]
   </td> 
   <td> <p>Wählen Sie aus, ob Sie den Umschlag als Entwurf speichern oder zum Signieren senden möchten.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Vorlagenempfänger]</td>
    <td>Klicken Sie für jeden Empfänger, den Sie diesem Umschlag hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die folgenden Details ein:
    <ul>
    <li><b>Zugriffscode</b><p>Geben Sie den Code ein, mit dem der Empfänger auf den Umschlag zugreift, oder ordnen Sie ihn zu.<p></li>
    <li><b>E-Mail</b><p>Geben Sie die E-Mail-Adresse des Empfängers ein oder mappen Sie sie.<p></li>
    <li><b>Name</b><p>Geben Sie den Namen des Empfängers ein oder mappen Sie ihn.<p></li>
    <li><b>Rollenname</b><p>Geben Sie den Rollennamen des Empfängers ein oder ordnen Sie ihn zu.<p></li>
    <li><b>Routing-Reihenfolge</b><p>Routingnummer des Empfängers eingeben oder zuordnen. Die Routing-Nummer bestimmt die Reihenfolge, in der Empfänger Ihre Dokumente erhalten und signieren.<p></li>
    </ul>
    </td>
    </tr>
  <tr> 
   <td role="rowheader">
     [!UICONTROL Drucken und Signieren zulassen]
   </td> 
   <td> <p>Aktivieren Sie diese Option, damit der Empfänger das Dokument drucken und das Papier unterschreiben kann.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Neuzuweisung zulassen]
   </td> 
   <td> <p>Aktivieren Sie diese Option, wenn die Empfänger die Dokumente einem anderen Benutzer zuweisen können sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Empfängerrekursion zulassen]
   </td> 
   <td> <p>Aktivieren Sie diese Option, um eine Rekursion der Empfänger zuzulassen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Autorisierende Kopie]
   </td> 
   <td> <p>Aktivieren Sie diese Einstellung, um Dokumente in diesem Briefumschlag als Originalkopien zu kennzeichnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Automatische Navigation]
   </td> 
   <td> <p>Aktivieren Sie diese Option, um die automatische Navigation für den Empfänger festzulegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Brand ID]
   </td> 
   <td> <p>Geben Sie die ID der Marke ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Markup enabled]
   </td> 
   <td> <p>Aktivieren Sie diese Option, um Dokument-Markup zu aktivieren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Expire enabled]
   </td> 
   <td> <p>Aktivieren Sie diese Option, um eine Gültigkeit für diesen Umschlag festzulegen. Wenn Sie diese Option aktivieren, füllen Sie die folgenden Felder aus:<ul><li><b>Läuft ab nach</b><p>Geben Sie die Anzahl der Tage ein, nach denen dieser Umschlag abläuft, oder mappen Sie sie.</p></li><li><b>Ablaufwarnung</b><p>Geben Sie die Anzahl der Tage vor Ablauf der Gültigkeit ein, für die eine Erinnerungs-E-Mail an den Empfänger gesendet wird, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL body]
   </td> 
   <td> <p>Geben Sie den Text (Inhalt) der E-Mail ein, die mit diesem Umschlag verbunden ist, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Betreff]
   </td> 
   <td> <p>Geben Sie den Betreff der E-Mail ein, die mit diesem Umschlag verbunden ist, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Konto]</td> 
   <td>Geben Sie das Konto ein, das Sie für den Zugriff auf die [!DNL DocuSign]-API verwenden möchten, oder ordnen Sie es zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Pfad relativ zu eingeben oder zuordnen <code>https://&lt;BASE_URI>/v2/accounts/&lt;ACCOUNT_ID>.</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Dadurch wird der Inhaltstyp der Anfrage bestimmt.</p> <p>Beispiel:<code> {"Content-type":"application/json"}</code></p> <p>Hinweis: Wenn Fehler auftreten und es schwierig ist, deren Ursprung zu ermitteln, sollten Sie die Kopfzeilen basierend auf der [!DNL Workfront] Dokumentation ändern. Wenn Ihr benutzerdefinierter API-Aufruf einen 422-HTTP-Anfragefehler zurückgibt, versuchen Sie es mit einer „Content-Type“:„text/plain“-Kopfzeile.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Ergebnissen ein, die während eines Ausführungszyklus bearbeitet werden sollen, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Beispiel:** Listenumschläge

Der folgende API-Aufruf gibt Umschläge ab dem angegebenen Datum in Ihrem [!DNL DocuSign]-Konto zurück:

**URL**: `/v2.1/accounts/{accountId}/envelopes/`

**Methode**: `GET`

**Abfragezeichenfolge**:

* **key**: `from_date`

* **Wert**: `YYYY-MM-DD`

Gibt an, wann mit der Prüfung auf Statusänderungen für Umschläge im Konto begonnen wird.

![Beispiel für DocuSign-Einrichtung](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)

Das Ergebnis finden Sie in der -Ausgabe des Moduls unter Paket > Hauptteil > Umschläge.

In unserem Beispiel wurden 6 Umschläge zurückgegeben:

![Beispiel für DocuSign-Ausgabe](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

>[!ENDSHADEBOX]

#### [!UICONTROL Dokument herunterladen]

Dieses Aktionsmodul lädt ein einzelnes Dokument herunter.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Konto] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Dokument enthält, das Sie herunterladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die Kennung des Umschlags ein, den Sie herunterladen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Dokument-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Dokuments ein, das Sie herunterladen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Zertifikat]</td> 
   <td>Aktivieren Sie diese Option, um das Envelope-Signaturzertifikat in den Download einzuschließen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokumente nach Benutzer-ID]</td> 
   <td>Aktivieren Sie diese Option, damit Empfängerinnen und Empfänger Dokumente nach Benutzer-ID abrufen können. Wenn beispielsweise ein(e) Benutzende(r) in zwei verschiedenen Routing-Aufträgen mit unterschiedlichen Sichtbarkeiten enthalten ist, werden bei Verwendung dieser Option alle Dokumente aus beiden Routen zurückgegeben.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL verschlüsseln]</td> 
   <td>Aktivieren Sie diese Option, wenn die in der Antwort zurückgegebenen PDF-Bytes für alle in Ihrem [!DNL DocuSign] konfigurierten Schlüsselmanager verschlüsselt werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Wählen Sie die Sprache.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Änderungen anzeigen]</td> 
   <td>Aktivieren Sie diese Option, um geänderte Felder für die zurückgegebene PDF gelb zu markieren und optionale Signaturen oder Initialen rot zu kennzeichnen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wasserzeichen]</td> 
   <td> <p>Aktivieren Sie diese Option, um die Wasserzeichenfunktion zu aktivieren. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Benutzerdefiniertes Feld ändern]

Dieses Aktionsmodul ändert ein benutzerdefiniertes Feld mithilfe des Feldnamens.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Konto] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Dokument enthält, in dem Sie ein benutzerdefiniertes Feld ändern möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die ID des Umschlags ein, der das Dokument enthält, in dem Sie ein benutzerdefiniertes Feld ändern möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Feld-ID]</td> 
   <td>Geben Sie die ID des Felds ein, das Sie ändern möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Feldname]</td> 
   <td>Geben Sie den Namen des Felds ein, das Sie ändern möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL erforderlich]</td> 
   <td>Aktivieren Sie diese Option, wenn das geänderte Feld ein erforderliches Feld sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Feld anzeigen]</td> 
   <td>Aktivieren Sie diese Option, wenn das Feld sichtbar sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Wert]</td> 
   <td>Geben Sie den Wert (Inhalt) des geänderten Felds ein oder ordnen Sie ihn zu. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Einen Umschlag lesen]

Dieses Aktionsmodul liest Informationen über einen Envelope in [!DNL DocuSign] unter Verwendung der Envelope-ID.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Konto] </td> 
   <td> <p>Wählen Sie das Konto aus, das das Dokument enthält, dessen Informationen Sie lesen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die Kennung des Umschlags ein, der das Dokument enthält, aus dem Informationen gelesen werden sollen, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Eigenschaften aus, die in der Modulausgabe angezeigt werden sollen. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Briefumschlag senden]

Dieses Aktionsmodul sendet einen Briefumschlag-Entwurf an seine Empfänger.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Konto] </td> 
   <td> <p>Wählen Sie das Konto aus, das den Briefumschlagentwurf enthält, den Sie an die Empfänger senden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die ID des Briefumschlags-Entwurfs ein, den Sie an die Empfänger senden möchten, oder mappen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei in einen Briefumschlag hochladen]

Dieses Modul lädt eine angegebene Datei in einen vorhandenen Envelope in DocuSign hoch.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL DocuSign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL DocuSign] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Konto] </td> 
   <td> <p>Wählen Sie das Konto aus, das den Umschlag enthält, in den Sie eine Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Geben Sie die ID des Umschlags ein, in den Sie eine Datei hochladen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder geben Sie den Namen und die Daten der Quelldatei ein.</td> 
  </tr> 
 </tbody> 
</table>
