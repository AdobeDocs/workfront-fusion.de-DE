---
title: OpenAI-Module (ChatGPT)
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die OpenAIT (ChatGPT) verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: c8138d82-fa5a-4e69-b3cb-aa232099cb33
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 0%

---

# [!DNL OpenAI (ChatGPT & DALL-E)]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL OpenAI (ChatGPT & DALL-E)] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

Um [!DNL OpenAI (ChatGPT & DALL-E)] Module verwenden zu können, müssen Sie über ein [!DNL OpenAI]-Konto verfügen, einschließlich eines API-Schlüssels und einer Organisations-ID.

## OpenAI (ChatGPT &amp; DALL-E) API-Informationen

Der OpenAI-Connector (ChatGPT &amp; DALL-E) verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.11.1</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL OpenAI (ChatGPT & DALL-E)] mit Workfront Fusion

Sie können direkt aus einem [!DNL OpenAI (ChatGPT & DALL-E)]-Modul heraus eine Verbindung zu Ihrem [!DNL OpenAI (ChatGPT & DALL-E)]-Konto herstellen.

1. Klicken Sie in einem [!DNL OpenAI (ChatGPT & DALL-E)] Modul **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Geben Sie die folgenden Informationen ein:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Verbindungsname]</p> </td> 
      <td> <p>Geben Sie einen Namen für die neue Verbindung ein.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API-Schlüssel]</td> 
      <td>Sie können Ihren API-Schlüssel in Ihren OpenAI-Benutzereinstellungen finden.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Organisations-ID] </td> 
      <td>Sie können Ihre Organisations-ID auf der Seite „Organisationseinstellungen“ in OpenAI finden.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.


## [!DNL OpenAI (ChatGPT & DALL-E)] Module und ihre Felder

Beim Konfigurieren von [!DNL OpenAI (ChatGPT & DALL-E)] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL OpenAI (ChatGPT & DALL-E)] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Erstellen eines Abschlusses

>[!IMPORTANT]
>
>Dieses Modul wird nicht mehr unterstützt.

<!--

This action module creates a completion for the provided prompt or chat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Enter or map the ID of the model to use. You can use the Get models module to see all of your available models. </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Temperature]</td> 
   <td> This value must be between 0 and 2, and determines the randomness of the output. Higher values produce output that is more random, while lower values produce more focused output. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating completions in the <a href="https://platform.openai.com/docs/api-reference/completions/create" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### Erstellen einer Moderation

Dieses Aktionsmodul ermittelt, ob Text gegen die Inhaltsrichtlinie von OpenAI verstößt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL OpenAI (ChatGPT & DALL-E)]-Kontos mit Workfront Fusion finden Sie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL OpenAI (ChatGPT & DALL-E)] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eingabe]</td> 
   <td> Klicken Sie für jedes Textbeispiel, das Sie einbeziehen möchten, auf <b>Element hinzufügen</b> und geben Sie den Text ein oder ordnen Sie ihn zu. Einschließen des gesamten Textbeispiels.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Modell]</td> 
   <td> Geben Sie die ID des zu verwendenden Modells ein oder mappen Sie sie. Mit dem Modul Modelle abrufen können Sie alle verfügbaren Modelle anzeigen. </td> 
  </tr> 
 </tbody> 
</table>

### Erstellen und bearbeiten

Dieses Aktionsmodul gibt eine bearbeitete Version einer von Ihnen bereitgestellten Eingabeaufforderung zurück, die Ihren Anweisungen entspricht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL OpenAI (ChatGPT & DALL-E)]-Kontos mit Workfront Fusion finden Sie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL OpenAI (ChatGPT & DALL-E)] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Modell]</td> 
   <td> Geben Sie die ID des zu verwendenden Modells ein oder mappen Sie sie. Mit dem Modul Modelle abrufen können Sie alle verfügbaren Modelle anzeigen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eingabe]</td> 
   <td> Geben Sie den Text ein, den Sie bearbeiten möchten, oder ordnen Sie ihn zu. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Anweisung]</td> 
   <td> Geben Sie die Anweisungen für die Bearbeitung ein oder ordnen Sie sie zu. Beispiel: „Korrigieren Sie die Rechtschreibfehler.“ </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Erweiterte Einstellungen]</td> 
   <td> <p>Informationen zu den optionalen erweiterten Einstellungen in diesem Modul finden Sie in den Informationen zum Erstellen von Bearbeitungen in der <a href="https://platform.openai.com/docs/api-reference/edits/create" class="MCXref xref">OpenAI-API-Dokumentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Erstellen einer Einbettung

