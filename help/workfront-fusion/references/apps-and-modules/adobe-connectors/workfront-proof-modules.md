---
title: Workfront Proof-Module
description: In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die verwenden [!DNL Workfront Proof] und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.
author: Becky
feature: Workfront Fusion, Workfront Proof, Digital Content and Documents
exl-id: 9e556ae5-e672-4872-9c40-8c8e5f0305be
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '3131'
ht-degree: 0%

---

# [!DNL Workfront Proof]

In einem Adobe Workfront Fusion-Szenario können Sie Workflows automatisieren, die [!DNL Workfront Proof] verwenden, und sie mit mehreren Anwendungen und Services von Drittanbietern verbinden.

Dies ist nützlich, wenn Sie Aufgaben ausführen müssen, die derzeit beim Proofing in Workfront oder in [!DNL Workfront Proof] nicht unterstützt werden, z. B. das Aktualisieren von Korrekturabzügen auf der Grundlage bestimmter Ereignisse und die Suche nach den Empfängern eines Korrekturabzugs.

Der [!DNL Workfront Proof]-Connector wird nicht auf die Anzahl der aktiven Apps angerechnet, die für Ihre Organisation verfügbar sind. Alle Szenarien werden mit der Gesamtanzahl der Szenarien Ihres Unternehmens verrechnet, auch wenn sie nur die [!DNL Workfront Proof]-App verwenden.

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

## Workfront Proof-Informationen

Der Workfront Proof-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Version</td> 
   <td> v21.3.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.8.92</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden von [!DNL Workfront Proof] mit Workfront Fusion

Sie können direkt aus einem Workfront Fusion-Modul heraus eine Verbindung zu Ihrem [!DNL Workfront Proof]-Konto herstellen.

1. Klicken Sie in einem beliebigen Workfront Fusion-Modul [!UICONTROL **Hinzufügen**] neben dem Feld [!UICONTROL Verbindung]

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
                <td  role="rowheader">[!UICONTROL Umgebung]</td>
                <td>Wählen Sie aus, ob es sich um eine Produktionsumgebung oder eine Nicht-Produktionsumgebung wie Vorschau oder Sandbox handelt.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Typ]</td>
                <td>Wählen Sie aus, ob dies ein Service-Konto oder ein persönliches Konto ist.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL E-Mail/Benutzername]</td>
                <td>Geben Sie den Benutzernamen für Ihr [!DNL Workfront Proof] ein.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Kennwort]</td>
                <td>Geben Sie das Passwort für Ihr [!DNL Workfront Proof] Konto ein.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Mandanten-ID]</td>
                <td><strong>Hinweis</strong>: Kunden, die BYOK nicht verwenden, müssen dieses Feld leer lassen. <p>Mandanten-ID für dieses Konto eingeben. Wenn Sie Hilfe bei der Suche nach Ihrer Mandanten-ID benötigen, wenden Sie sich an den Kunden-Support von Workfront.</p></td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Domain-Erweiterung]</td>
                <td>Geben Sie die Erweiterung für die URL ein, über die Sie auf Ihr Konto zugreifen möchten. <p>Beispiel: <code>com</code> oder <code>eu</code></p></td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Produktions-, Vorschau- oder benutzerdefinierte Umgebung]</td>
                <td>Die Produktions-, Vorschau- oder benutzerdefinierte Umgebung, mit der Sie eine Verbindung herstellen möchten.</td>
            </tr>
        </tbody>
    </table>


3. Klicken Sie [!UICONTROL **Fortfahren**], um die Verbindung zu speichern und zum Modul zurückzukehren

## [!DNL Workfront Proof] Module und ihre Felder

