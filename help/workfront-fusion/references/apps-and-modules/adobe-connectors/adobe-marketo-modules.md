---
title: Marketo-Module
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die  [!DNL Marketo] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2165'
ht-degree: 0%

---

# [!DNL Marketo]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Marketo] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Eine Videoeinführung zum Marketo-Connector finden Sie unter:

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

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

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um [!DNL Marketo]-Module verwenden zu können, müssen Sie über ein [!DNL Marketo]-Konto verfügen.

## Marketo-API-Informationen

Der Marketo-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.14.19</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL Marketo] mit Workfront Fusion {#connect-marketo-to-workfront-fusion}

Sie können direkt aus einem beliebigen [!DNL Marketo]-Modul heraus eine Verbindung zu Ihrem [!DNL Marketo]-Konto herstellen.

1. Klicken Sie in einem beliebigen Marketo **Modul** Hinzufügen) neben dem Feld Verbindung .
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
          <p>Geben Sie einen Namen für die neue Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>
          <p>Wählen Sie aus, ob eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung hergestellt werden soll.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL-Konto / Munchkin-ID]</td>
        <td>
          <p>Geben Sie Ihr [!DNL Marketo] oder [!DNL Marketo] [!UICONTROL Munchkin] ID ein. Dies ist der eindeutige Teil der Ihrem Konto zugewiesenen Basis-URL oder des Endpunkts, mit dem Sie über die [!UICONTROL REST]-API auf [!DNL Marketo] zugreifen. Anweisungen dazu, wie Sie dies finden, finden Sie unter [Basis-URL](https://developers.marketo.com/rest-api/base-url/) in der [!DNL Marketo].</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre Marketo-Client-ID ein. Anweisungen, wie Sie dies finden, finden Sie unter [Authentifizierung](https://developers.marketo.com/rest-api/authentication/) in der [!DNL Marketo].</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr Marketo-Client-Geheimnis ein. Anweisungen, wie Sie diese finden, finden Sie unter [Authentifizierung](https://developers.marketo.com/rest-api/authentication/) in der [!DNL Marketo].</td>
      </tr>
     </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Marketo] Module und ihre Felder

Beim Konfigurieren [!DNL Marketo] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Marketo] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

