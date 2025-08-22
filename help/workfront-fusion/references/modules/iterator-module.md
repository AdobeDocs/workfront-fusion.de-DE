---
title: Iterator-Modul
description: Ein Iterator-Modul ist ein spezieller Modultyp, der ein Array in eine Reihe von Bundles konvertiert. Jedes Array-Element wird als separates Bundle ausgegeben.
author: Becky
feature: Workfront Fusion
exl-id: 43d39955-3dd7-453d-8eb0-3253a768e114
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%

---

# [!UICONTROL Iterator]-Modul

Ein [!UICONTROL Iterator] ist ein Modultyp, der ein Array in eine Reihe von Bundles konvertiert. Jedes Array-Element wird als separates Bundle ausgegeben.

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
   <td> Neu: Standard<p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion]-Lizenz</td> 
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


Wenden Sie sich an Ihren Workfront-Administrator, um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## [!UICONTROL Iterator]-Modulkonfiguration

Das allgemeine Iteratormodul hat ein einzelnes Feld, das [!UICONTROL Array]-Feld. Dieses Feld enthält das Array, das konvertiert oder in separate Bundles aufgeteilt werden soll.

![Iterator einrichten](assets/set-up-iterator.jpg)

Andere Connectoren können für diesen Iterator spezifische Iteratormodule enthalten. Diese enthalten ein Source-Modulfeld , mit dem Sie das Modul auswählen können, das das Array ausgibt, das Sie iterieren möchten.

![Spezialisierte Iteratoren](assets/specialized-iterators.jpg)

Weitere Informationen finden Sie unter [Modul konfigurieren](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

>[!BEGINSHADEBOX]

**Beispiele:**

* Das folgende Szenario zeigt, wie Sie E-Mails mit Anhängen abrufen und die Anhänge als einzelne Dateien in einem ausgewählten [!DNL Dropbox] speichern können.

  E-Mails können ein Array von Anhängen enthalten. Das [!UICONTROL Iterator]-Modul nach dem ersten Modul ermöglicht dem Szenario die separate Verarbeitung jeder Anlage. Das [!UICONTROL Iterator]-Modul teilt das Array von Anlagen in einzelne Pakete auf. Jedes Bundle mit einer Anlage wird dann einzeln in einem ausgewählten [!DNL Dropbox]-Ordner gespeichert. Das [!UICONTROL Array] im Iteratormodul sollte das `Attachments`-Array enthalten.

  ![Attachments-Array](assets/attachments-array.jpg)

>[!ENDSHADEBOX]


## Fehlerbehebung

### Problem: Im Zuordnungsbereich werden keine zuordnbaren Elemente unter dem Modul [!UICONTROL Iterator] angezeigt

Wenn ein [!UICONTROL Iterator]-Modul keine Informationen über die Struktur der Elemente des Arrays hat, zeigt das Zuordnungsbedienfeld in den Modulen nach dem [!UICONTROL Iterator]-Modul nur zwei Elemente unter dem [!UICONTROL Iterator]-Modul an: `Total number of bundles` und `Bundle order position`.

![Zuordnungsbereich wird nicht angezeigt](assets/mapping-panel-doesnt-display.png)

Dies liegt daran, dass jedes Modul für die Bereitstellung von Informationen über von ihm ausgegebene Elemente verantwortlich ist, sodass diese Elemente im Zuordnungsbereich in den nachfolgenden Modulen ordnungsgemäß angezeigt werden können. In einigen Fällen können jedoch mehrere Module diese Informationen nicht bereitstellen. Beispielsweise würden [!UICONTROL JSON] > [!UICONTROL JSON parsen] oder [!UICONTROL Webhooks] > [!UICONTROL Custom Webhook]-Module mit fehlender Datenstruktur die Informationen nicht bereitstellen.

#### Lösung

Die Lösung besteht darin, das Szenario manuell auszuführen. Dadurch wird das Modul gezwungen, eine Ausgabe zu erstellen. Fusion kann das Format dieser Ausgabe dann auf spätere Module im Szenario anwenden.

Beispielsweise enthält ein Szenario ein [!UICONTROL JSON] > [!UICONTROL JSON parsen]-Modul ohne Datenstruktur.

![JSON analysieren](assets/json-parse-json.png)

Ein [!UICONTROL Iterator]-Modul, das mit diesem JSON-Modul verbunden ist, kann die Ausgabe des Moduls nicht dem Array-Feld im Setup-Bedienfeld des [!UICONTROL Iterator]-Moduls zuordnen.

![Iterator-Modul verbinden](assets/connect-iterator-module.png)

So beheben Sie das Problem:

Starten Sie das Szenario manuell im Szenario-Editor.

>[!NOTE]
>
>Um zu verhindern, dass das gesamte Szenario ausgeführt wird, haben Sie folgende Möglichkeiten:
>
>* Heben Sie die Verknüpfung der Module nach dem [!UICONTROL JSON] > [!UICONTROL Parsen von JSON]-Modul auf, um zu verhindern, dass der Fluss weiter fortfährt.
>  &#x200B;>   Oder
>* Klicken Sie mit der rechten Maustaste auf das Modul [!UICONTROL JSON] > [!UICONTROL JSON parsen] und wählen Sie **[!UICONTROL Nur dieses Modul ausführen]** aus dem Kontextmenü, um nur das Modul [!UICONTROL JSON] > [!UICONTROL JSON parsen] auszuführen.

Nachdem [!UICONTROL JSON] > [!UICONTROL Parse JSON] ausgeführt wurde, kann es dann Informationen über seine Ausgaben an alle nachfolgenden Module weitergeben, einschließlich des Iterator-Moduls. Das Zuordnungsbedienfeld bei der Einrichtung des Iterators zeigt dann die folgenden Elemente an:

![Das Zuordnungsbedienfeld zeigt Elemente an](assets/mapping-panel-displays-items.png)

Darüber hinaus zeigt das Zuordnungsbedienfeld in den Modulen, die nach dem Modul [!UICONTROL Iterator] verbunden sind, die im Array enthaltenen Elemente an:

![Im Array enthaltene Elemente](assets/items-contained-in-array.png)
