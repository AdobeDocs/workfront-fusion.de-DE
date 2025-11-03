---
title: Azure DevOps-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die verwenden [!DNL Azure DevOps] und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 1%

---

# [!DNL Azure DevOps]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Azure DevOps] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um [!DNL Azure DevOps] Module verwenden zu können, müssen Sie über ein [!DNL Azure] DevOps-Konto verfügen.

## [!DNL Azure DevOps] API-Informationen

Der Azure DevOps-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v5.1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.29.33</td> 
  </tr>
 </tbody> 
</table>

## Verbinden von [!DNL Azure DevOps] mit Workfront Fusion {#connect-azure-devops-to-workfront-fusion}

1. Fügen Sie Ihrem Szenario ein [!DNL Azure DevOps] hinzu.
1. Klicken Sie **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Wählen [!UICONTROL  im Feld ] den Verbindungstyp aus, den Sie verwenden möchten.

   >[!NOTE]
   >
   >Mit der [!UICONTROL [!DNL Azure DevOps] (EntraApp] können Sie alle Bereiche für die Verbindung anfordern.

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto">
      <tr>
            <td>[!UICONTROL Verbindungsname]</td>
            <td>Geben Sie einen Namen für die Verbindung ein, die Sie erstellen.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Organisation]</td>
            <td>Geben Sie den Namen der Organisation ein, unter der Sie Ihr [!DNL Azure DevOps]-Programm erstellt haben.</td>
      </tr>
      <tr>
            <td>[!UICONTROL App-ID]</td>
            <td>Geben Sie die ID der DevOps-Anwendung ein, mit der Sie eine Verbindung herstellen.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Client-Geheimnis]</td>
            <td>Geben Sie das Client-Geheimnis für die DevOps-Anwendungen ein, mit denen Sie eine Verbindung herstellen.</td>
      </tr>
      <tr>
            <td>[!UICONTROL, alle Bereiche anfordern]</td>
            <td>Wenn Sie den Verbindungstyp [!DNL Azure DevOps] (EntraApp) verwenden, aktivieren Sie diese Option, um alle Bereiche für die Verbindung anzufordern.</td>
      </tr>
   </table>

1. Um eine Azure DevOps-App-ID oder einen geheimen Client-Schlüssel einzugeben, klicken Sie auf <b>Erweiterte Einstellungen anzeigen</b> und geben Sie diese in die sich öffnenden Felder ein.
1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Einrichtung der Verbindung abzuschließen und mit der Erstellung Ihres Szenarios fortzufahren.

## [!UICONTROL Azure DevOps]-Module und ihre Felder

Beim Konfigurieren von [!DNL Azure DevOps] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Azure DevOps] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Trigger

#### [!UICONTROL Auf Arbeitselemente ]

