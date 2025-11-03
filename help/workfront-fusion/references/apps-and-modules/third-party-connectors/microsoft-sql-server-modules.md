---
title: Microsoft SQL Server-Module
description: Sie können Adobe Workfront Fusion verwenden, um eine Verbindung zu Microsoft SQL Server herzustellen.
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# [!DNL Microsoft SQL Server]

Sie können Adobe Workfront Fusion verwenden, um eine Verbindung zu [!UICONTROL Microsoft SQL Server] herzustellen.

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
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Verbinden des [!DNL Microsoft SQL Server]-Service mit Workfront Fusion

Anweisungen zum Verbinden Ihres [!DNL Microsoft SQL Server]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung mit [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
>
>Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.

## Verwenden von [!DNL Microsoft SQL Server]

Sie können Ihre benutzerdefinierte Logik über gespeicherte Prozeduren direkt auf Ihrem Datenbank-Server ausführen. Adobe Workfront Fusion lädt die Schnittstelle von Eingabe-/Ausgabeparametern und Recordset dynamisch, sodass jeder Parameter oder Wert einzeln zugeordnet werden kann. Bevor Sie mit der Konfiguration Ihres Szenarios beginnen, stellen Sie sicher, dass das Konto, das Sie für die Verbindung mit Ihrer Datenbank verwenden, Lesezugriff auf `INFORMATION_SCHEMA.ROUTINES`- und `INFORMATION_SCHEMA.PARAMETERS` hat.

Wenn [!DNL Fusion] die Verbindung zum [!DNL SQL server]-Ziel herstellt, identifiziert der [!DNL Fusion] den Host (den Domain-Namen oder die IP-Adresse, unter der der Server gehostet wird) und den Port. [!DNL Fusion] können eine Verbindung zu jedem verfügbaren Host und Port herstellen.

Informationen zu den von Workfront Fusion verwendeten IP-Adressen finden Sie unter [IP-Adressen für den Zugriff auf Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

Weitere Informationen zum Erstellen einer gespeicherten Prozedur finden Sie in der [!DNL Microsoft SQL Server].

>[!NOTE]
>
>Workfront Fusion unterstützt nicht mehrere Recordsets. Nur der erste wird verarbeitet.

## Fehlerbehebung für Fehler [!UICONTROL ER_LOCK_WAIT_TIMEOUT: Sperrwartezeitlimit überschritten; versuchen Sie, die Transaktion neu zu starten]

Dieser Fehler tritt auf, wenn Sie dieselben Daten mithilfe mehrerer Module ändern. Sie wird durch SQL-Transaktionen verursacht.

Wenn ein SQL-Modul ausgeführt wird, startet es eine Transaktion. Die Transaktion ist abgeschlossen, nachdem das Szenario vollständig ausgeführt wurde.

Wenn ein anderes Modul versucht, auf dieselben Daten zuzugreifen, muss es warten, bis die vorherige Transaktion abgeschlossen ist. Da die erste Transaktion abgeschlossen wird, nachdem das Szenario abgeschlossen ist, kann die zweite Transaktion nie beginnen.

### Lösung:

Aktivieren Sie die automatische Bestätigung. Der automatische Commit beendet (übergibt) jede Transaktion unmittelbar nach Abschluss der Modulausführung.

1. Klicken Sie auf [!UICONTROL Szenario]-Symbol ![Szenario-Einstellungen](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png) unten auf dem Bildschirm.
1. Aktivieren Sie **[!UICONTROL Kontrollkästchen]** Automatisch bestätigen“.
1. Klicken Sie **[!UICONTROL OK]**, um die Szenario-Einstellungen zu speichern.
