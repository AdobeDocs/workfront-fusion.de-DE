---
title: Google Sheets-Module
description: So verwenden Sie  [!DNL Google Sheets] -mit [!DNL Adobe Workfront Fusion],you need the [!UICONTROL Workfront Fusion Google Sheets] Erweiterung (optional, aber für sofortige Trigger erforderlich).
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 80965570-2937-4ac8-97c0-54f7a813ec50
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '3957'
ht-degree: 0%

---

# [!DNL Google Sheets]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Google Sheets] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung zu [!DNL Adobe Workfront Fusion]  - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

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

## Google Sheets-Module und ihre Felder

Beim Konfigurieren [!DNL Google Forms] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Google Sheets] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Auslöser

#### [!UICONTROL Zeilen ansehen]

Ruft Werte aus neu hinzugefügten Zeilen im Arbeitsblatt ab.

Das Modul ruft nur neue Zeilen ab, die noch nicht ausgefüllt wurden. Der Trigger verarbeitet keine überschriebene Zeile.

>[!IMPORTANT]
>
>Wenn das Arbeitsblatt eine leere Zeile enthält, werden nach der leeren Zeile keine Zeilen verarbeitet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie die Tabelle aus, die die Tabelle enthält, die Sie beobachten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, auf das Sie eine neue Zeile überwachen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tabelle enthält Kopfzeilen]</td> 
   <td> <p> Wählen Sie aus, ob das Arbeitsblatt eine Kopfzeile enthält.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>Das Modul ruft die Kopfzeile nicht als Ausgabedaten ab. </p> <p>Variablennamen in der Ausgabe werden von den Kopfzeilen aufgerufen.</p> </li> 
     <li> <p><strong>[!UICONTROL Nein]</strong> </p> <p>Das Modul ruft auch die erste Tabellenzeile ab</p> <p>Variablennamen in der Ausgabe werden als A, B, C, D usw. bezeichnet.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zeile mit Überschriften] </td> 
   <td> <p>Geben Sie den Bereich der Kopfzeile ein. Beispiel: <code>A1:F1</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Erste Tabellenzeile]</td> 
   <td> <p>Geben Sie den Bereich der ersten Zeile der Tabelle ein. Beispiel: <code>A1:F1</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Wert renderoption]</p> </td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL formatierter Wert]</p> <p>Die Werte werden in der Antwort entsprechend der Zellenformatierung berechnet und formatiert. Die Formatierung basiert auf dem Gebietsschema der Tabelle, nicht auf dem Gebietsschema des anfragenden Benutzers. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"$1.23"</code> zurück.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Unformatierter Wert]</p> <p>Die Werte werden berechnet, in der Antwort jedoch nicht formatiert. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> die Zahl <code>"1.23"</code> zurück.</p></li><li> <p style="font-weight: bold;">[!UICONTROL -Formel]</p> <p>Die Werte werden nicht berechnet. Die Antwort enthält die Formeln. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"=A1"</code> zurück.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Render-Option Datum und Uhrzeit]</p> </td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL Seriennummer]</p> <p>Die Felder „Datum“, „Uhrzeit“, „Datum/Uhrzeit“ und „Dauer“ werden als Dubletten im Format „Seriennummer“ ausgegeben, wie es von Lotus 1-2-3 populär gemacht wird. Der ganze Zahlenteil des Werts (links vom Dezimaltrennzeichen) zählt die Tage seit dem 30. Dezember 1899. Der Bruchteil (rechts neben der Dezimalstelle) zählt die Zeit als einen Bruchteil des Tages. Zum Beispiel wäre der 1. Januar 1900 mittags 2,5, 2 weil es 2 Tage nach dem 30. Dezember 1899 ist, und .5 weil mittags ein halber Tag ist. 1. Februar 1900 um 15 Uhr wäre 33.625 Uhr. Damit wird das Jahr 1900 korrekt als Schaltjahr behandelt.</p> </li><li><p style="font-weight: bold;">[!UICONTROL formatierter String]</p> <p>Die Felder für Datum, Uhrzeit, Datum/Uhrzeit und Dauer werden als Zeichenfolgen im angegebenen Zahlenformat ausgegeben (das vom Gebietsschema der Tabelle abhängt).</p></li><ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Legen Sie die maximale Anzahl von Ergebnissen fest, mit denen [!DNL Workfront Fusion] während eines Ausführungszyklus arbeiten soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Zeile hinzufügen]](#add-a-row)
* [[!UICONTROL Tabelle hinzufügen]](#add-a-sheet)
* [[!UICONTROL Zelle löschen]](#clear-a-cell)
* [[!UICONTROL Zeile löschen]](#clear-a-row)
* [[!UICONTROL Erstellen einer Tabelle]](#create-a-spreadsheet)
* [[!UICONTROL Zeile löschen]](#delete-a-row)
* [[!UICONTROL Tabelle löschen]](#delete-a-sheet)
* [[!UICONTROL Zelle abrufen]](#get-a-cell)
* [[!UICONTROL Erstellen eines API-Aufrufs]](#make-an-api-call)
* [[!UICONTROL Zelle aktualisieren]](#update-a-cell)
* [[!UICONTROL Zeile aktualisieren]](#update-a-row)

#### [!UICONTROL Zeile hinzufügen]

Dieses Modul fügt eine Zeile zu einem Blatt hinzu.

Beim Konfigurieren [!DNL Google Sheets] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Google Sheets] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Modus]</td> 
   <td> <p>Wählen Sie aus, ob Sie die Tabelle und das Blatt manuell oder durch Zuordnung auswählen möchten.</p> <p>Hinweis: Die manuelle Zuordnung ist beispielsweise dann nützlich, wenn in einem [!DNL Workfront Fusion] Szenario eine neue Tabelle erstellt wird und Sie der neu erstellten Tabelle direkt im Szenario Daten hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, dem Sie eine Zeile hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spaltenbereich]</td> 
   <td>Wählen Sie den Spaltenbereich aus, mit dem Sie arbeiten möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tabelle enthält Kopfzeilen]</td> 
   <td> <p> Wählen Sie aus, ob das Arbeitsblatt die Kopfzeile enthält.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>Das Modul ruft die Kopfzeile nicht als Ausgabedaten ab. </p> <p>Variablennamen in der Ausgabe werden von den Kopfzeilen aufgerufen.</p> </li> 
     <li> <p><strong>[!UICONTROL Nein]</strong> </p> <p>Das Modul ruft auch die erste Tabellenzeile ab</p> <p>Variablennamen in der Ausgabe werden als A, B, C, D usw. bezeichnet.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Werte] </td> 
   <td> <p>Geben Sie die gewünschten Zellen der Zeile ein, die Sie hinzufügen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Werteingabeoption]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Benutzer entered]</strong></p> <p>Die Werte werden analysiert, als ob der Benutzer sie in die Benutzeroberfläche eingegeben hätte. Zahlen bleiben Zahlen, Zeichenfolgen können jedoch nach denselben Regeln, die bei der Eingabe von Text in eine Zelle über die [!DNL Google Sheets]-Benutzeroberfläche angewendet werden, in Zahlen, Daten oder andere Formate konvertiert werden.</p> </li> 
     <li> <p><strong>[!UICONTROL RAW]</strong> </p> <p> Die vom Benutzer eingegebenen Werte werden nicht geparst und so gespeichert, wie sie eingegeben wurden. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Option zum Einfügen von Daten]</td> 
   <td> <p>Geben Sie an, wie vorhandene Daten bei der Eingabe neuer Daten geändert werden. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Zeilen einfügen]</strong></p> <p>Für die neuen Daten werden Zeilen eingefügt.</p> </li> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>Die neuen Daten überschreiben vorhandene Daten in den Bereichen, in denen sie geschrieben werden. Durch Hinzufügen von Daten am Ende des Arbeitsblatts werden neue Zeilen oder Spalten eingefügt, damit die Daten geschrieben werden können.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Tabelle hinzufügen]

Erstellt eine neue Tabelle in einer ausgewählten Tabelle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie das Google-Arbeitsblatt aus, dem Sie ein Arbeitsblatt hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Eigenschaften]</td> 
   <td> 
    <ul> 
     <li> <p style="font-weight: bold;">[!UICONTROL Titel]</p> <p>Geben Sie den Namen der neuen Tabelle ein.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Index]</p> <p>Die Position des Blatts eingeben. Der Standardwert ist 0 (wodurch das Blatt an erster Stelle steht).</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Zelle löschen]

