---
title: Datums- und Uhrzeitfunktionen
description: Die folgenden Datums- und Uhrzeitfunktionen sind im Zuordnungsbereich von Adobe Workfront Fusion verfügbar.
author: Becky
feature: Workfront Fusion
exl-id: 92813dac-4bf0-4681-9b71-7bd2e92a89a4
source-git-commit: 9249223c6fbe0360b11d41988fe8b9c35e45dbb8
workflow-type: tm+mt
source-wordcount: '1876'
ht-degree: 1%

---

# Datums- und Uhrzeitfunktionen

## Variablen

### now

Ruft die aktuelle Zeit im Format JJJJ-MM-TT-hh:mm:ss ab.

### Zeitstempel

Ruft die aktuelle Zeit als Unix-Zeitstempel ab.

## Funktionen

### [!UICONTROL addSeconds (Datum; Zahl)]

Gibt ein neues Datum zurück, nachdem einem Datum eine bestimmte Anzahl von Sekunden hinzugefügt wurde. Um Sekunden abzuziehen, geben Sie eine negative Zahl ein.

>[!BEGINSHADEBOX]

**Beispiele:**

* `addSeconds(2016-12-08T15:55:57.536Z;2)`

  Gibt 2016-12-08T15.:55:.536Z zurück

* `addSeconds(2016-12-08T15:55:57.536Z;-2)`

  Gibt 2016-12-08T15.:55:.536Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL addMinutes (Datum; Zahl)] {#addminutes-date-number}

Gibt ein neues Datum zurück, wenn einem Datum eine bestimmte Anzahl von Minuten hinzugefügt wird. Um Minuten abzuziehen, geben Sie eine negative Zahl ein.

>[!BEGINSHADEBOX]

**Beispiele:**

* `addMinutes(2016-12-08T15:55:57.536Z;2)`

  Gibt 2016-12-08T15.:57:.536Z zurück

* `addMinutes(2016-12-08T15:55:57.536Z;-2)`

  Gibt 2016-12-08T15.:53:.536Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL addHours (Datum; Zahl)] {#addhours-date-number}

Gibt ein neues Datum zurück, wenn einem Datum eine bestimmte Anzahl von Stunden hinzugefügt wird. Um Stunden abzuziehen, geben Sie eine negative Zahl ein.

>[!BEGINSHADEBOX]

**Beispiele:**

* `addHours(2016-12-08T15:55:57.536Z; 2)`

  Gibt 2016-12-08T17.:55:.536Z zurück

* `addHours(2016-12-08T15:55:57.536Z;-2)`

  Gibt 2016-12-08T13:55:57.536Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL addDays (Datum; Zahl)] {#adddays-date-number}

Gibt ein neues Datum zurück, wenn einem Datum eine bestimmte Anzahl von Tagen hinzugefügt wird. Um Tage abzuziehen, geben Sie eine negative Zahl ein.

>[!BEGINSHADEBOX]

**Beispiele:**

* `addDays(2016-12-08T15:55:57.536Z;2)`

  Gibt 2016-12-10T15.:55:.536Z zurück

* `addDays(2016-12-08T15:55:57.536Z;-2)`

  Gibt 2016-12-6T15:55:57.536Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL addMonths (Datum; Zahl)]

Gibt ein neues Datum zurück, wenn einem Datum eine bestimmte Anzahl von Monaten hinzugefügt wird. Um Monate abzuziehen, geben Sie eine negative Zahl ein.

>[!BEGINSHADEBOX]

**Beispiele:**

* `addMonths(2016-08-08T15:55:57.536Z;2)`

  Gibt 2016-10-08T15.:55:.536Z zurück

* `addMonths(2016-08-08T15:55:57.536Z;-2)`

  Gibt 2016-06-08T15.:55:.536Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL addYears (Datum; Zahl)]

Gibt ein neues Datum zurück, wenn einem Datum eine bestimmte Anzahl von Jahren hinzugefügt wird. Um Jahre abzuziehen, geben Sie eine negative Zahl ein.

