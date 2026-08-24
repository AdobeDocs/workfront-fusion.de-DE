---
title: Azure DevOps-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Azure DevOps] verwenden, und diese mit verschiedenen Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
TQID: https://experienceleague.adobe.com/RFI6MFgF-C1Cnn0bvjOLVf3qahyRblEp4dtypNrxqzE
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 0b7298ce53bf59695ce52cb46cb8d25b6ede5fc8
workflow-type: tm+mt
source-wordcount: 2645
ht-degree: 24%

---

# [!DNL Azure DevOps]-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Azure DevOps] verwenden, und diese mit verschiedenen Anwendungen und Services von Drittanbietern verbinden.

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
   <p>Betriebsbasiert: Verfügbar für Organisationen mit betriebsbasierten Lizenzen</p>
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

Um [!DNL Azure DevOps] Module verwenden zu können, müssen Sie über ein [!DNL Azure] DevOps-Konto verfügen.

## [!DNL Azure DevOps] API-Informationen

Der Azure DevOps-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v5.1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.29.33</td> 
  </tr>
 </tbody> 
</table>

## Verbinden von [!DNL Azure DevOps] mit Workfront Fusion {#connect-azure-devops-to-workfront-fusion}

* [Verbinden von Azure DevOps mit Workfront Fusion mithilfe von EntraApp](#connect-azure-devops-to-workfront-fusion-using-entraapp)
* [Verbinden von Azure DevOps mit Workfront Fusion mithilfe eines Service-Prinzipals](#connect-azure-devops-to-workfront-fusion-using-a-service-principal)

### Verbinden von Azure DevOps mit Workfront Fusion mithilfe von EntraApp

1. Fügen Sie Ihrem Szenario ein [!DNL Azure DevOps] hinzu.
1. Klicken Sie **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Wählen [!UICONTROL  im Feld ] den Verbindungstyp aus, den Sie verwenden möchten.

   >[!NOTE]
   >
   >Mit der [!UICONTROL [!DNL Azure DevOps] (EntraApp] können Sie alle Bereiche für die Verbindung anfordern.

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto">
      <tr>
            <td>[!UICONTROL Verbindungsname]</td>
            <td>Geben Sie einen Namen für die Verbindung ein, die Sie erstellen.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Organisation]</td>
            <td>Geben Sie den Namen der Organisation ein, unter der Sie Ihr [!DNL Azure DevOps]-Programm erstellt haben.</td>
      </tr>
      <tr>
            <td>[!UICONTROL App-ID]</td>
            <td>Geben Sie die ID der DevOps-Anwendung ein, mit der Sie eine Verbindung herstellen.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Client-Geheimnis]</td>
            <td>Geben Sie das Client-Geheimnis für die DevOps-Anwendungen ein, mit denen Sie eine Verbindung herstellen.</td>
      </tr>
      <tr>
            <td>[!UICONTROL, alle Bereiche anfordern]</td>
            <td>Wenn Sie den Verbindungstyp [!DNL Azure DevOps] (EntraApp) verwenden, aktivieren Sie diese Option, um alle Bereiche für die Verbindung anzufordern.</td>
      </tr>
   </table>

1. Um eine Azure DevOps-App-ID oder einen geheimen Client-Schlüssel einzugeben, klicken Sie auf <b>Erweiterte Einstellungen anzeigen</b> und geben Sie diese in die sich öffnenden Felder ein.
1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Einrichtung der Verbindung abzuschließen und mit der Erstellung Ihres Szenarios fortzufahren.

### Verbinden von Azure DevOps mit Workfront Fusion mithilfe eines Service-Prinzipals

Sie können eine Verbindung erstellen, die einen Service-Prinzipal (eine Anwendungs-API-Verbindung) anstelle eines persönlichen Kontos verwendet. Dies ist nützlich, wenn die Verbindung als Anwendung oder Service-Identität und nicht als eine bestimmte Person ausgeführt werden soll. Dies kann nützlich sein, damit die Integration nicht unterbrochen wird, wenn diese Person beispielsweise das Unternehmen verlässt oder ihr Passwort ändert.

Dieser Verbindungstyp ist für alle Azure DevOps-Module verfügbar.

>[!NOTE]
>
>Die Authentifizierung des Service-Prinzipals unterstützt nicht alle Azure DevOps-Funktionen. Für eine geringe Anzahl von Aktionen auf Admin-Ebene, z. B. die Verwaltung von Benutzerlizenzen, ist weiterhin eine persönliche Kontoverbindung erforderlich. Verwenden Sie die Authentifizierung des Service-Prinzipals, wenn Sie dies nur für Arbeitselemente, Pinnwände, Repos oder Pipelines benötigen.

* [Voraussetzungen für das Verbinden von Azure DevOps mit Workfront Fusion mithilfe eines Service-Prinzipals](#prerequisites-to-connecting-azure-devops-to-workfront-fusion-using-a-service-principal)
* [Erstellen der App-Registrierung in der Microsoft Entra ID](#create-the-app-registration-in-microsoft-entra-id)
* [Erstellen von Client-Geheimnissen](#create-a-client-secret)
* [Erfassen von Verbindungsdetails](#collect-your-connection-details)
* [Hinzufügen des Service-Prinzipals zu Ihrer Azure DevOps-Organisation](#add-the-service-principal-to-your-azure-devops-organization)
* [Erstellen der Verbindung](#create-the-connection)

#### Voraussetzungen für das Verbinden von Azure DevOps mit Workfront Fusion mithilfe eines Service-Prinzipals

Um diese Verbindung zu erstellen, benötigen Sie Folgendes:

* **Globaler Administrator** oder **Anwendungsadministrator** Zugriff auf die Microsoft Entra ID, um die App zu registrieren. Wenn Sie nicht über diesen Zugriff verfügen, bitten Sie jemanden in Ihrem IT- oder Identitäts-Team, diesen Schritt für Sie auszuführen.
* **Projektsammlungs-Administrator** greifen Sie in Ihrer Azure DevOps-Organisation zu, um den Service-Prinzipal als Mitglied hinzuzufügen. Häufig handelt es sich dabei um eine andere Person als die Person, die die Microsoft Entra ID verwaltet.
* Der Name Ihres Azure DevOps-Unternehmens. Sie finden diese in Ihrer Azure DevOps-URL: `dev.azure.com/<your organization name>`.

#### Erstellen der App-Registrierung in der Microsoft Entra ID

1. Melden Sie sich beim [!DNL Microsoft Entra] Admin Center an.
1. Navigieren Sie **[!UICONTROL App-Registrierungen]** > **[!UICONTROL Neue Registrierung]**.
1. Geben Sie der App einen klaren, erkennbaren Namen. Beispiel: `Workfront Fusion Azure DevOps Integration`.
1. Lassen Sie **[!UICONTROL Umleitungs-URI]** leer. Für diese Verbindung ist keine Anmeldung über einen Browser erforderlich.
1. Wählen Sie **[!UICONTROL Registrieren]** aus.
1. Fahren Sie mit [Erstellen eines Client-Geheimnisses](#create-a-client-secret) fort.

#### Erstellen von Client-Geheimnissen

1. Navigieren Sie in Ihrer neuen App-Registrierung zu **[!UICONTROL Zertifikate und Geheimnisse]**.
1. Wählen Sie **[!UICONTROL Neues Client-Geheimnis]**, fügen Sie eine Beschreibung hinzu und wählen Sie einen Ablaufzeitraum aus.
1. Bestätigen Sie die Angaben mithilfe der Schaltfläche **[!UICONTROL Hinzufügen]**.
1. Kopieren Sie den (Wert **[!UICONTROL der geheimen Daten]**. Er wird nur einmal angezeigt. Wenn Sie die Seite verlassen möchten, bevor Sie sie kopieren, müssen Sie eine neue erstellen.
1. Fahren Sie [Verbindungsdetails erfassen](#collect-your-connection-details) fort.

#### Erfassen von Verbindungsdetails

1. Beachten Sie auf der Seite **[!UICONTROL Übersicht]** der App-Registrierung die folgenden Werte. Diese werden beim Erstellen der Verbindung im Modul eingegeben.

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[!UICONTROL Mandanten-ID]</td>
      <td>Auf der Seite Überblick mit der Beschriftung <b>Verzeichnis (Mandanten-ID</b>.</td>
      </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Client-ID]</td>
      <td>Auf der Seite Überblick mit der Bezeichnung <b>Anwendungs-(Client-)ID</b>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
      <td>Der Wert, den Sie in "<a href="#create-a-client-secret" class="MCXref xref"> eines Client-Geheimnisses“ kopiert </a>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Organisation]</td>
      <td>Ihr Azure DevOps-Organisationsname. Wenn Ihre URL beispielsweise <code>dev.azure.com/yourorg</code> ist, geben Sie <code>yourorg</code> ein.</td>
     </tr>
    </tbody>
   </table>

   >[!NOTE]
   >
   >Sie können den Bereich (API-Berechtigungen) **App** Registrierung überspringen. Wenn Sie dort Azure DevOps hinzufügen, sind nur **Delegierte Berechtigungen** verfügbar. **Anwendungsberechtigungen** werden ausgegraut angezeigt. Dies ist zu erwarten, da Azure DevOps die Gewährung von Zugriff auf diese Weise nicht unterstützt. Stattdessen wird der Zugriff direkt innerhalb von Azure DevOps gewährt, im nächsten Teil.

1. Fahren Sie fort [Service-Prinzipal zu Ihrer Azure DevOps-Organisation hinzufügen](#add-the-service-principal-to-your-azure-devops-organization).

#### Hinzufügen des Service-Prinzipals zu Ihrer Azure DevOps-Organisation

Durch die Registrierung der App in der Microsoft Entra ID wird nur deren Identität erstellt. Sie gewährt der App noch keinen Zugriff auf Ihre Azure DevOps-Daten. Durch dieses Verfahren wird diesem Zugriff gewährt.

1. Melden Sie sich bei Ihrer Azure DevOps-Organisation unter `dev.azure.com/<your organization name>` an.
1. Wählen Sie **[!UICONTROL Organisationseinstellungen]** unten links aus und klicken Sie auf **[!UICONTROL Benutzer]**.
1. Wählen Sie **[!UICONTROL Benutzer hinzufügen]** aus.
1. Suchen Sie im Suchfeld nach dem Anzeigenamen der App, d. h. dem Namen, den Sie bei der Registrierung der App angegeben haben. Suchen Sie nicht nach der Client-ID.
1. Zugriffsebene auswählen:

   * **[!UICONTROL Standard]** reicht in der Regel aus, um Arbeitselemente, Pinnwände und Repos zu lesen und zu schreiben.
   * Wenn Ihr Workflow im Rahmen der Einrichtung verfügbare Prozesse wie Agile, Scrum oder benutzerdefinierte Vorlagen durchsuchen muss, fügen Sie den Service-Prinzipal stattdessen der Gruppe **[!UICONTROL Projektsammlungs-]**&quot; hinzu. Dies ist eine umfassendere Zugriffsberechtigung, gewähren Sie sie also nur, wenn Sie diese Funktion benötigen.

1. Weisen Sie den Service-Prinzipal gemäß den üblichen Zugriffsverfahren Ihres Unternehmens dem jeweiligen Projekt bzw. den Projekten zu, das bzw. die er benötigt.
1. Bestätigen Sie die Angaben mithilfe der Schaltfläche **[!UICONTROL Hinzufügen]**.
1. Fahren Sie [Verbindung erstellen](#create-the-connection) fort.

#### Erstellen der Verbindung

1. Wählen Sie im Bildschirm zur Verbindungseinrichtung des Moduls den Verbindungstyp **[!UICONTROL Service-]**) aus.
1. Geben Sie Folgendes ein:

   * [!UICONTROL Mandanten-ID]
   * [!UICONTROL Client-ID]
   * [!UICONTROL Client Secret] (Client-Geheimnis)
   * [!UICONTROL Organisation]

1. Speichern Sie die Verbindung.

   Wenn alles korrekt eingerichtet ist, wird die Verbindung erfolgreich validiert.

## [!UICONTROL Azure DevOps]-Module und ihre Felder

Beim Konfigurieren von [!DNL Azure DevOps]-Modulen werden in Workfront Fusion die unten aufgeführten Felder angezeigt. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere [!DNL Azure DevOps]-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

#### [!UICONTROL Auf Arbeitselemente ]

Dieses Instant Trigger-Modul führt ein Szenario aus, wenn ein Datensatz in [!UICONTROL Azure DevOps} hinzugefügt, aktualisiert oder gelöscht ].

Das Modul gibt alle Standardfelder zurück, die mit dem Eintrag verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Webhook für das Modul auswählen oder hinzufügen.</p> <p>Weitere Informationen zu Webhooks in Trigger-Modulen finden Sie unter <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Instant Trigger (Webhooks)</a>.</p> <p>Informationen zum Erstellen eines Webhooks finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [Eintrag erstellen](#create-a-record)
* [Benutzerdefinierter API-Aufruf](#custom-api-call)
* [Herunterladen eines Anhangs](#download-an-attachment)
* [Arbeitselemente verknüpfen](#link-work-items)
* [Datensatz lesen](#read-record)
* [Aktualisieren eines Arbeitselements](#update-a-work-item)
* [[!UICONTROL Anlage hochladen]](#upload-an-attachment)

#### [!UICONTROL Eintrag erstellen]

Dieses Aktionsmodul erstellt ein neues Projekt oder Arbeitselement.

Das Modul gibt die Objekt-ID für das neu erstellte Arbeitselement oder die URL und den Status-Code eines neu erstellten Projekts aus.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eintragstyp]</td> 
   <td> <p>Wählen Sie aus, ob Sie ein Arbeitselement oder ein Projekt erstellen möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL-Projekt]</strong> </p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Name]</strong>: Geben Sie einen Namen für das neue Projekt ein oder ordnen Sie ihn ihm zu.</p> </li> 
       <li> <p><strong>[!UICONTROL Description]</strong>: Geben Sie eine Beschreibung für das neue Projekt ein oder ordnen Sie sie zu. </p> </li> 
       <li> <p><strong>[!UICONTROL Sichtbarkeit]</strong>: Wählen Sie aus, ob Ihr Projekt öffentlich oder privat sein soll. Benutzer müssen bei Ihrer Organisation angemeldet sein und Zugriff auf das Projekt erhalten haben, damit sie mit einem privaten Projekt interagieren können. Öffentliche Projekte sind für Benutzer sichtbar, die nicht bei Ihrer Organisation angemeldet sind.</p> </li> 
       <li> <p><strong>[!UICONTROL Versionskontrolle]</strong>: Wählen Sie aus, ob das Projekt [!DNL Git] oder [!UICONTROL Team Foundation Version Control (TFCV)] für die Versionskontrolle verwenden soll.</p> </li> 
       <li> <p><strong>[!UICONTROL Arbeitselementprozess]</strong>: Wählen Sie den Arbeitsprozess aus, den Sie für das Projekt verwenden möchten. Die Optionen sind [!UICONTROL Basic], [!UICONTROL Scrum], [!UICONTROL Capability Maturity Model Integration (CMMI)] und [!UICONTROL Agile].</p> <p>Weitere Informationen zu [!DNL Azure DevOps]-Prozessen finden Sie unter <a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&amp;tabs=basic-process">Standardprozesse und Prozessvorlagen</a> in der [!DNL Azure DevOps].</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Arbeitselement]</strong> </p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Project]</strong>: Wählen Sie das Projekt aus, in dem Sie das Arbeitselement erstellen möchten.</p> </li> 
       <li> <p><strong>[!UICONTROL Arbeitsaufgabentyp]</strong>: Wählen Sie den Typ des Arbeitselements, das Sie erstellen möchten.</p> </li> 
       <li> <p><strong>[!UICONTROL Andere Felder]</strong>: Geben Sie in diesen Feldern den Wert ein, den das Arbeitselement für eine bestimmte Eigenschaft haben soll. Die verfügbaren Felder hängen vom Typ des Arbeitselements ab.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Azure DevOps]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, was über die anderen [!DNL Azure DevOps]-Module nicht möglich ist.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Basis-URL]</td> 
   <td> <p>Wählen Sie die Basis-URL aus, mit der Sie eine Verbindung zu Ihrem [!DNL Azure DevOps]-Konto herstellen, oder ordnen Sie sie zu</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL relative URL]</td> 
   <td> <p>Geben Sie die relative URL ein, mit der Sie sich für diesen API-Aufruf verbinden möchten.</p> <p><b>Beispiel: </b><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL API-Version]</td> 
   <td>Wählen Sie die Version der [!DNL Azure DevOps]-API aus, mit der Sie sich für diesen API-Aufruf verbinden möchten, oder ordnen Sie sie zu. Wenn keine Version ausgewählt ist, stellt Workfront Fusion eine Verbindung zu [!DNL Azure DevOps] API-Version 5.1 her.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Header]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p>Fügen Sie den Textinhalt für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrem JSON-Objekt verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Anlage herunterladen]

Dieses Aktionsmodul lädt eine Anlage herunter.

Das -Modul gibt den Dateiinhalt des Anhangs zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Anhang URL]</td> 
   <td> <p>Geben Sie die URL des Anhangs ein, den Sie herunterladen möchten, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Arbeitselemente verknüpfen]

Dieses Aktionsmodul verknüpft zwei Arbeitselemente und definiert die Beziehung zwischen ihnen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitselement-ID]</td> 
   <td>Geben Sie die ID des Hauptarbeitselements ein, mit dem Sie ein anderes Arbeitselement verknüpfen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID des verknüpften Arbeitselements]</td> 
   <td>Geben Sie die ID des Arbeitselements ein, das Sie mit dem Hauptarbeitselement verknüpfen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Link-Typ]</td> 
   <td> <p>Definieren Sie die Beziehung zwischen den Arbeitselementen, die Sie verknüpfen möchten.</p> <p>Weitere Informationen finden Sie <a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops">Referenzhandbuch für Link-Typen</a> in der [!UICONTROL Azure DevOps]-Dokumentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kommentar]</td> 
   <td>Geben Sie den Text eines Kommentars ein oder mappen Sie ihn. Dies ist nützlich, um die Begründung oder Absicht des Links zu erklären.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datensatz lesen]

Dieses Aktionsmodul liest Daten aus einem einzelnen Datensatz in [!DNL Azure DevOps].

Geben Sie die ID des Eintrags an.

Das Modul gibt daraufhin die ID des Eintrags und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Eintragstyp]</td> 
   <td> <p>Auswählen, ob ein Projekt oder ein Arbeitselement gelesen werden soll</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong>: Wählen Sie das Projekt aus, das Sie lesen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL Arbeitselement]</strong>: Wählen Sie das Projekt aus, das das Arbeitselement enthält, das Sie lesen möchten, und wählen Sie dann den Arbeitselementtyp aus.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen. Die verfügbaren Felder hängen vom Typ des Arbeitselements ab.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Geben Sie die ID des Datensatzes ein, den Sie lesen möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Arbeitselement aktualisieren]

