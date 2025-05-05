---
title: Verwenden eines Netzwerks zur Inhaltsbereitstellung
description: Erfahren Sie, wie Sie ein Content Delivery Network (CDN) zum Speichern von Mediendateien verwenden.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Verwenden eines Netzwerks zur Inhaltsbereitstellung

Ein Content Delivery Network (CDN) kann zum Speichern von Mediendateien verwendet werden. Adobe Commerce in Cloud-Infrastruktur umfasst das Fastly CDN (siehe [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html?lang=de) im _Handbuch zu Commerce in Cloud-Infrastruktur_). Bei einer (On _Premise) installierten Commerce_ Instanz ist keine Integration mit einem bestimmten CDN vorhanden. Sie können das CDN Ihrer Wahl verwenden.

Nach der Konfiguration des CDN müssen Sie die Konfiguration über den Administrator abschließen. Die Änderungen können entweder auf globaler oder auf Website-Ebene vorgenommen werden. Wenn ein CDN für die Medienspeicherung verwendet wird, werden alle Pfade zu Medien auf Commerce-Speicherseiten in die in der Konfiguration angegebenen CDN-Pfade geändert.

## CDN-Workflow

1. **Browser fordert Medien an** - Eine Seite aus dem Store wird im Browser des Kunden geöffnet, und der Browser fordert das Medium an, das auf der HTML angegeben ist.
1. **Anfrage an CDN gesendet; Bilder gefunden und bereitgestellt** - Die Anfrage wird zuerst an das CDN gesendet. Wenn das CDN die Bilder im Speicher hat, stellt es die Mediendateien im Browser des Kunden bereit.
1. **Medien nicht gefunden, Anfrage an [!DNL Commerce] Webserver gesendet** - Wenn das CDN nicht über die Mediendateien verfügt, wird die Anfrage an den [!DNL Commerce] Webserver gesendet. Wenn die Mediendateien im Dateisystem gefunden werden, sendet der Webserver sie an den Browser des Kunden.

>[!IMPORTANT]
>
>Wenn ein CDN als Medienspeicher verwendet wird, funktioniert JavaScript aus Sicherheitsgründen möglicherweise nicht ordnungsgemäß, wenn sich das CDN außerhalb Ihrer Subdomain befindet.

## Konfigurieren eines Content Delivery Network

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL General]_&#x200B;die Option **[!UICONTROL Web]**&#x200B;aus.

1. Legen Sie in der oberen linken Ecke nach Bedarf **[!UICONTROL Store View]** fest.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Base URLs]** und führen Sie folgende Schritte aus:

   ![Allgemeine Konfiguration - Web-Basis-URLs](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Aktualisieren Sie die **[!UICONTROL Base URL for Static View Files]** mit der URL des Speicherorts im CDN, an dem statische Ansichtsdateien gespeichert werden.

   - Aktualisieren Sie die **[!UICONTROL Base URL for User Media Files]** mit der URL der JavaScript-Dateien im CDN.

     Beide Felder können leer gelassen werden oder mit dem Platzhalter beginnen: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Base URLs (Secure)]** und führen Sie folgende Schritte aus:

   ![Allgemeine Konfiguration - Web-Basis-URLs (sicher)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Aktualisieren Sie die **[!UICONTROL Secure Base URL for Static View Files]** mit der URL des Speicherorts im CDN, an dem statische Ansichtsdateien gespeichert werden.

   - Aktualisieren Sie die **[!UICONTROL Secure Base URL for User Media Files]** mit der URL der JavaScript-Dateien im CDN.

     Beide Felder können leer gelassen werden oder mit dem Platzhalter beginnen: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
