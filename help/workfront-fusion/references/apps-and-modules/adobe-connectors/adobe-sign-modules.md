---
title: Adobe Acrobat Sign-Module
description: Mit den  [!DNL Adobe Acrobat Sign] -Modulen können Sie ein  [!DNL Adobe Workfront Fusion]  auf der Grundlage von Ereignissen in Ihrem  [!DNL Adobe] Acrobat Sign-Konto starten, Vereinbarungen erstellen, lesen oder aktualisieren und andere Datensätze suchen, anhand der von Ihnen festgelegten Kriterien nach Datensätzen suchen und Dokumente hochladen.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0ef9d40e-8ad6-434e-8fa0-076920ff29ea
source-git-commit: 85cd8dbf70dff220f593fa669b447bf5df2a21a2
workflow-type: tm+mt
source-wordcount: '6666'
ht-degree: 0%

---

# [!DNL Adobe Acrobat Sign]

Mit den [!DNL Adobe Acrobat Sign]-Modulen können Sie ein [!DNL Adobe Workfront Fusion] Szenario auf der Grundlage von Ereignissen in Ihrem [!DNL Adobe Acrobat Sign]-Konto starten, Vereinbarungen erstellen, lesen oder aktualisieren und andere Datensätze suchen, anhand der von Ihnen festgelegten Kriterien nach Datensätzen suchen und Dokumente hochladen.

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
   <td> <p>[!UICONTROL -Plan], [!UICONTROL -Arbeit]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] for Work Automation and Integration] </p>
   </td>  
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den [!DNL Adobe Workfront] [!UICONTROL Select] oder [!UICONTROL Prime] verfügen, muss Ihr Unternehmen [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu nutzen. [!DNL Workfront Fusion] ist im [!DNL Workfront] [!UICONTROL Ultimate] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## [!DNL Adobe Acrobat Sign] API-Informationen

Der Adobe Acrobat Sign-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v6 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.35.1</td> 
  </tr>
 </tbody> 
</table>


## Empfehlungen zur Verwendung des [!DNL Adobe Acrobat Sign]-Connectors

Die [!DNL Adobe Sign]App macht die Automatisierung von eSignature-Geschäftsprozessen in [!DNL Fusion] viel einfacher und leistungsfähiger.

Neue Benutzer in [!DNL Adobe Sign] sollten einige der Einschränkungen bei der Aktualisierung von Vereinbarungen genau beachten. Vereinbarungen werden in der Regel nicht geändert, sobald sie gestartet wurden. Wir empfehlen neuen Benutzern von [!DNL Adobe Sign], sich mithilfe des Moduls zur Vertragserstellung auf die Erstellung neuer Vereinbarungen zu konzentrieren. Dies erleichtert [!DNL Fusion] Automatisierungen und verbessert die Arbeit mit [!DNL Adobe Sign].

[!DNL Adobe Sign] brauchen ein Feld, mit dem Sie arbeiten können. Es gibt einige Optionen dafür, aber die einfachste und häufigste ist das Hochladen eines vorübergehenden Dokuments und das anschließende Zuordnen dieses Dokuments zu Ihrer Vereinbarung.

![Adobe Sign-Empfehlungen](/help/workfront-fusion/references/apps-and-modules/assets/adobe-sign-recommendations-350x168.png)

## [!DNL Adobe Acrobat Sign] Module und ihre Felder

Beim Konfigurieren [!DNL Adobe Acrobat Sign] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Adobe Acrobat Sign] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

<!--
* [Watch for agreements](#watch-for-agreements) 
* [Watch for events](#watch-for-events)
-->

+++ **[!UICONTROL Auf Vereinbarungen achten]**

Dieses Trigger-Modul startet ein Szenario, wenn eine Vereinbarung erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
<td>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL filter]</td> 
   <td>Wählen Sie aus, ob auf neue, aktualisierte oder beides Datensätze geachtet werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp] </td> 
   <td>Wählen Sie den Datensatztyp aus, den der Datensatz überwachen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text suchen]</td> 
   <td> <p>Geben Sie Begriffe ein, nach denen Sie suchen möchten. Das -Modul gibt Datensätze zurück, die diese Begriffe als Feldwerte enthalten.</p> <p>Weitere Informationen zum Suchen von Feldern in [!DNL Adobe Acrobat Sign] finden Sie unter „Funktionsweise der Textsuche“ in <a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">Adobe Sign-Suche - Funktionsweise</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Vereinbarungen]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Auf Ereignisse achten]**

Dieses Ereignismodul startet ein Trigger, wenn ein ausgewähltes Ereignis auftritt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td>Wählen Sie den gewünschten Webhook aus, oder klicken Sie auf <b>[!UICONTROL Hinzufügen]</b> und füllen Sie die folgenden Felder aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name]</td> 
   <td> <p>Einen Namen für den Webhook eingeben</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Bereiche]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL -Konto]</p> </li> 
     <li> <p>[!UICONTROL -Gruppe]</p> </li> 
     <li> <p>[!UICONTROL -Benutzer]</p> </li> 
     <li> <p>[!UICONTROL -Ressource]</p> <p>Wenn Sie [!UICONTROL Resource] auswählen, geben Sie die Ressourcen-ID und den Ressourcentyp ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ressourcenebene]</td> 
   <td> <p>Wählen Sie den Ressourcentyp aus, den Sie überwachen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL -Vereinbarungen]</p> </li> 
     <li> <p>[!UICONTROL Widgets]</p> </li> 
     <li> <p>[!UICONTROL MegaSigns]</p> </li> 
     <li> <p>[!UICONTROL -Bibliotheksdokumente]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Abonnementereignisse]</td> 
   <td>Wählen Sie die [!DNL Adobe Sign] Ereignisse aus, die das Modul beobachten soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzeigename der-Anwendung]</td> 
   <td>Der Anzeigename der Anwendung, über die der Webhook erstellt wird.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anwendungsname]</td> 
   <td>Der Anzeigename der Anwendung, über die der Webhook erstellt wird.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Problem Notification emails]</td> 
   <td> <p>Diese Einstellung funktioniert nur für Administratorkonten</p> <p>Klicken Sie für jede E-Mail-Adresse, an die Sie Benachrichtigungen zu Problemen senden möchten, auf <b>[!UICONTROL Hinzufügen]</b> und geben Sie die E-Mail-Adresse ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bedingte Parameter der-Vereinbarung]</td> 
   <td>Wenn Sie bedingte Parameter hinzufügen möchten, wählen Sie <b>[!UICONTROL Yes]</b> für den Datensatztyp aus, dem Sie Parameter hinzufügen möchten, und wählen Sie dann <b>[!UICONTROL Yes]</b> für alle Parameter aus, die Sie aktivieren möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Aktionen

