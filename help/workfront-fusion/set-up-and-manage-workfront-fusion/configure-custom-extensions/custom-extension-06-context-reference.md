---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Kontextreferenz zu Fusion
description: Kontextreferenz zu Fusion
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
source-wordcount: 757
ht-degree: 8%

---

# Kontextreferenz zu Fusion

>[!NOTE]
>
>Dieser Artikel setzt eine gewisse Vertrautheit mit Software-Entwicklungs-Tools voraus.

Wenn Ihre Benutzeroberfläche `attach(...)` aufruft, gibt Fusion ein **context**-Objekt frei, das die aktuelle Sitzung beschreibt. Auf dieser Seite werden alle Felder, ihre Bedeutung und die Beziehung zwischen den Fusion- und Adobe IMS-Kennungen aufgelistet.

## Lesen des Kontexts

* **Anfangswerte:** `connection.sharedContext.get("<key>")`
* **Updates:** Überwachen Sie das `contextchange`. Das neueste Objekt kommt am `event.detail.context` an.

Das vollständige Code-Muster finden Sie unter [Erstellen der benutzerdefinierten Erweiterungs-Benutzeroberfläche](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).

```js
const organization = connection.sharedContext.get("organization");
const fusionOrgId  = organization?.id;        // Fusion's organization id
const imsOrgId     = connection.sharedContext.get("imsOrgId"); // Adobe IMS org id
```

## Schlüssel der obersten Ebene

