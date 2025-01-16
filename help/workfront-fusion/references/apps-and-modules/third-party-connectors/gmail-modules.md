---
title: Gmail-Module
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die Gmail verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
source-git-commit: 0581601a254a9492f4166d78eb0f11868d390f24
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 0%

---

# [!DNL Gmail]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Gmail] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

Um [!DNL Gmail]-Module verwenden zu können, müssen Sie über ein [!DNL Gmail]-Konto verfügen.

## [!DNL Gmail] mit [!DNL Workfront Fusion] verbinden {#connect-gmail-to-workfront-fusion}

* [Verbinden [!DNL Gmail] mit [!DNL Workfront Fusion] verwenden [!DNL Google Workspace]](#connect-gmail-to-workfront-fusion-usingg-suite)
* [Connect [!DNL Gmail] to [!DNL Workfront Fusion] using [!DNL gmail.com] or [!DNL googlemail].com](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### Verbinden von [!DNL Gmail] mit [!DNL Workfront Fusion] mithilfe von[!DNL  Google Workspace] {#connect-gmail-to-workfront-fusion-using-g-suite}

Anweisungen zum Verbinden Ihres [!DNL Google Workspace]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Verbindung erstellen - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

### Verbinden von [!DNL Gmail] mit [!DNL Workfront Fusion] über [!DNL gmail.com] oder [!DNL googlemail].com {#connect-gmail-to-workfront-fusion-using-gmail-com-or-googlemail-com}

Wenn Sie [!DNL @gmail.com] oder [!DNL @googlemail.com] Benutzer sind, müssen Sie einen OAuth-Client auf [dem [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) erstellen, um eine [!UICONTROL Client ID] und [!UICONTROL Client Secret] zu erhalten.

Eine schrittweise Anleitung zum Erstellen des OAuth-Clients und zum Abrufen einer [!UICONTROL Client ID] und eines [!UICONTROL Client Secret] finden Sie unter [Verbinden von Adobe Workfront Fusion mit Google Services mithilfe eines benutzerdefinierten OAuth-Clients](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## [!DNL Gmail] Module und ihre Felder

Beim Konfigurieren [!DNL Gmail] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Gmail] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Iteratoren](#iterators)

### Trigger

#### [!UICONTROL Watch emails]

Dieses Trigger-Modul führt ein Szenario aus, wenn eine neue E-Mail zur Verarbeitung empfangen wird.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz oder den Datensätzen verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den E-Mail-Ordner aus, den Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter type] </td> 
   <td> <p>Filtertyp auswählen, der zum Ansehen von E-Mails verwendet werden soll</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Simple filter]</strong> </p> <p>Füllen Sie die Felder [!UICONTROL Criteria], [!UICONTROL Sender Email Address], [!UICONTROL Subject] und [!UICONTROL Search Phrase] aus</p> </li> 
     <li> <p> <strong>[!UICONTROL Gmail filter]</strong> </p> <p>Geben Sie im Feld [!UICONTROL Query] die Abfrage ein, die Sie zum Filtern von E-Mails verwenden möchten.</p> <p>Weitere Informationen zu [!DNL Gmail] finden Sie unter <a href="https://support.google.com/mail/answer/7190">Suchoperatoren</a> in der [!DNL Gmail].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteria]</td> 
   <td>Wählen Sie aus, ob Sie [!UICONTROL all email], [!UICONTROL only read emails] oder [!UICONTROL only unread] E-Mails ansehen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sender email address]</td> 
   <td> <p> Geben Sie eine E-Mail-Adresse ein, um nur E-Mails anzuzeigen, die von dieser Adresse gesendet wurden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>Geben Sie eine Textzeichenfolge ein, um nur E-Mails anzusehen, die diese Textzeichenfolge im Betreff enthalten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search phrase]</td> 
   <td>Geben Sie eine Textzeichenfolge ein, um nur E-Mails anzuzeigen, die diese Textzeichenfolge an einer beliebigen Stelle in der E-Mail enthalten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mark email message(s) as read when fetched]</td> 
   <td> <p> Aktivieren Sie diese Option, um abgerufene E-Mails als gelesen zu markieren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of results]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Ergebnissen fest, mit denen [!DNL Workfront Fusion] während eines Zyklus arbeiten soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Send an email]](#send-an-email)
* [[!UICONTROL Create a draft]](#create-a-draft)
* [[!UICONTROL Mark an email as read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an email as unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an email]](#move-an-email)
* [[!UICONTROL Copy an email]](#copy-an-email)
* [[!UICONTROL Delete an email]](#delete-an-email)
* [[!UICONTROL Modify email labels]](#modify-email-labels)

#### [!UICONTROL Send an email]

Dieses Aktionsmodul sendet eine neue E-Mail.

Sie geben den Empfänger der E-Mail an.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL From]</td> 
   <td> <p>Geben Sie eine Absender-E-Mail-Adresse ein oder mappen Sie sie.</p> <p>Hinweis: Wenn Sie eine falsche E-Mail-Adresse eingeben, kann beim Senden einer Nachricht ein Fehler auftreten, da Ihr Konto möglicherweise nicht berechtigt ist, E-Mails von einer anderen Adresse als Ihrer eigenen zu senden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Klicken Sie auf <strong>[!UICONTROL Add]</strong> und geben Sie dann die E-Mail-Adresse für jeden Empfänger ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Geben Sie den E-Mail-Betreff ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Geben Sie den E-Mail-Inhalt (Nachrichtentext) ein oder ordnen Sie ihn zu. HTML-Tags sind erlaubt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Klicken Sie auf <strong>[!UICONTROL Add]</strong> , um einen Anhang hinzuzufügen. Sie können eine Datei aus den vorherigen Modulen zuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Klicken Sie auf <strong>[!UICONTROL Add]</strong> und geben Sie dann die E-Mail-Adresse für jeden Kopierempfänger ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Klicken Sie auf <strong>[!UICONTROL Add]</strong> und geben Sie dann die E-Mail-Adresse für jeden Blind Copy-Empfänger ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a draft]

Dieses Aktionsmodul erstellt einen neuen E-Mail-Entwurf und fügt ihn einem von Ihnen angegebenen Ordner hinzu.

Sie geben den Ordner an, in dem Sie einen Entwurf erstellen möchten.

Das Modul gibt die ID des E-Mail-Entwurfs und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Ordner aus, in dem Sie einen Entwurf erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Klicken Sie auf <strong>[!UICONTROL Add]</strong> und geben Sie dann die E-Mail-Adresse für jeden Empfänger ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Geben Sie den E-Mail-Betreff ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Geben Sie den E-Mail-Inhalt (Nachrichtentext) ein oder ordnen Sie ihn zu. HTML-Tags sind erlaubt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Klicken Sie auf <strong>[!UICONTROL Add]</strong> , um einen Anhang hinzuzufügen. Sie können eine Datei aus den vorherigen Modulen zuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Klicken Sie auf <strong>[!UICONTROL Add]</strong> und geben Sie dann die E-Mail-Adresse für jeden Kopierempfänger ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Klicken Sie auf <strong>[!UICONTROL Add]</strong> und geben Sie dann die E-Mail-Adresse für jeden Blind Copy-Empfänger ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as read]

Dieses Aktionsmodul markiert eine E-Mail als gelesen.

Sie geben die ID der E-Mail und ihren Ordner an.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Ordner aus, der die E-Mail enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> E-Mail-ID eingeben oder zuordnen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as unread]

Dieses Aktionsmodul kennzeichnet eine E-Mail oder einen E-Mail-Entwurf als ungelesen.

Sie geben die ID der E-Mail und ihren Ordner an.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Ordner aus, der die E-Mail enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)] </td> 
   <td> <p>Geben Sie die E-Mail-ID der E-Mail ein, die Sie als ungelesen markieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an email]

