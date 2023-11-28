---
title: Mediendatenbank verwenden
description: Erfahren Sie, wie Sie mit einer Mediendatenbank Ihre [!DNL Commerce] Mediendateien.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Mediendatenbank verwenden

>[!IMPORTANT]
>
>Die Speichermethode für Datenbankmedien wird seit Adobe Commerce und Magento Open Source 2.4.3 nicht mehr unterstützt.

Standardmäßig werden alle Bilder, kompilierte CSS-Dateien und kompilierte JavaScript-Dateien der [!DNL Commerce] -Instanz im Dateisystem auf dem Webserver gespeichert. Sie können diese Dateien in einer Datenbank auf einem Datenbankserver speichern. Ein Vorteil dieses Ansatzes ist die Option der automatischen Synchronisation und umgekehrten Synchronisation zwischen dem Dateisystem des Webservers und der Datenbank. Sie können die Standarddatenbank verwenden, um Medien zu speichern oder eine zu erstellen. Um eine neu erstellte Datenbank als Medienspeicher verwenden zu können, müssen Sie Informationen zu ihr und ihren Zugriffsberechtigungen zum `env.php` -Datei.

## Datenbank-Workflow

1. **Browser-Anforderungen Medien** - Eine Seite aus dem Store wird im Browser des Kunden geöffnet und der Browser fordert das in der HTML angegebene Medium an.

1. **System sucht nach Medien im Dateisystem** - Das System sucht im Dateisystem nach den Medien und übergibt sie, falls sie gefunden werden, an den Browser.

1. **System lokalisiert Medien in der Datenbank** - Wenn das Medium nicht im Dateisystem gefunden wird, wird eine Anforderung für das Medium an die in der Konfiguration angegebene Datenbank gesendet.

1. **System lokalisiert Medien in der Datenbank** - Ein PHP-Skript überträgt die Dateien aus der Datenbank in das Dateisystem und sendet sie an den Browser des Kunden. Die Browser-Anfrage für Media Trigger führt das Skript wie folgt aus:

   - Wenn Webserver [rewrites](../merchandising-promotions/url-rewrite.md) aktiviert sind für [!DNL Commerce] und vom Server unterstützt wird, wird das PHP-Skript nur ausgeführt, wenn die angeforderten Medien nicht im Dateisystem gefunden werden.
   - Wenn Webserver-Neuschreibungen deaktiviert sind für [!DNL Commerce]oder vom Server nicht unterstützt wird, wird das PHP-Skript trotzdem ausgeführt, auch wenn die erforderlichen Medien im Dateisystem verfügbar sind.

## Datenbank für Medienspeicherung verwenden

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL System]**.

1. Legen Sie in der oberen linken Ecke **[!UICONTROL Store View]** nach `Default Config` , um die Konfiguration auf globaler Ebene anzuwenden.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Storage Configuration for Media]** und führen Sie folgende Schritte aus:

   ![Erweiterte Konfiguration - Speicherkonfiguration für Medien](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Satz **[!UICONTROL Media Storage]** nach `Database`.

   - Satz **[!UICONTROL Select Media Database]** in die Datenbank, die Sie verwenden möchten.

   - Um die vorhandenen Medien in die neu ausgewählte Datenbank zu übertragen, klicken Sie auf **[!UICONTROL Synchronize]**.

   - Geben Sie die **[!UICONTROL Environment Update Time]** in Sekunden.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
