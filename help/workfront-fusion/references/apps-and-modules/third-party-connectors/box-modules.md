---
title: Box-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Box verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden. Überwacht einen angegebenen Ordner, um auf Dateiänderungen zu prüfen, vorhandene Dateien zu ändern und zu löschen oder neue Dateien in einen Ordner hochzuladen.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1548'
ht-degree: 1%

---

# Box-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Box] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden. Überwacht einen angegebenen Ordner, um auf Dateiänderungen zu prüfen, vorhandene Dateien zu ändern und zu löschen oder neue Dateien in einen Ordner hochzuladen.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

Um [!DNL Box]-Module verwenden zu können, müssen Sie über ein [!DNL Box]-Konto verfügen.

## Box-API-Informationen

Der Box-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box] Module und ihre Felder

Beim Konfigurieren von [!DNL Box] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Box] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Trigger

* [[!UICONTROL Neues Dateiereignis]](#new-file-event)
* [Neues Ordnerereignis](#new-folder-event)
* [[!UICONTROL Dateien ansehen]](#watch-files)

#### [!UICONTROL Neues Dateiereignis]

Dieses Instant Trigger-Modul startet ein Szenario, wenn eine ausgewählte Aktion auf einer Datei stattfindet.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Wählen Sie den Webhook aus, den Sie zum Überwachen ausgehender Nachrichten verwenden möchten, oder fügen Sie einen Webhook hinzu. </p><p>Um einen Webhook hinzuzufügen, klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie den Namen und die Verbindung des Webhooks, die Datei, die Sie überwachen möchten, und die Trigger ein, auf die Sie achten möchten.</p> <p> Anweisungen zum Verbinden Ihres [!UICONTROL Box]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung mit einem Dienst herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Neues Ordnerereignis

Dieses Instant Trigger-Modul startet ein Szenario, wenn die Auswahlaktion im Ordner stattfindet.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Wählen Sie den Webhook aus, den Sie zum Überwachen ausgehender Nachrichten verwenden möchten, oder fügen Sie einen Webhook hinzu. </p><p>Um einen Webhook hinzuzufügen, klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie den Namen und die Verbindung des Webhooks, den Ordner, den Sie überwachen möchten, und die Trigger ein, auf die Sie achten möchten.</p> <p> Anweisungen zum Verbinden Ihres [!UICONTROL Box]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung mit einem Dienst herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dateien ansehen]

Dieses Dateimodul startet ein Szenario, wenn eine neue Trigger hinzugefügt oder eine vorhandene Datei in einem überwachten Ordner aktualisiert wird.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  <tr> 
   <td role="rowheader">Im Ordner ansehen</td> 
   <td> <p>Wählen Sie den Ordner aus, den Sie beobachten möchten. Ein Szenario kann einen einzelnen Ordner überwachen.</p> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beobachten</td> 
   <td> <p>Wählen Sie den Typ der Dateien aus, die Sie beobachten möchten.</p> 
    <ul> 
     <li> <p><strong>Nur neue Dateien</strong> </p> <p>Das Szenario beginnt, wenn eine neue Datei hinzugefügt wird.</p> </li> 
     <li> <p><strong>Neue Dateien und alle Änderungen</strong> </p> <p>Das Szenario beginnt, wenn eine Datei hinzugefügt wird oder wenn der Dateiinhalt oder ein Dateiattribut (z. B. der Name) geändert wird.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Maximale Anzahl heruntergeladener Dateien</p> </td> 
   <td> <p>Geben Sie die höchste Anzahl von Dateien ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

<!--* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Upload] a file](#upload-a-file)-->
* [Erstellen eines Ordners](#create-a-folder)
* [Ordner abrufen](#get-a-folder)
* [Abrufen von Ordnermetadaten](#get-folder-metadata)
* [Durchführen eines API-Aufrufs](#make-an-api-call)
* [Aktualisieren von Ordnermetadaten](#update-folder-metadata)

<!--#### [!UICONTROL Delete a file] 

This action module deletes a file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

This action module downloads a file.

You specify the ID of the file.

>[!NOTE]
>
>This module is useful for providing files to subsequent modules.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to retrieve.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a file] 

This action module updates a file.

You specify the ID of the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to update.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file] 

This action module uploads a file.

You specify the file. You can also provide a new filename for the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Select the folder where you want to upload the file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If this module is not successful, consider the following:
>
>* The size of the file might exceed the maximum file size limit for your [!DNL Box] plan, or you may have used all of your [!DNL Box] account's storage quota. To get more storage space, delete existing files from [!DNL Box] or upgrade your [!DNL Box] account.
>* [!DNL Box] does not upload more than one files with the same name to a single folder. If the destination folder contains a file with the same name as the file being uploaded, the scenario run terminates with an error. To avoid this, rename the file. If you want to update the file, use the **[!UICONTROL Update a file]** module.-->

#### Erstellen eines Ordners

Dieses Aktionsmodul erstellt einen neuen leeren Ordner im angegebenen übergeordneten Ordner.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td> <p>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Übergeordneter Ordner]</td> 
   <td> <p>Wählen Sie den Ordner aus, in dem Sie den neuen Ordner erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner hochladen E-Mail-Zugriff]</td> 
   <td> <p>Wenn dieser Parameter festgelegt wurde, können Benutzer Dateien per E-Mail an die für diesen Ordner automatisch erstellte E-Mail-Adresse senden. Die Optionen für Mitwirkende lassen nur registrierte E-Mails für Mitwirkende zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Synchronisationsstatus]</td> 
   <td> <p>Gibt an, ob ein Ordner mit dem Gerät eines Benutzers synchronisiert werden soll. Dies wird von Box Sync (eingestellt) und nicht von Box Drive verwendet.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Ordner abrufen

Dieses Aktionsmodul ruft Details für einen Ordner ab, einschließlich der ersten 100 Einträge im Ordner.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td> <p>Wählen Sie den Ordner aus, für den Sie Details abrufen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen von Ordnermetadaten

Dieses Aktionsmodul ruft Ordnermetadaten nach Ordner-ID ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Umfang]</td> 
   <td> <p>Wählen Sie den Umfang aus, den Sie für diesen Metadatenabruf verwenden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td> <p>Wählen Sie den Ordner aus, für den Sie Metadaten abrufen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Durchführen eines API-Aufrufs