Dieses Aktionsmodul verschiebt eine E-Mail oder einen E-Mail-Entwurf in einen von Ihnen angegebenen Ordner.

Sie geben den Ordner, den Zielordner und die ID der E-Mail an.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Quellordner aus, der die zu verschiebende E-Mail enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p> Wählen Sie den [!DNL Gmail] Zielordner aus, in den Sie die E-Mail verschieben möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Geben Sie die E-Mail-ID der E-Mail ein, die Sie verschieben möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy an email]

Dieses Aktionsmodul kopiert einen E-Mail- oder E-Mail-Entwurf in einen von Ihnen angegebenen Ordner.

Sie geben den Ordner, den Zielordner und die ID der E-Mail an.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Quellordner aus, der die E-Mail enthält, die Sie kopieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Zielordner aus, in den Sie die E-Mail kopieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p>Geben Sie die E-Mail-ID der E-Mail ein, die Sie kopieren möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an email]

Dieses Aktionsmodul entfernt eine E-Mail oder einen E-Mail-Entwurf aus einem von Ihnen angegebenen Ordner.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] Nachrichten-ID]</p> </td> 
   <td> <p>Geben Sie die E-Mail-ID der E-Mail ein, die Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Permanently] </td> 
   <td> <p>Aktivieren Sie diese Option, damit das Modul die E-Mail dauerhaft löschen kann, anstatt sie in den Papierkorb-Ordner zu verschieben.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify email labels]

Dieses Aktionsmodul ändert die Beschriftung einer von Ihnen angegebenen E-Mail-Nachricht.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] Nachrichten-ID]</td> 
   <td> <p> Geben Sie die E-Mail-ID der E-Mail ein, die Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Labels to add]</p> </td> 
   <td> <p>Wählen Sie die Bezeichnung aus, die Sie der ausgewählten E-Mail-Nachricht hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Labels to remove]</td> 
   <td> <p> Wählen Sie die Bezeichnung aus, die Sie aus der ausgewählten E-Mail-Nachricht entfernen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!UICONTROL Label to add] und [!UICONTROL Label to remove] Felder werden nur von Benutzenden erstellte Beschriftungen geladen.

### Iteratoren

#### [!UICONTROL Iterate attachments]

Sie können E-Mail-Anhänge iterieren. Jeder Anhang ist ein separates Bundle in der -Ausgabe des Moduls. Weitere Informationen finden Sie unter [Iterator-Modul](/help/workfront-fusion/references/modules/iterator-module.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> <p>Wählen Sie das Modul aus, von dem aus Sie Anlagen iterieren möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>
