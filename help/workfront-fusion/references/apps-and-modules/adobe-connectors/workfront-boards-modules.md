---
title: Adobe Workfront Boards-Module
description: Sie können den Adobe Workfront Boards-Connector verwenden, um Ihre Prozesse in Workfront Boards zu automatisieren und ihn mit Apps und Services von Drittanbietern zu verbinden.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: dcc5044d-8fdf-4a74-b664-e965e714ce92
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2929'
ht-degree: 1%

---

# Adobe Workfront Boards-Module

>[!NOTE]
>
>Der Boards Fusion-Connector befindet sich im Beta-Status. Daher ist die Unterstützung für diesen Connector begrenzt und kann sich aufgrund der zukünftigen Entwicklung von Boards ändern. Darüber hinaus kann es ohne Vorankündigung Änderungen an der GraphQL-API geben, die sich auf Ihren Fusion-Connector-Prozess auswirken könnten.

Adobe Workfront-Pinnwände sind flexible Tools für die Zusammenarbeit von Teams, indem sie Zugriff auf eine freigegebene Pinnwand mit Spalten und Karten bieten.

Sie können die Adobe Workfront-Pinnwand-Module verwenden, um Datensätze zu lesen oder zu aktualisieren, einen API-Aufruf an die Workfront-Pinnwand-API durchzuführen oder ein Szenario Trigger auszulösen, wenn eine Aktion auf einer Pinnwand stattfindet.

<!--For general information on Workfront Boards, see [Boards overview](/help/quicksilver/agile/boards-overview.md).-->

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

Sie müssen eine Pinnwand in Adobe Workfront konfiguriert haben, bevor Sie eine Verbindung damit herstellen können.

## Informationen zur Adobe Workfront Boards-API

Der Adobe Workfront Boards-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.23.6</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung zu Workfront Boards

>[!NOTE]
>
>Sie können eine Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine separate Workfront Boards-Verbindung erstellen.

So erstellen Sie eine Workfront Boards-Verbindung:

1. Klicken Sie in einem beliebigen [!DNL Adobe Workfront Boards] auf **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Verbindungsname]</td>
          <td>
            <p>Geben Sie einen Namen für diese Verbindung ein.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Umgebung]</td>
          <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Typ]</td>
          <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-ID]<p>(Optional)</p></td>
          <td>Geben Sie Ihre [!DNL Adobe] [!UICONTROL Client ID] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-Geheimnis]<p>(Optional)</p></td>
          <td>Geben Sie Ihren [!DNL Adobe] [!UICONTROL Client Secret] ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL -Authentifizierungs-URL]<p>(Optional)</p></td>
          <td>Geben Sie die URL ein, die Ihre Workfront-Instanz zur Authentifizierung dieser Verbindung verwenden soll. <p>Der Standardwert lautet <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host-Präfix]</td>
          <td>Geben Sie Ihr Host-Präfix ein.<p>Der Standardwert lautet <code>origin-</code>.</p>
        </tr>
      </tbody>
    </table>
1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## Adobe Workfront-Pinnwand-Module und ihre Felder

