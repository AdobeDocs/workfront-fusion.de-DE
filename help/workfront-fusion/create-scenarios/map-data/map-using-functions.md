---
title: Zuordnen von Elementen mithilfe integrierter Funktionen
description: Beim Zuordnen von Elementen können Sie Funktionen verwenden, um einfache oder komplexe Formeln zu erstellen.
author: Becky
feature: Workfront Fusion
exl-id: b9d7643e-febf-42e2-9ddc-8ec8eba98e7a
source-git-commit: 8de3e365ff7ff91f4b29fb8a298f3b846de0a980
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 23%

---

# Map an item using built-in functions

Workfront Fusion enthält integrierte Funktionen, mit denen Sie einfache oder komplexe Formeln erstellen können. Diese Funktionen decken eine Vielzahl von Anwendungsfällen ab, einschließlich Funktionen für Arrays, Zeichenfolgen, Zahlen und Daten aus vorherigen Modulen.

Darüber hinaus können Sie benutzerdefinierte Funktionen erstellen, mit denen Ihre Szenarien dann Daten transformieren und bearbeiten können.

For information and instructions on custom functions, see [Map data using custom functions](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

## Zugriffsanforderungen

+++ Erweitern, um die Zugriffsanforderungen für die in diesem Artikel beschriebene Funktionalität anzuzeigen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Ein beliebiges Adobe Workfront Workflow- und Adobe Workfront Automation and Integration-Paket</p><p>Workfront Ultimate</p><p>Workfront Prime- und Select-Pakete bei zusätzlichem Kauf von Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenzen</td> 
   <td> <p>Standard</p><p>Work oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p><ul><li>Wenn Ihre Organisation über ein Workfront Select- oder Prime-Paket ohne Workfront Automation and Integration verfügt, muss Ihre Organisation Adobe Workfront Fusion erwerben.</li><li>You must have an Adobe App Builder license to use custom functions.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Details zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Map data using built-in functions

Beim Zuordnen von Elementen können Sie Funktionen verwenden, um einfache oder komplexe Formeln zu erstellen. Die verfügbaren Funktionen ähneln den Funktionen in Excel und in einigen Programmiersprachen:

* Sie werten allgemeine Logik, Mathematik, Text, Daten und Arrays aus.
* Mit ihnen können Sie bedingte Logik anwenden und Elementwerte umwandeln, z. B. einen Text in Großbuchstaben umwandeln, Text kürzen, ein Datum in ein anderes Format konvertieren und vieles mehr.

### Insert functions into fields

To insert a function into a field:

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Szenarien“ im linken Bedienfeld.
1. Wählen Sie das Szenario aus, in dem Sie Daten zuordnen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Click the field where you want to insert a function.
1. Select the tab in the mapping panel that contains the function you want to insert.

   For information on mapping panel tabs, see [Function overview](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md)
1. Click the function name.

   ODER

   Drag the function into the field.
1. Configure the function parameters.

   For an explanation of function parameters, hover over the function in the mapping panel.

   For more information on functions and their parameters, see the articles under [Function references: article index](/help/workfront-fusion/references/mapping-panel/functions/functions-toc.md).

1. Continue configuring the module, or click **OK**.

>[!TIP]
>
>When you create a complex formula that you want to reuse in another field, you can click the field that contains the combination, use Cmd-A or Ctrl-A to select it, then copy and paste it into the other field.


>[!BEGINSHADEBOX]

**Example:** Some data types prevent users from entering more than a certain number of characters. You can use the substring function to limit a value to a certain number of characters.

In diesem Beispiel beschränkt die Funktion Teilzeichenfolge den Projektnamen auf 50 Zeichen.

![Beispiel für eine Besprechungslängenbeschränkung](assets/example-meet-length-restriction-350x184.png)

>[!ENDSHADEBOX]

### Verschachteln von Funktionen

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

### [!DNL Google Sheets] verwenden

Wenn Workfront Fusion keine Funktion enthält, die Sie verwenden möchten, es jedoch in [!DNL Google Sheets] vorhanden ist, können Sie sie wie folgt verwenden:

1. Erstellen Sie [!DNL Google Sheets] eine neue leere Tabelle.
1. Öffnen Sie in Workfront Fusion Ihr Szenario.
1. Fügen Sie das **[!DNL Google Sheets]** Modul **[!UICONTROL Zelle aktualisieren]** zum Szenario hinzu.

1. Konfigurieren Sie das Modul:

   1. Wählen Sie die neu erstellte Tabelle im Feld **[!UICONTROL Tabelle]** aus.
   1. Insert your formula containing the [!DNL Google Sheets] function(s) into the **[!UICONTROL Value]** field.

      You can use the output of preceding modules as usual.

      ![Use Google Sheets functions](assets/exploit-google-sheet-functions-350x218.png)

1. Insert the **[!UICONTROL Google Sheets] >[!UICONTROL Get a cell]** module to obtain the calculated result.
1. Configure the module, using the same Cell ID that you used in step 4.

   ![Use Google Sheets functions](assets/exploit-google-sheet-functions-2-350x187.png)
