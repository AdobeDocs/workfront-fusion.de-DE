---
title: SOAP-Modul
description: Sie können das SOAP-Modul verwenden, um eine Verbindung zu SOAP-APIs in Adobe Workfront Fusion herzustellen.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
TQID: https://experienceleague.adobe.com/MIMXln44-LWfrQf0w-lZXfZJ3020Flty2CgwSC3JI9c
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 647
ht-degree: 27%

---

# [!UICONTROL SOAP]-Modul

Sie können das Modul [!UICONTROL SOAP] verwenden, um eine Verbindung zu [!UICONTROL SOAP]-APIs in [!UICONTROL Adobe Workfront Fusion herzustellen].

## SOAP-Modul und seine Felder

Der SOAP-Connector enthält nur ein Modul: Aktion &quot;SOAP ausführen“

### SOAP-Aktion ausführen

Dieses Aktionsmodul führt die angegebene SOAP-Aktion aus.



## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Ein beliebiges Adobe Workfront Workflow- und Adobe Workfront Automation and Integration-Paket</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: keine Workfront Fusion-Lizenz erforderlich</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## SOAP-Modul und seine Felder

Beim Konfigurieren von SOAP-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an.  Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### SOAP-Aktion ausführen

Dieses Aktionsmodul führt eine SOAP-Aktion basierend auf der von Ihnen angegebenen WSDL aus.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL WSDL]</td> 
   <td> Wählen Sie die WSDL aus, die das Modul verwenden soll. Um eine WSDL zu erstellen, klicken <b> auf „Hinzufügen</b> neben dem Feld und füllen Sie die Felder aus. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTTP-Kopfzeilen]</td> 
   <td> Klicken Sie für jede HTTP-Kopfzeile, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Namen und den Wert der Kopfzeile ein.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL SOAP-Kopfzeilen]</td> 
   <td> Klicken Sie für jede SOAP-Kopfzeile, die Sie hinzufügen möchten<b> auf „Element hinzufügen</b> und geben Sie den Namen, den Wert, den Namespace und das XMLNS der Kopfzeile ein.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL SOAP-Kopfzeilen erzwingen]</td> 
   <td> Aktivieren Sie diese Option, um Kopfzeilen für SOAP 1.2 zu konfigurieren. </td> 
  </tr> 
  </tbody> 
</table>

## Einschränkungen des [!UICONTROL SOAP]-Moduls

>[!NOTE]
>
>Umleitungen sind beim Laden von WSDL deaktiviert. Dies ist eine Sicherheitsfunktion, kann jedoch bedeuten, dass nicht verifizierte Weiterleitungen blockiert werden, wenn das Modul ausgeführt wird.

Das [!UICONTROL SOAP]-Modul befindet sich derzeit in der Beta-Phase und unterstützt nicht:

* Elemente neu definieren
* Einschränkungen für Bruchziffern
* Einschränkungen für Ziffernstellen insgesamt
* Einschränkungen bei Leerzeichen
* Mehrere Teile in Ein- und Ausgabemeldungen. Es werden nur Einzelteilnachrichten unterstützt
* Benutzerdefinierte XML-Schemaelemente, die mithilfe von SOAP-Kodierungsschemata und -elementen definiert wurden.

>[!BEGINSHADEBOX]

**Beispiel:**

Folgendes würde von [!UICONTROL Workfront Fusion nicht korrekt erkannt]:

```
<complexType name="ArrayOfFloat">
   <complexContent>
      <restriction base="soapenc:Array">
         <attribute ref="soapenc:arrayType"
            wsdl:arrayType="xsd:integer[]"/>
      </restriction>
   </complexContent>
</complexType>
```

Dieses Beispiel enthält die Verweise `soapenc:Array`, `soapenc:arrayType` und `wsdl:arrayType`, die in [!UICONTROL Workfront Fusion noch nicht unterstützt &#x200B;].

>[!ENDSHADEBOX]

## Problemumgehung

Wenn das [!UICONTROL SOAP]-Modul die Verarbeitung der WSDL-Datei ablehnt oder verschiedene Fehler in der Modulkonfiguration auslöst, können Sie stattdessen das Modul Universal **[!UICONTROL HTTP] > [!UICONTROL Anfrage]** verwenden:

1. Erstellen Sie in Workfront Fusion ein neues Szenario.
1. Fügen Sie das Modul **[!UICONTROL HTTP] > [!UICONTROL Anfrage stellen]** in das Szenario ein.
1. Öffnen Sie die Konfiguration des Moduls und füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Methode]</td> 
      <td> <p>[!UICONTROL POST]</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td role="rowheader">[!UICONTROL Texttyp]</td> 
      <td> <p>[!UICONTROL Roh]</p> </td>
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Content-Typ]</td> 
      <td> <p>[!UICONTROL XML (application/xml)]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Parse response]</td> 
      <td>[!UICONTROL aktiviert]</td> 
     </tr> 
    </tbody> 
   </table>

   <!--![Workaround](/help/workfront-fusion/references/apps-and-modules/assets/workaround-350x443.png)-->

1. Öffnen Sie ein neues Webbrowser-Fenster oder eine neue Registerkarte.
1. Fügen Sie die WSDL-URL in die Adressleiste des Webbrowsers ein und rufen Sie die XML-Datei ab.

   Die WSDL-URL endet normalerweise mit `?wsdl`, aber nicht notwendigerweise, z. B. `http://voip.ms/api/v1/server.wsdl`.

1. Wenn die WSDL-Datei nicht direkt im Webbrowser angezeigt wird, öffnen Sie die heruntergeladene Datei in einem Texteditor.
1. Suchen Sie nach dem `<service>`- oder `<wsdl:service>`-Tag:

   <!--![Service](/help/workfront-fusion/references/apps-and-modules/assets/service-350x65.png)-->

1. Kopieren Sie nach dem Auffinden die URL aus dem `location`.
1. Fügen Sie in Workfront Fusion die URL in das Feld (Inhalt anfragen **des HTTP-** ein.
1. Geben Sie Werte für ausgewählte Parameter an, indem Sie die Fragezeichen durch die tatsächlichen Werte ersetzen.

   >[!NOTE]
   >
   > Um bestimmte Werte aus der WSDL-Datei abzurufen, verwenden Sie einen Online-WSDL-Viewer.

   <!--![Request](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. Schließen Sie die Modulkonfiguration, indem Sie auf **[!UICONTROL OK]** klicken.
1. Führen Sie das Szenario oder Modul aus.