Löscht einen Wert aus einer angegebenen Zelle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie das Google-Arbeitsblatt aus, das das Arbeitsblatt enthält, aus dem Sie eine Zelle löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie die Tabelle aus, aus der Sie eine Zelle löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zelle] </td> 
   <td> <p>Geben Sie die ID der Zelle ein, die Sie löschen möchten, oder mappen Sie sie. Beispiel: <code>A5</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Zeile löschen]

Löscht Werte aus einer angegebenen Zeile.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus, die das Blatt enthält, aus dem Sie eine Zeile löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p> Wählen Sie die Tabelle aus, deren Daten Sie löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zeilennummer]</td> 
   <td> <p>Geben Sie die Nummer der Zeile ein, aus der Sie Daten löschen möchten. Beispiel: <code> 23</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen einer Tabelle]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Titel] </td> 
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
   <td>[!UICONTROL Neuberechnungsintervall]</td> 
   <td> <p>Die Wartezeit, bevor flüchtige Funktionen neu berechnet werden:</p> <ul><li><p style="font-weight: bold;">[!UICONTROL bei Änderung]</p> <p>Flüchtige Funktionen werden bei jeder Änderung aktualisiert.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Bei Änderung und jede Minute]</p> <p>Flüchtige Funktionen werden bei jeder Änderung und jede Minute aktualisiert.</p></li> <li><p style="font-weight: bold;">[!UICONTROL Bei Änderung und stündlich]</p> <p>Volatile Funktionen werden bei jeder Änderung und stündlich aktualisiert.</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zeitzone]</td> 
   <td> <p> Wählen Sie die Zeitzone der Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zahlenformat]</td> 
   <td> <p>Wählen Sie das Standardformat aller Zellen im Arbeitsblatt aus.</p> <p><strong>[!UICONTROL Text]</strong>: Textformatierung. Beispiel: <code>1000. 12</code></p> <p><strong>[!UICONTROL number]</strong>: Zahlenformatierung. Beispiel: <code>1,000.12</code></p> <p><strong>[!UICONTROL Percent]</strong>: Formatierung in Prozent. Beispiel: <code>10. 12%</code></p> <p><strong>[!UICONTROL currency]</strong>: Währungsformatierung. Beispiel: <code>$1,000.12</code></p> <p><strong>[!UICONTROL date]</strong>: Datumsformatierung. Beispiel: <code>9/26/2008</code></p> <p><strong>[!UICONTROL Time]</strong>: Zeitformatierung. Beispiel: <code>3:59:00 PM</code></p> <p><strong>[!UICONTROL Datum/Uhrzeit]</strong>: Formatierung von Datum und Uhrzeit. Beispiel: <code>9/26/08 15:59:00</code> </p> <p><strong>[!UICONTROL Scientific]</strong>: Wissenschaftliche Zahlenformatierung. Beispiel: <code>1. 01E+03</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheets] </td> 
   <td> <p>Klicken Sie für jedes Blatt, das Sie dem Arbeitsblatt hinzufügen möchten, auf <strong>[!UICONTROL Element hinzufügen]</strong> und geben Sie einen Titel für das Blatt und den Index des Blatts ein oder mappen Sie ihn. Ein Index von 0 stellt das erste Blatt dar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Zeile löschen]

