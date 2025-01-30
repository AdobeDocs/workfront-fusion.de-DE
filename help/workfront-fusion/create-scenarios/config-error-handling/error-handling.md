---
title: Hinzufügen der Fehlerbehandlung
description: Wenn bei der Ausführung eines Szenarios Fehler auftreten, liegt dies in der Regel daran, dass ein Service aufgrund eines Fehlers nicht verfügbar ist, ein Service mit unerwarteten Daten antwortet oder die Validierung der Eingabedaten fehlschlägt.
author: Becky
feature: Workfront Fusion
exl-id: 82ddaf73-ecf9-4fd6-8f8e-909351023c77
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---

# Hinzufügen der Fehlerbehandlung

Bei der Ausführung eines Szenarios können Fehler auftreten.

Ein Fehler kann beispielsweise aus folgenden Gründen auftreten:

* Ein Dienst ist aufgrund eines Fehlers nicht verfügbar
* Ein Service antwortet mit unerwarteten Daten
* Die Validierung der Eingabedaten schlägt fehl
* Andere Gründe

Wenn bei der Ausführung eines Szenarios ein Fehler auftritt und dem Modul keine Route zur Fehlerbehandlung angehängt ist, wird die standardmäßige Logik zur Fehlerbehandlung ausgeführt.

Durch Hinzufügen einer Fehler-Handler-Route zu einem Modul können Sie die standardmäßige Fehlerbehandlungslogik durch Ihre eigene ersetzen. Adobe Workfront Fusion bietet fünf verschiedene Anweisungen, die am Ende Ihrer Fehler-Handler-Routen eingefügt werden können.

Weitere Informationen zur standardmäßigen Fehlerbehandlung finden Sie unter [Fehlertypen](/help/workfront-fusion/references/errors/error-processing.md).

Weitere Informationen zu Anweisungen zur Fehlerbehandlung finden Sie unter [Anweisungen für die Fehlerbehandlung](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz</td> 
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
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
   <p>Neu:</p> <ul><li>Prime oder Workfront-Plan auswählen: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>Ultimate Workfront Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Hinzufügen eines Fehler-Handlers

So fügen Sie einem Modul einen Fehler-Handler hinzu:

1. Klicken Sie im linken Bedienfeld auf die Registerkarte **[!UICONTROL Scenarios]** .
1. Wählen Sie das Szenario aus, in dem Sie eine Fehlerbehandlungsroute hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie mit der rechten Maustaste auf das Modul, dem Sie eine Fehler-Handler-Route hinzufügen möchten, und wählen Sie **[!UICONTROL Add error handler]**:

   ![Fehler-Handler-Route](assets/error-handler-route.png)

   Dem Modul wird eine Fehler-Handler-Route hinzugefügt. Wenn das Modul das letzte Modul in einer Route ist, folgt der Fehler-Handler direkt dem Modul. Wenn das Modul danach weitere Module hat, wird eine separate Fehler-Handler-Route hinzugefügt.

   Das Modul zur Fehlerbehandlung zeigt eine Liste der Anweisungen sowie der in Ihrem Szenario verwendeten Apps an.

   ![Fehlerroute](assets/error-route.png)

1. Wählen Sie eine der Anweisungen.

   Oder

   Fügen Sie ein oder mehrere Module zur Fehler-Handler-Route hinzu.

   Wenn Sie der Route weitere Module hinzufügen, wird die Ignorieren-Direktive standardmäßig angewendet. Wenn ein Fehler auftritt, werden die nachfolgenden Module auf dieser Route verarbeitet.

   Weitere Informationen zu Anweisungen finden Sie unter [Anweisungen zur Fehlerbehandlung](#error-handling-directives) in diesem Artikel.

1. (Optional) Fügen Sie einen Filter zur Route für die Fehlerbehandlung hinzu. Anweisungen finden Sie unter [Hinzufügen von Filtern und Verschachtelungen zu Routen für die Fehlerbehandlung](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md).

>[!NOTE]
>
>Eine Route für Fehler-Handler besteht aus transparenten Kreisen, während eine reguläre Route aus durchgezogenen Kreisen besteht.

## Anweisungen zur Fehlerbehandlung

Die Richtlinien werden im Folgenden kurz erläutert. Weitere Informationen finden Sie unter [Anweisungen für die Fehlerbehandlung](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

Es gibt fünf Anweisungen, die in die folgenden Kategorien unterteilt werden können, je nachdem, ob die Ausführung eines Szenarios nach dem Fehler fortgesetzt wird.

Die folgenden Anweisungen stellen sicher, dass ein Szenario weiterhin ausgeführt wird:

* **[!UICONTROL Resume]**: Ermöglicht die Angabe einer Ersatzausgabe für das Modul mit dem Fehler. Der Ausführungsstatus des Szenarios wird als erfolgreich markiert.
* **[!UICONTROL Ignore]**: Ignoriert den Fehler. Der Ausführungsstatus des Szenarios wird als erfolgreich markiert.
* **[!UICONTROL Break]**: Speichert die Eingabe von unvollständigen Ausführungen in die Warteschlange. Der Ausführungsstatus des Szenarios wird als Warnung gekennzeichnet.

  Weitere Informationen finden Sie unter [Anzeigen und Auflösen unvollständiger Ausführungen](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Wenn die Ausführung eines Szenarios bei einem Fehler beendet werden soll, verwenden Sie eine der folgenden Anweisungen:

* **[!UICONTROL Rollback]**: Hält die Ausführung des Szenarios sofort an und markiert seinen Status als Fehler.
* **[!UICONTROL Commit]**: Hält die Ausführung des Szenarios sofort an und markiert seinen Status als Erfolg.

## Ressourcen

Weitere Informationen zur Fehlerbehandlung finden Sie unter:

* [Anweisungen für die Fehlerbehandlung in Adobe Workfront Fusion](/help/workfront-fusion/references/errors/directives-for-error-handling.md)
* [Hinzufügen von Filterung und Verschachtelung zu Fehlerbehandlungsrouten](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md)
