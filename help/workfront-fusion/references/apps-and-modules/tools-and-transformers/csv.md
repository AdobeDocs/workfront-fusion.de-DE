---
title: CSV
description: Mit den CSV-Modulen von Adobe Workfront Fusion können Sie CSV-Dateien erstellen und CSV-Text aus einem empfangenen Textwert oder einer Datei analysieren.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 0%

---

# CSV

Mit den Adobe Workfront Fusion [!UICONTROL CSV]-Modulen können Sie CSV-Dateien erstellen und CSV-Text aus einem empfangenen Textwert oder einer Datei analysieren.

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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## [!UICONTROL CSV erstellen]

Mit [!UICONTROL &#x200B; Aggregator „CSV erstellen] können Sie CSV-Text aus empfangenen Textwerten erstellen.

Weitere Informationen zu Aggregatoren finden Sie unter [Aggregatormodul](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source-Modul]</td>
        <td>Wählen Sie das Modul aus, das die Felder ausgibt, die Sie zum Erstellen der CSV-Datei verwenden möchten.</td>
    </tr>
    <tr>
        <td>[!UICONTROL aggregierte Felder]</td>
        <td>Wählen Sie die Felder, die Sie aggregieren möchten, aus der Liste der verfügbaren Felder aus.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Kopfzeilen in die erste Zeile einfügen]</td>
        <td>Wählen Sie diese Option, um die Kopfzeilen in das Ergebnis aufzunehmen.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Gruppieren nach]</td>
        <td>Geben Sie den Filter ein, um die Ergebnisse zu gruppieren. Geben Sie beispielsweise ein Datum ein.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Verarbeitung nach einer leeren Aggregation anhalten]</td>
        <td>Wählen Sie diese Option, um das Szenario anzuhalten, wenn keine Ergebnisse vorliegen.</td>
    </tr>
</table>

## [!UICONTROL CSV erstellen (erweitert)]

Mit [!UICONTROL &#x200B; Aggregator CSV erstellen (erweitert] können Sie CSV-Text aus empfangenen Textwerten erstellen. Sie verwendet eine Datenstruktur, die die CSV-Spalten in der resultierenden CSV-Datei definiert. Nach der Definition erscheinen die Spalten als Felder bei der Einrichtung des CSV-Moduls und können einem späteren Modul im Szenario zugeordnet werden.

Weitere Informationen zu Aggregatoren finden Sie unter [Aggregatormodul](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Modul]</td> 
        <td>Wählen Sie das Modul aus, das die Felder ausgibt, die Sie zum Erstellen der CSV-Datei verwenden möchten.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Datenstruktur]</td> 
   <td> <p>Wählen Sie die Datenstruktur aus, um die Felder wie gewünscht zu aggregieren. Nachdem Sie die Datenstruktur definiert haben, können Sie die Elemente den entsprechenden Feldern zuordnen.</p> <p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Datenstrukturen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kopfzeilen in die erste Zeile einfügen] </td> 
   <td>Wählen Sie diese Option, um die Kopfzeilen in das Ergebnis aufzunehmen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Gruppieren nach] </td> 
   <td>Geben Sie den Filter ein, um die Ergebnisse zu gruppieren. Geben Sie beispielsweise ein Datum ein. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verarbeitung nach einer leeren Aggregation anhalten] </td> 
   <td>Wählen Sie diese Option, um das Szenario anzuhalten, wenn keine Ergebnisse vorliegen. </td> 
  </tr> 
 </tbody> 
</table>


>[!BEGINSHADEBOX]

**Beispiel**:

Dieses Beispiel zeigt, wie Google-Kontakte in eine CSV-Datei mit zwei Spalten namens „Vollständiger Name“ und „E-Mail“ exportiert werden. Das Ausgabepaket des Moduls [!UICONTROL Google-] > [!UICONTROL Kontakte aus einer Gruppe abrufen] weist die folgende Struktur auf. Die E-Mail-Adressen werden in den <code>[!UICONTROL E-Mails[]]</code> item: ein Array von Sammlungen, wobei jede Sammlung zwei Elemente enthält: <code>label</code> und <code>E-Mail</code>.
![Transformieren](/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png)

