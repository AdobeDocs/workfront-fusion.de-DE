---
title: Adobe Campaign v7/v8-Module
description: Mit den  [!DNL Adobe Campaign] -Modulen können Sie ein auf  [!DNL Adobe Workfront Fusion]  Ereignissen in Ihrem  [!DNL Adobe Campaign] -Konto basierendes Szenario starten, Vereinbarungen und andere Datensätze erstellen, lesen oder aktualisieren, mit von Ihnen festgelegten Kriterien nach Datensätzen suchen und Dokumente hochladen.
author: Becky
feature: Workfront Fusion
exl-id: 9fdff26c-c7c0-4eb8-a36f-4aeaf432b333
source-git-commit: 9bcda2cc1a5f483a8db49eae8e4f3d10f0d39c67
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# [!DNL Adobe Campaign]

Mit den [!DNL Adobe Campaign]-Modulen können Sie ein [!DNL Adobe Workfront Fusion] Szenario auf der Grundlage von Ereignissen in Ihrem [!DNL Adobe Campaign v7/v8]-Konto starten, Datensätze erstellen, lesen oder aktualisieren, mit von Ihnen festgelegten Kriterien nach Datensätzen suchen und benutzerdefinierte API-Aufrufe durchführen.

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
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung.</p>
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

Fügen Sie die Fusion-IP-Adressen zu [!DNL Adobe Campaign] hinzu.

* Anweisungen zum Hinzufügen von IP-Adressen zu Ihrer Campaign-Zulassungsliste auf die Zulassungsliste setzte finden Sie unter [Hinzufügen von IP-Adressen ](https://experienceleague.adobe.com/en/docs/control-panel/using/sftp-management/ip-range-allow-listing#adding-ip-addresses-allow-list) der Adobe Campaign-Dokumentation.
* Eine Liste der IP-Adressen, die der Zulassungsliste auf die Zulassungsliste setzte hinzugefügt werden können, finden Sie [Konfigurieren von IP-Adressen für Fusion in der -](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md).

## Adobe Campaign-API-Informationen

Der Adobe Campaign-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.7.22</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Adobe Campaign] mit [!DNL Adobe Workfront Fusion] verbinden

>[!IMPORTANT]
>
>Es wird dringend empfohlen, eine Server-zu-Server-Verbindung zu erstellen. Adobe Campaign hat seine API so aktualisiert, dass nur Server-zu-Server-Verbindungen akzeptiert werden. Wenn Sie eine Verbindung zu Campaign Version 8 oder höher herstellen, **müssen** eine Server-zu-Server-Verbindung erstellen.
>
>Weitere Informationen zu den neuen Verbindungsanforderungen von Campaign finden Sie unter [Migration technischer Campaign-Benutzerinnen und -Benutzer zu Adobe Developer Console](https://experienceleague.adobe.com/docs/campaign/technotes-ac/tn-new/ims-migration.html) in der Campaign-Dokumentation.

1. Klicken Sie in einem beliebigen [!DNL Adobe Campaign] auf **[!UICONTROL Add]** neben dem Feld [!UICONTROL Connection] .
1. Füllen Sie die folgenden Felder aus:
   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>Wählen Sie aus, ob Sie eine Basisverbindung oder eine Server-zu-Server-Verbindung erstellen.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Geben Sie einen Namen für diese Verbindung ein.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Base URL]</td>
          <td>Geben Sie die Basis-URL ein, mit der Sie eine Verbindung zu Ihrer [!DNL Adobe Campaign]-Instanz herstellen.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Username]</td>
          <td>Wenn Sie eine Basisverbindung erstellen, geben Sie Ihren Adobe Campaign-Benutzernamen ein.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Password]</td>
          <td>Wenn Sie eine Basisverbindung erstellen, geben Sie Ihr Adobe Campaign-Kennwort ein.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Wenn Sie eine Server-zu-Server-Verbindung erstellen, geben Sie Ihre [!DNL Adobe] [!UICONTROL Client ID] ein. Diese finden Sie im [!UICONTROL Credentials details] Abschnitt der [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Wenn Sie eine Server-zu-Server-Verbindung erstellen, geben Sie Ihre [!DNL Adobe] [!UICONTROL Client Secret] ein. Diese finden Sie im [!UICONTROL Credentials details] Abschnitt der [!DNL Adobe Developer Console].
        </tr>
     </tbody>
    </table>
1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

## [!DNL Adobe Campaign] Module und ihre Felder

Beim Konfigurieren [!DNL Adobe Campaign] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Adobe Campaign] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<!--* [Triggers](#triggers)-->
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

<!--### Triggers

#### [!UICONTROL Watch records]

This scheduled trigger module starts a scenario when a record changes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Campaign], see <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Create a connection to [!DNL Adobe Campaign]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Select whether you want to watch for new records, updated records, or both.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Select the resource that you want to watch for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output]</td> 
   <td>Select the fields that you want to include in the module's output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>For each custom field that you want to include in output, click <b>[!UICONTROL Add]</b> and enter the name of the custom field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>-->


### Aktionen

* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Delete a record]](#delete-record)
* [[!UICONTROL Make a custom API call]](#make-a-custom-api-call)
* [[!UICONTROL Perform an action]](#perform-an-action)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Subscribe or unsubscribe]](#subscribe-or-unsubscribe)
* [[!UICONTROL Update a record]](#update-record)

#### [!UICONTROL Create a record]

Dieses Aktionsmodul erstellt einen neuen Datensatz in [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Campaign]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Wählen Sie den Typ [!DNL Adobe Campaign] Datensatzes aus, den Sie erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields] </td> 
   <td>Wählen Sie die Felder aus, für die Sie Werte festlegen möchten, wenn der Datensatz erstellt wird, und füllen Sie dann die Werte für diese Felder aus. Felder variieren je nach ausgewähltem Datensatztyp.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> Klicken Sie für jedes benutzerdefinierte Feld, das Sie zum neuen Datensatz hinzufügen möchten, auf <b>[!UICONTROL Add item]</b> und geben Sie den Namen und den Wert des Felds ein oder mappen Sie ihn. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Record]

Dieses Aktionsmodul löscht einen einzelnen Datensatz aus [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Campaign]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Wählen Sie den Ressourcentyp aus, den Sie löschen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID der Ressource ein, die Sie löschen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make a custom API call]

Dieses Modul führt einen benutzerdefinierten API-Aufruf an die [!DNL Adobe Campaign]-API durch

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Campaign]</a> in diesem Artikel.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Action]</td>
      <td><p>Wählen Sie die Aktion aus, die der API-Aufruf ausführen soll.</p>
      <p>[!UICONTROL Execute query]</p>
      <p>[!UICONTROL Write]</p>
      <p>[!UICONTROL Get entity if more recent]</p>
      <p>[!UICONTROL Select all]</p>
      <p>[!UICONTROL Push event]</p>
    </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Fügt automatisch die Kopfzeile des [!UICONTROL x-security]-Tokens hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL XML Body]</td>
   <td> <p>Fügen Sie den Hauptteil des API-Aufrufs in XML hinzu, ohne das Sitzungselement zu verwenden. </td>     </tr>
  </tbody>
</table>


#### [!UICONTROL Perform an action]

Dieses Aktionsmodul führt eine ausgewählte Aktion für ein Objekt in der [!DNL Adobe Campaign]-API aus.

Informationen zu bestimmten Aktionen und Feldern finden Sie unter [[!DNL Adobe Campaign]  - API-Dokumentation](https://experienceleague.adobe.com/developer/campaign-api/api/p-14.html).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Campaign]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td><p>Wählen Sie die Aktion aus, die mit dem Objekt durchgeführt werden soll.</p>
   <ul>
   <li><p><b>[!DNL List]</b></p><p> Informationen zu verfügbaren Feldern finden Sie unter <a href="#search" class="MCXref xref" >[!UICONTROL Search]</a> in diesem Artikel. </p></li>
     <li><p><b>[!UICONTROL Get]</b></p><p> Informationen zu verfügbaren Feldern finden Sie unter <a href="#search" class="MCXref xref" >[!UICONTROL Search]</a> in diesem Artikel. </p></li> 
   <li><p><b>[!UICONTROL Create]</b></p><p> Informationen zu verfügbaren Feldern finden Sie unter <a href="#create-a-record" class="MCXref xref" >[!UICONTROL Create a record]</a> in diesem Artikel. </p></li>
   <li><p><b>[!UICONTROL Update]</b></p><p> Informationen zu verfügbaren Feldern finden Sie unter <a href="#update-record" class="MCXref xref" >[!UICONTROL Update a record]</a> in diesem Artikel. </p></li>
   <li><p><b>[!UICONTROL Delete]</b></p><p> Informationen zu verfügbaren Feldern finden Sie unter <a href="#delete-record" class="MCXref xref" >[!UICONTROL Delete a record]</a> in diesem Artikel. </p></li>
   </ul>
   </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Dieses Aktionsmodul liest einen Datensatz aus [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Campaign]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Wählen Sie den Typ [!DNL Adobe Campaign] Datensatzes aus, den Sie lesen möchten.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>Geben Sie die Zuordnungs-ID des Datensatzes ein, den Sie lesen möchten.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output] </td> 
   <td>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>Klicken Sie für jedes benutzerdefinierte Feld, das Sie in die Ausgabe aufnehmen möchten, auf <b>[!UICONTROL Add]</b> und geben Sie den Namen des benutzerdefinierten Felds ein.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Subscribe or unsubscribe]

Dieses Aktionsmodul meldet eine Benutzerin bzw. einen Benutzer an oder ab für einen Informations-Service.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Campaign]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe or unsubscribe]</td> 
   <td>Wählen Sie aus, ob Sie den Informations-Service abonnieren oder abmelden möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Service name]</td> 
   <td>Wählen Sie den Service aus, den Sie abonnieren oder abbestellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recipient email address] </td> 
   <td>Geben Sie die E-Mail-Adresse des Benutzers ein, den Sie für den Informations-Service abonnieren oder abmelden möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update record]

Dieses Aktionsmodul aktualisiert einen einzelnen Datensatz in [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Campaign]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Wählen Sie den Typ [!DNL Adobe Campaign] Datensatzes aus, den Sie erstellen möchten.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>Geben Sie die Zuordnungs-ID des Datensatzes ein, den Sie aktualisieren möchten.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Fields] </td> 
   <td>Wählen Sie die Felder aus, für die Sie Werte aktualisieren möchten, und füllen Sie dann die Werte für diese Felder aus. Felder variieren je nach ausgewähltem Datensatztyp.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> Klicken Sie für jedes benutzerdefinierte Feld, das Sie aktualisieren möchten, auf <b>[!UICONTROL Add item]</b> und geben Sie den Namen und den Wert des Felds ein oder ordnen Sie ihn zu. </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

#### [!UICONTROL Search]

Dieses Suchmodul gibt Datensätze basierend auf den angegebenen Kriterien zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Campaign] finden Sie unter <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Campaign]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Wählen Sie den Typ [!DNL Adobe Campaign] Datensatzes aus, den Sie erstellen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>Geben Sie die Felder und Werte ein, die die Suche verwenden soll. Felder hängen von der ausgewählten Ressource ab.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>
