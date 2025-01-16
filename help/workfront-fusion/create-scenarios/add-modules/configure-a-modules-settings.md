---
title: Konfigurieren eines Moduls
description: Sie müssen für jedes Modul, das Sie erstellen, Einstellungen konfigurieren.
author: Becky
feature: Workfront Fusion
exl-id: ae82d1fe-31e1-424a-9c1a-42dc1a20b749
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 2%

---

# Konfigurieren eines Moduls

Sie müssen für jedes Modul, das Sie erstellen, Einstellungen konfigurieren.

Beispielsweise erfordert das Modul Workfront > Dokument hochladen , dass Sie den Datensatz angeben, in den Sie ein Dokument hochladen möchten.

>[!NOTE]
>
>Neben den Moduleinstellungen können Sie auch Einstellungen für ein Szenario anpassen. Sie können unter anderem Ihr Szenario umbenennen, seinen Zeitplan ändern und zusätzliche Einstellungen angeben.

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
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Konfigurieren der Moduleinstellungen

1. Klicken Sie im linken Bedienfeld auf die Registerkarte **[!UICONTROL Scenarios]** .
1. Wählen Sie das Szenario aus, in dem Sie einen Filter hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Fügen Sie einem Szenario ein neues Modul hinzu.

   Oder

   Klicken Sie auf das Modul, das Sie konfigurieren möchten.

1. Erstellen Sie bei Bedarf für das Modul eine **[!UICONTROL Connection]** zu Ihrem registrierten Benutzerkonto für diesen Service, wie unter [Verbindungen - Übersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md) beschrieben.
1. Geben Sie in jedes Feld den entsprechenden Text ein.

   Oder

   Ordnen Sie die Ausgabe eines vorherigen Moduls dem Feld zu.

   Weitere Informationen zur Zuordnung finden Sie unter [Zuordnungsübersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).

   Informationen zu den verschiedenen Elementdatentypen, die [!DNL Workfront Fusion] erkennen können (z. B. Datum, Zahl und Text), finden Sie [Elementdatentypen](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

   >[!NOTE]
   >
   >Fettgedruckte Parameter sind erforderlich.

1. (Bedingt) Wenn das Modul erweiterte Optionen aufweist, die angezeigt und verwendet werden sollen, wählen Sie **[!UICONTROL Show advanced settings]** aus.
