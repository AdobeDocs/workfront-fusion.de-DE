---
title: Überblick über Szenarios
description: Adobe Workfront Fusion erfordert zusätzlich zu einer Adobe Workfront-Lizenz eine Adobe Workfront Fusion-Lizenz.
author: Becky
feature: Workfront Fusion
exl-id: de81ad4c-27e5-4b6c-acf0-f01a8c85922e
source-git-commit: 34dad92019ca855f40698d3f3795788698c1cece
workflow-type: ht
source-wordcount: '704'
ht-degree: 100%

---

# Überblick über Szenarios

Adobe Workfront Fusion dient dazu, Ihre Prozesse zu automatisieren, damit Ihre Benutzenden nicht so viel Zeit mit Routineaufgaben verbringen müssen. Dies funktioniert durch die Verknüpfung von Aktionen innerhalb und zwischen Anwendungen und Services, um ein Szenario zu erstellen, in dem Ihre Daten automatisch übertragen und umgewandelt werden. Das von Ihnen erstellte Szenario ermöglicht es, auf Daten in einer Anwendung oder einem Service zu achten und diese Daten zu verarbeiten, um das gewünschte Ergebnis zu liefern.

Ein Szenario besteht aus einer Reihe von Modulen, die angeben, wie Daten innerhalb einer Anwendung umgewandelt oder zwischen Anwendungen und Webservices übertragen werden sollen.

## Überblick über Szenario-Elemente

Ein Szenario besteht aus verschiedenen Elementen. Wenn Sie die Terminologie der folgenden Elemente verstehen, können Sie die Dokumentation einfacher und besser nutzen:

* [Szenario](#scenario)
* [Auslöser](#trigger)
* [Modul](#module)
* [Route](#route)
* [Szenario-Segment](#scenario-segment)
* [Connector](#connector)

### Szenario

Ein **Szenario** ist eine benutzerseitig erstellte Reihe automatisierter Schritte, mit denen Daten verschoben und bearbeitet werden. Der Begriff „Szenario“ bezieht sich auf die gesamte Gruppe verbundener Schritte.

![Szenario](assets/entire-scenario-scenario.png)

### Auslöser

Ein Szenario beginnt mit einem **Auslöser**. Der Auslöser achtet auf neue und aktualisierte Daten und startet das Szenario, wenn bestimmte im Modul konfigurierte Bedingungen zutreffen. Auslöser können so konfiguriert werden, dass ein Szenario nach einem Zeitplan (auf Abruf) oder bei jeder Datenänderung (sofort) gestartet wird.

![Auslöser](assets/scenario-trigger.png)

### Modul

Auf den Auslöser folgt eine Reihe von **Modulen**. Ein Modul stellt einen einzelnen Schritt in einem Szenario dar, durch das eine bestimmte Aktion ausgeführt wird. Module werden konfiguriert und miteinander verkettet, um Szenarios zu erstellen.

![Module](assets/scenario-module.png)

### Route

Ein Szenario kann in **Routen** unterteilt werden. Eine Route ist ein Abschnitt des Szenarios, der für ein bestimmtes Datenpaket verwendet werden kann. Routen werden mithilfe eines Router-Moduls und verschiedener Filter eingerichtet.

![Route](assets/scenario-route.png)

### Szenario-Segment

Ein Szenario-Segment ist ein Abschnitt eines Szenarios, der aus einer Reihe zusammenhängender Module besteht, die alle mit derselben Anwendung verbunden sind. Szenario-Segmente stellen oft einen kurzen Workflow in der Anwendung dar.

![Szenario-Segment](assets/scenario-segment.png)

### Connector

Ein Connector ist ein Satz von Modulen für eine bestimmte Anwendung. Workfront Fusion bietet Connectoren für viele gängige Arbeitsanwendungen wie Workfront, Salesforce und Jira sowie generische Connectoren, die für jeden Webservice verwendet werden können.

![Connectoren](assets/scenario-connectors.png)

## Beispiele

Erweitern Sie die folgenden Abschnitte, um Beispielszenarios und zugehörige Erläuterungen anzuzeigen.

+++**Automatisieren von Prozessen in Adobe Workfront**

Workfront Fusion ermöglicht die Automatisierung einfacher oder komplexer Workflows in Workfront, was Zeit spart und eine konsistente Prozessausführung sicherstellt.

In diesem Beispiel wird das Szenario ausgelöst, wenn sich ein bestimmtes Feld in einer Aufgabe oder einem Problem in Workfront ändert. Nach der Auslösung ruft das Szenario Informationen im zugehörigen Projekt ab und erstellt eine maßgeschneiderte Aktualisierung für eine Person, die einer bestimmten Rolle im Projekt zugewiesen wurde.

![Vorlagenbeispiel](assets/fusion-template-example.png)

+++

+++**Verbinden von Workfront mit einer anderen Anwendung oder einem anderen Webservice**

>[!NOTE]
>
>Wenn Ihre Organisation das alte Lizenzierungsmodell verwendet, benötigt sie eine Workfront Fusion for Work Automation and Integration-Lizenz, um eine Verbindung zu anderen Anwendungen herzustellen.

Workfront Fusion kann eine Verbindung zu anderen Anwendungen und Webservices herstellen. Sie können auf Daten aus anderen Anwendungen zugreifen, diese importieren, bearbeiten oder exportieren und auf diese Weise mit Workfront oder miteinander integrieren.

Viele Anwendungen verfügen über dedizierte Workfront Fusion-Connectoren. Wenn für die Anwendung, auf die Sie zugreifen möchten, kein dedizierter Connector vorhanden ist, können Sie die HTTP- oder SOAP-Module von Workfront Fusion verwenden, um über die zugehörige API eine Verbindung zur Anwendung herzustellen.

In diesem Beispiel wird das Szenario ausgelöst, wenn eine Person zu einer [!DNL Excel]-Tabelle hinzugefügt wird. Im Rahmen des Szenarios wird geprüft, ob es sich um eine Workfront-Benutzerin bzw. einen Workfront-Benutzer handelt. Falls nicht, wird das Benutzerprofil in Workfront erstellt und die zugehörige Workfront-Benutzer-ID wird wieder in die Tabelle eingefügt.

![Integrationsbeispiel](assets/fusion-integration-example.png)

Eine Liste der dedizierten Connectoren finden Sie unter [Fusion-Anwendungen und ihre Modulverweise: Artikelindex](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).


>[!IMPORTANT]
>
>Adobe Workfront Fusion kann eine Verbindung zu fast jedem Webservice herstellen. Wenn die Anwendung, mit der Sie arbeiten möchten, über keinen dedizierten Workfront Fusion-Connector verfügt, können Sie universelle Connectoren verwenden, um eine Verbindung zur Anwendung oder zum Service herzustellen.
>
>Eine Liste der universellen Connectoren finden Sie unter [Universelle Connectoren](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)

+++

## Referenzen

* Ein Glossar der in Workfront Fusion verwendeten Begriffe finden Sie im [Adobe Workfront Fusion-Glossar](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md).
* Informationen zum Erstellen eines Übungsszenarios finden Sie unter [Erstellen eines Basisszenarios](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).
* Informationen zum Erstellen und Verwalten von Szenarios finden Sie in den Artikeln, die unter den folgenden Themen aufgeführt sind:
   * [Erstellen von Szenarios](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)
   * [Verwalten von Szenarios](/help/workfront-fusion/manage-scenarios/manage-scenarios-toc.md)
