---
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Anaplan verwenden, und es mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 81c9b141-4e40-430f-99f1-c44b7a833bcd
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2029'
ht-degree: 1%

---

# [!DNL Anaplan] Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Anaplan] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Bevor Sie den [!DNL Anaplan]-Connector verwenden können, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

* Sie müssen über ein aktives [!UICONTROL Anaplan]-Konto verfügen.
* Sie müssen Arbeitsbereiche, Modelle und andere [!DNL Anaplan] Objekte in Ihrem [!UICONTROL Anaplan“-] konfigurieren, bevor Workfront Fusion mit ihnen interagieren kann.

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
   <td>v1.11.5</td> 
 </tbody> 
</table>

## Verbinden von [!DNL Anaplan] mit Workfront Fusion {#connect-anaplan-to-workfront-fusion}

So erstellen Sie eine Verbindung für Ihre [!DNL Anaplan]:

1. Klicken Sie **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
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
        <td role="rowheader">[!UICONTROL email]</td>
        <td>
          <p>E-Mail-Adresse für dieses Anaplan-Konto eingeben</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Kennwort]</td>
        <td>Passwort für dieses Anaplan-Konto eingeben.</td>
      </tr>
     </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

<!--1. Click **[!UICONTROL Add]** next to the [!UICONTROL Connection] box.
1. Select the connection type.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL Basic]</td> 
      <td> <p>An [!DNL Anaplan] [!UICONTROL Basic] connection requires only an email address and password to create the connection. </p> <p>Enter a name for the connection, then enter your email address and the password of your [!DNL Anaplan] account.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL CA Certificate]</td> 
      <td> <p>An [!DNL Anaplan] [!UICONTROL CA Certificate] connection requires a [!UICONTROL Certificate Key], [!UICONTROL Encoded Data], and [!UICONTROL Encoded Signed Data]. You can generate these in your [!DNL Anaplan] account. For instructions, see the [!DNL Anaplan] documentation.</p> <p>Enter a name for the connection, then enter the [!UICONTROL Certificate Key], [!UICONTROL Encoded Data], and [!UICONTROL Encoded Signed Data] that you generated in your [!DNL Anaplan] account.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.-->

## [!DNL Anaplan] Module und ihre Felder

