---
title: Microsoft Dynamics 365 Finance and Operations-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, die Microsoft Dynamics 365 Finance and Operations verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 96f8d4f1-f97b-4da8-8d82-83cccb54ec68
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# [!DNL Microsoft Dynamics 365 Finance and Operations modules]

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Microsoft Dynamics 365] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

>[!NOTE]
>
>Der [!DNL Microsoft Dynamics 365 Finance and Operations]-Connector unterstützt keine [!DNL Dynamics 365].
>
>Informationen zu Microsoft Dynamics 365-Modulen finden Sie [[!DNL Microsoft Dynamics 365 modules]](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).



Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Erstellen einer Verbindung

So erstellen Sie eine Verbindung für Ihre Microsoft Dynamics 365 Finance and Operations-Module:

1. Klicken Sie in einem beliebigen Microsoft Dynamics 365-Finanz- und Betriebsmodul neben dem Feld Verbindung auf **[!UICONTROL Add]** .

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
          <p>Wählen Sie aus, ob Sie eine Standardverbindung für Dynamics Finance and Operations oder eine Verbindung mit einem Autorisierungs-Code erstellen.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Geben Sie Ihre Dynamics Finance and Operations-[!UICONTROL Client ID] ein.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Geben Sie Ihre Dynamics Finance and Operations-[!UICONTROL Client Secret] ein. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tenant ID]</td>
        <td>Geben Sie Ihre Dynamics Finance and Operations-Mandanten-ID ein.</td>
        </tr>
        <tr>
        <td role="rowheader">Ressource</td>
        <td>URL Ihres Dynamics Finance and Operations-Kontos eingeben (ohne https://)</td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu speichern und zum Modul zurückzukehren.



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
    <td>[!UICONTROL Connection]</td>
    <td> <p>Anweisungen zum Verbinden von Microsoft Dynamics 365 Finance and Operations mit [!DNL Workfront Fusion] finden Sie <a href="#create-a-connection" class="MCXref xref">Erstellen einer Verbindung</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Geben Sie den Entitätstyp Dynamics Finance and Operations ein, den Sie erstellen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
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
    <td>[!UICONTROL Connection]</td>
    <td> <p>Anweisungen zum Verbinden von Microsoft Dynamics 365 Finance and Operations mit [!DNL Workfront Fusion] finden Sie <a href="#create-a-connection" class="MCXref xref">Erstellen einer Verbindung</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Geben Sie den Entitätstyp Dynamics Finance and Operations ein, den Sie löschen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>Anweisungen zum Verbinden von Microsoft Dynamics 365 Finance and Operations mit [!DNL Workfront Fusion] finden Sie <a href="#create-a-connection" class="MCXref xref">Erstellen einer Verbindung</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Geben Sie einen Pfad relativ zu Ihrer Dynamics Finance and Operations-URL ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu. Dadurch wird der Inhaltstyp der Anfrage bestimmt.</p> <p>Beispiel:<code> {"Content-type":"application/json"}</code></p> <p>Hinweis: Wenn Fehler auftreten und es schwierig ist, deren Ursprung zu ermitteln, sollten Sie die Kopfzeilen basierend auf der [!DNL Workfront] Dokumentation ändern. Wenn Ihr benutzerdefinierter API-Aufruf einen 422-HTTP-Anfragefehler zurückgibt, versuchen Sie es mit einer <code>"Content-Type":"text/plain"</code>-Kopfzeile.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query string]</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> <p>Tipp: Es wird empfohlen, Informationen über den JSON-Text und nicht als Abfrageparameter zu senden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
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
    <td>[!UICONTROL Connection]</td>
    <td> <p>Anweisungen zum Verbinden von Microsoft Dynamics 365 Finance and Operations mit [!DNL Workfront Fusion] finden Sie <a href="#create-a-connection" class="MCXref xref">Erstellen einer Verbindung</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Geben Sie den Entitätstyp Dynamics Finance and Operations ein, den Sie lesen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
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
    <td>[!UICONTROL Connection]</td>
    <td> <p>Anweisungen zum Verbinden von Microsoft Dynamics 365 Finance and Operations mit [!DNL Workfront Fusion] finden Sie <a href="#create-a-connection" class="MCXref xref">Erstellen einer Verbindung</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Geben Sie den Entitätstyp Dynamics Finance and Operations ein, den Sie aktualisieren möchten, oder ordnen Sie ihn zu.</td> 
  </tr>  
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> Die Primären Schlüsselfelder identifizieren das Element. Klicken Sie für jedes Primärschlüsselfeld, das Sie bereitstellen möchten, auf <b>Element hinzufügen</b> und geben Sie den eindeutigen Schlüssel und Wert, der dieses Element identifiziert, ein oder ordnen Sie ihn zu. </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
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
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihrer [!DNL Workfront] App mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Workfront] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Entity]</td> 
   <td>Geben Sie den Entitätstyp Dynamics Finance and Operations ein, nach dem Sie suchen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Geben Sie das Feld ein, nach dem Sie suchen möchten, den Operator, den Sie in Ihrer Abfrage verwenden möchten, und den Wert, nach dem Sie in dem Feld suchen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort by]</td> 
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
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to [!DNL Workfront Fusion], see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
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
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to [!DNL Workfront Fusion], see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of [!DNL Workfront] record that you want the module to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to [!DNL Workfront] logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
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
