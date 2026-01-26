---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Verwenden von Vorlagen zur Verbindung von Adobe Workfront Fusion und Jira
description: Verwenden Sie diese Vorlagen, um Workflows zwischen Adobe Workfront Fusion und Jira zu automatisieren.
author: Becky
feature: Workfront Fusion
source-git-commit: 4ede5c7a75725a6540d6a8ff9cd056e6147d5c55
workflow-type: tm+mt
source-wordcount: '4171'
ht-degree: 3%

---

# Verwenden von Vorlagen zur Verbindung von Adobe Workfront Fusion und Jira

Adobe Workfront Fusion bietet Vorlagen zur Automatisierung gängiger Workflows zwischen Fusion und Jira.

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
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Workfront: Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</p><p>Jira: Sie müssen über eine Lizenz für Jira Cloud verfügen</p>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Konfigurationen der Zugriffsebene</td> 
   <td> <p>Workfront: Berechtigung zum Erstellen von Benutzenden, benutzerdefinierten Formularen und benutzerdefinierten Feldern.</p> <p>Jira: Berechtigungen zum Erstellen von Benutzern und benutzerdefinierten Feldern und zum Ändern von Bildschirmen und Webhooks.</td> 
  </tr> 
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Voraussetzungen

### Workfront

* Sie müssen über ein technisches Konto in der Adobe Developer Console verfügen.

  Weitere Informationen und Anweisungen finden Sie unter [Einrichtung technischer Konten](https://developer.adobe.com/cloud-storage/guides/getting-started/technical-account-setup) in der Dokumentation zu Adobe.
* Sie müssen Systemadministrator-Berechtigungen auf das technische Konto im Bereich Adobe Admin Console-Produktprofile anwenden.

  Informationen und Anweisungen finden Sie unter [Erstellen von Systemadministratoren in Workfront mit der Adobe Admin Console](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console#create-system-administrators-in-workfront-with-the-adobe-admin-console)

### Jira

Wenn Sie die OAuth2-Autorisierung für Jira verwenden (empfohlen), müssen Sie eine OAuth2-Anwendung unter [https://developer.atlassian.com/console](https://developer.atlassian.com/console) einrichten. Weitere Informationen und Anweisungen finden Sie unter [Erstellen einer OAuth2-Verbindung zu Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#create-an-oauth2-connection-to-jira) im Artikel Jira-Module.

<!--

When configuring this application, you will need the following scopes:

* `read:jira-work` 
* `read:jira-user`
* `write:jira-work`

-->

## Annahmen

Diese Module setzen Folgendes voraus:

* Workfront ist die wahre Quelle des gesamten Marketing-Kampagnenprojekts
* Jira wird von technischen Teams verwendet und erfüllt einen Teil eines Projekts, das in Workfront begonnen hat.
* Nicht alle Jira-Benutzer haben Zugriff auf Workfront oder umgekehrt.
* Workfront und Jira werden in der Cloud gehostet.

## Datenmodell (Feldzuordnungen)


| Workfront | Jira | Richtung | Anmerkungen |
|---|---|---|---|
| ObjId | WF-ID * | WF → Jira | Bei der Erstellung eines Jira-Problems |
| Jira-Schlüssel * | Problemschlüssel | Jira → WF | Bei der Erstellung eines Jira-Problems |
| Jira-URL * | – | Jira → WF | Vom Benutzer klickbarer Link in WF zu Jira |
| – | WF-Link * | WF → Jira | Vom Benutzer klickbarer Link in Jira zu WF |
| Name | Zusammenfassung | WF → Jira |  |
| Beschreibung | Beschreibung | WF → Jira |  |
| Status | WF-Status | WF → Jira | WF-Status |
| Jira-Status * | Status | Jira → WF | Jira-Status |
| Geplantes Abschlussdatum | Fälligkeitsdatum | WF → Jira | Geplantes Abschlussdatum |
| Anmerkungen | Kommentare | WF ↔ Jira | Bidirektionale Kopie |
| Dokument | Anhang | WF → Jira | als Anhänge zur Anfrageerstellung und als Kommentare zu neuen Dokumenten nach der Erstellung. |

\* Diese Felder werden im Rahmen dieser Integrationskonfiguration konfiguriert. Anweisungen finden Sie unter [Konfigurieren von Voraussetzungen in Workfront, Jira und Workfront Fusion](/help/workfront-fusion/create-and-manage-templates/use-jira-scenario-templates.md#configure-prerequisites-in-workfront-jira-and-workfront-fusion).

## Konfigurieren der Voraussetzungen in Workfront, Jira und Workfront Fusion

Um die Jira-Integrationsvorlagen zu verwenden, müssen Sie die folgenden Konfigurationen durchführen:

* [Jira konfigurieren](#configure-jira)
* [Konfigurieren von Workfront](#configure-workfront)
* [Konfigurieren von Verbindungen in Workfront Fusion](#configure-connections-in-workfront-fusion)

### Jira konfigurieren

Um diese Module verwenden zu können, muss in Jira Folgendes erstellt werden:

* Einen Benutzer für die Systemintegration
* Drei spezifische benutzerdefinierte Felder

#### Erstellen eines Benutzers für die Systemintegration in Jira

1. Erstellen Sie in Jira einen bestimmten Benutzer namens „Systemintegrationsbenutzer“. Dieser Benutzer sollte nur von Workfront Fusion verwendet werden und keinen menschlichen Benutzer darstellen. Die Anmeldeinformationen dieses Benutzers werden von Workfront Fusion-Verbindungen verwendet.

#### Erstellen erforderlicher benutzerdefinierter Felder in Jira

Diese Integration erwartet drei spezifische Felder in dem Jira-Konto, mit dem sie eine Verbindung herstellt. Ohne diese Felder ist die Integration nicht erfolgreich

1. Wechseln Sie in Jira zu **Einstellungen** (Zahnradsymbol) und wählen Sie **Arbeitselemente** aus.
1. Wählen Sie in der linken Navigation die Option **Benutzerdefinierte Felder**.
1. Klicken Sie in der rechten oberen Ecke des Bildschirms auf **Benutzerdefiniertes Feld erstellen.**
1. Erstellen Sie die folgenden Felder:

   | Feldname | Feldtyp |
   |---|---|
   | WF-ID | Textfeld (einzeilig) |
   | WF-Status | Textfeld (einzeilig) |
   | WF-Link | URL-Feld |

   Informationen zum Erstellen von Links in Jira finden Sie in der Jira-Dokumentation zum Erstellen von Feldern .
1. Fügen Sie die neu erstellten Felder dem Bildschirm hinzu, der mit Ihrem Jira-Projekt verknüpft ist.

   Informationen zu Bildschirmen in Jira finden Sie in der Jira-Dokumentation unter Einrichten von Arbeitselementbildschirmen .


### Konfigurieren von Workfront

Um diese Module verwenden zu können, muss in Workfront Folgendes erstellt werden:

* Einen Benutzer für die Systemintegration
* Ein bestimmtes benutzerdefiniertes Formular

#### Erstellen eines Systemintegrationsbenutzers in Workfront

1. Erstellen Sie in Workfront einen Benutzer für die Systemintegration. Dieser Benutzer wird nur von Workfront Fusion verwendet und stellt keinen menschlichen Benutzer dar. Aufgaben, die diesem Benutzer zugewiesen sind, führen zu Triggern bei dem Szenario, das Workfront mit Jira synchronisiert.

   Anweisungen finden Sie unter [Benutzer hinzufügen](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/add-users) in der Dokumentation zu Workfront.

#### Erstellen eines benutzerdefinierten Formulars in Workfront

1. Beginnen Sie in Workfront mit der Erstellung eines benutzerdefinierten Formulars.

   Anweisungen finden Sie unter [Erstellen eines benutzerdefinierten Formulars](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/design-a-form/design-a-form) in der Dokumentation zu Workfront.
1. Benennen Sie das Formular **JIRA-Felder**.
1. Fügen Sie die folgenden Felder in das benutzerdefinierte Formular ein:

| Feldname | Feldtyp |
|---|---|
| Jira Key | Einzeiliges Textfeld |
| Jira-URL | Einzeiliges Textfeld |
| Jira-Status | Einzeiliges Textfeld |

1. Fügen Sie alle zusätzlichen Felder hinzu, die Sie zwischen Jira und Workfront zuordnen möchten.
1. Speichern Sie das benutzerdefinierte Formular.

>[!NOTE]
>
>Es wird empfohlen, dieses Formular nicht von anderen Benutzern bearbeiten zu lassen. Sie können dies erreichen, indem Sie sicherstellen, dass alle Benutzenden, die zum benutzerdefinierten Formular hinzugefügt werden, nur Lesezugriff haben.
>
>Anweisungen finden Sie unter [Freigeben eines benutzerdefinierten Formulars](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/manage-custom-forms/share-access-to-a-custom-form) in der Dokumentation zu Workfront.

### Konfigurieren von Verbindungen in Workfront Fusion

Sie müssen die Benutzer für die Systemintegration in Jira und Workfront erstellt haben, bevor Sie Verbindungen erstellen können.

Stellen Sie beim Erstellen dieser Verbindungen sicher, dass Sie die Anmeldeinformationen der erstellten Benutzer der Systemintegration verwenden.

Bei Bedarf können Sie diese Verbindungen im Rahmen der Konfiguration der Vorlagen erstellen.

* Anweisungen zum Erstellen einer Verbindung zu Workfront finden Sie unter [Verbinden von Workfront mit Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#connect-workfront-to-workfront-fusion) im Artikel Workfront-Module.
* Anweisungen zum Erstellen einer Verbindung zu Jira finden Sie unter [Verbinden von Jira mit Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion) im Artikel Jira Software-Module .


## Szenarios

Acht einsatzbereite Vorlagen für Jira sollen dabei helfen, gängige Workflows zu replizieren und die Implementierung zu beschleunigen. Vorlagen können vollständig an spezifische Geschäftsanforderungen angepasst und bei sich ändernden Anforderungen erweitert werden.

Sie müssen nicht alle Szenarien implementieren. Für die minimale Implementierung ist Szenario 1 erforderlich, das eine Integration in eine JIRA-Anfrage aus einem Arbeitsauftrag in Workfront in eine Richtung erstellt.  Sie können die zusätzlichen Szenarien hinzufügen, um für Robustheit und eine bidirektionale Interkonnektivität zwischen Workfront und JIRA zu sorgen.  Sie können auch zusätzliche Szenarien erstellen, um Fälle wie die Integration von Projekt zu Epic oder JIRA-Probleme mit Workfront-Problemen oder -Aufgaben zu behandeln.

Jede Verwendung dieser Vorlagen oder Erweiterungen dieser Vorlagen wird als benutzerdefinierte Konfiguration betrachtet, und wir empfehlen die Verwendung von Adobe Professional Services oder einem Adobe-Partner für Unterstützung und Implementierung.

* **[Workfront zu Jira: JIRA-Anfrage aus Workfront-Aufgaben- oder -Problemzuweisung erstellen](#scenario-1-workfront-to-jira-create-jira-issue-from-workfront-task-or-issue-assignment)**
* [JIRA zu Workfront: JIRA zu Workfront: Senden Sie Updates zu Problemen und Kommentare von Jira zurück an Workfront](#scenario-2-jira-to-workfront-send-updates-on-issues-and-comments-back-to-workfront-from-jira)
* [Workfront zu Jira: Änderungen an Workfront-Aufgabe zu JIRA-Problem](#scenario-3-workfront-to-jira-changes-to-workfront-task-to-jira-issue)
* [Workfront zu Jira: Änderungen an Workfront-Problem zu JIRA-Problem](#scenario-4-workfront-to-jira-changes-to-workfront-issue-to-jira-issue)
* [Workfront zu Jira: Kommentar in JIRA erstellen, wenn eine neue Notiz zu einer Aufgabe oder einem Problem in Workfront erscheint](#scenario-5-workfront-to-jira-create-comment-in-jira-when-new-note-on-workfront-task-or-issue)
* [Workfront zu Jira: Kommentar in JIRA bei gelöschter Notiz zu Workfront-Aufgabe oder -Problem erstellen](#scenario-6-workfront-to-jira-create-comment-in-jira-on-deleted-note-on-workfront-task-or-issue)
* [Workfront zu Jira: Erstellen eines Kommentars in JIRA, wenn ein neues Dokument zu einer Aufgabe oder einem Problem in Workfront erstellt wird](#scenario-7-workfront-to-jira-create-comment-in-jira-when-new-document-on-workfront-task-or-issue)
* [Workfront zu Jira: Erstellen eines Kommentars in JIRA zu einem gelöschten Dokument zu einer Workfront-Aufgabe oder einem -Problem](#scenario-8-workfront-to-jira-create-comment-in-jira-on-deleted-document-on-workfront-task-or-issue)

### Allgemeine Parameter

Verwenden Sie beim Konfigurieren dieser Vorlagen die folgenden allgemeinen Parameter:

* **JiraBaseURL**: Die Basis-URL für die Jira-Instanz. Beispiel: `https://myjira.atlassian.net/`
* **wfBaseURL**: Die Basis-URL für die Workfront-Instanz.  Normalerweise: `https://<domain>.my.workfront.com`, wobei `<domain>` Ihr bestimmter Workfront-Domain-Name ist.
* **defaultJIRAReporterID**: Die ID für den Benutzer in JIRA, der Probleme erstellt. (Beispiel: `557058:5aedf933-2312-40bc-b328-0c21314167f0`)
Sie können diese ID abrufen, indem Sie einen der folgenden Schritte ausführen:
   * Klicken Sie auf das Profil des Benutzers in JIRA und überprüfen Sie die URL in Ihrem Browser.
(Beispiel`https://myjira.atlassian.net/jira/people/<JiraUserID>`
   * Führen Sie den folgenden API-Aufruf auf Ihrer JIRA-Instanz aus, um die ID für das jeweilige Konto in JIRA abzurufen:
     `GET /rest/api/3/user/search?query=email@example.com`


### Szenario 1: Workfront zu Jira: Erstellen eines JIRA-Problems über eine Workfront-Aufgabe oder -Problemzuweisung

Dieses Szenario erzeugt ein Jira-Problem, wenn dem Benutzer der Systemintegration eine Workfront-Aufgabe oder ein -Problem zugewiesen wird. Das Szenario füllt die Felder Zusammenfassung, Beschreibung, Fälligkeitsdatum, WF-Status und WF-ID aus. Nachdem das Problem erstellt wurde, werden in diesem Szenario auch die Liste der Anhänge und der Verlauf der Notizen zu der ursprünglichen Aufgabe oder dem ursprünglichen Problem in Workfront hochgeladen.

Wenn eine Workfront-Aufgabe zugewiesen wird, ist das Problem in Jira eine Aufgabe. Wenn ein Workfront-Problem zugewiesen wird, ist das Jira-Problem ein Fehler.

+++**Erweitern Sie , um Anweisungen zur Konfiguration von Szenario 1 :Workfront Jira anzuzeigen: Erstellen eines JIRA-Problems über eine Workfront-Aufgabe oder -Problemzuweisung**

#### Konfigurieren des Trigger-Moduls

1. Klicken Sie auf **Registerkarte** Vorlagen![ (Vorlagensymbol](assets/templates-icon.png) im linken Navigationsbereich.
1. Suchen Sie mithilfe der Suchleiste in der linken oberen Ecke des Bildschirms nach der Vorlage. Sie können nach Vorlagennamen oder eingeschlossenen Programmen suchen.
1. Klicken Sie auf die Vorlage **Workfront zu Jira: JIRA-Problem aus Workfront-Aufgabe oder -** erstellen .

   Es öffnet sich eine Ansicht der Vorlage mit Informationen und einer Animation des Datenflusses.
1. Beginnen Sie im ersten Modul mit dem Hinzufügen eines Webhooks.
1. Wählen Sie die Workfront-Verbindung aus, die Sie unter [Konfigurieren von Verbindungen in Workfront Fusion](#configure-connections-in-workfront-fusion) erstellt haben.
1. Wählen Sie **Feld** Datensatztyp“ `Assignment` aus.
1. Wählen Sie im **Status** die Option `New state` aus.
1. Konfigurieren Sie den Filter mit den folgenden Vorgängen mithilfe der Option **Und**:

   | Feld | Benutzerin oder Benutzer | Wert |
   |---|---|---|
   | assignedToID | Gleich | (Workfront-ID des Systemintegrationsbenutzers eingeben) |
   | Aufgaben-ID | Vorhanden |  |
   | projectID | Gleich | (Geben Sie die ID des Projekts oder der Projekte ein, die der Webhook überwachen soll.) |

1. Aktivieren Sie die **Von dieser Verbindung vorgenommene Aktualisierungen ausschließen**.
1. Wählen Sie **Feld „Datensatzherkunft** nur neuen Datensatz aus.
1. Klicken Sie **Speichern**, um den Webhook zu speichern, und klicken Sie dann auf **OK**, um das Trigger-Modul zu speichern.
1. Fahren Sie fort [Vorlagenmodule mit Workfront und Jira verbinden](#connect-template-modules-to-workfront-and-jira)

#### Verbinden von Vorlagenmodulen mit Workfront und Jira

1. Wählen Sie **jedes** Workfront-Modul im Feld Verbindung die Workfront-Verbindung aus, die Sie unter [Konfigurieren von Verbindungen in Workfront Fusion](#configure-connections-in-workfront-fusion) erstellt haben, und klicken Sie dann auf **OK**, um die Verbindung zu diesem Modul zu speichern.
1. Wählen Sie **jedes** Jira-Modul im Feld Verbindung die Workfront-Verbindung aus, die Sie unter [Konfigurieren von Verbindungen in Workfront Fusion](#configure-connections-in-workfront-fusion) erstellt haben, und klicken Sie dann auf **OK**, um die Verbindung zu diesem Modul zu speichern.
1. Fahren Sie [Aktualisieren des Moduls Allgemeine Parameter](#update-the-general-parameters-module) fort.

#### Aktualisieren Sie das Modul Allgemeine Parameter .

1. Klicken Sie im zweiten Modul der Vorlage (Umgebungsdetails festlegen) für jede der folgenden Variablen auf **Element hinzufügen** und geben Sie den Namen und Wert der Variablen ein

   | Variablenname | Variablenwert |
   |---|---|
   | defaultJiraReporterID | Geben Sie die ID des Standardbenutzers ein, wenn der Erstellende Benutzer nicht in Jira vorhanden ist. Sie können diese Benutzer-ID finden, indem Sie auf das Profil des Benutzers klicken und die URL des Browsers überprüfen. Beispiel: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Geben Sie die Basis-URL des Jira-Kontos ein, mit dem Sie eine Verbindung herstellen. |
   | wfBaseURL | Geben Sie die Basis-URL des Workfront-Kontos ein, mit dem Sie eine Verbindung herstellen. |

1. Weiter zu [Benutzerdefinierte Felder in Jira zuordnen](#map-custom-fields-in-jira)

<!--#### Map custom fields in Jira. 

Awaiting feedback-->

+++

### Szenario 2: JIRA an Workfront: Von Jira Aktualisierungen zu Problemen und Kommentare an Workfront zurücksenden

In diesem Szenario wird eine Workfront-Aufgabe oder ein -Problem erstellt, wenn ein Problem in Jira erstellt wird.

>[!NOTE]
>
>Dieses Szenario erfordert eine OAuth2-Verbindung für Jira.
>Um die OAuth2-Autorisierung für Jira zu verwenden, müssen Sie eine OAuth2-Anwendung unter [https://developer.atlassian.com/console](https://developer.atlassian.com/console) einrichten. Informationen und Anweisungen finden Sie in der Jira-Dokumentation.

+++**Erweitern Sie , um Anweisungen zur Konfiguration von Szenario 2: JIRA für Workfront anzuzeigen: Senden Sie Updates zu Problemen und Kommentare von Jira zurück an Workfront**

1. Klicken Sie auf **Registerkarte** Vorlagen![ (Vorlagensymbol](assets/templates-icon.png) im linken Navigationsbereich.
1. Suchen Sie mithilfe der Suchleiste in der linken oberen Ecke des Bildschirms nach der Vorlage. Sie können nach Vorlagennamen oder eingeschlossenen Programmen suchen.
1. Klicken Sie auf **Teil 2: JIRA an Workfront: Senden Sie von der Jira2-Vorlage Aktualisierungen zu Problemen und Kommentaren** Workfront zurück.

   Es öffnet sich eine Ansicht der Vorlage mit Informationen und einer Animation des Datenflusses.
1. Beginnen Sie im ersten Modul mit dem Hinzufügen eines Webhooks.
1. Wählen Sie eine Verbindung aus, die die Anmeldeinformationen für den Systemintegrationsbenutzer verwendet, oder erstellen Sie eine Verbindung zu Jira mit den Anmeldeinformationen für die Systemintegration.

* Anweisungen zum Erstellen einer Verbindung zu Jira finden Sie unter [Verbinden von Jira mit Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion) im Artikel Jira Software-Module .

1. Webhook-Filter konfigurieren

1. Fahren Sie fort mit [Konfigurieren eines Webhooks in Jira](#configure-a-webhook-in-jira)

#### Webhook in Jira konfigurieren

1. Erstellen Sie in Jira einen Webhook.

   Anweisungen finden Sie [Webhooks](https://developer.atlassian.com/server/jira/platform/webhooks/) in der Jira-Dokumentation.

1. Verwenden Sie beim Konfigurieren des Webhooks die folgenden Werte:

   * **JQL**: project = „yourProjectName“ (wobei yourProjectName = Name Ihres JIRA-Projekts ist)
   * **Problem**: erstellt, aktualisiert
   * **Kommentar**: erstellt, gelöscht


1. Fahren Sie fort [Vorlagenmodule mit Workfront und Jira verbinden (Modul 2)](#connect-template-modules-to-workfront-and-jira-module-2)

#### Vorlagenmodule mit Workfront und Jira verbinden (Modul 2)

1. Wählen Sie **jedes** Workfront-Modul im Feld Verbindung die Workfront-Verbindung aus, die Sie unter [Konfigurieren von Verbindungen in Workfront Fusion](#configure-connections-in-workfront-fusion) erstellt haben, und klicken Sie dann auf **OK**, um die Verbindung zu diesem Modul zu speichern.
1. Wählen Sie **jedes** Jira-Modul im Feld Verbindung die Workfront-Verbindung aus, die Sie unter [Konfigurieren von Verbindungen in Workfront Fusion](#configure-connections-in-workfront-fusion) erstellt haben, und klicken Sie dann auf **OK**, um die Verbindung zu diesem Modul zu speichern.
   <!--#### Map custom fields-->

+++

### Szenario 3: Workfront zu Jira: Änderungen an Workfront-Aufgabe zu JIRA-Problem

+++**Erweitern Sie , um Anweisungen zum Konfigurieren von Szenario 3: WF-zu-Jira-Änderungen (Aufgaben) anzuzeigen**

1. Klicken Sie auf **Registerkarte** Vorlagen![ (Vorlagensymbol](assets/templates-icon.png) im linken Navigationsbereich.
1. Suchen Sie mithilfe der Suchleiste in der linken oberen Ecke des Bildschirms nach der Vorlage. Sie können nach Vorlagennamen oder eingeschlossenen Programmen suchen.
1. Klicken Sie auf die **Teil 3: Workfront zu Jira: Änderungen an Workfront-Aufgabe zu JIRA-Problem**-Vorlage.

   Es öffnet sich eine Ansicht der Vorlage mit Informationen und einer Animation des Datenflusses.

1. Klicken Sie auf die Vorlage, um den Editor aufzurufen.
1. Wählen Sie die Organisation und das Team aus, denen dieses Szenario gehört.
1. Beginnen Sie im ersten Modul mit dem Hinzufügen eines Webhooks.
1. Wählen Sie im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet.
1. Wählen Sie **Feld** Datensatztyp“ `Task` aus.
1. Wählen Sie im **Status** die Option `New state` aus.
1. Konfigurieren Sie den Filter mit den folgenden Vorgängen mithilfe der Option **Und**:

   | Feld | Benutzerin oder Benutzer | Wert |
   |---|---|---|
   | assignedToID | Gleich | Geben Sie die Workfront-ID des Systemintegrationsbenutzers ein |
   | projectID | Gleich | Geben Sie die ID des Projekts bzw. der Projekte ein, die der Webhook überwachen soll. |
   | DE: Jira Key | Vorhanden |  |

1. Aktivieren Sie die **Von dieser Verbindung vorgenommene Aktualisierungen ausschließen**.
1. Wählen Sie **Feld &quot;**&quot; die Option &quot;`Updated record only`&quot;.
1. Klicken Sie **Speichern**, um den Webhook zu speichern, und klicken Sie dann auf **OK**, um das Trigger-Modul zu speichern.
1. Legen Sie im **Set JIRA Variables**-Modul die folgenden Variablen fest und klicken Sie dann auf **OK**, um das Modul zu speichern.

   | Variablenname | Variablenwert |
   |---|---|
   | defaultJiraReporterID | Dies ist die ID des Standardbenutzers, wenn der Erstellende Benutzer nicht in Jira vorhanden ist. Sie können diese Benutzer-ID finden, indem Sie auf das Profil des Benutzers klicken und die URL des Browsers überprüfen. Beispiel: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Die Basis-URL des Jira-Kontos, mit dem Sie eine Verbindung herstellen. |
   | wfBaseURL | Die Basis-URL des Workfront-Kontos, mit dem Sie eine Verbindung herstellen. |

1. Wählen **in** Workfront-Modul im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.
1. Wählen **in jedem**-Modul im Feld Verbindung die Jira-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.

+++

### Szenario 4: Workfront zu Jira: Änderungen am Workfront-Problem zu JIRA-Problem

Dieses Szenario sendet Aktualisierungen von Workfront-Problemen an zuvor verbundene JIRA-Probleme.

+++**Erweitern Sie , um Anweisungen zur Konfiguration von Szenario 4: Workfront zu Jira: Änderungen an Workfront-Problem zu JIRA-Problem anzuzeigen**

1. Klicken Sie auf **Registerkarte** Vorlagen![ (Vorlagensymbol](assets/templates-icon.png) im linken Navigationsbereich.
1. Suchen Sie mithilfe der Suchleiste in der linken oberen Ecke des Bildschirms nach der Vorlage. Sie können nach Vorlagennamen oder eingeschlossenen Programmen suchen.
1. Klicken Sie auf **Vorlage „Szenario 4: WF-zu-Jira-Änderungen (Probleme**&quot;.

   Es öffnet sich eine Ansicht der Vorlage mit Informationen und einer Animation des Datenflusses.

1. Klicken Sie auf die Vorlage, um den Editor aufzurufen.
1. Wählen Sie die Organisation und das Team aus, denen dieses Szenario gehört.
1. Beginnen Sie im ersten Modul mit dem Hinzufügen eines Webhooks.
1. Wählen Sie im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet.
1. Wählen Sie **Feld** Datensatztyp“ `Issues` aus.
1. Wählen Sie im **Status** die Option `New state` aus.
1. Konfigurieren Sie den Filter mit den folgenden Vorgängen mithilfe der Option **Und**:

   | Feld | Benutzerin oder Benutzer | Wert |
   |---|---|---|
   | assignedToID | Gleich | Geben Sie die Workfront-ID des Systemintegrationsbenutzers ein |
   | projectID | Gleich | Geben Sie die ID des Projekts bzw. der Projekte ein, die der Webhook überwachen soll. |
   | DE: Jira Key | Vorhanden |  |

1. Aktivieren Sie die **Von dieser Verbindung vorgenommene Aktualisierungen ausschließen**.
1. Wählen Sie **Feld &quot;**&quot; die Option &quot;`Updated record only`&quot;.
1. Klicken Sie **Speichern**, um den Webhook zu speichern, und klicken Sie dann auf **OK**, um das Trigger-Modul zu speichern.
1. Legen Sie im **Set JIRA Variables**-Modul die folgenden Variablen fest und klicken Sie dann auf **OK**, um das Modul zu speichern.

   | Variablenname | Variablenwert |
   |---|---|
   | defaultJiraReporterID | Dies ist die ID des Standardbenutzers, wenn der Erstellende Benutzer nicht in Jira vorhanden ist. Sie können diese Benutzer-ID finden, indem Sie auf das Profil des Benutzers klicken und die URL des Browsers überprüfen. Beispiel: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Die Basis-URL des Jira-Kontos, mit dem Sie eine Verbindung herstellen. |
   | wfBaseURL | Die Basis-URL des Workfront-Kontos, mit dem Sie eine Verbindung herstellen. |

1. Wählen **in** Workfront-Modul im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.
1. Wählen **in jedem**-Modul im Feld Verbindung die Jira-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.

+++

### Szenario 5: Workfront zu Jira: Erstellen eines Kommentars in JIRA, wenn eine neue Notiz zu einer Aufgabe oder einem Problem in Workfront erstellt wird

+++**Erweitern Sie , um Anweisungen zum Konfigurieren von Szenario 5: Workfront zu Jira: Kommentar in JIRA erstellen, wenn eine neue Notiz zur Aufgabe oder zum Problem von Workfront erscheint**

1. Klicken Sie auf **Registerkarte** Vorlagen![ (Vorlagensymbol](assets/templates-icon.png) im linken Navigationsbereich.
1. Suchen Sie mithilfe der Suchleiste in der linken oberen Ecke des Bildschirms nach der Vorlage. Sie können nach Vorlagennamen oder eingeschlossenen Programmen suchen.
1. Klicken Sie auf **Vorlage „Szenario 5: Neue WF-zu-Jira-Notizen (Aufgaben und Probleme** .

   Es öffnet sich eine Ansicht der Vorlage mit Informationen und einer Animation des Datenflusses.
1. Beginnen Sie im ersten Modul mit dem Hinzufügen eines Webhooks.
1. Wählen Sie im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet.
1. Wählen Sie **Feld** Datensatztyp“ `Note` aus.
1. Wählen Sie im **Status** die Option `New state` aus.
1. Konfigurieren Sie den Filter wie folgt:

   | Feld | Benutzerin oder Benutzer | Wert |
   |---|---|---|
   | projectID<br>AND<br>TaskID | Equals<br><br>exists | Geben Sie die ID des Projekts bzw. der Projekte ein, die der Webhook überwachen soll. |
   | ODER |  |  |
   | projectID<br>AND<br>OpTaskID | Equals<br><br>exists | Geben Sie die ID des Projekts bzw. der Projekte ein, die der Webhook überwachen soll. |

1. Aktivieren Sie die **Von dieser Verbindung vorgenommene Aktualisierungen ausschließen**.
1. Wählen Sie **Feld &quot;**&quot; die Option &quot;`New record only`&quot;.
1. Klicken Sie **Speichern**, um den Webhook zu speichern, und klicken Sie dann auf **OK**, um das Trigger-Modul zu speichern.
1. Legen Sie im Modul **Variablen festlegen** die folgenden Variablen fest und klicken Sie dann auf **OK**, um das Modul zu speichern.

   | Variablenname | Variablenwert |
   |---|---|
   | defaultJiraReporterID | Dies ist die ID des Standardbenutzers, wenn der Erstellende Benutzer nicht in Jira vorhanden ist. Sie können diese Benutzer-ID finden, indem Sie auf das Profil des Benutzers klicken und die URL des Browsers überprüfen. Beispiel: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Die Basis-URL des Jira-Kontos, mit dem Sie eine Verbindung herstellen. |
   | wfBaseURL | Die Basis-URL des Workfront-Kontos, mit dem Sie eine Verbindung herstellen. |

1. Wählen **in** Workfront-Modul im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.
1. Wählen **in jedem**-Modul im Feld Verbindung die Jira-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.

+++

### Szenario 6: Workfront zu Jira: Erstellen eines Kommentars in JIRA bei gelöschter Anmerkung zu Workfront-Aufgabe oder -Problem

+++**Erweitern Sie , um Anweisungen zur Konfiguration von Szenario 6: Workfront zu Jira: Kommentar in JIRA bei gelöschter Notiz zu Workfront-Aufgabe oder -Problem erstellen anzuzeigen**

1. Klicken Sie auf **Registerkarte** Vorlagen![ (Vorlagensymbol](assets/templates-icon.png) im linken Navigationsbereich.
1. Suchen Sie mithilfe der Suchleiste in der linken oberen Ecke des Bildschirms nach der Vorlage. Sie können nach Vorlagennamen oder eingeschlossenen Programmen suchen.
1. Klicken Sie auf **Vorlage „Szenario 6: WF-zu-Jira - Notizen (Aufgaben und Probleme) entfernen**.

   Es öffnet sich eine Ansicht der Vorlage mit Informationen und einer Animation des Datenflusses.
1. Beginnen Sie im ersten Modul mit dem Hinzufügen eines Webhooks.
1. Wählen Sie im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet.
1. Wählen Sie **Feld** Datensatztyp“ `Note` aus.
1. Wählen Sie im **Status** die Option `New state` aus.
1. Konfigurieren Sie den Filter wie folgt:

   | Feld | Benutzerin oder Benutzer | Wert |
   |---|---|---|
   | projectID<br>AND<br>TaskID | Equals<br><br>exists | Geben Sie die ID des Projekts bzw. der Projekte ein, die der Webhook überwachen soll. |
   | ODER |  |  |
   | projectID<br>AND<br>OpTaskID | Equals<br><br>exists | Geben Sie die ID des Projekts bzw. der Projekte ein, die der Webhook überwachen soll. |

1. Aktivieren Sie die **Von dieser Verbindung vorgenommene Aktualisierungen ausschließen**.
1. Wählen Sie **Feld &quot;**&quot; die Option &quot;`Deleted record only`&quot;.
1. Klicken Sie **Speichern**, um den Webhook zu speichern, und klicken Sie dann auf **OK**, um das Trigger-Modul zu speichern.
1. Legen Sie im zweiten Modul die folgenden Variablen fest und klicken Sie dann auf **OK**, um das Modul zu speichern.

   | Variablenname | Variablenwert |
   |---|---|
   | defaultJiraReporterID | Dies ist die ID des Standardbenutzers, wenn der Erstellende Benutzer nicht in Jira vorhanden ist. Sie können diese Benutzer-ID finden, indem Sie auf das Profil des Benutzers klicken und die URL des Browsers überprüfen. Beispiel: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Die Basis-URL des Jira-Kontos, mit dem Sie eine Verbindung herstellen. |
   | wfBaseURL | Die Basis-URL des Workfront-Kontos, mit dem Sie eine Verbindung herstellen. |

1. Wählen **in** Workfront-Modul im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.
1. Wählen **in jedem**-Modul im Feld Verbindung die Jira-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.

+++

### Szenario 7: Workfront zu Jira: Erstellen eines Kommentars in JIRA, wenn ein neues Dokument zu einer Aufgabe oder einem Problem in Workfront erstellt wird

+++**Erweitern Sie , um Anweisungen zur Konfiguration von Szenario 7: Workfront zu Jira: Kommentar in JIRA erstellen, wenn ein neues Dokument zu Workfront-Aufgaben oder -Problemen erstellt wird**

1. Klicken Sie auf **Registerkarte** Vorlagen![ (Vorlagensymbol](assets/templates-icon.png) im linken Navigationsbereich.
1. Suchen Sie mithilfe der Suchleiste in der linken oberen Ecke des Bildschirms nach der Vorlage. Sie können nach Vorlagennamen oder eingeschlossenen Programmen suchen.
1. Klicken Sie auf **Vorlage „Szenario 7: Neue Anlagen (Aufgaben und Probleme) von WF-zu-Jira**.

   Es öffnet sich eine Ansicht der Vorlage mit Informationen und einer Animation des Datenflusses.
1. Beginnen Sie im ersten Modul mit dem Hinzufügen eines Webhooks.
1. Wählen Sie im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet.
1. Wählen Sie **Feld** Datensatztyp“ `Document` aus.
1. Wählen Sie im **Status** die Option `New state` aus.
1. Konfigurieren Sie den Filter mit den folgenden Vorgängen mithilfe der Option **Und**:

   | Feld | Benutzerin oder Benutzer | Wert |
   |---|---|---|
   | assignedToID | Gleich | Geben Sie die Workfront-ID des Systemintegrationsbenutzers ein |
   | projectID | Gleich | Geben Sie die ID des Projekts bzw. der Projekte ein, die der Webhook überwachen soll. |

1. Legen Sie im zweiten Modul die folgenden Variablen fest.

   | Variablenname | Variablenwert |
   |---|---|
   | defaultJiraReporterID | Dies ist die ID des Standardbenutzers, wenn der Erstellende Benutzer nicht in Jira vorhanden ist. Sie können diese Benutzer-ID finden, indem Sie auf das Profil des Benutzers klicken und die URL des Browsers überprüfen. Beispiel: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Die Basis-URL des Jira-Kontos, mit dem Sie eine Verbindung herstellen. |
   | wfBaseURL | Die Basis-URL des Workfront-Kontos, mit dem Sie eine Verbindung herstellen. |

1. Aktivieren Sie die **Von dieser Verbindung vorgenommene Aktualisierungen ausschließen**.
1. Wählen Sie **Feld &quot;**&quot; die Option &quot;`New record only`&quot;.
1. Klicken Sie **Speichern**, um den Webhook zu speichern, und klicken Sie dann auf **OK**, um das Trigger-Modul zu speichern.
1. Wählen **in** Workfront-Modul im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.
1. Wählen **in jedem**-Modul im Feld Verbindung die Jira-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.

+++

### Szenario 8: Workfront zu Jira: Erstellen eines Kommentars in JIRA zu einem gelöschten Dokument zu einer Workfront-Aufgabe oder einem -Problem

+++**Erweitern Sie , um Anweisungen zur Konfiguration von Szenario 8: Workfront zu Jira: Erstellen Sie einen Kommentar in JIRA zu einem gelöschten Dokument zu Workfront-Aufgaben oder -Problemen**

1. Klicken Sie auf **Registerkarte** Vorlagen![ (Vorlagensymbol](assets/templates-icon.png) im linken Navigationsbereich.
1. Suchen Sie mithilfe der Suchleiste in der linken oberen Ecke des Bildschirms nach der Vorlage. Sie können nach Vorlagennamen oder eingeschlossenen Programmen suchen.
1. Klicken Sie auf **Vorlage „Szenario 8: WF-zu-Jira - Anhänge (Aufgaben und Probleme) entfernen**.

   Es öffnet sich eine Ansicht der Vorlage mit Informationen und einer Animation des Datenflusses.
1. Beginnen Sie im ersten Modul mit dem Hinzufügen eines Webhooks.
1. Wählen Sie im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet.
1. Wählen Sie **Feld** Datensatztyp“ `Document` aus.
1. Wählen Sie im **Status** die Option `New state` aus.
1. Konfigurieren Sie den Filter wie folgt:

   | Feld | Benutzerin oder Benutzer | Wert |
   |---|---|---|
   | projectID<br>AND<br>TaskID | Equals<br><br>exists | Geben Sie die ID des Projekts bzw. der Projekte ein, die der Webhook überwachen soll. |
   | ODER |  |  |
   | projectID<br>AND<br>OpTaskID | Equals<br><br>exists | Geben Sie die ID des Projekts bzw. der Projekte ein, die der Webhook überwachen soll. |

1. Legen **im Modul** die folgenden Variablen fest.

   | Variablenname | Variablenwert |
   |---|---|
   | defaultJiraReporterID | Dies ist die ID des Standardbenutzers, wenn der Erstellende Benutzer nicht in Jira vorhanden ist. Sie können diese Benutzer-ID finden, indem Sie auf das Profil des Benutzers klicken und die URL des Browsers überprüfen. Beispiel: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Die Basis-URL des Jira-Kontos, mit dem Sie eine Verbindung herstellen. |
   | wfBaseURL | Die Basis-URL des Workfront-Kontos, mit dem Sie eine Verbindung herstellen. |

1. Aktivieren Sie die **Von dieser Verbindung vorgenommene Aktualisierungen ausschließen**.
1. Wählen Sie **Feld &quot;**&quot; die Option &quot;`Deleted record only`&quot;.
1. Klicken Sie **Speichern**, um den Webhook zu speichern, und klicken Sie dann auf **OK**, um das Trigger-Modul zu speichern.
1. Wählen **in** Workfront-Modul im Feld Verbindung die Workfront-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.
1. Wählen **in jedem**-Modul im Feld Verbindung die Jira-Verbindung aus, die die Anmeldeinformationen für die Systemintegration verwendet, und klicken Sie dann auf **OK**, um das Modul zu speichern.


+++

