---
title: E-Mail-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Ihr E-Mail-Konto mit mehreren Anwendungen und Services von Drittanbietern verbinden. Damit können Sie E-Mails über IMAP herunterladen, E-Mails über SMTP senden, neue Entwürfe erstellen, E-Mails von einem Ordner in einen anderen verschieben und kopieren, E-Mails als gelesen oder ungelesen markieren und E-Mails löschen.
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2491'
ht-degree: 0%

---

# E-Mail-Module

In einem Adobe Workfront Fusion-Szenario können Sie Ihr E-Mail-Konto mit mehreren Anwendungen und Services von Drittanbietern verbinden. Damit können Sie E-Mails über IMAP herunterladen, E-Mails über SMTP senden, neue Entwürfe erstellen, E-Mails von einem Ordner in einen anderen verschieben und kopieren, E-Mails als gelesen oder ungelesen markieren und E-Mails löschen.

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

## Verbinden Ihrer E-Mail mit Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [Verbindung mit Google herstellen](#connect-to-google)
* [Herstellen einer Verbindung zu anderen E-Mail-Services (IMAP)](#connect-to-other-email-services-smap)

### Mit [!DNL Google] verbinden

Verwenden Sie diese Option, um Szenarien mit E-Mail-Modulen zu erstellen, für die eine Verbindung zu Ihrem [!DNL Google]-Konto erforderlich ist. Dies ist ein Konto mit eingeschränkten Gültigkeitsbereichen.

Sie können direkt aus einem E-Mail-Modul heraus eine Verbindung zu Ihrem [!DNL Google]-Konto herstellen.

1. Klicken Sie in einem beliebigen E **[!UICONTROL Mail-Modul]** dem Feld [!UICONTROL Verbindung] auf „Hinzufügen“.
1. Wählen Sie **[!DNL Google]** als Verbindungstyp aus.
1. Geben Sie einen Namen für die Verbindung ein.
1. (Optional) Geben Sie Ihre [!UICONTROL [!DNL Google]-Client]ID und [!UICONTROL Client-Geheimnis] ein.
1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

### Herstellen einer Verbindung zu anderen E-Mail-Services (IMAP)

Mit der IMAP-Verbindung können Sie aus der Ferne auf Ihre Mailbox zugreifen und Nachrichten in Ihrer Mailbox lesen oder bearbeiten. Die IMAP-Verbindung wird von den meisten E-Mail-Modulen verwendet.

1. Klicken Sie in einem beliebigen E **[!UICONTROL Mail-Modul]** dem Feld [!UICONTROL Verbindung] auf „Hinzufügen“.
1. Wählen Sie **[!UICONTROL Sonstige (SMTP)]** als Verbindungstyp aus.
1. Geben Sie einen **[!UICONTROL Namen]** für die Verbindung ein.
1. Wählen Sie Ihren **[!UICONTROL E-Mail]** Anbieter) aus der Liste aus. Wenn Ihr E-Mail-Anbieter nicht in der Liste aufgeführt ist, wählen Sie Sonstige aus.
1. Geben Sie **[!UICONTROL Benutzername]** und Ihr **[!UICONTROL Kennwort]** für das E-Mail-Konto ein.
1. (Bedingt) Wenn sich Ihr Provider nicht auf der Liste befindet, geben Sie Ihren **[!UICONTROL SMTP-Server]** und **[!UICONTROL Port]** ein und geben an, ob Sie **[!UICONTROL Sichere Verbindung (TLS) verwenden)]**. Diese Informationen finden Sie im Abschnitt [!UICONTROL Hilfe] für Ihr Postfach. Wenn Sie nicht über diese Informationen verfügen, wenden Sie sich an Ihren E-Mail-Dienstanbieter.
1. Um ein selbstsigniertes Zertifikat zu verwenden, aktivieren Sie die Option **Nicht autorisierte Zertifikate zurückweisen** und laden Sie Ihr selbstsigniertes Zertifikat hoch. Anweisungen finden Sie [Hochladen eines selbstsignierten Zertifikats](#upload-a-self-signed-certificate)
1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

#### Hochladen eines selbstsignierten Zertifikats

So fügen Sie ein selbstsigniertes Zertifikat hinzu:

1. Klicken Sie **Extrahieren**.
1. Wählen Sie den zu extrahierenden Dateityp aus.
1. Wählen Sie die Datei aus, die das - oder -Zertifikat enthält.
1. Geben Sie das Kennwort für die Datei ein.
1. Klicken Sie auf **Speichern**, um die Datei zu extrahieren und zur Moduleinrichtung zurückzukehren.

## [!UICONTROL E]Mail-Module und ihre Felder

Beim Konfigurieren von [!UICONTROL E-Mail]-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können je nach Faktoren wie Ihrer Zugriffsebene in der App oder im Service weitere Felder angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Einige der E-Mail-Felder enthalten möglicherweise bereits Daten, da Sie diese in einem anderen Modul im Szenario verwendet haben. Weitere Informationen finden Sie in der E-Mail-Hilfe.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>Die eindeutige E-Mail-ID [!UICONTROL E-Mail-ID (UID)] ist die Kennung der E-Mail. Die E-Mail-ID ist für jeden Ordner der E-Mail spezifisch.

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Iteratoren](#iterators)

### Trigger

#### [!UICONTROL E-Mails ansehen]

Dieses Trigger-Modul startet ein Szenario, wenn eine neue E-Mail zur Verarbeitung gemäß den angegebenen Kriterien empfangen wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner] </td> 
   <td> <p>Wählen Sie den Ordner aus, der E-Mails enthält, die Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Kriterien]</p> </td> 
   <td> <p>Wählen Sie die Kriterien aus, nach denen Sie E-Mails ansehen möchten:</p> 
    <ul> 
     <li>[!UICONTROL Alle E-Mails]</li> 
     <li>[!UICONTROL Nur E-Mails lesen]</li> 
     <li>[!UICONTROL only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Absender-E-Mail-Adresse] </td> 
   <td> <p>Geben Sie die E-Mail-Adresse des Absenders ein, dessen E-Mails Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Betreff] </td> 
   <td> <p>Geben Sie den Betreff der E-Mail ein, die Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Geben Sie Suchbegriffe ein, um nur die E-Mails zu sehen, die die Suchbegriffe enthalten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachricht(en) beim Abrufen als gelesen markieren]</td> 
   <td> <p>Aktivieren Sie diese Option, um die ungelesene E-Mail nach dem Abrufen der Details als gelesen zu markieren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl an Ergebnissen]</td> 
   <td> <p> Geben Sie die maximale Anzahl von E-Mails ein, die Workfront Fusion während eines Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Kopieren einer E-Mail]](#copy-an-email)
* [[!UICONTROL Entwurf erstellen]](#create-a-draft)
* [[!UICONTROL E-Mail löschen]](#delete-an-email)
* [[!UICONTROL E-Mails abrufen]](#get-emails)
* [[!UICONTROL Markieren einer E-Mail als gelesen]](#mark-an-email-as-read)
* [[!UICONTROL Markieren einer E-Mail als ungelesen]](#mark-an-email-as-unread)
* [[!UICONTROL Verschieben einer E-Mail]](#move-an-email)
* [[!UICONTROL E-Mail senden]](#send-an-email)

#### [!UICONTROL Kopieren einer E-Mail]

Dieses Aktionsmodul kopiert eine E-Mail oder einen Entwurf in einen ausgewählten Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Ordner]</td> 
   <td>Wählen Sie den Ordner aus, aus dem Sie die E-Mail kopieren möchten. Beispiel: Primär.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zielordner]</td> 
   <td> <p> Wählen Sie den Ordner aus, in den Sie die E-Mail kopieren möchten. Beispiel: Arbeit.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL E-Mail-ID (UID)]</p> </td> 
   <td> <p>Geben Sie die E-Mail-UID der E-Mail ein, die Sie in den Zielordner kopieren möchten.</p> <p>Sie können die UID der E-Mail mit dem Modul [!UICONTROL E-Mail] &gt; [!UICONTROL E-Mail ansehen] oder dem Modul [!UICONTROL E-Mail suchen] abrufen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Entwurf erstellen]

Dieses Aktionsmodul erstellt einen neuen Entwurf und fügt ihn einem ausgewählten Ordner hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td>Wählen Sie den Ordner aus, in dem Sie den E-Mail-Entwurf erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL nach] </td> 
   <td> <p>Geben Sie die E-Mail-Adresse ein, an die Sie die E-Mail senden möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Betreff] </td> 
   <td> <p>Geben Sie die Betreffzeile der E-Mail ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Inhalt] </td> 
   <td> <p>Geben Sie den E-Mail-Inhalt im HTML-Format mit HTML-Tags oder im Nur-Text-Format ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anlagen]</p> </td> 
   <td> <p>Klicken Sie für jeden Anhang, den Sie hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Dateiname]</strong> </p> <p>Geben Sie den Dateinamen einschließlich der Erweiterung ein. </p> </li> 
     <li> <p><strong>[!UICONTROL -Daten]</strong> </p> <p>Geben Sie den Pfad zu dem Ordner ein, in den Sie die Anlage hochladen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL content-ID]</strong> </p> <p>Geben Sie die Inhalts-ID ein, um den Anhang (Bild) in den Inhalt einzufügen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Empfänger kopieren] </td> 
   <td> <p>Klicken Sie für jede E-Mail-Adresse, an die Sie eine Kopie dieser E-Mail senden möchten<b> auf „Element hinzufügen</b> und geben Sie die E-Mail-Adresse ein. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy-Empfänger]</td> 
   <td> <p> Klicken Sie für jede E-Mail-Adresse, an die Sie eine Kopie dieser E-Mail senden möchten, ohne dass die E-Mail-Adresse in der E-Mail angezeigt wird, auf <b>Element hinzufügen</b> und geben Sie die E-Mail-Adresse ein.</p> </td> 
  </tr> 
  <!--<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Enter or map the email address (and name, if needed) that appears in the [!UICONTROL From] field in the email. </p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code>.</p> <p>Note:  Normally, Workfront Fusion uses the email address that you entered when creating the connection as the sender address. If you enter any other email address, an error may occur when sending a message because your account may not have permission to send emails from a different address than your own. E.g. <code>test@mail.com</code> or "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Enter or map the email address that appears in the [!UICONTROL Sender] field in the email.</p> <p>Tip:  If you are unsure whether to use this field or the From field, we recommend choosing the From field.</p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> If you want replies to this email sent to a different address than the "[!UICONTROL from]" address, enter the email address where you want replies to this email sent.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> If you are replying to a specific email, enter or map the ID of the email you are replying to.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Enter the message IDs of all the replies in the thread.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Select the priority of the email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Add the headers:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Add the key. For example, Sender, Date, To, and so on.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter the value for the key.</p> </li> 
    </ul> </td> 
  </tr> -->
 </tbody> 