Dieses Aktionsmodul führt einen benutzerdefinierten Aufruf an die Box-API durch.



<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://api.box.com</code> ein. <p>Beispiel: <code>/2.0/users/me</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren von Ordnermetadaten

Dieses Aktionsmodul erstellt oder aktualisiert die Metadaten eines Ordners.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Umfang]</td> 
   <td> <p>Wählen Sie den Bereich aus, den Sie für diese Metadatenaktualisierung verwenden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td> <p>Wählen Sie den Ordner aus, für den Sie Metadaten aktualisieren möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Suchvorgänge

#### Suchen nach Inhalten

Dieses Suchmodul sucht nach Elementen, die dem Benutzer oder dem gesamten Unternehmen zur Verfügung stehen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Box]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Abfrage]</td> 
   <td> <p>Geben Sie die Zeichenfolge ein, nach der gesucht werden soll, oder ordnen Sie sie zu. Diese Abfrage wird mit Elementnamen, Beschreibungen, Textinhalten von Dateien und verschiedenen anderen Feldern der verschiedenen Elementtypen abgeglichen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Umfang]</td> 
   <td> <p>Wählen Sie aus, ob Sie nach Inhalten suchen, die mit dem Benutzer verknüpft sind, dessen Anmeldeinformationen für die in diesem Modul verwendete Verbindung verwendet werden, oder nach Inhalten suchen, die mit dem gesamten Unternehmen verknüpft sind.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Typ]</td> 
   <td> <p>Wählen Sie aus, ob Sie nach Dateien, Ordnern oder Weblinks suchen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL sort]</td> 
   <td> <p>Wählen Sie aus, ob Sie nach Relevanz oder Änderungsdatum sortieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Papierkorbinhalt]</td> 
   <td> <p>Wählen Sie aus, ob Sie nach Inhalt im Papierkorb oder nach Inhalten suchen möchten, die nicht im Papierkorb abgelegt wurden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs des übergeordneten Ordners]</td> 
   <td> <p>Um in einem bestimmten Ordner zu suchen, klicken Sie für jeden Ordner, den Sie suchen möchten, auf <b>Element hinzufügen</b> und geben Sie die ID des Ordners ein. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL erstellt aus]</td> 
   <td> <p>Um nach Assets zu suchen, die in einem bestimmten Datumsbereich erstellt wurden, geben Sie das früheste Datum im Bereich ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL erstellt bis]</td> 
   <td> <p>Um nach Assets zu suchen, die in einem bestimmten Datumsbereich erstellt wurden, geben Sie das letzte Datum im Bereich ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL aktualisiert von]</td> 
   <td> <p>Um nach Assets zu suchen, die in einem bestimmten Datumsbereich aktualisiert wurden, geben Sie das früheste Datum im Bereich ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL aktualisiert auf]</td> 
   <td> <p>Um nach Assets zu suchen, die in einem bestimmten Datumsbereich aktualisiert wurden, geben Sie das neueste Datum im Bereich ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Felder]</td> 
   <td> <p>Klicken Sie für jedes Attribut, das Sie in der Modulantwort zurückgeben möchten, auf <b>Element hinzufügen</b> und geben Sie das Feld ein.</p><p>Dies kann verwendet werden, um Felder anzufordern, die normalerweise nicht in einer Standardantwort zurückgegeben werden. Beachten Sie, dass die Angabe dieses Parameters dazu führt, dass keines der Standardfelder in der Antwort zurückgegeben wird, es sei denn, dies wird explizit angegeben. </p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dateierweiterungen]</td> 
   <td> <p>Um die Suche auf bestimmte Dateierweiterungen zu beschränken, geben Sie eine kommagetrennte Liste von Dateierweiterungen ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Größe von]</td> 
   <td> <p>Um nach Assets in einem bestimmten Größenbereich zu suchen, geben Sie das kleine Ende des Bereichs in Byte ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Größe auf]</td> 
   <td> <p>Um nach Assets in einem bestimmten Größenbereich zu suchen, geben Sie das große Ende des Bereichs in Byte ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eigentümer-Benutzer-ID]</td> 
   <td> <p>Um nach Assets zu suchen, die bestimmten Benutzern gehören, geben Sie eine kommagetrennte Liste von Eigentümer-IDs ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Ergebnissen ein, die das Modul in jedem Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>


