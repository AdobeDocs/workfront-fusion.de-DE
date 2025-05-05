---
title: Adobe Experience Manager Assets-Module
description: Mit dem  [!DNL Adobe Experience Manager Assets] -Connector für [!DNL Adobe Workfront Fusion] können Sie Assets erstellen, hochladen und aktualisieren sowie Ordner und Assets kopieren oder verschieben.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1727'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager Assets]

Mit dem [!DNL Adobe Experience Manager Assets]-Connector für [!DNL Adobe Workfront Fusion] können Sie Assets erstellen, hochladen und aktualisieren sowie Ordner und Assets kopieren oder verschieben.

Eine Videoeinführung zum Adobe Experience Manager Assets-Connector finden Sie unter:

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

## Zugriffsanforderungen

+++ Erweitern Sie , um die Zugriffsanforderungen für die -Funktion in diesem Artikel anzuzeigen.

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Paket</td> 
   <td> <p>Beliebig</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz</td> 
   <td> <p>Neu: Standard</p><p>Oder</p><p>Aktuell: Arbeit oder höher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuell: Keine Workfront Fusion-Lizenzanforderung</p>
   <p>Oder</p>
   <p>Legacy: Workfront Fusion für Automatisierung und Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Neu:</p> <ul><li>Prime oder Workfront auswählen: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</li><li>Ultimate Workfront-Paket: Workfront Fusion ist enthalten.</li></ul>
   <p>Oder</p>
   <p>Aktuell: Ihr Unternehmen muss Adobe Workfront Fusion erwerben.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Weitere Informationen zu den Informationen in dieser Tabelle finden Sie unter [Zugriffsanforderungen in der Dokumentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Informationen zu [!DNL Adobe Workfront Fusion] finden Sie unter [[!DNL Adobe Workfront Fusion] Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voraussetzungen

* Sie müssen über ein [!DNL Adobe Experience Manager Assets]-Konto verfügen, um diese Module verwenden zu können.
* Sie müssen [!UICONTROL Server-zu-Server]-Fluss im [!DNL Adobe Developer console] einrichten.

  Anweisungen zum Einrichten des [!UICONTROL Server-zu-Server]-Flusses im [!DNL Adobe Developer console] finden Sie unter [Generieren von Zugriffstoken für Server-seitige APIs](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow).
* Ihr technisches Adobe Experience Manager-Konto muss über Schreibberechtigungen verfügen.

  Anweisungen zum Hinzufügen von Schreibberechtigungen für Ihr technisches Adobe Experience Manager-Konto finden Sie unter [Service-Anmeldeinformationen](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) in der Dokumentation zu Adobe Experience Manager.

## Adobe Experience Manager Assets-API-Informationen

Der Adobe Experience Manager Assets-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Adobe Experience Manager Assets] mit [!DNL Workfront Fusion] verbinden {#connect-adobe-experience-manager-assets-to-workfront-fusion}

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe Experience Manager Assets]:

1. Klicken Sie [!UICONTROL Hinzufügen] neben dem Feld [!UICONTROL Verbindung].

2. Wählen Sie den Verbindungstyp aus, den Sie erstellen:

   * **[!DNL AEM Assets as a Cloud Service]**

     Diese Konfiguration erfordert Informationen vom [!DNL Adobe Admin Console].

   * **[!DNL AEM Assets Basic] ([!DNL Adobe Managed Services])**

     Diese Konfiguration erfordert einen Benutzernamen und ein Kennwort.

3. Füllen Sie die Felder für den Verbindungstyp aus, den Sie erstellen.

   [!DNL AEM Assets as a Cloud Service] finden Sie unter [Konfigurieren der Verbindung für [!DNL AEM Assets as a Cloud Service]](#configure-the-connection-for-aem-assets-as-a-cloud-service).

   Informationen zu [!UICONTROL AEM Assets Basic] ([!DNL Adobe Managed Services]) finden Sie unter [Konfigurieren der Verbindung für [!UICONTROL AEM Assets Basic]](#configure-the-connection-for-aemassets-basic-adobe-managed-services).

4. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.


### Konfigurieren der Verbindung für [!DNL AEM Assets as a Cloud Service]

>[!NOTE]
>
>* Die Informationen für diese Felder werden im Rahmen der Einrichtung eines [!UICONTROL Server-zu-Server]-Flusses auf dem [!DNL Adobe Developer Console] generiert. Diese Werte finden Sie in der JSON-Datei mit den Service-Anmeldeinformationen, die im Rahmen dieses Setups generiert wurde.
>
>   Anweisungen zum Einrichten des [!UICONTROL Server-zu-Server]-Flusses auf der [!UICONTROL Adobe Developer Console] finden Sie unter [Generieren von Zugriffstoken für Server-seitige APIs](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow).
>
>* Ihr technisches Adobe Experience Manager-Konto muss über Schreibberechtigungen verfügen.
>
>   Anweisungen zum Hinzufügen von Schreibberechtigungen für Ihr technisches Adobe Experience Manager-Konto finden Sie unter [Service-Anmeldeinformationen](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) in der Dokumentation zu Adobe Experience Manager.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">[!UICONTROL Verbindungsname]</td>
                  <td>
                      <p>Einen Namen für diese Verbindung eingeben</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL -Instanz-URL ohne Schrägstrich]</td>
                  <td>Geben Sie die URL für Ihre [!DNL Adobe Experience Manager] ein. Geben Sie am Ende der URL keinen Schrägstrich <code>/</code>.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Kontodetails-Fülloptionen]</td>
                  <td>Wählen Sie aus, ob Sie eine JSON zur Beschreibung Ihrer Kontodetails bereitstellen oder Details manuell eingeben möchten.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Technische Kontodetails im JSON-Format]</td>
                  <td>Wenn Sie JSON bereitstellen, geben Sie die JSON-Datei ein, die Ihre Kontodetails beschreibt, oder fügen Sie sie ein.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Client-ID]</td>
                  <td>Wenn Sie Details manuell eingeben, geben Sie die Client-ID ein, die bei der Einrichtung von [!UICONTROL Server-zu-Server] generiert wurde.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
                  <td>Wenn Sie Details manuell eingeben, geben Sie den im Setup [!UICONTROL Server-to-Server] generierten geheimen Clientschlüssel ein.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL ID des technischen Kontos]</td>
                  <td>Wenn Sie Details manuell eingeben, geben Sie die ID des technischen Kontos ein. Dies ist das Feld "[!UICONTROL id]" in der JSON-Datei mit den Client-Anmeldeinformationen.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Org ID]</td>
                  <td class="">Wenn Sie Details manuell eingeben, geben Sie die ID Ihrer Organisation ein. Dies ist das Feld "[!UICONTROL org]" in der JSON-Datei mit den Client-Anmeldeinformationen.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Meta Scopes]</td>
                  <td>Geben Sie die Meta-Bereiche ein, die im Setup von [!UICONTROL Server-zu-Server] generiert wurden.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Privater Schlüssel]</td>
                  <td>Geben Sie den privaten Schlüssel ein, der bei der [!UICONTROL Server-to-Server]-Einrichtung generiert wurde. Um den privaten Schlüssel zu extrahieren, klicken Sie auf [!UICONTROL Extract], geben Sie dann die zu extrahierende Datei und das Kennwort für die Datei ein.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL -Authentifizierungs-URL]</td>
                  <td>Authentifizierungs-URL für dieses Konto eingeben.</td>
              </tr>
          </tbody>
      </table>


