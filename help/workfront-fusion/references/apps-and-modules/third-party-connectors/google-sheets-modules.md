---
title: Google Sheets-Module
description: So verwenden Sie  [!DNL Google Sheets] -mit [!DNL Adobe Workfront Fusion],you need the [!UICONTROL Workfront Fusion Google Sheets] Erweiterung (optional, aber für sofortige Trigger erforderlich).
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 80965570-2937-4ac8-97c0-54f7a813ec50
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '3367'
ht-degree: 0%

---

# [!DNL Google Sheets]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Google Sheets] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion]  - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

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

Um [!UICONTROL Google Sheets]-Module verwenden zu können, müssen Sie über ein [!UICONTROL Google]-Konto verfügen.

## Google Sheets-API-Informationen

Der Google Sheets-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://sheets.googleapis.com/v4</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v2.5.7</td> 
  </tr>
 </tbody> 
 </table>

## Trigger

### [!UICONTROL Watch Rows]

Ruft Werte aus jeder neu hinzugefügten Zeile im Arbeitsblatt ab.

Das Modul ruft nur neue Zeilen ab, die noch nicht ausgefüllt wurden. Der Trigger verarbeitet keine überschriebene Zeile.

>[!IMPORTANT]
>
>Wenn das Arbeitsblatt eine leere Zeile enthält, werden keine Zeilen nach der leeren Zeile verarbeitet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie die Tabelle aus, die die Tabelle enthält, die Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, auf das Sie eine neue Zeile überwachen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table contains headers]</td> 
   <td> <p> Wählen Sie aus, ob das Arbeitsblatt die Kopfzeile enthält.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>Das Modul ruft die Kopfzeile nicht als Ausgabedaten ab. </p> <p>Variablennamen in der Ausgabe werden von den Kopfzeilen aufgerufen.</p> </li> 
     <li> <p><strong>[!UICONTROL No]</strong> </p> <p>Das Modul ruft auch die erste Tabellenzeile ab</p> <p>Variablennamen in der Ausgabe werden als A, B, C, D usw. bezeichnet.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row with headers] </td> 
   <td> <p>Geben Sie den Bereich der Kopfzeile ein. Beispiel: <code>A1:F1</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL First table row]</td> 
   <td> <p>Geben Sie den Bereich der ersten Zeile der Tabelle ein. Beispiel: <code>A1:F1</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Value render option]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>Die Werte werden in der Antwort entsprechend der Zellenformatierung berechnet und formatiert. Die Formatierung basiert auf dem Gebietsschema der Tabelle, nicht auf dem Gebietsschema des anfragenden Benutzers. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"$1.23"</code> zurück.</p> <p style="font-weight: bold;">[!UICONTROL Unformatted value]</p> <p>Die Werte werden berechnet, in der Antwort jedoch nicht formatiert. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> die Zahl <code>"1.23"</code> zurück.</p> <p style="font-weight: bold;">[!UICONTROL Formula]</p> <p>Die Werte werden nicht berechnet. Die Antwort enthält die Formeln. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"=A1"</code> zurück.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Date and time render option]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Serial number]</p> <p>Weist Felder für Datum, Uhrzeit, Datum, Uhrzeit und Dauer an, die als Dubletten im Format „Seriennummer“ ausgegeben werden, wie durch Lotus 1-2-3 populär gemacht. Der ganze Zahlenteil des Werts (links vom Dezimaltrennzeichen) zählt die Tage seit dem 30. Dezember 1899. Der Bruchteil (rechts neben der Dezimalstelle) zählt die Zeit als einen Bruchteil des Tages. Zum Beispiel wäre der 1. Januar 1900 mittags 2,5, 2 weil es 2 Tage nach dem 30. Dezember 1899 ist, und .5 weil mittags ein halber Tag ist. 1. Februar 1900 um 15 Uhr wäre 33.625 Uhr. Damit wird das Jahr 1900 korrekt als Schaltjahr behandelt.</p> <p style="font-weight: bold;">[!UICONTROL Formatted string]</p> <p>Weist Felder für Datum, Uhrzeit, Datum, Uhrzeit und Dauer an, die als Zeichenfolgen im angegebenen Zahlenformat (das vom Gebietsschema der Tabelle abhängt) ausgegeben werden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Ergebnissen fest, mit denen [!DNL Workfront Fusion] während eines Ausführungszyklus arbeiten soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Aktionen