Beim Konfigurieren von [!DNL Anaplan] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Anaplan] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Trigger

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
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit Workfront </a> in diesem Artikel.</td> 
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
   <td role="rowheader">Limit</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Listenelement erstellen]](#create-a-list-item)
* [Löschen eines Datensatzes](#delete-a-record)
* [Daten exportieren](#export-data)
* [Daten importieren](#import-data)
* [[!UICONTROL Erstellen eines benutzerdefinierten API-Aufrufs]](#make-a-custom-api-call)
* [[!UICONTROL Eintrag lesen]](#read-a-record)
* [[!UICONTROL Aktion ausführen]](#run-an-action)
* [[!UICONTROL Aktualisieren eines Datensatzes]](#update-a-record)
* [[!UICONTROL Datei hochladen]](#upload-a-file)

#### [!UICONTROL Listenelement erstellen]

Dieses Aktionsmodul fügt ein neues Element zu einer Liste in Anaplan hinzu.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL-Verbindung]</td>
        <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit Workfront </a> in diesem Artikel.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Workspace ID]</td>
        <td>Wählen Sie die ID der Anaplan Workspace aus, die die Liste enthält, der Sie ein Element hinzufügen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Modell-ID]</td>
        <td>Wählen Sie die ID des Modells aus, das die Liste enthält, der Sie ein Element hinzufügen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Listen-ID]</td>
        <td>Wählen Sie die ID der Liste aus, in der Sie ein Element erstellen möchten, oder ordnen Sie sie zu.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Name]</td>
        <td>Geben Sie einen Namen für das neue Element ein.</td>
    </tr>
    <tr>
        <td>[!UICONTROL-Code]</td>
        <td>Geben Sie den Code für den neuen Artikel ein. Codes sind benutzergenerierte Codes, mit denen Sie zwischen Zeileneinträgen mit demselben Namen unterscheiden können.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Parent]</td>
        <td>Geben Sie den Namen des übergeordneten Elements ein, unter dem Sie das neue Element erstellen möchten.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Eigenschaften]</td>
        <td>Wenn die Liste, der Sie ein Element hinzufügen möchten, über benutzerdefinierte Eigenschaften verfügt, wählen Sie die Eigenschaften aus, denen Sie Werte hinzufügen möchten, und fügen Sie dann die Werte hinzu.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Teilmengen]</td>
        <td>Wenn die Liste, der Sie Elemente hinzufügen möchten, benutzerdefinierte Teilmengen enthält, wählen Sie die Teilmengen aus, denen Sie das Element hinzufügen möchten.</td>
    </tr>
</table>

#### [!UICONTROL Löschen eines Datensatzes]

Dieses Aktionsmodul löscht einen vorhandenen Datensatz.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie die ID der Anaplan Workspace aus, die das zu löschende Objekt enthält, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modell-ID]</td> 
   <td>Geben Sie die ID des Modells ein, das das zu löschende Objekt enthält, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eintragstyp</td> 
   <td> <p>Wählen Sie den Typ des zu löschenden Objekts.</p> 
    <ul> 
     <li> <p><b>Aktion</b> </p> <p>Wählen Sie die zu löschende Aktion aus oder ordnen Sie sie zu.</p> </li> 
     <li> <p><b>Listenelement</b> </p> <p>Wählen Sie die Liste aus, aus der Sie ein Element löschen möchten, und geben Sie dann die ID oder den Code des Elements ein, das Sie löschen möchten, oder ordnen Sie sie zu</p>  </li> 
     <li> <p><b>[!UICONTROL-Datei]</b> </p> <p>Wählen Sie die zu löschende Datei aus oder ordnen Sie sie zu.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Exportieren von Daten]

Dieses Aktionsmodul ruft Daten aus Anaplan mithilfe von Exportdefinitionen ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie die ID der Anaplan Workspace aus, die die zu exportierenden Daten enthält, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modell-ID]</td> 
   <td>Geben Sie die ID des Modells ein, das die zu exportierenden Daten enthält, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Definition-ID exportieren</td> 
   <td> <p>Geben Sie die ID der Anaplan-Exportdefinition ein, die Sie verwenden möchten, oder mappen Sie sie.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>

#### Daten importieren

Dieses Aktionsmodul importiert Daten in Anaplan.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Wählen Sie die ID der Anaplan Workspace, in die Sie die Daten importieren möchten, aus oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modell-ID]</td> 
   <td>Geben Sie die ID des Modells ein, in das Sie die Daten importieren möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Definition-ID exportieren</td> 
   <td> <p>Geben Sie die Kennung der Importdefinition von Anaplan ein, die Sie verwenden möchten, oder mappen Sie sie.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Erstellen eines benutzerdefinierten API-Aufrufs]

In diesem Modul können Sie einen benutzerdefinierten API-Aufruf an die [!DNL Anaplan]-API durchführen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Pfad eingeben für <code>https://api.anaplan.com/2/0/</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL-Methode]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt Autorisierungs-Header automatisch hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge] </td> 
   <td> <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p> </td> 
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

#### [!UICONTROL Eintrag lesen]

Dieses Aktionsmodul liest einen einzelnen Datensatz.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Typ des zu lesenden Datensatzes auswählen.</p> 
    <ul> 
     <li> <p><b>Modell</b> </p> <p>Wählen Sie die ID des Modells aus, das Sie lesen möchten, oder ordnen Sie sie zu</p> </li> 
     <li> <p><b>Modellliste</b> </p> <p>Wählen Sie die IDs der Workspace und des Modells aus, die die zu lesende Liste enthalten, oder ordnen Sie sie zu und wählen Sie dann die Liste aus. Wählen Sie im Feld [!UICONTROL Datentyp] aus, ob Sie Daten oder Metadaten lesen möchten.</p> </li> 
     <li> <p><b>Modellversion</b> </p> <p>Wählen Sie die ID des Modells aus, das Sie lesen möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><b>Benutzer</b> </p> <p>Wählen Sie aus, ob Sie Daten zum Eigentümer des verwendeten Kontos oder zu einem anderen Benutzer zurückgeben möchten. Wenn Sie einen anderen Benutzer auswählen, wählen Sie dessen Namen aus.</p> </li> 
     <li> <p><b>Workspace</b> </p> <p>Wählen Sie die ID der Workspace aus, die Sie lesen möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><b>Anzeigen</b> </p> <p>Wählen Sie die ID des Modells aus, das die Ansicht enthält, die Sie lesen möchten, oder ordnen Sie sie zu.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktion ausführen]

