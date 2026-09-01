---
title: Initialisieren des Speichers
description: Wenn ein(e) Benutzende(r) zum ersten Mal zu Storage navigiert, wird ein Initialisierungsbildschirm angezeigt, der im Namen des Teams eine sichere Verbindung zu Adobe Storage herstellt.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 216
ht-degree: 0%

---

# Initialisieren des Speichers in Workfront Fusion

Der Fusion-Speicherbereich muss initialisiert werden, damit Sie Repositorys, Ordner und Dateien in Ihrem Adobe-Cloud-Speicher anzeigen können.

Einen Überblick über Speicher finden Sie unter [Speicherübersicht](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

## Initialisieren des Speichers

1. Klicken Sie in Workfront Fusion **linken** auf „Speicher“.
1. Klicken Sie **Speicher initialisieren**.

Fusion erstellt im Auftrag des Teams automatisch eine sichere Verbindung zum Adobe-Speicher.

Nachdem die Verbindung hergestellt wurde, lädt Fusion die Speicher-Repositorys des Teams.

## Fehlerbehebung bei der Initialisierung

| Nachricht | Grund | Was der Benutzer tun sollte |
| -------- | -------- | ------------------------ |
| **Zugriff eingeschränkt** | Die Organisation hat sich nicht in Adobe IMS integriert. | Wenden Sie sich an den Organisationsadministrator, um das IMS-Onboarding abzuschließen. |
| **Organisationskonflikt** | Der Benutzer ist bei einer anderen Adobe-Organisation als der in Fusion ausgewählten angemeldet. | Melden Sie sich ab und melden Sie sich dann mit der richtigen Adobe IMS-Organisation wieder an. |
| **Zugriff verweigert** | Das Benutzerkonto verfügt nicht über die erforderlichen Berechtigungen oder Adobe Storage ist für das Unternehmen nicht verfügbar. | Überprüfen Sie die Kontoberechtigungen mit dem Organisations-Admin. Klicken Sie nach dem Auflösen auf **Wiederholen**. |
| **Kein Speicher gefunden** | Die Verbindung wurde hergestellt, aber es wurden keine Repositorys gefunden. | Stellen Sie sicher, dass der Adobe-Speicher für das Unternehmen bereitgestellt wird. Klicken Sie nach der Überprüfung auf **Speicher laden**, um es erneut zu versuchen. |
