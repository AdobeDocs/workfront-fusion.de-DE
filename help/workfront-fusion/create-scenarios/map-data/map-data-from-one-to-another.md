---
title: Zuordnen von Informationen von einem Modul zu einem anderen
description: Bei der Zuordnung werden die Ausgaben eines Moduls, strukturiert in Elemente, den Eingabefeldern eines anderen Moduls zugewiesen.
author: Becky
feature: Workfront Fusion
exl-id: 1e3f7729-f48e-451e-a90b-d680c9e3bcbc
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# Zuordnen von Informationen von einem Modul zu einem anderen

Beim Mapping werden die Ausgaben eines Moduls den Eingabefeldern eines anderen Moduls zugewiesen.

Das Zuordnungsbedienfeld wird angezeigt, wenn Sie auf ein Feld klicken, in das Sie einen Wert einfügen können, der von einem vorherigen Modul in einem Szenario ausgegeben wurde.

Sie können auch eine Formel erstellen, indem Sie eine beliebige Kombination von Funktionen und zugeordneten Elementen aus dem Zuordnungsbereich mit von Ihnen eingegebenem statischem Text verwenden. Diese Elemente können ineinander geschachtelt werden.

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
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Plan für [!UICONTROL Select] oder [!UICONTROL Prime] Workfront: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>[!UICONTROL Ultimate] Workfront-Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Zuordnen eines Elements

Nachdem Sie eine Sequenz von Modulen erstellt haben, indem Sie zwei oder mehr von ihnen verknüpft haben, kann jedes Modul Werte von Elementen verarbeiten, die von den Modulen ausgegeben werden, die ihm vorausgehen.

So weisen Sie den Eingabefeldern eines Moduls Ausgabeelemente zu:

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie Daten zuordnen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf das Modul, das die Ausgabe des oder der vorhergehenden Module verarbeiten soll(en).
1. Klicken Sie im angezeigten Bedienfeld Moduleinstellungen auf ein Feld, in dem Sie den Wert eines Elements verwenden möchten, das von einem vorherigen Modul ausgegeben wurde.

   Das Zuordnungsbedienfeld wird geöffnet.

1. (Optional) Um nach einem bestimmten Feld im Zuordnungsbereich zu suchen, klicken Sie auf die Suchleiste des Zuordnungsbereichs und geben Sie den Begriff ein, nach dem Sie suchen möchten. Klicken Sie auf das Feld, wenn es in der Liste angezeigt wird.

   Suchergebnisse enthalten den Suchbegriff und unterscheiden nicht zwischen Groß- und Kleinschreibung.
1. Um einen Wert auszuwählen, der ein Element einer Sammlung ist, klicken Sie auf den Pfeil neben dieser Sammlung und wählen Sie das Element aus, wenn es angezeigt wird.

   ![Sammlungselement](assets/collection-dropdown.png)

1. Klicken Sie auf ein Element im Zuordnungsbereich, um es in das Feld einzufügen.

Weitere Informationen finden Sie unter [Modul konfigurieren](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).


## Fehlerbehebung

### Problem: Fehlende Elemente im Zuordnungsbereich

Im Zuordnungsbereich werden Ausgabeelemente aus vorherigen Modulen angezeigt. Gelegentlich fehlen einige Elemente in diesem Bedienfeld. Sie können das Modul ausführen, dem die Ausgabe im Szenario-Editor fehlt, und das Zuordnungsbedienfeld kann diese Elemente dann in späteren Modulen einbeziehen. Die genaue Vorgehensweise unterscheidet sich je nach Modultyp

* [Sofortiger Trigger](#instant-trigger)
* [Trigger wird abgerufen](#polling-trigger)
* [Andere Module](#other-modules)

#### Sofortiger Trigger

1. Klicken Sie mit der rechten Maustaste auf das Modul und klicken Sie **[!UICONTROL Nur dieses Modul ausführen]** in dem angezeigten Menü.

   Da es sich um einen sofortigen Trigger handelt, beginnt es, nach Ereignissen zu suchen.

1. Erstellen Sie das Ereignis, das vom Modul beobachtet wird.

   Wenn das Modul beispielsweise ein Modul Workfront > Ereignisse beobachten ist, das auf Aufgabenzuweisungen überwacht, melden Sie sich bei Workfront an (als Benutzer, der nicht derjenige ist, den die Fusion-Verbindung verwendet) und weisen Sie eine Aufgabe zu.

1. Wenn das Modul fertig ausgeführt wird, klicken Sie auf die Blase über dem Modul, um die vollständige Ausgabe zu überprüfen.

   Das Zuordnungsfeld für spätere Module enthält jetzt alle Elemente in der Modulausgabe.

#### Trigger wird abgerufen

1. Klicken Sie mit der rechten Maustaste auf das Modul und klicken Sie **[!UICONTROL Nur dieses Modul ausführen]** in dem angezeigten Menü.
1. Wenn keine Ausgabe vorhanden ist, klicken Sie auf **[!UICONTROL Startpunkt auswählen]** und passen Sie die Einstellungen an.
1. (Bedingt) Wenn kein zu verarbeitendes Ereignis vorhanden ist, erstellen Sie das Ereignis, das vom Modul überwacht wird, und wiederholen Sie Schritt 2.

   Wenn das Modul beispielsweise ein Modul Workfront > Datensätze beobachten ist, das auf Aufgabenzuweisungen überwacht, melden Sie sich bei Workfront an (als Benutzer, der nicht derjenige ist, den die Fusion-Verbindung verwendet) und weisen Sie eine Aufgabe zu, und führen Sie das Modul dann erneut aus.

1. Wenn das Modul fertig ausgeführt wird, klicken Sie auf die Blase über dem Modul, um die vollständige Ausgabe zu überprüfen.

   Das Zuordnungsfeld für spätere Module enthält jetzt alle Elemente in der Modulausgabe.

#### Andere Module

Sie können Folgendes ausführen:

* Das gesamte Szenario (oder nur der Teil, der das Modul enthält)
* Das einzelne Modul

So führen Sie das einzelne Modul aus:

1. Klicken Sie mit der rechten Maustaste auf das Modul und klicken Sie **[!UICONTROL Nur dieses Modul ausführen]** in dem angezeigten Menü auf..
1. Geben Sie Beispielwerte für die Eingabeelemente ein und klicken Sie dann auf **[!UICONTROL OK]** .
1. Wenn das Modul fertig ausgeführt wird, klicken Sie auf die Blase über dem Modul, um die vollständige Ausgabe zu überprüfen.

   Das Zuordnungsfeld für spätere Module enthält jetzt alle Elemente in der Modulausgabe.
