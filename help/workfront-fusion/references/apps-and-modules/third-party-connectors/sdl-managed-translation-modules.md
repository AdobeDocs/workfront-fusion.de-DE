---
title: SDL Managed Translation Modules
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Ihr SDL Managed Translation-Konto mit mehreren Anwendungen und Dienstleistungen von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# [!DNL SDL Managed Translation]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Ihr [!DNL SDL Managed Translation]-Konto mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

## Informationen zur von SDL verwalteten Übersetzungs-API

Der SDL Managed Translation Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://languagecloud.sdl.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.4.26</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL SDL Managed Translation] Module

>[!NOTE]
>
>Das Zeitlimit für Vorgangs-Aufrufe an [!DNL SDL Managed Translation] beträgt **Sekunden**.

### Dateien

#### [!UICONTROL Download Translated File]

Dieses Modul ruft den Inhalt einer einzelnen übersetzten Datei ab, die im angegebenen Projekt enthalten ist. Wenn sich die angeforderte Datei noch nicht im Status Herunterladen befindet, ist der Inhalt der Datei möglicherweise noch nicht vollständig übersetzt. Wenn sich die Datei im Status Download befindet und Sie sie erfolgreich abgerufen haben, stellen Sie sicher, dass Sie die Datei mit der `Cancel or Complete File`-Methode als abgeschlossen markieren.

#### [!UICONTROL Upload a File]

Dieses Modul ermöglicht das Hochladen von Dateien für die Übersetzung oder die Aufnahme in ein Übersetzungsprojekt als Referenzmaterial. Uploads müssen mit multipart/form-data übermittelt werden und können mehr als eine Datei enthalten. Sie legen die `ProjectOptionId` fest, die zur Bewertung der hochgeladenen Datei(en) verwendet werden sollen. Dadurch wird bestimmt, ob jede Datei, die Sie hochladen, ein möglicher Übersetzungskandidat ist oder als Referenzmaterial gehandhabt werden muss. Bei Archiven (`zip `, `rar`, `7z`, `tar` Dateien) untersucht die App den Inhalt des Archivs und zeigt an, ob das Archiv als Ganzes übersetzt werden kann oder ob es eine Mischung aus übersetzbaren und nicht übersetzbaren Dateien enthält.

>[!NOTE]
>
>Das gleichzeitige Hochladen von mehr als einer Datei wird nicht empfohlen, da dies die Auswirkungen von Fehlern erhöhen kann.

#### [!UICONTROL Add a Reference File]

Dieses Modul fügt eine Referenzdatei hinzu.

### Projekte

#### [!UICONTROL Create a project]

Dieses Modul erstellt das angegebene Projekt.

#### Abbrechen oder Abschließen eines Projekts

Dieses Modul bricht das angegebene Projekt ab oder schließt es ab. Wenn das Projekt auf den Download wartet, durchläuft das Projekt alle letzten Schritte im Workflow und fährt schließlich bis zum Abschluss. Wenn das Projekt auf Genehmigung wartet oder die Kreditorenauswahl abgebrochen wird. Wenn sich das Projekt in einem anderen Status befindet, schlägt die Anfrage fehl.

#### [!UICONTROL Download Project Zip]

Dieses Modul ruft die `zip` der übersetzten Dateien für das angegebene Projekt ab.

#### [!UICONTROL Read a Project]

Dieses Modul ruft das angegebene Projekt ab.

#### [!UICONTROL Get Projects at Status]

Dieses Modul ruft alle verfügbaren Projekte mit dem angegebenen Status ab. Mit dieser Methode können die Ergebnisse per Paging abgerufen werden, indem `$top`-, `$skip`- und `$orderby`-Abfrageparameter angegeben werden.

#### [!UICONTROL Get Projects List]

Erstellt eine einfache Liste aller Projekte mit allgemeinen Informationen zu jedem Projekt. Mit dieser Methode können die Ergebnisse Seiten sein, indem `$top`-, `$skip`- und `$orderby`-Abfrageparameter angegeben werden.

#### [!UICONTROL Search Project Creation Options]

Dieses Modul erhält Optionen zur Projekterstellung.

### Sonstige

#### [!UICONTROL Make an API Call]

Dieses Modul führt einen beliebigen autorisierten API-Aufruf aus.
