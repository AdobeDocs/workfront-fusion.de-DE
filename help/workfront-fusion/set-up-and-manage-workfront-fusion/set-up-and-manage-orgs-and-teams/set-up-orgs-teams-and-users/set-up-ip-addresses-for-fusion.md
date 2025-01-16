---
title: Konfigurieren von IP-Adressen für Fusion in der Zulassungsliste Ihres Unternehmens
description: Fusion verwendet bestimmte IP-Adressen und Domains für die Web-Kommunikation. Diese müssen zur Zulassungsliste Ihres Unternehmens hinzugefügt werden, bevor Sie Workfront in Ihrem Unternehmen verwenden können.
author: Becky
feature: Workfront Fusion
exl-id: 406dd45c-0863-4270-a80e-c1c115e0b367
source-git-commit: 59d739093c88238af7a7e97499fd0c7d7cf6053a
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# Konfigurieren von IP-Adressen für Fusion in der Zulassungsliste Ihres Unternehmens

Da Adobe Workfront Fusion mit dem Netzwerk Ihres Unternehmens kommuniziert, muss die Firewall Ihres Unternehmens so konfiguriert sein, dass diese Kommunikation möglich ist. Firewalls sind hochwirksame Sicherheitsmaßnahmen, die durch die Trennung des Unternehmensnetzwerks vom Internet funktionieren. Sie stellen sicher, dass nur ausgewählte Daten und der Netzwerk-Traffic in das Netzwerk des Unternehmens bzw. aus diesem heraus verschoben werden können. Die Firewall lässt Daten basierend auf der Website, die die Daten sendet oder empfängt, zu oder blockiert diese. Als Fusion-Administrator müssen Sie sicherstellen, dass Daten, die an oder von Fusion gesendet werden, die Firewall Ihrer Organisation durchlaufen können.

Dies wird durch eine -Zulassungsliste erreicht, die im Wesentlichen eine „Liste“ von Sites ist, die „erlaubt“ sind, Daten über die Firewall zu senden oder zu empfangen. Websites können auf zwei Arten identifiziert werden:

* **IP-Adresse**: eine Reihe von Zahlen wie 52.31.132.175
* **Domain**: Teil einer URL, z. B. `thisdomain` in `www.thisdomain.com`

Fusion verwendet bestimmte IP-Adressen und Domains für die Web-Kommunikation. Diese müssen zur Zulassungsliste Ihres Unternehmens hinzugefügt werden, bevor Sie Workfront in Ihrem Unternehmen verwenden können.

Normalerweise wird eine Zulassungsliste von einem Netzwerkadministrator konfiguriert. Arbeiten Sie mit dem Netzwerkadministrator Ihres Unternehmens zusammen, um sicherzustellen, dass Ihre Firewall diese IP-Adressen zulässt. Wenn Sie nicht wissen, wer Ihr Netzwerkadministrator ist, kann die IT-Abteilung Ihres Unternehmens Sie in die richtige Richtung weisen.

>[!IMPORTANT]
>
>Als Fusion-Administrator müssen Sie sicherstellen, dass diese IP-Adressen und Domains zur Zulassungsliste Ihres Unternehmens hinzugefügt werden. Dies gilt auch, wenn Sie sie nicht selbst hinzufügen. Fusion kann die Zulassungsliste Ihres Unternehmens nicht konfigurieren.

Sie können alle IP-Adressen und Domains von Fusion zu Ihrer Zulassungsliste hinzufügen oder Ihren Fusion-Cluster suchen und nur die IP-Adressen und Domains für diesen Cluster hinzufügen.

## Alle IP-Adressen und Domains von Fusion hinzufügen

Fügen Sie Ihrer Zulassungsliste die folgenden IP-Adressen hinzu:

* 52.30.133.50
* 54.220.93.204
* 34.254.76.122
* 54.244.142.219
* 52.39.217.230
* 44.241.82.96
* 100.20.126.137
* 34.223.32.4
* 52.39.176.220
* 20.36.133.48/28
* 20.81.156.240/28
* 172.172.84.48/28

Wenn Ihr Unternehmen ausgehende Netzwerkfilter verwendet, fügen Sie außerdem die folgende Domain zu Ihrer Zulassungsliste hinzu, damit Ihr System auf Workfront Fusion zugreifen kann.

* hook.app.workfrontfusion.com
* hook.app-eu.workfrontfusion.com
* hook.app-az.workfrontfusion.com

## Fügen Sie Fusion IP-Adressen und Domains nur für Ihren Cluster hinzu

### Identifizieren des Rechenzentrums

Die IP-Adressen variieren je nachdem, wo Ihre Daten gespeichert werden.

Wenn Sie über eine URL auf Fusion zugreifen, können Sie die URL überprüfen, um Ihr Rechenzentrum zu finden.

| URL | Rechenzentrum |
| --- | --- |
| `https://app.workfrontfusion.com` | US-Rechenzentrum |
| `https://app-eu.workfrontfusion.com` | EU-Rechenzentrum |
| `https://app-az.workfrontfusion.com` | Azure-Cluster |

Wenn Sie über `experience.adobe.com` auf Fusion zugreifen, können Sie die Registerkarte Netzwerk in Ihrem Browser überprüfen, um das Rechenzentrum zu identifizieren.

| URL | Rechenzentrum |
| --- | --- |
| Aufrufe an `https://fusion.adobe.com` | US-Rechenzentrum |
| Aufrufe an `https://eu.fusion.adobe.com` | EU-Rechenzentrum |
| Aufrufe an `https://az.fusion.adobe.com` | Azure-Cluster |

### Hinzufügen von IP-Adressen und Domains für Ihr Rechenzentrum

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] EU-Rechenzentrum</td> 
   <td> 
    <ul> 
     <li>52.30.133.50</li> 
     <li>54.220.93.204</li> 
     <li>34.254.76.122</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront] US-Rechenzentrum</p> </td> 
   <td> 
    <ul> 
     <li>54.244.142.219</li> 
     <li>52.39.217.230</li> 
     <li>44.241.82.96</li>
     <li>100.20.126.137</li>
     <li>34.223.32.4</li>
     <li>52.39.176.220</li>
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] im Microsoft Azure-Cluster</td> 
   <td> 
    <ul> 
     <li>20.36.133.48/28</li> 
     <li>20.81.156.240/28</li> 
     <li>172.172.84.48/28</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Wenn Ihr Unternehmen ausgehende Netzwerkfilter verwendet, fügen Sie außerdem die folgende Domain zu Ihrer Zulassungsliste hinzu, damit Ihr System auf Workfront Fusion zugreifen kann. Diese werden für Webhooks verwendet

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] EU-Rechenzentrum</td> 
   <td> <p> hook.app-eu.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront] US-Rechenzentrum</p> </td> 
   <td> <p>hook.app.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront Fusion] im Microsoft Azure-Cluster</p> </td> 
   <td> <p>hook.app-az.workfrontfusion.com </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Filterung ausgehender Netzwerke ist ungewöhnlich. Erkundigen Sie sich bei Ihrem Netzwerkadministrator, ob Sie Ihre Zulassungsliste aktualisieren müssen, um sie zu berücksichtigen.
