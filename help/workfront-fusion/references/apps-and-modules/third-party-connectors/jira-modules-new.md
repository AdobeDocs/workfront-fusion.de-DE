---
title: Jira-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Jira-Software verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: b74a3618-c4a1-4965-a88d-1643bfab12db
source-git-commit: e65d868dc2165cbe800600f271f6b03d0a906cb4
workflow-type: tm+mt
source-wordcount: '2348'
ht-degree: 25%

---

# Jira-Module

>[!NOTE]
>
>Diese Anweisungen gelten für die neue Version des Jira-Connectors, der einfach Jira genannt wird. Anweisungen zu den alten Jira Cloud- und Jira Server-Connectoren finden Sie unter [Jira-Softwaremodule](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md).

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Jira verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Der Jira-Connector kann sowohl für Jira Cloud als auch für Jira Data Server verwendet werden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Erstellen von Szenarios: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Voraussetzungen

* Um Jira-Module verwenden zu können, müssen Sie über ein Jira-Konto verfügen.
* Sie müssen Zugriff auf die Jira-Developer Console haben, um eine OAuth2-Anwendung in Jira zu erstellen.

## Verbinden von Jira mit Workfront Fusion

Das Verfahren zum Erstellen einer Verbindung zu Jira unterscheidet sich je nachdem, ob Sie eine Basisverbindung oder eine OAuth2-Verbindung erstellen.

