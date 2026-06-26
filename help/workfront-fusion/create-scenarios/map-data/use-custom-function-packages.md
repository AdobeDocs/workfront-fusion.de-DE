---
title: Verwenden benutzerdefinierter Funktionspakete
description: Beim Zuordnen von Elementen können Sie Funktionen verwenden, um einfache oder komplexe Formeln zu erstellen.
author: Becky
feature: Workfront Fusion
source-git-commit: 4ec81401b5a76edd620b9779414ee578966b4315
workflow-type: tm+mt
source-wordcount: '2042'
ht-degree: 6%

---


# Verwenden benutzerdefinierter Funktionspakete

Mithilfe von Paketen können Sie Ihre eigene benutzerdefinierte Logik in Adobe Workfront Fusion erstellen und ausführen, ohne die Fusion-Benutzeroberfläche zu verlassen. Wenn die Standardmodule nicht genau das tun, was Sie benötigen, können Sie eine Funktion verwenden, um Daten umzuwandeln, eine Berechnung durchzuführen, einen externen Service aufzurufen oder eine Routine einzuschließen, die Sie wiederverwenden möchten. Anschließend können Sie sie testen, live schalten und in Ihren Szenarien verwenden.

Komplexe Funktionen erfordern möglicherweise Ressourcen wie Variablen und Abhängigkeiten wie Bibliotheken. Für diese Funktionen können Sie ein Paket erstellen, das die Funktion und ihre Ressourcen enthält.

Ein Paket kann Folgendes enthalten:

* **Funktionen**: Die Logik, die während der Ausführung eines Szenarios ausgeführt wird.
* **Variablen**: Wiederverwendbare Werte, wie eine Basis-URL oder ein API-Schlüssel, die von der Funktion im Paket verwendet werden.
* **Abhängigkeiten**: Außerhalb von Bibliotheken können Ihre Funktionen auf Folgendes angewiesen sein.
* **History**: Frühere Versionen jeder Funktion, die automatisch gespeichert wurde und auf die Sie verweisen können.


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
   <p><ul><li>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li><li>Sie benötigen eine Adobe App Builder-Lizenz, um benutzerdefinierte Funktionen verwenden zu können.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Einrichten der Verbindung zur Laufzeitumgebung

>[!NOTE]
>
>Dies ist ein einmaliges Setup.

Wenn Ihr Team diese Funktion zum ersten Mal verwendet, müssen Sie die Umgebung einrichten, in der die Funktionen ausgeführt werden. Dies ist nur einmal pro Team möglich.

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.

   Wenn die Umgebung nicht eingerichtet wurde, wird der Bildschirm **Laufzeitumgebung nicht konfiguriert** angezeigt.

1. Klicken Sie **Laufzeit initialisieren**.

1. Um einen anderen Namen als den Standardnamen einzugeben, geben Sie den Namen in das Feld **Verbindungsname** ein.

1. Wählen Sie das Adobe App Builder-Projekt aus, zu dem dieses Paket gehören soll:

   * Um ein vorhandenes Projekt auszuwählen, geben Sie zunächst den Projektnamen ein und wählen Sie ihn aus, wenn er angezeigt wird.
   * Um ein neues Projekt zu erstellen, geben Sie einen Namen ein, der noch nicht vorhanden ist, und klicken Sie auf **Neu erstellen**.
   * Wenn Sie dieses Feld leer lassen, verwendet Fusion ein Standardprojekt.

1. Wählen Sie **Weiter**.

   Fusion beendet die Einrichtung und Sie können Pakete erstellen.

   Ihre Umgebung wird als Registerkarte Verbindung oben auf der Seite angezeigt.

   ![Umgebung als Registerkarte „Verbindung“](assets/package-environment-as-connection.png)

1. (Bedingt) Um eine zusätzliche Umgebung hinzuzufügen, klicken Sie auf das Pluszeichen und befolgen Sie die Anweisungen in diesem Abschnitt.

