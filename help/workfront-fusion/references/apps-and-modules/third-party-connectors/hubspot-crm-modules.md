---
title: HubSpot CRM-Module
description: Die  [!DNL Adobe Workfront Fusion] HubSpot CRM-Module ermöglichen es Ihnen, Ereignisse, Datensätze, Kontakte, Interaktionen, Datei- und Formularübermittlungen zu überwachen oder Datensätze, Kontakte, Interaktionen, Ereignisse oder Dateien in Ihrem - [!DNL HubSpot CRM]  zu erstellen, abzurufen, zu aktualisieren und zu löschen.
author: Becky
feature: Workfront Fusion
exl-id: b8a1bbcd-337e-4c92-a1a6-d6d4bab1f440
source-git-commit: 9cea5de748873720247db39161cea12c7e9c7186
workflow-type: tm+mt
source-wordcount: '5530'
ht-degree: 0%

---

# [!DNL HubSpot CRM]

Mit den [!DNL Adobe Workfront Fusion] [!DNL HubSpot CRM]-Modulen können Sie Ereignisse, Datensätze, Kontakte, Interaktionen, Datei- und Formularübermittlungen überwachen oder Datensätze, Kontakte, Interaktionen, Ereignisse oder Dateien in Ihrem [!DNL HubSpot CRM]-Konto erstellen, abrufen, aktualisieren und löschen.

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um [!DNL HubSpot CRM]-Module verwenden zu können, müssen Sie über ein [!DNL HubSpot CRM]-Konto verfügen.

## HubSpot CRM-API-Informationen

Der HubSpot CRM-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://api.hubapi.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v2.0.14</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Adobe Workfront Fusion] mit [!DNL HubSpot CRM] verbinden

Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion]  - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Wählen Sie beim Konfigurieren einer Verbindung den **HubSpot CRM**-Verbindungstyp aus. Der HubSpot-CRM-Typ (veraltet) unterstützt bestehende Verbindungen, wir empfehlen jedoch, ihn nicht zur Erstellung neuer Verbindungen zu verwenden.

## [!DNL HubSpot CRM] Module und ihre Felder