<!--
* [Create a record](#create-a-record) 
* [Create an agreement](#create-an-agreement) 
* [Create related records](#create-related-records) 
* [Custom API Call](#custom-api-call) 
* [List records](#list-records) 
* [Read a record](#read-a-record) 
* [Read related records](#read-related-records) 
* [Update a record](#update-a-record) 
* [Update related record](#update-related-record) 
* [Upload document](#upload-document)
-->

+++ **[!UICONTROL Datensatz erstellen]**

Dieses Aktionsmodul erstellt einen neuen Datensatz des ausgewählten Typs.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Beispiel: <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie erstellen möchten.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Group]</b> </p> </li> 
     <li> <p><b>[!UICONTROL -Bibliotheksdokument]</b> </p> </li> 
     <li> <p><b>[!UICONTROL user]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Web Form] ([!UICONTROL Widget])</b> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Gruppeninformationen]</td> 
   <td> <p>Geben Sie den [!UICONTROL Name] und die [!UICONTROL ID] der Gruppe ein oder ordnen Sie sie zu und geben Sie an, ob diese Gruppe die Standardgruppe für das Konto ist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Library Document Info]</td> 
   <td> <p>Füllen Sie die folgenden Felder aus:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Dateien] senden</b> </p> <p>Klicken Sie für jede Datei, die Sie hinzufügen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und füllen Sie die Felder aus.</p> 
      <ul> 
       <li><b>[!UICONTROL Vorübergehende Dokument-ID]</b> <p>Kennung des vorübergehenden Dokuments eingeben</p> </li> 
       <li> <p><b>[!UICONTROL URL-Dateiübertragung]</b> </p> <p>Füllen Sie die folgenden Felder aus:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL MIME-type]</b> </p> <p>Geben Sie den MIME-Typ der Originaldatei an. MIME-Typen (Multipurpose Internet Mail Extension) sind Bezeichnungen, mit denen Software verschiedene Arten von im Internet freigegebenen Daten identifizieren kann. Webserver und Browser verwenden den MIME-Typ, um zu bestimmen, was mit einer Datei getan werden soll. Beispielsweise wird eine Datei mit dem MIME-Typ <code>text/html</code> in einem Browser anders verarbeitet als eine Datei mit dem MIME-Typ <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL name]</b> </p> <p>Geben Sie einen Namen für die Datei ein.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Geben Sie die URL der Datei ein, die Sie senden möchten.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL notarize]</b> </p> <p>Wählen Sie aus, ob dieses Dokument notariell beglaubigt werden muss.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Bibliotheksvorlagenname]</b> </p> <p>Namen der Bibliotheksvorlage eingeben oder zuordnen</p> </li> 
     <li> <p><b>[!UICONTROL Freigabemodus]</b> </p> <p>Geben Sie an, wer Zugriff auf das Bibliotheksdokument haben soll.</p> </li> 
     <li> <p><b>[!UICONTROL Library Document State]</b> </p> <p>Wählen Sie aus, ob das Dokument den Status Authoring aufweist oder aktiv ist.</p> </li> 
     <li> <p><b>[!UICONTROL Bibliotheksvorlagentyp]</b> </p> <p>Klicken Sie für jeden gewünschten Bibliotheksvorlagentyp auf <b>[!UICONTROL Element hinzufügen]</b> und wählen Sie den Vorlagentyp aus.</p> </li> 
     <li> <p><b>[!UICONTROL Letztes Ereignisdatum]</b> </p> <p>Geben Sie das letzte Datum ein, an dem ein Ereignis im Bibliotheksdokument aufgetreten ist.</p> <p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
     <li> <p><b>[!UICONTROL Library Document Status]</b> </p> <p>Wählen Sie den Status des Bibliotheksdokuments aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Benutzerinformationen]</td> 
   <td> <p>Füllen Sie die folgenden Felder aus:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL email]</b> </p> <p>Geben Sie die E-Mail-Adresse des Benutzers ein.</p> </li> 
     <li> <p><b>[!UICONTROL ist Kontoadministrator]</b> </p> <p>Aktivieren Sie diese Option, wenn der erstellte Benutzer ein Kontoadministrator ist.</p> </li> 
     <li> <p><b>[!UICONTROL Benutzer-ID]</b> </p> <p>Eindeutige ID des Benutzers eingeben</p> </li> 
     <li> <p><b>[!UICONTROL Konto-ID]</b> </p> <p>Geben Sie die eindeutige ID des [!DNL Adobe Acrobat Sign] Kontos ein, das diesem Benutzer zugeordnet ist.</p> </li> 
     <li> <p><b>[!UICONTROL Vorname]</b> </p> <p>Geben Sie den Vornamen des Benutzers ein.</p> </li> 
     <li> <p><b>[!UICONTROL Nachname]</b> </p> <p>Geben Sie den Nachnamen des Benutzers ein</p> </li> 
     <li> <p><b>[!UICONTROL Firma]</b> </p> <p>Geben Sie den Namen der Firma des Benutzers ein.</p> </li> 
     <li> <p><b>[!UICONTROL -Initialen]</b> </p> <p>Geben Sie die Initialen des Benutzers ein.</p> </li> 
     <li> <p><b>[!UICONTROL locale]</b> </p> <p>Geben Sie das Gebietsschema des Benutzers ein. Dadurch wird die Sprache der Benutzeroberfläche bestimmt. </p> </li> 
     <li> <p><b>[!UICONTROL Phone]</b> </p> <p>Telefonnummer des Benutzers eingeben</p> </li> 
     <li> <p><b>Primäre Gruppen-ID</b> </p> <p>Geben Sie die Gruppe ein, der der neue Benutzer hinzugefügt wird. Wenn nichts eingegeben wird, wird der Benutzer der Standardgruppe für das Konto hinzugefügt.</p> </li> 
     <li> <p><b>[!UICONTROL Auftragstitel]</b> </p> <p>Geben Sie die Stellenbezeichnung des Benutzers ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Web-Formular-Info]</td> 
   <td> <p>Füllen Sie die folgenden Felder aus</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Datei-Info]</b> </p> <p>Klicken Sie für jede Datei, die Sie dem Web-Formular hinzufügen möchten, auf Hinzufügen und füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p>[!UICONTROL Dateityp]</p> <p>[!UICONTROL -Dokument]</p> </li> 
       <li> <p>[!UICONTROL Vorübergehendes Dokument]</p> </li> 
       <li> <p>[!UICONTROL URL-Dateiinformationen]</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Name des Web-Formulars]</b> </p> <p>Geben Sie einen Namen für das Web-Formular ein. Dieser Name wird verwendet, um das Web-Formular an Stellen wie E-Mails und Websites zu identifizieren.</p> </li> 
     <li> <p><b>[!UICONTROL Web-Formularstatus]</b> </p> <p>Wählen Sie den Status aus, in dem das neue Web-Formular erstellt werden soll.</p> </li> 
     <li> <p><b>[!UICONTROL Web Form Participant Set Info]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Member Info]</b> </p> <p>Klicken Sie für jedes Mitglied, das Sie zum Teilnehmerset hinzufügen möchten, auf <b>[!UICONTROL Element hinzufügen]</b>. </p> 
        <ul> 
         <li> <p><b>[!UICONTROL email]</b> </p> <p>Lassen Sie diese Option leer.</p> </li> 
         <li> <p><b>[!UICONTROL Sicherheitsoption]</b> </p> <p>Wenn Sie eine Sicherheitsoption zur Authentifizierung dieses Benutzers hinzufügen möchten, wählen Sie <b>[!UICONTROL Yes]</b> aus, wählen Sie dann die Sicherheitsoption aus und füllen Sie alle erforderlichen Felder aus.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL role]</b> </p> <p>Rolle auswählen. Alle Mitglieder dieses Teilnehmersatzes teilen die Rolle.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web Form Additional Participant Sets info]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Member Info]</b> </p> <p>Klicken Sie für jedes Mitglied, das Sie zum Teilnehmerset hinzufügen möchten, auf <b>[!UICONTROL Element hinzufügen]</b>.</p> 
        <ul> 
         <li> <p><b>[!UICONTROL email]</b> </p> <p>Lassen Sie diese Option leer.</p> </li> 
         <li> <p><b>[!UICONTROL Sicherheitsoption]</b> </p> <p>Wenn Sie eine Sicherheitsoption zur Authentifizierung dieses Benutzers hinzufügen möchten, wählen Sie <b>[!UICONTROL Yes]</b> aus, wählen Sie dann die Sicherheitsoption aus und füllen Sie alle erforderlichen Felder aus.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL role]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Web Form Participant ID] </b> </p> <p>Geben Sie die ID des Web-Formular-Teilnehmers ein.</p> </li> 
       <li> <p><b>[!UICONTROL order]</b> </p> <p>Geben Sie die Reihenfolge an, in der diese Teilnehmergruppe mit dem Web-Formular interagieren soll. Beispielsweise muss die Teilnehmergruppe mit dem Bestellwert 1 zuerst ausgeführt werden, 2 muss als Nächstes ausgeführt werden usw. Die Bestellnummern müssen mit einer beginnen und weisen keine Lücken in der Serie auf. </p> </li> 
       <li> <p><b>[!UICONTROL Provider Participant Set Info]</b> </p> <p>Wenn der Teilnehmer unbekannt ist, geben Sie an, ob der Provider Details für den Teilnehmer angeben muss, und geben Sie eine Nachricht mit den Details ein, die Sie für den unbekannten Teilnehmer benötigen.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Informationen zu Authentifizierungsfehlern]</b> </p> <p>Wenn Sie eine Fehler- oder Fehlerseite für Ihre Benutzer bereitstellen möchten, wählen Sie <b>[!UICONTROL Yes]</b> aus und füllen Sie dann die folgenden Felder aus:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>URL für die Fehlerseite eingeben</p> </li> 
       <li> <p><b>[!UICONTROL deframe]</b> </p> <p>Aktivieren Sie diese Option, wenn die Fehlerseite im Web-Formular angezeigt werden soll</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Geben Sie die Verzögerung in Sekunden ein, bevor der Benutzer zur Fehlerseite weitergeleitet wird.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL CC INFO]</b> </p> <p>Klicken Sie für jede E-Mail-Adresse, die Sie bei Unterzeichnung der endgültigen Vereinbarung über das Web-Formular erhalten möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie die E-Mail-Adresse ein.</p> </li> 
     <li> <p><b>[!UICONTROL Completion info]</b> </p> <p style="font-style: normal;">Wenn Sie Ihren Benutzern eine Erfolgsseite bereitstellen möchten, wählen Sie <b>[!UICONTROL Yes]</b> aus und füllen Sie dann die folgenden Felder aus:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>URL für die Erfolgsseite eingeben</p> </li> 
       <li> <p><b>[!UICONTROL deframe]</b> </p> <p>Aktivieren Sie diese Option, wenn die Erfolgsseite im Web-Formular angezeigt werden soll</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Geben Sie die Verzögerung in Sekunden ein, bevor der Benutzer zur Erfolgsseite weitergeleitet wird.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Gruppen-ID]</b> </p> <p>Geben Sie die ID der Gruppe ein, zu der das Web-Formular gehört. Wenn nichts eingegeben wird, gehört das Web-Formular zur primären Gruppe des Kontobenutzers.</p> </li> 
     <li> <p><b>[!UICONTROL Letztes Ereignisdatum]</b> </p> <p>Geben Sie das Datum ein, an dem das letzte Ereignis im Web-Formular aufgetreten ist. Verwenden Sie den <code>yyyy-MM-dd'T'HH:mm:ssZ</code>.</p> </li> 
     <li> <p><b>[!UICONTROL locale]</b> </p> <p>Geben Sie das Gebietsschema des Benutzers ein. Dadurch wird die Sprache der Benutzeroberfläche bestimmt. </p> </li> 
     <li> <p><b>[!UICONTROL Sicherheitsoption]</b> </p> <p>Geben Sie das Kennwort zum Schützen des Dokuments ein. Sie müssen dieses Passwort den relevanten Parteien separat mitteilen.</p> </li> 
     <li> <p><b>[!UICONTROL Vaulting info]</b> </p> <p>Wenn Ihr Konto für das Dokument-Vaulting eingerichtet ist und Sie die Option pro Vereinbarung aktivieren können, können Sie diese Option aktivieren, um diese Vereinbarung zu Vault.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Vereinbarung erstellen]**

