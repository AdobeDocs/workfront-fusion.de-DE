---
title: Adobe Target-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die  [!DNL Adobe Target], as well as connect it to multiple third-party applications and services. [!DNL Adobe Target] -Module verwenden. Damit können Sie Datensätze erstellen, lesen, aktualisieren oder löschen, alle Datensätze eines bestimmten Typs auflisten, Datensätze anhand von von Ihnen angegebenen Kriterien suchen oder einen benutzerdefinierten API-Aufruf an die  [!DNL Adobe Target] -API durchführen.
author: Becky
feature: Workfront Fusion
exl-id: f3c1ed7b-b69b-478a-8240-1a2ab89e11e5
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1923'
ht-degree: 0%

---

# [!DNL Adobe Target] Module

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Adobe Target] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden. Mit [!DNL Adobe Target]-Modulen können Sie Datensätze erstellen, lesen, aktualisieren oder löschen, alle Datensätze eines bestimmten Typs auflisten, Datensätze anhand von von Ihnen angegebenen Kriterien suchen oder einen benutzerdefinierten API-Aufruf an die [!DNL Adobe Target]-API durchführen.


Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] Plan*</td>
      <td>
        <p>[!UICONTROL Pro] oder höher</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td>
      <td>
   <p>Aktuelle Lizenzanforderung: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] für Arbeitsautomatisierung und -integration] </p>
   </td>
    </tr>
    <tr>
      <td role="rowheader">Produkt</td>
      <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den [!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Adobe Workfront] verfügen, muss Ihr Unternehmen [!DNL Adobe Workfront Fusion] kaufen und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden. [!DNL Workfront Fusion] ist im [!UICONTROL Ultimate] [!DNL Workfront] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden.</p>
   </td>
    </tr>
    </tr>
  </tbody>
</table>


Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Voraussetzungen

Bevor Sie den [!DNL Adobe Target]-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein aktives [!DNL Adobe Target] verfügen.

## Adobe Target-API-Informationen

Der Adobe Target-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.7.33</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung zu [!DNL Adobe Target]

>[!IMPORTANT]
>
>Verbindungen, die nach dem 3. Juni 2024 erstellt wurden, erfordern eine Adobe Target-Server-zu-Server-Verbindung.
>
>* Vorhandene Service-Kontoverbindungen funktionieren weiterhin bis Januar 2025. Sie müssen Ihre Service-Kontoverbindungen bis Januar 2024 durch Adobe Target Server-zu-Server-Verbindungen ersetzen.
>* Sie müssen Entwickler für Ihr Unternehmen sein, um eine Adobe Target-Server-zu-Server-Verbindung erstellen zu können. Die Entwicklerrolle ist in der Adobe Admin Console festgelegt.

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe Target]:

1. Klicken Sie **[!UICONTROL Add]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>Wählen Sie aus, ob Sie eine Service-Konto- oder eine Adobe Target-Server-zu-Server-Verbindung erstellen.<p><b>WICHTIG</b>: Verbindungen, die nach dem 3. Juni 2024 erstellt wurden, erfordern eine Adobe Target-Server-zu-Server-Verbindung. Vorhandene Service-Kontoverbindungen funktionieren weiterhin bis Januar 2025. Sie müssen Ihre Service-Kontoverbindungen bis Januar 2024 durch Adobe Target Server-zu-Server-Verbindungen ersetzen.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Geben Sie Ihre [!DNL Adobe]-Client-ID ein. Diese finden Sie im [!UICONTROL Credentials details] Abschnitt der [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Geben Sie Ihr [!DNL Adobe]-Client-Geheimnis ein. Diese finden Sie im [!UICONTROL Credentials details] Abschnitt der [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Geben Sie die ID Ihres [!DNL Adobe] technischen Kontos ein. Diese finden Sie im [!UICONTROL Credentials details] Abschnitt der [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Geben Sie Ihre [!DNL Adobe] Organisations-ID ein. Diese finden Sie im [!UICONTROL Credentials details] Abschnitt der [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tenant]</td>
        <td>
          <p> Um Ihren Mandanten zu finden, melden Sie sich bei der [!DNL Adobe Experience Cloud] an, öffnen Sie [!DNL Target] und klicken Sie auf die [!DNL Target]. Verwenden Sie den Mandanten-ID-Wert, wie in der URL-Subdomain angegeben.</p>
          <p>Wenn beispielsweise Ihre URL bei der Anmeldung bei [!DNL Adobe Target] <code>&lt;https://mycompany.experiencecloud.adobe.com/...></code> ist, lautet Ihre Mandanten-ID „mycompany“.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td><code>ent_marketing_sdk</code> eingeben       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Geben Sie den privaten Schlüssel ein, der bei der Erstellung Ihrer Anmeldeinformationen im [!DNL Adobe Developer Console] generiert wurde. </p>
          <p>So extrahieren Sie Ihren privaten Schlüssel oder Ihr Zertifikat:</p>
          <ol>
            <li value="1">
              <p>Klicken Sie auf <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Wählen Sie den zu extrahierenden Dateityp aus.</p>
            </li>
            <li value="3">
              <p>Wählen Sie die Datei aus, die den privaten Schlüssel oder das Zertifikat enthält.</p>
            </li>
            <li value="4">
              <p>Geben Sie das Kennwort für die Datei ein.</p>
            </li>
            <li value="5">
              <p>Klicken Sie auf <b>[!UICONTROL Save]</b> , um die Datei zu extrahieren und zur Verbindungseinrichtung zurückzukehren.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu speichern und zum Modul zurückzukehren.

## [!DNL Adobe Target] Module und ihre Felder

Beim Konfigurieren [!DNL Adobe Target] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Adobe Target] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktionen](#actions)

* [Suchvorgänge](#searches)


### Aktionen

* [[!UICONTROL Create a record]](#create-a-record)

* [[!UICONTROL Make a custom API call]](#make-a-custom-api-call)

* [[!UICONTROL Delete a record]](#delete-a-record)

* [[!UICONTROL Read a record]](#read-a-record)

* [[!UICONTROL Update a record]](#update-a-record)


#### [!UICONTROL Create a record]

Dieses Aktionsmodul erstellt eine AB- oder XT-Aktivität, ein Angebot oder eine Zielgruppe.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Target] finden Sie unter <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Target]</a> in diesem Artikel.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>
      <p>Wählen Sie den Typ des Datensatzes aus, den Sie erstellen möchten.</p>
      <ul>
        <li>
        <b>property</b><p>Einzelheiten zu Feldern finden Sie unter <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Properties/operation/createProperty">Erstellen einer Eigenschaft</a> in der Adobe Target-API-Dokumentation.</p>
        </li>
        <li>
        <b>Angebotsempfehlung</b><p>Einzelheiten zu Feldern finden Sie unter <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Offers/operation/createOffer">Erstellen eines neuen Recs-Angebots</a> in der Adobe Target-API-Dokumentation.</p>
        </li>
        <li>
          <b>[!UICONTROL Offer JSON]</b>
          <p>Fahren Sie fort <a href="#offer-fields" class="MCXref xref" >Angebotsfelder</a>.</p>
        </li>
        <li>
          <b>[!UICONTROL Offer Content]</b>
          <p>Fahren Sie fort <a href="#offer-fields" class="MCXref xref" >Angebotsfelder</a>.</p>
        </li>
        <li>
        <b>Umgebung</b><p>Einzelheiten zu Feldern finden Sie unter <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Environments/operation/createEnvironment">Umgebung erstellen</a> in der Dokumentation zur Adobe Target-API.</p>
        </li>
        <li>
          <b>[!UICONTROL Audience]</b>
          <p>Einzelheiten zu Feldern finden Sie unter <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Audiences/operation/createAudience_1_1">Zielgruppe erstellen</a> in der Adobe Target-API-Dokumentation.</p>
        </li>
        <li>
          <b>[!UICONTROL AB Activity]</b>
          <p>Einzelheiten zu Feldern finden Sie unter <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">Erstellen einer AB-Aktivität</a> in der Adobe Target-API-Dokumentation.</p>
        </li>
        <li>
          <b>[!UICONTROL XT Activity]</b>
          <p>Fahren Sie mit <a href="#xt-activity-fields" class="MCXref xref" >XT-Aktivitätsfelder</a> fort.</p>
        </li>
        <li>
          <b>[!UICONTROL AP Activity]</b>
          <p>Einzelheiten zu Feldern finden Sie unter <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_2">Erstellen einer API-Aktivität</a> in der Dokumentation zur Adobe Target-API.</p>
        </li>
        <li>
          <b>[!UICONTROL Response Token]</b>
          <p>Einzelheiten zu Feldern finden Sie unter <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Response-tokens/operation/createResponseToken">Antwort-Token erstellen</a> in der Adobe Target-API-Dokumentation.</p>
        </li>
      </ul>
    </td>
  </tr>
</tbody>
</table>

<!--

##### AB Activity fields

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this activity. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>For each option that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the option across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the option. The name must be no more than 250 characters.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>Select or map the Offer associated with the option.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Mboxes]</td>
      <td>
        <p>For each Mbox that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selectors]</td>
      <td>
        <p>For each selector that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Selector]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>A list of locations on the page where the content offer is served. A location contains the following:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>Enter or map the ID of the experience</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map the name of the experience
</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>For each audience that you want to see the experience, click <b>[!UICONTROL Add item]</b> and enter the Audience ID.
</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>Enter or map the percentage of visitors that is allocated to the experience</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td><p>For details on metrics, see <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">Create AB activity</a> in the Adobe Target API documentation.</p> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>Enter or map an ID to identify this activity. You can choose this ID. This ID must not be the same as another activity, and can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>Enter or map the date and time to start the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>Enter or map the date and time to end the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Enter or map the state of the activity.</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Enter a number that defines the priority of the activity. Higher numbers have higher priority. This value must be between 0 and 999. The default value is 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>Enable this option to auto-allocate traffic. Auto-allocating sends more traffic to the more successful experience.</p>
        <p>Select or map the evaluation criteria by which to judge which experience is more successful.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Enter or map the workspace that the activity is associated with</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>For each property that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and select or map the property's ID.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>For each reporting audience that you want to add to the activity, click [!UICONTROL Add item] and enter the following information:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the Reporting Audience across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>Enter or map the Segment to be used in reporting</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the metric across API requests.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

-->

##### XT-Aktivitätsfelder

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Geben Sie einen Namen für diese Aktivität ein oder mappen Sie ihn. Der Name darf nicht länger 250 Zeichen sein.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>Klicken Sie für jede Option, die Sie der Aktivität hinzufügen möchten, auf <b>[!UICONTROL Add item]</b> und füllen Sie die folgenden Felder aus:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>Geben Sie eine Zeichenfolge ein, die verwendet werden soll, um die Option über API-Anfragen hinweg zu verfolgen, oder ordnen Sie sie zu.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Geben Sie einen Namen für die Option ein oder mappen Sie ihn. Der Name darf nicht länger 250 Zeichen sein.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>Wählen Sie das mit der Option verknüpfte Angebot aus oder ordnen Sie es zu.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Locations]</td>
      <td>
        <p>Klicken Sie für jede Mbox, die Sie der Aktivität hinzufügen möchten, auf <b>[!UICONTROL Add item]</b> und füllen Sie die folgenden Felder aus:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>Klicken Sie für jede Zielgruppe, die Sie der Mbox hinzufügen möchten, auf <b>[!UICONTROL Add item]</b> und wählen Sie die Zielgruppen-ID aus.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Geben Sie eine Zeichenfolge ein, die verwendet werden soll, um den Speicherort über API-Anfragen hinweg zu verfolgen, oder ordnen Sie sie zu.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Geben Sie einen Namen für den Speicherort ein oder mappen Sie ihn. Der Name darf nicht länger 250 Zeichen sein.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>Eine Liste der Stellen auf der Seite, an denen das Inhaltsangebot bereitgestellt wird. Ein Speicherort enthält Folgendes:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>ID des Erlebnisses eingeben oder zuordnen</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Namen des Erlebnisses eingeben oder zuordnen

</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>Klicken Sie für jede Zielgruppe, die Sie sehen möchten, auf <b>[!UICONTROL Add item]</b> und geben Sie die Zielgruppen-ID ein.

</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>Geben Sie den Prozentsatz der Besucher ein, der dem Erlebnis zugeordnet ist, oder ordnen Sie ihn zu</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>Geben Sie eine ID ein, um diese Aktivität zu identifizieren, oder mappen Sie sie. Sie können diese ID auswählen. Diese ID darf nicht mit einer anderen Aktivität identisch sein und darf nicht länger 250 Zeichen sein.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>Geben Sie Datum und Uhrzeit für den Beginn der Aktivität im <code>YYYY-MM-DD hh:mm:ss.z</code> Format ein oder mappen Sie sie.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>Geben Sie das Datum und die Uhrzeit für das Ende der Aktivität im Format <code>YYYY-MM-DD hh:mm:ss.z</code> ein oder mappen Sie sie.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Geben Sie den Status der Aktivität ein oder mappen Sie ihn.</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Geben Sie eine Zahl ein, die die Priorität der Aktivität definiert. Höhere Zahlen haben eine höhere Priorität. Dieser Wert muss zwischen 0 und 999 liegen. Der Standardwert ist 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>Aktivieren Sie diese Option, um Traffic automatisch zuzuordnen. Durch die automatische Zuordnung wird mehr Traffic an das erfolgreichere Erlebnis gesendet.</p>
        <p>Wählen Sie die Bewertungskriterien aus oder ordnen Sie sie zu, um zu beurteilen, welches Erlebnis erfolgreicher ist.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Den Arbeitsbereich eingeben oder zuordnen, mit dem die Aktivität verknüpft ist</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>Klicken Sie für jede Eigenschaft, die Sie der Aktivität hinzufügen möchten, auf <b>[!UICONTROL Add item]</b> und wählen Sie die ID der Eigenschaft aus oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>Klicken Sie für jede Reporting-Zielgruppe, die Sie der Aktivität hinzufügen möchten, auf [!UICONTROL Add item] und geben Sie die folgenden Informationen ein:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>Geben Sie eine Zeichenfolge ein, die zur Verfolgung der Reporting-Zielgruppe über API-Anfragen hinweg verwendet werden soll, oder ordnen Sie sie zu.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>Segment eingeben oder zuordnen, das im Reporting verwendet werden soll</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>Geben Sie eine Zeichenfolge ein, die zur Verfolgung der Metrik über API-Anfragen hinweg verwendet werden soll, oder ordnen Sie sie zu.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### Angebotsfelder

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Geben Sie einen Namen für diese Aktivität ein oder mappen Sie ihn. Der Name darf nicht länger 250 Zeichen sein.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content]</td>
      <td>
        <p>Geben Sie den Inhalt des Angebots ein, das dem Benutzer angezeigt werden soll, oder ordnen Sie ihn zu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Geben Sie die ID des mit dem Angebot verknüpften Arbeitsbereichs ein oder mappen Sie sie. Wenn das Feld leer gelassen wird, wird das Angebot mit dem Standardarbeitsbereich des Kontos verknüpft. Diese Funktion gilt nur für [!DNL Target] Premium-Konten.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Geben Sie das Datum und die Uhrzeit der Änderung dieses Angebots ein oder mappen Sie sie.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--

##### Audience fields

>[!NOTE]
>
>Audiences created through Workfront Fusion can only be edit in Fusion or through the API. They cannot be edited from within Target.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this audience. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Description]</td>
      <td>
        <p>Enter or map a description of this audience.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Origin]</td>
      <td>
        <p>Select whether this audience's origin is from Target or from the cloud.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Target Rule]</td>
      <td>
        <p>Enable the toggle to make rules AND, that is, all rules must be applied.</p>
        <p>For each rule that you want to apply to the audience, click <b>[!UICONTROL Add item]</b> and enter the JSON of the rule you want to apply. </p>
        <div class="example"><span class="autonumber"><span><b>Example: </b></span></span>
          <p>Example 1:</p>
          <p ><code>&lbrace;</code></p>
                    <p ><code>                "page": "url",</code>
                    </p>
                    <p><code>                "equals":&lbrack;</code>
                    </p>
                    <p ><code>                    "http://www.myhomepage.com/"</code>
                    </p>
                    <p><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;,</code>
                    </p>
                    <p>Example 2</p>
                    <p ><code>            &lbrace;</code>
                    </p>
                    <p><code>                "geo": "region",</code>
                    </p>
                    <p><code>                "matches": &lbrack;</code>
                    </p>
                    <p ><code>                    "california"</code>
                    </p>
                    <p ><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;</code>
                    </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Enter or map the ID of the workspace associated with the audience. If left blank, the offer is associated with the default workspace of the account. This functionality applies only to [!DNL Target Premium] accounts.</p>
      </td>
    </tr>
  </tbody>
