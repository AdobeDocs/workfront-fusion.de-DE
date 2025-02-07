---
title: CSV
description: Mit den CSV-Modulen von Adobe Workfront Fusion können Sie CSV-Dateien erstellen und CSV-Text aus einem empfangenen Textwert oder einer Datei analysieren.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: 5971b2210eaac8f8a75fd7a4aac5a9f7954d27ef
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# CSV

Mit den [!DNL Adobe Workfront Fusion] [!UICONTROL CSV] können Sie CSV-Dateien erstellen und CSV-Text aus einem empfangenen Textwert oder einer Datei analysieren.

Da es sich um einen Transformator handelt, ist für diese Module keine Verbindung erforderlich.

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
   <p>Keine Workfront Fusion-Lizenzanforderung</p>
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

## [!UICONTROL Create CSV]

Mit [!UICONTROL Create CSV] Aggregator können Sie CSV-Text aus empfangenen Textwerten erstellen.

Weitere Informationen zu Aggregatoren finden Sie unter [Aggregatormodul](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Wählen Sie das Modul aus, das die Felder ausgibt, die Sie zum Erstellen der CSV-Datei verwenden möchten.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Aggregated Fields]</td>
        <td>Wählen Sie die Felder, die Sie aggregieren möchten, aus der Liste der verfügbaren Felder aus.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Include headers in the first row]</td>
        <td>Wählen Sie diese Option, um die Kopfzeilen in das Ergebnis aufzunehmen.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Group by]</td>
        <td>Geben Sie den Filter ein, um die Ergebnisse zu gruppieren. Geben Sie beispielsweise ein Datum ein.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Stop processing after an empty aggregation]</td>
        <td>Wählen Sie diese Option, um das Szenario anzuhalten, wenn keine Ergebnisse vorliegen.</td>
    </tr>
</table>

## [!UICONTROL Create CSV (advanced)]

Mit [!UICONTROL Create CSV (advanced)] Aggregator können Sie CSV-Text aus empfangenen Textwerten erstellen. Sie verwendet eine Datenstruktur, die die CSV-Spalten in der resultierenden CSV-Datei definiert. Nach der Definition erscheinen die Spalten als Felder bei der Einrichtung des CSV-Moduls und können einem späteren Modul im Szenario zugeordnet werden.

Weitere Informationen zu Aggregatoren finden Sie unter [Aggregatormodul](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
        <td>Wählen Sie das Modul aus, das die Felder ausgibt, die Sie zum Erstellen der CSV-Datei verwenden möchten.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>Wählen Sie die Datenstruktur aus, um die Felder wie gewünscht zu aggregieren. Nachdem Sie die Datenstruktur definiert haben, können Sie die Elemente den entsprechenden Feldern zuordnen.</p> <p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Datenstrukturen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include headers in the first row] </td> 
   <td>Wählen Sie diese Option, um die Kopfzeilen in das Ergebnis aufzunehmen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by] </td> 
   <td>Geben Sie den Filter ein, um die Ergebnisse zu gruppieren. Geben Sie beispielsweise ein Datum ein. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation] </td> 
   <td>Wählen Sie diese Option, um das Szenario anzuhalten, wenn keine Ergebnisse vorliegen. </td> 
  </tr> 
 </tbody> 
</table>


>[!BEGINSHADEBOX]

**Beispiel**:

Dieses Beispiel zeigt, wie Google-Kontakte in eine CSV-Datei mit zwei Spalten namens „Vollständiger Name“ und „E-Mail“ exportiert werden. Das Ausgabepaket aus dem Modul [!UICONTROL Google Contacts] > [!UICONTROL Get contacts from a group] weist die folgende Struktur auf. Die E-Mail-Adressen werden in der <code>[!UICONTROL Emails[]] gespeichert</code> item: ein Array von Sammlungen, wobei jede Sammlung zwei Elemente enthält: <code>label</code> und <code>E-Mail</code>.
![Transformieren](/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png)

Das Modul Einfache [!DNL Create CSV] bietet eine Liste von Kontrollkästchen, die den Elementen auf der obersten Ebene eines Bundles entsprechen. Wenn Sie versuchen, „Vollständiger Name<code> auszuwählen,</code> und <code>Emails</code> -Elementen erzeugt das [!UICONTROL Create CSV]-Modul die folgende Ausgabe, die möglicherweise nicht das ist, was Sie möchten:

```
"emails","fullName"
"[object Object]","Shon Winer"
"[object Object]","Lizeth Fulmore"
"[object Object]","Hilario Gullatt"
"[object Object]","Abby Eisenbarth"
```