### Konfigurieren der Verbindung für AEM Assets Basic (Adobe Managed Services)

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">[!UICONTROL Verbindungsname]</td>
                <td>
                    <p>Einen Namen für diese Verbindung eingeben</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL -Instanz-URL ohne Schrägstrich]</td>
                <td>Geben Sie die URL für Ihre [!DNL Adobe Experience Manager] ein. Geben Sie am Ende der URL keinen Schrägstrich <code>/</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Benutzername]</td>
                <td>Geben Sie den Benutzernamen für das [!DNL AEM Assets] Konto ein, das für diese Verbindung verwendet wird.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Kennwort]</td>
                <td>Geben Sie das Passwort für das [!DNL AEM Assets] Konto ein, das für diese Verbindung verwendet wird.</td>
            </tr>
        </tbody>
    </table>


## [!DNL Adobe Experience Manager Assets] Module und ihre Felder

Beim Konfigurieren [!DNL Adobe Experience Manager Essentials] Module zeigt [!DNL Workfront Fusion] die unten aufgeführten Felder an. Darüber hinaus können abhängig von Faktoren wie Ihrer Zugriffsebene in der App oder dem Service weitere [!DNL Adobe Experience Manager Essentials] angezeigt werden. Ein fett gedruckter Titel in einem Modul gibt ein erforderliches Feld an.

