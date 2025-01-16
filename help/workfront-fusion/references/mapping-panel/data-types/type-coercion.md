---
title: Typzwang
description: In diesem Dokument wird beschrieben [!DNL Adobe Workfront Fusion]  wie sich in Situationen verhält, in denen es Werte in erwarteten und unerwarteten Datenformaten empfängt.
author: Becky
feature: Workfront Fusion
exl-id: a8bdd36d-c01f-4019-a3ea-fb185101500e
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 3%

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
    <td role="rowheader">[!DNL Adobe Workfront] Plan*</td> 
   <td> <p>[!DNL Pro] oder höher</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] Lizenz **</td> 
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

Weitere Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

### Typzwang

In diesem Dokument wird beschrieben, wie sich [!DNL Adobe Workfront Fusion] in Situationen verhält, in denen es Werte in erwarteten und unerwarteten Datenformaten erhält.

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
   <td>Array </td> 
   <td>Array </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Array </td> 
   <td>Sonstige </td> 
   <td> <p>Wenn der empfangene Wert nicht vom Array-Typ ist, erstellen [!DNL Workfront Fusion] ein Array und das erste (und einzige) Element ist der empfangene Wert.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolescher Wert </td> 
   <td>Boolescher Wert </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolescher Wert </td> 
   <td>Zahl </td> 
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
   <td> <p>Der Wert wird nur dann unverändert übergeben, wenn die Codepage erwartungsgemäß ist. Wenn die Codepage unterschiedlich ist, versuchen [!DNL Workfront Fusion], den empfangenen Wert in die angeforderte Codepage zu konvertieren. Wenn diese Konvertierung nicht unterstützt wird, gibt [!DNL Workfront Fusion] einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Puffer </td> 
   <td>Boolescher Wert </td> 
   <td> <p>Der Wert wird nach den oben genannten Schritten für die Umwandlung in Text in Text (true/false) und dann in Binärdaten konvertiert.</p> </td> 
  </tr> 
  <tr> 
   <td>Puffer </td> 
   <td>Datum </td> 
   <td> <p>Der Wert wird in ISO 8601-Text und anschließend in Binärdaten konvertiert, indem die für die Umwandlung in Text genannten Schritte ausgeführt werden.</p> </td> 
  </tr> 
  <tr> 
   <td>Puffer </td> 
   <td>Zahl </td> 
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
   <td> <p>[!DNL Workfront Fusion] Gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Ansammlung </td> 
   <td>Ansammlung </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Ansammlung </td> 
   <td>Sonstige </td> 
   <td> <p>[!DNL Workfront Fusion] Gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Datum </td> 
   <td>Datum </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Datum </td> 
   <td>Text </td> 
   <td> <p>[!DNL Workfront Fusion] versucht, den Text in ein Datum zu konvertieren. Wenn die Konvertierung fehlschlägt, wird ein Validierungsfehler zurückgegeben. Datum muss Tag, Monat und Jahr enthalten. Datum kann Zeit und Zeitzone enthalten. Die Standardzeitzone basiert auf Ihren Einstellungen. Beispiele:</p> <p><code>2016-06-20T17:26:44.356Z</code> </p> <p><code>2016-06-20 19:26:44 GMT+02:00</code> </p> <p><code>2016-06-20 19:26+0200</code> </p> <p><code>2016-06-20 17:26:44</code> </p> <p><code>2016-06-20</code> </p> <p><code>2016/06/20 17:26:44</code> </p> <p><code>2016/06/20 19:26:44+02:00</code> </p> <p><code>2016/06/20 17:26</code> </p> <p><code>2016/06/20 5:26 PM</code> </p> <p><code>2016/06/20</code> </p> <p><code>06/20/2016 17:26:44</code> </p> <p><code>06/20/2016 19:26:44+02:00</code> </p> <p><code>06/20/2016 17:26</code> </p> <p><code>06/20/2016 5:26 PM</code> </p> <p><code>06/20/2016</code> </p> <p><code>20.6.2016 17:26:44</code> </p> <p><code>20.6.2016 19:26:44+02:00</code> </p> <p><code>20.6.2016 17:26</code> </p> <p><code>20.6.2016</code> </p> </td> 
  </tr> 
  <tr> 
   <td>Datum </td> 
   <td>Sonstige </td> 
   <td> <p>[!DNL Workfront Fusion] Gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Zahl </td> 
   <td>Zahl </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Zahl </td> 
   <td>Text </td> 
   <td> <p>[!DNL Workfront Fusion] versucht, den Text in eine Zahl zu konvertieren. Wenn die Konvertierung fehlschlägt, wird ein Validierungsfehler zurückgegeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Zahl </td> 
   <td>Sonstige </td> 
   <td> <p>[!DNL Workfront Fusion] Gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Text </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Array </td> 
   <td> <p>Wenn das angegebene Array die Konvertierung in Text unterstützt, wird der Wert konvertiert. Andernfalls gibt [!DNL Workfront Fusion] einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Boolescher Wert </td> 
   <td> <p>Der Wert wird in Text konvertiert (true/false).</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Puffer </td> 
   <td> <p>Wenn für Binärdaten die Textkodierung angegeben ist, wird der Wert in Text konvertiert. Andernfalls gibt [!DNL Workfront Fusion] einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Datum </td> 
   <td> <p>Der Wert wird in ISO 8601-Text konvertiert.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Zahl </td> 
   <td> <p>Der Wert wird in Text konvertiert.</p> </td> 
  </tr> 
  <tr> 
   <td>Text </td> 
   <td>Sonstige </td> 
   <td> <p>[!DNL Workfront Fusion] Gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
  <tr> 
   <td>Uhrzeit </td> 
   <td>Uhrzeit </td> 
   <td> <p>Der Wert wird unverändert übergeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Uhrzeit </td> 
   <td>Text </td> 
   <td> <p>[!DNL Workfront Fusion] versucht, die Zeit in das <code>hours:minutes:seconds</code> Format zu konvertieren. Wenn die Konvertierung fehlschlägt, wird ein Validierungsfehler zurückgegeben.</p> </td> 
  </tr> 
  <tr> 
   <td>Uhrzeit </td> 
   <td>Sonstige </td> 
   <td> <p>[!DNL Workfront Fusion] Gibt einen Validierungsfehler zurück.</p> </td> 
  </tr> 
 </tbody> 
</table>
