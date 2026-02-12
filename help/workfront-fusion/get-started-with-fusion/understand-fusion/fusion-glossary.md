---
title: Adobe Workfront Fusion-Glossar
description: Im folgenden Glossar werden einige häufig verwendete Begriffe in Adobe Workfront Fusion erläutert.
author: Becky
feature: Workfront Fusion
exl-id: 7f098ec2-8594-4e5d-9ce7-d1738a05f9a6
source-git-commit: c89536b6d3e6ca5f7e5048b8487a2d86bda3b213
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 98%

---

# Adobe Workfront Fusion-Glossar

Im folgenden Glossar werden einige häufig verwendete Begriffe in Adobe Workfront Fusion erläutert.


<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Aktion</p> </td> 
   <td>Ein Modul, mit dem Sie eine Aktion durchführen können, z. B. Daten aus ausgewählten Anwendungen oder Services lesen oder in diese schreiben.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Aggregator</p> </td> 
   <td> <p>Ein Modultyp, der mehrere Pakete (mehrere Sammlungen von Daten) zu einem einzigen Paket zusammenführt. </p><p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/aggregator-module.md" class="MCXref xref">Aggregatormodul</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API</td> 
   <td>Über Anwendungsprogrammierschnittstellen (Application Programming Interfaces, APIs) können Anwendungen und Services miteinander kommunizieren. Fusion nutzt APIs zur Kommunikation mit der Anwendung, zu der Sie eine Verbindung herstellen. Jede Anwendung verfügt über eine separate API. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-Schlüssel</td> 
   <td>Ein eindeutiger Code, der zur Authentifizierung die Benutzenden, Entwickelnden oder Programme identifiziert, die die API einer Software aufrufen. Da Fusion-Module durch die Verbindung von APIs funktionieren, sind mitunter API-Schlüssel erforderlich. API-Schlüssel werden von der Anwendung verteilt, die diese benötigt. Wenn Sie beispielsweise einen API-Schlüssel benötigen, um Fusion mit Adobe Lightroom zu verbinden, würden Sie ihn über Ihr Adobe Lightroom-Konto anfordern.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Anwendung oder Service</td> 
   <td> <p>Eine Software-Anwendung. Fusion kann sich mit den meisten Anwendungen verbinden, auch wenn es über keinen dedizierten Connector für jeweilige Anwendung verfügt.</p> <p>Eine Anwendung kann auch eine spezielle Funktion sein, die Daten ändert, z. B. ein Iterator oder Aggregator. </p> <p>Ein Service ist eine Datenquelle, die eine Web-API, eine Web-Seite, verschiedene Arten von Servern (FTP, SMTP, IMAP) usw. umfassen kann. </p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Paket</p> </td> 
   <td> <p>Ein Paket ist eine Basiseinheit von Daten, die von Modulen zurückgegeben oder empfangen wird. Beispielsweise würde ein Suchmodul, das drei Einträge zurückgibt, drei Datenpakete ausgeben: eines für jeden Eintrag. Ein Paket besteht aus Elementen.</p> </td> 
  </tr> 
  <tr>
   <td role="rowheader"> <p>Verbindung</p> </td> 
   <td> <p>Eine Verbindung stellt einen Satz von Anmeldeinformationen dar, mit denen eine Verbindung zu einem bestimmten Service hergestellt werden kann. Sie können Verbindungen innerhalb jedes Moduls konfigurieren und diese Verbindung dann in einem anderen Modul verwenden. Für jedes Modul muss eine Verbindung ausgewählt sein, damit Fusion über diese Anmeldeinformationen auf die für das Modul erforderlichen Informationen zugreifen kann. </p><p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md" class="MCXref xref">Überblick über Verbindungen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Connector</td> 
   <td>Ein Connector ist ein Satz von Modulen für eine bestimmte Anwendung. Workfront Fusion bietet Connectoren für viele gängige Arbeitsanwendungen wie Workfront, Salesforce und Jira.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Zyklus</p> </td> 
   <td> <p>Ein Zyklus besteht aus zwei Phasen der Szenario-Ausführung: „Vorgang“ und „Verpflichtung“. Das Szenario kann aus einem oder mehreren Zyklen bestehen. Ausführlichere Informationen finden Sie unter <a href="/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md" class="MCXref xref">Szenarioausführung, Zyklen und Phasen</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Datenspeicher</p> </td> 
   <td> <p>Ein Datenspeicher speichert Daten aus Szenarios oder ermöglicht Ihnen die Übertragung von Daten zwischen einzelnen Szenarios oder Szenario-Ausführungen. </p><p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/map-data/data-stores.md" class="MCXref xref">Datenspeicher</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Filter</p> </td> 
   <td> <p> Ein Filter kann zwischen zwei Modulen angewendet werden und ermöglicht es Ihnen, dann nur mit Paketen zu arbeiten, die bestimmten Kriterien entsprechen. Es gibt eine Reihe verschiedener Filter, die Sie anwenden können. </p><p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md" class="MCXref xref">Hinzufügen eines Filters zu einem Szenario</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID </p> </td> 
   <td> <p>Ein Name, der zur eindeutigen Identifizierung eines Pakets dient. Eine ID wird normalerweise verwendet, um ein Paket zu unterscheiden, das von einem bestimmten Service aktualisiert oder gelöscht werden soll. IDs können aus der Ausgabe eines vorherigen Moduls zugeordnet werden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Elemente</p> </td> 
   <td> <p>Ein Teil eines Pakets. Pakete können aus mehreren Elementen bestehen. Es gibt verschiedene Elementtypen: Text, Zahl, boolescher Wert (ja/nein), Datum, Uhrzeit, Puffer (Binärdaten), Sammlungen, Menüauswahl, Array und Validierung.</p><p> Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Elementdatentypen</a>.</p> </td> 
  </tr>
  <tr> 
   <td role="rowheader"> <p>Iterator</p> </td> 
   <td> <p>Ein Modultyp, mit dem Sie ein Datenpaket (eine Sammlung von Daten) in separate Pakete unterteilen können. Diese Pakete können dann von nachfolgenden Modulen einzeln verarbeitet werden. </p><p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">[!UICONTROL Iterator]modul</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Modul</p> </td> 
   <td> <p>Ein einzelner Schritt innerhalb eines Szenarios, mit dem innerhalb der zugehörigen Anwendung oder des zugehörigen Services eine Funktion ausgeführt wird, z. B. zum Erstellen eines Eintrags.</p> <p>Jede Anwendung bzw. jeder Service verfügt über verschiedene Module, die definieren, wie auf eine Anfrage reagiert wird.</p>  <p> <img src="assets/module.png"> </p> <p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md" class="MCXref xref">Überblick über Module</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Vorgang</p> </td> 
   <td> <p>Eine von einem Modul ausgeführte Aufgabe, z. B. das Abrufen eines Eintrags oder das Hochladen einer Datei.</p><p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md" class="MCXref xref">Vorgänge</a>.</p>
  </tr> 
  <tr> 
   <td role="rowheader">Öffentliche/private Schlüssel</td> 
   <td>Öffentliche und private Schlüssel werden zum Ver- und Entschlüsseln von Daten verwendet. Der öffentliche Schlüssel kann verteilt werden. Alle, die über den öffentlichen Schlüssel verfügen, können Daten verschlüsseln. Eine Entschlüsselung ist aber nur mit dem privaten Schlüssel möglich. Ebenso können Benutzende mit einem privaten Schlüssel Daten verschlüsseln, die von allen Personen mit dem öffentlichen Schlüssel entschlüsselt werden können. Die Verschlüsselung mit dem privaten Schlüssel stellt zum einen sicher, dass die Daten von der Person stammen, der der private Schlüssel gehört, und dient zum anderen zur Validierung der Datenquelle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Router</p> </td> 
   <td>Ein Router ermöglicht es Ihnen, Daten zu duplizieren oder einem Szenario neue Routen hinzuzufügen, sodass Sie Daten umleiten und verschiedene Datengruppen separat verarbeiten können.</p><p> Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/create-scenarios/add-modules/router-module.md" class="MCXref xref">[!UICONTROL Router]-Modul</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Szenario</p> </td> 
   <td> <p>Eine benutzerseitig erstellte Reihe automatisierter Schritte, die jeweils von einem Modul repräsentiert und ausgeführt werden. Der Zweck eines Szenarios besteht darin, Daten zu verschieben und zu bearbeiten.</p> <p> <img src="assets/entire-scenario-blank.png" style="width: 350;height: 178;"> </p> <p> Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md" class="MCXref xref">Überblick über Szenarios</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Szenario-Segment</p> </td> 
   <td> <p> Ein Szenario-Segment ist ein Abschnitt eines Szenarios, das aus einer Reihe von Modulen besteht, die alle mit derselben Anwendung verbunden sind. Szenario-Segmente stellen oft einen kurzen Workflow in der Anwendung dar.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Auslöser</p> </td> 
   <td> <p>Ein Auslöser ist eine Art Modul, das auf neue und aktualisierte Daten achtet und das Szenario startet, wenn bestimmte im Modul konfigurierte Bedingungen zutreffen. Auslöser können so konfiguriert werden, dass ein Szenario nach einem Zeitplan (Abruf) oder bei jeder Datenänderung (Instant-Auslöser oder Webhook) gestartet wird.</p> <p>Weitere Informationen finden Sie im Artikel „Überblick über Module“ unter <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md" class="MCXref xref">Auslöser</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Webhook</p> </td> 
   <td> <p>Ein spezieller Auslösertyp, mit dem Sie ein Szenario sofort ausführen können, wenn ein neues Paket verfügbar ist. </p><p>Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Instant-Auslöser (Webhooks)</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