Beim Konfigurieren von Workfront-Motherboard-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus werden möglicherweise zusätzliche Felder für Workfront-Boards angezeigt, je nach Faktoren wie Ihrer Zugriffsebene in der App oder im Service. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Karten](#cards)
* [Pinnwände](#boards)
* [Spalten](#columns)
* [Tags](#tags)
* [Kommentare](#comments)
* [Sonstiges](#other)

### Karten

* [Checklisten-Objekt hinzufügen](#add-checklist-item)
* [Teilaufgabe hinzufügen](#add-subtask)
* [Erstellen einer Karte](#create-a-card)
* [Karte verschieben](#move-a-card)
* [Karte lesen](#read-a-card)
* [Aktualisieren einer Karte](#update-a-card)

#### Checklisten-Objekt hinzufügen

Dieses Aktionsmodul fügt der angegebenen Karte ein Checklisten-Element hinzu.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Kartenkennung]</td> 
   <td>Geben Sie die ID der Karte ein, der Sie ein Checklisten-Element hinzufügen möchten, oder ordnen Sie sie zu.<p>Die Karten-ID finden Sie in der URL, wenn Sie die Karte in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Checklisten-Elemente]</td> 
   <td>Klicken Sie für jedes Checklisten-Element, das Sie hinzufügen möchten, auf Element hinzufügen, geben Sie den Namen des Checklisten-Elements ein und wählen Sie aus, ob das Element abgeschlossen wurde.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Teilaufgabe hinzufügen

Dieses Aktionsmodul fügt einer Karte in Pinnwänden eine Unteraufgabe hinzu. Die Karte muss eine verbundene Karte sein. Die Unteraufgabe wird auch der Workfront-Aufgabe hinzugefügt, die die Karte darstellt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID der übergeordneten Karte]</td> 
   <td>Geben Sie die ID der Karte ein, der Sie eine Unteraufgabe hinzufügen möchten, oder ordnen Sie sie zu.<p>Die Karten-ID finden Sie in der URL, wenn Sie die Karte in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Geben Sie die ID der Pinnwand ein, die die Karte enthält, der Sie eine Unteraufgabe hinzufügen möchten, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Einen Namen für die neue Teilaufgabe eingeben oder zuordnen.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen einer Karte

Dieses Aktionsmodul erstellt eine neue Karte auf einer Workfront-Pinnwand.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Geben Sie die ID der Pinnwand ein, der Sie eine Karte hinzufügen möchten, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spalten-ID]</td> 
   <td>Geben Sie die ID der Spalte ein, der Sie eine Unteraufgabe hinzufügen möchten, oder ordnen Sie sie zu.<p>Die Spalten-ID finden Sie in den Informationen, die vom Modul Eine Pinnwand lesen zurückgegeben werden.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Geben Sie einen Namen für die neue Karte ein oder mappen Sie ihn.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Karte verschieben

Dieses Aktionsmodul verschiebt eine Karte in eine andere Spalte auf derselben Pinnwand.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Kartenkennung]</td> 
   <td>Geben Sie die ID der Karte ein, die Sie verschieben möchten, oder mappen Sie sie.<p>Die Karten-ID finden Sie in der URL, wenn Sie die Karte in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Geben Sie die ID der Pinnwand ein, die die Karte enthält, die Sie verschieben möchten, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Zielspalten-ID]</td> 
   <td>Geben Sie die ID der Spalte ein, in die Sie die Karte verschieben möchten, oder ordnen Sie sie zu.<p>Die Spalten-ID finden Sie in den Informationen, die vom Modul Eine Pinnwand lesen zurückgegeben werden.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL zu Index]</td> 
   <td>Geben Sie die Position, die die Karte in der neuen Spalte haben soll, ein oder ordnen Sie sie zu.<p>Die oberste Position in der Spalte in Index 0.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Karte lesen

Dieses Aktionsmodul ruft Informationen zu einer bestimmten Karte ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Kartenkennung]</td> 
   <td>Geben Sie die ID der Karte ein, die Sie lesen möchten, oder mappen Sie sie.<p>Die Karten-ID finden Sie in der URL, wenn Sie die Karte in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Kartenkennung]</td> 
   <td>Geben Sie die ID der Pinnwand ein, die die Karte enthält, die Sie lesen möchten, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren einer Karte

Dieses Aktionsmodul aktualisiert die Informationen für eine von Ihnen angegebene Karte.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Kartenkennung]</td> 
   <td>Geben Sie die ID der Karte ein, die Sie aktualisieren möchten, oder mappen Sie sie.<p>Die Karten-ID finden Sie in der URL, wenn Sie die Karte in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Geben Sie die ID der Pinnwand ein, die die Karte enthält, die Sie aktualisieren möchten, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Geben Sie einen neuen Namen für die Karte ein oder mappen Sie ihn.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Beschreibung]</td> 
   <td>Geben Sie eine neue Beschreibung für die Karte ein oder mappen Sie sie.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Schätzung]</td> 
   <td>Geben Sie eine Schätzung der Zeit ein, die zum Ausfüllen dieser Karte benötigt wird, oder mappen Sie sie.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Fälligkeitsdatum]</td> 
   <td>Geben Sie das Fälligkeitsdatum für diese Karte ein oder mappen Sie es.</p>
   <p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</p>
   </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Status]</td> 
   <td>Wählen Sie einen neuen Status für die Karte aus.</p></td> 
  </tr> 
 </tbody> 