Dieses Aktionsmodul importiert, exportiert, löscht oder verarbeitet eine Aktion.

<table style="table-layout:auto"> 
     <col/>
     <col/>
     <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL-Verbindung]</td>
        <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect Anaplan to Workfront Fusion]</a> in diesem Artikel.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Workspace ID]</td>
        <td>Wählen Sie die ID der [!DNL Anaplan] Workspace aus, in der Sie die Aktion durchführen möchten, oder ordnen Sie sie zu</td>
      </tr>
      <tr >
        <td role="rowheader">[!UICONTROL Modell-ID]</td>
        <td>Wählen Sie die ID des Modells aus, in dem Sie die Aktion durchführen möchten, oder ordnen Sie sie zu.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Aktionstyp]</td>
        <td>
          <p>Wählen Sie die Aktion aus, die Sie durchführen möchten</p>
            <ul>
              <li>
                <p><b>[!UICONTROL DELETE]</b>
                </p>
                <p>Geben Sie die ID der Aktion ein, die Sie löschen möchten, oder ordnen Sie sie zu.</p>
              </li>
              <li>
                <p><b>[!UICONTROL export]</b>
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
                  <p><b>[!UICONTROL Import]-</b>
                  </p>
                  <p style="font-weight: normal;">Geben Sie die ID der Importdefinition ein, die Sie verwenden möchten, oder mappen Sie sie zu.</p>
                </li>
                <li>
                 <p><b>[!UICONTROL-Prozess]</b>
                 </p>
                  <p>Geben Sie die ID des Prozesses ein, den Sie verwenden möchten, oder ordnen Sie sie zu. </p>
                </li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>


#### [!UICONTROL Aktualisieren eines Datensatzes]

Dieses Aktionsmodul aktualisiert einen einzelnen Datensatz in [!UICONTROL Anaplan].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie aktualisieren möchten.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Listenelement]</b> </p> <p>Informationen zu Feldern finden <a href="#create-a-list-item" class="MCXref xref"> unter „Listenelement erstellen</a> in diesem Artikel.</p> </li> 
     <li> <p><b>[!UICONTROL Module Cell Data]</b> </p> <p>Wenn Sie Zelldaten aktualisieren, werden auch alle nachgelagerten Berechnungen aktualisiert, die diese Daten verwenden.</p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Model ID]</b> </p> <p>Wählen Sie das Modell aus, das die zu aktualisierende Zelle enthält, oder ordnen Sie es zu.</p> </li> 
       <li> <p><b>[!UICONTROL MODULE ID]</b> </p> <p>Wählen Sie das Modul aus, das die zu aktualisierende Zelle enthält, oder ordnen Sie es zu</p> </li> 
       <li> <p><b>[!UICONTROL Zeilenname]</b> </p> <p>Wählen Sie den Zeileneintrag der Zelle aus, die Sie aktualisieren möchten, oder ordnen Sie ihn zu</p> </li> 
       <li> <p style="font-weight: bold;">[!UICONTROL Dimension ID]</p> <p>Wählen Sie die Dimension aus, die sich im Zeileneintrag befindet, oder ordnen Sie sie zu.</p> 
       <p><b>Hinweis: </b> 
       <ul>
       <li> Dimension-Schlüssel (Wert) muss entweder <code>dimensionName</code> (Weiter) oder <code>dimensionId</code> (ID) sein.</li>
       <li>Elementschlüssel (Wert) muss <code>itemName</code> (Text), <code>itemCode</code> (Text) oder <code>itemId</code> (ID) sein.</li>
       <li>Dimension- und Elementschlüssel müssen vom gleichen Typ sein (Text oder ID).
       </ul>
        </p> 
        <p>Suchen Sie für Informationen zu Dimensionen in der [!DNL Anaplan Anapedia] nach Dimensionen .</p> </li> 
       <li> <p><b>[!UICONTROL value]</b> </p> <p>Geben Sie den neuen Wert für die Zelle ein oder mappen Sie ihn.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Modell aktuelles Geschäftsjahr]</b> </p> <p>Geben Sie die Workspace-ID und Modell-ID des Modells ein, für das Sie das Geschäftsjahr aktualisieren möchten, und geben Sie dann das neue Jahr für das Modell ein oder ordnen Sie es zu.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei für Aktion hochladen]

