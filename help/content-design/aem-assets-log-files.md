---
title: Konfigurieren der Protokollrotation
description: Konfigurieren der Protokollrotation für die AEM Assets-Integration für Commerce.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: 'https://experienceleague.adobe.com/I6iWurcyEbPi3fJmBZAnvbPlZfOJiSS4yGR6j5xFsp4'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: ddbd0f6e-b569-5a04-8a70-55058777c373
    internal-label: CMS
  - id: 4ca54350-01cb-5b22-8966-5f2873dc6d90
    internal-label: Media
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%
---
# Konfigurieren von Experience Manager Assets

Die AEM Assets-Integration für Commerce stellt die folgenden Protokolldateien in Ihrer Commerce-Instanz bereit:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Bitten Sie Ihren Systemadministrator, den Drehplan für die Protokolldateien auf diese Protokolle zu überprüfen, um zu verhindern, dass sie zu groß werden. In einigen Umgebungen werden die Protokolldateien automatisch rotiert, in anderen müssen Sie die Protokollrotation jedoch manuell einrichten. Weitere Informationen finden Sie in den folgenden Themen:

- Bitten Sie bei lokalen Installationen von Adobe Commerce Ihren Systemadministrator, eine [ einzurichten](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/next-steps/configuration#server-settings).
- Informationen zu Adobe Commerce in Cloud-Infrastrukturprojekten finden Sie unter [Protokolle anzeigen und verwalten](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/test/log-locations).

