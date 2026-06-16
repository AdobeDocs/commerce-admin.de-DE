---
title: Media Gallery-Bildoptimierung
description: Erfahren Sie, wie Sie die Bildoptimierung für Ihre Medien [!DNL Commerce] Assets verwenden.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/BTjXX6X70q2Mwm0xPNx-t429R5m93VprCHBDcYgQNpY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 211
ht-degree: 0%

---

# Media Gallery-Bildoptimierung

Die neue [Mediensammlung](media-gallery.md) bietet eine Funktion _Bildoptimierung_, die die Leistung verbessert und die Größe der Mediendateien in der Storefront verringert. Diese Optimierung ist standardmäßig aktiviert und kann in den Store-Konfigurationseinstellungen geändert werden.

## Konfigurieren der Bildoptimierung

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Enable Image Optimization]** auf `Yes` fest.
   - Geben Sie die **[!UICONTROL Maximum Width]** und **[!UICONTROL Maximum Height]** Werte (in Pixeln) entsprechend Ihren Anforderungen ein.

## Verhalten

Wenn die Bildoptimierungsfunktion der Mediensammlung aktiviert ist, wird automatisch eine optimierte Kopie eines Bildes anstelle der Originaldatei in den Inhalt [Mediensammlung](media-gallery.md) eingefügt.

Wenn die Werte _Maximale Breite_ und _Maximale Höhe_ in der Konfiguration geändert werden, werden alle vorhandenen optimierten Bilder aktualisiert, die zuvor eingefügt wurden.

Für die Bildoptimierung der Mediensammlung ist es erforderlich, dass die Verbraucher der `media.gallery.renditions.update`-Warteschlange ausgeführt werden, um optimierte Bilder neu zu generieren, wenn die Konfiguration geändert wird. Weitere [ finden Sie unter „Verwalten ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) Nachrichtenwarteschlangen _im_ Konfigurationshandbuch“.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

<!-- Last updated from includes: 2024-01-30 15:43:39 -->
