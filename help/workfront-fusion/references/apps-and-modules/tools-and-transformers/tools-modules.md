---
title: Tools
description: Der  [!DNL Adobe Workfront Fusion Tools]  enthält mehrere nützliche Module, die Ihr Szenario verbessern können.
author: Becky
feature: Workfront Fusion
exl-id: d9425f5b-4f4a-42da-9aca-1c1783be5fa7
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2286'
ht-degree: 0%

---

# [!UICONTROL Tools]

Der [!DNL Adobe Workfront Fusion Tools] Abschnitt enthält mehrere nützliche Module, die Ihr Szenario verbessern können.

[!UICONTROL Tools]-Module sind in der Liste der Apps oder über das [!UICONTROL Tools]-Symbol ![Tools-Symbol](/help/workfront-fusion/references/apps-and-modules/assets/tools-icon-small.png) am unteren Bildschirmrand verfügbar.

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

## [!UICONTROL Tools] und ihre Felder

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Aggregatoren](#aggregators)
* [Transformatoren](#transformers)

### Auslöser

#### [!UICONTROL Grundlegender Trigger ]

In diesem Modul können Sie einen benutzerdefinierten Trigger erstellen und dessen Eingabepakete definieren.

Dieses Modul kann beispielsweise für Kontakte oder andere Listen verwendet werden, die an eine bestimmte E-Mail-Adresse gesendet werden sollen (z. B. [!UICONTROL E-Mail] > [!UICONTROL E-Mail senden] oder [!DNL Gmail] > [!UICONTROL E-Mail senden]-Module) oder als einfache Erinnerung, die jederzeit ausgelöst werden soll.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Bundle]</td> 
   <td> <p>Erstellen benutzerdefinierter Bundles durch Hinzufügen von Array-Elementen. Klicken Sie für jedes Element, das Sie dem Bundle hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Namen und den Wert des Elements ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Abrufen mehrerer Variablen]](#get-multiple-variables)
* [[!UICONTROL Variable abrufen]](#get-variable)
* [[!UICONTROL Inkrementfunktion]](#increment-function)
* [[!UICONTROL Mehrere Variablen festlegen]](#set-multiple-variables)
* [[!UICONTROL Variable festlegen]](#set-variable)
* [[!UICONTROL Schlaf]](#sleep)

#### [!UICONTROL Abrufen mehrerer Variablen]

Dieses Modul ruft Werte ab, die zuvor vom Modul [!UICONTROL Variable festlegen] oder [!UICONTROL Mehrere Variablen festlegen] erstellt wurden.

Dieses Modul kann Variablen lesen, die an einer beliebigen Stelle im Szenario festgelegt wurden, selbst wenn die Variable auf einer anderen Route festgelegt wurde als der Ort, an dem sich das Modul [!UICONTROL Mehrere Variablen abrufen] befindet. Die einzige Anforderung besteht darin, dass das Modul [!UICONTROL Tools] > [!UICONTROL Variable festlegen] oder [!UICONTROL Tools] > [!UICONTROL Mehrere Variablen festlegen] vor dem Modul [!UICONTROL Tools] > [!UICONTROL Mehrere Variablen abrufen] ausgeführt wird. Weitere Informationen über die Reihenfolge, in der die Module ausgeführt werden, finden Sie unter [Hinzufügen eines Routermoduls und Konfigurieren von Routen](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL-Variablen]</td>
        <td>Klicken Sie für jede Variable, die das Modul abrufen soll, auf <b>Element hinzufügen</b> und geben Sie den Namen der Variablen ein.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

**Beispiele:** Die folgenden möglichen Verwendungen der [!UICONTROL Set]/[!UICONTROL Get(multiple) Variable(s)] sind:

* So speichern Sie einen berechneten Wert für die spätere Verwendung, auch in einer anderen Route. Dies ist nützlich, wenn der Wert in mehreren Modulen verwendet wird und die Formel zur Berechnung des Werts zu komplex ist.
* So debuggen Sie eine Formel. Wenn eine in einem Modul verwendete Formel scheinbar kein korrektes Ergebnis liefert, kopieren Sie die Formel und fügen Sie sie in ein Modul [!UICONTROL Variable festlegen] ein, das Sie vor dem entsprechenden Modul einfügen. Trennen Sie die Verbindung zu den Modulen nach dem Modul [!UICONTROL Variable festlegen] und führen Sie das Szenario aus. Überprüfen Sie die [!UICONTROL  des Moduls ]Variable festlegen“, passen Sie die Formel an oder vereinfachen Sie sie, führen Sie das Szenario erneut aus und fahren Sie damit fort, bis das Problem behoben ist.

>[!ENDSHADEBOX]


#### [!UICONTROL Variable abrufen]

Dieses Modul ruft einen Wert ab, der zuvor vom Modul [!UICONTROL Variable festlegen] oder [!UICONTROL Mehrere Variablen festlegen] erstellt wurde.

Dieses Modul kann Variablen lesen, die an einer beliebigen Stelle im Szenario festgelegt wurden, selbst wenn die Variable auf einer anderen Route festgelegt wurde als der Ort, an dem sich das Modul [!UICONTROL Variable abrufen] befindet. Die einzige Anforderung besteht darin, dass das Modul [!UICONTROL Tools] > [!UICONTROL Variable festlegen] oder [!UICONTROL Tools] > [!UICONTROL Mehrere Variablen festlegen] vor dem Modul [!UICONTROL Tools] > [!UICONTROL Variable abrufen] ausgeführt wird. Weitere Informationen über die Reihenfolge, in der die Module ausgeführt werden, finden Sie unter [Hinzufügen eines Routermoduls und Konfigurieren von Routen](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variablenname]</td> 
   <td> <p>Ordnen Sie den Namen der Variablen zu, die das Modul erhalten soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Inkrementfunktion]

Dieses Modul gibt einen Wert zurück, der nach jedem Zyklus oder jeder Ausführung eines Szenarios um 1 erhöht wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wert zurücksetzen]</td> 
   <td> <p>Wählen Sie aus, wann das Modul den Wert zurücksetzen soll. Dies ist der Fall, wenn der Wert beim ersten Wert von vorne beginnen soll.</p> 
    <ul> 
     <li>[!UICONTROL nach einem Zyklus]</li> 
     <li>[!UICONTROL nach einem Szenario]</li> 
     <li>[!UICONTROL Never]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Beispiel:**

Dieses Modul kann verwendet werden, um eine „Round Robin“-Zuweisung von Aufgaben, Leads, E-Mails usw. an Benutzer in einer Gruppe zu implementieren. Der Algorithmus wählt die Verantwortlichen aus einer Gruppe in einer rationalen Reihenfolge aus, normalerweise von oben nach unten in einer Liste. Wenn der Algorithmus das Ende der Liste erreicht, würde er dem Benutzer an oberster Stelle der Liste die nächste Zuweisung zuweisen und weitere Zuweisungen in der Liste nach unten vornehmen.

Im folgenden Szenario wird nach jeder Ausführung eines Szenarios mit ungeraden Zahlen eine E-Mail an den ersten Empfänger und nach jeder Ausführung eines Szenarios mit geraden Zahlen an den zweiten Empfänger gesendet.

![Beispiel-E-Mail](/help/workfront-fusion/references/apps-and-modules/assets/example-email.png)

So erstellen Sie dieses Szenario:

1. Stellen Sie das Feld **[!UICONTROL Wert zurücksetzen]** des Moduls auf Nie ein.
1. Route für ungerade Werte festlegen Den Filter für diese Route mit der Modulusmathematikfunktion festlegen, die `1` entspricht:

   ![Ungerade Zahlen](/help/workfront-fusion/references/apps-and-modules/assets/odd.png)

**Hinweis**: Vergessen Sie nicht, den [!UICONTROL Gleich]-Operator vom standardmäßigen [!UICONTROL Text]-Operator zum [!UICONTROL Numerisch]-Operator zu ändern.

1. Legen Sie die Route für gerade Werte mit der mathematischen Modulusfunktion fest, die `0` entspricht:

Die Inkrementfunktion fügt bei jeder Ausführung des Szenarios einen hinzu. Die Filter überprüfen das Inkrement und reagieren auf seinen Wert, um sicherzustellen, dass die E-Mails gleichmäßig verteilt werden.

>[!ENDSHADEBOX]

#### [!UICONTROL Mehrere Variablen festlegen]

Dieses Modul erstellt Variablen, die von anderen Modulen in der Route zugeordnet werden können. Die Variable kann auch den Modulen [!UICONTROL Variable abrufen] oder [!UICONTROL Mehrere Variablen abrufen] für jede Route im Szenario zugeordnet werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-Variablen]</td> 
   <td>Klicken Sie für jede Variable, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Namen und den Wert der Variablen ein.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variablenlebensdauer] </td> 
   <td> <p>Wählen Sie aus, wie lange die Variablen gültig bleiben sollen (Wert beibehalten).</p> 
    <ul> 
     <li><strong>[!UICONTROL One cycle]</strong>: Die Variable ist für einen Zyklus gültig. Dies ist nützlich, wenn mehrere Webhooks in einem Szenario ausgeführt werden, da mehr Webhooks mehr Zyklen erstellen. </li> 
     <li><strong>[!UICONTROL One execution]</strong>: Die Variable ist für die Ausführung eines einzigen Szenarios gültig. Eine Ausführung kann einen oder mehrere Zyklen enthalten.</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Variable festlegen]

Dieses Modul erstellt eine Variable, die von anderen Modulen in der Route zugeordnet werden kann. Die Variable kann auch den Modulen [!UICONTROL Variable abrufen] oder [!UICONTROL Mehrere Variablen abrufen] für jede Route im Szenario zugeordnet werden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Variablenname] </td> 
   <td>Geben Sie den Variablennamen ein. Dieser Name wird angezeigt, wenn die Variable in anderen Modulen zugeordnet wird. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variablenlebensdauer] </td> 
   <td> <p>Wählen Sie aus, wie lange die Variablen gültig bleiben sollen (Wert beibehalten).</p> 
    <ul> 
     <li><strong>[!UICONTROL One cycle]</strong>: Die Variable ist für einen Zyklus gültig. Nützlich, wenn mehrere Webhooks in einem Szenario empfangen werden (mehr Webhooks = mehr Zyklen). </li> 
     <li><strong>[!UICONTROL One execution]</strong>: Die Variable ist für die Ausführung eines einzigen Szenarios gültig. Eine Ausführung kann einen oder mehrere Zyklen enthalten.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variablenwert] </td> 
   <td>Geben Sie den Wert für die Variable ein oder ordnen Sie ihn zu. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Schlaf]

