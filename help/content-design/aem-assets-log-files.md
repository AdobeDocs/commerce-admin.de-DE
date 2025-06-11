---
title: Konfigurieren der Protokollrotation
description: Konfigurieren der Protokollrotation für die AEM Assets-Integration für Commerce.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Konfigurieren von Experience Manager Assets

Die AEM Assets-Integration für Commerce stellt die folgenden Protokolldateien in Ihrer Commerce-Instanz bereit:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Bitten Sie Ihren Systemadministrator, den Drehplan für die Protokolldateien auf diese Protokolle zu überprüfen, um zu verhindern, dass sie zu groß werden. In einigen Umgebungen werden die Protokolldateien automatisch rotiert, in anderen müssen Sie die Protokollrotation jedoch manuell einrichten. Weitere Informationen finden Sie in den folgenden Themen:

- Bitten Sie bei lokalen Installationen von Adobe Commerce Ihren Systemadministrator, eine [ einzurichten](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=de#server-settings).
- Informationen zu Adobe Commerce in Cloud-Infrastrukturprojekten finden Sie unter [Protokolle anzeigen und verwalten](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html?lang=de).