Beim Konfigurieren von [!DNL Workfront Proof] zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Workfront Proof] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Aktionen](#actions)
* [Suchvorgänge](#searches)

### Trigger

* [Auf PDF-Zusammenfassung achten](#watch-for-pdf-summary)
* [[!UICONTROL Aktivität „Korrekturabzug ansehen]](#watch-proof-activity)
* [Korrekturabzüge ansehen](#watch-proofs)

#### [!UICONTROL Auf PDF-Zusammenfassung achten]

Dieses Instant Trigger-Modul führt ein Szenario aus, wenn jemand eine PDF-Zusammenfassung für einen Korrekturabzug erstellt.

In diesem Modul ist ein Webhook erforderlich.

Das Modul gibt alle Standardfelder zurück, die mit dem Korrekturabzug verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Außerdem wird ein neues Ereignisabonnement für PDF-Zusammenfassungen erstellt und der Inhalt des `pdf_url`-Attributs ausgegeben, das in der Payload gesendet wird. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook-Name]</td> 
   <td>Namen für den neuen Webhook eingeben oder zuordnen</td> 
  </tr> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aktivität „Korrekturabzug ansehen]

Dieses Trigger-Modul führt ein Szenario aus, wenn eine bestimmte Aktivität in einem Korrekturabzug stattfindet.

Das Modul gibt alle Standardfelder zurück, die mit dem Korrekturabzug verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Außerdem wird ein neues Ereignisabonnement für PDF-Zusammenfassungen erstellt und der Inhalt des `pdf_url`-Attributs ausgegeben, das in der Payload gesendet wird. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Aktivitätstyp]</td> 
   <td>Wählen Sie aus, ob Sie eine neue Entscheidung (einschließlich Änderungen des Korrekturabzugsstatus) oder nur Änderungen des Gesamtstatus des Korrekturabzugs anzeigen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Testsendungen ansehen]

Dieses Modul für geplante Trigger führt ein Szenario aus, wenn jemand einen Korrekturabzug erstellt oder eine Entscheidung darüber trifft.

Das Modul gibt eine Liste aller Datensätze zusammen mit ihren Typen zurück, die es während des von Ihnen angegebenen Zeitraums findet. Außerdem werden die Werte der angegebenen Felder zurückgegeben. Wenn das Modul Entscheidungen gefunden hat, die für den Korrekturabzug getroffen wurden, enthält es sowohl den vorherigen als auch den aktuellen Wert in separaten Feldern. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Dies geschieht in einem regelmäßig geplanten Intervall, das Sie angeben.

Sie müssen über ausreichende Berechtigungen für den Zugriff auf den/die Korrekturabzug(e) in [!DNL Workfront Proof] verfügen, um diese Informationen abrufen zu können.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL-Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Art des Eintrags</td> 
   <td>Wählen Sie aus, ob Sie nach neuen Korrekturabzügen oder nach neuen allgemeinen Korrekturabzugsentscheidungen suchen möchten.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Limit</td> 
   <td> <p>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Elemente pro Seite</td> 
   <td> <p>Um die Ergebnisse zu paginieren, geben Sie die Anzahl der zurückgegebenen Ergebnisse ein, die auf jeder Ergebnisseite angezeigt werden sollen, oder mappen Sie sie. Diese Zahl muss kleiner oder gleich 100 sein.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aktionen

* [[!UICONTROL Korrekturabzug erstellen]](#create-proof)
* [[!UICONTROL Benutzerdefinierter API-Aufruf]](#custom-api-call)
* [[!UICONTROL Testversand herunterladen]](#download-proof)
* [[!UICONTROL Datensatz lesen]](#read-a-record)
* [[!UICONTROL PDF-Zusammenfassung anfordern]](#request-pdf-summary)
* [[!UICONTROL Korrekturabzug aktualisieren]](#update-proof)
* [[!UICONTROL Datei hochladen]](#upload-file)

#### [!UICONTROL Korrekturabzug erstellen]

<!--Cannot test Jan 2025-->

Dieses Aktionsmodul erstellt einen neuen Korrekturabzug oder eine neue Version eines Korrekturabzugs in [!DNL Workfront Proof].

Sie geben die Parameter für den neuen Korrekturabzug und den Quellkorrektur an, wenn Sie eine neue Version erstellen.

Das Modul gibt die ID der neuen Korrekturabzugs- oder Korrekturabzugsversion zurück. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Testversand-Typ]</td> 
   <td> <p>Geben Sie an, ob für den erstellten Korrekturabzug ein einfacher Workflow oder ein automatisierter [!UICONTROL Workflow] verwendet werden soll.</p> <p>Füllen Sie dann die Felder aus, die für den von Ihnen ausgewählten Testversand-Typ angezeigt werden. Wenn Sie beispielsweise [!UICONTROL Automated Workflow] ausgewählt haben, füllen Sie das Feld <strong>[!UICONTROL Workflow-Phasen]</strong> aus, um die Phasen zu konfigurieren.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Ursprüngliche Datei herunterladen zulassen]</td> 
   <td>Wählen Sie aus, ob der Download der Originaldatei, aus der der Korrekturabzug erstellt wurde, zugelassen werden soll.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Classic Proof Viewer]</td> 
   <td>Wählen Sie aus, ob Sie die klassische Korrekturabzugsansicht verwenden.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Alle Dateien in einem Korrekturabzug kombinieren]</td> 
   <td>Aktivieren Sie diese Option, um alle Dateien in einem mehrseitigen Korrekturabzug zu kombinieren.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Neue Korrekturabzugsversion erstellen]</td> 
   <td>Wählen Sie diese Option aus, wenn das Modul eine neue Version eines vorhandenen Korrekturabzugs erstellen soll. Ordnen Sie dann im Feld <strong>[!UICONTROL Existing Proof ID]</strong>, das angezeigt wird, die eindeutige ID des Korrekturabzugs zu oder geben Sie sie ein.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Kennzeichnung benutzerdefinierter Links]</td> 
   <td>Geben Sie einen Titel für den benutzerdefinierten Korrekturabzugs-Link ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL für benutzerdefinierten Link]</td> 
   <td>Geben Sie die URL für den benutzerdefinierten Link ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Standard-E-Mail-Benachrichtigungen für Abonnenten]</td> 
   <td>Geben Sie eine der folgenden Zahlen ein, um anzugeben, welche der folgenden standardmäßigen E-Mail-Benachrichtigungseinstellungen Sie für den erstellten Korrekturabzug verwenden möchten.
    <ul>
     <li><strong>1</strong> - Alle neuen Kommentare und Antworten</li>
     <li><strong>2</strong> - Antworten auf meine Kommentare</li>
     <li><strong>3</strong> - Tägliche Zusammenfassung</li>
     <li><strong>4</strong> - Stündliche Zusammenfassung</li>
     <li><strong>5</strong> - Nur Entscheidungen</li>
     <li><strong>9</strong> - Deaktiviert</li>
    </ul></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Excel-Zusammenfassung deaktivieren]</td> 
   <td>Wählen Sie aus, ob Sie die Möglichkeit deaktivieren möchten, Korrekturabzugskommentare in eine Excel-Datei herunterzuladen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL PDF deaktivieren]</td> 
   <td>Wählen Sie aus, ob Sie die Möglichkeit deaktivieren möchten, Korrekturabzugskommentare in eine PDF-Datei herunterzuladen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Abonnement-E-Mail deaktivieren]</td> 
   <td>Wählen Sie aus, ob Sie die Abonnement-E-Mail für diesen Korrekturabzug deaktivieren möchten.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Einbettungs-Player aktivieren]</td> 
   <td>Wählen Sie aus, ob Sie den eingebetteten Player für diesen Korrekturabzug aktivieren möchten.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Abonnements aktivieren]</td> 
   <td>Wählen Sie aus, ob Personen, die nicht Teilnehmer sind, den Testversand abonnieren dürfen.<br>Wenn Sie diese Option auswählen, können Sie auch die Standardrolle für Abonnenten auswählen, wie in dieser Tabelle beschrieben.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Abonnementvalidierung aktivieren]</td> 
   <td>Wählen Sie aus, ob Sie die Validierung von Abonnement-E-Mails aktivieren möchten. Wenn diese Option aktiviert ist, muss der Abonnent auf einen Link in einer E-Mail klicken, um auf einen Korrekturabzug zuzugreifen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Team-URL aktivieren]</td> 
   <td>Wählen Sie aus, ob der erstellte Korrekturabzug die Team-URL ausblenden oder anzeigen soll.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Datei Hash] <span style="font-weight: normal;">oder</span> [!UICONTROL Datei Hashes]</td> 
   <td>Fügen Sie die ID der Datei(en) hinzu, aus der/denen Sie einen Korrekturabzug oder Korrekturabzüge erstellen möchten.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Dateinamen]</td> 
   <td>Dateinamen für den erstellten Korrekturabzug hinzufügen. Dies ist ein Pflichtfeld.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sperren Sie den Korrekturabzug, wenn alle erforderlichen Entscheidungen getroffen werden]</td> 
   <td>Geben Sie an, ob der Korrekturabzug, der erstellt wird, nach allen erforderlichen Entscheidungen gesperrt werden soll.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Empfänger über diesen Korrekturabzug informieren]</td> 
   <td>Wählen Sie eine Option aus, um anzugeben, ob die Empfänger bei der Erstellung des Korrekturabzugs benachrichtigt werden sollen.&gt;</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name des Korrekturabzugs]</td> 
   <td>Geben Sie einen Namen für den Korrekturabzug ein, der erstellt wird. Dies ist ein Pflichtfeld. Verwenden Sie ein senkrechtes Strichsymbol (|), um Namen für mehrere Korrekturabzüge zu trennen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Testversand-Besitzer-ID]</td> 
   <td>Geben Sie die ID des Testversand-Inhabers ein oder mappen Sie sie. Wenn dieses Feld leer gelassen wird, wird der/die Verantwortliche für den Korrekturabzug auf den aktuellen Benutzer bzw. die aktuelle Benutzerin festgelegt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-Referenz-ID]</td> 
   <td>Geben Sie die Referenz-ID für den Testversand ein.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Elektronische Signatur erforderlich]</td> 
   <td>Wählen Sie aus, ob eine Person, die über einen Korrekturabzug entscheidet, eine elektronische Signatur senden soll.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Anmeldung erforderlich]</td> 
   <td> <p>Geben Sie an, ob für den erstellten Korrekturabzug eine Anmeldung erforderlich sein soll. </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Auflösungs-ID]</td> 
   <td>Geben Sie die ID der Auflösung ein, die Sie für Ihren Korrekturabzug verwenden möchten. Eine Liste der Auflösungs-IDs finden Sie in der [!DNL Workfront Proof] <a href="https://api.proofhq.com/home/objects/soapworkflowproofobject.html">API-Dokumentation</a>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL SWF]</td> 
   <td>Geben Sie den Typ des SWF-Korrekturabzugs ein.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Anzeigen] [Element]</td> 
   <td>Wählen Sie für jedes Element aus, ob es im Korrekturabzug angezeigt werden soll.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Workspace ID]</td> 
   <td>Geben Sie die ID des Arbeitsbereichs ein, in dem Sie den Korrekturabzug erstellen möchten. </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Empfänger]</td> 
   <td>Fügen Sie die E-Mail-Adressen der Empfänger hinzu, die für den erstellten Korrekturabzug verwendet werden sollen.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Frist]</td> 
   <td> <p>Geben Sie die Frist an, bis zu der der Korrekturabzug erstellt werden soll. Verwenden Sie das folgende Datumsformat:</p> <p><code>YYYY-MM-DD hh:mm</code></p> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Benutzerdefinierter API-Aufruf]

