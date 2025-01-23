---
description: In  [!DNL Adobe Workfront Fusion]  Szenario können Sie Workflows automatisieren, die Anaplan verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 81c9b141-4e40-430f-99f1-c44b7a833bcd
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1616'
ht-degree: 0%

---

# [!DNL Anaplan] Module

In einem [!DNL Adobe Workfront Fusion] Szenario können Sie Workflows automatisieren, die [!DNL Anaplan] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenarios erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Plan*</td>
  <td> <p>[!UICONTROL Pro] oder höher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
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
 </tbody> 
</table>

Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Voraussetzungen

Bevor Sie den [!DNL Anaplan]-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein aktives [!UICONTROL Anaplan] verfügen.
* Sie müssen Arbeitsbereiche, Modelle und andere [!DNL Anaplan] Objekte in Ihrem [!UICONTROL Anaplan]-Konto konfigurieren, bevor [!DNL Workfront Fusion] mit ihnen interagieren können.

## Anaplan-API-Informationen

Der Anaplan-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://api.anaplan.com/2/0/
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.11.5/td&gt; 
 </tbody> 
</table>

## [!DNL Anaplan] mit [!DNL Workfront Fusion] verbinden {#connect-anaplan-to-workfront-fusion}

So erstellen Sie eine Verbindung für Ihre [!DNL Anaplan]:

1. Klicken Sie **[!UICONTROL Add]** neben dem [!UICONTROL Connection].
1. Wählen Sie den Verbindungstyp aus.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL Basic]</td> 
      <td> <p>Für eine [!DNL Anaplan] [!UICONTROL Basic] Verbindung sind nur eine E-Mail-Adresse und ein Kennwort erforderlich, um die Verbindung herzustellen. </p> <p>Geben Sie einen Namen für die Verbindung ein und dann Ihre E-Mail-Adresse und das Passwort Ihres [!DNL Anaplan] Kontos.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL CA Certificate]</td> 
      <td> <p>Eine [!DNL Anaplan] [!UICONTROL CA Certificate]-Verbindung erfordert eine [!UICONTROL Certificate Key], eine [!UICONTROL Encoded Data] und eine [!UICONTROL Encoded Signed Data]. Sie können diese in Ihrem [!DNL Anaplan]-Konto generieren. Anweisungen hierzu finden Sie in der [!DNL Anaplan].</p> <p>Geben Sie einen Namen für die Verbindung ein und geben Sie dann die [!UICONTROL Certificate Key], [!UICONTROL Encoded Data] und [!UICONTROL Encoded Signed Data] ein, die Sie in Ihrem [!DNL Anaplan]-Konto generiert haben.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie auf **[!UICONTROL Continue]** , um die Verbindung zu speichern und zum Modul zurückzukehren.

## [!DNL Anaplan] Module und ihre Felder