Das Modul Einfache [!DNL Create CSV] bietet eine Liste von Kontrollkästchen, die den Elementen auf der obersten Ebene eines Bundles entsprechen. Wenn Sie versuchen, „Vollständiger Name<code> auszuwählen,</code> und <code>Emails</code> für Elemente erzeugt [!UICONTROL &#x200B; Modul &#x200B;]CSV erstellen) die folgende Ausgabe, die möglicherweise nicht das ist, was Sie möchten:

```
"emails","fullName"
"[object Object]","Shon Winer"
"[object Object]","Lizeth Fulmore"
"[object Object]","Hilario Gullatt"
"[object Object]","Abby Eisenbarth"
```

Weil das Element <code>Vollständiger Name</code> vom einfachen Typ Text ist, wird er erwartungsgemäß exportiert. Das Element <code>E-Mails</code>, einem komplexen Array von Sammlungen, wird als [Objekt) exportiert, ] wie Sammlungen und Arrays standardmäßig in Text umgewandelt werden.

Weitere Informationen finden Sie unter [Elementdatentypen](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).


So exportieren Sie den Inhalt der <code>E-Mail </code>Element der ersten Sammlung der <code>E-Mails[]</code> -Array verwenden, müssen Sie stattdessen das Modul [!UICONTROL CSV erstellen (erweitert] verwenden. Mit diesem Modul können Sie einzelne Spalten Ihrer CSV-Datei definieren und ihnen Elemente zuordnen, einschließlich der verschachtelten.

1. Fügen Sie das Modul [!UICONTROL CSV erstellen (erweitert] in ein Szenario ein.
1. Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong>-Schaltfläche neben dem Feld [!UICONTROL Datenstruktur], um eine neue Datenstruktur zu erstellen.
1. Geben Sie einen Namen für die Datenstruktur ein und klicken Sie auf <strong>[!UICONTROL Element hinzufügen]</strong>, um die einzelnen Spalten hinzuzufügen. Beim Exportieren von zwei Spalten: „Vollständiger Name“ und „E-Mail“ würde die resultierende Datenstruktur wie folgt aussehen:

   ![Ausgabe von Google-Kontakten](/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png)

1. Nachdem Sie die Datenstruktur definiert haben, werden die Felder, die den einzelnen Spalten entsprechen, in der Konfiguration des Moduls [!UICONTROL CSV erstellen (erweitert)] angezeigt, damit Sie die Elemente zuordnen können. Nehmen Sie den ersten Artikel aus dem <code>[!UICONTROL E-Mails[]]</code> Array und Zuordnen seines Elements <code>E-Mail </code>in das Feld/die Spalte E-Mail:

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

## [!UICONTROL CSV analysieren]

Der [!UICONTROL CSV parsen]-Transformer ermöglicht das Analysieren von CSV-Text aus einem empfangenen Textwert oder einer Datei.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anzahl der Spalten]</td> 
   <td>Geben Sie die Anzahl der Spalten in der CSV-Datei an.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV enthält Kopfzeilen]</td> 
   <td> <p>Wählen Sie diese Option, wenn die erste Zeile des CSV-Texts Kopfzeilen enthält.</p> <p>Hinweis: Das Modul verwendet diese Kopfzeilen nicht zur Beschriftung der Spalten in der Ausgabe. Stattdessen stellt dieses Feld sicher, dass die -Kopfzeilen nicht in den Ausgabedaten enthalten sind.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL delimiterType]</td> 
   <td> <p>Trennzeichen für die CSV-Datei auswählen. Das Trennzeichen ist das Textzeichen, das die Grenze zwischen separaten Werten oder Feldern angibt.</p> 
    <ul> 
     <li>[!UICONTROL Komma]</li> 
     <li>[!UICONTROL tab]</li> 
     <li> <p>[!UICONTROL Sonstige]</p> <p>Wenn Sie [!UICONTROL Other] auswählen, geben Sie das Trennzeichen ein, das die CSV-Datei zum Trennen der Werte verwendet. Sie müssen genau ein Zeichen eingeben.<br></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anführungszeichen in nicht angeführten Feldern beibehalten]</td> 
   <td>Aktivieren Sie diese Option, um Anführungszeichen beizubehalten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV]</td> 
   <td>Geben Sie die CSV-Datei ein, die Sie parsen möchten, oder mappen Sie sie.<p>Hinweis: <p>Wenn Ihre Daten in binärer Form vorliegen (normalerweise aus einer Datei), müssen Sie die Funktion „toString()“ verwenden, um die Binärdaten in [!UICONTROL String] zu konvertieren:</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png"></p></p></td> 
  </tr> 
 </tbody> 
</table>