Löscht eine angegebene Zeile.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
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

#### [!UICONTROL Tabelle löschen]

Löscht eine bestimmte Tabelle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie die Tabelle aus, die Sie löschen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Zelle abrufen]

Ruft einen Wert aus einer ausgewählten Zelle ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, das die Zelle enthält, aus der Sie Daten abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zelle] </td> 
   <td> <p>Geben Sie die ID der Zelle ein, von der Sie Daten abrufen möchten. Beispiel: <code>A6</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Wert renderoption]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL formatierter Wert]</p> <p>Die Werte werden in der Antwort entsprechend der Zellenformatierung berechnet und formatiert. Die Formatierung basiert auf dem Gebietsschema der Tabelle, nicht auf dem Gebietsschema des anfragenden Benutzers. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"$1.23"</code> zurück.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Unformatierter Wert]</p> <p>Die Werte werden berechnet, in der Antwort jedoch nicht formatiert. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> die Zahl <code>"1.23"</code> zurück.</p></li><li> <p style="font-weight: bold;">[!UICONTROL -Formel]</p> <p>Die Werte werden nicht berechnet. Die Antwort enthält die Formeln. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"=A1"</code> zurück.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[!DNL Date and time render option]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!DNL Serial number]</p> <p>Die Felder „Datum“, „Uhrzeit“, „Datum/Uhrzeit“ und „Dauer“ werden als Dubletten im Format „Seriennummer“ ausgegeben, wie es von Lotus 1-2-3 populär gemacht wird. Der ganze Zahlenteil des Werts (links vom Dezimaltrennzeichen) zählt die Tage seit dem 30. Dezember 1899. Der Bruchteil (rechts neben der Dezimalstelle) zählt die Zeit als einen Bruchteil des Tages. Zum Beispiel wäre der 1. Januar 1900 mittags 2,5, 2 weil es 2 Tage nach dem 30. Dezember 1899 ist, und .5 weil mittags ein halber Tag ist. 1. Februar 1900 um 15 Uhr wäre 33.625 Uhr. Damit wird das Jahr 1900 korrekt als Schaltjahr behandelt.</p></li><li> <p style="font-weight: bold;">[!DNL Formatted string]</p> <p>Die Felder für Datum, Uhrzeit, Datum/Uhrzeit und Dauer werden als Zeichenfolgen im angegebenen Zahlenformat ausgegeben (das vom Gebietsschema der Tabelle abhängt).</p> </li><ul></td> 
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
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Google Sheets-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://sheets.googleapis.com/v4/</code> ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Methode]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Beispiel: <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p> Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:   <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Zelle aktualisieren]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie die Tabelle aus, in der Sie eine Zelle aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zelle] </td> 
   <td> <p>Geben Sie die ID der Zelle ein, die Sie aktualisieren möchten. Beispiel: <code>A5</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Wert]</td> 
   <td> <p>Geben Sie den neuen Wert für die Zelle ein.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Werteingabeoption]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Benutzer entered]</strong></p> <p>Die Werte werden analysiert, als ob der Benutzer sie in die Benutzeroberfläche eingegeben hätte. Zahlen bleiben Zahlen, Zeichenfolgen können jedoch nach denselben Regeln, die bei der Eingabe von Text in eine Zelle über die [!DNL Google Sheets]-Benutzeroberfläche angewendet werden, in Zahlen, Daten oder andere Formate konvertiert werden.</p> </li> 
     <li> <p><strong>[!UICONTROL RAW]</strong> </p> <p> Die vom Benutzer eingegebenen Werte werden nicht geparst und so gespeichert, wie sie eingegeben wurden. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Zeile aktualisieren]

