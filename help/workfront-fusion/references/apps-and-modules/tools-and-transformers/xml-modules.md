---
title: XML
description: Die XML-App ermöglicht es, einen im XML-Format formatierten Text mithilfe des XML&map;gt;-Parse-XML-Moduls zu analysieren und in ein Bundle zu konvertieren, um die Daten für andere Module verfügbar zu machen. Sie können ein Bundle auch über das XML-Modul "*.gt;“ in einen XML-formatierten Text konvertieren
author: Becky
feature: Workfront Fusion
exl-id: ab323361-cd04-4dcc-ab02-0fb468334fdb
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '1433'
ht-degree: 2%

---

# XML

Die [!UICONTROL XML]-App ermöglicht es, einen im XML-Format formatierten Text über das [!UICONTROL XML] > [!UICONTROL Parse XML]-Modul zu analysieren und in ein Bundle zu konvertieren, um die Daten für andere Module verfügbar zu machen. Sie können ein Bundle auch über das Modul [!UICONTROL XML] > [!UICONTROL XML erstellen] in einen Text im XML-Format konvertieren

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
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## XML erstellen

Das Modul [!UICONTROL XML] > [!UICONTROL XML erstellen] konvertiert ein Bundle in einen Text im XML-Format.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Datenstruktur]</p> </td> 
   <td> <p>Die Datenstruktur beschreibt die Struktur der resultierenden XML. Wenn Sie über ein Beispiel für die XML verfügen, die Sie erstellen möchten, können Sie damit die Datenstruktur generieren:</p> 
    <ol> 
     <li value="1">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Hinzufügen</strong>.</li> 
     <li value="2">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Generator]</strong>.</li> 
     <li value="3">Kopieren Sie das XML-Beispiel und fügen Sie es in das Feld Beispieldaten ein.</li> 
     <li value="4">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Speichern</strong>.</li> 
     <li value="5">Stellen Sie sicher, dass die Datenstruktur erfolgreich generiert wurde.</li> 
     <li value="6">Klicken Sie auf <strong>[!UICONTROL Speichern]</strong>, um die Datenstruktur zu speichern.</li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stammelementname]</td> 
   <td>Geben Sie den Namen des XML-Stammelements ein. Der Standardwert lautet <code>root</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL DOCTYPE SYSTEM-ID]</td> 
   <td>Dateinamen eingeben, der in der <code>!DOCTYPE SYSTEM</code> verwendet werden soll</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL DOCTYPE PUBLIC ID]</td> 
   <td>Dateinamen eingeben, der in der <code>!DOCTYPE PUBLIC</code> verwendet werden soll</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Strip XML-Deklaration]</td> 
   <td>Aktivieren Sie diese Option, um die XML-Deklaration <code>&lt;?xml ... ?&gt;</code> und <code>&lt;!DOCTYPE ... &gt;</code>zu entfernen und nur das XML-Stammelement und dessen Inhalte zu belassen.</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Beispiel:**

Ein typischer Anwendungsfall besteht darin, Daten aus einer [!DNL Google] > Tabelle in XML umzuwandeln.

1. Platzieren Sie das Modul [!DNL Google Sheets] > [!UICONTROL Zeilen auswählen] in Ihrem Szenario, um die Daten abzurufen. Richten Sie das -Modul ein, um Zeilen aus Ihrer [!DNL Google] Tabelle abzurufen. Legen Sie &#x200B;**[!UICONTROL Maximale Anzahl der zurückgegebenen Zeilen]** auf eine kleine Anzahl fest, die zu Testzwecken jedoch größer als 1 ist (z. B. drei). Führen Sie das [!DNL Google Sheets] Modul aus, indem Sie mit der rechten Maustaste darauf klicken und &quot;**[!UICONTROL Nur dieses Modul ausführen]** auswählen. Überprüfen Sie die Ausgabe des Moduls.
1. Verbinden Sie das [!UICONTROL Array Aggregator]-Modul nach dem [!DNL Google Sheets]. Wählen Sie im Setup des Moduls das [!DNL Google Sheets] im Feld **[!UICONTROL Source-Knoten]** aus. Lassen Sie die anderen Felder so, wie sie für den Moment sind.
1. Verbinden Sie das Modul [!UICONTROL XML] > [!UICONTROL XML erstellen] nach dem Modul [!UICONTROL Array Aggregator].

   Die Einrichtung des Moduls erfordert eine Datenstruktur, die die Struktur der XML-Ausgabe beschreibt. Klicken Sie auf **[!UICONTROL Hinzufügen]**, um die Einrichtung der Datenstruktur zu öffnen. Die einfachste Möglichkeit, diese Datenstruktur zu erstellen, besteht darin, sie automatisch aus einem XML-Beispiel zu generieren.

