---
title: Anzeigen und Verwalten von Zeitzonen
description: Erfahren Sie, wie Sie Zeitzoneneinstellungen in Adobe Workfront Fusion anzeigen und verwalten können.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9910d9b4-5a7a-4f4a-9e66-8600d3b6c785
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 39c34b17e766678e187837e07c90b67f365a4f1d
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 17%
---
# Anzeigen und Verwalten von Zeitzonen

Adobe Workfront Fusion enthält Steuerelemente für Zeitzonen auf Unternehmens- und Benutzerebene.

* Zeitzonen der Organisation: In Szenarien werden Zeitzonen der Organisation verwendet, um zu bestimmen, wann ein geplantes Ereignis eintritt.

* Benutzer-Zeitzonen: Benutzer-Zeitzonen bestimmen die Zeit, die einem Benutzer angezeigt wird.

>[!BEGINSHADEBOX]

Beispiel:

Eine Organisation hat ihren Sitz in New York City und die Organisationszeit ist auf UTC-5 (America/New York) festgelegt. Szenario A gehört dieser Organisation und ist so geplant, dass es jeden Tag um 9:00 Uhr ausgeführt wird. Das Szenario läuft um 9:00 Uhr in der Zeitzone von New York.

Eine Benutzerin bzw. ein Benutzer in dieser Organisation lebt in Los Angeles und hat die Zeitzone ihrer/seines Benutzenden auf UTC-8 (America/Los Angeles) eingestellt. Wenn dieser Benutzer den Ausführungsverlauf des Szenarios für Szenario A anzeigt, sieht er, dass das Szenario um 6:00 Uhr morgens ausgeführt wurde. Obwohl das Szenario zu der Zeit in New York ausgeführt wurde, sieht der/die Benutzende die Zeit als in seine/ihre eigene Zeitzone umgewandelt an.

>[!ENDSHADEBOX]



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
  <tr> 
   <td role="rowheader">Zugriffsebene</td> 
   <td> Sie müssen Eigentümer oder Administrator für eine Organisation sein, um die Zeitzone für diese Organisation bearbeiten zu können. </td>
   </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Anzeigen und Verwalten der Zeitzone Ihrer Benutzer

1. Klicken Sie in Fusion auf Ihr Adobe-Profilsymbol oben rechts im Bildschirm.
1. Wählen Sie im daraufhin angezeigten Menü die Option **Fusionsprofil** aus.
1. Wählen Sie die **Zeitzonenoptionen** aus. Registerkarten befinden sich direkt unter Ihrem Namen.
Die Liste Zeitzonenoptionen wird geöffnet.
1. Suchen Sie im Web-Bereich der Liste Zeitzonenoptionen nach Ihrem Namen.

   Rechts neben Ihrem Namen wird die aktuelle Zeitzoneneinstellung des Benutzers angezeigt.
1. Klicken Sie zum Bearbeiten der Zeitzone neben ![ Zeitzone auf ](assets/edit-timezone-icon.png)Zeitzone bearbeiten“.
1. Wählen Sie im Fenster Details ändern im Feld **Zeitzone** die Zeitzone aus, die Sie für sich selbst festlegen möchten.
1. Klicken Sie auf **Speichern**.


## Anzeigen und Verwalten der Zeitzone Ihres Unternehmens

>[!NOTE]
>
>Sie müssen Eigentümer oder Administrator für eine Organisation sein, um die Zeitzone für diese Organisation bearbeiten zu können.

1. Klicken Sie in Fusion auf Ihr Adobe-Profilsymbol oben rechts im Bildschirm.
1. Wählen Sie im daraufhin angezeigten Menü die Option **Fusionsprofil** aus.
1. Wählen Sie die **Zeitzonenoptionen** aus. Registerkarten befinden sich direkt unter Ihrem Namen.
Die Liste Zeitzonenoptionen wird geöffnet.
1. Suchen Sie im Bereich Szenarien der Liste Zeitzonenoptionen die Organisation, für die Sie die Zeitzone anzeigen oder verwalten möchten.

   Die aktuelle Zeitzoneneinstellung des Unternehmens wird rechts neben dem Organisationsnamen angezeigt.
1. Klicken Sie zum Bearbeiten der Zeitzone neben ![ Zeitzone auf ](assets/edit-timezone-icon.png)Zeitzone bearbeiten“.
1. Wählen Sie im Fenster Details ändern im Feld **Zeitzone** die Zeitzone aus, die Sie für Ihre Organisation festlegen möchten.
1. Klicken Sie auf **Speichern**.


