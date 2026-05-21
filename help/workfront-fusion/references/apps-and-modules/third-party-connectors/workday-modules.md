---
filename: workday-modules
title: Workday-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Workday] verwenden, und diese mit verschiedenen Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 77237a1b-2acd-4350-9cc0-ec43b8b08137
TQID: https://experienceleague.adobe.com/b-RlvqOsRRrFZMh8JrPFAS2pigkQP-6ugZ5kZl8AdZ8
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1063
ht-degree: 52%

---

# [!DNL Workday]-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Workday] verwenden, und diese mit verschiedenen Anwendungen und Services von Drittanbietern verbinden.

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

Um die [!DNL Workday]-Module zu verwenden, müssen Sie:

* Ein [!DNL Workday] Konto haben.

* Erstellen Sie eine OAuth-Anwendung in [!DNL Workday]. Anweisungen hierzu finden Sie in der [!DNL Workday].

## Workday-API-Informationen

Der Workday-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td><pre><code>https://&#123;&#123;connection.servicesUrl&#125;&#125;/api</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.6.4</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL Workday] mit Workfront Fusion

1. Klicken Sie in einem beliebigen Workfront Fusion-Modul [!UICONTROL Hinzufügen] neben dem Feld [!UICONTROL Verbindung]

2. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Verbindungsname]</p>
                </td>
                <td>Geben Sie einen Namen für die Verbindung ein.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Workday-Host]</td>
                <td>Geben Sie die Adresse Ihres [!DNL Workday]-Hosts ohne <code>https://</code> ein. Beispiel: <code>mycompany.workday.com</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Services URL]</td>
                <td>Geben Sie die Adresse Ihrer [!DNL Workday] Webservices ohne <code>https://</code> ein. Beispiel: <code>mycompany-services.workday.com</code>.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Mandantenname]</td>
                <td>Geben Sie den Mandanten für dieses [!DNL Workday] ein. Ihr Mandant ist die Kennung Ihres Unternehmens und ist in der URL zu sehen, mit der Sie sich bei Workday anmelden. Beispiel: Im <code>https://www.myworkday.com/mycompany</code> Adresse wird der Mandant <code>mycompany</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Client-ID]</td>
                <td>Geben Sie die Client-ID für die [!DNL Workday] ein, die diese Verbindung verwendet. Dies erhalten Sie, wenn Sie das Programm in [!DNL Workday] erstellen.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Client-Geheimnis]</td>
                <td>Geben Sie das Client-Geheimnis für die [!DNL Workday]-Anwendung ein, die diese Verbindung verwendet. Dies erhalten Sie, wenn Sie das Programm in [!DNL Workday] erstellen.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Sitzungs-Timeout (Min.)]</td>
                <td >Geben Sie die Anzahl der Minuten ein, nach denen Ihr Autorisierungs-Token abläuft.</td>
            </tr>
        </tbody>
    </table>


3. Klicken Sie [!UICONTROL Fortfahren], um die Verbindung zu speichern und zum Modul zurückzukehren

## [!DNL Workday]-Module und ihre Felder

Beim Konfigurieren von [!DNL Workday]-Modulen werden in Workfront Fusion die unten aufgeführten Felder angezeigt. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der Anwendung oder im Service weitere [!DNL Workday]-Felder angezeigt werden. Ein fett formatierter Titel in einem Modul kennzeichnet ein Pflichtfeld.

Wenn die Schaltfläche „Zuordnung“ über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen zwischen Modulen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter „Zuordnung“](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktion](#action)

* [Suchen](#search)


### Aktion

* [[!UICONTROL Eintrag erstellen]](#create-a-record)

* [[!UICONTROL Löschen eines Datensatzes]](#delete-a-record)

* [[!UICONTROL Benutzerdefinierten API-Aufruf durchführen]](#make-a-custom-api-call)

* [[!UICONTROL Eintrag aktualisieren]](#update-a-record)


#### [!UICONTROL Eintrag erstellen]

Dieses Aktionsmodul erstellt einen einzelnen Datensatz in [!DNL Workday].

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Verbindung]</td>
            <td>Anweisungen zum Verbinden Ihres [!DNL Workday]-Kontos mit Workfront Fusion finden Sie unter <a href="#Connect" class="MCXref xref" >Verbinden von [!DNL Workday] mit Workfront Fusion</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Eintragstyp]</td>
            <td>Wählen Sie den Typ des Eintrags aus, der erstellt werden soll.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Geben Sie die ID des Datensatzes ein, den Sie erstellen möchten, oder ordnen Sie sie zu.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Unterressourcen-ID]</td>
            <td >Geben Sie die ID der Unterressource ein, die Sie erstellen möchten, oder mappen Sie sie.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL Löschen eines Datensatzes]

Dieses Aktionsmodul löscht einen einzelnen Datensatz in [!DNL Workday].

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Verbindung]</td>
            <td>Anweisungen zum Verbinden Ihres [!DNL Workday]-Kontos mit Workfront Fusion finden Sie unter <a href="#Connect" class="MCXref xref" >Verbinden von [!DNL Workday] mit Workfront Fusion</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Eintragstyp]</td>
            <td>Wählen Sie den Typ des Datensatzes aus, den Sie löschen möchten.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Spezifischer Datensatztyp]</td>
            <td>Wählen Sie den spezifischen Typ des Datensatzes aus, den Sie löschen möchten. Diese basieren auf dem von Ihnen ausgewählten Datensatztyp.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Unterressourcen-ID]</td>
            <td>Geben Sie die ID der Teilressource ein, die Sie löschen möchten, oder mappen Sie sie.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >Geben Sie die ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</td>
        </tr>
    </tbody>