Dieses Aktionsmodul erstellt eine Vereinbarung, sendet sie zur Signatur und gibt die Vereinbarungs-ID zurück.

>[!NOTE]
>
>Es wird empfohlen, das Dokument zum Signieren als vorübergehendes Dokument hochzuladen und es dann dem Feld [!UICONTROL Zu sendende Datei] im Modul [!UICONTROL Vereinbarung erstellen] zuzuordnen. Ein Beispiel finden Sie unter „Dokument hochladen“ in diesem Artikel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
<td>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Beispiel: <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zu sendende Dateien]</td> 
   <td> <p>Klicken Sie für jedes Element, das Sie in die Vereinbarung aufnehmen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und füllen Sie die folgenden Felder aus:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Dateityp]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL -Dokument]</b> </p> <p>Füllen Sie die folgenden Felder aus:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Erstellungsdatum]</b> </p> <p>Geben Sie das Datum, an dem das Dokument erstellt wurde, im Format <code>yyyy-MM-dd'T'HH:mm:ssZ</code> ein oder ordnen Sie es zu. Beispiel: <code>2016-02-25T18:46:19Z</code> stellt die UTC-Zeit dar.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Geben Sie die ID des Dokuments ein oder mappen Sie sie.</p> </li> 
         <li> <p><b>[!UICONTROL label]</b> </p> <p>Geben Sie eine eindeutige Beschriftung für die Datei ein oder mappen Sie sie. Bei einem benutzerdefinierten Workflow wird dadurch eine Datei dem entsprechenden Dateielement in der Workflow-Definition zugeordnet. Dies muss im Falle einer Anfrage zur Erstellung einer benutzerdefinierten Workflow-Vereinbarung angegeben werden.</p> </li> 
         <li> <p><b>[!UICONTROL Anzahl der Seiten]</b> </p> <p>Geben Sie die Anzahl der Seiten im Dokument ein oder mappen Sie sie.</p> </li> 
         <li> <p><b>[!UICONTROL MIME-type]</b> </p> <p>Geben Sie den MIME-Typ der Originaldatei ein oder ordnen Sie ihn zu. MIME-Typen (Multipurpose Internet Mail Extension) sind Bezeichnungen, mit denen Software verschiedene Arten von im Internet freigegebenen Daten identifizieren kann. Webserver und Browser verwenden den MIME-Typ, um zu bestimmen, was mit einer Datei getan werden soll. Beispielsweise wird eine Datei mit dem MIME-Typ <code>text/html</code> in einem Browser anders verarbeitet als eine Datei mit dem MIME-Typ <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL name]</b> </p> <p>Geben Sie einen Namen für das Dokument ein oder ordnen Sie ihn zu.<br></p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Library Document ID]</b> </p> <p>ID des Bibliotheksdokuments eingeben</p> </li> 
       <li> <p><b>[!UICONTROL Vorübergehende Dokument-ID]</b> </p> <p>Kennung des vorübergehenden Dokuments eingeben</p> </li> 
       <li> <p><b>[!UICONTROL URL-Dateiübertragung]</b> </p> <p>Füllen Sie die folgenden Felder aus:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL MIME-type]</b> </p> <p>Geben Sie den MIME-Typ der Originaldatei an. MIME-Typen (Multipurpose Internet Mail Extension) sind Bezeichnungen, mit denen Software verschiedene Arten von im Internet freigegebenen Daten identifizieren kann. Webserver und Browser verwenden den MIME-Typ, um zu bestimmen, was mit einer Datei getan werden soll. Beispielsweise wird eine Datei mit dem MIME-Typ <code>text/html</code> in einem Browser anders verarbeitet als eine Datei mit dem MIME-Typ <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL name]</b> </p> <p>Geben Sie einen Namen für die Datei ein.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Geben Sie die URL der Datei ein, die Sie senden möchten.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL label]</b> </p> <p>Geben Sie einen Titel für die Datei ein.</p> </li> 
     <li> <p><b>[!UICONTROL notarize]</b> </p> <p>Aktivieren Sie diese Option, um anzugeben, dass die Datei notariell beglaubigt werden muss.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vereinbarungsname]</td> 
   <td>Geben Sie einen Namen für die neue Vereinbarung ein. Dieser Name wird verwendet, um die Vereinbarung an Stellen wie E-Mails und Websites zu identifizieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilnehmereinstellungen Info]</td> 
   <td> <p>Klicken Sie für jedes Teilnehmerset, das Sie hinzufügen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und füllen Sie die folgenden Felder aus.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL -Member]</b> </p> <p>Klicken Sie für jede Person, die Sie zum Teilnehmerset hinzufügen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie die E-Mail-Adresse der Person ein.</p> </li> 
     <li> <p><b>[!UICONTROL order]</b> </p> <p>Geben Sie die Reihenfolge an, in der dieser Teilnehmer die Vereinbarung unterzeichnen soll. Beispielsweise muss die Teilnehmergruppe mit dem Bestellwert 1 zuerst signieren, 2 muss als Nächstes signieren usw. Die Bestellnummern müssen mit einer beginnen und weisen keine Lücken in der Serie auf. </p> </li> 
     <li> <p><b>[!UICONTROL role]</b> </p> <p>Wählen Sie eine Rolle für dieses Teilnehmerset aus. Alle Teilnehmer des Sets erhalten diese Rolle.</p> </li> 
     <li> <p><b>[!UICONTROL ID]</b> </p> <p>Die ID dieses Teilnehmersatzes eingeben oder zuordnen.</p> </li> 
     <li> <p><b>[!UICONTROL label]</b> </p> <p>Geben Sie eine eindeutige Beschriftung für das Teilnehmerset ein oder mappen Sie sie. Bei benutzerdefinierten Workflows sollte die im Teilnahmesatz angegebene Beschriftung dem Teilnahmenschritt im benutzerdefinierten Workflow zugeordnet werden.</p> </li> 
     <li> <p><b>[!UICONTROL name]</b> </p> <p>Geben Sie einen Namen für das Teilnehmerset ein. Dieser Name muss innerhalb der Vereinbarung eindeutig sein.</p> </li> 
     <li> <p><b>[!UICONTROL Private Nachricht]</b> </p> <p>Geben Sie eine Nachricht für dieses Teilnehmerset ein oder ordnen Sie sie zu. Alle Teilnehmer des Sets erhalten diese Nachricht.</p> </li> 
     <li> <p><b>[!UICONTROL Sichtbare Seiten]</b> </p> <p>Wenn für diese Vereinbarung die eingeschränkte Dokumentsichtbarkeit aktiviert ist, geben Sie an, welche Dateien für diese Teilnehmergruppe sichtbar sein sollen. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Signaturtyp]</td> 
   <td> <p>Wählen Sie den Signaturtyp aus, den die Vereinbarung erfordert.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL E-sign]</b> </p> <p>Die Vereinbarung muss elektronisch unterzeichnet werden.</p> </li> 
     <li> <p><b>[!UICONTROL Written]</b> </p> <p>Die Vereinbarung muss von Hand unterzeichnet werden, und die unterzeichnete Vereinbarung muss gescannt und hochgeladen werden.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Status]</td> 
   <td> <p>Status für diese Vereinbarung auswählen.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Authoring]</b> </p> <p>Sie können weiterhin Felder für diese Vereinbarung bearbeiten oder hinzufügen.</p> </li> 
     <li> <p><b>[!UICONTROL Draft]</b> </p> <p>Sie können diese Vereinbarung inkrementell erstellen, bevor Sie sie senden.</p> </li> 
     <li> <p><b>[!UICONTROL in Process]</b> </p> <p>Diese Vereinbarung wird sofort gesendet.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CS]</td> 
   <td> <p>Sie können diese Vereinbarung an Interessenten senden, die sie nicht unterzeichnen müssen, z. B. Stakeholder. Sie erhalten eine E-Mail zu Beginn des Signiervorgangs und eine weitere, wenn die endgültige Signatur empfangen wird. Außerdem erhalten sie eine PDF-Kopie des Vertrags. </p> <p>Klicken Sie für jede Person, die diesen Vertrag als CC verwenden möchte, auf <b>[!UICONTROL Element hinzufügen]</b> und füllen Sie die folgenden Felder aus:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL email]</b> </p> <p>Geben Sie die E-Mail-Adresse ein, die Sie für die Vereinbarung verwenden möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><b>[!UICONTROL label]</b> </p> <p>Geben Sie einen Titel für diese E-Mail-Adresse ein, wie in der Workflow-Beschreibung dargestellt.</p> </li> 
     <li> <p><b>[!UICONTROL Sichtbare Seiten]</b> </p> </li> 
     <li> <p>Wenn für diese Vereinbarung die eingeschränkte Dokumentsichtbarkeit aktiviert ist, geben Sie an, welche Dateien für diese Teilnehmergruppe sichtbar sein sollen. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email option]</td> 
   <td> <p>Wählen Sie für jeden E-Mail-Typ aus, ob dieser E-Mail-Typ an alle Teilnehmer gesendet werden soll oder nicht.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL E-Mails zum Abschluss]</b> </p> <p>Senden Sie eine E-Mail, wenn dieser Vertrag abgeschlossen, gekündigt, abgelaufen oder abgelehnt wurde.</p> </li> 
     <li> <p><b>[!UICONTROL In-Flight-E-Mails]</b> </p> <p>Eine E-Mail wurde gesendet, wenn diese Vereinbarung delegiert oder ersetzt wurde.</p> </li> 
     <li> <p><b>[!UICONTROL Vereinbarung-Initiierungs-E-Mails]</b> </p> <p>Senden Sie eine E-Mail, wenn diese Vereinbarung erstellt wird oder eine Aktion dafür angefordert wird.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Externe ID]</td> 
   <td> <p>Geben Sie eine ID für diese Vereinbarung ein oder mappen Sie sie. Sie können dies angeben, wenn die Vereinbarung erstellt wird, und sie verwenden, um die Vereinbarung in späteren Modulen oder Abfragen zu finden.</p> <p>Hinweis: Der Wert der externen ID ist für alle Teilnehmer über die API sichtbar und sollte daher nicht zur Eingabe eines vertraulichen Tokens verwendet werden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Feldinfo zusammenführen]</td> 
   <td> <p>Klicken Sie für jedes Feld in der Vereinbarung, für das Sie einen Standardwert festlegen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie den Standardwert und den Feldnamen ein.</p> <p>Die Werte werden den Unterzeichnern für bearbeitbare Felder angezeigt. Für schreibgeschützte Felder sind die angegebenen Werte während des Signiervorgangs nicht bearbeitbar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Notary info]</td> 
   <td> <p>Füllen Sie die folgenden Felder aus:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Termin]</b> </p> <p>Geben Sie eine vorgeschlagene Uhrzeit und ein Datum für die Ernennung ein, um diese Vereinbarung zu beglaubigen, oder kartieren Sie sie.</p> </li> 
     <li> <p><b>[!UICONTROL HINWEIS]</b> </p> <p>Geben Sie alle Notizen ein, die Sie über die Notarsitzung einbeziehen möchten, oder mappen Sie sie.</p> </li> 
     <li> <p><b>[!UICONTROL Zahlung]</b> </p> <p>Wählen Sie aus, ob der Notar vom Unterzeichner oder vom Absender der Vereinbarung bezahlt wird.</p> </li> 
     <li> <p><b>[!UICONTROL notary type]</b> </p> <p>Notartyp auswählen</p> 
      <ul> 
       <li> <p>[!UICONTROL Provider-Notar]</p> <p>Der Notar wird vom notariellen Leistungserbringer gestellt.</p> </li> 
       <li> <p>[!UICONTROL BYON-Notar]</p> <p>Der Notar wird vom Kunden gestellt.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Post Sign-Option]</td> 
   <td> <p>Wählen Sie aus, ob die Unterzeichner nach Unterzeichnung der Vereinbarung zu einer Erfolgsseite weitergeleitet werden sollen. Wenn Sie <b>[!UICONTROL Yes]</b> auswählen, füllen Sie die folgenden Felder aus:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Umleitungsverzögerung]</b> </p> <p>Geben Sie eine Zahl ein, die die Anzahl der Sekunden darstellt, bevor der Unterzeichner zur Erfolgsseite weitergeleitet wird, oder ordnen Sie sie zu. Wenn dieser Wert größer als 0 ist, wird dem/der Benutzenden zunächst die standardmäßige Erfolgsmeldung [!DNL Adobe Sign] angezeigt und dann nach einer Verzögerung zu Ihrer Erfolgsseite weitergeleitet.</p> </li> 
     <li> <p><b>[!UICONTROL Umleitungs-URL]</b> </p> <p>Geben Sie eine öffentlich zugängliche URL ein, zu der der Benutzer nach erfolgreichem Abschluss des Signiervorgangs gesendet wird, oder ordnen Sie sie zu.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sicherheitsoption]</td> 
   <td> <p>Geben Sie das sekundäre Kennwort zum Schützen des PDF-Dokuments ein, oder ordnen Sie es zu. </p> <p>Wichtig: [!DNL Adobe Sign] geben dieses Kennwort nie weiter, daher müssen Sie es den relevanten Parteien separat mitteilen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vaulting-Info]</td> 
   <td>Wenn Ihr Konto für das Dokument-Vaulting eingerichtet ist und Sie die Option pro Vereinbarung aktivieren können, können Sie diese Option aktivieren, um diese Vereinbarung zu Vault.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Erstellen verwandter Datensätze]**