</table>

-->

#### [!UICONTROL Make a custom API call]

Dieses Modul führt einen benutzerdefinierten API-Aufruf an die [!DNL Adobe Target]-API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Target] finden Sie unter <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Target]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL [!DNL Target] Basis-URL]</td>
      <td>Geben Sie Ihre [!DNL Target]-Basis-URL ein oder mappen Sie sie.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Pfad relativ zu {baseURL}/ eingeben</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungs- und X-API-Schlüssel-Header hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### [!UICONTROL Delete a record]

Dieses Aktionsmodul löscht eine einzelne AB-Aktivität, XT-Aktivität, ein einzelnes Angebot oder eine einzelne Audience.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Target] finden Sie unter <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Target]</a> in diesem Artikel.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Wählen Sie den Typ des Datensatzes aus, den Sie löschen möchten.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record ID]</td>
    <td>Geben Sie die ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Read a record]

Dieses Aktionsmodul ruft Daten für eine einzelne Aktivität, ein einzelnes Angebot, eine einzelne Zielgruppe, eine einzelne Eigenschaft oder einen einzelnen Bericht ab.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Target] finden Sie unter <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Target]</a> in diesem Artikel.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Wählen Sie den Datensatztyp aus, den Sie lesen möchten.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record ID]</td>
    <td>Geben Sie die ID des Datensatzes ein, den Sie lesen möchten, oder mappen Sie sie.</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Update a record]

