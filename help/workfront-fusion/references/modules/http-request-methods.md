---
title: HTTP-Anfragemethoden
description: Wenn Sie einen API-Aufruf in einem Modul konfigurieren, müssen Sie die HTTP-Anfragemethode auswählen. In diesem Artikel werden die verfügbaren Methoden beschrieben und warum Sie jede auswählen sollten.
author: Becky
feature: Workfront Fusion
exl-id: 481131c9-356a-4c62-a653-d6bba9be5be8
TQID: https://experienceleague.adobe.com/Z11y3dk6PtoN11Gja8S2ZyJlTJZNZfXfcPPrNJWvbRk
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 303
ht-degree: 1%

---

# HTTP-Anfragemethoden

Wenn Sie einen API-Aufruf in einem Modul konfigurieren, müssen Sie die HTTP-Anfragemethode auswählen. In diesem Artikel werden die verfügbaren Methoden beschrieben und warum Sie jede auswählen sollten.

## HTTP-Methoden

Verwenden Sie eine der folgenden HTTP-Methoden.

* **[!UICONTROL GET]**: Ruft Daten von einem Webserver basierend auf Ihren Parametern ab. [!UICONTROL GET] fordert eine Darstellung der angegebenen Ressource an und erhält bei Erfolg eine [!UICONTROL 200 OK]-Antwortnachricht mit dem angeforderten Inhalt.
* **[!UICONTROL POST]**: Sendet Daten basierend auf Ihren Parametern an einen Webserver. [!UICONTROL POST]-Anfragen enthalten Aktionen wie das Hochladen einer Datei. Mehrere [!UICONTROL POST]s können zu einem anderen Ergebnis führen als ein einzelner [!UICONTROL POST]. Gehen Sie daher vorsichtig vor, wenn Sie versehentlich mehrere [!UICONTROL POST] senden. Wenn ein [!UICONTROL POST] erfolgreich ist, erhalten Sie eine [!UICONTROL 200 OK]-Antwortnachricht.
* **[!UICONTROL PUT]**: Sendet Daten basierend auf Ihren Parametern an einen Speicherort im Webserver. [!UICONTROL PUT]-Anfragen enthalten Aktionen wie das Hochladen einer Datei. Der Unterschied zwischen einem [!UICONTROL PUT] und [!UICONTROL POST] besteht darin, dass PUT idempotent ist, was bedeutet, dass das Ergebnis eines einzelnen erfolgreichen [!UICONTROL PUT] dasselbe ist wie viele identische [!UICONTROL PUT]s. Wenn eine PUT erfolgreich ist, erhalten Sie eine Antwort von 200 (normalerweise 201 oder 204).
* **[!UICONTROL PATCH]**: (Für einige API-Aufrufmodule nicht verfügbar) Wendet basierend auf Ihren Parametern partielle Änderungen an einer Ressource auf einem Webserver an. [!UICONTROL PATCH] ist nicht idempotent, was bedeutet, dass das Ergebnis mehrerer [!UICONTROL PATCH]s unbeabsichtigte Folgen haben kann. Wenn eine [!UICONTROL PATCH] erfolgreich ist, erhalten Sie eine Antwortnachricht von 200 (normalerweise 204).
* **[!UICONTROL DELETE]**: Löscht die angegebene Ressource vom Webserver basierend auf Ihren Parametern (wenn die Ressource vorhanden ist). Wenn eine [!UICONTROL DELETE] erfolgreich ist, erhalten Sie eine Antwort von 200 OK.
