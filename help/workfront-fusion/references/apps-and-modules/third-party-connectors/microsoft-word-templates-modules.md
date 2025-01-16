---
title: Microsoft Word-Vorlagenmodule
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Microsoft Word-Vorlagen verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: a5ba5634-226b-4886-a4f1-3a14948c1605
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '1286'
ht-degree: 0%

---

# [!DNL Microsoft Word Template]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Microsoft Word Templates] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td> <p>[!UICONTROL [!DNL Workfront Fusion] Arbeit für Automatisierung und Integration] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu nutzen.</td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">Access level configurations*</td> 
    <td> 
      <p>You must be a Workfront Fusion administrator for your organization.</p>
     --> <!--
      <p>You must be a Workfront Fusion administrator for your team.</p>
     --> </td> 
   </tr>
 </tbody> 
</table>

Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Voraussetzungen

Um [!DNL Miscrosoft Word Templates] mit [!DNL Adobe Workfront Fusion] verwenden zu können, muss ein [!DNL Office 365] Konto vorhanden sein. Sie können `www.office.com` eine erstellen.



## Verbinden des [!DNL Office]-Services mit [!DNL Workfront Fusion]

Anweisungen zum Verbinden Ihres [!DNL Office]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung zu [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
>
>Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.

## Verwenden von [!DNL Microsoft Word Templates]

Sie können ein [!DNL Microsoft Word Template]-Modul verwenden, um Daten aus mehreren Web-Services in einem [!DNL Microsoft Word]-Dokument zusammenzuführen.

Sie können beispielsweise diese [!DNL Microsoft Word] verwenden:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-before-filled-350x62.png)

So erstellen Sie dieses Dokument:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-exampled-filled-350x85.png)

## Über Wert-Tags

Eine [!DNL Microsoft Word] ist ein reguläres [!DNL Microsoft Word]-Dokument (.docx-Datei) mit speziellen Tags in seinem Text, die bestimmen, wo und wie Daten zusammengeführt oder ausgefüllt werden sollen. Es gibt drei Arten von Tags:

* [Einfaches Wert-Tag](#simple-value-tag)
* [Bedingungs-Tag](#condition-tag)
* [Loop-Tag](#loop-tag)

### Einfaches Wert-Tag {#simple-value-tag}

Ein einfaches Wert-Tag wird einfach durch einen entsprechenden Wert ersetzt. Der Name des Tags entspricht dem Wert des [!UICONTROL Key], der in doppelten geschweiften Klammern steht, z. B. `{{name}}`.

**Beispiel** Um ein Dokument zu erstellen, in dem „Hallo Petr!“ steht, können Sie ein [!DNL Microsoft Word Template] Modul verwenden, um die folgende Vorlage zu erstellen:

```
> Hi {{name}}!
```

Richten Sie dazu das Modul wie folgt ein:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-simple-value-350x286.png)

### Bedingungs-Tag {#condition-tag}

Sie können ein Bedingungs-Tag verwenden, um Text einzuschließen, der nur gerendert werden soll, wenn bestimmte Bedingungen erfüllt sind. Um den Text einzuschließen, platzieren Sie ihn zwischen öffnenden und schließenden Bedingungs-Tags, z. B. „hasPhone“, wenn die Bedingung ist, ob die Daten eine Telefonnummer enthalten oder nicht. Dem Namen eines öffnenden Tags wird ein Hash-Zeichen # vorangestellt, dem Namen eines schließenden Tags wird ein Schrägstrich / vorangestellt, wie im folgenden Beispiel gezeigt.

**Beispiel** Um ein Dokument zu erstellen, das die Telefonnummer eines Kunden enthält, wenn die Eingabedaten eine Telefonnummer, aber keine E-Mail-Adresse enthalten, können Sie ein [!DNL Microsoft Word Template] verwenden und die folgende Vorlage erstellen:

```
> {{#hasPhone}}Phone: {{phone}} {{/hasPhone}}
> {{#hasEmail}}Email: {{email}} {{/hasEmail}}
```

Richten Sie dazu das Modul wie folgt ein:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-conditional-350x501.png)

Im Dokument würde die Telefonnummer wie folgt angezeigt:

```
> Phone: 4445551234
```

### Loop-Tag {#loop-tag}

Sie können ein Schleifen-Tag, auch als Abschnittstags bezeichnet, verwenden, um einen Textabschnitt zu wiederholen. Umschließen Sie den Text, indem Sie ihn zwischen den öffnenden und schließenden Schleifen-Tags platzieren. Dem Namen eines öffnenden Tags wird ein Hash-Zeichen # vorangestellt; dem Namen eines schließenden Tags wird ein Schrägstrich / vorangestellt.

* [Loop-Tag mit dem Modul Dokument ausfüllen](#loop-tag-with-fill-out-a-document-module)
  <!-- [Loop tag with Fill a document with a batch of data module](#loop-tag-with-fill-a-document-with-a-batch-of-data-module)-->

#### Loop-Tag mit dem Modul Dokument ausfüllen {#loop-tag-with-fill-out-a-document-module}

**Beispiel** Um ein Dokument zu erstellen, das den Namen und die Telefonnummer jedes Kontakts in einer Kundenliste auflistet, können Sie ein [!DNL Microsoft Word Template] Modul verwenden und die folgende Vorlage erstellen:

```
> {{#contact}}
>     {{name}}, {{phone}}
> {{/contact}}
```

Richten Sie dazu das Modul wie folgt ein:


![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-fill-out-a-document-350x732.png)

Das Modul würde das folgende Dokument erstellen:

```
> Jan Toman, 4445551234
> Eduard Salo, 4445552345
```

<!--

#### Loop tag with Fill a document with a batch of data module {#loop-tag-with-fill-a-document-with-a-batch-of-data-module}

**Example:** You can export Google contacts into a table that you create using loop tags.

The first module loads the template. The next module retrieves all contacts from the group you specify in [!DNL Google Contacts]. The aggregator module aggregates all values retrieved from Google Contacts and merges them into the template. And the last module saves the filled template to the desired location.

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-scenario-350x124.png)

You could use this scenario with the following template:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-template-350x26.png)

To do this, you would set up the module as follows:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-module-setup-350x323.png)

