---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Benutzeroberflächen-Erweiterbarkeit - Übersicht
description: Benutzerdefinierte Erweiterungen in Workfront Fusion
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 835
ht-degree: 1%

---

# Benutzeroberflächen-Erweiterbarkeit - Übersicht

Die Erweiterbarkeit der Benutzeroberfläche ermöglicht es Ihnen, Ihre benutzerdefinierte Logik und Benutzeroberfläche (Benutzeroberfläche) in Adobe Workfront Fusion zu integrieren. Durch die Verwendung von Adobe App Builder können Sie das Workfront Fusion-Erlebnis Ihres Unternehmens so anpassen, dass es den Anforderungen des Unternehmens besser entspricht, und sich dabei weiterhin auf die Kernfunktionen von Fusion verlassen.

Dieser Artikel bietet einen Überblick über die Erweiterbarkeit der Benutzeroberfläche und darüber, wie Ihre benutzerdefinierte Erweiterung mit Workfront Fusion kommuniziert.

## Struktur einer Erweiterung

* [Gastgeber und Gäste](#hosts-and-guests)
* [Die Technologie darunter](#the-technology-underneath)

### Gastgeber und Gäste

Fusion kann eine Benutzeroberfläche anzeigen, die nicht vom Workfront Fusion-Team erstellt wurde. Um sicherzustellen, dass diese Änderungen an der Benutzeroberfläche die Kernfunktionalität von Fusion nicht beeinträchtigen, wird die Benutzeroberfläche in einem eigenen isolierten Browser-Frame (einem `<iframe>`) ausgeführt, der vollständig vom Code von Fusion getrennt ist.

* **Host**: Die Anwendung, *die Erweiterung*. Hier, das ist **Fusion**. Der Host entscheidet, wo Erweiterungen angezeigt werden können und welche Daten er für sie freigibt.
* **Gast**: *Ihre* Erweiterung. Es handelt sich dabei um eine kleine Webanwendung, die der Host in einen iFrame lädt.

Beim Erstellen einer UI-Erweiterung ändern Sie Fusion nicht. Sie erstellen und veröffentlichen einen Gast, den Fusion nach der Veröffentlichung des Gastes verwenden kann.

### Die Technologie darunter

Ihr Gast wird mit zwei Adobe-Technologien erstellt:

* **Adobe App Builder**: Eine kostenlose Hosting- und Toolingplattform für kleine Web-Anwendungen und Server-lose Aktionen. Ihre Erweiterung ist eine App Builder-App. App Builder bietet Ihnen einen Ort, an dem Sie Ihre Benutzeroberfläche (im `*.adobeio-static.net` Content Delivery Network von Adobe) und ein Befehlszeilen-Tool namens `aio` hosten können, um sie zu erstellen, zu erstellen und zu veröffentlichen.
* **Erweiterbarkeits-SDK für die Adobe-Benutzeroberfläche (UIX)**: Die Bibliotheken, über die Host und Gast sprechen können. Sie verwenden ein Paket, `@adobe/uix-guest`, auf Ihrer Seite. Fusion verwendet das passende `@adobe/uix-host` auf seiner Seite.

<!--

```
   ┌────────── Browser ─────────────────────────────┐
   │                                                                   │
   │   Fusion (Host)                      Your extension (Guest)       │
   │   ────────────                       ─────────────────────        │
   │   @adobe/uix-host   ◀── messages ──▶  @adobe/uix-guest            │
   │        │                                    │                     │
   │   renders an iframe ───────────────▶  your React/HTML UI          │
   │                                                                   │
   └───────────────────────────────────────────────────────────────────┘

   Your UI files are hosted by Adobe App Builder at
   https://<your-app>.adobeio-static.net
```

-->

## Erweiterungspunkte

Ein Erweiterungspunkt ist ein „Slot“ im Host, in dem ein Gast erscheinen darf. Fusion definiert seine Slots, und Sie wählen, welche der Gast benutzen wird.

Der Name eines Erweiterungspunkts besteht aus drei Teilen: `service/name/version`.

Fusion bietet die folgenden Erweiterungspunkte:

| Erweiterungspunkt | Wo Ihre Benutzeroberfläche in Fusion angezeigt wird | Einsatz |
| --- | --- | ---- |
| `fusion/nav-organization/1` | Im Abschnitt **Organisation** der linken Navigationsleiste. | Ihr Tool gilt für die gesamte Organisation. |
| `fusion/nav-team/1` | Im Abschnitt **Team** des linken Navigationsbereichs (wird angezeigt, wenn ein Team ausgewählt wird). | Ihr Tool bezieht sich auf ein bestimmtes Team. |

* `fusion` ist der **Service** (das Produkt, Fusion).
* `nav-organization` / `nav-team` ist der **Name** (der spezifische Slot).
* `1` ist die **Version**.

Eine Erweiterung kann einen oder beide Erweiterungspunkte implementieren. Die meisten Erweiterungen verwenden einen Punkt.

Je nachdem, welcher Erweiterungspunkt ausgewählt ist, fügt Fusion eine Schaltfläche mit dem Titel der Erweiterung zum entsprechenden Navigationsbereich hinzu. Wenn Sie darauf klicken, wird eine dedizierte Seite im Hauptinhaltsbereich von Fusion geöffnet und Ihre Benutzeroberfläche wird dort geladen.

## In einer UI-Erweiterung enthaltene Frames

>[!IMPORTANT]
>
>In diesem Abschnitt wird ein Aspekt von Benutzeroberflächenerweiterungen behandelt, der zu Verwirrung führen kann. Wir empfehlen, es sorgfältig zu lesen.

Wenn Fusion Ihren Gast lädt, wird Ihre Erweiterung in **zwei** Frames ausgeführt:

1. **Der Registrierungsrahmen (unsichtbar).** Läuft zuerst, im Hintergrund. Der Registrierungsrahmen teilt Fusion mit, was Ihre Erweiterung bietet. Beispielsweise kann es angeben, dass es über ein Dashboard-Widget verfügt, und den Titel des Widgets und die URL seiner Benutzeroberfläche senden. Der Registrierungsrahmen tut dies, indem er `register(...)` aufruft. Es wird keine sichtbare Benutzeroberfläche gerendert.
1. **Der UI-Frame (sichtbar).** Dies ist die Seite, die Fusion dem Benutzer zeigt. Sie muss sich selbst beim Host ankündigen, indem sie `attach(...)` aufruft. Wenn es nie `attach` aufruft, wartet Fusion und schließlich wird es mit einem Fehler beendet.

>[!BEGINSHADEBOX]

Dieses Beispiel zeigt den Fluss, wenn ein Benutzer auf die Schaltfläche Erweiterung klickt.

1. Die Schaltfläche wird angeklickt.
1. Fusion lädt Ihren REGISTRIERUNGS-Frame (ausgeblendet).

   ```
   register({ methods: { dashboard: { getWidget() {...} } } })
   ```

   `getWidget()` gibt die URL Ihrer sichtbaren Benutzeroberfläche zurück
1. Fusion lädt Ihren UI-Frame (sichtbar) unter dieser URL.

   ```
   attach({ id }) 
   ```

   Dies ist erforderlich, oder bei Fusion tritt eine Zeitüberschreitung auf
1. Fusion sendet Kontext, und die Benutzeroberfläche wird gerendert.

>[!ENDSHADEBOX]

Beide Frames werden beim Erstellen der Benutzeroberfläche geschrieben. Wichtig ist, sich daran zu erinnern, dass die sichtbare Seite **muss** `attach` aufruft.

Weitere Informationen zum Erstellen der Benutzeroberfläche finden Sie unter [Erstellen der benutzerdefinierten Erweiterungs-Benutzeroberfläche](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).

## Kontext aus Fusion

Nachdem die Erweiterung angehängt wurde, gibt Fusion ein `context`-Objekt für Ihren Gast frei. Sie enthält Folgendes:

* **Benutzer**: Das Fusion-Profil und die Adobe IMS-Benutzer-ID des angemeldeten Benutzers.
* **Organisation**: Der vollständige Fusion-Organisationsdatensatz der aktiven Organisation und die Adobe IMS-Organisations-ID.
* **Team**: Das aktive Team, falls zutreffend.
* **Adobe IMS-Zugriffstoken**: Dadurch werden bei Bedarf Adobe- oder Fusion-APIs im Namen des Benutzers aufgerufen.

Fusion überträgt auch Aktualisierungen. Wenn der Benutzer beispielsweise die Organisation oder das Team wechselt, während die Benutzeroberfläche geöffnet ist, sendet Fusion den neuen Kontext, damit die Benutzeroberfläche sofort reagieren kann.

Eine vollständige Liste der Kontextfelder finden Sie unter [Die Fusion-Kontextreferenz](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

## Erstellen einer UI-Erweiterung

Gehen Sie wie folgt vor, um eine Benutzeroberflächenerweiterung zu erstellen:

1. [Installieren Sie Tools und erstellen Sie ein Adobe-Projekt](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
1. [Generieren Sie ein leeres App Builder-Projekt, richten Sie es auf einen Fusion-Erweiterungspunkt und registrieren Sie Ihr Widget](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).
1. [Erstellen Sie die Benutzeroberfläche und verbinden Sie sich mit Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).
1. [Verwenden Sie den Kontext, den Fusion sendet](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).
1. [Veröffentlichen, damit Fusion es finden kann](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. (Optional) [Rufen Sie Workfront/Fusion-APIs für echte Daten ohne CORS auf](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).

Um mit dem Vorgang zu beginnen, gehen Sie zu [Tools und Adobe-Konto einrichten](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).


