---
title: Google Docs-Module
description: Mit den Adobe Workfront Fusion [!DNL Google Docs] Modulen können Sie Dokumente in Ihren und/oder  [!DNL Google Docs]  [!DNL Google Docs]  (für  [!DNL Google Workspace] ) überwachen, erstellen bearbeiten und abrufen.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: cd44250d-c2cd-46b2-8773-15b30472a8d8
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '4087'
ht-degree: 0%

---

# [!DNL Google Docs]

Mit den Adobe Workfront Fusion [!DNL Google Docs]-Modulen können Sie Dokumente in Ihren [!DNL Google Docs] und [!DNL Google Docs] (für [!DNL Google Workspace]) überwachen, erstellen, bearbeiten und abrufen.

Um [!DNL Google Docs] mit Adobe Workfront Fusion verwenden zu können, benötigen Sie ein [!DNL Google]. Wenn Sie noch kein [!DNL Google] Konto haben, können Sie eines auf der Hilfeseite zum [!DNL Google] Konto erstellen.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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

Um [!DNL Google Docs] Module verwenden zu können, müssen Sie über ein Google-Konto verfügen.

## Google Docs-API-Informationen

Der Google Docs-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://docs.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.4.13</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Docs] Module und ihre Felder

Beim Konfigurieren von [!DNL Google Docs]-Modulen zeigt [!UICONTROL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Google Docs] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Dokument

