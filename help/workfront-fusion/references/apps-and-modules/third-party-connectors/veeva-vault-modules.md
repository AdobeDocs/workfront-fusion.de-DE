---
title: Veeva Vault-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Veeva Vault verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 2ef967b6-0a69-4801-8574-5f17c9ce991d
source-git-commit: d64d894cfb0e1905c135cdf5ea39f11cd7a6e5f2
workflow-type: tm+mt
source-wordcount: '4125'
ht-degree: 13%

---

# Veeva Vault-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Veeva Vault verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um Veeva Vault-Module verwenden zu können, benötigen Sie ein Veeva Vault-Konto.

## Verbinden von Veeva Vault mit Workfront Fusion

Sie können direkt aus einem Veeva Vault-Modul heraus eine Verbindung zu Ihrem Veeva Vault-Konto herstellen.

Beim Erstellen einer Verbindung können Sie auswählen, ob ein Kennwort oder eine OAuth2-Authentifizierung verwendet werden soll.

### Verbinden von mit Veeva Vault mithilfe eines Benutzernamens und Kennworts

1. Klicken Sie in einem beliebigen Veeva Vault-Modul **Hinzufügen** neben dem Feld Verbindung .
1. Wählen Sie im Feld **Verbindungstyp** die Option `Veeva Username Password`.
1. Füllen Sie die folgenden Felder aus.

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">Verbindungsname</td> 
       <td> <p>Geben Sie einen Namen für die Verbindung ein.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">Benutzername</td>
        <td>
          <p>Geben Sie den Benutzernamen für das Veeva Vault-Konto ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Kennwort</td>
        <td>
          <p>Geben Sie das Passwort für das Veeva Vault-Konto ein.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">Vault-DNS</td> 
       <td>Geben Sie Ihr Veeva Vault-DNS (Domain-Name) ein.</p><p>Um Ihr Veeva Vault-DNS zu finden, überprüfen Sie die URL, die Sie für den Zugriff auf Veeva Vault verwenden.</p>Im URL-<code>https://my-dns.veevavault.com</code> wird beispielsweise der DNS <code>my-dns</code>. Sie müssen nicht die gesamte URL eingeben.</td> 
      </tr> 
     </tbody> 
    </table>

1. Klicken Sie auf **[!UICONTROL Fortsetzen]**, um die Verbindung zu erstellen und zum Modul zurückzukehren.

### Verbinden mit Veeva Vault mithilfe der OAuth2-Authentifizierung

1. Klicken Sie in einem beliebigen Veeva Vault-Modul **Hinzufügen** neben dem Feld Verbindung .
1. Wählen Sie im Feld **Verbindungstyp** die Option `Veeva Oauth 2`.
1. Füllen Sie die folgenden Felder aus.

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">Verbindungsname</td> 
       <td> <p>Geben Sie einen Namen für die Verbindung ein.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader">Autorisierungsserveranbieter</td> 
       <td> <p>Wählen Sie den Anbieter aus, den Sie für diese Authentifizierung verwenden möchten.</p> 
       <p><b>HINWEIS:</b> Der Veeva Vault verwendet Azure AD-Client-Anmeldeinformationen, wenn Azure als Autorisierungs-Server-Anbieter ausgewählt wird.</p>
       </td> 
      </tr> 
      <tr> 
       <td role="rowheader">Ping-Host</td> 
       <td> <p>Wenn Sie PingFederate verwenden, geben Sie den Ping-Host ein.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">Umfang</td>
        <td>
          <p>Geben Sie den Bereich für diese Verbindung ein. Der Bereich muss wie <code>{Application ID URI}/.default</code> formatiert sein. Der Anwendungs-ID-URI muss zu der Ressource oder dem Programm gehören, die bzw. das die Berechtigungen bereitstellt.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Mandantenkennung</td>
        <td>
          <p>Wenn Sie die Azure AD/Microsoft Entra ID für Ihren Autorisierungs-Server-Anbieter verwenden, geben Sie die Mandanten-ID für diese Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Client-ID</td>
        <td>
          <p>Geben Sie die Client-ID für die Veeva Vault-Anwendung ein, die diese Verbindung verwenden wird.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Client-Geheimnis</td>
        <td>
          <p>Geben Sie das Client-Geheimnis für die Veeva Vault-Anwendung ein, die diese Verbindung verwenden wird.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Profil-ID</td>
        <td>
          <p>Geben Sie die ID Ihres OAuth2/Open ID Connect-Profils ein.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">Vault-DNS</td> 
       <td>Geben Sie Ihr Veeva Vault-DNS (Domain-Name) ein.</p><p>Um Ihr Veeva Vault-DNS zu finden, überprüfen Sie die URL, die Sie für den Zugriff auf Veeva Vault verwenden.</p>Im URL-<code>https://my-dns.veevavault.com</code> wird beispielsweise der DNS <code>my-dns.veevavault.com</code>. </td> 
      </tr> 
      <tr>
        <td role="rowheader">Ihre Sitzungsablaufzeit in Minuten</td>
        <td>
          <p>Geben Sie die Ablaufzeit Ihrer Sitzung in Minuten ein.</p>
        </td>
      </tr>
     </tbody> 
    </table>