| Schlüssel | Typ | Beschreibung |
| ----- | ------ | ------------- |
| `imsToken` | string | Das Adobe-Zugriffstoken (IMS **des angemeldeten Benutzers**. Verwenden Sie dies als `Bearer`-Token, um Adobe- oder Fusion-APIs im Namen des Benutzers aufzurufen. **Da dies sensibel ist, sollten Sie dies niemals protokollieren oder anzeigen.** |
| `imsOrgId` | string | Die Adobe **IMS-Organisations** ID) in der `XXXXXXXXXXXX@AdobeOrg`. |
| `imsUserId` | string | Die Adobe **IMS-Benutzer** ID) des angemeldeten Benutzers. |
| `organization` | object | Die **aktive Fusion-Organisation**. Weitere Informationen finden Sie unter [`organization` Felder](#organization-fields) in diesem Artikel. |
| `team` | Objekt \| nicht definiert | Das **volle aktive Fusion-Team**, wenn man aktiv ist (immer relevant für `fusion/nav-team/1`). Weitere Informationen finden Sie unter [`team` Felder](#team-fields) in diesem Artikel. |
| `user` | object | Der **vollständig angemeldete Fusion-Benutzer**. Weitere Informationen finden Sie unter [`user` Felder](#user-fields) in diesem Artikel. |

### Fusions-ID und IMS-ID

Jede Entität verfügt über eine **Fusion-ID** (die von den Fusion-eigenen APIs verwendet wird) und, sofern vorhanden, eine **Adobe IMS-ID** (die von Adobe Platform-APIs verwendet wird):

| Entität | Fusion-ID | Adobe IMS-ID |
| -------- | ----------- | -------------- |
| Organisation | `organization.id` | `imsOrgId` (auch als `organization.externalOrgId` verfügbar gemacht) |
| Team | `team.id` | *(Teams sind nur Fusion; keine IMS-ID)* |
| Benutzerin oder Benutzer | `user.id` | `imsUserId` |

## Felder `organization`

Diese Felder befinden sich im aktiven Organisationsdatensatz. Die meisten Erweiterungen erfordern nur `id`, `name` und die Kennungen .

| Feld | Typ | Beschreibung |
| ------- | ------ | ------------- |
| `id` | string | Fusion-Organisations-ID. |
| `name` | string | Anzeigename der Organisation |
| `externalOrgId` | string | Adobe IMS-Organisations-ID (gleicher Wert wie `imsOrgId`). |
| `externalId` | string | Externe Kennung, die von Fusion-Integrationen verwendet wird |
| `countryId` | string | Ländereinstellungs-ID. |
| `timezoneId` | string | Zeitzoneneinstellungs-ID |
| `serviceName` | string | Service-/Plankennung |
| `teamIds` | Zeichenfolge[] | IDs der Teams in dieser Organisation |
| `license` | object | Planbeschränkungen und -berechtigungen wie Vorgänge, Datenübertragung, Benutzersitze und Feature Flags |
| `scenariosCount` | number | Gesamtzahl der Szenarien in der Organisation |
| `activeScenarios` | number | Derzeit aktive Szenarien |
| `activeApps` | number | Anzahl aktiver Apps oder Verbindungen |
| `operations`, `operationsExt` | number | Nutzungszähler für Vorgänge |
| `transfer`, `transferExt` | number | Nutzungszähler für die Datenübertragung |
| `isPaused` | Boolescher Wert | Ob die Organisation angehalten wurde |
| `isDeleted` | Boolescher Wert | Ob die Organisation als gelöscht markiert ist |
| `imsEnabled` | Boolescher Wert | Ob die Organisation mit Adobe IMS verknüpft ist |
| `usersCount` | number | Anzahl der Benutzer in der Organisation |
| `nextReset` | Zeichenfolge (Datum) | Beim nächsten Zurücksetzen der Nutzungszähler. Siehe [Daten](#dates) |

## Felder `team`

Diese Felder sind vorhanden, wenn ein Team aktiv ist. Für den Fall, dass das Team `undefined` wird (z. B. auf einem Bildschirm auf Organisationsebene, wo kein Team ausgewählt ist), müssen Sie einen Fallback bereitstellen.

| Feld | Typ | Beschreibung |
| ------- | ------ | ------------- |
| `id` | string | Fusion-Team-ID. |
| `name` | string | Anzeigename des Teams. |
| `organizationId` | string | Fusion-ID der Organisation, der dieses Team angehört. |
| `country` | string | Ländereinstellung des Teams. |
| `timezone` | string | Team-Zeitzone. |
| `license` | object | Beschränkungen und Berechtigungen auf Team-Ebene. |
| `activeScenarios` | number | Aktive Szenarien im Team. |
| `activeApps` | number | Aktive Apps oder Verbindungen im Team. |
| `scenarioDrafts` | Boolescher Wert | Ob Szenario-Entwürfe aktiviert sind. |
| `isDeleted` | Boolescher Wert | Ob das Team als gelöscht markiert ist. |
| `created` | Zeichenfolge (Datum) | Als das Team erstellt wurde. Siehe [Daten](#dates). |

## Felder `user`

Diese Felder gelten für den angemeldeten Fusion-Benutzer.

| Feld | Typ | Beschreibung |
| ------- | ------ | ------------- |
| `id` | string | Fusion-Benutzer-ID. |
| `name` | string | Vollständiger Name. |
| `email` | string | E-Mail-Adresse |
| `avatar` | string | Avatar-Bild-URL. |
| `locale` | string | Benutzergebietsschema, z. B. `en`. |
| `language` | string | Bevorzugte Sprache, wenn festgelegt. |
| `timezone` | string | Name der Zeitzone. |
| `timezoneId` | string | Zeitzoneneinstellungs-ID. |
| `countryId` | string | Ländereinstellungs-ID. |
| `localeId` | string | Gebietsschema-ID. |
| `features` | object | Feature Flags pro Benutzer (z. B. `allow_apps`, `public_templates`). |
| `usersAdminsRoleId` | string | Die Kennung der Administratorrolle des Benutzers, falls zutreffend. |

>[!NOTE]
>
> Das `user` kann zusätzliche interne Felder enthalten. Sie sollten sich nur auf die hier dokumentierten Felder verlassen. Andere Felder können sich ohne Vorankündigung ändern, und einige authentifizierungsbezogene Felder dürfen niemals protokolliert oder angezeigt werden.

## Daten

Der Kontext wird serialisiert, bevor er Ihre Erweiterung erreicht, sodass **Datumsfelder als Zeichenfolgen eintreffen** (ISO 8601, z. B. `"2026-06-24T00:00:00.000Z"`) und nicht als JavaScript `Date`-Objekte. Sie können diese bei Bedarf konvertieren:

```js
const resetDate = new Date(context.organization.nextReset);
```

## Kontextaktualisierungen

Fusion sendet den gesamten Kontext erneut (über `contextchange`), wenn:

* Der Benutzer **wechselt die Organisation**,
* der Benutzer **wechselt Teams** oder
* Die **des angemeldeten Benutzers** sich.

Lesen Sie immer alle Schlüssel erneut, die Sie in Ihrem `contextchange`-Handler verwenden, anstatt nur einen geänderten Wert anzunehmen.

## Best Practices für die Sicherheit

* **Nie protokollieren, anzeigen oder `imsToken` beibehalten.** Behandeln Sie sie wie ein Kennwort.
* Senden Sie das Token über HTTPS nur als `Bearer`-Token an vertrauenswürdige Adobe/Fusion-Endpunkte.
* Speichern Sie keine personenbezogenen Daten aus dem Kontext, der über das hinausgeht, was Ihre Funktion benötigt.

## Verwenden des Tokens zum Aufrufen von APIs

So wandeln Sie `imsToken` (plus `organization.id`/`team.id`) in echte Workfront um oder
Fusion-Daten können diese APIs nicht direkt über den Browser aufgerufen werden, da CORS blockiert
Es. Führen Sie den Aufruf stattdessen über eine kleine App Builder-Laufzeitaktion weiter. Siehe
[Aufrufen von Workfront- und Fusion-](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).


Um mit dem Erstellen einer benutzerdefinierten Erweiterung fortzufahren, siehe [Veröffentlichen der Erweiterung](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