</table>

#### [!UICONTROL E-Mail löschen]

Dieses Aktionsmodul entfernt eine E-Mail oder einen Entwurf aus dem ausgewählten Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td>Wählen Sie den Ordner aus, der die zu löschende E-Mail enthält.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL E-Mail-ID (UID)]</p> </td> 
   <td> <p>Geben Sie die E-Mail-UID der E-Mail ein, die Sie löschen möchten.</p> <p>Sie können die UID der E-Mail über das Modul E-Mail &gt; E-Mail ansehen oder das Modul [!UICONTROL E-Mail suchen] abrufen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL löschen]</td> 
   <td> <p>Aktivieren Sie diese Option, um alle Nachrichten, die im aktuell geöffneten Postfach als [!UICONTROL Deleted] gekennzeichnet sind, dauerhaft zu entfernen.</p> <p>Hinweis: In [!DNL Gmail] wird dieses Verhalten durch die Einstellung im Abschnitt [!UICONTROL -Einstellungen] &gt;[!UICONTROL Weiterleitung POP/IMAP im IMAP-Zugriff] gesteuert.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL E-Mails abrufen]

Dieses Modul gibt E-Mails zurück, die den angegebenen Kriterien entsprechen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner] </td> 
   <td> <p>Wählen Sie den Ordner aus, der die abzurufenden E-Mails enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachricht(en) beim Abrufen als gelesen markieren] </td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie die ungelesene E-Mail nach dem Abrufen der Details als gelesen markieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Kriterien]</p> </td> 
   <td> <p>Wählen Sie die Kriterien der E-Mails aus, die Sie abrufen möchten:</p> 
    <ul> 
     <li>[!UICONTROL Alle E-Mails]</li> 
     <li>[!UICONTROL Nur E-Mails lesen]</li> 
     <li>[!UICONTROL only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Absender-E-Mail-Adresse] </td> 
   <td> <p>Geben Sie die E-Mail-Adresse des Absenders ein, dessen E-Mails Sie abrufen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Empfänger-E-Mail]</td> 
   <td> <p> Geben Sie die E-Mail-Adresse des Empfängers ein, dessen E-Mails Sie abrufen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Von Datum] </td> 
   <td> <p>Geben Sie das Datum ein, an dem die am oder nach dem angegebenen Datum verarbeiteten E-Mails abgerufen werden sollen, oder mappen Sie es.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL vor Datum]</td> 
   <td> <p> Datum eingeben oder zuordnen, an dem die am oder vor dem angegebenen Datum verarbeiteten E-Mails abgerufen werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Betreff] </td> 
   <td> <p>Geben Sie den Betreff der E-Mail ein, die Sie abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Geben Sie Schlüsselwörter ein oder ordnen Sie sie zu, um nur die E-Mails abzurufen, die diese Schlüsselwörter enthalten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL E-Mail-ID (UID)]</td> 
   <td> <p> Geben Sie die E-Mail-ID (UID) der E-Mail ein, deren Details Sie abrufen möchten.</p> <p>Sie können die UID der E-Mail abrufen, indem Sie das Modul [!UICONTROL E-Mail ansehen] oder das Modul [!UICONTROL E-Mail suchen] von Workfront Fusion verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximale Anzahl an Ergebnissen]</td> 
   <td> <p> Die maximale Anzahl von E-Mails, die Workfront Fusion während eines Szenario-Ausführungszyklus zurückgeben sollte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Die Routenausführung auch dann fortsetzen, wenn das Modul keine Ergebnisse zurückgibt]</td> 
   <td> <p> Wählen Sie aus, ob Sie das Modul auch dann weiter ausführen möchten, wenn keine Ergebnisse zurückgegeben wurden.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Markieren einer E-Mail als gelesen]

