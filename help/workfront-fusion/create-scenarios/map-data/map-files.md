---
title: Zuordnen einer Datei zwischen Modulen
description: Einige Module können Dateien verarbeiten. Diese Module können entweder eine Ausgabedatei zurückgeben, die zur weiteren Verarbeitung gesendet werden soll, oder sie erfordern, dass eine Datei zur Verarbeitung an sie übergeben wird. Bevor diese Module zusammenarbeiten können, um Dateien zu verarbeiten, müssen sie einander zugeordnet werden.
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# Zuordnen einer Datei zwischen Modulen

Einige Module können Dateien verarbeiten. Diese Module können entweder eine Ausgabedatei zur weiteren Verarbeitung zurückgeben oder verlangen, dass eine Datei zur Verarbeitung an sie übergeben wird. Dateien können zugeordnet werden, sodass eine von einem Modul ausgegebene Datei von einem anderen Modul verarbeitet werden kann.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Packstück</td> 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz</td> 
   <td> <p>Neu: [!UICONTROL Standard]</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuell: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>[!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Workfront]: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein [!DNL Workfront Fusion]-Administrator für Ihre Organisation sein.</p>
     <p>Sie müssen [!DNL Workfront Fusion] für Ihr Team sein.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Zuordnen von Dateien aus Quellmodulen zu Zielmodulen

Module können Dateien verarbeiten, die zwei Informationen erfordern:

* Dateiname
* Dateiinhalt (Daten)

Wenn vorherige Module eine Datei ausgeben, können Sie das Quellmodul auswählen. Der Name und die Daten der von diesem Modul ausgegebenen Datei werden dem Zielmodul zugeordnet.

Sie können diesen Namen und die Daten auch manuell eingeben oder aus vorherigen Modulen zuordnen. Dies kann beispielsweise beim Umbenennen einer Datei praktisch sein.

>[!NOTE]
>
>Wenn Sie eine Datei über eine URL verarbeiten müssen, empfehlen wir die Verwendung des `HTTP > Get a File`-Moduls , um die Datei über die URL herunterzuladen, und dann die Zuordnung der Datei aus dem `HTTP > Get a File`-Modul zum Feld des gewünschten Moduls in Ihrem Szenario.
>
>![Zuordnungsdatei](assets/map-source-file.png)

Zuordnen einer Datei:

1. Klicken Sie im linken Bedienfeld auf die Registerkarte **[!UICONTROL Scenarios]** .
1. Wählen Sie das Szenario aus, in dem Sie eine Datei zuordnen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Suchen Sie im Zielmodul, dem Ziel, dem Sie die Zuordnung zuordnen, den Bereich **Source-**.
1. Um eine Ausgabedatei einem vorherigen Modul zuzuordnen, wählen Sie das Modul aus, das die Datei ausgibt.

   ![Workfront-Dokument herunterladen](assets/wf-download-document.png)

1. Um den Namen und die Daten manuell zuzuordnen, wählen Sie „Zuordnen“ aus und geben Sie dann den Namen und die Daten der Datei ein bzw. ordnen Sie sie zu.

   ![Verwenden der Zuordnungsoption](assets/use-the-map-option.png)

1. Fahren Sie mit der Konfiguration des Moduls fort oder klicken Sie auf **OK**.
