---
title: SFTP-Module
description: Mit  [!DNL Adobe Workfront Fusion SFTP]  Modulen können Sie Dateiänderungen in einem ausgewählten Ordner/Unterordner überwachen, neue Dateien in den gewünschten Ordner hochladen, vorhandene Dateien, die sich bereits in einem Ordner befinden, ändern oder löschen oder Dateiberechtigungen ändern.
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2216'
ht-degree: 0%

---

# SFTP-Module

Mit den Adobe Workfront Fusion SFTP-Modulen können Sie Dateiänderungen in einem ausgewählten Ordner/Unterordner überwachen, neue Dateien in den gewünschten Ordner hochladen, vorhandene Dateien ändern oder löschen, die sich bereits in einem Ordner befinden, oder Dateiberechtigungen ändern.

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung</p>
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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um SFTP mit Workfront Fusion verwenden zu können, benötigen Sie ein SFTP-Konto (z. B. [!DNL GoDaddy] Web-Hosting).

## Verbinden von SFTP mit Workfront Fusion {#connect-sftp-to-workfront-fusion}

Um Ihr SFTP-Konto mit Workfront Fusion zu verbinden, müssen Sie eine Verbindung erstellen, die den Ziel-Host und die SFTP-Anmeldeinformationen (Benutzername und Kennwort oder Benutzername und Schlüssel) angibt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindungsname]</td> 
   <td> <p> Geben Sie den Namen für Ihre SFTP-Verbindung ein.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Umgebung]</td>
    <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Typ]</td>
    <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</td>
  </tr>
  <tr>
   <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
   <td> <p>Geben Sie den Host-Namen des SFTP-Servers ein, zu dem Sie eine Verbindung herstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Port] </td> 
   <td> <p>Geben Sie den SFTP-Server-Port ein. Beispiel: 22.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Authentifizierungstyp]</p> </td> 
   <td> <p>Wählen Sie die Autorisierungsmethode aus, die Sie für die Verbindung mit dem SFTP-Server verwenden möchten.</p> 
    <ul> 
     <li><strong>[!UICONTROL Benutzername und Kennwort]</strong>: Geben Sie Ihre Anmeldedaten ein.</li> 
     <li> <p><strong>[!UICONTROL Benutzername und Schlüssel]</strong>: Geben Sie Ihren Benutzernamen und den privaten Schlüssel/das Zertifikat ein</p> <p>Laden Sie den privaten Schlüssel hoch, um die Client-seitige Autorisierung zu verwenden, oder laden Sie Ihr Zertifikat (P12- oder PFX-Datei) hoch, wenn Sie TLS mit Ihrem selbstsignierten Zertifikat verwenden möchten. Wenn Sie die Client-seitige Zertifikatautorisierung verwenden, können Sie Ihr CA-Zertifikat hier eingeben.</p> <p>Workfront Fusion speichert und speichert keine Daten (Dateien, Passwörter), die Sie hier angeben. Datei und Passwort werden nur zum Extrahieren eines privaten Schlüssels/Zertifikats verwendet.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Schlüsselaustauschalgorithmen] </td> 
   <td> <p>Sie können eine Reihe von Algorithmen für den Schlüsselaustausch eingeben. Das Modul priorisiert Algorithmen basierend auf der Reihenfolge, in der sie hinzugefügt wurden. Klicken Sie für jeden Algorithmus, den Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und wählen Sie den Algorithmus aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Chiffren] </td> 
   <td> <p>Sie können einen Satz von Chiffren für den Schlüsselaustausch eingeben. Das Modul priorisiert Chiffren basierend auf der Reihenfolge, in der sie hinzugefügt wurden. Klicken Sie für jede Chiffre, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und wählen Sie die Chiffre aus.</p> </td> 
  </tr> 
 </tbody> 
</table>

Klicken Sie nach Eingabe der Verbindungsinformationen auf **[!UICONTROL Weiter]**, um eine Verbindung herzustellen.

### Unterstützte Verbindungsoptionen

