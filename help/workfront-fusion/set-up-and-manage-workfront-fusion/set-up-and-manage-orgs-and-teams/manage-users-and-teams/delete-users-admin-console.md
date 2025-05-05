---
content-type: reference
title: 'Einrichten und Verwalten von Organisationen und Teams: Artikelindex'
description: Dieser Abschnitt enthält Artikel zum Einrichten und Verwalten von Organisationen und Teams in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Löschen von Benutzern über die [!DNL Adobe Admin Console]

Sie können einen Benutzer nur aus [!DNL Adobe Workfront Fusion] entfernen, sodass der Zugriff auf alle anderen [!DNL Adobe] Produktprofile verbleibt, oder Sie können den Benutzer vollständig aus dem [!DNL Adobe Admin Console] entfernen.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Packstück</td> 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz</td> 
   <td> <p>Neu: [!UICONTROL Standard]</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuell: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>[!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Workfront]: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein [!DNL Adobe Admin Console]-Administrator für Ihre Organisation sein.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Benutzer nur aus [!DNL Adobe Workfront Fusion] entfernen

Sie können einen Benutzer aus Workfront Fusion entfernen, während die anderen Adobe-Produktberechtigungen intakt bleiben.

Anweisungen finden Sie unter „Entfernen von Benutzenden und Benutzergruppen aus einem Produkt“ im Artikel [Verwalten von Produkten in der Admin Console ](https://helpx.adobe.com/de/enterprise/using/manage-products.html).

## Deaktivieren von Benutzern in allen Produkten der [!DNL Adobe Admin Console]

Um einen Benutzer zu löschen, müssen Sie ihn über die [!DNL Adobe Admin Console] deaktivieren.

Ein Benutzer wird aus dem [!DNL Adobe Admin Console] deaktiviert, wenn einer der folgenden Punkte zutrifft:

* Der Benutzer wird aus einem Produkt- oder Produktprofil verschoben und keinem anderen Produkt oder Produktprofil zugewiesen.
* Der Benutzer wird aus einer Gruppe entfernt, die mit einem Produktprofil verknüpft ist, und ist nicht in einer anderen Gruppe enthalten, die mit einem Produktprofil verknüpft ist.
* Der Benutzer wird aus einem Produktprofil entfernt und keinem anderen Produktprofil zugewiesen.
* Der Benutzer wird in der Organisation, die Workfront Fusion umfasst, gelöscht oder deaktiviert.

  Anweisungen finden Sie im Abschnitt „Entfernen von Benutzern“ in [Benutzer einzeln verwalten](https://helpx.adobe.com/de/enterprise/using/manage-users-individually.html).

[!DNL Workfront Fusion] wirkt sich die Deaktivierung auf eine der folgenden Arten auf die Benutzenden aus:

* Wenn sich der Benutzer nur in einer Organisation befindet, wird der Benutzer deaktiviert.
* Wenn sich der Benutzer in mehr als einer Organisation befindet, wird der Benutzer aus der Organisation entfernt, in der der Benutzer in der [!DNL Adobe Admin Console] geändert wurde.
* Beachten Sie beim Löschen eines Benutzers Folgendes.

### Überlegungen beim Löschen eines Benutzers in Workfront Fusion

Beachten Sie beim Löschen eines Benutzers Folgendes.

* Wenn ein Benutzer gelöscht wird, werden die Verbindungen, Schlüssel und Webhooks des Benutzers entfernt.
* Alle Szenarien, die dem Benutzer gehören, werden an den Organisationsbesitzer übertragen. Die Verbindungen in diesen Szenarien müssen aktualisiert werden, da die zum Benutzer gehörenden Verbindungen nicht mehr gültig sind.
* Wenn der gelöschte Benutzer Eigentümer von Anwendungen oder öffentlichen Vorlagen ist, werden die Anwendungen oder öffentlichen Vorlagen an den Organisationseigentümer übertragen. Wenn kein Organisationsverantwortlicher vorhanden ist, werden die Programme oder öffentlichen Vorlagen an einen anderen Benutzer übertragen.
