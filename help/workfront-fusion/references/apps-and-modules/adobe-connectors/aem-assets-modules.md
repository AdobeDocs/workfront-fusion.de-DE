---
title: Adobe Experience Manager Assets-Module
description: Mit dem Adobe Experience Manager Assets-Connector für Adobe Workfront Fusion können Sie Assets erstellen, hochladen und aktualisieren sowie Ordner und Assets kopieren oder verschieben.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: d4bdc4005a3b7b22d64adc8ca1d20bcf534ddfd1
workflow-type: tm+mt
source-wordcount: '3734'
ht-degree: 3%

---

# Adobe Experience Manager Assets-Module

Mit dem Adobe Experience Manager Assets-Connector für Adobe Workfront Fusion können Sie Assets erstellen, hochladen und aktualisieren sowie Ordner und Assets kopieren oder verschieben.

Eine Videoeinführung zum Adobe Experience Manager Assets-Connector finden Sie unter:

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

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

* Sie benötigen ein Adobe Experience Manager Assets-Konto, um diese Module verwenden zu können.
* Sie müssen den Server-zu-Server-Fluss in der Adobe Developer-Konsole einrichten.

  Anweisungen zum Einrichten des Server-zu-Server-Flusses in der Adobe Developer-Konsole finden Sie unter [Generieren von Zugriffstoken für Server-seitige APIs](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=de#the-server-to-server-flow).
* Ihr technisches Adobe Experience Manager-Konto muss über Schreibberechtigungen verfügen.

  Anweisungen zum Hinzufügen von Schreibberechtigungen für Ihr technisches Adobe Experience Manager-Konto finden Sie unter [Service-Anmeldeinformationen](https://experienceleague.adobe.com/de/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) in der Dokumentation zu Adobe Experience Manager.

## Adobe Experience Manager Assets-API-Informationen

Der Adobe Experience Manager Assets-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von Adobe Experience Manager Assets mit Workfront Fusion {#connect-adobe-experience-manager-assets-to-workfront-fusion}

So erstellen Sie eine Verbindung für Ihre Adobe Experience Manager Assets-Module:

1. Klicken Sie neben dem Feld Verbindung auf Hinzufügen .

2. Wählen Sie den Verbindungstyp aus, den Sie erstellen:

   * **AEM Assets as a Cloud Service**

     Diese Konfiguration erfordert Informationen von der Adobe Admin Console.

   * **AEM Assets Basic (Adobe Managed Services)**

     Diese Konfiguration erfordert einen Benutzernamen und ein Kennwort.

3. Füllen Sie die Felder für den Verbindungstyp aus, den Sie erstellen.

   Informationen zu AEM Assets as a Cloud Service finden Sie [Konfigurieren der Verbindung für AEM Assets as a Cloud Service](#configure-the-connection-for-aem-assets-as-a-cloud-service).

   Informationen zu AEM Assets Basic (Adobe Managed Services) finden Sie unter [Konfigurieren der Verbindung für AEM Assets Basic](#configure-the-connection-for-aemassets-basic-adobe-managed-services).

4. Klicken Sie **Fortfahren**, um die Verbindung zu speichern und zum Modul zurückzukehren.


### Konfigurieren der Verbindung für AEM Assets as a Cloud Service

>[!NOTE]
>
>* Die Informationen für diese Felder werden beim Einrichten des Server-zu-Server-Flusses auf der Adobe Developer Console generiert. Diese Werte finden Sie in der JSON-Datei mit den Service-Anmeldeinformationen, die im Rahmen dieses Setups generiert wurde.
>
>   Anweisungen zum Einrichten eines Server-zu-Server-Flusses auf der Adobe Developer Console finden Sie unter [Generieren von Zugriffstoken für Server-seitige APIs](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=de#the-server-to-server-flow).
>
>* Ihr technisches Adobe Experience Manager-Konto muss über Schreibberechtigungen verfügen.
>
>   Anweisungen zum Hinzufügen von Schreibberechtigungen für Ihr technisches Adobe Experience Manager-Konto finden Sie unter [Service-Anmeldeinformationen](https://experienceleague.adobe.com/de/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) in der Dokumentation zu Adobe Experience Manager.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">Name der Verbindung</td>
                  <td>
                      <p>Geben Sie einen Namen für diese Verbindung ein.</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">Instanz-URL ohne Schrägstrich</td>
                  <td>Geben Sie die URL für Ihre Adobe Experience Manager-Instanz ein. Geben Sie am Ende der URL keinen Schrägstrich <code>/</code>.</td>
              </tr>
              <tr>
                  <td role="rowheader">Ausfülloptionen für Kontodetails</td>
                  <td>Wählen Sie aus, ob Sie eine JSON zur Beschreibung Ihrer Kontodetails bereitstellen oder Details manuell eingeben möchten.</td>
              </tr>
              <tr>
                  <td role="rowheader">Technische Kontodetails im JSON-Format</td>
                  <td>Wenn Sie JSON bereitstellen, geben Sie die JSON-Datei ein, die Ihre Kontodetails beschreibt, oder fügen Sie sie ein.</td>
              </tr>
              <tr>
                  <td role="rowheader">Client-ID</td>
                  <td>Wenn Sie Details manuell eingeben, geben Sie die Client-ID ein, die bei der Server-zu-Server-Einrichtung generiert wurde.</td>
              </tr>
              <tr>
                  <td role="rowheader">Client-Geheimnis</td>
                  <td>Wenn Sie Details manuell eingeben, geben Sie den im Server-zu-Server-Setup generierten geheimen Client-Schlüssel ein.</td>
              </tr>
              <tr>
                  <td role="rowheader">ID des technischen Kontos</td>
                  <td>Wenn Sie Details manuell eingeben, geben Sie die ID des technischen Kontos ein. Dies ist das Feld „id“ in der JSON-Datei mit den Client-Anmeldeinformationen.</td>
              </tr>
              <tr>
                  <td role="rowheader">Organisations-ID</td>
                  <td class="">Wenn Sie Details manuell eingeben, geben Sie die ID Ihrer Organisation ein. Dies ist das Feld „org“ in der JSON-Datei mit den Client-Anmeldeinformationen.</td>
              </tr>
              <tr>
                  <td role="rowheader">Meta-Bereiche</td>
                  <td>Geben Sie die im Server-zu-Server-Setup generierten Meta-Bereiche ein.</td>
              </tr>
              <tr>
                  <td role="rowheader">Privater Schlüssel</td>
                  <td>Geben Sie den privaten Schlüssel ein, der bei der Server-zu-Server-Einrichtung generiert wurde. Um den privaten Schlüssel zu extrahieren, klicken Sie auf Extrahieren und geben Sie dann die zu extrahierende Datei und das Kennwort für die Datei ein.</td>
              </tr>
              <tr>
                  <td role="rowheader">Authentifizierungs-URL</td>
                  <td>Authentifizierungs-URL für dieses Konto eingeben.</td>
              </tr>
          </tbody>
      </table>


### Konfigurieren der Verbindung für AEM Assets Basic (Adobe Managed Services)

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">Name der Verbindung</td>
                <td>
                    <p>Geben Sie einen Namen für diese Verbindung ein.</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">Instanz-URL ohne Schrägstrich</td>
                <td>Geben Sie die URL für Ihre Adobe Experience Manager-Instanz ein. Geben Sie am Ende der URL keinen Schrägstrich <code>/</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">Benutzername</td>
                <td>Geben Sie den Benutzernamen für das AEM Assets-Konto ein, das für diese Verbindung verwendet wird.</td>
            </tr>
            <tr>
                <td role="rowheader">Kennwort</td>
                <td>Geben Sie das Kennwort für das AEM Assets-Konto ein, das für diese Verbindung verwendet wird.</td>
            </tr>
        </tbody>
    </table>


## Adobe Experience Manager Assets-Module und ihre Felder

Beim Konfigurieren von Adobe Experience Manager Assets-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service können zusätzlich dazu weitere Adobe Experience Manager Assets-Felder angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Dateifunktionen](#files-operations)
* [Sonstiges](#other)
* [Assets (Author-API)](#assets-author-api)
* [Ereignisse (Autoren-API)](#events-author-api)
* [Metadaten (Autoren-API)](#metadata-author-api)
* [Import (Autoren-API)](#import-author-api)
* [Beziehungen (Autoren-API)](#relations-author-api)
* [Ordner (Ordner-API)](#folders-folders-api)

### Dateifunktionen

* [Upload abschließen](#complete-upload)
* [Vordefinierte Speicherung abrufen](#get-presigned-storage)
* [Upload starten](#initiate-upload)
* [Hochladen eines Assets](#upload-an-asset)

#### Upload abschließen

Dieses Aktionsmodul führt einen initiierten Upload durch, nachdem alle Teile der Datei hochgeladen wurden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dateiname</td> 
   <td> <p>Geben Sie einen Namen für die hochgeladene Datei ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Upload-Token</td> 
   <td>Geben Sie das Upload-Token für die Binärdatei ein oder ordnen Sie es zu, wie von der Initiierung angegeben.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">MIME-Typ</td> 
   <td>Geben Sie den MIME-Typ für die abgeschlossene Datei ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vollständiger URI</td> 
   <td>Geben Sie den vollständigen URI für die Datei ein oder mappen Sie ihn.</td> 
  </tr> 
 </tbody> 
</table>


#### Vordefinierte Speicherung abrufen

Dieses Aktionsmodul erstellt eine temporäre vordefinierte URL für das sichere Hochladen oder Herunterladen von Dateien aus AEM, ohne dass direkte Anmeldeinformationen erforderlich sind.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lookup Type</td> 
   <td> <p>Wählen Sie aus, ob Sie das Asset anhand seines Pfads oder seiner ID nachschlagen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Asset</td> 
   <td>Wählen Sie den Pfad zum Asset aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UDID</td> 
   <td>Geben Sie die UDID für das Asset ein oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Upload starten

Dieses Aktionsmodul initiiert einen Upload.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ziel</td> 
   <td> <p>Wählen Sie den Ordner aus, in den Sie eine Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dateiname</td> 
   <td> <p>Namen für die hochgeladene Datei eingeben oder zuordnen</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Max. zulässige Dateigröße</td> 
   <td>Geben Sie die Größe der hochgeladenen Datei in Byte ein oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>


#### Hochladen eines Assets

Dieses Aktionsmodul lädt ein Asset in Ihr Adobe Experience Manager Assets-Konto hoch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ziel</td> 
   <td> <p>Wählen Sie den Ordner aus, in den Sie ein Asset hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source-Datei</td> 
   <td>Geben Sie den Namen und die Daten der Quelldatei ein oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges


* [Kopieren von Ordnern oder Assets](#copy-a-folder-or-asset)
* [Erstellen eines Datensatzes](#create-a-record)
* [Löschen von Ordnern, Assets oder Ausgabedarstellungen](#delete-a-folder-asset-or-rendition)
* [Abrufen einer Ordnerauflistung](#get-a-folder-listing)
* [Erstellen eines benutzerdefinierten API-Aufrufs](#make-a-custom-api-call)
* [Verschieben von Ordnern oder Assets](#move-a-folder-or-asset)
* [Aktualisieren eines Datensatzes](#update-a-record)



#### Kopieren von Ordnern oder Assets

Dieses Aktionsmodul kopiert einen Ordner oder ein Asset an einen anderen Speicherort in Ihrem Adobe Experience Manager Assets-Konto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> <p>Wählen Sie aus, ob Sie einen Ordner oder ein Asset kopieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordner/Asset</td> 
   <td>Wählen Sie den zu kopierenden Ordner oder das zu kopierende Asset aus oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zielpfad</td> 
   <td>Wählen Sie den Pfad für den neuen Ordner oder das neue Asset aus oder ordnen Sie ihn dem Speicherort zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name des kopierten Ordners/Assets</td> 
   <td>Geben Sie einen Namen für den neuen Ordner oder das neue Asset ein. Der in Adobe Experience Manager Assets angezeigte Ordnername ist mit dem Originalnamen identisch. Der hier eingegebene Name erscheint in der URL des neuen Ordners oder Assets.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Untergeordnete Elemente kopieren</td> 
   <td>Wenn Sie einen Ordner kopieren, aktivieren Sie diese Option, um alle Unterordner oder Assets innerhalb des Ordners zu kopieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Überschreiben</td> 
   <td>Aktivieren Sie diese Option, um alle Ordner oder Assets am Zielspeicherort zu überschreiben, die denselben Namen wie der kopierte Ordner oder das kopierte Asset haben.</td> 
  </tr> 
 </tbody> 
</table>



#### Erstellen eines Datensatzes

Dieses Aktionsmodul erstellt einen Ordner oder einen Asset-Kommentar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Objekttyp</td> 
   <td> <p>Wählen Sie aus, ob Sie einen Ordner oder einen Kommentar zu einem Asset erstellen möchten.</p> 
    <ul> 
     <li> <p>Ordner</p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p>Name</p> <p>Geben Sie einen Namen für den Ordner ein. Dieser Name wird im Dateipfad angezeigt und darf daher keine Leerzeichen oder anderen Zeichen enthalten. </p> </li> 
       <li> <p>Titel</p> <p>Geben Sie einen Titel für den Ordner ein, der anstelle des Namens angezeigt werden kann.</p> </li> 
      </ul> </li> 
     <li> <p>Asset-Kommentar</p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p>Asset-Auswahl</p> <p>Wählen Sie die ID des Assets aus, dem Sie einen Kommentar hinzufügen möchten, oder ordnen Sie sie zu.</p> </li> 
       <li> <p>Kommentar</p> <p>Geben Sie den Text des Kommentars ein.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Löschen von Ordnern, Assets oder Ausgabedarstellungen

Dieses Aktionsmodul löscht einen Ordner, ein Asset oder eine Ausgabedarstellung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> <p>Wählen Sie aus, ob Sie einen Ordner, ein Asset oder eine Ausgabedarstellung löschen möchten.</p> 
    <ul> 
     <li> <p>Ordner</p> <p>Wählen Sie den zu löschenden Ordner aus, indem Sie die Ordner unter seinem Pfad auswählen.</p> </li> 
     <li> <p>Asset</p> <p>Wählen Sie zuerst die Ordner im Pfad und dann das Asset aus, das Sie löschen möchten.</p> </li> 
     <li> <p>Ausgabedarstellung</p> <p>Wählen Sie die Ausgabedarstellung aus, indem Sie die Ordner unter ihrem Pfad auswählen.</p> <p>Geben Sie den Namen der Ausgabedarstellung ein oder mappen Sie ihn.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen einer Ordnerauflistung

Dieses Aktionsmodul ruft eine Darstellung eines vorhandenen Ordners und seiner untergeordneten Entitäten (Ordner oder Assets) ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordner</td> 
   <td>Wählen Sie den Ordner aus, den Sie abrufen möchten, oder ordnen Sie ihn zu. Um dem Pfad Unterordner hinzuzufügen, klicken Sie auf das Pluszeichen und wählen Sie den Unterordner aus.</td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt einen benutzerdefinierten API-Aufruf an die Adobe Experience Manager Assets-API durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu Ihrer Adobe Experience Manager-Basis-URL ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Methode</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kopfzeilen</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion fügt Autorisierungs-Header automatisch hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Abfragezeichenfolge</td> 
   <td> <p>Geben Sie die Abfragezeichenfolge der Anfrage ein. Klicken Sie für jedes Schlüssel/Wert-Paar <b>Element hinzufügen</b> und geben Sie den Schlüssel und den Wert ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Textkörper</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Verschieben von Ordnern oder Assets

Dieses Aktionsmodul verschiebt das Asset oder den Ordner unter dem angegebenen Pfad an einen neuen Speicherort.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> <p>Wählen Sie aus, ob Sie einen Ordner oder ein Asset verschieben möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordner/Asset</td> 
   <td>Wählen Sie den Ordner oder das Asset aus, den/das Sie verschieben möchten, oder ordnen Sie ihn/es zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zielpfad</td> 
   <td>Wählen Sie den Pfad zum Speicherort aus, an den Sie den Ordner oder das Asset verschieben möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name des verschobenen Ordners/Assets</td> 
   <td>Geben Sie einen neuen Namen für den verschobenen Ordner oder das verschobene Asset ein. Der in Adobe Experience Manager Assets angezeigte Ordnername ist mit dem Originalnamen identisch. Der hier eingegebene Name erscheint in der URL des verschobenen Ordners oder Assets.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Überschreiben</td> 
   <td>Aktivieren Sie diese Option, um alle Ordner oder Assets am Zielspeicherort zu überschreiben, die denselben Namen wie der verschobene Ordner oder das verschobene Asset haben.</td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren eines Datensatzes

Dieses Aktionsmodul aktualisiert einen vorhandenen Datensatz.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> <p>Wählen Sie aus, ob Sie Asset-Metadaten oder eine Asset-Ausgabedarstellung löschen möchten.</p> 
    <ul> 
     <li> <p>Asset-Metadaten</p> 
      <ul> 
       <li> <p>Wählen Sie das Asset aus, für das Sie Metadaten aktualisieren möchten.</p> </li> 
       <li> <p>Geben Sie den neuen Titel des Assets ein.</p> </li> 
      </ul> </li> 
     <li> <p>Asset-Ausgabedarstellung</p> 
      <ul> 
       <li> <p>Wählen Sie das Asset aus, für das Sie die Ausgabedarstellung aktualisieren möchten.</p> </li> 
       <li> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Assets (Author-API)

* [Asset löschen](#delete-asset)
* [Auftragsstatus abrufen](#get-job-status)

#### Asset löschen

Dieses Aktionsmodul löscht ein einzelnes Asset anhand seiner ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kreativelement-ID</td> 
   <td> <p>Geben Sie die ID des Assets ein, das Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">erzwingen</td> 
   <td>Aktivieren Sie diese Option, um das Löschen des Assets zu erzwingen, selbst wenn es referenziert wird.</td> 
  </tr> 
 </tbody> 
</table>

#### Auftragsstatus abrufen

Dieses Aktionsmodul ruft den aktuellen Status eines asynchronen Auftrags ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vorgangs-ID</td> 
   <td> <p>Geben Sie die ID des Auftrags ein, für den Sie den Status abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ereignisse (Autoren-API)

#### Ereignisse ansehen

Dieses Ereignismodul startet ein Trigger, wenn ein Ereignis in AEM Assets auftritt.

Das -Modul enthält ein einzelnes Feld: Webhook. Wählen Sie einen vorhandenen Webhook aus, der für diese Ereignisse verwendet werden soll, oder erstellen Sie einen neuen.

So erstellen Sie einen neuen Webhook:

1. Klicken Sie **Hinzufügen** neben dem Feld Webhook .
1. Füllen Sie die folgenden Felder aus:

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">Webhook-Name</td>
        <td>Einen Namen für diesen Webhook eingeben.</td>
       </tr>
       <tr>
         <td role="rowheader">Verbindung</td>
        <td>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</td>
       </tr>
     </tbody>
   </table>

1. Klicken Sie auf Speichern , um den Webhook zu speichern und zum Modul zurückzukehren.


### Metadaten (Autoren-API)

* [Abrufen von Asset-Metadaten](#get-asset-metadata)
* [Aktualisieren von Asset-Metadaten](#update-asset-metadata)

#### Abrufen von Asset-Metadaten

Dieses Aktionsmodul ruft Metadaten zum angegebenen Asset ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kreativelement-ID</td> 
   <td> <p>Geben Sie die ID des Assets ein, für das Sie die Metadaten abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren von Asset-Metadaten

Dieses Aktionsmodul aktualisiert Metadaten für das angegebene Asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kreativelement-ID</td> 
   <td> <p>Geben Sie die ID des Assets ein, für das Sie die Metadaten aktualisieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Updates</td> 
   <td> <p>Klicken Sie für jedes Metadatenelement, das Sie aktualisieren möchten, auf <b>Element hinzufügen</b> und wählen Sie den Vorgang aus. Andere Felder im Feld Element hinzufügen hängen von dem ausgewählten Vorgang ab.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Import (Autoren-API)

* [Ergebnisse des Importvorgangs abrufen](#get-import-job-results)
* [Abrufen des Status des Importvorgangs](#get-import-job-status)
* [Hochladen eines Assets über eine URL](#upload-an-asset-from-a-url)

#### Ergebnisse des Importvorgangs abrufen

Dieses Aktionsmodul ruft Ergebnisse für den angegebenen Importvorgang ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Importvorgang-ID</td> 
   <td> <p>Geben Sie die ID des Auftrags ein, für den Sie Ergebnisse abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen des Status des Importvorgangs

Dieses Aktionsmodul ruft den Status des angegebenen Importvorgangs ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Importvorgang-ID</td> 
   <td> <p>Geben Sie die ID des Auftrags ein, dessen Status Sie abrufen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Hochladen eines Assets über eine URL

Dieses Aktionsmodul lädt ein neues Asset hoch, indem Dateien aus den angegebenen URLs importiert werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Titel</td> 
   <td> <p>Geben Sie einen Titel für das Asset ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beschreibung</td> 
   <td> <p>Geben Sie eine Beschreibung für das Asset ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Betreff</td> 
   <td> <p>Geben Sie einen Betreff für das Asset ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ersteller</td> 
   <td> <p>Geben Sie den Ersteller des Assets ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ablaufdatum</td> 
   <td> <p>Geben Sie das Ablaufdatum für das Asset ein oder mappen Sie es.</p><p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benutzerdefinierte Metadaten</td> 
   <td> <p>Klicken Sie für jedes Element der benutzerdefinierten Metadaten, das Sie dem Asset hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Namen und den Wert der Metadaten ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordnerpfad oder -kennung</td> 
   <td> <p>Wählen Sie aus, ob Sie den Zielordner anhand des Pfads oder der ID angeben möchten, wählen Sie dann den Pfad aus oder geben Sie die ID ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zu importierende Dateien</td> 
   <td> <p>Klicken Sie für jede Datei, die Sie importieren möchten, auf <b>Element hinzufügen&lt;/&gt; und geben Sie die Details für die Datei ein. <code>Title</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"></td> 
   <td> <p></p> </td> 
  </tr> 
 </tbody> 
</table>

### Beziehungen (Autoren-API)

* [Erstellen von Asset-Beziehungen](#create-asset-relations)
* [Asset-Beziehung löschen](#create-asset-relations)
* [Asset-Beziehungstypen abrufen](#get-asset-relation-types)
* [Asset-Beziehungen abrufen](#get-asset-relations)

#### Erstellen von Asset-Beziehungen

Dieses Aktionsmodul erstellt neue Asset-Beziehungen für das ausgewählte Asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kreativelement-ID</td> 
   <td> <p>Geben Sie die Asset-ID ein, mit der Sie andere Assets verknüpfen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zugehörige Assets</td> 
   <td> <p>Klicken Sie für jedes Asset, das Sie mit dem ausgewählten Asset verknüpfen möchten, auf <b>Element hinzufügen</b> und geben Sie die Asset-ID und den Beziehungstyp ein bzw. ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Asset-Beziehung löschen

Dieses Aktionsmodul löscht eine Asset-Beziehung für ein Asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kreativelement-ID</td> 
   <td> <p>Geben Sie die Asset-ID ein, aus der Sie eine Beziehung löschen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zugehörige Assets</td> 
   <td> <p>Geben Sie den Beziehungstyp ein, den Sie löschen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Spezifische ID des zu löschenden zugehörigen Assets angeben</td> 
   <td> <p>Aktivieren Sie dieses Kontrollkästchen, wenn Sie eine bestimmte Beziehung löschen möchten. Wenn dieses Feld nicht markiert ist, werden alle Relationen des gewählten Typs gelöscht.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kennung des zugehörigen Assets</td> 
   <td> <p>Wenn Sie eine bestimmte Beziehung löschen, geben Sie die ID der Beziehung ein, die Sie löschen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### Asset-Beziehungstypen abrufen

Dieses Modul listet die Asset-Beziehungstypen auf, die für das angegebene Asset vorhanden sind.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kreativelement-ID</td> 
   <td> <p>Geben Sie die Asset-ID ein, für die Sie Beziehungstypen auflisten möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Asset-Beziehungen abrufen

Dieses Modul listet die Asset-Beziehungen für das angegebene Asset auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kreativelement-ID</td> 
   <td> <p>Geben Sie die Asset-ID ein, für die Sie Beziehungen auflisten möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beziehungstypen</td> 
   <td> <p>Geben Sie eine kommagetrennte Liste der Beziehungstypen ein, für die Sie die Beziehungen auflisten möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Ordner (Ordner-API)

* [Ordner erstellen](#create-folders)
* [Löschen eines Ordners nach ID](#delete-a-folder-by-id)
* [Löschen von Ordnern nach Pfad](#delete-folders-by-path)
* [Abrufen von Ordnervorgangsergebnissen](#get-folders-job-results)
* [Abrufen des Auftragsstatus für Ordner](#get-folders-job-status)
* [Listenordner](#list-folders)

#### Ordner erstellen

Dieses Aktionsmodul erstellt einen neuen Ordner in Adobe Experience Manager Assets.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zu erstellende Ordner</td> 
   <td> <p>Klicken Sie für jeden Ordner, den Sie erstellen möchten, auf <b>Element hinzufügen</b> und geben Sie die folgenden Informationen ein:</p>
   <ul>
   <li><b>Neuer Ordnerspeicherort</b><p>Wählen Sie den Pfad zu dem Speicherort aus, an dem Sie den neuen Ordner erstellen möchten.</p></li>
       <li> <b>Name</b> <p>Geben Sie einen Namen für den Ordner ein. Dieser Name wird im Dateipfad angezeigt und darf daher keine Leerzeichen oder anderen Zeichen enthalten. </p> </li> 
       <li> <b>Titel</b> <p>Geben Sie einen Titel für den Ordner ein, der anstelle des Namens angezeigt werden kann.</p> </li> 
   </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Löschen eines Ordners nach ID

Dieses Aktionsmodul löscht den Adobe Experience Manager Assets-Ordner mit der angegebenen ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordner-ID</td> 
   <td> Geben Sie die ID des Ordners ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Unterordner löschen</td> 
   <td> Aktivieren Sie diese Option, um den Ordner und alle zugehörigen Unterordner zu löschen.</td>
  </tr> 
 <tr> 
   <td role="rowheader">erzwingen</td> 
   <td> Aktivieren Sie diese Option, um das Löschen der Ordner zu erzwingen, selbst wenn ein Verweis vorhanden ist.</td>
  </tr> 
 </tbody> 
</table>

#### Löschen von Ordnern nach Pfad

Dieses Aktionsmodul löscht die Adobe Experience Manager Assets-Ordner unter den angegebenen Pfaden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordnerpfade</td> 
   <td>Klicken Sie für jeden Ordner, den Sie löschen möchten, auf <b>Element hinzufügen</b> und wählen Sie den Ordnerpfad aus.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Unterordner löschen</td> 
   <td> Aktivieren Sie diese Option, um den Ordner und alle zugehörigen Unterordner zu löschen.</td>
  </tr> 
 <tr> 
   <td role="rowheader">erzwingen</td> 
   <td> Aktivieren Sie diese Option, um das Löschen des Assets zu erzwingen, selbst wenn es referenziert wird.</td>
  </tr> 
 </tbody> 
</table>

#### Abrufen von Ordnervorgangsergebnissen

Dieses Modul ruft die Ergebnisse eines asynchronen Auftrags ab, der von der Adobe Experience Manager Assets-Ordner-API erstellt wurde.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vorgangs-ID</td> 
   <td> Geben Sie die ID des Auftrags ein, für den Sie Ergebnisse abrufen möchten, oder ordnen Sie sie zu.</td>
  </tr> 
 </tbody> 
</table>

#### Abrufen des Auftragsstatus für Ordner

Dieses Modul ruft den Status eines asynchronen Auftrags ab, der von der Adobe Experience Manager Assets-Ordner-API erstellt wurde.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vorgangs-ID</td> 
   <td> Geben Sie die ID des Auftrags ein, für den Sie den Status abrufen möchten, oder ordnen Sie sie zu.</td>
  </tr> 
 </tbody> 
</table>


#### Listenordner

Dieses Modul listet Unterordner des angegebenen Ordners auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Adobe Experience Manager Assets-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager Assets mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Ordnerpfad oder -kennung</td> 
   <td> <p>Wählen Sie aus, ob Sie den Zielordner anhand des Pfads oder der ID angeben möchten, wählen Sie dann den Pfad aus oder geben Sie die ID ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
i! I added a lot of modules to the AEM Assets connector and we need new documentation for them. The connector is available in the QA environment. Heres the added modules and a brief description of them, more info about them can be found in the Assets Author Api docs and the Folders Api docs. Im not fully confident that i kept all the best practices for naming things :sweat_smile:, i hope you can take a look at that as well. Let me know if theres anything i can tell about the modules and thanks again in advance!
Author API
Assets
Delete Asset
Deletes an asset when provided an Asset ID, There is a force parameter that when toggled will delete the folder regardless if it's referenced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get assets job status
Given an assets job ID will return the state that the job is currently in (PROCESSING, COMPLETED, etc.)
Events
AEM Assets events
The costumer can create a web hook in this module and register it in the Adobe admin console
Metadata
Get asset metadata
Given asset ID returns assets metadata.
Update asset metadata
Given asset ID, there are 6 patch operations that can be done with the metadata. The operations are visible in the module as well as the documentation.
Import
Get import job results
Given Job ID returns it's result.
Get import job status
Given Job ID returns its status.
Upload an asset from url
Takes global metadata which applies to all the assets and local ones which apply individually.In both it is also possible to specify custom metadata.
Also takes the folder path or folder ID to place the assets there and url-s of the assets.
Relations
Create asset relation
Given asset ID and a list of related asset ID as well as the relation types creates those relationships.
Delete asset relations
Given asset ID and relation type deletes all relations of that type. Can also specify a related asset to target only that.
 there is a checkbox that is checked by default and when unchecked reveals a field where the user can specify the related user ID.
Get asset relation types
Given asset ID returns all the relation types that the asset has.
Get asset relations
Given asset ID returns all relations. Can also specify a specific type of relation.
Folders API
Create folders
Given a list of folders with their path, name, title, creates them.
Delete a folder by ID
Given Folder ID deletes the folder. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Delete folders by path
Given a list of paths, deletes everything in them. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get folders job results
Given job ID returns its result.
Get folders job status
Given job ID returns its status.
List Folders
List folders under the given folder. In the module you can choose the root folder either by ID or by Path.
-->