Der SFTP-Connector unterstützt beim Erstellen einer Verbindung Folgendes:

#### Schlüsselaustauschalgorithmen (KEX)

* `ecdh-sha2-nistp256`
* `ecdh-sha2-nistp384`
* `ecdh-sha2-nistp521`
* `diffie-hellman-group-exchange-sha256`
* `diffie-hellman-group14-sha256`
* `diffie-hellman-group16-sha512`
* `diffie-hellman-group18-sha512`
* `diffie-hellman-group14-sha1`

#### Chiffren

* `aes256-gcm@openssh.com`
* `aes256-gcm`
* `aes128-gcm@openssh.com`
* `aes128-gcm`
* `aes256-ctr`
* `aes192-ctr`
* `aes128-ctr`
* `aes256-cbc`
* `aes192-cbc`
* `aes128-cbc`
* `blowfish-cbc`

#### Schlüsselformate für Server-Hosts

* `ssh-ed25519`
* `ecdsa-sha2-nistp256`
* `ecdsa-sha2-nistp384`
* `ecdsa-sha2-nistp521`
* `ssh-rsa`
* `ssh-dss`
<!--
* `rsa-sha2-256`
* `rsa-sha2-512`
-->

## [!UICONTROL SFTP]-Module und ihre Felder

Beim Konfigurieren von [!UICONTROL SFTP]-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können zusätzliche [!UICONTROL SFTP]-Felder angezeigt werden, abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Trigger

* [Überwachen von Dateien in einem Ordner](#watch-files-in-a-folder)
* [Überwachen von Unterordnern in einem Ordner](#watch-subfolders-in-a-folder)

#### [!UICONTROL Dateien in einem Ordner ansehen]

Gibt Dateien mit Details zurück, wenn eine Datei in einem angegebenen Ordner erstellt oder geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Ordner] </td> 
   <td> <p>Geben Sie den Ordner ein, den Sie beobachten möchten. Sie können einen absoluten Pfad wie <code>/home/user/</code> angeben oder einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>Puffergröße [b]</td> 
   <td> <p> Geben Sie die Puffergröße in Byte ein. Der Wert definiert die Größe der vom Server übertragenen Blöcke. Einige Server können Probleme verursachen oder Dateien beschädigen, wenn der Wert zu hoch ist.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Dateien]</td> 
   <td> <p> Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Überwachen von Unterordnern in einem Ordner]