Dieses Aktionsmodul aktualisiert ein vorhandenes Arbeitselement mithilfe seiner ID.

Das Modul gibt die ID des aktualisierten Arbeitselements zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt]</td> 
   <td>Wählen Sie das Projekt aus, das das Arbeitselement enthält, das Sie aktualisieren möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsaufgabentyp]</td> 
   <td> <p>Wählen Sie den Typ des Arbeitselements aus, das Sie aktualisieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Andere Felder]</td> 
   <td>Geben Sie in jedem dieser Felder den Wert ein, den das Arbeitselement für eine bestimmte Eigenschaft haben soll. Die verfügbaren Felder hängen vom Typ des Arbeitselements ab.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitselement-ID]</td> 
   <td>Geben Sie die ID des Arbeitselements ein, das Sie aktualisieren möchten, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Anlage hochladen]

Dieses Aktionsmodul lädt eine Datei hoch und hängt sie an ein Arbeitselement an.

Das Modul gibt die Anlagen-ID und eine Download-URL für den Anhang zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt] </td> 
   <td> <p>Wählen Sie das Projekt aus, in das Sie eine Anlage hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitselement-ID]</td> 
   <td> <p>Geben Sie die ID des Arbeitselements ein, in das Sie eine Anlage hochladen möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kommentar]</td> 
   <td>Geben Sie den Text eines Kommentars ein, den Sie zum hochgeladenen Anhang hinzufügen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Quelldatei] </td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder geben Sie den Namen und den Inhalt der Quelldatei ein oder mappen Sie ihn.</td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

#### [!UICONTROL Arbeitselemente auflisten]

Dieses Aktionsmodul ruft alle Arbeitselemente eines bestimmten Typs in einem [!DNL Azure DevOps] Projekt ab.

Das Modul gibt die ID des Hauptarbeitselements und alle zugehörigen Felder sowie alle benutzerdefinierten Felder und Werte zurück, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Azure DevOps]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Azure DevOps] mit [!UICONTROL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Projekt]</td> 
   <td>Wählen Sie das Projekt aus, aus dem Sie Arbeitselemente abrufen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsaufgabentyp]</td> 
   <td> <p>Wählen Sie den Typ des Arbeitselements, das Sie abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td>Wählen Sie die Eigenschaften aus, die in der Modulausgabe angezeigt werden sollen. Die verfügbaren Felder hängen vom Typ des Arbeitselements ab, das Sie abrufen möchten. Sie müssen mindestens eine Eigenschaft auswählen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Beschränkung]</td> 
   <td>Geben Sie die maximale Anzahl von Arbeitselementen ein, die Workfront Fusion während eines Ausführungszyklus zurückgibt, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>