Mit diesem Modul können Sie den Szenario-Fluss um bis zu 300 Sekunden (5 Minuten) verzögern.

Diese Funktion kann beispielsweise nützlich sein, wenn Sie die Last des [!DNL target]-Service-Servers senken oder menschliches Verhalten beim Senden von Massen-SMS oder E-Mails imitieren möchten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL-Verzögerung]</p> </td> 
   <td> <p>Geben Sie die Anzahl der Sekunden ein, für die das Szenario angehalten wird.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!TIP]
>
>Wenn Sie den Fluss für längere Zeiträume anhalten möchten, empfehlen wir, Ihr Szenario in zwei Szenarien aufzuteilen:
>
>* Das erste Szenario würde den Teil vor der Pause enthalten.
>* Das zweite Szenario würde den darauffolgenden Teil enthalten.
>
>Im ersten Szenario würden alle erforderlichen Informationen zusammen mit dem aktuellen Zeitstempel in einem Datenspeicher gespeichert. Das zweite Szenario würde den Datenspeicher regelmäßig auf Datensätze mit einem Zeitstempel überprüfen, der älter als die vorgesehene Verzögerung ist, die Datensätze abrufen, die Verarbeitung der Daten abschließen und die Datensätze aus dem Datenspeicher entfernen.
>
><!--For more information on data stores, see [Data Stores in [!DNL Adobe Workfront Fusion]]().-->
>
>Weitere Informationen zu bestimmten Datenspeichermodulen finden Sie unter [[!UICONTROL Datenspeicher]-Module](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/data-store-modules.md).