* [[!UICONTROL Ereignisse beobachten (Sofort)]](#watch-events-instant)
* [[!UICONTROL Einträge beobachten]](#watch-records)

#### [!UICONTROL Ereignisse beobachten (Sofort)]

Dieses Trigger-Modul startet ein Szenario, wenn ein Datensatz erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Geben Sie den Webhook ein, den das Modul verwenden soll.</p> <p>Weitere Informationen zu Webhooks finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Einträge beobachten]

Dieses Trigger-Modul startet ein Szenario, wenn ein Datensatz erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie erstellen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL-Aktivität]</strong> </p> <p>Wählen Sie den Aktivitätstyp aus, den Sie überwachen möchten. </p> <p>Das Modul überwacht nur neue Aktivitäten.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>Wählen Sie im Feld <b>Ereignistyp</b> aus, ob Sie auf neue, aktualisierte, neue und aktualisierte Datensätze oder bestimmte Feldaktualisierungen achten möchten. Wenn Sie festlegen, dass bestimmte Feldaktualisierungen überwacht werden sollen, wählen Sie das Feld aus, das das Modul überwachen soll.</p> </li> 
     <li> <p><strong>[!UICONTROL-Programm]</strong> </p> <p>Wählen Sie im Feld <b>Ereignistyp</b> aus, ob Sie auf neue, aktualisierte oder sowohl neue als auch aktualisierte Datensätze achten möchten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Hinzufügen von Leads zu einer Liste]](#add-leads-to-a-list)
* [[!UICONTROL Klonen eines Programms]](#clone-a-program)
* [[!UICONTROL Datensatz erstellen]](#create-a-record)
* [[!UICONTROL Benutzerdefinierter API-Aufruf]](#custom-api-call)
* [[!UICONTROL Datei herunterladen]](#download-a-file)
* [[!UICONTROL Datensatz lesen]](#read-a-record)
* [[!UICONTROL Entfernen von Leads aus einer Liste]](#remove-leads-from-a-list)
* [[!UICONTROL Kampagne planen]](#schedule-a-campaign)
* [[!UICONTROL Aktualisieren eines Datensatzes]](#update-a-record)
* [[!UICONTROL Datei hochladen]](#upload-a-file)

#### [!UICONTROL Hinzufügen von Leads zu einer Liste]

Dieses Aktionsmodul fügt mithilfe der Lead-ID einen oder mehrere Leads zu einer Liste hinzu. Sie können bis zu 300 Leads gleichzeitig hinzufügen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listen-ID]</td> 
   <td>Geben Sie die ID der Liste ein, der Sie Leads hinzufügen möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead-IDs]</td> 
   <td> <p>Klicken Sie für jeden Lead, den Sie der Liste hinzufügen möchten, auf <b>[!UICONTROL Hinzufügen]</b> und geben Sie dann die ID des Leads ein, den Sie hinzufügen möchten, oder mappen Sie sie. Sie können bis zu 300 Leads für das Modul hinzufügen, das der Liste hinzugefügt werden soll.</p> <p>Klicken Sie auf den Umschalter Zuordnung , um eine vorhandene Sammlung von Leads zuzuordnen, die Sie der Liste hinzufügen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Klonen eines Programms]

Dieses Aktionsmodul erstellt eine Kopie eines Programms mit der ID des vorhandenen Programms.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorhandene Programm-ID]</td> 
   <td>Geben Sie die ID des Programms ein, das Sie kopieren möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Neuer Programmname]</p> </td> 
   <td> <p>Namen für das neue Programm eingeben oder zuordnen</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID]</td> 
   <td>Geben Sie die ID des Ordners ein, in dem sich das neue Programm befinden soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datensatz erstellen]

Dieses Aktionsmodul erstellt einen neuen Datensatz in [!DNL Marketo]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie erstellen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL Firma]</p> </li> 
     <li> <p>[!UICONTROL-Ordner]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL-Programm]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Felder zum Zuordnen auswählen]</td> 
   <td>Wenn Sie eine Firma oder einen Lead erstellen, wählen Sie die Felder aus, für die Sie Werte beim Erstellen des neuen Datensatzes festlegen möchten, und geben Sie dann Werte für diese Felder ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Programmtyp]</td> 
   <td>Wenn Sie ein Programm erstellen, wählen Sie den Programmtyp aus, den Sie erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Programmkanal] </td> 
   <td>Wenn Sie ein Programm erstellen, wählen Sie den Programmkanal aus, in dem Sie das Programm erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Ordner] / [!UICONTROL-Programmname]</td> 
   <td>Wenn Sie einen Ordner oder ein Programm erstellen, geben Sie einen Namen für den neuen Datensatz ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td> <p>Wenn Sie einen Ordner oder ein Programm erstellen, geben Sie eine Beschreibung für den neuen Datensatz ein oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID des übergeordneten Ordners]</td> 
   <td>Wenn Sie einen Ordner oder ein Programm erstellen, geben Sie die ID des übergeordneten Ordners ein, in dem Sie den neuen Datensatz erstellen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kosten]</td> 
   <td>Wenn Sie ein Programm erstellen, fügen Sie etwaige Kosten hinzu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Wenn Sie ein Programm erstellen, fügen Sie beliebige Tags hinzu</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Marketo]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Marketo] nicht durchgeführt werden kann.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://{your-base-url}.mktorest.com/</code> ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Felder]</td> 
   <td> <p>Klicken Sie für jedes Feld, das Sie Ihrem API-Aufruf hinzufügen möchten, <b> „Element hinzufügen</b> und geben Sie den Schlüssel und den Wert des Felds ein.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei herunterladen]

Dieses Aktionsmodul lädt eine Datei unter Verwendung der Datei-ID herunter.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td>Geben Sie die ID der Datei ein, die Sie herunterladen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datensatz lesen]

Dieses Aktionsmodul liest Informationen über einen Datensatz unter Verwendung seiner ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie erstellen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaign]</p> </li> 
     <li> <p>[!UICONTROL Firma]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL-Liste]</p> </li> 
     <li> <p>[!UICONTROL-Programm]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen. Die Felder sind je nach ausgewähltem [!UICONTROL Record Type] verfügbar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL &lt;Objekt&gt;-ID]</td> 
   <td>Geben Sie die ID des Objekts ein, zu dem Sie Informationen abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Entfernen von Leads aus einer Liste]