Mit diesem Modul können Sie den Zelleninhalt in einer ausgewählten Zeile ändern.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Modus]</td> 
   <td> <p>Wählen Sie aus, ob Sie die Tabelle und das Blatt manuell oder durch Zuordnung auswählen möchten.</p> <p>Hinweis: Die manuelle Zuordnung ist beispielsweise dann nützlich, wenn im Szenario [!UICONTROL Workfront Fusion] eine neue Tabelle erstellt wird und Sie der neu erstellten Tabelle direkt im Szenario Daten hinzufügen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, in dem Sie eine Zeile aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zeilennummer]</td> 
   <td> <p> Geben Sie die Nummer der Zeile ein, die Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tabelle enthält Kopfzeilen]</td> 
   <td> <p> Wählen Sie aus, ob das Arbeitsblatt die Kopfzeile enthält.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>Das Modul ruft die Kopfzeile nicht als Ausgabedaten ab. </p> <p>Variablennamen in der Ausgabe werden von den Kopfzeilen aufgerufen.</p> </li> 
     <li> <p><strong>[!UICONTROL Nein]</strong> </p> <p>Das Modul ruft auch die erste Tabellenzeile ab</p> <p>Variablennamen in der Ausgabe werden als A, B, C, D usw. bezeichnet.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Werte] </td> 
   <td> <p>Geben Sie die Werte in die gewünschten Zellen der Zeile ein, die Sie ändern (aktualisieren) möchten, oder ordnen Sie sie ihnen zu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Werteingabeoption]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Benutzer entered]</strong></p> <p>Die Werte werden analysiert, als ob der Benutzer sie in die Benutzeroberfläche eingegeben hätte. Zahlen bleiben Zahlen, Zeichenfolgen können jedoch nach denselben Regeln, die bei der Eingabe von Text in eine Zelle über die [!DNL Google Sheets]-Benutzeroberfläche angewendet werden, in Zahlen, Daten oder andere Formate konvertiert werden.</p> </li> 
     <li> <p><strong>[!UICONTROL RAW]</strong> </p> <p> Die vom Benutzer eingegebenen Werte werden nicht geparst und so gespeichert, wie sie eingegeben wurden. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL Bereichswerte abrufen]](#get-range-values)
* [[!UICONTROL Arbeitsblätter auflisten]](#list-sheets)
* [[!UICONTROL Zeilen suchen]](#search-rows)
* [[!UICONTROL Suchzeilen (erweitert)]](#search-rows-advanced)

#### [!UICONTROL Bereichswerte abrufen]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie die Tabelle aus, aus der Sie den Bereichsinhalt abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Bereich] </td> 
   <td> <p>Geben Sie den Bereich ein, den Sie erhalten möchten. Beispiel: <code>A1:D25</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tabelle enthält Kopfzeilen]</td> 
   <td> <p>Aktivieren Sie dieses Kontrollkästchen, wenn das Blatt eine Kopfzeile hat</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zeile mit Überschriften]</td> 
   <td>Geben Sie den Bereich der Tabellenüberschriften ein. Beispiel <code>A1:F1</code>. Wenn Sie das Feld leer lassen, behandelt [!DNL Workfront Fusion] die erste Zeile des angegebenen Bereichs als Kopfzeile.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Wert renderoption]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL formatierter Wert]</p> <p>Die Werte werden in der Antwort entsprechend der Zellenformatierung berechnet und formatiert. Die Formatierung basiert auf dem Gebietsschema der Tabelle, nicht auf dem Gebietsschema des anfragenden Benutzers. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"$1.23"</code> zurück.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Unformatierter Wert]</p> <p>Die Werte werden berechnet, in der Antwort jedoch nicht formatiert. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> die Zahl <code>"1.23"</code> zurück.</p></li><li> <p style="font-weight: bold;">[!UICONTROL -Formel]</p> <p>Die Werte werden nicht berechnet. Die Antwort enthält die Formeln. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"=A1"</code> zurück.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Render-Option Datum und Uhrzeit]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL Seriennummer]</p> <p>Die Felder „Datum“, „Uhrzeit“, „Datum/Uhrzeit“ und „Dauer“ werden als Dubletten im Format „Seriennummer“ ausgegeben, wie es von Lotus 1-2-3 populär gemacht wird. Der ganze Zahlenteil des Werts (links vom Dezimaltrennzeichen) zählt die Tage seit dem 30. Dezember 1899. Der Bruchteil (rechts neben der Dezimalstelle) zählt die Zeit als einen Bruchteil des Tages. Zum Beispiel wäre der 1. Januar 1900 mittags 2,5, 2 weil es 2 Tage nach dem 30. Dezember 1899 ist, und .5 weil mittags ein halber Tag ist. 1. Februar 1900 um 15 Uhr wäre 33.625 Uhr. Damit wird das Jahr 1900 korrekt als Schaltjahr behandelt.</p> </li><li><p style="font-weight: bold;">[!UICONTROL formatierter String]</p> <p>Die Felder für Datum, Uhrzeit, Datum/Uhrzeit und Dauer werden als Zeichenfolgen im angegebenen Zahlenformat ausgegeben (das vom Gebietsschema der Tabelle abhängt).</p></li><ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Arbeitsblätter auflisten]

