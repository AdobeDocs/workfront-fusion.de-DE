---
title: Gmail-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Gmail verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1852'
ht-degree: 0%

---

# [!DNL Gmail]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Gmail] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

Um [!DNL Gmail]-Module verwenden zu können, müssen Sie über ein [!DNL Gmail]-Konto verfügen.

## Verbinden von [!DNL Gmail] mit Workfront Fusion {#connect-gmail-to-workfront-fusion}

* [Verbinden  [!DNL Gmail]  Workfront Fusion mit [!DNL Google Workspace]](#connect-gmail-to-workfront-fusion-usinggoogle-workspace)
* [Verbinden  [!DNL Gmail]  Workfront Fusion mit  [!DNL gmail.com] .oder [!DNL googlemail].com](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### Verbinden von [!DNL Gmail] mit Workfront Fusion mithilfe von[!DNL  Google Workspace]

Anweisungen zum Verbinden Ihres [!DNL Google Workspace]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Verbindung erstellen - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

### Verbinden von [!DNL Gmail] mit Workfront Fusion mithilfe von [!DNL gmail.com] oder [!DNL googlemail].com

Wenn Sie [!DNL @gmail.com] oder [!DNL @googlemail.com] Benutzer sind, müssen Sie einen OAuth-Client auf [ erstellen [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) um eine [!UICONTROL Client-ID] und [!UICONTROL Client-Geheimnis] zu erhalten.

Eine schrittweise Anleitung zum Erstellen des OAuth-Clients und zum Abrufen einer [!UICONTROL Client-ID] und eines [!UICONTROL Client-Geheimnisses] finden Sie unter [Verbinden von Adobe Workfront Fusion mit Google-Services mithilfe eines benutzerdefinierten OAuth-Clients](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## [!DNL Gmail] Module und ihre Felder

Beim Konfigurieren von [!DNL Gmail] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Gmail] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Iteratoren](#iterators)

### Trigger

#### [!UICONTROL E-Mails ansehen]

Dieses Trigger-Modul führt ein Szenario aus, wenn eine neue E-Mail zur Verarbeitung empfangen wird.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz oder den Datensätzen verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den E-Mail-Ordner aus, den Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filtertyp] </td> 
   <td> <p>Filtertyp auswählen, der zum Ansehen von E-Mails verwendet werden soll</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Einfacher Filter]</strong> </p> <p>Füllen Sie die Felder [!UICONTROL Criteria], [!UICONTROL Absender Email Address], [!UICONTROL Subject] und [!UICONTROL Search Phrase] aus</p> </li> 
     <li> <p> <strong>[!UICONTROL Gmail-Filter]</strong> </p> <p>Geben Sie im Feld [!UICONTROL-Abfrage] die Abfrage ein, die Sie zum Filtern von E-Mails verwenden möchten.</p> <p>Weitere Informationen zu [!DNL Gmail] finden Sie unter <a href="https://support.google.com/mail/answer/7190">Suchvorgänge verfeinern</a> in der [!DNL Gmail].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Kriterien]</td> 
   <td>Wählen Sie aus, ob Sie [!UICONTROL Alle E-Mails], [!UICONTROL Nur E-Mails lesen] oder [!UICONTROL Nur ungelesene E-Mails lesen] möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Absender-E-Mail-Adresse]</td> 
   <td> <p> Geben Sie eine E-Mail-Adresse ein, um nur E-Mails anzuzeigen, die von dieser Adresse gesendet wurden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Betreff]</td> 
   <td>Geben Sie eine Textzeichenfolge ein, um nur E-Mails anzusehen, die diese Textzeichenfolge im Betreff enthalten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suchbegriff]</td> 
   <td>Geben Sie eine Textzeichenfolge ein, um nur E-Mails anzuzeigen, die diese Textzeichenfolge an einer beliebigen Stelle in der E-Mail enthalten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL E-Mail-Nachricht(en) beim Abrufen als gelesen markieren]</td> 
   <td> <p> Aktivieren Sie diese Option, um abgerufene E-Mails als gelesen zu markieren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl an Ergebnissen]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Ergebnissen fest, mit denen Workfront Fusion während eines Zyklus arbeiten soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

