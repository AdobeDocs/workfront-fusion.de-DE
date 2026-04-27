---
content-type: reference
title: 'Einrichten und Verwalten von Organisationen und Teams: Artikelindex'
description: Dieser Abschnitt enthält Artikel zum Einrichten und Verwalten von Organisationen und Teams in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: 6762806f17a0fc55531b647a84901b8ca572a997
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 21%

---

# Löschen von Benutzern über die [!DNL Adobe Admin Console]

Sie können einen Benutzer nur aus Adobe Workfront Fusion entfernen, sodass er Zugriff auf alle anderen [!DNL Adobe]-Produktprofile hat, oder den Benutzer vollständig aus dem [!DNL Adobe Admin Console] entfernen.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene</td> 
   <td> 
     <p>Sie müssen ein Adobe Admin Console-Administrator für Ihr Unternehmen sein.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Entfernen eines Benutzers nur aus Adobe Workfront Fusion

Sie können einen Benutzer aus Workfront Fusion entfernen und gleichzeitig seine anderen Adobe-Produktberechtigungen intakt lassen.

Anweisungen finden Sie unter „Entfernen von Benutzenden und Benutzergruppen aus einem Produkt“ im Artikel [Verwalten von Produkten auf Admin Console](https://helpx.adobe.com/de/enterprise/using/manage-products.html).

## Deaktivieren von Benutzern in allen Produkten der [!DNL Adobe Admin Console]

Um einen Benutzer zu löschen, müssen Sie ihn über die [!DNL Adobe Admin Console] deaktivieren.

Ein Benutzer wird aus dem [!DNL Adobe Admin Console] deaktiviert, wenn einer der folgenden Punkte zutrifft:

* Der Benutzer wird aus einem Produkt- oder Produktprofil verschoben und keinem anderen Produkt oder Produktprofil zugewiesen.
* Der Benutzer wird aus einer Gruppe entfernt, die mit einem Produktprofil verknüpft ist, und ist nicht in einer anderen Gruppe enthalten, die mit einem Produktprofil verknüpft ist.
* Der Benutzer wird aus einem Produktprofil entfernt und keinem anderen Produktprofil zugewiesen.
* Der Benutzer wird in der Organisation, die Workfront Fusion umfasst, gelöscht oder deaktiviert.

  Anweisungen finden Sie im Abschnitt „Entfernen von Benutzern“ in [Benutzer einzeln verwalten](https://helpx.adobe.com/de/enterprise/using/manage-users-individually.html).

In Workfront Fusion wirkt sich die Deaktivierung auf eine der folgenden Arten auf die Benutzenden aus:

* Wenn sich der Benutzer nur in einer Organisation befindet, wird der Benutzer deaktiviert.
* Wenn sich der Benutzer in mehr als einer Organisation befindet, wird der Benutzer aus der Organisation entfernt, in der der Benutzer in der [!DNL Adobe Admin Console] geändert wurde.

### Überlegungen beim Löschen eines Benutzers in Workfront Fusion

Beachten Sie beim Löschen eines Benutzers Folgendes.

* Wenn ein Benutzer gelöscht wird, werden die Verbindungen, Schlüssel und Webhooks des Benutzers entfernt.
* Alle Szenarien, die dem Benutzer gehören, werden an den Organisationsbesitzer übertragen. Die Verbindungen in diesen Szenarien müssen aktualisiert werden, da die zum Benutzer gehörenden Verbindungen nicht mehr gültig sind.
* Wenn der gelöschte Benutzer Eigentümer von Anwendungen oder öffentlichen Vorlagen ist, werden die Anwendungen oder öffentlichen Vorlagen an den Organisationseigentümer übertragen. Wenn kein Organisationsverantwortlicher vorhanden ist, werden die Programme oder öffentlichen Vorlagen an einen anderen Benutzer übertragen.
