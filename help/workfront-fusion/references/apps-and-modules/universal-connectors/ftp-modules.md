---
title: FTP-Module
description: Mit FTP-Modulen können Sie Dateiänderungen in einem ausgewählten Ordner überwachen, neue Dateien in den gewünschten Ordner hochladen und vorhandene Dateien, die sich bereits in einem Ordner befinden, ändern oder löschen.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: 54c368d335b30f55cab19595a5b4740dde6013a7
workflow-type: tm+mt
source-wordcount: '1397'
ht-degree: 0%

---

# FTP-Module

Mit FTP-Modulen können Sie Dateiänderungen in einem ausgewählten Ordner überwachen, neue Dateien in den gewünschten Ordner hochladen und vorhandene Dateien, die sich bereits in einem Ordner befinden, ändern oder löschen.

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

Um FTP-Module verwenden zu können, müssen Sie über ein Konto mit einem FTP-Dienst verfügen.

## Erstellen einer Verbindung in einem FTP-Modul {#create-a-connection}

1. Klicken Sie in einem beliebigen FTP **Modul** Hinzufügen“ neben dem Verbindungsfeld.
1. Füllen Sie die folgenden Felder aus.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Verbindungsname]</td> 
      <td> <p> Geben Sie den Namen für Ihre FTP-Verbindung ein.</p> </td> 
     </tr> 
     <tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Umgebung]</p> </td> 
      <td> <p>Wählen Sie aus, ob Sie eine Produktions- oder eine Nicht-Produktionsumgebung verwenden.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Typ]</p> </td> 
      <td> <p>Wählen Sie aus, ob Sie ein Service-Konto oder ein persönliches Konto verwenden.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Host] </td> 
      <td> <p>Geben Sie den Host-Namen des FTP-Servers ein. Beispiel: <code>myftp123.server.com</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Port] </td> 
      <td> <p>Geben Sie die Port-Nummer des FTP-Servers ein. Beispiel: <code>21</code></p> </td> 
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
      <td> <p>Wählen Sie aus, ob Sie eine sichere Verbindung verwenden möchten.</p> <ul><li><p><b>[!UICONTROL Nein]</b></p> <p>Die Verbindung ist nicht gesichert.</p></li><li> <p><b>Explizite Verschlüsselung</b> oder <b>Implizite Verschlüsselung</b></p> <p>Die Verbindung wird mit SSL gesichert.</p> </td> 
     </tr> 
    <tr> 
   <td> <p>[!UICONTROL Nicht autorisierte Zertifikate ablehnen]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um das FTP-Server-Zertifikat zu überprüfen. Wenn die Verifizierung fehlschlägt, wird die Verbindung nicht hergestellt. Um die Prüfung bestehen zu können, muss die Bescheinigung eines der folgenden Kriterien erfüllen:</p> 
    <ul> 
     <li>von einer Root-Zertifizierungsstelle signiert werden</a></li> 
     <li>von einer zwischengeschalteten Zertifizierungsstelle unterzeichnet werden. In diesem Fall sollten alle Zwischenzertifikate auf dem FTP-Server installiert werden.</li> 
     <li>ein selbstsigniertes Zertifikat sein, das im Feld [!UICONTROL Selbstsigniertes Zertifikat] angegeben ist (siehe unten)</li> </ul>
     <p>Wenn diese Option deaktiviert ist, wird das FTP-Serverzertifikat nicht verifiziert. Wir raten dringend davon ab, die Option zu deaktivieren, da sie die Verbindung unsicher macht und ein ernstes Sicherheitsrisiko darstellt.</p></td>
    </tr> 
    <tr> 
     <td> <p>[!UICONTROL Selbstsigniertes Zertifikat]</p> </td> 
     <td> <p>Klicken Sie auf die Schaltfläche <b>[!UICONTROL Extract]</b>, um das Upload-Dialogfeld zu öffnen.</p> <p>Laden Sie das Zertifikat hoch, um das TLS mit Ihrem selbstsignierten Zertifikat zu verwenden. Workfront Fusion speichert und speichert keine von Ihnen bereitgestellten Daten wie Dateien und Kennwörter. Datei und Kennwort werden nur zum Extrahieren des Zertifikats verwendet.</p> </td> 
    </tr> 
   </tbody> 
   </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## FTP-Module und ihre Felder

