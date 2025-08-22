---
title: Adobe Experience Manager Forms-Module
description: Mit dem  [!DNL Adobe Experience Manager Forms] -Connector für Adobe Workfront Fusion können Sie ein Szenario starten, das auf Ereignissen in Ihrem - [!DNL Adobe Experience Manager Forms]  basiert, Assets erstellen, hochladen und aktualisieren sowie Ordner und Assets kopieren oder verschieben.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0d7a655-1353-4d24-83d4-7da73d859a63
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 2%

---

# [!DNL Adobe Experience Manager Forms]

Mit dem [!DNL Adobe Experience Manager Forms]-Connector für Adobe Workfront Fusion können Sie ein Szenario starten, das auf Ereignissen in Ihrem [!DNL Adobe Experience Manager Forms] basiert, indem Sie einen Webhook erstellen.

Sie können ein Formular in [!DNL Adobe Experience Manager Forms] so konfigurieren, dass Formularübermittlungen an diesen Webhook gesendet werden.

## Zugriffsanforderungen

Sie müssen über folgenden Zugriff verfügen, um die Funktion in diesem Artikel verwenden zu können:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-Plan*</td>
  <td> <p>[!UICONTROL Pro] oder höher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-Lizenz*</td>
   <td> <p>[!UICONTROL -Plan], [!UICONTROL -Arbeit]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lizenz für Adobe Workfront Fusion**</td> 
   <td>
   <p>Aktuelle Lizenzanforderung: Keine Workfront Fusion-Lizenzanforderung.</p>
   <p>Oder</p>
   <p>Legacy-Lizenzanforderung: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produkt</td> 
   <td>
   <p>Aktuelle Produktanforderung: Wenn Sie über den Plan [!UICONTROL Select] oder [!UICONTROL Prime] Adobe Workfront verfügen, muss Ihr Unternehmen Adobe Workfront Fusion sowie Adobe Workfront erwerben, um die in diesem Artikel beschriebenen Funktionen nutzen zu können. Workfront Fusion ist im Workfront-Plan [!UICONTROL Ultimate] enthalten.</p>
   <p>Oder</p>
   <p>Legacy-Produktanforderung: Ihr Unternehmen muss Adobe Workfront Fusion sowie Adobe Workfront erwerben, um die in diesem Artikel beschriebenen Funktionen nutzen zu können.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Wenden Sie sich an Ihren Workfront-Administrator, um herauszufinden, über welchen Plan, welchen Lizenztyp oder welchen Zugriff Sie verfügen.

Informationen zu Adobe Workfront Fusion-Lizenzen finden Sie unter [Adobe Workfront Fusion-Lizenzen](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Voraussetzungen

* Sie müssen über ein [!DNL Adobe Experience Manager Forms]-Konto verfügen, um dieses Modul verwenden zu können.

## Adobe Experience Manager Assets-API-Informationen

Der Adobe Experience Manager Assets-Connector verwendet Folgendes:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-Tag</td> 
   <td>v1.2.27</td> 
  </tr>
 </tbody> 
 </table>

## Erstellen einer Verbindung mit Adobe Experience Manager Forms

So erstellen Sie eine Verbindung für Ihre [!DNL Adobe Experience Manager Forms]:

1. Klicken Sie in einem beliebigen Modul **[!UICONTROL Hinzufügen]** neben dem Feld Verbindung .

1. Füllen Sie die folgenden Felder aus:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Verbindungsname]</td>
        <td>
          <p>Geben Sie einen Namen für diese Verbindung ein.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Umgebung]</td>
        <td>
          <p>Wählen Sie aus, ob diese Verbindung mit einer Produktions- oder Nicht-Produktionsumgebung verbunden werden soll.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Typ]</td>
        <td>
          <p>Wählen Sie aus, ob dieses Konto ein Service-Konto oder ein persönliches Konto ist.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL -Instanz-URL ohne Schrägstrich]</td>
        <td>
          <p>Geben Sie die URL ein, über die Sie auf das Konto zugreifen möchten, ohne den abschließenden Schrägstrich.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL IMS-Endpunkt]</td>
        <td>
          <p><code>https://ims-na1.adobelogin.com</code></p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-ID]</td>
        <td>Geben Sie Ihre [!DNL Adobe]-Client-ID ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client-Geheimnis]</td>
        <td>Geben Sie Ihr [!DNL Adobe]-Client-Geheimnis ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Org ID]</td>
        <td>Geben Sie Ihre [!DNL Adobe] Organisations-ID ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID des technischen Kontos]</td>
        <td>Geben Sie die ID Ihres [!DNL Adobe] technischen Kontos ein. Dies finden Sie im Abschnitt [!UICONTROL Anmeldeinformationen] des [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>Geben Sie alle passenden Metabereiche ein       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Privater Schlüssel]</td>
        <td>
          <p>Geben Sie den privaten Schlüssel ein, der bei der Erstellung Ihrer Anmeldeinformationen im [!DNL Adobe Developer Console] generiert wurde. </p>
          <p>So extrahieren Sie Ihren privaten Schlüssel oder Ihr Zertifikat:</p>
          <ol>
            <li value="1">
              <p>Klicken Sie auf <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Wählen Sie den zu extrahierenden Dateityp aus.</p>
            </li>
            <li value="3">
              <p>Wählen Sie die Datei aus, die den privaten Schlüssel oder das Zertifikat enthält.</p>
            </li>
            <li value="4">
              <p>Geben Sie das Kennwort für die Datei ein.</p>
            </li>
            <li value="5">
              <p>Klicken Sie auf <b>[!UICONTROL Speichern]</b>, um die Datei zu extrahieren und zur Verbindungseinrichtung zurückzukehren.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. Klicken Sie **[!UICONTROL Fortfahren]**, um die Verbindung zu speichern und zum Modul zurückzukehren.

## Adobe Experience Manager Forms-Modul und seine Felder

Derzeit gibt es nur ein Modul im Adobe Experience Manager Forms-Connector.

### Nach Formularereignissen suchen

Mit diesem Trigger (Webhook) können Sie ein Szenario starten, wenn eine Übermittlungsaktion in einem Adobe Experience Manager-Formular stattfindet.

>[!IMPORTANT]
>
>Dieses Modul muss auch in Adobe Experience Manager konfiguriert werden. Nachdem Sie diesen Webhook eingerichtet haben, müssen Sie Adobe Experience Manager öffnen und Ihr Formular so konfigurieren, dass Übermittlungen an den Webhook gesendet werden.
>
><!--For instructions on the required form configuration, see insert url here-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook-Name]</td> 
   <td> <p>Einen Namen für den Webhook eingeben</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL -Verbindung]</td> 
   <td> <p>Anweisungen zum Verbinden Ihres [!DNL Adobe Experience Manager]-Kontos mit Workfront Fusion finden Sie unter <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/aem-forms-modules.md#create-a-connection-to-adobe-experience-manager-forms" class="MCXref xref">Erstellen einer Verbindung zu [!DNL Adobe Experience Manager Forms]</a></p> </td> 
  </tr>

Das Modul erstellt einen Webhook und gibt die Webhook-Adresse an, die Sie in [!DNL Adobe Experience Manager Forms] in das Dialogfeld für die Formularübermittlung eingeben können.
