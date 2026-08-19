---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Veröffentlichen der benutzerdefinierten Erweiterung
description: Veröffentlichen der benutzerdefinierten Erweiterung
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
source-wordcount: 1236
ht-degree: 1%

---

# Veröffentlichen der benutzerdefinierten Erweiterung

>[!NOTE]
>
>Dieser Artikel setzt eine gewisse Vertrautheit mit Software-Entwicklungs-Tools voraus.

Ihre Erweiterung wird in Fusion erst ausgeführt, nachdem sie **erstellt** **bereitgestellt** in Adobe **und** wurde. Die Verfahren auf dieser Seite zeigen, wie Sie Ihre Erweiterung veröffentlichen und das Ergebnis überprüfen können.

Diese Informationen werden aus der offiziellen Adobe-Dokumentation übernommen und gelten speziell für Workfront Fusion. Allgemeine Informationen zu Adobe finden Sie unter [UI-Erweiterungs-Entwicklungsablauf](https://developer.adobe.com/uix/docs/guides/development-flow/) und [UI-Erweiterungsverwaltung](https://developer.adobe.com/uix/docs/guides/publication/) in der Dokumentation zu Adobe.

## Arbeitsbereiche

Jedes App Builder-Projekt verfügt über **Staging** und einen **Produktions** Arbeitsbereich. Betrachten Sie sie als Umgebungen:

* **Staging** dient der Entwicklung und dem Testen. Sie stellen hier bereit, während Sie iterieren. Es ist keine Genehmigung erforderlich und das Ergebnis ist nur über den unten beschriebenen Staging-Test-Schalter (oder die lokale Vorschau) sichtbar.
* **Produktion** dient der Freigabe für alle. Nach der Bereitstellung in der Produktionsumgebung übermitteln Sie eine **Genehmigungsanfrage** und nach der Genehmigung wird die Erweiterung in der Adobe-App-Registrierung registriert und für Ihr gesamtes Unternehmen angezeigt.

>[!NOTE]
>
> **Rollen:** Erstellen und Bereitstellen erfordert die Rolle **Entwickler**; das Senden der Genehmigungsanfrage zum Veröffentlichen erfordert die Rolle **Systemadministrator**.
>Weitere Informationen finden Sie unter:
>
> * [Einrichten von Tools und Konto für die Benutzeroberflächenerweiterung](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)
> * [So erhalten Sie Zugriff](https://developer.adobe.com/uix/docs/guides/get-access/) in der Dokumentation zu Adobe.

Standardmäßig zeigt Fusion nur **veröffentlichte** Erweiterungen an. Hierbei handelt es sich um Erweiterungen, die Sie im Arbeitsbereich **Produktion** bereitgestellt und dann zur (**)** haben. Dies ist die sichere Standardeinstellung, sodass eine laufende Bereitstellung Ihrer gesamten Organisation nie versehentlich angezeigt wird.

Eine Bereitstellung im **Staging**-Arbeitsbereich wird nicht veröffentlicht und daher nicht eigenständig in Fusion angezeigt. Es gibt zwei Möglichkeiten, eine Erweiterung zu testen, bevor Sie sie veröffentlichen:

* **Lokale Vorschau** mit `aio app run` (siehe [Lokale Vorschau von Benutzeroberflächenerweiterungen](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/) in der Dokumentation zu Adobe). Es wird nichts bereitgestellt, und nur Sie sehen es.
* **Laden Sie sie von Stage in Fusion** indem Sie einen Benutzer-Testschalter in Ihrem Fusion-Profil einschalten. Dies wird in [&#x200B; Artikel unter „Testen eines Staging-Builds in &#x200B;](#test-a-stage-build-in-fusion)&quot; beschrieben.

## Testen eines Staging-Builds in Fusion

Verwenden Sie diesen Fluss, um eine Staging-Bereitstellung in Fusion anzuzeigen, bevor Sie sie veröffentlichen.

### Schritt 1: Staging-Arbeitsbereich auswählen

```sh
aio console where                  # shows current org / project / workspace
aio console workspace select       # choose Stage
```

### Schritt 2: Erstellen

```sh
aio app build
```

Dadurch wird Ihr Frontend kompiliert und der Metadaten-Hook ausgeführt (der `app-metadata.json` generiert). Beheben Sie alle gemeldeten Fehler, bevor Sie fortfahren.

### Schritt 3: Bereitstellen

```sh
aio app deploy
```

`deploy` hat zwei Möglichkeiten:

* **Hostet Ihre** im Content Delivery Network von Adobe unter einer URL wie `https://<project>-stage.adobeio-static.net`. Die CLI druckt diese **Erweiterungs-Endpunkt-URL** nach Abschluss. Dies ist die URL, die Fusion in seinen iframe lädt.
* **Registriert die Endpunkte Ihrer** für den Erweiterungspunkt (`fusion/nav-organization/1`) im Staging-Arbeitsbereich.

>[!TIP]
>
> **Wenn die Bereitstellung mit „Erweiterungspunkt &#39;fusion/nav-organization/1&#39; existiert nicht“ fehlschlägt (Fehler 1060):** Der Fusion-Erweiterungspunkt ist für Ihre Organisation noch nicht aktiviert. Dies ist ein Onboarding-Schritt, kein Fehler in Ihrem Code.
>Weitere Informationen finden Sie unter [Erweiterungspunkt ist nicht vorhanden](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md#error-1060-extension-point-does-not-exist) im Artikel zur Fehlerbehebung.

### Schritt 4: Aktivieren Sie das Staging-Testing in Ihrem Fusion-Profil

Fusion lädt Staging-Erweiterungen nur beim Opt-in pro Benutzer:

1. Melden Sie sich bei Fusion mit einem Konto an, das **derselben Organisation**, für die Sie bereitgestellt haben.
1. Öffnen Sie das Benutzeravatar-Menü in der oberen Ecke und gehen Sie zu **Produkteinstellungen** > **Fusionsprofil** > **Voreinstellungen**.
1. Schalten Sie den **Staging-Erweiterungen** ein.

   Fusion fordert Sie zum Neuladen auf.
1. Bestätigen Sie das Neuladen.

Nach dem Neuladen lädt Fusion Erweiterungen aus dem Staging-Arbeitsbereich anstelle des veröffentlichten Sets und kennzeichnet jedes **(Staging)** in der Navigation, damit Sie es auseinanderhalten können.

Dieser Schalter ist eine persönliche Testeinstellung, die in Ihrem Browser gespeichert ist, keine Unternehmenseinstellung. Deaktivieren (und neu laden), um zu den veröffentlichten Erweiterungen zurückzukehren. Da es lokal gespeichert ist, folgt es Ihnen nicht zu einem anderen Browser oder Computer.

### Schritt 5: Überprüfen in Fusion

1. Öffnen Sie den Abschnitt, der Ihrem Erweiterungspunkt entspricht:
   * `fusion/nav-organization/1` → den Bereich **Organisation** im linken Navigationsbereich.
   * `fusion/nav-team/1` → den Bereich **Team** (wählen Sie zuerst ein Team aus).

   Eine Schaltfläche mit dem Titel, den Sie in `getWidget()` festgelegt haben, wird angezeigt, markiert **(Phase)**.
1. Klicken Sie auf die angezeigte Schaltfläche.

Ihre Benutzeroberfläche lädt und empfängt den [Fusion-Kontext](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

Wenn die Schaltfläche nicht angezeigt wird oder im Bedienfeld ein Fehler angezeigt wird, finden Sie weitere Informationen unter [Fehlerbehebung](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

## Produktionsfreigabe

Wenn Ihre Erweiterung in der Staging-Umgebung funktioniert und Sie für alle Benutzer bereit sind:

### Schritt 1: Wechseln Sie zum Arbeitsbereich Produktion .

```sh
aio console workspace select       # choose Production
```

Wenn Sie von der CLI zur `.env` der Datei aufgefordert werden, wählen Sie **Zusammenführen** aus, damit Ihre Umgebungsvariablen beibehalten werden.

### Schritt 2: Erstellen und für die Produktion bereitstellen

```sh
aio app build
aio app deploy
```

### Schritt 3: Validierungsanfrage einreichen

Die Veröffentlichung ist eine **Genehmigungsanfrage, die vom Produktionsarbeitsbereich gesendet wird**:

1. Öffnen Sie die [Adobe Developer Console](https://developer.adobe.com/console), wählen Sie Ihre **Organisation** aus, öffnen Sie Ihr **Projekt** und wechseln Sie zum Arbeitsbereich **Produktion**.
1. Senden Sie Ihre App zur **Genehmigung/Veröffentlichung** (hierfür ist die Rolle **Systemadministrator** erforderlich).
1. Nach der Genehmigung wird Ihre Erweiterung der **Adobe App Registry** hinzugefügt und steht für Ihr Unternehmen in [Adobe Experience Cloud](https://experience.adobe.com) einschließlich Fusion zur Verfügung.

Detaillierte Anweisungen finden Sie unter [Verwaltung von Benutzeroberflächenerweiterungen](https://developer.adobe.com/uix/docs/guides/publication/) in der Dokumentation zu Adobe Developer.

## Status und Updates

Einige Verhaltensweisen sind es wert, geklärt zu werden, sodass man „noch daran arbeitet“ von „irgendetwas stimmt nicht“ unterscheiden kann:

* **In der Produktion bereitgestellt ist nicht dasselbe wie sichtbar.** `aio app deploy` zur Produktion lädt Ihre App hoch, aber die Erweiterung wird dadurch nicht angezeigt. Sie wird erst angezeigt, nachdem die Genehmigungsanforderung übermittelt und genehmigt wurde. Wenn Sie in der Produktion bereitgestellt haben und es immer noch nicht in Fusion sehen, liegt der übliche Grund darin, dass es noch nicht genehmigt ist.
* **Nur-Code-Aktualisierungen erfordern keine neue Genehmigung.** Wenn Ihre Erweiterung bereits veröffentlicht ist und Sie nur ihren Code ändern (die Benutzeroberfläche oder die Laufzeitaktionen), stellen Sie sie erneut für dieselbe URL bereit mit:

  ```sh
  aio app deploy --force-deploy
  ```

  Benutzer erhalten die neue Version, wenn sie die Erweiterung das nächste Mal öffnen. Es gibt nichts für sie zu installieren. Sie müssen nur dann einen neuen Genehmigungsantrag einreichen, wenn Sie die **Registrierung** ändern, z. B. wenn Sie einen neuen Erweiterungspunkt hinzufügen oder ändern, was `getWidget()` annimmt.
* **Eine widerrufene oder zurückgenommene Erweiterung verschwindet.** Wenn eine Erweiterung von Ihnen widerrufen oder zurückgenommen wird, wird sie in Fusion nicht mehr ohne Fehlermeldung angezeigt. Wenn eine zuvor funktionierende Erweiterung für alle verschwindet, überprüfen Sie, ob sie widerrufen wurde, bevor Sie nach einem Code-Problem suchen.

## Entfernen (Widerrufen) einer Erweiterung

Eine veröffentlichte Erweiterung wird in Adobe Exchange durch **Widerrufen** entfernt:

1. Bei **Adobe Exchange anmelden**.
1. Navigieren Sie **Verwalten** > **App Builder Apps**.
1. Klicken **neben** Erweiterung, die Sie entfernen möchten, auf „Widerrufen“ und bestätigen Sie den Vorgang.

Nach dem Widerrufen zeigt die Erweiterung den *widerrufen* in Extension Manager an und wird nicht mehr in Fusion angezeigt. Um es vollständig zu entfernen, löschen Sie das Projekt in der Developer Console. Ein Projekt kann erst gelöscht werden, nachdem seine Erweiterung widerrufen wurde.

Bei einer reinen Staging-Testbereitstellung können Sie die Bereitstellung mit folgenden Optionen entfernen:

```sh
aio app undeploy
```

## Weitere Ressourcen

Die folgenden Ressourcen stehen in der Dokumentation zu Adobe zur Verfügung:

* [Entwicklungsablauf für UI-Erweiterungen](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [Verwaltung von UI-Erweiterungen (Veröffentlichen/Genehmigen/Sperren)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Erstellen eines Projekts in Developer Console](https://developer.adobe.com/uix/docs/guides/creating-project-in-dev-console/)
* [So erhalten Sie Zugriff (Rollen)](https://developer.adobe.com/uix/docs/guides/get-access/)
* [Lokale Vorschau von UI-Erweiterungen](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/)
