---
title: AWS S3-Module
description: Mit  [!DNL Adobe Workfront Fusion AWS] S3-Modulen können Sie Vorgänge an Ihren S3-Buckets durchführen.
author: Becky
feature: Workfront Fusion
exl-id: 6b2d9dd5-0b33-4297-aea0-aba26072b26a
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 0%

---

# AWS S3-Module

Mit den [!DNL Adobe Workfront Fusion AWS] S3-Modulen können Sie Vorgänge an Ihren S3-Buckets durchführen.

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

## Voraussetzungen

Um [!UICONTROL AWS S3] Module verwenden zu können, müssen Sie über ein [!DNL Amazon Web Service]-Konto verfügen.

## AWS S3-API-Informationen

Der AWS S3-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://s3.{{parameters.region}}.amazonaws.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.5.21</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL AWS] mit [!DNL Workfront Fusion] verbinden {#connect-aws-to-workfront-fusion}

Um [!DNL AWS S3] mit [!DNL Workfront Fusion] zu verbinden, müssen Sie Ihr [!DNL AWS]-Konto mit [!DNL Workfront Fusion] verbinden. Dazu müssen Sie zunächst einen API-Benutzer in [!DNL AWS] [!UICONTROL IAM] erstellen.

1. Melden Sie sich bei Ihrem [!DNL AWS] [!UICONTROL IAM] Konto an.
1. Navigieren Sie zu **[!UICONTROL Identity and Access Management]** > **[!UICONTROL Access Management]** > **[!UICONTROL Users]**.

1. Klicken Sie auf **[!UICONTROL Add User]**.
1. Geben Sie den Namen des neuen Benutzers ein und wählen Sie die Option **[!UICONTROL Programmatic access]** im Abschnitt [!UICONTROL Access type] aus.
1. Klicken Sie auf **[!UICONTROL Attach existing policies directly]** und suchen Sie dann in der Suchleiste nach **[!UICONTROL AmazonS3FullAccess]**. Klicken Sie, wenn es angezeigt wird, und klicken Sie dann auf **[!UICONTROL Next]**.

1. Gehen Sie durch die anderen Dialogfelder und klicken Sie dann auf **[!UICONTROL Create User]**.
1. Kopieren Sie die bereitgestellten **[!UICONTROL Access key ID]** und **[!UICONTROL Secret access key]**.

1. Navigieren Sie zu [!DNL Workfront Fusion] und öffnen Sie das **[!UICONTROL Create a connection]**-Dialogfeld des [!DNL AWS S3].
1. Geben Sie die [!UICONTROL Access key ID] und [!UICONTROL Secret access key] aus Schritt 7 in die entsprechenden Felder ein und klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung herzustellen.

Die Verbindung wurde hergestellt. Sie können mit der Einrichtung des Moduls fortfahren.

## [!DNL AWS S3] Module und ihre Felder

Beim Konfigurieren [!DNL AWS S3] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL AWS S3] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Aktionen