* [[!UICONTROL Add a Row]](#add-a-row)
* [[!UICONTROL Update a Row]](#update-a-row)
* [[!UICONTROL Clear a Row]](#clear-a-row)
* [[!UICONTROL Delete a Row]](#delete-a-row)
* [[!UICONTROL Get a Cell]](#get-a-cell)
* [[!UICONTROL Update a Cell]](#update-a-cell)
* [[!UICONTROL Clear a Cell]](#clear-a-cell)
* [[!UICONTROL Add a Sheet]](#add-a-sheet)
* [[!UICONTROL Create a Spreadsheet]](#create-a-spreadsheet)
* [[!UICONTROL Delete a Sheet]](#delete-a-sheet)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

### [!UICONTROL Add a Row]

Dieses Modul fügt eine Zeile zu einem Blatt hinzu.

Beim Konfigurieren [!DNL Google Sheets] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Google Sheets] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mode]</td> 
   <td> <p>Wählen Sie aus, ob Sie die Tabelle und das Blatt manuell oder durch Zuordnung auswählen möchten.</p> <p>Hinweis: Die manuelle Zuordnung ist beispielsweise dann nützlich, wenn in einem [!DNL Workfront Fusion] Szenario eine neue Tabelle erstellt wird und Sie der neu erstellten Tabelle direkt im Szenario Daten hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, dem Sie eine Zeile hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Range]</td> 
   <td>Wählen Sie den Spaltenbereich aus, mit dem Sie arbeiten möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> Wählen Sie aus, ob das Arbeitsblatt die Kopfzeile enthält.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>Das Modul ruft die Kopfzeile nicht als Ausgabedaten ab. </p> <p>Variablennamen in der Ausgabe werden von den Kopfzeilen aufgerufen.</p> </li> 
     <li> <p><strong>[!UICONTROL No]</strong> </p> <p>Das Modul ruft auch die erste Tabellenzeile ab</p> <p>Variablennamen in der Ausgabe werden als A, B, C, D usw. bezeichnet.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Values] </td> 
   <td> <p>Geben Sie die gewünschten Zellen der Zeile ein, die Sie hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>Die Werte werden analysiert, als ob der Benutzer sie in die Benutzeroberfläche eingegeben hätte. Zahlen bleiben Zahlen, Zeichenfolgen können jedoch nach denselben Regeln, die bei der Eingabe von Text in eine Zelle über die [!DNL Google Sheets]-Benutzeroberfläche angewendet werden, in Zahlen, Daten oder andere Formate konvertiert werden.</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Die vom Benutzer eingegebenen Werte werden nicht geparst und unverändert gespeichert. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Insert data option]</td> 
   <td> <p>Geben Sie an, wie vorhandene Daten bei der Eingabe neuer Daten geändert werden. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Insert rows]</strong></p> <p>Für die neuen Daten werden Zeilen eingefügt.</p> </li> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>Die neuen Daten überschreiben vorhandene Daten in den Bereichen, in denen sie geschrieben werden. Durch Hinzufügen von Daten am Ende des Arbeitsblatts werden neue Zeilen oder Spalten eingefügt, damit die Daten geschrieben werden können.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a Row]

Mit diesem Modul können Sie den Zelleninhalt in einer ausgewählten Zeile ändern.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mode]</td> 
   <td> <p>Wählen Sie aus, ob Sie die Tabelle und das Blatt manuell oder durch Zuordnung auswählen möchten.</p> <p>Hinweis: Die manuelle Zuordnung ist beispielsweise dann nützlich, wenn im [!UICONTROL Workfront Fusion] Szenario eine neue Tabelle erstellt wird und Sie der neu erstellten Tabelle direkt im Szenario Daten hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, in dem Sie eine Zeile aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Row number]</td> 
   <td> <p> Geben Sie die Nummer der Zeile ein, die Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> Wählen Sie aus, ob das Arbeitsblatt die Kopfzeile enthält.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>Das Modul ruft die Kopfzeile nicht als Ausgabedaten ab. </p> <p>Variablennamen in der Ausgabe werden von den Kopfzeilen aufgerufen.</p> </li> 
     <li> <p><strong>[!UICONTROL No]</strong> </p> <p>Das Modul ruft auch die erste Tabellenzeile ab</p> <p>Variablennamen in der Ausgabe werden als A, B, C, D usw. bezeichnet.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Values] </td> 
   <td> <p>Geben Sie die Werte in die gewünschten Zellen der Zeile ein, die Sie ändern (aktualisieren) möchten, oder ordnen Sie sie ihnen zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>Die Werte werden analysiert, als ob der Benutzer sie in die Benutzeroberfläche eingegeben hätte. Zahlen bleiben Zahlen, Zeichenfolgen können jedoch nach denselben Regeln, die bei der Eingabe von Text in eine Zelle über die [!DNL Google Sheets]-Benutzeroberfläche angewendet werden, in Zahlen, Daten oder andere Formate konvertiert werden.</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Die vom Benutzer eingegebenen Werte werden nicht geparst und unverändert gespeichert. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Clear a Row]