</table>


### [!UICONTROL Benutzerdefinierten API-Aufruf durchführen]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Workday]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, was über die anderen [!DNL Workday]-Module nicht möglich ist.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

Das Modul gibt den Status-Code zusammen mit den Kopfzeilen und dem Hauptteil des API-Aufrufs zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Connection]</p> </td> 
            <td>Anweisungen zum Verbinden Ihres [!DNL Workday]-Kontos mit Workfront Fusion finden Sie unter <a href="#Connect" class="MCXref xref" >Verbinden von [!DNL Workday] mit Workfront Fusion</a>.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Geben Sie einen Pfad relativ zu <code style="color: #ff1493;">https://&lt;tenantHostname>/api/&lt;serviceName>/&lt;version>/&lt;tenant></code> ein.</td> 
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
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p>Fügen Sie den Textinhalt für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrem JSON-Objekt verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eintrag aktualisieren]

Dieses Aktionsmodul aktualisiert einen einzelnen Datensatz in [!DNL Workday].

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Verbindung]</td>
            <td>Anweisungen zum Verbinden Ihres [!DNL Workday]-Kontos mit Workfront Fusion finden Sie unter <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect [!DNL Workday] to Workfront Fusion]</a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Eintragstyp]</td>
            <td>Wählen Sie den Typ des Datensatzes aus, den Sie aktualisieren möchten.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Geben Sie die ID des Eintrags ein, der aktualisiert werden soll, oder ordnen Sie diese zu.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Unterressourcen-ID]</td>
            <td >Geben Sie die ID der Unterressource ein, die Sie aktualisieren möchten, oder mappen Sie sie.</td>
        </tr>
    </tbody>
</table>

### Suchen

* [[!UICONTROL Eintrag lesen]](#read-a-record)

* [[!UICONTROL Einträge auflisten]](#list-records)


#### [!UICONTROL Eintrag lesen]

Dieses Aktionsmodul liest einen einzelnen Datensatz.

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Verbindung]</td>
            <td>Anweisungen zum Verbinden Ihres [!DNL Workday]-Kontos mit Workfront Fusion finden Sie unter <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect [!DNL Workday] to Workfront Fusion]</a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Eintragstyp]</td>
            <td>Wählen Sie den Typ des Datensatzes aus, den Sie löschen möchten.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Spezifischer Datensatztyp]</td>
            <td>Wählen Sie den Datensatztyp aus, den Sie lesen möchten. Diese basieren auf dem von Ihnen ausgewählten Datensatztyp.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >Geben Sie die ID des Datensatzes ein, den Sie löschen möchten, oder mappen Sie sie.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL Einträge auflisten]

Dieses Suchmodul ruft eine Liste von Datensätzen des angegebenen Typs ab.

<table style="table-layout:auto"> 
      <col/>
      <col/>
      <tbody>
          <tr>
              <td role="rowheader">[!UICONTROL Verbindung]</td>
              <td>Anweisungen zum Verbinden Ihres [!DNL Workday]-Kontos mit Workfront Fusion finden Sie unter <a href="#Connect" class="MCXref xref" >Verbinden von [!DNL Workday] mit Workfront Fusion</a></td>
          </tr>
          <tr>
              <td  role="rowheader">[!UICONTROL Eintragstyp]</td>
              <td>Wählen Sie den Typ des Datensatzes aus, den Sie abrufen möchten.</td>
          </tr>
          <tr>
              <td role="rowheader">[!UICONTROL Beschränkung]</td>
              <td >
                  <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus abrufen soll, oder mappen Sie sie.</p>
              </td>
          </tr>
      </tbody>
  </table>