Dieses Aktionsmodul aktualisiert einen Datensatz in Target.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Target] finden Sie unter <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Target]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>
        <p>Wählen Sie den Typ des Datensatzes aus, den Sie aktualisieren möchten.</p>
       </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Field names]</td>
      <td>Wählen Sie die Felder aus, die Sie aktualisieren möchten. Die Felder werden unten angezeigt.
          <p>Weitere Informationen zu Feldern finden Sie unter <a href="https://developer.adobe.com/target/administer/admin-api/">Adobe Target-API-Dokumentation</a>.</p>
      </td>
    </tr>
  </tbody>
</table>

### Suchvorgänge

* [[!UICONTROL Get records]](#get-records)

* [[!UICONTROL Search]](#search)


#### [!UICONTROL Get records]

Dieses Suchmodul ruft eine Liste von Datensätzen des ausgewählten Typs ab.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Target] finden Sie unter <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Target]</a> in diesem Artikel.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Wählen Sie den Typ des Datensatzes aus, den Sie aktualisieren möchten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Sort by]</td>
      <td>Klicken Sie für jedes Feld, nach dem Sie sortieren möchten, auf <b>[!UICONTROL Add item]</b> und wählen Sie das Feld aus und geben Sie an, ob die zurückgegebenen Ergebnisse aufsteigend oder absteigend sein sollen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts At]</td>
      <td>
        <p>Geben Sie das früheste Datum ein, für das Sie Datensätze abrufen möchten. </p>
        <p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends At]</td>
      <td>
        <p>Geben Sie das letzte Datum ein, für das Sie Datensätze abrufen möchten. </p>
        <p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang in [!DNL Adobe Workfront Fusion]</a>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Search]