Beim Konfigurieren [!DNL Hubspot CRM] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Hubspot CRM] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [CRM-Objekte](#crm-objects)
* [Datensätze (Abschlüsse, Kontakte und Unternehmen)](#records-deals-contacts-and-companies)
* [Kontakte](#contacts)
* [Angebote](#deals)
* [Firmen](#companies)
* [Interaktionen](#engagements)
* [Ereignisse und Benachrichtigungen](#events-and-notifications)
* [Dateien](#files)
* [Aufgaben](#tasks)
* [Benutzende](#users)
* [Tickets](#tickets)
* [Formulare](#forms)
* [Social Media (Broadcast)](#social-media-broadcast)
* [Blog-Beiträge](#blog-posts)
  <!--* [Workflows]()-->
* [Abonnements](#subscriptions)
  <!--* [Associations]()-->
* [Sonstige](#other)

### CRM-Objekte

<!--* [Search for CRM objects](#search-for-crm-objects)
* [Watch CRM objects](#watch-crm-objects)-->

+++ **[!UICONTROL Search for CRM Objects]**

Dieses Suchmodul sucht nach CRM-Objekten anhand benutzerdefinierter Eigenschaften oder anhand einer Abfrage. Um nach Produkten oder Zeileneinträgen zu suchen, verwenden Sie eine spezielle Verbindung mit einem erforderlichen benutzerdefinierten Bereich.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl an Elementen ein, die das Modul in einem Ausführungszyklus zurückgibt, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type to Search]</td> 
   <td>Wählen Sie den Typ des Hubspot-CRM-Objekts aus, nach dem Sie suchen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Wählen Sie die Eigenschaften aus, die in der Modulausgabe angezeigt werden sollen. Die verfügbaren Felder hängen vom ausgewählten Objekt ab.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by] </td> 
   <td> <p>Bitte auswählen, wie die Suche gefiltert werden soll</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Abfrage eingeben oder zuordnen</p> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>Geben Sie die Gruppen oder Filter für Ihre Suche ein.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Klicken Sie auf , wenn Sie die Ergebnisse sortieren möchten. Wenn Sie die Ergebnisse sortieren, werden die folgenden Felder angezeigt. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Property name]</strong> </p> <p>Wählen Sie die Eigenschaft aus, nach der Sie die Ergebnisse sortieren möchten</p> </li> 
     <li> <p><strong>[!UICONTROL Direction]</strong> </p> <p>Wählen Sie aus, ob die Ergebnisse in auf- oder absteigender Richtung sortiert werden sollen.</p> </li> 
    </ul> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Versatz starten</td> 
    <td>Geben Sie die ID des ersten Elements ein, für das Sie Details abrufen möchten, oder ordnen Sie sie zu. Dieses Modul gibt nur bis zu 5.000 Ergebnisse gleichzeitig zurück. Durch Festlegen eines Startversatzes können Sie andere Elemente als die ersten 5.000 abrufen. Wenn der Startversatz 5000 beträgt, gibt das Modul die Elemente 5000-9999 zurück.</td> 
   </tr>
 </tbody> 
</table>

+++

+++ **CRM-Objekte ansehen**

Dieses Trigger-Modul startet ein Szenario, wenn ein CRM-Objekt erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl an Elementen ein, die das Modul in einem Ausführungszyklus zurückgibt, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object type to search]</td> 
   <td> <p>Wählen Sie den Typ des Objekts aus, nach dem Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Wählen Sie die Eigenschaften aus, die Sie in die Ausgabe für dieses Modul aufnehmen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created/Updated]</td> 
   <td>Wählen Sie aus, ob erstellte (neue) oder aktualisierte (geänderte) Objekte überwacht werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by]</td> 
   <td>Sie können einen Filter hinzufügen, um sicherzustellen, dass das Szenario nur gestartet wird, wenn bestimmte Bedingungen erfüllt sind.<ul><li><b>Abfrage</b><p>Geben Sie die Abfrage ein, nach der Sie filtern möchten.</li><li><b>Eigenschaften</b><p>Klicken Sie für jede Eigenschaft, die Sie zum Filtern von Ergebnissen verwenden möchten<b> auf „Element hinzufügen</b> und geben Sie den Eigenschaftsnamen, den Operator und den Eigenschaftswert ein.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Datensätze (Abschlüsse, Kontakte und Unternehmen)

<!--* [Create a Record](#create-a-record)
* [[!UICONTROL Create a Record (Legacy)]](#create-a-record-legacy)
* [[!UICONTROL Delete a Record]](#delete-a-record)
* [[!UICONTROL Get a Record]](#get-a-record)
* [[!UICONTROL Get a Record Property]](#get-a-record-property)
* [List Records](#list-records)
* [[!UICONTROL Update a Record]](#update-a-record)
* [[!UICONTROL Watch Records]](#watch-records)-->

+++ **Datensatz erstellen**

Mit diesem Aktionsmodul wird ein Kontakt, eine Firma oder ein Abschluss erstellt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>Wählen Sie für jede Eigenschaft, die Sie beim Erstellen des Datensatzes hinzufügen möchten, die Gruppe aus, in der sich die Eigenschaft befindet. Die Eigenschaftengruppe wird geöffnet, und Sie können dann den Wert für die Eigenschaften ausfüllen. Die verfügbaren Eigenschaftengruppen und -eigenschaften hängen vom Typ des Datensatzes ab, den Sie erstellen möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Record (Legacy)]**

Mit diesem Aktionsmodul wird ein Kontakt, ein Unternehmen oder ein Abschluss erstellt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Füllen Sie alle Eigenschaften aus, die Sie für den Datensatz festlegen möchten. Die verfügbaren Felder hängen vom Typ des Datensatzes ab, den Sie erstellen möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Delete a Record]**

Dieses Aktionsmodul löscht einen Kontakt, ein Unternehmen oder einen Abschluss.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Wählen Sie den Typ des Datensatzes aus, den Sie löschen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Kontakts, der Firma oder des Angebots ein, den bzw. das Sie löschen möchten. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ [!UICONTROL Get a Record]

Dieses Aktionsmodul ruft Details zu einem Kontakt, einem Unternehmen oder einem Abschluss ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Wählen Sie den Datensatztyp aus.</p> 
    <ul> 
     <li>[!UICONTROL Contact]</li> 
     <li>[!UICONTROL Company] </li> 
     <li>[!UICONTROL Deal]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td>Wenn Sie einen Kontakt erhalten, wählen Sie aus, ob Sie ihn nach ID oder E-Mail-Adresse identifizieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Kontakts, Unternehmens oder Angebots ein, den Sie abrufen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Geben Sie die E-Mail-Adresse des Kontakts ein, dessen Details Sie abrufen möchten. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Record Property]**

Dieses Aktionsmodul ruft Metadaten für eine bestimmte Datensatzeigenschaft über ihren (internen) Namen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Wählen Sie den Datensatztyp mit der Eigenschaft aus, für die Sie Metadaten abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property Name]</td> 
   <td>Wählen Sie die Eigenschaft aus, für die Sie Metadaten abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Option ID]</td> 
   <td> <p> Einige Eigenschaften verfügen über eine Reihe verfügbarer Optionen, die ein Benutzer als Eigenschaftswert auswählen kann. Geben Sie die ID der Option ein, die den abzurufenden Eigenschaftswert darstellt.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Einträge auflisten**

Dieses Suchmodul gibt eine Liste von Kontakten, Unternehmen oder Angeboten zurück. Die Ausgabe ist auf 5.000 Kontakte, 12.500 Unternehmen oder 12.500 Angebote beschränkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Wählen Sie den Datensatztyp aus, den Sie zurückgeben möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Wählen Sie die Eigenschaften aus, die Sie in die Ausgabe für dieses Modul aufnehmen möchten.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Update a Record]**

Dieses Aktionsmodul aktualisiert einen Kontakt, ein Unternehmen oder einen Abschluss.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Wählen Sie den Typ des Datensatzes aus, den Sie aktualisieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td> <p>Wenn Sie einen Kontakt erhalten, wählen Sie aus, wie Sie den Datensatz identifizieren möchten:</p> 
    <ul> 
     <li> <p>[!UICONTROL ID]</p> </li> 
     <li> <p>[!UICONTROL Email]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Kontakts, Unternehmens oder Angebots ein, den Sie aktualisieren möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Geben Sie die E-Mail-Adresse des Kontakts ein, dessen Details Sie aktualisieren möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Füllen Sie alle Eigenschaften aus, die Sie für den Datensatz festlegen möchten. Die verfügbaren Felder hängen vom Typ des Datensatzes ab, den Sie erstellen möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch Records]**

Dieses Kontaktmodul startet ein Trigger, wenn ein Kontakt, ein Unternehmen oder ein Abschluss innerhalb der letzten 30 Tage geändert oder erstellt wurde. Die Ausgabe ist auf 10.000 Datensätze beschränkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Wählen Sie den Datensatztyp aus, der die Eigenschaft aufweist, die Sie überwachen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>Wählen Sie aus, ob Sie kürzlich geänderte oder kürzlich erstellte Datensätze ansehen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Wählen Sie die Eigenschaften aus, die Sie in die Ausgabe des Moduls aufnehmen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Kontakte

<!--* [[!UICONTROL Add Contacts to a List]](#add-contacts-to-a-list)
* [Create/Update a contact](#createupdate-a-contact)
* [[!UICONTROL Create/Update a Contact (Legacy)]](#createupdate-a-contact-legacy)
* [[!UICONTROL Create/Update a Group of Contacts]](#createupdate-a-group-of-contacts)
* [[!UICONTROL List Contacts]](#list-contacts)
* [[!UICONTROL List Contacts of a Company]](#list-contacts-of-a-company)
* [[!UICONTROL Merge contacts]](#merge-contacts)
* [[!UICONTROL Remove a Contact from a List]](#remove-a-contact-from-a-list)
* [[!UICONTROL Search for Contacts]](#search-for-contacts)
* [Watch Contacts Added to a List](#watch-contacts-added-to-a-list)-->

+++ **[!UICONTROL Add Contacts to a List]**

Dieses Modul fügt Kontakteinträge, die bereits im System erstellt wurden, einer Kontaktliste hinzu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>Wählen Sie die ID der Liste aus, der Sie den Kontakt hinzufügen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs/Emails] </td> 
   <td> <p>Wählen Sie aus, wie Sie die Kontakte identifizieren möchten, die Sie der Liste hinzufügen möchten:</p> 
    <ul> 
     <li> <p>[!UICONTROL IDs]</p> <p>Fügen Sie die IDs der Kontakte hinzu, die Sie der Liste hinzufügen möchten.</p> </li> 
     <li> <p>[!UICONTROL Emails]</p> <p>Fügen Sie die E-Mail-Adressen der Kontakte hinzu, die Sie der Liste hinzufügen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Kontakt erstellen/aktualisieren**

Dieses Aktionsmodul erstellt einen Kontakt, wenn es nicht in einem Portal vorhanden ist. Wenn der Kontakt im Portal vorhanden ist, wird er von diesem Modul mit den angegebenen Werten aktualisiert.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>Wählen Sie für jede Eigenschaft, die Sie beim Erstellen des Kontakts hinzufügen möchten, die Gruppe aus, in der sich die Eigenschaft befindet. Die Eigenschaftengruppe wird geöffnet, und Sie können dann die Werte für die Eigenschaften ausfüllen.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create/Update a Contact (Legacy)]**

Erstellt einen Kontakt, wenn er noch nicht in einem Portal vorhanden ist, oder aktualisiert ihn mit den neuesten Eigenschaftswerten, wenn er noch in einem Portal vorhanden ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Füllen Sie alle Eigenschaften aus, die Sie für den Kontakt festlegen oder aktualisieren möchten. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create/Update a Group of Contacts]**

Erstellt eine Gruppe von Kontakten oder aktualisiert sie, falls sie bereits existieren. Die Leistung ist am besten, wenn die Batch-Größe auf 100 Kontakte oder weniger begrenzt ist. Änderungen, die über diesen Endpunkt vorgenommen wurden, werden asynchron verarbeitet. Es kann also mehrere Minuten dauern, bis Änderungen auf Kontakteinträge angewendet werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Batch of Contacts to Create/Update] </td> 
   <td> <p>Fügen Sie den Stapel der Kontakte hinzu.</p> <p>Klicken Sie auf <strong>[!UICONTROL Add item]</strong> , um einen neuen Kontakt hinzuzufügen. Geben Sie im angezeigten Fenster die folgenden Informationen ein bzw. ordnen Sie sie zu:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search Type]</strong> </p> <p>Bitte auswählen, wie der Kontakt identifiziert werden soll:</p> 
      <ul> 
       <li> <p>[!UICONTROL ID]</p> <p>Geben Sie die ID des Kontakts ein, den Sie erstellen oder aktualisieren möchten. </p> </li> 
       <li> <p>[!UICONTROL Email]</p> <p>Geben Sie die E-Mail-Adresse des Kontakts ein, den Sie erstellen oder aktualisieren möchten. </p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>Füllen Sie alle Eigenschaften aus, die Sie für den Kontakt festlegen oder aktualisieren möchten.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Contacts]**

Gibt alle im Portal erstellten Kontakte aus. Die Ausgabe ist auf 5000 Kontakte begrenzt. Um vorherige oder nächste Kontakte aufzulisten, können Sie den [!UICONTROL advanced]-Parameter verwenden, um die Liste zu versetzen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Die maximale Anzahl von Kontakten, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben soll. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Wählen Sie die Eigenschaften aus, die in der Modulausgabe angezeigt werden sollen. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Kontakt-ID [Start-Offset] </td> 
    <td>Geben Sie die ID des Benutzers ein, den Sie die Liste starten möchten, oder ordnen Sie sie zu. Wenn Sie beispielsweise die Kontakt-ID als ID des 101. Kontakts festlegen, kann das Modul die Kontakte 101-5100 anstatt 1-5000 auflisten. </td> 
   </tr>
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Contacts of a Company]**

Ruft eine Liste der Kontakte im Unternehmen ab. Die Ausgabe ist auf 5000 Kontakte begrenzt. Um vorherige oder nächste Kontakte aufzulisten, können Sie den [!UICONTROL advanced]-Parameter verwenden, um die Liste zu versetzen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID der Firma ein, deren Kontakte Sie auflisten möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Die maximale Anzahl von Kontakten, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben soll. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Kontakt-ID [Start-Offset] </td> 
    <td>Geben Sie die ID des Benutzers ein, den Sie die Liste starten möchten, oder ordnen Sie sie zu. Wenn Sie beispielsweise die Kontakt-ID als ID des 101. Kontakts festlegen, kann das Modul die Kontakte 101-5100 anstatt 1-5000 auflisten. </td> 
   </tr>
 </tbody> 
</table>

+++

+++ **[!UICONTROL Merge contacts]**

Dieses Aktionsmodul führt Kontakte zusammen

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 1] </td> 
   <td>Geben Sie die ID des Kontakts ein, den Sie zusammenführen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 2] </td> 
   <td>Geben Sie die ID des anderen Kontakts ein, den Sie zusammenführen möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Remove a Contact from a List]**

Entfernt einen Kontakt aus einer Kontaktliste.

>[!NOTE]
>
>Kontakte können nicht manuell aus einer dynamischen Liste entfernt werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>Wählen Sie die ID der Liste aus, aus der Sie den Kontakt entfernen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact ID] </td> 
   <td>Geben Sie die ID des Kontakts ein, den Sie aus der Liste entfernen möchten. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search for Contacts]**

Ruft mithilfe der Suchabfrage eine Liste von Kontakten ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>Geben Sie die Suchanfrage ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>Geben Sie die maximale Anzahl an Kontakten ein, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben sollen, oder mappen Sie sie. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch contacts added to a list]**

Dieses Kontaktmodul startet ein Trigger, wenn ein neuer Kontakt zu einer Liste hinzugefügt wird. Dies ist nur für Benutzer mit einem Paid Marketing-Konto verfügbar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Geben Sie die ID der Liste ein, die die Kontakte enthält, die Sie beobachten möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Wählen Sie die Eigenschaften aus, die Sie in die Ausgabe des Moduls aufnehmen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Angebote

<!--* [[!UICONTROL Get a Deal's CRM Pipeline]](#get-a-deals-crm-pipeline)
* [[!UICONTROL List Deal/Ticket Pipelines]](#list-dealticket-pipelines)-->

+++ **[!UICONTROL Get a Deal's CRM Pipeline]**

Gibt eine bestimmte Abschluss-Pipeline zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pipeline ID] </td> 
   <td>Geben Sie die ID der Pipeline ein, für die Sie Details abrufen möchten, oder mappen Sie sie. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stage ID] </td> 
   <td>Geben Sie die ID der Phase ein, für die Sie Details abrufen möchten, oder mappen Sie sie. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Deal/Ticket Pipelines]**

Gibt alle Angebots- und Ticket-Pipelines für ein bestimmtes Portal zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type] </td> 
   <td>Wählen Sie aus, ob Sie Angebote oder Tickets auflisten möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Firmen

+++ **[!UICONTROL Search for Companies by domain]**

Ruft eine Liste von Unternehmen ab, die auf einer exakten Übereinstimmung mit der Domain-Eigenschaft basieren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Domain] </td> 
   <td>Geben Sie die Domain der Unternehmen ein, nach denen Sie suchen möchten, z. B. <code>[!DNL hubspot].com</code>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Die maximale Anzahl von Unternehmen, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben sollen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Wählen Sie die Eigenschaften aus, die in der Modulausgabe angezeigt werden sollen. </td> 
  </tr> 
 </tbody> 
</table>

+++

### Interaktionen

<!--* [Associate an Engagement with a CRM object](#associate-an-engagement-with-a-crm-object)
* [Create an Engagement](#create-an-engagement)
* [Delete an Engagement](#delete-an-engagement)
* [Watch Engagements](#watch-engagements)-->

+++ **Interaktion mit einem CRM-Objekt verknüpfen**

Dieses Aktionsmodul verknüpft eine Interaktion mit einem Kontakt, einem Unternehmen oder einem Abschluss.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Wählen Sie den CRM-Datensatztyp aus, mit dem Sie eine Interaktion verknüpfen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Engagement ID]</td> 
  <td>Geben Sie die ID der Interaktion ein, die Sie mit dem Objekt verknüpfen möchten, oder mappen Sie sie.</td> 
   </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
  <td>Geben Sie die ID des Datensatzes ein, mit dem Sie die Interaktion verknüpfen möchten, oder ordnen Sie sie zu.</td> 
   </tr> 
 </tbody> 
</table>

+++

+++ **Interaktion erstellen**

Dieses Aktionsmodul erstellt eine Interaktion (z. B. eine Notiz, Aufgabe oder Aktivität) mit einem CRM-Objekt in HubSpot. Interaktionen sind jede Interaktion mit einem Kontakt, der im CRM protokolliert werden soll.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Is Active?]</td> 
   <td>Aktivieren Sie diese Option, wenn die neue Interaktion bei ihrer Erstellung aktiv sein soll. Um in der Zeitleiste angezeigt zu werden, muss ein Projekt aktiv sein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
  <td>Wählen Sie den Interaktionstyp aus, den Sie erstellen möchten.
  <ul>
  <li><b>E-Mail</b><p></p>Fahren Sie mit <a href="#email-metadata" class="MCXref xref" >E-Mail-Metadaten</a> fort.</p></li>
  <li><b>Anruf</b><p>Fahren Sie mit <a href="#call-metadata" class="MCXref xref" >Aufrufen von Metadaten</a> fort.</p></li>
  <li><b>Besprechung</b><p>Fahren Sie <a href="#meeting-fields" class="MCXref xref" >Meeting-Felder</a> fort.</p></li>
  <li><b>Aufgabe</b><p>Fahren Sie fort <a href="#task-fields" class="MCXref xref" >Aufgabenfelder</a>.</p></li>
  <li><b>Notiz</b><p>Geben Sie im Feld Textkörper den Text der Anmerkung ein.</p></li>
  </ul>
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Zeitstempel</td> 
   <td>Geben Sie einen Zeitstempel für die Interaktion ein oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Inhaber-ID</td> 
   <td>Geben Sie die Eigentümer-ID der Person ein, der das Projekt zugewiesen werden soll, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UID</td> 
   <td>Geben Sie eine ID für die Interaktion ein oder ordnen Sie sie zu, die über Objekttypen hinweg verwendet werden kann.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Portal-ID</td> 
   <td>Geben Sie die ID des Portals ein oder mappen Sie sie. Dies ist nützlich, wenn Ihr Unternehmen über mehrere Portale verfügt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zugeordnete Kontakte</td> 
   <td>Klicken Sie für jeden Kontakt, mit dem Sie diese Interaktion verknüpfen möchten, auf <b>Element hinzufügen</b> und geben Sie die Kontakt-ID ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verbundene Unternehmen</td> 
   <td>Klicken Sie für jedes Unternehmen, mit dem Sie diese Interaktion verknüpfen möchten, auf <b>Element hinzufügen</b> und geben Sie die Unternehmens-ID ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zugeordnete Angebote</td> 
   <td>Klicken Sie für jeden Deal, mit dem Sie diese Interaktion verknüpfen möchten, auf <b>Element hinzufügen</b> und geben Sie die Deal-ID ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zugeordnete Tickets</td> 
   <td>Klicken Sie für jedes Ticket, mit dem Sie diese Interaktion verknüpfen möchten, auf <b>Element hinzufügen</b> und geben Sie die Ticket-ID ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Anhänge</td> 
   <td>Klicken Sie für jeden Anhang, mit dem Sie diese Interaktion verknüpfen möchten, auf <b>Element hinzufügen</b> und geben Sie die Datei-ID der Datei ein, die Sie anhängen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### E-Mail-Metadaten

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL From > Email]</p> </td> 
   <td> <p>Geben Sie die E-Mail-Adresse, von der die E-Mail gesendet werden soll, ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL First Name]</td> 
   <td>Geben Sie den Vornamen der Person ein, von der die E-Mail gesendet werden soll, oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Last Name]</td> 
  <td>Geben Sie den Nachnamen der Person ein, von der die E-Mail gesendet werden soll, oder mappen Sie ihn.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Bis</td> 
   <td>Klicken Sie für jede E-Mail-Adresse, an die Sie die E-Mail senden möchten<b> auf „Element hinzufügen</b> und geben Sie die E-Mail-Adresse ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">CC</td> 
   <td>Klicken Sie für jede E-Mail-Adresse, an die Sie die E-Mail CC senden möchten<b> auf „Element hinzufügen</b> und geben Sie die E-Mail-Adresse ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">BCC</td> 
   <td>Klicken Sie für jede E-Mail-Adresse, an die Sie die BCC-E-Mail senden möchten<b> auf „Element hinzufügen</b> und geben Sie die E-Mail-Adresse ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Betreff</td> 
   <td>Text des E-Mail-Betreffs eingeben oder zuordnen</td> 
  </tr> 
  <tr> 
   <td role="rowheader">HTML</td> 
   <td>Um eine HTML-formatierte E-Mail zu senden, geben Sie den Textkörper der E-Mail ein, einschließlich HTML-Tags.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Text</td> 
   <td>Um eine reine Text-E-Mail zu senden, geben Sie den Text des E-Mail-Textkörpers ein oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Metadaten aufrufen

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL To Number]</p> </td> 
   <td> <p>Geben Sie die Telefonnummer ein, unter der der Anruf erfolgen soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From Number]</td> 
   <td>Geben Sie die Telefonnummer ein, von der aus der Anruf getätigt werden soll, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
  <td>Wählen Sie den Status des Anrufs aus.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Text</td> 
   <td>Geben Sie die Details oder Notizen für den Anruf ein oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Externe ID</td> 
   <td>Dieses Feld stellt die interne ID eines Aufrufs in HubSpot dar. Es erfordert keine Maßnahmen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dauer</td> 
   <td>Länge des Aufrufs in Millisekunden eingeben oder zuordnen</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Externe Konto-ID</td> 
   <td>Dieses Feld stellt die interne Konto-ID eines Aufrufs in HubSpot dar. Es erfordert keine Maßnahmen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aufnahme-URL</td> 
   <td>Geben Sie die URL der Aufzeichnungsdatei ein oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### Meeting-Felder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Title]</p> </td> 
   <td> <p>Geben Sie den Titel oder den Betreff des Meetings ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Geben Sie den Text der Besprechungsbeschreibung oder der Details ein oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Time]</td> 
  <td>Geben Sie die Startzeit des Meetings als UNIX-Zeitstempel ein oder mappen Sie sie.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Endzeit</td> 
   <td>Geben Sie die Endzeit des Meetings als UNIX-Zeitstempel ein oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Aufgabenfelder

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Subject]</p> </td> 
   <td> <p>Geben Sie den Titel oder den Betreff der Aufgabe ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Geben Sie den Text der Aufgabenbeschreibung oder der Aufgabendetails ein oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Status</td> 
   <td>Wählen Sie den Status der Aufgabe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL For Object Type]</td> 
  <td>Geben Sie entweder <code>CONTACT</code> oder <code>COMPANY</code> ein.
  </td> 
   </tr> 
 </tbody> 
</table>

+++

+++ **Interaktion löschen**

Dieses Aktionsmodul löscht eine Interaktion anhand ihrer ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Geben Sie die ID der Interaktion ein, die Sie löschen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Interaktionen ansehen**

Dieses Portmodul startet ein Trigger, wenn in einem Portal ein neues Projekt erstellt wird. Dieses Modul gibt nur die Datensätze zurück, die in den letzten 30 Tagen erstellt wurden, oder die 10.000 zuletzt erstellten Datensätze.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Die maximale Anzahl von Unternehmen, die [!DNL Workfront Fusion] während eines Szenario-Ausführungszyklus zurückgeben sollen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since]</td> 
   <td>Geben Sie das früheste Datum ein, für das Sie Ereignisse beobachten möchten, oder ordnen Sie es zu. Verwenden Sie den <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Ereignisse und Benachrichtigungen

<!--* [Create / Update a Timeline Event](#create--update-a-timeline-event)
* [List Timeline Event Types](#list-timeline-event-types)
* [Watch Calendar Events](#watch-calendar-events)
* [Watch Notifications](#watch-notifications)-->

+++ **Erstellen/Aktualisieren eines Zeitleistenereignisses**

Dieses Aktionsmodul erstellt oder aktualisiert ein Zeitleistenereignis. Dieses Modul kann nur mit einer Entwicklerverbindung verwendet werden, die Ihre Benutzerkennung, Ihren HubSpot-API-Schlüssel, Ihre Client-ID und Ihr Client-Geheimnis enthält.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Geben Sie die ID der Anwendung ein, zu der dieses Ereignis gehört, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td>Eine ID für dieses Ereignis eingeben oder zuordnen. Ereignis-IDs werden vom System nicht generiert.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Type ID]</td> 
   <td>Geben Sie die ID des Ereignistyps dieses Ereignisses ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Geben Sie die E-Mail-Adresse des Kontakts ein, für den Sie das Ereignis erstellen, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object ID]</td> 
   <td>Geben Sie die ID des Kontakts ein, für den Sie das Ereignis erstellen, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp]</td> 
   <td>Zeitstempel für dieses Ereignis eingeben oder zuordnen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom data]</td> 
   <td>Klicken Sie für jedes benutzerdefinierte Datenelement, das Sie diesem Ereignis hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Namen und den Wert des Elements ein.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Auflisten der Zeitleisten-Ereignistypen**

Dieses Suchmodul gibt eine Liste aller Zeitleistenereignisse für eine bestimmte Anwendung zurück. Dieses Modul kann nur mit einer Entwicklerverbindung verwendet werden, die Ihre Benutzerkennung, Ihren HubSpot-API-Schlüssel, Ihre Client-ID und Ihr Client-Geheimnis enthält.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Geben Sie die ID der Anwendung ein, zu der diese Ereignisse gehören, oder ordnen Sie sie zu. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Kalenderereignisse ansehen**

Dieses Kalendermodul startet ein Trigger, wenn einem Kalender ein neues Ereignis hinzugefügt wird. Es umfasst bis zu 500 Aufgaben im Intervall zwischen dem Start- und dem Enddatum. Dieses Modul kann nur mit einer Entwicklerverbindung verwendet werden, die Ihre Benutzerkennung, Ihren HubSpot-API-Schlüssel, Ihre Client-ID und Ihr Client-Geheimnis enthält.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Events Type]</td> 
   <td>Wählen Sie aus, ob Sie Social-Media-Ereignisse, Inhaltsereignisse oder alle Ereignisse ansehen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Dateien ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Geben Sie das Startdatum ein oder mappen Sie es.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Geben Sie das Enddatum ein oder mappen Sie es.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Benachrichtigungen ansehen**

Dieses Trigger-Modul startet ein Szenario, wenn eine neue Benachrichtigung über Änderungen gesendet wird.  Es umfasst bis zu 500 Aufgaben im Intervall zwischen dem Start- und dem Enddatum. Dieses Modul kann nur mit einer Entwicklerverbindung verwendet werden, die Ihre Benutzerkennung, Ihren HubSpot-API-Schlüssel, Ihre Client-ID und Ihr Client-Geheimnis enthält. Pro Entwickleranwendung kann in HubSpot nur eine Webhook-URL verwendet werden.

Um einen Webhook für dieses Modul zu erstellen, klicken Sie **Hinzufügen** neben dem Webhook-Feld und füllen Sie die folgenden Felder aus:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Geben Sie die Anwendungs-ID ein, die Sie für diesen Webhook verwenden möchten. Die ID finden Sie in Ihrem HubSpot-Entwicklerportal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscriptions]</td> 
   <td> <p>Klicken Sie für jeden Benachrichtigungstyp, den Sie überwachen möchten, auf <b>Element hinzufügen</b> und wählen Sie den Abonnementtyp aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Force to Remove Old Subscriptions]</td> 
   <td>Aktivieren Sie diese Option, um alte, an diesen Webhook angehängte Abonnements zu trennen oder zu löschen.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Dateien

