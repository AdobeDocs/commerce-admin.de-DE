---
title: Verwenden einer Mediendatenbank
description: Erfahren Sie, wie Sie mit einer Mediendatenbank Ihre  [!DNL Commerce] -Mediendateien speichern können.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/QUhPGliOg0grz9UcLAcWWiPd5Zh4pIvB-n-QeORilfg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 0%

---

# Verwenden einer Mediendatenbank

>[!IMPORTANT]
>
>Die Datenbankspeichermethode wird seit Adobe Commerce und Magento Open Source 2.4.3 nicht mehr unterstützt.

Standardmäßig werden alle Bilder, kompilierten CSS-Dateien und kompilierten JavaScript-Dateien der [!DNL Commerce]-Instanz im Dateisystem auf dem Webserver gespeichert. Sie können diese Dateien in einer Datenbank auf einem Datenbankserver speichern. Ein Vorteil dieses Ansatzes ist die Möglichkeit der automatischen Synchronisation und umgekehrten Synchronisation zwischen dem Webserver-Dateisystem und der Datenbank. Sie können die Standarddatenbank verwenden, um Medien zu speichern oder eine zu erstellen. Um eine neu erstellte Datenbank als Medienspeicher verwenden zu können, müssen Sie Informationen über sie und ihre Zugriffsberechtigungen zur `env.php`-Datei hinzufügen.

## Datenbank-Workflow

1. **Browser fordert Medien an** - Eine Seite aus dem Store wird im Browser des Kunden geöffnet, und der Browser fordert die Medien an, die in der HTML angegeben sind.

1. **System sucht im Dateisystem nach Medien** - Das System sucht im Dateisystem nach den Medien und übergibt sie, wenn sie gefunden werden, an den Browser.

1. **System findet Medien in der Datenbank** - Wenn das Medium nicht im Dateisystem gefunden wird, wird eine Anforderung für das Medium an die in der Konfiguration angegebene Datenbank gesendet.

1. **System findet Medien in der Datenbank** - Ein PHP-Skript überträgt die Dateien von der Datenbank an das Dateisystem und sendet sie an den Browser des Kunden. In der Browser-Anfrage für Media Triggers wird das Skript wie folgt ausgeführt:

   - Wenn Webserver [rewrites](../merchandising-promotions/url-rewrite.md) für [!DNL Commerce] aktiviert und vom Server unterstützt werden, wird das PHP-Skript nur ausgeführt, wenn das angeforderte Medium nicht im Dateisystem gefunden wird.
   - Wenn Webserver-Neuschreibungen für [!DNL Commerce] deaktiviert sind oder vom Server nicht unterstützt werden, wird das PHP-Skript trotzdem ausgeführt, auch wenn die erforderlichen Medien im Dateisystem verfügbar sind.

## Verwenden einer Datenbank für Medienspeicher

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Legen Sie in der oberen linken Ecke **[!UICONTROL Store View]** auf `Default Config` fest, um die Konfiguration auf globaler Ebene anzuwenden.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Storage Configuration for Media]** und führen Sie folgende Schritte aus:

   ![Erweiterte Konfiguration - Speicherkonfiguration für Medien](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Legen Sie **[!UICONTROL Media Storage]** auf `Database` fest.

   - Legen Sie **[!UICONTROL Select Media Database]** auf die Datenbank fest, die Sie verwenden möchten.

   - Um das vorhandene Medium in die neu ausgewählte Datenbank zu übertragen, klicken Sie auf **[!UICONTROL Synchronize]**.

   - Geben Sie die **[!UICONTROL Environment Update Time]** in Sekunden ein.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
