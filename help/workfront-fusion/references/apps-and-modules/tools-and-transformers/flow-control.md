---
title: Flusssteuerung
description: Beim Erstellen oder Bearbeiten eines Szenarios können Sie Einstellungen konfigurieren, um den Datenfluss zu steuern.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 2%

---

# Flusssteuerung

Beim Erstellen oder Bearbeiten eines Szenarios können Sie Einstellungen konfigurieren, um den Datenfluss zu steuern.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Repeater

Sie können ein [!UICONTROL Repeater]-Modul verwenden, um eine Aufgabe eine bestimmte Anzahl von Malen zu wiederholen. Ein [!UICONTROL Repeater]-Modul generiert Pakete nacheinander.


<table>
    <tr>
        <td>[!UICONTROL Anfangswert]</td>
        <td>Geben Sie den Wert ein, den das Modul in der ersten Iteration haben soll, oder ordnen Sie ihn zu. Der Standardwert lautet 1.</td>
    </tr>
    <tr>
        <td>[!UICONTROL wiederholt]</td>
        <td>Geben Sie die Anzahl der Wiederholungen des Moduls ein oder mappen Sie sie. Diese Zahl muss größer oder gleich 0 und kleiner oder gleich 10.000 sein.</td>
    </tr>
    <tr>
        <td>[!UICONTROL -Schritt]</td>
        <td>Dies ist die Zahl, um die das Modul den Wert erhöht. Der Standardwert lautet 1.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

Sie können beispielsweise ein [!UICONTROL Repeater]-Modul verwenden, um fünf E-Mails mit den Betreffen „Hello 1“, „Hello 2“ usw. zu senden, indem Sie das Modul **[!UICONTROL E-Mail] > [!UICONTROL E-Mail senden]** mit dem Modul [!UICONTROL Repeater] verbinden.

1. Klicken Sie auf [!UICONTROL Fluss]-Symbol ![Flusssteuerungs-Symbol](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif) unten im Bildschirm und klicken Sie dann im angezeigten Menü auf **[!UICONTROL Repeater]**.
1. Klicken Sie auf das [!UICONTROL Repeater]-Modul und dann in **[!UICONTROL angezeigten Feld auf]** Automatisch verbinden.

   Das Repeater-Modul wird geöffnet.

1. Geben Sie im Feld **[!UICONTROL Wiederholungen]** die Anzahl der Wiederholungen (ausgegebenen Bundles) ein, die das Modul produzieren soll.

   In diesem Beispiel geben Sie 5 ein.

   ![Repeater](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   Der Wert des Elements erhöht sich bei jeder Wiederholung um diesen Wert, der im Feld **[!UICONTROL Schritt]** angegeben ist, das Sie durch Auswahl von **[!UICONTROL Erweiterte Einstellungen anzeigen]** anzeigen können. Diese Zahl ist standardmäßig 1.

1. Klicken Sie **[!UICONTROL OK]**, um das **[!UICONTROL &quot;]**&quot; zu schließen.

1. Klicken Sie auf die App oder das Service-Modul, das mit dem [!UICONTROL Repeater]-Modul verbunden ist.
1. Geben Sie in das sich öffnende Feld die Informationen ein, die Sie wiederholen möchten.

   In unserem E-Mail-Beispiel geben Sie Hello in das Feld [!UICONTROL Subject] ein und ordnen dann `i` aus dem Repeater-Modul zu.

   ![Repeater](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>Die Anzahl der Wiederholungen wird nicht durch den Wert von `i` bestimmt, wie dies bei der Programmierung in einer Schleife der Fall wäre. Das Modul wiederholt die im Feld „Wiederholungen[!UICONTROL &#x200B; angegebenen &#x200B;]. Der Wert `i` ändert sich mit jeder Iteration des [!DNL repeater] Moduls und kann späteren Modulen zugeordnet werden. Im obigen Beispiel wird der Wert von `i` der „Hello“-Nachricht zugeordnet, was zu Meldungen mit dem Wert „Hello 1“, „Hello 2“ usw. führt.

>[!ENDSHADEBOX]

## [!UICONTROL Iterator]

Ein [!UICONTROL Iterator] ist ein spezieller Modultyp, der ein Array in eine Reihe von Bundles konvertiert. Jedes Array-Element ist ein separates Bundle in der Ausgabe des [!UICONTROL Iterator]-Moduls. Weitere Informationen finden Sie unter [Iterator-Modul](/help/workfront-fusion/references/modules/iterator-module.md).

## Array-Aggregator

Ein Array-Aggregator ist ein spezieller Modultyp, mit dem mehrere Bundles zu einem Bundle zusammengeführt werden können. Weitere Informationen finden Sie unter [Aggregator-Modul](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

Das [!UICONTROL Router]-Modul ermöglicht es Ihnen, Ihren Fluss in mehrere Routen zu verzweigen und die Daten innerhalb jeder Route unterschiedlich zu verarbeiten. Sobald ein [!UICONTROL Router]-Modul ein Bundle erhält, leitet es es es an jede angeschlossene Route in der Reihenfolge weiter, in der die Routen an das [!UICONTROL Router]-Modul angehängt wurden. Weitere Informationen finden Sie unter [Router-Modul in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Anweisungen

Mit den Anweisungen zur Fehlerbehandlung können Sie steuern, wie Ihr Szenario auf Fehler reagiert.

Informationen zu Anweisungen zur Fehlerbehandlung finden Sie unter [Anweisungen für die Fehlerbehandlung](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

