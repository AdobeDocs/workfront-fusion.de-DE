---
title: Microsoft Dynamics 365-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die Microsoft Dynamics 365 verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 16ae173b-10ce-481d-8f6c-1df0e65f7c0e
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1810'
ht-degree: 0%

---

# [!DNL Microsoft Dynamics 365 modules]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Microsoft Dynamics 365] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

>[!NOTE]
>
>Der [!DNL Microsoft Dynamics 365]-Connector unterstützt keine [!DNL Dynamics Finance and Operations].
>
>Weitere Informationen zum [!DNL Microsoft Dynamics 365 Finance and Operations]-Connector finden Sie unter [[!DNL Microsoft Dynamics 365 Finance and Operations] module](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/dynamics-finance-operations-modules.md).

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

Um [!DNL Microsoft Dynamics] 365 verwenden zu können, müssen Sie über ein [!DNL Microsoft Dynamics 365] verfügen.

## Verbinden von Microsoft Dynamics 365 mit Workfront Fusion

Sie können direkt aus einem [!DNL Microsoft Dynamics 365]-Modul heraus eine Verbindung zu Ihrem [!DNL Microsoft Dynamics 365]-Konto herstellen.

>[!NOTE]
>
>Einige Microsoft-Apps verwenden dieselbe Verbindung, die an individuelle Benutzerberechtigungen gebunden ist. Daher werden beim Erstellen einer Verbindung im Einverständnisbildschirm für Berechtigungen alle Berechtigungen angezeigt, die zuvor der Verbindung dieses Benutzers gewährt wurden, zusätzlich zu den neuen Berechtigungen, die für die aktuelle Anwendung erforderlich sind.
>
>Wenn ein Benutzer beispielsweise über die über den Excel-Connector gewährten Berechtigungen zum Lesen von Tabellen verfügt und dann im Outlook-Connector eine Verbindung zum Lesen von E-Mails erstellt, zeigt der Einverständnisbildschirm für Berechtigungen sowohl die bereits erteilte Berechtigung zum Lesen von Tabellen als auch die neu erforderliche Berechtigung zum Schreiben von E-Mails an.

1. Klicken Sie in einem [!DNL Microsoft Dynamics 365] Modul **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].


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
          <td>Geben Sie Ihre [!DNL Microsoft Dynamics] [!UICONTROL Client ID] ein.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client-Geheimnis]<p>(Optional)</p></td>
          <td>Geben Sie Ihren [!DNL Microsoft Dynamics] [!UICONTROL Client Secret] ein.
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL-Authentifizierungs-URL]</td>
          <td>Geben Sie die URL ein, die Ihre Workfront-Instanz zur Authentifizierung dieser Verbindung verwenden soll. <p>Der Standardwert ist <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL-Ressource]</td>
          <td>Geben Sie die Adresse Ihres [!DNL Dynamics 365] Kontos ohne <code>>https://</code> ein.</p>
        </tr>
      </tbody>
    </table>
1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

>[!NOTE]
>
>Verwenden Sie beim Registrieren von [!DNL Workfront Fusion] in Ihrem [!DNL Microsoft Azure]-Portal den folgenden Umleitungs-URI:
>
>* `https://app.workfrontfusion.com/oauth/cb/workfront-microsoft-dynamics2`


## [!DNL Microsoft Dynamics 365] Module und ihre Felder

Beim Konfigurieren [!DNL Microsoft Dynamics 365] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Microsoft Dynamics 365] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

