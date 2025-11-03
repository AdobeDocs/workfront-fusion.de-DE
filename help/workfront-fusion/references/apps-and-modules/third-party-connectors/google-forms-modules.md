---
title: Google Forms-Module
description: Mit  [!DNL Adobe Workfront Fusion Google Forms]  Modulen können Sie Antworten auf Ihre Google Forms überwachen, auswählen, hinzufügen, aktualisieren oder löschen.
author: Becky
feature: Workfront Fusion
exl-id: dc017957-c0f8-4206-916f-21ccda346fb9
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%

---

# [!DNL Google Forms]

Mit den Adobe Workfront Fusion [!DNL Google Forms]-Modulen können Sie Antworten auf Ihre [!DNL Google Forms] überwachen, auswählen, hinzufügen, aktualisieren oder löschen.

Um [!DNL Google Docs] mit Adobe Workfront Fusion verwenden zu können, benötigen Sie ein [!DNL Google]. Wenn Sie noch kein [!DNL Google] Konto haben, können Sie eines auf der Hilfeseite zum [!DNL Google] Konto erstellen.

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

Um [!DNL Google Forms]-Module verwenden zu können, müssen Sie über ein [!DNL Google]-Konto verfügen.

## Google Forms-API-Informationen

Der Google Forms-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>2,0,10</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Tabelle aus dem Formular

Um mit Ihren Formularantworten zu arbeiten, müssen Sie zunächst die Antwort-Tabelle erstellen.

1. Öffnen Sie das Formular.
1. Navigieren Sie zur Registerkarte **[!UICONTROL Antworten]** .
1. Klicken Sie auf das **[!UICONTROL Arbeitsblatt erstellen]**-Symbol ![Arbeitsblattsymbol](/help/workfront-fusion/references/apps-and-modules/assets/spreadsheet-icon.png).

1. Wählen Sie aus, ob Sie eine neue Tabelle oder eine vorhandene Tabelle erstellen möchten
1. Klicken Sie auf **[!UICONTROL Erstellen]**.

## [!DNL Google Forms] Module und ihre Felder

Beim Konfigurieren von [!DNL Google Forms] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Google Forms] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Trigger

#### [!UICONTROL Antworten ansehen]

