---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Verwenden einer Funktion zum Aktualisieren eines Projekts in einem einfachen Szenario
description: Erfahren Sie, wie Sie eine Funktion hinzufügen, um ein Arbeitselement in Workfront zu aktualisieren.
author: Becky
feature: Workfront Fusion
exl-id: aa082ac8-48e8-4569-880e-024dd77feaa1
source-git-commit: 8884aef2237ad358c774110b81ac17b9efb386d4
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 1%

---

# Verwenden einer Funktion zum Aktualisieren eines Projekts in einem einfachen Szenario

Das Aktualisieren eines Workfront-Arbeitselements ist ein gängiges Anwendungsbeispiel für Workfront Fusion. In diesem Beispiel verwenden Sie eine Funktion, um den Namen eines Projekts so zu ändern, dass er in Großbuchstaben geschrieben wird.

Fusion enthält viele Arten von Funktionen, mit denen Sie bedingte Logik für Ihre Daten transformieren und ausführen können. Weitere Informationen zur Verwendung von Funktionen finden Sie unter [Funktionsübersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md).

Dieses Beispiel ändert das in erstellte Szenario [Erstellen eines einfachen Szenarios](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Packstück</td> 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] Lizenz</td> 
   <td> <p>Neu: [!UICONTROL Standard]</p><p>Oder</p><p>Aktuell: [!UICONTROL Work] oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] Lizenz **</td> 
   <td>
   <p>Aktuell: Keine [!DNL Workfront Fusion].</p>
   <p>Oder</p>
   <p>Legacy: Beliebig </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>[!UICONTROL Select] oder [!UICONTROL Prime] [!DNL Workfront]: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan: [!DNL Workfront Fusion] ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss [!DNL Adobe Workfront Fusion] erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

Sie müssen das unter &quot;[ eines einfachen Szenarios“ beschriebene Szenario erstellen](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) bevor Sie dieses Verfahren ausführen.

## Verwenden einer Funktion zum Aktualisieren eines Projekts

### Hinzufügen des Moduls Eintrag aktualisieren zu Ihrem Szenario

1. Öffnen Sie das Szenario im Szenario-Editor.
1. Bewegen Sie den Mauszeiger über den Teilkreis rechts neben dem des zweiten Moduls und klicken Sie dann auf **[!UICONTROL Add another module]**.
1. Wählen Sie [!DNL Adobe Workfront] aus der Liste der Programme und dann die **[!UICONTROL Update Record]** aus.
1. Wählen Sie im Feld ID den ID-Block aus, der sich unter dem Modul Objekt konvertieren befindet. Dies ist die ID des Projekts, das von diesem Modul ausgegeben wurde.

   ![ID aus dem Konvertierungsobjekt](assets/id-convert-object.png)

1. Wählen Sie im Feld Datensatztyp die Option Projekt aus, da das zu aktualisierende Objekt ein Projekt ist.
1. Klicken Sie im Bereich Zuzuordnende Felder auswählen auf Name.

   Ein Namensfeld wird geöffnet.
1. Fahren Sie fort [Zuordnen der Funktion für die Namensaktualisierung](#map-the-function-for-the-name-update).

### Zuordnen der Funktion für die Namensaktualisierung

Wenn dieses Szenario eine Anfrage in ein Projekt konvertiert, ist der Projektname mit der Anfrage identisch. Die Funktion übernimmt hier diesen Namen und schreibt alle Buchstaben groß.

1. Klicken Sie auf das **Name**.

   Das Zuordnungsbedienfeld wird geöffnet.
1. Klicken Sie im Zuordnungsbereich auf das Symbol **Text und binäre Funktionen** . ![Symbol für Textfunktionen](assets/toolbar-icon-text&binary-functions.png)
1. Wählen Sie die Funktion **upper**.

   Die Funktion wird im Feld Name angezeigt, einschließlich der Formatierung für die erwartete Eingabe.

   Die Eingabe für dieses Beispiel ist der Name des Problems, aus dem das Projekt konvertiert wurde.

1. Bewegen Sie den Cursor zwischen den Klammern, denn hier wird die Eingabe eingefügt.
1. Klicken Sie im Zuordnungsbereich auf das Symbol **Modulausgabe** . ![Modul-Ausgabesymbol](assets/toolbar-icon-functions-you-map-from-other-modules.png)
1. Wählen Sie den Namensblock aus, der von Ihrem ersten Modul ausgegeben wurde.

   Der Block Name wird in der Funktion angezeigt.

   ![Namensblock in der Funktion](assets/map-name.png)

1. Klicken Sie **OK**, um die Moduleinstellungen zu speichern.

### Testen und Aktivieren

1. Testen Sie das Szenario, indem **Einmal ausführen** in der linken unteren Ecke des Bildschirms klicken.
1. Überprüfen Sie die Ausgabe, um sicherzustellen, dass das Szenario erwartungsgemäß ausgeführt wurde.
1. Wenn Sie sich vergewissert haben, dass das Szenario erwartungsgemäß funktioniert, klicken Sie auf **Umschalter** Planung“ unten links im Bildschirm auf **Ein**.

   Dadurch wird das Szenario aktiviert. Aktive Szenarien werden nach dem im Trigger-Modul festgelegten Zeitplan ausgeführt.
1. Klicken Sie [!DNL Workfront Fusion] unten links auf **[!UICONTROL Save]** , um den Fortschritt des Szenarios zu speichern.

   >[!IMPORTANT]
   >
   >Speichern Sie häufig, während Sie ein Szenario verfeinern und testen.

## Ressourcen

* [Zuordnen von Elementen mithilfe von Funktionen](/help//workfront-fusion/create-scenarios/map-data/map-using-functions.md)
