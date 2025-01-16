---
title: E-Mail-Module
description: In einem  [!DNL Adobe Workfront Fusion] -Szenario können Sie Ihr E-Mail-Konto mit mehreren Anwendungen und Services von Drittanbietern verbinden. Damit können Sie E-Mails über IMAP herunterladen, E-Mails über SMTP senden, neue Entwürfe erstellen, E-Mails von einem Ordner in einen anderen verschieben und kopieren, E-Mails als gelesen oder ungelesen markieren und E-Mails löschen.
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2103'
ht-degree: 0%

---

# E-Mail-Module

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Ihr E-Mail-Konto mit mehreren Anwendungen und Services von Drittanbietern verbinden. Damit können Sie E-Mails über IMAP herunterladen, E-Mails über SMTP senden, neue Entwürfe erstellen, E-Mails von einem Ordner in einen anderen verschieben und kopieren, E-Mails als gelesen oder ungelesen markieren und E-Mails löschen.

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

## Verbinden Ihrer E-Mail mit Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [Verbindung mit Google herstellen](#connect-to-google)
* [Herstellen einer Verbindung zu anderen E-Mail-Services (SMAP)](#connect-to-other-email-services-smap)

### Mit [!DNL Google] verbinden

Verwenden Sie diese Option, um Szenarien mit E-Mail-Modulen zu erstellen, für die eine Verbindung zu Ihrem [!DNL Google]-Konto erforderlich ist. Dies ist ein Konto mit eingeschränkten Gültigkeitsbereichen.

Sie können direkt aus einem E-Mail-Modul heraus eine Verbindung zu Ihrem [!DNL Google]-Konto herstellen.

1. Klicken Sie in einem beliebigen E-Mail-Modul **[!UICONTROL Add]** neben dem Feld [!UICONTROL Connection] .
1. Wählen Sie **[!DNL Google]** als Verbindungstyp aus.
1. Geben Sie einen Namen für die Verbindung ein.
1. (Optional) Geben Sie Ihre [!UICONTROL [!DNL Google] Client ID] und [!UICONTROL Client Secret] ein.
1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

### Herstellen einer Verbindung zu anderen E-Mail-Services (SMAP)

Mit der SMAP-Verbindung können Sie aus der Ferne auf Ihre Mailbox zugreifen und Nachrichten in Ihrer Mailbox lesen oder bearbeiten. Die SMAP-Verbindung wird von den meisten E-Mail-Modulen verwendet.

1. Klicken Sie in einem beliebigen E-Mail-Modul **[!UICONTROL Add]** neben dem Feld [!UICONTROL Connection] .
1. Wählen Sie **[!UICONTROL Others (SMTP)]** als Verbindungstyp aus.
1. Geben Sie einen **[!UICONTROL Name]** für die Verbindung ein.
1. Wählen Sie Ihre **[!UICONTROL Email provider]** aus der Liste aus. Wenn Ihr E-Mail-Anbieter nicht in der Liste aufgeführt ist, wählen Sie Sonstige aus.
1. Geben Sie Ihre **[!UICONTROL Email address]**, **[!UICONTROL Your full name]**, Ihre **[!UICONTROL User name]** und Ihre **[!UICONTROL Password]** ein.
1. (Bedingt) Wenn Ihr Provider nicht in der Liste aufgeführt ist, geben Sie Ihre **[!UICONTROL SMTP server]** und **[!UICONTROL Port]** ein und geben an, ob Sie **[!UICONTROL Use a secure connection (TLS)]** möchten. Um diese Informationen zu finden, überprüfen Sie den Abschnitt [!UICONTROL Help] für Ihr Postfach. Wenn Sie nicht über diese Informationen verfügen, wenden Sie sich an Ihren E-Mail-Dienstanbieter.
1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!UICONTROL Email] Module und ihre Felder