>[!BEGINSHADEBOX]

**Beispiele:**

* `addYears(2016-08-08T15:55:57.536Z;2)`

  Gibt 2018-08-08T15.:55:.536Z zurück

* `addYears(2016-12-08T15:55:57.536Z; -2)`

  Gibt 2014-08-08T15.:55:.536Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL setSecond (Datum; Zahl)]

Diese Funktion gibt ein neues Datum mit den in den Parametern angegebenen Sekunden zurück.

Geben Sie eine Zahl zwischen 0 und 59 an. Wenn die Zahl außerhalb dieses Bereichs liegt, gibt die Funktion eine Sekunde aus der vorherigen Minute (für eine negative Zahl) oder der nachfolgenden Minute (für eine positive Zahl) zurück.

Wenn Sie eine Zahl außerhalb des Bereichs angeben müssen, empfehlen wir die Verwendung von [!UICONTROL addSeconds], wie oben im Abschnitt [addSeconds (date; number)](#addseconds-date-number).

>[!BEGINSHADEBOX]

**Beispiele:**

* `setSecond(2015-10-07T11:36:39.138Z;10)`

  Gibt 2015-10-07T11:36:10.138Z zurück

* `setSecond(2015-10-07T11:36:39.138Z; 61)`

  Gibt 2015-10-07T11-:37:.138Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL setMinute (Datum; Zahl)]

Diese Funktion gibt ein neues Datum mit den in den Parametern angegebenen Minuten zurück.

Geben Sie eine Zahl zwischen 0 und 59 an. Wenn die Zahl außerhalb dieses Bereichs liegt, gibt die Funktion eine Minute aus der vorherigen Stunde (für eine negative Zahl) oder der nachfolgenden Stunde (für eine positive Zahl) zurück.

Wenn Sie eine Zahl außerhalb des Bereichs angeben müssen, empfehlen wir, addMinutes zu verwenden, wie oben unter [addMinutes (date; number) beschrieben](#addminutes-date-number).

>[!BEGINSHADEBOX]

**Beispiele:**

* `setMinute(2015-10-07T11:36:39.138Z;10)`

  Gibt 2015-10-07T11-:10:.138Z zurück

* `setMinute(2015-10-07T11:36:39.138Z;61)`

  Gibt 2015-10-07T12.:01:.138Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL setHour (Datum; Zahl)]

Diese Funktion gibt ein neues Datum mit der in den Parametern angegebenen Stunde zurück.

Geben Sie eine Zahl zwischen 0 und 23 an. Wenn die Zahl außerhalb dieses Bereichs liegt, gibt die Funktion eine Stunde vom vorherigen Tag (für eine negative Zahl) oder nachfolgenden Tag (für eine positive Zahl) zurück.

Wenn Sie eine Zahl außerhalb des Bereichs angeben müssen, empfehlen wir, addHours zu verwenden, wie oben unter [addHours (date; number) beschrieben](#addhours-date-number).

>[!BEGINSHADEBOX]

**Beispiele:**

* `setHour(2015-08-07T11:36:39.138Z;6)`

  Gibt 2015-08-07T06.:36:.138Z zurück

* `setHour(2015-08-07T11:36:39.138;-6)`

  Gibt 2015-08-06T18.:36:.138Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL setDay (date; number/name of the day in English)]

Diese Funktion gibt ein neues Datum mit dem in den Parametern angegebenen Tag zurück.

Mit dieser Funktion können Sie den Wochentag festlegen, wobei „Sonntag“ den Wert „1“ und „Samstag“ den Wert „7“ hat. Wenn Sie eine Zahl zwischen 1 und 7 angeben, liegt das resultierende Datum innerhalb der aktuellen Woche (Sonntag bis Samstag). Wenn die Zahl außerhalb dieses Bereichs liegt, gibt die Funktion einen Tag aus der vorherigen Woche (für eine negative Zahl) oder der nachfolgenden Woche (für eine positive Zahl) zurück.

