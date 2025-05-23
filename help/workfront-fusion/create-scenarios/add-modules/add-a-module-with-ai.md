---
title: Erstellen eines Szenariosegments mit KI
description: Sie können KI verwenden, um eine Textaufforderung einzugeben, die beschreibt, was Sie für ein Segment Ihres Szenarios tun müssen. Fusion generiert dann ein oder mehrere Module, die diese Aktionen ausführen. Diese Module können Sie dann in Ihrem Szenario verwenden.
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
source-git-commit: 9d29abc82a3bb09affc4d17d7ea214d7bb850294
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 1%

---

# Erstellen eines Szenariosegments mit KI

<!--DO NOT DELETE - linked through CSH-->

<!--Check if this is in GA before repo goes live. If not, hide this article.-->

<!--Check if they need to have signed the rider and stuff-->

Sie können KI verwenden, um eine Textaufforderung einzugeben, die beschreibt, was Sie für ein Segment Ihres Szenarios tun müssen. Fusion generiert dann ein oder mehrere Module, die diese Aktionen ausführen. Diese Module können Sie dann in Ihrem Szenario verwenden.

Generierte Szenariosegmente enthalten Module für einen einzelnen Connector. Um Module für einen anderen Connector zu generieren, erstellen Sie eine separate Eingabeaufforderung und fügen Sie dann die Szenario-Segmente in Ihr Szenario ein.

Wie bei allen aus KI generierten Modulen empfehlen wir, die generierten Module zweimal zu überprüfen und zu testen, um sicherzustellen, dass sie die beabsichtigte Leistung erbringen.

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

Ihr Unternehmen muss die folgenden Voraussetzungen erfüllen, um diese Funktion nutzen zu können:

* Ihr Unternehmen muss am Workfront AI Assistant Beta-Programm teilgenommen haben.
* Adobe muss eine unterzeichnete Adobe Gen AI-Vereinbarung für Ihr Unternehmen haben.

  Weitere Informationen zum Unterzeichnen der Vereinbarung finden Sie unter [Unterschreiben der Adobe Gen AI-](https://experienceleague.adobe.com/de/docs/workfront/using/basics/ai-assistant/ai-assistant-overview#sign-the-adobe-gen-ai-agreement)) im Artikel KI-Assistent - Übersicht in der Dokumentation zu Workfront.

## Derzeit unterstützte KI-Modulanwendungen

Die Fusion-KI kann derzeit Module generieren, die eine Verbindung zu den folgenden Anwendungen herstellen:

* Adobe Firefly
* Azure OpenAI
* Microsoft-Diagramm
* Adobe Workfront-Planung
* Adobe Analytics
* Adobe PDF Services
* Adobe Marketo
* Adobe Frame.io
* Dropbox
* NetSuite
* Google-Kalendar
* Atlassischer Jira
* GitLab
* Spotify
* Bitbucket
* OpenAI
* Slack

## Module generieren

1. Klicken Sie im linken Bedienfeld auf die Registerkarte **[!UICONTROL Scenarios]** .
1. Wählen Sie das Szenario aus, in dem Sie ein Modul hinzufügen möchten.
1. Klicken Sie auf eine beliebige Stelle im Szenario, um den Szenario-Editor aufzurufen.
1. Klicken Sie auf **KI** Assistent![ Symbol KI-Assistent](assets/ai-assistant-icon.png) in der oberen rechten Ecke des Bildschirms.
1. Geben Sie im Bedienfeld „KI-Assistent“ eine Textaufforderung ein.

   Tipps zu Eingabeaufforderungen finden Sie unter [Tipps zum Erstellen von Eingabeaufforderungen für Szenariosegmente](#tips-for-creating-prompts-for-scenario-segments) in diesem Artikel.

   Der KI-Assistent generiert das Modul oder den Satz von Modulen.
1. (Bedingt) Fügen Sie bei Bedarf Ihr API-Token für die Anwendung in die Module ein.
1. Überprüfen Sie die Module, um sicherzustellen, dass sie für das entsprechende Programm und die entsprechende Aktion konfiguriert sind.
1. (Bedingt) Wenn der Abschnitt Erzeugtes Szenario nicht mit Ihrem Szenario verbunden ist, ziehen Sie ihn an die gewünschte Position.

Es wird empfohlen, die Module zu testen, um sicherzustellen, dass sie die beabsichtigte Leistung erzielen.

## Tipps zum Erstellen von Eingabeaufforderungen für Szenario-Segmente

Textaufforderungen sollten mindestens die folgenden Informationen enthalten:

* Die Anwendung, mit der Sie eine Verbindung herstellen
* Die Aktion(en), die Sie ausführen möchten

>[!IMPORTANT]
>
>Sie können mehr als ein Modul gleichzeitig generieren, können aber nur Module für jeweils ein Programm generieren.

>[!BEGINSHADEBOX]

**Beispiele**:

* `Delete the records 'xyz-123', 'xyz-456', 'xyz-789' from Adobe Workfront Planning`
Dazu gehören die `Workfront Planning` und die `delete records`. Bei dieser Eingabeaufforderung werden drei Module erstellt, eines für jeden zu löschenden Datensatz.
* `Change campaign summary of the record 'xyz-123' from Adobe Workfront Planning`
Dazu gehören die `Workfront Planning` und die `change campaign summary`.
* `Get all field details in the record type with ID 'test-record' from Adobe Workfront Planning`
Dazu gehören die `Workfront Planning` und die `get field details`.

Das folgende Beispiel ist NICHT korrekt:

* `Generate an image in Adobe Firefly and upload it to Dropbox`

  Dieses Beispiel ist falsch, da es mehr als ein Programm enthält

>[!ENDSHADEBOX]

Beachten Sie beim Erstellen von Textaufforderungen Folgendes:

* Verwenden Sie eine direkte, einfache Sprache.
* Überprüfen und testen Sie Ihr Szenario-Segment. Wenn die Eingabeaufforderung nicht die erwartete Leistung zeigt, verfeinern Sie sie und versuchen Sie es erneut.
