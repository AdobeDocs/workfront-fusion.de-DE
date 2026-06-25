---
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---
# Referenzvorlagen für Versionshinweise

Detaillierte Vorlagen für jeden Seitentyp der Versionshinweise Diese basieren auf den Vorlagen in
`help/quicksilver/product-announcements/product-releases/release-note-templates/` und
Die tatsächliche Formatierung, die in den letzten vierteljährlichen Versionen verwendet wurde.

---

## Vorlage für die Produktbereichsseite

```markdown
---
title: {Written Quarter} {Year} {Area} enhancements
description: {Written Quarter} {Year} {Area} enhancements
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---
# {Written Quarter} {Year} {Area} enhancements

This page describes {Area} enhancements made with the {Written Quarter} {Year} release to the Preview environment. These enhancements will be made available in the Production environment as noted.

For a list of all changes available at this point in the {Written Quarter} {Year} release cycle, see [{Written Quarter} {Year} release overview](/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-release-overview.md).

## Feature Title Here

>[!NOTE]
>
>Preview: {Month Day, Year}
>Production fast release: {Month Day, Year}
>Production for everyone: {Month Day, Year}

Feature description paragraph.

For more information, see [Help article title](/help/quicksilver/path/to/article.md).
```

### Regeln für Produktbereichsseiten

- Markdown (nicht HTML) für Textinhalte verwenden
- Jede Funktion erhält eine H2-Überschrift
- Die `>[!NOTE]`-Legende muss eine leere Zeile vor sich haben
- Das `>[!NOTE]` ist genau:

  ```
  >[!NOTE]
  >
  >Preview: {date}
  >Production fast release: {date}
  >Production for everyone: {date}
  ```
- Wenn eine Funktion vorübergehend entfernt wurde, fügen Sie nach dem Datum eine Zeile hinzu:

  ```
  >
  >This feature has been temporarily removed from the Production environment on {date}.
  ```
- Hilfe-Links verwenden absolute Pfade, die mit `/help/quicksilver/` beginnen.

---

## Vorlage für Übersichtsseite

```markdown
---
title: {Written Quarter} {Year} release overview
description: This page provides information about functionality that is included in the {Written Quarter} {Year} release. These enhancements are planned to become available in the Production environment throughout the quarter.
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---
# {Written Quarter} {Year} release overview

This page provides information about functionality that is included in the {Written Quarter} {Year} release scheduled for {Release Month} {Year}.

The enhancements on this page are available in the Preview environment. This page will be updated with additional enhancements as the {Written Quarter} {Year} release nears its planned Production release.

>[!IMPORTANT]
>
>
>Monthly and quarterly releases are planned to be available on the Thursday of the second full week of the month, unless otherwise specified.
>
>|Monthly release|Quarterly release|
>|----|----|
>|<ul><li>{VV}.{M} ({Month Day, Year})</li><li>{VV}.{M} ({Month Day, Year})</li><li>{VV}.{M} ({Month Day, Year})</li></ul>|<ul><li>{VV}.{M} ({Month Day, Year})</li></ul>|
>
>Note that for the final release of each quarter ({VV}.{M} this quarter), users on the fast release schedule will receive the release one day early ({Month Day, Year}).
>
>For more information on the fast release process, see [Enable or disable the fast release process](/help/quicksilver/administration-and-setup/set-up-workfront/configure-system-defaults/enable-fast-release-process.md).

## Adobe Workfront enhancements

* [Administrator enhancements](#administrator-enhancements)
* [Document enhancements](#document-enhancements)
* [Project enhancements](#project-enhancements)
* [Reporting enhancements](#reporting-enhancements)
* [Requesting enhancements](#requesting-enhancements)
* [Other enhancements](#other-enhancements)
```

### Übersicht über die Funktionstabelle

Jeder Abschnitt des H3-Produktbereichs enthält eine HTML-Tabelle. Verwenden Sie genau diese Struktur:

```html
### {Area} enhancements

<table>
            <col style="width: 50%;" />
            <col style="width: 25%;" />
            <tbody>
              <tr>
        <td><strong>Feature</strong>
        </td>
        <td><strong>Preview</strong></td>
        <td><strong>Fast release</strong></td>
        <td><strong>Quarterly</strong></td>
        </tr>
    <tr>
        <td>
            <a href="/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-{area}.md" class="MCXref xref" xrefformat="{para}">Feature Title</a><p>Short description of the feature.</p>
        </td>
        <td><p>{Month Day, Year}</p></td>
        <td><p>{Month Day, Year}</p></td>
        <td><p>{Month Day, Year}</p></td>
    </tr>
            </tbody>
        </table>
```

