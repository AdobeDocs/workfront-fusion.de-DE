---
title: Adobe Workfront-Module für Inhalte und Genehmigungen
description: Mit den Adobe Workfront-Modulen für Inhalte und Genehmigungen können Sie Genehmigungsdetails abrufen, eine Entscheidung über ein Asset treffen, Genehmigungsteilnehmer hinzufügen oder löschen, Genehmigungsphasen hinzufügen oder aktualisieren, Phasen sperren oder entsperren und benutzerdefinierte API-Aufrufe durchführen.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: e9ea91840c9be594e98b97202cb46dfa009349a9
workflow-type: tm+mt
source-wordcount: 3743
ht-degree: 15%

---

# Einheitliche Prüfungs- und Genehmigungsmodule für Adobe Workfront

Mit den Modulen Adobe Workfront Unified Review and Approvals können Sie Genehmigungsdetails abrufen, eine Entscheidung über ein Asset treffen, Genehmigungsteilnehmer hinzufügen oder löschen, Genehmigungsphasen hinzufügen oder aktualisieren, Phasen sperren oder entsperren und benutzerdefinierte API-Aufrufe durchführen.

Informationen zu einheitlichen Workfront-Überprüfungen und -Genehmigungen finden Sie unter [Einheitliche Überprüfung und Genehmigung - Übersicht](https://experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/document-approvals-overview) in der Dokumentation zu Workfront.

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

1. Klicken Sie auf **[!UICONTROL Continue]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

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
* [Erstellen einer Genehmigung](#create-an-approval)
* [Stadien erstellen](#create-stages)
* [Löschen einer Entscheidung in einem Stadium](#delete-a-decision-on-a-stage)
* [Löschen eines Stadiums](#delete-a-stage)
* [Löschen einer Vorlage](#delete-a-template)
* [Löschen einer Genehmigung](#delete-an-approval)
* [Entscheidungen löschen](#delete-decisions)
* [Teilnehmer löschen](#delete-participants)
* [Stadium sperren](#lock-a-stage)
* [Entscheidung treffen](#make-a-decision)
* [Etappenentscheidung treffen](#make-a-decision-on-a-stage)
* [Erinnern eines Teilnehmers an einer Bühne](#remind-a-participant-on-a-stage)
* [Teilnehmer erinnern](#remind-participant)
* [Unentschlossene Teilnehmende erinnern](#remind-undecided-participants)
* [Unentschlossene Teilnehmer auf einer Bühne erinnern](#remind-undecided-participants-on-a-stage)
* [Phase entsperren](#unlock-a-stage)
* [Aktualisierungsschritt](#update-a-stage)
* [Aktualisieren einer Vorlage](#update-a-template)
* [Alle Stadien aktualisieren](#update-all-stages)


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
      <td role="rowheader"><p>Firmen ID</p></td>
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

#### Erstellen einer Genehmigung

Dieses Aktionsmodul erstellt eine Genehmigung für ein Dokument im Adobe Cloud-Speicher, einschließlich Staging-Daten oder einer Vorlage.

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
      <td>Geben Sie die ID des Assets ein, für das Sie eine Genehmigung erstellen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Schritte</p>
      </td>
      <td>Klicken Sie für jeden Schritt, den Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Daten für den Schritt ein.<p>Weitere Informationen finden Sie unter <a href="#stages-fields" class="MCXref xref" >Stadienfelder</a> in diesem Artikel. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Vorlagen ID</p></td>
      <td>Geben Sie die ID der Vorlage ein, die Sie für diese Genehmigung verwenden möchten, oder ordnen Sie sie zu.</td> 
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
      <td role="rowheader"><p>Vorlagen ID</p></td>
      <td>Geben Sie die ID des Assets ein, für das Sie Stadien erstellen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
  </tbody>
</table>

#### Löschen einer Entscheidung in einem Stadium

Dieses Modul entfernt die Entscheidung des aktuellen Benutzers aus dem angegebenen Stadium. Der aktuelle Benutzer ist der Benutzer, dessen Anmeldeinformationen in der in diesem Modul verwendeten Verbindung verwendet werden.

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
      <td>Geben Sie die ID des Dokuments ein, aus dem Sie eine Entscheidung löschen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stadien-ID</p></td>
      <td>Geben Sie die ID des Schritts ein, den Sie löschen möchten, oder mappen Sie sie.</td> 
      </tr>
   </tbody>
</table>


#### Löschen eines Stadiums

Dieses Aktionsmodul löscht den angegebenen Schritt aus der Validierung.

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
      <td>Geben Sie die ID des Dokuments ein, aus dem Sie einen Schritt löschen möchten, oder mappen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stadien-ID</p></td>
      <td>Geben Sie die ID des Schritts ein, den Sie löschen möchten, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

#### Löschen einer Vorlage

Dieses Modul löscht die angegebene Validierungsvorlage.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen finden Sie unter <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Verbindung mit einheitlichen Adobe Workfront-Überprüfungen und -Genehmigungen</a> in diesem Artikel.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Vorlagen ID</p></td>
      <td>Geben Sie die ID der Vorlage ein, die Sie löschen möchten, oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

#### Löschen einer Genehmigung

Dieses Aktionsmodul löscht die Genehmigung für das angegebene Dokument.

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
      <td>Geben Sie die ID des Dokuments ein, aus dem Sie eine Genehmigung löschen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
  </tbody>
</table>

#### Entscheidungen löschen

Dieses Modul entfernt die Entscheidung des aktuellen Benutzers aus dem angegebenen Stadium. Der aktuelle Benutzer ist der Benutzer, dessen Anmeldeinformationen in der in diesem Modul verwendeten Verbindung verwendet werden.

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
      <td>Geben Sie die ID des Dokuments ein, aus dem Sie eine Entscheidung löschen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
  </tbody>
</table>

#### Teilnehmer löschen

Dieses Aktionsmodul löscht Teilnehmer aus einer Validierung.

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
      <td>Geben Sie die ID des Assets ein, aus dem Sie Teilnehmer löschen möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Teilnehmertyp</p>
      </td>
      <td>Wählen Sie aus, ob die Teilnehmer Benutzer oder Teams sind.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Teilnehmer-ID</p>
      </td>
      <td>Geben Sie die ID des Teilnehmers ein oder mappen Sie sie.</td> 
      </tr>
  </tbody>
</table>

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
      <td role="rowheader"><p>Vorlagen ID</p></td>
      <td>Geben Sie einen Namen für die Vorlage ein oder mappen Sie ihn.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Name</p></td>
      <td>Geben Sie die ID der Vorlage ein, die Sie aktualisieren möchten, oder ordnen Sie sie zu.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Firmen ID</p></td>
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

### Suchvorgänge

* [Abrufen einer Vorlage](#get-a-template)
* [Genehmigungsdetails abrufen](#get-approval-details)
* [Mehrere Genehmigungen einholen](#get-multiple-approvals)
* [Empfohlene Genehmigungen einholen](#get-suggested-approvals)
* [Empfohlene Teilnehmer abrufen](#get-suggested-participants)
* [Bots auflisten](#list-bots)
* [Listenvorlagen](#list-templates)
* [Suche nach KI-Markenvalidierern](#search-ai-brand-reviews)


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
      <td role="rowheader"><p>Vorlagen ID</p></td>
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

#### Auflisten von Bots

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

