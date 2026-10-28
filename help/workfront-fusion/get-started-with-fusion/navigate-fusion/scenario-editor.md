---
title: Der Szenario-Editor
description: Mit dem Szenario-Editor können Sie Szenarien in einer visuellen Benutzeroberfläche erstellen und bearbeiten.
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
TQID: 'https://experienceleague.adobe.com/0NhWgeBcqYtVJ7XKqZ30O1lg3fKSs7YijEhhYBQ-jfg'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '2357'
ht-degree: 6%
---
# Der Szenario-Editor

Mit dem Szenario-Editor können Sie Szenarien in einer visuellen Benutzeroberfläche erstellen und bearbeiten.

Das neue Szenario-Editor-Erlebnis:

![Neuer Szenario-Editor](assets/scenario-editor-new.png)

Das klassische Szenario-Editor-Erlebnis

![Szenario-Editor](assets/scenario-editor.jpg)

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

## Neue und klassische Erlebnisse

Workfront Fusion stellt den Szenario-Editor auf ein neues Erlebnis um. Während dieser Umstellung sind sowohl die klassischen als auch die neuen Erlebnisse verfügbar und Sie können jederzeit zwischen ihnen wechseln. Es wird empfohlen, die neue -Version zu verwenden.

Das neue Erlebnis umfasst:

* Eine neu gestaltete Arbeitsfläche mit Kartenmodulen, einer Minikarte und Zoom-Steuerelementen.
* Neue Szenario-Editor-Steuerelemente, einschließlich Suchen und Ersetzen, Ausschnitte und Rückgängig/Wiederholen.
* Eine Ask AI-Schaltfläche.
* Eine aktualisierte Connector-Auswahl mit Kategoriennavigation und der Möglichkeit, Favoriten inline zu markieren.
* Ein Dunkelmodus, der Ihrer Erscheinungsbildeinstellung folgt.
* Die Möglichkeit, einen Router zu falten, um seine Routen auszublenden.
* [Live Trail](/help/workfront-fusion/manage-scenarios/live-trail.md) ein Bedienfeld, das eine ausgeführte Szenario-Ausführung anzeigt.
* Verschiedene Entwickler-Tools, die jetzt im Szenario-Editor integriert sind.
* Temporäre Debug-Protokolle, die Sie in den Szenario-Einstellungen aktivieren können.

So wechseln Sie zwischen den klassischen und neuen Erlebnissen:

1. Suchen Sie im Szenario-Editor den Umschalter **[!UICONTROL Neues Design ausprobieren]** in der oberen rechten Ecke.
1. Klicken Sie auf den Umschalter, um zur neuen Version zu wechseln.
1. Um zum klassischen Erlebnis zurückzukehren, klicken Sie erneut auf den Umschalter.

Das Szenario wird beim Umschalten neu geladen. Ihre Auswahl wird für Ihre Benutzerin bzw. Ihren Benutzer gespeichert, sodass das Erlebnis, das Ihre Teammitglieder sehen, dadurch nicht verändert wird. Ein Wechsel ändert nichts am Szenario selbst.

Wenn der Umschalter nicht angezeigt wird, ist das neue Erlebnis für Ihre Organisation möglicherweise noch nicht verfügbar. Wenden Sie sich an Ihren Workfront Fusion-Administrator.

## Szenario-Editor in der neuen -Version verwenden (empfohlen)