Beim Konfigurieren [!UICONTROL Email] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können je nach Faktoren wie Ihrer Zugriffsebene in der App oder im Service weitere Felder angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Einige der E-Mail-Felder enthalten möglicherweise bereits Daten, da Sie diese in einem anderen Modul im Szenario verwendet haben. Weitere Informationen finden Sie in der E-Mail-Hilfe.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>Die eindeutige E-Mail-ID &quot;[!UICONTROL Email ID (UID)]&quot; ist die Kennung der E-Mail. Die E-Mail-ID ist für jeden Ordner der E-Mail spezifisch.

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Iteratoren](#iterators)

### Trigger

#### [!UICONTROL Watch Emails]

Trigger beim Empfang einer neuen E-Mail zur Verarbeitung gemäß den angegebenen Kriterien.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den Ordner aus, der E-Mails enthält, die Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Wählen Sie die Kriterien aus, nach denen Sie E-Mails ansehen möchten:</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>Geben Sie die E-Mail-Adresse des Absenders ein, dessen E-Mails Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Recipient Email Address]</td> 
   <td> <p> Geben Sie die E-Mail-Adresse des Empfängers ein, dessen E-Mails Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Geben Sie den Betreff der E-Mail ein, die Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Geben Sie Schlüsselwörter ein, um nur E-Mails mit bestimmten Phrasen anzusehen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched]</td> 
   <td> <p>Aktivieren Sie diese Option, um die ungelesene E-Mail nach dem Abrufen der Details als gelesen zu markieren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> Die maximale Anzahl von E-Mails, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben sollten.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Send an Email]](#send-an-email)
* [[!UICONTROL Create a Draft]](#create-a-draft)
* [[!UICONTROL Mark an Email as Read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an Email as Unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an Email]](#move-an-email)
* [[!UICONTROL Copy an Email]](#copy-an-email)
* [[!UICONTROL Delete an Email]](#delete-an-email)
* [[!UICONTROL Get Emails]](#get-emails)

#### [!UICONTROL Send an Email]

Sendet eine neue E-Mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save Message after Sending]</td> 
   <td>Nachdem die E-Mail gesendet wurde, wird sie in Ihrem Postfach gespeichert. Aktivieren Sie diese Option, wenn Sie mit [!DNL Workfront Fusion] gesendete E-Mails im <i>[!UICONTROL Sent mail]</i> oder einem anderen Ordner in Ihrem Postfach speichern möchten. Einige E-Mail-Dienste, z. B. [!DNL Gmail], speichern gesendete Nachrichten automatisch.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>Fügen Sie die E-Mail-Adressen hinzu, an die Sie die E-Mail senden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Geben Sie die Betreffzeile der E-Mail ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Content Type]</p> </td> 
   <td> <p>Wählen Sie den [!UICONTROL content] für die E-Mail:</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Plaintext]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Geben Sie den E-Mail-Inhalt im HTML-Format mithilfe von HTML-Tags ein oder mappen Sie ihn im Klartext, je nachdem, was Sie im Feld [!UICONTROL Content Type] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Anlage hinzufügen:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Geben Sie den Dateinamen ein. Beispiel: sample.doc.</p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Geben Sie den Pfad zum Ordner ein, in den die Anlage hochgeladen werden soll.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Geben Sie die [!UICONTROL content ID] ein, um den Anhang (Bild) in den Inhalt einzufügen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Geben Sie eine oder mehrere E-Mail-Adressen ein, an die Sie eine Kopie dieser E-Mail senden möchten, oder ordnen Sie sie zu. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Geben Sie eine oder mehrere E-Mail-Adressen ein, an die Sie eine Kopie dieser E-Mail senden möchten, ohne dass die E-Mail-Adresse in der E-Mail angezeigt wird, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Geben Sie die E-Mail-Adresse (und ggf. den Namen), die im Feld [!UICONTROL From] in der E-Mail angezeigt wird, ein oder ordnen Sie sie zu. </p> <p>Wichtig: Verwenden Sie die richtige Syntax: <code>name@email.com</code> oder <code>"Name" name@email.com</code>.</p> <p>Hinweis: Normalerweise verwendet [!DNL Workfront Fusion] die E-Mail-Adresse, die Sie beim Erstellen der Verbindung eingegeben haben, als Absenderadresse. Wenn Sie eine andere E-Mail-Adresse eingeben, kann beim Senden einer Nachricht ein Fehler auftreten, da Ihr Konto möglicherweise nicht berechtigt ist, E-Mails von einer anderen Adresse als Ihrer eigenen zu senden. Z. B. <code>test@mail.com</code> oder "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Geben Sie die E-Mail-Adresse ein, die im Feld [!UICONTROL Sender] in der E-Mail angezeigt wird, oder ordnen Sie sie zu.</p> <p>Tipp: Wenn Sie sich nicht sicher sind, ob Sie dieses Feld oder das Feld „Von“ verwenden sollen, empfehlen wir die Auswahl des Felds „Von“.</p> <p>Wichtig: Verwenden Sie die richtige Syntax: <code>name@email.com</code> oder <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> Wenn Antworten auf diese E-Mail an eine andere Adresse als die Absenderadresse gesendet werden sollen, geben Sie die E-Mail-Adresse ein, an die Antworten auf diese E-Mail gesendet werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> Wenn Sie auf eine bestimmte E-Mail antworten, geben Sie die ID der E-Mail, auf die Sie antworten, ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Geben Sie die Nachrichten-IDs aller Antworten im Thread ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Priorität der E-Mail auswählen:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Fügen Sie die Kopfzeilen hinzu:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Fügen Sie den Schlüssel hinzu. Zum Beispiel [!UICONTROL Sender], [!UICONTROL Date], [!UICONTROL To] usw.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Geben Sie den Wert für den Schlüssel ein.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Draft]

Erstellt einen neuen Entwurf und fügt ihn einem ausgewählten Ordner hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Wählen Sie den Ordner aus, in dem Sie den E-Mail-Entwurf erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>Geben Sie die E-Mail-Adresse ein, an die Sie die E-Mail senden möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Geben Sie die Betreffzeile der E-Mail ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Content Type]</p> </td> 
   <td> <p>Content-Typ für die E-Mail auswählen:</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Plain Text]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Geben Sie den E-Mail-Inhalt im HTML-Format mithilfe von HTML-Tags ein oder mappen Sie ihn im Klartext, je nachdem, was Sie im Feld [!UICONTROL Content Type] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Anlage hinzufügen:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Geben Sie den Dateinamen ein. Beispiel: sample.doc.</p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Geben Sie den Pfad zum Ordner ein, in den die Anlage hochgeladen werden soll.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Geben Sie die Inhalts-ID ein, um den Anhang (Bild) in den Inhalt einzufügen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Geben Sie eine oder mehrere E-Mail-Adressen ein, an die Sie eine Kopie dieser E-Mail senden möchten, oder ordnen Sie sie zu. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Geben Sie eine oder mehrere E-Mail-Adressen ein, an die Sie eine Kopie dieser E-Mail senden möchten, ohne dass die E-Mail-Adresse in der E-Mail angezeigt wird, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Geben Sie die E-Mail-Adresse (und ggf. den Namen), die im Feld [!UICONTROL From] in der E-Mail angezeigt wird, ein oder ordnen Sie sie zu. </p> <p>Wichtig: Verwenden Sie die richtige Syntax: <code>name@email.com</code> oder <code>"Name" name@email.com</code>.</p> <p>Hinweis: Normalerweise verwendet [!DNL Workfront Fusion] die E-Mail-Adresse, die Sie beim Erstellen der Verbindung eingegeben haben, als Absenderadresse. Wenn Sie eine andere E-Mail-Adresse eingeben, kann beim Senden einer Nachricht ein Fehler auftreten, da Ihr Konto möglicherweise nicht berechtigt ist, E-Mails von einer anderen Adresse als Ihrer eigenen zu senden. Z. B. <code>test@mail.com</code> oder "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Geben Sie die E-Mail-Adresse ein, die im Feld [!UICONTROL Sender] in der E-Mail angezeigt wird, oder ordnen Sie sie zu.</p> <p>Tipp: Wenn Sie sich nicht sicher sind, ob Sie dieses Feld oder das Feld „Von“ verwenden sollen, empfehlen wir die Auswahl des Felds „Von“.</p> <p>Wichtig: Verwenden Sie die richtige Syntax: <code>name@email.com</code> oder <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> Wenn Antworten auf diese E-Mail an eine andere Adresse als die "[!UICONTROL from]"-Adresse gesendet werden sollen, geben Sie die E-Mail-Adresse ein, an die Antworten auf diese E-Mail gesendet werden sollen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> Wenn Sie auf eine bestimmte E-Mail antworten, geben Sie die ID der E-Mail, auf die Sie antworten, ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Geben Sie die Nachrichten-IDs aller Antworten im Thread ein.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Priorität der E-Mail auswählen:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Fügen Sie die Kopfzeilen hinzu:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Fügen Sie den Schlüssel hinzu. Beispielsweise „Absender“, „Datum“, „An“ usw.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Geben Sie den Wert für den Schlüssel ein.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Read]

Markiert eine E-Mail oder einen Entwurf in einem ausgewählten Ordner als gelesen, indem das [!UICONTROL Read]-Flag gesetzt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Wählen Sie den Ordner der E-Mail aus, den Sie als gelesen markieren möchten. Beispiel: Primär.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Geben Sie die E-Mail-UID der E-Mail ein, die Sie als gelesen markieren möchten.</p> <p>Sie können die UID der E-Mail über das Modul [!UICONTROL Email] &gt;[!UICONTROL Watch Email] oder [!UICONTROL Search Email] abrufen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Unread]