Beim Konfigurieren [!DNL Anaplan] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Anaplan] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Auslöser](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Auslöser

#### [!DNL Watch records]

Dieses Trigger-Modul startet ein Szenario, wenn ein Datensatz des ausgewählten Typs erstellt oder aktualisiert wird.

>[!NOTE]
>
>Dieses Modul gibt die Daten neuer Datensätze zurück. Es werden nicht die Daten der geänderten vorhandenen Datensätze zurückgegeben.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Typ des zu überwachenden Objekts</td> 
   <td>Wählen Sie den Typ des Elements aus, das Sie beobachten möchten. Das Szenario beginnt, wenn dieser Datensatztyp erstellt oder aktualisiert wird.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">&lt;Objekt&gt;-ID</td> 
   <td>Geben Sie die ID des Objekts in Anaplan ein, z. B. ein Modell oder Modul, das mit den Objekten verknüpft ist, die Sie beobachten möchten</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Grenze</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, denen das Modul während jedes Szenario-Ausführungszyklus [Aktion] zugeordnet werden soll.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Create a list item]](#create-a-list-item)
* [[!UICONTROL Make a custom API Call]](#make-a-custom-api-call)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Run an action]](#run-an-action)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Upload a file]](#upload-a-file)

#### [!UICONTROL Create a list item]

Dieses Aktionsmodul fügt ein neues Element zu einer Liste in Anaplan hinzu.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Connection]</td>
        <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Workspace ID]</td>
        <td>Wählen Sie die ID der Anaplan Workspace aus, die die Liste enthält, der Sie ein Element hinzufügen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Model ID]</td>
        <td>Wählen Sie die ID des Modells aus, das die Liste enthält, der Sie ein Element hinzufügen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
        <td>[!UICONTROL List ID]</td>
        <td>Wählen Sie die ID der Liste aus, in der Sie ein Element erstellen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Name]</td>
        <td>Geben Sie einen Namen für das neue Element ein.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Code]</td>
        <td>Geben Sie den Code für den neuen Artikel ein. Codes sind benutzergenerierte Codes, mit denen Sie zwischen Zeileneinträgen mit demselben Namen unterscheiden können.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Parent]</td>
        <td>Geben Sie den Namen des übergeordneten Elements ein, unter dem Sie das neue Element erstellen möchten.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Properties]</td>
        <td>Wenn die Liste, der Sie ein Element hinzufügen möchten, über benutzerdefinierte Eigenschaften verfügt, wählen Sie die Eigenschaften aus, denen Sie Werte hinzufügen möchten, und fügen Sie dann die Werte hinzu.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Subsets]</td>
        <td>Wenn die Liste, der Sie Elemente hinzufügen möchten, benutzerdefinierte Teilmengen enthält, wählen Sie die Teilmengen aus, denen Sie das Element hinzufügen möchten, und wählen Sie dann <b>[!UICONTROL Yes]</b> aus, um das neue Element zu dieser Teilmenge hinzuzufügen.</td>
    </tr>
</table>

#### [!UICONTROL Make a custom API Call]

In diesem Modul können Sie einen benutzerdefinierten API-Aufruf an die [!DNL Anaplan]-API durchführen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Pfad eingeben für <code>https://api.anaplan.com/2/0/</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p> </td> 
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

#### [!UICONTROL Delete a record]

Dieses Aktionsmodul löscht einen vorhandenen Datensatz.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie die ID der Anaplan Workspace aus, die das zu löschende Objekt enthält, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model ID]</td> 
   <td>Geben Sie die ID des Modells ein, das das zu löschende Objekt enthält, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Löschen</td> 
   <td> <p>Wählen Sie den Typ des zu löschenden Objekts.</p> 
    <ul> 
     <li> <p><b>Aktion</b> </p> <p>Wählen Sie die zu löschende Aktion aus oder ordnen Sie sie zu.</p> </li> 
     <li> <p><b>Listenelement</b> </p> <p>Wählen Sie die Liste aus, aus der Sie ein Element löschen möchten, und geben Sie dann die ID oder den Code des Elements ein, das Sie löschen möchten, oder ordnen Sie sie zu</p>  </li> 
     <li> <p><b>[!UICONTROL File]</b> </p> <p>Wählen Sie die zu löschende Datei aus oder ordnen Sie sie zu.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Dieses Aktionsmodul liest einen einzelnen Datensatz.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Typ des zu lesenden Datensatzes auswählen.</p> 
    <ul> 
     <li> <p><b>Modell</b> </p> <p>Wählen Sie die ID des Modells aus, das Sie lesen möchten, oder ordnen Sie sie zu</p> </li> 
     <li> <p><b>Modellliste</b> </p> <p>Wählen Sie die IDs der Workspace und des Modells aus, die die zu lesende Liste enthalten, oder ordnen Sie sie zu und wählen Sie dann die Liste aus. Wählen Sie im Feld [!UICONTROL Data type] aus, ob Sie Daten oder Metadaten lesen möchten.</p> </li> 
     <li> <p><b>Modellversion</b> </p> <p>Wählen Sie die ID des Modells aus, das Sie lesen möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><b>Benutzer</b> </p> <p>Wählen Sie aus, ob Sie Daten zum Eigentümer des verwendeten Kontos oder zu einem anderen Benutzer zurückgeben möchten. Wenn Sie einen anderen Benutzer auswählen, wählen Sie dessen Namen aus.</p> </li> 
     <li> <p><b>Workspace</b> </p> <p>Wählen Sie die ID der Workspace aus, die Sie lesen möchten, oder ordnen Sie sie zu.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Run an action]

