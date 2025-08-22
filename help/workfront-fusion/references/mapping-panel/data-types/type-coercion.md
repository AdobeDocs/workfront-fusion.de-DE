---
title: Typzwang
description: In diesem Dokument wird beschrieben, wie sich Adobe Workfront Fusion in Situationen verhält, in denen es Werte in erwarteten und unerwarteten Datenformaten erhält.
author: Becky
feature: Workfront Fusion
exl-id: a8bdd36d-c01f-4019-a3ea-fb185101500e
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 6%

---

# Typzwang

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">Adobe Workfront-Plan*</td> 
   <td> <p>[!DNL Pro] oder höher</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz*</td> 
   <td> <p>[!UICONTROL-Plan], [!UICONTROL-Arbeit]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] Lizenz**</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den Plan [!UICONTROL Select] oder [!UICONTROL Prime] Adobe Workfront verfügen, muss Ihr Unternehmen Adobe Workfront Fusion sowie Adobe Workfront erwerben, um die in diesem Artikel beschriebenen Funktionen nutzen zu können. Workfront Fusion ist im Workfront-Plan [!UICONTROL Ultimate] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss Adobe Workfront Fusion sowie Adobe Workfront erwerben, um die in diesem Artikel beschriebenen Funktionen nutzen zu können.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Wenden Sie sich an Ihren Workfront-Administrator, um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

### Typzwang

In diesem Dokument wird beschrieben, wie sich Adobe Workfront Fusion in Situationen verhält, in denen es Werte in erwarteten und unerwarteten Datenformaten erhält.

