---
title: Jira-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Jira-Software verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
source-git-commit: d16c1d9f257d44b72cfb93caa2a814fd62b0b733
workflow-type: tm+mt
source-wordcount: '1564'
ht-degree: 5%

---

# Jira-Module

>[!NOTE]
>
>Diese Anweisungen gelten für die neue Version des Jira-Connectors, der einfach Jira genannt wird. Anweisungen zu den alten Jira Cloud- und Jira Server-Connectoren finden Sie unter [Jira-Softwaremodule](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md).

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Jira verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Der Jira-Connector kann sowohl für Jira Cloud als auch für Jira Data Server verwendet werden.

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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um Jira-Module verwenden zu können, müssen Sie über ein Jira-Konto verfügen.

## Verbinden von Jira mit Workfront Fusion

Sie können direkt aus einem Jira-Modul heraus eine Verbindung zu Ihrem Jira-Konto herstellen.

>[!IMPORTANT]
>
>* Um eine einfache Verbindung zum Jira-Rechenzentrum herzustellen, benötigen Sie ein Jira Personal Access Token.
>* Um eine einfache Verbindung zu Jira Cloud herzustellen, benötigen Sie ein Jira-API-Token
>* Um eine OAuth 2-Verbindung zu Jira Cloud oder Jira Data Center herzustellen, benötigen Sie eine Jira Client-ID und ein Client-Geheimnis.
>
>Anweisungen zum Erstellen dieser Elemente finden Sie in der Jira-Dokumentation.

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
      <td role="rowheader"> <p>Name der Verbindung</p> </td> 
      <td> <p>Geben Sie einen Namen für die neue Verbindung ein.</p> </td> 
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
      <td> <p>Wenn Sie eine OAuth 2-Verbindung erstellen, geben Sie Ihre Jira Client ID ein</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Client-Geheimnis</td> 
      <td> <p>Wenn Sie eine OAuth 2-Verbindung erstellen, geben Sie Ihr Jira-Client-Geheimnis ein</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">E-Mail</td> 
      <td>Wenn Sie eine Basisverbindung zu Jira Cloud herstellen, geben Sie Ihre E-Mail-Adresse ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API-Token</td> 
      <td>Wenn Sie eine Basisverbindung zu Jira Cloud erstellen, geben Sie Ihr API-Token ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Persönliches Zugriffstoken</td> 
      <td>Wenn Sie eine Basisverbindung zum Jira-Rechenzentrum herstellen, geben Sie Ihr persönliches Zugriffstoken ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API-Version</td> 
      <td>Wählen Sie die Jira-API-Version aus, mit der sich diese Verbindung verbinden soll.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.


## Jira-Module und ihre Felder

Beim Konfigurieren von Jira-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere Jira-Felder angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Trigger

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
* [Aktualisieren eines Datensatzes](#update-a-record)

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
     <li>Benutzerin bzw. Benutzer</li> 
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
   <td role="rowheader">Kopfzeilen</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Abfragezeichenfolge</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Textkörper</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
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
   <td role="rowheader">Datensatztyp</td> 
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
     <li>Benutzerin bzw. Benutzer</li> 
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

#### Aktualisieren eines Datensatzes

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
     <li>Benutzerin bzw. Benutzer</li> 
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