The module would create the following document:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-document-350x46.png)
-->

## [!DNL Microsoft Word Template]

Für diese Module ist keine Verbindung erforderlich.

* [Füllen Sie ein Dokument aus](#fill-out-a-document)
* [Ausfüllen eines Dokuments mit einem Datenstapel](#fill-a-document-with-a-batch-of-data)

### [!UICONTROL Fill out a document] {#fill-out-a-document}

Mit diesem Transformatormodul können Sie ein Dokument mit von Ihnen angegebenen Daten füllen. Es kann mit einfachen Werten, Tags, bedingten Tags oder Schleifen-Tags verwendet werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start delimiter of the text being replaced]</td> 
   <td> <p>Geben Sie die Zeichen ein, die den Anfang des zu ersetzenden Textes markieren sollen. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>Geben Sie <code>&#91;&#91;</code> ein, wenn Sie einen ähnlichen Text ersetzen möchten: <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL End delimiter of the text being replaced]</p> </td> 
   <td> <p>Geben Sie die Zeichen ein, die am Ende des zu ersetzenden Textes stehen sollen. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>Geben Sie <code>&#93;&#93;</code> ein, wenn Sie einen ähnlichen Text ersetzen möchten: <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p> Ordnen Sie die Datei zu, die Sie aus dem vorherigen Modul hochladen möchten (z. B. das Modul HTTP &gt; Datei abrufen oder Dropbox &gt; Dateimodul abrufen ). Oder geben Sie die Datendatei manuell ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of filled out file]</td> 
   <td>Geben Sie einen Dateinamen (einschließlich Erweiterung) für die Zielausgabedatei ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data source]</td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, ob die von Ihnen verwendeten Daten aus einem Formular oder aus einer Rohdatenerfassung (nicht verarbeitete Computerdaten) stammen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>Dies muss ein Array von Sammlungen sein, wobei:</p> 
    <ul> 
     <li>Jede Sammlung entspricht einem Dateneintrag und enthält ein Element <code>entry</code></li> 
     <li>Element <code>entry </code>enthält eine Sammlung der <code>key </code>und <code>value</code></li> 
     <li>Element <code>key </code>enthält den Namen des Tags</li> 
     <li>Element <code>value </code>enthält den Wert des Tags</li> 
    </ul> 
    <p>Einen Eintrag hinzufügen:</p>
    <ol> 
     <li> Klicken Sie auf <b>[!UICONTROL Add Item]</b>. </li> 
     <li>Wählen Sie den Werttyp des Eintrags aus.</li> 
     <li>Fügen Sie den Namen und Wert hinzu. Weitere Informationen finden Sie im Beispiel für den ausgewählten Wertetyp in diesem Artikel. 
      <ul> 
       <li><a href="#simple-value-tag" class="MCXref xref">Einfaches Wert-Tag</a></li> 
       <li><a href="#condition-tag" class="MCXref xref">Bedingungs-Tag</a></li> 
       <li><a href="#loop-tag" class="MCXref xref">Loop-Tag</a></li> 
      </ul></li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Fill a document with a batch of data] {#fill-a-document-with-a-batch-of-data}

Dieses Aggregator-Modul ist nützlich, wenn Ihre Dateneinträge als separate Bundles vorliegen. Mit diesem Modul können Sie einfach die für das Wertefeld erforderliche Struktur einrichten und jedem Wertelement Elemente zuordnen. Im Gegensatz zum Modul Dokument ausfüllen erlaubt das Feld Werte im Modul Dokument mit einem Batch von Daten ausfüllen nur einen einzigen Eintrag, der Variablen enthält.

Sie können dieses Modul auch verwenden, wenn Ihre Dateneinträge als Array eingehen, indem Sie das Modul *Iterator* verwenden, um den Inhalt des Arrays in eine Reihe von Bundles umzuwandeln.

Die tatsächlichen Werte werden für jedes eingehende Bundle erstellt und ausgefüllt. Die Vorlage wird erstellt, nachdem alle Eingabepakete verarbeitet wurden.

Dieses Aggregator-Modul ist besonders nützlich für die Erstellung von Listen oder Berichten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td>Wählen Sie das Modul aus, das die Quelle Ihres Textes ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start delimiter of the text being replaced]</td> 
   <td> <p>Geben Sie die Zeichen ein, die den Anfang des zu ersetzenden Textes markieren sollen. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>Geben Sie <code>&#91;&#91;</code> ein, wenn Sie einen ähnlichen Text ersetzen möchten: <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL End delimiter of the text being replaced]</p> </td> 
   <td> <p>Geben Sie die Zeichen ein, die am Ende des zu ersetzenden Textes stehen sollen. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span>Geben Sie <code>&#93;&#93;</code> ein, wenn Sie einen ähnlichen Text ersetzen möchten: <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by]</td> 
   <td> Definieren Sie einen Ausdruck, der ein oder mehrere zugeordnete Elemente enthält. Die aggregierten Daten werden unter Gruppen mit demselben Ausdruckswert getrennt. Jede Gruppe gibt als separates Bundle aus, das einen Schlüssel mit dem ausgewerteten Ausdruck und dem aggregierten Text enthält. Auf diese Weise können Sie den Schlüssel als Filter in nachfolgenden Modulen verwenden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Aktivieren Sie diese Option, um die Verarbeitung zu stoppen, wenn eine Aggregation keine Bundles enthält.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p> Ordnen Sie die Datei zu, die Sie aus dem vorherigen Modul hochladen möchten (z. B. das Modul HTTP &gt; Datei abrufen oder Dropbox &gt; Dateimodul abrufen ). Oder geben Sie die Datendatei manuell ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of filled out file]</td> 
   <td>Geben Sie einen Dateinamen (einschließlich Erweiterung) für die Zielausgabedatei ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data source]</td> 
   <td> <p>Wählen Sie eine Option aus, um anzugeben, ob die von Ihnen verwendeten Daten aus einem Formular oder aus einer Rohdatenerfassung (nicht verarbeitete Computerdaten) stammen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>Dies muss ein Array von Sammlungen sein, wobei:</p> 
    <ul> 
     <li>Jede Sammlung entspricht einem Dateneintrag und enthält ein Element <code>entry</code></li> 
     <li>Element <code>entry </code>enthält eine Sammlung der <code>key </code>und <code>value</code></li> 
     <li>Element <code>key </code>enthält den Namen des Tags</li> 
     <li>Element <code>value </code>enthält den Wert des Tags</li> 
    </ul> 
    <p>Einen Eintrag hinzufügen:</p>
    <ol> 
     <li> Klicken Sie auf <b>[!UICONTROL Add Item]</b>. </li> 
     <li>Wählen Sie den Werttyp des Eintrags aus.</li> 
     <li>Fügen Sie den Namen und Wert hinzu. Weitere Informationen finden Sie im Beispiel für den ausgewählten Wertetyp in diesem Artikel. 
      <ul> 
       <li><a href="#simple-value-tag" class="MCXref xref">Einfaches Wert-Tag</a></li> 
       <li><a href="#condition-tag" class="MCXref xref">Bedingungs-Tag</a></li> 
       <li><a href="#loop-tag" class="MCXref xref">Loop-Tag</a></li> 
      </ul></li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>
