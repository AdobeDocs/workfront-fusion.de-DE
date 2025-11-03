---
title: Microsoft Office 365-E-Mail
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Microsoft Office 365-E-Mails verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 5d4072ba-c598-4347-a42f-c59c7add0a1b
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2921'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Email]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!UICONTROL Microsoft Office 365 Email] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um [!DNL Microsoft Office 365 Email]-Module verwenden zu können, müssen Sie über ein [!DNL Microsoft Office 365 Email]-Konto verfügen.

## Microsoft Office 365 E-Mail-API-Informationen

Der Microsoft Office 365 E-Mail-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v2.6.5</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden des [!DNL Office 365 Email]-Service mit Workfront Fusion

Anweisungen zum Verbinden Ihres [!DNL Office 365 Email]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung mit [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
>
>Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.

## [!DNL Microsoft Office 365 Email] Module und ihre Felder

Beim Konfigurieren von [!DNL Microsoft Office 365 Email] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Microsoft Office 365 Email] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Nachricht](#message)
* [Nachrichtenentwurf](#draft-message)
* [Anhang](#attachment)
* [Sonstiges](#other)

### Nachricht

* [[!UICONTROL Erstellen und Senden einer Nachricht (veraltet)]](#create-and-send-a-message)
* [[!UICONTROL Löschen einer Nachricht]](#delete-a-message)
* [[!UICONTROL Nachricht abrufen]](#get-a-message)
* [[!UICONTROL Nachricht verschieben]](#move-a-message)
* [[!UICONTROL Nachrichten suchen]](#search-messages)
* [[!UICONTROL Nachrichten ansehen]](#watch-messages)



#### [!UICONTROL Erstellen und Senden einer Nachricht (veraltet)]

Dieses Aktionsmodul erstellt und sendet eine E-Mail-Nachricht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Betreff]</td> 
   <td> <p>Geben Sie die Betreffzeile der Nachricht ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hauptteilinhalt]</td> 
   <td> <p>Geben Sie den Nachrichtentext der E-Mail ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wichtigkeit]</td> 
   <td> <p>Wichtigkeit der E-Mail auswählen</p> 
    <ul> 
     <li>[!UICONTROL Niedrig]</li> 
     <li>[!UICONTROL normal]</li> 
     <li>[!UICONTROL Hoch]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL an Empfänger]</p> </td> 
   <td> <p>Klicken Sie für jeden Empfänger, an den Sie die E-Mail senden möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Empfänger]</p> </td> 
   <td> <p><p>Klicken Sie für jeden Empfänger, an den Sie eine Kopie der E-Mail senden möchten, auf <b>Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL BCC-Empfänger]</p> </td> 
   <td> <p>Klicken Sie für jeden Empfänger, an den Sie eine Kopie der E-Mail senden möchten, ohne dass andere Empfänger ihre Namen oder E-Mail-Adressen sehen können, <b>Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anlagen]</p> </td> 
   <td> <p>Klicken Sie für jeden Anhang, den Sie der E-Mail hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source-Datei]</strong> </p> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Internet-Nachrichtenkopfzeilen]</td> 
   <td> <p>Klicken Sie für jede Kopfzeile, die Sie der E-Mail hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen der Kopfzeile ein</p> </li> 
     <li> <p><strong>[!UICONTROL value]</strong> </p> <p>Geben Sie einen Wert für die Kopfzeile ein.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Löschen einer Nachricht]

Dieses Aktionsmodul löscht eine vorhandene E-Mail-Nachricht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Von E-Mail-Adresse]</td> 
   <td> <p> Um eine freigegebene E-Mail-Adresse zu verwenden, geben Sie die Adresse hier ein. Der Benutzer, dessen Anmeldeinformationen in der für dieses Modul verwendeten Verbindung verwendet werden, muss Zugriff auf den freigegebenen Ordner haben.<p>Lassen Sie dieses Feld leer, um die E-Mail-Adresse des Verbindungseigentümers zu verwenden.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID]</td> 
   <td> <p> Wählen Sie die ID der Nachricht aus, die Sie löschen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Nachricht abrufen]

Dieses Aktionsmodul ruft die Metadaten einer bestimmten Nachricht ab

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Von E-Mail-Adresse]</td> 
   <td> <p> Um eine freigegebene E-Mail-Adresse zu verwenden, geben Sie die Adresse hier ein. Der Benutzer, dessen Anmeldeinformationen in der für dieses Modul verwendeten Verbindung verwendet werden, muss Zugriff auf den freigegebenen Ordner haben.<p>Lassen Sie dieses Feld leer, um die E-Mail-Adresse des Verbindungseigentümers zu verwenden.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID]</td> 
   <td> <p> Wählen Sie die ID der Nachricht aus, für die Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME-Inhalte abrufen]</td> 
   <td>Aktivieren Sie diese Option, um Daten über den MIME-Inhalt der Nachricht abzurufen. [!UICONTROL MIME]-Inhalte können Bilder, Audio, Video oder andere Dateitypen enthalten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Nachricht verschieben]