Dieses Aktionsmodul erstellt Datensätze, die mit einem von Ihnen ausgewählten Modul verknüpft sind.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Datensatztyp des ursprünglichen Datensatzes aus, mit dem Sie die erstellten Datensätze verknüpfen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Vereinbarung]/[!UICONTROL -Bibliotheksdokument]/[!UICONTROL -Benutzer]/[!UICONTROL -Widget-ID]</td> 
   <td>Geben Sie die ID des Objekts ein, mit dem Sie den erstellten Datensatz verknüpfen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vereinbarungsbezogenes Feld]</td> 
   <td> <p>Wählen Sie den Typ des zugehörigen Felds aus, das Sie erstellen möchten</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Formularfelder]</b> </p> <p>Geben Sie die Vorlagen-ID der Vorlage ein, die die zu erstellenden Felder enthält</p> </li> 
     <li> <p><b>[!UICONTROL reminders]</b> </p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Empfänger-ID]</b> </p> <p>Klicken Sie für jeden Teilnehmer, für den Sie eine Erinnerung erhalten möchten, auf [!UICONTROL Element hinzufügen], und geben Sie die ID des Teilnehmers ein.</p> </li> 
       <li> <p><b>[!UICONTROL Status]</b> </p> <p>Für neue Datensätze muss der Status [!UICONTROL Active] lauten.</p> </li> 
       <li> <p><b>[!UICONTROL Verzögerung der ersten Erinnerung]</b> </p> <p>Geben Sie die Verzögerung in Stunden vor dem Senden der ersten Erinnerung ein. Der zulässige Mindestwert ist 1 Stunde, und der Höchstwert darf nicht größer sein als die Differenz zwischen der Erstellung der Vereinbarung und der Ablaufzeit der Vereinbarung in Stunden. Wenn diese Verzögerung nicht festgelegt ist, basiert die erste Erinnerung auf der Häufigkeit.</p> </li> 
       <li> <p><b>[!UICONTROL Erinnerungsfrequenz]</b> </p> <p>Legen Sie fest, wie häufig die Erinnerung gesendet werden soll. Wenn keine Häufigkeit angegeben wird, wird die Erinnerung einmal gesendet.</p> </li> 
       <li> <p><b>[!UICONTROL Datum des letzten Versands]</b> </p> <p>Dieses Feld wird vom System festgelegt.</p> </li> 
       <li> <p><b>[!UICONTROL Nächstes Sendedatum]</b> </p> <p>Dieses Feld muss leer sein oder auf [!UICONTROL ONCE] gesetzt werden.</p> </li> 
       <li> <p><b>[!UICONTROL HINWEIS]</b> </p> <p>Geben Sie eine Notiz ein, die in die Erinnerung aufgenommen werden soll. Dies ist nützlich, um dem Teilnehmer zu sagen, warum seine Teilnahme erforderlich ist.</p> </li> 
       <li> <p><b>[!UICONTROL Starterinnerungszähler von]</b> </p> <p>Wählen Sie aus, ob die Erinnerung basierend auf dem Zeitpunkt gesendet wird, zu dem die Vereinbarung erstellt wurde, sobald sie verfügbar wird.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Unterzeichner-Identitätsbericht]</b> </p> <p>Geben Sie das Kennwort zum Schützen des PDF-Dokuments ein.</p> </li> 
     <li> <p><b>[!UICONTROL Views]</b> </p> <p>Folgende Felder eingeben</p> 
      <ul> 
       <li> <p><b>[!UICONTROL name]</b> </p> <p>Wählen Sie den Namen der Ansicht aus, die Sie erstellen möchten.</p> </li> 
       <li> <p><b>[!UICONTROL Benutzer automatisch anmelden]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um den Benutzer automatisch bei der zurückgegebenen URL anzumelden.</p> </li> 
       <li> <p><b>[!UICONTROL übergeordneter Frame]</b> </p> <p>Geben Sie eine kommagetrennte Liste der URLs der übergeordneten Domain ein, in der die zurückgegebenen URLs eingerahmt werden können, oder ordnen Sie sie zu. Wenn Sie das Feld leer lassen, können die [!DNL Adobe Acrobat Sign]-Seiten nicht in iframe angezeigt werden.</p> </li> 
       <li> <p><b>[!UICONTROL locale]</b> </p> <p>Geben Sie die Sprache ein, in der Sie die Ansicht erstellen möchten. </p> </li> 
       <li> <p><b>[!UICONTROL Keine Chrome-Markierung]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um die eingebettete Seite ohne Navigationskopfzeile oder -fußzeile anzuzeigen.</p> </li> 
       <li> <p><b>[!UICONTROL kann Dateien bearbeiten]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, wenn Sie den Abschnitt „Datei-Upload“ durch Hinzufügen oder Entfernen von Dateien bearbeiten möchten. Dies ist kein Zugriffskontrollmechanismus. Der Standardwert ist [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL -Bibliotheksdokument]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, wenn Links für Bibliotheksdokumente sichtbar sein sollen. Der Standardwert ist [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Lokale Datei]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, wenn die Schaltfläche Lokaler Datei-Upload angezeigt werden soll. Der Standardwert ist [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Web Connectors]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b>, wenn die Links zum Anhängen von Dokumenten aus Web-Quellen angezeigt werden sollen. Der Standardwert lautet Ja.</p> </li> 
       <li> <p><b>[!UICONTROL ist in der Vorschau ausgewählt]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um für die Seite „Erstellen“ den Autorenmodus festzulegen.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Mitgliederfreigabe]</b> </p> <p>Klicken Sie für jedes Mitglied, für das Sie die Vereinbarung freigeben möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie die E-Mail-Adresse des Mitglieds und eine Nachricht an dieses Mitglied ein.</p> </li> 
     <li> <p>[!UICONTROL Teilnehmersatz delegieren]</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Teilnehmersatz-ID]</b> </p> <p>ID des Teilnehmersatzes eingeben</p> </li> 
       <li> <p><b>[!UICONTROL Member Info]</b> </p> <p>Klicken Sie für jedes Mitglied, das Sie hinzufügen möchten, auf [!UICONTROL Element hinzufügen] und geben Sie die E-Mail-Adresse und die Telefoninformationen für das Mitglied ein.</p> </li> 
       <li> <p><b>[!UICONTROL Private Nachricht]</b> </p> <p>Eine Nachricht eingeben. Alle Mitglieder des Teilnehmersatzes erhalten diese Nachricht.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Library View Info]</td> 
   <td> <p>Füllen Sie die folgenden Felder aus:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL name]</b> </p> <p>Geben Sie einen Namen für die Bibliotheksvorlage ein. Dieser Name wird in E-Mails und Websites verwendet.</p> </li> 
     <li> <p><b>[!UICONTROL Benutzer automatisch anmelden]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um den Benutzer automatisch bei der zurückgegebenen URL anzumelden.</p> </li> 
     <li> <p><b>[!UICONTROL übergeordneter Frame]</b> </p> <p>Geben Sie eine kommagetrennte Liste der URLs der übergeordneten Domain ein, in der die zurückgegebenen URLs eingerahmt werden können, oder ordnen Sie sie zu. Wenn Sie das Feld leer lassen, können die [!DNL Adobe Acrobat Sign]-Seiten nicht in iframe angezeigt werden.</p> </li> 
     <li> <p><b>[!UICONTROL locale]</b> </p> <p>Geben Sie die Sprache ein, in der Sie die Ansicht erstellen möchten. </p> </li> 
     <li> <p><b>[!UICONTROL Keine Chrome-Markierung]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um die eingebettete Seite ohne Navigationskopfzeile oder -fußzeile anzuzeigen.</p> </li> 
     <li> <p><b>[!UICONTROL Konfiguration der Sendeansicht]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b>, wenn Sie die Ansicht [!UICONTROL Send] konfigurieren möchten, füllen Sie die folgenden Felder aus.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Name der Vereinbarung]</b> </p> <p>Geben Sie den Namen der Vereinbarung für das Bibliotheksdokument auf der Erstellungsseite ein oder ordnen Sie ihn zu.</p> </li> 
       <li> <p><b>[!UICONTROL kann Dateien bearbeiten]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, wenn Sie den Abschnitt „Datei-Upload“ durch Hinzufügen oder Entfernen von Dateien bearbeiten möchten. Dies ist kein Zugriffskontrollmechanismus. Der Standardwert ist [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Lokale Datei]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, wenn Links für Bibliotheksdokumente sichtbar sein sollen. Der Standardwert ist [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Web Connectors]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b>, wenn die Links zum Anhängen von Dokumenten aus Web-Quellen angezeigt werden sollen. Der Standardwert ist [!UICONTROL Yes].</p> </li> 
       <li> <p><b>Ist Vorschau ausgewählt</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um für die Seite „Erstellen“ den Autorenmodus festzulegen.</p> </li> 
      </ul> <p> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Benutzeransichtsinfo]</td> 
   <td> <p>Füllen Sie die folgenden Felder aus</p> 
    <ul> 
     <li> <p><b>[!UICONTROL name]</b> </p> <p>Name der angeforderten Benutzeransicht auswählen.</p> </li> 
     <li> <p><b>[!UICONTROL Benutzer automatisch anmelden]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um den Benutzer automatisch anzumelden. Wählen Sie <b>[!UICONTROL No]</b> aus, um Anmeldeinformationen anzufordern. Der Standardwert ist [!UICONTROL No].</p> </li> 
     <li> <p><b>[!UICONTROL übergeordneter Frame]</b> </p> <p>Geben Sie eine kommagetrennte Liste der URLs der übergeordneten Domain ein, in der die zurückgegebenen URLs eingerahmt werden können, oder ordnen Sie sie zu. Wenn Sie das Feld leer lassen, können die [!DNL Adobe Acrobat Sign]-Seiten nicht in iframe angezeigt werden.</p> </li> 
     <li> <p><b>Keine Chrome-Markierung</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um die eingebettete Seite ohne Navigationskopfzeile oder -fußzeile anzuzeigen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Widget-bezogene Felder]</td> 
   <td> <p>Wählen Sie den entsprechenden Datensatz aus, den Sie erstellen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL -Ansichten]</p> <p>Füllen Sie die folgenden Felder aus.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL name]</b> </p> <p>Namen der angeforderten Web-Formular-Ansicht auswählen</p> </li> 
       <li> <p><b>[!UICONTROL Benutzer automatisch anmelden]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um den Benutzer automatisch anzumelden. Wählen Sie <b>[!UICONTROL No]</b> aus, um Anmeldeinformationen anzufordern. Der Standardwert ist [!UICONTROL No].</p> </li> 
       <li> <p><b>[!UICONTROL übergeordneter Frame]</b> </p> <p>Geben Sie eine kommagetrennte Liste der URLs der übergeordneten Domain ein, in der die zurückgegebenen URLs eingerahmt werden können, oder ordnen Sie sie zu. Wenn Sie das Feld leer lassen, können die [!DNL Adobe Acrobat Sign]-Seiten nicht in iframe angezeigt werden.</p> </li> 
       <li> <p><b>[!UICONTROL locale]</b> </p> <p>Geben Sie die Sprache ein, in der Sie die Ansicht erstellen möchten. </p> </li> 
       <li> <p><b>[!UICONTROL Keine Chrome-Markierung]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um die eingebettete Seite ohne Navigationskopfzeile oder -fußzeile anzuzeigen.</p> </li> 
       <li> <p>[!UICONTROL Konfiguration der Ansicht für personalisierte Signatur]</p> <p>Wenn Sie eine personalisierte Signaturansicht konfigurieren möchten, wählen Sie <b>[!UICONTROL Yes]</b> aus und füllen Sie die folgenden Felder aus:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL email]</b> </p> <p>E-Mail-Adresse der Person eingeben, die das neu erstellte Web-Formular erhält</p> </li> 
         <li> <p><b>[!UICONTROL comment]</b> </p> <p>Geben Sie einen Kommentar ein, der beschreibt, wie der API-Aufrufer die Identität des Unterzeichners ermittelt hat. Diese Informationen werden im Audit-Protokoll der [!DNL Adobe Acrobat Sign] angezeigt.</p> </li> 
         <li> <p><b>[!UICONTROL Expiration]</b> </p> <p>Geben Sie ein Ablaufdatum für die Personalisierung dieses Web-Formulars ein. </p> <p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL wiederverwendbar]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b>, wenn der vorgesehene Unterzeichner das Formular mehrmals signieren kann.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Mitgliederfreigabe]</b> </p> <p>Klicken Sie für jedes Mitglied, für das Sie die Vereinbarung freigeben möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie die E-Mail-Adresse des Mitglieds und eine Nachricht an dieses Mitglied ein.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Benutzerdefinierter API-Aufruf]**