<!--* [Add labels](#add-labels)-->
* [[!UICONTROL Kopieren einer E-Mail]](#copy-an-email)
* [[!UICONTROL Entwurf erstellen]](#create-a-draft)
* [[!UICONTROL E-Mail löschen]](#delete-an-email)
  <!--* [Delete labels](#delete-labels)-->
* [[!UICONTROL Markieren einer E-Mail als gelesen]](#mark-an-email-as-read)
* [[!UICONTROL Markieren einer E-Mail als ungelesen]](#mark-an-email-as-unread)
* [[!UICONTROL Verschieben einer E-Mail]](#move-an-email)
* [[!UICONTROL E-Mail-Kennzeichnungen ändern]](#modify-email-labels)
* [[!UICONTROL E-Mail senden]](#send-an-email)
  <!--* [Set labels](#set-labels)-->

<!--#### Add labels-->

#### [!UICONTROL Kopieren einer E-Mail]

Dieses Aktionsmodul kopiert einen E-Mail- oder E-Mail-Entwurf in einen von Ihnen angegebenen Ordner.

Sie geben den Ordner, den Zielordner und die ID der E-Mail an.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Quellordner aus, der die E-Mail enthält, die Sie kopieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zielordner]</td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Zielordner aus, in den Sie die E-Mail kopieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL E-Mail-ID (UID)]</td> 
   <td> <p>Geben Sie die E-Mail-ID der E-Mail ein, die Sie kopieren möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Entwurf erstellen]

Dieses Aktionsmodul erstellt einen neuen E-Mail-Entwurf und fügt ihn einem von Ihnen angegebenen Ordner hinzu.

Sie geben den Ordner an, in dem Sie einen Entwurf erstellen möchten.

Das Modul gibt die ID des E-Mail-Entwurfs und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Ordner aus, in dem Sie einen Entwurf erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL nach] </td> 
   <td> <p>Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie dann die E-Mail-Adresse für jeden Empfänger ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Betreff] </td> 
   <td> <p>Geben Sie den E-Mail-Betreff ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Inhalt] </td> 
   <td> <p>Geben Sie den E-Mail-Inhalt (Nachrichtentext) ein oder ordnen Sie ihn zu. HTML-Tags sind zulässig.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Anlagen] </td> 
   <td> <p>Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong>, um einen Anhang hinzuzufügen. Sie können eine Datei aus den vorherigen Modulen zuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Empfänger kopieren]</td> 
   <td> <p> Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie dann die E-Mail-Adresse für jeden Kopierempfänger ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Empfänger von Blind Copies]</td> 
   <td> <p> Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie dann die E-Mail-Adresse für jeden Blind Copy-Empfänger ein oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL E-Mail löschen]

Dieses Aktionsmodul entfernt eine E-Mail oder einen E-Mail-Entwurf aus einem von Ihnen angegebenen Ordner.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] Nachrichten-ID]</p> </td> 
   <td> <p>Geben Sie die E-Mail-ID der E-Mail ein, die Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Dauerhaft] </td> 
   <td> <p>Aktivieren Sie diese Option, damit das Modul die E-Mail dauerhaft löschen kann, anstatt sie in den Papierkorb-Ordner zu verschieben.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Delete labels-->



#### [!UICONTROL Markieren einer E-Mail als gelesen]

Dieses Aktionsmodul markiert eine E-Mail als gelesen.

Sie geben die ID der E-Mail und ihren Ordner an.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Ordner aus, der die E-Mail enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL E-Mail-ID (UID)]</td> 
   <td> <p> E-Mail-ID eingeben oder zuordnen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Markieren einer E-Mail als ungelesen]