<!--* [[!UICONTROL Create a Folder]](#create-a-folder)
* [Delete a File](#delete-a-file)
* [[!UICONTROL Delete a Folder]](#delete-a-folder)
* [List Files](#list-files)
* [[!UICONTROL Move a File]](#move-a-file)
* [Upload a file](#upload-a-file)
* [Watch files](#watch-files)-->

+++ **[!UICONTROL Create a Folder]**

Dieses Modul erstellt einen Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder Name] </td> 
   <td>Geben Sie einen Namen für den neuen Ordner ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID] </td> 
   <td>Wählen Sie die ID des übergeordneten Ordners für den Ordner aus, den Sie erstellen. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Datei löschen**

Dieses Aktionsmodul löscht dauerhaft eine Datei und alle zugehörigen Daten und Miniaturen aus dem Datei-Manager.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Geben Sie die ID der Datei ein, die Sie löschen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Delete a Folder]**

Markiert einen Ordner als gelöscht.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Ordners ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Dateien auflisten**

Dieses Suchmodul gibt eine Liste der im Datei-Manager gespeicherten Dateien zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Dateien ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Geben Sie die ID des Ordners ein, der die Dateien enthält, die Sie auflisten möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Um nur Dateien einzubeziehen, die bestimmte Zeichen im Dateinamen enthalten, geben Sie die Zeichen ein, die im Dateinamen enthalten sein sollen, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Move a File]**

Verschiebt eine Datei in einen anderen Ordner.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID] </td> 
   <td>Geben Sie die ID der Datei ein, die Sie verschieben möchten, oder mappen Sie sie. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>Wählen Sie die ID des Ordners aus, in den Sie die Datei verschieben möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Geben Sie einen Namen für die verschobene Datei ein.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Datei hochladen**

Dieses Aktionsmodul lädt eine Datei in den Datei-Manager hoch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Access type] </td> 
   <td>Wählen Sie aus, ob die Datei privat, öffentlich, aber nicht indizierbar oder öffentlich und indizierbar sein soll. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>Wählen Sie die ID des Ordners aus, in den Sie die Datei hochladen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Aktivieren Sie diese Option, um die Datei zu überschreiben, wenn sie bereits im Ordner existiert.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Dateien ansehen**

Dieses Dateimodul startet ein Trigger, wenn eine neue Datei im Dateimanager gespeichert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Dateien ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Geben Sie die ID des Ordners ein, der die Dateien enthält, die Sie beobachten möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Um nur Dateien einzubeziehen, die bestimmte Zeichen im Dateinamen enthalten, geben Sie die Zeichen ein, die im Dateinamen enthalten sein sollen, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Aufgaben

<!--* [Create a Calendar Task](#create-a-calendar-task)
* [Delete a Calendar Task](#create-a-calendar-task)
* [Watch Task Events](#watch-task-events)-->

+++ **Kalenderaufgabe erstellen**

Dieses Aktionsmodul erstellt eine neue Aufgabe für einen Kalender. Die in diesem Modul verwendete Verbindung muss die Anmeldeinformationen eines Benutzers mit einem Paid-Marketing-Konto verwenden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Geben Sie einen Namen für die neue Kalenderaufgabe ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Geben Sie eine Beschreibung für die neue Kalenderaufgabe ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td>Geben Sie die Eigentümer-ID des Benutzers ein, der dieser Aufgabe zugewiesen ist, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Date]</td> 
   <td>Datum für diese Aufgabe eingeben oder zuordnen.<p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>Wählen Sie den Ereignistyp.<ul><li><b>Blogpost</b><p>Geben Sie die Inhaltsgruppen-ID ein. Dies ist die ID der Blog-Seite.</p></li><li><b>E-Mail</b><p>Geben Sie den Pfad zur E-Mail-Vorlage ein, die Sie verwenden möchten, oder ordnen Sie ihn zu.</li><li><b>Landingpage</b><p>Geben Sie den Pfad zur gewünschten Landingpage-Vorlage ein oder ordnen Sie ihn ihr zu.</li><li><b>Benutzerdefiniert</b></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Geben Sie ein, ob das Ereignis den Status „Aufgabe“ oder „Fertig“ hat.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign GUID]</td> 
   <td>Geben Sie die interne HubSpot-ID der Kampagne ein, zu der dieses Ereignis gehört, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Kalenderaufgabe löschen**

Dieses Aktionsmodul löscht eine Kalenderaufgabe. Die in diesem Modul verwendete Verbindung muss die Anmeldeinformationen eines Benutzers mit einem Paid-Marketing-Konto verwenden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID der Aufgabe ein, die Sie löschen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Aufgabenereignisse ansehen**

Dieses Kalendermodul startet ein Trigger, wenn ein neues Aufgabenereignis in einem Kalender vorhanden ist. Die in diesem Modul verwendete Verbindung muss die Anmeldeinformationen eines Benutzers mit einem Paid-Marketing-Konto verwenden. Das -Modul gibt bis zu 500 Ereignisse zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Dateien ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Geben Sie das früheste Datum ein, für das Sie Ereignisse beobachten möchten, oder ordnen Sie es zu. Verwenden Sie den <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Geben Sie das letzte Datum ein, für das Sie Ereignisse ansehen möchten, oder mappen Sie es. Verwenden Sie den <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Benutzende

<!--* [Get an Owner](#get-an-owner)
* [List Owners](#list-owners)-->

+++ **Erhalten Sie einen Besitzer**

Dieses Aktionsmodul gibt Details zu einem Eigentümer zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td> <p>Geben Sie die ID des Besitzers ein, für den Sie Details zurückgeben möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Besitzer auflisten**

Dieses Suchmodul gibt eine Liste aller Eigentümer in einem HubSpot-Konto zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Tickets

<!--* [Create a Ticket]-->
<!--* [Delete a Ticket](#delete-a-ticket)-->
<!--* [Create a Ticket]-->
<!--* [Create a Ticket]-->
<!--* [Create a Ticket]-->
<!--* [Create a Ticket]-->

<!-- Create a Ticket Need to find a working connection-->

+++ **[!UICONTROL Delete a Ticket]**

Löscht ein vorhandenes Ticket anhand seiner ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Tickets ein, das Sie löschen möchten. </td> 
  </tr> 
 </tbody> 
</table>

+++

<!-- Get a Ticket  Need to find a working connection-->

<!-- List Tickets  Need to find a working connection-->

&lt;!— Aktualisieren eines Tickets Notwendigkeit, eine funktionierende Verbindung zu finden—>

<!-- Watch Tickets Need to find a working connection-->

### Formulare

<!--* [Get a File Uploaded via Form](#get-a-file-uploaded-via-form)
* [List Forms](#list-forms)-->
<!--* [Submit Data to a Form]-->
<!--* [Watch Submissions for a Form]-->

+++ **Datei per Formular hochladen**

Dieses Aktionsmodul gibt eine Datei zurück, die über ein Formular hochgeladen wurde.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td>Geben Sie die URL der Datei ein, die Sie abrufen möchten, oder mappen Sie sie. Dies finden Sie in den Formularmetadaten.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Forms auflisten**

Dieses Aktionsmodul gibt alle Formulare zurück, die in dem Konto erstellt wurden, das mit der für dieses Modul verwendeten Verbindung verknüpft ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Formularen ein, die das Modul in einem Ausführungszyklus zurückgibt, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--#### Submit Data to a Form Need to find a working connection-->



&lt;!—#### Übermittlungen für ein Formular beobachten - Es muss eine funktionierende Verbindung gefunden werden>—>

### Social Media (Broadcast)

<!--* [Cancel a Broadcast Message](#cancel-a-broadcast-message)
* [Create a Broadcast Message](#create-a-broadcast-message)
* [Watch Broadcast Messages](#watch-broadcast-messages)-->

+++ **Abbrechen einer Broadcast-Nachricht**

Dieses Aktionsmodul bricht eine geplante Übertragung ab, z. B. einen Tweet oder einen Facebook-Beitrag.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>Geben Sie die ID der Sendung ein, die Sie abbrechen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Erstellen einer Broadcast-Nachricht**

Dieses Aktionsmodul erstellt eine Nachricht und veröffentlicht sie sofort in dem angegebenen Social-Media-Kanal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel ID]</td> 
   <td>Geben Sie die Kennung des Kanals ein, den Sie für diese Übertragung verwenden möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Titel für diese Sendung eingeben oder zuordnen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Geben Sie den Text der Sendung ein oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Photo URL]</td> 
   <td>Geben Sie die URL eines Fotos ein, das Sie in die Sendung einbeziehen möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thumbnail URL]</td> 
   <td>Geben Sie die URL einer Miniaturansicht ein, die Sie für diese Übertragung verwenden möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trigger at]</td> 
   <td>Geben Sie das Datum und die Uhrzeit ein, zu der die Sendung gesendet werden soll, oder mappen Sie sie. Wenn dies leer gelassen wird, wird die Übertragung sofort gesendet.<p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Broadcast-Nachrichten ansehen**

Dieses Trigger-Modul startet ein Szenario, wenn eine Nachricht von HubSpot an den angegebenen Social-Media-Kanal gesendet wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl an Elementen ein, die das Modul in einem Ausführungszyklus zurückgibt, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Status]</td> 
   <td>Um das Szenario nur dann zu starten, wenn die Nachricht einen bestimmten Status aufweist, wählen Sie den Status aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Channel]</td> 
   <td>Um das Szenario nur dann zu starten, wenn sich die Nachricht auf einem bestimmten Kanal befindet, wählen Sie den Kanal aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>Um das Szenario nur dann zu starten, wenn die Nachricht an oder nach einem bestimmten Datum liegt, geben Sie das Datum im <code>MM/DD/YYYY</code> Format ein oder ordnen Sie es zu.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Blog-Beiträge

<!--* [Create a Blog Post]-->
<!--* [Delete a Blog Post](#delete-a-blog-post)-->
<!--* [List Blog Posts]-->
&lt;!—* [Blogpost veröffentlichen/Veröffentlichung aufheben](#publish--unpublish-a-blog-post)—>
<!--* [Watch Blog Posts]-->

<!--
#### Create a Blog Post May need connection
-->


+++ **Blogpost löschen**

Dieses Aktionsmodul löscht einen einzelnen Blogpost.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Blogposts ein, den Sie löschen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--#### List Blog Posts May need connection

This search module retrieves posts from a HubSpot blog.-->

+++ **Veröffentlichen/Rückgängigmachen der Veröffentlichung eines Blogposts**

Dieses Aktionsmodul plant oder bricht die Veröffentlichung eines Blogposts ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Blogposts ein, den Sie planen oder abbrechen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Wählen Sie aus, ob Sie den Blogpost planen oder einen zuvor geplanten Blogpost abbrechen möchten.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--#### Watch Blog PostsMay need connection-->

<!--+++**Workflows**>

<!--### Workflows May need connection

#### Add a Contact to a Workflow


#### Remove a Contact from a Workflow

-->

<!--+++-->

### Abonnements

<!--* [Update Email Subscription](#update-email-subscription)
* [Watch Subscriptions Timeline for a Portal](#watch-subscriptions-timeline-for-a-portal)-->

+++ **E-Mail-Abonnement aktualisieren**

Dieses Aktionsmodul aktualisiert ein E-Mail-Abonnement in HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Geben Sie die E-Mail-Adresse des Abonnements ein, das Sie aktualisieren möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Statuses]</td> 
   <td>Klicken Sie für jeden Status, für den Sie das Abonnement aktualisieren möchten, auf <b>Element hinzufügen</b> und geben Sie die Status-ID sowie an, ob die E-Mail-Adresse für diesen Status abonniert werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Status]</td> 
   <td>Um die Rechtsgrundlage für dieses Abonnement aufgrund der DSGVO zu erfassen, wählen Sie den Rechtsstatus dieses Abonnements aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Basis Explanation]</td> 
   <td>Um einen Hinweis zur Rechtsgrundlage für dieses Abonnement für die DSGVO hinzuzufügen, geben Sie den Text des Vermerks ein oder mappen Sie ihn.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Zeitleiste für Abonnements für ein Portal ansehen**

Dieses Portmodul startet ein Trigger-Szenario, wenn dem Portal ein neues E-Mail-Zeitleistenabonnement hinzugefügt wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl an Elementen ein, die das Modul in einem Ausführungszyklus zurückgibt, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Timestamp]</td> 
   <td>Um Ergebnisse ab einem bestimmten Datum oder danach zurückzugeben, geben Sie das Datum im folgenden Format ein <code>MM/DD/YYYY.</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Timestamp]</td> 
   <td>Um Ergebnisse von einem oder vor einem bestimmten Datum zurückzugeben, geben Sie das Datum im folgenden Format ein <code>MM/DD/YYYY.</code></td> 
  </tr> 
 </tbody> 
</table>

+++

<!--+++**Associations**-->

<!--### Associations-->

<!--#### Associate CRM Objects  May need connection

This action module associates two CRM objects.-->

<!--#### Associate Multiple CRM Objects  May need connection-->



<!--#### Delete an Association May need connection-->



<!--#### Delete Multiple Associations between CRM Objects May need connection-->



<!--#### List Associations for a CRM Object May need connection-->

<!--+++-->

### Sonstige

+++ **[!UICONTROL Make an API Call]**

Ermöglicht die Durchführung eines benutzerdefinierten API-Aufrufs.

>[!NOTE]
>
>Die folgenden Endpunkte wurden in der HubSpot-API am 31. August 2023 eingestellt und können nicht mehr in Fusion-Modulen verwendet werden.
>
>* Auflisten von Inhaltsereignissen
>* Auflisten von Social Media-Ereignissen
>* Auflisten von Kalenderaufgaben-Ereignissen
>* Alle Kalenderereignisse auflisten
>* Kalenderaufgabe erstellen
>* Kalenderaufgabe nach ID abrufen
>* Kalenderaufgabe aktualisieren
>* Kalenderaufgabe löschen

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL HubSpot CRM]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion] - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu https://api.hubapi.com/ ein. Beispiel: /contact/v1/lists/all/contact/all</p> <p>Eine Liste der verfügbaren Endpunkte finden Sie in der <a href="https://legacydocs.hubspot.com/docs/overview">[!DNL HubSpot] API-Dokumentation</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Methode aus, die Sie verwenden möchten:</p> <p>[!UICONTROL GET]</p> <p>um Informationen für einen Eintrag abzurufen.</p> <p>[!UICONTROL POST]</p> <p>um einen neuen Eintrag zu erstellen.</p> <p>[!UICONTROL PUT]</p> <p>um einen vorhandenen Eintrag zu aktualisieren/ersetzen.</p> <p>[!UICONTROL PATCH]</p> <p>um eine partielle Eingabeaktualisierung vorzunehmen.</p> <p>[!UICONTROL DELETE]</p> <p>um einen Eintrag zu löschen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p> Geben Sie die gewünschten Anfrage-Header ein. Sie müssen keine Autorisierungskopfzeilen hinzufügen. Das haben wir bereits für Sie getan.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Geben Sie die Abfragezeichenfolge der Anfrage ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Fügen Sie den Hauptteil des API-Aufrufs in Form eines standardmäßigen JSON-Objekts hinzu. Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Beispiel:** Der folgende API-Aufruf gibt alle Kontakte in Ihrem [!DNL HubSpot]-Konto zurück:
>
>**URL**: `/contacts/v1/lists/all/contacts/all`
>
>**Methode**: `GET`
>
>![Hubspot-API-Konfiguration](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-config.png)
>
>Treffer der Suche finden Sie in der Modulausgabe unter [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL contacts].
>
>In unserem Beispiel wurden drei Kontakte zurückgegeben:
>
>![Hubspot-API-Ausgabe](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-output.png)

+++

## Neue Anwendung erstellen

1. Melden Sie sich bei Ihrem [!DNL HubSpot]-Entwicklerkonto an.
1. Wählen Sie die Option **[!UICONTROL Create an App]** aus.
1. Geben Sie den App-Namen ein und [!UICONTROL Save] Sie das Dialogfeld.
1. Wählen Sie die Bereiche aus, die Sie für Ihren Webhook benötigen.

   Fügen Sie beispielsweise Kontaktbereiche zum Auslösen des Moduls hinzu, wenn ein neuer Kontakt erstellt oder gelöscht wird.

   Der [!UICONTROL contacts scope] ist alles, was Sie benötigen, um Kontakte, Angebote und Webhooks für Firmenveranstaltungen zu erhalten.

   >[!IMPORTANT]
   >
   >Füllen Sie das Feld [!UICONTROL Redirect URL] nicht aus.
