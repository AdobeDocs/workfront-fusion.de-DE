---
title: Zuordnen von Daten mithilfe benutzerdefinierter Funktionen
description: Beim Zuordnen von Elementen können Sie Funktionen verwenden, um einfache oder komplexe Formeln zu erstellen.
author: Becky
feature: Workfront Fusion
source-git-commit: 109ea8a6b3c37918110dc930a19ac85ef3e6d764
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 20%

---

# Zuordnen von Daten mithilfe benutzerdefinierter Funktionen

Im Bereich Funktionen von Fusion können Sie benutzerdefinierte Funktionen erstellen. Anschließend fügen Sie diese Funktionen in Form eines Adobe App Builder-Moduls zu Ihren Szenarien hinzu.

Da benutzerdefinierte Funktionen über Adobe App Builder funktionieren, muss Ihr Unternehmen über eine Adobe App Builder-Lizenz verfügen, um sie verwenden zu können.

Benutzerdefinierte Funktionen gehören wie die meisten Szenario-Elemente Teams.

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

Benutzerdefinierte Funktionen werden im Bereich „Funktionen“ von Workfront Fusion konfiguriert. Nachdem eine Funktion konfiguriert wurde, können Sie sie mit dem Adobe App Builder-Connector zu einem Szenario hinzufügen.

### Initialisieren der Laufzeitumgebung

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

### Erstellen einer benutzerdefinierten Funktion

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

## Hinzufügen einer benutzerdefinierten Funktion zu einem Szenario

Um einem Szenario eine benutzerdefinierte Funktion hinzuzufügen, verwenden Sie den Adobe App Builder-Connector.

Anweisungen finden Sie unter [Adobe App Builder-Modul](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

