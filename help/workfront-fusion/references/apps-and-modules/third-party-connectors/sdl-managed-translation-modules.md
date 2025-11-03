---
title: SDL Managed Translation Modules
description: In einem Adobe Workfront Fusion-Szenario können Sie Ihr SDL Managed Translation-Konto mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 1%

---

# [!DNL SDL Managed Translation]

In einem Adobe Workfront Fusion-Szenario können Sie Ihr [!DNL SDL Managed Translation]-Konto mit mehreren Anwendungen und Services von Drittanbietern verbinden.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

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

#### [!UICONTROL Übersetzte Datei herunterladen]

Dieses Modul ruft den Inhalt einer einzelnen übersetzten Datei ab, die im angegebenen Projekt enthalten ist. Wenn sich die angeforderte Datei noch nicht im Status Herunterladen befindet, ist der Inhalt der Datei möglicherweise noch nicht vollständig übersetzt. Wenn sich die Datei im Status Download befindet und Sie sie erfolgreich abgerufen haben, stellen Sie sicher, dass Sie die Datei mit der `Cancel or Complete File`-Methode als abgeschlossen markieren.

#### [!UICONTROL Datei hochladen]

Dieses Modul ermöglicht das Hochladen von Dateien für die Übersetzung oder die Aufnahme in ein Übersetzungsprojekt als Referenzmaterial. Uploads müssen mit multipart/form-data übermittelt werden und können mehr als eine Datei enthalten. Sie legen die `ProjectOptionId` fest, die zur Bewertung der hochgeladenen Datei(en) verwendet werden sollen. Dadurch wird bestimmt, ob jede Datei, die Sie hochladen, ein möglicher Übersetzungskandidat ist oder als Referenzmaterial gehandhabt werden muss. Bei Archiven (`zip `, `rar`, `7z`, `tar` Dateien) untersucht die App den Inhalt des Archivs und zeigt an, ob das Archiv als Ganzes übersetzt werden kann oder ob es eine Mischung aus übersetzbaren und nicht übersetzbaren Dateien enthält.

>[!NOTE]
>
>Das gleichzeitige Hochladen von mehr als einer Datei wird nicht empfohlen, da dies die Auswirkungen von Fehlern erhöhen kann.

#### [!UICONTROL Referenzdatei hinzufügen]

Dieses Modul fügt eine Referenzdatei hinzu.

### Projekte

#### [!UICONTROL Erstellen eines Projekts]

Dieses Modul erstellt das angegebene Projekt.

#### Abbrechen oder Abschließen eines Projekts

Dieses Modul bricht das angegebene Projekt ab oder schließt es ab. Wenn das Projekt auf den Download wartet, durchläuft das Projekt alle letzten Schritte im Workflow und fährt schließlich bis zum Abschluss. Wenn das Projekt auf Genehmigung wartet oder die Kreditorenauswahl abgebrochen wird. Wenn sich das Projekt in einem anderen Status befindet, schlägt die Anfrage fehl.

#### [!UICONTROL Projekt-ZIP herunterladen]

Dieses Modul ruft die `zip` der übersetzten Dateien für das angegebene Projekt ab.

#### [!UICONTROL Projekt lesen]

Dieses Modul ruft das angegebene Projekt ab.

#### [!UICONTROL Projekte mit Status abrufen]

Dieses Modul ruft alle verfügbaren Projekte mit dem angegebenen Status ab. Mit dieser Methode können die Ergebnisse per Paging abgerufen werden, indem `$top`-, `$skip`- und `$orderby`-Abfrageparameter angegeben werden.

#### [!UICONTROL Projektliste abrufen]

Erstellt eine einfache Liste aller Projekte mit allgemeinen Informationen zu jedem Projekt. Mit dieser Methode können die Ergebnisse Seiten sein, indem `$top`-, `$skip`- und `$orderby`-Abfrageparameter angegeben werden.

#### [!UICONTROL Optionen zur Projekterstellung durchsuchen]

Dieses Modul erhält Optionen zur Projekterstellung.

### Sonstiges

#### [!UICONTROL Erstellen eines API-Aufrufs]

Dieses Modul führt einen beliebigen autorisierten API-Aufruf aus.
