---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: errors
title: Konfigurieren einer Umgehungslösung zur Fehlerauslösung
description: In einigen Fällen empfiehlt es sich, die Ausführung des Szenarios mit anschließender Rollback- oder Commit-Phase zu stoppen oder die Verarbeitung einer Route zu stoppen und sie optional in der Warteschlange der Ansichten zu speichern und unvollständige Ausführungen in Adobe Workfront Fusion aufzulösen.
author: Becky
feature: Workfront Fusion
exl-id: 4bf2a6c7-16b2-4545-9adf-be3947a7017d
TQID: https://experienceleague.adobe.com/zdEDHRJhIt8dc4Ql835IDypV-CM3YRT5w41mjGDVpSE
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 25%

---

# Konfigurieren `throw` Fehlerumgehung

In einigen Fällen empfiehlt es sich, die Ausführung des Szenarios mit anschließender Rollback- oder Commit-Phase zu stoppen oder die Verarbeitung einer Route zu stoppen und sie optional in der Warteschlange unvollständiger Ausführungen zu speichern.

Derzeit können die Anweisungen zur Fehlerbehandlung nicht außerhalb eines Routenbereichs für Fehlerhandler verwendet werden, und Adobe Workfront Fusion bietet kein Modul, mit dem Sie einfach bedingte Fehler erzeugen (auslösen) können.

Sie können die folgende Problemumgehung verwenden, um `throw` Fehlerfunktionalität nachzuahmen.

Informationen zu unvollständigen Ausführungen finden Sie unter [Anzeigen und Auflösen unvollständiger Ausführungen in Adobe Workfront Fusion](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Informationen zu Anweisungen zur Fehlerbehandlung finden Sie unter [Anweisungen zur Fehlerbehandlung in Adobe Workfront Fusion](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

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
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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
