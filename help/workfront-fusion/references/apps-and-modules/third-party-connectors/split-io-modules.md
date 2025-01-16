---
title: Split.io-Module
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die  [!DNL Split.io] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 7d738a96-5424-4c30-831f-82e1d4c6f9d2
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1493'
ht-degree: 0%

---

# [!DNL Split.io]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Split.io] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung und -integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den [!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Adobe Workfront] verfügen, muss Ihr Unternehmen [!DNL Adobe Workfront Fusion] kaufen und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden. [!DNL Workfront Fusion] ist im [!UICONTROL Ultimate] [!DNL Workfront] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

## [!DNL Split.io] mit [!DNL Workfront Fusion] verbinden {#connect-split-io-to-workfront-fusion}

Sie können direkt aus einem [!DNL Split.io]-Modul heraus eine Verbindung zu Ihrem [!DNL Split.io]-Konto herstellen.

1. Klicken Sie in einem beliebigen [!DNL Split.io] auf **[!UICONTROL Add]** neben dem Feld [!UICONTROL Connection] .
1. Geben Sie einen Namen für die Verbindung ein.
1. Geben Sie Ihren [!DNL Split.io] API-Schlüssel ein.

   Weitere Informationen zu [!DNL Split.io] API-Schlüsseln finden Sie unter [API-](https://help.split.io/hc/en-us/articles/360019916211-API-keys)) in der [!DNL Split.io].

1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Split.io] Module und ihre Felder

Beim Konfigurieren [!DNL split.io] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL split.io] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Aktionen

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Get Split]](#get-split)
* [[!UICONTROL Get Split Definition in Environment]](#get-split-definition-in-environment)
* [[!UICONTROL Create Split]](#create-split)
* [[!UICONTROL Delete Split]](#delete-split)
* [[!UICONTROL Create Split Definition in Environment]](#create-split-definition-in-environment)
* [[!UICONTROL Remove Split Definition from Environment]](#remove-split-definition-from-environment)
* [[!UICONTROL Partial Update Split Definition in Environment]](#partial-update-split-definition-in-environment)
* [[!UICONTROL Associate Tags]](#associate-tags)

#### [!UICONTROL Custom API Call]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL split.io]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL split.io] nicht durchgeführt werden kann.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://api.split.io/internal/api/v2/</code> ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
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

#### [!UICONTROL Get Split]

Dieses Aktionsmodul ruft die Aufspaltung ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die abzurufende Aufspaltung enthält, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Geben Sie den Namen der Teilung, die Sie abrufen möchten, ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Split Definition in Environment]

Dieses Aktionsmodul ruft eine bestimmte Aufspaltungsdefinition aus der angegebenen Umgebung ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die abzurufende Aufspaltungsdefinition enthält, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Wählen Sie die Umgebung aus, die die abzurufende Aufspaltungsdefinition enthält, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Geben Sie den Namen der Aufspaltung ein, für die Sie die Aufspaltungsdefinition abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Split]

Dieses Aktionsmodul erstellt bei einem Traffic-Typ eine neue Aufspaltung in Ihrer Organisation.

>[!NOTE]
>
>Die API konfiguriert die Aufspaltung in keiner Umgebung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Geben Sie einen Namen für die zu erstellende Teilung ein, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Description]</td> 
   <td>Geben Sie eine [!UICONTROL split] Beschreibung für die zu erstellende Teilung ein oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Split]

Dieses Aktionsmodul löscht eine Aufspaltung aus Ihrer Organisation. Dadurch wird die Konfiguration der Aufspaltungsdefinition in allen Umgebungen automatisch aufgehoben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, in dem Sie die Aufspaltung löschen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Geben Sie den Namen der zu löschenden Aufspaltung ein oder mappen Sie ihn.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Split Definition in Environment]

Dieses Aktionsmodul konfiguriert eine Aufspaltungsdefinition für eine bestimmte Umgebung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, in dem Sie eine Aufspaltungsdefinition erstellen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Wählen Sie die Umgebung aus, in der Sie eine Aufspaltungsdefinition erstellen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Geben Sie den Namen der Teilung ein, für die Sie eine Definition erstellen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>Geben Sie alle Kommentare ein, die Sie der Aufspaltungsdefinition hinzufügen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rules]</td> 
   <td> <p>Klicken Sie für jede Zielgruppenregel, die Sie der Definition hinzufügen möchten, auf <b>[!UICONTROL Add item]</b> und geben Sie dann die Regel ein oder ordnen Sie sie zu.</p> <p>Weitere Informationen zu Zielgruppenbestimmungsregeln finden Sie unter <a href="https://docs.split.io/reference#create-split-definition-in-environment">Erstellen einer Aufspaltungsdefinition in einer Umgebung</a> in der [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Default rule]</td> 
   <td> <p>Geben Sie die Regel ein, die die Aufspaltung für den Traffic verwenden soll und die Spezifikationen für die anderen Regeln nicht erfüllt, oder ordnen Sie sie zu.</p> <p>Weitere Informationen zu Zielgruppenbestimmungsregeln finden Sie unter <a href="https://docs.split.io/reference#create-split-definition-in-environment">Erstellen einer Aufspaltungsdefinition in einer Umgebung</a> in der [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Default treatment]</td> 
   <td> <p>Geben Sie die Behandlung ein oder mappen Sie sie, wenn die Aufspaltung abgebrochen werden soll oder der Kunde nicht in die Traffic-Zuordnung einbezogen ist.</p> <p>Weitere Informationen zu Abwandlungen finden Sie unter <a href="https://docs.split.io/reference#create-split-definition-in-environment">Erstellen einer Aufspaltungsdefinition in einer Umgebung</a> in der [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Treatments]</td> 
   <td> <p>Klicken Sie für jede Abwandlung, die Sie der Definition hinzufügen möchten, auf <b>[!UICONTROL Add item]</b> und geben Sie dann die Abwandlung ein oder ordnen Sie sie zu.</p> <p>Weitere Informationen zu Abwandlungen finden Sie unter <a href="https://docs.split.io/reference#create-split-definition-in-environment">Erstellen einer Aufspaltungsdefinition in einer Umgebung</a> in der [!DNL Split.io].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Split Definition from Environment]

Mit diesem Aktionsmodul wird die Konfiguration einer Aufspaltungsdefinition für eine bestimmte Umgebung aufgehoben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, in dem Sie eine Aufspaltungsdefinition entfernen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Wählen Sie die Umgebung aus, in der Sie eine Aufspaltungsdefinition entfernen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Geben Sie den Namen der Teilung ein, für die Sie eine Definition entfernen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>Geben Sie alle Kommentare ein, die Sie der Aufspaltungsdefinition hinzufügen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Partial Update Split Definition in Environment]

