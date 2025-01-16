---
title: XML
description: Die XML-App ermöglicht es, einen im XML-Format formatierten Text mithilfe des XML&map;gt;-Parse-XML-Moduls zu analysieren und in ein Bundle zu konvertieren, um die Daten für andere Module verfügbar zu machen. Sie können ein Bundle auch über das XML-Modul "*.gt;“ in einen XML-formatierten Text konvertieren
author: Becky
feature: Workfront Fusion
exl-id: ab323361-cd04-4dcc-ab02-0fb468334fdb
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 2%

---

# XML

Die [!UICONTROL XML] App ermöglicht es Ihnen, einen XML-formatierten Text über das Modul [!UICONTROL XML] > [!UICONTROL Parse XML] zu analysieren und in ein Bundle zu konvertieren, um die Daten für andere Module verfügbar zu machen. Sie können ein Bundle auch über das Modul [!UICONTROL XML] > [!UICONTROL Create XML] in einen Text im XML-Format konvertieren

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

## [!UICONTROL Parse XML]

Das Modul [!UICONTROL XML] > [!UICONTROL Parse XML] analysiert einen XML-formatierten Text und gibt ein einzelnes Bundle aus, das alle aus der XML extrahierten Informationen enthält.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>Die Datenstruktur beschreibt die Struktur der XML, um die Ausgabe des Moduls im Zuordnungsbereich für die folgenden Module verfügbar zu machen.</p> <p>Wenn Sie über ein Beispiel für die XML verfügen, die Sie parsen möchten, können Sie sie zum Generieren der Datenstruktur verwenden:</p> 
    <ol> 
     <li value="1">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Add]</strong> .</li> 
     <li value="2">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Generator]</strong> .</li> 
     <li value="3">Kopieren Sie das XML-Beispiel und fügen Sie es in das Feld <strong>[!UICONTROL Sample data]</strong> ein.</li> 
     <li value="4">Klicken Sie auf <strong>[!UICONTROL Save]</strong>.</li> 
     <li value="5">Stellen Sie sicher, dass die Datenstruktur erfolgreich generiert wurde.</li> 
     <li value="6"> <p>Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Save]</strong> , um die Datenstruktur zu speichern.</p> <p>Sie können die Schritte 2-5 überspringen, um eine leere Datenstruktur bereitzustellen. Wenn die Datenstruktur leer ist, ist die Ausgabe des Moduls erst dann im Zuordnungsbereich verfügbar, wenn das Modul mindestens einmal ausgeführt wurde.</p> </li> 
    </ol> <p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Datenstrukturen in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve numbers as text]</td> 
   <td>Aktivieren Sie diese Option, um sicherzustellen, dass Zahlen als Text-(String-)Werte erhalten bleiben. Andernfalls werden Zahlen in Zahlenwerte umgewandelt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL XML]</p> </td> 
   <td> <p>Geben Sie den XML-formatierten Text ein, den Sie analysieren möchten, oder ordnen Sie ihn zu.</p> <p>Wenn Sie eine Formel verwenden, stellen Sie sicher, dass ihr Ergebnisdatentyp der [!UICONTROL Text]-Datentyp ist (oder automatisch konvertiert werden kann). </p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/if-you-use-a-formula-350x164.png" style="width: 350;height: 164;"> </p> <p>Wenn der Ergebnisdatentyp "[!UICONTROL Buffer]" ist (Binärdaten), konvertieren Sie ihn mithilfe der <code>toString()</code> in den Datentyp „Text“. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in den Datentypen [!DNL Adobe Workfront Fusion]</a> und <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Element“ in [!UICONTROL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Beispiel:** So laden Sie eine XML-Datei von einer URL herunter und analysieren ihren Inhalt:
>
>1. Erstellen Sie ein neues Szenario.
>1. [!UICONTROL HTTP] > [!UICONTROL Get a file] einfügen
>1. Öffnen Sie die -Konfiguration des Moduls und konfigurieren Sie sie wie folgt:
>
>   **URL**: URL der XML-Datei (z. B. `https://siftrss.com/f/rqLy05ayMBJ`)
>
>   ![](/help/workfront-fusion/references/apps-and-modules/assets/url-of-xml-file-350x184.png)
>
>1. Klicken Sie auf **[!UICONTROL OK]**&#x200B;, um die Konfiguration des Moduls zu speichern und zu schließen.
1. Fügen Sie das Modul [!UICONTROL XML] > [!UICONTROL Parse XML] hinzu, verbinden Sie es nach dem Modul [!UICONTROL HTTP] > [!UICONTROL Get a file] und konfigurieren Sie es wie folgt:
>
<table style="table-layout:auto"> 
&gt;    <col> 
&gt;    <col> 
&gt;    <tbody> 
&gt;     <tr> 
&gt;      <td role="rowheader">[!UICONTROL Data structure]</td> 
&gt;      <td> 
&gt;       <ol> 
&gt;        <li value="1">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Add]</strong> .</li> 
&gt;        <li value="2">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Generator]</strong> .</li> 
&gt;        <li value="3">Öffnen Sie in Ihrem Webbrowser eine neue Registerkarte oder ein neues Fenster.</li> 
&gt;        <li value="4">Fügen Sie die im dritten Schritt verwendete URL in die Adressleiste ein und rufen Sie die XML-Datei ab.</li> 
&gt;        <li value="5">Wählen Sie den gesamten XML-Text aus und kopieren Sie ihn in die Zwischenablage.</li> 
&gt;        <li value="6">Schließen Sie die Registerkarte oder das Fenster und kehren Sie zu Ihrem Szenario zurück.</li> 
&gt;        <li value="7">Fügen Sie den kopierten XML-Text in das Feld Beispieldaten ein.</li> 
&gt;        <li value="8">Klicken Sie auf <strong>[!UICONTROL Save]</strong>.</li> 
&gt;        <li value="9">Stellen Sie sicher, dass die Datenstruktur erfolgreich generiert wurde.</li> 
&gt;        <li value="10">Klicken Sie auf <strong>[!UICONTROL Save]</strong> , um die Datenstruktur zu speichern.</li> 
&gt;       </ol> <p>Sie können die Schritte 2 bis 9 überspringen, um eine leere Datenstruktur bereitzustellen. Wenn die Datenstruktur leer ist, ist die Ausgabe des Moduls erst dann im Zuordnungsbereich verfügbar, wenn das Modul mindestens einmal ausgeführt wurde.</p> </td> 
&gt;     </tr> 
&gt;     <tr> 
&gt;      <td role="rowheader">[!UICONTROL XML]</td> 
&gt;      <td> <p>Ordnen Sie <code>Data </code>Element aus der Ausgabe des Moduls [!UICONTROL HTTP] &gt; [!UICONTROL Get a file] dem Feld zu. Verwenden Sie die <code>toString()</code>-Funktion, um ihren Wert aus dem [!UICONTROL Buffer] (binäre Daten) in [!UICONTROL Text] Datentyp zu konvertieren.</p> <p>Sie können den Code der Formel kopieren und in das Feld einfügen: <code>&#123;&#123;toString(1.data)&#125;&#125;</code></p> <p>Weitere Informationen zu den Datentypen „Puffer“ und „Text“ finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Elementdatentypen in Adobe Workfront Fusion</a>.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/paste-formula-code-350x99.png" style="width: 350;height: 99;"> </p> </td> 
&gt;     </tr> 
&gt;    </tbody> 
&gt;   </table>

## [!UICONTROL Parsing XML attributes]

Standardmäßig legt das Modul [!UICONTROL XML] > [!UICONTROL Parse XML] Attribute in einer speziellen `_attributes` als untergeordnetes Element des Knotens ab, der diese Attribute aufweist. Wenn es sich bei dem Knoten um einen Textknoten handelt und er über Attribute verfügt, werden zwei spezielle Eigenschaften hinzugefügt: `_attributes` für Attribute und `_value` für den Textinhalt des Knotens.

>[!INFO]
>
**Beispiel:** Diese XML:

```
<root attr="1">
<node attr="ABC">Hello, World</node>
</root>
```

wird in dieses Bundle konvertiert:

![](/help/workfront-fusion/references/apps-and-modules/assets/xml-converted-to-bundle.png)

## XML erstellen

Das Modul [!UICONTROL XML] > [!UICONTROL Create XML] konvertiert ein Bundle in einen Text im XML-Format.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>Die Datenstruktur beschreibt die Struktur der resultierenden XML. Wenn Sie über ein Beispiel für die XML verfügen, die Sie erstellen möchten, können Sie damit die Datenstruktur generieren:</p> 
    <ol> 
     <li value="1">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Add]</strong> .</li> 
     <li value="2">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Generator]</strong> .</li> 
     <li value="3">Kopieren Sie das XML-Beispiel und fügen Sie es in das Feld Beispieldaten ein.</li> 
     <li value="4">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Save]</strong> .</li> 
     <li value="5">Stellen Sie sicher, dass die Datenstruktur erfolgreich generiert wurde.</li> 
     <li value="6">Klicken Sie auf <strong>[!UICONTROL Save]</strong> , um die Datenstruktur zu speichern.</li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Root element name]</td> 
   <td>Geben Sie den Namen des XML-Stammelements ein. Der Standardwert ist <code>root</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype SYSTEM ID]</td> 
   <td>Dateinamen eingeben, der in der Deklaration verwendet <code> !DOCTYPE SYSTEM</code> soll</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype PUBLIC ID]</td> 
   <td>Dateinamen eingeben, der in der Deklaration verwendet <code> !DOCTYPE PUBLIC</code> soll</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Strip Xml Declaration]</td> 
   <td>Aktivieren Sie diese Option, um die XML-Deklaration <code>&lt;?xml ... ?&gt;</code> und <code>&lt;!DOCTYPE ... &gt;</code>zu entfernen und nur das XML-Stammelement und dessen Inhalte zu belassen.</td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
