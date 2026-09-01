---
title: Erstellen von Szenarien aus dem Speicher
description: Storage ist mit dem Szenario Builder von Fusion integriert, sodass Sie vorkonfigurierte Szenarien direkt auf der Storage-Seite erstellen können, um Dateien herunterzuladen oder hochzuladen.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: aef1685cb25c0cdcb0dcdf9b0c73fb482d392e5f
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 0%

---

# Erstellen von Szenarien aus dem Speicher

Einen Überblick über Speicher finden Sie unter [Speicherübersicht](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

Storage lässt sich mit dem Szenario Builder von Fusion integrieren. Auf der Seite „Speicherung“ können Benutzer ein Szenario erstellen, in dem die ausgewählte Datei heruntergeladen wird.

## In Szenario herunterladen

1. Klicken Sie in Workfront Fusion **linken** auf „Speicher“.
1. Navigieren Sie zum Repository, das die Datei enthält, die Sie in einem Szenario herunterladen möchten.
1. Wählen Sie eine Datei aus und klicken Sie dann in der Aktionsleiste auf **In Szenario herunterladen**.

Fusion erstellt dann ein neues Szenario mit dem Namen **Download {fileName}&quot;**. Dieses Szenario wird in einer separaten Browser-Registerkarte geöffnet.

Das Szenario ist wie folgt vorkonfiguriert:

* Die aktive Verbindung.
* Repository, Ordner und Datei sind vorausgewählt.
* Ein Modul zum Generieren einer vordefinierten Download-URL.
* Ein HTTP-Modul zum Abrufen der Datei von dieser URL.
* Ein standardmäßiges Zeitplanintervall von 15 Minuten.

## Datei in Szenario hochladen

1. Klicken Sie in Workfront Fusion **linken** auf „Speicher“.
1. Navigieren Sie zum Repository und Ordner, der die Datei enthält, die Sie in einem Szenario herunterladen möchten.
1. Klicken Sie beim Durchsuchen eines Ordners auf das **-Dropdown-Menü „Datei hochladen**.
1. Wählen Sie **Datei in Szenario hochladen“**.

Fusion erstellt dann ein neues Szenario mit dem Namen **In {folderName} hochladen“**. Dieses Szenario wird in einer neuen Browser-Registerkarte geöffnet. Sie müssen Module hinzufügen, um die Datei bereitzustellen, die Sie hochladen möchten, z. B. das Modul Workfront > Dokument herunterladen .

Das Szenario ist wie folgt vorkonfiguriert:

* Die aktive Verbindung.
* Repository und Ordner sind vorausgewählt.
* Ein Modul zum Generieren einer vordefinierten Upload-URL mit einem Platzhalterdateinamen.
* Ein standardmäßiges Zeitplanintervall von 15 Minuten.

