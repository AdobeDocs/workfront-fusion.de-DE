---
title: Szenario-Versionen anzeigen und verwalten
description: Sie können Blueprints für frühere Versionen eines Szenarios anzeigen, wiederherstellen, umbenennen oder herunterladen.
author: Becky
feature: Workfront Fusion
exl-id: e7fd0351-b840-422c-b861-82ae110c703b
TQID: https://experienceleague.adobe.com/xVihxZH-fwPCIkryQAQEOWgeShtPTMXth4jEl5OLdbo
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: ac7190293e7c4b3bb9bfd48d73cd59ad687690e6
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 14%

---

# Szenario-Versionen anzeigen und verwalten

Adobe Workfront Fusion speichert bei jeder Änderung eine Version des Szenarios.

Sie können Blueprints für frühere Versionen eines Szenarios anzeigen, wiederherstellen, umbenennen oder herunterladen.

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
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Anzeigen und Verwalten des Versionsverlaufs eines Szenarios

1. Klicken Sie **[!UICONTROL linken Bereich auf]** Szenarios![Symbol](assets/scenarios-icon.png) und klicken Sie dann auf das Szenario, um es zu öffnen.
1. Klicken Sie auf [!UICONTROL Mehr]-Symbol ![Mehr](assets/more-icon.png) unten im Bildschirm und anschließend auf **[!UICONTROL Frühere Versionen]**.

   Eine Liste der vorherigen Versionen wird angezeigt.
1. (Optional) Um die Version umzubenennen, klicken Sie auf das Menü Mehr ![Mehr](assets/more-icon-vertical.png) in der Zeile für diese Version, wählen Sie **Bearbeiten** aus und geben Sie einen Namen in das Feld ein. Klicken Sie **Speichern**, um den neuen Namen zu speichern.

   Es wird empfohlen, einen Namen anzugeben, der die für diese Version vorgenommenen Änderungen beschreibt.
1. (Optional) Um den Blueprint für eine frühere Version herunterzuladen, klicken Sie auf das Menü Mehr ![Mehr](assets/more-icon-vertical.png) in der Zeile für diese Version und wählen Sie dann **Herunterladen**.
1. (Optional) Um Änderungen zwischen zwei Versionen zu vergleichen, klicken Sie auf **Änderungen anzeigen** für diese Version.

   Einzelheiten und Anweisungen zum Vergleichen von Versionen finden Sie unter [Szenario-Versionen vergleichen](#compare-scenario-versions) in diesem Artikel.
1. (Optional) Um die Version wiederherzustellen, klicken Sie in **Zeile für** Version auf „Wiederherstellen“


   >[!NOTE]
   >
   >Die wiederhergestellte Version des Szenarios wird nicht automatisch gespeichert. Wenn Sie die wiederhergestellte Version des Szenarios speichern möchten, müssen Sie sie manuell speichern.



## Szenario-Versionen vergleichen

&#x200B;
Die Funktion Änderungen anzeigen zeigt die Unterschiede zwischen zwei Szenarioversionen nebeneinander an, sodass Sie genau sehen können, welche Änderungen vorgenommen wurden, bevor Sie eine ältere wiederherstellen.

1. Klicken Sie **[!UICONTROL linken Bereich auf]** Szenarios![Symbol](assets/scenarios-icon.png) und klicken Sie dann auf das Szenario, um es zu öffnen.
1. Klicken Sie auf [!UICONTROL Mehr]-Symbol ![Mehr](assets/more-icon.png) unten im Bildschirm und anschließend auf **[!UICONTROL Frühere Versionen]**.

   Eine Liste der vorherigen Versionen wird angezeigt.
&#x200B;
1. Klicken Sie **die Szenario** Version, die Sie anzeigen möchten, auf „Änderungen anzeigen“.
1. Die **Änderungen überprüfen** wird geöffnet und vergleicht diese Version mit Ihrem aktuellen Szenario.

   Das Bedienfeld Änderungen überprüfen wird geöffnet und zeigt zwei Szenario-Versionen nebeneinander an.

   * Links sehen Sie die aktuelle Version.
   * Rechts sehen Sie die Version, auf die Sie geklickt haben. Dies ist die Version, die Sie wiederherstellen können.

   Informationen zu Änderungen finden Sie unter [Untersuchen von Änderungen](#examine-changes) in diesem Artikel.

1. Um eine andere Version für eine der Seiten auszuwählen, klicken Sie auf das **Vergleichen von** oder **Vergleichen mit** Dropdown-Menü oben im Bedienfeld und wählen Sie eine andere Szenarioversion aus.
1. Um die Seiten zu wechseln, klicken Sie zwischen den Szenarien auf die Schaltfläche **⇄**.
1. Um zum Szenario auf der rechten Seite zurückzukehren, klicken Sie auf **Auf die ausgewählte Version zurücksetzen**

   Wiederhergestellte Versionen werden als neue Versionen gespeichert und können daher in Zukunft rückgängig gemacht werden.

   Um zu dem Szenario zurückzukehren, das sich derzeit auf der linken Seite befindet, tauschen Sie die Seiten aus, sodass es sich auf der rechten Seite befindet, und klicken Sie dann auf **Auf die ausgewählte Version zurücksetzen**.


### Untersuchen von Änderungen

&#x200B;
Jede Änderung wird auf der Seite angezeigt, zu der sie gehört, und durch das gefärbt, was die Wiederherstellung tun würde
Führen Sie Folgendes aus:

* Rot (links): Diese Änderung ist nicht in der Version auf der rechten Seite und würde entfernt, wenn die Version wiederhergestellt würde.
* Grün (rechts): Diese Änderung ist in der Version auf der rechten Seite und würde hinzugefügt, wenn die Version wiederhergestellt würde.

Wenn etwas geändert wurde, wird der Wert nicht entfernt oder hinzugefügt, sondern links rot und rechts grün angezeigt.
&#x200B;
Änderungen werden in Abschnitten gruppiert:
&#x200B;

* **Szenario**: Name, Beschreibung und Typ.
* **Szenarioeinstellungen**: Zeitplan- und Verarbeitungsoptionen.
* **Modules**: Module hinzugefügt, entfernt, verschoben oder neu konfiguriert.
* **Flüsse**: Verzweigungen hinzugefügt, entfernt oder neu angeordnet.
* **Router routes**: Routen und deren Inhalte.
* **Fehler-Handler**: Verzweigungen für die Fehlerbehandlung.
* **Verwaiste Gruppen**: Nicht verbundene Module auf der Arbeitsfläche.
&#x200B;
Wenn die beiden Versionen identisch sind, zeigt die Ansicht die Meldung an **Keine Unterschiede gefunden**.
&#x200B;