Mit diesem Aktionsmodul können Sie einen benutzerdefinierten authentifizierten Aufruf an die [!DNL Workfront Proof]-API durchführen. Auf diese Weise können Sie eine Datenflussautomatisierung erstellen, die von den anderen [!DNL Workfront Proof] nicht durchgeführt werden kann.

Das Modul gibt den Status-Code, die Kopfzeilen und den Hauptteil zurück. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL-Methode]</td> 
   <td>Festlegen der Aktion für den API-Aufruf. Informationen zu verfügbaren Aktionen finden Sie in der <a href="https://api.proofhq.com/">Dokumentation zur Korrekturabzugs-API</a>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Hauptteil (XML)]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Beispiel:**
>
>![Beispiel für ein Proof-API-Modul](/help/workfront-fusion/references/apps-and-modules/assets/wfp-api-module-example-350x586.png)

#### [!UICONTROL Testversand herunterladen]

Dieses Aktionsmodul lädt die Quelldatei eines bestimmten Korrekturabzugs herunter, den Sie mithilfe seiner ID identifizieren.

Sie geben die ID des Korrekturabzugs an.

Das -Modul gibt den Inhalt der Quelldatei zurück, die zum Erstellen des Korrekturabzugs verwendet wird. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Sie müssen über ausreichende Berechtigungen für den Zugriff auf den Datensatz in [!DNL Workfront Proof] verfügen, um diese Informationen abrufen zu können.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Korrekturabzugs-ID]</td> 
   <td> <p>Geben Sie die eindeutige ID des Korrekturabzugs ein, die auf der Seite [!UICONTROL Korrekturabzugsdetails] zu finden ist.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datensatz lesen]

