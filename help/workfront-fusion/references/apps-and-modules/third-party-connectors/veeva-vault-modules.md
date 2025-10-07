---
title: Veeva Vault-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Veeva Vault verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion
source-git-commit: 6e7125bee77526caa93edc17f05b75bdfd7d7ac4
workflow-type: tm+mt
source-wordcount: '1514'
ht-degree: 3%

---

# Veeva Vault-Module

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die Veeva Vault verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

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

Um Veeva Vault-Module verwenden zu können, benötigen Sie ein Veeva Vault-Konto.

## Veeva Vault-Module und ihre Felder

Beim Konfigurieren von Veeva Vault-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service zusätzliche Veeva-Vault-Felder angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Dokument

* [Ein einzelnes Dokument erstellen](#create-a-single-document)
* [Mehrere Dokumente erstellen](#create-multiple-documents)
* [Ein einzelnes Dokument löschen](#delete-a-single-document)
* [Dokumente exportieren](#export-documents)
* [Ein einzelnes Dokument abrufen](#get-a-single-document)
* [Benutzeraktion initiieren](#initiate-user-action)
* [Dokumente auflisten](#list-documents)
* [Ergebnisse des Dokumentexports abrufen](#retrieve-document-export-results)
* [Mehrere Dokumente aktualisieren](#update-multiple-documents)
* [Einzelnes Dokument aktualisieren](#update-a-single-document)

#### Ein einzelnes Dokument erstellen

Dieses Modul erstellt ein einzelnes Dokument, einen einzelnen Binder oder eine einzelne Vorlage.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie ein Dokument, einen Binder oder eine Vorlage erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Felder auswählen</p> </td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Daten eingeben möchten, und geben Sie dann die Daten in diese Felder ein.</td> 
  </tr> 
 </tbody> 
</table>

#### Mehrere Dokumente erstellen

Dieses Modul erstellt mehrere Dokumente oder Vorlagen mithilfe einer CSV-Datei.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Auswählen, ob Vorlagen oder Dokumente erstellt werden sollen</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dateidaten</p> </td> 
   <td> <p>Ordnen Sie die CSV-Datei zu, die zum Erstellen der Dokumente verwendet wird.</td> 
  </tr> 
 </tbody> 
</table>

#### Ein einzelnes Dokument löschen

Dieses Modul löscht ein einzelnes Dokument, einen Binder oder eine Vorlage.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie ein Dokument, einen Binder oder eine Vorlage löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokument-ID/Binder-ID/Vorlagenname</p> </td> 
   <td> <p>Wählen Sie die Felder aus, die Sie löschen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### Dokumente exportieren

Dieses Modul exportiert von Ihnen angegebene Dokumente, einschließlich Quellen, Ausgabedarstellungen und Text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie ein Dokument, einen Binder oder eine Vorlage löschen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Quelle</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um Quelldateien in den Export einzuschließen.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Ausgabedarstellungen</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um Ausgabedarstellungsdateien in den Export einzuschließen.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Alle Versionen</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um alle Versionen der Dokumentdateien in den Export einzubeziehen.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Text</p> </td> 
   <td> <p>Aktivieren Sie diese Option, um Quelldokumenttext in den Export einzuschließen.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Ein einzelnes Dokument abrufen

Dieses Modul ruft Metadaten für ein einzelnes Dokument, einen Binder oder eine Vorlage ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie Daten für ein Dokument, einen Binder oder eine Vorlage abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokument-ID/Binder-ID/Vorlagenname</p> </td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Daten abrufen möchten.</td> 
  </tr> 
 </tbody> 
</table>

#### Benutzeraktion initiieren

Dieses Modul initiiert Aktionen für Dokumente und Binder, z. B. das Senden eines Dokuments zur Überprüfung oder das Ändern seines Status.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie eine Aktion auf einem Dokument oder einem Binder durchführen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokument/Binder</p> </td> 
   <td> <p>Wählen Sie das Dokument oder den Binder aus, für das bzw. den Sie die Aktion durchführen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Dokumentversion/-binderversion</p> </td> 
   <td> <p>Wählen Sie das Dokument oder den Binder aus, für das bzw. den Sie die Aktion durchführen möchten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Aktion</p> </td> 
   <td> <p>Wählen Sie die Aktion aus, die mit dem Dokument oder dem Binder durchgeführt werden soll.</td> 
  </tr> 
 </tbody> 
</table>

#### Dokumente auflisten

Dieses Modul listet alle Dokumente des ausgewählten Typs auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Dokumente, Ordner oder Vorlagen aufgelistet werden sollen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### Ergebnisse des Dokumentexports abrufen

Dieses Modul gibt die Ergebnisse eines zuvor angeforderten Dokumentexports zurück.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Vorgangs-ID</p> </td> 
   <td> <p>Geben Sie die ID des Auftrags ein, für den Sie Ergebnisse zurückgeben möchten, oder mappen Sie sie. </p> </td> 
  </tr> 
  </tbody> 
</table>

#### Mehrere Dokumente aktualisieren

Dieses Modul aktualisiert mehrere Dokumente oder Vorlagen mithilfe einer CSV-Datei.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Auswählen, ob Vorlagen oder Dokumente erstellt werden sollen</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dateidaten</p> </td> 
   <td> <p>Ordnen Sie die CSV-Datei zu, die zum Erstellen der Dokumente verwendet wird.</td> 
  </tr> 
 </tbody> 
</table>

#### Einzelnes Dokument aktualisieren

Dieses Modul aktualisiert ein einzelnes Dokument, einen Binder oder eine Vorlage.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Wählen Sie aus, ob Sie ein Dokument, einen Binder oder eine Vorlage erstellen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID/Name</p> </td> 
   <td> <p>Wenn Sie eine Vorlage aktualisieren, geben Sie einen neuen Namen für die Vorlage ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Name der neuen Vorlage</p> </td> 
   <td> <p>Geben Sie die ID oder den Namen des Objekts ein, das Sie aktualisieren möchten, oder ordnen Sie sie zu.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>Felder auswählen</p> </td> 
   <td> <p>Wählen Sie die Felder aus, für die Sie Daten eingeben möchten, und geben Sie dann die Daten in diese Felder ein.</td> 
  </tr> 
 </tbody> 
</table>

### Objekt



#### Objekte auflisten

Dieses Modul ruft alle Vault-Objekte im authentifizierten Vault ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Lokalisierte Kennzeichnungen abrufen</p> </td> 
   <td> <p>Wählen Sie Ja , um lokalisierte (übersetzte) Zeichenfolgen für die Felder label und label_plural abzurufen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### Sonstiges

* [Erstellen eines benutzerdefinierten API-Aufrufs](#make-a-custom-api-call)
* [Erstellen einer VQL-Abfrage](#make-a-vql-query)
* [Protokolle lesen](#read-logs)

#### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt einen benutzerdefinierten Aufruf an die Veeva Vault-API durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Geben Sie einen Pfad relativ zu <code>baseurl/api/v</code> ein.  Beispiel: <code>/objects/documents</code>. <code>baseurl/api/v/</code> nicht einschließen, da es bereits eingeschlossen ist.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Methode</td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kopfzeilen</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion fügt die Autorisierungskopfzeilen für Sie hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Abfragezeichenfolge</td> 
   <td> <p>Fügen Sie die Abfrage für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Textkörper</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen einer VQL-Abfrage

Dieses Modul führt eine Abfrage mit Vault Query Language (VQL) durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Typ</p> </td> 
   <td> <p>Auswählen, ob Vorlagen oder Dokumente erstellt werden sollen</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dateidaten</p> </td> 
   <td> <p>Ordnen Sie die CSV-Datei zu, die zum Erstellen der Dokumente verwendet wird.</td> 
  </tr> 
 </tbody> 
</table>

#### Protokolle lesen

Dieses Modul gibt Daten aus Audit-Protokollen zurück

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung </td> 
   <td> <p>Anweisungen zum Verbinden Ihres Veeva Vault-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Prüfungstyp</p> </td> 
   <td> <p>Wählen Sie den Audittyp aus, für den Sie Daten abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Startdatum</p> </td> 
   <td> <p>Geben Sie das Startdatum für die Audits ein, die Sie abrufen möchten, oder ordnen Sie es zu.</p><p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Enddatum</p> </td> 
   <td> <p>Geben Sie das Enddatum für die Audits ein, die Sie abrufen möchten, oder ordnen Sie es zu.</p><p>Eine Liste der unterstützten Datums- und Zeitformate finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Typzwang</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Ergebnis-URL </p> </td> 
   <td> <p>Wählen Sie CSV aus, wenn Sie eine URL zum Herunterladen einer CSV-Datei des Ergebnisses abrufen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>