Dieses Instant-Trigger-Modul führt ein Szenario aus, wenn ein Datensatz in (Azure DevOps[!UICONTROL  hinzugefügt, aktualisiert oder gelöscht ].

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Webhook für das Modul auswählen oder hinzufügen.</p> <p>Weitere Informationen zu Webhooks in Trigger-Modulen finden Sie unter <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Instant Trigger (Webhooks)</a>.</p> <p>Informationen zum Erstellen eines Webhooks finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [Erstellen eines Datensatzes](#create-a-record)
* [Benutzerdefinierter API-Aufruf](#custom-api-call)
* [Herunterladen eines Anhangs](#download-an-attachment)
* [Arbeitselemente verknüpfen](#link-work-items)
* [Datensatz lesen](#read-record)
* [Aktualisieren eines Arbeitselements](#update-a-work-item)
* [[!UICONTROL Anlage hochladen]](#upload-an-attachment)

#### [!UICONTROL Datensatz erstellen]

Dieses Aktionsmodul erstellt ein neues Projekt oder Arbeitselement.

Das Modul gibt die Objekt-ID für das neu erstellte Arbeitselement oder die URL und den Status-Code eines neu erstellten Projekts aus.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie aus, ob Sie ein Arbeitselement oder ein Projekt erstellen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL-Projekt]</strong> </p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Name]</strong>: Geben Sie einen Namen für das neue Projekt ein oder ordnen Sie ihn ihm zu.</p> </li> 
       <li> <p><strong>[!UICONTROL Description]</strong>: Geben Sie eine Beschreibung für das neue Projekt ein oder ordnen Sie sie zu. </p> </li> 
       <li> <p><strong>[!UICONTROL Sichtbarkeit]</strong>: Wählen Sie aus, ob Ihr Projekt öffentlich oder privat sein soll. Benutzer müssen bei Ihrer Organisation angemeldet sein und Zugriff auf das Projekt erhalten haben, damit sie mit einem privaten Projekt interagieren können. Öffentliche Projekte sind für Benutzer sichtbar, die nicht bei Ihrer Organisation angemeldet sind.</p> </li> 
       <li> <p><strong>[!UICONTROL Versionskontrolle]</strong>: Wählen Sie aus, ob das Projekt [!DNL Git] oder [!UICONTROL Team Foundation Version Control (TFCV)] für die Versionskontrolle verwenden soll.</p> </li> 
       <li> <p><strong>[!UICONTROL Arbeitselementprozess]</strong>: Wählen Sie den Arbeitsprozess aus, den Sie für das Projekt verwenden möchten. Die Optionen sind [!UICONTROL Basic], [!UICONTROL Scrum], [!UICONTROL Capability Maturity Model Integration (CMMI)] und [!UICONTROL Agile].</p> <p>Weitere Informationen zu [!DNL Azure DevOps]-Prozessen finden Sie unter <a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&amp;tabs=basic-process">Standardprozesse und Prozessvorlagen</a> in der [!DNL Azure DevOps].</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Arbeitselement]</strong> </p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Project]</strong>: Wählen Sie das Projekt aus, in dem Sie das Arbeitselement erstellen möchten.</p> </li> 
       <li> <p><strong>[!UICONTROL Arbeitsaufgabentyp]</strong>: Wählen Sie den Typ des Arbeitselements, das Sie erstellen möchten.</p> </li> 
       <li> <p><strong>[!UICONTROL Andere Felder]</strong>: Geben Sie in diesen Feldern den Wert ein, den das Arbeitselement für eine bestimmte Eigenschaft haben soll. Die verfügbaren Felder hängen vom Typ des Arbeitselements ab.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Azure DevOps]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Azure DevOps] nicht durchgeführt werden kann.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Basis-URL]</td> 
   <td> <p>Wählen Sie die Basis-URL aus, mit der Sie eine Verbindung zu Ihrem [!DNL Azure DevOps]-Konto herstellen, oder ordnen Sie sie zu</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL relative URL]</td> 
   <td> <p>Geben Sie die relative URL ein, mit der Sie sich für diesen API-Aufruf verbinden möchten.</p> <p><b>Beispiel: </b><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL API-Version]</td> 
   <td>Wählen Sie die Version der [!DNL Azure DevOps]-API aus, mit der Sie sich für diesen API-Aufruf verbinden möchten, oder ordnen Sie sie zu. Wenn keine Version ausgewählt ist, stellt Workfront Fusion eine Verbindung zu [!DNL Azure DevOps] API-Version 5.1 her.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> </td> 
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

#### [!UICONTROL Anlage herunterladen]

Dieses Aktionsmodul lädt eine Anlage herunter.

Das -Modul gibt den Dateiinhalt des Anhangs zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anhang URL]</td> 
   <td> <p>Geben Sie die URL des Anhangs ein, den Sie herunterladen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Arbeitselemente verknüpfen]

