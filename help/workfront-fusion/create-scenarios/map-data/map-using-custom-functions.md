---
title: Zuordnen von Daten mithilfe benutzerdefinierter Funktionen
description: Beim Zuordnen von Elementen können Sie Funktionen verwenden, um einfache oder komplexe Formeln zu erstellen.
author: Becky
feature: Workfront Fusion
exl-id: dc4e697a-a65c-48bc-99de-8e26fbeb7ba7
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: c716296d771974ffdb59e916f9865c9efb2ad5a9
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 11%
---
# Zuordnen von Daten mithilfe benutzerdefinierter Funktionen

Im Bereich Funktionen von Fusion können Sie benutzerdefinierte Funktionen erstellen. Anschließend fügen Sie diese Funktionen in Form eines Adobe App Builder-Moduls zu Ihren Szenarien hinzu.

Da benutzerdefinierte Funktionen über Adobe App Builder funktionieren, muss Ihr Unternehmen über eine Adobe App Builder-Lizenz verfügen, um sie verwenden zu können.

Benutzerdefinierte Funktionen gehören wie die meisten Szenario-Elemente Teams.

Bei Funktionen handelt es sich um einfache JavaScript-Funktionen. Um Variablen oder Abhängigkeiten in Ihre Funktionslogik aufzunehmen, verwenden Sie Pakete.

