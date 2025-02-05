---
title: Flusskontrolle
description: Beim Erstellen oder Bearbeiten eines Szenarios können Sie Einstellungen konfigurieren, um den Datenfluss zu steuern.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: 5a95b2c191d4e6d8750dc57a47923f416612b4a9
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# Flusskontrolle

Beim Erstellen oder Bearbeiten eines Szenarios können Sie Einstellungen konfigurieren, um den Datenfluss zu steuern.

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
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Keine Workfront Fusion-Lizenzanforderung.</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Prime oder Workfront auswählen: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>Ultimate Workfront-Paket: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Repeater

Sie können ein [!UICONTROL Repeater] Modul verwenden, um eine Aufgabe eine bestimmte Anzahl von Malen zu wiederholen. Ein [!UICONTROL Repeater] Modul erzeugt Pakete, eines nach dem anderen.


<table>
    <tr>
        <td>[!UICONTROL Initial value]</td>
        <td>Geben Sie den Wert ein, den das Modul in der ersten Iteration haben soll, oder ordnen Sie ihn zu. Der Standardwert ist 1.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Repeats]</td>
        <td>Geben Sie die Anzahl der Wiederholungen des Moduls ein oder mappen Sie sie. Diese Zahl muss größer oder gleich 0 und kleiner oder gleich 10.000 sein.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Step]</td>
        <td>Dies ist die Zahl, um die das Modul den Wert erhöht. Der Standardwert ist 1.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

Sie können beispielsweise ein [!UICONTROL Repeater] verwenden, um fünf E-Mails mit den Betreffen „Hallo 1“, „Hallo 2“ usw. zu senden, indem Sie das Modul **[!UICONTROL Email]>[!UICONTROL Send me an email]** mit dem [!UICONTROL Repeater] verbinden.

1. Klicken Sie auf das [!UICONTROL Flow Control] ![Fluss-](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif)-Symbol) unten im Bildschirm und klicken Sie dann im angezeigten Menü auf **[!UICONTROL Repeater]**.
1. Klicken Sie auf das [!UICONTROL Repeater] und dann in dem angezeigten Feld auf **[!UICONTROL Connect automatically]** .

   Das Repeater-Modul wird geöffnet.

1. Geben Sie im Feld **[!UICONTROL Repeats]** die Anzahl der Wiederholungen (ausgegebene Bundles) ein, die das Modul produzieren soll.

   In diesem Beispiel geben Sie 5 ein.

   ![Repeater](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   Der Wert des Elements erhöht sich bei jeder Wiederholung um den im Feld **[!UICONTROL Step]** angegebenen Wert, den Sie durch Auswahl von **[!UICONTROL Show advanced settings]** anzeigen können. Diese Zahl ist standardmäßig 1.

1. Klicken Sie auf **[!UICONTROL OK]** , um das **[!UICONTROL Flow Control]** zu schließen.

1. Klicken Sie auf die App oder das Service-Modul, die bzw. das mit dem [!UICONTROL Repeater] verbunden ist.
1. Geben Sie in das sich öffnende Feld die Informationen ein, die Sie wiederholen möchten.

   In unserem E-Mail-Beispiel würden Sie „Hello“ in das [!UICONTROL Subject] Feld eingeben und dann `i` aus dem Repeater-Modul zuordnen.

   ![Repeater](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>Die Anzahl der Wiederholungen wird nicht durch den Wert von `i` bestimmt, wie dies bei der Programmierung in einer Schleife der Fall wäre. Das Modul wiederholt die im Feld [!UICONTROL Repeats] angegebene Anzahl. Der Wert `i` ändert sich mit jeder Iteration des [!DNL repeater] Moduls und kann späteren Modulen zugeordnet werden. Im obigen Beispiel wird der Wert von `i` der „Hello“-Nachricht zugeordnet, was zu Meldungen mit dem Wert „Hello 1“, „Hello 2“ usw. führt.

>[!ENDSHADEBOX]

## [!UICONTROL Iterator]

Ein [!UICONTROL Iterator] ist ein spezieller Modultyp, der ein Array in eine Reihe von Bundles konvertiert. Jedes Array-Element ist ein separates Bundle in der [!UICONTROL Iterator]. Weitere Informationen finden Sie unter [Iterator-Modul](/help/workfront-fusion/references/modules/iterator-module.md).

## Array-Aggregator

Ein Array-Aggregator ist ein spezieller Modultyp, mit dem mehrere Bundles zu einem Bundle zusammengeführt werden können. Weitere Informationen finden Sie unter [Aggregator-Modul](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

Mit dem [!UICONTROL Router] Modul können Sie Ihren Fluss in mehrere Routen verzweigen und die Daten innerhalb jeder Route unterschiedlich verarbeiten. Sobald ein [!UICONTROL Router] ein Bundle erhält, leitet es es es an jede verbundene Route in der Reihenfolge weiter, in der die Routen an das [!UICONTROL Router]-Modul angehängt wurden. Weitere Informationen finden Sie unter [Router-Modul in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Anweisungen

Mit den Anweisungen zur Fehlerbehandlung können Sie steuern, wie Ihr Szenario auf Fehler reagiert.

Informationen zu Anweisungen zur Fehlerbehandlung finden Sie unter [Anweisungen für die Fehlerbehandlung](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

