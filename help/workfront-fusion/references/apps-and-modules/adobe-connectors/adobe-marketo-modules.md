---
title: Marketo-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Marketo] verwenden, und diese mit verschiedenen Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: ht
source-wordcount: '2237'
ht-degree: 100%

---

# [!DNL Marketo]-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Marketo] verwenden, und diese mit verschiedenen Anwendungen und Services von Drittanbietern verbinden.

Eine Videoeinführung zum Marketo-Connector finden Sie über folgenden Link:

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Erstellen von Szenarios: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Ein beliebiges Adobe Workfront Workflow- und Adobe Workfront Automation and Integration-Paket</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-Lizenz</td> 
   <td>
   <p>Betriebsbasiert: keine Workfront Fusion-Lizenz erforderlich</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

1. Klicken Sie in einem beliebigen Marketo-Modul neben dem Feld „Verbindung“ auf **Hinzufügen**.
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
          <p>Geben Sie einen Namen für die neue Verbindung ein. </p>
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
          <p>Wählen Sie aus, ob eine Verbindung zu einem Service-Konto oder einem persönlichen Konto hergestellt werden soll.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Konto-/Munchkin-ID]</td>
        <td>
          <p>Geben Sie Ihre [!DNL Marketo]-Konto- oder [!DNL Marketo] [!UICONTROL Munchkin]-ID ein. Dies ist der eindeutige Teil der Basis-URL oder der Ihrem Konto zugewiesene Endpunkt, mit dem Sie über die [!UICONTROL REST]-API auf [!DNL Marketo] zugreifen. Anweisungen dazu, wie Sie dies finden, finden Sie unter [Basis-URL](https://developers.marketo.com/rest-api/base-url/) in der [!DNL Marketo]-Dokumentation.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre Marketo-Client-ID ein. Anweisungen, wie Sie diese finden, finden Sie unter [Authentifizierung](https://developers.marketo.com/rest-api/authentication/) in der [!DNL Marketo]-Dokumentation.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr Marketo-Client-Geheimnis ein. Anweisungen, wie Sie diese finden, finden Sie unter [Authentifizierung](https://developers.marketo.com/rest-api/authentication/) in der [!DNL Marketo]-Dokumentation.</td>
      </tr>
     </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Fortsetzen]**, um die Verbindung zu erstellen und zum Modul zurückzukehren.

## [!DNL Marketo]-Module und ihre Felder

Beim Konfigurieren von [!DNL Marketo]-Modulen werden in Workfront Fusion die unten aufgeführten Felder angezeigt. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere [!DNL Marketo]-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

* [[!UICONTROL Ereignisse überwachen (sofort)]](#watch-events-instant)
* [[!UICONTROL Einträge überwachen]](#watch-records)

#### [!UICONTROL Ereignisse überwachen (sofort)]

Dieses Auslösermodul startet ein Szenario, wenn ein Eintrag erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Geben Sie den Webhook ein, den das Modul verwenden soll.</p> <p>Weitere Informationen zu Webhooks finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschränkung]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Einträge überwachen]