Mit diesem Modul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Pfad eingeben für <code>https://api.[region].adobesign.com/api/rest/v6/</code></p> <p>Hinweis: Eine Liste der verfügbaren Endpunkte finden Sie in der [!DNL Adobe Sign] API-Referenz.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Methode]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge] </td> 
   <td> <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorübergehendes Dokument hochladen]</td> 
   <td> <p>Wenn Sie ein vorübergehendes Dokument hochladen möchten, geben Sie die Quelldatei für das Dokument ein, das Sie hochladen möchten.</p> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Einträge auflisten]**

Dieses Aktionsmodul listet alle Datensätze des ausgewählten Typs auf, auf den das Konto Zugriff hat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Datensatztyp aus, für den Sie verknüpfte Datensätze abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td> <p>Geben Sie das Gebietsschema des Benutzers ein. Dadurch wird die Sprache der Benutzeroberfläche bestimmt. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Externe ID]</td> 
   <td>Geben Sie die externe ID (eine ID, die außerhalb von [!DNL Adobe Acrobat Sign] zugewiesen wird) für die Vereinbarungen, die Sie zurückgeben möchten, ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Gruppen-ID]</td> 
   <td>Geben Sie die ID der Gruppe ein, die mit den Datensätzen verknüpft ist, die Sie auflisten möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgeblendet anzeigen (Einträge)]</td> 
   <td>Aktivieren Sie diese Option, wenn Sie ausgeblendete Datensätze in die Ergebnisse aufnehmen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cursor] / [!UICONTROL Start index]</td> 
   <td> <p>Geben Sie die Nummer des ersten Datensatzes ein, den das Modul zurückgeben soll. </p> <p>Hinweis: Dieses Feld wird mit dem Feld [!UICONTROL Maximale Anzahl zurückgegebener Datensätze] für die Paginierung kombiniert. Wenn beispielsweise die [!UICONTROL Maximale Anzahl der zurückgegebenen Ereignisse] 100 und der [!UICONTROL Start index] 101 ist, gibt das Modul die Datensätze 101-200 oder die zweite Ergebnisseite zurück.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Datensätze]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> <p>Hinweis: Dieses Feld wird mit dem Feld [!UICONTROL Cursor] oder [!UICONTROL Start Index] für die Paginierung kombiniert. Wenn beispielsweise die [!UICONTROL Maximale Anzahl der zurückgegebenen Ereignisse] 100 und der [!UICONTROL Start index] 101 ist, gibt das Modul die Datensätze 101-200 oder die zweite Ergebnisseite zurück.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URLs der übergeordneten Domain]</td> 
   <td> <p>Geben Sie eine kommagetrennte Liste der URLs der übergeordneten Domain ein, in der die zurückgegebenen URLs eingerahmt werden können, oder ordnen Sie sie zu. Wenn Sie das Feld leer lassen, können die [!DNL Adobe Acrobat Sign]-Seiten nicht in iframe angezeigt werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Datensatz lesen]**

