---
title: Anzeigen einer bestimmten Szenarioausführung
description: Sie können Details zu einer bestimmten Szenario-Ausführung anzeigen, einschließlich Filtern und Suchen nach Szenario-Ereignissen.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
source-git-commit: 62b09469c1d85fd2bd1f154cde339cc4a10fc34a
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 1%

---

# Anzeigen einer bestimmten Szenarioausführung

Sie können Details zu einer bestimmten Szenario-Ausführung anzeigen, einschließlich Filtern und Suchen nach Szenario-Ereignissen.

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
   <p>Keine Workfront Fusion-Lizenzanforderung</p>
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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Anzeigen einer bestimmten Ausführung

Sie können eine Ausführung aus dem Szenarioverlauf des Szenarios anzeigen.


1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenario“ im linken Bereich und klicken Sie dann auf das Szenario.

   Oder

   Wenn Sie das Szenario im Szenario-Editor bearbeiten, klicken Sie auf den Pfeil nach links ![Pfeil zum Beenden der Bearbeitung](assets/exit-editing-arrow.png) in der oberen linken Ecke des Fensters.

1. Klicken Sie **Verlauf** neben dem Namen des Szenarios.
   ![Registerkarte „Verlauf“](assets/history-tab.png)


1. Suchen Sie die Ausführung, die Sie anzeigen möchten, und klicken **ganz rechts in der Zeile für** Ausführung auf „Details“. Der [!UICONTROL details]-Link ist nur sichtbar, wenn für die Ausführung Details verfügbar sind.

   Das Szenario-Diagramm wird geöffnet, wobei rechts das Bedienfeld Ausführungsdetails geöffnet ist.

   Module, die eine Ausgabe für diese Ausführung erzeugt haben, sind mit grünen Titeln gekennzeichnet.

   Module, die nicht ausgeführt wurden, sind abgeblendet.

1. Um die Ausgabe eines Moduls anzuzeigen, klicken Sie auf die Blase Ausgabedetails neben dem Modul. Die Zahl in der Bubble gibt die Anzahl der Bundles an, die vom Modul ausgegeben werden.

   ![Ausgabeblase in der Nähe eines Moduls](assets/output-bubble.png)

1. Um die Bundles anzuzeigen, die einen Filter durchlaufen haben, klicken Sie auf den Filter. Die Zahl in der Nähe des Filters gibt die Anzahl der Bundles an, die den Filter passiert haben.
1. Um im Ausführungsbereich nach einem bestimmten Modul oder Ereignis zu suchen, geben Sie den Suchbegriff in das Feld **Ausführungsereignisse suchen** ein. Die Ergebnisse werden während der Eingabe angezeigt.
1. Um die Suchergebnisse des Ausführungsbereichs nach Status wie Erfolg oder Warnung zu begrenzen, klicken Sie auf das **Statusfilter** und wählen Sie den Status aus.




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
