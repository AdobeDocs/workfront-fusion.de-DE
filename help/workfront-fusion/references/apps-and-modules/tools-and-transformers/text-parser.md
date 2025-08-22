---
title: Text-Parser
description: Sie können das Text-Parser-Tool verwenden, um Text zu analysieren, der in anderen Adobe Workfront Fusion-Szenario-Modulen verwendet werden soll. Der Text-Parser benötigt keine Verbindung.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 885d714e-fc09-41a2-89dc-ebe29a355e43
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1326'
ht-degree: 0%

---

# [!UICONTROL Text-Parser]

Sie können das [!UICONTROL Text-Parser-Tool] verwenden, um Text zur Verwendung in anderen Adobe Workfront Fusion-Szenario-Modulen zu analysieren. Der [!UICONTROL Text-Parser] erfordert keine Verbindung.

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

## Text-Parser-API-Informationen

Der Text-Parser-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v2</td> 
  </tr>
 </tbody> 
 </table>

## [!UICONTROL Text-Parser] Module und ihre Felder

Beim Konfigurieren von [!UICONTROL Text-Parser]-Modulen zeigt Adobe Workfront Fusion die unten aufgeführten Felder an. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Transformatoren

* [[!UICONTROL Elemente aus HTML abrufen]](#get-elements-from-html)
* [[!UICONTROL Elemente aus Text abrufen]](#get-elements-from-text)
* [[!UICONTROL HTML in Text]](#html-to-text)
* [[!UICONTROL Übereinstimmungsmuster]](#match-pattern)
* [[!UICONTROL Ersetzen]](#replace)

#### [!UICONTROL Elemente aus HTML abrufen]

Ruft die gewünschten Elemente aus dem HTML-Code ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Die Routenausführung auch dann fortsetzen, wenn das Modul keine Übereinstimmungen findet]</td> 
   <td> <p>Aktivieren Sie diese Option, um sicherzustellen, dass das Modul das Szenario nicht stoppt, wenn es keine Ergebnisse zurückgibt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Elementtyp]</td> 
   <td> <p> Wählen Sie den Elementtyp aus, den Sie aus dem HTML-Code abrufen möchten. </p> 
    <ul> 
     <li>[!UICONTROL Bild]</li> 
     <li>[!UICONTROL Link]</li> 
     <li>[!UICONTROL iFrame-Element(e)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>Geben Sie den HTML-Code ein, aus dem Sie die angegebenen Elementtypen abrufen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elemente aus Text abrufen]

Analysiert Elemente aus Text anhand des angegebenen Musters.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Eingabetext]</td> 
   <td> <p>Geben Sie den Text ein, den Sie analysieren möchten, oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Muster]</td> 
   <td> <p>Wählen Sie aus dem Text das Muster aus, das die zu analysierenden Elemente enthält.</p> <p>Um einen benutzerdefinierten regulären Ausdruck einzugeben, wählen Sie Benutzerdefiniert aus der Liste und geben Sie dann den benutzerdefinierten Ausdruck im benutzerdefinierten Regex-Feld ein.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Doppelte Vorkommen ignorieren]</td> 
   <td> <p>Aktivieren Sie dieses Kontrollkästchen, um doppelte Vorkommen eines Textelements zu ignorieren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL HTML in Text]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>Geben Sie den HTML-Code ein, den Sie in Nur-Text konvertieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zeilenumbruch] </td> 
   <td> <p>Wählen Sie den Zeilenumbruchtyp aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Großbuchstaben]</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um in Überschriften-Tags eingeschlossenen Text (z. B. &lt;h2&gt; &lt;/h2&gt;) in Großbuchstaben zu konvertieren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Übereinstimmungsmuster]

Das [!UICONTROL Match pattern]-Modul ermöglicht es, Zeichenfolgenelemente zu finden und zu extrahieren, die einem Suchmuster aus einem bestimmten Text entsprechen. Dieses Modul verwendet reguläre Ausdrücke (auch als Regex oder Regex bezeichnet).

