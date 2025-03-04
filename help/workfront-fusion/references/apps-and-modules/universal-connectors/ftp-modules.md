---
title: FTP-Module
description: Mit FTP-Modulen können Sie Dateiänderungen in einem ausgewählten Ordner überwachen, neue Dateien in den gewünschten Ordner hochladen und vorhandene Dateien, die sich bereits in einem Ordner befinden, ändern oder löschen.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: c5e9c643c828e5556e386a5f46e1d17680b7d4e9
workflow-type: tm+mt
source-wordcount: '1328'
ht-degree: 0%

---

# FTP-Module

Mit FTP-Modulen können Sie Dateiänderungen in einem ausgewählten Ordner überwachen, neue Dateien in den gewünschten Ordner hochladen und vorhandene Dateien, die sich bereits in einem Ordner befinden, ändern oder löschen.

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

## Voraussetzungen

Um FTP-Module verwenden zu können, benötigen Sie ein FTP-Konto.

## Erstellen einer Verbindung in einem FTP-Modul {#create-a-connection}

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Verbindungsname]</td> 
   <td> <p> Geben Sie den Namen für Ihre FTP-Verbindung ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Host] </td> 
   <td> <p>Geben Sie den Host-Namen des FTP-Servers ein. E.g. <code>myftp123.server.com</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Port] </td> 
   <td> <p>Geben Sie die Port-Nummer des FTP-Servers ein. E.g. <code>21</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Benutzername] </td> 
   <td> <p>Geben Sie den Benutzernamen Ihres FTP-Kontos ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Kennwort] </td> 
   <td> <p>Geben Sie Ihr FTP-Kontokennwort ein.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Sichere Verbindung (TLS) verwenden</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie eine sichere Verbindung verwenden möchten.</p> <p style="font-weight: bold;">[!UICONTROL Nein]</p> <p>Die Verbindung ist nicht gesichert.</p> <p style="font-weight: bold;">[!UICONTROL Explizite Verschlüsselung oder implizite Verschlüsselung]</p> <p>Die Verbindung wird mit SSL gesichert.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Nicht autorisierte Zertifikate ablehnen]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um das FTP-Server-Zertifikat zu überprüfen. Wenn die Verifizierung fehlschlägt, wird die Verbindung nicht hergestellt. Um die Prüfung bestehen zu können, muss die Bescheinigung eines der folgenden Kriterien erfüllen:</p> 
    <ul> 
     <li>von einer Root-Zertifizierungsstelle <a href="https://en.wikipedia.org/wiki/Certificate_authority"> werden</a></li> 
     <li>von einer zwischengeschalteten Zertifizierungsstelle unterzeichnet werden (weitere Erläuterungen finden Sie unter <a href="https://knowledge.digicert.com/solution/SO16297.html">So funktionieren Zertifikatsketten</a>). In diesem Fall sollten alle Zwischenzertifikate auf dem FTP-Server installiert werden.</li> 
     <li>ein selbstsigniertes Zertifikat sein, das im Feld [!UICONTROL Selbstsigniertes Zertifikat] angegeben ist (siehe unten)</li> </ul>

Wenn diese Option deaktiviert ist, wird das FTP-Serverzertifikat nicht verifiziert. Wir raten dringend davon ab, die Option zu deaktivieren, da sie die Verbindung unsicher macht und ein ernstes Sicherheitsrisiko darstellt.</td>
</tr> 
  <tr> 
   <td> <p>[!UICONTROL Selbstsigniertes Zertifikat]</p> </td> 
   <td> <p>Klicken Sie auf die Schaltfläche <b>[!UICONTROL Extract]</b>, um das Upload-Dialogfeld zu öffnen.</p> <p>Laden Sie das Zertifikat hoch, um das TLS mit Ihrem selbstsignierten Zertifikat zu verwenden. [!DNL Workfront Fusion] speichert und speichert keine von Ihnen bereitgestellten Daten, z. B. Dateien und Kennwörter. Datei und Kennwort werden nur zum Extrahieren des Zertifikats verwendet.</p> </td> 
  </tr> 
 </tbody> 
</table>

## FTP-Module und ihre Felder