Löscht Werte aus einer angegebenen Zeile.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus, die das Blatt enthält, aus dem Sie eine Zeile löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p> Wählen Sie die Tabelle aus, deren Daten Sie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Row number]</td> 
   <td> <p>Geben Sie die Nummer der Zeile ein, aus der Sie Daten löschen möchten. Beispiel: <code> 23</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a Row]

Löscht eine angegebene Zeile.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie das Google-Arbeitsblatt aus, das das Arbeitsblatt enthält, aus dem Sie eine Zeile löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Arbeitsblatt </td> 
   <td> <p>Wählen Sie das Blatt aus, aus dem Sie eine Zeile löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>Zeilennummer</td> 
   <td> <p>Geben Sie die Nummer der Zeile ein, die Sie löschen möchten. Beispiel: <code>23</code></p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get a Cell]

Ruft einen Wert aus einer ausgewählten Zelle ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, das die Zelle enthält, aus der Sie Daten abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cell] </td> 
   <td> <p>Geben Sie die ID der Zelle ein, von der Sie Daten abrufen möchten. Beispiel: <code>A6</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>Die Werte werden in der Antwort entsprechend der Zellenformatierung berechnet und formatiert. Die Formatierung basiert auf dem Gebietsschema der Tabelle, nicht auf dem Gebietsschema des anfragenden Benutzers. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"$1.23"</code> zurück.</p> <p style="font-weight: bold;">[!DNL Unformatted value]</p> <p>Die Werte werden berechnet, in der Antwort jedoch nicht formatiert. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> die Zahl <code>"1.23"</code> zurück.</p> <p style="font-weight: bold;">[!DNL Formula]</p> <p>Die Werte werden nicht berechnet. Die Antwort enthält die Formeln. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"=A1"</code> zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Date and time render option]</td> 
   <td> <p style="font-weight: bold;">[!DNL Serial number]</p> <p>Weist Felder für Datum, Uhrzeit, Datum, Uhrzeit und Dauer an, die als Dubletten im Format „Seriennummer“ ausgegeben werden, wie durch Lotus 1-2-3 populär gemacht. Der ganze Zahlenteil des Werts (links vom Dezimaltrennzeichen) zählt die Tage seit dem 30. Dezember 1899. Der Bruchteil (rechts neben der Dezimalstelle) zählt die Zeit als einen Bruchteil des Tages. Zum Beispiel wäre der 1. Januar 1900 mittags 2,5, 2 weil es 2 Tage nach dem 30. Dezember 1899 ist, und .5 weil mittags ein halber Tag ist. 1. Februar 1900 um 15 Uhr wäre 33.625 Uhr. Damit wird das Jahr 1900 korrekt als Schaltjahr behandelt.</p> <p style="font-weight: bold;">[!DNL Formatted string]</p> <p>Weist Felder für Datum, Uhrzeit, Datum, Uhrzeit und Dauer an, die als Zeichenfolgen im angegebenen Zahlenformat (das vom Gebietsschema der Tabelle abhängt) ausgegeben werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a Cell]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cell] </td> 
   <td> <p>Geben Sie die ID der Zelle ein, die Sie aktualisieren möchten. Beispiel: <code>A5</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value]</td> 
   <td> <p>Geben Sie den neuen Wert für die Zelle ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>Die Werte werden analysiert, als ob der Benutzer sie in die Benutzeroberfläche eingegeben hätte. Zahlen bleiben Zahlen, Zeichenfolgen können jedoch nach denselben Regeln, die bei der Eingabe von Text in eine Zelle über die [!DNL Google Sheets]-Benutzeroberfläche angewendet werden, in Zahlen, Daten oder andere Formate konvertiert werden.</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Die vom Benutzer eingegebenen Werte werden nicht geparst und unverändert gespeichert. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Clear a Cell]