Dieses Aktionsmodul verschiebt eine E-Mail-Nachricht in einen ausgewählten Ordner im Postfach.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID]</td> 
   <td> <p> Wählen Sie die ID der Nachricht aus, die Sie in einen anderen Ordner verschieben möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mail-Ordner] </td> 
   <td> <p>Wählen Sie die ID des Ordners aus, in den Sie die Nachricht verschieben möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Nachrichten suchen]

Dieses Suchmodul sucht anhand bestimmter Kriterien nach Nachrichten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Von E-Mail-Adresse]</td> 
   <td> <p> Um eine freigegebene E-Mail-Adresse zu verwenden, geben Sie die Adresse hier ein. Der Benutzer, dessen Anmeldeinformationen in der für dieses Modul verwendeten Verbindung verwendet werden, muss Zugriff auf den freigegebenen Ordner haben.<p>Lassen Sie dieses Feld leer, um die E-Mail-Adresse des Verbindungseigentümers zu verwenden.</p></p> </td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Mail-Ordner]</td> 
   <td> <p>Wählen Sie den Ordner aus, der die zu durchsuchenden Nachrichten enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Suche]</td> 
   <td>Geben Sie Ihre Suchanfrage ein. Informationen zum Schreiben einer Suchanfrage finden Sie im [!DNL Microsoft] Support-Artikel <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&rs=en-us&ad=us">Search Mail and People in [!DNL Outlook.com]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortieren nach]</td> 
   <td> <p>Wählen Sie aus, wie Sie die Ergebnisse sortieren möchten:</p> 
    <ul> 
     <li>[!UICONTROL Betreff (aufsteigend oder absteigend)]</li> 
     <li>[!UICONTROL Erstellungsdatum Uhrzeit (aufsteigend oder absteigend)]</li> 
     <li>[!UICONTROL Datum der letzten Änderung (aufsteigend oder absteigend)]</li> 
     <li>[!UICONTROL Received Date Time (aufsteigend oder absteigend)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl an Nachrichten ein, die Workfront Fusion während eines Szenario-Ausführungszyklus zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Nachrichten ansehen]

Dieses Trigger-Modul startet ein Szenario, wenn eine neue E-Mail-Nachricht gesendet oder empfangen wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nachrichten ansehen]</p> </td> 
   <td> <p>Wählen Sie die Nachrichten aus, die Sie beobachten möchten:</p> 
    <ul> 
     <li>[!UICONTROL only unread]</li> 
     <li>[!UICONTROL Nur lesen]</li> 
     <li>[!UICONTROL ALL]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mail-Ordner]</td> 
   <td> <p>Wählen Sie den Ordner aus, der die Nachrichten enthält, die Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Suche]</td> 
   <td>Geben Sie Ihre Suchanfrage ein. Das -Modul gibt Nachrichten zurück, die mit dieser Abfrage übereinstimmen. Informationen zum Schreiben einer Suchanfrage finden Sie im [!DNL Microsoft] Support-Artikel <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&rs=en-us&ad=us">Search Mail and People in [!DNL Outlook.com]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Geben Sie die maximale Anzahl an Nachrichten ein, die Workfront Fusion während eines Szenario-Ausführungszyklus zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Nachrichtenentwurf

* [Nachrichtenentwurf erstellen](#create-a-draft-message)
* [Nachrichtenentwurf senden](#send-a-draft-message)
* [Aktualisieren einer Nachricht](#update-a-message)

#### [!UICONTROL Nachrichtenentwurf erstellen]

Dieses Aktionsmodul erstellt eine neue E-Mail-Nachricht als Entwurf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Betreff]</td> 
   <td> <p>Geben Sie die Betreffzeile der Nachricht ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hauptteil-Inhaltstyp]</td> 
   <td>Wählen Sie aus, ob der Nachrichtentext HTML oder Text enthält.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hauptteilinhalt]</td> 
   <td> <p>Geben Sie den Nachrichtentext der E-Mail ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wichtigkeit]</td> 
   <td> <p>Wichtigkeit der E-Mail auswählen</p> 
    <ul> 
     <li>[!UICONTROL Niedrig]</li> 
     <li>[!UICONTROL normal]</li> 
     <li>[!UICONTROL Hoch]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL an Empfänger]</p> </td> 
   <td> <p>Klicken Sie für jeden Empfänger, an den Sie die E-Mail senden möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Empfänger]</p> </td> 
   <td> <p><p>Klicken Sie für jeden Empfänger, an den Sie eine Kopie der E-Mail senden möchten, auf <b>Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL BCC-Empfänger]</p> </td> 
   <td> <p>Klicken Sie für jeden Empfänger, an den Sie eine Kopie der E-Mail senden möchten, ohne dass andere Empfänger ihre Namen oder E-Mail-Adressen sehen können, <b>Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anlagen]</p> </td> 
   <td> <p>Klicken Sie für jeden Anhang, den Sie der E-Mail hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source-Datei]</strong> </p> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Von E-Mail-Adresse]</td> 
   <td> <p> Um eine freigegebene E-Mail-Adresse zu verwenden, geben Sie die Adresse hier ein. Der Benutzer, dessen Anmeldeinformationen in der für dieses Modul verwendeten Verbindung verwendet werden, muss Zugriff auf den freigegebenen Ordner haben.<p>Lassen Sie dieses Feld leer, um die E-Mail-Adresse des Verbindungseigentümers zu verwenden.</p></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Nachrichtenentwurf senden]