Dieses Aktionsmodul lädt eine vorhandene Datei in Anaplan an zusätzliche Stellen in Anaplan hoch.
<table style="table-layout:auto">
<col>
<col>
<tbody>
<tr>
<td role="rowheader">[!UICONTROL-Verbindung]</td>
<td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit Workfront </a> in diesem Artikel.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Workspace ID]</td>
<td>Wählen Sie die ID der [!DNL Anaplan] Workspace aus, in die Sie eine Datei hochladen möchten, oder ordnen Sie sie zu.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Modell-ID]</td>
<td>Wählen Sie die ID des Modells aus, in das Sie eine Datei hochladen möchten, oder ordnen Sie sie zu.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Datei-ID]</td>
<td>Wählen Sie die ID der Datei aus, die Sie hochladen möchten, oder ordnen Sie sie zu.</td>
</tr>
</tbody>
</table>
</div>

### Suchvorgänge

#### [!UICONTROL Datensatz abrufen]

Dieses Suchmodul gibt alle Datensätze des ausgewählten Typs zurück, auf die zugegriffen werden kann.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td>Anweisungen zum Erstellen einer Verbindung zu [!DNL Anaplan] finden Sie unter <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Anaplan] mit Workfront </a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztypen]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, den Sie abrufen möchten.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Workspace]</b> </p> </li> 
       <li> <p><b>[!UICONTROL-Modelle]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Zeileneinträge]</b> </p> <p>Wählen Sie die ID des Modells aus, das die [!DNL line] Elemente enthält, die Sie abrufen möchten, oder ordnen Sie sie zu.</p> </li> 
       <li> <p><b>[!UICONTROL Modelllisten]</b> </p> <p>Wählen Sie die ID der Workspace und die Modell-ID aus bzw. ordnen Sie sie zu, die die Modelllisten enthalten, die Sie abrufen möchten.</p> </li> 
       <li> <p><b>[!UICONTROL Modellkalender]</b> </p> <p>Wählen Sie die ID der Workspace aus, die den abzurufenden Modellkalender enthält, oder ordnen Sie sie zu.</p> </li> 
       <li> <p><b>[!UICONTROL Modellversionen]</b> </p> </li> 
       <li> <p>Wählen Sie die ID des Modells aus, das die Modellversionen enthält, die Sie abrufen möchten, oder ordnen Sie sie zu.</p> </li> 
       <li> <p><b>[!UICONTROL Benutzer]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Views]</b> </p> <p>Wählen Sie aus, ob Sie die Ansicht nach Modul oder nach Modell auswählen möchten, und wählen Sie dann die ID des Moduls oder Modells aus, das die abzurufende Ansicht enthält, oder ordnen Sie sie zu.</p> </li> 
      </ul> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Arbeitsbereichsgröße zurückgeben]</td> 
   <td>Aktivieren Sie diese Option, um eine Schätzung der aktuellen Größe des Arbeitsbereichs zurückzugeben. Diese Schätzung basiert auf den Größen aller im Arbeitsbereich enthaltenen Module.</td> 
  </tr> 
 </tbody> 
</table>
