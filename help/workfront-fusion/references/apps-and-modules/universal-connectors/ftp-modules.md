---
title: FTP-Module
description: Mit FTP-Modulen können Sie Dateiänderungen in einem ausgewählten Ordner überwachen, neue Dateien in den gewünschten Ordner hochladen und vorhandene Dateien, die sich bereits in einem Ordner befinden, ändern oder löschen.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%

---

# FTP-Module

Mit FTP-Modulen können Sie Dateiänderungen in einem ausgewählten Ordner überwachen, neue Dateien in den gewünschten Ordner hochladen und vorhandene Dateien, die sich bereits in einem Ordner befinden, ändern oder löschen.

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

Um die [Fusion-App] mit [!DNL Workfront Fusion] verwenden zu können, benötigen Sie ein FTP-Konto.

## Erstellen einer Verbindung in einem FTP-Modul {#create-a-connection}

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection name]</td> 
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
   <td>[!UICONTROL User name] </td> 
   <td> <p>Geben Sie den Benutzernamen Ihres FTP-Kontos ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Password] </td> 
   <td> <p>Geben Sie Ihr FTP-Kontokennwort ein.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Sichere Verbindung (TLS) verwenden</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie eine sichere Verbindung verwenden möchten.</p> <p style="font-weight: bold;">[!UICONTROL No]</p> <p>Die Verbindung ist nicht gesichert.</p> <p style="font-weight: bold;">[!UICONTROL Explicit encryption or Implicit encryption]</p> <p>Die Verbindung wird mit SSL gesichert.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Reject unauthorized certificates]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um das FTP-Server-Zertifikat zu überprüfen. Wenn die Verifizierung fehlschlägt, wird die Verbindung nicht hergestellt. Um die Prüfung bestehen zu können, muss die Bescheinigung eines der folgenden Kriterien erfüllen:</p> 
    <ul> 
     <li>von einer Root-Zertifizierungsstelle <a href="https://en.wikipedia.org/wiki/Certificate_authority"> werden</a></li> 
     <li>von einer zwischengeschalteten Zertifizierungsstelle unterzeichnet werden (weitere Erläuterungen finden Sie unter <a href="https://knowledge.digicert.com/solution/SO16297.html">So funktionieren Zertifikatsketten</a>). In diesem Fall sollten alle Zwischenzertifikate auf dem FTP-Server installiert werden.</li> 
     <li>ein selbstsigniertes Zertifikat sein, das im Feld [!UICONTROL Self-signed certificate] angegeben wird (siehe unten)</li> </ul>

Wenn diese Option deaktiviert ist, wird das FTP-Serverzertifikat nicht verifiziert. Wir raten dringend davon ab, die Option zu deaktivieren, da sie die Verbindung unsicher macht und ein ernstes Sicherheitsrisiko darstellt.</td>
</tr> 
  <tr> 
   <td> <p>[!UICONTROL Self-signed certificate]</p> </td> 
   <td> <p>Klicken Sie auf die Schaltfläche <b>[!UICONTROL Extract]</b> , um das Dialogfeld Hochladen zu öffnen.</p> <p>Laden Sie das Zertifikat hoch, um das TLS mit Ihrem selbstsignierten Zertifikat zu verwenden. [!DNL Workfront Fusion] speichert und speichert keine von Ihnen bereitgestellten Daten, z. B. Dateien und Kennwörter. Datei und Kennwort werden nur zum Extrahieren des Zertifikats verwendet.</p> </td> 
  </tr> 
 </tbody> 
</table>

## FTP-Module und ihre Felder

