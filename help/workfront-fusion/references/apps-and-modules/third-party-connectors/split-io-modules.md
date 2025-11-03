---
title: Split.io-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die verwenden [!DNL Split.io] und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 7d738a96-5424-4c30-831f-82e1d4c6f9d2
source-git-commit: d4bdc4005a3b7b22d64adc8ca1d20bcf534ddfd1
workflow-type: tm+mt
source-wordcount: '1925'
ht-degree: 0%

---

# [!DNL Split.io]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Split.io] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

Um [!DNL Split.io]-Module verwenden zu können, müssen Sie über ein [!DNL Split.io]-Konto verfügen.

## Split.io-API-Informationen

Der Split.io-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.split.io/internal/api</td>
   </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.34.1</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL Split.io] mit Workfront Fusion  {#connect-split-io-to-workfront-fusion}

Sie können direkt aus einem [!DNL Split.io]-Modul heraus eine Verbindung zu Ihrem [!DNL Split.io]-Konto herstellen.

1. Klicken Sie in einem [!DNL Split.io] Modul **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Füllen Sie die folgenden Felder aus.

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">[!UICONTROL Verbindungsname]</td> 
       <td> <p>Geben Sie einen Namen für die Verbindung ein.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>
          <p>Wählen Sie aus, ob eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung hergestellt werden soll.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">[!UICONTROL API-Schlüssel]</td> 
       <td>Geben Sie Ihren [!DNL Split.io] API-Schlüssel ein.<p>Weitere Informationen zu [!DNL Split.io] API-Schlüsseln finden Sie unter <a href="https://help.split.io/hc/en-us/articles/360019916211-API-keys">API-</a>) in der [!DNL Split.io].</p></td> 
      </tr> 
     </tbody> 
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Split.io] Module und ihre Felder

Beim Konfigurieren von [!DNL split.io] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL split.io] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Aktionen

* [[!UICONTROL Tags verknüpfen]](#associate-tags)
* [[!UICONTROL Aufspaltung erstellen]](#create-split)
* [[!UICONTROL Erstellen einer Aufspaltungsdefinition in der Umgebung]](#create-split-definition-in-environment)
* [[!UICONTROL Benutzerdefinierter API-Aufruf]](#custom-api-call)
* [[!UICONTROL Aufspaltung löschen]](#delete-split)
* [[!UICONTROL Geteilt werden]](#get-split)
* [[!UICONTROL Aufspaltungsdefinition in Umgebung abrufen]](#get-split-definition-in-environment)
* [[!UICONTROL Teilweise Aktualisierung der Aufspaltungsdefinition in der Umgebung]](#partial-update-split-definition-in-environment)
* [[!UICONTROL Aufspaltungsdefinition aus der Umgebung entfernen]](#remove-split-definition-from-environment)

#### [!UICONTROL Tags verknüpfen]

Dieses Aktionsmodul fügt dem angegebenen Objekt Tags hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, dem Sie ein Tag hinzufügen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objektname]</td> 
   <td>Geben Sie den Namen des Objekts ein, dem Sie Tags hinzufügen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objekttyp]</td> 
   <td> <p>Geben Sie den Objekttyp ein, dem Sie Tags hinzufügen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> <p>Klicken Sie für jedes Tag, das Sie hinzufügen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie das Tag ein oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufspaltung erstellen]

Dieses Aktionsmodul erstellt bei einem Traffic-Typ eine neue Aufspaltung in Ihrer Organisation.

>[!NOTE]
>
>Die API konfiguriert die Aufspaltung in keiner Umgebung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, in dem Sie die Aufspaltung erstellen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Traffic Type ID or Name]</td> 
   <td>Wählen Sie den Traffic-Typ aus, den Sie zum Erstellen der Aufspaltung verwenden möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilungsname]</td> 
   <td> <p>Geben Sie einen Namen für die zu erstellende Teilung ein, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilungsbeschreibung]</td> 
   <td>Geben Sie eine [!UICONTROL split]-Beschreibung für die zu erstellende Teilung ein oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen einer Aufspaltungsdefinition in der Umgebung]

Dieses Aktionsmodul konfiguriert eine Aufspaltungsdefinition für eine bestimmte Umgebung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, in dem Sie eine Aufspaltungsdefinition erstellen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Umgebungsname oder ID]</td> 
   <td>Wählen Sie die Umgebung aus, in der Sie eine Aufspaltungsdefinition erstellen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilungsname]</td> 
   <td> <p>Geben Sie den Namen der Teilung ein, für die Sie eine Definition erstellen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentare]</td> 
   <td>Geben Sie alle Kommentare ein, die Sie der Aufspaltungsdefinition hinzufügen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Regeln]</td> 
   <td> <p>Klicken Sie für jede Targeting-Regel, die Sie der Definition hinzufügen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie dann die Regel ein oder ordnen Sie sie zu. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Standardregel]</td> 
   <td> <p>Geben Sie die Regel ein, die die Aufspaltung für den Traffic verwenden soll und die Spezifikationen für die anderen Regeln nicht erfüllt, oder ordnen Sie sie zu.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Standardbehandlung]</td> 
   <td> <p>Geben Sie die Behandlung ein oder mappen Sie sie, wenn die Aufspaltung abgebrochen werden soll oder der Kunde nicht in die Traffic-Zuordnung einbezogen ist.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abwandlungen]</td> 
   <td> <p>Klicken Sie für jede Abwandlung, die Sie der Definition hinzufügen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie dann die Abwandlung und Größe ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL split.io]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL split.io] nicht durchgeführt werden kann.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://api.split.io/internal/api/v2/</code> ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufspaltung löschen]