Wenn die Zuordnungsschaltfläche über einem Feld oder einer Funktion angezeigt wird, können Sie damit Variablen und Funktionen für dieses Feld festlegen. Weitere Informationen finden Sie unter [Zuordnen von Informationen von einem Modul zu einem anderen](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Umschalter für Zuordnung](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Kopieren von Ordnern oder Assets](#copy-a-folder-or-asset)
* [Erstellen eines Datensatzes](#create-a-record)
* [Löschen von Ordnern, Assets oder Ausgabedarstellungen](#delete-a-folder-asset-or-rendition)
* [Abrufen einer Ordnerauflistung](#get-a-folder-listing)
* [Erstellen eines benutzerdefinierten API-Aufrufs](#make-a-custom-api-call)
* [Verschieben von Ordnern oder Assets](#move-a-folder-or-asset)
* [Aktualisieren eines Datensatzes](#update-a-record)
* [Hochladen eines Assets](#upload-an-asset)

### [!UICONTROL Kopieren von Ordnern oder Assets]

Dieses Aktionsmodul kopiert einen Ordner oder ein Asset an einen anderen Speicherort in Ihrem Adobe Experience Manager Assets-Konto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Experience Manager Assets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Adobe Experience Manager Assets] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie aus, ob Sie einen Ordner oder ein Asset kopieren möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner] / [!UICONTROL -Asset]</td> 
   <td>Wählen Sie den zu kopierenden Ordner oder das zu kopierende Asset aus oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zielpfad]</td> 
   <td>Wählen Sie den Pfad für den neuen Ordner oder das neue Asset aus oder ordnen Sie ihn dem Speicherort zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Name des kopierten Ordners] / [!UICONTROL -Asset]</td> 
   <td>Geben Sie einen Namen für den neuen Ordner oder das neue Asset ein. Der in [!DNL Adobe Experience Manager Assets] angezeigte Ordnername entspricht dem ursprünglichen Namen. Der hier eingegebene Name erscheint in der URL des neuen Ordners oder Assets.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Untergeordnete Elemente kopieren]</td> 
   <td>Wenn Sie einen Ordner kopieren, aktivieren Sie diese Option, um alle Unterordner oder Assets innerhalb des Ordners zu kopieren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL überschreiben]</td> 
   <td>Aktivieren Sie diese Option, um alle Ordner oder Assets am Zielspeicherort zu überschreiben, die denselben Namen wie der kopierte Ordner oder das kopierte Asset haben.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Datensatz erstellen]

Dieses Aktionsmodul erstellt einen Ordner oder einen Asset-Kommentar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Experience Manager Assets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Adobe Experience Manager Assets] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objekttyp]</td> 
   <td> <p>Wählen Sie aus, ob Sie einen Ordner oder einen Kommentar zu einem Asset erstellen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL -Ordner]</p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p>[!UICONTROL Name]</p> <p>Geben Sie einen Namen für den Ordner ein. Dieser Name wird im Dateipfad angezeigt und darf daher keine Leerzeichen oder anderen Zeichen enthalten. </p> </li> 
       <li> <p>[!UICONTROL Titel]</p> <p>Geben Sie einen Titel für den Ordner ein, der anstelle des Namens angezeigt werden kann.</p> </li> 
      </ul> </li> 
     <li> <p>[!UICONTROL Asset-Kommentar]</p> <p>Füllen Sie die folgenden Felder aus:</p> 
      <ul> 
       <li> <p>[!UICONTROL Asset-Auswahl]</p> <p>Wählen Sie die ID des Assets aus, dem Sie einen Kommentar hinzufügen möchten, oder ordnen Sie sie zu.</p> </li> 
       <li> <p>[!UICONTROL -Kommentar]</p> <p>Geben Sie den Text des Kommentars ein.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Löschen von Ordnern, Assets oder Ausgabedarstellungen]

Dieses Aktionsmodul löscht einen Ordner, ein Asset oder eine Ausgabedarstellung.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Experience Manager Assets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Adobe Experience Manager Assets] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie aus, ob Sie einen Ordner, ein Asset oder eine Ausgabedarstellung löschen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL -Ordner]</p> <p>Wählen Sie den zu löschenden Ordner aus, indem Sie die Ordner unter seinem Pfad auswählen.</p> </li> 
     <li> <p>[!UICONTROL Asset] </p> <p>Wählen Sie zuerst die Ordner im Pfad und dann das Asset aus, das Sie löschen möchten.</p> </li> 
     <li> <p>[!UICONTROL -Ausgabedarstellung]</p> <p>Wählen Sie die Ausgabedarstellung aus, indem Sie die Ordner unter ihrem Pfad auswählen.</p> <p>Geben Sie den Namen der Ausgabedarstellung ein oder mappen Sie ihn.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Ordnerauflistung abrufen]

Dieses Aktionsmodul ruft eine Darstellung eines vorhandenen Ordners und seiner untergeordneten Entitäten (Ordner oder Assets) ab.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Experience Manager Assets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Adobe Experience Manager Assets] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner]</td> 
   <td>Wählen Sie den Ordner aus, den Sie abrufen möchten, oder ordnen Sie ihn zu. Um dem Pfad Unterordner hinzuzufügen, klicken Sie auf das Pluszeichen und wählen Sie den Unterordner aus.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Erstellen eines benutzerdefinierten API-Aufrufs]