Dieses Aktionsmodul markiert eine E-Mail oder einen Entwurf in einem ausgewählten Ordner als gelesen, indem es die Markierung [!UICONTROL Lesen] festlegt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td>Wählen Sie den Ordner aus, der die E-Mail enthält, die Sie als gelesen markieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL E-Mail-ID (UID)]</p> </td> 
   <td> <p>Geben Sie die E-Mail-UID der E-Mail ein, die Sie als gelesen markieren möchten.</p> <p>Sie können die UID der E-Mail über das Modul E-Mail &gt; E-Mail ansehen oder das Modul [!UICONTROL E-Mail suchen] abrufen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Markieren einer E-Mail als ungelesen]

Markiert eine E-Mail oder einen Entwurf in einem ausgewählten Ordner als ungelesen, indem die Markierung Ungelesen gesetzt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td>Wählen Sie den Ordner aus, der die E-Mail enthält, die Sie als ungelesen markieren möchten. Beispiel: Primär.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL E-Mail-ID (UID)]</p> </td> 
   <td> <p>Geben Sie die E-Mail-UID der E-Mail ein, die Sie als ungelesen markieren möchten.</p> <p>Sie können die UID der E-Mail über das Modul E-Mail &gt; E-Mail ansehen oder das Modul [!UICONTROL E-Mail suchen] abrufen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Verschieben einer E-Mail]