* [Erstellen einer OAuth2-Verbindung mit Jira](#create-an-oauth2-connection-to-jira)
* [Erstellen einer Basisverbindung zu Jira](#create-a-basic-connection-to-jira)

### Erstellen einer OAuth2-Verbindung mit Jira

Um eine OAuth2-Verbindung zu Jira herzustellen, müssen Sie eine Anwendung in Jira erstellen, bevor Sie die Verbindung in Fusion konfigurieren können.

* [Erstellen einer OAuth2-Anwendung in Jira](#create-an-oauth2-application-in-jira)
* [Konfigurieren der OAuth2-Verbindung in Fusion](#configure-the-oauth2-connection-in-fusion)

#### Erstellen einer OAuth2-Anwendung in Jira

>[!IMPORTANT]
>
>Sie müssen Zugriff auf die Jira-Developer Console haben, um ein OAuth2-Programm für Ihre Jira-Verbindung zu erstellen und zu konfigurieren.

1. Gehen Sie zur [Jira Developer Console](https://developer.atlassian.com/console.myapps/).
1. Klicken Sie im Bereich Meine Apps auf **Erstellen** und wählen Sie dann **OAuth 2.0-Integration**.
1. Geben Sie einen Namen für die Integration ein, stimmen Sie den Bedingungen für den Entwickler zu und klicken Sie auf **Erstellen**.

   Die Anwendung wird erstellt und Sie gelangen in den Bereich für die Anwendungskonfiguration.
1. Klicken Sie **linken** auf „Berechtigungen“.
1. Suchen Sie im Bereich Berechtigungen die Zeile **Jira API** .
1. Klicken Sie **der Jira** API-Zeile auf „Hinzufügen“ und klicken Sie dann **derselben Zeile auf** Weiter“.
1. Aktivieren Sie die folgenden Bereiche:

   * Jira-Problemdaten anzeigen (`read:jira-work`)
   * Benutzerprofile anzeigen (`read:jira-user`)
   * Probleme erstellen und verwalten (`write:jira-work`)

1. Klicken Sie in der linken Navigation auf **Autorisierung**.
1. Klicken Sie **Hinzufügen** in der Zeile für die OAuth 2.0-Autorisierung.
1. Geben Sie im Feld **Callback** URL eine der folgenden URLs ein, die auf Ihrem Workfront Fusion-Rechenzentrum basieren:

   | Fusion-Rechenzentrum | Callback-URL |
   |---|---|
   | USA | `https://app.workfrontfusion.com/oauth/cb/workfront-jira2` |
   | EU | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira2` |
   | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira2` |

1. Klicken Sie in der linken Navigation auf **Einstellungen**.
1. (Optional) Geben Sie eine Beschreibung in das Feld Beschreibung ein und klicken Sie **diesem Feld auf**&#x200B;Änderungen speichern“.
1. Kopieren Sie die Client-ID und den geheimen Client-Schlüssel aus dem Bereich Einstellungen an einen sicheren Speicherort oder lassen Sie diese Seite offen, während Sie die Verbindung in Fusion konfigurieren.
1. Fahren Sie fort [Konfigurieren der OAutt2-Verbindung in Fusion](#configure-the-oauth2-connection-in-fusion)

#### Konfigurieren der OAuth2-Verbindung in Fusion

1. Klicken Sie in einem beliebigen Jira-Modul **Hinzufügen** neben dem Feld Verbindung .
1. Konfigurieren Sie die folgenden Felder:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Verbindungstyp</p> </td> 
      <td> <p>Wählen Sie <b>OAuth 2</b> aus.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Verbindungsname</p> </td> 
      <td> <p>Geben Sie einen Namen für die neue Verbindung ein. </p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">Service-URL</td>
      <td>Geben Sie Ihre Jira-Instanz-URL ein. Dies ist die URL, über die Sie auf Jira zugreifen.</td>
     </tr>
     <tr>
      <td role="rowheader">Jira-Kontotyp</td>
       <td>Wählen Sie aus, ob Sie eine Verbindung zu Jira Cloud oder Jira Data Center herstellen möchten.</td>
     </tr>
     <tr> 
      <td role="rowheader">Client-ID</td> 
      <td> <p>Geben Sie die Client-ID der Jira-Anwendung ein, die Sie in "<a href="#create-an-oauth2-application-in-jira" class="MCXref xref" data-mc-variable-override=""> einer OAuth2-Anwendung in Jira“ erstellt </a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Client-Geheimnis</td> 
      <td> <p>Geben Sie den geheimen Client-Schlüssel der Jira-Anwendung ein, die Sie in <a href="#create-an-oauth2-application-in-jira" class="MCXref xref" data-mc-variable-override="">Erstellen einer OAuth2-Anwendung in Jira</a> erstellt haben.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Zusätzliche Bereiche</td> 
      <td>Geben Sie alle zusätzlichen Bereiche ein, die Sie zu dieser Verbindung hinzufügen möchten.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API-Version</td> 
      <td>Wählen Sie die Jira-API-Version aus, mit der sich diese Verbindung verbinden soll.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie auf **[!UICONTROL Fortsetzen]**, um die Verbindung zu erstellen und zum Modul zurückzukehren.

### Erstellen einer Basisverbindung zu Jira

Das Erstellen einer Basisverbindung zu Jira unterscheidet sich, je nachdem, ob Sie eine Verbindung zu Jira Cloud oder Jira Data Center erstellen.

* [Erstellen einer Basisverbindung zu Jira Cloud](#create-a-basic-connection-to-jira-cloud)
* [Erstellen einer Basisverbindung zum Jira-Rechenzentrum](#create-a-basic-connection-to-jira-data-center)

#### Erstellen einer Basisverbindung zu Jira Cloud

>[!IMPORTANT]
>
> Um eine einfache Verbindung zu Jira Cloud herzustellen, benötigen Sie ein Jira-API-Token.
>Anweisungen zum Erwerb eines Jira-API-Tokens finden Sie unter [Verwalten von API-Token für Ihr Atlassian](https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account) in der Atlassian-Dokumentation.


1. Klicken Sie in einem beliebigen Jira-Modul **Hinzufügen** neben dem Feld Verbindung .
1. Konfigurieren Sie die folgenden Felder:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Verbindungstyp</p> </td> 
      <td> <p>Wählen Sie aus, ob Sie eine Basisverbindung oder eine OAuth 2-Verbindung erstellen.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Verbindungsname</p> </td> 
      <td> <p>Geben Sie einen Namen für die neue Verbindung ein. </p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">Service-URL</td>
      <td>Geben Sie Ihre Jira-Instanz-URL ein. Dies ist die URL, über die Sie auf Jira zugreifen.</td>
     </tr>
     <tr>
      <td role="rowheader">Jira-Kontotyp</td>
       <td>Wählen Sie aus, ob Sie eine Verbindung zu Jira Cloud oder Jira Data Center herstellen möchten.</td>
     </tr>
     <tr> 
      <td role="rowheader">E-Mail</td> 
      <td>Geben Sie Ihre E-Mail-Adresse ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API-Token</td> 
      <td>Geben Sie Ihr API-Token ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API-Version</td> 
      <td>Wählen Sie die Jira-API-Version aus, mit der sich diese Verbindung verbinden soll.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie auf **[!UICONTROL Fortsetzen]**, um die Verbindung zu erstellen und zum Modul zurückzukehren.

#### Erstellen einer Basisverbindung zum Jira-Rechenzentrum

>[!IMPORTANT]
>
> Um eine einfache Verbindung zum Jira-Rechenzentrum herzustellen, benötigen Sie ein Jira Personal Access Token (PAT).
>Anweisungen zum Erwerb eines Jira Personal Access Token finden Sie unter [Verwalten von API Token für Ihr Atlassian-Konto](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html) in der Atlassian-Dokumentation.
>Überlegungen zum Erstellen des PATS finden Sie unter [Konfigurieren des PATS](#configure-your-pat) in diesem Artikel.

1. Klicken Sie in einem beliebigen Jira-Modul **Hinzufügen** neben dem Feld Verbindung .
1. Konfigurieren Sie die folgenden Felder:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Verbindungstyp</p> </td> 
      <td> <p>Wählen Sie aus, ob Sie eine Basisverbindung oder eine OAuth 2-Verbindung erstellen.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Verbindungsname</p> </td> 
      <td> <p>Geben Sie einen Namen für die neue Verbindung ein. </p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">Service-URL</td>
      <td>Geben Sie Ihre Jira-Instanz-URL ein. Dies ist die URL, über die Sie auf Jira zugreifen.</td>
     </tr>
     <tr>
      <td role="rowheader">Jira-Kontotyp</td>
       <td>Wählen Sie aus, ob Sie eine Verbindung zu Jira Cloud oder Jira Data Center herstellen möchten.</td>
     </tr>
     <tr> 
      <td role="rowheader">PAT (Personal access token)</td> 
      <td>Geben Sie Ihr persönliches Jira-Zugriffstoken ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API-Version</td> 
      <td>Wählen Sie die Jira-API-Version aus, mit der sich diese Verbindung verbinden soll.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie auf **[!UICONTROL Fortsetzen]**, um die Verbindung zu erstellen und zum Modul zurückzukehren.

##### Konfigurieren des PATH

Um eine einfache Verbindung zum Jira-Rechenzentrum herzustellen, benötigen Sie ein Jira Personal Access Token (PAT).

Anweisungen zum Erwerb eines Jira Personal Access Token finden Sie unter [Verwalten von API Token für Ihr Atlassian-Konto](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html) in der Atlassian-Dokumentation.

Möglicherweise benötigen Sie bei der Konfiguration Ihres PAT die folgenden Informationen

* Redirect URLs

  | Fusion-Rechenzentrum | Umleitungs-URL |
  |---|---|
  | USA | `https://app.workfrontfusion.com/oauth/cb/workfront-jira` |
  | EU | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira` |
  | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira` |

* Dateikonfigurationen

Um einen Pfad zu verwenden, müssen Sie Folgendes in der `jira/bin/WEB-INF/classes` Dateien im `jira-config.properties` aktivieren:

* `jira.rest.auth.allow.basic = true`
* `jira.rest.csrf.disabled = true`

Wenn diese Datei nicht vorhanden ist, müssen Sie sie erstellen.

## Jira-Module und ihre Felder

Beim Konfigurieren von Jira-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere Jira-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

#### Auf Einträge achten

Dieses Trigger-Modul startet ein Szenario, wenn ein Datensatz hinzugefügt, aktualisiert oder gelöscht wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Webhook</td> 
   <td> <p>Wählen Sie den Webhook aus, den Sie verwenden möchten, um nach Datensätzen zu suchen, oder erstellen Sie einen neuen Webhook. </p> <p>So erstellen Sie einen neuen Webhook:</p> 
    <ol> 
     <li>Klicken Sie auf <strong>Hinzufügen</strong></li> 
     <li>Geben Sie einen Namen für den Webhook ein.</li> 
     <li> Wählen Sie die Verbindung aus, die Sie für Ihren Webhook verwenden möchten. <p>Anweisungen zum Verbinden Ihres Jira-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Jira mit Workfront Fusion</a> in diesem Artikel.</p> </li> 
     <li> <p>Wählen Sie den Datensatztyp aus, auf den die Software achten soll:</p> 
      <ul> 
       <li>Problem</li> 
       <li>Kommentar </li> 
       <li>Arbeitsprotokoll </li> 
       <li>Projekt </li> 
       <li>Sprint</li> 
       <li>Anhang </li> 
      </ul> </li> 
     <li>Wählen Sie einen oder mehrere Ereignistypen aus, die dieses Szenario zum Trigger bringen sollen.</li> 
     <li>Geben Sie einen Jira Query Language-Filter für dieses Modul ein.<p>Weitere Informationen zu JQL finden Sie unter <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a> auf der Atlassian-Hilfeseite. </p></li>
     <li>Klicken Sie <b>Speichern</b>, um den Webhook zu speichern. 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [Problem zum Sprint hinzufügen](#add-issue-to-sprint)
* [Erstellen eines Datensatzes](#create-a-record)
* [Benutzerdefinierter API-Aufruf](#custom-api-call)
* [Löschen eines Datensatzes](#delete-a-record)
* [Herunterladen eines Anhangs](#download-an-attachment)
* [Datensatz lesen](#read-a-record)
* [Eintrag aktualisieren](#update-a-record)

#### Problem zum Sprint hinzufügen

Dieses Aktionsmodul fügt einem Sprint ein oder mehrere Probleme hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Jira-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Jira mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sprint-ID</td> 
   <td>Geben Sie die Sprint-ID des Sprints ein, dem Sie ein Problem hinzufügen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Anfrage-ID oder Schlüssel</td> 
   <td>Klicken Sie für jedes Problem oder jeden Schlüssel, das bzw. den Sie dem Sprint hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Problem-ID oder den Schlüssel ein. Sie können bis zu 50 in einem Modul eingeben.</td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen eines Datensatzes

Dieses Aktionsmodul erstellt einen neuen Datensatz in Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Jira-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Jira mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Art des Eintrags</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den das Modul erstellen soll.</p> 
    <ul> 
     <li>Anhang</li> 
     <li>Kommentar</li> 
     <li>Problem</li> 
     <li>Projekt</li> 
     <li>Sprint </li> 
     <li>Arbeitsprotokoll</li> 
     <li>Benutzerin oder Benutzer</li> 
     <li>Pinnwand</li> 
     <li>Kategorie</li> 
     <li>Filter</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Andere Felder</td> 
   <td> Füllen Sie die anderen Felder aus. Die Felder sind je nach ausgewähltem Datensatztyp verfügbar. </td> 
  </tr> 
 </tbody> 
</table>

#### Benutzerdefinierter API-Aufruf

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die Jira-API durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Jira-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Jira mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Pfad eingeben für<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Methode</td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Header</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Abfragezeichenfolge</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Textkörper</td> 
   <td> <p>Fügen Sie den Textinhalt für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrem JSON-Objekt verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### Löschen eines Datensatzes

Dieses Aktionsmodul löscht den angegebenen Datensatz.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Jira-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Jira mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den das Modul löschen soll. </p> 
    <ul> 
     <li>Kommentar</li> 
     <li>Problem</li> 
     <li>Projekt</li> 
     <li>Sprint </li> 
     <li>Arbeitsprotokoll</li> 
     <li>Anhang</li> 
     <li>Pinnwand</li> 
     <li>Kategorie</li> 
     <li>Filter</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Datensatztyp)ID</td> 
   <td>Geben Sie die ID oder den Schlüssel des Datensatzes ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Herunterladen eines Anhangs

Dieses Aktionsmodul lädt den angegebenen Anhang herunter.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Jira-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Jira mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td>Geben Sie die ID des Anhangs ein, den Sie herunterladen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### Datensatz lesen

Dieses Aktionsmodul liest Daten aus dem angegebenen Datensatz in Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Jira-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Jira mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Art des Eintrags</td> 
   <td> <p>Wählen Sie den Typ des Jira-Eintrags aus, den das Modul lesen soll.</p> 
    <ul> 
     <li>Anhang</li> 
     <li>Kommentar</li> 
     <li>Problem</li> 
     <li>Projekt</li> 
     <li>Sprint </li> 
     <li>Arbeitsprotokoll</li> 
     <li>Benutzerin oder Benutzer</li> 
     <li>Pinnwand</li> 
     <li>Kategorie</li> 
     <li>Filter</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ausgaben</td> 
   <td>Wählen Sie die Ausgaben aus, die Sie empfangen möchten. Je nach dem im Feld „Datensatztyp“ ausgewählten Datensatztyp stehen Ausgabeoptionen zur Verfügung.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Datensatztyp) ID</td> 
   <td> <p>Geben Sie die eindeutige Jira-ID des Datensatzes ein, den das Modul lesen soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Eintrag aktualisieren

Dieses Aktionsmodul aktualisiert einen vorhandenen Datensatz, z. B. ein Problem oder Projekt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Jira-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Jira mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Art des Eintrags</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den das Modul aktualisieren soll. Wenn Sie einen Datensatztyp auswählen, werden im Modul andere für diesen Datensatztyp spezifische Felder angezeigt.</p> 
    <ul> 
     <li>Kommentar</li> 
     <li>Problem</li> 
     <li>Projekt</li> 
     <li>Sprint </li> 
     <li>Übergangsproblem</li> 
     <li>Kategorie </li> 
     <li>Filter </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kennung oder Schlüssel</td> 
   <td>Geben Sie die ID oder den Schlüssel des Datensatzes ein, den Sie aktualisieren möchten, oder ordnen Sie sie zu.</td> 
  <tr> 
   <td role="rowheader">Andere Felder</td> 
   <td> Füllen Sie die anderen Felder aus. Die Felder sind je nach ausgewähltem Datensatztyp verfügbar. </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

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

#### Nach Datensätzen suchen

Dieses Suchmodul sucht in einem Jira-Objekt nach Datensätzen, die mit der von Ihnen angegebenen Suchanfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Jira-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Verbinden von Jira mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Art des Eintrags</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, nach dem das Modul suchen soll. Wenn Sie einen Datensatztyp auswählen, werden im Modul andere für diesen Datensatztyp spezifische Felder angezeigt.</p> 
    <ul> 
     <li>Problem</li> 
     <li>Projekt</li> 
     <li>Benutzerin oder Benutzer</li> 
     <li>Sprint</li> 
     <li>Pinnwand</li> 
     <li>Arbeitsprotokoll</li> 
     <li>Kommentar</li> 
     <li>Übergangsproblem</li> 
     <li>Kategorie</li> 
    </ul> </td> 
  <tr> 
   <td role="rowheader"> <p>Max Ergebnisse</p> </td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus abrufen soll, oder mappen Sie sie.</p> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Geben Sie die ID des ersten Elements ein, für das Sie Details abrufen möchten, oder ordnen Sie sie zu. Dies ist eine Möglichkeit, die Datensätze zu paginieren. Wenn Sie das 5000. Element als Offset eingeben, gibt das Modul die Elemente 5000-9999 zurück.</td> 
   </tr>
  <tr> 
   <td role="rowheader">Andere Felder</td> 
   <td> Füllen Sie die anderen Felder aus. Die Felder sind je nach ausgewähltem Datensatztyp verfügbar. </td> 
  </tr> 
 </tbody> 
</table>
