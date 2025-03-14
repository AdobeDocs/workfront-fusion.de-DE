---
title: JSON-Module
description: Die Adobe Workfront Fusion-JSON-App bietet Module zur Verarbeitung von Daten im JSON-Format, damit Adobe Workfront Fusion weiter mit den Dateninhalten arbeiten oder neue JSON-Inhalte erstellen kann.
author: Becky
feature: Workfront Fusion
exl-id: f8b281c5-bb63-4412-98c5-d82f45f8eafc
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# [!UICONTROL JSON]-Module

Die [!DNL Adobe Workfront Fusion] [!UICONTROL JSON]-App bietet Module zur Verarbeitung von Daten im JSON-Format, damit [!DNL Adobe Workfront Fusion] weiter mit den Dateninhalten arbeiten oder neue JSON-Inhalte erstellen können.

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

## Überlegungen beim Analysieren von JSON

* [Datenstruktur](#data-structure)
* [Sammlung vs. Array](#collection-vs-array)

### Datenstruktur

Die Datenstruktur beschreibt, wie die JSON-Daten organisiert sind, und ermöglicht die Zuordnung einzelner JSON-Elemente zu anderen Modulen in Ihrem Szenario. Wenn Sie die Datenstruktur nicht bereitstellen, können Sie das Modul manuell ausführen und [!DNL Workfront Fusion] die Struktur aus der bereitgestellten JSON-Datei erstellen:

1. Fügen Sie das [!UICONTROL Parse JSON]-Modul zu einem Szenario hinzu.
1. Geben Sie im Feld **[!UICONTROL JSON]** Zeichenfolge“ die JSON-Datei ein, aus der Sie eine Datenstruktur erstellen möchten.
1. Verbinden Sie noch keine anderen Module mit dem [!UICONTROL Parse JSON]-Modul. Da [!DNL Workfront Fusion] die Struktur der JSON-Daten noch nicht kennt, ist es noch nicht möglich, Daten aus dem Modul [!UICONTROL JSON analysieren] anderen Modulen in Ihrem Szenario zuzuordnen.
1. Führen Sie das Szenario manuell aus. Dadurch kann das [!UICONTROL Parse JSON]-Modul die JSON-Struktur aus der von Ihnen bereitgestellten JSON identifizieren.
1. Sie können jetzt folgende Module verbinden. Die Elemente aus dem Parse-JSON-Modul sind jetzt für die Zuordnung verfügbar.

Weitere Informationen finden Sie unter [Datenstrukturen in [!UICONTROL Adobe Workfront Fusion]](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

### Sammlung vs. Array

Wenn das JSON-Zeichenfolgenfeld einen Sammlungscode `{ ... }`, ist die Ausgabe ein einzelnes Bundle, das die Elemente der Sammlung enthält.

>[!BEGINSHADEBOX]

**Beispiel:**

```
{
    "name" : "Peter",

    "ID" : 1>}
```


![JSON-Sammlung](/help/workfront-fusion/references/apps-and-modules/assets/json-collection.png)

>[!ENDSHADEBOX]

Wenn das JSON-Zeichenfolgenfeld ein Array-`[ ... ]` enthält, ist die Ausgabe eine Reihe von Bundles. Jedes Bundle enthält ein Element des Arrays.

>[!BEGINSHADEBOX]

**Beispiel:**

```
[
  {
    "name" : "Peter",
    "ID" : 1
  },

  {
    "name" : "Mike",
    "ID" : 2
  }
]
```

![JSON-Array](/help/workfront-fusion/references/apps-and-modules/assets/json-array.png)

>[!ENDSHADEBOX]

## [!UICONTROL JSON]-Module und ihre Felder

Beim Konfigurieren [!DNL JSON] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können je nach Faktoren wie Ihrer Zugriffsebene in der App oder im Service weitere JSON-Felder angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Konvertieren von JSON in XML](#convert-json-to-xml)
* [JSON analysieren](#parse-json)
* [JSON erstellen](#create-json)
* [JSON transformieren](#transform-json)

### Aggregatoren

#### [!UICONTROL Aggregieren in JSON]

Dieses Aggregator-Modul aggregiert die Ausgabe eines vorherigen Moduls in JSON.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Modul] </td> 
   <td> <p>Wählen Sie das Modul aus, das die Daten ausgibt, die Sie in JSON aggregieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Datenstruktur]</td> 
   <td> <p>Wählen Sie die Datenstruktur aus, die Sie zum Erstellen von JSON verwenden möchten. Die Datenstruktur bestimmt, welche anderen Felder in diesem Modul verfügbar sind. Weitere Informationen finden Sie unter <a href="#data-structure" class="MCXref xref">Datenstruktur</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Einzug]</td> 
   <td> <p> Wählen Sie aus, ob Sie die JSON-Datei mithilfe von Registerkarten, zwei Leerzeichen oder vier Leerzeichen einrücken möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Gruppieren nach]</td> 
   <td>Definieren Sie einen Ausdruck, nach dem die aggregierte Ausgabe gruppiert werden soll. Dieser Ausdruck kann ein oder mehrere zugeordnete Elemente enthalten. Die aggregierten Daten werden dann mithilfe des -Werts dieses Ausdrucks in Gruppen aufgeteilt. Jede Gruppe gibt als separates Bundle mit einem Schlüssel (dem ausgewerteten Ausdruck) und einem Wert (dem aggregierten Text) aus. Sie können den Schlüssel als Filter in nachfolgenden Modulen verwenden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verarbeitung nach einer leeren Aggregation anhalten]</td> 
   <td>Aktivieren Sie diese Option, um das Szenario zu stoppen, wenn keine Ergebnisse vorliegen.</td> 
  </tr> 
 </tbody> 
</table>

### Transformatoren

* [Konvertieren von JSON in XML](#convert-json-to-xml)
* [JSON erstellen](#create-json)
* [JSON analysieren](#parse-json)
* [JSON transformieren](#transform-json)

#### [!UICONTROL Konvertieren von JSON in XML]

Dieses Aktionsmodul konvertiert eine JSON-Zeichenfolge in XML.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON-Zeichenfolge] </td> 
   <td> <p>Geben Sie die JSON-Datei ein, die Sie in XML konvertieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL JSON erstellen]

Dieses Aktionsmodul erstellt JSON aus einer Datenstruktur.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Datenstruktur</td> 
   <td> <p>Wählen Sie die Datenstruktur aus, die Sie zum Erstellen von JSON verwenden möchten. Weitere Informationen finden Sie unter <a href="#data-structure" class="MCXref xref">Datenstruktur</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Einzug</td> 
   <td> <p>Wählen Sie die Einrückung aus, die Sie für diese JSON-Datei verwenden möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL JSON analysieren]

Dieses Aktionsmodul analysiert eine JSON-Zeichenfolge in eine Datenstruktur, mit der Sie auf die Daten in der JSON-Zeichenfolge zugreifen können.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Datenstruktur]</td> 
   <td> <p>Wählen Sie die Datenstruktur aus, die Sie zum Erstellen von JSON verwenden möchten. Weitere Informationen finden Sie unter <a href="#data-structure" class="MCXref xref">Datenstruktur</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON-Zeichenfolge] </td> 
   <td> <p>Geben Sie die JSON ein, die Sie parsen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL JSON transformieren]

