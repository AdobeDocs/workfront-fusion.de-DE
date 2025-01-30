---
title: Datenspeicher in [!DNL Adobe Workfront Fusion]
description: Ein Datenspeicher, ähnlich einer Datenbank oder einer einfachen Tabelle, kann Daten aus Szenarien speichern und ermöglicht so die Übertragung von Daten zwischen einzelnen Szenarien oder Szenarioausführungen. Sie können einen Datenspeicher verwenden, um während der Synchronisierung neue Daten aus verschiedenen Systemen zu speichern.
author: Becky
feature: Workfront Fusion
exl-id: 8bfa3201-45db-49d7-985d-9c324acd56b6
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1215'
ht-degree: 1%

---

# Erstellen und Verwalten von Datenspeichern

Ein Datenspeicher, ähnlich einer Datenbank oder einer einfachen Tabelle, kann Daten aus Szenarien speichern und ermöglicht so die Übertragung von Daten zwischen einzelnen Szenarien oder Szenarioausführungen. Sie können einen Datenspeicher verwenden, um während der Synchronisierung neue Daten aus verschiedenen Systemen zu speichern.

Mit den Datenspeichermodulen können Sie die folgenden Aktionen für Datensätze in Ihrem [!DNL Adobe Workfront Fusion] Datenspeicher durchführen:

* Hinzufügen
* Ersetzen
* Aktualisieren
* abrufen
* Löschen
* Suchen
* Count

Informationen zur Verwendung von Datenspeichermodulen finden Sie unter [[!UICONTROL Data store] Module](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/data-store-modules.md).

Eine Videoeinführung zu Datenspeichern in Workfront Fusion finden Sie unter:

* [Datenspeicher](https://video.tv.adobe.com/v/3427029/){target=_blank}

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

## Verfügbarer Datenspeicher

Wenn Ihr Unternehmen das neue Workfront-Abo-Modell verwendet (die Pakete Select, Prime und Ultimate), wirkt sich der Plan Ihres Unternehmens auf die Größe und Anzahl der in Ihrer Fusion-Instanz verfügbaren Datenspeicher aus.

### Ultimate-Plan

Fusion-Instanzen im Ultimate-Paket erhalten:

* 100 MB Speicherplatz
* 50 Datenspeicher

### Prime-Pläne auswählen

Fusion-Instanzen der Select- oder Prime-Pakete erhalten:—>

* 100 MB für die ersten 500.000 Vorgänge.

* 10 MB für jeden zusätzlichen 100.000-Arbeitsgänge.

  Beispielsweise erhält eine Organisation mit 600.000 Vorgängen 110 MB.

Ihr Unternehmen kann über bis zu 50 Datenspeicher verfügen. Die Gesamtgröße dieser Datenspeicher darf die Gesamtgröße der Datenspeicher Ihres Unternehmens nicht überschreiten.

## Erstellen eines Datenspeichers in [!DNL Workfront Fusion]

* [Einrichten des Datenspeichers](#set-up-the-data-store)
* [Einrichten der Datenstruktur](#set-up-the-data-structure)

### Einrichten des Datenspeichers

Bevor Sie einen Datenspeicher in einem Modul verwenden können, müssen Sie den Datenspeicher in [!DNL Workfront Fusion] erstellen.

>[!NOTE]
>
>Ihre Organisation verfügt über eine begrenzte Anzahl verfügbarer Datenspeicher. Wenn Sie versuchen, mehr Datenspeicher zu erstellen, als Ihnen zur Verfügung stehen, gibt [!DNL Workfront] einen [!UICONTROL Maximum stores reached] zurück.
>
>Weitere Informationen finden Sie unter [Fehler: Maximal erreichte Stores](#maximum-stores-reached-error) in diesem Artikel.

1. Melden Sie sich bei Ihrem [!DNL Workfront Fusion] an.
1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Data stores]** .
1. Klicken Sie oben rechts im Bildschirm auf **[!UICONTROL Add data store]** .
1. Geben Sie die Einstellungen für den neuen Datenspeicher ein.

   Ein fett gedruckter Titel auf einem Feld in einem [!DNL Workfront Fusion] Modul zeigt eine erforderliche Einstellung an.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Data store name] </td> 
      <td> <p>Geben Sie einen Namen für den Datenspeicher ein. </p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Data Structure]</p> </td> 
      <td> <p>Eine Datenstruktur ist eine Liste der Spalten für eine Tabelle. Diese Liste gibt den Spaltennamen und den Datentyp an.</p> <p>Führen Sie einen der folgenden Schritte aus:</p> 
       <ul> 
        <li><b>Eine bereits erstellte Datenstruktur auswählen</b></li> 
        <li><b>Neue Datenstruktur hinzufügen</b> <p>Klicken Sie auf <strong>[!UICONTROL Add]</strong> , um eine neue Datenstruktur zu erstellen.</p> <p>Weitere Informationen finden Sie <a href="#set-up-the-data-structure" class="MCXref xref"> Abschnitt „Einrichten der </a>" in diesem Artikel.</p> </li> 
        <li style="font-weight: bold;"> <p>Lassen Sie das Feld leer</p> <p style="font-weight: normal;">Wenn Sie keine Datenstruktur auswählen oder hinzufügen, enthält die Datenbank nur den Primärschlüssel. Ein solcher Datenbanktyp ist nützlich, wenn Sie nur Schlüssel speichern möchten und nur daran interessiert sind zu erfahren, ob ein bestimmter Schlüssel in der Datenbank vorhanden ist oder nicht.</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>Datenspeichergröße in MB</td> 
      <td> <p>Weisen Sie die Größe für den Datenspeicher aus Ihrem gesamten internen Datenspeicher zu.</p> <p> Der Standardwert ist 10 MB. Wenn Sie weniger als 10 MB nicht zugewiesenen Datenspeicherplatz aus Ihrer 95-MB-Zuteilung haben, ist die Standardgröße die Menge des nicht zugewiesenen Speichers.  <p>Hinweis: Der reservierte Betrag kann jederzeit geändert werden.</p>  </td> 
     </tr> 
    </tbody> 
   </table>

### Einrichten der Datenstruktur

1. Klicken Sie beim Erstellen oder Bearbeiten eines Datenspeichers auf **[!UICONTROL Add]**.
1. Konfigurieren Sie im angezeigten **[!UICONTROL Add data structure]** die folgenden Felder:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Data structure name]</td> 
      <td> <p> Geben Sie einen Namen für die neue Datenstruktur ein.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Specification]</p> </td> 
      <td> <p>Führen Sie einen der folgenden Schritte aus, um die Spalten Ihres Datenspeichers einzurichten.</p> 
       <ul> 
        <li> <p>Klicken Sie auf <strong>[!UICONTROL Add item]</strong> , um die Eigenschaften einer Spalte manuell anzugeben.</p> <p>Geben Sie die <strong>[!UICONTROL Name]</strong> und <strong>[!UICONTROL Type]</strong> für die Datenspeicherspalte ein und definieren Sie die entsprechenden Eigenschaften.</p> </li> 
        <li> <p>Klicken Sie auf <strong>[!UICONTROL Generator]</strong> , um die Spalten aus den von Ihnen bereitgestellten Beispieldaten zu bestimmen.</p> 
         <div class="example" data-mc-autonum="<b>Example: </b>">
          <span class="autonumber"><span><b>Beispiel: </b></span></span> 
          <p>Beispielsweise werden mit den folgenden JSON-Beispieldaten drei Spalten erstellt: Name, Alter und Telefonnummer. Eine Telefonnummer ist eine Sammlung von Handy- und Festnetztelefonnummern.</p> 
          <p><code>&lbrace;</code> </p> 
          <p><code>"name":"John",</code> </p> 
          <p><code>"age":30,</code> </p> 
          <p><code>"phone number": &lbrace;</code> </p> 
          <p><code>"mobile":"987654321",</code> </p> 
          <p><code>"landline":"123456789"</code> </p> 
          <p><code>&rbrace;</code> </p> 
          <p><code>&rbrace;</code> </p> 
          <p>Die leeren Spalten in der Datenspeicheransicht:</p> 
          <p> <img src="assets/empty-columns-350x132.png" style="width: 350;height: 132;"> </p> 
          <p>Sie können Werte manuell oder mithilfe der [!DNL Workfront Fusion] Datenspeichermodule zum Datenspeicher hinzufügen.</p> 
         </div> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Strict] </td> 
      <td> <p>Aktivieren Sie diese Option, um sicherzustellen, dass die Payload mit den Datenstrukturen übereinstimmt. Payloads, die zusätzliche Elemente enthalten, die nicht in der Datenstruktur angegeben sind, werden abgelehnt.</p> </td> 
     </tr> 
    </tbody> 
   </table>

## Bearbeiten eines vorhandenen Datenspeichers

Sie können die Eigenschaften und Inhalte eines vorhandenen Datenspeichers im [!UICONTROL Data stores] von [!DNL Workfront Fusion] bearbeiten.