* [[!UICONTROL Dokument erstellen]](#create-a-document)
* [[!UICONTROL Erstellen eines Dokuments aus einer Vorlage]](#create-a-document-from-a-template)
* [[!UICONTROL Dokument löschen]](#delete-a-document)
* [[!UICONTROL Dokument herunterladen]](#download-a-document)
* [[!UICONTROL Abrufen des Inhalts eines Dokuments]](#get-content-of-a-document)
* [[!UICONTROL Einfügen eines Absatzes in ein Dokument]](#insert-a-paragraph-to-a-document)
* [[!UICONTROL Einfügen eines Bildes in ein Dokument]](#insert-an-image-to-a-document)
* [[!UICONTROL Dokumente auflisten]](#list-documents)
* [[!UICONTROL Ersetzen von Text in einem Dokument]](#replace-text-in-a-document)
* [[!UICONTROL Ersetzen eines Bildes durch ein neues Bild]](#replace-an-image-with-a-new-image)
* [[!UICONTROL Dokumente ansehen]](#watch-documents)

#### [!UICONTROL Dokument erstellen]

Mit diesem Aktionsmodul können Sie ein neues Dokument im ausgewählten Ordner erstellen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie einen Namen für das Dokument ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Inhalt]</td> 
   <td> <p>Geben Sie den Inhalt des Dokuments ein. Sie können HTML zum Formatieren des Dokuments einbeziehen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, auf dem Sie ein Dokument erstellen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie im Feld Speicherort des neuen Dokuments den Ordner aus, in dem Sie ein Dokument erstellen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie im Feld Speicherort des neuen Dokuments den Ordner aus, in dem Sie ein Dokument erstellen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, auf dem Sie ein Dokument erstellen möchten.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kopfzeile einfügen]</td> 
   <td> <p> Aktivieren Sie diese Option, um die Kopfzeile in das Dokument einzufügen und den Text der Kopfzeile einzugeben oder zuzuordnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fußzeile einfügen] </td> 
   <td> <p>Aktivieren Sie diese Option, um die Fußzeile in das Dokument einzufügen und dann den Text der Kopfzeile einzugeben oder zuzuordnen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen eines Dokuments aus einer Vorlage]

Dieses Aktionsmodul erstellt eine Kopie eines vorhandenen Vorlagendokuments und ersetzt alle Tags. Dieses Modul ermöglicht es den Benutzern auch, Bilder durch neue Bilder anhand der URL zu ersetzen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Dokument aus Vorlage erstellen]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Wählen Sie diese Option, um die Dokumentvorlage zuzuordnen.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br>Wählen Sie diese Option, um die Dokumentvorlage aus dem Dropdown-Menü auszuwählen.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, auf dem sich Ihre Vorlage befindet. Diese Option ist verfügbar, wenn Sie im vorherigen Feld [!UICONTROL By Dropdown] ausgewählt haben.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p>  </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, auf dem sich Ihre Vorlage befindet.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokument-ID]</td> 
   <td> <p>Ordnen Sie die ID der Vorlage zu, wenn Sie Durch Zuordnung ausgewählt haben, oder wählen Sie den Pfad zur Vorlage und zur Vorlage aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Werte]</p> </td> 
   <td> <p>Klicken Sie für jedes Tag, für das Sie einen Wert eingeben möchten, auf <b>Element hinzufügen</b>, geben Sie das Tag ein und geben Sie den Wert ein, der anstelle des Tags in das neue Dokument eingegeben werden soll.</p> 
    <ul> 
     <li><strong>[!UICONTROL Tags]</strong><br>Geben Sie die Tags ein, die in der Dokumentvorlage enthalten sind. Verwenden Sie <code>&#123;&#123;&#125;&#125;</code> nicht. Beispiel: Verwenden Sie <code>name</code> anstelle von <code>&#123;&#123;name&#125;&#125;</code>.</li> 
     <li><strong>[!UICONTROL Replace Value]</strong><br>Geben Sie den Wert des Tags ein.</li> 
    </ul> <p>Beispielsweise wird die Variable <code> &#123;&#123;name&#125;&#125;</code> Quelldokument hier als Namensfeld angezeigt, in das der Wert eingefügt werden kann, z. B. <code>John</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Images Replacement]</p> </td> 
   <td> <p>&gt;Klicken Sie für jedes Tag, für das Sie einen Wert eingeben möchten, auf <b>Element hinzufügen</b> und geben Sie dann den Link zur [!UICONTROL Bildobjekt-ID] und [!UICONTROL Bild-URL] ein, die das aktuelle Bild ersetzen werden.</p> <p>Hinweis: Sie können die Bild-IDs mit dem Modul [!UICONTROL Dokument abrufen] abrufen, wobei die IDs im Array [!UICONTROL Inline Object Array] enthalten sind.</p> <p>Es wird empfohlen, Bildern in Ihrem [!DNL Google]-Dokument ALT-Text hinzuzufügen. </p> <p>So fügen Sie dem [!DNL Google Docs] einen ALT-Text hinzu:</p> 
    <ol> 
     <li value="1">Rechtsklick auf das Bild.</li> 
     <li value="2">Wählen Sie die Option [!UICONTROL ALT text].</li> 
     <li value="3">Geben Sie den [!UICONTROL ALT-Text] in das Feld [!UICONTROL Title] ein und klicken Sie auf [!UICONTROL OK].</li> 
    </ol> <p>Nachdem der ALT-Text zum Bild hinzugefügt wurde, wird der ALT-Text im Feldnamen in Klammern angezeigt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Titel] </td> 
   <td> <p>Geben Sie den Namen für das neue Dokument ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, auf dem sich Ihre Vorlage befindet. Diese Option ist verfügbar, wenn Sie im vorherigen Feld [!UICONTROL By Dropdown] ausgewählt haben.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie den Ordner aus, in dem das Dokument erstellt werden soll.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie den Ordner aus, in dem das Dokument erstellt werden soll.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, auf dem das Dokument erstellt werden soll.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dokument löschen]

Dieses Aktionsmodul löscht ein Dokument.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, auf dem sich das zu löschende Dokument befindet.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das zu löschende Dokument befindet, und wählen Sie dann das Dokument aus.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das zu löschende Dokument befindet, und wählen Sie dann das Dokument aus.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, auf dem sich das zu löschende Dokument befindet, und wählen Sie dann das Dokument aus.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared Drive]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das das Dokument enthält, das Sie herunterladen möchten, und wählen Sie dann ein Dokument aus. Diese Option ist verfügbar, wenn Sie [!DNL My Drive] im Feld [!UICONTROL Laufwerk auswählen] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokument-ID]</td> 
   <td> <p> Wählen Sie das Dokument aus, das Sie löschen möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dokument herunterladen]

