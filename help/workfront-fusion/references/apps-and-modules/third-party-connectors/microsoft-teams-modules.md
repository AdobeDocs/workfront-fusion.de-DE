---
title: Microsoft Teams-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Teams verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
source-git-commit: f5b49cca308fad01167aed27e4716a3d630cb026
workflow-type: tm+mt
source-wordcount: '3642'
ht-degree: 2%

---

# Microsoft Teams-Module

<!-- ADD REDIRECTS -->

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Microsoft Teams verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um Microsoft Teams-Module verwenden zu können, müssen Sie über ein Microsoft Teams-Konto verfügen, das die Aktion im Modul ausführen kann.

## Verbinden des Microsoft Teams-Service mit Workfront Fusion

Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter [Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
>
>Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.

## Microsoft Teams-Module und ihre Felder

Beim Konfigurieren von Microsoft Teams-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service können zusätzlich dazu weitere Microsoft Teams-Felder angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Team](#team)
* [Kanal](#channel)
* [Nachricht](#message)
* [Mitglied](#member)
* [Online-Besprechung](#online-meeting)
* [Sonstige](#other)

### Team

* [Erstellen eines Teams aus einer Gruppe](#create-a-team-from-a-group)
* [Erstellen einer Office 365-Gruppe](#create-an-office-365-group)
* [Löschen eines Teams oder einer Gruppe](#delete-a-team-or-group)
* [Team abrufen](#get-a-team)
* [Auflisten aller Teams und Gruppen](#list-all-teams-and-groups)
* [Auflisten der hinzugekommenen Teams](#list-joined-teams)
* [Aktualisieren eines Teams](#update-a-team)
* [Teams beobachten](#watch-teams)

#### Erstellen eines Teams aus einer Gruppe

Dieses Aktionsmodul erstellt ein Team aus einer bestehenden Microsoft Office 365-Gruppe und konfiguriert Einstellungen für das neue Team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppen-ID</td> 
   <td> <p>Wählen Sie die Gruppe aus, aus der Sie ein Team erstellen möchten.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Mitgliedern erlauben, Kanäle zu erstellen und zu aktualisieren</td> 
   <td>Wählen Sie aus, ob Mitglieder Kanäle erstellen und aktualisieren dürfen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Löschen von Kanälen durch Mitglieder zulassen</td> 
   <td>Wählen Sie aus, ob Mitglieder Kanäle löschen dürfen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zulassen, dass Mitglieder Apps hinzufügen und entfernen</td> 
   <td>Wählen Sie aus, ob Mitgliedern das Hinzufügen und Entfernen von Apps erlaubt werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zulassen, dass Mitglieder Registerkarten erstellen, aktualisieren und entfernen</td> 
   <td>Wählen Sie aus, ob Mitglieder Registerkarten erstellen, aktualisieren und entfernen dürfen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zulassen, dass Mitglieder Connectoren erstellen und entfernen</td> 
   <td>Wählen Sie aus, ob Mitglieder Connectoren erstellen und entfernen dürfen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benutzern erlauben, ihre Nachrichten zu bearbeiten</td> 
   <td>Wählen Sie aus, ob Benutzerinnen und Benutzern erlaubt werden soll, ihre Nachrichten zu bearbeiten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benutzern erlauben, ihre Nachrichten zu löschen</td> 
   <td>Wählen Sie aus, ob Benutzerinnen und Benutzern das Löschen ihrer Nachrichten erlaubt werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zulassen, dass Besitzer Nachrichten löschen</td> 
   <td>Wählen Sie aus, ob Besitzer eine Nachricht löschen dürfen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Erwähnungen @team</td> 
   <td>Wählen Sie aus, ob @team Erwähnungen zulässig sein sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Erwähnungen @channel</td> 
   <td>Wählen Sie aus, ob @channel Erwähnungen zulässig sein sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Graphi zulassen</td> 
   <td>Wählen Sie aus, ob Sie die Verwendung von Giphy für dieses Team zulassen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aufkleber und Meme zulassen</td> 
   <td>Wählen Sie aus, ob Benutzerinnen und Benutzern erlaubt werden soll, Aufkleber und Meme einzuschließen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benutzerdefinierte Meme zulassen</td> 
   <td>Wählen Sie aus, ob Benutzerinnen und Benutzern das Einschließen benutzerdefinierter Meme erlaubt werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zulassen, dass Gäste Kanäle erstellen und aktualisieren</td> 
   <td>Wählen Sie aus, ob Sie Gästen das Erstellen und Aktualisieren von Kanälen erlauben möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Löschen von Kanälen durch Gäste zulassen</td> 
   <td>Wählen Sie aus, ob Sie den Gästen das Löschen von Kanälen erlauben möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen einer Office 365-Gruppe

Dieses Aktionsmodul erstellt eine Gruppe in Microsoft Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Anzeigename</td> 
   <td> <p>Geben Sie den Namen ein, den diese Gruppe in ihrem Adressbuch anzeigt, oder ordnen Sie ihn zu.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias für Gruppe</td> 
   <td>Geben Sie den E-Mail-Alias für diese Gruppe ein oder ordnen Sie ihn zu. Sie können Kleinbuchstaben, Zahlen und Unterstriche verwenden. Für den Office 365-Gruppentyp ist dies der E-Mail-Alias der Gruppe ([Alias]@[Ihre Domain].onmicrosoft.com). Für den Typ Sicherheitsgruppe fungiert der Alias als Spitzname.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppentyp</td> 
   <td>Wählen Sie aus, ob Sie eine Office 365-Gruppe oder eine Sicherheitsgruppe erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beschreibung</td> 
   <td>Beschreibung für diese Gruppe eingeben oder zuordnen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sicherheit aktiviert</td> 
   <td>Aktivieren Sie diese Option, wenn die Gruppe für Sicherheit aktiviert sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Inhaber</td> 
   <td>Wählen Sie die Besitzer für diese Gruppe aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Abonnenten</td> 
   <td>Die Mitglieder für diese Gruppe auswählen.</td> 
  </tr> 
 </tbody> 
</table>

#### Löschen eines Teams oder einer Gruppe

Dieses Aktionsmodul löscht die angegebene Gruppe oder Gruppe.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppen-ID</td> 
   <td> <p>Geben Sie die ID der Gruppe ein, die Sie löschen möchten, oder ordnen Sie sie zu.</p> 
   </tr> 
 </tbody> 
</table>

#### Team abrufen

Dieses Modul ruft Eigenschaften und Beziehungen für das angegebene Microsoft-Team oder die angegebene Office 365-Gruppe ab.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppen-ID</td> 
   <td> <p>Geben Sie die ID der Gruppe ein, für die Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> 
   </tr> 
 </tbody> 
</table>

#### Auflisten aller Teams und Gruppen

In diesem Modul werden alle Teams in Microsoft Teams- und Office 365-Gruppen aufgelistet, die mit der Organisation verknüpft sind. Sie können filtern, um nur Ergebnisse zurückzugeben, die den von Ihnen angegebenen Kriterien entsprechen.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>Sie können einen Filter festlegen, der nur Teams und Gruppen zurückgibt, die die von Ihnen ausgewählten Kriterien erfüllen.</p> <p>Geben Sie für jeden Filter das Feld ein, das vom Filter ausgewertet werden soll, den Operator und den Wert, den der Filter zulassen soll. Sie können mehr als einen Filter verwenden, indem Sie AND- oder OR-Regeln hinzufügen.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Legen Sie die maximale Anzahl von Teams oder Gruppen fest, die Workfront Fusion während eines Ausführungszyklus zurückgeben soll.</td> 
  </tr> 
 </tbody> 
</table>


#### Teammitglieder auflisten

Dieses Aktionsmodul listet die Teams auf, denen sich der Benutzer angeschlossen hat, der mit der in diesem Modul verwendeten Verbindung verknüpft ist.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Legen Sie die maximale Anzahl von Teams oder Gruppen fest, die Workfront Fusion während eines Ausführungszyklus zurückgeben soll.</td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren eines Teams

Dieses Aktionsmodul aktualisiert die Eigenschaften der angegebenen Teams in Microsoft Teams oder der Office 365-Gruppe.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Anzeigename</td> 
   <td> <p>Geben Sie den Namen ein, den diese Gruppe in ihrem Adressbuch anzeigt, oder ordnen Sie ihn zu.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias für Gruppe</td> 
   <td>Geben Sie den E-Mail-Alias für diese Gruppe ein oder ordnen Sie ihn zu. Sie können Kleinbuchstaben, Zahlen und Unterstriche verwenden. Für den Office 365-Gruppentyp ist dies der E-Mail-Alias der Gruppe ([Alias]@[Ihre Domain].onmicrosoft.com). Für den Sicherheitsgruppentyp fungiert der Alias als Spitzname.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beschreibung</td> 
   <td>Beschreibung für diese Gruppe eingeben oder zuordnen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sicherheit aktiviert</td> 
   <td>Aktivieren Sie diese Option, wenn die Gruppe für Sicherheit aktiviert sein soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sichtbarkeit</td> 
   <td>Geben Sie die Sichtbarkeit der Office 365-Gruppe an.</td> 
  </tr> 
 </tbody> 
</table>

#### Teams beobachten

Dieses Teammodul startet ein Trigger, wenn ein Team erstellt wird.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>Sie können einen Filter einrichten, um nur nach Teams und Gruppen zu suchen, die die von Ihnen ausgewählten Kriterien erfüllen.</p> <p>Geben Sie für jeden Filter das Feld ein, das vom Filter ausgewertet werden soll, den Operator und den Wert, den der Filter zulassen soll. Sie können mehr als einen Filter verwenden, indem Sie AND- oder OR-Regeln hinzufügen.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Legen Sie die maximale Anzahl von Teams oder Gruppen fest, die Workfront Fusion während eines Ausführungszyklus zurückgeben soll.</td> 
  </tr> 
 </tbody> 
</table>

### Kanal

* [Erstellen eines Kanals](#create-a-channel)
* [Löschen eines Kanals](#delete-a-channel)
* [Kanal abrufen](#get-a-channel)
* [Kanäle auflisten](#list-channels)
* [Aktualisieren eines Kanals](#update-a-channel)

#### Erstellen eines Kanals

Dieses Aktionsmodul erstellt einen neuen Kanal für das angegebene Team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-Kennung</td> 
   <td> <p>Wählen Sie das Team in Microsoft Teams aus, für das Sie einen Kanal erstellen möchten.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanalname</td> 
   <td>Geben Sie einen Namen für den neuen Kanal ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td>Beschreibungen</td> 
   <td>Geben Sie eine Beschreibung für den neuen Kanal ein oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### Löschen eines Kanals

Dieses Aktionsmodul löscht den angegebenen Kanal aus einem Microsoft-Team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-Kennung</td> 
   <td> <p>Geben Sie die ID des Teams in Microsoft Teams ein, aus dem Sie einen Kanal löschen möchten, oder ordnen Sie sie zu.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanal-ID</td> 
   <td>Geben Sie die ID des Kanals ein, den Sie löschen möchten, oder mappen Sie sie.</td> 
  </tr> 
  </tbody> 
</table>

#### Kanal abrufen

Dieses Modul ruft die Eigenschaften und Beziehungen eines Kanals ab.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-Kennung</td> 
   <td> <p>Geben Sie die ID des Teams in Microsoft Teams ein, das Eigentümer des Kanals ist, für den Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanal-ID</td> 
   <td>Geben Sie die ID des Kanals ein, für den Sie Details abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  </tbody> 
</table>

#### Kanäle auflisten

Dieses Modul listet die Kanäle auf, die dem angegebenen Team in Microsoft Teams gehören.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-Kennung</td> 
   <td> <p>Wählen Sie das Team in Microsoft Teams aus, für das Sie die Kanäle auflisten möchten.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Legen Sie die maximale Anzahl an Kanälen fest, die Workfront Fusion während eines Ausführungszyklus zurückgeben soll.</td> 
  </tr> 
  </tbody> 
</table>

#### Aktualisieren eines Kanals

Dieses Aktionsmodul aktualisiert die Beschreibung des angegebenen Kanals.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-Kennung</td> 
   <td> <p>Wählen Sie das Team in Microsoft Teams aus, dem der Kanal gehört, den Sie aktualisieren möchten.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanalname</td> 
   <td>Geben Sie den Namen des Kanals ein, den Sie aktualisieren möchten, oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td>Beschreibung</td> 
   <td>Geben Sie die neue Beschreibung für den Kanal ein oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

### Nachricht

* [Auf eine Kanalnachricht antworten](#reply-to-a-channel-message)
* [Senden einer Nachricht](#send-a-message)
* [Nachrichten ansehen](#watch-messages)
* [Neue Antworten ansehen](#watch-new-replies)

#### Auf eine Kanalnachricht antworten

Dieses Aktionsmodul erstellt eine Antwort auf eine Nachricht im angegebenen Kanal.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-Kennung</td> 
   <td> <p>Wählen Sie das Team in Microsoft Teams aus, dem der Kanal gehört, der die Nachricht enthält, auf die Sie antworten möchten.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanal-ID</td> 
   <td>Wählen Sie den Kanal aus, der die Nachricht enthält, auf die Sie antworten möchten.</td> 
  </tr> 
  <tr> 
   <td>Nachrichten-ID</td> 
   <td>Geben Sie die ID der Nachricht ein, auf die Sie antworten möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td>Content-Typ</td> 
   <td>Wählen Sie aus, ob die Nachricht im Nur-Text- oder HTML-Format gesendet werden soll.</td> 
  </tr> 
  <tr> 
   <td>Antwortnachricht</td> 
   <td>Geben Sie den Text der Antwortnachricht ein, die Sie senden möchten, oder mappen Sie ihn.</td> 
  </tr> 
 </tbody> 
</table>

#### Senden einer Nachricht

Dieses Aktionsmodul sendet eine Nachricht an den Kanal eines Teams oder an einen Chat.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nachrichtentyp/td&gt; 
   <td> <p>Wählen Sie aus, ob Sie eine Kanal- oder eine Chat-Nachricht senden möchten.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Team-Kennung</td> 
   <td> <p>Wenn Sie eine Nachricht an einen Kanal senden, geben Sie die ID des Teams in Microsoft Teams ein, dem der Kanal gehört, an den Sie eine Nachricht senden möchten, oder ordnen Sie sie zu.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanal-ID</td> 
   <td>Wenn Sie eine Nachricht an einen Kanal senden, geben Sie die ID des Kanals ein, an den Sie eine Nachricht senden möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td>Neuen Chat erstellen</td> 
   <td>Wenn Sie eine Chat-Nachricht senden, wählen Sie aus, ob Sie einen neuen Chat erstellen möchten.
   <ul><li><b>Ja</b><p>Wählen Sie aus, ob Sie einen Eins-zu-Eins-Chat oder einen Gruppenchat wünschen, und wählen Sie das Mitglied aus, das Sie in den Chat aufnehmen möchten. Sie müssen den Benutzer auswählen, der mit der Verbindung verbunden ist, die dieses Modul verwendet, und ein Eins-zu-eins-Chat darf nur diesen Benutzer und einen anderen Benutzer enthalten.</p><p>Wenn Sie einen Gruppen-Chat erstellen, können Sie ein Thema im Feld Thema festlegen.</p>
   <li><b>Nein</b><p>Geben Sie die ID des Teams ein, dem der Kanal gehört, an den Sie eine Nachricht senden möchten, oder ordnen Sie sie zu und geben Sie dann die ID des Kanals ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td>Nachricht</td> 
   <td>Geben Sie den Text der Nachricht ein, die Sie senden möchten, oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td>Content-Typ</td> 
   <td>Wählen Sie aus, ob die Nachricht im Nur-Text- oder HTML-Format gesendet werden soll.</td> 
  </tr> 
 </tbody> 
</table>

#### Nachrichten ansehen

Dieses Trigger-Modul startet ein Szenario, wenn eine Nachricht an den Kanal eines Teams oder an einen Chat gesendet wird.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Typ der zu überwachenden Nachrichten</td> 
   <td> <p>Wählen Sie aus, ob Sie Kanal- oder Chat-Nachrichten ansehen möchten.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Team-Kennung</td> 
   <td> <p>Wenn Sie Kanalnachrichten ansehen, wählen Sie das Team in Microsoft Teams aus, dem der Kanal gehört, den Sie auf Nachrichten überwachen.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanal-ID</td> 
   <td>Wenn Sie Kanalnachrichten ansehen, wählen Sie den Kanal aus, den Sie auf Nachrichten überwachen möchten.</td> 
  </tr> 
  <tr> 
   <td>Chat-ID</td> 
   <td>Wenn Sie Chat-Nachrichten ansehen, wählen Sie den Chat aus, den Sie auf Nachrichten beobachten möchten.</td> 
  </tr> 
  <tr> 
   <td>Maximale Anzahl an zurückgegebenen Nachrichten</td> 
   <td>Legen Sie die maximale Anzahl von Nachrichten fest, die Workfront Fusion während eines Ausführungszyklus zurückgeben soll.</td> 
  </tr> 
 </tbody> 
</table>

#### Neue Antworten ansehen

Dieses Trigger-Modul startet ein Szenario, wenn eine neue Antwort von der angegebenen Nachricht empfangen wird.

Dieses Modul ist nicht für persönliche Konten verfügbar.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Team-Kennung</td> 
   <td> <p>Wählen Sie das Team in Microsoft Teams aus, dem der Kanal gehört, den Sie auf Antworten überwachen.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanal-ID</td> 
   <td>Wählen Sie den Kanal aus, den Sie auf Antworten überwachen möchten.</td> 
  </tr> 
  <tr> 
   <td>Nachrichten-ID</td> 
   <td>Wählen Sie den Chat aus, den Sie auf Antworten beobachten möchten.</td> 
  </tr> 
  <tr> 
   <td>Maximale Anzahl an zurückgegebenen Antworten</td> 
   <td>Legen Sie die maximale Anzahl von Antworten fest, die Workfront Fusion während eines Ausführungszyklus zurückgeben soll.</td> 
  </tr> 
 </tbody> 
</table>

### Mitglied

* [Mitglied hinzufügen](#add-a-member)
* [Hinzufügen eines Mitglieds zu einer Gruppe](#add-a-member-to-a-group)

#### Mitglied hinzufügen

Dieses Aktionsmodul fügt ein Mitglied zu Microsoft Teams hinzu.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Abonnentenname</td> 
   <td> <p>Geben Sie den Namen des Mitglieds ein, das Sie zu Microsoft Teams hinzufügen möchten, oder ordnen Sie ihn zu.</p> </td> 
   </tr> 
  <tr> 
   <td>Kennwort</td> 
   <td>Geben Sie das Kennwort für das Mitglied ein oder ordnen Sie es zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Hinzufügen eines Mitglieds zu einer Gruppe

Dieses Aktionsmodul fügt ein Mitglied zu einer Office 365-Gruppe hinzu.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Gruppen-ID</td> 
   <td> <p>Wählen Sie die Gruppe aus, der Sie ein Mitglied hinzufügen möchten.</p> </td> 
   </tr> 
  <tr> 
   <td>Mitglieds-ID</td> 
   <td>Wählen Sie das Mitglied aus, das Sie der Gruppe hinzufügen möchten.</td> 
  </tr> 
 </tbody> 
</table>

### Online-Besprechung

* [Erstellen eines Online-Meetings](#create-an-online-meeting)
* [Löschen eines Online-Meetings](#delete-an-online-meeting)
* [Online-Meeting abrufen](#get-an-online-meeting)
* [Online-Besprechung aktualisieren](#update-an-online-meeting)

#### Erstellen eines Online-Meetings

Dieses Aktionsmodul erstellt eine eigenständige Besprechung, die keinem Ereignis im Kalender des Benutzers zugeordnet ist. Diese Besprechung wird nicht im Kalender des Benutzers angezeigt.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Betreff</td> 
   <td>Geben Sie einen Betreff für dieses Meeting ein oder ordnen Sie ihn zu.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Startdatum und -uhrzeit</td> 
   <td>Geben Sie das Datum und die Uhrzeit ein, zu der das Meeting beginnen soll, oder mappen Sie sie. Eine Liste der unterstützten Datumsformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Enddatum und -uhrzeit</td> 
   <td>Geben Sie das Datum und die Uhrzeit ein, zu der das Meeting enden soll, oder mappen Sie sie. Eine Liste der unterstützten Datumsformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Zulässige Referenten</td> 
   <td>Wählen Sie die Gruppe aus, die an dieser Besprechung teilnehmen darf.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Teilnehmer</td> 
   <td>Klicken Sie für jeden Teilnehmer, den Sie der Besprechung hinzufügen möchten, auf <b>Element hinzufügen</b> und wählen Sie den Namen und die Rolle des Teilnehmers aus.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Teilnehmern erlauben, ihre Kameras zu aktivieren</td> 
   <td>Wählen Sie aus, ob Teilnehmer ihre eigenen Kameras aktivieren können sollen.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Teilnehmern erlauben, ihre Mikrofone zu aktivieren</td> 
   <td>Wählen Sie aus, ob Teilnehmer die Möglichkeit haben sollen, ihre eigenen Mikrofone zu aktivieren.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Meeting-Chat zulassen</td> 
   <td>Wählen Sie aus, ob der Meeting-Chat aktiviert, deaktiviert oder auf die Dauer des Meeting-Aufrufs beschränkt werden soll</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Team-Reaktionen zulassen</td> 
   <td>Wählen Sie aus, ob Sie Team-Reaktionen für diese Besprechung aktivieren möchten.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Thread-ID</td> 
   <td>Geben Sie die ID eines Threads ein, der mit dieser Besprechung verknüpft ist, oder mappen Sie sie.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Nachrichten-ID</td> 
   <td>Geben Sie die ID einer Nachricht ein, die mit dieser Besprechung verknüpft ist, oder mappen Sie sie.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Nachrichtenkennung der Antwortkette</td> 
   <td>Geben Sie die ID der Antwortkette ein, die mit dieser Besprechung verknüpft ist, oder mappen Sie sie.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Ein- und Austritt ankündigen</td> 
   <td>Wählen Sie aus, ob die Besprechung ankündigen soll, wenn Teilnehmer eintreten oder austreten.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Umfang</td> 
   <td>Wählen Sie die Teilnehmergruppe aus, die das Warten in der Lobby umgehen kann. Diese Teilnehmer nehmen direkt an der Besprechung teil.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Aktivieren der Umgehung der Lobby durch Einwählbenutzer</td> 
   <td>Wählen Sie aus, ob Einwählbenutzer die Lobby umgehen sollen.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Automatisch aufzeichnen</td> 
   <td>Wählen Sie aus, ob das Meeting automatisch aufgezeichnet werden soll.</td> 
   </tr> 
   </tbody> 
</table>

#### Löschen eines Online-Meetings

Dieses Aktionsmodul löscht das Online-Meeting mit der angegebenen ID.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Meeting-ID</td> 
   <td> <p>Geben Sie die ID des Meetings ein, das Sie löschen möchten, oder mappen Sie sie.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Online-Meeting abrufen

Dieses Aktionsmodul ruft Details des Online-Meetings mit der angegebenen ID ab.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Meeting-ID</td> 
   <td> <p>Geben Sie die ID des Meetings ein, für das Sie Details abrufen möchten, oder ordnen Sie sie zu.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Online-Besprechung aktualisieren

Dieses Aktionsmodul aktualisiert die Online-Besprechung mit der angegebenen ID.



<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Meeting-ID</td> 
   <td>Geben Sie die ID des Meetings ein, das Sie aktualisieren möchten, oder mappen Sie sie.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Betreff</td> 
   <td>Geben Sie einen Betreff für dieses Meeting ein oder ordnen Sie ihn zu.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Startdatum und -uhrzeit</td> 
   <td>Geben Sie das Datum und die Uhrzeit ein, zu der das Meeting beginnen soll, oder mappen Sie sie. Eine Liste der unterstützten Datumsformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Enddatum und -uhrzeit</td> 
   <td>Geben Sie das Datum und die Uhrzeit ein, zu der das Meeting enden soll, oder mappen Sie sie. Eine Liste der unterstützten Datumsformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Zulässige Referenten</td> 
   <td>Wählen Sie die Gruppe aus, die an dieser Besprechung teilnehmen darf.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Teilnehmer</td> 
   <td>Klicken Sie für jeden Teilnehmer, den Sie der Besprechung hinzufügen möchten, auf <b>Element hinzufügen</b> und wählen Sie den Namen und die Rolle des Teilnehmers aus.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Teilnehmern erlauben, ihre Kameras zu aktivieren</td> 
   <td>Wählen Sie aus, ob Teilnehmer ihre eigenen Kameras aktivieren können sollen.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Teilnehmern erlauben, ihre Mikrofone zu aktivieren</td> 
   <td>Wählen Sie aus, ob Teilnehmer die Möglichkeit haben sollen, ihre eigenen Mikrofone zu aktivieren.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Meeting-Chat zulassen</td> 
   <td>Wählen Sie aus, ob der Meeting-Chat aktiviert, deaktiviert oder auf die Dauer des Meeting-Aufrufs beschränkt werden soll</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Team-Reaktionen zulassen</td> 
   <td>Wählen Sie aus, ob Sie Team-Reaktionen für diese Besprechung aktivieren möchten.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Thread-ID</td> 
   <td>Geben Sie die ID eines Threads ein, der mit dieser Besprechung verknüpft ist, oder mappen Sie sie.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Nachrichten-ID</td> 
   <td>Geben Sie die ID einer Nachricht ein, die mit dieser Besprechung verknüpft ist, oder mappen Sie sie.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Nachrichtenkennung der Antwortkette</td> 
   <td>Geben Sie die ID der Antwortkette ein, die mit dieser Besprechung verknüpft ist, oder mappen Sie sie.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Ein- und Austritt ankündigen</td> 
   <td>Wählen Sie aus, ob die Besprechung ankündigen soll, wenn Teilnehmer eintreten oder austreten.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Umfang</td> 
   <td>Wählen Sie die Teilnehmergruppe aus, die das Warten in der Lobby umgehen kann. Diese Teilnehmer nehmen direkt an der Besprechung teil.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Aktivieren der Umgehung der Lobby durch Einwählbenutzer</td> 
   <td>Wählen Sie aus, ob Einwählbenutzer die Lobby umgehen sollen.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Automatisch aufzeichnen</td> 
   <td>Wählen Sie aus, ob das Meeting automatisch aufgezeichnet werden soll.</td> 
   </tr> 
   </tbody> 
</table>

### Sonstige

* [Überprüfen der Benutzerpräsenz](#check-presence-of-users)
* [Erstellen eines benutzerdefinierten API-Aufrufs](#make-a-custom-api-call)
* [Benutzende suchen](#search-users)

#### Überprüfen der Benutzerpräsenz

Dieses Aktionsmodul prüft, ob die ausgewählten Benutzenden in Microsoft Teams vorhanden sind.

Dieses Modul unterstützt keine persönlichen Konten.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Benutzer-IDs</td> 
   <td> <p>Wählen Sie die Benutzer aus, für die Sie die Anwesenheit überprüfen möchten.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt eine benutzerdefinierte Anfrage an die Microsoft Teams-API durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://graph.microsoft.com</code> ein. Beispiel:<code> /v1.0/groups</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Benutzende suchen

Dieses Modul sucht Benutzer anhand der von Ihnen angegebenen Kriterien.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Microsoft Teams-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Verbindung erstellen - Grundlegende Anweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>Sie können einen Filter so einrichten, dass nur Benutzer zurückgegeben werden, die die von Ihnen ausgewählten Kriterien erfüllen.</p> <p>Geben Sie für jeden Filter das Feld ein, das vom Filter ausgewertet werden soll, den Operator und den Wert, den der Filter zulassen soll. Sie können mehr als einen Filter verwenden, indem Sie AND- oder OR-Regeln hinzufügen.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Legen Sie die maximale Anzahl von Teams oder Gruppen fest, die Workfront Fusion während eines Ausführungszyklus zurückgeben soll.</td> 
  </tr> 
 </tbody> 
</table>



