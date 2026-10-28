---
title: Hinzufügen eines Router-Moduls und Konfigurieren von Routen
description: Mit dem Router-Modul können Sie Ihren Fluss in mehrere Routen verzweigen und die Daten innerhalb jeder Route unterschiedlich verarbeiten. Sobald ein Router-Modul ein Bundle erhält, leitet es es es an jede angeschlossene Route in der Reihenfolge weiter, in der die Routen an das Router-Modul angehängt wurden.
author: Becky
feature: Workfront Fusion
exl-id: 8344cde4-df3e-4b72-9d10-46ff4b186400
TQID: 'https://experienceleague.adobe.com/ZKrvE8zGuVmfPCTMx7LZHw979aPLo89lARWejMCSETs'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '1869'
ht-degree: 6%
---
# Hinzufügen eines Router-Moduls und Konfigurieren von Routen

Mit dem Modul Router können Sie Ihr Szenario in mehrere Routen verzweigen und die Daten innerhalb jeder Route unterschiedlich verarbeiten. Wenn ein Router-Modul ein Bundle erhält, leitet es es es an jede angeschlossene Route in der Reihenfolge weiter, in der die Routen an das Router-Modul angehängt wurden.

Routen werden sequenziell verarbeitet, nicht parallel. Ein Bundle wird erst dann an die nächste Route gesendet, wenn es von der vorherigen Route vollständig verarbeitet wurde.

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

## Hinzufügen eines Router-Moduls zu einem Szenario

Sie müssen ein Router-Modul hinzufügen, bevor Sie Routen konfigurieren.