Dieses Aktionsmodul konvertiert das ausgewählte Dokument und lädt es herunter.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, auf dem sich das Dokument befindet, das Sie herunterladen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie im Feld Dokument-ID den Ordner aus, in dem sich das Dokument befindet, das Sie herunterladen möchten, und wählen Sie dann das Dokument aus.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie im Feld Dokument-ID den Ordner aus, in dem sich das Dokument befindet, das Sie herunterladen möchten, und wählen Sie dann das Dokument aus.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, auf das sich das Dokument befindet, das Sie herunterladen möchten, und wählen Sie dann das Dokument aus.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Typ] </p> </td> 
   <td> <p>Zieldateiformat des heruntergeladenen Dokuments auswählen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Abrufen des Inhalts eines Dokuments]

Dieses Aktionsmodul ruft ein angegebenes Dokument ab.

Möglicherweise müssen Sie Ihre Berechtigungen erweitern.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inhalt eines Dokuments abrufen]</td> 
   <td> <p>Wählen Sie aus, ob Sie die Dokument-ID des Dokuments zuordnen möchten, oder wählen Sie das Dokument aus dem Dropdown-Menü manuell aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, der das Dokument enthält, das Sie abrufen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie den Ordner aus, der das Dokument enthält, das Sie abrufen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie den Ordner aus, der das Dokument enthält, das Sie abrufen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, das das Dokument enthält, das Sie abrufen möchten.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokument-ID]</td> 
   <td> <p>Geben Sie das Dokument ein, das Sie abrufen möchten, oder wählen Sie es aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL filter]</p> </td> 
   <td> <p>Wählen Sie das -Objekt aus, das in der Ausgabe des Moduls zurückgegeben werden soll.</p> 
    <ul> 
     <li>[!UICONTROL Image] (Standard)</li> 
     <li>[!UICONTROL Zeichnung]</li> 
     <li>[!UICONTROL -Diagramm]</li> 
    </ul> <p>Hinweis:  <p>Für weitere Zuordnungen dieser Objekte verwenden Sie bitte den Wert [!UICONTROL Inline Objects Array] in der Ausgabe dieses Moduls (anstelle von [!UICONTROL inlineObjects]).</p> <p>Die [!UICONTROL Inline Objects Array]-Objekte werden in der gleichen Reihenfolge sortiert, in der sie im Dokument erscheinen. Dies erleichtert die weitere Verarbeitung.</p> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Einfügen eines Absatzes in ein Dokument]

Dieses Aktionsmodul fügt einen neuen Absatz an ein vorhandenes Dokument an oder fügt ihn ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Dokument auswählen]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Wählen Sie diese Option, um das Dokument zuzuordnen.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> Wählen <br> diese Option, um das Dokument aus dem Dropdown-Menü auszuwählen.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, auf dem sich das Dokument befindet, dem Sie einen Absatz hinzufügen möchten. Diese Option ist verfügbar, wenn Sie im vorherigen Feld [!UICONTROL By Dropdown] ausgewählt haben.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das Dokument befindet, dem Sie einen Absatz hinzufügen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das Dokument befindet, dem Sie einen Absatz hinzufügen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, auf dem sich das Dokument befindet, dem Sie einen Absatz hinzufügen möchten, und wählen Sie dann das Dokument aus.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokument-ID]</td> 
   <td> <p>Ordnen Sie das Dokument zu, in das Sie Text einfügen möchten, oder wählen Sie es aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Absatz einfügen]</p> </td> 
   <td> <p>Wählen Sie aus, wie der neue Text in das Dokument eingefügt werden soll.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nach Angabe des Ortes]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL nach Index]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL Index]</strong> </p> <p>Geben Sie die Indexnummer ein, unter der Sie Ihren Text einfügen möchten. Sie können das Modul [!UICONTROL Dokument abrufen] verwenden, um die Indexnummer abzurufen.</p> </li> 
         <li> <p><strong>[!UICONTROL eingefügter Text]</strong> </p> <p>Geben Sie den Text ein, den Sie in das Dokument einfügen möchten.</p> </li> 
        </ul> </li> 
       <li> <p><strong>[!UICONTROL nach Segment-ID]</strong> </p> <p>Wählen Sie die Kopf- und Fußzeile aus, in die Sie den Textinhalt einfügen möchten, und geben Sie den einzufügenden Text in die entsprechenden Felder ein.</p> <p>Wenn die Kopf- oder Fußzeile bereits Text enthält, wird der neue Text vor dem vorhandenen Text hinzugefügt.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Durch Anhängen von an den Hauptteil des Dokuments]</strong> </p> <p>Hängt den eingegebenen Text am Ende des Textinhalts des Dokuments an.</p> <p>Der Stil des neuen Absatzes wird am aktuellen Einfügeindex aus dem Absatz kopiert, einschließlich Listen und Aufzählungszeichen.</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Durch Anhängen von an das Ende des Segments (Kopf- und Fußzeile)]</strong> </p> <p>Wählen Sie die Kopf- und Fußzeile aus, in die Sie den Textinhalt einfügen möchten, und geben Sie den einzufügenden Text in die entsprechenden Felder ein.</p> <p>Wenn die Kopf- oder Fußzeile bereits Text enthält, wird der neue Text nach dem vorhandenen Text hinzugefügt.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL angehängter Text]</td> 
   <td>Text eingeben oder zuordnen, der an das Dokument angehängt werden soll</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Einfügen eines Bildes in ein Dokument]