Dieses Aktionsmodul liest Daten aus einem einzelnen Korrekturabzug in [!DNL Workfront Proof].

Geben Sie die ID des Korrekturabzugs und die Informationen an, die Sie vom Korrekturabzug erhalten möchten.

Das Modul gibt die Werte der Felder zurück, die Sie für den Testversand auswählen, zusammen mit ihren Typen. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Sie müssen über ausreichende Berechtigungen für den Zugriff auf den Datensatz in [!DNL Workfront Proof] verfügen, um diese Informationen abrufen zu können.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Datensatztyp]</td> 
   <td>Wählen Sie aus, ob Sie einen Korrekturabzug, Kommentare zu Korrekturabzügen oder Prüfer für Korrekturabzüge lesen möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Geben Sie die eindeutige [!DNL Workfront Proof]-ID des Datensatzes ein, den das Modul lesen soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL PDF-Zusammenfassung anfordern]

Dieses Aktionsmodul fordert die PDF-Zusammenfassung für einen bestimmten Korrekturabzug in [!DNL Workfront Proof] an.

Sie geben die ID des Korrekturabzugs an.

Das -Modul gibt zusammenfassende Informationen zu PDF zurück. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Sie müssen über ausreichende Berechtigungen für den Zugriff auf den Datensatz in [!DNL Workfront Proof] verfügen, um diese Informationen abrufen zu können.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Korrekturabzugs-ID]</td> 
   <td> <p>Geben Sie die eindeutige [!DNL Workfront Proof]-ID des Testversands ein, für den Sie eine PDF-Zusammenfassung anfordern möchten.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Callback-URL]</td> 
   <td>Geben Sie die URL ein, an die die PDF-Zusammenfassung gesendet werden soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