1. Klicken Sie auf **[!UICONTROL Generator]** und fügen Sie Ihr XML-Beispiel in das Feld [!UICONTROL Beispieldaten] ein:

   ![Beispieldatenfeld](/help/workfront-fusion/references/apps-and-modules/assets/sample-data-field-350x146.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Das Feld Spezifikation in der Datenstruktur enthält jetzt die generierte Struktur.
1. Ändern Sie den Namen Ihrer Datenstruktur in etwas Spezifischeres und klicken Sie auf **[!UICONTROL Speichern]**.

   Ein Feld, das dem Stamm-Array-Attribut entspricht, wird im Setup des JSON-Moduls als zuordnungsfähiges Feld angezeigt.
1. Klicken Sie auf **[!UICONTROL Map]**-Schaltfläche neben dem Feld und ordnen Sie das `Array[]` aus der Ausgabe des [!UICONTROL Array] zu:
1. Klicken Sie **[!UICONTROL OK]**, um die Einrichtung des XML-Moduls zu schließen.
1. Öffnen Sie das Setup des Moduls [!UICONTROL Array Aggregator]. Ändern Sie die **[!UICONTROL Zielstruktur]** von Benutzerdefiniert in das Feld eines XML-Moduls, das dem übergeordneten XML-Element entspricht. Ordnen Sie Elemente aus dem [!DNL Google Sheets]-Modul den entsprechenden Feldern zu.
1. Klicken Sie **[!UICONTROL OK]**, um die Einrichtung des Array Aggregator-Moduls zu schließen.
1. Führen Sie das Szenario aus.

   Das XML-Modul gibt die richtige XML-Datei aus.

1. Öffnen Sie die Einrichtung des [!DNL Google Sheets] und erhöhen Sie die [!UICONTROL Maximale Anzahl zurückgegebener Zeilen] um größer als die Anzahl an Zeilen in Ihrer Tabelle zu sein, um alle Daten zu verarbeiten.

   Die resultierende XML kann in [!DNL Dropbox] gespeichert, als Anhang per E-Mail gesendet, per FTP auf einen Server hochgeladen usw. werden.

>[!ENDSHADEBOX]

### XML-Attribute hinzufügen

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

## [!UICONTROL XML analysieren]

Das Modul [!UICONTROL XML] > [!UICONTROL Parse XML] analysiert einen XML-formatierten Text und gibt ein einzelnes Bundle aus, das alle aus der XML extrahierten Informationen enthält.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Datenstruktur]</p> </td> 
   <td> <p>Die Datenstruktur beschreibt die Struktur der XML, um die Ausgabe des Moduls im Zuordnungsbereich für die folgenden Module verfügbar zu machen.</p> <p>Wenn Sie über ein Beispiel für die XML verfügen, die Sie parsen möchten, können Sie sie zum Generieren der Datenstruktur verwenden:</p> 
    <ol> 
     <li value="1">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Hinzufügen</strong>.</li> 
     <li value="2">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Generator]</strong>.</li> 
     <li value="3">Kopieren Sie das XML-Beispiel und fügen Sie es in das Feld <strong>[!UICONTROL Beispieldaten]</strong> ein.</li> 
     <li value="4">Klicken Sie auf <strong>[!UICONTROL Speichern]</strong>.</li> 
     <li value="5">Stellen Sie sicher, dass die Datenstruktur erfolgreich generiert wurde.</li> 
     <li value="6"> <p>Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Speichern]</strong>, um die Datenstruktur zu speichern.</p> <p>Sie können die Schritte 2-5 überspringen, um eine leere Datenstruktur bereitzustellen. Wenn die Datenstruktur leer ist, ist die Ausgabe des Moduls erst dann im Zuordnungsbereich verfügbar, wenn das Modul mindestens einmal ausgeführt wurde.</p> </li> 
    </ol> <p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Datenstrukturen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zahlen als Text beibehalten]</td> 
   <td>Aktivieren Sie diese Option, um sicherzustellen, dass Zahlen als Text-(String-)Werte erhalten bleiben. Andernfalls werden Zahlen in Zahlenwerte umgewandelt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL XML]</p> </td> 
   <td> <p>Geben Sie den XML-formatierten Text ein, den Sie analysieren möchten, oder ordnen Sie ihn zu.</p> <p>Wenn Sie eine Formel verwenden, stellen Sie sicher, dass ihr Ergebniswerttyp der Datentyp [!UICONTROL Text] ist (oder automatisch konvertiert werden kann). </p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/if-you-use-a-formula-350x164.png" style="width: 350;height: 164;"> </p> <p>Wenn der Ergebniswerttyp [!UICONTROL Buffer] (Binärdaten) ist, konvertieren Sie ihn mit der Funktion <code>toString()</code> in den Datentyp Text . Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a> und <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Datentypen</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Beispiel:**