Dieses Aktionsmodul erstellt einen Einbettungsvektor, der den Eingabetext darstellt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL OpenAI (ChatGPT & DALL-E)]-Kontos mit Workfront Fusion finden Sie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL OpenAI (ChatGPT & DALL-E)] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Modell]</td> 
   <td> Geben Sie die ID des zu verwendenden Modells ein oder mappen Sie sie. Mit dem Modul Modelle abrufen können Sie alle verfügbaren Modelle anzeigen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Einzubettender Eingabetext]</td> 
   <td> Geben Sie den Text ein, den Sie einbetten möchten, oder ordnen Sie ihn zu. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Benutzer-ID]</td> 
   <td> Geben Sie eine eindeutige Kennung ein, die Ihren Endbenutzer repräsentiert, oder ordnen Sie sie zu, was OpenAI dabei helfen kann, Missbrauch zu überwachen und zu erkennen </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Geben Sie die maximale Anzahl von Bearbeitungen ein, mit denen das Modul während jedes Szenario-Ausführungszyklus arbeiten soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### Chat-Abschluss erstellen

Dieses Aktionsmodul gibt bei einer Liste von Nachrichten, die eine Konversation beschreiben, eine Antwort zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL OpenAI (ChatGPT & DALL-E)]-Kontos mit Workfront Fusion finden Sie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL OpenAI (ChatGPT & DALL-E)] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Modell]</td> 
   <td> Geben Sie die ID des zu verwendenden Modells ein oder mappen Sie sie. Mit dem Modul Modelle abrufen können Sie alle verfügbaren Modelle anzeigen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Nachrichten]</td> 
   <td>Nachrichten beschreiben das bisherige Gespräch. Klicken Sie für jede Nachricht, die Sie hinzufügen möchten<b> auf „Element hinzufügen</b> und füllen Sie Folgendes aus:
   <ul>
   <li> <b>Rolle</b>: Wählen Sie die Rolle des Autors dieser Nachricht aus.</li>
   <li> <b>Inhalt</b>: Geben Sie den Inhalt dieser Nachricht ein oder ordnen Sie ihn zu.</li>
   <li> <b>Name</b>: Geben Sie den Namen des Autors dieser Nachricht ein oder mappen Sie ihn. Der Name kann Groß- und Kleinbuchstaben, Zahlen und Unterstriche enthalten. Die maximale Länge für den Namen beträgt 64 Zeichen.</li>
   </ul>
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Erweiterte Einstellungen]</td> 
   <td> <p>Informationen zu den optionalen erweiterten Einstellungen in diesem Modul finden Sie in den Informationen zum Erstellen von Chat-Fertigstellungen in der <a href="https://platform.openai.com/docs/api-reference/chat/create" class="MCXref xref">OpenAI-API-Dokumentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Edit image

This action module makes edits or creates variations of existing images.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to create edits or variations of the image.
   <p>NOTE: Images must be a valid PNG file, less than 4MB, and square. If mask is not provided, the image must have transparency, which will be used as the mask.</p> 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Text description of desired image]</td> 
   <td> <p>If editing an image, enter or map a description of the edits you want to create. Maximum length is 1000 characters.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating image edits or variations in the <a href="https://platform.openai.com/docs/api-reference/images/createEdit" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### Erstellen von Bildern

Dieses Aktionsmodul generiert oder bearbeitet Bilder mit Dall-E-Modellen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL OpenAI (ChatGPT & DALL-E)]-Kontos mit Workfront Fusion finden Sie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL OpenAI (ChatGPT & DALL-E)] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Textbeschreibung des gewünschten Bildes]</td> 
   <td> Geben Sie eine Beschreibung des gewünschten Bildes ein oder mappen Sie sie. Die maximale Länge der Beschreibung beträgt 1.000 Zeichen. 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Erweiterte Einstellungen]</td> 
   <td> <p>Informationen zu den optionalen erweiterten Einstellungen in diesem Modul finden Sie in den Informationen zum Erstellen von Bildern in der <a href="https://platform.openai.com/docs/api-reference/images/create" class="MCXref xref">OpenAI-API-Dokumentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Abrufen von Modellen