* [Hinzufügen eines Router-Moduls zu einem Szenario in der neuen -Version (empfohlen)](#add-a-router-module-to-a-scenario-in-the-new-experience-recommended)
* [Hinzufügen eines Router-Moduls zu einem Szenario in der klassischen -Version](#add-a-router-module-to-a-scenario-in-the-classic-experience)

### Hinzufügen eines Router-Moduls zu einem Szenario in der neuen -Version (empfohlen)

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Router hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Bewegen Sie den Mauszeiger über die rechte Kante des Moduls, nach dem Sie den Router hinzufügen möchten, und klicken Sie dann auf **[!UICONTROL Weitere Module hinzufügen]** wenn es angezeigt wird. Wählen Sie in der sich öffnenden Liste die Kategorie **[!UICONTROL Integriert]** und dann **[!UICONTROL Flusssteuerung]** > **[!UICONTROL Router]**.

   ODER

   Um das Router-Modul zwischen zwei Modulen einzufügen, klicken Sie mit der rechten Maustaste auf den Pfad, der die beiden Module verbindet, und wählen Sie dann **[!UICONTROL Router hinzufügen]**.

   ![Router zwischen zwei Modulen hinzufügen](assets/add-a-module-between-modules.png)

1. Fügen Sie dem Router die erste Route hinzu, indem Sie den Mauszeiger über die rechte Kante des Routers bewegen und ein Modul hinzufügen, ähnlich wie beim Hinzufügen eines beliebigen Moduls.
1. Um eine weitere Route hinzuzufügen, klicken Sie auf das Routermodul. Eine Route wird angezeigt. Fügen Sie dieser Route nach Bedarf Module hinzu.

   Sie können beliebig viele Routen hinzufügen.

1. Um die Reihenfolge der Routen zu überprüfen, überprüfen Sie das Label für jede Route. Route 1 wird zuerst ausgeführt, dann Route 2 usw.

   ODER

   Klicken Sie auf das **Auto-align**-Symbol ![Auto-align-Symbol](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/auto-align-icon-new.png) im Bereich Steuerelemente.

   Die Routen sind in der Reihenfolge ihrer Ausführung angeordnet. Die Top-Route wird zuerst ausgeführt.

1. (Optional) Klicken Sie zum Ändern der Routenreihenfolge mit der rechten Maustaste auf das Router-Modul und wählen Sie **Routen bestellen**. Ziehen Sie die Routen per Drag-and-Drop in die Reihenfolge, in der sie ausgeführt werden sollen. Routen werden durch das erste Modul markiert, das dem Router folgt (das erste Modul der Route).
1. (Optional) Um eine Route zu deaktivieren, klicken Sie mit der rechten Maustaste auf den Pfad, der vom Router zu dieser Route führt, und wählen Sie **Route deaktivieren**.

   Deaktivierte Routen zeigen graue Punkte, die vom Router zum ersten Modul auf der Route führen, und zeigen das Symbol für deaktivierte Routen ![Symbol für deaktivierte Routen](assets/disabled-route-icon.png) auf dem Titel an.

1. (Optional und bedingt) Um eine deaktivierte Route zu aktivieren, klicken Sie auf das Symbol „Deaktivierte Route![ auf ](assets/disabled-route-icon.png) Routenbeschriftung.
1. Fahren Sie [Hinzufügen eines Filters zu einer Route in der neuen -Version](#add-a-filter-to-a-route-in-the-new-experience-recommended) fort.

### Hinzufügen eines Router-Moduls zu einem Szenario in der klassischen -Version

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Router hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie im Szenario-Editor auf den rechten Griff des Moduls, nach dem Sie den Router hinzufügen möchten, und wählen Sie dann **[!UICONTROL Flusssteuerung]** > **Router** in der angezeigten Modulliste.

   ![Route verbinden](assets/connect-the-router-350x108.png)

   ODER

   Um das Router-Modul zwischen zwei Modulen einzufügen, klicken Sie auf das Schraubenschlüssel-Symbol unter der Route, die die beiden Module verbindet, und wählen Sie **[!UICONTROL Router hinzufügen]** aus dem Menü.

   ![Router einfügen](assets/insert-router-350x191.png)
1. Fügen Sie dem Router die erste Route hinzu, indem Sie auf den rechten Griff des Routers klicken und ein Modul hinzufügen, ähnlich wie beim Hinzufügen eines beliebigen Moduls.
1. Um eine weitere Route hinzuzufügen, klicken Sie auf das Routermodul. Eine Route wird angezeigt. Fügen Sie dieser Route nach Bedarf Module hinzu.

   Sie können beliebig viele Routen hinzufügen.

1. Um die Reihenfolge der Routen zu überprüfen, überprüfen Sie das Label für jede Route. Route 1 wird zuerst ausgeführt, dann Route 2 usw.

   ODER

   Klicken Sie auf das Symbol für die automatische Ausrichtung ![Symbol für die automatische Ausrichtung](assets/auto-align.png).

   Die Routen sind in der Reihenfolge ihrer Ausführung angeordnet. Die Top-Route wird zuerst ausgeführt.

1. (Optional) Um die Routenreihenfolge zu ändern, klicken Sie mit der rechten Maustaste auf das Router-Modul und wählen **Routen** bestellen“. Ziehen Sie die Routen per Drag-and-Drop in die gewünschte Reihenfolge. Routen werden durch das erste Modul markiert, das dem Router folgt (das erste Modul der Route).

   ![Bestellroute](assets/order-routes.png)

1. (Optional) Um eine Route zu deaktivieren, klicken Sie mit der rechten Maustaste auf die Punkte, die vom Router zu dieser Route führen, und wählen Sie **Route deaktivieren**.

   Deaktivierte Routen zeigen graue Punkte, die vom Router zum ersten Modul auf der Route führen, und zeigen das Symbol für deaktivierte Routen ![Symbol für deaktivierte Routen](assets/disabled-route-icon.png) auf dem Titel an.

1. (Optional und bedingt) Um eine deaktivierte Route zu aktivieren, klicken Sie auf das Symbol „Deaktivierte Route![ auf ](assets/disabled-route-icon.png) Routenbeschriftung.
1. Fahren Sie [In der klassischen -Version mit dem Schritt Filter zu einer Route hinzufügen ](#add-a-filter-to-a-route-in-the-classic-experience).

## Hinzufügen eines Filters zu einer Route

Sie können nach dem Router-Modul einen Filter für eine Route einfügen, um Pakete zu filtern. Nur Bundles, die den Filter durchlaufen, werden von den Modulen auf der Route verarbeitet.

Wenn Daten den Filter mehrerer Routen übergeben, werden die Daten von beiden Routen verarbeitet. Die Top-Route verarbeitet die Daten zuerst.

Router mit Filtern zeigen das Filtersymbol ![Filtersymbol) ](assets/fusion-scenario-filter-icon.png) Routenbeschriftung an.

* [Hinzufügen eines Filters zu einer Route in der neuen -Version (empfohlen)](#add-a-filter-to-a-route-in-the-new-experience-recommended)
* [Hinzufügen eines Filters zu einer Route in der klassischen Benutzeroberfläche](#add-a-filter-to-a-route-in-the-classic-experience)

### Hinzufügen eines Filters zu einer Route in der neuen -Version (empfohlen)

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Filter hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie mit der linken Maustaste auf den Pfad, in dem Sie einen Filter festlegen möchten. Dies ist der Pfad zwischen dem Router-Modul und dem ersten Modul der Route.

   Das **[!UICONTROL Filter einrichten]** wird direkt geöffnet.

1. Fügen Sie im Feld Titel des angezeigten Bedienfelds einen Titel hinzu. Diese Beschriftung wird im Szenario angezeigt.
1. Filterbedingungen konfigurieren.

   Weitere Informationen finden Sie unter [Hinzufügen eines Filters zu einem Szenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).

   ![Einrichten eines Filters für eine Route](assets/new-filter-specific-user.png)

1. Klicken Sie **[!UICONTROL OK]**, um die Filtereinstellungen zu speichern.
1. (Bedingt) Wenn der Filtername zu lang ist, um in die Beschriftung zu passen, bewegen Sie den Mauszeiger über die Beschriftung, um den gesamten Namen anzuzeigen.

1. Fahren Sie [Konfigurieren einer Ausweichroute in der neuen -Version](#configure-a-fallback-route-in-the-new-experience-recommended) fort.

### Hinzufügen eines Filters zu einer Route in der klassischen Benutzeroberfläche

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie einen Filter hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf das Schraubenschlüsselsymbol ![Schraubenschlüssel](assets/wrench-icon.png) in dem Pfad, in dem Sie einen Filter festlegen möchten. Dies ist der Pfad zwischen dem Router-Modul und dem ersten Modul der Route.
1. Wählen Sie **Filter einrichten.**
1. Fügen Sie im Feld Titel des angezeigten Bedienfelds einen Titel hinzu. Diese Beschriftung wird im Szenario angezeigt.
1. Filterbedingungen konfigurieren.

   Weitere Informationen finden Sie unter [Hinzufügen eines Filters zu einem Szenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).

1. Klicken Sie **[!UICONTROL OK]**, um die Filtereinstellungen zu speichern.
1. (Bedingt) Wenn der Filtername zu lang ist, um in die Beschriftung zu passen, bewegen Sie den Mauszeiger über die Beschriftung, um den gesamten Namen anzuzeigen.

1. Fahren Sie [Konfigurieren einer Ausweichroute in der klassischen ](#configure-a-fallback-route-in-the-classic-experience)) fort.

## Fallback-Route konfigurieren

Die Fallback-Route ist die Route, die für alle Bundles ausgeführt wird, die keinen Filter an eine andere Route übergeben.

Fallback-Routen zeigen auf dem Titel „Fallback“ an.

Sie können im Filterbedienfeld eine Ausweichroute aktivieren.

* [Konfigurieren einer Ausweichroute in der neuen -Version (empfohlen)](#configure-a-fallback-route-in-the-new-experience-recommended)
* [Konfigurieren einer Fallback-Route in der klassischen Benutzeroberfläche](#configure-a-fallback-route-in-the-classic-experience)

### Konfigurieren einer Ausweichroute in der neuen -Version (empfohlen)

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie eine Ausweichroute hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie mit der linken Maustaste auf den Pfad, in dem Sie einen Filter festlegen möchten. Dies ist der Pfad zwischen dem Router-Modul und dem ersten Modul der Route.

   Das **[!UICONTROL Filter einrichten]** wird direkt geöffnet.

1. Fügen Sie im Feld Titel des angezeigten Bedienfelds einen Titel hinzu. Diese Beschriftung wird im Szenario angezeigt.
1. Aktivieren Sie das Kontrollkästchen Fallback-Route .

   ![Fallback-Route](assets/fallback-route-new.png)

1. Klicken Sie **[!UICONTROL OK]**, um die Filtereinstellungen zu speichern.

Die Beschriftung der Fallback-Route wird **Fallback** grün angezeigt.

### Konfigurieren einer Fallback-Route in der klassischen Benutzeroberfläche

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie eine Ausweichroute hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf das Schraubenschlüsselsymbol ![Schraubenschlüssel](assets/wrench-icon.png) in dem Pfad, in dem Sie einen Filter festlegen möchten. Dies ist der Pfad zwischen dem Router-Modul und dem ersten Modul der Route.
1. Wählen Sie **Filter einrichten.**
1. Fügen Sie im Feld Titel des angezeigten Bedienfelds einen Titel hinzu. Diese Beschriftung wird im Szenario angezeigt.
1. Aktivieren Sie das Kontrollkästchen Fallback-Route .

   ![Fallback-Route](assets/fallback-route-350x260.png)

1. Klicken Sie **[!UICONTROL OK]**, um die Filtereinstellungen zu speichern.

Die Ausweichroute wird im Router-Modul mit einem anderen Pfeil gekennzeichnet:

![Arrow-Anmelde-Router](assets/arrow-sign-in-router-module-350x361.png)

## Falten eines Routers

>[!NOTE]
>
>Diese Funktion ist nur in der neuen Version des Szenario-Editors verfügbar.

In der neuen -Version können Sie einen Router falten, um dessen Routen vorübergehend auszublenden. Dies ist in großen Szenarien nützlich.

1. Öffnen Sie das Szenario im Szenario-Editor im Bearbeitungsmodus.
1. Klicken Sie mit der rechten Maustaste auf den Router, den Sie falten möchten, und wählen Sie dann **Routen falten**

Der gefaltete Router zeigt an, wie viele Routen und Module ausgeblendet sind, einschließlich des Schweregrads von ausgeblendeten Warnungen oder Fehlern.

![Faltrouter](assets/fold-router.png)

Durch das Falten eines Routers wird nichts entfernt oder deaktiviert. Suche, Validierung, Live-Protokoll und Ausführungsverlauf erweitern automatisch einen gefalteten Router, wenn ein darin befindliches Modul angezeigt werden soll.

Der Ordnerstatus wird mit dem Szenario gespeichert und funktioniert mit „Rückgängig“ und „Wiederherstellen“. Wenn Sie die Ausführung eines Szenarios überprüfen, wird immer das vollständige Szenario angezeigt.

## Beispiel: `if/else` Anwendungsfall

>[!BEGINSHADEBOX]

Ein typischer Anwendungsfall der Ausweichroute besteht darin, den Fluss mit einer Route fortzusetzen, wenn die Bedingung erfüllt ist, und mit einer anderen Route, wenn dies nicht der Fall ist. Wie in den folgenden Schritten:

In diesem Beispiel wird die erste Route mit einem Filter konfiguriert. Dies stellt die `if` dar.

![Richten Sie einen Filter in der Route ein](assets/new-filter-specific-user-unmarked.png)

Die zweite Route ist als Ausweichroute konfiguriert. Dies stellt die `else` dar.

![Fallback-Option aktivieren](assets/new-not-specific-user-unmarked.png)

>[!ENDSHADEBOX]