Dieses Aktionsmodul fügt ein Bild aus der URL in das Dokument ein.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Dokument auswählen]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Wählen Sie diese Option, um die Dokumentvorlage zuzuordnen.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> Wählen <br> diese Option, um das Dokument aus dem Dropdown-Menü auszuwählen.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, auf dem sich das Dokument befindet, dem Sie ein Bild hinzufügen möchten. Diese Option ist verfügbar, wenn Sie im vorherigen Feld [!UICONTROL By Dropdown] ausgewählt haben.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das Dokument befindet, dem Sie ein Bild hinzufügen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das Dokument befindet, dem Sie ein Bild hinzufügen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, auf dem sich das Dokument befindet, dem Sie ein Bild hinzufügen möchten, und wählen Sie dann das Dokument aus.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokument-ID]</td> 
   <td> <p>Ordnen Sie das Dokument zu, in das Sie ein Bild einfügen möchten, oder wählen Sie es aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bild einfügen]</p> </td> 
   <td> <p>Auswählen, wie das neue Bild in das Dokument eingefügt werden soll.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nach Angabe des Ortes]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL nach Index]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL Index]</strong> </p> <p>Geben Sie die Indexnummer ein, unter der Sie Ihr Bild einfügen möchten. Sie können das Modul [!UICONTROL Dokument abrufen] verwenden, um [!UICONTROL Indexnummer] abzurufen.</p>  </li> 
         <li> <p><strong>[!UICONTROL Bild URL]</strong> </p> <p>Geben Sie die URL des Bildes ein, das Sie in das Dokument einfügen möchten.</p> <p>Die maximale Bildgröße beträgt 50 MB. Darf 25 Megapixel nicht überschreiten. Es wird nur das PNG-, JPEG- oder GIF-Format unterstützt.</p> </li> 
        </ul> </li> 
       <li> <p><strong>[!UICONTROL nach Segment-ID]</strong> </p> <p>Wählen Sie die Kopf- und Fußzeile aus, in die Sie das Bild einfügen möchten, und geben Sie die Bild-URL in die entsprechenden Felder ein.</p> <p>Die maximale Bildgröße beträgt 50 MB. Das Bild darf 25 Megapixel nicht überschreiten. Es wird nur das PNG-, JPEG- oder GIF-Format unterstützt.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Durch Anhängen von an den Hauptteil des Dokuments]</strong> </p> <p>Hängt ein bestimmtes Bild an das Ende des Textinhalts des Dokuments an.</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Durch Anhängen von an das Ende des Segments (Kopf- und Fußzeile)]</strong> </p> <p>Wählen Sie die Kopf- und Fußzeile aus, in die Sie ein Bild einfügen möchten, und geben Sie die Bild-URL ein, die Sie in die entsprechenden Felder einfügen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Höhe Betrag in Punkt/Breite Betrag in Punkt]</p> </td> 
   <td> <p>Definieren Sie die Höhe oder Breite des eingefügten Bildes. Das Seitenverhältnis wird beibehalten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Dokumente auflisten]