**Beispiel:**
>
Ein typischer Anwendungsfall besteht darin, Daten aus einer [!DNL Google] > Tabelle in XML umzuwandeln.
>
1. Platzieren Sie das Modul [!DNL Google Sheets] > [!UICONTROL Select rows] in Ihrem Szenario, um die Daten abzurufen. Richten Sie das -Modul ein, um Zeilen aus Ihrer [!DNL Google] Tabelle abzurufen. Legen Sie &#x200B;**[!UICONTROL Maximum number of returned rows]**) auf eine kleine Zahl fest, die zu Testzwecken jedoch größer als 1 ist (z. B. drei). Führen Sie das [!DNL Google Sheets] aus, indem Sie mit der rechten Maustaste darauf klicken und &quot;**[!UICONTROL Run this module only]**&quot; auswählen. Überprüfen Sie die Ausgabe des Moduls.
1. Schließen Sie das [!UICONTROL Array Aggregator] nach dem [!DNL Google Sheets] an. Wählen Sie im Setup des Moduls das [!DNL Google Sheets] im Feld **[!UICONTROL Source node]** aus. Lassen Sie die anderen Felder so, wie sie für den Moment sind.
1. Schließen Sie das Modul [!UICONTROL XML] > [!UICONTROL Create XML] nach dem Modul [!UICONTROL Array Aggregator] an.
>
Die Einrichtung des Moduls erfordert eine Datenstruktur, die die Struktur der XML-Ausgabe beschreibt. Klicken Sie auf die Schaltfläche **[!UICONTROL Add]** , um die Einrichtung der Datenstruktur zu öffnen. Die einfachste Möglichkeit, diese Datenstruktur zu erstellen, besteht darin, sie automatisch aus einem XML-Beispiel zu generieren.
>
1. Klicken Sie auf die Schaltfläche **[!UICONTROL Generator]** und fügen Sie Ihr XML-Beispiel in das Feld [!UICONTROL Sample data] ein:
>
![](/help/workfront-fusion/references/apps-and-modules/assets/sample-data-field-350x146.png)
>
1. Klicken Sie auf **[!UICONTROL Save]**. Das Feld Spezifikation in der Datenstruktur enthält jetzt die generierte Struktur.
1. Ändern Sie den Namen Ihrer Datenstruktur in etwas Spezifischeres und klicken Sie auf **[!UICONTROL Save]**. Ein Feld, das dem Stamm-Array-Attribut entspricht, wird im Setup des JSON-Moduls als zuordnungsfähiges Feld angezeigt.
1. Klicken Sie auf die Schaltfläche **[!UICONTROL Map]** neben dem Feld und ordnen Sie das `Array[]` aus der [!UICONTROL Array aggregator] zu:
1. Klicken Sie auf **[!UICONTROL OK]** , um die Einrichtung des XML-Moduls zu schließen.
1. Öffnen Sie die Einrichtung des [!UICONTROL Array Aggregator]. Ändern Sie die **[!UICONTROL Target structure]** von Benutzerdefiniert in das Feld eines XML-Moduls, das dem übergeordneten XML-Element entspricht. Ordnen Sie Elemente aus dem [!DNL Google Sheets]-Modul den entsprechenden Feldern zu.
1. Klicken Sie auf **[!UICONTROL OK]** , um die Einrichtung des Array Aggregator-Moduls zu schließen.
1. Führen Sie das Szenario aus.
>
Das XML-Modul gibt die richtige XML-Datei aus.
>
1. Öffnen Sie die Einrichtung des [!DNL Google Sheets] und erhöhen Sie die [!UICONTROL Maximum number of returned rows], sodass sie größer ist als die Anzahl der Zeilen in Ihrer Tabelle, um alle Daten zu verarbeiten.
>
Die resultierende XML kann in [!DNL Dropbox] gespeichert, als Anhang per E-Mail gesendet, per FTP auf einen Server hochgeladen usw. werden.

## XML-Attribute hinzufügen

Wenn Sie Attribute zu einem komplexen Knoten (einem Knoten, der andere Knoten enthalten wird) hinzufügen möchten, müssen Sie eine Sammlung mit dem Namen `_attributes` für die komplexe Anmerkung in Ihrer benutzerdefinierten Datenstruktur hinzufügen. Diese Sammlung wird Knotenattributen zugeordnet. Wenn Sie Attribute zu einem Textknoten hinzufügen möchten (z. B.: `<node attr="1">abc</node>`), müssen Sie eine `_attributes` für Attribute und eine Texteigenschaft `_value` für den Knotenwert für diesen Knoten in Ihrer benutzerdefinierten Datenstruktur hinzufügen.

```
{
   "name": "node",
   "type": "collection",
   "spec": [
      {
         "name": "_attributes",
         "type": "collection"
         "spec": [
            {
               "name": "attr1",
               "type": "text"
            }
         ]
      },
      {
         "name": "_value",
         "type": "text"
      }
   ]
}
```

## Fehlerbehebung: Daten aus dem [!UICONTROL Parse XML] können nicht zugeordnet werden

Stellen Sie sicher, dass die Datenstruktur korrekt definiert ist. Alternativ können Sie eine leere Datenstruktur verwenden und das Modul mindestens einmal ausführen, um eine XML-Eingabe zu verarbeiten.