Dieses Aktionsmodul sendet eine E-Mail-Nachricht, die sich derzeit im Entwurf befindet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Von E-Mail-Adresse]</td> 
   <td> <p> Um eine freigegebene E-Mail-Adresse zu verwenden, geben Sie die Adresse hier ein. Der Benutzer, dessen Anmeldeinformationen in der für dieses Modul verwendeten Verbindung verwendet werden, muss Zugriff auf den freigegebenen Ordner haben.<p>Lassen Sie dieses Feld leer, um die E-Mail-Adresse des Verbindungseigentümers zu verwenden.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entwurfs-Nachrichten-ID]</td> 
   <td> <p> Wählen Sie die Nachrichten-ID des Entwurfs aus, den Sie senden möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren einer Nachricht]

Dieses Aktionsmodul aktualisiert eine vorhandene Nachricht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Von E-Mail-Adresse]</td> 
   <td> <p> Um eine freigegebene E-Mail-Adresse zu verwenden, geben Sie die Adresse hier ein. Der Benutzer, dessen Anmeldeinformationen in der für dieses Modul verwendeten Verbindung verwendet werden, muss Zugriff auf den freigegebenen Ordner haben.<p>Lassen Sie dieses Feld leer, um die E-Mail-Adresse des Verbindungseigentümers zu verwenden.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichtenkennung eingeben]</td> 
   <td> <p>Wählen Sie aus, wie Sie die zu aktualisierende Nachricht identifizieren möchten:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Manuell eingeben]</strong> </p> <p>Geben Sie die Nachrichten-ID ein oder mappen Sie sie.</p> </li> 
     <li> <p><strong>[!UICONTROL Aus der Liste auswählen]</strong> </p> <p>Wählen Sie den Ordner aus, der die zu aktualisierende Nachricht enthält, und wählen Sie dann die Nachricht aus</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Betreff]</td> 
   <td> <p>Geben Sie die Betreffzeile der Nachricht ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Hauptteilinhalt]</td> 
   <td> <p>Geben Sie den Nachrichtentext der E-Mail ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wichtigkeit]</td> 
   <td> <p>Wichtigkeit der E-Mail auswählen</p> 
    <ul> 
     <li>[!UICONTROL Niedrig]</li> 
     <li>[!UICONTROL normal]</li> 
     <li>[!UICONTROL Hoch]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL an Empfänger]</p> </td> 
   <td> <p>Klicken Sie für jeden Empfänger, an den Sie die E-Mail senden möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Empfänger]</p> </td> 
   <td> <p><p>Klicken Sie für jeden Empfänger, an den Sie eine Kopie der E-Mail senden möchten, auf <b>Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL BCC-Empfänger]</p> </td> 
   <td> <p>Klicken Sie für jeden Empfänger, an den Sie eine Kopie der E-Mail senden möchten, ohne dass andere Empfänger ihre Namen oder E-Mail-Adressen sehen können, <b>Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anlagen]</p> </td> 
   <td> <p>Klicken Sie für jeden Anhang, den Sie der E-Mail hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source-Datei]</strong> </p> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Als gelesen markieren]</td> 
   <td>Aktivieren Sie diese Option, um die aktualisierte Nachricht als gelesen zu markieren.</td> 
  </tr> 
 </tbody> 
</table>

### Anhang

* [[!UICONTROL Anlage herunterladen]](#download-an-attachment)
* [[!UICONTROL Anhänge auflisten]](#list-attachments)

#### [!UICONTROL Anlage herunterladen]

Dieses Modul lädt den angegebenen Anhang herunter.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Von E-Mail-Adresse]</td> 
   <td> <p> Um eine freigegebene E-Mail-Adresse zu verwenden, geben Sie die Adresse hier ein. Der Benutzer, dessen Anmeldeinformationen in der für dieses Modul verwendeten Verbindung verwendet werden, muss Zugriff auf den freigegebenen Ordner haben.<p>Lassen Sie dieses Feld leer, um die E-Mail-Adresse des Verbindungseigentümers zu verwenden.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID]</td> 
   <td> <p> Wählen Sie die ID der Nachricht aus, die den Anhang enthält, den Sie herunterladen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anhang-ID]</td> 
   <td> <p>Geben Sie die ID des Anhangs ein, den Sie herunterladen möchten, oder mappen Sie sie. Sie können diese Idee mithilfe des Moduls „Listenanhänge“ finden.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Anhänge auflisten]