Löscht einen Wert aus einer angegebenen Zelle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie das Google-Arbeitsblatt aus, das das Arbeitsblatt enthält, aus dem Sie eine Zelle löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie die Tabelle aus, aus der Sie eine Zelle löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cell] </td> 
   <td> <p>Geben Sie die Kennung der Zelle ein, die Sie löschen möchten. Beispiel: <code>A5</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Add a Sheet]

Erstellt eine neue Tabelle in einer ausgewählten Tabelle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie das Google-Arbeitsblatt aus, dem Sie ein Arbeitsblatt hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Properties]</td> 
   <td> 
    <ul> 
     <li> <p style="font-weight: bold;">[!UICONTROL Title]</p> <p>Geben Sie den Namen der neuen Tabelle ein.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Index]</p> <p>Die Position des Blatts eingeben. Der Standardwert ist 0 (platziert das Blatt an erster Stelle)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Create a Spreadsheet]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title] </td> 
   <td> <p>Geben Sie den Namen einer neuen Tabelle ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Locale]</td> 
   <td> <p>Geben Sie das Gebietsschema des Arbeitsblatts in einem der folgenden Formate ein:</p> 
    <ul> 
     <li>einem ISO-639-1-Sprach-Code, z. B. <code>en</code></li> 
     <li>einen ISO-639-2-Sprach-Code wie <code>haw</code>, wenn kein 639-1-Code vorhanden ist</li> 
     <li>eine Kombination aus ISO-Sprach-Code und Ländercode, z. B. <code>en_US</code></li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recalculation interval]</td> 
   <td> <p>Die Wartezeit, bevor flüchtige Funktionen neu berechnet werden:</p> <p style="font-weight: bold;">[!UICONTROL On change]</p> <p>Flüchtige Funktionen werden bei jeder Änderung aktualisiert.</p> <p style="font-weight: bold;">[!UICONTROL On change and every minute]</p> <p>Flüchtige Funktionen werden bei jeder Änderung und jede Minute aktualisiert.</p> <p style="font-weight: bold;">[!UICONTROL On change and hourly]</p> <p>Volatile Funktionen werden bei jeder Änderung und stündlich aktualisiert.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Time zone]</td> 
   <td> <p> Wählen Sie die Zeitzone der Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Number format]</td> 
   <td> <p>Wählen Sie das Standardformat aller Zellen im Arbeitsblatt aus.</p> <p><strong>[!UICONTROL Text]</strong>: Textformatierung. Beispiel: <code>1000. 12</code></p> <p><strong>[!UICONTROL Number]</strong>: Formatierung von Zahlen. Beispiel: <code>1,000.12</code></p> <p><strong>[!UICONTROL Percent]</strong>: Prozentformatierung. Beispiel: <code>10. 12%</code></p> <p><strong>[!UICONTROL Currency]</strong>: Währungsformatierung. Beispiel: <code>$1,000.12</code></p> <p><strong>[!UICONTROL Date]</strong>: Datumsformatierung. Beispiel: <code>9/26/2008</code></p> <p><strong>[!UICONTROL Time]</strong>: Zeitformatierung. Beispiel: <code>3:59:00 PM</code></p> <p><strong>[!UICONTROL Date time]</strong>: Formatierung von Datum und Uhrzeit. Beispiel: <code>9/26/08 15:59:00</code> </p> <p><strong>[!UICONTROL Scientific]</strong>Wissenschaftliche Zahlenformatierung. Beispiel: <code>1. 01E+03</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheets] </td> 
   <td> <p>Klicken Sie auf <strong>[!UICONTROL Add]</strong> , um dem Arbeitsblatt ein Arbeitsblatt hinzuzufügen. Geben Sie für jedes Blatt einen Titel für das Blatt und den Index des Blatts ein oder mappen Sie ihn. Ein Index von 0 stellt das erste Blatt dar.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a Sheet]

