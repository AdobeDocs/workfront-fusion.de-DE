---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: errors
title: Problemumgehung für Wurffehler konfigurieren
description: In einigen Fällen empfiehlt es sich, die Ausführung des Szenarios mit anschließender Rollback- oder Commit-Phase zu stoppen oder die Verarbeitung einer Route zu stoppen und sie optional in der Warteschlange der Ansichten zu speichern und unvollständige Ausführungen in Adobe Workfront Fusion aufzulösen.
author: Becky
feature: Workfront Fusion
exl-id: 4bf2a6c7-16b2-4545-9adf-be3947a7017d
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

---

# Konfigurieren `throw` Fehlerumgehung

In einigen Fällen empfiehlt es sich, die Ausführung des Szenarios mit anschließender Rollback- oder Commit-Phase zu stoppen oder die Verarbeitung einer Route zu stoppen und sie optional in der Warteschlange unvollständiger Ausführungen zu speichern.

Derzeit können die Anweisungen zur Fehlerbehandlung nicht außerhalb eines Routenbereichs für Fehlerhandler verwendet werden, und Adobe Workfront Fusion bietet kein Modul, mit dem Sie einfach bedingte Fehler erzeugen (auslösen) können.

Sie können die folgende Problemumgehung verwenden, um `throw` Fehlerfunktionalität nachzuahmen.

Informationen zu unvollständigen Ausführungen finden Sie unter [Anzeigen und Auflösen unvollständiger Ausführungen in Adobe Workfront Fusion](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Informationen zu Anweisungen zur Fehlerbehandlung finden Sie unter [Anweisungen zur Fehlerbehandlung in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz</td> 
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Prime oder Workfront-Plan auswählen: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>Ultimate Workfront Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Problemumgehung für `throw`

Um einen Fehler bedingt auszulösen, können Sie ein Modul so konfigurieren, dass es während seines Vorgangs absichtlich fehlschlägt. Eine Möglichkeit besteht darin, das Modul [!UICONTROL JSON] > [!UICONTROL Parse JSON] zu verwenden, das so konfiguriert ist, dass es optional einen Fehler auslöst (in diesem `BundleValidationError`):

![JSON-Fehler](assets/json-parse-json.png)

Anschließend können Sie eine der Fehlerbehandlungsanweisungen an die Fehlerbehandlungsroute anhängen:

* **Rollback**: Erzwingt, dass die Ausführung des Szenarios angehalten und die Rollback-Phase durchgeführt wird.
* **Bestätigen**: Erzwingt, dass die Ausführung des Szenarios angehalten wird und die Commit-Phase durchgeführt wird.
* **Ignorieren**: Beendet die Verarbeitung einer Route.
* **break**: Beendet die Verarbeitung einer Route und speichert sie in der Warteschlange der unvollständigen Ausführungsordner.

Das folgende Beispiel zeigt die Verwendung der [!DNL Rollback]-Direktive:

![Rollback-Direktive](assets/rollback-directive.png)