Wenn Sie eine Zahl außerhalb des Bereichs angeben müssen, empfehlen wir die Verwendung von addDays, wie oben unter [addDays (date; number) beschrieben](#adddays-date-number).

>[!BEGINSHADEBOX]

**Beispiele:**

* `setDay(2018-06-27T11:36:39.138Z;Monday)`

  Gibt 2018-06-25T11-:36:.138Z zurück

* `setDay(2018-06-27T11:36:39.138Z;1)`

  Gibt 2018-06-24T11-:36:.138Z zurück

* `setDay(2018-06-27T11:36:39.138Z;7)`

  Gibt 2018-06-30T11-:36:.138Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL setDate (date; number)]

Diese Funktion gibt ein neues Datum mit dem in den Parametern angegebenen Tag des Monats zurück.

Geben Sie eine Zahl zwischen 1 und 31 an. Wenn die Zahl außerhalb dieses Bereichs liegt, gibt die Funktion einen Tag aus dem vorherigen Monat (bei einer negativen Zahl) oder dem nachfolgenden Monat (bei einer positiven Zahl) zurück.

>[!BEGINSHADEBOX]

**Beispiele:**

* `setDate(2015-08-07T11:36:39.138Z;5)`

  Gibt 2015-08-05T11.:36:.138Z zurück

* `setDate(2015-08-07T11:36:39.138Z;32)`

  Gibt 2015-09-01T11-:36:.138Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL setMonth (date; number/name of the month in englischer Sprache)]

Diese Funktion gibt ein neues Datum mit dem in den Parametern angegebenen Monat zurück.

Geben Sie eine Zahl zwischen 1 und 12 an. Wenn die Zahl außerhalb dieses Bereichs liegt, gibt die Funktion den Monat des Vorjahres (bei einer negativen Zahl) oder des Folgejahres (bei einer positiven Zahl) zurück.

>[!BEGINSHADEBOX]

**Beispiele:**

* `setMonth(2015-08-07T11:36:39.138Z;5)`

  Gibt 2015-05-07T11.:36:.138Z zurück

* `setMonth(2015-08-07T11:36:39.138Z;17)`

  Gibt 2016-05-07T11.:36:.138Z zurück

* `setMonth(2015-08-07T11:36:39.138Z;january)`

  Gibt 2015-01-07T12.:36:.138Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL setYear (date;number)]

Gibt ein neues Datum mit dem in den Parametern angegebenen Jahr zurück.

>[!BEGINSHADEBOX]

**Beispiel:**

* `setYear(2015-08-07T11:36:39.138Z;2017)`

  Gibt 2017-08-07T11-:36:.138Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL formatDate (Datum; Format; [Zeitzone])]

Verwenden Sie diese Funktion, wenn Sie einen Datumswert haben, z. B. `12-10-2021 20:30`, den Sie als Textwert formatieren möchten, z. B. `Dec 10, 2021 8:30 PM`.

Dies ist beispielsweise nützlich, wenn Sie das Datumsformat einer Anwendung oder eines Webservices im selben Szenario in das Format einer verbundenen Anwendung oder eines Webservices ändern müssen.

Weitere Informationen finden Sie unter Datum und Text im Artikel [Elementdatentypen](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

#### Parameter

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Parameter</th> 
   <th>Erwarteter Datentyp* </th> 
   <th>Funktion</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL date] </td> 
   <td>Datum </td> 
   <td> <p>Konvertiert einen Datumswert in einen Textwert. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Format] </td> 
   <td>Text </td> 
   <td> <p>Ermöglicht die Angabe eines Formats mithilfe von Datums-/Uhrzeitformatierungs-Token. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md" class="MCXref xref">Token zur Datums- und Zeitformatierung</a>.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span><code>DD.MM.YYYY HH:mm</code> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL timezone] </td> 
   <td>Text </td> 
   <td> <p>(Optional) Hier können Sie die Zeitzone angeben, die für die Konvertierung verwendet wird. </p> <p>Eine Liste der erkannten Zeitzonen finden Sie in der Spalte „TZ-Datenbankname“ in der Wikipedia <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones">Liste der tz-Datenbankzeitzonen</a>. Nur die in dieser Spalte aufgelisteten Werte werden von der Funktion als gültige Zeitzone erkannt. Alle anderen Werte werden ignoriert und stattdessen wird die in Ihrem Profil angegebene Zeitzone „Szenarios“ verwendet. </p> <p>Wenn Sie diesen Parameter auslassen, wird die in Ihren Profileinstellungen angegebene Zeitzone „Szenarios“ angewendet. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span><code>Europe/Prague</code>, <code>UTC</code></p> </td> 
  </tr> 
 </tbody> 