* [[!UICONTROL Create Bucket]](#create-bucket)
* [[!UICONTROL Get File]](#get-file)
* [[!UICONTROL Upload File]](#upload-file)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Create Bucket]

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL AWS]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL AWS] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Geben Sie den Namen des neuen Buckets ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Wählen Sie Ihren regionalen Endpunkt aus. Weitere Informationen finden Sie in der Dokumentation zu <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html">regionalen Endpunkten</a> in AWS.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get File]

Lädt eine Datei aus einem Bucket herunter.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL AWS]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL AWS] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Wählen Sie Ihren regionalen Endpunkt aus. Weitere Informationen finden Sie in der [!DNL AWS]-Dokumentation unter <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html"> von </a>regionalen Endpunkten“.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Wählen Sie den Bucket aus, von dem Sie die Datei herunterladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Path]</p> </td> 
   <td> <p>Geben Sie den Pfad zur Datei ein. Beispiel: <code>/photos/2019/February/image023.jpg</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload File]

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL AWS]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL AWS] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Wählen Sie Ihren regionalen Endpunkt aus. Weitere Informationen finden Sie in der [!DNL AWS]-Dokumentation unter <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html"> von </a>regionalen Endpunkten“.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Folder] (optional) </p> </td> 
   <td> <p>Geben Sie den Zielordner an, in den Sie eine Datei hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers] (optional)</p> </td> 
   <td> <p> Anfrage-Header einfügen. Verfügbare Kopfzeilen finden Sie in der <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">[!DNL AWS S3]-Dokumentation - [!UICONTROL PUT] Objekt</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Eine ausführliche Erläuterung der [!DNL Amazon S3]-API finden Sie unter Einführung in [[!DNL Amazon S3] [!UICONTROL REST] API](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL AWS]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL AWS] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Region] </td> 
   <td> <p>Wählen Sie Ihren regionalen Endpunkt aus. Weitere Informationen finden Sie in der [!DNL AWS]-Dokumentation unter <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html"> von </a>regionalen Endpunkten“.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>URL Geben Sie eine Host-URL ein. Der Pfad muss relativ sein zu<code> https://s3.&lt;selected-region>.amazonaws.com/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Wählen Sie die [!UICONTROL HTTP] Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">[!UICONTROL HTTP] von Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie einen Anfrage-Header hinzu. Sie können die folgenden allgemeinen Anfragekopfzeilen verwenden. Weitere Informationen zu Anfragekopfzeilen finden Sie in <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTCommonRequestHeaders.html">[!DNL AWS S3] API-</a>.</p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> 
    <table style="table-layout:auto">
     <col> 
     <col> 
     <thead> 
      <tr> 
       <th>Header-Name</th> 
       <th> <p> Beschreibung</p> </th> 
      </tr> 
     </thead> 
     <tbody> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Length]</p> </td> 
       <td> <p>Länge der Nachricht (ohne Kopfzeilen) gemäß RFC 2616. Dieser Header ist für [!UICONTROL PUT] und Vorgänge erforderlich, die XML laden, z. B. Protokollierung und ACLs.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Type]</p> </td> 
       <td> <p>Der Content-Typ der Ressource, falls sich der Anfrageinhalt im Hauptteil befindet. Beispiel: <code>text/plain</code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-MD5]</p> </td> 
       <td> <p>Der base64-kodierte MD5-Digest der Nachricht (ohne die Header) mit 128 Bit gemäß RFC 1864. Dieser Header kann als Integritätsprüfung von Nachrichten verwendet werden, um sicherzustellen, dass es sich bei den Daten um dieselben Daten handelt, die ursprünglich gesendet wurden. Obwohl dies optional ist, empfehlen wir, den [!UICONTROL Content-MD5]-Mechanismus als End-to-End-Integritätsprüfung zu verwenden. Weitere Informationen zur Authentifizierung für [!UICONTROL REST]-Anfragen finden Sie unter <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html?r=1821">[!UICONTROL REST]-Authentifizierung </a> Entwicklerhandbuch für den <i>[!DNL Amazon] Simple Storage Service</i>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Date]</p> </td> 
       <td> <p>Das aktuelle Datum und die aktuelle Uhrzeit gemäß dem Anforderer. Beispiel: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. Wenn Sie den <code>Authorization </code>Header“ angeben, müssen Sie entweder den <code>x-amz-date</code> oder den <code>Date </code>Header“ angeben.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Expect]</p> </td> 
       <td> <p>Wenn Ihre Anwendung [!UICONTROL 100-continue] verwendet, sendet sie den Anfragetext erst, wenn sie eine Bestätigung erhält. Wenn die Nachricht anhand der Kopfzeilen abgelehnt wird, wird der Nachrichtentext nicht gesendet. Dieser Header kann nur verwendet werden, wenn Sie einen Textkörper senden.</p> <p>Gültige Werte: [!UICONTROL 100-continue]</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
       <td> <p>Bei Anfragen im Pfadstil ist der Wert <code>s3.amazonaws.com</code>. Bei Anfragen im virtuellen Stil lautet der Wert <code>BucketName.s3.amazonaws.com</code>. Weitere Informationen finden Sie unter <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/VirtualHosting.html">Virtuelles Hosting</a> im <i>[!DNL Amazon] Simple Storage Service-Entwicklerhandbuch</i>.</p> <p>Dieser Header ist für HTTP 1.1 erforderlich (die meisten Toolkits fügen diesen Header automatisch hinzu); optional für HTTP/1.0-Anfragen.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-content-sha256]</p> </td> 
       <td> <p>Wenn Sie die Signaturversion 4 zum Authentifizieren der Anfrage verwenden, liefert dieser Header einen Hash der Anfrage-Payload. Wenn Sie ein -Objekt in Blöcken hochladen, setzen Sie den Wert auf <code>STREAMING-AWS4-HMAC-SHA256-PAYLOAD</code> , um anzugeben, dass die Signatur nur Kopfzeilen abdeckt und keine Payload vorhanden ist. Weitere Informationen finden Sie unter <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-streaming.html">Signaturberechnungen für den Autorisierungs-Header: Übertragen von Payload in mehreren Blöcken (Chunked Upload) ([!DNL AWS] Signature Version 4)</a>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-date]</p> </td> 
       <td> <p>Das aktuelle Datum und die aktuelle Uhrzeit gemäß dem Anforderer. Beispiel: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. Wenn Sie den <code>Authorization </code>Header“ angeben, müssen Sie entweder den <code>x-amz-date</code> oder den <code>Date </code>Header“ angeben. Wenn Sie beide angeben, hat der für die <code>x-amz-date</code> Kopfzeile angegebene Wert Vorrang.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-security-token]</p> </td> 
       <td> <p>Dieser Header kann in den folgenden Szenarien verwendet werden:</p> 
        <ul> 
         <li>Geben Sie Sicherheits-Token für [!DNL Amazon DevPay] Vorgänge an. Für jede Anfrage, die [!DNL Amazon DevPay] verwendet, sind zwei <code>x-amz-security-token</code>-Kopfzeilen erforderlich: eine für das Produkt-Token und eine für das Benutzer-Token. Wenn [!DNL Amazon S3] eine authentifizierte Anfrage erhält, vergleicht es die berechnete Signatur mit der bereitgestellten Signatur. Falsch formatierte Kopfzeilen mit mehreren Werten, die zur Berechnung einer Signatur verwendet werden, können zu Authentifizierungsproblemen führen.</li> 
         <li>Geben Sie bei Verwendung temporärer Sicherheitsberechtigungen ein Sicherheits-Token an. Wenn Sie Anfragen mit temporären Sicherheitsanmeldeinformationen stellen, die Sie von IAM erhalten haben, müssen Sie mithilfe dieser Kopfzeile ein Sicherheits-Token angeben. Weitere Informationen zu temporären Sicherheitsberechtigungen finden Sie unter Anfragen stellen .</li> 
        </ul> <p>Dieser Header ist für Anfragen erforderlich, die [!DNL Amazon DevPay] verwenden, und für Anfragen, die mit temporären Sicherheitsberechtigungen signiert sind.</p> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Fügen Sie die gewünschten Abfragezeichenfolgen wie Parameter oder Formularfelder hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:   <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL List Files]](#list-files)
* [[!UICONTROL List Folders]](#list-folders)

#### [!UICONTROL List Files]

Gibt eine Liste mit Dateien von einem angegebenen Speicherort zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL AWS]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL AWS] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Wählen Sie Ihren regionalen Endpunkt aus. Weitere Informationen finden Sie in der [!DNL AWS]-Dokumentation unter <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html"> von </a>regionalen Endpunkten“.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Wählen Sie den [!DNL Amazon S3]-Bucket aus, nach dem Sie nach Dateien suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix] (optional)</p> </td> 
   <td> <p> Pfad zu einem Ordner, in dem Dateien nachgeschlagen werden sollen, z. B. <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Folders]

Gibt eine Liste mit Ordnern von einem angegebenen Speicherort zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL AWS]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL AWS] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Wählen Sie Ihren regionalen Endpunkt aus. Weitere Informationen finden Sie in der Dokumentation zu <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html">regionalen Endpunkten</a> in AWS.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Wählen Sie den [!DNL Amazon S3]-Bucket aus, nach dem Sie nach Ordnern suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix] (optional)</p> </td> 
   <td> <p> Pfad zu einem Ordner, in dem Ordner gesucht werden sollen, z. B. <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>