* [Bearbeiten der Eigenschaften eines Datenspeichers](#edit-the-properties-of-a-data-store)
* [Bearbeiten des Inhalts eines Datenspeichers](#edit-the-contents-of-a-data-store)

### Bearbeiten der Eigenschaften eines Datenspeichers

Zu den Eigenschaften eines Datenspeichers gehören die Datenstruktur, die der Datenspeicher verwendet, sowie die Größe des Datenspeichers.

1. Klicken Sie **[!UICONTROL Data stores]** linken ](assets/data-store-icon.png) auf ![Datenspeichersymbol), um den [!UICONTROL Data stores] zu öffnen.
1. Klicken Sie **[!UICONTROL Edit]** ![Datenspeicher bearbeiten](assets/data-store-edit.png) neben dem Datenspeicher, den Sie bearbeiten möchten.
1. (Optional) Wenn Sie die von diesem Datenspeicher verwendete Datenstruktur in eine andere vorhandene Datenstruktur ändern möchten, wählen Sie sie aus der Dropdown-Liste **[!UICONTROL Data structure]** aus.

   Oder

   (Optional) Wenn Sie die von diesem Datenspeicher verwendete Datenstruktur in eine völlig neue Datenstruktur ändern möchten, finden Sie weitere Informationen unter [Einrichten der Datenstruktur](#set-up-the-data-structure) in diesem Artikel.

1. (Optional) Ändern Sie die Größe des Datenspeichers, indem Sie die neue Größe in das Feld **[!UICONTROL Data storage size in MB]** eingeben.
1. Klicken Sie auf **[!UICONTROL Save]**.

### Bearbeiten des Inhalts eines Datenspeichers

1. Klicken Sie im linken Navigationsbereich auf das **[!UICONTROL Data Store]** ![Datenspeichersymbol](assets/data-store-icon.png), um den [!UICONTROL Data Store] zu öffnen.
1. Klicken Sie **[!UICONTROL Browse]** neben dem Datenspeicher, den Sie bearbeiten möchten.
1. (Optional) Sortieren Sie die Spalten neu, indem Sie sie an die gewünschte Position ziehen.
1. (Optional) [!UICONTROL Edit] Sie eine einzelne Zelle, indem Sie auf das **[!UICONTROL Edit]** in dieser Zelle klicken und dann den gewünschten Wert eingeben.
1. (Optional) Fügen Sie dem Datenspeicher ein neues Element hinzu, indem Sie auf **[!UICONTROL Add]** klicken und dann die Informationen für das neue Element eingeben.
1. Klicken Sie auf **[!UICONTROL Save]**.

## Fehlerbehebung

* [Wiederherstellen verlorener Daten aus einem Datenspeicher](#restoring-lost-data-from-a-data-store)
* [Fehler wegen zu wenig Speicherplatz](#out-of-space-error)
* [Fehler bei maximal erreichtem Speicher](#maximum-stores-reached-error)

### Wiederherstellen verlorener Daten aus einem Datenspeicher

Es gibt derzeit kein Tool, das die Wiederherstellung verlorener Daten automatisieren kann.

#### Abhilfe

1. Untersuchen Sie alle Ausführungsprotokolle von Szenarien, in denen Elemente in den Datenspeicher eingefügt wurden.

   Weitere Informationen zum Überprüfen von Ausführungsprotokollen finden Sie [Anzeigen des Ausführungsverlaufs eines Szenarios](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md).

1. Kopieren Sie die Daten.
1. Fügen Sie die Daten erneut in Ihren Datenspeicher ein.

   Informationen zum Einfügen von Daten in einen Datenspeicher finden Sie unter [Bearbeiten des Inhalts eines Datenspeichers](#edit-the-contents-of-a-data-store) in diesem Artikel.

### [!UICONTROL Out of space]

Ein [!UICONTROL Out of Space] tritt auf, da die zuvor erstellten Datenspeicher bereits dem zugewiesenen Datenspeicher zugewiesen wurden.

#### Abhilfe

1. Bearbeiten Sie einen Ihrer vorhandenen Datenspeicher, um weniger Speicherplatz zu verbrauchen. Dadurch wird Speicherplatz für Ihren neuen Datenspeicher freigegeben.

   Weitere Informationen finden Sie unter [Bearbeiten der Eigenschaften eines Datenspeichers](#edit-the-properties-of-a-data-store) in diesem Artikel.

>[!NOTE]
>
>Es wird empfohlen, nicht den gesamten Speicherplatz einem einzigen Datenspeicher zuzuweisen, es sei denn, Sie sind sicher, dass Sie keine weiteren Datenspeicher benötigen.

### [!UICONTROL Maximum stores reached]

Ein [!UICONTROL Maximum stores reached] tritt auf, weil Ihre Organisation alle verfügbaren Datenspeicher verwendet hat.

#### Abhilfe

Um die Anzahl der vorhandenen Datenspeicher zu reduzieren, sollten Sie einen der folgenden Schritte ausführen:

* Kombinieren vorhandener Datenspeicher
* Löschen nicht verwendeter Datenspeicher
