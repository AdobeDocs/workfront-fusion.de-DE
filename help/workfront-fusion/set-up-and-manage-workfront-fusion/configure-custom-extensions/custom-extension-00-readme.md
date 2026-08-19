---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 'Benutzerdefinierte UI-Erweiterungen: Artikelindex'
description: Benutzerdefinierte Erweiterungen in Workfront Fusion
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 603
ht-degree: 3%

---


# Benutzerdefinierte UI-Erweiterungen: Artikelindex

Fusion kann in seiner Benutzeroberfläche Ihre eigene Web-Benutzeroberfläche anzeigen. Sie erstellen eine kleine Web-Anwendung, eine so genannte Erweiterung, veröffentlichen sie in Adobe und sie erscheint als Schaltfläche in der Navigation von Fusion. Wenn ein Benutzer darauf klickt, wird Ihre Benutzeroberfläche im Hauptbereich von Fusion geladen und erhält automatisch Informationen darüber, wer angemeldet ist, in welcher Organisation und in welchem Team er arbeitet, und mehr.

Dieser Abschnitt der Fusion-Dokumentation führt Sie durch den gesamten Prozess, ohne Vorkenntnisse mit Adobe App Builder oder Frontend-Frameworks vorauszusetzen. Sie enthält auch den erforderlichen Code sowie Erläuterungen zu diesem Code.

## Verwendung dieses Handbuchs

Verwenden Sie dieses Handbuch, wenn Sie einen benutzerdefinierten Bildschirm oder ein benutzerdefiniertes Tool zu Fusion hinzufügen möchten. Sie müssen kein erfahrener Entwickler sein. Sie müssen sich nicht damit abfinden, Befehle in ein Terminal zu kopieren und einige Textdateien zu bearbeiten.

Um eine benutzerdefinierte Benutzeroberflächenerweiterung zu erstellen, benötigen Sie eine Adobe ID und Zugriff auf eine Adobe-Organisation (dieselbe Art von Zugriff, die Sie zum Anmelden bei Fusion verwenden).

## Was Sie erstellen werden

Am Ende dieses Handbuchs werden Sie über Folgendes verfügen:

1. Ein kostenloses Adobe **App Builder**-Projekt. Hier wohnt Ihre Erweiterung.
1. Eine kleine Web-App, die Ihre benutzerdefinierte Benutzeroberfläche rendert.
1. Diese Web-App ist mit einem der Erweiterungspunkte von Fusion verbunden, sodass sie in der Navigation von Fusion angezeigt wird.
1. Ihre Benutzeroberfläche liest Live-Kontext von Fusion, z. B. den aktuellen Benutzer, die Organisation und das Team, und reagiert, wenn der Benutzer die Organisation oder das Team wechselt.
1. Die Erweiterung wurde veröffentlicht, damit sie andere Benutzende in Ihrer Organisation sehen können.

<!--

## How it works, in one picture

```
  Fusion (the "Host")                         Your extension (the "Guest")
  ───────────────────────────────                         ──────────────────────────────
  Left navigation                             A web app hosted by Adobe
   └── Organization                            (App Builder + UI Extensibility)
       └── [Your extension button]  ── click ──▶ Fusion opens your UI in an iframe
                                              and sends it live context:
                                               * signed-in user
                                               * active organization
                                               * active team
                                               * Adobe IMS identifiers
```

Fusion is the **host**. Your extension is the **guest**. They run in separate browser frames and talk to each other through Adobe's **UI Extensibility SDK** (no custom networking required on your side).

-->

## Inhaltsverzeichnis

Lesen Sie die Seiten das erste Mal in der richtigen Reihenfolge. Später können Sie direkt zu dem springen, den Sie benötigen.

| # | Seite | Was es abdeckt |
| --- | ------ | ---------------- |
| 1 | [Überblick und Schlüsselkonzepte](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md) | Das Vokabular, die Architektur und wofür jeder Fusion-Erweiterungspunkt bestimmt ist. |
| 2 | [Richten Sie Ihre Tools und Ihr Adobe-Konto ein](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md) | Node.js, die Adobe I/O-CLI, die Anmeldung und die Erstellung Ihres Projekts in der Adobe Developer Console. |
| 3 | [Erstellen Sie das Projekt und konfigurieren Sie es für Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md) | Generieren Sie ein generisches App Builder-Projekt mit der `aio` Befehlszeile (keine produktspezifische Vorlage). Verweisen Sie dann Ihr Projekt auf einen Fusion-Erweiterungspunkt und registrieren Sie Ihr Widget. |
| 5 | [Erstellen der Benutzeroberfläche](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md) | Rendern Sie Ihren benutzerdefinierten Bildschirm und schließen Sie die Verbindung („Handshake„) mit Fusion ab. |
| 6 | [Die Fusion-Kontextreferenz](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md) | Jedes Feld sendet Ihnen, was es bedeutet und wie Sie auf Änderungen reagieren können. |
| 7 | [Veröffentlichen Sie Ihre Erweiterung](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md) | Erstellen, Bereitstellen und Anzeigen der Erweiterung in Fusion. |
| 8 | [Fehlerbehebung](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md) | Korrekturen der häufigsten Fehler. |
| 9 | [Anleitung zur Demo](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-09-demo-walkthrough.md) | Ein lineares Skript zum Kopieren und Einfügen: Strukturvorlage aus der generischen Experience Cloud-Shell-Vorlage → erneut auf Fusion ausgerichtet → für die Staging-→ in Fusion bereitgestellt. Am besten für eine Live-Demo. |
| 10 | [Aufrufen von Workfront- und Fusion-APIs](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md) | Rufen Sie Backend-APIs über Ihre Erweiterung auf, ohne das CORS des Browsers zu erreichen, indem Sie einen Laufzeitaktions-Proxy verwenden. Behandelt `require-adobe-auth`, Fusion v3-Kopfzeilen und ein Beispiel. |

## Hinweis zur Verfügbarkeit

Fusion legt derzeit diese Erweiterungspunkte offen:

* `fusion/nav-organization/1` — wird im Abschnitt **Organisation** angezeigt.
* `fusion/nav-team/1` — wird im Abschnitt **Team** angezeigt.

Bevor Sie eine dieser Erweiterungspunkte veröffentlichen können, muss der Erweiterungspunkt für Ihr Adobe-Unternehmen integriert werden. Wenn beim Veröffentlichungsschritt nicht angegeben wird, dass der Erweiterungspunkt „nicht vorhanden“ ist, finden Sie weitere Informationen unter [Fehlerbehebung](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

## Offizielle Adobe-Dokumentation

Dieses Handbuch ist für Fusion spezifisch. Für die zugrunde liegende Plattform lauten die kanonischen Referenzen:

* [Benutzeroberflächen-Erweiterbarkeit - Übersicht](https://developer.adobe.com/uix/docs/)
* [Entwicklungsablauf für UI-Erweiterungen](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [Verwaltung von UI-Erweiterungen (Veröffentlichen/Genehmigen/Sperren)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Erste Schritte mit Adobe App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
