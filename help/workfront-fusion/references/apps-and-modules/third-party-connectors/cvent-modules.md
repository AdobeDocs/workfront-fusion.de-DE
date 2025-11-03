---
title: Cvent-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Cvent verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: b7e16180-1db8-4aff-bb7b-69ca98194b00
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 1%

---

# [!DNL Cvent]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Cvent] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um [!DNL Cvent]-Module verwenden zu können, müssen Sie über ein [!DNL Cvent]-Konto verfügen.

## Ereignis-API-Informationen

Der Event-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> V200611.ASMX </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.7.14</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL Cvent] mit Adobe Workfront Fusion {#connect-cvent-to-adobe-workfront-fusion}

>[!NOTE]
>
>Die [!DNL Cvent]-Module funktionieren über eine [!UICONTROL SOAP]-API. Um eine Verbindung zu [!DNL Cvent] herzustellen, müssen Sie Folgendes sicherstellen:
>
>* Sie haben [!UICONTROL SOAP] Zugriff auf die [!DNL Cvent]-API.
>* Die IP-Adressen von Workfront Fusion wurden zur -Zulassungsliste Ihres Unternehmens hinzugefügt.
>
>  Eine Liste der IP-Adressen von Workfront Fusion finden Sie unter [Konfigurieren von IP-Adressen für Fusion in der -Zulassungsliste Ihres Unternehmens](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)


Sie können direkt aus einem [!DNL Cvent]-Modul heraus eine Verbindung zu Ihrem [!DNL Cvent]-Konto herstellen.

1. Klicken Sie in einem [!DNL Cvent] Modul **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Wählen Sie die Region aus, mit der Sie eine Verbindung herstellen möchten.

   * [!UICONTROL Nordamerika]
   * [!UICONTROL Europa]
   * [!UICONTROL Sandbox]

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Cvent] Module und ihre Felder

Beim Konfigurieren von [!DNL Cvent] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Cvent] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Aktionen

* [[!UICONTROL Benutzerdefinierter API-Aufruf]](#create-meeting-request)
* [[!UICONTROL Eintrag lesen]](#read-a-record)
* [[!UICONTROL Registrieren des &#x200B;]](#register-invitee)
* [[!UICONTROL Einladende hinzufügen]](#add-invitee)
* [[!UICONTROL Kontakt löschen]](#delete-contact)
* [[!UICONTROL Kontakt aktualisieren]](#update-contact)
* [[!UICONTROL Besprechungsanfrage erstellen]](#create-meeting-request)

#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Cvent]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Cvent] nicht durchgeführt werden kann.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

Das Modul gibt den Status-Code zusammen mit den Kopfzeilen und dem Hauptteil des API-Aufrufs zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Cvent]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Cvent] mit Adobe Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vorgang</td> 
   td&gt; <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Hauptteil (XML)</td> 
   <td> <p>Geben Sie den Hauptteil des API-Aufrufs ein oder mappen Sie ihn. Dies darf nur die XML enthalten. Das Modul enthält automatisch Authentifizierungskopfzeilen. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eintrag lesen]

Dieses Aktionsmodul liest Informationen zu einem bestimmten Datensatz.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Cvent]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Cvent] mit Adobe Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Datensatztyp]</p> </td> 
   <td>Wählen Sie den Elementtyp des Datensatzes aus, den Sie lesen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kontakt] / [!UICONTROL Ereignis] / [!UICONTROL Einladungs-ID]</td> 
   <td> <p>Geben Sie die ID des Elements ein, das Sie lesen möchten, oder mappen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten. Felder sind je nach ausgewähltem Elementtyp verfügbar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Registrieren des &#x200B;]

Dieses Aktionsmodul registriert eine Einladung für ein Ereignis.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Cvent]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Cvent] mit Adobe Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Einladungs-ID</p> </td> 
   <td> <p>Geben Sie die ID der Einladung ein, die Sie für ein Ereignis registrieren möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ereignis-ID</td> 
   <td> <p>Geben Sie die ID des Ereignisses ein, für das Sie die Einladung registrieren möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Einladende hinzufügen]

Dieses Aktionsmodul lädt einen Kontakt zu einem Ereignis ein.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Cvent]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Cvent] mit Adobe Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kontakt-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Kontakts ein, den Sie einem Ereignis hinzufügen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ereignis-ID]</td> 
   <td> <p>Geben Sie die ID des Ereignisses ein, dem Sie den Kontakt hinzufügen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kontakt löschen]

Dieses Aktionsmodul löscht einen einzelnen Kontakt in Cvent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Cvent]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Cvent] mit Adobe Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kontakt-ID]</td> 
   <td> <p>Geben Sie die ID des Kontakts ein, den Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kontakt aktualisieren]

Dieses Aktionsmodul aktualisiert einen vorhandenen Kontakt mithilfe seiner ID.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Cvent]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Cvent] mit Adobe Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Kontakt-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Kontakts ein, den Sie aktualisieren möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Felder]</td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Informationen eingeben möchten, und geben Sie dann die gewünschten Werte für diese Felder ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Benutzerdefinierte Felder]</td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Informationen eingeben möchten, und geben Sie dann die gewünschten Werte für diese Felder ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Besprechungsanfrage erstellen]

Dieses Aktionsmodul fügt Ihrem Konto eine Besprechungsanfrage hinzu.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Cvent]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Cvent] mit Adobe Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Formular-ID]</p> </td> 
   <td> <p>Geben Sie die ID des Formulars ein, das Sie zum Erstellen der neuen Besprechungsanfrage verwenden möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Felder für Besprechungsanfragen]</td> 
   <td> <p>Wählen Sie die Felder für die Besprechungsanfrage aus, für die Sie Informationen eingeben möchten, und geben Sie dann die gewünschten Werte für diese Felder ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ereignisanforderungsfelder]</td> 
   <td> <p>Wählen Sie die Ereignisanforderungsfelder aus, für die Sie Informationen eingeben möchten, und füllen Sie dann die gewünschten Werte für diese Felder aus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL RFP-Anforderungsfelder]</td> 
   <td> <p>Wählen Sie die Felder der Angebotsanforderung aus, für die Sie Informationen eingeben möchten, und geben Sie dann die gewünschten Werte für diese Felder ein.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

#### [!UICONTROL Einträge auflisten]

Dieses Suchmodul ruft Informationen zu allen Datensätzen eines bestimmten Typs ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Cvent]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Cvent] mit Adobe Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Datensatztyp]</p> </td> 
   <td> <p>Wählen Sie den Datensatztyp aus, den Sie auflisten möchten.</p> 
    <ul> 
     <li> <p>Alle Ereignisse aus Ihrem [!DNL Cvent] Konto</p> </li> 
     <li> <p>Alle Sitzungen für ein Ereignis</p> </li> 
     <li> <p>Alle Einladungen für eine Veranstaltung</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ereignis-ID]</td> 
   <td> <p>Wenn Sie Einladungen oder Sitzungen auflisten, geben Sie die ID des Ereignisses ein, mit dem diese Einladungen oder Sitzungen verknüpft sind, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>