Dieses Aktionsmodul ruft Informationen aus einem einzelnen Datensatz ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Datensatztyp aus, für den Sie verknüpfte Datensätze abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatz-ID]</td> 
   <td>Geben Sie die ID des Datensatzes ein, den Sie abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Lesen verwandter Datensätze]**

Weitere Informationen zu einem einzelnen Datensatz lesen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Datensatztyp aus, für den Sie verknüpfte Datensätze abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatz-ID] (Beispiel: [!UICONTROL Konto-ID])</td> 
   <td>Geben Sie die ID des Datensatzes ein, für den Sie verwandte Datensätze abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Andere Felder]</td> 
   <td>Geben Sie Informationen in bestimmte Felder basierend auf dem Datensatztyp und verwandten Feldern ein.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Aktualisieren eines Datensatzes]**

Dieses Aktionsmodul aktualisiert einen einzelnen Datensatz in [!DNL Adobe Acrobat Sign].

>[!IMPORTANT]
>
>* Wenn Sie wesentliche Änderungen an einem Abkommen erwarten, empfehlen wir als Best Practice die Erstellung eines neuen Abkommens, anstatt das bestehende zu aktualisieren.
>* Einige Updates verfügen über erforderliche Felder. Achten Sie beim Konfigurieren des Updates darauf, alle erforderlichen Felder auszufüllen. Erforderliche Felder sind in [!DNL Workfront Fusion] Modulen fett formatiert.
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatz-ID] </td> 
   <td>Geben Sie die ID des Datensatzes ein, den Sie aktualisieren möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Typ des Datensatzes aus, den Sie aktualisieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Andere Felder]</td> 
   <td> <p>Geben Sie Informationen in bestimmte Felder basierend auf dem Datensatztyp und verwandten Feldern ein.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL -Vereinbarung]</b> </p> <p>Wenn Sie wesentliche Änderungen an einem Abkommen erwarten, empfehlen wir als Best Practice die Erstellung eines neuen Abkommens, anstatt das bestehende zu aktualisieren.</p> </li> 
     <li> <p><b>[!UICONTROL -Bibliotheksdokument]</b> </p> <p>Wählen Sie die Felder aus, die Sie aktualisieren möchten, und füllen Sie dann die ausgewählten Felder aus:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Status]</b> </p> <p>Wählen Sie den neuen Status für das Bibliotheksdokument aus.</p> </li> 
       <li> <p><b>[!UICONTROL name]</b> </p> <p>Namen der Bibliotheksvorlage eingeben oder zuordnen</p> </li> 
       <li> <p><b>[!UICONTROL Freigabemodus]</b> </p> <p>Geben Sie an, wer Zugriff auf das Bibliotheksdokument haben soll.</p> </li> 
       <li> <p><b>[!UICONTROL Bibliotheksvorlagentyp]</b> </p> <p>Klicken Sie für jeden gewünschten Bibliotheksvorlagentyp auf <b>[!UICONTROL Element hinzufügen]</b> und wählen Sie den Vorlagentyp aus.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL user]</b> </p> <p>Wählen Sie die Felder aus, die Sie aktualisieren möchten, und füllen Sie dann die ausgewählten Felder aus:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Vorname]</b> </p> <p>Geben Sie den Vornamen des Benutzers ein.</p> </li> 
       <li> <p><b>[!UICONTROL Nachname]</b> </p> <p>Geben Sie den Nachnamen des Benutzers ein</p> </li> 
       <li> <p><b>[!UICONTROL Firma]</b> </p> <p>Geben Sie den Namen der Firma des Benutzers ein.</p> </li> 
       <li> <p><b>[!UICONTROL Phone]</b> </p> <p>Telefonnummer des Benutzers eingeben</p> </li> 
       <li> <p><b>[!UICONTROL Primäre Gruppen-ID]</b> </p> <p>Geben Sie die Gruppe ein, der der neue Benutzer hinzugefügt wird. Wenn nichts eingegeben wird, wird der Benutzer der Standardgruppe für das Konto hinzugefügt.</p> </li> 
       <li> <p><b>[!UICONTROL Auftragstitel]</b> </p> <p>Geben Sie die Stellenbezeichnung des Benutzers ein.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web-Formular] ([!UICONTROL -Widget])</b> </p> <p>Geben Sie Informationen in bestimmte Felder basierend auf dem Datensatztyp und verwandten Feldern ein.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Aktualisieren des zugehörigen Datensatzes]**

