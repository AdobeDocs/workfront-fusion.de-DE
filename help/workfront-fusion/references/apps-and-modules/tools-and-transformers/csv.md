---
title: CSV
description: Mit den CSV-Modulen von Adobe Workfront Fusion können Sie CSV-Dateien erstellen und CSV-Text aus einem empfangenen Textwert oder einer Datei analysieren.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 1%

---

# CSV

Mit den [!DNL Adobe Workfront Fusion] [!UICONTROL CSV] können Sie CSV-Dateien erstellen und CSV-Text aus einem empfangenen Textwert oder einer Datei analysieren.

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
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung und -integration], [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung]</p>
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

## [!UICONTROL Create CSV]

Mit [!UICONTROL Create CSV] Aggregator können Sie CSV-Text aus empfangenen Textwerten erstellen.

Weitere Informationen zu Aggregatoren finden Sie unter [Aggregatormodul](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Wählen Sie das Modul aus, das Sie zum Aggregieren der benötigten Felder verwenden.</td>
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

Weitere Informationen zu Aggregatoren finden Sie unter [Aggregator-Modul in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td>Wählen Sie das App-Modul aus, das Sie verwenden, um die benötigten Felder zu aggregieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>Wählen Sie die Datenstruktur aus, um die Felder wie gewünscht zu aggregieren. Nachdem Sie die Datenstruktur definiert haben, können Sie die Elemente den entsprechenden Feldern zuordnen.</p> <p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Datenstrukturen in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
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


<p>Angenommen, Sie möchten Ihre Google-Kontakte in eine CSV-Datei mit zwei Spalten „Vollständiger Name“ und „E-Mail“ exportieren. Das Ausgabepaket des Moduls [!UICONTROL Google Contacts] &gt;[!UICONTROL Get contacts from a group] weist die folgende Struktur auf. Die E-Mail-Adressen werden im <code>[!UICONTROL Emails[]]</code> gespeichert, einem Array von Sammlungen, wobei jede Sammlung zwei Elemente enthält: <code>Label</code> und <code>Email</code>.</p>
<p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png" style="width: 350;height: 546;"> </p>
<p>Wenn Sie das Modul Einfache [!DNL Create CSV] verwenden, erhalten Sie eine Liste von Kontrollkästchen, die den Elementen auf oberster Ebene eines Pakets entsprechen. Wenn Sie versuchen, <code>Full name</code> und <code>Emails</code> Elemente anzukreuzen, erzeugt das [!UICONTROL Create CSV]-Modul die folgende Ausgabe, die wahrscheinlich nicht das ist, was Sie möchten:</p>
<p>„emails“,„fullName“</p>
<p>"[Objekt]",„Gewinner anzeigen“</p>
<p>"[Objekt]",„Lizeth Fulmore“</p>
<p>"[Objekt]",„Hilario Gullatt“</p>
<p>"[Objekt]",„Abby Eisenbarth“</p>
<p>Da das Element <code>Full Name</code> vom einfachen Typ Text ist, wird es problemlos exportiert. Das Element "<code>Emails</code>", das ein komplexes Array von Sammlungen ist, wird jedoch als [Object Object] exportiert, d. h. wie Sammlungen und Arrays standardmäßig in Text umgewandelt werden. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Elementdatentypen in Adobe Workfront Fusion</a>.</p>
<p>Um stattdessen den Inhalt des <code>Email </code>Elements der ersten Sammlung des <code>Emails[]</code>-Arrays zu exportieren, muss das [!UICONTROL Create CSV (advanced)]-Modul verwendet werden. Mit dem Modul können Sie einzelne Spalten Ihrer CSV-Datei definieren und ihnen Elemente zuordnen, einschließlich der verschachtelten.</p>
<ol>
<li value="1">Fügen Sie die [!UICONTROL Create CSV (advanced)] in ein Szenario ein und öffnen Sie die Konfiguration.</li>
<li value="2">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Add]</strong> neben dem Feld [!UICONTROL Data structure] , um eine neue Datenstruktur zu erstellen.</li>
<li value="3"> <p>Geben Sie einen Namen für die Datenstruktur ein und klicken Sie auf die Schaltfläche <strong>[!UICONTROL Add item]</strong> , um die einzelnen Spalten hinzuzufügen. Wenn Sie zwei Spalten exportieren möchten: „Vollständiger Name“ und „E-Mail“, würde die resultierende Datenstruktur wie folgt aussehen:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png" style="width: 350;height: 524;"> </p> </li>
<li value="4"> <p>Nachdem Sie die Datenstruktur erfolgreich definiert haben, sollten die Felder, die jeder einzelnen Spalte entsprechen, in der Konfiguration des [!UICONTROL Create CSV (advanced)] angezeigt werden, damit Sie die Elemente zuordnen können. Nehmen Sie das erste Element aus dem <code>[!UICONTROL Emails[]]</code>-Array und ordnen Sie sein Element <code>Email </code>dem Feld/der Spalte E-Mail zu:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png" style="width: 350;height: 308;"> </p> </li>
<li value="5"> <p>Führen Sie das Szenario aus. Da das Element der Spalte „E-Mail“ zugeordnet <code>Emails[1]: Email</code>, vom einfachen Typ „Text“ ist, wird es jetzt korrekt exportiert:</p> <p>„Vollständiger Name“,„E-Mail“</p> <p>„Shon Winer“,“Shon@Winer.com"</p> <p>„Lizeth Fulmore“,“Lizeth@Fulmore.com"</p> <p>„Hilario Gullatt“,“Hilario@Gullatt.com"</p> <p>„Abby Eisenbarth“,“Abby@Eisenbarth.com"</p> </li>
</ol>
</div>

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
   <td>Geben Sie die CSV-Datei ein, die Sie parsen möchten, oder mappen Sie sie.<p>Hinweis: <p>Wenn Ihre Daten in binärer Form vorliegen (normalerweise aus einer Datei), müssen Sie die Funktion „toString()“ verwenden, um die Binärdaten in [!UICONTROL String] zu konvertieren:</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png" style="width: 350;height: 123;"></p></p></td> 
  </tr> 
 </tbody> 
</table>