Dieses Aktionsmodul kennzeichnet eine E-Mail oder einen E-Mail-Entwurf als ungelesen.

Sie geben die ID der E-Mail und ihren Ordner an.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Ordner aus, der die E-Mail enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL E-Mail-ID (UID)] </td> 
   <td> <p>Geben Sie die E-Mail-ID der E-Mail ein, die Sie als ungelesen markieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL E-Mail-Kennzeichnungen ändern]

Dieses Aktionsmodul ändert die Beschriftung einer von Ihnen angegebenen E-Mail-Nachricht.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] Nachrichten-ID]</td> 
   <td> <p> Geben Sie die E-Mail-ID der E-Mail ein, die Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL hinzuzufügende Kennzeichnungen]</p> </td> 
   <td> <p>Wählen Sie die Bezeichnung aus, die Sie der ausgewählten E-Mail-Nachricht hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL zu entfernende Kennzeichnungen]</td> 
   <td> <p> Wählen Sie die Bezeichnung aus, die Sie aus der ausgewählten E-Mail-Nachricht entfernen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!UICONTROL  Felder ]Beschriftung hinzufügen“ und [!UICONTROL Beschriftung entfernen] werden nur von Benutzenden erstellte Beschriftungen geladen.

#### [!UICONTROL Verschieben einer E-Mail]

Dieses Aktionsmodul verschiebt eine E-Mail oder einen E-Mail-Entwurf in einen von Ihnen angegebenen Ordner.

Sie geben den Ordner, den Zielordner und die ID der E-Mail an.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Ordner] </td> 
   <td> <p>Wählen Sie den [!DNL Gmail] Quellordner aus, der die zu verschiebende E-Mail enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zielordner]</td> 
   <td> <p> Wählen Sie den [!DNL Gmail] Zielordner aus, in den Sie die E-Mail verschieben möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL E-Mail-ID (UID)]</td> 
   <td> <p> Geben Sie die E-Mail-ID der E-Mail ein, die Sie verschieben möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL E-Mail senden]

Dieses Aktionsmodul sendet eine neue E-Mail.

Sie geben den Empfänger der E-Mail an.

Das Modul gibt die ID der E-Mail und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Gmail]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Gmail] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL from]</td> 
   <td> <p>Geben Sie eine Absender-E-Mail-Adresse ein oder mappen Sie sie.</p> <p>Hinweis: Wenn Sie eine falsche E-Mail-Adresse eingeben, kann beim Senden einer Nachricht ein Fehler auftreten, da Ihr Konto möglicherweise nicht berechtigt ist, E-Mails von einer anderen Adresse als Ihrer eigenen zu senden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL nach] </td> 
   <td> <p>Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie dann die E-Mail-Adresse für jeden Empfänger ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Betreff] </td> 
   <td> <p>Geben Sie den E-Mail-Betreff ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Inhalt] </td> 
   <td> <p>Geben Sie den E-Mail-Inhalt (Nachrichtentext) ein oder ordnen Sie ihn zu. HTML-Tags sind zulässig.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Anlagen] </td> 
   <td> <p>Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong>, um einen Anhang hinzuzufügen. Sie können eine Datei aus den vorherigen Modulen zuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Empfänger kopieren]</td> 
   <td> <p> Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie dann die E-Mail-Adresse für jeden Kopierempfänger ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Empfänger von Blind Copies]</td> 
   <td> <p> Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong> und geben Sie dann die E-Mail-Adresse für jeden Blind Copy-Empfänger ein oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Set labels-->

### Iteratoren

#### [!UICONTROL Iterieren von Anhängen]

Sie können E-Mail-Anhänge iterieren. Jeder Anhang ist ein separates Bundle in der -Ausgabe des Moduls. Weitere Informationen finden Sie unter [Iterator-Modul](/help/workfront-fusion/references/modules/iterator-module.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source-Modul] </td> 
   <td> <p>Wählen Sie das Modul aus, von dem aus Sie Anlagen iterieren möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>