Dieses Modul gibt eine Liste aller Blätter in einer Tabelle zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus, die die Tabellen enthält, die Sie auflisten möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Zeilen suchen]

Durchsucht Zeilen mithilfe der Filteroptionen.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Google Sheets-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung zu [!DNL Adobe Workfront Fusion] herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie die [!DNL Google] Tabelle aus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, in dem Sie die Zeilen durchsuchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tabelle enthält Kopfzeilen]</td> 
   <td> <p> Wählen Sie aus, ob das Arbeitsblatt die Kopfzeile enthält. Wenn die Option [!UICONTROL Yes] ausgewählt ist, ruft das Modul die Kopfzeile nicht ab, da die Ausgabedaten und Variablennamen in der Ausgabe von den Kopfzeilen aufgerufen werden. Wenn die Option [!UICONTROL No] ausgewählt ist, ruft das Modul auch die erste Tabellenzeile ab, und die Variablennamen in der Ausgabe werden nur A, B, C, D usw. genannt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spaltenbereich]</td> 
   <td>Wählen Sie den Spaltenbereich aus, mit dem Sie arbeiten möchten. Beispiel: <code>A-F</code></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL filter]</td> 
   <td> <p>Legen Sie den Filter fest, den Sie zum Suchen nach Zeilen verwenden möchten.</p> <!--<p>For more information about filters, see <a href="/help/workfront-fusion/create-scenarios/add-modules/" class="MCXref xref">Add a filter to a scenario in [!UICONTROL Adobe Workfront Fusion]</a>.</p>--> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sortierreihenfolge]</td> 
   <td>Wählen Sie aus, ob auf- oder absteigend sortiert werden soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sortieren nach]</td> 
   <td>Wählen Sie die Spalte aus, nach der Sie sortieren möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Wert renderoption]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL formatierter Wert]</p> <p>Die Werte werden in der Antwort entsprechend der Zellenformatierung berechnet und formatiert. Die Formatierung basiert auf dem Gebietsschema der Tabelle, nicht auf dem Gebietsschema des anfragenden Benutzers. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"$1.23"</code> zurück.</p></li><li> <p style="font-weight: bold;">[!UICONTROL Unformatierter Wert]</p> <p>Die Werte werden berechnet, in der Antwort jedoch nicht formatiert. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> die Zahl <code>"1.23"</code> zurück.</p></li><li> <p style="font-weight: bold;">[!UICONTROL -Formel]</p> <p>Die Werte werden nicht berechnet. Die Antwort enthält die Formeln. Wenn <code>A1</code> beispielsweise <code>1.23</code> ist und <code>A2</code> als Währung <code>=A1</code> und formatiert ist, gibt <code>A2</code> <code>"=A1"</code> zurück.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Render-Option Datum und Uhrzeit]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL Seriennummer]</p> <p>Die Felder „Datum“, „Uhrzeit“, „Datum/Uhrzeit“ und „Dauer“ werden als Dubletten im Format „Seriennummer“ ausgegeben, wie es von Lotus 1-2-3 populär gemacht wird. Der ganze Zahlenteil des Werts (links vom Dezimaltrennzeichen) zählt die Tage seit dem 30. Dezember 1899. Der Bruchteil (rechts neben der Dezimalstelle) zählt die Zeit als einen Bruchteil des Tages. Zum Beispiel wäre der 1. Januar 1900 mittags 2,5, 2 weil es 2 Tage nach dem 30. Dezember 1899 ist, und .5 weil mittags ein halber Tag ist. 1. Februar 1900 um 15 Uhr wäre 33.625 Uhr. Damit wird das Jahr 1900 korrekt als Schaltjahr behandelt.</p> </li><li><p style="font-weight: bold;">[!UICONTROL formatierter String]</p> <p>Die Felder für Datum, Uhrzeit, Datum/Uhrzeit und Dauer werden als Zeichenfolgen im angegebenen Zahlenformat ausgegeben (das vom Gebietsschema der Tabelle abhängt).</p></li><ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximale Anzahl der zurückgegebenen Zeilen]</td> 
   <td>Legen Sie die maximale Anzahl von Zeilen fest, die [!DNL Workfront Fusion] während eines Ausführungszyklus zurückgeben.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Suchzeilen (erweitert)]