Dieses Aktionsmodul importiert, exportiert, löscht oder verarbeitet eine Aktion.

<table style="table-layout:auto"> 
     <col/>
     <col/>
     <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect Anaplan to Workfront Fusion]</a> diesem Artikel.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Workspace ID]</td>
        <td>Wählen Sie die ID der [!DNL Anaplan] Workspace aus, in der Sie die Aktion durchführen möchten, oder ordnen Sie sie zu</td>
      </tr>
      <tr >
        <td role="rowheader">[!UICONTROL Model ID]</td>
        <td>Wählen Sie die ID des Modells aus, in dem Sie die Aktion durchführen möchten, oder ordnen Sie sie zu.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Action type]</td>
        <td>
          <p>Wählen Sie die Aktion aus, die Sie durchführen möchten</p>
            <ul>
              <li>
                <p><b>[!UICONTROL Delete]</b>
                </p>
                <p>Geben Sie die ID der Aktion ein, die Sie löschen möchten, oder ordnen Sie sie zu.</p>
              </li>
              <li>
                <p><b>[!UICONTROL Export]</b>
                </p>
                <p>Geben Sie die ID der Exportdefinition ein, die Sie verwenden möchten, oder ordnen Sie sie zu. Sie können in die folgenden Dateiformate exportieren:</p>
                  <ul>
                    <li>
                      <p>XLS</p>
                    </li>
                    <li>
                      <p>XLSX</p>
                    </li>
                    <li>
                      <p>CSV</p>
                    </li>
                  </ul>
                </li>
                <li>
                  <p><b>[!UICONTROL Import] </b>
                  </p>
                  <p style="font-weight: normal;">Geben Sie die ID der Importdefinition ein, die Sie verwenden möchten, oder mappen Sie sie zu.</p>
                </li>
                <li>
                 <p><b>[!UICONTROL Process]</b>
                 </p>
                  <p>Geben Sie die ID des Prozesses ein, den Sie verwenden möchten, oder ordnen Sie sie zu. </p>
                </li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>


#### [!UICONTROL Update a record]

Dieses Aktionsmodul aktualisiert einen einzelnen Datensatz in [!UICONTROL Anaplan].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie aktualisieren möchten.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL List item]</b> </p> <p>Informationen zu Feldern finden <a href="#create-a-list-item" class="MCXref xref"> unter „Listenelement erstellen</a> in diesem Artikel.</p> </li> 
     <li> <p><b>[!UICONTROL Module cell data]</b> </p> <p>Wenn Sie Zelldaten aktualisieren, werden auch alle nachgelagerten Berechnungen aktualisiert, die diese Daten verwenden.</p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Model ID]</b> </p> <p>Wählen Sie das Modell aus, das die zu aktualisierende Zelle enthält, oder ordnen Sie es zu.</p> </li> 
       <li> <p><b>[!UICONTROL Module ID]</b> </p> <p>Wählen Sie das Modul aus, das die zu aktualisierende Zelle enthält, oder ordnen Sie es zu</p> </li> 
       <li> <p><b>[!UICONTROL Line item name]</b> </p> <p>Wählen Sie den Zeileneintrag der Zelle aus, die Sie aktualisieren möchten, oder ordnen Sie ihn zu</p> </li> 
       <li> <p style="font-weight: bold;">[!UICONTROL Dimension ID]</p> <p>Wählen Sie die Dimension aus, die sich im Zeileneintrag befindet, oder ordnen Sie sie zu.</p> 
       <p><b>Hinweis: </b> 
       <ul>
       <li> Dimension-Schlüssel (Wert) muss entweder <code>dimensionName</code> (Weiter) oder <code>dimensionId</code> (ID) sein.</li>
       <li>Elementschlüssel (Wert) muss <code>itemName</code> (Text), <code>itemCode</code> (Text) oder <code>itemId</code> (ID) sein.</li>
       <li>Dimensionen- und Elementschlüssel müssen vom gleichen Typ sein (Text oder ID).
       </ul>
        </p> 
        <p>Suchen Sie in der [!DNL Anaplan Anapedia] nach Dimensionen, um Informationen zu Dimensionen zu erhalten.</p> </li> 
       <li> <p><b>[!UICONTROL Value]</b> </p> <p>Geben Sie den neuen Wert für die Zelle ein oder mappen Sie ihn.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Model current fiscal year]</b> </p> <p>Geben Sie die Workspace-ID und Modell-ID des Modells ein, für das Sie das Geschäftsjahr aktualisieren möchten, und geben Sie dann das neue Jahr für das Modell ein oder ordnen Sie es zu.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

