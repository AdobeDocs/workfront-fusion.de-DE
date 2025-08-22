---
title: SOAP-Modul
description: Sie können das SOAP-Modul verwenden, um eine Verbindung zu SOAP-APIs in Adobe Workfront Fusion herzustellen.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 1%

---

# [!UICONTROL SOAP]-Modul

Sie können das Modul [!UICONTROL SOAP] verwenden, um eine Verbindung zu [!UICONTROL SOAP]-APIs in [!UICONTROL Adobe Workfront Fusion herzustellen].

## SOAP-Modul und seine Felder

Der SOAP-Connector enthält nur ein Modul: Aktion &quot;SOAP ausführen“

### SOAP-Aktion ausführen

Dieses Aktionsmodul führt die angegebene SOAP-Aktion aus.



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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Oder</p>
   <p>Legacy: Workfront Fusion für Arbeitsautomatisierung und -integration </p>
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

## SOAP-Modul und seine Felder

Beim Konfigurieren von SOAP-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an.  Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

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

## Abhilfe

Wenn das [!UICONTROL SOAP]-Modul die Verarbeitung der WSDL-Datei ablehnt oder verschiedene Fehler in der Modulkonfiguration auslöst, können Sie stattdessen das Modul Universal **[!UICONTROL HTTP] > [!UICONTROL Anfrage]** verwenden:

1. Erstellen Sie in Workfront Fusion ein neues Szenario.
1. Fügen Sie das Modul **[!UICONTROL HTTP] > [!UICONTROL Anfrage stellen]** in das Szenario ein.
1. Öffnen Sie die Konfiguration des Moduls und füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL -Methode]</td> 
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
1. Fügen Sie in Workfront Fusion die URL in das URL-Feld des HTTP-Moduls ein.
1. Öffnen Sie [Online [!UICONTROL SOAP] Client](https://wsdlbrowser.com/) in einem neuen Webbrowserfenster/-tab.
1. Fügen Sie die WSDL-URL in das Feld WSDL-URL ein.
1. Klicken Sie **[!UICONTROL Durchsuchen]**.
1. Wählen Sie aus der Liste der Funktionen links aus, z. B. `getLanguages`.
1. Kopieren Sie den Inhalt des Textbereichs [!UICONTROL Anfrage]XML).
1. Fügen Sie in [!UICONTROL Workfront Fusion] den kopierten Inhalt in das URL-Feld des Moduls ein.
1. Geben Sie Werte für ausgewählte Parameter an, indem Sie die Fragezeichen durch die tatsächlichen Werte ersetzen:

   <!--![Request](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. Schließen Sie die Modulkonfiguration, indem Sie auf **[!UICONTROL OK]** klicken.
1. Führen Sie das Szenario oder Modul aus.