* [Auslöser](#triggers)
* [Aktionen](#actions)

### Auslöser

#### [!UICONTROL Dateien ansehen]

[!UICONTROL Watch files] ist das einzige Trigger-Modul für FTP. Es überwacht den Dateiinhalt des ausgewählten Ordners. Der Trigger wird ausgeführt, wenn eine neue Datei in den angegebenen Ordner eingefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#create-a-connection" class="MCXref xref">[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-Ordner]</p> </td> 
   <td> <p>Wählen Sie den Ordner aus, den Sie beobachten möchten.</p> <p><b>Hinweis</b> Pro Szenario ist nur ein Ordner zulässig. Unterordner werden ignoriert.</p> <p><b>Tipp</b> Um mehrere Ordner zu verfolgen, erstellen Sie für jeden Ordner ein unabhängiges Szenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Dateien] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Ergebnissen fest, mit denen [!DNL Workfront Fusion] während eines Zyklus arbeiten soll. Wenn der Wert zu hoch eingestellt ist, kann die Verbindung auf der Seite des angegebenen Drittanbieterdienstes unterbrochen werden (Zeitüberschreitung). [!DNL Workfront Fusion] hat darauf keinen Einfluss. Es wird empfohlen, einen niedrigeren Wert festzulegen und entweder einen höheren Wert für die maximale Anzahl an Zyklen zu definieren oder das Szenario häufiger auszuführen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Berechtigungen ändern]](#change-permissions)
* [[!UICONTROL Erstellen eines Ordners]](#create-a-folder)
* [[!UICONTROL Datei löschen]](#delete-a-file)
* [[!UICONTROL Löschen eines Ordners]](#delete-a-folder)
* [[!UICONTROL Datei abrufen]](#get-a-file)
* [[!UICONTROL Liste der Dateien in einem Ordner]](#list-of-files-in-a-folder)
* [[!UICONTROL Verschieben einer Datei oder eines Ordners]](#move-a-file-or-folder)
* [[!UICONTROL Hochladen] einer Datei](#upload-a-file)

#### [!UICONTROL Berechtigungen ändern]

Dieses Aktionsmodul ändert die Berechtigungseinstellungen einer Datei oder eines Ordners.

<table style="width: 100%;" class="TableStyle-TableStyle-List-options-in-steps" cellspacing="0">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1" />
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2" />
   <tbody>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL-Verbindung]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-MediumGray" role="rowheader">[!UICONTROL Berechtigungseinstellungen ändern von]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-MediumGray">
               <p>Wählen Sie aus, ob Sie die Einstellungen für eine Datei oder einen Ordner ändern möchten.</p>
            </td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL Dateipfad]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Geben Sie den Dateipfad zum Ordner oder zur Datei ein oder ordnen Sie ihn zu.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-MediumGray" role="rowheader">[!UICONTROL-Berechtigungen]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-MediumGray">
               <p>Legen Sie die gewünschten Datei- oder Ordnerberechtigungen fest. Verwenden Sie die chmod-Parameter. Beispiel: <code>777 </code>oder <code>-rwxrwxrwx</code>.</p>
               <p>Berechtigungen müssen mit dem <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code> übereinstimmen.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Erstellen eines Ordners]

Dieses Aktionsmodul erstellt einen neuen Ordner.

<table style="width: 100%;" class="TableStyle-TableStyle-List-options-in-steps" cellspacing="0">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1" />
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2" />
   <tbody>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL-Verbindung]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-MediumGray" role="rowheader">[!UICONTROL Ordnerpfad]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-MediumGray">Geben Sie den Dateipfad zum neuen Ordner ein oder ordnen Sie ihn zu.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-LightGray" role="rowheader">[!UICONTROL Neuer Ordnername]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-LightGray">
               <p>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie ihn zu.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Datei löschen]

Löscht eine Datei aus dem angegebenen Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den FTP-Ordner aus, aus dem Sie eine Datei löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dateiname]</td> 
   <td> <p> Geben Sie den Dateinamen einschließlich der Dateinamenerweiterung ein. Beispiel: <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Löschen eines Ordners]

Dieses Aktionsmodul löscht den angegebenen Ordner dauerhaft.

<table style="width: 100%;" class="TableStyle-TableStyle-HeaderRow" cellspacing="15">
   <col style="width: 301px;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <col style="width: 50%;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <tbody>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-LightGray" style="font-weight: bold;">[!UICONTROL-Verbindung]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-LightGray">Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-MediumGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyB-Column1-MediumGray" style="font-weight: bold;">[!UICONTROL-Ordner]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyA-Column1-MediumGray">
               <p>Wählen Sie den FTP-Ordner aus, aus dem Sie eine Datei löschen möchten.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Datei abrufen]