Verschiebt eine ausgewählte E-Mail oder einen Entwurf in einen ausgewählten Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Ordner]</td> 
   <td>Wählen Sie den Ordner aus, der die zu verschiebende E-Mail enthält. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zielordner]</td> 
   <td> <p> Wählen Sie den Ordner aus, dem Sie die E-Mail hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL E-Mail-ID (UID)]</p> </td> 
   <td> <p>Geben Sie die E-Mail-UID der E-Mail ein, die Sie in den Zielordner verschieben möchten.</p> <p>Sie können die UID der E-Mail über das Modul E-Mail &gt; E-Mail ansehen oder das Modul [!UICONTROL E-Mail suchen] abrufen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL E-Mail senden]

Sendet eine neue E-Mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nachricht nach dem Senden speichern]</td> 
   <td>Nachdem die E-Mail gesendet wurde, wird sie in Ihrem Postfach gespeichert. Aktivieren Sie diese Option, wenn Sie mit Workfront Fusion gesendete E-Mails im Ordner <i>[!UICONTROL Sent Mail]</i> oder in einem anderen Ordner in Ihrem Postfach speichern möchten. Einige E-Mail-Dienste, z. B. [!DNL Gmail], speichern gesendete Nachrichten automatisch.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL nach] </td> 
   <td> <p>Fügen Sie die E-Mail-Adressen hinzu, an die Sie die E-Mail senden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Betreff] </td> 
   <td> <p>Geben Sie die Betreffzeile der E-Mail ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Content-Typ]</p> </td> 
   <td> <p>Wählen Sie den [!UICONTROL content]-Typ für die E-Mail aus:</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL plaintext]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Inhalt] </td> 
   <td> <p>Geben Sie den E-Mail-Inhalt im HTML-Format mithilfe von HTML-Tags ein oder ordnen Sie ihn zu oder im Klartext, je nachdem, was Sie im Feld [!UICONTROL Content Type] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Anlagen]</p> </td> 
   <td> <p>Klicken Sie für jeden Anhang, den Sie hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Dateiname]</strong> </p> <p>Geben Sie den Dateinamen einschließlich der Erweiterung ein. </p> </li> 
     <li> <p><strong>[!UICONTROL -Daten]</strong> </p> <p>Geben Sie den Pfad zu dem Ordner ein, in den Sie die Anlage hochladen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL content-ID]</strong> </p> <p>Geben Sie die Inhalts-ID ein, um den Anhang (Bild) in den Inhalt einzufügen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Empfänger kopieren] </td> 
   <td> <p>Klicken Sie für jede E-Mail-Adresse, an die Sie eine Kopie dieser E-Mail senden möchten<b> auf „Element hinzufügen</b> und geben Sie die E-Mail-Adresse ein. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy-Empfänger]</td> 
   <td> <p> Klicken Sie für jede E-Mail-Adresse, an die Sie eine Kopie dieser E-Mail senden möchten, ohne dass die E-Mail-Adresse in der E-Mail angezeigt wird, auf <b>Element hinzufügen</b> und geben Sie die E-Mail-Adresse ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Geben Sie die E-Mail-Adresse ein, die im Feld [!UICONTROL Absender] in der E-Mail angezeigt wird, oder ordnen Sie sie zu.</p> <p>Tipp: Wenn Sie sich nicht sicher sind, ob Sie dieses Feld oder das Feld „Von“ verwenden sollen, empfehlen wir die Auswahl des Felds „Von“.</p> <p>Wichtig: Verwenden Sie die richtige Syntax: <code>name@email.com</code> oder <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Antwort-An]</td> 
   <td> <p> Wenn Antworten auf diese E-Mail an eine andere Adresse als die Absenderadresse gesendet werden sollen, geben Sie die E-Mail-Adresse ein, an die Antworten auf diese E-Mail gesendet werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL in-response-to]</td> 
   <td> <p> Wenn Sie auf eine bestimmte E-Mail antworten, geben Sie die ID der E-Mail, auf die Sie antworten, ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verweise] </td> 
   <td> <p>Geben Sie die Nachrichten-IDs aller Antworten im Thread ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Priorität]</p> </td> 
   <td> <p>Priorität der E-Mail auswählen:</p> 
    <ul> 
     <li>[!UICONTROL Hoch]</li> 
     <li>[!UICONTROL normal]</li> 
     <li>[!UICONTROL Niedrig]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Kopfzeilen]</p> </td> 
   <td> <p>Fügen Sie die Kopfzeilen hinzu:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL key]</strong> </p> <p>Fügen Sie den Schlüssel hinzu. Beispielsweise [!UICONTROL Sender], [!UICONTROL Date], [!UICONTROL To] usw.</p> </li> 
     <li> <p><strong>[!UICONTROL value]</strong> </p> <p>Geben Sie den Wert für den Schlüssel ein.</p> </li> 
    </ul> </td> 
  </tr> 
