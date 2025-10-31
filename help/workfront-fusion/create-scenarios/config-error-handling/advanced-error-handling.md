---
title: Hinzufügen von Filterung und Verschachtelung zu Fehlerbehandlungsrouten
description: Sie können Ihrer Fehlerbehandlungsroute erweiterte Techniken zur Fehlerbehandlung hinzufügen, indem Sie Filterung und Verschachtelung einschließen.
author: Becky
feature: Workfront Fusion
exl-id: 745bfdc4-1327-4a28-a863-c217f15a7fc5
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%

---

# Hinzufügen von Filterung und Verschachtelung zu Fehlerbehandlungsrouten

Sie können Ihrer Fehlerbehandlungsroute erweiterte Techniken zur Fehlerbehandlung hinzufügen, indem Sie Filterung und Verschachtelung einschließen.

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Jedes Adobe Workfront-Workflow-Paket und jedes Adobe Workfront-Automatisierungs- und Integrationspaket</p><p>Workfront Ultimate</p><p>Workfront Prime und Select-Pakete, mit einem zusätzlichen Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Wenn Ihr Unternehmen über ein Select- oder Prime Workfront-Paket verfügt, das keine Workfront-Automatisierung und -Integration enthält, muss Ihr Unternehmen Adobe Workfront Fusion erwerben.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Filterung

Es gibt zwei Arten der Filterung, die bei einer Fehler-Handler-Route erfolgen kann.