Löscht eine bestimmte Tabelle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie die Tabelle aus, die Sie löschen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Make an API Call]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten API-Aufruf durchführen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [Fusion App]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://sheets.googleapis.com/v4/</code> ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu, z. B. <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:   <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suchvorgänge

* [[!UICONTROL Search Rows]](#search-rows)
* [[!UICONTROL Search Rows (Advanced)]](#search-rows-advanced)
* [[!UICONTROL Get Range Values]](#get-range-values)
* [[!UICONTROL List Sheets]](#list-sheets)

### [!UICONTROL Search Rows]

Durchsucht Zeilen mithilfe der Filteroptionen.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [Fusion App]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, in dem Sie die Zeilen durchsuchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> Wählen Sie aus, ob das Arbeitsblatt die Kopfzeile enthält. Wenn die Option [!UICONTROL Yes] ausgewählt ist, ruft das Modul die Kopfzeile nicht ab, da Ausgabedaten und Variablennamen in der Ausgabe von den Kopfzeilen aufgerufen werden. Wenn die Option [!UICONTROL No] ausgewählt ist, ruft das Modul auch die erste Tabellenzeile ab und die Variablennamen in der Ausgabe werden nur A, B, C, D usw. genannt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column range]</td> 
   <td>Wählen Sie den Spaltenbereich aus, mit dem Sie arbeiten möchten. Beispiel: <code>A-F</code></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter]</td> 
   <td> <p>Filter für die Zeile festlegen, nach der gesucht werden soll.</p> <!--<p>For more information about filters, see <a href="/help/workfront-fusion/create-scenarios/add-modules/" class="MCXref xref">Add a filter to a scenario in [!UICONTROL Adobe Workfront Fusion]</a>.</p>--> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort order]</td> 
   <td>Wählen Sie aus, ob auf- oder absteigend sortiert werden soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td>Wählen Sie die Spalte aus, nach der Sie sortieren möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>Die Werte werden in der Antwort entsprechend der Zellenformatierung berechnet und formatiert. Die Formatierung basiert auf dem Gebietsschema der Tabelle, nicht auf dem Gebietsschema des anfragenden Benutzers. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"$1.23"</code> zurück.</p> <p style="font-weight: bold;">[!UICONTROL Unformatted value]</p> <p>Die Werte werden berechnet, in der Antwort jedoch nicht formatiert. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> die Zahl <code>"1.23"</code> zurück.</p> <p style="font-weight: bold;">[!UICONTROL Formula]</p> <p>Die Werte werden nicht berechnet. Die Antwort enthält die Formeln. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"=A1"</code> zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Date and time render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Serial number]</p> <p>Weist Felder für Datum, Uhrzeit, Datum/Uhrzeit und Dauer an, die als Dubletten im Format „Seriennummer“ ausgegeben werden, wie durch Lotus 1-2-3 populär gemacht. Der ganze Zahlenteil des Werts (links vom Dezimaltrennzeichen) zählt die Tage seit dem 30. Dezember 1899. Der Bruchteil (rechts neben der Dezimalstelle) zählt die Zeit als einen Bruchteil des Tages. Zum Beispiel wäre der 1. Januar 1900 mittags 2,5, 2 weil es 2 Tage nach dem 30. Dezember 1899 ist, und .5 weil mittags ein halber Tag ist. 1. Februar 1900 um 15 Uhr wäre 33.625 Uhr. Damit wird das Jahr 1900 korrekt als Schaltjahr behandelt.</p> <p style="font-weight: bold;">[!UICONTROL Formatted string]</p> <p>Weist Felder für Datum, Uhrzeit, Datum, Uhrzeit und Dauer an, die als Zeichenfolgen im angegebenen Zahlenformat (das vom Gebietsschema der Tabelle abhängt) ausgegeben werden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned rows]</td> 
   <td>Legen Sie die maximale Anzahl von Zeilen fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Search Rows (Advanced)]