Überwacht das Formular auf neue Antworten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Tabelle]</td> 
   <td> <p>Wählen Sie die Tabelle aus, die die Antworten aus dem Formular enthält, auf das Sie auf neue Antworten achten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Wählen Sie das Blatt aus, das die Formularantworten enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zeile mit Überschriften]</td> 
   <td>Geben Sie die Kopfzeile der Tabelle an. Die Standardzeile lautet <code>A1:Z1</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wert rendern option]</td> 
   <td> <p>Geben Sie an, wie die Werte in der Ausgabe gerendert werden sollen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL formatierter Wert]</strong> </p> <p>Die Werte werden in der Antwort entsprechend der Zellenformatierung berechnet und formatiert. Die Formatierung basiert auf dem Gebietsschema der Tabelle, nicht auf dem Gebietsschema des anfragenden Benutzers. Wenn <code>A1</code> beispielsweise <code>1. 23</code> und <code>A2 </code>als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>$1. 23</code> zurück.</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>Die Werte werden berechnet, aber in der Antwort nicht formatiert. Wenn <code>A1</code> beispielsweise <code>1. 23</code> und <code>A2 </code>als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> die Zahl <code>1. 23</code> zurück.</p> </li> 
     <li> <p><strong>[!UICONTROL -Formel]</strong> </p> <p>Werte werden nicht berechnet. Die Antwort enthält die Formeln. Wenn <code>A1</code> beispielsweise <code>1. 23</code> und <code>A2 </code>als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>=A1</code> zurück.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Render-Option Datum und Uhrzeit]</td> 
   <td>Wählen Sie aus, wie Datum, Uhrzeit und Dauer in der Ausgabe dargestellt werden sollen. Dieses Feld wird ignoriert, wenn [!UICONTROL Value Render Option] auf [!UICONTROL Formatted Value] gesetzt ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Antworten fest, mit denen Workfront Fusion während eines Zyklus arbeitet.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Antwort hinzufügen]](#add-a-response)
* [[!UICONTROL Antwort löschen]](#delete-a-response)
* [[!UICONTROL Aktualisieren einer Antwort]](#update-a-response)

#### [!UICONTROL Antwort hinzufügen]

Dieses Modul fügt eine neue Antwort an das untere Ende der Tabelle des Formulars an.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Tabelle]</td> 
   <td> <p>Wählen Sie das Arbeitsblatt aus, das das Arbeitsblatt enthält, dem Sie eine Antwort hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Wählen Sie das Blatt aus, das die Formularantworten enthält.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL -Werte]</p> </td> 
   <td> <p>Geben Sie die gewünschten Werte in die Tabellenspalten ein. Die Spalten sind je nach Blatt verfügbar.</p> <p>Verwenden Sie für die Spalte [!UICONTROL Timestamp] den folgenden Wert:</p><pre>formatDate(now;TT/MM/JJJJ hh:mm;UTC)</pre> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL -Werteingabeoption]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL RAW]</strong> </p> <p> Die vom Benutzer eingegebenen Werte werden nicht geparst und unverändert gespeichert. </p> </li> 
     <li> <p><strong>[!UICONTROL Benutzer entered]</strong></p> <p>Die Werte werden analysiert, als ob der Benutzer sie in die Benutzeroberfläche eingegeben hätte. Zahlen bleiben Zahlen, Zeichenfolgen können jedoch nach denselben Regeln, die bei der Eingabe von Text in eine Zelle über die [!DNL Google Sheets]-Benutzeroberfläche angewendet werden, in Zahlen, Daten oder andere Formate konvertiert werden.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Option zum Einfügen von Daten]</td> 
   <td> <p>Geben Sie an, wie vorhandene Daten bei der Eingabe neuer Daten geändert werden. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>Die neuen Daten überschreiben vorhandene Daten in den Bereichen, in denen sie geschrieben werden. Durch Hinzufügen von Daten am Ende des Arbeitsblatts werden neue Zeilen oder Spalten eingefügt, damit die Daten geschrieben werden können.</p> </li> 
     <li> <p><strong>[!UICONTROL Zeilen einfügen]</strong></p> <p>Für die neuen Daten werden Zeilen eingefügt.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Antwort löschen]

Dieses Modul löscht eine ausgewählte Antwort.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Tabelle]</td> 
   <td> <p>Wählen Sie das Arbeitsblatt aus, das das Arbeitsblatt enthält, in dem Sie eine Antwort löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Wählen Sie das Blatt aus, das die Formularantworten enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Zeilennummer]</p> </td> 
   <td> <p>Geben Sie die Nummer der Zeile ein, die Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren einer Antwort]

