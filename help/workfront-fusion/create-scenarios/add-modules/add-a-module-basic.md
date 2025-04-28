---
title: Hinzufügen eines Moduls zu einem Szenario
description: In diesem Artikel wird der grundlegende Prozess zum Hinzufügen eines Moduls zu einem Szenario beschrieben.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
source-git-commit: 860209fdcf2e7707663cc2d454c0499972b1261e
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# Hinzufügen eines Moduls zu einem Szenario

Ein Szenario besteht aus einer Reihe von Modulen, die angeben, wie Daten innerhalb einer App transformiert oder zwischen Apps und Web-Services übertragen werden sollen. Sie erstellen ein Modul, indem Sie Module hinzufügen und konfigurieren.

In diesem Artikel wird der grundlegende Prozess zum Hinzufügen eines Moduls zu einem Szenario beschrieben. Spezifischere Anweisungen dazu, wie Sie ein Szenario hinzufügen, finden Sie in den anderen Artikeln unter [Module hinzufügen: Artikelindex](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

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
   <p>Neu:</p> <ul><li>[!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Workfront] Plan: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] kaufen.</li><li>[!UICONTROL Ultimate] [!DNL Workfront]: [!DNL Workfront Fusion] ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Hinzufügen des ersten Moduls zu einem Szenario

Das erste Modul eines Szenarios ist normalerweise ein Trigger-Modul.

Weitere Informationen zu Trigger-Modulen finden Sie unter [Trigger-Module](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) im Artikel Module - Übersicht.

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Beginnen Sie mit der Erstellung eines Szenarios **indem Sie oben** auf „Neues Szenario erstellen“ klicken.

   Der Szenario-Editor wird mit einem Platzhaltermodul (Fragezeichen) und der Liste der verfügbaren Connectoren geöffnet.

   ![Platzhaltermodul](assets/placeholder-module.png)

1. Wählen Sie den Connector oder Webhook aus, der dieses Szenario starten soll. Sie können den Namen des Connectors in die Suchleiste der Liste eingeben, um die Liste zu filtern.
1. Konfigurieren Sie das Modul .

   Anweisungen zur Konfiguration bestimmter Module finden Sie im Artikel für die ausgewählten Programme, der unter [Fusion-Programme und ihre Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md) aufgeführt ist.

>[!NOTE]
>
>Wenn Sie das erste Modul aus einem Szenario entfernt haben und es ersetzen möchten, klicken Sie auf das Modul Platzhalter (Fragezeichen) , um die Liste der Connectoren zu öffnen.

## Hinzufügen eines weiteren Moduls zu einem Szenario

1. Wenn Sie sich nicht im Szenario-Editor des Szenarios befinden, in dem Sie ein Modul hinzufügen möchten, klicken Sie auf die **[!UICONTROL Szenarios]** im linken Bedienfeld.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Um ein Modul zu einem anderen Modul hinzuzufügen, bewegen Sie den Mauszeiger über den rechten Griff des Moduls, nach dem Sie ein Modul hinzufügen möchten, und klicken Sie dann auf **Weitere Module hinzufügen** wenn es angezeigt wird.

   Die Liste der Connectoren wird geöffnet und zeigt alle bereits im Szenario verwendeten Connectoren an.

1. (Optional) Um einen anderen Connector auszuwählen, klicken **in der Liste auf &quot;** Modul hinzufügen“ und wählen Sie dann den Connector aus. Sie können den Namen des Connectors in die Suchleiste der Liste eingeben, um die Liste zu filtern.
1. Konfigurieren Sie das Modul .

   Anweisungen zur Konfiguration bestimmter Module finden Sie im Artikel für die ausgewählten Programme, der unter [Fusion-Programme und ihre Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md) aufgeführt ist.

## Einfügen eines Moduls zwischen vorhandenen Modulen in einem Szenario

1. Wenn Sie sich nicht im Szenario-Editor des Szenarios befinden, in dem Sie ein Modul hinzufügen möchten, klicken Sie auf die **[!UICONTROL Szenarios]** im linken Bedienfeld.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf den gepunkteten Pfad zwischen den Modulen, in denen Sie ein Modul einfügen möchten.
1. Wählen Sie im angezeigten Menü die Option **Modul hinzufügen** aus.

Die Liste der Connectoren wird geöffnet und zeigt alle bereits im Szenario verwendeten Connectoren an.

1. (Optional) Um einen anderen Connector auszuwählen, klicken **in der Liste auf &quot;** Modul hinzufügen“ und wählen Sie dann den Connector aus. Sie können den Namen des Connectors in die Suchleiste der Liste eingeben, um die Liste zu filtern.
1. Konfigurieren Sie das Modul .

   Anweisungen zur Konfiguration bestimmter Module finden Sie im Artikel für die ausgewählten Programme, der unter [Fusion-Programme und ihre Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md) aufgeführt ist.