Ein regulärer Ausdruck ist eine Sequenz von Zeichen, in der jedes Zeichen entweder ein Metazeichen mit einer speziellen Bedeutung oder ein reguläres Zeichen mit einer wörtlichen Bedeutung ist. Diese Zeichen und Metazeichen identifizieren ein Muster, das für die Suche nach Text verwendet werden kann. Wenn Sie beispielsweise nach Namen suchen möchten, können Sie einen regulären Ausdruck einrichten, um nach einem Muster zu suchen, das aus zwei aufeinander folgenden Wörtern besteht, die mit Großbuchstaben beginnen. Reguläre Ausdrücke sind ein leistungsstarkes Tool zum Suchen und Bearbeiten von Text.

Eine Diskussion über reguläre Ausdrücke würde den Rahmen dieses Artikels sprengen. Wir empfehlen die folgenden Ressourcen:

* Eine vollständige Liste der Metazeichen finden Sie unter [Reguläre Ausdrücke](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) in MDN-Webdokumenten.
* Für ein Tutorial zum Erstellen regulärer Ausdrücke empfehlen wir [RegexOne](https://regexone.com/).
* Zum Experimentieren mit regulären Ausdrücken empfehlen wir die Website [Reguläre Ausdrücke 101](https://regex101.com/). Wählen Sie im linken Bedienfeld das ECMAScript (JavaScript)-FLAVOR aus.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Muster] </td> 
   <td> <p>Geben Sie das Muster für reguläre Ausdrücke ein. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span> <code>[+-]?(\d+(\.\d+)?|\.\d+)([eE][+-]?\d+)?</code> extrahiert alle Ziffern im angegebenen Text.</p> <p>Hinweis:  <p>Das Muster muss mindestens eine Erfassungsgruppe in Klammern <code>()</code>. Wenn das Muster keine Erfassungsgruppen enthält, ist das Ausgabepaket leer.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Globale Übereinstimmung]</td> 
   <td> <p>Aktivieren Sie diese Option, um alle Übereinstimmungen im Text abzurufen. Jede Übereinstimmung wird in einem separaten Bundle ausgegeben. Wenn diese Option deaktiviert ist, ruft das Modul nur den ersten Eintrag ab.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Groß-/Kleinschreibung beachten]</td> 
   <td> <p> Aktivieren Sie diese Einstellung, damit bei Text zwischen Groß- und Kleinschreibung unterschieden wird.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL multiline] </td> 
   <td> <p>Aktivieren Sie diese Option, um sicherzustellen, dass die Anfangs- und Endmetazeichen (<code>^</code> und <code>$</code>) mit dem Beginn oder Ende jeder Zeile übereinstimmen, nicht nur mit dem Anfang oder Ende der gesamten Eingabezeichenfolge.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL SingleLine]</td> 
   <td>Aktivieren Sie diese Option, um sicherzustellen, dass der Punkt (.) mit Zeilenumbruchzeichen (<code>\n</code>) übereinstimmt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Die Routenausführung auch dann fortsetzen, wenn das Modul keine Ergebnisse zurückgibt]</td> 
   <td> <p>Aktivieren Sie diese Option, um sicherzustellen, dass das Modul das Szenario nicht stoppt, wenn es keine Ergebnisse zurückgibt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Text] </td> 
   <td> <p>Geben Sie den Text ein, der dem Muster entsprechen soll, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ersetzen]