1. Klicken Sie auf **[!UICONTROL Fortsetzen]**, um die Verbindung zu erstellen und zum Modul zurückzukehren.


## Veeva Vault-Module und ihre Felder

Beim Konfigurieren von Veeva Vault-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service zusätzliche Veeva-Vault-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Dokument](#document)
* [Objekt](#object)
* [Multi-Datei-Extraktion](#multi-file-extract)
* [Laden mehrerer Dateien](#multi-file-load)
* [Datei-Staging](#file-staging)
* [Sonstiges](#other)

### Dokument

* [Ein einzelnes Dokument erstellen](#create-a-single-document)
* [Einzelne Dokumentbeziehung erstellen](#create-a-single-document-relationship)
* [Erstellen mehrerer Anmerkungen](#create-multiple-annotations)
* [Mehrere Dokumente erstellen](#create-multiple-documents)
* [Erstellen mehrerer Dokumentbeziehungen](#create-multiple-document-relationships)
* [Ein einzelnes Dokument löschen](#delete-a-single-document)
* [Löschen einer einzelnen Dokumentbeziehung](#delete-a-single-document-relationship)
* [Mehrere Anmerkungen löschen](#delete-multiple-annotations)
* [Löschen mehrerer Dokumentbeziehungen](#delete-multiple-document-relationships)
* [Datei herunterladen](#download-file)
* [Dokumente exportieren](#export-documents)
* [Ein einzelnes Dokument abrufen](#get-a-single-document)
* [Dokumentanmerkungen abrufen](#get-document-annotations)
* [Abrufen von Dokumentbeziehungen](#get-document-relationships)
* [Benutzeraktion initiieren](#initiate-user-action)
* [Dokumente auflisten](#list-documents)
* [Ergebnisse des Dokumentexports abrufen](#retrieve-document-export-results)
* [Einzelnes Dokument aktualisieren](#update-a-single-document)
* [Mehrere Anmerkungen aktualisieren](#update-multiple-annotations)
* [Mehrere Dokumente aktualisieren](#update-multiple-documents)

#### Ein einzelnes Dokument erstellen

Dieses Modul erstellt ein einzelnes Dokument, einen einzelnen Binder oder eine einzelne Vorlage.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie ein Dokument, einen Binder oder eine Vorlage erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Felder auswählen</p> </td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Daten eingeben möchten, und geben Sie dann die Daten in diese Felder ein.</td> 
  </tr> 
 </tbody> 
</table>

#### Einzelne Dokumentbeziehung erstellen

Dieses Aktionsmodul erstellt eine Beziehung zwischen zwei Dokumenten

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Dokument-ID</p> </td> 
   <td> <p>Geben Sie die ID des Dokuments ein, von dem die Beziehung ausgehen soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>Wählen Sie die ID der Version aus, für die Sie eine Beziehung erstellen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Zieldokument-ID</p> </td> 
   <td> <p>Geben Sie die ID des Dokuments ein, auf das die Beziehung verweist.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Target-Hauptversion</p> </td> 
   <td> <p>Geben Sie die Hauptversion des Zieldokuments ein. Das ist die Zahl vor dem Punkt.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Nebenversion der Zielversion</p> </td> 
   <td> <p>Geben Sie die Hauptversion des Zieldokuments ein. Das ist die Zahl nach dem Punkt.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Beziehungstyp</p> </td> 
   <td> <p>Geben Sie den Typ der Beziehung ein, die Sie erstellen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen mehrerer Anmerkungen

Mit diesem Aktionsmodul können Sie bis zu 500 Anmerkungen erstellen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Anmerkungen</p> </td> 
   <td> <p>Klicken Sie für jede Anmerkung, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und füllen Sie die Daten aus, die in <a href="#annotation-fields" class="MCXref xref">Anmerkungsfeldern</a> in diesem Artikel beschrieben sind.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### Anmerkungsfelder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Anmerkungstyp </td> 
   <td> <p>Wählen Sie den Typ der Anmerkung aus, die Sie erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Geben Sie den Typ der Ortsmarke ein, den Sie für diese Anmerkung verwenden möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Seitennummer</p> </td> 
   <td> <p>Geben Sie die Seitenzahl der Seite ein, auf der diese Anmerkung angezeigt werden soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>X-Koordinate</p> </td> 
   <td> <p>Geben Sie die X-Koordinate der Ortsmarke ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Y-Koordinate</p> </td> 
   <td> <p>Geben Sie die Y-Koordinate der Ortsmarke ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Breite</p> </td> 
   <td> <p>Geben Sie die Breite der Ortsmarke ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Höhe</p> </td> 
   <td> <p>Geben Sie die Höhe der Ortsmarke ein oder kartieren Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Stil</p> </td> 
   <td> <p>Geben Sie den Stil der Ortsmarke ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Referenz</p> </td> 
   <td> <p>Mit einem Verweis kann die Anmerkung auf eine externe Quelle verweisen. Klicken Sie für jeden Verweis, den Sie der Anmerkung hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie den Typ, die Dokumentversions-ID und eine Anmerkung des Verweises ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Felder auswählen</p> </td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Werte angeben möchten, und geben Sie dann die Werte in die einzelnen Felder ein. Die verfügbaren Felder hängen vom Anmerkungstyp ab.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### Mehrere Dokumente erstellen

Dieses Modul erstellt mehrere Dokumente oder Vorlagen mithilfe einer CSV-Datei.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie Vorlagen oder Dokumente erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dateidaten</p> </td> 
   <td> <p>Ordnen Sie die CSV-Datei zu, die zum Erstellen der Dokumente verwendet wird.</td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen mehrerer Dokumentbeziehungen

Dieses Aktionsmodul konfiguriert mehrere Dokumentbeziehungen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Eingabetyp</p> </td> 
   <td> <p>Wählen Sie den Typ der Eingabe aus, den Sie zum Erstellen dieser Beziehungen bereitstellen.</p> <ul><li>CSV</li><li>JSON</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Dateidaten</p> </td> 
   <td> <p>Wenn Sie eine CSV-Datei verwenden, geben Sie die CSV-Dateidaten ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Beziehungsdaten</p> </td> 
   <td> <p>Wenn Sie JSON verwenden, klicken Sie für jede Beziehung, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und füllen Sie die Daten aus, die in <a href="#relationship-fields" class="MCXref xref">Beziehungsfelder</a> in diesem Artikel beschrieben sind.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### Beziehungsfelder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Source-Dokument-ID </td> 
   <td> <p>Geben Sie die ID des Dokuments ein, von dem die Beziehung ausgehen soll, oder mappen Sie sie.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Source-Hauptversion</p> </td> 
   <td> <p>Geben Sie die Hauptversion des Quelldokuments ein. Das ist die Zahl vor dem Punkt.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Source-Nebenversion</p> </td> 
   <td> <p>Geben Sie die Hauptversion des Quelldokuments ein. Das ist die Zahl nach dem Punkt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Zieldokument-ID</p> </td> 
   <td> <p>Geben Sie die ID des Dokuments ein, auf das die Beziehung verweist.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Target-Hauptversion</p> </td> 
   <td> <p>Geben Sie die Hauptversion des Zieldokuments ein. Das ist die Zahl vor dem Punkt.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Nebenversion der Zielversion</p> </td> 
   <td> <p>Geben Sie die Hauptversion des Zieldokuments ein. Das ist die Zahl nach dem Punkt.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader"> <p>Beziehungstyp</p> </td> 
   <td> <p>Geben Sie den Typ der Beziehung ein, die Sie erstellen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Ein einzelnes Dokument löschen

Dieses Modul löscht ein einzelnes Dokument, einen Binder oder eine Vorlage.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie ein Dokument, einen Binder oder eine Vorlage löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokument-ID/Binder-ID/Vorlagenname</p> </td> 
   <td> <p>Wählen Sie das Element aus, das Sie löschen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### Löschen einer einzelnen Dokumentbeziehung

Dieses Aktionsmodul löscht eine Beziehung aus einem Dokument

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Dokument-ID</p> </td> 
   <td> <p>Geben Sie die ID des Quelldokuments für die Beziehung ein, die Sie löschen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>Wählen Sie die ID der Version aus, für die Sie eine Beziehung löschen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Beziehungs-ID</p> </td> 
   <td> <p>Geben Sie die ID der Beziehung ein, die Sie löschen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### Mehrere Anmerkungen löschen

Dieses Aktionsmodul löscht Anmerkungen. Der Benutzer muss über die Berechtigung zum Löschen von Anmerkungen in Veeva Vault verfügen. Sie können bis zu 500 Anmerkungen löschen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Anmerkungen</p> </td> 
   <td> <p>Klicken Sie für jede Anmerkung, die Sie löschen möchten<b> auf „Element hinzufügen</b> und geben Sie die folgenden Felder ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID</p> </td> 
   <td> <p>Geben Sie die ID der Anmerkung ein, die Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokumentversions-ID</p> </td> 
   <td> <p>Geben Sie die Versionsnummer des Dokuments ein, das die Anmerkung enthält, die Sie löschen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Löschen mehrerer Dokumentbeziehungen

Dieses Aktionsmodul löscht Beziehungen aus mehreren Dokumenten

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Eingabetyp</p> </td> 
   <td> <p>Wählen Sie den Typ der Eingabe aus, die Sie zum Löschen dieser Beziehungen bereitstellen.</p> <ul><li>CSV</li><li>JSON</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Dateidaten</p> </td> 
   <td> <p>Wenn Sie eine CSV-Datei verwenden, geben Sie die CSV-Dateidaten ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Beziehungsdaten</p> </td> 
   <td> <p>Wenn Sie JSON verwenden, klicken Sie für jede Beziehung, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Beziehungs-ID ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Herunterladen der Datei

Dieses Modul lädt ein Dokument, eine Dokumentversion oder eine Vorlage aus Veeva Vault herunter.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie ein Dokument oder eine Vorlage herunterladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Download-Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie ein Dokument oder eine Dokumentversion herunterladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokument-ID/Vorlagenname</p> </td> 
   <td> <p>Geben Sie die ID des Dokuments oder den Namen der Vorlage, die Sie herunterladen möchten, ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokument auschecken</p> </td> 
   <td> <p>Wenn Sie ein Dokument herunterladen, aktivieren Sie diese Option, um das Dokument vor dem Herunterladen auszuchecken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>Wenn Sie eine Dokumentversion herunterladen, wählen Sie die herunterzuladende Version aus.</td> 
  </tr> 
 </tbody> 
</table>

#### Dokumente exportieren

Dieses Modul exportiert von Ihnen angegebene Dokumente, einschließlich Quellen, Ausgabedarstellungen und Text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie ein Dokument, einen Binder oder eine Vorlage löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Quelle</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um Quelldateien in den Export einzuschließen.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Ausgabedarstellungen</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um Ausgabedarstellungsdateien in den Export einzuschließen.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Alle Versionen</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um alle Versionen der Dokumentdateien in den Export einzubeziehen.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Text</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um Quelldokumenttext in den Export einzuschließen.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Ein einzelnes Dokument abrufen

Dieses Modul ruft Metadaten für ein einzelnes Dokument, einen Binder oder eine Vorlage ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie Daten für ein Dokument, einen Binder oder eine Vorlage abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokument-ID/Binder-ID/Vorlagenname</p> </td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Daten abrufen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### Dokumentanmerkungen abrufen

Dieses Modul ruft Anmerkungen aus einer bestimmten Dokumentversion ab. Sie können alle Anmerkungen abrufen oder nur bestimmte Anmerkungstypen abrufen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Dokument-ID</p> </td> 
   <td> <p>Wählen Sie das Dokument aus, für das Sie Anmerkungen abrufen möchten, oder ordnen Sie es zu. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>Wählen Sie die ID der Version aus, für die Sie Anmerkungen abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl der zurückgegebenen Anmerkungen</td> 
   <td>Geben Sie die maximale Anzahl von Anmerkungen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen von Dokumentbeziehungen

Dieses Modul ruft alle Beziehungen für ein Dokument ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Dokument-ID</p> </td> 
   <td> <p>Wählen Sie das Dokument aus, für das Sie Beziehungen abrufen möchten, oder ordnen Sie es zu. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>Wählen Sie die ID der Version aus, für die Sie Beziehungen abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Beziehungen</td> 
   <td>Geben Sie die maximale Anzahl von Beziehungen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### Benutzeraktion initiieren

Dieses Modul initiiert Aktionen für Dokumente und Binder, z. B. das Senden eines Dokuments zur Überprüfung oder das Ändern seines Status.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie eine Aktion auf einem Dokument oder einem Binder durchführen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokument/Binder</p> </td> 
   <td> <p>Wählen Sie das Dokument oder den Binder aus, für das bzw. den Sie die Aktion durchführen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokumentversion/-binderversion</p> </td> 
   <td> <p>Wählen Sie das Dokument oder den Binder aus, für das bzw. den Sie die Aktion durchführen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Aktion</p> </td> 
   <td> <p>Wählen Sie die Aktion aus, die mit dem Dokument oder dem Binder durchgeführt werden soll.</td> 
  </tr> 
 </tbody> 
</table>

#### Dokumente auflisten

Dieses Modul listet alle Dokumente des ausgewählten Typs auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Dokumente, Ordner oder Vorlagen aufgelistet werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Ergebnisse des Dokumentexports abrufen

Dieses Modul gibt die Ergebnisse eines zuvor angeforderten Dokumentexports zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Auftrags-ID</p> </td> 
   <td> <p>Geben Sie die ID des Auftrags ein, für den Sie Ergebnisse zurückgeben möchten, oder mappen Sie sie. </p> </td> 
  </tr> 
  </tbody> 
</table>

#### Mehrere Anmerkungen aktualisieren

Dieses Aktionsmodul aktualisiert bis zu 500 Anmerkungen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Anmerkungen</p> </td> 
   <td> <p>Klicken Sie für jede Anmerkung, die Sie aktualisieren möchten, auf <b>Element hinzufügen</b> und füllen Sie die Daten aus, die in <a href="#annotation-fields" class="MCXref xref">Anmerkungsfeldern</a> in diesem Artikel beschrieben sind.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### Mehrere Dokumente aktualisieren

Dieses Modul aktualisiert mehrere Dokumente oder Vorlagen mithilfe einer CSV-Datei.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Auswählen, ob Vorlagen oder Dokumente erstellt werden sollen</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dateidaten</p> </td> 
   <td> <p>Ordnen Sie die CSV-Datei zu, die zum Erstellen der Dokumente verwendet wird.</td> 
  </tr> 
 </tbody> 
</table>

#### Einzelnes Dokument aktualisieren

Dieses Modul aktualisiert ein einzelnes Dokument, einen Binder oder eine Vorlage.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie ein Dokument, eine Dokumentversion, einen Binder oder eine Vorlage erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID/Name</p> </td> 
   <td> <p>Wenn Sie eine Vorlage aktualisieren, geben Sie einen neuen Namen für die Vorlage ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Name der neuen Vorlage</p> </td> 
   <td> <p>Geben Sie die ID oder den Namen des Objekts ein, das Sie aktualisieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>Felder auswählen</p> </td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Daten eingeben möchten, und geben Sie dann die Daten in diese Felder ein.</td> 
  </tr> 
 </tbody> 
</table>

### Objekt

* [Erstellen eines einzelnen Objektdatensatzes](#create-a-single-object-record)
* [Löschen eines einzelnen Objektdatensatzes](#delete-a-single-object-record)
* [Abrufen eines einzelnen Objekts](#get-a-single-object)
* [Auflisten von Objekten und Datensätzen](#list-objects-records)
* [Aktualisieren eines einzelnen Objektdatensatzes](#update-a-single-object-record)

#### Erstellen eines einzelnen Objektdatensatzes

Dieses Modul erstellt, kopiert oder tief kopiert einen einzelnen Objektdatensatz.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob ein Datensatz erstellt oder kopiert werden soll oder ob ein Datensatz tief kopiert werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Migrationsmodus</td> 
   <td>Wenn Sie einen Datensatz erstellen oder kopieren, aktivieren Sie diese Option, um Objektdatensätze nicht im Anfangszustand und mit minimaler Validierung zu erstellen oder zu aktualisieren, inaktive Datensätze zu erstellen und standardmäßige und systemverwaltete Felder wie <code>createdby_v</code> festzulegen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Keine Trigger</td> 
   <td>Wenn auf „true“ gesetzt und der Migrationsmodus aktiviert ist, umgeht das Modul alle System-, Standard-, benutzerdefinierten SDK-Trigger und Aktions-Trigger.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Objektname</td> 
   <td>Geben Sie den Wert des Feldes __v) des Objektnamens ein oder ordnen Sie ihn zu, z. B. <code>product__v</code>, <code>country__v</code> oder <code>custom_object__c</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintrags-ID</td> 
   <td>Wenn Sie einen Datensatz tief kopieren, wählen Sie den zu kopierenden Datensatz aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Datensatzfelder</td> 
   <td>Wenn Sie einen Datensatz tief kopieren, wählen Sie die Felder aus, für die Sie Werte angeben möchten, und geben Sie diese Werte an.</td> 
  </tr> 
 </tbody> 
</table>

#### Löschen eines einzelnen Objektdatensatzes

Dieses Modul löscht oder kaskadiert einen einzelnen Objektdatensatz. Durch das kaskadierende Löschen eines Datensatzes werden der Datensatz und alle untergeordneten Objekte gelöscht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob ein Datensatz gelöscht oder kaskadierend gelöscht werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Objektname</td> 
   <td>Wählen Sie das Objekt aus, das Sie löschen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintrags-ID</td> 
   <td>Wählen Sie die ID des Datensatzes aus, den Sie löschen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Externe ID</td> 
   <td>Anstelle der Datensatz-ID können Sie diese benutzerdefinierte externe Dokument-ID verwenden.</td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen eines einzelnen Objekts

Dieses Modul ruft Metadaten ab, die für einen bestimmten Objektdatensatz in Ihrem Tresor konfiguriert sind.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Objektname</td> 
   <td>Wählen Sie das Objekt aus, für das Sie Metadaten abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintrags-ID</td> 
   <td>Wählen Sie die ID des Datensatzes aus, für den Sie Metadaten abrufen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### Auflisten von Objekten und Datensätzen

Dieses Modul ruft alle Vault-Objekte im authentifizierten Vault ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Lokalisierte Kennzeichnungen abrufen</p> </td> 
   <td> <p>Wählen Sie Ja , um lokalisierte (übersetzte) Zeichenfolgen für die Felder label und label_plural abzurufen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Update a single object record-->

Dieses Modul aktualisiert Felder in einem vorhandenen Objektdatensatz.

Dieses Modul erstellt, kopiert oder tief kopiert einen einzelnen Objektdatensatz.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob ein Datensatz erstellt oder kopiert werden soll oder ob ein Datensatz tief kopiert werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Migrationsmodus</td> 
   <td>Aktivieren Sie diese Option, um Objektdatensätze in einem nicht anfänglichen Status und mit minimaler Validierung zu erstellen oder zu aktualisieren, inaktive Datensätze zu erstellen und standardmäßige und systemverwaltete Felder wie <code>createdby_v</code> festzulegen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Keine Trigger</td> 
   <td>Wenn der Migrationsmodus aktiviert ist, können Sie diese Option aktivieren, um alle System-, Standard-, benutzerdefinierten SDK-Trigger und Aktions-Trigger zu umgehen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Objektname</td> 
   <td>Geben Sie den Wert des Feldes __v) des Objektnamens ein oder ordnen Sie ihn zu, z. B. <code>product__v</code>, <code>country__v</code> oder <code>custom_object__c</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintrags-ID</td> 
   <td>Kennung des zu aktualisierenden Eintrags auswählen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Land</td> 
   <td>Geben Sie den Lebenszyklusstatus des Datensatzes an, wenn <code>X-VaultAPI-MigrationMode</code> auf „true“ gesetzt ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Statuslabel</td> 
   <td>Geben Sie den Lebenszyklusstatustyp des Datensatzes an, wenn <code>X-VaultAPI-MigrationMode</code> auf „true“ gesetzt ist. Verwenden Sie das Format <code>base:object_lifecycle:</code> gefolgt vom Objektstatustyp .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Datensatzfelder</td> 
   <td>Wenn Sie einen Datensatz tief kopieren, wählen Sie die Felder aus, für die Sie Werte angeben möchten, und geben Sie diese Werte an.</td> 
  </tr> 
 </tbody> 
</table>

### Multi-Datei-Extraktion

* [Mehrere Dateien extrahieren](#extract-multiple-files)
* [Abrufen von Extraktergebnissen](#retrieve-extract-results)

#### Mehrere Dateien extrahieren

Dieses Aktionsmodul erstellt einen Ladevorgang zum Extrahieren einer oder mehrerer Datendateien.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Datendateien</td> 
   <td>Klicken Sie für jede Datei, die Sie extrahieren möchten, auf <b>Element hinzufügen</b> und geben Sie Folgendes ein:
   <ul>
   <li>Objekttyp</li>
   <li>VQL-Kriterien (Optional): Um den Datensatz so zu filtern, dass er nur Dateien enthält, die bestimmte Kriterien erfüllen, geben Sie die Kriterien in Vault Query Language (VQL) ein.</li>
   </ul>
    </td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen von Extraktergebnissen

Dieses Aktionsmodul ruft Ergebnisse einer angegebenen Extraktionsanfrage ab.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Auftrags-ID</p> </td> 
   <td> <p>Geben Sie den Auftrag ein, für den Sie Ergebnisse abrufen möchten, oder ordnen Sie ihn zu. Sie können dies über das Modul Datendateien extrahieren zuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aufgaben ID</td> 
   <td> <p>Geben Sie die Aufgabe ein, für die Sie Ergebnisse abrufen möchten, oder ordnen Sie sie zu. Sie können dies über das Modul Datendateien extrahieren zuordnen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Laden mehrerer Dateien

* [Mehrere Dateien laden](#load-multiple-files)
* [Abrufen von Protokollergebnissen](#retrieve-log-results)

#### Mehrere Dateien laden

Dieses Modul erstellt einen Ladevorgang und lädt einen Satz von Datendateien.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Datei</td> 
   <td>Geben Sie den Dateipfad der CSV-Datei ein, die für diesen Auftrag verwendet werden soll, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bestellung</td> 
   <td>Geben Sie die Reihenfolge für die Dateiliste ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Keine Trigger</td> 
   <td>Wählen Sie Ja aus, um Trigger bei Datensätzen oder Dokumenten zu umgehen.</td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen von Protokollergebnissen

Dieses Aktionsmodul ruft ein Protokoll der Ergebnisse des Ladevorgangs ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Auftrags-ID</p> </td> 
   <td> <p>Geben Sie den Auftrag ein, für den Sie Ergebnisse abrufen möchten, oder ordnen Sie ihn zu. Sie können dies über das Modul Datendateien laden zuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aufgaben ID</td> 
   <td> <p>Geben Sie die Aufgabe ein, für die Sie Ergebnisse abrufen möchten, oder ordnen Sie sie zu. Sie können dies über das Modul Datendateien laden zuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Typ</td> 
   <td> <p>Wählen Sie aus, ob erfolgreiche oder fehlgeschlagene Aufträge abgerufen werden sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Datei-Staging

#### Elemente unter dem Pfad auflisten

Dieses Modul gibt eine Liste von Dateien und Ordnern für den angegebenen Pfad zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Persönlichen Ordner auswählen</td> 
   <td>Wählen Sie den Basisordner aus, in dem die Elemente aufgelistet werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bestellung</td> 
   <td>Geben Sie die Reihenfolge für die Dateiliste ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Keine Trigger</td> 
   <td>Wählen Sie Ja aus, um Trigger bei Datensätzen oder Dokumenten zu umgehen.</td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

* [Benutzerdefinierten API-Aufruf erstellen](#make-a-custom-api-call)
* [Erstellen einer VQL-Abfrage](#make-a-vql-query)
* [Protokolle lesen](#read-logs)

#### Benutzerdefinierten API-Aufruf erstellen

Dieses Aktionsmodul führt einen benutzerdefinierten Aufruf an die Veeva Vault-API durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Geben Sie einen Pfad relativ zu <code>baseurl/api/v</code> ein.  Beispiel: <code>/objects/documents</code>. <code>baseurl/api/v/</code> nicht einschließen, da es bereits eingeschlossen ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Methode</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Header</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Abfragezeichenfolge</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Textkörper</td> 
   <td> <p>Fügen Sie den Textinhalt für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrem JSON-Objekt verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen einer VQL-Abfrage

Dieses Modul führt eine Abfrage mit Vault Query Language (VQL) durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Auswählen, ob Vorlagen oder Dokumente erstellt werden sollen</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dateidaten</p> </td> 
   <td> <p>Ordnen Sie die CSV-Datei zu, die zum Erstellen der Dokumente verwendet wird.</td> 
  </tr> 
 </tbody> 
</table>

#### Protokolle lesen

Dieses Modul gibt Daten aus Audit-Protokollen zurück

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-veeva-vault-to-workfront-fusion" class="MCXref xref">Verbinden von Veeva Vault mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Prüfungstyp</p> </td> 
   <td> <p>Wählen Sie den Audittyp aus, für den Sie Daten abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Startdatum</p> </td> 
   <td> <p>Geben Sie das Startdatum für die Audits ein, die Sie abrufen möchten, oder ordnen Sie es zu.</p><p>Eine Liste der unterstützten Datums- und Uhrzeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Erzwungene Typumwandlung</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Enddatum</p> </td> 
   <td> <p>Geben Sie das Enddatum für die Audits ein, die Sie abrufen möchten, oder ordnen Sie es zu.</p><p>Eine Liste der unterstützten Datums- und Uhrzeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Erzwungene Typumwandlung</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Ergebnis-URL </p> </td> 
   <td> <p>Wählen Sie CSV aus, wenn Sie eine URL zum Herunterladen einer CSV-Datei des Ergebnisses abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</td> 
  </tr> 
 </tbody> 
</table>