Dieses Aktionsmodul wandelt ein -Objekt in eine JSON-Zeichenfolge um.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Einzug</td> 
   <td> <p>Wählen Sie die Einrückung aus, die Sie für diese JSON-Datei verwenden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Objekt]</td> 
   <td> <p>Geben Sie das Objekt ein, das Sie in JSON umwandeln möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Umwandeln von Datensätzen in JSON

>[!BEGINSHADEBOX]

**Beispiel:** Das folgende Beispiel zeigt, wie Datensätze von [!DNL Google Sheets] in das JSON-Format umgewandelt werden:

1. Platzieren Sie das Modul [!DNL Google Sheets] > [!UICONTROL Zeilen auswählen] in Ihrem Szenario, um die Daten abzurufen. Richten Sie das -Modul ein, um Zeilen aus Ihrer [!DNL Google] Tabelle abzurufen. Legen Sie &#x200B;**[!UICONTROL Maximale Anzahl der zurückgegebenen Zeilen]** auf eine kleine Anzahl fest, die zu Testzwecken jedoch größer als 1 ist (z. B. drei). Führen Sie das [!DNL Google Sheets] Modul aus, indem Sie mit der rechten Maustaste darauf klicken und &quot;**[!UICONTROL Nur dieses Modul ausführen]** auswählen. Überprüfen Sie die Ausgabe des Moduls.