</table>

Wenn ein anderer Typ angegeben wird, wird Typzwang angewendet. Weitere Informationen finden Sie unter [Typzwang](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

#### Rückgabewert und -typ

Die Funktion `formatDate` gibt eine Textdarstellung des angegebenen Datumswerts entsprechend dem angegebenen Format und der angegebenen Zeitzone zurück. Der Datentyp ist Text.

>[!BEGINSHADEBOX]

**Beispiele:** In diesen Beispielen wurden sowohl das Szenario als auch die Web-Zeitzone auf `Europe/Prague` festgelegt.

![Beispiel für eine Datums-/Uhrzeitfunktion](assets/date&time-functions-examples-350x61.png)

* `formatDate(1. Date created;MM/DD/YYYY)`

  Gibt 10/01/2018 zurück

* `formatDate(1. Date created; YYYY-MM-DD hh:mm A)`

  Gibt 2018-10-01 09:32 Uhr zurück

* `formatDate(1. Date created;DD.MM.YYYY HH:mm;UTC)`

  Gibt 01.10.2018 07:32 zurück

* `formatDate(now;DD.MM.YYYY HH:mm)`

  Gibt 19.03.2019 15:30 zurück

>[!ENDSHADEBOX]

### [!UICONTROL parseDate (text;format; [timezone])]

Verwenden Sie diese Funktion, wenn Sie einen Textwert haben, der ein Datum darstellt (z. B. `12-10-2019 20:30` oder `Aug 18, 2019 10:00 AM`) und Sie ihn in einen Datumswert konvertieren (parsen) möchten (eine binäre maschinenlesbare Darstellung). Weitere Informationen finden Sie unter Datum und Text im Artikel [Elementdatentypen](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

#### Parameter

Die zweite Spalte zeigt den erwarteten Typ an. Wenn ein anderer Typ angegeben wird, wird Typzwang angewendet. Weitere Informationen finden Sie unter [Typzwang](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Parameter</th> 
   <th>Erwarteter Datentyp* </th> 
   <th>Funktion</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Text] </td> 
   <td>Text </td> 
   <td> <p>Konvertiert einen Datumswert in einen Textwert. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Format] </td> 
   <td>Text </td> 
   <td> <p>Ermöglicht die Angabe eines Formats mithilfe von Datums-/Uhrzeitformatierungs-Token. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md" class="MCXref xref">Token zur Datums- und Zeitformatierung</a>.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span><code>DD.MM.YYYY HH:mm</code> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL timezone] </td> 
   <td>Text </td> 
   <td> <p>(Optional) Hier können Sie die Zeitzone angeben, die für die Konvertierung verwendet wird. </p> <p>Eine Liste der erkannten Zeitzonen finden Sie in der Spalte „TZ-Datenbankname“ in der Wikipedia <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones">Liste der tz-Datenbankzeitzonen</a>. Nur die in dieser Spalte aufgelisteten Werte werden von der Funktion als gültige Zeitzone erkannt. Alle anderen Werte werden ignoriert und stattdessen wird die in Ihrem Profil angegebene Zeitzone „Szenarios“ verwendet. </p> <p>Wenn Sie diesen Parameter auslassen, wird die in Ihren Profileinstellungen angegebene Zeitzone „Szenarios“ angewendet.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Beispiel: </b></span></span><code>Europe/Prague</code>, <code>UTC</code></p> </td> 
  </tr> 
 </tbody> 
</table>

Wenn ein anderer Typ angegeben wird, wird Typzwang angewendet. Weitere Informationen finden Sie unter [Typzwang](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

#### Rückgabewert und -typ

Diese Funktion konvertiert eine Textzeichenfolge in ein Datum, entsprechend dem Format und der Zeitzone, die Sie angeben. Der Datentyp des Werts ist Datum.

>[!BEGINSHADEBOX]

**Beispiele:** In den folgenden Beispielen wird der zurückgegebene Datumswert gemäß ISO 8601 ausgedrückt, aber der Datentyp des Ergebnisses ist „Datum“.

* `parseDate(2016-12-28;YYYY-MM-DD)`

  Gibt 2016-28T00-:00:.000Z zurück

* `parseDate(2016-12-28 16:03;YYYY-MM-DD HH:mm)`

  Gibt 2016-28-12-16.:03:.000Z zurück

* `parseDate(2016-12-28 04:03 pm; YYYY-MM-DD hh:mm a)`

  Gibt 2016-28-12-16.:03:.000Z zurück

* `parseDate(1482940986;X)`

  Gibt 2016-28-12-16.:03:.000Z zurück

>[!ENDSHADEBOX]

### [!UICONTROL dateDifference (Date1; Date2; Unit)]

Gibt eine Zahl zurück, die den Unterschied zwischen den beiden Daten darstellt, ausgedrückt in der angegebenen Einheit.

Datum2 wird von Datum1 abgezogen.

Verwenden Sie einen der folgenden Zeitwerte für den `unit`:

* Millisekunden
* Sekunden
* Minuten
* Stunden
* Tagen
* Wochen
* Monate

Wenn keine Einheit angegeben ist, gibt die Funktion die Differenz in Millisekunden zurück.

>[!BEGINSHADEBOX]

**Beispiele:**

* `dateDifference(2021-05-11T18:10:00.000Z;2021-05-11T18:00:00.000Z)`

  Gibt `600,000`

* `dateDifference(2021-05-11T18:10:00.000Z;2021-05-11T18:00:00.000Z;hours)`

  Gibt `4`

* `dateDifference2021-06-11T18:10:00.000Z;2021-05-11T18:00:00.000Z;months)`

  Gibt `1`

>[!ENDSHADEBOX]

### Zusätzliche Beispiele

#### Berechnung des n-ten Wochentags im Monat

Dieser Abschnitt ist für [!DNL Workfront Fusion] von der [!DNL Exceljet]-Webseite angepasst, in der erläutert wird, wie Sie den n-ten Wochentag in einem Monat erhalten.

Wenn Sie ein Datum berechnen müssen, das dem n-ten Wochentag im Monat entspricht (z. B. erster Dienstag, dritter Freitag usw.), können Sie die folgende Formel verwenden:

![n-ten Tag berechnen](assets/date&time-functions-calc-nth-day-350x31.png)

```
{{addDays(setDate(1.date; 1); 1.n * 7 - formatDate(addDays(setDate(1.date; 1); "-" + 1.dow); "E"))}}
```

Die Formel enthält die folgenden Elemente:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>1.n</code> </td> 
   <td> <p> N-ter Tag:</p> 
    <ul> 
     <li><code>1</code> für 1. Dienstag</li> 
     <li><code>2</code> für 2. Dienstag</li> 
     <li><code>3</code> für den 3. Dienstag usw</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td><code>2.dow</code> </td> 
   <td> <p> Wochentag:</p> 
    <ul> 
     <li><code>1</code> für Montag</li> 
     <li><code>2</code> für Dienstag</li> 
     <li><code>3</code> für Mittwoch</li> 
     <li><code>4</code> für Donnerstag</li> 
     <li><code>5</code> für Freitag</li> 
     <li><code>6</code> für Samstag</li> 
     <li><code>7</code> für Sonntag</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td><code>1.date</code> </td> 
   <td> <p> Das Datum bestimmt den Monat. Um den n-ten Wochentag im aktuellen Monat zu berechnen, verwenden Sie die Variable <code>now</code> .</p> </td> 
  </tr> 
 </tbody> 
</table>

Wenn Sie nur einen bestimmten Fall berechnen möchten, z. B. jeden zweiten Mittwoch, können Sie die Elemente `1.n` und `2.dow` in der Formel durch entsprechende Zahlen ersetzen. Für den zweiten Mittwoch im aktuellen Monat würden Sie die folgenden Werte verwenden:

* `1.n` = `2`
* `1.dow` = `3`
* `1.date` = `now`

![n-ter Tag-Variablenwert](assets/nth-day-variable-value-350x33.png)

#### Erklärung:

* `setDate(now;1)` gibt den ersten Wert des aktuellen Monats zurück
* `formatDate(....;E)` gibt den Wochentag (1, 2, … 6) zurück

### Berechnen von Tagen zwischen Datumsangaben

Eine Möglichkeit besteht darin, den folgenden Ausdruck zu verwenden:

![Tage zwischen Datumsangaben berechnen](assets/calculate-days-between-dates-350x68.png)

```
{{round((2.value - 1.value) / 1000 / 60 / 60 / 24)}}
```

>[!NOTE]
>
>* Die Werte `D1`und `D2` müssen vom Typ Datum sein. Wenn es sich um Werte vom Typ Zeichenfolge handelt (z. B. 20.10.2018), konvertieren Sie sie mit der Funktion `parseDate()` in Werte vom Typ Datum .
>
>* Die `round()`-Funktion wird für Fälle verwendet, in denen eines der Datumsangaben in den Zeitraum der Sommerzeit fällt und das andere nicht. In diesen Fällen beträgt der Stundenunterschied eine Stunde weniger oder mehr. Bei einem Ergebnis, das keine Ganzzahl ist, können Sie es durch 24 teilen. Man verliert eine Stunde der Sommerzeit. Rund flacht es, sodass man keinen Prozentsatz hat

#### Berechnung des letzten Tages/der letzten Millisekunde des Monats

Wenn Sie einen Datumsbereich angeben, z. B. in einem Suchmodul, und der Bereich den gesamten Vormonat als geschlossenes Intervall umfasst (das Intervall, das beide Endpunkte umfasst), müssen Sie den letzten Tag des Monats berechnen.

2019-09-01 ≤ D ≤ 2019-09-30

Die folgende Formel zeigt eine Möglichkeit, den letzten Tag des Vormonats zu berechnen:

![Letzter Tag des Vormonats](assets/last-day-prev-month.png)

```
{{addDays(setDate(now; 1); -1)}}
```

In einigen Fällen müssen Sie nicht nur den letzten Tag des Monats berechnen, sondern buchstäblich seine letzte Millisekunde:

2019-09-01T00:00:00.000Z ≤ D ≤ 2019-09-30T23:59:59.999Z

Diese Formel zeigt eine Möglichkeit, die letzte Millisekunde des Vormonats zu berechnen:

![Letzte Millisekunde des Vormonats](assets/last-millisecond-prev-month-350x45.png)

```
{{parseDate(parseDate(formatDate(now; "YYYYMM01"); "YYYYMMDD"; "UTC") - 1; "x")}}
```

Wenn Sie das Ergebnis benötigen, um Ihre Zeitzoneneinstellung zu verwenden, lassen Sie das UTC-Argument weg:

![UTC auslassen](assets/omit-utc-argument-350x45.png)

`{{parseDate(parseDate(formatDate(now; "YYYYMM01"); "YYYYMMDD") - 1; "x")}}`

Es ist jedoch vorzuziehen, stattdessen das halb offene Intervall zu verwenden (das Intervall, das einen seiner Grenzpunkte ausschließt), wobei stattdessen der erste Tag des folgenden Monats angegeben wird und der Operator „kleiner oder gleich“ durch „kleiner als“ wie folgt ersetzt wird:

`2019-09-01 ≤ D < 2019-10-01`

`2019-09-01T00:00:00.000Z ≤ D < 2019-10-01T00:00:00.000Z`
