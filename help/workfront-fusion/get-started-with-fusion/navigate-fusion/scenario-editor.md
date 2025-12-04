---
title: Der Szenario-Editor
description: Mit dem Szenario-Editor können Sie Szenarien in einer visuellen Benutzeroberfläche erstellen und bearbeiten.
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: f968b9141173725160cea36575ad4e02a09a5e3f
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 17%

---

# Der Szenario-Editor

Mit dem Szenario-Editor können Sie Szenarien in einer visuellen Benutzeroberfläche erstellen und bearbeiten.

![Szenario-Editor](assets/scenario-editor.jpg)

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Paket für Adobe Workfront Workflow und Workfront Automation and Integration</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Adobe Workfront Fusion erworben werden.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Angaben in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Öffnen Sie den Szenario-Editor und fügen Sie ein Modul hinzu:

1. Klicken Sie **[!UICONTROL linken Bedienfeld]** Szenarios![ (](assets/scenarios-icon.png)).
1. Klicken Sie auf das Fragezeichensymbol ![Fragesymbol](assets/question-mark-full-size.png), suchen Sie nach der App oder dem Service, mit der bzw. dem Sie beginnen möchten, und klicken Sie darauf. Detaillierte Informationen zum Konfigurieren eines Moduls finden Sie unter [Modul konfigurieren](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

## Verfügbare Szenario-Editor-Aktionen

### Szenario ausführen

| Aktion | Details |
|----------|----------|
| Testlauf des Szenarios | Vergewissern Sie sich vor der Aktivierung, dass das Szenario erwartungsgemäß ausgeführt wird. Nach der Aktivierung wird das Szenario gemäß seinem Zeitplan ausgeführt. Wenn nicht alles wie erwartet ausgeführt wird, finden Sie unter [Fehlerbehandlung hinzufügen](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md) Informationen zum Umgang mit Fehlern. |

![Schaltfläche „Szenario ausführen“](assets/run-your-scenario.png)

### Planung

| Aktion | Details |
|----------|----------|
| Szenario planen | Standardmäßig wird ein Szenario alle 15 Minuten ausgeführt. Sie können dies ändern, indem Sie festlegen, wann und wie oft ein aktiviertes Szenario ausgeführt wird. Fusionsszenarien können so geplant werden, dass sie alle 5 Minuten ausgeführt werden. Weitere Informationen finden Sie unter [Szenario planen](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md). |

![Bedienfeld „Planung](assets/scheduling-scenario-editor.png)

### Steuerelemente

Möglicherweise müssen Sie auf das Dreipunkt-Symbol im Bereich Steuerelemente klicken, um einige dieser Steuerelemente anzuzeigen.

| Aktion | Details |
|----------|----------|
| Speichern Sie. <p>![Speichersymbol](assets/save-icon.png)</p> | Nach dem Speichern Ihres Szenarios wird eine neue Version unter dem Dreipunkt-Menü verfügbar sein, falls Sie in Zukunft darauf zugreifen müssen. Zuvor gespeicherte Szenario-Versionen sind nur für 60 Tage verfügbar. |
| Szenario-Einstellungen <p>![Symbol für Szenario-Einstellungen](assets/scenario-settings-icon.png)</p> | Das Bedienfeld Szenario-Einstellungen enthält erweiterte Einstellungen für das Szenario. Weitere Informationen zu den verfügbaren Einstellungen finden Sie unter [Szenarioeinstellungen konfigurieren](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md). |
| Anmerkungen  <p>![Notizensymbol](assets/notes-icon.png)</p> | Machen Sie sich Notizen zum Szenario. Andere Benutzende können diese Notizen anzeigen, wenn sie sich im Szenario befinden. |
| Automatisch ausrichten <p>![Symbol für automatische Ausrichtung](assets/auto-align-icon.png)</p> | Automatische Ausrichtung der Module in Ihrem Szenario. |
| Suchmodule ![Suchmodule](assets/search-modules-icon.png)  </p> | Geben Sie einen Suchbegriff ein, um ein Modul zu finden, und klicken Sie dann auf die Suchergebnisse, um zu diesem Modul zu gelangen. Sie können nach Modulnamen, ID, Typ oder Anwendung suchen. |
| Fluss erläutern  <p>![Flusssymbol erläutern](assets/explain-flow-icon.png) </p> | Zeigen Sie eine Animation an, in der bewegte Punkte zeigen, wie Daten durch das Szenario fließen. |
| DevTool <p>![DevTool-Symbol](assets/devtool-icon.png)</p> | Mit dem DevTool können Sie alle manuellen Ausführungen Ihres Szenarios überprüfen, alle ausgeführten Vorgänge überprüfen und die Details jedes durchgeführten API-Aufrufs anzeigen. Sie können sehen, welches Modul, welcher Vorgang oder welche einzelne Antwort den Fehler verursacht hat, und dieses Wissen verwenden, um Ihr Szenario zu verfeinern. Weitere Informationen finden Sie unter [Debuggen eines Szenarios](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md). |
| Blueprint exportieren  <p>![Blueprint-Symbol exportieren](assets/export-blueprint-icon.png) </p> | Exportiert einen Blueprint des aktuellen Szenarios. |
| Blueprint importieren  <p>![Blueprint-Symbol importieren](assets/import-blueprint-icon.png) </p> | Importieren Sie eine zuvor exportierte Szenario-Blueprint. |
| Vorherige Version  <p>![Symbol für vorherige Version](assets//previous-version-icon.png) </p> | Frühere Versionen dieses Szenarios anzeigen. |

![Bedienfeld](assets/controls-editor-scenario.png)

### Tools

| Aktion | Details |
|----------|----------|
| Flusssteuerung | Einstellungen konfigurieren, um den Datenfluss zu steuern. Weitere Informationen finden Sie [Link erforderlich]. |
| Tools | Der Abschnitt Tools enthält mehrere nützliche Module, die Ihre Szenarien verbessern können. Weitere Informationen finden Sie [Link erforderlich]. |
| Text-Parser | Verwenden Sie das Text-Parser-Tool, um Text zur Verwendung in anderen Szenario-Modulen zu analysieren. Der Text-Parser benötigt keine Verbindung. Weitere Informationen finden Sie [Link erforderlich]. |

![Tools-Bereich](assets/tools-scenario-editor.png)

### Favoriten

Mit dem Symbol Favoriten können Sie häufig verwendete Module hinzufügen.

![Bedienfeld „Favoriten“](assets/favorites-scenario-editor.png)