<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL from] </td> 
   <td> <p>Geben Sie die E-Mail-Adresse (und ggf. den Namen) ein, die im Feld [!UICONTROL Von] in der E-Mail angezeigt wird, oder ordnen Sie sie zu. </p> <p>Wichtig: Verwenden Sie die richtige Syntax: <code>name@email.com</code> oder <code>"Name" name@email.com</code>.</p> <p>Hinweis: Normalerweise verwendet Workfront Fusion die E-Mail-Adresse, die Sie beim Erstellen der Verbindung eingegeben haben, als Absenderadresse. Wenn Sie eine andere E-Mail-Adresse eingeben, kann beim Senden einer Nachricht ein Fehler auftreten, da Ihr Konto möglicherweise nicht berechtigt ist, E-Mails von einer anderen Adresse als Ihrer eigenen zu senden. Z. B. <code>test@mail.com</code> oder "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Iteratoren

#### [!UICONTROL Iterieren von Anhängen]

Iteriert empfangene Anhänge einzeln.

Mit dem Modul E-Mail-Iterator können Sie E-Mail-Anhänge separat verwalten. Sie können beispielsweise einrichten, dass E-Mails überwacht werden, um die E-Mails mit Anhängen zu durchlaufen und Warnhinweise zu erhalten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Modul]</td> 
   <td> <p>Wählen Sie das Modul aus, das die E-Mail mit den Anhängen ausgibt, durch die Sie iterieren möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu Iteratoren finden Sie unter [Iteratormodul](/help/workfront-fusion/references/modules/iterator-module.md).
