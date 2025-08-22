---
title: Datenspeichermodule
description: Ein Adobe Workfront Fusion-Datenspeicher kann ähnlich wie eine Datenbank oder eine einfache Tabelle Daten aus Szenarien speichern und ermöglicht so die Übertragung von Daten zwischen einzelnen Szenarien oder Szenarioausführungen. Sie können einen Datenspeicher verwenden, um während der Synchronisierung neue Daten aus verschiedenen Systemen zu speichern.
author: Becky
feature: Workfront Fusion
exl-id: 0338b822-b345-429e-850d-3978b692231d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1154'
ht-degree: 0%

---

# [!UICONTROL Datenspeicher] Module

Ein Adobe Workfront Fusion-Datenspeicher kann ähnlich wie eine Datenbank oder eine einfache Tabelle Daten aus Szenarien speichern und ermöglicht so die Übertragung von Daten zwischen einzelnen Szenarien oder Szenarioausführungen. Sie können einen Datenspeicher verwenden, um während der Synchronisierung neue Daten aus verschiedenen Systemen zu speichern.

Mit den Datenspeichermodulen können Sie Datensätze in Ihrem Adobe Workfront Fusion-Datenspeicher hinzufügen, ersetzen, aktualisieren, abrufen, löschen, suchen oder zählen.

<!--For information on creating, editing, and troubleshooting data stores, see [Data Stores in Adobe Workfront Fusion](/help/workfront-fusion/references/mapping-panel/data-types/)-->

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
   <p>Keine Workfront Fusion-Lizenzanforderung</p>
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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um [!UICONTROL Datenspeicher]-Module verwenden zu können, müssen Sie zunächst einen Datenspeicher erstellen.

Informationen zum Erstellen von Datenspeichern finden Sie unter [Erstellen und Verwalten von Datenspeichern](/help/workfront-fusion/create-scenarios/map-data/data-stores.md).

## [!UICONTROL Datenspeicher]-Module und ihre Felder

Beim Konfigurieren von Datenspeichermodulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere Datenspeicherfelder angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Sie müssen keine Verbindung erstellen, um Datenspeicher zu verwenden.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Datensatz hinzufügen/ersetzen](#addreplace-a-record)
* [Überprüfen, ob ein Datensatz vorhanden ist](#check-the-existence-of-a-record)
* [Datensätze zählen](#count-records)
* [Löschen eines Datensatzes](#delete-a-record)
* [Alle Datensätze löschen](#delete-all-records)
* [Datensatz abrufen](#get-a-record)
* [Datensätze suchen](#search-records)
* [Aktualisieren eines Datensatzes](#update-a-record)

### [!UICONTROL Datensatz hinzufügen/ersetzen]

Dieses Aktionsmodul fügt einen Datensatz hinzu oder ersetzt ihn.

Sie geben den Datenspeicher und den Schlüssel des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

>[!NOTE]
>
>Das Modul gibt einen Fehler aus, wenn Sie versuchen, einen Datensatz hinzuzufügen, der sich bereits unter demselben Namen im Datenspeicher befindet, und die Option [!UICONTROL Vorhandenen Datensatz überschreiben] ist deaktiviert.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Datenspeicher]</td> 
   <td> <p> Wählen Sie den Datenspeicher aus, in dem Sie einen Datensatz erstellen möchten, oder fügen Sie ihn hinzu. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Schlüssel] </td> 
   <td> <p>Geben Sie den eindeutigen Schlüssel des Datensatzes ein, den das Modul hinzufügen oder ersetzen soll. Der Schlüssel kann später zum Abrufen des Datensatzes verwendet werden. Wenn Sie dieses Feld leer lassen, wird automatisch ein Schlüssel generiert.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Vorhandenen Datensatz überschreiben] </td> 
   <td> <p>Aktivieren Sie diese Option, um den Datensatz zu überschreiben. Der Datensatz, den Sie überschreiben möchten, muss im obigen Feld Schlüssel angegeben werden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Eintrag] </td> 
   <td> <p>Geben Sie die gewünschten Werte in die Felder des Datensatzes ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Überprüfen Sie, ob ein Datensatz vorhanden ist]

Dieses Aktionsmodul gibt an, ob ein bestimmter Datensatz vorhanden ist.

Sie geben den Datenspeicher und den Schlüssel des Datensatzes an.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Datenspeicher] </td> 
   <td> <p>Wählen Sie den Datenspeicher aus, den Sie auf das Vorhandensein des Datensatzes überprüfen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Schlüssel] </td> 
   <td> <p>Geben Sie den eindeutigen Schlüssel des Datensatzes ein, auf dessen Existenz das Modul prüfen soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Datensätze zählen]