1. (Bedingt) Um eine vorhandene Umgebung zu entfernen, bewegen Sie den Mauszeiger über die Registerkarte Umgebungsverbindung und klicken Sie auf **X** wenn sie angezeigt wird.

   >[!WARNING]
   >
   >Durch das Entfernen einer Verbindung wird Fusion von dieser Umgebung getrennt. Die darin enthaltenen Pakete sind in Fusion über diese Verbindung nicht mehr verfügbar.

## Erstellen und Öffnen eines Pakets

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.

1. Wählen Sie die Registerkarte für die Verbindung aus, in der Sie arbeiten möchten.

1. Klicken Sie **Paket erstellen**.

1. Geben Sie einen Namen ein und wählen Sie **Erstellen**.

   Das Paket wird automatisch geöffnet.

1. Um ein Paket später erneut zu öffnen, wählen Sie es aus der Liste Pakete aus und klicken Sie auf **Anzeigen**.
1. Um ein Paket zu löschen, wählen Sie es aus der Liste Pakete aus und klicken Sie auf **Löschen**.

   >[!WARNING]
   >
   >Wenn Sie ein Paket löschen, werden es und alles, was darin ist, dauerhaft entfernt.

## Verwalten eines Pakets

Ein offenes Paket ist in vier Bereiche unterteilt:

* **Funktionen**: Erstellen, testen und veröffentlichen Sie die Funktion.
* **Variablen**: Konfigurieren von Variablen für die Funktion.
* **Abhängigkeiten**: Installieren Sie Abhängigkeiten wie externe Bibliotheken für diese Funktion.
* **History**: Frühere Versionen jeder Funktion anzeigen.

Zusätzlich zu diesen vier Bereichen zeigt ein Speichermeter oben an, wie viel von Ihrem Platz belegt ist. Jedes Paket hat eine Gesamtgrößenbeschränkung von **21 MB**. Dazu gehören Funktionen, Variablen und Abhängigkeiten, einschließlich gespeicherter Versionen.

Wenn Sie keinen Speicherplatz mehr haben, empfehlen wir, nicht verwendete Abhängigkeiten, Variablen oder ältere Versionen zu entfernen, um einige freizugeben.

Um zur Paketliste zurückzukehren, klicken Sie auf den Rückwärtspfeil neben dem Paketnamen.

