---
title: MariaDB-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die verwenden [!DNL MariaDB] und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 41179cfe-c0f9-4d18-ab7e-374670ac688b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 1%

---

# [!DNL MariaDB]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL MariaDB] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Oder</p>
   <p>Legacy: Workfront Fusion für Arbeitsautomatisierung und -integration </p>
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

Um [!DNL MariaDB]-Module verwenden zu können, müssen Sie über ein [!DNL MariaDB]-Konto verfügen.

## Verbinden von [!DNL MariaDB] mit Workfront Fusion

Sie können direkt aus einem [!DNL MariaDB]-Modul heraus eine Verbindung zu Ihrem [!DNL MariaDB]-Konto herstellen.

1. Klicken Sie in einem [!DNL MariaDB] Modul **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Konfigurieren Sie die folgenden Felder:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Verbindungsname]</p> </td> 
      <td> <p>Geben Sie einen Namen für die neue Verbindung ein.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>Wählen Sie aus, ob diese Verbindung für eine Produktions- oder Nicht-Produktionsumgebung vorgesehen ist.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Host]</td> 
      <td> <p>Geben Sie die IP-Adresse oder den Hostnamen Ihrer Datenbankinstanz ein. Dieser Host muss von außerhalb Ihres Netzwerks zugänglich sein.</p> <p>Beispiel: <code>[!DNL mariadb.hwoh2j5h.us-east-1.rds.amazon.com]</code></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Port]</td> 
      <td>Der Standard-Port ist 3306. Wenn Sie einen nicht standardmäßigen Port verwenden, setzen Sie diese Nummer auf Ihren Port. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL -Datenbank &#x200B;]</td> 
      <td>Geben Sie den Namen der Datenbank ein, mit der Sie interagieren möchten.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL -Benutzer]</td> 
      <td>Geben Sie Ihren Benutzernamen ein.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Kennwort]</td> 
      <td>Geben Sie Ihr Kennwort ein.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL MariaDB] Module und ihre Felder

Beim Konfigurieren von [!DNL MariaDB] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL MariaDB] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Ausführen einer Abfrage (erweitert)

Dieses Aktionsmodul ruft basierend auf einer von Ihnen angegebenen Abfrage Informationen aus Ihrer Datenbank ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL MariaDB]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL MariaDB] mit Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Abfrage]</td> 
   <td> <p>Geben Sie die SQL-Abfrage ein, mit der das Modul Daten abrufen soll.</p> <p>Wichtig: In der Abfrage verwendete Variablen werden nicht bereinigt. Stellen Sie sicher, dass Sie Variablen ordnungsgemäß bereinigen, um SQL-Injections zu verhindern.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Zeilen aus einer Tabelle auswählen (erweitert)]

Dieses Modul liest Einträge aus Ihrer Datenbank.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres [!DNL MariaDB]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL MariaDB] mit Workfront Fusion</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Tabelle]</td> 
   <td> <p>Wählen Sie die Tabelle aus, die die Datensätze enthält, die Sie lesen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL filter]</td> 
   <td> <p>Richten Sie den Filter ein, nach dem Sie Zeilen auswählen möchten</p> 
    <ul> 
     <li> <p>Wählen Sie das Feld aus, nach dem Sie suchen möchten</p> </li> 
     <li> <p>Wählen Sie den Operator aus, den Sie für Ihre Suche verwenden möchten</p> </li> 
     <li> <p>Geben Sie den Wert ein, nach dem Sie suchen möchten, oder ordnen Sie ihn zu.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL sort] </td> 
   <td> <p>Klicken Sie für jede Ebene, nach der Ihre Ergebnisse sortiert werden sollen, auf <strong>[!UICONTROL Element hinzufügen]</strong> und wählen Sie dann das Feld aus, nach dem Sie die Ergebnisse sortieren möchten, und ob Sie auf- oder absteigend sortieren möchten</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>