* [Trigger](#triggers)
* [Aktionen](#actions)

### Trigger

#### [!UICONTROL Dateien ansehen]

[!UICONTROL Watch files] ist das einzige Trigger-Modul für FTP. Es überwacht den Dateiinhalt des ausgewählten Ordners. Der Trigger wird ausgeführt, wenn dem angegebenen Ordner eine neue Datei hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#create-a-connection" class="MCXref xref">[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL -Ordner]</p> </td> 
   <td> <p>Wählen Sie den Ordner aus, den Sie beobachten möchten.</p> <p><b>Hinweis</b> Pro Szenario ist nur ein Ordner zulässig. Unterordner werden ignoriert.</p> <p><b>Tipp</b> Um mehrere Ordner anzusehen, erstellen Sie für jeden Ordner ein eigenes Szenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Dateien] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Ergebnissen fest, mit denen das Modul während eines Zyklus arbeiten soll. Wenn der Wert zu hoch eingestellt ist, kann die Verbindung auf der Seite des FTP-Servers unterbrochen werden. Workfront Fusion hat darauf keinen Einfluss. Es wird empfohlen, einen niedrigeren Wert festzulegen und entweder einen höheren Wert für die maximale Anzahl an Zyklen zu definieren oder das Szenario häufiger auszuführen.</p> </td> 
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

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL -Verbindung]</td>
            <td>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Berechtigungseinstellungen ändern von]</td>
            <td>
               <p>Wählen Sie aus, ob Sie die Einstellungen für eine Datei oder einen Ordner ändern möchten.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL Dateipfad]</td>
            <td>Geben Sie den Dateipfad zum Ordner oder zur Datei ein oder ordnen Sie ihn zu.</td>
         </tr>
         <tr>
            <td>[!UICONTROL -Berechtigungen]</td>
            <td>
               <p>Legen Sie die gewünschten Datei- oder Ordnerberechtigungen fest. Verwenden Sie die chmod-Parameter. Beispiel: <code>777 </code>oder <code>-rwxrwxrwx</code>.</p>
               <p>Berechtigungen müssen mit dem <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code> übereinstimmen.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Erstellen eines Ordners]

Dieses Aktionsmodul erstellt einen neuen Ordner.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL -Verbindung]</td>
            <td>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Ordnerpfad]</td>
            <td>Geben Sie den Dateipfad zum neuen Ordner ein oder ordnen Sie ihn zu.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Neuer Ordnername]</td>
            <td>
               <p>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie ihn zu.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Datei löschen]

Dieses Aktionsmodul löscht eine Datei aus dem angegebenen Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
            <td>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL -Ordner] </td> 
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

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL -Verbindung]</td>
            <td>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr>
            <td>[!UICONTROL -Ordner]</td>
            <td>
               <p>Wählen Sie den FTP-Ordner aus, aus dem Sie eine Datei löschen möchten.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Datei abrufen]

Dieses Aktionsmodul ruft eine Datei vom FTP-Server ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#creating-the-ftp-connection" class="MCXref xref">Erstellen der FTP</a>Verbindung in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dateipfad]</td> 
   <td> <p> Geben Sie den Pfad der Datei ein, die Sie erhalten möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Liste der Dateien in einem Ordner]

Dieses Aktionsmodul ruft Datei- und/oder Ordnerinformationen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#creating-the-ftp-connection" class="MCXref xref">Erstellen der FTP</a>Verbindung in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Ordner] </td> 
   <td> <p>Wählen Sie den FTP-Ordner aus, in dem Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Anzeigen] </td> 
   <td> <p>Wählen Sie aus, ob Sie Informationen zu Dateien, Ordnern oder beidem abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suche] </td> 
   <td> <p>Geben Sie den Suchbegriff ein. Wenn kein Suchbegriff eingegeben wird, werden alle Dateien oder Ordner aus dem angegebenen Ordner abgerufen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Dateien]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Ergebnissen ein, mit denen das Modul während eines Zyklus arbeiten soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Verschieben einer Datei oder eines Ordners]

Dieses Aktionsmodul verschiebt eine Datei oder einen Ordner an einen anderen Speicherort.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL -Verbindung]</td>
            <td>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#Create" class="MCXref xref" >[!UICONTROL Verbindung erstellen] in einem FTP-Modul</a> in diesem Artikel.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Alter Dateipfad]</td>
            <td>
               <p>Geben Sie den Pfad ein, aus dem Sie die Datei verschieben möchten. Beispiel: <code>/folder1/document.txt</code>.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL Neuer Dateipfad]</td>
            <td>
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
   <td>[!UICONTROL -Verbindung] </td> 
   <td>Anweisungen zum Herstellen einer Verbindung mit dem FTP-Konto finden Sie unter <a href="#creating-the-ftp-connection" class="MCXref xref">Erstellen der FTP</a>Verbindung in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Ordner] </td> 
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