### Aggregatoren

* [[!UICONTROL Numerischer Aggregator]](#numeric-aggregator)
* [[!UICONTROL Tabellenaggregator]](#table-aggregator)
* [[!UICONTROL Text-Aggregator]](#text-aggregator)

#### [!UICONTROL Numerischer Aggregator]

Mit diesem Modul können Sie numerische Werte abrufen, dann eine der ausgewählten Funktionen (SUM, AVG, COUNT, MAX, MIN) anwenden und das Ergebnis in einem Bundle zurückgeben.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source-Modul]</p> </td> 
   <td> <p>Wählen Sie das Modul aus, aus dem Sie Felder aggregieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Aggregatfunktion]</p> </td> 
   <td> <p>Wählen Sie die Funktion aus, die Sie zum Aggregieren der Werte verwenden möchten.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Gruppieren nach]</p> </td> 
   <td> <p>Definieren Sie einen Ausdruck, nach dem die aggregierte Ausgabe gruppiert werden soll. Dieser Ausdruck kann ein oder mehrere zugeordnete Elemente enthalten. Die aggregierten Daten werden dann mithilfe des -Werts dieses Ausdrucks in Gruppen aufgeteilt. Jede Gruppe gibt als separates Bundle mit einem Schlüssel (dem ausgewerteten Ausdruck) und einem Wert (dem aggregierten Wert) aus. Sie können den Schlüssel als Filter in nachfolgenden Modulen verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Verarbeitung nach einer leeren Aggregation anhalten]</td> 
   <td>Aktivieren Sie diese Option, um das Szenario zu stoppen, wenn keine Ergebnisse vorliegen.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-Wert]</p> </td> 
   <td> <p>Geben Sie den Wert ein, den Sie aggregieren möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Tabellenaggregator]