* [Hinzufügen eines Filters zur Fehler-Handler-Route](#add-a-filter-to-the-error-handler-route)
* [Fügen Sie der Fehler-Handler-Route einen Router und anschließend Filter hinzu](#add-a-router-followed-by-filters-to-the-error-handler)

### Hinzufügen eines Filters zur Fehler-Handler-Route

Sie können einen Filter verwenden, um zu steuern, welche Fehler von der Fehler-Handler-Route verarbeitet werden. Auf diese Weise können Sie nur bestimmte Fehlertypen verarbeiten. Wenn ein Fehler nicht durch den Filter geleitet wird, wird dies so behandelt, als ob für das angegebene Modul keine Fehler-Handler-Route definiert ist.

Diese Filter sind wie alle anderen Filter in Fusion konfiguriert. Anweisungen finden Sie unter [Hinzufügen eines Filters zu einem Szenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).

### Fügen Sie dem Fehler-Handler einen Router und anschließend Filter hinzu

Durch das Hinzufügen eines Routers zu einer Fehlerbehandlungsroute können Sie verschiedene Routen für verschiedene Fehlertypen konfigurieren.

Um beispielsweise eine Route zu konfigurieren, die ausgeführt werden soll, wenn der Fehler ein DataError ist, können Sie einen Filter einrichten, der den Durchlauf der Daten ermöglicht, wenn der zugeordnete Fehlertyp DataError entspricht.

![DataError-Filter](assets/filter-dataerror.png)

Informationen dazu, wie Fusion verschiedene Datentypen auswertet und verarbeitet, finden Sie unter [Fehlertypen](/help/workfront-fusion/references/errors/error-processing.md).

### Beispiel: Fehlerbehandlung mit Filtern

>[!BEGINSHADEBOX]

Dieses Beispielszenario zeigt, wie diese Filter bei der Fehlerbehandlung funktionieren.

Wenn Sie Dropbox > Ordnermodul erstellen verwenden und bereits ein Ordner mit demselben Namen vorhanden ist, gibt das Modul einen DataError aus:

![Fehler in Dropbox](assets/dropbox.png)

Das vollständige Szenario funktioniert wie folgt:

![Dropbox-Szenario](assets/dropbox-scenario.png)

1. Das Modul Werkzeuge > Variable festlegen enthält den Ordnernamen
1. Das Modul HTTP > Datei abrufen ruft die Datei ab, die in den Ordner hochgeladen werden muss
1. Das Modul Dropbox > Ordner erstellen gibt einen Fehler aus, wenn bereits ein Ordner mit demselben Namen wie der im Modul zugeordnete vorhanden ist
1. Die Route des Fehler-Handlers (transparente Blasen) enthält einen Router zum Filtern der Fehler
Die erste Route ist für einen bestimmten Fehlertyp mit der Bezeichnung `DataError`.

   1. Wenn ein `DataError` stattfindet und die Fehlerdetails den Filter durchlaufen, listet Dropbox unter Alle Dateien/Unterordner in einem Ordnermodul alle Ordner in Dropbox auf.
   1. Der nachfolgende Filter entspricht den Ordnernamen.
   1. Die **resume**-Direktive gibt die Ordner-ID und den Ordnerpfad des bestehenden Ordners an, und die Ausführung des Szenarios wird über Dropbox > Ordnermodul erstellen fortgesetzt. Anstatt jedoch einen neuen Ordner zu erstellen, verwendet Fusion die Werte aus der Fortsetzungsanweisung, um zum nächsten Modul zu wechseln und die Datei in den vorhandenen Ordner hochzuladen.

1. Die zweite Route ist für alle anderen Fehler und endet mit der Rollback-Direktive, was dazu führt, dass das Szenario sofort gestoppt wird

Nachfolgend finden Sie eine detaillierte Erklärung der Datenfehler-Route.

Um den vorhandenen Ordner in Ihren nachfolgenden Modulen zu verwenden, z. B. zum Hochladen einer Datei, müssen Sie eine Fehler-Handler-Route zum -Modul hinzufügen und den Ordnerpfad abrufen, der dem folgenden Fortsetzungsanweisungsmodul zugeordnet werden soll:

![Fehler-Handler-Route hinzufügen](assets/add-error-handler-route.png)

Der Filter für die erste Route ist so eingestellt, dass nur der bestimmte Fehler (DataError) verarbeitet wird, der angezeigt wird, wenn bereits ein Ordner mit demselben Namen vorhanden ist:

![Bedingung](assets/condition.png)

Dropbox > Alle Dateien in einem Ordnermodul auflisten ist so konfiguriert, dass alle Ordner im Zielordner zurückgegeben werden. Der folgende Filter übergibt nur den Filter, den wir ursprünglich erstellen wollten. (Der Ordnername wird unter 33 gespeichert. Element „Ordnername“.)

![Bedingung](assets/condition2.png)

Die Fortsetzungsanweisung liefert dann den Ordnerpfad als Ausgabe für das fehlgeschlagene Modul. Beachten Sie, dass die Ordner-ID leer gelassen wurde, da sie vom Modul Hochladen einer Datei nicht benötigt wird.

![Flusskontrolle](assets/flow-control.png)

>[!ENDSHADEBOX]

## Verschachtelung

Fehlerhandler-Routen können für alle Module mit Ausnahme von Routern erstellt und konfiguriert werden. Daher können Sie eine Fehler-Handler-Route für ein Modul erstellen, das bereits Teil einer vorhandenen Fehler-Handler-Route ist.

>[!BEGINSHADEBOX]

Beispiel:

Eine verschachtelte Fehler-Handler-Route mit Filtern:

![Verschachtelte Route zur Fehlerbehandlung](assets/nested-error-handling-route.png)

In diesem Szenario wird die zweite Fehler-Handler-Route unter der ersten Fehler-Handler-Route verschachtelt.

Wenn beim Modul Dropbox > Ordner erstellen ein Fehler auftritt, wird die Ausführung auf die erste Route verschoben. Wenn der `DataError Takes Place` übergeben wird, wird das nächste Modul ausgeführt, gefolgt vom Fortsetzungsanweisungsmodul, wenn in Dropbox kein Fehler auftritt > Alle Dateien/Unterordner in einem Ordnermodul auflisten.

Wenn jedoch in Dropbox unter Alle Dateien/Unterordner in einem Ordnermodul auflisten ein Fehler auftritt, wechselt die Ausführung zu Fehler-Handler-Route 2 und endet mit der [!UICONTROL Ignore]-Anweisung. Das [!UICONTROL Resume-Direktive]-Modul wird in diesem Fall nicht ausgeführt.

>[!ENDSHADEBOX]
