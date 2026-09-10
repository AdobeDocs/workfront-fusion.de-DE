---
title: Adobe Experience Manager MCP-Module
description: Mit dem Adobe Experience Manager MCP-Modul können Sie eine Eingabeaufforderung in englischer Sprache an den MCP-Server von Adobe Experience Manager senden und die Anforderung von einem KI-Modell ausführen lassen.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 06271bbe8dd3c5eb7e3c6b45b71e7e0f7fd4d444
workflow-type: tm+mt
source-wordcount: 1020
ht-degree: 11%

---

# Adobe Experience Manager MCP-Module

Der Adobe Experience Manager MCP-Connector ist eine dedizierte Fusion-Integration für Adobe Experience Managers eigenen MCP-Server (Model Context Protocol). Im Gegensatz zu einem typischen Connector, bei dem jedes Modul eine feste Aktion ausführt, verfügt dieser Connector über ein einziges Modul, das eine offene, englischsprachige Anweisung akzeptiert und es einem KI-Modell ermöglicht zu entscheiden, welche Adobe Experience Manager-Vorgänge erforderlich sind, um sie zu erfüllen, und zwar über Bereiche wie Sites, digitale Assets, Inhaltsfragmente, Ordner, das Inhalts-Repository und Inhalts-KI hinweg.

Dieser Connector ist für Adobe Experience Managers eigenen MCP-Server vorgesehen. Andere, nicht verwandte MCP-Server werden nicht unterstützt. Verwenden Sie für einen Connector, den Sie stattdessen auf einen beliebigen MCP-Server verweisen können, den MCP Agent Connector.

Informationen zum MCP Agent Connector finden Sie unter [MCP Agent-Modul](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md).

>[!NOTE]
>
>Antworten aus diesem Modul werden von KI generiert und können gelegentlich unvollkommen sein, sogar mit allen verfügbaren Sicherheitsmaßnahmen. Dieses Modul eignet sich für Automatisierungen, bei denen ein Mensch nicht jede Ausführung in Echtzeit überprüft, aber es ist keine Garantie für das deterministische Verhalten, das ein herkömmliches Adobe Experience Manager-Modul verspricht.

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
   <p>Betriebsbasiert: Verfügbar für Organisationen mit betriebsbasierten Lizenzen</p>
   <p>Connector-basiert (veraltet): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

* Sie benötigen ein Adobe Experience Manager-Konto, um dieses Modul verwenden zu können.

## Adobe Experience Manager MCP mit Workfront Fusion verbinden {#connect-adobe-experience-manager-mcp-to-workfront-fusion}

Der Adobe Experience Manager MCP-Connector verwendet OAuth, um eine Verbindung zu Adobe Experience Manager herzustellen. Es gibt keine Verbindungsfelder, die manuell ausgefüllt werden müssen, z. B. einen Benutzernamen, ein Kennwort oder einen API-Schlüssel.

So erstellen Sie eine Verbindung:

1. Klicken Sie im MCP-Modul von Adobe Experience Manager **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .
1. Wählen Sie aus, ob Sie eine Verbindung zu einer Produktions- oder Nicht-Produktionsumgebung herstellen.
1. Auswählen, ob Sie eine Verbindung zu einem Service-Konto oder einem persönlichen Konto herstellen möchten
1. Klicken Sie auf **Fortfahren**.

   Sie werden zur Anmeldeseite von Adobe weitergeleitet.
1. Melden Sie sich auf der Adobe-Anmeldeseite an und genehmigen Sie den Zugriff.

Sie werden zurück zu Workfront Fusion weitergeleitet, und die neue Verbindung ist im -Modul verfügbar.

## Adobe Experience Manager MCP-Modul und seine Felder

Derzeit gibt es nur ein Modul im Adobe Experience Manager MCP-Connector.

### Benutzeraufforderung verarbeiten

Dieses Aktionsmodul sendet eine englischsprachige Anweisung an den MCP-Server von Adobe Experience Manager und gibt die Antwort der KI zurück.

Jede Ausführung dieses Moduls ist eine einzelne, in sich abgeschlossene Ausführung, die dem Senden einer E-Mail ähnelt, anstatt eine Live-Konversation zu führen. Die KI kann keine Folgefrage stellen und auf Ihre Antwort warten. Stattdessen trifft sie ihr bestes Urteil und gibt eine vollständige Antwort zurück. Wenn Ihre Eingabeaufforderung mehrdeutig ist, gibt die KI jede Annahme an, die sie als Teil ihrer Antwort gemacht hat, anstatt aufzuhören, Sie um Klarstellung zu bitten.

