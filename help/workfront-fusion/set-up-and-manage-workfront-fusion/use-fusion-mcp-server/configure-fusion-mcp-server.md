---
title: Konfigurieren des Adobe Workfront Fusion MCP-Servers
description: Verbinden Sie Adobe Workfront Fusion mit einer MCP-kompatiblen KI-Agentenplattform oder mit Coworker (eigenständig oder in der rechten Leiste von Fusion).
source-git-commit: d5861015b3bb0e9c176fcf4fd71db426671764dd
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 8%
---

# Konfigurieren des Adobe Workfront Fusion MCP-Servers

Mit dem Adobe Workfront Fusion MCP-Server können Sie über eine unterstützte KI-Agentenplattform mit den Szenarien, Ausführungen, Verbindungen, Webhooks, Datenspeichern und mehr Ihrer Fusion-Organisation arbeiten.

Eine Liste der im Adobe Workfront Fusion MCP-Server verfügbaren Tools finden Sie unter [Adobe Workfront Fusion MCP-Server-Tools](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-fusion-mcp-server/fusion-mcp-server-tools.md).

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
   <p>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Voraussetzungen

Bevor Sie Fusion mit einer KI-Agent-Plattform verbinden können, müssen Sie Folgendes tun:

* Sie besitzen eine aktive Adobe Workfront Fusion-Lizenz und Zugriff auf mindestens eine Fusion-Organisation.
* Verwenden Sie eine Benutzerrolle und Teamrollen von Fusion, die Zugriff auf die Daten gewähren, mit denen Sie arbeiten möchten.
* Melden Sie sich mit einem Adobe ID (Adobe Identity Management System, IMS) an.
* Zugriff auf eine MCP-kompatible KI-Agentenplattform oder auf Coworker haben.

## Unterstützte MCP-Anwendungen

Der Fusion MCP-Server funktioniert mit den folgenden Anwendungen.

**Chat-Anwendungen**

* Claude Anthropica
* OpenAI ChatGPT
* Microsoft 365 Copilot

**Entwickler-Tools**

* Anthropischer Claude-Code
* Cursor
* GitHub-Copilot
* VS-Code
* OpenAI-Code
* MCP Inspector, mcp-remote und andere Tools, die einen lokalen Callback verwenden

**Automatisierungs- und KI-Plattformen**

* Adobe Workfront Fusion
* Google Vertex-KI-Suche
* Glean
* Writer AI Studio
* Postman

### Einschränkungen

* Nur die in diesem Abschnitt aufgeführten Anwendungen können eine Verbindung zum Fusion MCP-Server herstellen.
* Desktop-Programme und Befehlszeilenschnittstellen (CLIs) funktionieren, wenn sie den Anmeldungsrückruf auf Ihrem eigenen Computer erhalten (`localhost`).
* Sie können keine eigenen Programme hinzufügen. Um Unterstützung für ein neues Programm anzufordern, wenden Sie sich an das Fusion-Team unter [fusiondev@adobe.com](mailto:fusiondev@adobe.com).

<!-- BECKY CHECK ME: Other parts of this article might conflict with these limitations. See the comments in the important note below, in the section Connect Fusion to a custom MCP solution, and in the troubleshooting table. -->

>[!NOTE]
>
> Adobe veröffentlicht derzeit keinen Workfront Fusion-Connector im Claude-Connector-Verzeichnis oder im ChatGPT-App-/Plug-in-Verzeichnis. Um Fusion mit Claude, ChatGPT oder Microsoft Copilot zu verwenden, fügen Sie es als **benutzerdefinierten MCP-Server** nach URL hinzu, wie in diesem Artikel beschrieben.

Dieser Artikel führt Sie durch die Schritte zur Verbindung von:

* [Adobe-Mitarbeiter](#use-fusion-with-coworker): Mitarbeiter als eigenständiger Benutzer und Mitarbeiter in der rechten Leiste von Fusion
* [Claude](#connect-fusion-to-claude): Benutzerdefinierter Connector
* [ChatGPT](#connect-fusion-to-chatgpt): Benutzerdefinierter MCP-Server
* [Eine benutzerdefinierte MCP-Lösung](#connect-fusion-to-a-custom-mcp-solution)

>[!IMPORTANT]
>
>Wenn Sie eine andere MCP-kompatible Plattform verwenden, befolgen Sie die Dokumentation dieser Plattform, um einen benutzerdefinierten MCP-Server hinzuzufügen. Geben Sie nach Aufforderung zur Eingabe der MCP-Server-URL Folgendes ein:
>
>```
>https://mcp.fusion.adobe.com/mcp
>```

## Verwenden von Fusion mit einem Kollegen

Ein Mitarbeiter ist der KI-Agent von Adobe. Fusion ist in Coworker integriert, sodass Sie keine MCP-URL eingeben oder eine OAuth-App registrieren müssen. Sie können Coworker with Fusion an zwei Stellen verwenden:

* Coworker (standalone): Arbeiten Sie mit Fusion zusammen mit Ihren anderen Adobe-Apps.
* Mitarbeiter in der rechten Leiste von Fusion: Öffnen Sie den Mitarbeiter in einem Bedienfeld in der Benutzeroberfläche von Fusion.

Beide verwenden dieselben Fusion MCP-Tools, Ihren Adobe ID und Ihre Fusion-Berechtigungen. Die Einstellungen der Lese- oder Schreib-MCP-Tools gelten für beide. Destruktive Aktionen wie Löschen, Warteschlange löschen oder überschreiben fragen immer nach einer Bestätigung.

### Verwenden von Fusion in einem Kollegen

1. Offener Kollege. Sie finden ihn unter https://experience.adobe.com/#/coworker.
1. Öffnen Sie **Anpassungen** > **Integrationen**
1. Suchen oder suchen Sie **fusion-mcp** und klicken Sie darauf.
1. Klicken Sie im sich öffnenden Fenster auf **Test**.
1. Wenn Sie Zugriff auf mehr als eine Fusion-Organisation haben, wird sie automatisch ausgewählt. Sie können einen Kollegen bitten, die Organisation bei Bedarf später zu wechseln.

### Verwenden von Coworker in der rechten Leiste von Fusion

In Fusion wird Coworker in der rechten Leiste geöffnet

1. Anmelden bei Workfront Fusion.
1. Klicken Sie auf **Symbol &quot;**&quot; in der rechten Leiste.
1. Stellen Sie eine Frage im Bedienfeld.

### Beispiel-Prompts

* *Zeigen Sie mir alle Szenarien, die in den letzten 24 Stunden nicht ausgeführt wurden.*
* *Listen Sie alle Szenarien auf, die diese Woche erstellt oder gelöscht wurden, sortiert nach dem letzten Datum.*
* *Was macht dieses Szenario?*
* *Warum ist diese Ausführung fehlgeschlagen?*

## Fusion mit Claude verbinden

Fügen Sie Fusion als benutzerdefinierten Connector hinzu.

>[!NOTE]
>
> In Claude Team/Enterprise müssen Sie Besitzer sein, um einen benutzerdefinierten Connector hinzufügen zu können. Weitere Informationen finden Sie unter [Erste Schritte mit benutzerdefinierten Connectoren mit Remote-MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp) in der Claude-Dokumentation.

1. Anmelden bei [Claude](https://claude.ai).
1. Wählen Sie im linken Menü **Anpassen** aus.
1. Wählen Sie **Connectoren** aus.
1. Wählen Sie **+** und dann **Benutzerdefinierten Connector hinzufügen** aus.
1. Geben Sie einen Namen (z. B. &quot;Workfront Fusion„) und die MCP-Server-URL ein:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

1. Klicken Sie auf **Verbinden**.
1. Anmelden. Wählen Sie ein Profil und eine Fusion-Organisation aus.

Für Claude-Code können Sie den Server über die Befehlszeile hinzufügen:

```
claude mcp add --transport http fusion-mcp https://mcp.fusion.adobe.com/mcp
```

## Verbinden von Fusion mit ChatGPT

Fügen Sie Fusion als benutzerdefinierten MCP-Server hinzu.

### ChatGPT Desktop oder Codex

1. Öffnen Sie in ChatGPT **Einstellungen**.
1. Klicken Sie **Plugins**.
1. Klicken Sie **Server hinzufügen**.
1. Geben Sie einen Namen für den Server ein.
1. Wählen Sie für den Typ **Streamable HTTP** aus.
1. MCP-Server-URL eingeben:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

1. Klicken Sie auf **Speichern**.
1. Klicken Sie **Authentifizieren** für den neuen Server und melden Sie sich an.
1. Stellen Sie sicher, dass der Umschalter neben dem Server eingeschaltet ist.

### ChatGPT im Web

1. Melden Sie sich bei [ChatGPT) &#x200B;](https://chatgpt.com).
1. Navigieren Sie zu [https://chatgpt.com/plugins](https://chatgpt.com/plugins). (Der Entwicklermodus muss möglicherweise unter „Einstellungen **aktiviert werden** In Geschäfts-/Unternehmensplänen muss ein Administrator benutzerdefinierte Connectoren zulassen.)
1. Klicken Sie auf **+**.
1. Geben Sie einen &quot;**&quot;**.
1. Wählen Sie **Verbindung** die Option **Server-URL** und geben Sie die MCP-Server-URL ein.
1. Lassen Sie **Authentifizierung** auf **OAuth**.
1. Lesen Sie die Risikomeldung und aktivieren Sie das Kontrollkästchen.
1. Klicken Sie **Erstellen** und melden Sie sich mit Ihrer an.

## Zu einer anderen Fusion-Organisation wechseln

Sie müssen die Verbindung nicht trennen, um die Organisation zu wechseln. Der Fusion MCP-Server kann die aktive Organisation innerhalb einer Sitzung wechseln:

* _Welche Fusion-Organisationen habe ich?_
* _Wechseln Sie zur 1234-Organisation._

Der Agent verwendet `fusion_orgs_list` und `fusion_orgs_set`. Der Wechsel gilt nur für die aktuelle Konversation/Sitzung. Organisationen in verschiedenen Rechenzentrumszonen (z. B. USA und EU) sind alle über dieselbe MCP-URL verfügbar.

## Fehlerbehebung bei Setup und Authentifizierung

| Problem | Wahrscheinliche Ursache | Korrigieren |
| --- | --- | --- |
| Im Verzeichnis Claude oder ChatGPT kann kein Fusion-Connector gefunden werden. | Adobe veröffentlicht keinen Verzeichnis-Connector für Fusion. | Fügen Sie Fusion mithilfe der URL in diesem Artikel als benutzerdefinierten MCP-Server hinzu. |
| Sie können keinen benutzerdefinierten Connector in Claude oder ChatGPT hinzufügen. | Ihr Plan beschränkt benutzerdefinierte Connectoren auf Eigentümer oder Administratoren. | Bitten Sie Ihren Claude- oder ChatGPT-Administrator, den Connector hinzuzufügen oder benutzerdefinierte MCP-Server zuzulassen. |
| Sie haben verbunden, sehen aber keine oder falsche Daten. | Die falsche Fusion-Organisation ist aktiv. | Bitten Sie den Agenten, Ihre Organisationen aufzulisten und zur richtigen zu wechseln. |
| Die Authentifizierung ist fehlgeschlagen oder die Verbindung funktioniert nicht mehr. | Sitzung abgelaufen oder Verbindungsfehler. | Trennen Sie die Verbindung zum Server und stellen Sie sie wieder her. |
| Es wird eine Meldung angezeigt, dass der MCP-Zugriff deaktiviert ist. | Der MCP-Zugriff für Ihre Fusion-Organisation ist deaktiviert. | Bitten Sie Ihren Fusion-Administrator, es zu aktivieren. |
| Der Agent kann Szenarien lesen, sie jedoch nicht erstellen, ausführen, aktualisieren oder löschen. | MCP-Schreibwerkzeuge sind deaktiviert oder in der Team-Rolle nicht zulässig. | Bitten Sie Ihren Fusion-Administrator, Schreib-Tools zu aktivieren oder Ihnen die erforderliche Team-Rolle zu gewähren. |
| Benutzerdefinierte App-Authentifizierung wird abgelehnt. | Callback-URL ist nicht auf der Zulassungsliste. | Bitten Sie Ihren Administrator, die genaue Callback-URL hinzuzufügen. |
| Fusion wird nicht in der rechten Leiste von „Coworker“ aufgelistet oder Coworker fehlt in der rechten Leiste von Fusion. | Die Funktion ist für Ihre Organisation nicht aktiviert. | Wenden Sie sich an Ihren Fusion-Administrator. |

## Häufig gestellte Fragen

### Gibt es einen offiziellen Fusion-Connector für Claude oder ChatGPT?

Zurzeit nicht. Verwenden Sie die benutzerdefinierte MCP-Server-URL. Bei einem (eigenständigen und in der rechten Leiste von „Fusion“ befindlichen) Kollegen ist Fusion integriert.

### Kann ich mehr als eine Fusion-Organisation verwenden?

Ja. Sie können die aktive Organisation während eines Gesprächs wechseln, ohne die Verbindung erneut herzustellen.

### Was kann der Agent in meinem Namen tun?

Der Agent agiert wie Sie und verwendet dabei Ihre Fusion-Rolle und Team-Berechtigungen. Es hat keinen Zugriff auf irgendetwas, auf das man in Fusion nicht zugreifen kann. Destruktive Aktionen erfordern eine explizite Bestätigung.

### Sieht der Agent meine Verbindungsgeheimnisse?

Nein. Verbindungs- und Schlüssel-Tools geben Metadaten (Name, Typ, Bereiche, Gültigkeit) zurück, keine Anmeldeinformationen oder geheimen Werte.