Dieses Aktionsmodul verknüpft zwei Arbeitselemente und definiert die Beziehung zwischen ihnen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitselement-ID]</td> 
   <td>Geben Sie die ID des Hauptarbeitselements ein, mit dem Sie ein anderes Arbeitselement verknüpfen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID des verknüpften Arbeitselements]</td> 
   <td>Geben Sie die ID des Arbeitselements ein, das Sie mit dem Hauptarbeitselement verknüpfen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Link-Typ]</td> 
   <td> <p>Definieren Sie die Beziehung zwischen den Arbeitselementen, die Sie verknüpfen möchten.</p> <p>Weitere Informationen finden Sie <a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops">Referenzhandbuch für Link-Typen</a> in der [!UICONTROL Azure DevOps]-Dokumentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kommentar]</td> 
   <td>Geben Sie den Text eines Kommentars ein oder mappen Sie ihn. Dies ist nützlich, um die Begründung oder Absicht des Links zu erklären.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datensatz lesen]

Dieses Aktionsmodul liest Daten aus einem einzelnen Datensatz in [!DNL Azure DevOps].

Sie geben die ID des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Auswählen, ob ein Projekt oder ein Arbeitselement gelesen werden soll</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong>: Wählen Sie das Projekt aus, das Sie lesen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL Arbeitselement]</strong>: Wählen Sie das Projekt aus, das das Arbeitselement enthält, das Sie lesen möchten, und wählen Sie dann den Arbeitselementtyp aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen. Die verfügbaren Felder hängen vom Typ des Arbeitselements ab.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Datensatzes ein, den Sie lesen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Arbeitselement aktualisieren]

Dieses Aktionsmodul aktualisiert ein vorhandenes Arbeitselement mithilfe seiner ID.

Das Modul gibt die ID des aktualisierten Arbeitselements zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Projekt]</td> 
   <td>Wählen Sie das Projekt aus, das das Arbeitselement enthält, das Sie aktualisieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsaufgabentyp]</td> 
   <td> <p>Wählen Sie den Typ des Arbeitselements aus, das Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Andere Felder]</td> 
   <td>Geben Sie in jedem dieser Felder den Wert ein, den das Arbeitselement für eine bestimmte Eigenschaft haben soll. Die verfügbaren Felder hängen vom Typ des Arbeitselements ab.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitselement-ID]</td> 
   <td>Geben Sie die ID des Arbeitselements ein, das Sie aktualisieren möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Anlage hochladen]

Dieses Aktionsmodul lädt eine Datei hoch und hängt sie an ein Arbeitselement an.

Das Modul gibt die Anlagen-ID und eine Download-URL für den Anhang zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Projekt] </td> 
   <td> <p>Wählen Sie das Projekt aus, in das Sie eine Anlage hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitselement-ID]</td> 
   <td> <p>Geben Sie die ID des Arbeitselements ein, in das Sie eine Anlage hochladen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kommentar]</td> 
   <td>Geben Sie den Text eines Kommentars ein, den Sie zum hochgeladenen Anhang hinzufügen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei] </td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder geben Sie den Namen und den Inhalt der Quelldatei ein oder mappen Sie ihn.</td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

#### [!UICONTROL Arbeitselemente auflisten]

Dieses Aktionsmodul ruft alle Arbeitselemente eines bestimmten Typs in einem [!DNL Azure DevOps] Projekt ab.

Das Modul gibt die ID des Hauptarbeitselements und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Projekt]</td> 
   <td>Wählen Sie das Projekt aus, aus dem Sie Arbeitselemente abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsaufgabentyp]</td> 
   <td> <p>Wählen Sie den Typ des Arbeitselements, das Sie abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Eigenschaften aus, die in der Modulausgabe angezeigt werden sollen. Die verfügbaren Felder hängen vom Typ des Arbeitselements ab, das Sie abrufen möchten. Sie müssen mindestens eine Eigenschaft auswählen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Arbeitselementen ein, die Workfront Fusion während eines Ausführungszyklus zurückgibt, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>