<!--Create toc here-->
* [Funktionen](#functions)
* [Variablen](#variables)
* [Abhängigkeiten](#dependencies)
* [Verlauf](#history)

### Funktionen

Der Bereich **Funktionen** zeigt eine Liste der Funktionen im Paket an, einschließlich des Namens der Funktion, ihres Status, ihrer Größe und der erwarteten Anzahl von Eingaben.

* [Anzeigen und Verwalten der Funktionsliste](#view-and-manage-the-functions-list)
* [Erstellen oder Bearbeiten einer Funktion im Bereich Pakete](#create-or-edit-a-function-in-the-packages-area)
* [Änderungen an einer Live-Funktion vornehmen](#make-changes-to-a-live-function)
* [Funktion löschen](#delete-a-function)

#### Anzeigen und Verwalten der Funktionsliste

So filtern Sie die Liste Funktionen :

1. Filtern Sie nach Status, indem Sie auf **Alle**, **Entwürfe** oder **Veröffentlicht** klicken.
1. Verwenden Sie die Suchleiste, um nach bestimmten Funktionen zu suchen.

Eine Funktion kann den Status „Entwurf“ oder „Veröffentlicht“ haben.

* **Entwurf**: Funktionen im Entwurfsstatus sind in Bearbeitung. Sie können frei bearbeiten und testen, ohne die Live-Daten zu beeinflussen.
* **Veröffentlicht**: Veröffentlichte Versionen sind live. Ihre Szenarien führen veröffentlichte Versionen von Funktionen aus.

Mit Entwürfen können Sie sicher Änderungen vornehmen. Sie können einen Entwurf verfeinern, testen und ihn dann veröffentlichen, wenn Sie damit zufrieden sind.

| Status | Bedeutung |
|---|---|
| **Veröffentlicht** | Eine Live-Version ist vorhanden. |
| **Entwurf** | Die Funktion ist noch in Bearbeitung oder eine Live-Funktion enthält Änderungen, die Sie noch nicht veröffentlicht haben. |

#### Erstellen oder Bearbeiten einer Funktion im Bereich Pakete

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.
1. Wählen Sie im Bereich **Funktionen** die Option **Funktion erstellen**.

   ODER

   Klicken Sie auf das Kontrollkästchen neben einer vorhandenen Funktion und wählen Sie **Bearbeiten** in der Aktionsleiste unten auf der Seite aus.

1. (Bedingt) Wenn Sie eine neue Funktion erstellen, geben Sie im Feld **Neue Funktion** einen Namen für die Funktion ein.

1. (Optional und bedingt) Um eine vorhandene Funktion umzubenennen, klicken Sie auf das Bearbeitungssymbol neben dem Namen der Funktion und geben Sie den neuen Namen ein.

1. Geben **auf der Registerkarte** Code“ die Funktionslogik ein.

   Beachten Sie beim Erstellen Ihrer Funktion Folgendes:

   * Funktionen müssen in JavaScript geschrieben werden.
   * Sie können die von Ihnen definierten Eingaben lesen, Ihre Variablen wiederverwenden und Ihre anderen Funktionen aufrufen.
   * Während der Eingabe werden Vorschläge angezeigt.

1. Um die Funktionsformatierung zu bereinigen, klicken Sie auf **Beautify**.

1. (Optional) Definieren Sie auf der Registerkarte **Parameter** die Eingaben, die Ihre Funktion erwartet.

   Informationen zu Eingaben finden Sie unter [Definieren von Eingaben](#define-inputs) in diesem Artikel.

1. Testen Sie auf **Registerkarte** Ihre Funktion.

   Anweisungen finden Sie unter [Testen einer Funktion](#test-a-function) in diesem Artikel.

1. Um diese Funktion als Entwurf zu speichern, klicken Sie auf **Als Entwurf speichern**.

   ODER

   Um die Funktion zu veröffentlichen, klicken Sie auf &quot;**&quot;**.

   >[!NOTE]
   >
   >Das Veröffentlichen einer Funktion löscht ihren Versionsverlauf. Die veröffentlichte Version wird zum aktuellen Ausgangspunkt, und frühere Entwurfsversionen werden nicht mehr beibehalten.

* [Eingaben definieren](#define-inputs)
* [Testen einer Funktion](#test-a-function)

##### Eingaben definieren

Auf der Registerkarte **Parameter** können Sie die Informationen beschreiben, die Ihre Funktion bei jeder Ausführung benötigt.

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.
1. Wählen Sie im Bereich **Funktionen** die Option **Funktion erstellen**.

   ODER

   Klicken Sie auf das Kontrollkästchen neben einer vorhandenen Funktion und wählen Sie **Bearbeiten** in der Aktionsleiste unten auf der Seite aus.

1. Klicken Sie auf **Registerkarte** Parameter“.

1. Klicken Sie für jeden Parameter, den Sie hinzufügen möchten **auf „Parameter hinzufügen** und konfigurieren Sie Folgendes:

* **Name**: Der Name der Eingabe
* **Label**: Ein benutzerfreundlicher Name, der beim Testen der Funktion angezeigt wird
* **Type**: Der Datentyp, z. B. Text, Zahl, true/false oder ein strukturiertes Objekt.
* **Erforderlich**: Ob ein Wert angegeben werden muss.

Diese Eingaben werden zu den Feldern, die Sie beim Testen ausfüllen, und zu den Werten, die Ihr Szenario beim Ausführen der Funktion übergibt.

##### Testen einer Funktion

Es wird empfohlen, eine Funktion vor ihrer Veröffentlichung zu testen.

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.
1. Wählen Sie im Bereich **Funktionen** die Option **Funktion erstellen**.

   ODER

   Klicken Sie auf das Kontrollkästchen neben einer vorhandenen Funktion und wählen Sie **Bearbeiten** in der Aktionsleiste unten auf der Seite aus.

1. Klicken Sie auf **Registerkarte** Test“.

1. Geben Sie für jede Eingabe einen Wert ein.

1. Funktion ausführen:

   * Wählen **Entwurf testen**, um Ihre laufende Version zu testen.
   * Wählen **Veröffentlicht ausführen**, um die Live-Version auszuführen.

1. Überprüfen Sie das Ergebnis, einschließlich der Frage, ob es erfolgreich war, wie lange es dauerte und welche Ausgabe zurückgegeben wurde.

>[!NOTE]
>
>**Veröffentlicht ausführen** ist erst nach der Veröffentlichung einer Funktion verfügbar.

#### Änderungen an einer Live-Funktion vornehmen

Nachdem eine Funktion veröffentlicht wurde, wird die Schaltfläche **Veröffentlichen** zu einem Menü:

* **Erneut veröffentlichen** — Pushen Sie Ihre neuesten Entwurfsänderungen auf die Live-Version.
* **Veröffentlichung aufheben** - Die Funktion wird nicht mehr bereitgestellt. Ihre Arbeit wird als Entwurf gespeichert, damit Sie darauf zurückkommen können.

#### Funktion löschen

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.
1. Klicken Sie auf das Kontrollkästchen neben einer vorhandenen Funktion und wählen Sie **Löschen** in der Aktionsleiste am unteren Rand der Seite aus.

>[!WARNING]
>
>Durch das Löschen einer Funktion wird sie vollständig entfernt, ebenso wie ihr Verlauf. Jedes Szenario oder jede Funktion, die es verwendet, funktioniert nicht mehr.

### Variablen

Variablen sind wiederverwendbare Werte, die Ihre Funktionen verwenden können, z. B. eine Basis-URL, eine Konto-ID oder ein API-Schlüssel. Wenn Sie diese Variablen als Variablen speichern, legen Sie einen Wert einmal fest und aktualisieren ihn an einer Stelle, anstatt ihn über viele Funktionen hinweg zu aktualisieren.

* [Erstellen oder Bearbeiten einer Variablen](#create-or-edit-a-variable)
* [Löschen einer Variablen](#delete-a-variable)

#### Erstellen oder Bearbeiten einer Variablen

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.
1. Wählen Sie auf der **Variablen** die Option **Neue Variable** aus.

   ODER


   Klicken Sie auf **Bearbeiten**-Symbol neben der Variablen, die Sie bearbeiten möchten.

1. Füllen Sie die Details aus:

   * **Schlüssel**: Geben Sie den Namen ein, mit dem Ihre Funktionen auf den Wert verweisen.

   Um diese Variable umzubenennen, ändern Sie den Schlüsselwert.
   * **Wert**: Geben Sie den zu speichernden Wert ein.
   * **Type**: Wählen Sie aus, ob der Werttyp Text, eine Zahl, ein boolescher Wert (true/false) oder ein strukturiertes Objekt ist.
   * **Beschreibung**: Geben Sie einen optionalen Hinweis ein, um Sie daran zu erinnern, wozu er verwendet werden soll.
   * **Öffentlich**: Aktivieren Sie diese Option, wenn Sie die Variable im Szenario-Designer verwenden möchten. Wenn diese Option deaktiviert ist, ist die Variable nur innerhalb der -Funktionen des Pakets verfügbar.
   * **Geheimnis**: Aktivieren Sie diese Option, um vertrauliche Werte wie Schlüssel auszublenden. Der Wert wird in der Variablenliste ausgeblendet und ebenfalls bereinigt, sodass er nicht im Szenario-Designer verfügbar gemacht wird. Ihre Funktionen erhalten bei ihrer Ausführung weiterhin den tatsächlichen Wert.

1. Wählen **Variable erstellen** oder **Änderungen speichern**.

#### Löschen einer Variablen

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.
1. Klicken Sie auf **Registerkarte** auf das Symbol **Löschen** neben der Variablen, die Sie löschen möchten.

>[!WARNING]
>
>Funktionen, die eine gelöschte Variable verwenden, funktionieren nicht mehr.

### Abhängigkeiten

Einige Funktionen erfordern zusätzliche Bibliotheken, um ihre Aufgabe zu erfüllen. Auf **Registerkarte** Abhängigkeiten“ können Sie diese Bibliotheken hinzufügen und verwalten.

* [Bibliotheken hinzufügen](#add-libraries)
* [Bibliothek entfernen](#remove-a-library)

#### Bibliotheken hinzufügen

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.
1. Geben Sie auf **Registerkarte** einen oder mehrere Bibliotheksnamen ein, getrennt durch Kommas. Sie können eine bestimmte Version anfordern, indem Sie sie nach dem Namen hinzufügen (z. B. `axios, lodash@4.17.21`).

1. Klicken Sie auf **Installieren**.

#### Bibliothek entfernen

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.
1. Klicken Sie auf **Registerkarte** auf das Symbol **Löschen** neben der Bibliothek, die Sie entfernen möchten.

>[!WARNING]
>
>Funktionen, die auf einer entfernten Bibliothek basieren, funktionieren möglicherweise nicht mehr.

### Verlauf

Jedes Mal, wenn Sie einen Entwurf einer Funktion speichern, speichert Fusion eine Kopie. Auf **Registerkarte** Verlauf“ können Sie frühere Versionen anzeigen und wiederherstellen.

1. Klicken Sie auf **Registerkarte** Pakete![&#x200B; Pakete](assets/packages-icon.png) im linken Navigationsbereich.
1. Wählen Sie auf **Registerkarte** Verlauf“ auf der linken Seite eine Funktion aus, um deren zuletzt gespeicherte Versionen anzuzeigen.
1. Wählen Sie eine Version aus, um genau anzuzeigen, was sie zu diesem Zeitpunkt enthielt.
1. Um eine Version wiederherzustellen, klicken Sie auf **Als Entwurf wiederherstellen**.

   Die Version wird als neuer Entwurf wiederhergestellt, sodass Sie sie vor der Veröffentlichung überprüfen und testen können. Ihre Live-Version bleibt bis zur Veröffentlichung bestehen.
1. Um eine Version zu löschen, wählen Sie die Version aus, klicken Sie auf **Version löschen** und bestätigen Sie dann.

>[!NOTE]
>
>* Das Veröffentlichen einer Funktion löscht ihren Verlauf. Der Verlauf verfolgt die Änderungen, die Sie während der Arbeit an einem Entwurf vornehmen, bis zur Veröffentlichung.
>* Das Löschen einer Version kann nicht rückgängig gemacht werden.



## Verwenden eines Pakets in einem Szenario

Der Zweck des Erstellens von Funktionen und Variablen besteht darin, sie in Ihren Szenarien zum Einsatz zu bringen. Um Funktionen und Variablen zu verwenden, verwenden Sie den **Adobe App Builder**-Connector.

* **Funktion aus Paket verwenden**: Dieses Modul führt eine Ihrer Funktionen als Schritt in einem Szenario aus. Wählen Sie das Paket und die Funktion aus, füllen Sie die von Ihnen definierten Eingaben aus, und das Ergebnis der Funktion wird an die folgenden Module weitergegeben.
* **Variable aus Paket verwenden**: Dieses Modul bringt eine Ihrer Paketvariablen in ein Szenario, sodass Sie seinen Wert anderen Modulen zuordnen können.

Informationen und Anweisungen finden Sie unter [Adobe App Builder-Module](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

<!--

To add one:

1. In the scenario designer, add a module and choose the **Adobe App Builder** connector.

1. Select **Use function from package** or **Use variable from package**.

1. Choose the package and the function or variable you want, then map the inputs or value as needed.

>[!NOTE]
>
>Publish a function before using it in a scenario, and turn on **Public** for any variable you want to use there.

-->





