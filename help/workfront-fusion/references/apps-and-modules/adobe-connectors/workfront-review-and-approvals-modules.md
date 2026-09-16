---
title: Adobe Workfront-Module für Inhalte und Genehmigungen
description: Mit den Adobe Workfront-Modulen für Inhalte und Genehmigungen können Sie Genehmigungsdetails abrufen, eine Entscheidung über ein Asset treffen, Genehmigungsteilnehmer hinzufügen oder löschen, Genehmigungsphasen hinzufügen oder aktualisieren, Phasen sperren oder entsperren und benutzerdefinierte API-Aufrufe durchführen.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4f637dcb9d7865f73b41faa5b0acf397944bb559
workflow-type: tm+mt
source-wordcount: '5202'
ht-degree: 11%
---
# Einheitliche Prüfungs- und Genehmigungsmodule für Adobe Workfront

Mit den Modulen Adobe Workfront Unified Review and Approvals können Sie Genehmigungsdetails abrufen, eine Entscheidung über ein Asset treffen, Genehmigungsteilnehmer hinzufügen oder löschen, Genehmigungsphasen hinzufügen oder aktualisieren, Phasen sperren oder entsperren und benutzerdefinierte API-Aufrufe durchführen.

Informationen zu einheitlichen Workfront-Überprüfungen und -Genehmigungen finden Sie unter [Einheitliche Überprüfung und Genehmigung - Übersicht](https://experienceleague.adobe.com/de/docs/workfront/using/review-and-approve-work/document-approvals-overview) in der Dokumentation zu Workfront.

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
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td>
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Voraussetzungen

Sie müssen über Folgendes verfügen, um auf Workfront-Inhalte und -Genehmigungen zugreifen zu können:

* Sie müssen eine Version von Workfront verwenden, die den Adobe-Cloud-Speicher unterstützt. Wenn für Ihr Unternehmen noch keine unterstützte Version verfügbar ist, wenden Sie sich an den Adobe-Kundenbetreuer.

## Mit Adobe Workfront einheitliche Überprüfung und Genehmigungen verbinden


1. Klicken Sie in einem beliebigen einheitlichen Adobe Workfront-Modul für Überprüfung und Genehmigungen **Hinzufügen** neben dem Feld Verbindung .
1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungstyp]</td>
        <td>
          <p>Wählen Sie <b>Adobe Workfront-Server-zu-Server-Verbindung</b> aus.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für die neue Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instanzname]</td>
        <td>
          <p>Geben Sie den Namen Ihrer Instanz ein (auch als Domain bezeichnet).</p><p>Wenn Ihre URL z. B. <code>https://example.my.workfront.com</code> lautet, geben Sie <code>example</code> ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instanzen-Lane]</td>
        <td>
          <p>Geben Sie den Umgebungstyp für die Verbindung ein.</p><p>Wenn Ihre URL z. B. <code>https://example.my.workfront.com</code> lautet, geben Sie <code>my</code> ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre Workfront-Client-ID ein. Diese finden Sie im Workfront-Bereich „Setup“ unter „OAuth2-Programme“. Öffnen Sie die Anwendung, zu der eine Verbindung hergestellt werden soll, um die Client-ID anzuzeigen.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr Workfront-Client-Geheimnis ein. Diese finden Sie im Workfront-Bereich „Setup“ unter „OAuth2-Programme“. Wenn Sie in Workfront kein Client-Geheimnis für Ihre OAuth2-Anwendung besitzen, können Sie ein anderes generieren. Anweisungen hierzu finden Sie in der Workfront-Dokumentation.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Bereiche]</td>
        <td>Geben Sie alle zutreffenden Bereiche für diese Verbindung ein.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host-Präfix]</td>
        <td>In den meisten Fällen sollte dieser Wert auf <code>origin</code> gesetzt werden.
      </tr>
    </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

   Wenn Sie nicht bei Workfront Unified Review and Approvals angemeldet sind, werden Sie zu einem Anmeldebildschirm weitergeleitet. Nach der Anmeldung können Sie die Verbindung zulassen.

## Einheitliche Prüfungs- und Genehmigungsmodule für Adobe Workfront