Dieses Aktionsmodul nummeriert die Datensätze in einem Datenspeicher.

Sie geben den Datenspeicher an.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Datenspeicher] </td> 
   <td> <p>Wählen Sie den Datenspeicher aus, der die Datensätze enthält, die gezählt werden sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Löschen eines Datensatzes]

Dieses Aktionsmodul löscht einen Datensatz.

Sie geben den Datenspeicher und den Schlüssel des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Datenspeicher] </td> 
   <td> <p>Wählen Sie den Datenspeicher aus, den Sie auf das Vorhandensein des Datensatzes überprüfen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Schlüssel] </td> 
   <td> <p>Geben Sie den eindeutigen Schlüssel des Datensatzes ein, den das Modul löschen soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Alle Datensätze löschen]

Dieses Aktionsmodul löscht alle Datensätze aus einem bestimmten Datenspeicher.

Sie geben den Datenspeicher an.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Datenspeicher] </td> 
   <td> <p>Wählen Sie den Datenspeicher aus, aus dem Sie alle Datensätze löschen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Datensatz abrufen]

Dieses Aktionsmodul ruft einen Datensatz ab.

Sie geben den Datenspeicher und den Schlüssel des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Datenspeicher]</td> 
   <td> <p> Wählen Sie den Datenspeicher aus, aus dem Sie einen Datensatz abrufen möchten</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Schlüssel] </td> 
   <td> <p>Geben Sie den eindeutigen Schlüssel des Datensatzes ein, den das Modul abrufen soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Datensätze suchen]

Dieses Suchmodul sucht in einem -Objekt im Datenspeicher nach Datensätzen, die mit der von Ihnen angegebenen Suchabfrage übereinstimmen.

Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Datenspeicher]</td> 
   <td> <p> Wählen Sie den zu durchsuchenden Datenspeicher aus.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL filter]</p> </td> 
   <td> <p>Filter für die Suche festlegen.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL sort]</p> </td> 
   <td> <p style="font-weight: normal;">Füllen Sie für jedes Feld, nach dem Sie sortieren möchten, die folgenden Felder aus:</p> <p style="font-weight: bold;">[!UICONTROL-Schlüssel]</p> <p>Wählen Sie den Spaltennamen aus, nach dem die Ergebnisse sortiert werden sollen.</p> <p style="font-weight: bold;">[!UICONTROL-Reihenfolge]</p> <p>Wählen Sie aus, ob die Ergebnisse in auf- oder absteigender Reihenfolge sortiert werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p> Legen Sie die maximale Anzahl von Suchergebnissen fest, die Workfront Fusion während eines Ausführungszyklus zurückgibt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Die Routenausführung auch dann fortsetzen, wenn das Modul keine Ergebnisse zurückgibt]</td> 
   <td> <p> Wenn diese Option aktiviert ist, wird die Route, zu der dieses Modul gehört, auch dann weiter verarbeitet, wenn dieses Modul keine Ergebnisse zurückgibt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Aktualisieren eines Datensatzes]

Dieses Aktionsmodul aktualisiert einen Datensatz.

Sie geben den Datenspeicher und den Schlüssel des Datensatzes an.

Das Modul gibt die ID des Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Datenspeicher]</td> 
   <td> <p> Wählen Sie den Datenspeicher aus, in dem Sie einen Datensatz erstellen möchten, oder fügen Sie ihn hinzu. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Schlüssel] </td> 
   <td> <p>Geben Sie den eindeutigen Schlüssel des Datensatzes ein, den das Modul aktualisieren soll.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Fehlenden Eintrag einfügen] </td> 
   <td> <p>Aktivieren Sie diese Option, um einen neuen Datensatz zu erstellen, wenn der Datensatz mit dem angegebenen Schlüssel noch nicht vorhanden ist.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Eintrag]</td> 
   <td> <p> Geben Sie die gewünschten Werte in die Felder des Datensatzes ein, die Sie aktualisieren möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>
