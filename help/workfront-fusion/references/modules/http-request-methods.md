---
title: HTTP-Anfragemethoden
description: Wenn Sie einen API-Aufruf in einem Modul konfigurieren, müssen Sie die HTTP-Anfragemethode auswählen. In diesem Artikel werden die verfügbaren Methoden beschrieben und warum Sie jede auswählen sollten.
author: Becky
feature: Workfront Fusion
exl-id: 481131c9-356a-4c62-a653-d6bba9be5be8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# HTTP-Anfragemethoden

Wenn Sie einen API-Aufruf in einem Modul konfigurieren, müssen Sie die HTTP-Anfragemethode auswählen. In diesem Artikel werden die verfügbaren Methoden beschrieben und warum Sie jede auswählen sollten.

## HTTP-Methoden

Verwenden Sie eine der folgenden HTTP-Methoden.

* **[!UICONTROL GET]**: Ruft Daten von einem Webserver basierend auf Ihren Parametern ab. [!UICONTROL GET] fordert eine Darstellung der angegebenen Ressource an und erhält bei Erfolg eine [!UICONTROL 200 OK]-Antwortnachricht mit dem angeforderten Inhalt.
* **[!UICONTROL POST]**: Sendet Daten basierend auf Ihren Parametern an einen Webserver. [!UICONTROL POST] Anfragen enthalten Aktionen wie das Hochladen einer Datei. Mehrere [!UICONTROL POST] können zu einem anderen Ergebnis führen als ein einzelnes [!UICONTROL POST]. Gehen Sie daher vorsichtig vor, wenn Sie versehentlich mehrere [!UICONTROL POST] senden. Wenn eine [!UICONTROL POST] erfolgreich ist, erhalten Sie eine [!UICONTROL 200 OK].
* **[!UICONTROL PUT]**: Sendet Daten anhand Ihrer Parameter an einen Speicherort im Webserver. [!UICONTROL PUT] Anfragen enthalten Aktionen wie das Hochladen einer Datei. Der Unterschied zwischen einem [!UICONTROL PUT] und [!UICONTROL POST] besteht darin, dass PUT idempotent ist, d. h., dass das Ergebnis eines einzelnen erfolgreichen [!UICONTROL PUT] dasselbe ist wie viele identische [!UICONTROL PUT]. Bei erfolgreicher PUT erhalten Sie eine 200-fache Antwortnachricht (normalerweise 201 oder 204).
* **[!UICONTROL PATCH]**: (Für einige API-Aufrufmodule nicht verfügbar) Wendet basierend auf Ihren Parametern partielle Änderungen an einer Ressource auf einem Webserver an. [!UICONTROL PATCH] ist nicht idempotent, was bedeutet, dass das Ergebnis mehrerer [!UICONTROL PATCH] unbeabsichtigte Folgen haben könnte. Wenn eine [!UICONTROL PATCH] erfolgreich ist, erhalten Sie eine 200-fache Antwortnachricht (normalerweise 204).
* **[!UICONTROL DELETE]**: Löscht die angegebene Ressource vom Webserver basierend auf Ihren Parametern (wenn die Ressource vorhanden ist). Wenn eine [!UICONTROL DELETE] erfolgreich ist, erhalten Sie eine 200-OK-Antwortnachricht.