Markiert eine E-Mail oder einen Entwurf in einem ausgewählten Ordner als ungelesen, indem die Markierung Ungelesen gesetzt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Wählen Sie den Ordner der E-Mail aus, den Sie als ungelesen markieren möchten. Beispiel: Primär.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Geben Sie die E-Mail-UID der E-Mail ein, die Sie als ungelesen markieren möchten.</p> <p>Sie können die UID der E-Mail über das Modul [!UICONTROL Email] &gt;[!UICONTROL Watch Email] oder [!UICONTROL Search Email] abrufen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Email]

Verschiebt eine ausgewählte E-Mail oder einen Entwurf in einen ausgewählten Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Wählen Sie den Ordner aus, der die E-Mail enthält, von der Sie die E-Mail verschieben möchten. Beispiel: Primär.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Wählen Sie den Ordner aus, dem Sie die E-Mail hinzufügen möchten. Beispiel: Arbeit.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Geben Sie die E-Mail-UID der E-Mail ein, die Sie in den Zielordner verschieben möchten.</p> <p>Sie können die UID der E-Mail über das Modul [!UICONTROL Email] &gt;[!UICONTROL Watch Email] oder [!UICONTROL Search Email] abrufen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy an Email]

Kopiert eine E-Mail oder einen Entwurf in einen ausgewählten Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Wählen Sie den Ordner aus, aus dem Sie die E-Mail kopieren möchten. Beispiel: Primär.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Wählen Sie den Ordner aus, in den Sie die E-Mail kopieren möchten. Beispiel: Arbeit.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Geben Sie die E-Mail-UID der E-Mail ein, die Sie in den Zielordner kopieren möchten.</p> <p>Sie können die UID der E-Mail über das Modul [!UICONTROL Email] &gt;[!UICONTROL Watch Email] oder [!UICONTROL Search Email] abrufen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Email]