Dieses Aktionsmodul ruft eine Liste der Dokumente aus dem ausgewählten Ordner ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, von dem Dokumente aufgelistet werden sollen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie den Ordner aus, aus dem Dokumente aufgelistet werden sollen.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie den Ordner aus, aus dem Dokumente aufgelistet werden sollen.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, dessen Dokumente Sie auflisten möchten.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Dokumenten fest, die Workfront Fusion in einem Ausführungszyklus zurückgibt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ersetzen von Text in einem Dokument]

Dieses Aktionsmodul ersetzt Text in einem Dokument.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Dokument auswählen]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Wählen Sie diese Option, um die Dokumentvorlage zuzuordnen.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> Wählen <br> diese Option, um das Dokument aus dem Dropdown-Menü auszuwählen.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, auf dem sich das Dokument befindet, dem Sie Text hinzufügen möchten. Diese Option ist verfügbar, wenn Sie im vorherigen Feld [!UICONTROL By Dropdown] ausgewählt haben.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das Dokument befindet, dem Sie Text hinzufügen möchten, und wählen Sie dann das Dokument aus.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das Dokument befindet, dem Sie Text hinzufügen möchten, und wählen Sie dann das Dokument aus.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, auf dem sich das Dokument befindet, dem Sie Text hinzufügen möchten, und wählen Sie dann das Dokument aus.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokument-ID]</td> 
   <td> <p>Ordnen Sie das Dokument zu, in dem Sie Text ersetzen möchten, oder wählen Sie es aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text ersetzen]</p> </td> 
   <td> <p>Klicken Sie für jedes Textstück, das Sie ersetzen möchten, auf <b>Element hinzufügen</b> und geben Sie Folgendes ein:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Alter Text, der ersetzt werden soll]</strong> </p> <p>Geben Sie den Text ein, den Sie ersetzen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL Neuer einzufügender Text]</strong> </p> <p>Geben Sie den neuen Text ein.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL Ersetzen eines Bildes durch ein neues Bild]

Dieses Aktionsmodul ersetzt ein vorhandenes Bild. Das Seitenverhältnis des Originalbilds wird beibehalten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Dokument auswählen]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Wählen Sie diese Option, um die Dokumentvorlage zuzuordnen.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> Wählen <br> diese Option, um das Dokument aus dem Dropdown-Menü auszuwählen.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, auf dem sich das Dokument befindet, das Sie durch ein Bild ersetzen möchten. Diese Option ist verfügbar, wenn Sie im vorherigen Feld [!UICONTROL By Dropdown] ausgewählt haben.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das Dokument befindet, das Sie durch ein Bild ersetzen möchten, und wählen Sie dann das Dokument aus.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das Dokument befindet, das Sie durch ein Bild ersetzen möchten, und wählen Sie dann das Dokument aus.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, auf dem sich das Dokument befindet, das Sie durch ein Bild ersetzen möchten, und wählen Sie dann das Dokument aus.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokument-ID]</td> 
   <td> <p>Ordnen Sie das Dokument zu, in dem Sie ein Bild ersetzen möchten, oder wählen Sie es aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Images Replacement]</p> </td> 
   <td> Klicken Sie für jedes Bild, das Sie ersetzen möchten, auf <b>Element hinzufügen</b> und geben Sie die vorhandene Bild-ID ein. Geben Sie dann die URL des neuen Bildes ein, das das vorhandene Bild ersetzen soll, oder mappen Sie sie. <p>Bilder werden in der Reihenfolge aufgelistet, in der sie im Dokument angezeigt werden. Beispielsweise ist <code>Body: Image No. 1</code> das erste Bild im Dokument.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Dokumente ansehen]