#### Tabellenregeln

- Funktionszelle: `<a>` Tag mit `class="MCXref xref" xrefformat="{para}"` gefolgt von `<p>` Beschreibung
- Die `href` verweist auf die Produktbereichsseite (kein spezifischer Anker)
- Datumszellen: in `<p>` Tags eingeschlossen
- Fügen Sie bei außerplanmäßigen Elementen `<p>[!BADGE Off schedule]{type=Neutral}</p>` nach dem Link hinzu
- Leere `<p></p>` nach dem Link ist akzeptabel, wenn kein Abzeichen benötigt wird
- HTML-Einzüge konsistent mit bestehenden Dateien halten

### Nachfolgende Abschnitte - Übersicht

Nach allen Produktbereichstabellen:

```markdown
## Release notes for other areas

### Workfront Fusion enhancements

New features in Workfront Fusion are available in Production at a cadence outside of the standard release schedule. For more information about the latest features, see [Adobe Workfront Fusion release activity](https://experienceleague.adobe.com/en/docs/workfront-fusion/using/fusion-release-activity/fusion-release-activity).

### Workfront Planning enhancements

New features in Workfront Planning are available in Production. For more information about the latest features, see [{Written Quarter} {Year} release activity for Adobe Workfront Planning](/help/quicksilver/product-announcements/product-releases/planning-release-activity/planning-release-activity-{YY}-q{N}.md).

There are no updates for the following at this point in the release:

* Scenario Planner
* Proof
* Goals

## Desktop proofing viewer updates

{Version info if available, otherwise omit section}

## Announcements

{Announcement content}

### API version {NN}

{API version info}

### Workfront Maintenance Updates

For information about the maintenance updates made during the {Written Quarter} {Year} release, see [Workfront Maintenance Updates](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html).

### Training updates

Explore the latest updates made to learning programs, learning paths, videos, and guides for each Adobe Workfront product release. For more information, see the "What's New" section of the [Workfront Tutorials page](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/home.html).
```

---

## Seitenvorlage für Look-and-Feel

```markdown
---
title: Look-and-feel updates during the {Written Quarter} {Year} release time frame
description: Look-and-feel updates during the {Written Quarter} {Year} release time frame
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---

# Look-and-feel updates during the {Written Quarter} {Year} release time frame

This page describes minor updates to the look and feel of various areas of the Adobe Workfront application that were made within the {Written Quarter} {Year} release timeframe. These enhancements will be made available in the Production environment a minimum of 2 weeks after releasing to Preview.

For a list of all changes available with the {Written Quarter} {Year} release, see [{Written Quarter} {Year} Release overview](/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-release-overview.md).

## Feature Title

>[!NOTE]
>
>Preview release: {Month Day, Year}; Planned Production release: {Month Day, Year}

Description of the look-and-feel change.
```

---

## Datumsbeschriftungsformate

### Produktbereichsseiten (mehrzeilig)

```markdown
>[!NOTE]
>
>Preview: March 5, 2026
>Production fast release: April 15, 2026
>Production for everyone: April 16, 2026
```

### Look-and-Feel-Seiten (einzeilig)

```markdown
>[!NOTE]
>
>Preview release: March 5, 2026; Planned Production release: March 19, 2026
```

### Wöchentliche Seiten (einzeilig)

```markdown
>[!NOTE]
>
>Preview release: February 9, 2023; Planned Production release: February 23, 2023
```

---

## Bekannte Inkonsistenzen, auf die gewartet werden muss

1. **Falscher Übersichts-Link** - Produktbereichsseiten enthalten manchmal Links zur Übersicht des Vorquartals (z. B. `26-q1` statt `26-q2`)
2. **Vorschaudaten zeigen falsches Jahr an** — Übersichtstabellen zeigen manchmal das Vorjahr in der Vorschauspalte an (z. B. „2025“ anstelle von „2026„)
3. **Fehlende schließende `</tr>`-Tags** - Einige HTML-Tabellenzeilen verfügen nicht über geeignete schließende Tags
4. **`content-type: release-notes`** - In älteren Dateien vorhanden, in neueren Produktbereichsseiten im 26. Quartal 2 weggelassen. Folgt dem Muster des aktuellen Quartals.
5. **Tippfehler in der Vorlage** - Die Look-and-Feel-Vorlage enthält `relesae` anstelle von `release`. Verwenden Sie immer die richtige Schreibweise
6. **Fehlende `<p></p>` nach Funktions-** - In einigen Übersichtstabellenzeilen wird das leere `<p>`-Tag nach dem `<a>`-Tag weggelassen