Gibt Ordner mit Details zurück, wenn ein Ordner in einem angegebenen Ordner erstellt oder geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Ordner] </td> 
   <td> <p>Geben Sie den Ordner ein, den Sie beobachten möchten, oder ordnen Sie ihn zu. Sie können einen absoluten Pfad wie <code>/home/user/</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Dateien]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [Erstellen eines Ordners](#create-a-folderr)
* [Löschen einer Datei](#delete-a-file)
* [Löschen eines Ordners](#delete-a-folder)
* [Datei abrufen](#get-a-file)
* [Dateien abrufen](#get-files)
* [Auflisten des Inhalts eines Ordners](#list-a-folders-content)
* [Verschieben einer Datei](#move-a-file)
* [Umbenennen einer Datei](#rename-a-file)
* [Aktualisieren von Dateiberechtigungen](#update-file-permissions)
* [Datei hochladen](#upload-a-file)

#### [!UICONTROL Erstellen eines Ordners]

Dieses Aktionsmodul erstellt einen neuen Ordner am angegebenen Speicherort.

>[!NOTE]
>
>Wenn der Ordner bereits vorhanden ist, gibt das Modul einen Fehler aus. Um den Fluss ununterbrochen fortzusetzen, fügen Sie eine Fehler-Handler-Route an das Modul an, um den Fehler zu erfassen, und verwenden Sie die [!UICONTROL Resume]-Direktive, um den Fluss fortzusetzen. Informationen zum Anhängen einer Fehler-Handler-Route finden Sie unter [Fehlerbehandlung in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md). Informationen zur Fehler-Handler-Route finden Sie unter [Anweisungen für die Fehlerbehandlung in Adobe Workfront Fusion](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Ordner] </td> 
   <td> <p>Geben Sie einen vorhandenen Ordner als Speicherort für den neuen Ordner an. Sie können einen absoluten Pfad wie <code>/home/user/file.txt</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordnername]</td> 
   <td> <p> Geben Sie den Ordnernamen ein.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL -Berechtigungen]</p> </td> 
   <td> <p>Festlegen der gewünschten Ordnerberechtigungen. Verwenden Sie chmod-Parameter. Beispiel: <code>777</code> oder <code>-rwxrwxrwx</code>.</p> <p>Diese Berechtigungen müssen dem Muster entsprechen <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Weitere Informationen zu chmod finden Sie in der <a href="https://ss64.com/bash/chmod.html">chmod-Dokumentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei löschen]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dateipfad]</td> 
   <td> <p> Geben Sie den Pfad zu der Datei ein, die Sie löschen möchten. Sie können einen absoluten Pfad wie <code>/home/user/file.txt</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Löschen eines Ordners]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Folder Path]</td> 
   <td> <p> Geben Sie den Pfad zum Ordner an, den Sie löschen möchten. Sie können einen absoluten Pfad wie <code>/home/user/</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei abrufen]

Dieses Modul ruft Dateidetails ab, einschließlich der Daten einer Datei.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Puffergröße [B]]</td> 
   <td> <p> Geben Sie die Puffergröße in Byte ein. Der Wert definiert die Größe der vom Server übertragenen Blöcke. Einige Server können Probleme verursachen oder Dateien beschädigen, wenn der Wert zu hoch ist.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dateipfad] </td> 
   <td> <p>Geben Sie den Pfad zur Datei ein. Sie können einen absoluten Pfad wie <code>/home/user/file.txt</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dateien abrufen]

Dieses Modul gibt Dateien aus einem angegebenen Ordner zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Puffergröße [B]]</td> 
   <td> <p> Geben Sie die Puffergröße in Byte ein. Der Wert definiert die Größe der vom Server übertragenen Blöcke. Einige Server können Probleme verursachen oder Dateien beschädigen, wenn der Wert zu hoch ist.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Ordner] </td> 
   <td> <p>Geben Sie den Ordner ein, der die Dateien oder Ordner enthält, die Sie auflisten möchten, oder ordnen Sie ihn zu. Sie können einen absoluten Pfad wie <code>/home/user/</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suche] </td> 
   <td> <p>Geben Sie den Suchbegriff ein oder ordnen Sie ihn zu. Wenn Sie beispielsweise nach Dateien mit der Dateierweiterung .txt suchen möchten, geben Sie <code>.txt</code> ein. Sie können auch den Namen der Datei eingeben oder zuordnen, nach der Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL sortieren nach]</td> 
   <td> <p> Wählen Sie aus, ob die Ergebnisse nach Dateiname, Größe, Datum des letzten Zugriffs oder Datum der letzten Änderung sortiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sortierreihenfolge]</td> 
   <td> <p> Wählen Sie aus, ob das Ergebnis in auf- oder absteigender Reihenfolge zurückgegeben werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Die Routenausführung auch dann fortsetzen, wenn das Modul keine Ergebnisse zurückgibt]</p> </td> 
   <td>Aktivieren Sie diese Option, um sicherzustellen, dass das Modul das Szenario nicht beendet, wenn es keine Ergebnisse zurückgibt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Den Inhalt eines Ordners auflisten]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Anzeigen] </td> 
   <td> <p>Wählen Sie aus, ob Sie Dateien, Ordner oder beides abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Ordner] </td> 
   <td> <p>Geben Sie den Ordner ein, der die Dateien oder Ordner enthält, die Sie auflisten möchten, oder ordnen Sie ihn zu. Sie können einen absoluten Pfad wie <code>/home/user/</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suche] </td> 
   <td> <p>Geben Sie den Suchbegriff ein oder ordnen Sie ihn zu. Wenn Sie beispielsweise nach Dateien mit der Dateierweiterung .txt suchen möchten, geben Sie <code>.txt</code> ein. Sie können auch den Namen der Datei eingeben oder zuordnen, nach der Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL sortieren nach]</td> 
   <td> <p> Wählen Sie aus, ob die Ergebnisse nach Dateiname, Größe, Datum des letzten Zugriffs oder Datum der letzten Änderung sortiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sortierreihenfolge] </td> 
   <td> <p>Wählen Sie aus, ob das Ergebnis in auf- oder absteigender Reihenfolge zurückgegeben werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Die Routenausführung auch dann fortsetzen, wenn das Modul keine Ergebnisse zurückgibt]</p> </td> 
   <td>Aktivieren Sie diese Option, um sicherzustellen, dass das Modul das Szenario nicht beendet, wenn es keine Ergebnisse zurückgibt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Ergebnisse]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Verschieben einer Datei]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dateipfad]</td> 
   <td> <p> Geben Sie den Pfad zur zu verschiebenden Datei ein. Sie können einen absoluten Pfad wie <code>/home/user/file.txt</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Neuer Ordner]</td> 
   <td> <p> Geben Sie den Pfad zum neuen Speicherort der Datei ein. Sie können einen absoluten Pfad wie <code>/home/user/</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei umbenennen]

