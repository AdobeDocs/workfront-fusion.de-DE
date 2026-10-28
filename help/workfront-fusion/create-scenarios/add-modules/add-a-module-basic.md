---
title: Hinzufügen eines Moduls zu einem Szenario
description: In diesem Artikel wird der grundlegende Prozess zum Hinzufügen eines Moduls zu einem Szenario beschrieben.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
TQID: 'https://experienceleague.adobe.com/R2JCX7aaYzmYHgiLqj1WDlVFHI-s-qanltoOrycQ5JU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '1508'
ht-degree: 8%
---
# Hinzufügen eines Moduls zu einem Szenario

Ein Szenario besteht aus einer Reihe von Modulen, die angeben, wie Daten innerhalb einer Anwendung umgewandelt oder zwischen Anwendungen und Webservices übertragen werden sollen. Sie erstellen ein Modul, indem Sie Module hinzufügen und konfigurieren.

In diesem Artikel wird der grundlegende Prozess zum Hinzufügen eines Moduls zu einem Szenario beschrieben. Spezifischere Anweisungen dazu, wie Sie ein Szenario hinzufügen, finden Sie in den anderen Artikeln unter [Module hinzufügen: Artikelindex](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

>[!NOTE]
>
>Workfront Fusion stellt den Szenario-Editor auf ein neues Erlebnis um. Während dieser Umstellung sind sowohl die klassischen als auch die neuen Erlebnisse verfügbar und Sie können jederzeit zwischen ihnen wechseln. Es wird empfohlen, die neue -Version zu verwenden. Weitere Informationen finden Sie unter [Neue und klassische Erlebnisse](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) im Artikel Szenario-Editor.

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

## Hinzufügen des ersten Moduls zu einem Szenario

Das erste Modul eines Szenarios ist normalerweise ein Trigger-Modul.

Weitere Informationen zu Trigger-Modulen finden Sie unter [Trigger-Module](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) im Artikel Module - Übersicht.

* [Hinzufügen des ersten Moduls in der neuen -Version (empfohlen)](#add-the-first-module-in-the-new-experience-recommended)
* [Hinzufügen des ersten Moduls in der klassischen Benutzeroberfläche](#add-the-first-module-in-the-classic-experience)

### Hinzufügen des ersten Moduls in der neuen -Version (empfohlen)

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Beginnen Sie mit der Erstellung eines Szenarios **indem Sie oben** auf „Neues Szenario erstellen“ klicken.

   Der Szenario-Editor wird mit einem Platzhaltermodul und der Liste der verfügbaren Connectoren geöffnet.

   ![Platzhaltermodul](/help/workfront-fusion/build-practice-scenarios/assets/new-placeholder-module.png)

   ![App- und Service-Auswahl](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. Wählen Sie den Connector oder Webhook aus, der dieses Szenario starten soll:

   * Mithilfe des Bedienfelds auf der linken Seite nach Kategorie suchen ([!UICONTROL Favoriten], [!UICONTROL Alle Apps], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative &amp; Content], [!UICONTROL Adobe Cloud Services], [!UICONTROL Generative AI] oder [!UICONTROL integriert]) oder
   * Geben Sie einen Begriff in das Suchfeld ein. Die Ergebnisse werden während der Eingabe aktualisiert, und die Connector-Übereinstimmungen werden aufgelistet, bevor Modulname und Beschreibung übereinstimmen.

1. Klicken Sie auf das Modul, das Sie dem Szenario hinzufügen möchten.

1. Konfigurieren Sie das Modul .

   Die Einstellungen des Moduls werden im Bedienfeld auf der rechten Seite der Arbeitsfläche geöffnet.

   Anweisungen zur Konfiguration bestimmter Module finden Sie im Artikel für die ausgewählten Programme, der unter [Fusion-Programme und ihre Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md) aufgeführt ist.

>[!NOTE]
>
>* In der Liste der Connectoren identifizieren Abzeichen private, Premium- und Beta-Apps.
>* Module für große Apps sind in Gruppen unterteilt.
>* Wenn Sie einen Fehler-Handler hinzufügen, werden Anweisungen zuerst aufgeführt.
>* Wenn ein Connector mehr als eine Version aufweist, können Sie die Version auswählen, nachdem Sie den Connector ausgewählt haben.

>[!NOTE]
>
>Wenn Sie das erste Modul aus einem Szenario entfernt haben und es ersetzen möchten, klicken Sie auf das Platzhaltermodul, um die Liste der Connectoren zu öffnen.

### Hinzufügen des ersten Moduls in der klassischen Benutzeroberfläche

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

* [Hinzufügen eines weiteren Moduls in der neuen -Version (empfohlen)](#add-another-module-in-the-new-experience-recommended)
* [Hinzufügen eines weiteren Moduls im klassischen Erlebnis](#add-another-module-in-the-classic-experience)

### Hinzufügen eines weiteren Moduls in der neuen -Version (empfohlen)

1. Wenn Sie sich nicht im Szenario-Editor des Szenarios befinden, in dem Sie ein Modul hinzufügen möchten, klicken Sie auf die **[!UICONTROL Szenarios]** im linken Bedienfeld.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Um ein Modul nach einem anderen Modul hinzuzufügen, bewegen Sie den Mauszeiger über den rechten Rand des Moduls, nach dem Sie ein Modul hinzufügen möchten, und klicken Sie dann auf **Weitere Module hinzufügen** wenn es angezeigt wird.

   Die Liste der Connectoren wird geöffnet und zeigt alle bereits im Szenario verwendeten Connectoren an.

1. (Optional) Um einen anderen Connector auszuwählen, klicken **in der Liste auf „Weiteres** hinzufügen“ und wählen Sie dann den Connector aus:

   * Mithilfe des Bedienfelds auf der linken Seite nach Kategorie suchen ([!UICONTROL Favoriten], [!UICONTROL Alle Apps], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative &amp; Content], [!UICONTROL Adobe Cloud Services], [!UICONTROL Generative AI] oder [!UICONTROL integriert]) oder
   * Geben Sie einen Begriff in das Suchfeld ein. Die Ergebnisse werden während der Eingabe aktualisiert, und die Connector-Übereinstimmungen werden aufgelistet, bevor Modulname und Beschreibung übereinstimmen.

1. Klicken Sie auf das Modul, das Sie dem Szenario hinzufügen möchten.

1. Konfigurieren Sie das Modul .

   Die Einstellungen des Moduls werden im Bedienfeld auf der rechten Seite der Arbeitsfläche geöffnet.

   Anweisungen zur Konfiguration bestimmter Module finden Sie im Artikel für die ausgewählten Programme, der unter [Fusion-Programme und ihre Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md) aufgeführt ist.

### Hinzufügen eines weiteren Moduls im klassischen Erlebnis

1. Wenn Sie sich nicht im Szenario-Editor des Szenarios befinden, in dem Sie ein Modul hinzufügen möchten, klicken Sie auf die **[!UICONTROL Szenarios]** im linken Bedienfeld.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Um ein Modul zu einem anderen Modul hinzuzufügen, bewegen Sie den Mauszeiger über den rechten Griff des Moduls, nach dem Sie ein Modul hinzufügen möchten, und klicken Sie dann auf **Weitere Module hinzufügen** wenn es angezeigt wird.

   Die Liste der Connectoren wird geöffnet und zeigt alle bereits im Szenario verwendeten Connectoren an.

1. (Optional) Um einen anderen Connector auszuwählen, klicken **in der Liste auf &quot;** Modul hinzufügen“ und wählen Sie dann den Connector aus. Sie können den Namen des Connectors in die Suchleiste der Liste eingeben, um die Liste zu filtern.
1. Konfigurieren Sie das Modul .

   Anweisungen zur Konfiguration bestimmter Module finden Sie im Artikel für die ausgewählten Programme, der unter [Fusion-Programme und ihre Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md) aufgeführt ist.

## Einfügen eines Moduls zwischen vorhandenen Modulen in einem Szenario

* [Einfügen eines Moduls in die neue -Version (empfohlen)](#insert-a-module-in-the-new-experience-recommended)
* [Einfügen eines Moduls in das klassische Erlebnis](#insert-a-module-in-the-classic-experience)

### Einfügen eines Moduls in die neue -Version (empfohlen)

1. Wenn Sie sich nicht im Szenario-Editor des Szenarios befinden, in dem Sie ein Modul hinzufügen möchten, klicken Sie auf die **[!UICONTROL Szenarios]** im linken Bedienfeld.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie mit der rechten Maustaste auf den Pfad zwischen den Modulen, in denen Sie ein Modul einfügen möchten, und wählen Sie dann **Modul hinzufügen** aus.

   ![Ein Modul zwischen vorhandenen Modulen hinzufügen](assets/add-a-module-between-modules.png)

   Die Liste der Connectoren wird geöffnet und zeigt alle bereits im Szenario verwendeten Connectoren an.

1. (Optional) Um einen anderen Connector auszuwählen, klicken **in der Liste auf „Weiteres** hinzufügen“ und wählen Sie dann den Connector aus:

   * Mithilfe des Bedienfelds auf der linken Seite nach Kategorie suchen ([!UICONTROL Favoriten], [!UICONTROL Alle Apps], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative &amp; Content], [!UICONTROL Adobe Cloud Services], [!UICONTROL Generative AI] oder [!UICONTROL integriert]) oder
   * Geben Sie einen Begriff in das Suchfeld ein. Die Ergebnisse werden während der Eingabe aktualisiert, und die Connector-Übereinstimmungen werden aufgelistet, bevor Modulname und Beschreibung übereinstimmen.

1. Klicken Sie auf das Modul, das Sie dem Szenario hinzufügen möchten.

1. Konfigurieren Sie das Modul .

   Die Einstellungen des Moduls werden im Bedienfeld auf der rechten Seite der Arbeitsfläche geöffnet.

   Anweisungen zur Konfiguration bestimmter Module finden Sie im Artikel für die ausgewählten Programme, der unter [Fusion-Programme und ihre Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md) aufgeführt ist.

>[!NOTE]
>
>Um einen Link zu einem bestimmten Modul zu erstellen, fügen Sie bei der Anzeige der folgenden Seiten `?moduleId=<module-id>` zur URL hinzu:
>
>* Szenario-Bearbeitungsseite (URL endet in `/edit`)
>* Bestimmte Szenario-Ausführung (URL endet in `/logs/<log-id>`)
>
>`<module-id>` bezieht sich auf die Zahl neben der Modulbeschriftung beim Anzeigen des Szenarios.
>
>Dies kann beim Debuggen von Szenarien oder beim Kopieren der Modulkonfiguration nützlich sein.

### Einfügen eines Moduls in das klassische Erlebnis

1. Wenn Sie sich nicht im Szenario-Editor des Szenarios befinden, in dem Sie ein Modul hinzufügen möchten, klicken Sie auf die **[!UICONTROL Szenarios]** im linken Bedienfeld.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf den gepunkteten Pfad zwischen den Modulen, in denen Sie ein Modul einfügen möchten.
1. Wählen Sie im angezeigten Menü die Option **Modul hinzufügen** aus.

Die Liste der Connectoren wird geöffnet und zeigt alle bereits im Szenario verwendeten Connectoren an.

1. (Optional) Um einen anderen Connector auszuwählen, klicken **in der Liste auf &quot;** Modul hinzufügen“ und wählen Sie dann den Connector aus. Sie können den Namen des Connectors in die Suchleiste der Liste eingeben, um die Liste zu filtern.
1. Konfigurieren Sie das Modul .

   Anweisungen zur Konfiguration bestimmter Module finden Sie im Artikel für die ausgewählten Programme, der unter [Fusion-Programme und ihre Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md) aufgeführt ist.

>[!NOTE]
>
>Um einen Link zu einem bestimmten Modul zu erstellen, fügen Sie bei der Anzeige der folgenden Seiten `?moduleId=<module-id>` zur URL hinzu:
>
>* Szenario-Bearbeitungsseite (URL endet in `/edit`)
>* Bestimmte Ausführung eines Szenarios (URL endet auf `/logs/<log-id>`)
>
>`<module-id>` bezieht sich auf die Zahl neben der Modulbeschriftung beim Anzeigen des Szenarios.
>
>Dies kann beim Debuggen von Szenarien oder beim Kopieren der Modulkonfiguration nützlich sein.