In diesem Modul werden die verschiedenen in der OpenAI-API verfügbaren Modelle aufgelistet und beschrieben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL OpenAI (ChatGPT & DALL-E)]-Kontos mit Workfront Fusion finden Sie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL OpenAI (ChatGPT & DALL-E)] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Aktion]</td> 
   <td> Wählen Sie aus, ob Sie eine Liste aller Modelle erhalten oder ein bestimmtes Modell abrufen möchten.
    <ul>
    <li><p><b>Auflisten von Modellen </b></p><p>Diese Aktion listet die derzeit verfügbaren Modelle auf und stellt grundlegende Informationen zu jedem Modell bereit, z. B. den Eigentümer und die Verfügbarkeit.</p></li>
    <li><p><b>Modell abrufen </b></p><p>Geben Sie die ID des Modells ein, das Sie abrufen möchten, oder ordnen Sie sie zu. </p></li>
   </ul>
 </td> 
  </tr>
 </tbody> 
</table>

### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt eine benutzerdefinierte HTTP-Anfrage an die OpenAI-API aus.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL OpenAI (ChatGPT & DALL-E)]-Kontos mit Workfront Fusion finden Sie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL OpenAI (ChatGPT & DALL-E)] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Pfad relativ zu <code>https://api.openai.com/v1/</code> eingeben </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen automatisch hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
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

<!--

### Manage Audio

This action modules converts audio to text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to transcribe the audio into the input language, or into English.
   <p>If transcribing into the input language, you can select the language in this module's advanced settings. </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Enter or map the maximum number of edits you want the module to work with during each scenario execution cycle.</td> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating transcriptions in the <a href="https://platform.openai.com/docs/api-reference/audio/createTranscription" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

-->

### Verwalten von Dateien

Dieses Aktionsmodul listet, löscht oder ruft Dateien oder Dateiinhalte ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL OpenAI (ChatGPT & DALL-E)]-Kontos mit Workfront Fusion finden Sie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL OpenAI (ChatGPT & DALL-E)] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Aktion]</td> 
   <td> Wählen Sie die Aktion aus, die Sie durchführen möchten. 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td> Wenn Sie eine Datei löschen oder eine Datei oder einen Dateiinhalt abrufen, geben Sie die ID der Datei ein bzw. mappen Sie sie. 
  </tr> 
</tbody>
</table>

### Optimierungen verwalten

Verwalten Sie Optimierungsaufträge, um ein Modell an Ihre spezifischen Schulungsdaten anzupassen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL OpenAI (ChatGPT & DALL-E)]-Kontos mit Workfront Fusion finden Sie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL OpenAI (ChatGPT & DALL-E)] mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorgang auswählen]</td> 
   <td> Wählen Sie die Aktion aus, die Sie durchführen möchten.
   <ul>
   <li><p>Optimieren eines Modells aus einem Datensatz</p><p>Geben Sie eine Beschreibung für das gewünschte Bild ein oder mappen Sie sie.</p>
     <li><p>Abrufen von Informationen über einen Feinabstimmungsauftrag</p><p>Geben Sie die Kennung des Vorgangs ein oder mappen Sie sie.</p>
   <li><p>Abbrechen von Optimierungsaufträgen</p><p>Geben Sie die Kennung des Vorgangs ein oder mappen Sie sie.</p>
   <li><p>Abbrechen von Optimierungsaufträgen</p><p>Geben Sie die Kennung des Vorgangs ein oder mappen Sie sie.</p>
   <li><p>Abrufen von Statusaktualisierungen für einen Optimierungsauftrag</p><p>Geben Sie die ID des Auftrags ein oder mappen Sie sie und wählen Sie aus, ob Sie diese Aktualisierungen streamen möchten.</p>
   <li><p>Löschen eines angepassten Modells</p><p>Geben Sie die ID des Modells ein, das Sie löschen möchten, oder ordnen Sie sie zu.</p>
 </ul> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td> Wenn Sie eine Datei löschen oder eine Datei oder einen Dateiinhalt abrufen, geben Sie die ID der Datei ein bzw. mappen Sie sie. 
  </tr> 
</tbody>