Dieses Auslösermodul startet ein Szenario, wenn ein Eintrag erstellt oder aktualisiert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Eintrags aus, der erstellt werden soll.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Aktivität]</strong> </p> <p>Wählen Sie den Aktivitätstyp aus, der überwacht werden soll. </p> <p>Das Modul achtet nur auf neue Aktivitäten.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>Wählen Sie im Feld <b>Ereignistyp</b> aus, ob auf neue, aktualisierte, neue und aktualisierte Einträge oder bestimmte Feldaktualisierungen geachtet werden soll. Wenn Sie festlegen, dass bestimmte Feldaktualisierungen überwacht werden sollen, wählen Sie das Feld aus, das vom Modul überwacht werden soll.</p> </li> 
     <li> <p><strong>[!UICONTROL Programm]</strong> </p> <p>Wählen Sie im Feld <b>Ereignistyp</b> aus, ob auf neue, aktualisierte oder sowohl auf neue als auch aktualisierte Einträge geachtet werden soll.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschränkung]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Leads zu einer Liste hinzufügen]](#add-leads-to-a-list)
* [[!UICONTROL Programm klonen]](#clone-a-program)
* [[!UICONTROL Eintrag erstellen]](#create-a-record)
* [[!UICONTROL Benutzerdefinierter API-Aufruf]](#custom-api-call)
* [[!UICONTROL Datei herunterladen]](#download-a-file)
* [[!UICONTROL Eintrag lesen]](#read-a-record)
* [[!UICONTROL Leads aus einer Liste entfernen]](#remove-leads-from-a-list)
* [[!UICONTROL Kampagne planen]](#schedule-a-campaign)
* [[!UICONTROL Eintrag aktualisieren]](#update-a-record)
* [[!UICONTROL Datei hochladen]](#upload-a-file)

#### [!UICONTROL Leads zu einer Liste hinzufügen]

Dieses Aktionsmodul fügt mithilfe der Lead-ID einen oder mehrere Leads zu einer Liste hinzu. Sie können bis zu 300 Leads gleichzeitig hinzufügen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listen-ID]</td> 
   <td>Geben Sie die ID der Liste ein, der Leads hinzugefügt werden sollen, oder ordnen Sie diese zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead-IDs]</td> 
   <td> <p>Klicken Sie für jeden Lead, der der Liste hinzugefügt werden soll, auf <b>[!UICONTROL Hinzufügen]</b> und geben Sie dann die ID des hinzuzufügenden Leads ein oder ordnen Sie diese zu. Sie können bis zu 300 Leads hinzufügen, die vom Modul der Liste hinzugefügt werden sollen.</p> <p>Klicken Sie auf den Umschalter „Zuordnung“, um eine vorhandene Sammlung von Leads zuzuordnen, die der Liste hinzugefügt werden sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Programm klonen]

Dieses Aktionsmodul erstellt eine Kopie eines Programms mit der ID des vorhandenen Programms.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vorhandene Programm-ID]</td> 
   <td>Geben Sie die ID des Programms ein, das kopiert werden soll, oder ordnen Sie diese zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Neuer Programmname]</p> </td> 
   <td> <p>Geben Sie einen Namen für das neue Programm ein oder ordnen Sie diesen zu.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID]</td> 
   <td>Geben Sie die ID des Ordners ein, in dem das neue Programm gespeichert werden soll, oder ordnen Sie diese zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eintrag erstellen]

Dieses Aktionsmodul erstellt einen neuen Eintrag in [!DNL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Eintrags aus, der erstellt werden soll.</p> 
    <ul> 
     <li> <p>[!UICONTROL Unternehmen]</p> </li> 
     <li> <p>[!UICONTROL Ordner]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Programm]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Felder zum Zuordnen auswählen]</td> 
   <td>Wenn Sie ein Unternehmen oder einen Lead erstellen, wählen Sie die Felder aus, für die beim Erstellen des neuen Eintrags Werte festgelegt werden sollen, und geben Sie dann Werte für diese Felder ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Programmtyp]</td> 
   <td>Wenn Sie ein Programm erstellen, wählen Sie den zu erstellenden Programmtyp aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Programmkanal] </td> 
   <td>Wenn Sie ein Programm erstellen, wählen Sie den Programmkanal aus, in dem das Programm erstellt werden soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner]/[!UICONTROL Programmname]</td> 
   <td>Wenn Sie einen Ordner oder ein Programm erstellen, geben Sie einen Namen für den neuen Eintrag ein oder ordnen Sie diesen zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td> <p>Wenn Sie einen Ordner oder ein Programm erstellen, geben Sie eine Beschreibung für den neuen Eintrag ein oder ordnen Sie diese zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID des übergeordneten Ordners]</td> 
   <td>Wenn Sie einen Ordner oder ein Programm erstellen, geben Sie die ID des übergeordneten Ordners ein, in dem der neue Eintrag erstellt werden soll, oder ordnen Sie die ID zu.</td> 
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

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Marketo]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, was über die anderen [!DNL Marketo]-Module nicht möglich ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://{your-base-url}.mktorest.com/</code> ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Header]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] fügt die Autorisierungs-Header für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Felder]</td> 
   <td> <p>Klicken Sie für jedes dem API-Aufruf hinzuzufügende Feld auf <b>Element hinzufügen</b> und geben Sie den Schlüssel und den Wert des Felds ein.</td> 
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
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datei-ID]</td> 
   <td>Geben Sie die ID der Datei ein, die heruntergeladen werden soll, oder ordnen Sie diese zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eintrag lesen]

Dieses Aktionsmodul liest Informationen zu einem Eintrag unter Verwendung seiner ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Eintrags aus, der erstellt werden soll.</p> 
    <ul> 
     <li> <p>[!UICONTROL Kampagne]</p> </li> 
     <li> <p>[!UICONTROL Unternehmen]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Liste]</p> </li> 
     <li> <p>[!UICONTROL Programm]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen. Die Felder sind abhängig von der Auswahl unter „[!UICONTROL Eintragstyp]“ verfügbar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL &lt;Object&gt;-ID]</td> 
   <td>Geben Sie die ID des Objekts ein, zu dem Informationen abgerufen werden sollen, oder ordnen Sie diese zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leads aus einer Liste entfernen]