Dieses Aktionsmodul aktualisiert Datensätze, die sich auf ein bestimmtes Objekt beziehen.

>[!IMPORTANT]
>
>* Wenn Sie wesentliche Änderungen an einem Abkommen erwarten, empfehlen wir als Best Practice die Erstellung eines neuen Abkommens, anstatt das bestehende zu aktualisieren.
>* Einige Updates verfügen über erforderliche Felder. Achten Sie beim Konfigurieren des Updates darauf, alle erforderlichen Felder auszufüllen. Erforderliche Felder sind in [!DNL Workfront Fusion] Modulen fett formatiert.
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie den Datensatztyp des Datensatzes aus, mit dem die zugehörigen Felder verknüpft sind.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Vereinbarung]/[!UICONTROL -Bibliotheksdokument]/[!UICONTROL -Benutzer]/[!UICONTROL -Widget-ID]</td> 
   <td>Geben Sie die ID des Objekts ein, mit dem Sie den erstellten Datensatz verknüpfen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Andere Felder]</td> 
   <td> <p>Geben Sie Informationen in bestimmte Felder basierend auf dem Datensatztyp und verwandten Feldern ein.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL -Vereinbarung]</b> </p> <p>Wenn Sie wesentliche Änderungen an einem Abkommen erwarten, empfehlen wir als Best Practice die Erstellung eines neuen Abkommens, anstatt das bestehende zu aktualisieren.</p> </li> 
     <li> <p><b>[!UICONTROL -Bibliotheksdokument]</b> </p> <p>Wählen Sie die Felder aus, die Sie aktualisieren möchten, und füllen Sie dann die ausgewählten Felder aus:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL state]</b> </p> <p>Wählen Sie den neuen Status für das Bibliotheksdokument aus.</p> </li> 
       <li> <p><b>[!UICONTROL HINWEIS]</b> </p> <p>Geben Sie den Text der Anmerkung ein oder mappen Sie ihn.</p> </li> 
       <li> <p><b>[!UICONTROL Visibility]</b> </p> <p>Wählen Sie aus, ob das Bibliotheksdokument angezeigt oder ausgeblendet werden soll.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL user]</b> </p> <p>Wählen Sie die Felder aus, die Sie aktualisieren möchten, und füllen Sie dann die ausgewählten Felder aus:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Group info list]</b> </p> <p>Füllen Sie die folgenden Felder aus</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Status]</b> </p> <p>Wählen Sie den neuen Status für den Benutzer aus.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Eindeutige ID der Gruppe eingeben</p> </li> 
         <li> <p><b>[!UICONTROL ist Gruppenadmin]</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um diesen Benutzer als Gruppenadministrator festzulegen.</p> </li> 
         <li> <p><b>Ist primäre Gruppe</b> </p> <p>Wählen Sie <b>[!UICONTROL Yes]</b> aus, um diese Gruppe auf die primäre Gruppe des Benutzers zu aktualisieren.</p> </li> 
         <li> <p><b>[!UICONTROL Erstellungsdatum]</b> </p> <p>Geben Sie das Datum ein, an dem die Gruppe erstellt wurde.</p> <p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Typzwang in [!UICONTROL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL name]</b> </p> <p>Geben Sie den Namen der Gruppe ein oder mappen Sie ihn.</p> </li> 
         <li> <p><b>[!UICONTROL Library Document Creation visible]</b> </p> <p>Diese Einstellungen bestimmen, ob der Benutzer Bibliotheksdokumente erstellen kann</p> 
          <ul> 
           <li> <p>[!UICONTROL -Wert]</p> <p>zulassen</p> </li> 
           <li> <p>[!UICONTROL vererbt]</p> <p>Gruppeneinstellungen von Gruppe oder Konto übernehmen</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL Senden eingeschränkt an Workflows]</b> </p> <p>Diese Einstellungen bestimmen, ob der Benutzer Vereinbarungen nur mithilfe von Workflows erstellen kann.</p> 
          <ul> 
           <li> <p>[!UICONTROL -Wert]</p> <p>zulassen</p> </li> 
           <li> <p>[!UICONTROL vererbt]</p> <p>Gruppeneinstellungen von Gruppe oder Konto übernehmen</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL Benutzer can send]</b> </p> 
          <ul> 
           <li> <p>[!UICONTROL -Wert]</p> <p>zulassen</p> </li> 
           <li> <p>[!UICONTROL vererbt]</p> <p>Gruppeneinstellungen von Gruppe oder Konto übernehmen</p> </li> 
          </ul> </li> 
        </ul> </li> 
      </ul> 
      <ul> 
       <li> <p><b>[!UICONTROL state]</b> </p> <p>Wählen Sie den neuen Status für den Benutzer aus und geben Sie einen Kommentar dazu ein, warum Sie den Benutzer aktivieren oder deaktivieren möchten.</p> </li> 
       <li> <p><b>[!UICONTROL locale]</b> </p> <p>Geben Sie das Gebietsschema des Benutzers ein. Dadurch wird die Sprache der Benutzeroberfläche bestimmt. </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web-Formular] ([!UICONTROL -Widget])</b> </p> <p>Geben Sie Informationen in bestimmte Felder basierend auf dem Datensatztyp und verwandten Feldern ein.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Dokument hochladen]**

