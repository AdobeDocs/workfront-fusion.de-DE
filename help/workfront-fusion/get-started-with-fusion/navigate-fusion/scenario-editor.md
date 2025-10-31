---
title: Der Szenario-Editor
description: Mit dem Szenario-Editor können Sie Szenarien in einer visuellen Benutzeroberfläche erstellen und bearbeiten.
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: 93d06cb917680f9cabc1bad6be0f9cd843449d07
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 3%

---

# Der Szenario-Editor

Mit dem Szenario-Editor können Sie Szenarien in einer visuellen Benutzeroberfläche erstellen und bearbeiten.

![Szenario-Editor](assets/scenario-editor.jpg)

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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

| Aktion | Details |
|----------|----------|
| Speichern Sie. | Nach dem Speichern Ihres Szenarios wird eine neue Version unter dem Dreipunkt-Menü verfügbar sein, falls Sie in Zukunft darauf zugreifen müssen. Zuvor gespeicherte Szenario-Versionen sind nur für 60 Tage verfügbar. |
| Szenario-Einstellungen | Das Bedienfeld Szenario-Einstellungen enthält erweiterte Einstellungen für das Szenario. Weitere Informationen zu den verfügbaren Einstellungen finden Sie unter [Szenarioeinstellungen konfigurieren](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md). |
| Anmerkungen | Machen Sie sich Notizen zum Szenario. Andere Benutzende können diese Notizen anzeigen, wenn sie sich im Szenario befinden. |
| Automatisch ausrichten | Automatische Ausrichtung der Module in Ihrem Szenario. |
| Fluss erläutern | Zeigen Sie eine Animation an, in der bewegte Punkte zeigen, wie Daten durch das Szenario fließen. |
| Entwicklungs-Tools | Mit dem DevTool können Sie alle manuellen Ausführungen Ihres Szenarios überprüfen, alle ausgeführten Vorgänge überprüfen und die Details jedes durchgeführten API-Aufrufs anzeigen. Sie können sehen, welches Modul, welcher Vorgang oder welche einzelne Antwort den Fehler verursacht hat, und dieses Wissen verwenden, um Ihr Szenario zu verfeinern. Weitere Informationen finden Sie unter [Debuggen eines Szenarios](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md). |
| Mehr | Im Menü Mehr können Sie Blueprints importieren und exportieren und das Szenario wieder auf die vorherigen Versionen zurücksetzen. |

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