Dieses Aktionsmodul entfernt einen oder mehrere Leads mithilfe der Lead-ID aus einer Liste. Sie können bis zu 300 Leads gleichzeitig entfernen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listen-ID]</td> 
   <td>Geben Sie die ID der Liste ein, aus der Sie Leads entfernen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead-IDs]</td> 
   <td> <p>Klicken Sie für jeden Lead, den Sie aus der Liste entfernen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie dann die ID des Leads ein, den Sie entfernen möchten, oder ordnen Sie sie zu. Sie können bis zu 300 Leads hinzufügen, damit das Modul aus der Liste entfernt werden kann. </p> <p>Klicken Sie auf den Umschalter Zuordnung , um eine vorhandene Sammlung von Leads zuzuordnen, die Sie aus der Liste entfernen möchten.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Kampagne planen]

Dieses Aktionsmodul plant eine vorhandene Kampagne für ein bestimmtes Datum.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kampagnen-ID]</td> 
   <td>Geben Sie die ID der Kampagne ein, die Sie planen möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Zeitplan für Datum]</p> </td> 
   <td>Datum auswählen, an dem die Kampagne ausgeführt werden soll. Wenn dieses Feld leer gelassen wird, wird die Kampagne fünf Minuten nach Beginn des Szenarios ausgeführt.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren eines Datensatzes]

Dieses Aktionsmodul aktualisiert einen vorhandenen Datensatz unter Verwendung seiner ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie erstellen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL Firma]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL-Programm]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Unternehmen] / [!UICONTROL Lead] / [!UICONTROL Programm-ID]</td> 
   <td>Geben Sie die ID des Datensatzes ein, den Sie aktualisieren möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Felder zum Zuordnen auswählen]</td> 
   <td>Wenn Sie eine Firma oder einen Lead aktualisieren, wählen Sie die Felder aus, deren Werte Sie aktualisieren möchten, und geben Sie dann Werte für diese Felder ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Programmname]</td> 
   <td>Wenn Sie ein Programm aktualisieren, geben Sie einen neuen Namen für das Programm ein oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td> <p>Wenn Sie ein Programm aktualisieren, geben Sie eine neue Beschreibung für das Programm ein oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Startdatum]</td> 
   <td>Wenn Sie ein Programm aktualisieren, geben Sie ein neues Startdatum für das Programm ein oder mappen Sie es.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enddatum]</td> 
   <td>Wenn Sie ein Programm aktualisieren, geben Sie ein neues Enddatum für das Programm ein oder mappen Sie es.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kosten]</td> 
   <td>Wenn Sie ein Programm aktualisieren, fügen Sie etwaige Kosten hinzu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Wenn Sie ein Programm aktualisieren, fügen Sie beliebige Tags hinzu</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei hochladen]

Dieses Aktionsmodul lädt eine neue Datei in [!UICONTROL Marketo] hoch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID]</td> 
   <td>Geben Sie die ID des Ordners ein, in dem sich die neue Datei befinden soll, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td>Geben Sie eine Beschreibung für die hochgeladene Datei ein.</td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL Einträge auflisten]](#list-records)
* [[!UICONTROL Datensätze suchen]](#update-a-record)

#### [!UICONTROL Einträge auflisten]

Dieses Aktionsmodul ruft alle Datensätze eines bestimmten Typs ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Datensatztyp aus, den Sie auflisten möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL Alle Kampagnen lesen]</p> </li> 
     <li> <p>[!UICONTROL Alle Programme lesen]</p> </li> 
     <li> <p>[!UICONTROL Alle Leads lesen] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Feld]</td> 
   <td>Wenn Sie Leads abrufen möchten, wählen Sie aus, ob Sie Leads aus einer Liste oder aus einem Programm abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen. Die Felder sind je nach ausgewähltem [!UICONTROL Record Type] verfügbar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datensätze suchen]

Dieses Suchmodul ruft eine Liste von Datensätzen ab, die bestimmten Suchkriterien entsprechen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie suchen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL Kampagnen]</p> </li> 
     <li> <p>[!UICONTROL Leads]</p> </li> 
     <li> <p>[!UICONTROL Programme]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Feld]</p> </td> 
   <td> <p>Wählen Sie das Feld aus, nach dem Sie suchen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wert / Werte]</td> 
   <td>Geben Sie den Wert des Felds ein, nach dem Sie suchen möchten. Wenn Sie im Feld nach mehreren Werten suchen können, klicken Sie für jeden Wert, nach dem Sie suchen möchten, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie den Wert ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabe]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>
