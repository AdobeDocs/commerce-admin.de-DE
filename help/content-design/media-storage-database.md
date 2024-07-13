---
title: Mediendatenbank verwenden
description: Erfahren Sie, wie Sie mit einer Mediendatenbank Ihre [!DNL Commerce] Mediendateien speichern können.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Mediendatenbank verwenden

>[!IMPORTANT]
>
>Die Speichermethode für Datenbankmedien wird seit Adobe Commerce und Magento Open Source 2.4.3 nicht mehr unterstützt.

Standardmäßig werden alle Bilder, kompilierten CSS-Dateien und kompilierten JavaScript-Dateien der [!DNL Commerce] -Instanz im Dateisystem auf dem Webserver gespeichert. Sie können diese Dateien in einer Datenbank auf einem Datenbankserver speichern. Ein Vorteil dieses Ansatzes ist die Option der automatischen Synchronisation und umgekehrten Synchronisation zwischen dem Dateisystem des Webservers und der Datenbank. Sie können die Standarddatenbank verwenden, um Medien zu speichern oder eine zu erstellen. Um eine neu erstellte Datenbank als Medienspeicher verwenden zu können, müssen Sie der Datei &quot;`env.php`&quot;Informationen über sie und ihre Zugriffsberechtigungen hinzufügen.

## Datenbank-Workflow

1. **Browser fordert media an** - Eine Seite aus dem Store wird im Browser des Kunden geöffnet und der Browser fordert die im HTML angegebenen Medien an.

1. **System sucht im Dateisystem nach Medien** - Das System sucht im Dateisystem nach den Medien und übergibt sie, falls sie gefunden werden, an den Browser.

1. **System sucht Medien in der Datenbank** - Wenn das Medium nicht im Dateisystem gefunden wird, wird eine Anforderung für das Medium an die Datenbank gesendet, die in der Konfiguration angegeben ist.

1. **System lokalisiert Medien in Datenbank** - Ein PHP-Skript überträgt die Dateien aus der Datenbank in das Dateisystem und sendet sie an den Browser des Kunden. Die Browser-Anfrage für Media Trigger führt das Skript wie folgt aus:

   - Wenn der Webserver [rewrites](../merchandising-promotions/url-rewrite.md) für [!DNL Commerce] aktiviert und vom Server unterstützt wird, wird das PHP-Skript nur ausgeführt, wenn die angeforderten Medien nicht im Dateisystem gefunden werden.
   - Wenn Webserver-Neuschreibungen für [!DNL Commerce] deaktiviert sind oder vom Server nicht unterstützt werden, wird das PHP-Skript trotzdem ausgeführt, auch wenn die erforderlichen Medien im Dateisystem verfügbar sind.

## Datenbank für Medienspeicherung verwenden

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]** aus.

1. Setzen Sie oben links **[!UICONTROL Store View]** auf `Default Config` , um die Konfiguration auf die globale Ebene anzuwenden.

1. Erweitern Sie den Abschnitt **[!UICONTROL Storage Configuration for Media]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Erweiterte Konfiguration - Speicherkonfiguration für Medien](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Setzen Sie **[!UICONTROL Media Storage]** auf `Database`.

   - Setzen Sie **[!UICONTROL Select Media Database]** auf die Datenbank, die Sie verwenden möchten.

   - Um die vorhandenen Medien in die neu ausgewählte Datenbank zu übertragen, klicken Sie auf **[!UICONTROL Synchronize]**.

   - Geben Sie den Wert **[!UICONTROL Environment Update Time]** in Sekunden ein.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