Gibt Ergebnisse zurück, die den angegebenen Kriterien entsprechen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie das Google-Arbeitsblatt aus, das das zu durchsuchende Arbeitsblatt enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, das die Zeilen enthält, nach denen Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>Verwenden Sie die [!DNL Google Charts Query Language]. Beispiel: <code>select * where B = "John"</code></p> <p>Weitere Informationen zu [!DNL Google Charts Query Language] finden Sie unter <a href="https://developers.google.com/chart/interactive/docs/querylanguage">Abfrage-</a>" in der [!DNL Google].</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get Range Values]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie die Tabelle aus, aus der Sie den Bereichsinhalt abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Range] </td> 
   <td> <p>Geben Sie den Bereich ein, den Sie erhalten möchten. Beispiel: <code>A1:D25</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p>Aktivieren Sie dieses Kontrollkästchen, wenn das Blatt eine Kopfzeile hat</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Row with headers]</td> 
   <td>Geben Sie den Bereich der Tabellenüberschriften ein. Beispiel <code>A1:F1</code>. Wenn Sie das Feld leer lassen, nehmen [!DNL Workfront Fusion] an, dass sich die Kopfzeile in der ersten Zeile des angegebenen Bereichs befindet.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>Die Werte werden in der Antwort entsprechend der Zellenformatierung berechnet und formatiert. Die Formatierung basiert auf dem Gebietsschema der Tabelle, nicht auf dem Gebietsschema des anfragenden Benutzers. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"$1.23"</code> zurück.</p> <p style="font-weight: bold;">[!UICONTROL Unformatted value]</p> <p>Die Werte werden berechnet, in der Antwort jedoch nicht formatiert. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> die Zahl <code>"1.23"</code> zurück.</p> <p style="font-weight: bold;">[!UICONTROL Formula]</p> <p>Die Werte werden nicht berechnet. Die Antwort enthält die Formeln. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"=A1"</code> zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Date and time render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Serial number]</p> <p>Weist Felder für Datum, Uhrzeit, Datum/Uhrzeit und Dauer an, die als Dubletten im Format „Seriennummer“ ausgegeben werden, wie durch Lotus 1-2-3 populär gemacht. Der ganze Zahlenteil des Werts (links vom Dezimaltrennzeichen) zählt die Tage seit dem 30. Dezember 1899. Der Bruchteil (rechts neben der Dezimalstelle) zählt die Zeit als einen Bruchteil des Tages. Zum Beispiel wäre der 1. Januar 1900 mittags 2,5, 2 weil es 2 Tage nach dem 30. Dezember 1899 ist, und .5 weil mittags ein halber Tag ist. 1. Februar 1900 um 15 Uhr wäre 33.625 Uhr. Damit wird das Jahr 1900 korrekt als Schaltjahr behandelt.</p> <p style="font-weight: bold;">[!UICONTROL Formatted string]</p> <p>Weist Felder für Datum, Uhrzeit, Datum, Uhrzeit und Dauer an, die als Zeichenfolgen im angegebenen Zahlenformat (das vom Gebietsschema der Tabelle abhängt) ausgegeben werden.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL List Sheets]