Dieses Modul führt Werte aus den ausgewählten Feldern empfangener Bundles mithilfe eines angegebenen Spalten- und Zeilentrennzeichens in einem Bundle zusammen (sodass Sie eine Tabelle erstellen können).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source-Modul]</p> </td> 
   <td> <p>Wählen Sie das Modul aus, aus dem Sie Felder aggregieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Aggregierte Felder]</td> 
   <td> <p> Wählen Sie aus dem oben ausgewählten Modul die Felder aus, die Werte enthalten, die Sie in das eine Bundle aggregieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-Spaltentrennzeichen]</p> </td> 
   <td> <p>Wählen Sie den Typ des Trennzeichens aus, das die Feldwertspalten im resultierenden Bundle trennt, oder geben Sie ihn ein. Wenn Sie [!UICONTROL Other] auswählen, geben Sie das Zeichen ein, mit dem Werte in das Feld Trennzeichen getrennt werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-Zeilentrennzeichen]</p> </td> 
   <td> <p>Wählen Sie den Typ des Trennzeichens aus, das die Zeilen mit den Feldwerten im resultierenden Bundle trennt, oder geben Sie ihn ein. Wenn Sie [!UICONTROL Other] auswählen, geben Sie das Zeichen ein, mit dem Werte in das Feld Trennzeichen getrennt werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Gruppieren nach]</p> </td> 
   <td> <p>Definieren Sie einen Ausdruck, nach dem die aggregierte Ausgabe gruppiert werden soll. Dieser Ausdruck kann ein oder mehrere zugeordnete Elemente enthalten. Die aggregierten Daten werden dann mithilfe des Werts dieses Ausdrucks in Gruppen aufgeteilt. Jede Gruppe gibt als separates Bundle mit einem Schlüssel (dem ausgewerteten Ausdruck) und einem Wert (dem aggregierten Wert) aus. Sie können den Schlüssel als Filter in nachfolgenden Modulen verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Verarbeitung nach einer leeren Aggregation anhalten]</td> 
   <td>Wählen Sie diese Option, um das Szenario anzuhalten, wenn keine Ergebnisse vorliegen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Text-Aggregator]

Dieses Modul führt Werte aus den ausgewählten Feldern empfangener Bundles in einem Bundle zusammen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source-Modul]</p> </td> 
   <td> <p>Wählen Sie das Modul aus, aus dem Sie Felder aggregieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-Zeilentrennzeichen]</p> </td> 
   <td> <p>Wählen Sie den Typ des Trennzeichens aus, das die Zeilen mit den Feldwerten im resultierenden Bundle trennt, oder geben Sie ihn ein. Wenn Sie [!UICONTROL Other] auswählen, geben Sie das Zeichen ein, mit dem Werte in das Feld Trennzeichen getrennt werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Gruppieren nach]</p> </td> 
   <td> <p>Definieren Sie einen Ausdruck, der ein oder mehrere zugeordnete Elemente enthält. Die aggregierten Daten werden unter Gruppen mit demselben Ausdruckswert getrennt. Jede Gruppe gibt als separates Bundle aus, das einen Schlüssel mit dem ausgewerteten Ausdruck und dem aggregierten Text enthält. Auf diese Weise können Sie den Schlüssel als Filter in nachfolgenden Modulen verwenden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Verarbeitung nach einer leeren Aggregation anhalten]</td> 
   <td>Wählen Sie diese Option, um das Szenario anzuhalten, wenn keine Ergebnisse vorliegen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Text]</td> 
   <td> <p> Geben Sie den Text ein, den das Modul aggregieren soll, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Beispiel** Sie können den Text-Aggregator verwenden, um weitere Werte (z. B. Kundennamen oder Notizen) in ein einzelnes Bundle einzufügen und eine E-Mail zu senden, die alle Werte im Textkörper der E-Mail oder im E-Mail-Betreff enthält.

>[!ENDSHADEBOX]

### Transformatoren

