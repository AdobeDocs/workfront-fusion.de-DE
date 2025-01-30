---
title: Zuordnen von Elementen mithilfe von Funktionen
description: Beim Zuordnen von Elementen können Sie Funktionen verwenden, um einfache oder komplexe Formeln zu erstellen.
author: Becky
feature: Workfront Fusion
exl-id: b9d7643e-febf-42e2-9ddc-8ec8eba98e7a
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Zuordnen eines Elements mithilfe von Funktionen

Beim Zuordnen von Elementen können Sie Funktionen verwenden, um einfache oder komplexe Formeln zu erstellen. Die verfügbaren Funktionen ähneln den Funktionen in Excel und in einigen Programmiersprachen:

* Sie bewerten allgemeine Logik, Mathematik, Text, Daten und Arrays.
* Mit ihnen können Sie bedingte Logik und Umwandlungen von Elementwerten durchführen, z. B. einen Text in Großbuchstaben umwandeln, Text kürzen, ein Datum in ein anderes Format konvertieren und vieles mehr.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Konfigurationen der Zugriffsebene*</td> 
   <td> 
     <p>Sie müssen ein [!DNL Workfront Fusion]-Administrator für Ihre Organisation sein.</p>
     <p>Sie müssen [!DNL Workfront Fusion] für Ihr Team sein.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Funktionen in Felder einfügen

So fügen Sie eine Funktion in ein Feld ein:

1. Klicken Sie im linken Bedienfeld auf die Registerkarte **[!UICONTROL Scenarios]** .
1. Wählen Sie das Szenario aus, in dem Sie Daten zuordnen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf das Feld, in das Sie eine Funktion einfügen möchten.
1. Wählen Sie die Registerkarte im Bedienfeld Zuordnung aus, die die Funktion enthält, die Sie einfügen möchten.

   Informationen zu Registerkarten des Zuordnungsbereichs finden Sie unter [Funktionsübersicht](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md)
   1. Klicken Sie auf den Funktionsnamen.

      Oder

      Ziehen Sie die Funktion in das Feld.
1. Konfigurieren Sie die Funktionsparameter.

   Um eine Erklärung der Funktionsparameter zu erhalten, bewegen Sie den Mauszeiger über die Funktion im Zuordnungsbereich.

   Weitere Informationen zu Funktionen und ihren Parametern finden Sie in den Artikeln unter [Funktionsverweise: Artikelindex](/help/workfront-fusion/references/mapping-panel/functions/functions-toc.md).

1. Fahren Sie mit der Konfiguration des Moduls fort oder klicken Sie auf **OK**.

>[!TIP]
>
>Wenn Sie eine komplexe Formel erstellen, die Sie in einem anderen Feld wiederverwenden möchten, können Sie auf das Feld klicken, das die Kombination enthält, sie mit Befehlstaste A oder Strg-A auswählen und sie dann kopieren und in das andere Feld einfügen.


>[!BEGINSHADEBOX]

**Beispiel:** Einige Datentypen verhindern, dass Benutzer mehr als eine bestimmte Anzahl von Zeichen eingeben. Sie können die Funktion Teilzeichenfolge verwenden, um einen Wert auf eine bestimmte Anzahl von Zeichen zu beschränken.

In diesem Beispiel beschränkt die Funktion Teilzeichenfolge den Projektnamen auf 50 Zeichen.

![Beispiel für eine Besprechungslängenbeschränkung](assets/example-meet-length-restriction-350x184.png)

>[!ENDSHADEBOX]

## Verschachteln von Funktionen

Sie können Funktionen ineinander verschachteln.

>[!BEGINSHADEBOX]

**Beispiel:**

In diesem Beispiel beschränkt die Funktion Teilzeichenfolge den gekürzten Projektnamen auf 50 Zeichen.

![Zugeschnittener Name](assets/trimmed-name-under-50.png)

>[!ENDSHADEBOX]

So verschachteln Sie eine Funktion:

1. Klicken Sie auf das Feld, in dem Sie eine Formel erstellen.

   Dadurch wird das Zuordnungsfeld geöffnet.

1. Klicken Sie auf die erste Funktion, die Sie hinzufügen möchten. Das ist die Funktion von außen. Im folgenden Beispiel ist dies die `substring`.
1. Klicken Sie in dieser Funktion auf die Stelle, an der die verschachtelte Funktion angezeigt werden soll. In diesem Beispiel tritt die verschachtelte Funktion an die Stelle des ersten Parameters.
1. Klicken Sie im Zuordnungsbereich auf die verschachtelte Funktion. In diesem Beispiel ist dies die `trim`.
1. Fahren Sie mit der Konfiguration der Funktion wie gewünscht fort.
1. Fahren Sie mit der Konfiguration des Moduls fort oder klicken Sie auf **OK**.

## [!DNL Google Sheets] verwenden

Wenn [!DNL Workfront Fusion] keine Funktion enthält, die Sie verwenden möchten, es aber von [!DNL Google Sheets] vorgestellt wird, können Sie sie wie folgt verwenden:

1. Erstellen Sie [!DNL Google Sheets] eine neue leere Tabelle.
1. Öffnen Sie [!DNL Workfront Fusion] Ihr Szenario.
1. Fügen Sie das Modul **[!DNL Google Sheets]** > **[!UICONTROL Update a cell]** zum Szenario hinzu.

1. Konfigurieren Sie das Modul:

   1. Wählen Sie die neu erstellte Tabelle im Feld **[!UICONTROL Spreadsheet]** aus.
   1. Fügen Sie die Formel, die die [!DNL Google Sheets] enthält, in das Feld **[!UICONTROL Value]** ein.

      Sie können die Ausgabe vorhergehender Module wie gewohnt verwenden.

      ![Verwenden von Google Sheets-Funktionen](assets/exploit-google-sheet-functions-350x218.png)

1. Fügen Sie das Modul **[!UICONTROL Google Sheets]>[!UICONTROL Get a cell]** ein, um das berechnete Ergebnis zu erhalten.
1. Konfigurieren Sie das Modul mit derselben Zellen-ID, die Sie in Schritt 4 verwendet haben.

   ![Verwenden von Google Sheets-Funktionen](assets/exploit-google-sheet-functions-2-350x187.png)