Durchsucht den eingegebenen Text nach einem angegebenen Wert oder regulären Ausdruck und ersetzt das Ergebnis durch den neuen Wert.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Muster] </td> 
   <td> <p>Geben Sie den Suchbegriff ein. Sie können auch einen regulären Ausdruck verwenden. Weitere Informationen zum regulären Ausdruck finden Sie im <a href="#match-pattern" class="MCXref xref">[!UICONTROL Match Pattern]</a>-Modul.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Neuer Wert]</td> 
   <td> <p> Geben Sie den Wert ein, den Sie den Suchbegriff ersetzen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Globale Übereinstimmung]</td> 
   <td> <p>Aktivieren Sie diese Option, um alle Übereinstimmungen im Text abzurufen. Jede Übereinstimmung wird in einem separaten Bundle ausgegeben. Wenn diese Option deaktiviert ist, ruft das Modul nur den ersten Eintrag ab.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Groß-/Kleinschreibung beachten]</td> 
   <td> <p> Aktivieren Sie diese Einstellung, damit bei Text zwischen Groß- und Kleinschreibung unterschieden wird.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL multiline] </td> 
   <td> <p>Aktivieren Sie diese Option, um sicherzustellen, dass die Anfangs- und Endmetazeichen (<code>^</code> und <code>$</code>) mit dem Beginn oder Ende jeder Zeile übereinstimmen, nicht nur mit dem Anfang oder Ende der gesamten Eingabezeichenfolge.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL SingleLine]</td> 
   <td>Aktivieren Sie diese Option, um sicherzustellen, dass der Punkt (.) mit Zeilenumbruchzeichen (<code>\n</code>) übereinstimmt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Text] </td> 
   <td> <p>Geben Sie den zu suchenden Text ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Daten-Scraping

Beim Daten-Scraping (manchmal auch als Web-Scraping, Datenextraktion oder Web-Sammeln bezeichnet) werden Daten von Websites erfasst und in Ihrer lokalen Datenbank oder in Tabellen gespeichert. Wenn Sie Daten von einer Website kratzen möchten und mit regulären Ausdrücken nicht vertraut sind, können Sie ein Tool zum Kratzen von Daten verwenden.

Wenn das Tool zum Daten-Scraping eine REST-API bereitstellt, können Sie über unsere universellen [[!UICONTROL HTTP]-Module](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors) und [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)-Module eine Verbindung herstellen.

## Fehlerbehebung beim Text-Parser

Verwenden Sie diese Informationen, wenn Sie keinen Text-Parser erhalten können, um eine Ausgabe zu erzeugen.

>[!BEGINSHADEBOX]

Beispiel:

Das Modul sollte den Dateityp eines Dateidokuments „filename.docx“ analysieren, und die Dateinamenerweiterung variiert von DOCX zu PDF zu CSV.

Der Ausdruck, den Sie in diesem Fall verwenden können, lautet [!DNL \..+]

Dieser reguläre Ausdruck führt normalerweise zu einer vollständigen Übereinstimmung.

Die Implementierung dieses Ausdrucks in Ihrem Text-Parser führt jedoch nicht zu einer Übereinstimmung:

![Keine Übereinstimmung](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-you-dont-get-a-match-350x365.png)

Der Grund dafür ist, dass das „i“ nur die Anzahl der Übereinstimmungen pro Übereinstimmung anzeigt. In diesem Fall haben wir also 2 Übereinstimmungen, daher gibt es nach dem „i“ einen numerischen Wert 1 und 2. Der Anwendungsfall hierfür besteht darin, dass Sie, falls Sie Daten jemals mit dem zweiten übereinstimmenden Wert abgleichen oder durch einen Filter übergeben müssen, angeben können, welcher Wert durch den numerischen Wert dargestellt wird.

![Übereinstimmung](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-matches-350x355.png)

Um die Übereinstimmungswerte abzurufen, die Sie benötigen, um dem zu analysierenden Teil Klammern hinzuzufügen (z. B. um nur aus „filename.docx“ - „docx“ zu extrahieren), sollten die Klammern gemäß dem Regex-Ausdruck, den wir für dieses Szenario verwenden, auf \ angewendet werden.(.+)

Erfasst das DOCX, platziert es in einer Gruppe und lässt das &quot;.“ Raus damit.

![Treffer abrufen](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-get-matches-350x592.png)

In der im folgenden Bild gezeigten Ausgabe entspricht die Erfassungsgruppe einem beliebigen Zeichen (mit Ausnahme der Zeilenumbrüche).

![Ausgabe](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-output-350x389.png)

Eine weitere Problemumgehung, die auch Regex enthält, ist die Verwendung der Funktion Ersetzen .

`{{replace("abcdefghijklmno pqr stuvw xyz.docx"; "/.\./"; ".")}}`

Ersetzen Sie dann `abcdefghijklmno pqr stuvw xyz.docx` durch die eigentliche Dateinamenvariable .

>[!ENDSHADEBOX]
