---
title: Microsoft SQL Server-Module
description: Sie können verwenden [!DNL Adobe Workfront Fusion]  um eine Verbindung zu Microsoft SQL Server herzustellen.
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: ef1a96d9ef4c2c82eaf376c84188e3ed6ea7b2cf
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# [!DNL Microsoft SQL Server]

Sie können [!DNL Adobe Workfront Fusion] verwenden, um eine Verbindung zu [!UICONTROL Microsoft SQL Server] herzustellen.

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy: Workfront Fusion für Arbeitsautomatisierung und -integration </p>
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

## Verbinden des [!DNL Microsoft SQL Server]-Services mit [!DNL Workfront Fusion]

Anweisungen zum Verbinden Ihres [!DNL Microsoft SQL Server]-Kontos mit [!UICONTROL Workfront Fusion] finden Sie unter [Erstellen einer Verbindung zu [!UICONTROL Adobe Workfront Fusion] - Grundlegende Anweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
>
>Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.

## Verwenden von [!DNL Microsoft SQL Server]

Sie können Ihre benutzerdefinierte Logik über gespeicherte Prozeduren direkt auf Ihrem Datenbank-Server ausführen. [!DNL Adobe Workfront Fusion] lädt dynamisch die Schnittstelle von Eingabe/Ausgabe-Parametern und Recordset , sodass jeder Parameter oder Wert einzeln zugeordnet werden kann. Bevor Sie mit der Konfiguration Ihres Szenarios beginnen, stellen Sie sicher, dass das Konto, das Sie für die Verbindung mit Ihrer Datenbank verwenden, Lesezugriff auf `INFORMATION_SCHEMA.ROUTINES`- und `INFORMATION_SCHEMA.PARAMETERS` hat.

Wenn [!DNL Fusion] die Verbindung zum [!DNL SQL server]-Ziel herstellt, identifiziert der [!DNL Fusion] den Host (den Domain-Namen oder die IP-Adresse, unter der der Server gehostet wird) und den Port. [!DNL Fusion] können eine Verbindung zu jedem verfügbaren Host und Port herstellen.

Informationen zu den von [!DNL Workfront Fusion] verwendeten IP-Adressen finden Sie unter [IP-Adressen für den Zugriff [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

Weitere Informationen zum Erstellen einer gespeicherten Prozedur finden Sie in der [!DNL Microsoft SQL Server].

>[!NOTE]
>
>[!DNL Workfront Fusion] unterstützt nicht mehrere Recordsets. Nur der erste wird verarbeitet.

## Fehlerbehebung bei [!UICONTROL ER_LOCK_WAIT_TIMEOUT: Lock wait timeout exceeded; try restarting transaction]

Dieser Fehler tritt auf, wenn Sie dieselben Daten mithilfe mehrerer Module ändern. Sie wird durch SQL-Transaktionen verursacht.

Wenn ein SQL-Modul ausgeführt wird, startet es eine Transaktion. Die Transaktion ist abgeschlossen, nachdem das Szenario vollständig ausgeführt wurde.

Wenn ein anderes Modul versucht, auf dieselben Daten zuzugreifen, muss es warten, bis die vorherige Transaktion abgeschlossen ist. Da die erste Transaktion abgeschlossen wird, nachdem das Szenario abgeschlossen ist, kann die zweite Transaktion nie beginnen.

### Lösung:

Aktivieren Sie die automatische Bestätigung. Der automatische Commit beendet (übergibt) jede Transaktion unmittelbar nach Abschluss der Modulausführung.

1. Klicken Sie auf das Symbol [!UICONTROL Scenario settings] ![Szenario-Einstellungen](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png) unten auf dem Bildschirm.
1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL Auto commit]** .
1. Klicken Sie auf **[!UICONTROL OK]** , um die Szenario-Einstellungen zu speichern.