Dieses Aktionsmodul lädt eine Datei in Anaplan hoch. Die Datei muss bereits in Anaplan hochgeladen worden sein. Sie können dieses Modul verwenden, um es an zusätzliche Stellen in Anaplan hochzuladen.
<table style="table-layout:auto">
<col>
<col>
<tbody>
<tr>
<td role="rowheader">[!UICONTROL Connection]</td>
<td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Workspace ID]</td>
<td>Wählen Sie die ID der [!DNL Anaplan] Workspace aus, in die Sie eine Datei hochladen möchten, oder ordnen Sie sie zu.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Model ID]</td>
<td>Wählen Sie die ID des Modells aus, in das Sie eine Datei hochladen möchten, oder ordnen Sie sie zu.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL File ID]</td>
<td>Wählen Sie die ID der Datei aus, die Sie hochladen möchten, oder ordnen Sie sie zu.</td>
</tr>
</tbody>
</table>
</div>

### Suchvorgänge

#### [!UICONTROL Get record]

Dieses Suchmodul gibt alle Datensätze des ausgewählten Typs zurück, auf die zugegriffen werden kann.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record types]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie abrufen möchten.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Workspaces]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Models]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Line items]</b> </p> <p>Wählen Sie die ID des Modells aus, das die [!DNL line] Elemente enthält, die Sie abrufen möchten, oder ordnen Sie sie zu.</p> </li> 
       <li> <p><b>[!UICONTROL Model lists]</b> </p> <p>Wählen Sie die ID der Workspace und die Modell-ID aus bzw. ordnen Sie sie zu, die die Modelllisten enthalten, die Sie abrufen möchten.</p> </li> 
       <li> <p><b>[!UICONTROL Model calendar]</b> </p> <p>Wählen Sie die ID der Workspace aus, die den abzurufenden Modellkalender enthält, oder ordnen Sie sie zu.</p> </li> 
       <li> <p><b>[!UICONTROL Model versions]</b> </p> </li> 
       <li> <p>Wählen Sie die ID des Modells aus, das die Modellversionen enthält, die Sie abrufen möchten, oder ordnen Sie sie zu.</p> </li> 
       <li> <p><b>[!UICONTROL Users]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Views]</b> </p> <p>Wählen Sie aus, ob Sie die Ansicht nach Modul oder nach Modell auswählen möchten, und wählen Sie dann die ID des Moduls oder Modells aus, das die abzurufende Ansicht enthält, oder ordnen Sie sie zu.</p> </li> 
      </ul> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Return workspace size]</td> 
   <td>Aktivieren Sie diese Option, um eine Schätzung der aktuellen Größe des Arbeitsbereichs zurückzugeben. Diese Schätzung basiert auf den Größen aller im Arbeitsbereich enthaltenen Module.</td> 
  </tr> 
 </tbody> 
</table>