Ruft eine Datei vom FTP-Server ab, die weiter verarbeitet, z.B. in den [!DNL Dropbox] hochgeladen werden kann.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#creating-the-ftp-connection" class="MCXref xref">Erstellen der FTP</a>Verbindung in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dateipfad]</td> 
   <td> <p> Geben Sie den Pfad der Datei ein, die Sie erhalten möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Liste der Dateien in einem Ordner]

Ruft Datei- und/oder Ordnerinformationen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#creating-the-ftp-connection" class="MCXref xref">Erstellen der FTP</a>Verbindung in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den FTP-Ordner aus, in dem Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Anzeigen] </td> 
   <td> <p>Wählen Sie aus, ob Sie Informationen zu Dateien, Ordnern oder beidem abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suche] </td> 
   <td> <p>Geben Sie den Suchbegriff ein. Wenn kein Suchbegriff eingegeben wird, werden alle Dateien und Ordner aus dem angegebenen Ordner abgerufen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Dateien]</td> 
   <td> <p> Legen Sie die maximale Anzahl der von diesem Modul abgerufenen Dateien fest.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Verschieben einer Datei oder eines Ordners]

Dieses Aktionsmodul verschiebt eine Datei oder einen Ordner an einen anderen Speicherort.

<table style="width: 100%;" class="TableStyle-TableStyle-HeaderRow" cellspacing="15">
   <col style="width: 301px;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <col style="width: 50%;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <tbody>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-LightGray" style="font-weight: bold;">[!UICONTROL-Verbindung]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-LightGray">Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-MediumGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-MediumGray" style="font-weight: bold;">[!UICONTROL Alter Dateipfad]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-MediumGray">
               <p>Geben Sie den Pfad ein, aus dem Sie die Datei verschieben möchten. Beispiel: <code>/folder1/document.txt</code>.</p>
            </td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyB-Column1-LightGray" style="font-weight: bold;">[!UICONTROL Neuer Dateipfad]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyA-Column1-LightGray">
               <p>Geben Sie den Pfad ein, in den Sie die Datei verschieben möchten. Beispiel: <code>/folder2/document.txt</code>.</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL Datei hochladen]

Lädt eine Datei auf den FTP-Server.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#creating-the-ftp-connection" class="MCXref xref">Erstellen der FTP</a>Verbindung in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den FTP-Ordner aus, in den Sie die Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source-Datei] </td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL An bereits vorhandene Datei anhängen]</td> 
   <td> <p>Wenn diese Option aktiviert ist und die Datei bereits auf dem FTP-Server existiert, wird der Inhalt der Datei an die vorhandene Datei angehängt. Wenn diese Option nicht aktiviert ist, wird der Inhalt der Datei überschrieben.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordner erstellen, wenn noch nicht vorhanden] </td> 
   <td> <p>Wenn diese Option aktiviert ist und der Ordner, den Sie in das Feld Ordner eingegeben haben, nicht auf dem FTP-Server existiert, erstellt das Modul den Ordner</p> </td> 
  </tr> 
 </tbody> 
</table>

## Fehlerbehebung {#troubleshooting}

Wenn bei der Erstellung einer Verbindung oder beim Vorgang eines Moduls Probleme mit der FTP-App auftreten, versuchen Sie, einen der beliebten FTP-Clients zu verwenden und dieselbe Aktion durchzuführen (z. B. eine Verbindung zu erstellen oder Dateien in einem Ordner aufzulisten). mit dem FTP-Client. Wenn dieselben Probleme auch mit dem FTP-Client auftreten, kann der Grund eine Fehlkonfiguration des FTP-Servers sein.