Gibt Ergebnisse zurück, die den angegebenen Kriterien entsprechen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Google Sheets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Tabelle] </td> 
   <td> <p>Wählen Sie das Google-Arbeitsblatt aus, das das zu durchsuchende Arbeitsblatt enthält.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Wählen Sie das Blatt aus, das die Zeilen enthält, nach denen Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Abfrage]</td> 
   <td> <p>Verwenden Sie die [!DNL Google Charts Query Language]. Beispiel: <code>select * where B = "John"</code></p> <p>Weitere Informationen zu [!DNL Google Charts Query Language] finden Sie unter <a href="https://developers.google.com/chart/interactive/docs/querylanguage">Abfrage-</a>" in der [!DNL Google].</p> </td> 
  </tr> 
 </tbody> 
</table>

## Nutzungsbeschränkungen

Wenn der `429: RESOURCE_EXHAUSTED` auftritt, haben Sie das API-Ratenlimit überschritten.

Die [!DNL Google Sheets]-API begrenzt 500 Anfragen pro 100 Sekunden pro Projekt und 100 Anfragen pro 100 Sekunden pro Benutzer. Beschränkungen für Lese- und Schreibvorgänge werden separat verfolgt. Es gibt keine tägliche Nutzungsbeschränkung.

Weitere Informationen finden Sie unter [developers.google.com/sheets/api/limits](https://developers.google.com/sheets/api/limits).

## Tipps und Tricks

* [Leere Zellen aus einem  [!DNL Google]  abrufen](#get-empty-cells-from-a-google-sheet)
* [Schaltfläche in einem Blatt hinzufügen, um ein Szenario auszuführen](#add-a-button-in-a-sheet-to-run-a-scenario)

### Leere Zellen aus einer [!DNL Google Sheet] abrufen

Um leere Zellen zu erhalten, können Sie das Modul [!UICONTROL Zeilen suchen (Erweitert)] verwenden. Verwenden Sie diese Formel, um leere Spalten abzurufen.

```
select * where E is null
```

Dabei ist „E“ die Spalte und „ist null“ die Bedingung. Sie können eine erweiterte Abfrage mithilfe der Google-Abfragesprache erstellen. Weitere Informationen finden Sie unter [Google Query Lang](https://developers.google.com/chart/interactive/docs/querylanguage) in der Google-Dokumentation.

### Schaltfläche in einem Blatt hinzufügen, um ein Szenario auszuführen

1. Fügen Sie [!DNL Workfront Fusion] das Modul **[!UICONTROL Webhook]** > **[!UICONTROL Custom Webhooks]** in das Szenario ein und konfigurieren Sie es. Anweisungen finden Sie unter [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

1. Kopieren Sie die URL des Webhooks.
1. Führen Sie das Szenario aus.
1. Wählen Sie in Google Sheets **[!UICONTROL Einfügen]** > **[!UICONTROL Zeichnen]**… aus der Hauptmenüleiste aus.

1. Klicken Sie [!UICONTROL &#x200B; Fenster &#x200B;]Zeichnung“ auf das Symbol **[!UICONTROL Textfeld]** (![Textfeld](/help/workfront-fusion/references/apps-and-modules/assets/text-box.png) oben im Fenster.
1. Entwerfen Sie eine Schaltfläche und klicken Sie auf **[!UICONTROL Schaltfläche „Speichern und]**&quot; in der oberen rechten Ecke:
1. Die Schaltfläche wird in Ihrem Arbeitsblatt platziert. Klicken Sie auf die drei vertikalen Punkte in der oberen rechten Ecke der Schaltfläche:
1. Wählen Sie **[!UICONTROL Skript zuweisen..].** aus dem Menü.
1. Geben Sie den Namen Ihres Skripts (Funktion) ein, z. B. `runScenario`, und klicken Sie auf **[!UICONTROL OK]**:
1. Wählen Sie **[!UICONTROL Tools]** > **[!UICONTROL Skript-]**) in der Hauptmenüleiste aus.

1. Fügen Sie den folgenden Code ein:

   * Der Name der Funktion muss dem in Schritt 9 angegebenen Namen entsprechen.
   * Ersetzen Sie die URL durch die URL des Webhooks, die Sie in Schritt 2 kopiert haben.

     ```
     function runScenario() {
     UrlFetchApp.fetch("&lt;webhook you copied>");
     }
     ```

1. Drücken Sie **[!UICONTROL Strg+S]**, um die Skriptdatei zu speichern, geben Sie einen Projektnamen ein und klicken Sie auf **[!UICONTROL OK]**.

1. Wechseln Sie zurück zu [!DNL Google Sheets] und klicken Sie auf Ihre neue Schaltfläche.
1. Gewähren Sie dem Skript die erforderliche Autorisierung:
1. Überprüfen Sie [!DNL Workfront Fusion], ob das Szenario erfolgreich ausgeführt wurde.

## Daten in einer Tabelle speichern

Wenn Sie einen Datumswert ohne Formatierung in einer Tabelle speichern, wird er in der Tabelle als Text im ISO 8601-Format angezeigt. [!DNL Google Sheets] Formeln oder Funktionen, die mit Datumsangaben arbeiten, die diesen Text nicht verstehen (Beispiel: Formel `=A1+10`), zeigen jedoch den folgenden Fehler an:

![Fehler](/help/workfront-fusion/references/apps-and-modules/assets/mceclip6-350x87.png)

Damit [!DNL Google Sheets] das Datum besser verstehen können, formatieren Sie es mit der Funktion `formatDate` . Das richtige Format, das als zweites Argument an die Funktion übergeben wird, hängt von den Gebietsschemaeinstellungen der Tabelle ab.

Weitere Informationen zu dieser Funktion finden Sie unter [[!UICONTROL formatDate] (Datum; Format; [Zeitzone])](/help/workfront-fusion/references/mapping-panel/functions/date-and-time-functions.md#formatdate-date-format-timezone) im Artikel Datums- und Uhrzeitfunktionen.

So bestimmen Sie das richtige Format:

1. Wählen Sie in Google Sheets **[!UICONTROL Datei]** > **[!UICONTROL Tabelle]** Einstellungen aus dem Hauptmenü aus, um das Gebietsschema zu überprüfen und festzulegen.

1. Nachdem Sie das richtige Gebietsschema überprüft oder festgelegt haben, bestimmen Sie das entsprechende Datums- und Uhrzeitformat, indem Sie **[!UICONTROL Format]** > **[!UICONTROL Number]** aus dem Hauptmenü auswählen. Das Format wird neben dem Datums-/Uhrzeitmenüpunkt angezeigt:

1. Um das richtige Format zu erstellen, das an die Funktion [!UICONTROL formatDate()] übergeben werden soll, lesen Sie die Liste der [Token zur Datums- und Zeitformatierung](/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md).

>[!BEGINSHADEBOX]

**Beispiel:**

Für `MM/DD/YYYY HH:mm:ss` Format (für das Gebietsschema der Vereinigten Staaten):

![Gebietsschema-Zeitformel](/help/workfront-fusion/references/apps-and-modules/assets/locale-time-350x83.png)

>[!ENDSHADEBOX]

## Nutzung [!DNL Google Sheets] Funktionen

Um eine integrierte Funktion aus Google Sheets zu verwenden, können Sie sie nutzen. Weitere Informationen finden Sie unter [Verwenden [!DNL Google Sheets] Funktionen](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md#use-google-sheets-functions) im Artikel Zuordnen eines Elements mithilfe von Funktionen.

## Verhindern, dass [!DNL Google Sheets] Zahlen in Daten ändern

Wenn eine Zeichenfolge von Zahlen, die Sie als Text verwenden, in einem [!DNL Google] Arbeitsblatt als Datum interpretiert wird, können Sie die Zahl als einfachen Text vorformatieren, um dies zu verhindern. Wenn Sie beispielsweise 1-2019 eingeben und als Text beabsichtigen, interpretiert Google dies möglicherweise als Datum.

1. Markieren Sie [!DNL Google Sheets] die Spalte oder Zelle, die die Zahl oder die Zahlen enthält.
1. Klicken Sie auf **[!UICONTROL Format]** > **[!UICONTROL Zahl]** > **[!UICONTROL Nur Text]**.

Eine weitere Problemumgehung in [!DNL Workfront Fusion] besteht darin, vor einer Zahl ein Apostroph (&#39;) einzugeben, z. B. &#39;1-2019 oder &#39;1/47. Das Apostroph wird in der Zelle nicht angezeigt, nachdem die Daten von [!DNL Workfront Fusion] gesendet wurden.