Laden Sie ein vorübergehendes Dokument hoch. Ein vorübergehendes Dokument steht 7 Tage nach dem Hochladen zur Verfügung.

>[!NOTE]
>
>Es wird empfohlen, das Dokument zum Signieren als vorübergehendes Dokument hochzuladen und es dann dem Feld Zu sendende Datei im Modul Vereinbarung erstellen zuzuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatz-ID]</td> 
   <td>Die ID des Datensatzes eingeben oder zuordnen, den Sie aktualisieren möchten</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME-Typ]</td> 
   <td>Geben Sie den MIME-Typ der Originaldatei an. MIME-Typen (Multipurpose Internet Mail Extension) sind Bezeichnungen, mit denen Software verschiedene Arten von im Internet freigegebenen Daten identifizieren kann. Webserver und Browser verwenden den MIME-Typ, um zu bestimmen, was mit einer Datei getan werden soll. Beispielsweise wird eine Datei mit dem MIME-Typ <code>text/html</code> in einem Browser anders verarbeitet als eine Datei mit dem MIME-Typ <code>image/jpeg</code>.</td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** In diesem Workflow wird das zu signierende Dokument (zuvor von Workfront heruntergeladen) als vorübergehendes Dokument hochgeladen.

(/help/workfront-fusion/references/apps-and-modules/assets/sign-example-1-350x308.png)

Das [!UICONTROL Dokument hochladen]-Modul gibt dem Dokument eine [!DNL Adobe Acrobat Sign] ID, die in späteren Modulen referenziert werden kann. Wenn die Vereinbarung erstellt wird, wird die ID des hochgeladenen Dokuments in das Feld [!UICONTROL Zu sendende Dateien] aufgenommen.

![Sign-Beispiel](/help/workfront-fusion/references/apps-and-modules/assets/sign-example-2-350x356.png)

+++

### Suchvorgänge

+++ **[!UICONTROL Suchvereinbarungen]**

Dieses Suchmodul sucht anhand der von Ihnen angegebenen Kriterien nach Vereinbarungen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Acrobat Sign]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Textfilter]</td> 
   <td> <p>Nach Text in den Metadaten der Vereinbarung suchen. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Text suchen]</b> </p> <p>Geben Sie den Text ein, den Sie in den Vereinbarungsmetadaten finden möchten. Jedes Wort wird als separates Textelement behandelt. </p> </li> 
     <li> <p><b>[!UICONTROL Text suchen in]</b> </p> <p>Wählen Sie die Metadatenfelder aus, in denen Sie Text suchen möchten. Wenn Sie nichts auswählen, durchsuchen die Module alle Metadaten.</p> </li> 
    </ul> <p>Das Modul gibt alle Vereinbarungen zurück, die einen der eingegebenen Texte in einem der ausgewählten Felder enthalten. Beispiel: Wenn Sie „Frühlingskampagne“ eingeben und die Optionen Titel und Notiz auswählen, werden Vereinbarungen mit den Wörtern „Frühling“ oder „Kampagne“ in Titel oder Notiz zurückgegeben.</p> <p>Weitere Informationen zum Suchen von Feldern in [!DNL Adobe Acrobat Sign] finden Sie unter „Funktionsweise der Textsuche“ in <a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">[!DNL Adobe Sign] Suche - Funktionsweise</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Erstellungsdatum]</td> 
   <td>Datum auswählen. Das Modul gibt nur Datensätze zurück, deren Erstellungsdatum mit diesen Kriterien übereinstimmt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ablaufdatum]</td> 
   <td>Datum auswählen. Das Modul gibt nur Datensätze zurück, deren Ablaufdatum mit diesen Kriterien übereinstimmt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL Änderungsdatum]</p> </td> 
   <td>Datum auswählen. Das -Modul gibt nur Datensätze zurück, bei denen das geänderte Datum diesen Kriterien entspricht.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Externe ID]</td> 
   <td> <p> Die externe ID ist eine vom Absender zugewiesene ID der Vereinbarung, die in jeder Form vorliegen kann, üblicherweise jedoch in Form von "&lt;groupID&gt;:&lt;ID&gt;".</p> <p>Klicken Sie für jede externe ID, die Sie hinzufügen möchten, auf <b>[!UICONTROL Hinzufügen]</b> und geben Sie die externe ID ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Gruppen-ID]</td> 
   <td> <p>Die Gruppen-ID ist eine Kennung, die bei der Erstellung der Gruppe zugewiesen wurde.</p> <p>Klicken Sie für jede externe ID, die Sie hinzufügen möchten, auf <b>[!UICONTROL Hinzufügen]</b> und geben Sie die externe ID ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID]</td> 
   <td> <p>Dies ist die ID, die der spezifischen Vereinbarung zugewiesen wurde. </p> <p>Klicken Sie für jede externe ID, die Sie hinzufügen möchten, auf <b>[!UICONTROL Hinzufügen]</b> und geben Sie die externe ID ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Übergeordnete ID]</td> 
   <td> <p>Dies ist die ID, die dem übergeordneten Objekt der Vereinbarung zugewiesen ist. </p> <p>Klicken Sie für jede externe ID, die Sie hinzufügen möchten, auf <b>[!UICONTROL Hinzufügen]</b> und geben Sie die externe ID ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilnehmer-E-Mail]</td> 
   <td> <p>Die E-Mail-Adresse eines Teilnehmers. </p> <p>Klicken Sie für jede externe ID, die Sie hinzufügen möchten, auf <b>[!UICONTROL Hinzufügen]</b> und geben Sie die externe ID ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Role]</td> 
   <td>Wählen Sie Rollen aus, die die zurückgegebenen Ergebnisse enthalten sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortieren nach]</td> 
   <td>Wenn Sie möchten, dass das Modul die Ergebnisse sortiert, wählen Sie das Feld aus, nach dem Sie die Ergebnisse sortieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortierreihenfolge]r</td> 
   <td>Wenn Sie möchten, dass das Modul die Ergebnisse sortiert, wählen Sie aus, ob Sie auf- oder absteigend sortieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
   <td>Wählen Sie die Status aus, die die zurückgegebenen Ergebnisse enthalten sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Typ]</td> 
   <td>Wählen Sie die Vereinbarungstypen aus, die die zurückgegebenen Ergebnisse enthalten sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Untertypen]</td> 
   <td>Wählen Sie die Vereinbarungs-Untertypen aus, die die zurückgegebenen Ergebnisse enthalten sollen. Nur Bibliotheksvorlagenvereinbarungen weisen Untertypen auf.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Benutzer-ID]</td> 
   <td> <p>Die Benutzer-ID des Benutzers, für den die Vereinbarung freigegeben wurde.</p> <p>Klicken Sie für jede Benutzer-ID, die Sie hinzufügen möchten, auf <b>[!UICONTROL Hinzufügen]</b> und geben Sie die Benutzer-ID ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sichtbarkeit]</td> 
   <td>Wählen Sie die Sichtbarkeitsstufe aus, die die zurückgegebenen Ergebnisse enthalten sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Startindex]</td> 
   <td> <p>Geben Sie die Position des ersten Ergebnisses ein, das Sie zurückgeben möchten. Kombinieren Sie dies mit dem [!UICONTROL Maximum returned results], um die Ergebnisse zu paginieren</p> <p>Beispiel: Wenn Sie 100 Ergebnisse gleichzeitig zurückgeben, geben Sie 100 ein, um Ergebnisse 100-200 zurückzugeben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++