1. Verbinden Sie das [!UICONTROL Array Aggregator]-Modul nach dem [!DNL Google Sheets]. Wählen Sie im Setup des Moduls das [!DNL Google Sheets] im Feld **[!UICONTROL Source-Knoten]** aus. Lassen Sie die anderen Felder so, wie sie für den Moment sind.

1. Verbinden Sie [!UICONTROL JSON] > [!UICONTROL JSON erstellen]-Modul nach dem [!UICONTROL Array Aggregator]-Modul. Die Einrichtung des Moduls erfordert eine Datenstruktur, die das JSON-Format beschreibt. Klicken Sie **[!UICONTROL Hinzufügen]**, um die Einrichtung der Datenstruktur zu öffnen. Die einfachste Möglichkeit, diese Datenstruktur zu erstellen, besteht darin, sie automatisch aus einem JSON-Beispiel zu generieren. Klicken Sie auf **[!UICONTROL Generator]** und fügen Sie Ihr JSON-Beispiel in das Feld **[!UICONTROL Beispieldaten]** ein:

   **Beispiel:**

   ```
   {
   "books": [
   {
   "id": "ID",
   "title": "Title",
   "author": "Author"
   }
   ]
   }
   ```

1. Klicken Sie auf **[!UICONTROL Speichern]**. Das [!UICONTROL Spezifikation] in der Datenstruktur enthält jetzt die generierte Struktur.
1. Ändern Sie den Namen Ihrer Datenstruktur in etwas Spezifischeres und klicken Sie auf **[!UICONTROL Speichern]**. Ein Feld, das dem Stamm-Array-Attribut entspricht, wird im Setup des JSON-Moduls als zuordnungsfähiges Feld angezeigt.

1. Klicken Sie auf **[!UICONTROL Map]**-Schaltfläche neben dem Feld und ordnen Sie das `Array[]` aus der Array-Aggregator-Ausgabe zu.

1. Klicken Sie **[!UICONTROL OK]**, um die Einrichtung [!UICONTROL JSON]-Moduls zu schließen.

1. Öffnen Sie das Setup des Moduls [!UICONTROL Array Aggregator]. Ändern Sie die **[!UICONTROL Zielstruktur]** von [!UICONTROL Benutzerdefiniert] in das Feld des [!UICONTROL JSON]-Moduls, das dem Stamm-Array-Attribut entspricht. Ordnen Sie Elemente aus dem [!DNL Google Sheets] den entsprechenden Feldern zu.

1. Klicken Sie **[!UICONTROL OK]**, um die Einrichtung des [!UICONTROL Array Aggregator]-Moduls zu schließen.

1. Führen Sie das Szenario aus.

   Das [!UICONTROL JSON]-Modul gibt das richtige JSON-Format aus.

1. Öffnen Sie die Einrichtung des [!DNL Google Sheets] und erhöhen Sie die [!UICONTROL Maximale Anzahl zurückgegebener Zeilen] um größer als die Anzahl an Zeilen in Ihrer Tabelle zu sein, um alle Daten zu verarbeiten.

>[!ENDSHADEBOX]

## Fehlerbehebung

### Daten aus dem Modul [!UICONTROL JSON analysieren“ können nicht ] werden

Stellen Sie sicher, dass der JSON-Inhalt ordnungsgemäß dem [!UICONTROL Parse JSON]-Modul zugeordnet ist und dass die Datenstruktur korrekt definiert ist. Weitere Informationen finden Sie unter [Umwandeln von Datensätzen in JSON](#transforming-data-records-to-json) in diesem Artikel.

### Modul schlägt bei Verwendung bedingter Anweisungen in JSON fehl

Wenn Sie bedingte Anweisungen wie `if` in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.

>[!BEGINSHADEBOX]

**Beispiel:**

![Anführungszeichen in JSON](/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png)

>[!ENDSHADEBOX]