* [[!UICONTROL Zeichenfolge erstellen]](#compose-a-string)
* [[!UICONTROL Konvertiert die Textkodierung]](#convert-the-encoding-of-the-text)
* [[!UICONTROL Schalter]](#switch)

#### [!UICONTROL Zeichenfolge erstellen]

Konvertiert einen beliebigen Wert in einen Datentyp „Zeichenfolge“ (Text). Dies erleichtert die Zuordnung bei der Zuordnung von z. B. Binärdaten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Text]</td> 
   <td> <p>Geben Sie die Daten ein, die Sie in Text konvertieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Konvertiert die Textkodierung]

Konvertiert eingegebenen Eingabetext (oder Binärdaten) in die ausgewählte Codierung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Eingabedaten]</p> </td> 
   <td> <p>Geben Sie den zu konvertierenden Inhalt ein oder mappen Sie ihn.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Eingabedaten-Codepage]</td> 
   <td> <p>Wählen Sie den Kodierungstyp der Eingabedaten. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Codepage für Ausgabedaten]</p> </td> 
   <td> <p>Wählen Sie den Kodierungstyp Ihrer Ziel-(Ausgabe-)Daten aus.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Schalter]

Prüft den Eingabewert auf Übereinstimmung mit der bereitgestellten Werteliste. Gibt die Ausgabe basierend auf dem Ergebnis zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Eingabe]</p> </td> 
   <td> <p>Geben Sie den Ausdruck ein, den Sie auswerten möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Verwenden Sie reguläre Ausdrücke, um sie zuzuordnen]</td> 
   <td> <p>Aktivieren Sie diese Option, um reguläre Ausdrücke zu verwenden. Das Modul bestimmt die Groß-/Kleinschreibung anhand des regulären Ausdrucks und nicht anhand einer exakten Übereinstimmung.</p> 
    <div> 
     <p>Ein regulärer Ausdruck ist eine Sequenz von Zeichen, in der jedes Zeichen entweder ein Metazeichen mit einer speziellen Bedeutung oder ein reguläres Zeichen mit einer wörtlichen Bedeutung ist. Diese Zeichen und Metazeichen identifizieren ein Muster, das für die Suche nach Text verwendet werden kann. Wenn Sie beispielsweise nach Namen suchen möchten, können Sie einen regulären Ausdruck einrichten, um nach einem Muster zu suchen, das aus zwei aufeinander folgenden Wörtern besteht, die mit Großbuchstaben beginnen. Reguläre Ausdrücke sind ein leistungsstarkes Tool zum Suchen und Bearbeiten von Text.</p> 
     <p>Eine Diskussion über reguläre Ausdrücke würde den Rahmen dieses Artikels sprengen. Wir empfehlen die folgenden Ressourcen:</p> 
     <ul> 
      <li>Eine vollständige Liste der Metazeichen finden Sie unter <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions">Reguläre Ausdrücke</a> in MDN-Webdokumenten.</li> 
      <li>Für ein Tutorial zum Erstellen regulärer Ausdrücke empfehlen wir <a href="https://regexone.com/">RegexOne</a>.</li> 
      <li>Zum Experimentieren mit regulären Ausdrücken empfehlen wir die Website <a href="https://regex101.com/">Reguläre Ausdrücke 101</a>. Wählen Sie im linken Bedienfeld das ECMAScript (JavaScript)-FLAVOR aus.</li> 
     </ul> 
    </div> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cases] </td> 
   <td> Klicken Sie für jeden hinzuzufügenden Fall auf <b>Element hinzufügen</b> und geben Sie das Muster und die Ausgabe des Elements ein. <p>Wenn die Eingabe einen in das Feld [!UICONTROL Pattern] eingegebenen Wert enthält, wird der in das Feld [!UICONTROL Output] eingegebene Wert zurückgegeben.</p> <p>Wenn die Eingabe mit keinem der Werte übereinstimmt, die Sie in einem Feld [!UICONTROL Pattern] festgelegt haben, tritt einer der folgenden Fälle auf:</p> 
    <ul> 
     <li>Der Wert aus dem Feld [!UICONTROL Else] wird zurückgegeben</li> 
     <li>Wenn im Feld [!UICONTROL Else] kein Wert vorhanden ist, wird keine Ausgabe zurückgegeben.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL else]</p> </td> 
   <td> <p>Geben Sie den Wert ein, der zurückgegeben wird, wenn die im Feld Fälle festgelegten Kriterien nicht erfüllt sind. </p> </td> 
  </tr> 
 </tbody> 
</table>