##### Möglicher Fehler

* **Error**: &quot;[!UICONTROL Sie sind nicht berechtigt, diese Anfrage auszuführen. Die Phase muss mindestens einen Empfänger enthalten.]&quot;
* **Lösung**: Stellen Sie sicher, dass Sie nicht die einzige Person sind, die den Phasen des Workflows zugewiesen ist. Den Phasen des Workflows muss ein anderer Benutzer zugewiesen sein.

#### [!UICONTROL Korrekturabzug aktualisieren]

Dieses Aktionsmodul aktualisiert einen vorhandenen Korrekturabzug in [!DNL Workfront Proof].

Sie geben die ID und den Datensatztyp des Korrekturabzugs an und legen fest, welche Felder in die Ausgabe aufgenommen werden sollen.

Das Modul gibt alle Standardfelder zurück, die mit dem Datensatz verknüpft sind, sowie alle benutzerdefinierten Felder und Werte, auf die die Verbindung zugreift. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Sie müssen über ausreichende Berechtigungen für den Zugriff auf den Datensatz in [!DNL Workfront Proof] verfügen, um diese Informationen abrufen zu können.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Korrekturabzugs-ID]</td> 
   <td> <p>Geben Sie die eindeutige ID des Korrekturabzugs ein, die auf der Seite [!UICONTROL Korrekturabzugsdetails] zu finden ist. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Frist]</td> 
   <td> <p>Geben Sie die Frist an, bis zu der der Korrekturabzug erstellt werden soll. Verwenden Sie das Datumsformat <code>YYYY-MM-DD hh:mm</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Standard-E-Mail-Benachrichtigungen für Abonnenten]</td> 
   <td>Wählen Sie aus, welche der folgenden standardmäßigen E-Mail-Benachrichtigungseinstellungen Sie für den erstellten Korrekturabzug verwenden möchten.
    <ul>
     <li> [!UICONTROL Alle neuen Kommentare und Antworten]</li>
     <li>[!UICONTROL antwortet auf meine Kommentare]</li>
     <li>[!UICONTROL Tägliche Zusammenfassung]</li>
     <li> [!UICONTROL Stündliche Zusammenfassung]</li>
     <li> [!Nur UICONTROL-Entscheidungen]</li>
     <li> [!UICONTROL deaktiviert]</li>
    </ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Standardrolle]</td> 
   <td>Wählen Sie die Standardrolle für den Korrekturabzug aus.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Abonnement-E-Mail deaktivieren]</td> 
   <td>Wählen Sie aus, ob Sie die Abonnement-E-Mail für diesen Korrekturabzug deaktivieren möchten.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Abonnements aktivieren]</td> 
   <td>Wählen Sie aus, ob Personen, die nicht Teilnehmer sind, den Testversand abonnieren dürfen.<br>Wenn Sie diese Option auswählen, können Sie auch eine Option im Feld [!UICONTROL Standardrolle] auswählen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Abonnementvalidierung aktivieren]</td> 
   <td>Wählen Sie aus, ob Sie die Validierung von Abonnement-E-Mails aktivieren möchten. Wenn diese Option aktiviert ist, muss der Abonnent auf einen Link in einer E-Mail klicken, um auf einen Korrekturabzug zuzugreifen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team-URL aktivieren]</td> 
   <td>Wählen Sie aus, ob der erstellte Korrekturabzug die Team-URL ausblenden oder anzeigen soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sperren Sie den Korrekturabzug, wenn alle erforderlichen Entscheidungen getroffen werden]</td> 
   <td>Geben Sie an, ob der Korrekturabzug, der erstellt wird, nach allen erforderlichen Entscheidungen gesperrt werden soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nachricht]</td> 
   <td>Geben Sie eine Nachricht ein, die Sie dem Testversand beifügen möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Korrekturabzugs-ID] </td> 
   <td>Geben Sie die ID des Korrekturabzugs ein, den Sie aktualisieren möchten, oder mappen Sie sie.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Korrekturabzug-Name]</td> 
   <td>Geben Sie den Namen des Korrekturabzugs ein, den Sie aktualisieren möchten, oder mappen Sie ihn.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Anmeldung erforderlich]</td> 
   <td> <p>Geben Sie an, ob für den erstellten Korrekturabzug eine Anmeldung erforderlich sein soll. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Versionen anzeigen wie]</td> 
   <td>Wählen Sie aus, ob ein Link zu anderen Versionen dieses Korrekturabzugs angezeigt werden soll.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Betreff]</td> 
   <td>Betreff des Testversands eingeben oder zuordnen</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Datei hochladen]

