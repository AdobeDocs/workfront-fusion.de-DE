---
title: Microsoft Dynamics 365 Finance and Operations-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Microsoft Dynamics 365 Finance and Operations verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 96f8d4f1-f97b-4da8-8d82-83cccb54ec68
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1142'
ht-degree: 1%

---

# [!DNL Microsoft Dynamics 365 Finance and Operations modules]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Microsoft Dynamics 365] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

>[!NOTE]
>
>Der [!DNL Microsoft Dynamics 365 Finance and Operations]-Connector unterstützt keine [!DNL Dynamics 365].
>
>Informationen zu Microsoft Dynamics 365-Modulen finden Sie [[!DNL Microsoft Dynamics 365 modules]](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).



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



## Verbindung erstellen

So erstellen Sie eine Verbindung für Ihre Microsoft Dynamics 365 Finance and Operations-Module:

1. Klicken Sie in einem beliebigen Microsoft Dynamics 365-Finanz- und Betriebsmodul **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Verbindungstyp]</td>
        <td>
          <p>Wählen Sie aus, ob Sie eine Standardverbindung für Dynamics Finance and Operations oder eine Verbindung mit einem Autorisierungs-Code erstellen.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre Dynamics Finance and Operations [!UICONTROL Client ID] ein.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihren Dynamics Finance and Operations [!UICONTROL Client Secret] ein. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Mandanten-ID]</td>
        <td>Geben Sie Ihre Dynamics Finance and Operations-Mandanten-ID ein.</td>
        </tr>
        <tr>
        <td role="rowheader">Ressource</td>
        <td>URL Ihres Dynamics Finance and Operations-Kontos eingeben (ohne https://)</td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.



## Microsoft Dynamics 365 Finance and Operations-Module und ihre Felder

>[!IMPORTANT]
>
>Die über die Dynamics 365 F&amp;O-API verfügbaren Datenentitäten können je nach Instanz variieren. Wenn Sie nicht sicher sind, welche Entitäten über die API verfügbar sind, ist es nützlich, die Entitäten in Ihrer Instanz mithilfe des Endpunkts „data“ zu durchsuchen. Der Endpunkt „Daten“ in Dynamics 365 Finance and Operations ist die Stamm-URL für den Zugriff auf OData-Services. Dieser Endpunkt ermöglicht die Interaktion mit verschiedenen Datenentitäten, die vom System mithilfe von Standard-OData-Protokollen verfügbar gemacht werden.
>
>Sie können diese Entitäten mithilfe des Moduls für benutzerdefinierte API-Aufrufe abrufen.
>
><!--For more information -->



### Entitätselement erstellen

Dieses Aktionsmodul erstellt ein neues Entitätselement in Microsoft Dynamics 365 Finance and Operations.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL -Verbindung]</td>
    <td> <p>Anweisungen zum Verbinden von Microsoft Dynamics 365 Finance and Operations mit Workfront Fusion finden Sie <a href="#create-a-connection" class="MCXref xref">Erstellen einer Verbindung</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL -Entität]</td>
     <td>Geben Sie den Entitätstyp Dynamics Finance and Operations ein, den Sie erstellen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL body]</td>
     <td> <p>Geben Sie einen JSON-Text ein, der die Daten enthält, die Sie in das neue Entitätselement aufnehmen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Entitätselement löschen

Dieses Aktionsmodul löscht ein Entitätselement aus Dynamics Finance and Operations. Das Element wird durch seine Primären Schlüsselfelder identifiziert.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL -Verbindung]</td>
    <td> <p>Anweisungen zum Verbinden von Microsoft Dynamics 365 Finance and Operations mit Workfront Fusion finden Sie <a href="#create-a-connection" class="MCXref xref">Erstellen einer Verbindung</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL -Entität]</td>
     <td>Geben Sie den Entitätstyp Dynamics Finance and Operations ein, den Sie löschen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primäre Schlüsselfelder]</td>
     <td> Die Primären Schlüsselfelder identifizieren das Element. Klicken Sie für jedes Primärschlüsselfeld, das Sie bereitstellen möchten, auf <b>Element hinzufügen</b> und geben Sie den eindeutigen Schlüssel und Wert, der dieses Element identifiziert, ein oder ordnen Sie ihn zu. </td> 
  </tr> 
 </tbody> 
</table>

### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt einen benutzerdefinierten Aufruf an die Dynamics Finance and Operations-API durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
    <td> <p>Anweisungen zum Verbinden von Microsoft Dynamics 365 Finance and Operations mit Workfront Fusion finden Sie <a href="#create-a-connection" class="MCXref xref">Erstellen einer Verbindung</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Geben Sie einen Pfad relativ zu Ihrer Dynamics Finance and Operations-URL ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Dadurch wird der Inhaltstyp der Anfrage bestimmt.</p> <p>Beispiel:<code> {"Content-type":"application/json"}</code></p> <p>Hinweis: Wenn Fehler auftreten und es schwierig ist, deren Ursprung zu ermitteln, sollten Sie die Kopfzeilen basierend auf der Workfront-Dokumentation ändern. Wenn Ihr benutzerdefinierter API-Aufruf einen 422-HTTP-Anfragefehler zurückgibt, versuchen Sie es mit einer <code>"Content-Type":"text/plain"</code>-Kopfzeile.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> <p>Tipp: Es wird empfohlen, Informationen über den JSON-Text und nicht als Abfrageparameter zu senden.</p> </td> 
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



### Entitätselement lesen

Dieses Aktionsmodul gibt Daten aus einem Entitätselement zurück. Das Element wird durch seine Primären Schlüsselfelder identifiziert.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL -Verbindung]</td>
    <td> <p>Anweisungen zum Verbinden von Microsoft Dynamics 365 Finance and Operations mit Workfront Fusion finden Sie <a href="#create-a-connection" class="MCXref xref">Erstellen einer Verbindung</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL -Entität]</td>
     <td>Geben Sie den Entitätstyp Dynamics Finance and Operations ein, den Sie lesen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primäre Schlüsselfelder]</td>
     <td> Die Primären Schlüsselfelder identifizieren das Element. Klicken Sie für jedes Primärschlüsselfeld, das Sie bereitstellen möchten, auf <b>Element hinzufügen</b> und geben Sie den eindeutigen Schlüssel und Wert, der dieses Element identifiziert, ein oder ordnen Sie ihn zu. </td> 
  </tr> 
 </tbody> 
</table>

### Entitätselement aktualisieren

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL -Verbindung]</td>
    <td> <p>Anweisungen zum Verbinden von Microsoft Dynamics 365 Finance and Operations mit Workfront Fusion finden Sie <a href="#create-a-connection" class="MCXref xref">Erstellen einer Verbindung</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL -Entität]</td>
     <td>Geben Sie den Entitätstyp Dynamics Finance and Operations ein, den Sie aktualisieren möchten, oder ordnen Sie ihn zu.</td> 
  </tr>  
  <tr> 
    <td>[!UICONTROL Primäre Schlüsselfelder]</td>
     <td> Die Primären Schlüsselfelder identifizieren das Element. Klicken Sie für jedes Primärschlüsselfeld, das Sie bereitstellen möchten, auf <b>Element hinzufügen</b> und geben Sie den eindeutigen Schlüssel und Wert, der dieses Element identifiziert, ein oder ordnen Sie ihn zu. </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL body]</td>
     <td> <p>Geben Sie einen JSON-Text ein, der die Daten enthält, die Sie in das neue Entitätselement aufnehmen möchten, oder ordnen Sie ihn zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Suchen

Dieses Suchmodul gibt Ergebnisse basierend auf von Ihnen angegebenen Kriterien zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer Workfront-App mit Workfront Fusion finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von Workfront mit Workfront Fusion</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL -Entität]</td> 
   <td>Geben Sie den Entitätstyp Dynamics Finance and Operations ein, nach dem Sie suchen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Suchkriterien]</td> 
   <td> <p>Geben Sie das Feld ein, nach dem Sie suchen möchten, den Operator, den Sie in Ihrer Abfrage verwenden möchten, und den Wert, nach dem Sie in dem Feld suchen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sortieren nach]</td> 
   <td> <p>Geben Sie das Feld ein, nach dem Sie die Ergebnisse sortieren möchten, oder ordnen Sie es zu.</p> </td> 
  </tr> 
 </tbody> 
</table>


<!--

### List All

This module lists all records for a given entity.  The item is identified by its Primary key fields.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to Workfront Fusion, see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
     <td>Choose the Dynamics Finance and Operations entity type that you want the module to list.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
     <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Watch Record

This trigger module starts a scenario when a record of the given type is created or updated.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to Workfront Fusion, see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->
