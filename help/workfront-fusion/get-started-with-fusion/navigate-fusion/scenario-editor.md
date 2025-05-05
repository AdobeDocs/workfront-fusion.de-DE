---
title: Der Szenario-Editor
description: Mit dem Szenario-Editor können Sie Szenarien in einer visuellen Benutzeroberfläche erstellen und bearbeiten.
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 3%

---

# Der Szenario-Editor

Mit dem Szenario-Editor können Sie Szenarien in einer visuellen Benutzeroberfläche erstellen und bearbeiten.

![Szenario-Editor](assets/scenario-editor.jpg)

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
   <p>Neu:</p> <ul><li>[!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Workfront]: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein [!DNL Workfront Fusion]-Administrator für Ihre Organisation sein.</p>
     <p>Sie müssen [!DNL Workfront Fusion] für Ihr Team sein.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Öffnen Sie den Szenario-Editor und fügen Sie ein Modul hinzu:

1. Klicken Sie **[!UICONTROL Scenarios]** linken ![&#128279;](assets/scenarios-icon.png) auf Szenario-Symbol).
1. Klicken Sie auf das Fragezeichensymbol ![Fragesymbol](assets/question-mark-full-size.png), suchen Sie nach der App oder dem Service, mit der bzw. dem Sie beginnen möchten, und klicken Sie darauf. Detaillierte Informationen zum Konfigurieren eines Moduls finden Sie unter [Modul konfigurieren](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

## Verfügbare Szenario-Editor-Aktionen

### Szenario ausführen

| Aktion | Details |
|----------|----------|
| Testlauf des Szenarios | Vergewissern Sie sich vor der Aktivierung, dass das Szenario erwartungsgemäß ausgeführt wird. Nach der Aktivierung wird das Szenario gemäß seinem Zeitplan ausgeführt. Wenn nicht alles wie erwartet ausgeführt wird, finden Sie unter [Fehlerbehandlung hinzufügen](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md) Informationen zum Umgang mit Fehlern. |

![Schaltfläche „Szenario ausführen“](assets/run-your-scenario.png)

### Zeitplanung

| Aktion | Details |
|----------|----------|
| Szenario planen | Standardmäßig wird ein Szenario alle 15 Minuten ausgeführt. Sie können dies ändern, indem Sie festlegen, wann und wie oft ein aktiviertes Szenario ausgeführt wird. Fusionsszenarien können so geplant werden, dass sie alle 5 Minuten ausgeführt werden. Weitere Informationen finden Sie unter [Szenario planen](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md). |

![Bedienfeld „Planung](assets/scheduling-scenario-editor.png)

### Kontrollen

| Aktion | Details |
|----------|----------|
| Speichern | Nach dem Speichern Ihres Szenarios wird eine neue Version unter dem Dreipunkt-Menü verfügbar sein, falls Sie in Zukunft darauf zugreifen müssen. Zuvor gespeicherte Szenario-Versionen sind nur für 60 Tage verfügbar. |
| Szenario-Einstellungen | Das Bedienfeld Szenario-Einstellungen enthält erweiterte Einstellungen für das Szenario. Weitere Informationen zu den verfügbaren Einstellungen finden Sie unter [Szenarioeinstellungen konfigurieren](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md). |
| Notizen | Machen Sie sich Notizen zum Szenario. Andere Benutzende können diese Notizen anzeigen, wenn sie sich im Szenario befinden. |
| Automatisch ausrichten | Automatische Ausrichtung der Module in Ihrem Szenario. |
| Fluss erläutern | Zeigen Sie eine Animation an, die zeigt, wie Daten durch das Szenario fließen. |
| Entwicklungs-Tools | Mit dem DevTool können Sie alle manuellen Ausführungen Ihres Szenarios überprüfen, alle ausgeführten Vorgänge überprüfen und die Details jedes durchgeführten API-Aufrufs anzeigen. Sie können sehen, welches Modul, welcher Vorgang oder welche einzelne Antwort den Fehler verursacht hat, und dieses Wissen verwenden, um Ihr Szenario zu verfeinern. Weitere Informationen finden Sie unter [Debuggen eines Szenarios](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md). |
| Mehr | Im Menü Mehr können Sie Blueprints importieren und exportieren und das Szenario wieder auf die vorherigen Versionen zurücksetzen. |

![Bedienfeld](assets/controls-editor-scenario.png)

### Tools

| Aktion | Details |
|----------|----------|
| Flusskontrolle | Einstellungen konfigurieren, um den Datenfluss zu steuern. Weitere Informationen finden Sie [Link erforderlich]. |
| Tools | Der Abschnitt Tools enthält mehrere nützliche Module, die Ihre Szenarien verbessern können. Weitere Informationen finden Sie [Link erforderlich]. |
| Text-Parser | Verwenden Sie das Text-Parser-Tool, um Text zur Verwendung in anderen Szenario-Modulen zu analysieren. Der Text-Parser benötigt keine Verbindung. Weitere Informationen finden Sie [Link erforderlich]. |

![Tools-Bereich](assets/tools-scenario-editor.png)

### Favoriten

Mit dem Symbol Favoriten können Sie häufig verwendete Module hinzufügen.

![Bedienfeld „Favoriten“](assets/favorites-scenario-editor.png)