Dieses Aktionsmodul lädt eine Datei zur Verwendung mit dem Modul [!UICONTROL Korrekturabzug erstellen] in [!DNL Workfront Proof] hoch.

Das Modul gibt eine Hash-ID für die hochgeladene Datei zurück. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source-Datei]</td> 
   <td> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Suchvorgänge

* [[!UICONTROL Workflow-Vorlagen auflisten]](#list-workflow-templates)
* [[!UICONTROL Suche]](#search)

#### [!UICONTROL Workflow-Vorlagen auflisten]

Dieses Suchmodul listet alle verfügbaren Workflow-Vorlagen auf.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ausgaben]</td> 
   <td> <p>Wählen Sie die Informationen aus, die im Ausgabepaket für dieses Modul enthalten sein sollen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Geben Sie die maximale Anzahl von Vorlagen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Suche]

Dieses Suchmodul sucht in einem -Objekt nach Datensätzen, [!DNL Workfront Proof] mit der angegebenen Suchanfrage übereinstimmen.

Das Modul gibt die ID des Korrekturabzugs zurück, wenn es nach einem Korrekturabzug sucht. Oder es gibt die Benutzer-IDs, E-Mails, Namen, Positionen und E-Mail-Aliase der Empfänger zurück, wenn es nach Empfängern sucht. Sie können diese Informationen in nachfolgenden Modulen im Szenario zuordnen.

Sie müssen über ausreichende Berechtigungen für den Zugriff auf den Datensatz in [!DNL Workfront Proof] verfügen, um diese Informationen abrufen zu können.

Beim Konfigurieren dieses Moduls werden die folgenden Felder angezeigt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Workfront Proof]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Verbindung zu Adobe Workfront Fusion herstellen - Grundanweisungen</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Suchen nach]</td> 
   <td> <p>Wählen Sie den Typ des Datensatzes aus, nach dem das Modul suchen soll.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Korrekturabzug]</strong> </p> <p>Geben Sie den Namen des Korrekturabzugs ein, nach dem Sie suchen möchten.</p> </li> 
     <li> <p><strong>[!UICONTROL recipient]</strong> </p> <p>Geben Sie die E-Mail-Adresse des Empfängers ein, nach dem Sie suchen möchten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Ergebnissatz]</td> 
   <td>Geben Sie an, ob das Modul nach <strong>[!UICONTROL All Matching Records]</strong> oder nur nach dem <strong>[!UICONTROL First Matching Record]</strong> sucht.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL sortieren nach]</td> 
   <td>Wählen Sie das Feld aus, nach dem Sie die Ergebnisse sortieren möchten.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sortierrichtung]</td> 
   <td> <p>Wählen Sie aus, ob die Ergebnisse auf- oder absteigend sortiert werden sollen.</p> </td> 
  </tr> 
 </tbody> 
</table>

