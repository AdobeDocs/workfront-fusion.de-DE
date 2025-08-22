---
title: Partnermodule
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die verwenden [!DNL Bynder] und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 0a45f8a7-12cc-41cc-9135-92f4779afac0
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1847'
ht-degree: 1%

---

# [!DNL Bynder]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Bynder] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Um [!DNL Bynder]-Module verwenden zu können, müssen Sie über ein [!DNL Bynder]-Konto verfügen.

## Binder-API-Informationen

Der Binder-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.25.21</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL Bynder] mit Workfront Fusion  {#connect-bynder-to-workfront-fusion}

>[!NOTE]
>
>Bunter verwendet den Gewährungstyp Autorisierungs-Code/Aktualisierungstoken. Dies ist der einzige Gewährungstyp, den der Fusion Bunter-Connector verwendet.

* [Erstellen einer Verbindung zu  [!DNL Bynder]  von Workfront Fusion](#create-a-connection-to-bynder-from-workfront-fusion)
* [Generieren einer [!UICONTROL Client-ID] und [!UICONTROL Client-Geheimnis] in [!DNL Bynder] (optional)](#generate-a-client-id-and-client-secret-in-bynder-optional)

### Erstellen einer Verbindung zu [!DNL Bynder] von Workfront Fusion aus

Sie können direkt aus einem [!DNL Bynder]-Modul heraus eine Verbindung von Workfront Fusion zu Ihrem [!DNL Bynder]-Konto erstellen.

1. Klicken Sie in einem [!DNL Bynder] Modul **[!UICONTROL Hinzufügen]** neben dem Feld [!UICONTROL Verbindung].
1. Wählen Sie die [!DNL Bynder] Domain aus, mit der Sie eine Verbindung herstellen möchten.
1. (Optional) Klicken Sie auf **[!UICONTROL Erweiterte Einstellungen]** und geben Sie dann Ihre [!UICONTROL Client-ID] und [!UICONTROL Client-Geheimnis] ein.

   Anweisungen zum Generieren der Client-ID und des Client-Geheimnisses finden Sie unter [Generieren einer Client-ID und eines Client-Geheimnisses in [!DNL Bynder] (optional)](#generate-a-client-id-and-client-secret-in-bynder-optional) in diesem Artikel.

1. Geben [!UICONTROL &#x200B; im Fenster &quot;]&quot; Ihren Benutzernamen (E-Mail-Adresse) und Ihr Passwort ein.
1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu erstellen, und kehren Sie zum Modul zurück.

### Generieren einer [!UICONTROL Client-ID] und [!UICONTROL Client-]) in [!DNL Bynder] (optional)

Wenn Sie eine Verbindung mit der Client-ID und dem Client-Geheimnis erstellen möchten, können Sie sie aus Ihrem [!DNL Bynder]-Konto generieren. Die Client-ID und der geheime Client-Schlüssel werden beim Erstellen einer App in [!DNL Bynder] generiert.

Anweisungen zum Erstellen einer App in [!DNL Bynder] finden Sie unter [OAuth 2.0-](https://developer-docs.bynder.com/api/authentication-oauth2-oauth-apps/)) in der [!DNL Bynder].

>[!NOTE]
>
>* Geben Sie beim Erstellen der App in [!DNL Bynder] Folgendes als `redirect uri` ein:
>
>   * US-Cluster: `https://app.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * EU-Cluster: `https://app-eu.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * Azure-Cluster: `https://app-az.workfrontfusion.com/oauth/cb/workfront-bynder`
>* Bunter verwendet den Gewährungstyp Autorisierungs-Code/Aktualisierungstoken. Dies ist der einzige Gewährungstyp, den der Fusion Bunter-Connector verwendet.

## [!DNL Bynder] Module und ihre Felder

Beim Konfigurieren von [!DNL Bynder] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Bynder] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aktionen](#actions)
* [Suchvorgänge](#searches)
* [Trigger](#triggers)

### Aktionen

* [[!UICONTROL Hinzufügen eines Tags zu Assets]](#add-a-tag-to-assets)
* [[!UICONTROL Hinzufügen von Assets zu einer Sammlung]](#add-assets-to-a-collection)
* [[!UICONTROL Benutzerdefinierter API-Aufruf]](#custom-api-call)
* [[!UICONTROL Asset herunterladen]](#download-asset)
* [[!UICONTROL Asset-Metadaten lesen]](#read-asset-metadata)
* [[!UICONTROL Entfernen eines Tags] aus Assets](#remove-a-tag-from-assets)
* [[!UICONTROL Entfernen von Assets aus der Sammlung]](#remove-assets-from-collection)
* [[!UICONTROL Aktualisieren von Asset-Metadaten]](#update-asset-metadata)
* [[!UICONTROL Asset hochladen]](#upload-asset)

#### [!UICONTROL Hinzufügen eines Tags zu Assets]

Dieses Aktionsmodul fügt einem oder mehreren Assets ein Tag hinzu

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag-ID]</td> 
   <td> <p>Geben Sie die ID des Tags ein, das Sie zu Assets hinzufügen möchten, oder ordnen Sie sie zu.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-IDs]</td> 
   <td> <p>Klicken Sie für jedes Asset, das Sie mit einem Tag versehen möchten, auf <strong>[!UICONTROL Element hinzufügen]</strong> und geben Sie dann die Asset-ID ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL Hinzufügen von Assets zu einer Sammlung]

Dieses Aktionsmodul fügt ein oder mehrere Assets zu einer Sammlung hinzu.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Sammlungs-ID]</td> 
   <td> <p>Geben Sie die ID der Sammlung ein, der Sie Assets hinzufügen möchten, oder mappen Sie sie.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-IDs]</td> 
   <td> <p>Klicken Sie für jedes Asset, das Sie der Sammlung hinzufügen möchten, auf <strong>[!UICONTROL Element hinzufügen]</strong> und geben Sie dann die Asset-ID ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Bynder]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Bynder] nicht durchgeführt werden kann.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

Das Modul gibt einen Status-Code zusammen mit den Kopfzeilen und dem Hauptteil des API-Aufrufs zurück.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Geben Sie einen Pfad relativ zu <code>https://{your-bynder-domain}/api/{api-version}/</code> ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Methode]</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
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

#### [!UICONTROL Asset herunterladen]

Dieses Aktionsmodul lädt ein einzelnes Asset herunter.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID]</td> 
   <td>Geben Sie die ID des Assets ein, das Sie herunterladen möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-Version]</td> 
   <td> <p>Geben Sie die Version des Assets ein, das Sie herunterladen möchten, oder ordnen Sie sie zu. Um die neueste Version des Assets herunterzuladen, lassen Sie das Feld leer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Asset-Metadaten lesen]

Dieses Aktionsmodul liest die Metadaten eines Assets.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID]</td> 
   <td>Geben Sie die ID des Assets ein, für das Sie Metadaten abrufen möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Entfernen eines Tags aus Assets]

Dieses Aktionsmodul entfernt ein Tag aus einem oder mehreren Assets

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag-ID]</td> 
   <td> <p>Geben Sie die ID des Tags ein, das Sie aus Assets entfernen möchten, oder ordnen Sie sie zu.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-IDs]</td> 
   <td> <p>Klicken Sie für jedes Asset, aus dem Sie ein Tag entfernen möchten, auf <strong>[!UICONTROL Element hinzufügen]</strong> und geben Sie dann die Asset-ID ein bzw. mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Entfernen von Assets aus der Sammlung]

Dieses Aktionsmodul entfernt ein oder mehrere Assets aus einer Sammlung.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Sammlungs-ID]</td> 
   <td> <p>Geben Sie die ID der Sammlung ein, aus der Sie Assets entfernen möchten, oder mappen Sie sie.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-IDs]</td> 
   <td> <p>Klicken Sie für jedes Asset, das Sie aus der Sammlung entfernen möchten, auf <strong>[!UICONTROL Element hinzufügen]</strong> und geben Sie dann die Asset-ID ein oder ordnen Sie sie zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktualisieren von Asset-Metadaten]