Dieses Ordnermodul gibt Dokumentdetails zurück, wenn ein neues Trigger erstellt oder geändert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokumente ansehen]</td> 
   <td> <p style="color: #000000;">Wählen Sie aus, ob die Dokumente Erstellt ([!UICONTROL By Created Date]) oder Geändert ([!UICONTROL By Modified Date]) angezeigt werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, den Sie überwachen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie den Ordner aus, der auf erstellte oder geänderte Dokumente überwacht werden soll.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie den Ordner aus, der auf erstellte oder geänderte Dokumente überwacht werden soll.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, das Sie überwachen möchten.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Shared Drive] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Dokumenten fest, die Workfront Fusion in einem Ausführungszyklus zurückgibt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

* [[!UICONTROL Alle Links in einem Dokument können angeklickt werden]](#make-all-links-in-a-document-clickable)
* [[!UICONTROL Erstellen eines API-Aufrufs]](#make-an-api-call)

#### [!UICONTROL Alle Links in einem Dokument können angeklickt werden]

Dieses Aktionsmodul findet alle Links im Dokument und macht sie anklickbar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Alle Links in einem Dokument erstellen]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Wählen Sie diese Option, um die Dokumentvorlage zuzuordnen.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> Wählen <br> diese Option, um das Dokument aus dem Dropdown-Menü auszuwählen.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Laufwerk auswählen]</td> 
   <td> <p>Wählen Sie den Laufwerkstyp aus, auf dem sich das Dokument befindet, auf das Links geklickt werden sollen. Diese Option ist verfügbar, wenn Sie im vorherigen Feld [!UICONTROL By Dropdown] ausgewählt haben.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das Dokument befindet, auf das Links geklickt werden sollen.</p> </li> 
     <li> <p><strong>[!UICONTROL für mich freigegeben]</strong> </p> <p>Wählen Sie den Ordner aus, in dem sich das Dokument befindet, auf das Links geklickt werden sollen.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (nur für [!DNL Google Workspace] Benutzer verfügbar)</p> <p>Wählen Sie aus, ob Sie [!UICONTROL Domain-Administratorzugriff verwenden] möchten. Bei Auswahl von [!UICONTROL Yes] wird die Anfrage als Domain-Administrator ausgegeben, und alle freigegebenen Laufwerke, deren Administrator der Anforderer ist, werden zurückgegeben.</p> <p>Wählen Sie das freigegebene Laufwerk aus, auf dem sich das Dokument befindet, auf das Sie Links klicken möchten, und wählen Sie dann das Dokument aus.</p> <p>Hinweis: Wenn Sie die Option [!DNL Google Docs] in diesem Feld ausgewählt haben und kein [!DNL Google Workspace] Benutzer sind, wird der <code>[400] Invalid Value</code> zurückgegeben.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared Drive]</td> 
   <td> <p>Wählen Sie das Laufwerk aus, das das Dokument enthält, in dem Links aktualisiert werden sollen, und wählen Sie dann ein Dokument aus. Diese Option ist verfügbar, wenn Sie [!DNL My Drive] im Feld [!UICONTROL Laufwerk auswählen] ausgewählt haben.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dokument-ID]</td> 
   <td> <p> Wählen Sie das Dokument aus, in dem Sie die Links aktualisieren möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen eines API-Aufrufs]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>https://docs.googleapis.com/</code> ein. Beispiel: <code>/v1/documents/{presentationID}</code>. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Beispiel: <code>{"Content-type":"application/json"}</code>. Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p> Geben Sie die Abfragezeichenfolge der Anfrage ein.</p> </td> 
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

>[!BEGINSHADEBOX]

**Beispiel:** Der folgende API-Aufruf ruft die Details für das angegebene Dokument in Ihrer Google Docs ab:

**URL:**

/v1/documents/1ujkf-GDgB0TQSYPrxbCSK4Uso54tHVMqHZEVZZxB6aY

**Methode:**

[!UICONTROL GET]

![Beispiel für einen API-Aufruf](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

Details zum abgerufenen Dokument finden Sie in der Ausgabe des Moduls unter [!UICONTROL Bundle] > [!UICONTROL Body].

![API-Aufrufausgabe](/help/workfront-fusion/references/apps-and-modules/assets/api-output.png)

>[!ENDSHADEBOX]