* [Trigger](#triggers)
* [Aktionen](#actions)

### Trigger

#### [!UICONTROL Watch files]

[!UICONTROL Watch files] ist das einzige Trigger-Modul für FTP. Es überwacht den Dateiinhalt des ausgewählten Ordners. Der Trigger wird ausgeführt, wenn eine neue Datei in den angegebenen Ordner eingefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#create-a-connection" class="MCXref xref">[!UICONTROL Create a connection] in einem FTP-Modul</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Folder]</p> </td> 
   <td> <p>Wählen Sie den Ordner aus, den Sie beobachten möchten.</p> <p><b>Hinweis</b> Pro Szenario ist nur ein Ordner zulässig. Unterordner werden ignoriert.</p> <p><b>Tipp</b> Um mehrere Ordner zu verfolgen, erstellen Sie für jeden Ordner ein unabhängiges Szenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Ergebnissen fest, mit denen [!DNL Workfront Fusion] während eines Zyklus arbeiten soll. Wenn der Wert zu hoch eingestellt ist, kann die Verbindung auf der Seite des angegebenen Drittanbieterdienstes unterbrochen werden (Zeitüberschreitung). [!DNL Workfront Fusion] hat darauf keinen Einfluss. Es wird empfohlen, einen niedrigeren Wert festzulegen und entweder einen höheren Wert für die maximale Anzahl an Zyklen zu definieren oder das Szenario häufiger auszuführen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Change permissions]](#change-permissions)
* [[!UICONTROL Create a folder]](#create-a-folder)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Delete a folder]](#delete-a-folder)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL List of files in a folder]](#list-of-files-in-a-folder)
* [[!UICONTROL Move a file or folder]](#move-a-file-or-folder)
* [Datei [!UICONTROL Upload]](#upload-a-file)

#### [!UICONTROL Change permissions]

Dieses Aktionsmodul ändert die Berechtigungseinstellungen einer Datei oder eines Ordners.

<table style="width: 100%;" class="TableStyle-TableStyle-List-options-in-steps" cellspacing="0">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1" />
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2" />
   <tbody>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-MediumGray" role="rowheader">[!UICONTROL Change permission settings of]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-MediumGray">
               <p>Wählen Sie aus, ob Sie die Einstellungen für eine Datei oder einen Ordner ändern möchten.</p>
            </td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL File path]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Geben Sie den Dateipfad zum Ordner oder zur Datei ein oder ordnen Sie ihn zu.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-MediumGray" role="rowheader">[!UICONTROL Permissions]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-MediumGray">
               <p>Legen Sie die gewünschten Datei- oder Ordnerberechtigungen fest. Verwenden Sie die chmod-Parameter. Beispiel: <code>777 </code>oder <code>-rwxrwxrwx</code>.</p>
               <p>Berechtigungen müssen mit dem <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code> übereinstimmen.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Create a folder]

Dieses Aktionsmodul erstellt einen neuen Ordner.

<table style="width: 100%;" class="TableStyle-TableStyle-List-options-in-steps" cellspacing="0">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1" />
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2" />
   <tbody>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-MediumGray" role="rowheader">[!UICONTROL Folder path]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-MediumGray">Geben Sie den Dateipfad zum neuen Ordner ein oder ordnen Sie ihn zu.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-LightGray" role="rowheader">[!UICONTROL New folder name]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-LightGray">
               <p>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie ihn zu.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Delete a file]

Löscht eine Datei aus dem angegebenen Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in einem FTP-Modul</a> in diesem Artikel.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den FTP-Ordner aus, aus dem Sie eine Datei löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td> <p> Geben Sie den Dateinamen einschließlich der Dateinamenerweiterung ein. Beispiel: <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

Dieses Aktionsmodul löscht den angegebenen Ordner dauerhaft.

<table style="width: 100%;" class="TableStyle-TableStyle-HeaderRow" cellspacing="15">
   <col style="width: 301px;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <col style="width: 50%;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <tbody>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-LightGray" style="font-weight: bold;">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-LightGray">Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-MediumGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyB-Column1-MediumGray" style="font-weight: bold;">[!UICONTROL Folder]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyA-Column1-MediumGray">
               <p>Wählen Sie den FTP-Ordner aus, aus dem Sie eine Datei löschen möchten.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Get a file]

Ruft eine Datei vom FTP-Server ab, die weiter verarbeitet, z.B. in den [!DNL Dropbox] hochgeladen werden kann.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#creating-the-ftp-connection" class="MCXref xref">Erstellen der FTP</a>Verbindung in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File path]</td> 
   <td> <p> Geben Sie den Pfad der Datei ein, die Sie erhalten möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List of files in a folder]

Ruft Datei- und/oder Ordnerinformationen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#creating-the-ftp-connection" class="MCXref xref">Erstellen der FTP</a>Verbindung in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den FTP-Ordner aus, in dem Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>Wählen Sie aus, ob Sie Informationen zu Dateien, Ordnern oder beidem abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Geben Sie den Suchbegriff ein. Wenn kein Suchbegriff eingegeben wird, werden alle Dateien und Ordner aus dem angegebenen Ordner abgerufen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> Legen Sie die maximale Anzahl der von diesem Modul abgerufenen Dateien fest.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a file or folder]

Dieses Aktionsmodul verschiebt eine Datei oder einen Ordner an einen anderen Speicherort.

<table style="width: 100%;" class="TableStyle-TableStyle-HeaderRow" cellspacing="15">
   <col style="width: 301px;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <col style="width: 50%;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <tbody>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-LightGray" style="font-weight: bold;">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-LightGray">Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-MediumGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-MediumGray" style="font-weight: bold;">[!UICONTROL Old file path]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-MediumGray">
               <p>Geben Sie den Pfad ein, aus dem Sie die Datei verschieben möchten. Beispiel: <code>/folder1/document.txt</code>.</p>
            </td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyB-Column1-LightGray" style="font-weight: bold;">[!UICONTROL New file path]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyA-Column1-LightGray">
               <p>Geben Sie den Pfad ein, in den Sie die Datei verschieben möchten. Beispiel: <code>/folder2/document.txt</code>.</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL Upload a file]

Lädt eine Datei auf den FTP-Server.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#creating-the-ftp-connection" class="MCXref xref">Erstellen der FTP</a>Verbindung in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den FTP-Ordner aus, in den Sie die Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file] </td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Append to an already existing file]</td> 
   <td> <p>Wenn diese Option aktiviert ist und die Datei bereits auf dem FTP-Server existiert, wird der Inhalt der Datei an die vorhandene Datei angehängt. Wenn diese Option nicht aktiviert ist, wird der Inhalt der Datei überschrieben.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create folders if don't exist] </td> 
   <td> <p>Wenn diese Option aktiviert ist und der Ordner, den Sie in das Feld Ordner eingegeben haben, nicht auf dem FTP-Server existiert, erstellt das Modul den Ordner</p> </td> 
  </tr> 
 </tbody> 
</table>

## Fehlerbehebung {#troubleshooting}

Wenn bei der Erstellung einer Verbindung oder beim Vorgang eines Moduls Probleme mit der FTP-App auftreten, versuchen Sie, einen der beliebten FTP-Clients zu verwenden und dieselbe Aktion durchzuführen (z. B. eine Verbindung zu erstellen oder Dateien in einem Ordner aufzulisten). mit dem FTP-Client. Wenn dieselben Probleme auch mit dem FTP-Client auftreten, kann der Grund eine Fehlkonfiguration des FTP-Servers sein.