Informationen zu Paketen finden Sie unter [Verwenden benutzerdefinierter Funktionspakete](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

Workfront Fusion enthält auch integrierte Funktionen, mit denen Sie einfache oder komplexe Formeln erstellen können. Diese Funktionen decken eine Vielzahl von Anwendungsfällen ab, einschließlich Funktionen für Arrays, Zeichenfolgen, Zahlen und Daten aus vorherigen Modulen.

Informationen und Anweisungen zu integrierten Funktionen finden Sie unter [Zuordnen eines Elements mithilfe integrierter Funktionen](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

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
   <p><ul><li>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li><li>Sie benötigen eine Adobe App Builder-Lizenz, um benutzerdefinierte Funktionen verwenden zu können.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Konfigurieren einer benutzerdefinierten Funktion

Sie können im Bereich Funktionen eine benutzerdefinierte Funktion erstellen, die in mehreren Szenarien verwendet werden kann, oder Sie können benutzerdefinierte Funktionen in einzelnen Szenarien konfigurieren.

* [Erstellen einer benutzerdefinierten Funktion zur Verwendung in mehreren Szenarien](#create-a-custom-function-to-use-in-multiple-scenarios)
* [Erstellen einer benutzerdefinierten Funktion innerhalb eines Szenarios](#create-a-custom-function-within-a-scenario)

### Erstellen einer benutzerdefinierten Funktion zur Verwendung in mehreren Szenarien

Benutzerdefinierte Funktionen, die in mehreren Szenarien verwendet werden können, werden im Bereich „Funktionen“ von Workfront Fusion konfiguriert. Nachdem eine Funktion konfiguriert wurde, können Sie sie mit dem Adobe App Builder-Connector zu einem Szenario hinzufügen.

* [Initialisieren der Laufzeitumgebung](#initialize-your-runtime-environment)
* [Ein bestehendes App Builder-Projekt verbinden](#connect-an-existing-app-builder-project)
* [Erstellen einer benutzerdefinierten Funktion im Bereich „Funktionen“](#create-a-custom-function-in-the-functions-area)

#### Initialisieren der Laufzeitumgebung

Bevor Sie benutzerdefinierte Funktionen erstellen können, müssen Sie Ihre Laufzeitumgebung initialisieren. Dies muss nur erfolgen, wenn Ihr Team keine benutzerdefinierten Funktionen hat.

>[!IMPORTANT]
>
>Die Initialisierung kann nur von einem Anwender mit Zugriff auf Adobe App Builder durchgeführt werden, entweder von einem Entwickler oder einem Systemadministrator innerhalb der IMS-Organisation.
>
>Nach Abschluss der Initialisierung können alle Benutzer im Team, in dem die Initialisierung durchgeführt wurde, Funktionen erstellen und verwenden.

1. Klicken Sie auf **Registerkarte** Funktionen![&#x200B; (](assets/functions-icon.png)) im linken Bedienfeld.

   Wenn Sie Ihre Laufzeit noch nicht konfiguriert haben, wird die Meldung „Laufzeitumgebung nicht konfiguriert“ angezeigt.
1. Klicken Sie **Laufzeit initialisieren**.

   Nach einiger Zeit wird eine Liste Funktionen mit zwei Beispielfunktionen angezeigt.

#### Ein bestehendes App Builder-Projekt verbinden

Wenn Fusion das App Builder-Projekt erstellt, übernimmt es die Laufzeiteinrichtung für Sie. Wenn Ihr Team bereits über ein App Builder-Projekt verfügt, das erstellt wurde, bevor Sie Fusion verwendet haben, müssen Sie es manuell verbinden, indem Sie eine App Builder-Verbindung erstellen, die den Runtime-Namespace und die Anmeldeinformationen dieses Projekts verwendet. Sie müssen das Projekt nicht neu erstellen.

>[!NOTE]
>
>Die Anmeldeinformationen, die Sie in Fusion eingeben, sind Laufzeitanmeldeinformationen. Es handelt sich nicht um Ihre Adobe-Anmeldedaten. Bewahren Sie die Konfigurationsdatei, die Sie herunterladen, sicher auf und geben Sie ihren `auth` nicht weiter.

1. Wählen Sie in Fusion das Team aus, das die Verbindung benötigt.
1. Klicken Sie im linken Bereich auf **Verbindungen** und dann auf **Verbindung erstellen**.
1. Wählen Sie **Adobe App Builder** als Verbindungstyp aus und geben Sie einen Namen ein, der das vorhandene Projekt identifiziert.
1. Öffnen Sie in der [Adobe Developer Console](https://developer.adobe.com/console) das vorhandene Projekt und wählen Sie dann den Arbeitsbereich aus, mit dem Sie eine Verbindung herstellen möchten.
1. Klicken Sie in der Projektübersicht auf **Alle herunterladen**, um die JSON-Datei für die Workspace-Konfiguration herunterzuladen, und öffnen Sie die Datei in einem Texteditor.
1. Suchen Sie im `runtime` Abschnitt der Datei den `namespace`. Geben Sie sie in Fusion im Feld **Namespace** ein.
1. Suchen Sie im Abschnitt `runtime` nach dem `auth`. Es hat das Format `username:password`.

   * Geben Sie in Fusion das Teil vor dem Doppelpunkt im Feld **Benutzername** ein.
   * Geben Sie in Fusion das Teil nach dem Doppelpunkt im Feld **Kennwort** ein.

1. Klicken Sie **Fortfahren**, um die Verbindung zu speichern.
1. Kehren Sie zur Registerkarte **Funktionen** in Fusion zurück und aktualisieren Sie die Seite bei Bedarf.

Weitere Informationen zu den Verbindungsfeldern finden Sie unter [Adobe App Builder-Module](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md#create-a-connection-to-adobe-app-builder).

#### Erstellen einer benutzerdefinierten Funktion im Bereich „Funktionen“

Nachdem Ihre Laufzeitumgebung konfiguriert wurde, können Sie mit der Erstellung benutzerdefinierter Funktionen beginnen.

>[!IMPORTANT]
>
>* Ihre benutzerdefinierte Funktion **muss** eine JavaScript-Funktion sein.
>* Ihre benutzerdefinierte Funktion **muss** ein -Objekt zurückgeben.
>* Nach dem Erstellen einer benutzerdefinierten Funktion ist Folgendes nicht mehr möglich:
>
>   * Name ändern
>   * Standardparameterwerte anzeigen

1. Klicken Sie auf **Registerkarte** Funktionen![&#x200B; (](assets/functions-icon.png)) im linken Bedienfeld.
1. Klicken Sie **Funktion hinzufügen**.
1. Geben Sie einen Namen für die benutzerdefinierte Funktion ein.

   Sie können diesen Namen später nicht mehr ändern.
1. Geben Sie den Code für die Funktion ein.
1. Klicken Sie für jeden Standardparameterwert, den Sie hinzufügen möchten, auf **Parameter hinzufügen** und geben Sie den Parameternamen und den Standardwert ein.

   Sie können Standardparameter überschreiben, wenn Sie die Funktion zu einem Szenario hinzufügen.
1. Klicken Sie auf **Speichern**.

### Erstellen einer benutzerdefinierten Funktion innerhalb eines Szenarios

Um innerhalb eines Szenarios eine benutzerdefinierte Funktion zu erstellen, verwenden Sie das Modul **Benutzerdefinierten Codeblock ausführen** im Adobe App Builder Connector.

Anweisungen finden Sie unter [Adobe App Builder-Modul](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

## Hinzufügen einer benutzerdefinierten Funktion zu einem Szenario

Um einem Szenario eine benutzerdefinierte Funktion hinzuzufügen, verwenden Sie den Adobe App Builder-Connector.

Anweisungen finden Sie unter [Adobe App Builder-Modul](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