Benennt eine Datei um.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dateipfad]</td> 
   <td> <p> Geben Sie den Pfad zu der Datei ein, die Sie umbenennen möchten. Sie können einen absoluten Pfad wie <code>/home/user/file.txt</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Neuer Dateiname]</td> 
   <td> <p> Geben Sie den neuen Namen für die Datei ein, einschließlich der Dateierweiterung.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren von Dateiberechtigungen]

Ermöglicht das Ändern der Dateiberechtigungen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dateipfad]</td> 
   <td> <p> Geben Sie den Pfad zur zu verschiebenden Datei ein. Sie können einen absoluten Pfad wie <code>/home/user/file.txt</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL -Berechtigungen]</p> </td> 
   <td> <p>Legen Sie die gewünschten Dateiberechtigungen fest. Verwenden Sie chmod-Parameter. Beispiel: <code>777</code> oder <code>-rwxrwxrwx</code>.</p> <p>Diese Berechtigungen müssen dem Muster entsprechen <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Weitere Informationen zu chmod finden Sie in der <a href="https://ss64.com/bash/chmod.html">chmod-Dokumentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei hochladen]

Mit diesem Modul können Sie eine Datei auf den SFTP-Server hochladen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td>
   <td> <p>Anweisungen zum Verbinden Ihres SFTP-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Verbinden von SFTP mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Ordner] </td> 
   <td> <p>Geben Sie einen vorhandenen Ordner als Speicherort für die Datei an. Sie können einen absoluten Pfad wie <code>/home/user/</code> angeben. Sie können auch einen relativen Pfad angeben, der auf einen bestimmten Ordner des angemeldeten Benutzers verweist, z. B. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source-Datei]</td> 
   <td> <p> Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL -Berechtigungen]</p> </td> 
   <td> <p>Legen Sie die gewünschten Berechtigungen für die Datei oder den Ordner fest. Verwenden Sie chmod-Parameter. Beispiel: <code>777</code> oder <code>-rwxrwxrwx</code>.</p> <p>Diese Berechtigungen müssen dem Muster entsprechen <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Weitere Informationen zu chmod finden Sie in der <a href="https://ss64.com/bash/chmod.html">chmod-Dokumentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Puffergröße (B)]</p> </td> 
   <td> <p>Legen Sie die Größe (in Byte) jedes Blocks beim Hochladen der Datei fest. Dies ist bei großen Dateien oder dann nützlich, wenn die Speicherbeschränkungen des Servers kleinere Uploads erfordern. Wenn dieser Wert nicht festgelegt ist, wird die Datei in einem einzigen Vorgang geschrieben.</p> </td> 
  </tr> 
 </tbody> 
</table>