Dieses Aktionsmodul aktualisiert eine Aufspaltungsdefinition für eine bestimmte Umgebung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, in dem Sie eine Aufspaltungsdefinition aktualisieren möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Wählen oder mappen Sie die Umgebung, in der Sie eine Aufspaltungsdefinition aktualisieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Geben Sie den Namen der Aufspaltung ein, für die Sie eine Definition aktualisieren möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update content]</td> 
   <td> <p>Klicken Sie für jedes Attribut der Aufspaltung, das Sie aktualisieren möchten, auf <b>[!UICONTROL Add item]</b> und geben Sie die gewünschten Änderungen ein oder ordnen Sie sie zu.</p> <p>Weitere Informationen finden Sie unter <a href="https://docs.split.io/reference#partial-update-split-definition-in-environment">Teilweise Aktualisierung der Aufspaltungsdefinition in </a>) in der [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>Geben Sie alle Kommentare ein, die Sie der Aufspaltungsdefinition hinzufügen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Associate Tags]

Dieses Aktionsmodul fügt dem angegebenen Objekt Tags hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, dem Sie ein Tag hinzufügen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Name]</td> 
   <td>Geben Sie den Namen des Objekts ein, dem Sie Tags hinzufügen möchten, oder ordnen Sie ihn zu,</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type]</td> 
   <td> <p>Geben Sie den Objekttyp ein, dem Sie Tags hinzufügen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> <p>Klicken Sie für jedes Tag, das Sie hinzufügen möchten, auf <b>[!UICONTROL Add item]</b> und geben Sie das Tag ein oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL Get Workspaces]](#get-workspaces)
* [[!UICONTROL Get Environments]](#get-environments)
* [[!UICONTROL Get Splits]](#get-splits)
* [[!UICONTROL List Split Definitions in an Environment]](#list-split-definitions-in-an-environment)
* [[!UICONTROL Get Traffic Types]](#get-traffic-types)

#### [!UICONTROL Get Workspaces]

Dieses Suchmodul ruft die Arbeitsbereiche für eine Organisation ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Arbeitsbereichen ein, die das Modul während jedes Szenario-Ausführungszyklus abrufen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Environments]

Dieses Suchmodul ruft eine Liste von Umgebungen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die Umgebungen enthält, die Sie auflisten möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Splits]

Dieses Suchmodul ruft eine Liste von Teilungen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
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

#### [!UICONTROL List Split Definitions in an Environment]

Dieses Suchmodul ruft eine Liste von Aufspaltungsdefinitionen in einer bestimmten Umgebung ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die Aufspaltungsdefinitionen enthält, die Sie auflisten möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Wählen Sie die Umgebung aus, die die Aufspaltungsdefinitionen enthält, die Sie auflisten möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl an Aufspaltungsdefinitionen ein, die das Modul während jedes Szenario-Ausführungszyklus abrufen soll, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Traffic Types]

Dieses Suchmodul ruft eine Liste von Traffic-Typen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Split.io]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Split.io] mit [!UICONTROL Workfront Fusion] </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie den Arbeitsbereich aus, der die Traffic-Typen enthält, die Sie auflisten möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>
