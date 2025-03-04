---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe User Management-Module
description: In einem  [!DNL Adobe Workfront Fusion]  können Sie Workflows automatisieren, mit denen Benutzende in Ihrem Adobe-Konto verwaltet werden.
author: Becky
feature: Workfront Fusion
exl-id: e8fe8ec4-4b00-4c9a-81a5-acb2039b153b
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '2374'
ht-degree: 2%

---

# Adobe User Management-Module

In einem [!DNL Adobe Workfront Fusion] können Sie Workflows automatisieren, mit denen Benutzende in Ihrem Adobe-Konto verwaltet werden.

Anweisungen zum Erstellen eines Szenarios finden Sie in den Artikeln unter [Szenario erstellen: Artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Informationen zu Modulen finden Sie in den Artikeln unter [Module: Artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

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
   <td> <p>[!UICONTROL-Plan], [!UICONTROL-Arbeit]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL [!DNL Workfront Fusion] for Work Automation and Integration], [!UICONTROL [!DNL Workfront Fusion] for Work Automation]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den [!DNL Adobe Workfront] [!UICONTROL Select] oder [!UICONTROL Prime] verfügen, muss Ihr Unternehmen [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu nutzen. [!DNL Workfront Fusion] ist im [!DNL Workfront] [!UICONTROL Ultimate] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben und [!DNL Adobe Workfront], die in diesem Artikel beschriebenen Funktionen zu verwenden.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Wenden Sie sich an Ihren [!DNL Workfront], um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Erstellen einer Verbindung mit Adobe User Management

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe User Management]:

1. Klicken Sie in einem beliebigen Modul **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

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
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>Wählen Sie aus, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre [!UICONTROL Adobe] [!UICONTROL Client-ID] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihren [!DNL Adobe] [!UICONTROL Client Secret] ein. Diese finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS-Organisations-ID]</td>
        <td>Geben Sie Ihre [!DNL Adobe] IMS-Anmeldedaten ein. Die eindeutige Kennung für eine Organisation. Dies ist eine Zeichenfolge der Form A495E53@AdobeOrg, wobei das Präfix vor dem @ eine hexadezimale Zahl ist. Sie finden diesen Wert als Teil des URL-Pfads für das Unternehmen in der Admin Console oder in der adobe.io-Konsole für Ihre User Management-Integration.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Zusätzliche Bereiche]</td>
        <td>Klicken Sie für jeden zusätzlichen Bereich, den Sie hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie den Bereich ein.</td>
        </tr>
      </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.



## Adobe User Management-Module und ihre Felder

