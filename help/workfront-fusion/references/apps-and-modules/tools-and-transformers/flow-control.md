---
title: Flusskontrolle
description: Beim Erstellen oder Bearbeiten eines Szenarios können Sie Einstellungen konfigurieren, um den Datenfluss zu steuern.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---

# Flusskontrolle

Beim Erstellen oder Bearbeiten eines Szenarios können Sie Einstellungen konfigurieren, um den Datenfluss zu steuern.

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Plan*</td>
  <td> <p>[!UICONTROL Pro] oder höher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung und -integration], [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den [!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Adobe Workfront] verfügen, muss Ihr Unternehmen [!DNL Adobe Workfront Fusion] kaufen und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden. [!DNL Workfront Fusion] ist im [!UICONTROL Ultimate] [!DNL Workfront] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Repeater

Sie können ein [!UICONTROL Repeater] Modul verwenden, um eine Aufgabe eine bestimmte Anzahl von Malen zu wiederholen. Ein [!UICONTROL Repeater] Modul erzeugt Pakete, eines nach dem anderen.

Sie können beispielsweise ein [!UICONTROL Repeater] verwenden, um fünf E-Mails mit den Betreffen „Hallo 1“, „Hallo 2“ usw. zu senden, indem Sie das Modul **[!UICONTROL Email]>[!UICONTROL Send me an email]** mit dem [!UICONTROL Repeater] verbinden.

So verwenden Sie ein [!UICONTROL Repeater]:

1. Klicken Sie auf das [!UICONTROL Flow Control] ![Fluss-](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif)-Symbol) unten im Bildschirm und klicken Sie dann im angezeigten Menü auf **[!UICONTROL Repeater]**.
1. Klicken Sie auf das Bundle [!UICONTROL Repeater] und dann in dem angezeigten Feld auf **[!UICONTROL Connect automatically]** .
1. Geben Sie in das [!UICONTROL Flow Control] Feld die gewünschte Anzahl von Wiederholungen (ausgegebene Bundles) in das Feld **[!UICONTROL Repeats]** ein.

   In unserem E-Mail-Beispiel würden Sie 5 eingeben.

   ![Repeater](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   Der Wert des Elements erhöht sich bei jeder Wiederholung um den im Feld **[!UICONTROL Step]** angegebenen Wert, den Sie durch Auswahl von **[!UICONTROL Show advanced settings]** anzeigen können. Diese Zahl ist standardmäßig 1.

1. Klicken Sie auf **[!UICONTROL OK]** , um das **[!UICONTROL Flow Control]** zu schließen.

1. Klicken Sie auf die App oder das Service-Modul, die bzw. das mit dem [!UICONTROL Repeater] verbunden ist.
1. Geben Sie in das sich öffnende Feld die Informationen ein, die Sie wiederholen möchten.

   In unserem E-Mail-Beispiel würden Sie „Hello“ in das [!UICONTROL Subject] Feld eingeben und dann `i` aus dem Repeater-Modul zuordnen.

   ![Repeater](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)

| Element | Beschreibung |
|---|---|
| [!UICONTROL Initial value] | Geben Sie die Zahl ein, die das Modul in der ersten Iteration als `i` festlegen soll, oder ordnen Sie sie zu. Der Standardwert ist 1. |
| [!UICONTROL Repeats] | Geben Sie die Anzahl der Wiederholungen des Moduls ein oder mappen Sie sie. Diese Zahl muss größer oder gleich 0 und kleiner oder gleich 10.000 sein. |
| [!UICONTROL Step] | Dies ist die Zahl, um die das Modul den Wert von `i` erhöht. Der Standardwert ist 1. |

{style="table-layout:auto"}

>[!NOTE]
>
>Die Anzahl der Wiederholungen wird nicht durch den Wert von `i` bestimmt, wie dies bei der Programmierung in einer Schleife der Fall wäre. Das Modul wiederholt die im Feld [!UICONTROL Repeats] angegebene Anzahl. Der Wert `i` ändert sich mit jeder Iteration des [!DNL repeater] Moduls und kann späteren Modulen zugeordnet werden. Im obigen Beispiel wird der Wert von `i` der „Hello“-Nachricht zugeordnet, was zu Meldungen mit dem Wert „Hello 1“, „Hello 2“ usw. führt.

## [!UICONTROL Iterator]

Ein [!UICONTROL Iterator] ist ein spezieller Modultyp, der ein Array in eine Reihe von Bundles konvertiert. Jedes Array-Element ist ein separates Bundle in der [!UICONTROL Iterator]. Weitere Informationen finden Sie unter [Iterator-Modul](/help/workfront-fusion/references/modules/iterator-module.md).

## Array-Aggregator

Ein Array-Aggregator ist ein spezieller Modultyp, mit dem mehrere Bundles zu einem Bundle zusammengeführt werden können. Weitere Informationen finden Sie unter [Aggregator-Modul](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

Mit dem [!UICONTROL Router] Modul können Sie Ihren Fluss in mehrere Routen verzweigen und die Daten innerhalb jeder Route unterschiedlich verarbeiten. Sobald ein [!UICONTROL Router] ein Bundle erhält, leitet es es es an jede verbundene Route in der Reihenfolge weiter, in der die Routen an das [!UICONTROL Router]-Modul angehängt wurden. Weitere Informationen finden Sie unter [Router-Modul in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

<!--
<div>
<h2>Directives</h2>
<p>The error handling directives allow you to control how your scenario reacts to errors. For more information, see <a href="/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md" class="MCXref xref">Advanced error handling in Adobe Workfront Fusion</a> and <a href="/help/workfront-fusion/references/errors/directives-for-error-handling.md" class="MCXref xref">Directives for error handling in Adobe Workfront Fusion</a>.</p>
</div>
-->