Dieses Aktionsmodul entfernt mithilfe der Lead-ID einen oder mehrere Leads aus einer Liste. Sie können bis zu 300 Leads gleichzeitig entfernen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Listen-ID]</td> 
   <td>Geben Sie die ID der Liste ein, aus der Leads entfernt werden sollen, oder ordnen Sie diese zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead-IDs]</td> 
   <td> <p>Klicken Sie für jeden Lead, der aus der Liste entfernt werden soll, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie dann die ID des zu entfernenden Leads ein oder ordnen Sie diese zu. Sie können bis zu 300 Leads hinzufügen, die vom Modul aus der Liste entfernt werden sollen. </p> <p>Klicken Sie auf den Umschalter „Zuordnung“, um eine vorhandene Sammlung von Leads zuzuordnen, die aus der Liste entfernt werden sollen.</p> </td> 
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
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kampagnen-ID]</td> 
   <td>Geben Sie die ID der Kampagne ein, die geplant werden soll, oder ordnen Sie diese zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Datum festlegen]</p> </td> 
   <td>Wählen Sie das Datum aus, an dem die Kampagne ausgeführt werden soll. Wird dieses Feld leer gelassen, startet die Kampagne fünf Minuten nach Szenariobeginn.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eintrag aktualisieren]

Dieses Aktionsmodul aktualisiert einen vorhandenen Eintrag unter Verwendung seiner ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Eintrags aus, der erstellt werden soll.</p> 
    <ul> 
     <li> <p>[!UICONTROL Unternehmen]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Programm]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Unternehmen]/[!UICONTROL Lead]/[!UICONTROL Programm-ID]</td> 
   <td>Geben Sie die ID des Eintrags ein, der aktualisiert werden soll, oder ordnen Sie diese zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Felder zum Zuordnen auswählen]</td> 
   <td>Wenn Sie ein Unternehmen oder einen Lead aktualisieren, wählen Sie die Felder aus, deren Werte aktualisiert werden sollen, und geben Sie dann Werte für diese Felder ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Programmname]</td> 
   <td>Wenn Sie ein Programm aktualisieren, geben Sie einen neuen Namen für das Programm ein oder ordnen Sie diesen zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td> <p>Wenn Sie ein Programm aktualisieren, geben Sie eine neue Beschreibung für das Programm ein oder ordnen Sie diese zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Startdatum]</td> 
   <td>Wenn Sie ein Programm aktualisieren, geben Sie ein neues Startdatum für das Programm ein oder ordnen Sie dieses zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enddatum]</td> 
   <td>Wenn Sie ein Programm aktualisieren, geben Sie ein neues Enddatum für das Programm ein oder ordnen Sie dieses zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Kosten]</td> 
   <td>Wenn Sie ein Programm aktualisieren, fügen Sie etwaige Kosten hinzu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Wenn Sie ein Programm aktualisieren, fügen Sie beliebige Tags hinzu.</td> 
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
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordner-ID]</td> 
   <td>Geben Sie die ID des Ordners ein, in dem die neue Datei gespeichert werden soll, oder ordnen Sie diese zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschreibung]</td> 
   <td>Geben Sie eine Beschreibung für die hochgeladene Datei ein.</td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL Einträge auflisten]](#list-records)
* [[!UICONTROL Einträge suchen]](#update-a-record)

#### [!UICONTROL Einträge auflisten]

Dieses Aktionsmodul ruft alle Einträge eines bestimmten Typs ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Eintrags aus, der aufgelistet werden soll.</p> 
    <ul> 
     <li> <p>[!UICONTROL Alle Kampagnen lesen]</p> </li> 
     <li> <p>[!UICONTROL Alle Programme lesen]</p> </li> 
     <li> <p>[!UICONTROL Alle Leads lesen] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Feld]</td> 
   <td>Wenn Sie Leads abrufen möchten, wählen Sie aus, ob Leads aus einer Liste oder aus einem Programm abgerufen werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen. Die Felder sind abhängig von der Auswahl unter „[!UICONTROL Eintragstyp]“ verfügbar.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschränkung]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Einträge suchen]

Dieses Suchmodul ruft eine Liste von Einträgen ab, die bestimmten Suchkriterien entsprechen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Marketo]-Kontos mit Workfront Fusion finden Sie in diesem Artikel unter <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Marketo] mit Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie den Typ des Eintrags aus, der gesucht werden soll.</p> 
    <ul> 
     <li> <p>[!UICONTROL Kampagnen]</p> </li> 
     <li> <p>[!UICONTROL Leads]</p> </li> 
     <li> <p>[!UICONTROL Programme]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Feld]</p> </td> 
   <td> <p>Wählen Sie das Feld aus, nach dem gesucht werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Wert/Werte]</td> 
   <td>Geben Sie den Wert des Feldes ein, nach dem gesucht werden soll. Wenn Sie im Feld nach mehreren Werten suchen können, klicken Sie für jeden Wert, nach dem gesucht werden soll, auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie den Wert ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgabe]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschränkung]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Einträgen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder ordnen Sie diese zu.</p> </td> 
  </tr> 
 </tbody> 
</table>