Beim Konfigurieren von Adobe User Management-Modulen zeigt Workfront Fusion die unten aufgeführten Felder an. Darüber hinaus werden möglicherweise weitere Adobe-Benutzerverwaltungsfelder angezeigt, je nach Faktoren wie Ihrer Zugriffsebene in der App oder im Service. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Suchvorgänge](#searches)
* [Benutzeraktionen](#user-actions)
* [Benutzergruppenaktionen](#user-group-actions)
* [Sonstige](#other)

### Suchvorgänge

* [Abrufen von Benutzergruppen und Produktprofilen](#get-user-groups-and-product-profiles)
* [Abrufen von Benutzerinformationen](#get-user-information)
* [Abrufen von Benutzern in einer Benutzergruppe oder einem Produktprofil](#get-users-in-a-user-group-or-product-profile)
* [Abrufen von Benutzern in einer Organisation](#get-users-in-an-organization)

#### Abrufen von Benutzergruppen und Produktprofilen

Dieses Suchmodul ruft eine Liste aller Benutzergruppen und Produktprofile in Ihrer Organisation sowie Details zu den Gruppen und Profilen ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen von Benutzerinformationen

Dieses Suchmodul ruft Details für einen einzelnen Benutzer in der Organisation ab, der durch seine E-Mail-Adresse identifiziert wird.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">E-Mail-Adresse</td> 
   <td>Geben Sie die E-Mail-Adresse des Benutzers ein, für den Sie Details zurückgeben möchten, oder mappen Sie sie. Für Adobe ID-, Enterprise- und E-Mail-Federated-Benutzer sollte dies die vollständige E-Mail-Adresse einschließlich Domain sein. In allen Fällen wird bei dem Parameter nicht zwischen Groß- und Kleinschreibung unterschieden.</td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen von Benutzern in einer Benutzergruppe oder einem Produktprofil

Dieses Suchmodul ruft eine Liste aller Benutzer in der angegebenen Benutzergruppe oder dem angegebenen Produktprofil zusammen mit Details zu den Benutzern ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppenname</td> 
   <td>Die Benutzergruppe, der Produktprofilname oder eine Administratorgruppe. Bei einer Administratorgruppe kann der Name eine der festen Gruppen <code>_org_admin</code>, <code>_deployment_admin</code> oder <code>_support_admin</code> oder eine gruppenspezifische Administratorgruppe sein. Diese werden mit einem Präfix am Gruppennamen identifiziert, z. B. <code>_admin_groupName</code>, <code>_product_admin_productName</code> oder <code>_developer_groupName</code>. Wenn die Gruppe vorhanden ist, die Administratorgruppe jedoch nicht, wird eine leere Liste zurückgegeben.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nur Direkt</td> 
   <td>Geben Sie an, ob das Feld Gruppen in der zurückgegebenen Benutzerstruktur nur die Produktprofile enthält, denen dieser Benutzer direkt angehört. Bei „false“ werden alle Gruppen (Benutzergruppen, Produktprofile und Administratorgruppen) zurückgegeben, die den Benutzer enthalten, unabhängig davon, ob die Berechtigung für ein bestimmtes Produktprofil direkt (über die Benutzerzuweisung) oder indirekt (über eine Benutzergruppe, die den Benutzer enthält, der dem Produktprofil zugewiesen wird) eingeht. Wenn „true“, werden alle Benutzergruppen und Administratorgruppen zurückgegeben, die den Benutzer enthalten, jedoch nur die Produktprofile, denen der Benutzer explizit eine Berechtigung zugewiesen hat. Ein Benutzer kann sowohl direktes als auch indirektes Mitglied eines Produktprofils sein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppen ausschließen</td> 
   <td>Geben Sie an, ob die Antwort ausschließt, dass das Gruppen-Array für jeden einzelnen Benutzer zurückgegeben wird.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Status</td> 
   <td>Diese Option gilt nur für Produktprofile. Wählen Sie Aktiv aus, um Benutzer aufzulisten, die für das Produkt bereitgestellt wurden und über eine aktive Lizenz verfügen. Wählen Sie Inaktiv aus, um Benutzer aufzulisten, die zum Produktprofil hinzugefügt wurden, aber keine aktive Lizenz haben. Wenn dies leer gelassen wird, gibt das Modul alle Mitglieder unabhängig vom Berechtigungsstatus zurück.
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

#### Abrufen von Benutzern in einer Organisation

Dieses Suchmodul gibt alle Benutzer der Organisation zurück, die mit der Verbindung verknüpft ist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximale Anzahl an zurückgegebenen Ergebnissen</td> 
   <td>Geben Sie die maximale Anzahl von Datensätzen ein, die das Modul während jedes Szenario-Ausführungszyklus zurückgeben soll, oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>

### Benutzeraktionen

* [Benutzer als Mitglied einer Gruppe hinzufügen](#add-a-user-as-a-member-of-a-group)
* [Benutzer erstellen](#create-a-user)
* [Benutzer aus Gruppen entfernen](#remove-a-user-from-groups)
* [Aktualisieren von Benutzern](#update-a-user)

#### Benutzer als Mitglied einer Gruppe hinzufügen

Dieses Aktionsmodul fügt einen Benutzer als Mitglied der angegebenen Gruppe(n) hinzu. Dieses Modul kann den Benutzer zu bis zu vier Gruppen hinzufügen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benutzerin oder Benutzer</td> 
   <td>Geben Sie den Benutzer ein, den Sie den Gruppen hinzufügen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domäne</td> 
   <td>Geben Sie für Federated IDs, bei denen es sich nicht um E-Mail-Adressen handelt, die Domain ein, zu der der Benutzer gehört.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppen</td> 
   <td>Klicken Sie für jede Gruppe, der Sie den Benutzer hinzufügen möchten, auf <b>Element hinzufügen</b> und geben Sie die Gruppe ein oder ordnen Sie sie zu. Sie können bis zu vier Gruppen eingeben und müssen mindestens eine eingeben.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verwenden von Adobe ID</td> 
   <td>Wählen Sie „true“ aus, um sicherzustellen, dass die Benutzer-ID so interpretiert wird, dass sie auf eine bestehende Adobe ID verweist, selbst wenn eine Enterprise oder Federated ID mit demselben Namen vorhanden ist.</td> 
  </tr> 
 </tbody> 
</table>

#### Benutzer erstellen

Dieses Aktionsmodul erstellt einen neuen Benutzer in der Organisation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID-Typ</td> 
   <td>Wählen Sie aus, ob Sie eine Benutzerin bzw. einen Benutzer mit einer Adobe ID, einer Enterprise ID oder einer Federated ID erstellen möchten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Anmeldung</td> 
   <td>Wenn Sie eine Benutzerin oder einen Benutzer mit einer Federated ID erstellen, wählen Sie den Anmeldetyp aus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">E-Mail</td> 
   <td>Geben Sie die E-Mail-Adresse des neuen Benutzers ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domäne</td> 
   <td>Wenn Sie einen Benutzer mit einer Federated ID mit einer Domain-basierten Anmeldung erstellen, geben Sie die Domain ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benutzerin oder Benutzer</td> 
   <td>Wenn Sie einen Benutzer mit einer Federated ID mit einer Domain-basierten Anmeldung erstellen, geben Sie den Benutzer ein, den dieser neue Benutzer repräsentieren soll, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vorname</td> 
   <td>Geben Sie den Vornamen des Benutzers ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nachname</td> 
   <td>Geben Sie den Nachnamen des Benutzers ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Land</td> 
   <td>Geben Sie den zweistelligen ISO-Ländercode ein oder mappen Sie ihn. Dies kann nach der Erstellung des Benutzers nicht mehr geändert werden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Option</td> 
   <td>Wählen Sie die Aktion aus, die ausgeführt werden soll, wenn der Benutzer bereits in der Organisation vorhanden ist. Wenn keine Option ausgewählt ist und der Benutzer bereits vorhanden ist, gibt das Modul einen Fehler zurück.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verwenden von Adobe ID</td> 
   <td>Wenn „true“, wird die Benutzer-ID so interpretiert, dass sie auf eine bestehende Adobe ID verweist, selbst wenn eine Enterprise oder Federated ID mit demselben Namen vorhanden ist.</td> 
  </tr> 
 </tbody> 
</table>

#### Benutzer aus Gruppen entfernen

Dieses Aktionsmodul entfernt die Mitgliedschaft eines Benutzers aus den angegebenen Gruppen. Sie können einen Benutzer aus bis zu vier Gruppen gleichzeitig entfernen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benutzerin oder Benutzer</td> 
   <td>Geben Sie den Benutzer ein, den Sie aus den Gruppen entfernen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domäne</td> 
   <td>Geben Sie für Federated IDs, bei denen es sich nicht um E-Mail-Adressen handelt, die Domain ein, zu der der Benutzer gehört.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppen</td> 
   <td>Klicken Sie für jede Gruppe, aus der Sie den Benutzer entfernen möchten, auf <b>Element hinzufügen</b> und geben Sie die Gruppe ein oder ordnen Sie sie zu. Sie können bis zu vier Gruppen eingeben und müssen mindestens eine eingeben.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verwenden von Adobe ID</td> 
   <td>Wählen Sie „true“ aus, um sicherzustellen, dass die Benutzer-ID so interpretiert wird, dass sie auf eine bestehende Adobe ID verweist, selbst wenn eine Enterprise oder Federated ID mit demselben Namen vorhanden ist.</td> 
  </tr> 
 </tbody> 
</table>



#### Aktualisieren von Benutzern

Dieses Aktionsmodul aktualisiert einen vorhandenen Benutzer.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benutzerin oder Benutzer</td> 
   <td>Geben Sie die ID des Benutzers ein, den Sie aktualisieren möchten, oder ordnen Sie sie zu. Dies ist die E-Mail-Adresse des Benutzers, z. B. <code>user@example.com</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domäne</td> 
   <td>Wenn Sie Benutzende mit einer Federated ID aktualisieren, bei der es sich nicht um eine E-Mail-Adresse handelt, geben Sie die Domain, zu der die Benutzenden gehören, ein oder ordnen Sie sie zu, um die Benutzenden zu identifizieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">E-Mail</td> 
   <td>Geben Sie die neue E-Mail-Adresse des Benutzers ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Vorname</td> 
   <td>Geben Sie den Vornamen des Benutzers ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nachname</td> 
   <td>Geben Sie den Nachnamen des Benutzers ein oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

### Benutzergruppenaktionen

* [Hinzufügen von Mitgliedschaften für eine Benutzergruppe](#add-memberships-for-a-user-group)
* [Erstellen einer Benutzergruppe](#create-a-user-group)
* [Löschen einer Benutzergruppe](#delete-a-user-group)
* [Entfernen von Mitgliedschaften für eine Benutzergruppe](#remove-memberships-for-a-user-group)
* [Aktualisieren einer Benutzergruppe](#update-a-user-group)

#### Hinzufügen von Mitgliedschaften für eine Benutzergruppe

Dieses Aktionsmodul fügt Benutzer und Produktprofile einer Benutzergruppe hinzu. Benutzende, die der Benutzergruppe hinzugefügt wurden, erhalten die Berechtigung für alle Produktprofile in der Benutzergruppe. Durch Hinzufügen eines Produktprofils erhalten Benutzende in der Benutzergruppe eine Berechtigung für dieses Profil.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppenname</td> 
   <td>Geben Sie den Namen der Gruppe ein, aus der Sie die Benutzer oder Profile entfernen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benutzende</td> 
   <td>Klicken Sie für jeden Benutzer, den Sie hinzufügen möchten<b> auf „Benutzer hinzufügen</b> und geben Sie die E-Mail-Adresse des Benutzers ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Profile</td> 
   <td>Klicken Sie für jedes Profil, das Sie der Gruppe hinzufügen möchten, auf <b>Benutzer hinzufügen</b> und geben Sie den Profilnamen ein</td> 
  </tr> 
 </tbody> 
</table>

#### Erstellen einer Benutzergruppe

Dieses Aktionsmodul erstellt eine neue Benutzergruppe. Wenn bereits eine Gruppe mit dem angegebenen Namen vorhanden ist, kann das Modul die vorhandene Gruppe aktualisieren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppenname</td> 
   <td>Geben Sie einen Namen für die neue Benutzergruppe ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beschreibung</td> 
   <td>Geben Sie eine Beschreibung für die neue Benutzergruppe ein oder ordnen Sie sie zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Option</td> 
   <td>Auswahl der Aktion, die ausgeführt werden soll, wenn die Benutzergruppe bereits in der Organisation vorhanden ist. Wenn keine Option ausgewählt ist und die Benutzergruppe bereits vorhanden ist, gibt das Modul einen Fehler zurück.</td> 
  </tr> 
 </tbody> 
</table>

#### Löschen einer Benutzergruppe

Dieses Aktionsmodul löscht eine vorhandene Benutzergruppe.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppenname</td> 
   <td>Geben Sie den Namen der Gruppe ein, die Sie löschen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
 </tbody> 
</table>

#### Entfernen von Mitgliedschaften für eine Benutzergruppe

Dieses Aktionsmodul entfernt Benutzer oder Profile aus einer Benutzergruppe.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppenname</td> 
   <td>Geben Sie den Namen der Gruppe ein, aus der Sie die Benutzer oder Profile entfernen möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Benutzende</td> 
   <td>Klicken Sie für jeden Benutzer, den Sie entfernen möchten<b> auf „Benutzer hinzufügen</b> und geben Sie die E-Mail-Adresse des Benutzers ein.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Profile</td> 
   <td>Klicken Sie für jedes Profil, das Sie aus der Gruppe entfernen möchten, auf <b>Benutzer hinzufügen</b> und geben Sie den Profilnamen ein</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Verwenden von Adobe ID</td> 
   <td>Wenn „true“, wird die Benutzer-ID so interpretiert, dass sie auf eine bestehende Adobe ID verweist, selbst wenn ein Unternehmen oder eine Federated ID mit demselben Namen vorhanden ist.</td> 
  </tr> 
 </tbody> 
</table>

#### Aktualisieren einer Benutzergruppe

Dieses Aktionsmodul aktualisiert eine vorhandene Benutzergruppe.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbindung</td> 
   <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name der ursprünglichen Gruppe</td> 
   <td>Geben Sie den aktuellen Namen der Gruppe, die Sie aktualisieren möchten, ein oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Neuer Gruppenname</td> 
   <td>Geben Sie den neuen Namen ein, den die Gruppe haben soll, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Name der ursprünglichen Gruppe</td> 
   <td>Geben Sie die aktualisierte Beschreibung der Gruppe ein oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
 </table>

### Sonstige


#### Erstellen eines benutzerdefinierten API-Aufrufs

Dieses Aktionsmodul führt einen benutzerdefinierten Aufruf an die Adobe User Management-API durch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbindung</td>
      <td>Anweisungen zum Erstellen einer Verbindung mit Adobe User Management finden Sie unter <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Erstellen einer Verbindung mit Adobe User Management</a> in diesem Artikel.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>Pfad eingeben für <code>https://usermanagement.adobe.io/v2/usermanagement/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Methode</p>
      </td>
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-Anfragemethoden</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">Kopfzeilen</td>
      <td>
        <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p>
        <p>Beispiel: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungs- und X-API-Schlüssel-Header hinzu.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Abfragezeichenfolge  </td>
      <td>
        <p>Geben Sie die Abfragezeichenfolge der Anfrage ein.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Text</td>
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