* [[!UICONTROL Datensätze ansehen (Echtzeit)]](#watch-records-real-time)
* [[!UICONTROL Datensätze beobachten (geplant)]](#watch-records-scheduled)

#### [!UICONTROL Datensätze ansehen (Echtzeit)]

Dieses Instant Trigger-Modul führt ein Szenario aus, wenn ein von Ihnen angegebener Datensatz (Objekt) in [!DNL Dynamics 365] erstellt oder aktualisiert wird.

In diesem Modul ist ein Webhook erforderlich.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Wählen Sie den Webhook aus, den Sie für dieses Modul verwenden möchten. </p> <p>So fügen Sie einen neuen Webhook hinzu:</p> 
    <ol> 
     <li value="1"> <p>Klicken Sie auf <strong>[!UICONTROL Hinzufügen]</strong> rechts neben dem Feld Webhook</p> </li> 
     <li value="2"> <p>Geben Sie in das Namensfeld <strong>[!UICONTROL Webhook]</strong> einen beschreibenden Namen für den Webhook ein.</p> </li> 
     <li value="3"> <p>Wählen Sie im Feld <strong>[!UICONTROL Connection]</strong> die Verbindung, die Sie verwenden möchten, ausgewählt aus</p> <p>Anweisungen zum Verbinden Ihres [!DNL Microsoft Dynamics 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Microsoft Dynamics 365] mit [!DNL Workfront Fusion]</a> in diesem Artikel. </p> </li> 
     <li value="4"> <p>Klicken Sie auf <strong>[!UICONTROL Speichern]</strong>, um Ihren Webhook zu speichern und zum Modul zurückzukehren.</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datensätze beobachten (geplant)]

Dieses Modul für geplante Trigger führt ein Szenario aus, wenn ein Datensatz in dem angegebenen Objekt nach der letzten geplanten Ausführung dieses Szenarios erstellt oder aktualisiert wird.

Die Ausgabe des Moduls gibt an, ob der gefundene Datensatz neu oder aktualisiert ist. Wenn der Datensatz im Zeitraum hinzugefügt und aktualisiert wurde, wird er als neuer Datensatz zurückgegeben.

Dies geschieht in einem regelmäßig geplanten Intervall, das Sie angeben.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> "
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Microsoft Dynamics 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Microsoft Dynamics 365] mit [!DNL Workfront Fusion]</a> in diesem Artikel. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL include]</td> 
   <td>Wählen Sie aus, ob das Modul <strong>[!UICONTROL Nur neue Datensätze]</strong>, <strong>[!UICONTROL Nur aktualisierte Datensätze]</strong> oder <strong>[!UICONTROL Neue und aktualisierte Datensätze]</strong> überwachen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td>Wählen Sie den Datensatztyp [!UICONTROL Microsoft Dynamics 365] aus, den das Szenario überwachen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen. Die Felder sind je nach ausgewähltem Entitätstyp verfügbar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max. Einträge]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Datensatz erstellen]](#create-record)
* [[!UICONTROL Erstellen eines API-Aufrufs]](#make-an-api-call)
* [[!UICONTROL Datensatz löschen]](#delete-record)
* [[!UICONTROL Datensätze lesen]](#read-records)
* [[!UICONTROL Eintrag aktualisieren]](#update-record)


#### [!UICONTROL Datensatz erstellen]

Dieses Aktionsmodul erstellt eine Entität, z. B. einen Termin oder eine Aufgabe.

Sie geben Informationen zu der Entität an, die Sie erstellen möchten.

Das Modul gibt die ID der neuen Entität und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Microsoft Dynamics 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Microsoft Dynamics 365] mit [!DNL Workfront Fusion]</a> in diesem Artikel. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td>Wählen Sie den Entitätstyp aus, den das Modul erstellen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Felder zum Zuordnen auswählen]</td> 
   <td>Wählen Sie die Felder aus, für die Sie bei der Erstellung des Datensatzes Werte einbeziehen möchten. Die verfügbaren Felder hängen vom Entitätstyp ab.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL-Eigenschaftsfelder]</td> 
   <td> Dies sind die von Ihnen ausgewählten Felder. Geben Sie den Wert ein, den der Datensatz für eine bestimmte Eigenschaft haben soll. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datensatz löschen]

Dieses Aktionsmodul löscht eine Entität.

Geben Sie die ID der Entität an.

Das Modul gibt die ID der Entität und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Microsoft Dynamics 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Microsoft Dynamics 365] mit [!DNL Workfront Fusion]</a> in diesem Artikel. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td> <p>Wählen Sie den Typ der Entität aus, die das Modul löschen soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Geben Sie die eindeutige [!DNL Microsoft Dynamics 365]-ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen eines API-Aufrufs]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Microsoft Dynamics 365]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Microsoft Dynamics 365] nicht durchgeführt werden kann.