Dieses Aktionsmodul aktualisiert die Metadaten eines vorhandenen Assets.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset-ID]</td> 
   <td>Geben Sie die ID des Assets ein, für das Sie Metadaten aktualisieren möchten, oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Felder]</td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Informationen eingeben möchten, und geben Sie dann die Informationen, mit denen Sie die Metadaten aktualisieren möchten, in diese Felder ein oder ordnen Sie sie zu. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metaproperties]</p> </td> 
   <td>Wählen Sie die Optionen aus, die Sie aktualisieren möchten, und geben Sie dann die Informationen in diese Eigenschaften ein oder ordnen Sie sie ihnen zu. Metaeigenschaften sind Informationen über das Asset, die keine bestimmten Felder im Asset darstellen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Asset hochladen]

Dieses Aktionsmodul lädt ein einzelnes Asset hoch.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Speichern unter]</td> 
   <td> <p>Wählen Sie aus, wie Sie die hochgeladene Datei speichern möchten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Neues Asset]</strong> </p> <p>Wählen Sie die Felder und Metaeigenschaften aus, für die Sie Informationen eingeben möchten, und geben Sie dann die Informationen in diese Felder ein.</p> <p>Geben Sie die ID der Marke ein, die Sie für das hochgeladene Asset verwenden möchten, oder ordnen Sie sie zu.</p> </li> 
     <li> <p><strong>[!UICONTROL Neue Asset-Version]</strong> </p> <p>Geben Sie die ID des Assets ein, für das Sie eine neue Version hochladen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asynchroner Datei-Upload]</td> 
   <td>Aktivieren Sie diese Option beim Hochladen großer Dateien. Dadurch wird verhindert, dass große Dateien die Ausführung des Szenarios blockieren.</td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL Eintrag auflisten]](#list-record)
* [[!UICONTROL Assets durchsuchen]](#search-assets)

#### [!UICONTROL Eintrag auflisten]

Dieses Suchmodul ruft alle Elemente eines bestimmten Typs ab.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie den Typ des aufzulistenden Datensatzes aus.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Alle Sammlungen lesen]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Informationen über alle Tags lesen]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Alle Assets einer Sammlung lesen]</strong> </p> <p>Geben Sie die ID der Sammlung ein, für die Sie Assets auflisten möchten, oder ordnen Sie sie zu.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assets durchsuchen]

