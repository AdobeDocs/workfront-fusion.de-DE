---
title: Hinzufügen einer KI-Eingabeaufforderung zu Ihrem Szenario
description: Sie können in Ihr Szenario eine KI-Eingabeaufforderung einfügen, die eine Verbindung zu Ihrem
author: Becky
feature: Workfront Fusion
source-git-commit: 09e8ca28c12990a699816671d07f85288d973bc7
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Hinzufügen einer KI-Eingabeaufforderung zu Ihrem Szenario

Sie können eine KI-Eingabeaufforderung in Ihr Szenario einfügen, indem Sie das Model Context Protocol (MCP) in Kombination mit großen Sprachmodellen (LLMs) verwenden. Wenn Sie diese im MCP Agent-Modul konfigurieren, können Sie mit künstlicher Intelligenz Workflows einrichten, die effizient, sicher und flexibel sind.

>[!NOTE]
>
>Diese Funktion ist unabhängig von der Möglichkeit, einem Szenario mithilfe von KI Module hinzuzufügen.
>
>Informationen zum Hinzufügen von Modulen mit KI finden Sie unter [Generieren eines Szenario-Segments mit KI](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-with-ai.md).

## Übersicht über das Modell-Kontextprotokoll

Das Model Context Protocol (MCP) ist eine Möglichkeit, KI-Sprachmodelle sicher mit anderen Anwendungen zu verbinden. Sie konfigurieren MCP-Server, die dem KI-Modell den Zugriff auf die Anwendung ermöglichen. Sie können dann eine Eingabeaufforderung an das KI-Modell senden und es kann Informationen aus der Anwendung zurückgeben.

Sie können beispielsweise einen MCP-Server konfigurieren, um ein KI-Modell mit Gmail zu verbinden. Wenn Sie die Eingabeaufforderung „Give me my last 5 emails from Gmail“ an das große Sprachmodell senden, analysiert es diese Eingabeaufforderung und sendet sie an den Gmail MPC-Server, der dann auf Ihre Gmail-Adresse zugreifen und die E-Mails zurücksenden kann.

Das MCP Agent-Modul ermöglicht die Verarbeitung einer Benutzeraufforderung mithilfe eines Sprachmodells und MCP-Servern.

## Vorteile der Verwendung von MCP in Ihren Fusion-Szenarien

Die Verwendung von MCP in Ihren Szenarien bietet die folgenden Vorteile:

* Die Verwendung von MCP in Ihrem Szenario reduziert die Notwendigkeit, alle Situationen und möglichen Varianten einer Aktion zu durchdenken. Durch die Verwendung einer Eingabeaufforderung müssen Sie keine Regex- oder Analysedaten mehr verwenden, um diese Varianten zu berücksichtigen.
* Sie können für die Eingabeaufforderung Kontext bereitstellen, indem Sie Elemente verwenden, die aus vorherigen Modulen zugeordnet sind, oder andere Funktionen im Zuordnungsbereich verwenden.
* Die Verwendung einer Eingabeaufforderung kann effizienter und flexibler sein als das Erstellen eines Szenarios mit bestimmten Modulen, da sie bei der Eingabeaufforderung Argumentation verwenden und die beste Vorgehensweise aus dem verfügbaren Kontext auswählen kann.
* Da Sie die MCP-Server konfigurieren, mit denen das Modul eine Verbindung herstellen kann, steuern Sie die Sicherheit für diesen Server und können sicherstellen, dass die Sicherheit den Anforderungen Ihres Unternehmens entspricht.

>[!NOTE]
>
>Die verfügbaren Funktionen hängen von den im MCP-Server verfügbaren Tools ab und werden nicht von Fusion gesteuert.

## Hinzufügen einer KI-Eingabeaufforderung zu Ihrem Szenario

Sie können Ihrem Szenario eine KI-Eingabeaufforderung hinzufügen, indem Sie das MCP Agent-Modul verwenden.

Anweisungen finden Sie unter [MCP Agent-Modul](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md).