Dieses Modul aktualisiert die ausgewählte Antwort.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Tabelle]</td> 
   <td> <p>Wählen Sie die Tabelle aus, die das Blatt enthält, in dem Sie eine Antwort aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Wählen Sie das Blatt aus, das die Formularantworten enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Zeilennummer]</p> </td> 
   <td> <p>Geben Sie die Nummer der Zeile ein, die Sie aktualisieren möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Werte]</p> </td> 
   <td> <p>Geben Sie die neuen Werte für die gewünschten Spalten ein. Die Spalten sind je nach Blatt verfügbar.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL -Werteingabeoption]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL RAW]</strong> </p> <p> Die vom Benutzer eingegebenen Werte werden nicht geparst und unverändert gespeichert. </p> </li> 
     <li> <p><strong>[!UICONTROL Benutzer entered]</strong></p> <p>Die Werte werden analysiert, als ob der Benutzer sie in die Benutzeroberfläche eingegeben hätte. Zahlen bleiben Zahlen, Zeichenfolgen können jedoch nach denselben Regeln, die bei der Eingabe von Text in eine Zelle über die [!DNL Google Sheets]-Benutzeroberfläche angewendet werden, in Zahlen, Daten oder andere Formate konvertiert werden.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL Suchantworten]](#search-responses)
* [[!UICONTROL Suchantworten (Erweitert])](#search-responses-advanced)

#### [!UICONTROL Suchantworten]

Dieses Modul gibt Antworten zurück, die den angegebenen Kriterien entsprechen.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
    <td>Verbindung</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL -Tabelle]</td>
   <td> <p>Wählen Sie das Formular aus, in dem Sie suchen möchten.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Sheet] </td>
   <td> <p>Wählen Sie das Blatt aus, das die Formularantworten enthält.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Spaltenbereich]</td>
   <td> <p> Wählen Sie den Spaltenbereich aus, den Sie suchen möchten.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL filter]</td> 
   <td> <p>Definieren Sie den Filter, nach dem Sie Antworten suchen möchten.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Sortierreihenfolge] </td>
   <td> <p>Wählen Sie aus, ob die zurückgegebenen Antworten in auf- oder absteigender Reihenfolge sortiert werden sollen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Sortieren nach]</td>
   <td> <p> Wählen Sie die Spalte aus, nach der die zurückgegebenen Antworten sortiert werden sollen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Wert rendern option]</td> 
   <td> <p>Geben Sie an, wie die Werte in der Ausgabe gerendert werden sollen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL formatierter Wert]</strong></p> <p>Die Werte werden in der Antwort entsprechend der Zellenformatierung berechnet und formatiert. Die Formatierung basiert auf dem Gebietsschema der Tabelle, nicht auf dem Gebietsschema des anfragenden Benutzers. Wenn <code>A1</code> beispielsweise <code>1. 23</code> und <code>A2 </code>als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>$1. 23</code> zurück.</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>Die Werte werden berechnet, aber in der Antwort nicht formatiert. Wenn <code>A1</code> beispielsweise <code>1. 23</code> und <code>A2 </code>als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> die Zahl <code>1. 23</code> zurück.</p> </li> 
     <li> <p><strong>[!UICONTROL -Formel]</strong> </p> <p>Werte werden nicht berechnet. Die Antwort enthält die Formeln. Wenn <code>A1</code> beispielsweise <code>1. 23</code> und <code>A2 </code>als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>=A1</code> zurück.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Render-Option Datum und Uhrzeit]</td>
    <td>Wählen Sie aus, wie Datum, Uhrzeit und Dauer in der Ausgabe dargestellt werden sollen. Dieses Feld wird ignoriert, wenn die Option [!UICONTROL Value Render] auf Formatierter Wert gesetzt ist. </td>
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Maximale Anzahl der zurückgegebenen Antworten]</td>
   <td> <p> Legen Sie die maximale Anzahl von Antworten fest, die Workfront Fusion während eines Zyklus zurückgibt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Suchantworten (erweitert)]

Dieses Modul führt eine Suche mit dem [[!DNL Google Charts Query Language]](https://developers.google.com/chart/interactive/docs/querylanguage) durch. Dieses Modul gibt keine Zeilennummer zurück.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL -Verbindung]</td>
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google]-Kontos mit Workfront Fusion finden Sie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL -Tabelle]</td>
   <td> <p>Wählen Sie das Arbeitsblatt aus, das das zu durchsuchende Arbeitsblatt enthält.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Sheet]</td>
   <td> <p> Wählen Sie das Blatt aus, das die Formularantworten enthält.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Abfrage]</td> 
   <td> <p>Definieren Sie die Suchabfrage mithilfe der <a href="https://developers.google.com/chart/interactive/docs/querylanguage">[!DNL Google Charts Query Language]</a>.</p> <p>Beispiel: <code>select * where C = "John"</code> ruft alle Werte für die Zeile ab, in der die Spalte C „John“ lautet.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Zeilen]</td>
   <td> <p> Legen Sie die maximale Anzahl von Antworten fest, die Workfront Fusion während eines Zyklus zurückgibt.</p> </td> 
  </tr> 
 </tbody> 
</table>
