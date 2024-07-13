---
title: Netzwerk zur Inhaltsbereitstellung verwenden
description: Erfahren Sie, wie Sie zum Speichern von Mediendateien ein Content Delivery Network (CDN) verwenden.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Netzwerk zur Inhaltsbereitstellung verwenden

Zum Speichern von Mediendateien kann ein CDN (Content Delivery Network) verwendet werden. Adobe Commerce in der Cloud-Infrastruktur umfasst das Fastly-CDN (siehe [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) im _Commerce on Cloud Infrastructure Guide_). Eine Commerce-Instanz, die _vor Ort_ installiert ist, enthält keine Integration in ein bestimmtes CDN. Sie können das CDN Ihrer Wahl verwenden.

Nach dem Konfigurieren des CDN müssen Sie die Konfiguration vom Administrator abschließen. Die Änderungen können entweder auf globaler oder auf Website-Ebene vorgenommen werden. Wenn ein CDN für die Medienspeicherung verwendet wird, werden alle Pfade zu Medien auf Commerce-Speicherseiten in die in der Konfiguration angegebenen CDN-Pfade geändert.

## CDN-Workflow

1. **Browser fordert media an** - Eine Seite aus dem Store wird im Browser des Kunden geöffnet und der Browser fordert die im HTML angegebenen Medien an.
1. **Anfrage an CDN gesendet; Bilder gefunden und bereitgestellt** - Die Anfrage wird zuerst an das CDN gesendet. Wenn das CDN die Bilder im Speicher hat, stellt es die Mediendateien für den Browser des Kunden bereit.
1. **Medien nicht gefunden, Anfrage an [!DNL Commerce] Webserver** gesendet - Wenn das CDN nicht über die Mediendateien verfügt, wird die Anfrage an den [!DNL Commerce] Webserver gesendet. Wenn die Mediendateien im Dateisystem gefunden werden, sendet der Webserver sie an den Browser des Kunden.

>[!IMPORTANT]
>
>Aus Sicherheitsgründen funktioniert JavaScript möglicherweise nicht ordnungsgemäß, wenn ein CDN als Medienspeicher verwendet wird, wenn sich das CDN außerhalb Ihrer Subdomäne befindet.

## Netzwerk zur Inhaltsbereitstellung konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Web]**.

1. Legen Sie in der oberen linken Ecke den Wert &quot;**[!UICONTROL Store View]**&quot;nach Bedarf fest.

1. Erweitern Sie den Abschnitt **[!UICONTROL Base URLs]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Allgemeine Konfiguration - Web-Basis-URLs](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Aktualisieren Sie die **[!UICONTROL Base URL for Static View Files]** mit der URL des Speicherorts im CDN, in dem statische Ansichtsdateien gespeichert sind.

   - Aktualisieren Sie die **[!UICONTROL Base URL for User Media Files]** mit der URL der JavaScript-Dateien im CDN.

     Beide Felder können leer gelassen werden oder mit dem Platzhalter beginnen: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Erweitern Sie den Abschnitt **[!UICONTROL Base URLs (Secure)]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Allgemeine Konfiguration - Web-Basis-URLs (sicher)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Aktualisieren Sie die **[!UICONTROL Secure Base URL for Static View Files]** mit der URL des Speicherorts im CDN, in dem statische Ansichtsdateien gespeichert sind.

   - Aktualisieren Sie die **[!UICONTROL Secure Base URL for User Media Files]** mit der URL der JavaScript-Dateien im CDN.

     Beide Felder können leer gelassen werden oder mit dem Platzhalter beginnen: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