</table>

### Pinnwände

* [Pinnwand erstellen](#create-a-board)
* [Pinnwand lesen](#read-a-board)

#### Pinnwand erstellen

Dieses Aktionsmodul erstellt eine Pinnwand in Workfront. Sie können den Typ der Pinnwand angeben, die Sie erstellen möchten.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board name]</td> 
   <td>Geben Sie einen Namen für die neue Pinnwand ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Vorlage]</td> 
   <td>Wählen Sie die Vorlage für den Pinnwand-Typ aus, den Sie erstellen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### Pinnwand lesen

Dieses Aktionsmodul gibt Informationen über eine einzelne Pinnwand zurück, z. B. die Karten, Spalten, Tags und Mitglieder der Pinnwand.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Geben Sie die ID der Pinnwand ein, für die Sie Informationen abrufen möchten, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
 </tbody> 
</table>

### Spalten

* [Spalte erstellen](#create-a-column)
* [Nach einer Spalte suchen](#search-for-a-column)
* [Aktualisieren einer Spalte](#update-a-column)

#### Spalte erstellen

Dieses Aktionsmodul erstellt eine neue Spalte auf der angegebenen Pinnwand.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Geben Sie die ID der Pinnwand ein, der Sie eine Spalte hinzufügen möchten, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spalten-ID]</td> 
   <td>Geben Sie die ID der Spalte ein, die Sie aktualisieren möchten, oder ordnen Sie sie zu.<p>Die Spalten-ID finden Sie in den Informationen, die vom Modul Eine Pinnwand lesen zurückgegeben werden.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spaltenname]</td> 
   <td>Geben Sie einen neuen Namen für die Spalte ein oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Nach einer Spalte suchen

Dieses Suchmodul gibt Informationen über die Spalte mit dem angegebenen Namen zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Geben Sie die ID der Pinnwand ein, die die abzurufende Spalte enthält, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spaltenname]</td> 
   <td>Geben Sie den Namen der abzurufenden Spalte ein oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren einer Spalte

Dieses Aktionsmodul aktualisiert den Namen oder die WIP-Beschränkung der angegebenen Spalte.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Geben Sie die ID der Pinnwand ein, die die abzurufende Spalte enthält, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spaltenname]</td> 
   <td>Geben Sie den Namen der abzurufenden Spalte ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL WIP-Limit]</td> 
   <td>Geben Sie eine neue Fertigungsgrenze für die Spalte ein oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

### Tags

* [Hinzufügen eines Tags zu einer Karte](#add-a-tag-to-a-card)
* [Erstellen von Tags](#create-a-tag)

#### Hinzufügen eines Tags zu einer Karte

Dieses Aktionsmodul fügt einer Karte ein Tag hinzu.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Kartenkennung]</td> 
   <td>Geben Sie die ID der Karte ein, der Sie einen Tag hinzufügen möchten, oder mappen Sie sie.<p>Die Karten-ID finden Sie in der URL, wenn Sie die Karte in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Geben Sie die ID der Pinnwand ein, die die Karte enthält, der Sie ein Tag hinzufügen möchten, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag-ID]</td> 
   <td>Geben Sie die ID des Tags ein, das Sie hinzufügen möchten, oder mappen Sie sie.<p>Die Tag-ID finden Sie in den Informationen, die vom Modul „Pinnwand lesen“ zurückgegeben werden.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen von Tags