Das -Modul gibt Informationen über den Status-Code, die Kopfzeilen und den Hauptteil zurück. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Weitere Informationen finden Sie in der [!DNL Microsoft] Dokumentation zur Verwendung des [!DNL Dynamics 365 Customer Engagement Web API].

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Microsoft Dynamics 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Microsoft Dynamics 365] mit [!DNL Workfront Fusion]</a> in diesem Artikel. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Geben Sie einen Pfad relativ zu <code>&lt;Instance URL>/api/data/v9.1/</code> ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> <p>Für weitere Informationen in</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
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

#### [!UICONTROL Datensätze lesen]

Dieses Aktionsmodul liest Daten aus einer einzelnen Entität in [!DNL Microsoft Dynamics 365].

Geben Sie die ID der Entität an.

Das Modul gibt die ID der Entität und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Microsoft Dynamics 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Microsoft Dynamics 365] mit [!DNL Workfront Fusion]</a> in diesem Artikel. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td>Wählen Sie den Entitätstyp aus, den das Modul lesen soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die eindeutige [!DNL Microsoft Dynamics 365]-ID des Datensatzes ein, den das Modul lesen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eintrag aktualisieren]

Dieses Aktionsmodul aktualisiert eine Entität.

Geben Sie die ID der Entität an.

Das Modul gibt die ID des aktualisierten Datensatzes und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Microsoft Dynamics 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Microsoft Dynamics 365] mit [!DNL Workfront Fusion]</a> in diesem Artikel. </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td>Wählen Sie den Typ der Entität aus, die das Modul aktualisieren soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Felder zum Zuordnen auswählen]</td> 
   <td>Wählen Sie die Felder aus, für die Sie bei der Erstellung des Datensatzes Werte einbeziehen möchten. Die verfügbaren Felder hängen vom Entitätstyp ab.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL-Eigenschaftsfelder]</td> 
   <td>Dies sind die von Ihnen ausgewählten Felder. Geben Sie den Wert ein, den der Datensatz für eine bestimmte Eigenschaft haben soll.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die eindeutige [!DNL Microsoft Dynamics] 365-ID des Datensatzes ein, den Sie aktualisieren möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

#### [!UICONTROL Datensätze suchen]

Dieses Suchmodul sucht in einem -Objekt nach Datensätzen, [!DNL Microsoft Dynamics 365] mit der angegebenen Suchanfrage übereinstimmen. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
  <td> <p>Anweisungen zum Verbinden Ihres [!DNL Microsoft Dynamics 365]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Microsoft Dynamics 365] mit [!DNL Workfront Fusion]</a> in diesem Artikel. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entitätstyp]</td> 
   <td>Wählen Sie den Typ der Entität aus, die das Modul aktualisieren soll.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Wählen Sie den Filter aus, den Sie für diese Suche verwenden möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Standardfilter]</strong> </p> <p>Richten Sie den Filter ein, indem Sie ein Feld und einen Operator auswählen und den Wert eingeben oder zuordnen, nach dem Sie suchen möchten. Sie können AND- oder OR-Regeln für Ihren Filter verwenden.</p> </li> 
     <li> <p><strong>[!UICONTROL Abfragefunktionen]</strong> </p> <p>Geben Sie die Abfrage-Funktion der [!DNL Dynamics 365]-Web-API ein, die Sie für die Suche verwenden möchten. </p> <p>Weitere Informationen zu Abfragefunktionen finden Sie unter <a href="https://docs.microsoft.com/en-us/dynamics365/customer-engagement/web-api/queryfunctions?view=dynamics-ce-odata-9">Web-API-Abfragefunktionsreferenz</a> in der [!DNL Microsoft].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL sort]</td> 
   <td> <p>Geben Sie die Reihenfolge an, in der Elemente zurückgegeben werden. Sie können mehrere Sortierungen hinzufügen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL-Feld]</strong> </p> <p>Geben Sie das Feld an, nach dem Sie die Ergebnisse sortieren möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL Direction]</strong> </p> <p>Geben Sie die Sortierrichtung an (aufsteigend oder absteigend).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max. Einträge]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>