Dieses Aktionsmodul führt einen benutzerdefinierten API-Aufruf an die [!DNL Adobe Experience Manager Assets]-API durch.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Experience Manager Assets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Adobe Experience Manager Assets] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Geben Sie einen Pfad relativ zu Ihrer [!DNL Adobe Experience Manager]-Basis-URL ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL -Methode]</p> </td> 
   <td> <p>Wählen Sie die HTTP-Anfragemethode aus, die Sie zum Konfigurieren des API-Aufrufs benötigen. Weitere Informationen finden Sie unter <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP-Anfragemethoden</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Kopfzeilen]</td> 
   <td> <p>Fügen Sie die Header der Anfrage in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Beispiel: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Fügt automatisch Autorisierungskopfzeilen hinzu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abfragezeichenfolge] </td> 
   <td> <p>Geben Sie die Abfragezeichenfolge der Anfrage ein. Klicken Sie für jedes Schlüssel/Wert-Paar auf <b>[!UICONTROL Element hinzufügen]</b> und geben Sie den [!UICONTROL -Schlüssel] und den [!UICONTROL -Wert] ein.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL body]</td> 
   <td> <p>Fügen Sie den Hauptteil des Inhalts für den API-Aufruf in Form eines standardmäßigen JSON-Objekts hinzu.</p> <p>Hinweis:  <p>Wenn Sie bedingte Anweisungen wie <code>if</code> in Ihrer JSON-Datei verwenden, setzen Sie die Anführungszeichen außerhalb der bedingten Anweisung.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Verschieben von Ordnern oder Assets]

Dieses Aktionsmodul verschiebt das Asset oder den Ordner unter dem angegebenen Pfad an einen neuen Speicherort.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Experience Manager Assets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Adobe Experience Manager Assets] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie aus, ob Sie einen Ordner oder ein Asset verschieben möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ordner] / [!UICONTROL -Asset]</td> 
   <td>Wählen Sie den Ordner oder das Asset aus, den/das Sie verschieben möchten, oder ordnen Sie ihn/es zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Zielpfad]</td> 
   <td>Wählen Sie den Pfad zum Speicherort aus, an den Sie den Ordner oder das Asset verschieben möchten, oder ordnen Sie ihn zu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Name des verschobenen Ordners] / [!UICONTROL -Asset]</td> 
   <td>Geben Sie einen neuen Namen für den verschobenen Ordner oder das verschobene Asset ein. Der in [!DNL Adobe Experience Manager Assets] angezeigte Ordnername entspricht dem ursprünglichen Namen. Der hier eingegebene Name erscheint in der URL des verschobenen Ordners oder Assets.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL überschreiben]</td> 
   <td>Aktivieren Sie diese Option, um alle Ordner oder Assets am Zielspeicherort zu überschreiben, die denselben Namen wie der verschobene Ordner oder das verschobene Asset haben.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Aktualisieren eines Datensatzes]

Dieses Aktionsmodul aktualisiert einen vorhandenen Datensatz.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Experience Manager Assets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Adobe Experience Manager Assets] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Datensatztyp]</td> 
   <td> <p>Wählen Sie aus, ob Sie Asset-Metadaten oder eine Asset-Ausgabedarstellung löschen möchten.</p> 
    <ul> 
     <li> <p>[!UICONTROL Asset-Metadaten]</p> 
      <ul> 
       <li> <p>Wählen Sie das Asset aus, für das Sie Metadaten aktualisieren möchten.</p> </li> 
       <li> <p>Geben Sie den neuen Titel des Assets ein.</p> </li> 
      </ul> </li> 
     <li> <p>[!UICONTROL Asset-Ausgabedarstellung]</p> 
      <ul> 
       <li> <p>Wählen Sie das Asset aus, für das Sie die Ausgabedarstellung aktualisieren möchten.</p> </li> 
       <li> <p>Wählen Sie eine Quelldatei aus einem vorherigen Modul aus oder ordnen Sie den Namen und die Daten der Quelldatei zu.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Asset hochladen]

Dieses Aktionsmodul lädt ein Asset in Ihr [!DNL Adobe Experience Manager Assets].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Experience Manager Assets]-Kontos mit [!DNL Workfront Fusion] finden Sie unter <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Verbinden von [!DNL Adobe Experience Manager Assets] mit [!DNL Workfront Fusion]</a> in diesem Artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Ziel]</td> 
   <td> <p>Wählen Sie den Ordner aus, in den Sie ein Asset hochladen möchten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source-Datei]</td> 
   <td>Geben Sie den Namen und die Daten der Quelldatei ein oder mappen Sie sie.</td> 
  </tr> 
 </tbody> 
</table>