Entfernt eine E-Mail oder einen Entwurf aus dem ausgewählten Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Wählen Sie den Ordner der E-Mail aus, die Sie löschen möchten. Beispiel: Primär.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Geben Sie die E-Mail-UID der E-Mail ein, die Sie löschen möchten.</p> <p>Sie können die UID der E-Mail über das Modul [!UICONTROL Email] &gt;[!UICONTROL Watch Email] oder [!UICONTROL Search Email] abrufen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expunge]</td> 
   <td> <p>Aktivieren Sie diese Einstellung, damit das Modul alle Nachrichten, die im aktuell geöffneten Postfach als [!UICONTROL Deleted] gekennzeichnet sind, dauerhaft löschen kann.</p> <p>Hinweis: In [!DNL Gmail] wird dieses Verhalten durch die Einstellung im Abschnitt [!UICONTROL Settings] &gt;[!UICONTROL Forwarding POP/IMAP in IMAP access] gesteuert.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Emails]

Gibt E-Mails zurück, die den angegebenen Kriterien entsprechen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres E-Mail-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Verbinden Ihrer E-Mail mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den Ordner aus, der die abzurufenden E-Mails enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched] </td> 
   <td> <p>Aktivieren Sie diese Option, wenn Sie die ungelesene E-Mail nach dem Abrufen der Details als gelesen markieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Wählen Sie die Kriterien der E-Mails aus, die Sie abrufen möchten:</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>Geben Sie die E-Mail-Adresse des Absenders ein, dessen E-Mails Sie abrufen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Recipient Email Address]</td> 
   <td> <p> Geben Sie die E-Mail-Adresse des Empfängers ein, dessen E-Mails Sie abrufen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From date] </td> 
   <td> <p>Geben Sie das Datum ein, an dem die am oder nach dem angegebenen Datum verarbeiteten E-Mails abgerufen werden sollen, oder mappen Sie es.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before date]</td> 
   <td> <p> Datum eingeben oder zuordnen, an dem die am oder vor dem angegebenen Datum verarbeiteten E-Mails abgerufen werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Geben Sie den Betreff der E-Mail ein, die Sie abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Geben Sie Schlüsselwörter ein oder ordnen Sie sie zu, um nur die E-Mails abzurufen, die bestimmte Phrasen enthalten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Geben Sie die E-Mail-ID (UID) der E-Mail ein, deren Details Sie abrufen möchten.</p> <p>Sie können die UID der E-Mail über das Modul [!UICONTROL  Watch Email]oder [!UICONTROL Search Email] von [!DNL Workfront Fusion] abrufen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> Die maximale Anzahl von E-Mails, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben sollten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p> Wählen Sie aus, ob Sie das Modul auch dann weiter ausführen möchten, wenn keine Ergebnisse zurückgegeben wurden.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Iteratoren

#### [!UICONTROL Iterate Attachments]

Iteriert empfangene Anhänge einzeln.

Mit dem Modul E-Mail-Iterator können Sie E-Mail-Anhänge separat verwalten. Sie können beispielsweise einrichten, dass E-Mails überwacht werden, um die E-Mails mit Anhängen zu durchlaufen und Warnhinweise zu erhalten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module]</td> 
   <td> <p>Wählen Sie das Modul aus, das die E-Mail mit den Anhängen ausgibt, durch die Sie iterieren möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu Iteratoren finden Sie unter [Iteratormodul](/help/workfront-fusion/references/modules/iterator-module.md).
