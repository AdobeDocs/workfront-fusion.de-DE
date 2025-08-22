---
title: Verwenden von cURL zum Hinzufügen eines HTTP-Moduls
description: Sie können eine cURL-Anfrage in Ihr Szenario einfügen, und Fusion erstellt ein HTTP-Modul, das aus der cURL-Anfrage konfiguriert ist.
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 2%

---

# Verwenden von cURL zum Hinzufügen eines HTTP-Moduls

Sie können eine cURL-Anfrage in Ihr Szenario einfügen, und Fusion erstellt ein HTTP-Modul, das aus der cURL-Anfrage konfiguriert ist.

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
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Plan für [!UICONTROL Select] oder [!UICONTROL Prime] Workfront: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>[!UICONTROL Ultimate] Workfront-Plan: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Erstellen eines HTTP-Moduls aus einer cURL-Anfrage


So erstellen Sie ein HTTP-Modul mit cURL:

1. Erstellen Sie den Text der cURL-Anfrage außerhalb von Fusion, z. B. in einem Texteditor.
1. Kopieren Sie die cURL-Anfrage in die Zwischenablage.
1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie das Modul erstellen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie mit der rechten Maustaste auf eine beliebige Leerstelle im Szenario-Editor und wählen Sie **Einfügen**.

   Oder

   Drücken Sie Strg+V (Windows) oder Befehl+V (Mac).


   Ein HTML-Modul wird erstellt.
1. Ziehen Sie das Modul, um es mit Ihrem Szenario zu verbinden.

## Fehlerbehebung

Wenn Ihre cURL nicht in Ihr Szenario eingefügt wird, überprüfen Sie Ihre Browser-Einstellungen, um sicherzustellen, dass das Einfügen aus der Zwischenablage aktiviert ist.