Dieses Aktionsmodul erstellt ein neues Tag und weist ihm eine Farbe zu.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Geben Sie die ID der Pinnwand ein, für die Sie ein Tag erstellen möchten, oder ordnen Sie sie zu.<p>Die Pinnwand-ID finden Sie in der URL, wenn Sie die Pinnwand in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag-Name]</td> 
   <td>Geben Sie einen Namen für das neue Tag ein oder ordnen Sie ihn zu.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag-Farbe]</td> 
   <td>Farbe für dieses Tag auswählen.</td> 
  </tr> 
 </tbody> 
</table>

### Kommentare

* [Kommentar erstellen](#create-a-comment)
* [Kartenkommentare lesen](#read-card-comments)

#### Kommentar erstellen

Dieses Aktionsmodul hat einen Kommentar auf der angegebenen Karte erstellt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Kartenkennung]</td> 
   <td>Geben Sie die ID der Karte ein, der Sie einen Kommentar hinzufügen möchten, oder mappen Sie sie.<p>Die Karten-ID finden Sie in der URL, wenn Sie die Karte in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Kommentar]</td> 
   <td>Geben Sie den Text des Kommentars ein, den Sie hinzufügen möchten, oder mappen Sie ihn.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Kartenkommentare lesen

Dieses Aktionsmodul ruft die Kommentare von der angegebenen Karte ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Kartenkennung]</td> 
   <td>Geben Sie die ID der Karte ein, für die Sie die Kommentare abrufen möchten, oder ordnen Sie sie zu.<p>Die Karten-ID finden Sie in der URL, wenn Sie die Karte in Workfront anzeigen.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl an Kommentaren ein, die das Modul in einem Ausführungszyklus zurückgeben soll.</p></td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

#### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt einen benutzerdefinierten Aufruf an die Workfront Boards-API durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Geben Sie einen Pfad relativ zu ein<code> https://&lt;WORKFRONT_DOMAIN&gt;/boards-service/graphql?</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p><p>Bei den meisten Boards ist die Methode POST. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Dadurch wird der Inhaltstyp der Anfrage bestimmt.</p> <p>Beispiel:<code> { "Content-type":"application/json-stringify()"}</code></p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Bei Workfront-Boards bleibt dieser Abschnitt normalerweise leer.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteilinhalt für den API-Aufruf in Form einer in JSON eingebetteten GraphQL hinzu. </p> <p>Beispiel:</p><p>In diesem Beispiel wird ein Spaltenname aktualisiert. Sie können die <code>boardId</code> und <code>columnId</code> als GUIDs entweder hartcodiert oder von einem vorherigen Modul zugeordnet einbeziehen.<p><pre>{<br> „query“: „mutation { updateColumn(boardId: \"\", columnId: \"\", updateColumnInput: { name: \"\" }) { id name }}"<br>}</pre><p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


#### Erstellen eines benutzerdefinierten GraphQL-API-Aufrufs

Dieses Aktionsmodul führt eine benutzerdefinierte GraphQL-Anfrage an die Workfront Boards-API durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
      <td> <p>Sie können eine bestehende Workfront-Verbindung verwenden, um eine Verbindung zu Workfront Boards herzustellen, oder Sie können eine bestimmte Workfront Boards-Verbindung verwenden. </p><p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Erstellen einer Verbindung zu Workfront</a> in diesem Artikel.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL -Methode]</td> 
   <td> <p>Wählen Sie die Methode für diesen Aufruf. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Abfrage]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorgangsname]</td> 
   <td> <p>Geben Sie einen Namen für diesen Vorgang ein. Dies kann das Tracking und Debugging des Aufrufs vereinfachen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Variablen, Datenquelle]</td> 
   <td> <p>Auswählen, ob die Variablen aus einem Formular oder aus einer Sammlung stammen sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Variablen]</td> 
   <td> <p>Klicken Sie für jede Variable, die Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Schlüssel und den Wert der Variablen ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
   </tr> 
 </tbody> 
</table>