Dieses Suchmodul sucht anhand der von Ihnen angegebenen Kriterien nach Aktivitäten, Angeboten oder Zielgruppen.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Adobe Target] finden Sie unter <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Erstellen einer Verbindung zu [!DNL Adobe Target]</a> in diesem Artikel.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Wählen Sie den Typ des Datensatzes aus, den Sie aktualisieren möchten.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Sort by]</td>
    <td>Klicken Sie für jedes Feld, nach dem Sie sortieren möchten, auf <b>[!UICONTROL Add item]</b> und wählen Sie das Feld aus und geben Sie an, ob die zurückgegebenen Ergebnisse aufsteigend oder absteigend sein sollen.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Search criteria]</td>
    <td>Wählen Sie für jede Regel, die Sie einrichten möchten, das Feld, den Operator und den Wert aus. Klicken Sie auf <b>[!UICONTROL Add AND rule]</b> , um zusätzliche Regeln zu erstellen.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Offset]</td>
    <td>
      <p>Geben Sie die Nummer der ersten Antwort ein, die das Modul zurückgeben soll. Die erste zurückgegebene Antwort hat einen Offset von <code>0</code>. Verwenden Sie dieses Feld in Kombination mit dem Feld [!UICONTROL Maximum number of returned results] , um die Antworten zu paginieren.</p>
      <p>Um beispielsweise die dritte Seite mit Antworten anzuzeigen, wenn jede Seite zehn Antworten enthält, setzen Sie [!UICONTROL Offset] auf 20 und [!UICONTROL Maximum number of returned] die Ergebnisse auf 10.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limit]</td>
    <td>
      <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie. Verwenden Sie dieses Feld in Kombination mit dem Feld [!UICONTROL Offset] , um die Antworten zu paginieren.</p>
      <p>Um beispielsweise die dritte Seite mit Antworten anzuzeigen, wenn jede Seite zehn Antworten enthält, setzen Sie [!UICONTROL Offset] auf 20 und [!UICONTROL Maximum number of returned] die Ergebnisse auf 10.</p>
    </td>
  </tr>
</tbody>
</table>