So laden Sie eine XML-Datei von einer URL herunter und analysieren ihren Inhalt:

1. Erstellen Sie ein neues Szenario.
1. Fügen Sie das Modul [!UICONTROL HTTP] > [!UICONTROL Datei ]&quot; hinzu
1. Öffnen Sie die -Konfiguration des Moduls und konfigurieren Sie sie wie folgt:

   **URL**: URL der XML-Datei (z. B. `https://siftrss.com/f/rqLy05ayMBJ`)

   ![Beispiel für URL einer XML-Datei](/help/workfront-fusion/references/apps-and-modules/assets/url-of-xml-file-350x184.png)

1. Klicken Sie auf **[!UICONTROL OK]**, um die Konfiguration des Moduls zu speichern und zu schließen.
1. Fügen Sie das Modul [!UICONTROL XML] > [!UICONTROL Parse XML] hinzu, verbinden Sie es nach dem Modul [!UICONTROL HTTP] > [!UICONTROL Datei abrufen] und konfigurieren Sie es wie folgt:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL-Datenstruktur]</td> 
      <td> 
       <ol> 
        <li value="1">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Hinzufügen</strong>.</li> 
        <li value="2">Klicken Sie auf die Schaltfläche <strong>[!UICONTROL Generator]</strong>.</li> 
        <li value="3">Öffnen Sie in Ihrem Webbrowser eine neue Registerkarte oder ein neues Fenster.</li> 
        <li value="4">Fügen Sie die im dritten Schritt verwendete URL in die Adressleiste ein und rufen Sie die XML-Datei ab.</li> 
        <li value="5">Wählen Sie den gesamten XML-Text aus und kopieren Sie ihn in die Zwischenablage.</li> 
        <li value="6">Schließen Sie die Registerkarte oder das Fenster und kehren Sie zu Ihrem Szenario zurück.</li> 
        <li value="7">Fügen Sie den kopierten XML-Text in das Feld Beispieldaten ein.</li> 
        <li value="8">Klicken Sie auf <strong>[!UICONTROL Speichern]</strong>.</li> 
        <li value="9">Stellen Sie sicher, dass die Datenstruktur erfolgreich generiert wurde.</li> 
        <li value="10">Klicken Sie auf <strong>[!UICONTROL Speichern]</strong>, um die Datenstruktur zu speichern.</li> 
       </ol> <p>Sie können die Schritte 2 bis 9 überspringen, um eine leere Datenstruktur bereitzustellen. Wenn die Datenstruktur leer ist, ist die Ausgabe des Moduls erst dann im Zuordnungsbereich verfügbar, wenn das Modul mindestens einmal ausgeführt wurde.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL XML]</td> 
      <td> <p>Ordnen Sie das <code>Data </code>Element aus der Ausgabe des Moduls [!UICONTROL HTTP] &gt; [!UICONTROL Datei abrufen] dem Feld zu. Verwenden Sie die <code>toString()</code>-Funktion, um ihren Wert vom Datentyp [!UICONTROL Buffer] (Binärdaten) in den Datentyp [!UICONTROL Text] zu konvertieren.</p> <p>Sie können den Code der Formel kopieren und in das Feld einfügen: <code>&#123;&#123;toString(1.data)&#125;&#125;</code></p> <p>Weitere Informationen zu den Datentypen „Puffer“ und „Text“ finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Elementdatentypen</a>.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/paste-formula-code-350x99.png"> </p> </td> 
     </tr> 
    </tbody> 
   </table>

>[!ENDSHADEBOX]

### [!UICONTROL Analysieren von XML-Attributen]

Standardmäßig fügt das Modul [!UICONTROL XML] > [!UICONTROL Parse XML] Attribute in eine spezielle `_attributes` ein, die dem Knoten untergeordnet ist, der diese Attribute aufweist. Wenn es sich bei dem Knoten um einen Textknoten handelt und er über Attribute verfügt, werden zwei spezielle Eigenschaften hinzugefügt: `_attributes` für Attribute und `_value` für den Textinhalt des Knotens.

>[!BEGINSHADEBOX]

**Beispiel:** Diese XML:

```
<root attr="1">
<node attr="ABC">Hello, World</node>
</root>
```

wird in dieses Bundle konvertiert:

![XML in Bundle konvertiert](/help/workfront-fusion/references/apps-and-modules/assets/xml-converted-to-bundle.png)

>[!ENDSHADEBOX]

## Fehlerbehebung: Daten aus dem Modul [!UICONTROL XML analysieren“ können nicht ] werden

Stellen Sie sicher, dass die Datenstruktur korrekt definiert ist. Alternativ können Sie eine leere Datenstruktur verwenden und das Modul mindestens einmal ausführen, um eine XML-Eingabe zu verarbeiten.