Dieses Modul ruft eine Liste von Anhängen ab, die zur angegebenen Nachricht gehören.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Von E-Mail-Adresse]</td> 
   <td> <p> Um eine freigegebene E-Mail-Adresse zu verwenden, geben Sie die Adresse hier ein. Der Benutzer, dessen Anmeldeinformationen in der für dieses Modul verwendeten Verbindung verwendet werden, muss Zugriff auf den freigegebenen Ordner haben.<p>Lassen Sie dieses Feld leer, um die E-Mail-Adresse des Verbindungseigentümers zu verwenden.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID]</td> 
   <td> <p> Wählen Sie die ID der Nachricht aus, von der Sie Anhänge abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Anlagen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

* [[!UICONTROL Anlage hinzufügen]](#add-an-attachment)
* [Erstellen und Senden einer Nachricht](#create-and-send-a-message)
* [[!UICONTROL Erstellen eines API-Aufrufs]](#make-an-api-call)

#### [!UICONTROL Anlage hinzufügen]

Dieses Modul fügt einer Nachricht einen großen Anhang hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Von E-Mail-Adresse]</td> 
   <td> <p> Um eine freigegebene E-Mail-Adresse zu verwenden, geben Sie die Adresse hier ein. Der Benutzer, dessen Anmeldeinformationen in der für dieses Modul verwendeten Verbindung verwendet werden, muss Zugriff auf den freigegebenen Ordner haben.<p>Lassen Sie dieses Feld leer, um die E-Mail-Adresse des Verbindungseigentümers zu verwenden.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachrichten-ID]</td> 
   <td> <p> Wählen Sie die ID der Nachricht aus, der Sie einen Anhang hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Datei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen und Senden einer Nachricht]

Dieses Aktionsmodul erstellt und sendet eine E-Mail-Nachricht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Betreff]</td> 
   <td> <p>Geben Sie die Betreffzeile der Nachricht ein oder mappen Sie sie.</p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Hauptteilinhalt]</td> 
   <td> <p>Geben Sie den Nachrichtentext der E-Mail ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wichtigkeit]</td> 
   <td> <p>Wichtigkeit der E-Mail auswählen</p> 
    <ul> 
     <li>[!UICONTROL Niedrig]</li> 
     <li>[!UICONTROL normal]</li> 
     <li>[!UICONTROL Hoch]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL an Empfänger]</p> </td> 
   <td> <p>Klicken Sie für jeden Empfänger, an den Sie die E-Mail senden möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Empfänger]</p> </td> 
   <td> <p><p>Klicken Sie für jeden Empfänger, an den Sie eine Kopie der E-Mail senden möchten, auf <b>Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL BCC-Empfänger]</p> </td> 
   <td> <p>Klicken Sie für jeden Empfänger, an den Sie eine Kopie der E-Mail senden möchten, ohne dass andere Empfänger ihre Namen oder E-Mail-Adressen sehen können, <b>Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein.</p> </li> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen des Kontakts ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anlagen]</p> </td> 
   <td> <p>Klicken Sie für jeden Anhang, den Sie der E-Mail hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source-Datei]</strong> </p> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Internet-Nachrichtenkopfzeilen]</td> 
   <td> <p>Fügen Sie die Nachrichtenkopfzeilen für die E-Mail hinzu.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL name]</strong> </p> <p>Geben Sie den Namen der Kopfzeile ein</p> </li> 
     <li> <p><strong>[!UICONTROL E-Mail-Adresse]</strong> </p> <p>Geben Sie einen Wert für die Kopfzeile ein.</p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Von E-Mail-Adresse]</td> 
   <td> <p> Um eine freigegebene E-Mail-Adresse zu verwenden, geben Sie die Adresse hier ein. Der Benutzer, dessen Anmeldeinformationen in der für dieses Modul verwendeten Verbindung verwendet werden, muss Zugriff auf den freigegebenen Ordner haben.<p>Lassen Sie dieses Feld leer, um die E-Mail-Adresse des Verbindungseigentümers zu verwenden.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen eines API-Aufrufs]

Mit diesem Modul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Office 365]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://graph.microsoft.com</code> ein. Beispiel:<code> /v1.0/me/messages</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Methode]</p> </td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Beispiel: <code>{"Content-type":"application/json"}</code>. Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p> Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> </td> 
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