Dieses Modul gibt eine Liste aller Blätter in einer Tabelle zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus, die die Tabellen enthält, die Sie auflisten möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Nutzungsbeschränkungen

Wenn der `429: RESOURCE_EXHAUSTED` auftritt, haben Sie das API-Ratenlimit überschritten.

Die [!DNL Google Sheets]-API begrenzt 500 Anfragen pro 100 Sekunden pro Projekt und 100 Anfragen pro 100 Sekunden pro Benutzer. Beschränkungen für Lese- und Schreibvorgänge werden separat verfolgt. Es gibt keine tägliche Nutzungsbeschränkung.

Weitere Informationen finden Sie unter [developers.google.com/sheets/api/limits](https://developers.google.com/sheets/api/limits).

## Tipps und Tricks

* [So rufen Sie leere Zellen aus einem  [!DNL Google]  ab](#how-to-get-empty-cells-from-a-google-sheet)
* [Schaltfläche in einem Blatt hinzufügen, um ein Szenario auszuführen](#add-a-button-in-a-sheet-to-run-a-scenario)

### So rufen Sie leere Zellen aus einem [!DNL Google Sheet] ab

Verwenden Sie das [!UICONTROL Search Rows (Advanced)] und verwenden Sie diese Formel, um die leeren Spalten abzurufen.
<pre>* auswählen, wobei E null ist</pre>Hier ist „E“ die Spalte und „ist null“ die Bedingung. Sie können eine erweiterte Abfrage mithilfe von [Google Query Lang](https://developers.google.com/chart/interactive/docs/querylanguage) erstellen.

### Schaltfläche in einem Blatt hinzufügen, um ein Szenario auszuführen

1. Fügen Sie [!DNL Workfront Fusion] das **[!UICONTROL Webhook]** > **[!UICONTROL Custom webhooks]**/den Trigger in das Szenario ein und konfigurieren Sie es (siehe [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)).

1. Kopieren Sie die URL des Webhooks.
1. Führen Sie das Szenario aus.
1. Wählen Sie in Google Sheets **[!UICONTROL Insert]** > **[!UICONTROL Drawing]**… aus der Hauptmenüleiste aus.

1. Klicken Sie im [!UICONTROL Drawing] Fenster oben ![](/help/workfront-fusion/references/apps-and-modules/assets/text-box.png) im Fenster auf das **[!UICONTROL Text box]**.
1. Gestalten Sie eine Schaltfläche und klicken Sie oben rechts auf die Schaltfläche **[!UICONTROL Save and Close]** :
1. Die Schaltfläche wird in Ihrem Arbeitsblatt platziert. Klicken Sie auf die drei vertikalen Punkte in der oberen rechten Ecke der Schaltfläche:
1. Wählen Sie **[!UICONTROL Assign script..].** aus dem Menü.
1. Geben Sie den Namen Ihres Skripts (Funktion) ein, z. B. `runScenario`, und klicken Sie auf **[!UICONTROL OK]**:
1. Wählen Sie in der Hauptmenüleiste **[!UICONTROL Tools]** > **[!UICONTROL Script editor]** aus.

1. Fügen Sie den folgenden Code ein:

   * Der Name der Funktion muss dem in Schritt 9 angegebenen Namen entsprechen.
   * Ersetzen Sie die URL durch die URL des Webhooks, die Sie in Schritt 2 kopiert haben.

     <pre>runScenario() {</pre><pre>UrlFetchApp.fetch(“&lt;Webhook Sie haben kopiert&gt;„);</pre><pre>}</pre>

1. Drücken Sie **[!UICONTROL Ctrl+S]**, um die Skriptdatei zu speichern, geben Sie einen Projektnamen ein und klicken Sie auf **[!UICONTROL OK]**.

1. Wechseln Sie zurück zu [!DNL Google Sheets] und klicken Sie auf Ihre neue Schaltfläche.
1. Gewähren Sie dem Skript die erforderliche Autorisierung:
1. Überprüfen Sie [!DNL Workfront Fusion], ob das Szenario erfolgreich ausgeführt wurde.

## Daten in einer Tabelle speichern

Wenn Sie einen Datumswert ohne Formatierung in einer Tabelle speichern, wird er in der Tabelle als Text im ISO 8601-Format angezeigt. [!DNL Google Sheets] Formeln oder Funktionen, die mit Datumsangaben arbeiten, die diesen Text nicht verstehen (Beispiel: Formel `=A1+10`), zeigen jedoch den folgenden Fehler an:

![](/help/workfront-fusion/references/apps-and-modules/assets/mceclip6-350x87.png)

Damit [!DNL Google Sheets] das Datum besser verstehen können, formatieren Sie es mit der [[!UICONTROL formatDate]-Funktion (Datum; Format; [Zeitzone])](/help/workfront-fusion/references/mapping-panel/functions/date-and-time-functions.md#formatda). Das richtige Format, das als zweites Argument an die Funktion übergeben wird, hängt von den Gebietsschemaeinstellungen der Tabelle ab.

So bestimmen Sie das richtige Format:

1. Wählen Sie **[!UICONTROL File]** > **[!UICONTROL Spreadsheet]** aus dem Hauptmenü, um das Gebietsschema zu überprüfen/festzulegen.

1. Nachdem Sie das richtige Gebietsschema überprüft/festgelegt haben, bestimmen Sie das entsprechende Datums- und Uhrzeitformat, indem Sie **[!UICONTROL Format]** > **[!UICONTROL Number]** aus dem Hauptmenü auswählen. Das Format wird neben dem Datums-/Uhrzeitmenüpunkt angezeigt:

1. Um das richtige Format zu erstellen, das an die [!UICONTROL formatDate()]-Funktion übergeben werden soll, verwenden Sie die Liste der [Token zur Datums- und Zeitformatierung](/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md).

**Beispiel** Die Verwendung `MM/DD/YYYY HH:mm:ss` Formats für das Gebietsschema der Vereinigten Staaten:

![](/help/workfront-fusion/references/apps-and-modules/assets/locale-time-350x83.png)

## Nutzung [!DNL Google Sheets] Funktionen

Wenn Sie eine integrierte Funktion vermissen, sie jedoch von [!DNL Google Sheets] vorgestellt wird, können Sie sie ausnutzen. Weitere Informationen finden Sie unter [Verwenden [!DNL Google Sheets] Funktionen](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md#exploiti) in [Zuordnen von Elementen mithilfe von Funktionen in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md) .

## Vermeiden [!DNL Google Sheets] das Ändern von Zahlen in Datumsangaben

Möglicherweise stellen Sie fest, dass eine Zahlenfolge, die Sie als Text verwenden, in einem [!DNL Google] Arbeitsblatt als Datum interpretiert wird. Sie geben z. B. 1-2019 ein, um es als Text zu interpretieren, aber Google interpretiert es als Datum. Um dies zu verhindern, können Sie die Zahl als einfachen Text vorformatieren.

1. Markieren Sie [!DNL Google Sheets] die Spalte oder Zelle, die die Zahl oder die Zahlen enthält.
1. Klicken Sie auf **[!UICONTROL Format]** > **[!UICONTROL Number]** > **[!UICONTROL Plain text]**.

Eine weitere Problemumgehung in [!DNL Workfront Fusion] besteht darin, vor einer Zahl ein Apostroph (&#39;) einzugeben, z. B. &#39;1-2019 oder &#39;1/47. Das Apostroph wird in der Zelle nicht angezeigt, nachdem die Daten von [!DNL Workfront Fusion] gesendet wurden.