Dieses Aktionsmodul löscht eine Aufspaltung aus Ihrer Organisation. Dadurch wird die Konfiguration der Aufspaltungsdefinition in allen Umgebungen automatisch aufgehoben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, in dem Sie die Aufspaltung löschen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilungsname]</td> 
   <td> <p>Geben Sie den Namen der zu löschenden Aufspaltung ein oder mappen Sie ihn.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Geteilt werden]

Dieses Aktionsmodul ruft die Aufspaltung ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die abzurufende Aufspaltung enthält, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilungsname]</td> 
   <td> <p>Geben Sie den Namen der Teilung, die Sie abrufen möchten, ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufspaltungsdefinition in Umgebung abrufen]

Dieses Aktionsmodul ruft eine bestimmte Aufspaltungsdefinition aus der angegebenen Umgebung ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die abzurufende Aufspaltungsdefinition enthält, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Umgebungsname oder ID]</td> 
   <td>Wählen Sie die Umgebung aus, die die abzurufende Aufspaltungsdefinition enthält, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilungsname]</td> 
   <td> <p>Geben Sie den Namen der Aufspaltung ein, für die Sie die Aufspaltungsdefinition abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Teilweise Aktualisierung der Aufspaltungsdefinition in der Umgebung]

Dieses Aktionsmodul aktualisiert eine Aufspaltungsdefinition für eine bestimmte Umgebung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, in dem Sie eine Aufspaltungsdefinition aktualisieren möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Umgebungsname oder ID]</td> 
   <td>Wählen oder mappen Sie die Umgebung, in der Sie eine Aufspaltungsdefinition aktualisieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilungsname]</td> 
   <td> <p>Geben Sie den Namen der Aufspaltung ein, für die Sie eine Definition aktualisieren möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inhalt aktualisieren]</td> 
   <td> <p>Klicken Sie für jedes Attribut der Aufspaltung, das Sie aktualisieren möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie die gewünschten Änderungen ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentare]</td> 
   <td>Geben Sie alle Kommentare ein, die Sie der Aufspaltungsdefinition hinzufügen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufspaltungsdefinition aus der Umgebung entfernen]

Mit diesem Aktionsmodul wird die Konfiguration einer Aufspaltungsdefinition für eine bestimmte Umgebung aufgehoben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, in dem Sie eine Aufspaltungsdefinition entfernen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Umgebungsname oder ID]</td> 
   <td>Wählen Sie die Umgebung aus, in der Sie eine Aufspaltungsdefinition entfernen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Teilungsname]</td> 
   <td> <p>Geben Sie den Namen der Teilung ein, für die Sie eine Definition entfernen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kommentare]</td> 
   <td>Geben Sie alle Kommentare ein, die Sie der Aufspaltungsdefinition hinzufügen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Tags verknüpfen]

Dieses Aktionsmodul fügt dem angegebenen Objekt Tags hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, dem Sie ein Tag hinzufügen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objektname]</td> 
   <td>Geben Sie den Namen des Objekts ein, dem Sie Tags hinzufügen möchten, oder ordnen Sie ihn zu,</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objekttyp]</td> 
   <td> <p>Geben Sie den Objekttyp ein, dem Sie Tags hinzufügen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> <p>Klicken Sie für jedes Tag, das Sie hinzufügen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie das Tag ein oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL Abrufen von Umgebungen]](#get-environments)
* [[!UICONTROL Traffic-Typen abrufen]](#get-traffic-types)
* [[!UICONTROL Arbeitsbereiche abrufen]](#get-workspaces)
* [[!UICONTROL Aufspaltungsdefinitionen in einer Umgebung auflisten]](#list-split-definitions-in-an-environment)
* [[!UICONTROL Aufspaltungen auflisten]](#list-splits)

#### [!UICONTROL Abrufen von Umgebungen]

Dieses Suchmodul ruft eine Liste von Umgebungen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die Umgebungen enthält, die Sie auflisten möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Traffic-Typen abrufen]

Dieses Suchmodul ruft eine Liste von Traffic-Typen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die Traffic-Typen enthält, die Sie auflisten möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Arbeitsbereiche abrufen]

Dieses Suchmodul ruft die Arbeitsbereiche für eine Organisation ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Arbeitsbereichen ein, die das Modul während jedes Szenario-Ausführungszyklus abrufen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufspaltungsdefinitionen in einer Umgebung auflisten]

Dieses Suchmodul ruft eine Liste von Aufspaltungsdefinitionen in einer bestimmten Umgebung ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die Aufspaltungsdefinitionen enthält, die Sie auflisten möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Umgebungsname oder ID]</td> 
   <td>Wählen Sie die Umgebung aus, die die Aufspaltungsdefinitionen enthält, die Sie auflisten möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl an Aufspaltungsdefinitionen ein, die das Modul während jedes Szenario-Ausführungszyklus abrufen soll, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aufspaltungen auflisten]

Dieses Suchmodul ruft eine Liste von Teilungen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die Aufspaltungen enthält, die Sie auflisten möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Aufspaltungen ein, die das Modul während jedes Szenario-Ausführungszyklus abrufen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>
