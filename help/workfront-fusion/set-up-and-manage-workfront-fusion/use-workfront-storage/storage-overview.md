---
title: Speicherübersicht
description: Der Speicher ist eine Seite in Workfront Fusion, die Teams direkten Zugriff auf ihre Adobe Enterprise Storage Management (ESM)-Repositorys bietet, sodass Anwender Ordner durchsuchen, Dateien hochladen und herunterladen, den Versionsverlauf anzeigen und Automatisierungsszenarien erstellen können.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: d5568479d43bd5518adae5b66b132b4075e7f356
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 2%

---

# Speicherübersicht

<!--Add to navigation articles once this goes to production-->

Der Speicherbereich in Workfront Fusion bietet Teams direkten Zugriff auf ihre Adobe Enterprise Storage Management (ESM)-Repositorys. Benutzer können Ordner durchsuchen, Dateien hochladen und herunterladen, Versionsverläufe anzeigen und Automatisierungsszenarien erstellen, ohne Fusion verlassen zu müssen.

Der Speicher gehört Teams und erfordert, dass das Unternehmen ein Onboarding für das Adobe Identity Management System (IMS) mit Zugriff auf den Adobe-Speicher durchführt.

Dateien im Fusion-Speicher werden in Adobe Files (adobe.com/files) gespiegelt, sodass auf alle Dateien, auf die in Adobe Files zugegriffen werden kann, im Fusion-Speicher zugegriffen werden kann.

Anweisungen zur Verwendung von Storage finden Sie unter:

* [Initialisieren des Speichers](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md)
* [Anzeigen und Verwalten von Speicher in Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-and-manage-storage-in-workfront-fusion.md)
* [Dateien in Speicher hochladen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/upload-files-to-storage.md)
* [Dateien aus dem Speicher herunterladen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/download-files-from-storage.md)
* [Löschen von Dateien aus dem Speicher](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/delete-files-from-storage.md)
* [Anzeigen des Dateiversionsverlaufs im Speicher](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-storage-file-version-history.md)
* [Erstellen von Szenarien aus dem Speicher](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/create-scenarios-from-storage.md)

## Voraussetzungen für die Speicherung

Um den Workfront Fusion-Speicherbereich verwenden zu können, muss Folgendes zutreffen:

* Das Unternehmen hat sich in das **Adobe Identity Management System (IMS) integriert**
* Das Unternehmen verfügt über **Adobe-Speicher**
* Der Benutzer ist bei der **richtigen Adobe IMS-Organisation** angemeldet (die der ausgewählten Fusion-Organisation entspricht)
* Das Benutzerkonto hat (Zugriff **den Adobe-Speicher**

## Glossar

Bei Verwendung von

| Begriff | Definition |
| ------ | ----------- |
| **Repository** | Ein Speicher-Container der obersten Ebene in Adobe ESM, der normalerweise einem Projekt oder Arbeitsbereich zugeordnet ist |
| **Verbindung** | Eine sichere Verbindung zwischen Fusion und dem Adobe-Speicher, die während der Initialisierung automatisch erstellt wird. Verwendet Adobe IMS-Authentifizierung mit automatischer Token-Aktualisierung |
| **ESM** | Enterprise Storage Management, Adobes Cloud-Dateispeicherungs-Service |
| **IMS** | Adobe Identity Management System, die Authentifizierungs- und Identitätsplattform von Adobe |

<!--

## UI Reference — Key Screens

### 1. Initialization Screen

* Cloud icon with **"Adobe Storage"** heading
* Description text explaining the feature
* **"Initialize Storage"** button (primary action)
* Error variants for access restriction, org mismatch, access denied, no storage found

### 2. Repository List

* Table with **Name** and **Region** columns
* **"Open"** action button per row

### 3. File Browser

* Breadcrumb navigation bar
* **"Upload File"** dropdown button (with "Upload File" and "Upload File in Scenario" options)
* File/folder table with **Name**, **Type**, **Size**, **Created** columns
* Floating action bar on file selection with: **Download**, **Download in Scenario**, **Versions**, **Delete**
* Upload/download progress banners (top-right corner)

### 4. Version History Panel

* Right-side slide-out panel
* Version list with date, version badge, and download button per entry
* **"current"** label on the latest version

-->
