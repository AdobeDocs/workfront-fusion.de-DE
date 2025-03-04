---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe-Speichermodule
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Projekte in der Adobe Admin Console erstellen und verwalten.
author: Becky
feature: Workfront Fusion
exl-id: 78ee905f-4713-44a4-bffb-c64cdb3665c2
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '1386'
ht-degree: 2%

---

# Adobe-Speichermodule

In einem [!DNL Adobe Workfront Fusion] können Sie Projekte in der Adobe Admin Console erstellen und verwalten.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Erstellen einer Verbindung mit dem Adobe-Speicher

Das Herstellen einer Verbindung zum Adobe-Speicher erfordert einige Konfigurationen in Adobe Developer Console sowie in Fusion.

### Konfigurieren des Projekts in der Adobe Developer Console

Sie müssen die API zu Ihrem Projekt in der Adobe Developer Console hinzufügen.

1. Öffnen Sie Ihr Projekt in der Adobe Developer Console.
1. Klicken Sie auf **Zum Projekt hinzufügen** und wählen Sie **API** aus.
1. Wählen Sie aus der Liste der verfügbaren APIs die Option **Adobe Cloud Platform und Collaboration API** aus.
1. Wählen Sie im Bildschirm Authentifizierungstyp auswählen die Option **OAuth-Server-zu-Server** aus und klicken Sie auf **Weiter**.
1. Fügen Sie einen Namen für die Berechtigung hinzu.
1. Klicken Sie **Weiter** und dann auf **Konfigurierte API speichern**.
1. Notieren Sie sich die angegebenen Anmeldedaten, die Sie beim Konfigurieren der Verbindung in Workfront Fusion verwenden werden.
1. Fahren Sie fort [Ihr technisches Konto zum Administrator in der Adobe Admin Console machen](#make-your-technical-account-an-admin-in-the-adobe-admin-console).

### Ihr technisches Konto in der Adobe Admin Console als Administrator festlegen

Wählen Sie auf der Adobe Admin Console-Seite die Registerkarte Produkte in der oberen Navigationsleiste und dann Workfront Fusion aus

1. Suchen Sie die E-Mail-Adresse des Benutzers des technischen Kontos in Ihrem Unternehmen und kopieren Sie sie.
1. Wenn eine Liste angezeigt wird, klicken Sie auf den Link oben.
1. Dies ist die Produktionsinstanz, in der die Benutzer arbeiten.
1. Klicken Sie in der angezeigten Liste bei ausgewählter Registerkarte Produktprofile auf den Namen des Workfront-Produktprofils.

   Diese Liste enthält alle Benutzenden, die bereits Ihrer Produktionsinstanz von Workfront zugewiesen sind.

1. Wählen Sie die **Administratoren** oberhalb der Benutzerliste aus.
1. Wählen Sie **Admin hinzufügen** aus.
1. Geben Sie im Feld Produktprofil-Administratoren hinzufügen die E-Mail-Adressen des technischen Kontos ein und klicken Sie dann auf **Speichern**.

   Das technische Konto ist ein Administrator.

1. Fahren Sie [Verbindung in Workfront Fusion erstellen](#create-the-connection-in-workfront-fusion) fort.

### Erstellen der Verbindung in Workfront Fusion

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe Storage]:

1. Klicken Sie in einem beliebigen Modul **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Verbindungstyp]</td>
        <td>Wählen Sie <code>Server to server</code> aus.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
        </tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre [!UICONTROL Adobe] [!UICONTROL Client-ID] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des Projekts in der [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihren [!DNL Adobe] [!UICONTROL Client Secret] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des Projekts in der [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS-Organisations-ID]</td>
        <td>Geben Sie Ihre Adobe IMS-Organisations-ID ein oder mappen Sie sie. Dies ist eine Zeichenfolge der Form <code> 123abc@AdobeOrg</code>, wobei der Abschnitt vor dem @ eine hexadezimale Zahl ist. Sie finden diesen Wert als Teil des URL-Pfads für Ihr Unternehmen in der Adobe Admin Console oder in der Adobe.IO-Konsole für Ihre User Management-Integration.</td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## Adobe-Speichermodule und ihre Felder

Beim Konfigurieren von Adobe User Management-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus werden möglicherweise weitere Adobe-Benutzerverwaltungsfelder angezeigt, je nach Faktoren wie Ihrer Zugriffsebene in der App oder im Service. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [ESM-Speicher](#esm-stores)
* [Einladungen](#invitations)
* [Sonstige](#other)

### ESM-Speicher

* [Erstellen eines ESM-Stores](#create-an-esm-store)
* [Löschen eines ESM-Stores](#delete-an-esm-store)
* [Verwerfen eines ESM-Speichers](#discard-an-esm-store)
* [Wiederherstellen eines ESM-Speichers](#restore-an-esm-store)

#### Erstellen eines ESM-Stores

Dieses Aktionsmodul richtet einen neuen ESM-Speicher (Enterprise Storage Management) ein, um geschäftskritische Assets zu organisieren und zu verwalten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zum Adobe-Speicher finden Sie unter <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Erstellen einer Verbindung zum Adobe-Speicher</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Projektname</td> 
   <td>Geben Sie einen Namen für das neue Projekt ein oder mappen Sie ihn.</td> 
  </tr> 
 </tbody> 
</table>

#### Löschen eines ESM-Stores

Dieses Aktionsmodul entfernt dauerhaft einen vorhandenen ESM-Speicher und alle zugehörigen Daten. Dieser Vorgang kann nicht rückgängig gemacht werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zum Adobe-Speicher finden Sie unter <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Erstellen einer Verbindung zum Adobe-Speicher</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Store-ID</td> 
   <td>Geben Sie die ID des Stores ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Verwerfen eines ESM-Speichers

Dieses Aktionsmodul markiert einen EMS-Speicher zum Löschen, sodass vor dem endgültigen Entfernen eine Übergangsfrist möglich ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zum Adobe-Speicher finden Sie unter <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Erstellen einer Verbindung zum Adobe-Speicher</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Store-ID</td> 
   <td>Geben Sie die ID des Stores ein, den Sie verwerfen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Wiederherstellen eines ESM-Speichers

Dieses Aktionsmodul stellt einen zuvor gelöschten ESM-Speicher wieder her und stellt den Zugriff auf seine Daten und Konfigurationen wieder her.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zum Adobe-Speicher finden Sie unter <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Erstellen einer Verbindung zum Adobe-Speicher</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Store-ID</td> 
   <td>Geben Sie die ID des Stores ein, den Sie wiederherstellen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

### Einladungen

#### Benutzer einladen

Dieses Aktionsmodul sendet eine Einladung, um einem neuen Benutzer Zugriff auf einen bestimmten ESM-Store zu gewähren und so die Zusammenarbeit und Dateiverwaltung zu ermöglichen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zum Adobe-Speicher finden Sie unter <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Erstellen einer Verbindung zum Adobe-Speicher</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">E-Mail-Adresse</td> 
   <td>Geben Sie die E-Mail-Adresse des Benutzers ein, den Sie in den Store einladen möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset-ID</td> 
   <td>Geben Sie die ID des Assets ein, zu dem Sie den Benutzer einladen möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Funktion</td> 
   <td>Wählen Sie die Rolle aus, die der neu eingeladene Benutzer für das Asset haben soll.<ul><li>Besitzerin bzw. Besitzer</li><li>Bearbeiterin bzw. Bearbeiter</li><li>Viewer</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kann kommentieren</td> 
   <td>Aktivieren Sie diese Option, damit der Benutzer das Asset kommentieren kann.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kann freigeben</td> 
   <td>Aktivieren Sie diese Option, damit der Benutzer das Asset für andere Benutzer freigeben kann.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Akzeptanz erforderlich</td> 
   <td>Aktivieren Sie diese Option, um sicherzustellen, dass Benutzende die Einladung annehmen müssen, bevor sie am Asset zusammenarbeiten können.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verwenden von Reittieren</td> 
   <td>Aktivieren Sie diese Option, wenn für den Einladenden ein Bereitstellungspunkt zur Ressource erstellt werden muss. Die Option Erforderliche Akzeptanz muss aktiviert sein, um diese Option zu aktivieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benachrichtigungstyp</td> 
   <td>Geben Sie den Adobe-Benachrichtigungstyp ein, den Sie verwenden möchten, um Benutzende über die Einladung zu informieren, oder ordnen Sie ihn zu. Wenn dies leer gelassen wird, basiert der Benachrichtigungstyp auf dem Mimetype des Assets.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vorlagenname</td> 
   <td>Geben Sie die Adobe Post Office ID der Vorlage ein, die Sie für die Einladungs-E-Mail verwenden möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gebietsschema</td> 
   <td>Geben Sie das Gebietsschema des Benutzers in Form eines Sprachcodes und eines Ländercodes ein. <p>Beispiel: <code>en-us</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Extern</td> 
   <td>Legen Sie diese Option auf „true“ fest, wenn Sie Benachrichtigungen mithilfe eines externen Systems zum Adobe-Einladungs-Service senden möchten. Externe Benachrichtigungen werden nur unterstützt, wenn keine Akzeptanz erforderlich ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset-Typ</td> 
   <td>Geben Sie den Typ des Assets ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nachricht</td> 
   <td>Geben Sie eine Nachricht ein, die in die Einladungs-E-Mail aufgenommen werden soll, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ziel-URL</td> 
   <td>Geben Sie die URL ein, die der Einladende zum Anzeigen des Assets verwenden kann, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### Sonstige

#### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt eine benutzerdefinierte HTTP-Anfrage an die Adobe-Speicher-API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
   <td>Anweisungen zum Erstellen einer Verbindung zum Adobe-Speicher finden Sie unter <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Erstellen einer Verbindung zum Adobe-Speicher</a> in diesem Artikel.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>Pfad eingeben für <code>https://ccprojects.adobe.io/api/v3/.</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Methode</p>
      </td>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">Kopfzeilen</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungs- und X-API-Schlüssel-Header hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Abfragezeichenfolge  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Text</td>
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