Weil das Element <code>Vollständiger Name</code> vom einfachen Typ Text ist, wird er erwartungsgemäß exportiert. Das Element <code>E-Mails</code>, einem komplexen Array von Sammlungen, wird als [Objekt) exportiert, ] wie Sammlungen und Arrays standardmäßig in Text umgewandelt werden.

Weitere Informationen finden Sie unter [Elementdatentypen](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).


So exportieren Sie den Inhalt der <code>E-Mail </code>Element der ersten Sammlung der <code>E-Mails[]</code> -Array verwenden, müssen Sie stattdessen das Modul [!UICONTROL Create CSV (advanced)] verwenden. Mit diesem Modul können Sie einzelne Spalten Ihrer CSV-Datei definieren und ihnen Elemente zuordnen, einschließlich der verschachtelten.

1. Fügen Sie das Modul [!UICONTROL Create CSV (advanced)] in ein Szenario ein.
1. Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Add]</strong> neben dem Feld [!UICONTROL Data structure] , um eine neue Datenstruktur zu erstellen.
1. Geben Sie einen Namen für die Datenstruktur ein und klicken Sie auf <strong>[!UICONTROL Add item]</strong> , um die einzelnen Spalten hinzuzufügen. Beim Exportieren von zwei Spalten: „Vollständiger Name“ und „E-Mail“ würde die resultierende Datenstruktur wie folgt aussehen:

   ![Ausgabe von Google-Kontakten](/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png)

1. Nachdem Sie die Datenstruktur definiert haben, werden Felder, die jeder einzelnen Spalte entsprechen, in der Konfiguration des [!UICONTROL Create CSV (advanced)] angezeigt, damit Sie die Elemente zuordnen können. Nimm das erste Element aus dem <code>[!UICONTROL Emails[]]</code> Array und Zuordnen seines Elements <code>E-Mail </code>in das Feld/die Spalte E-Mail:

   ![CSV erweitertes Modul erstellen](/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png)

1. Führen Sie das Szenario aus. Denn das Element <code>E-Mails[1]: E-Mail</code> der Spalte „E-Mail“ zugeordnet ist, vom einfachen Typ Text ist, wird sie korrekt exportiert.

```
"Full Name","Email"
"Shon Winer","Shon@Winer.com"
"Lizeth Fulmore","Lizeth@Fulmore.com"
"Hilario Gullatt","Hilario@Gullatt.com"
"Abby Eisenbarth","Abby@Eisenbarth.com"
```

>[!ENDSHADEBOX]

## [!UICONTROL Parse CSV]

Mit dem [!UICONTROL Parse CSV]-Transformator können Sie CSV-Text aus einem empfangenen Textwert oder einer Datei analysieren.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of columns]</td> 
   <td>Geben Sie die Anzahl der Spalten in der CSV-Datei an.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV contains headers]</td> 
   <td> <p>Wählen Sie diese Option, wenn die erste Zeile des CSV-Texts Kopfzeilen enthält.</p> <p>Hinweis: Das Modul verwendet diese Kopfzeilen nicht zur Beschriftung der Spalten in der Ausgabe. Stattdessen stellt dieses Feld sicher, dass die -Kopfzeilen nicht in den Ausgabedaten enthalten sind.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL delimiterType]</td> 
   <td> <p>Trennzeichen für die CSV-Datei auswählen. Das Trennzeichen ist das Textzeichen, das die Grenze zwischen separaten Werten oder Feldern angibt.</p> 
    <ul> 
     <li>[!UICONTROL Comma]</li> 
     <li>[!UICONTROL Tab]</li> 
     <li> <p>[!UICONTROL Other]</p> <p>Wenn Sie [!UICONTROL Other] auswählen, geben Sie das Trennzeichen ein, das die CSV-Datei zum Trennen von Werten verwendet. Sie müssen genau ein Zeichen eingeben.<br></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve quotes inside unquoted field]</td> 
   <td>Aktivieren Sie diese Option, um Anführungszeichen beizubehalten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV]</td> 
   <td>Geben Sie die CSV-Datei ein, die Sie parsen möchten, oder mappen Sie sie.<p>Hinweis: <p>Wenn Ihre Daten in binärer Form vorliegen (normalerweise aus einer Datei), müssen Sie die Funktion „toString()“ verwenden, um die Binärdaten in [!UICONTROL String] zu konvertieren:</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png"></p></p></td> 
  </tr> 
 </tbody> 
</table>