Dieses Suchmodul sucht anhand der von Ihnen angegebenen Kriterien nach Assets.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Suchkriterien]</td> 
   <td> <p>Geben Sie die Suchkriterien ein. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL -Feld]</strong> </p> <p>Wählen Sie das Feld aus, das Sie für Ihre Suche verwenden möchten</p> </li> 
     <li> <p><strong>[!UICONTROL Logischer Operator]</strong> </p> <p>Wählen Sie den Operator aus, den Sie für Ihre Suche verwenden möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL value]</strong> </p> <p>Geben Sie den Wert, nach dem im ausgewählten Feld gesucht werden soll, ein oder ordnen Sie ihn zu. Der Werttyp sollte mit dem Datentyp des ausgewählten Felds übereinstimmen. </p> <p>Weitere Informationen zu Datentypen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Elementdatentypen</a>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ergebnissatz]</td> 
   <td>Wählen Sie aus, ob das erste übereinstimmende Asset oder alle übereinstimmenden Assets zurückgegeben werden sollen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortieren nach]</td> 
   <td> <p>Wählen Sie das Feld aus, nach dem Sie sortieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortierrichtung]</td> 
   <td> <p>Wählen Sie aus, ob auf- oder absteigend sortiert werden soll.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Felder aus, die Sie in die Ausgabe des Moduls aufnehmen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Assets ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Trigger

#### [!UICONTROL Überwachen von Assets]

Dieses Trigger-Modul startet ein Szenario, wenn ein Asset erstellt oder aktualisiert wird.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL -Verbindung]</p> </td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Bynder]-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Bynder] mit Workfront Fusion </a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">Ereignistyp</td>
    <td>Wählen Sie aus, ob das Szenario gestartet werden soll, wenn ein neues Asset erstellt oder ein vorhandenes Asset aktualisiert wird.</td>
  </tr> 
  <tr>
     <td role="rowheader">[!UICONTROL -Sammlungen]</td>
   <td> <p>Wählen Sie die Sammlung aus, die Sie auf neue Assets überwachen möchten. Um alle Sammlungen zu sehen, lassen Sie dieses Feld leer.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">Ausgaben</td>
    <td>Wählen Sie die Felder aus, die Sie in die Ausgabe aufnehmen möchten.</td>
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Limit]</td>

<td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul bei jedem Ausführungszyklus des Szenarios zurückgeben soll.</p> </td> 
  </tr> 
 </tbody> 
</table>