Beim Konfigurieren von Workfront-Modulen werden in Workfront Fusion die unten aufgeführten Felder angezeigt. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere Workfront-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktionen](#actions)
* [Suchvorgänge](#searches)
* [Sonstiges](#other)

### Aktionen

* [Teilnehmer hinzufügen oder aktualisieren](#add-or-update-participants)
* [Massenlöschvorlagen](#bulk-delete-templates)
* [Erstellen einer Vorlage](#create-a-template)
* [Gruppierte Validierung erstellen](#create-grouped-approval)
* [Stadien erstellen](#create-stages)
* [Stadium sperren](#lock-a-stage)
* [Entscheidung treffen](#make-a-decision)
* [Etappenentscheidung treffen](#make-a-decision-on-a-stage)
* [Verwalten von Assets für eine gruppierte Genehmigung](#manage-assets-on-a-grouped-approval)
* [Stadiumsteilnehmer verwalten](#manage-stage-participants)
* [Stadien einer gruppierten Genehmigung verwalten](#manage-stages-on-a-grouped-approval)
* [Erinnern eines Teilnehmers an einer Bühne](#remind-a-participant-on-a-stage)
* [Teilnehmer erinnern](#remind-participant)
* [Unentschlossene Teilnehmende erinnern](#remind-undecided-participants)
* [Unentschlossene Teilnehmer auf einer Bühne erinnern](#remind-undecided-participants-on-a-stage)
* [Phase entsperren](#unlock-a-stage)
* [Aktualisierungsschritt](#update-a-stage)
* [Aktualisieren einer Vorlage](#update-a-template)
* [Alle Stadien aktualisieren](#update-all-stages)
* [Gruppierte Genehmigung aktualisieren (voller Status)](#update-grouped-approval-full-state)


#### Teilnehmer hinzufügen oder aktualisieren

Dieses Aktionsmodul fügt Teilnehmer im Standardstadium einer Genehmigung hinzu oder aktualisiert sie.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Dokument-ID</p>
      </td>
      <td>Geben Sie die ID des Assets ein, für das Sie einen Teilnehmer hinzufügen oder aktualisieren möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Teilnehmer zu Stadien hinzufügen</p>
      </td>
      <td>Klicken Sie für jede Phase, der Sie Teilnehmer hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Phase ein.<p> Klicken Sie dann für jeden Teilnehmer, den Sie der Phase hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Teilnehmerdetails ein.</p>
      <ul>
      <li><b>Teilnehmer-ID</b><p>Geben Sie die ID des Teilnehmers ein oder mappen Sie sie.</p></li>
      <li><b>Teilnehmertyp</b><p>Wählen Sie aus, ob der Teilnehmer ein Benutzer oder ein Team ist.</p></li>
      <li><b>Teilnehmerrolle</b><p>Wählen Sie aus, ob der Teilnehmer eine genehmigende Person oder eine prüfende Person ist.</p></li>
      </ul> 
      </td> 
      </tr>
  </tbody>
</table>

#### Massenlöschvorlagen

Dieses Modul löscht die angegebenen Validierungsvorlagen.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Vorlagen-IDs</p></td>
      <td>Klicken Sie für jede Vorlage, die Sie löschen möchten, auf <b>Element hinzufügen</b> und geben Sie die Vorlagen-ID ein.</td> 
      </tr>
  </tbody>
</table>

#### Erstellen einer Vorlage

Dieses Aktionsmodul erstellt eine Validierungsvorlage

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Name</p></td>
      <td>Geben Sie einen Namen für die Vorlage ein oder mappen Sie ihn.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Unternehmens-ID</p></td>
      <td>Wenn Sie der Vorlage einen Unternehmensbereich hinzufügen möchten, geben Sie die Unternehmens-ID ein oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Schritte</p>
      </td>
      <td>Klicken Sie für jeden Schritt, den Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Daten für den Schritt ein.<p>Weitere Informationen finden Sie unter <a href="#stages-fields" class="MCXref xref" >Stadienfelder</a> in diesem Artikel. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Freigegeben für</p></td>
      <td>Klicken Sie für jeden Benutzer, für den Sie die Vorlage freigeben möchten, auf <b>Element hinzufügen</b> und Benutzer-ID sowie auf die gewünschte Zugriffsebene.</td> 
      </tr>
  </tbody>
</table>

#### Gruppierte Validierung erstellen

Dieses Aktionsmodul erstellt eine gruppierte Genehmigung: eine Reihe von Dokumentversionen, die sich gemeinsam über einen oder mehrere Genehmigungspfade bewegen und jeweils eine geordnete Abfolge von Phasen mit eigenen Teilnehmern aufweisen.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Name</p></td>
      <td>Einen Anzeigenamen für die gruppierte Genehmigung eingeben oder zuordnen. Der Name muss zwischen 1 und 255 Zeichen lang sein.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Assets</p></td>
      <td>Klicken Sie für jede Dokumentversion, die Sie in die Gruppe aufnehmen möchten, auf <b>Element hinzufügen</b> und geben Sie die Dokumentversions-ID (DOCV) ein.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Pfade</p></td>
      <td>Klicken Sie für jeden Genehmigungspfad, den Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Pfad-ID, den Namen und die Stadien ein. Jeder Pfad enthält eine geordnete Sequenz von Phasen. Klicken Sie für jede Phase im Feld Phasen auf <b>Element hinzufügen</b> und geben Sie die folgenden Daten ein:
      <ul>
      <li><b>Stadien-ID</b><p>Geben Sie eine vom Client zugewiesene Kennung für das Stadium ein, die über alle Pfade hinweg eindeutig ist. Muss alphanumerisch sein, wobei Unterstriche oder Bindestriche zulässig sind und höchstens 64 Zeichen enthalten sein dürfen.</p></li>
      <li><b>Name der Phase</b><p>Geben Sie einen Namen für die Phase ein oder mappen Sie ihn.</p></li>
      <li><b>IDs des übergeordneten Stadiums</b><p>Klicken Sie für jedes übergeordnete Stadium, das Sie dem Stadium hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die übergeordnete ID ein.</p></li>
      <li><b>Teilnehmende</b><p>Klicken Sie für jeden Teilnehmer, den Sie der Phase hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Teilnehmerdetails ein.
      <ul>
      <li><b>Teilnehmer-ID</b><p>Geben Sie die ID des Teilnehmers ein oder mappen Sie sie.</p></li>
      <li><b>Teilnehmertyp</b><p>Wählen Sie aus, ob der Teilnehmer ein Benutzer oder ein Team ist.</p></li>
      <li><b>Teilnehmerrolle</b><p>Wählen Sie aus, ob der Teilnehmer eine genehmigende Person oder eine prüfende Person ist.</p></li>
      </ul>
      </p></li>
      <li><b>Deadline Date</b><p>Wenn die Frist ein bestimmtes Datum ist, geben Sie das Datum ein oder ordnen Sie es zu.</p></li>
      <li><b>Werktage bis Fristablauf</b><p>Wenn der Termin nach einer bestimmten Anzahl von Werktagen liegt, geben Sie die Anzahl der Tage ein oder mappen Sie sie.</p></li>
      <li><b>Deadline Time: Stunden</b><p>Geben Sie die Stunde des Tages für den Fristablauf ein (0-23) oder mappen Sie sie. Paar mit Deadline Time: Minutes.</p></li>
      <li><b>Deadline Time: Minuten</b><p>Geben Sie die Minute der Stunde für die Frist (0-59) ein oder mappen Sie sie. Paar mit Deadline Time: Hours.</p></li>
      <li><b>Benutzerdefinierte Nachricht</b><p>Geben Sie eine benutzerdefinierte Nachricht für das Stadium ein oder ordnen Sie sie zu.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Übergeordnete Objekt-ID</p></td>
      <td>Geben Sie die ID des übergeordneten Workfront-Objekts (z. B. eines Projekts oder einer Aufgabe) ein, das bzw. die Sie mit der gruppierten Genehmigung verknüpfen möchten, oder ordnen Sie sie zu. Wenn Sie dieses Feld verwenden, müssen Sie auch den Objektcode eingeben.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Objekt-Code</p></td>
      <td>Geben Sie den Workfront-Objekttyp-Code für das übergeordnete Objekt ein (z. B. <code>PROJ</code> oder <code>TASK</code>) oder ordnen Sie ihn zu. Erforderlich, wenn Sie eine ID des übergeordneten Objekts eingeben.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Vorlagen-ID</p></td>
      <td>(Optional) Geben Sie eine Vorlagen-ID ein, um die gruppierte Validierung zur Rückverfolgbarkeit aufzuzeichnen, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Beschränkungen</p></td>
      <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

#### Stadien erstellen

Dieses Aktionsmodul erstellt eine Genehmigung mit den angegebenen Stufendaten.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Assets ein, für das Sie einen Schritt erstellen oder aktualisieren möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Schritte</p>
      </td>
      <td>Klicken Sie für jeden Schritt, den Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Daten für den Schritt ein.<p>Weitere Informationen finden Sie unter <a href="#stages-fields" class="MCXref xref" >Stadienfelder</a> in diesem Artikel. </p> </td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>Vorlagen-ID</p></td>
      <td>Geben Sie die ID des Assets ein, für das Sie Stadien erstellen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
  </tbody>
</table>

<!--
BECKY CHECK ME: The following block of Delete-prefixed Actions modules (Delete a decision on a stage, Delete a stage, Delete a template, Delete an approval, Delete decisions, Delete grouped approval, Delete participants) is not confirmed to be current in the live connector as of this update - status uncertain. Commented out for now; restore (and remove this comment) once confirmed, or delete for good if confirmed removed.

#### Delete a decision on a stage

This module removes the current user's decision from the specified stage. The current user is the user whose credentials are used in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a decision from.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stage ID</p></td>
      <td>Enter or map the ID of the stage that you want to delete.</td> 
      </tr>
   </tbody>
</table>


#### Delete a stage

This action module deletes the specified stage from the approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a stage from.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stage ID</p></td>
      <td>Enter or map the ID of the stage that you want to delete.</td> 
      </tr>
  </tbody>
</table>

#### Delete a template

This module deletes the specified approval template.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Template ID</p></td>
      <td>Enter or map the ID of the template that you want to delete.</td> 
      </tr>
  </tbody>
</table>

#### Delete an approval

This action module deletes the approval for the given document.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete an approval from.</td> 
      </tr>
  </tbody>
</table>

#### Delete decisions

This module removes the current user's decision from the specified stage. The current user is the user whose credentials are used in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a decision from.</td> 
      </tr>
  </tbody>
</table>

#### Delete grouped approval

This action module deletes a grouped approval, cascading to its child asset approvals and paths.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Group GUID</p></td>
      <td>Enter or map the GUID of the grouped approval that you want to delete.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limit</p></td>
      <td>Enter or map the maximum number of results you want the module to work with during each scenario execution cycle.</td> 
      </tr>
  </tbody>
</table>

#### Delete participants

This action module deletes participants from an approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to delete participants from.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant type</p>
      </td>
      <td>Select whether the participants is a user or a team.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant ID</p>
      </td>
      <td>Enter or map the ID of the participant.</td> 
      </tr>
  </tbody>
</table>
-->

#### Stadium sperren

Dieses Aktionsmodul sperrt die angegebene Genehmigungsphase und setzt die Phase auf „Inaktiv“.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Assets ein, das Sie sperren möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Stadien-ID</p>
      </td>
      <td>Geben Sie die ID der Phase ein, die Sie sperren möchten, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

#### Entscheidung treffen

Dieses Aktionsmodul wendet eine Entscheidung auf eine Genehmigungs- oder Genehmigungsphase an.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Assets ein, das Sie sperren möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Entscheidung</p></td>
      <td>Wählen Sie die Entscheidung aus, die auf die Genehmigung oder Phase angewendet werden soll.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Stadien-IDs</p>
      </td>
      <td>Klicken Sie für jedes Stadium, auf das Sie die Entscheidung anwenden möchten, auf <b>Element hinzufügen</b> und geben Sie die Stadien-ID ein.</td> 
      </tr>
  </tbody>
</table>

#### Etappenentscheidung treffen

Dieses Modul wendet eine Entscheidung auf die angegebene Stufe an.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Dokuments ein, über das Sie eine Entscheidung treffen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stadien-ID</p></td>
      <td>Geben Sie die ID der Phase ein, für die Sie eine Entscheidung treffen möchten, oder mappen Sie sie.</td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Entscheidung</p></td>
      <td>Wählen Sie die Entscheidung aus, die Sie auf diese Phase anwenden möchten.</td> 
      </tr>
  </tbody>
</table>

#### Verwalten von Assets für eine gruppierte Genehmigung

Dieses Aktionsmodul fügt Dokumentversionen zu einer gruppierten Genehmigung hinzu bzw. entfernt diese.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Gruppierte Genehmigungs-ID</p></td>
      <td>Geben Sie die GUID der gruppierten Genehmigung ein, für die Sie Assets verwalten möchten, oder mappen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Assets hinzufügen</p></td>
      <td>Klicken Sie für jede Dokumentversion, die Sie der Gruppe hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Dokumentversions-ID (DOCV) ein.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Assets entfernen</p></td>
      <td>Klicken Sie für jede Dokumentversion, die Sie aus der Gruppe entfernen möchten, auf <b>Element hinzufügen</b> und geben Sie die Dokumentversions-ID (DOCV) ein.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Beschränkungen</p></td>
      <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

#### Stadiumsteilnehmer verwalten

Dieses Aktionsmodul fügt Teilnehmer in einem bestimmten Schritt einer gruppierten Genehmigung hinzu, aktualisiert und/oder entfernt sie.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Gruppierte Genehmigungs-ID</p></td>
      <td>Geben Sie die GUID der gruppierten Genehmigung ein oder mappen Sie sie.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stadien-ID</p></td>
      <td>Geben Sie die ID der Phase ein, für die Sie Teilnehmer verwalten möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Add Participants</p></td>
      <td>Klicken Sie für jeden Teilnehmer, den Sie der Phase hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die folgenden Details ein:
      <ul>
      <li><b>Teilnehmertyp</b><p>Wählen Sie aus, ob der Teilnehmer ein Benutzer oder ein Team ist.</p></li>
      <li><b>Teilnehmende/r</b><p>Geben Sie die ID des Teilnehmers ein oder mappen Sie sie.</p></li>
      <li><b>Rolle</b><p>Wählen Sie aus, ob der Teilnehmer eine genehmigende Person oder eine prüfende Person ist.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Teilnehmer aktualisieren</p></td>
      <td>Klicken Sie für jeden Teilnehmer, den Sie auf der Bühne aktualisieren möchten, auf <b>Element hinzufügen</b> und geben Sie die folgenden Details ein:
      <ul>
      <li><b>Teilnehmertyp</b><p>Wählen Sie aus, ob der Teilnehmer ein Benutzer oder ein Team ist.</p></li>
      <li><b>Teilnehmende/r</b><p>Geben Sie die ID des Teilnehmers ein oder mappen Sie sie.</p></li>
      <li><b>Rolle</b><p>Wählen Sie aus, ob der Teilnehmer eine genehmigende Person oder eine prüfende Person ist.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Teilnehmer entfernen</p></td>
      <td>Klicken Sie für jeden Teilnehmer, den Sie aus der Phase entfernen möchten, auf <b>Element hinzufügen</b> und geben Sie die folgenden Details ein:
      <ul>
      <li><b>Teilnehmertyp</b><p>Wählen Sie aus, ob der Teilnehmer ein Benutzer oder ein Team ist.</p></li>
      <li><b>Teilnehmende/r</b><p>Geben Sie die ID des Teilnehmers ein oder mappen Sie sie.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Beschränkungen</p></td>
      <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

#### Stadien einer gruppierten Genehmigung verwalten

Dieses Aktionsmodul fügt Phasen einer gruppierten Genehmigung hinzu, aktualisiert und/oder entfernt sie.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Gruppierte Genehmigungs-ID</p></td>
      <td>Geben Sie die GUID der gruppierten Genehmigung ein oder mappen Sie sie.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stadien hinzufügen</p></td>
      <td>Klicken Sie für jedes Stadium, das Sie hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie die folgenden Details ein:
      <ul>
      <li><b>Stadien-ID</b><p>Geben Sie eine Kennung für die Phase ein oder ordnen Sie sie zu.</p></li>
      <li><b>Name der Phase</b><p>Geben Sie einen Namen für die Phase ein oder mappen Sie ihn.</p></li>
      <li><b>Deadline Date</b><p>Wenn die Frist ein bestimmtes Datum ist, geben Sie das Datum ein oder ordnen Sie es zu.</p></li>
      <li><b>Werktage bis Fristablauf</b><p>Wenn der Termin nach einer bestimmten Anzahl von Werktagen liegt, geben Sie die Anzahl der Tage ein oder mappen Sie sie.</p></li>
      <li><b>Benutzerdefinierte Nachricht</b><p>Geben Sie eine benutzerdefinierte Nachricht für das Stadium ein oder ordnen Sie sie zu.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stadien aktualisieren</p></td>
      <td>Klicken Sie für jede Phase, die Sie aktualisieren möchten, auf <b>Element hinzufügen</b> und geben Sie die folgenden Details ein:
      <ul>
      <li><b>Stadien-ID</b><p>Geben Sie die ID der Phase ein, die Sie aktualisieren möchten, oder mappen Sie sie.</p></li>
      <li><b>Name der Phase</b><p>Geben Sie einen Namen für die Phase ein oder mappen Sie ihn.</p></li>
      <li><b>Deadline Date</b><p>Wenn die Frist ein bestimmtes Datum ist, geben Sie das Datum ein oder ordnen Sie es zu.</p></li>
      <li><b>Werktage bis Fristablauf</b><p>Wenn der Termin nach einer bestimmten Anzahl von Werktagen liegt, geben Sie die Anzahl der Tage ein oder mappen Sie sie.</p></li>
      <li><b>Benutzerdefinierte Nachricht</b><p>Geben Sie eine benutzerdefinierte Nachricht für das Stadium ein oder ordnen Sie sie zu.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stadien entfernen</p></td>
      <td>Klicken Sie für jedes Stadium, das Sie entfernen möchten, auf <b>Element hinzufügen</b> und geben Sie die Stadien-ID ein.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Beschränkungen</p></td>
      <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

#### Erinnern eines Teilnehmers an einer Bühne

Dieses Modul sendet eine Erinnerung an einen bestimmten Teilnehmer in einer bestimmten Phase.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Assets ein, für das Sie eine Erinnerung senden möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Stadien-ID</p>
      </td>
      <td>Geben Sie die ID des Stadiums ein, für das Sie eine Erinnerung senden möchten, oder ordnen Sie sie zu.</td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>Teilnehmer-ID</p></td>
      <td>Geben Sie die ID des Teilnehmers ein, an den Sie eine Erinnerung senden möchten, oder ordnen Sie sie zu.</td> 
      </tr>
  </tbody>
</table>

#### Teilnehmer erinnern

Dieses Modul sendet eine Erinnerungsnachricht an den angegebenen Teilnehmer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Assets ein, für das Sie eine Erinnerung senden möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Teilnehmer-ID</p>
      </td>
      <td>Geben Sie die ID des Teilnehmers ein, an den Sie eine Erinnerung senden möchten, oder ordnen Sie sie zu.</td> 
      </tr>
      <tr>
      <td role="rowheader">
        <p>Teilnehmertyp</p>
      </td>
      <td>Geben Sie den Typ des Teilnehmers ein, an den Sie eine Erinnerung senden möchten, oder ordnen Sie ihn zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Teilnehmerrolle</p>
      </td>
      <td>Geben Sie die Rolle des Teilnehmers ein, an den Sie eine Erinnerung senden möchten, oder ordnen Sie sie zu.</td> 
      </tr>
  </tbody>
</table>

#### Unentschlossene Teilnehmende erinnern

Dieses Modul sendet Erinnerungsbenachrichtigungen an alle unentschlossenen Teilnehmer bei der angegebenen Genehmigung.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Assets ein, für das Sie eine Erinnerung senden möchten, oder ordnen Sie sie zu.</td> 
      </tr>
  </tbody>
</table>

#### Unentschlossene Teilnehmer auf einer Bühne erinnern

Dieses Modul sendet Erinnerungsnachrichten an alle unentschlossenen Teilnehmer einer Bühne.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Assets ein, für das Sie eine Erinnerung senden möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Stadien-ID</p>
      </td>
      <td>Geben Sie die ID des Stadiums ein, für das Sie eine Erinnerung senden möchten, oder ordnen Sie sie zu.</td> 
      </tr>
  </tbody>
</table>

#### Phase entsperren

Dieses Aktionsmodul entsperrt die angegebene Genehmigungsphase und setzt die Phase auf „aktiv“.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Assets ein, das Sie entsperren möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Stadien-ID</p>
      </td>
      <td>Geben Sie die ID der Phase ein, die Sie sperren möchten, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>


#### Aktualisierungsschritt

Dieses Aktionsmodul aktualisiert Felder in der angegebenen Phase.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Dokuments ein, über das Sie eine Entscheidung treffen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stadien-ID</p></td>
      <td>Geben Sie die ID der Phase ein, für die Sie eine Entscheidung treffen möchten, oder mappen Sie sie.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Name der Phase</p></td>
      <td>Geben Sie einen Namen für die Vorlage ein oder mappen Sie ihn.</td> 
      </tr>
      <td role="rowheader">
        <p>Andere Felder</p>
      </td>
      <td>Geben Sie Daten in die Felder des Schritts ein.<p>Weitere Informationen finden Sie unter <a href="#stages-fields" class="MCXref xref" >Stadienfelder</a> in diesem Artikel. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Freigegeben für</p></td>
      <td>Klicken Sie für jeden Benutzer, für den Sie die Vorlage freigeben möchten, auf <b>Element hinzufügen</b> und Benutzer-ID sowie auf die gewünschte Zugriffsebene.</td> 
      </tr>
  </tbody>
</table>

#### Aktualisieren einer Vorlage

Dieses Modul aktualisiert Felder in der angegebenen Validierungsvorlage.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Vorlagen-ID</p></td>
      <td>Geben Sie einen Namen für die Vorlage ein oder mappen Sie ihn.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Name</p></td>
      <td>Geben Sie die ID der Vorlage ein, die Sie aktualisieren möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Unternehmens-ID</p></td>
      <td>Wenn Sie der Vorlage einen Unternehmensbereich hinzufügen möchten, geben Sie die Unternehmens-ID ein oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Schritte</p>
      </td>
      <td>Klicken Sie für jeden Schritt, den Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Daten für den Schritt ein.<p>Weitere Informationen finden Sie unter <a href="#stages-fields" class="MCXref xref" >Stadienfelder</a> in diesem Artikel. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Freigegeben für</p></td>
      <td>Klicken Sie für jeden Benutzer, für den Sie die Vorlage freigeben möchten, auf <b>Element hinzufügen</b> und Benutzer-ID sowie auf die gewünschte Zugriffsebene.</td> 
      </tr>
  </tbody>
</table>

#### Alle Stadien aktualisieren

Dieses Modul ersetzt alle Phasen einer bestehenden Genehmigung durch die angegebenen Stufendaten. Das Dokument muss sich in einem bearbeitbaren Zustand befinden.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Assets ein, für das Sie Stadien aktualisieren möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Schritte</p>
      </td>
      <td>Klicken Sie für jedes Stadium, das Sie aktualisieren möchten, auf <b>Element hinzufügen</b> und geben Sie die Stadiendaten ein.<p>Weitere Informationen finden Sie unter <a href="#stages-fields" class="MCXref xref" >Stadienfelder</a> in diesem Artikel. </p> </td> 
      </tr>
  </tbody>
</table>

#### Gruppierte Genehmigung aktualisieren (voller Status)

Dieses Aktionsmodul führt eine vollständige Aktualisierung des Status für eine gruppierte Genehmigung durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Gruppierte Genehmigungs-ID</p></td>
      <td>Geben Sie die GUID der gruppierten Genehmigung, die Sie aktualisieren möchten, ein oder mappen Sie sie. Beispiel: <code>9f8b60820000462ecf66c409d1248fa9</code>.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Pfade</p></td>
      <td>Klicken Sie für jeden Genehmigungspfad, den Sie für die gruppierte Genehmigung verwenden möchten<b> auf „Element hinzufügen</b> und geben Sie die Pfad-ID, den Namen und die Phasen ein. Fusion gleicht dies mit dem aktuellen Status ab und fügt Pfade hinzu, aktualisiert sie und entfernt sie, sodass sie mit dem übereinstimmen, was Sie senden. Jeder Pfad enthält eine geordnete Sequenz von Phasen. Klicken Sie für jede Phase im Feld Phasen auf <b>Element hinzufügen</b> und geben Sie die folgenden Daten ein:
      <ul>
      <li><b>Stadien-ID</b><p>Geben Sie eine vom Client zugewiesene Kennung für das Stadium ein, die über alle Pfade hinweg eindeutig ist. Muss alphanumerisch sein, wobei Unterstriche oder Bindestriche zulässig sind und höchstens 64 Zeichen enthalten sein dürfen.</p></li>
      <li><b>Name der Phase</b><p>Geben Sie einen Namen für die Phase ein oder mappen Sie ihn.</p></li>
      <li><b>IDs des übergeordneten Stadiums</b><p>Klicken Sie für jedes übergeordnete Stadium, das Sie dem Stadium hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die übergeordnete ID ein.</p></li>
      <li><b>Teilnehmende</b><p>Klicken Sie für jeden Teilnehmer, den Sie der Phase hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Teilnehmerdetails ein.
      <ul>
      <li><b>Teilnehmer-ID</b><p>Geben Sie die ID des Teilnehmers ein oder mappen Sie sie.</p></li>
      <li><b>Teilnehmertyp</b><p>Wählen Sie aus, ob der Teilnehmer ein Benutzer oder ein Team ist.</p></li>
      <li><b>Teilnehmerrolle</b><p>Wählen Sie aus, ob der Teilnehmer eine genehmigende Person oder eine prüfende Person ist.</p></li>
      </ul>
      </p></li>
      <li><b>Deadline Date</b><p>Wenn die Frist ein bestimmtes Datum ist, geben Sie das Datum ein oder ordnen Sie es zu.</p></li>
      <li><b>Werktage bis Fristablauf</b><p>Wenn der Termin nach einer bestimmten Anzahl von Werktagen liegt, geben Sie die Anzahl der Tage ein oder mappen Sie sie.</p></li>
      <li><b>Deadline Time: Stunden</b><p>Geben Sie die Stunde des Tages für den Fristablauf ein (0-23) oder mappen Sie sie. Paar mit Deadline Time: Minutes.</p></li>
      <li><b>Deadline Time: Minuten</b><p>Geben Sie die Minute der Stunde für die Frist (0-59) ein oder mappen Sie sie. Paar mit Deadline Time: Hours.</p></li>
      <li><b>Benutzerdefinierte Nachricht</b><p>Geben Sie eine benutzerdefinierte Nachricht für das Stadium ein oder ordnen Sie sie zu.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Assets</p></td>
      <td>(Optional) Klicken Sie für jede Dokumentversion, die die Gruppe enthalten soll, auf <b>Element hinzufügen</b> und geben Sie die Dokumentversions-(DOCV-)ID ein. Wenn Sie dieses Feld auslassen, bleiben die aktuellen Assets unverändert.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Idempotenzschlüssel</p></td>
      <td>(Optional) Geben Sie einen vom Client bereitgestellten Schlüssel (maximal 128 Zeichen) ein, der eine erneute Anfrage sicher macht, oder ordnen Sie ihn zu. Wenn Sie denselben Schlüssel erneut senden, wendet das Modul die Aktualisierung kein zweites Mal an.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Beschränkungen</p></td>
      <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

### Suchvorgänge

* [Abrufen einer Vorlage](#get-a-template)
* [Genehmigungsdetails abrufen](#get-approval-details)
* [Abrufen von Genehmigungen in einer gruppierten Genehmigung](#get-approvals-in-a-grouped-approval)
* [Details zur gruppierten Genehmigung abrufen](#get-grouped-approval-details)
* [Mehrere Genehmigungen einholen](#get-multiple-approvals)
* [Empfohlene Genehmigungen einholen](#get-suggested-approvals)
* [Empfohlene Teilnehmer abrufen](#get-suggested-participants)
* [Bots auflisten](#list-bots)
* [Auflisten gruppierter Genehmigungen nach übergeordnetem Element](#list-grouped-approvals-by-parent)
* [Listenvorlagen](#list-templates)
* [Search AI Brand Reviews](#search-ai-brand-reviews)
* [Gruppierte Genehmigungen suchen](#search-grouped-approvals)


#### Abrufen einer Vorlage

Dieses Modul gibt die angegebene Validierungsvorlage zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Vorlagen-ID</p></td>
      <td>Geben Sie die ID des Dokuments ein, das Sie Teilnehmern vorschlagen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Maximale Anzahl an zurückgegebenen Vorlagen
         </td>
         <td>
              Geben Sie die maximale Anzahl von Vorlagen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie. 
         </td>
       </tr>
  </tbody>
</table>

#### Genehmigungsdetails abrufen

Dieses Suchmodul ruft Genehmigungsdetails für ein Asset ab.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Dokument</p>
      </td>
      <td>Geben Sie die ID des Assets ein, für das Sie Genehmigungsdetails abrufen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
  </tbody>
</table>

#### Abrufen von Genehmigungen in einer gruppierten Genehmigung

Dieses Suchmodul gibt die einzelnen Asset-Genehmigungen zurück, aus denen eine gruppierte Genehmigung besteht.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Gruppen-GUID</p></td>
      <td>Geben Sie die GUID der gruppierten Genehmigung ein, für die Sie Genehmigungen erhalten möchten, oder mappen Sie sie.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Dokumentversionsdaten</p></td>
      <td>Wählen Sie aus, ob der Datensatzdokument-Version von Redrock an jede Dokumentversionsgenehmigung (DOCV) angehängt werden soll. </td>
      </tr>
     <tr>
      <td role="rowheader"><p>Beschränkungen</p></td>
      <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

#### Details zur gruppierten Genehmigung abrufen

Dieses Suchmodul gibt eine gruppierte Validierung anhand der GUID zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Gruppen-GUID</p></td>
      <td>Geben Sie die GUID der gruppierten Genehmigung ein, für die Sie Details abrufen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Beschränkungen</p></td>
      <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

#### Mehrere Genehmigungen einholen

Dieses Modul ruft Details zu Validierungen für eine Liste von Dokumenten eines bestimmten Typs ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-IDs</p></td>
      <td>Klicken Sie für jedes Dokument, für das Sie Genehmigungsdetails abrufen möchten, auf <b>Element hinzufügen</b> und geben Sie die Dokument-ID ein.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Maximale Anzahl an zurückgegebenen Ergebnissen
         </td>
         <td>
              Geben Sie die maximale Anzahl von Ergebnissen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie. 
         </td>
       </tr>
  </tbody>
</table>

#### Empfohlene Genehmigungen einholen

Dieses Modul gibt vorgeschlagene Genehmigungs-Payloads aus früheren Dokumentversionen zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Dokuments ein, für das Sie vorgeschlagene Genehmigungen erhalten möchten, oder mappen Sie sie.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Maximale Anzahl an zurückgegebenen Genehmigungen
         </td>
         <td>
              Geben Sie die maximale Anzahl von Validierungen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie. 
         </td>
       </tr>
  </tbody>
</table>

#### Empfohlene Teilnehmer abrufen

Dieses Modul gibt Teilnehmervorschläge aus der Genehmigung für die vorherige Dokumentgenehmigung zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Dokument-ID</p></td>
      <td>Geben Sie die ID des Dokuments ein, das Sie Teilnehmern vorschlagen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Maximale Anzahl an zurückgegebenen Teilnehmern
         </td>
         <td>
              Geben Sie die maximale Anzahl an Teilnehmern ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie. 
         </td>
       </tr>
  </tbody>
</table>

#### Bots auflisten

Dieses Modul gibt eine paginierte Liste von Bot-Konten zurück.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Seite</p></td>
      <td>Geben Sie die Ergebnisseite ein, die Sie zurückgeben möchten, oder mappen Sie sie.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Maximale Anzahl an zurückgegebenen Ergebnissen
         </td>
         <td>
              Geben Sie die maximale Anzahl von Ergebnissen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie. 
         </td>
       </tr>
  </tbody>
</table>

#### Auflisten gruppierter Genehmigungen nach übergeordnetem Element

Dieses Suchmodul gibt die gruppierten Genehmigungen zurück, die mit einem übergeordneten Workfront-Objekt verknüpft sind.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID des übergeordneten Elements</p></td>
      <td>Geben Sie die ID des übergeordneten Workfront-Objekts (z. B. eines Projekts oder einer Aufgabe) ein, für das Sie gruppierte Genehmigungen erhalten möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Objektcode</p></td>
      <td>(Optional) Geben Sie den Workfront-Objekttyp-Code für das übergeordnete Objekt ein (z. B. <code>PROJ</code> oder <code>TASK</code>) oder ordnen Sie ihn zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Beschränkungen</p></td>
      <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

#### Listenvorlagen

Dieses Modul gibt eine Liste aller Validierungsvorlagen zurück, die dem aktuellen Benutzer zur Verfügung stehen. Der aktuelle Benutzer ist der Benutzer, dessen Anmeldeinformationen in der in diesem Modul verwendeten Verbindung verwendet werden.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
   </tbody>
</table>

#### Search AI Brand Reviews

Dieses Modul gibt die Ergebnisse einer KI-Markenüberprüfung zurück, die im Rahmen einer Genehmigung für eine Dokumentversion erstellt wurden.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Bot-Benutzer-ID</p></td>
      <td>Geben Sie die Benutzer-ID des Bots ein, nach dem Sie Überprüfungen suchen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID des übergeordneten Dokuments</p></td>
      <td>Geben Sie die ID des übergeordneten Dokuments ein, nach dem Sie Überprüfungen suchen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Dokumentversions-ID</p></td>
      <td>Geben Sie die ID des Assets ein, für das Sie eine Erinnerung senden möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stadien-ID</p></td>
      <td>Geben Sie eine Stadien-ID ein oder ordnen Sie sie zu, um die Ergebnisse auf einen bestimmten Genehmigungsprozess zu beschränken.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Seite</p></td>
      <td>Geben Sie eine Seitenzahl ein oder ordnen Sie sie zu, um die Ergebnisse auf diese Seite zu beschränken.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Maximale Anzahl an zurückgegebenen Reviews
         </td>
         <td>
              Geben Sie die maximale Anzahl an Überprüfungen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie. 
         </td>
       </tr>
  </tbody>
</table>

#### Gruppierte Genehmigungen suchen

Dieses Suchmodul durchsucht gruppierte Genehmigungen anhand einer benannten Ansicht.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Ansicht</p></td>
      <td>(Optional) Wählen Sie die benannte Ansicht aus, die die Form der Antwort bestimmt, oder ordnen Sie sie zu. Derzeit werden nur ausstehende Genehmigungen unterstützt.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Beschränkungen</p></td>
      <td>(Optional) Geben Sie die Seitengröße für die erste Ergebnisseite ein oder ordnen Sie sie zu. Der Maximalwert ist 100, und der Standardwert ist 20.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Cursor</p></td>
      <td>(Optional) Geben Sie den undurchsichtigen Cursor aus einer vorherigen Antwort ein oder ordnen Sie ihn zu, um die nächste Ergebnisseite abzurufen. Wenn Sie einen Cursor angeben, ignoriert das Modul das Feld Limit .</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Team-IDs</p></td>
      <td>(Optional) Klicken Sie für jedes Team, das Sie auch mit gruppierten Genehmigungen abgleichen möchten (wobei das Team ein Teilnehmer ist), auf <b>Element hinzufügen</b> und geben Sie die Team-ID ein.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Beschränkungen</p></td>
      <td>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

<!-- BECKY CHECK ME: the screenshot shows two separate fields both labeled "Limit" - an optional pagination page-size field (max 100, default 20, ignored if Cursor is set) and a required general execution-cycle limit, matching the Limit field used in every other module in this article. Confirm this isn't a UI labeling issue before publishing, and that both rows are needed/correctly distinguished. -->

### Sonstiges

* [Benutzerdefinierten API-Aufruf erstellen](#make-a-custom-api-call)
* [Felder für Stadien](#stages-fields)


#### Benutzerdefinierten API-Aufruf erstellen

Dieses Modul führt einen benutzerdefinierten API-Aufruf an die Adobe Workfront Unified Review and Approvals API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Relativer Pfad</p>
      </td>
      <td>
        <p>Geben Sie einen Pfad relativ zu <code>https://workfront.adobe.io</code> ein. Beispiel: <code>/unified-approvals/public/api/v1/approvals/&lt;ASSET_TYPE&gt;/&lt;ASSET_ID&gt;</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Methode</p>
      </td>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">Header</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion fügt automatisch Autorisierungs-Header hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Abfragezeichenfolge]  </td>
      <td>
        <p>Klicken Sie für jedes Schlüssel/Wert-Paar, das Sie der Abfragezeichenfolge hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Schlüssel und den Wert ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Text]</td>
   <td> <p>Fügen Sie den Textinhalt für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrem JSON-Objekt verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>



#### Felder für Stadien

Die folgenden Felder sind bei der Konfiguration von Phasen verfügbar. Möglicherweise sind nicht alle Felder für alle Module verfügbar.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Name der Phase</td>
      <td>Geben Sie einen Namen für die Phase ein oder mappen Sie ihn.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Deadline date</p></td>
      <td>Wenn die Frist ein bestimmtes Datum ist, geben Sie das Datum ein oder ordnen Sie es zu.</td> 
      </tr>
  </tbody>
     <tr>
      <td role="rowheader"><p>Frist Werktage</p></td>
      <td>Wenn der Termin nach einer bestimmten Anzahl von Werktagen liegt, geben Sie die Anzahl der Tage ein oder mappen Sie sie.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Deadline Time</p></td>
      <td>Wenn die Frist eine bestimmte Zeit ist, geben Sie die Zeit ein oder mappen Sie sie.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Teilnehmende</p></td>
      <td>Klicken Sie für jeden Teilnehmer, den Sie der Phase hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Teilnehmerdetails ein.      
      <ul>
      <li><b>Teilnehmer-ID</b><p>Geben Sie die ID des Teilnehmers ein oder mappen Sie sie.</p></li>
      <li><b>Teilnehmertyp</b><p>Wählen Sie aus, ob der Teilnehmer ein Benutzer oder ein Team ist.</p></li>
      <li><b>Teilnehmerrolle</b><p>Wählen Sie aus, ob der Teilnehmer eine genehmigende Person oder eine prüfende Person ist.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Automatische Sperre aktiviert</p></td>
      <td>Geben Sie an, ob das Stadium automatisch gesperrt werden soll.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Entscheidungsregeln</p></td>
      <td>Wählen Sie aus, ob nur eine Entscheidung für das Stadium erforderlich sein soll.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>IDs des übergeordneten Stadiums/IDs des übergeordneten Stadiums</p></td>
      <td>Klicken Sie für jedes übergeordnete Stadium, das Sie dem Stadium hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die übergeordnete ID ein.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Auslöser</p></td>
      <td>Um einen Trigger für diese Genehmigungsphase zu konfigurieren, klicken Sie auf <b>Element hinzufügen</b> und geben Sie die Details des Triggers ein.      <ul>
      <li><b>Typ</b><p>Wählen Sie <b>Aktivierung</b> aus</p></li>
      <li><b>Wenn</b><p>Wählen Sie aus, ob der Trigger bei der Erstellung der Genehmigung oder nach Abschluss eines anderen Schritts ausgeführt werden soll.</p></li>
      <li><b>Schritte</b><p>Klicken Sie für jedes Stadium, das Sie dem Trigger hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Stadien-ID ein oder mappen Sie sie.</p></li>
      <li><b>Entscheidungen</b><p>Klicken Sie für jede Entscheidung, die Sie dem Trigger hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Entscheidung ein oder ordnen Sie sie zu.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Benutzerdefinierte Nachricht</p></td>
      <td>Geben Sie eine benutzerdefinierte Nachricht für das Stadium ein oder ordnen Sie sie zu.</td> 
      </tr>
</table>
