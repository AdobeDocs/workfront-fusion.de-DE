---
title: Szenario-Ausführung, Zyklen und Phasen
description: In diesem Artikel werden Ereignisse beschrieben, die während der Ausführung eines Adobe Workfront Fusion-Szenarios auftreten, z. B. Initialisierung, Vorgänge, Commits und Rollbacks.
author: Becky
feature: Workfront Fusion
exl-id: abf41be5-df32-4eaf-b3f4-93ddf005bfe3
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 1%

---

# Szenarioausführung, Zyklen und Phasen

Jede Szenarioausführung beginnt mit der Initialisierungsphase, wird mit mindestens einem Zyklus fortgesetzt, der aus den Vorgangs- und Commit-/Rollback-Phasen besteht, und endet mit der Finalisierungsphase

* Initialisierung
* #1
   * Betrieb (Lesen oder Schreiben)
   * Commit oder Rollback
* #2
   * Betrieb (Lesen oder Schreiben)
   * Commit oder Rollback
* …
* #n
   * Betrieb (Lesen oder Schreiben)
   * Commit oder Rollback
* Fertigstellung

In kleinerem Maßstab folgt auch jedes Modul diesen Phasen. Informationen zu den Modulphasen finden Sie in den verarbeiteten Bundle-Informationen, die in der nummerierten Blase oben rechts von jedem Modul zu finden sind, nachdem das Szenario ausgeführt wurde. Weitere Informationen zum Auffinden verarbeiteter Bundle-Informationen finden Sie unter [Informationen zu verarbeiteten Bundles](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md#information-about-processed-bundles) im Artikel Szenario-Ausführungsfluss .

Informationen zu den größeren Szenario-Phasen finden Sie in den Ausführungsdetails.

## Ausführungsphasen des Szenarios

### Initialisierung

Während der Initialisierungsphase werden alle erforderlichen Verbindungen (Verbindung zu einer Datenbank, E-Mail-Dienst usw.) erstellt und überprüft, um sicherzustellen, dass das Modul die beabsichtigten Vorgänge ausführen kann.

### Zyklen

Jeder Zyklus stellt eine unteilbare Arbeitseinheit dar, die aus einer Reihe von Vorgängen besteht, von denen jeder einen Commit oder ein Rollback aufweist.

Sie können die maximale Anzahl von Zyklen im Bedienfeld [!UICONTROL Szenario-Einstellungen] festlegen. Die Standardzahl ist 1.

* [Vorgang](#operation)
* [Zusichern](#commit)
* [Rollback](#rollback)

#### Vorgang

Während der Betriebsphase wird ein Lese- oder Schreibvorgang ausgeführt:

* Ein Lesevorgang besteht darin, Daten von einem Service abzurufen, die dann von anderen Modulen gemäß einem vordefinierten Szenario verarbeitet werden. Beispielsweise gibt das Modul [!UICONTROL Workfront] >[!UICONTROL Datensätze beobachten] neue Bundles (Datensätze) zurück, die seit der letzten Szenarioausführung erstellt wurden.
* Ein Schreibvorgang besteht darin, Daten zur weiteren Verarbeitung an einen bestimmten Dienst zu senden. Beispielsweise lädt das Modul Workfront > [!UICONTROL Dokument hochladen] eine Datei in Workfront hoch.

#### Zusichern

Wenn die Vorgangsphase erfolgreich ist, beginnt die Commit-Phase, während der alle von den Modulen ausgeführten Vorgänge übergeben werden. Das bedeutet, dass Workfront Fusion Informationen über den Erfolg an alle an der Betriebsphase beteiligten Services sendet.

### Rollback

Wenn während der Vorgangs- oder Commit-Phase auf einem Modul ein Fehler auftritt, wird die Phase abgebrochen und die Rollback-Phase gestartet, wodurch alle Vorgänge während des angegebenen Zyklus ungültig werden.

>[!IMPORTANT]
>
>Alle Workfront Fusion-Module, die Rollback unterstützen (auch als Transaktion bezeichnet), sind mit dem ACID-Tag gekennzeichnet.
>
>![Säuremodule](assets/acid-modules.png)
>
>Module, die nicht mit diesem Tag markiert sind, können nicht in ihren Ausgangszustand zurückgesetzt werden, wenn in anderen Modulen Fehler auftreten. Ein typisches Beispiel für ein Nicht-ACID-Modul ist die Aktion [!UICONTROL E] > [!UICONTROL E-Mail senden]. Nach dem Versand der E-Mail kann der Versand nicht mehr rückgängig gemacht werden.

### Fertigstellung

Während der Finalisierungsphase werden offene Verbindungen (z. B. FTP-Verbindungen, Datenbankverbindungen usw.) geschlossen und das Szenario ist abgeschlossen.

## Ressourcen

Weitere Informationen finden Sie unter [Konfigurieren von Szenarioeinstellungen](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).
