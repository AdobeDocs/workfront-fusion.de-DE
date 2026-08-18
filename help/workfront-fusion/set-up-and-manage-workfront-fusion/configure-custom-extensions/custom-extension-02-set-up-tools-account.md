---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Einrichten von UI-Erweiterungstools und -Konto
description: Einrichten von UI-Erweiterungstools und -Konto
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 500
ht-degree: 0%

---


# Einrichten von UI-Erweiterungstools und -Konto

Bevor Sie eine Benutzeroberflächenerweiterung für Workfront Fusion erstellen können, müssen Sie Ihre Tools und Ihr Konto einrichten. Dies muss nur einmal geschehen.

>[!NOTE]
>
>Dieser Artikel setzt eine gewisse Vertrautheit mit Software-Entwicklungs-Tools voraus.

<!--Access requirements-->

## Voraussetzungen

Um Ihre Tools und Ihr Konto für die Benutzeroberflächen-Erweiterbarkeit einzurichten, benötigen Sie Folgendes:

* **Eine Adobe ID** mit Zugriff auf eine Adobe-Organisation. Dies ist das Konto, mit dem Sie sich bei Fusion anmelden.
* **Entwicklerzugriff auf App Builder.** Ihr Organisationsadministrator muss Ihnen möglicherweise die Rolle **Entwickler** gewähren und Sie einem **Produktprofil“**, das App Builder enthält. Wenn Befehle später mit „Sie sind kein Entwickler“ fehlschlagen oder Ihr Unternehmen nicht angezeigt wird, bitten Sie Ihren Adobe-Organisationsadministrator, Sie hinzuzufügen.
* **Ein Systemadministrator** <!--Adobe? Fusion?--> (möglicherweise jemand anderes in Ihrem Team) für den letzten Veröffentlichungsschritt. Für das Erstellen und Bereitstellen ist nur die Rolle „Entwickler“ erforderlich **„Zum Übermitteln einer Erweiterung zur Genehmigung/Veröffentlichung ist jedoch die Rolle „Systemadministrator“**.

  Weitere Informationen zu Zugriffsebenen für Adobe finden Sie unter
  [So erhalten Sie Zugriff](https://developer.adobe.com/uix/docs/guides/get-access/) in der Dokumentation zu Adobe.

* **Ein Computer, auf dem Sie Software installieren** Terminal-Befehle ausführen können (macOS, Windows oder Linux).

## Installieren von Node.js

Das Adobe-Tool wird auf **Node.js** ausgeführt. Sie müssen die Version **LTS** (18 oder 20) installieren.

1. Gehen Sie zu <https://nodejs.org> und laden Sie das **LTS**-Installationsprogramm herunter.
1. Führen Sie das Installationsprogramm aus und akzeptieren Sie die Standardeinstellungen.
1. Bestätigen Sie, dass es funktioniert hat, indem Sie ein Terminal öffnen und Folgendes ausführen:

   ```sh
   node --version
   npm --version
   ```

   Es sollten Versionsnummern angezeigt werden (z. B. `v20.17.0` und `10.x`).

1. (Bedingt) Wenn `node` nicht gefunden wird, schließen und öffnen Sie das Terminal erneut oder starten Sie den Computer neu.

1. Fahren Sie mit [Installieren des Adobe I/O-CLI (`aio`)) ](#install-the-adobe-io-cli-aio).

>[!TIP]
>
>* Wenn Sie mit mehreren Knotenversionen arbeiten, ist ein Versionsmanager wie `nvm` praktisch, aber er ist optional.
>* Für die Adobe-CLI ist Knoten 18 oder neuer erforderlich. Sehr neue Nicht-LTS-Versionen können gelegentlich Probleme verursachen. Daher empfehlen wir die Verwendung von LTS.

## Installieren des Adobe I/O-CLI (`aio`)

Das Befehlszeilen-Tool, mit dem Sie Ihre Erweiterung erstellen, erstellen und veröffentlichen, heißt `aio`.

So installieren Sie es global:

1. Verwenden Sie den folgenden `npm`-Befehl in der Befehlszeile.

   ```sh
   npm install -g @adobe/aio-cli
   ```

1. Vergewissern Sie sich mithilfe des folgenden Befehls, dass es installiert ist:

   ```sh
   aio --version
   ```

   Du solltest so etwas wie `@adobe/aio-cli/11.x.x` sehen.

1. Fahren Sie [Bei Adobe anmelden](#sign-in-to-adobe) fort.

>[!NOTE]
>
> Wenn unter macOS/Linux ein Berechtigungsfehler angezeigt wird, verwenden **nicht** die `sudo`. Korrigieren Sie stattdessen die globalen Ordnerberechtigungen von npm oder verwenden Sie einen Knotenversions-Manager, der in Ihr Basisverzeichnis installiert wird.

## Bei Adobe anmelden

1. Verbinden Sie die CLI mit dem folgenden Befehl mit Ihrem Adobe-Konto:

   ```sh
   aio login
   ```

1. Melden Sie sich in dem sich öffnenden Browser-Fenster bei Ihrer Adobe ID an und genehmigen Sie den Zugriff.

1. Schließen Sie nach erfolgreicher Anmeldung die Browser-Registerkarte und kehren Sie zum Terminal zurück.

1. (Optional) Um sich später abzumelden (z. B. um zu einem anderen Konto zu wechseln), verwenden Sie den Befehl: `aio logout`.
1. Fahren Sie fort [Bestätigen Sie Ihre aktive Organisation](#confirm-your-active-organization).

## Bestätigen der aktiven Organisation

Überprüfen Sie, auf welche Organisation das CLI verweist:

```sh
aio console org list      # see organizations you can use
aio console where         # see your currently selected org/project/workspace
```

Wenn Sie mehreren Organisationen angehören, wählen Sie die richtige aus:

```sh
aio console org select
```

Jetzt können Sie das Projekt erstellen.
