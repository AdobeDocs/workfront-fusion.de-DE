---
title: Token zum Parsen von Datum und Uhrzeit
description: Die folgenden Token für das Parsen von Datum und Uhrzeit sind im - [!DNL Adobe Workfront Fusion mapping]  verfügbar.
author: Becky
feature: Workfront Fusion
exl-id: d3242af3-89e8-45ae-81a1-3b4dadf824fd
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 10%

---

# Token zum Parsen von Datum und Uhrzeit

## Token für Jahr, Monat und Tag

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Eingabe </th> 
   <th>Beispiel </th> 
   <th> <p>Beschreibung</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>YYYY </code> </td> 
   <td><code>2014 </code> </td> 
   <td> <p>4- oder 2-stelliges Jahr</p> </td> 
  </tr> 
  <tr> 
   <td><code>YY</code></td> 
   <td><code>14</code></td> 
   <td> <p>2-stelliges Jahr</p> </td> 
  </tr> 
  <tr> 
   <td><code>Y</code> </td> 
   <td><code>-25</code> </td> 
   <td> <p>[!UICONTROL Year with any number of digits and sign]</p> </td> 
  </tr> 
  <tr> 
   <td><code>Q</code> </td> 
   <td><code>1..4</code> </td> 
   <td> <p> Quartal des Jahres. Setzt den Monat auf den ersten Monat im Quartal.</p> </td> 
  </tr> 
  <tr> 
   <td><code>M MM</code> </td> 
   <td><code>1..12</code> </td> 
   <td> <p> Monatszahl</p> </td> 
  </tr> 
  <tr> 
   <td><code>MMM MMMM</code> </td> 
   <td><code>Jan..December</code> </td> 
   <td> <p> Month name</p> </td> 
  </tr> 
  <tr> 
   <td><code>D DD</code> </td> 
   <td><code>1..31</code> </td> 
   <td> <p> Tag des Monats</p> </td> 
  </tr> 
  <tr> 
   <td><code>Do </code> </td> 
   <td><code>1st..31st</code> </td> 
   <td> <p> Tag des Monats mit Ordinal</p> </td> 
  </tr> 
  <tr> 
   <td><code>DDD DDDD</code> </td> 
   <td><code>1..365</code></td> 
   <td> <p> Tag des Jahres</p> </td> 
  </tr> 
  <tr> 
   <td><code>X</code> </td> 
   <td><code>1410715640.579</code> </td> 
   <td> <p> Unix-Zeitstempel</p> </td> 
  </tr> 
  <tr> 
   <td><code>x</code> </td> 
   <td><code>1410715640579</code> </td> 
   <td> <p> Unix MS-Zeitstempel</p> </td> 
  </tr> 
 </tbody> 
</table>

## Wochenzeit, Woche und Wochentag-Token

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Eingabe </th> 
   <th>Beispiel </th> 
   <th> <p>Beschreibung</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>ddd dddd</code> </td> 
   <td><code>Mon...Sunday</code> </td> 
   <td> <p> Tagesname</p> </td> 
  </tr> 
  <tr> 
   <td><code>GGGG</code> </td> 
   <td><code>2014</code> </td> 
   <td> <p> ISO 4-stellige Zahl für Woche Jahr</p> </td> 
  </tr> 
  <tr> 
   <td><code>GG </code> </td> 
   <td><code>14</code> </td> 
   <td> <p> ISO 2-stellige Zahl für Woche Jahr</p> </td> 
  </tr> 
  <tr> 
   <td><code>W WW</code> </td> 
   <td><code>1..53</code></td> 
   <td> <p> ISO-Woche des Jahres</p> </td> 
  </tr> 
  <tr> 
   <td><code>E</code> </td> 
   <td><code>1..7</code> </td> 
   <td> <p> ISO-Wochentag</p> </td> 
  </tr> 
 </tbody> 
</table>

## Token für Stunden, Minuten, Sekunden, Millisekunden und Versätze

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Eingabe </th> 
   <th>Beispiel </th> 
   <th> <p>Beschreibung</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>H HH</code> </td> 
   <td><code>0..23</code></td> 
   <td> <p> Stunden (24-Stunden-Zeit)</p> </td> 
  </tr> 
  <tr> 
   <td><code>h hh</code> </td> 
   <td><code>1..12</code> </td> 
   <td> <p> Stunden (12-Stunden-Zeit in Verbindung mit einem A.)</p> </td> 
  </tr> 
  <tr> 
   <td><code>k kk</code> </td> 
   <td><code>1..24</code> </td> 
   <td> <p> Stunden (24-Stunden-Zeit von 1 bis 24)</p> </td> 
  </tr> 
  <tr> 
   <td><code>a A</code> </td> 
   <td><code>am pm</code> </td> 
   <td> <p> Post oder ante meridiem (Beachten Sie, dass ein Zeichen a auch als gültig gilt)</p> </td> 
  </tr> 
  <tr> 
   <td><code>m mm</code> </td> 
   <td><code>0..59</code> </td> 
   <td> <p> Minuten</p> </td> 
  </tr> 
  <tr> 
   <td><code>s ss</code> </td> 
   <td><code>0..59</code> </td> 
   <td> <p> Sekunden</p> </td> 
  </tr> 
  <tr> 
   <td><code>S SS SSS</code> </td> 
   <td><code>0..999</code> </td> 
   <td> <p> Bruchsekunden</p> </td> 
  </tr> 
  <tr> 
   <td><code>Z ZZ</code> </td> 
   <td><code>+12:00</code> </td> 
   <td> <p> Versatz von UTC als +-HH:mm, +-HHmm oder Z</p> </td> 
  </tr> 
 </tbody> 
</table>