<table style="table-layout:auto">
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Erwartet</th> 
   <th>Erhalten</th> 
   <th> <p>Beschreibung</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>array </td> 
   <td>array </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>array </td> 
   <td>Sonstige </td> 
   <td> <p>Wenn der empfangene Wert nicht vom Array-Typ ist, erstellt Workfront Fusion ein Array und das erste (und einzige) Element ist der empfangene Wert.</p> </td> 
  </tr> 
  <tr> 
   <td>boolean </td> 
   <td>boolean </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolescher Wert </td> 
   <td>number </td> 
   <td> <p>Der Wert wird in logisches Ja konvertiert, auch wenn der Wert 0 ist.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolescher Wert </td> 
   <td>Text </td> 
   <td> <p>Wenn der Wert gleich „false“ oder der Wert leer ist, wird er in „Logical No“ konvertiert. Wenn nicht, wird sie in ein logisches Ja konvertiert.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolescher Wert </td> 
   <td>Sonstige </td> 
   <td> <p>Der Wert wird in logisches Ja umgewandelt, wenn der empfangene Wert vorhanden ist (nicht null).</p> </td> 
  </tr> 
  <tr> 
   <td>Puffer </td> 
   <td>Puffer </td> 
   <td> <p>Der Wert wird nur dann unverändert übergeben, wenn die Codepage erwartungsgemäß ist. Wenn die Codepage unterschiedlich ist, versucht Workfront Fusion, den empfangenen Wert in die angeforderte Codepage zu konvertieren. Wenn diese Konvertierung nicht unterstützt wird, gibt Workfront Fusion einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Puffer </td> 
   <td>Boolescher Wert </td> 
   <td> <p>Der Wert wird nach den oben genannten Schritten für die Umwandlung in Text in Text (true/false) und dann in Binärdaten konvertiert.</p> </td> 
  </tr> 
  <tr> 
   <td>Puffer </td> 
   <td>date </td> 
   <td> <p>Der Wert wird in ISO 8601-Text und anschließend in Binärdaten konvertiert, indem die für die Umwandlung in Text genannten Schritte ausgeführt werden.</p> </td> 
  </tr> 
  <tr> 
   <td>Puffer </td> 
   <td>number </td> 
   <td> <p>Der Wert wird nach den oben genannten Schritten für die Umwandlung in Text in Text und dann in Binärdaten konvertiert.</p> </td> 
  </tr> 
  <tr> 
   <td>Puffer </td> 
   <td>Text </td> 
   <td> <p>Der Wert wird in Binärdaten konvertiert und erwartungsgemäß codiert. Wenn die erwartete Kodierung nicht angegeben ist, wird die UTF-8-Kodierung verwendet.</p> </td> 
  </tr> 
  <tr> 
   <td>Puffer </td> 
   <td>Sonstige </td> 
   <td> <p>Workfront Fusion gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Ansammlung </td> 
   <td>Ansammlung </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Ansammlung </td> 
   <td>Sonstige </td> 
   <td> <p>Workfront Fusion gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Datum </td> 
   <td>date </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>date </td> 
   <td>Text </td> 
   <td> <p>Workfront Fusion versucht, den Text in ein Datum zu konvertieren. Wenn die Konvertierung fehlschlägt, wird ein Validierungsfehler zurückgegeben. Datum muss Tag, Monat und Jahr enthalten. Datum kann Zeit und Zeitzone enthalten. Die Standardzeitzone basiert auf Ihren Einstellungen. Beispiele:</p> <p><code>2016-06-20T17:26:44.356Z</code> </p> <p><code>2016-06-20 19:26:44 GMT+02:00</code> </p> <p><code>2016-06-20 19:26+0200</code> </p> <p><code>2016-06-20 17:26:44</code> </p> <p><code>2016-06-20</code> </p> <p><code>2016/06/20 17:26:44</code> </p> <p><code>2016/06/20 19:26:44+02:00</code> </p> <p><code>2016/06/20 17:26</code> </p> <p><code>2016/06/20 5:26 PM</code> </p> <p><code>2016/06/20</code> </p> <p><code>06/20/2016 17:26:44</code> </p> <p><code>06/20/2016 19:26:44+02:00</code> </p> <p><code>06/20/2016 17:26</code> </p> <p><code>06/20/2016 5:26 PM</code> </p> <p><code>06/20/2016</code> </p> <p><code>20.6.2016 17:26:44</code> </p> <p><code>20.6.2016 19:26:44+02:00</code> </p> <p><code>20.6.2016 17:26</code> </p> <p><code>20.6.2016</code> </p> </td> 
  </tr> 
  <tr> 
   <td>date </td> 
   <td>Sonstige </td> 
   <td> <p>Workfront Fusion gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>number </td> 
   <td>number </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>number </td> 
   <td>Text </td> 
   <td> <p>Workfront Fusion versucht, den Text in eine Zahl zu konvertieren. Wenn die Konvertierung fehlschlägt, wird ein Validierungsfehler zurückgegeben.</p> </td> 
  </tr> 
  <tr> 
   <td>number </td> 
   <td>Sonstige </td> 
   <td> <p>Workfront Fusion gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Text </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>array </td> 
   <td> <p>Wenn das angegebene Array die Konvertierung in Text unterstützt, wird der Wert konvertiert. Andernfalls gibt Workfront Fusion einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Boolescher Wert </td> 
   <td> <p>Der Wert wird in Text konvertiert (true/false).</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Puffer </td> 
   <td> <p>Wenn für Binärdaten die Textkodierung angegeben ist, wird der Wert in Text konvertiert. Andernfalls gibt Workfront Fusion einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>date </td> 
   <td> <p>Der Wert wird in ISO 8601-Text konvertiert.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>number </td> 
   <td> <p>Der Wert wird in Text konvertiert.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Sonstige </td> 
   <td> <p>Workfront Fusion gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Uhrzeit </td> 
   <td>Uhrzeit </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Uhrzeit </td> 
   <td>Text </td> 
   <td> <p>Workfront Fusion versucht, die Zeit in das <code>hours:minutes:seconds</code> Format zu konvertieren. Wenn die Konvertierung fehlschlägt, wird ein Validierungsfehler zurückgegeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Uhrzeit </td> 
   <td>Sonstige </td> 
   <td> <p>Workfront Fusion gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
 </tbody> 
</table>