>[!IMPORTANT]
>
>Dieses Modul führt nur dann eine Schreib- oder Löschaktion durch, wenn in der Eingabeaufforderung nach einer Aktion gefragt wird. Es führt keine zusätzlichen Aktionen aus, die Sie nicht angefordert haben, auch nicht in der gleichen Ausführung, in der es etwas Anderes ausführt, worum Sie gebeten haben.

Da jeder Durchgang unabhängig ist, hat das Modul keinen Speicher für frühere Durchgänge. Um ein mehrgängiges, konversatives Erlebnis über mehrere Läufe hinweg zu erstellen, speichern Sie die vorherige Frage und Antwort. Sie können dafür einen Datenspeicher verwenden und diesen Verlauf dann zu Beginn der nächsten Eingabeaufforderung als Text einbeziehen, gefolgt von der neuen Frage.

Informationen zu Datenspeichern finden Sie unter [Datenspeicher](/help/workfront-fusion/create-scenarios/data-stores/data-store-overview.md).

<table style="table-layout:auto"> 
 <col/>
 <col/>
 <tbody>
  <tr>
   <td role="rowheader">LLM-<i> (optional, erweitert)</i></td>
   <td><p>Standardmäßig verarbeitet dieses Modul Ihre Eingabeaufforderung mit dem eigenen KI-Service von Adobe und Sie müssen keinen Schlüssel auswählen.</p><p>Um stattdessen Ihren eigenen KI-Anbieter zu verwenden, wählen Sie einen vorhandenen LLM-Schlüssel aus oder erstellen Sie einen neuen, indem Sie auf <b>Hinzufügen</b> klicken und die folgenden Informationen eingeben:</p>
    <ul>
     <li><b>Schlüsselname</b>: Geben Sie einen Namen für den neuen Schlüssel ein.</li>
     <li><b>LLM</b>: Wählen Sie das große Sprachmodell aus, mit dem dieser Schlüssel verknüpft ist. Unterstützte Anbieter sind OpenAI, Anthropic Claude und Amazon Bedrock.</li>
     <li><b>Schlüssel</b>: Geben Sie den API-Schlüssel für den ausgewählten Anbieter ein oder ordnen Sie ihn zu.</li>
     <li><b>Modell</b>: Wählen Sie das LLM-Modell aus, das der Schlüssel verwenden soll.</li>
     <li><b>Andere Felder</b>: Geben Sie Werte für alle anderen Felder ein, die für Ihr LLM erforderlich sind.</li>
    </ul>
   </td>
  </tr>
  <tr>
   <td role="rowheader">Verbindung</td>
   <td><p>Anweisungen zum Verbinden Ihres Adobe Experience Manager-Kontos mit Workfront Fusion finden Sie unter <a href="#connect-adobe-experience-manager-mcp-to-workfront-fusion" class="MCXref xref">Verbinden von Adobe Experience Manager MCP mit Workfront Fusion</a> in diesem Artikel.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Benutzeraufforderung</td>
   <td><p>Geben Sie die Anweisung ein, die die KI ausführen soll, oder kartieren Sie sie in einfachem Englisch.</p><p>Beispiel: <i>Finden Sie alle Assets im Marketing-Ordner, die in 90 Tagen nicht aktualisiert wurden.</i></p></td>
  </tr>
  <tr>
   <td role="rowheader">Schreibgeschützte Tools <i>(optional)</i></td>
   <td><p>Beschränken Sie, welche schreibgeschützten Adobe Experience Manager-Aktionen die KI aufrufen darf - Aktionen, die nur etwas nachschlagen, z. B. ein Asset suchen oder den Seiteninhalt lesen und nie etwas ändern.</p><p>Wenn Sie dieses Feld leer lassen, sind alle schreibgeschützten Aktionen zulässig.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Schreib-/Löschwerkzeuge <i>(optional)</i></td>
   <td><p>Beschränken Sie, welche Adobe Experience Manager-Aktionen die KI aufrufen darf, um sie zu schreiben oder zu löschen - Aktionen, die etwas ändern, z. B. das Aktualisieren einer Seite, das Veröffentlichen von Inhalten oder das Löschen eines Assets.</p><p>Wenn Sie dieses Feld leer lassen, sind alle Schreib- und Löschaktionen zulässig. Um sicherzustellen, dass ein unbeaufsichtigtes Szenario niemals eine destruktive Aktion ausführt, empfehlen wir, dieses Feld, das auf eine absichtlich leere Auswahl eingestellt ist, nicht unbeschränkt zu lassen.</p></td>
  </tr>
 </tbody>
</table>

Das Modul gibt die endgültige Antwort der KI als Text zurück, zusammen mit einer Aufzeichnung dessen, was während der Erstellung dieser Antwort passiert ist, einschließlich der aufgerufenen Tools, der Erfolgsmeldung jedes Aufrufs und der Dauer der Verarbeitung.