* [Öffnen Sie den Szenario-Editor und fügen Sie ein Modul hinzu:](#open-the-scenario-editor-and-add-a-module)
* [Verfügbare Szenario-Editor-Aktionen](#available-scenario-editor-actions)

### Öffnen Sie den Szenario-Editor und fügen Sie ein Modul hinzu:

1. Klicken Sie **[!UICONTROL linken Bedienfeld]** Szenarios![ (](assets/scenarios-icon.png)).
1. Klicken Sie auf das Platzhaltermodul, um die Liste der Apps und Services zu öffnen.
1. Wählen Sie die App oder den Service aus, mit der bzw. dem Sie beginnen möchten:

   * Mithilfe des Bedienfelds auf der linken Seite nach Kategorie suchen ([!UICONTROL Favoriten], [!UICONTROL Alle Apps], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative &amp; Content], [!UICONTROL Adobe Cloud Services], [!UICONTROL Generative AI] oder [!UICONTROL integriert]).
   * Geben Sie einen Begriff in das Suchfeld ein, um die Liste zu filtern.
   * Um einen Connector zu Ihren Favoriten hinzuzufügen, bewegen Sie den Mauszeiger über den Connector und klicken Sie dann auf das Sternsymbol neben dem Connector.

   Detaillierte Informationen zum Konfigurieren eines Moduls finden Sie unter [Modul konfigurieren](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

### Verfügbare Szenario-Editor-Aktionen

* [Bearbeiten von Aktionen](#editing-actions)
* [Planung](#scheduling)
* [Steuerelemente](#controls)
* [Tools](#tools)
* [Favoriten](#favorites)
* [Ask AI](#ask-ai)
* [Navigation auf der Arbeitsfläche](#canvas-navigation)
* [Canvas-Anzeige](#canvas-display)

#### Bearbeiten von Aktionen

Diese Aktionen sind am oberen Bildschirmrand und nicht in der unteren Symbolleiste verfügbar.

![Am oberen Bildschirmrand](assets/top-bar-new.png)

| Aktion | Details |
| ---------- | ---------- |
| Szenarioname | Der Name des Szenarios wird oben links im Bildschirm angezeigt. Um das Szenario umzubenennen, klicken Sie auf den Namen und geben Sie einen neuen ein. |
| Kompakte Ansicht | Schalten Sie eine Ansicht um, in der Module auf der Arbeitsfläche auf kleine Kacheln verkleinert, das Raster gestrafft und lange Modulnamen umgebrochen werden, anstatt abgeschnitten zu werden. Beim Wechseln der Ansicht wird das Szenario nicht neu geladen. |
| Feedback | Feedback zum neuen Erlebnis senden. Diese Schaltfläche befindet sich in der rechten oberen Ecke des Szenario-Editors neben dem Umschalter Ansicht komprimieren . |
| Rückgängig </br>![Symbol „Rückgängig“](assets/undo-icon.png) | Macht die letzten Aktionen rückgängig, die letzten zuerst. Sie können Aktionen nur in der aktuellen Sitzung rückgängig machen. |
| Wiederholen </br>![Symbol „Wiederholen](assets/redo-icon.png) | Wiederholen Sie die letzten Aktionen. Sie können Aktionen nur in der aktuellen Sitzung wiederholen. |
| Verlauf </br>![Symbol „Verlauf bearbeiten](assets/edit-history-icon.png) | Protokoll der in dieser Sitzung vorgenommenen Änderungen anzeigen. Sie können auch alle Sitzungsänderungen rückgängig machen. |

#### Planung

![Bedienfeld „Planung](assets/new-scheduling-area.png)

| Aktion | Details |
| ---------- | ---------- |
| Einmal ausführen | „Einmal ausführen“ ist im neuen Design nur als Symbol verfügbar. Bewegen Sie den Mauszeiger über das Symbol, um die QuickInfo **[!UICONTROL Einmal ausführen]** anzuzeigen. Hier können Sie das Szenario testen und überprüfen, ob es wie erwartet ausgeführt wird, bevor Sie es aktivieren |
| Aktivierungsschalter | Aktivieren oder Deaktivieren des Szenarios. Nach der Aktivierung wird das Szenario gemäß seinem Zeitplan ausgeführt. |
| Szenario planen | Standardmäßig wird alle 15 Minuten ein Szenario mit einem Trigger „Abfrage“ ausgeführt. Sie können dies ändern, indem Sie festlegen, wann und wie oft ein aktiviertes Szenario ausgeführt wird. Abgerufene Fusionsszenarien können so geplant werden, dass sie alle 5 Minuten ausgeführt werden. Weitere Informationen finden Sie unter [Szenario planen](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md). |

#### Steuerelemente

Möglicherweise müssen Sie auf das Dreipunkt-Symbol im Bereich Steuerelemente klicken, um einige dieser Steuerelemente anzuzeigen.

![Bedienfeld](assets/controls-new.png)

| Aktion | Details |
| ---------- | ---------- |
| Speichern Sie. <p>![Speichersymbol](assets/save-icon-new.png)</p> | <p>Nach dem Speichern Ihres Szenarios wird eine neue Version unter dem Dreipunkt-Menü verfügbar sein, falls Sie in Zukunft darauf zugreifen müssen. Zuvor gespeicherte Szenario-Versionen sind nach der Erstellung der nächsten Szenario-Version 60 Tage lang verfügbar. </p><p>Um den Szenario-Versionsverlauf über 60 Tage hinaus für Audit-Zwecke aufzubewahren, empfehlen wir, eine Blueprint des Szenarios an einem anderen Speicherort zu speichern und zu archivieren.</p> |
| Szenario-Einstellungen <p>![Symbol für Szenario-Einstellungen](assets/scenario-settings-icon-new.png)</p> | Das Bedienfeld Szenario-Einstellungen enthält erweiterte Einstellungen für das Szenario. Weitere Informationen zu den verfügbaren Einstellungen finden Sie unter [Szenarioeinstellungen konfigurieren](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md). Anfrage- und Antwortdetails werden nicht für jeden Durchgang gespeichert. Um sie für die regulären Ausführungen des Szenarios zu erfassen, aktivieren Sie die temporären Debug-Protokolle. Weitere Informationen finden Sie unter [Temporäre Debug-Protokolle](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs). |
| Anmerkungen <p>![Notizensymbol](assets/notes-icon-new.png)</p> | Machen Sie sich Notizen zum Szenario. Andere Benutzende können diese Notizen anzeigen, wenn sie sich im Szenario befinden. Weitere Informationen finden Sie unter [Hinzufügen von Anmerkungen zu einem Szenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/add-notes-to-scenario.md). |
| Automatisch ausrichten <p>![Symbol für automatische Ausrichtung](assets/auto-align-icon-new.png)</p> | Automatische Ausrichtung der Module in Ihrem Szenario. |
| Suchmodule <p>![Suchmodulsymbol](assets/search-modules-icon-new.png)</p> | Wählen Sie ein Modul aus dieser Liste aus, um zu diesem Modul im Szenario zu wechseln, oder geben Sie einen Suchbegriff ein, um ein Modul zu finden, und klicken Sie dann auf die Suchergebnisse, die zu diesem Modul geleitet werden sollen. Sie können nach Modulnamen, ID, Typ oder Anwendung suchen. |
| Suchen und Ersetzen <p>![Symbol „Suchen und Ersetzen](assets/find-and-replace-icon-new.png)</p> | <p>Variablen, zugeordnete Wertquellen oder Verbindungen in den Modulen des Szenarios suchen und ersetzen. Verwenden Sie die Registerkarten für Folgendes:</p><ul><li>Ersetzen Sie eine zugeordnete Variable im gesamten Szenario oder in einem Modul.</li><li>Ordnen Sie Verweise von einem Quellmodul einem anderen neu zu.</li><li>Kopieren Sie eine Verbindung zu einem oder allen kompatiblen Modulen aus derselben App.</li></ul><p>Das Bedienfeld zeigt eine Vorschau der Module an, die betroffen sind, bevor Sie die Änderung vornehmen. Wählen Sie eine Zeile in der Vorschau aus, um zu diesem Modul auf der Arbeitsfläche zu wechseln.</p> <p>Weitere Informationen finden Sie unter [ und Ersetzen von Variablen, Quellen und Verbindungen in einem Szenario](/help/workfront-fusion/manage-scenarios/find-and-replace.md).</p> |
| Snippets <p>![Snippets-Symbol](assets/snippets-icon-new.png)</p> | <p>Snippets sind Szenarioabschnitte, die als Einheit gespeichert werden. Um eines zu erstellen, wählen Sie Module aus und speichern Sie sie als Snippet. Im Snippets-Bedienfeld können Sie Snippets suchen, taggen, in der Vorschau anzeigen, anheften, sortieren, per Drag-and-Drop ziehen und importieren und exportieren. Sie können Snippets für Teams oder Organisationen freigeben oder eine Kopie direkt an einen anderen Benutzer senden. Freigegebene Snippets werden auf ihrer eigenen Registerkarte angezeigt.</p> <p>Weitere Informationen finden Sie unter [Szenarioabschnitte mit Snippets speichern und wiederverwenden](/help/workfront-fusion/create-scenarios/add-modules/use-snippets.md).</p> |
| Fluss erläutern <p>![Flusssymbol erläutern](assets/explain-flow-icon-new.png)</p> | Zeigen Sie eine Animation an, in der bewegte Punkte zeigen, wie Daten durch das Szenario fließen. |
| Blueprint exportieren <p>![Blueprint-Symbol exportieren](assets/export-blueprint-icon-new.png)</p> | Exportiert einen Blueprint des aktuellen Szenarios. Weitere Informationen finden Sie unter [Module oder Szenarien kopieren](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md). |
| Als Headless-Vorlage exportieren <p>![Als Headless-Vorlagensymbol exportieren](assets/export-as-headless-template-icon-new.png)</p> | Exportieren Sie das Szenario als Headless-Vorlage. |
| Blueprint importieren <p>![Blueprint-Symbol importieren](assets/import-blueprint-icon-new.png)</p> | Importieren Sie eine zuvor exportierte Szenario-Blueprint. Weitere Informationen finden Sie unter [Module oder Szenarien kopieren](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md). |
| DevTool <p>![DevTool-Symbol](assets/devtool-icon-new.png)</p> | Mit dem DevTool können Sie alle manuellen Ausführungen Ihres Szenarios überprüfen, alle ausgeführten Vorgänge überprüfen und die Details jedes durchgeführten API-Aufrufs anzeigen. Sie können sehen, welches Modul, welcher Vorgang oder welche einzelne Antwort den Fehler verursacht hat, und dieses Wissen verwenden, um Ihr Szenario zu verfeinern. Weitere Informationen finden Sie unter [Debuggen eines Szenarios](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md). |
| Frühere Versionen <p>![Symbol für vorherige Version](assets/previous-version-icon-new.png)</p> | Frühere Versionen dieses Szenarios anzeigen. Weitere Informationen finden Sie unter [Szenario-Versionen anzeigen und verwalten](/help/workfront-fusion/manage-scenarios/restore-a-scenario-version.md). |

#### Tools

![Tools-Bereich](assets/tools-new.png)

| Aktion | Details |
| ---------- | ---------- |
| Flusssteuerung | Konfigurieren Sie Einstellungen, um den Datenfluss durch das Szenario zu steuern. Weitere Informationen finden Sie unter [Flusskontrolle](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/flow-control.md). |
| Tools | Der Abschnitt Tools enthält mehrere nützliche Module, die Ihre Szenarien verbessern können. Weitere Informationen finden Sie unter [Tools](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/tools-modules.md). |
| Text-Parser | Verwenden Sie das Text-Parser-Tool, um Text zur Verwendung in anderen Szenario-Modulen zu analysieren. Weitere Informationen finden Sie unter [Text-Parser](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/text-parser.md). |

#### Favoriten

![Bedienfeld „Favoriten“](assets/favorites-new.png)

Mit dem Symbol Favoriten können Sie häufig verwendete Module hinzufügen.

| Aktion | Details |
| ---------- | ---------- |
| Ihre bevorzugten Connectoren | Die Connectoren, die Sie als Favoriten gekennzeichnet haben, werden hier angezeigt. |
| Favoritensymbol hinzufügen | Klicken Sie auf dieses Symbol, um einen anderen Connector auszuwählen, der zum Abschnitt Favoriten hinzugefügt werden soll. |
| Overflow-Symbol | Wenn Sie mehr Favoriten haben, als in die Symbolleiste passen, wird ein Überlaufsymbol (drei Punkte) angezeigt, damit Sie auf den Rest zugreifen können. |

#### Ask AI

![KI-Schaltfläche fragen](assets/ask-ai-new.png)

Klicken Sie auf **KI**, um den KI-Assistenten von Adobe zu öffnen. Diese Option ist möglicherweise aufgrund der KI-Einstellungen Ihres Unternehmens nicht verfügbar.

#### Navigation auf der Arbeitsfläche

![Navigationssteuerelemente der Arbeitsfläche](assets/canvas-navigation-new.png)

| Aktion | Details |
| ---------- | ---------- |
| Vergrößern/Verkleinern | Vergrößern oder Verkleinern der Arbeitsflächenansicht. |
| Focus | Kehren Sie zu einer Ansicht zurück, die zu Ihrem gesamten Szenario auf dem Bildschirm passt. |
| Minikarte | Zeigen Sie eine Miniaturansicht mit einer Übersicht des gesamten Szenarios an. Die Minikarte zeigt Ihren aktuellen Viewport. Klicken oder ziehen Sie, um sich auf der Arbeitsfläche zu bewegen. |

#### Canvas-Anzeige

Die neue Arbeitsfläche ändert auch das Aussehen von Szenarien.

| Funktion | Details |
| ---------- | ---------- |
| Modulkarten | Jedes Modul ist eine horizontale Karte, die das App-Symbol, den Modulnamen, die Beschreibung und die Modul-ID anzeigt. Router werden als kompakte Verzweigungskachel angezeigt, und Anweisungen werden als Karten mit kleinem Akzent angezeigt. |
| Links | Die Verknüpfungen zwischen den Modulen sind gekrümmt und enden in Pfeilspitzen, die die Richtung zeigen. Fehler-Handler-Links sind gestrichelt dargestellt. |
| Modulstatus | Die Indikatoren Grün, Gelb und Rot zeigen den Status der einzelnen Module an. |
| Zoom-Detail | Kartendetails werden beim Vergrößern angezeigt. Beim Verkleinern vereinfachen Module die Symbole, sodass Sie immer noch das gesamte Szenario sehen können. |
| Falten eines Routers | Im Bearbeitungsmodus können Sie einen Router falten, um seine Routen auszublenden. Weitere Informationen finden Sie unter [Router ](/help/workfront-fusion/create-scenarios/add-modules/router-module.md#fold-a-router). |
| Dunkler Modus | Die Arbeitsfläche entspricht der Einstellung für Ihr dunkles Erscheinungsbild in Ihren Adobe-Voreinstellungen, einschließlich Modulkarten, Links, Bedienfeldern, Steuerelementen und Statusinformationen. |
| Rechtes Bedienfeld | Das Modul-Setup, die Modulinspektion, der Modul-Browser, Suchen und Ersetzen, Snippets[Live-Trail](/help/workfront-fusion/manage-scenarios/live-trail.md) und Anfrage- und Antwortdetails werden im selben Bedienfeld auf der rechten Seite der Arbeitsfläche geöffnet. |

## Verwenden des Szenario-Editors in der klassischen -Version

* [Öffnen Sie den Szenario-Editor und fügen Sie ein Modul hinzu: (Classic)](#open-the-scenario-editor-and-add-a-module-classic)
* [Verfügbare Szenario-Editor-Aktionen (klassisch)](#available-scenario-editor-actions-classic)

### Öffnen Sie den Szenario-Editor und fügen Sie ein Modul hinzu: (Classic)

1. Klicken Sie **[!UICONTROL linken Bedienfeld]** Szenarios![ (](assets/scenarios-icon.png)).
1. Klicken Sie auf das Fragezeichensymbol ![Fragesymbol](assets/question-mark-full-size.png), suchen Sie nach der App oder dem Service, mit der bzw. dem Sie beginnen möchten, und klicken Sie darauf. Detaillierte Informationen zum Konfigurieren eines Moduls finden Sie unter [Modul konfigurieren](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

### Verfügbare Szenario-Editor-Aktionen (klassisch)

* [Ausführen eines Szenarios (klassisch)](#run-your-scenario-classic)
* [Planung (klassisch)](#scheduling-classic)
* [Steuerelemente (klassisch)](#controls-classic)
* [Tools (klassisch)](#tools-classic)
* [Favoriten (klassisch)](#favorites-classic)

#### Ausführen eines Szenarios (klassisch)

![Schaltfläche „Szenario ausführen“](assets/run-your-scenario.png)

| Aktion | Details |
|----------|----------|
| Testlauf des Szenarios | Vergewissern Sie sich vor der Aktivierung, dass das Szenario erwartungsgemäß ausgeführt wird. Nach der Aktivierung wird das Szenario gemäß seinem Zeitplan ausgeführt. Wenn nicht alles wie erwartet ausgeführt wird, finden Sie unter [Fehlerbehandlung hinzufügen](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md) Informationen zum Umgang mit Fehlern. |

#### Planung (klassisch)

![Bedienfeld „Planung](assets/scheduling-scenario-editor.png)

| Aktion | Details |
| ---------- | ---------- |
| Szenario planen | Standardmäßig wird ein Szenario alle 15 Minuten ausgeführt. Sie können dies ändern, indem Sie festlegen, wann und wie oft ein aktiviertes Szenario ausgeführt wird. Fusionsszenarien können so geplant werden, dass sie alle 5 Minuten ausgeführt werden. Weitere Informationen finden Sie unter [Szenario planen](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md). |

#### Steuerelemente (klassisch)

Möglicherweise müssen Sie auf das Dreipunkt-Symbol im Bereich Steuerelemente klicken, um einige dieser Steuerelemente anzuzeigen.

![Bedienfeld](assets/controls-editor-scenario.png)

| Aktion | Details |
| ---------- | ---------- |
| Speichern Sie. <p>![Speichersymbol](assets/save-icon.png)</p> | <p>Nach dem Speichern Ihres Szenarios wird eine neue Version unter dem Dreipunkt-Menü verfügbar sein, falls Sie in Zukunft darauf zugreifen müssen. Zuvor gespeicherte Szenario-Versionen sind nach der Erstellung der nächsten Szenario-Version 60 Tage lang verfügbar. </p><p>Um den Szenario-Versionsverlauf über 60 Tage hinaus für Audit-Zwecke aufzubewahren, empfehlen wir, eine Blueprint des Szenarios an einem anderen Speicherort zu speichern und zu archivieren.</p> |
| Szenario-Einstellungen <p>![Symbol für Szenario-Einstellungen](assets/scenario-settings-icon.png)</p> | Das Bedienfeld Szenario-Einstellungen enthält erweiterte Einstellungen für das Szenario. Weitere Informationen zu den verfügbaren Einstellungen finden Sie unter [Szenarioeinstellungen konfigurieren](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md). |
| Anmerkungen  <p>![Notizensymbol](assets/notes-icon.png)</p> | Machen Sie sich Notizen zum Szenario. Andere Benutzende können diese Notizen anzeigen, wenn sie sich im Szenario befinden. |
| Automatisch ausrichten <p>![Symbol für automatische Ausrichtung](assets/auto-align-icon.png)</p> | Automatische Ausrichtung der Module in Ihrem Szenario. |
| Suchmodule <p>![Suchmodule](assets/search-modules-icon.png)  </p> | Geben Sie einen Suchbegriff ein, um ein Modul zu finden, und klicken Sie dann auf die Suchergebnisse, um zu diesem Modul zu gelangen. Sie können nach Modulnamen, ID, Typ oder Anwendung suchen. |
| Fluss erläutern  <p>![Flusssymbol erläutern](assets/explain-flow-icon.png) </p> | Zeigen Sie eine Animation an, in der bewegte Punkte zeigen, wie Daten durch das Szenario fließen. |
| DevTool <p>![DevTool-Symbol](assets/devtool-icon.png)</p> | Mit dem DevTool können Sie alle manuellen Ausführungen Ihres Szenarios überprüfen, alle ausgeführten Vorgänge überprüfen und die Details jedes durchgeführten API-Aufrufs anzeigen. Sie können sehen, welches Modul, welcher Vorgang oder welche einzelne Antwort den Fehler verursacht hat, und dieses Wissen verwenden, um Ihr Szenario zu verfeinern. Weitere Informationen finden Sie unter [Debuggen eines Szenarios](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md). |
| Blueprint exportieren  <p>![Blueprint-Symbol exportieren](assets/export-blueprint-icon.png) </p> | Exportiert einen Blueprint des aktuellen Szenarios. |
| Als Headless-Vorlage exportieren  <p>![Als Headless-Vorlagensymbol exportieren](assets/export-as-headless-template-icon.png) </p> | Exportieren Sie das Szenario als Headless-Vorlage. |
| Blueprint importieren  <p>![Blueprint-Symbol importieren](assets/import-blueprint-icon.png) </p> | Importieren Sie eine zuvor exportierte Szenario-Blueprint. |
| Vorherige Version  <p>![Symbol für vorherige Version](assets//previous-version-icon.png) </p> | Frühere Versionen dieses Szenarios anzeigen. |

#### Tools (klassisch)

![Tools-Bereich](assets/tools-scenario-editor.png)

| Aktion | Details |
| ---------- | ---------- |
| Flusssteuerung | Einstellungen konfigurieren, um den Datenfluss zu steuern. Weitere Informationen finden Sie unter [Flusskontrolle](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/flow-control.md). |
| Tools | Der Abschnitt Tools enthält mehrere nützliche Module, die Ihre Szenarien verbessern können. Weitere Informationen finden Sie unter [Tools](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/tools-modules.md). |
| Text-Parser | Verwenden Sie das Text-Parser-Tool, um Text zur Verwendung in anderen Szenario-Modulen zu analysieren. Der Text-Parser benötigt keine Verbindung. Weitere Informationen finden Sie unter [Text-Parser](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/text-parser.md). |

#### Favoriten (klassisch)

![Bedienfeld „Favoriten“](assets/favorites-scenario-editor.png)

Mit dem Symbol Favoriten können Sie häufig verwendete Module hinzufügen.

