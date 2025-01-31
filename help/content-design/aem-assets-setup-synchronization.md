---
title: Asset-Synchronisierung aktivieren
description: Erfahren Sie, wie Sie Ihre Adobe Commerce- und Experience Manager Assets-Projekte verbinden, um die Synchronisierung von Assets zwischen diesen beiden Systemen zu aktivieren.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e9b3ede8945de0a6ed0cdb02e5675d736764d3e4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Asset-Synchronisierung aktivieren

Während des Aktivierungsprozesses registrieren Sie die Mandanten-ID für das Projekt mithilfe der Programm- und Umgebungs-ID für Ihre AEM-Autorenumgebung. Diese IDs identifizieren das AEM Assets-Projekt, mit dem Sie eine Verbindung herstellen, und geben die Anmeldeinformationen an, um die Kommunikation zwischen der Commerce- und der AEM Assets-Umgebung zu ermöglichen.

Nachdem Sie das AEM Assets-Projekt identifiziert haben, wählen Sie die Zuordnungsregel für die Synchronisierung von Assets zwischen Adobe Commerce und AEM Assets aus.

- **[!UICONTROL Match by product SKU]** - Standardregel, die die SKU in den Asset-Metadaten mit der [Commerce-Produkt-SKU](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku) abgleicht, um sicherzustellen, dass Assets mit den richtigen Produkten verknüpft sind.

- **[!UICONTROL Custom match]** - Matching-Regel für komplexere Szenarien oder spezifische Geschäftsanforderungen, die eine benutzerdefinierte Matching-Logik erfordern. Für die Implementierung des benutzerdefinierten Abgleichs ist die Entwicklung von benutzerdefiniertem Code in Adobe Developer App Builder erforderlich, um zu definieren, wie Assets mit Produkten abgeglichen werden. Weitere Details folgen in Kürze…

Verwenden Sie für das Onboarding die Standardregel *Übereinstimmung nach Produkt-SKU*.

## Voraussetzungen

- [Konfigurieren von AEM Experience Manager Assets zum Verwalten von Commerce-Assets](#aem-assets-configure-aem)

- [Installieren und konfigurieren Sie die AEM Assets-Integration für Commerce](#aem-assets-configure-commerce.md), um die Erweiterung hinzuzufügen und die erforderlichen Anmeldeinformationen und Verbindungen zur Verwendung der Erweiterung zu generieren.

- Erstellen Sie ein Support-Ticket, um die Aktivierung für die AEM Assets-Integration anzufordern. Sie müssen **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** und **[!UICONTROL IMS Org ID]** angeben.

  >[!TIP]
  >
  > (Optional) Geben Sie die **[!UICONTROL Asset Selector IMS Client ID]** an, falls verfügbar.

## Konfigurieren der Verbindung

1. Rufen Sie die Projekt- und Umgebungs-ID der ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start)0}AEM Assets-Autorenumgebung ab.[

   1. Öffnen Sie die AEM Sites-Konsole und wählen Sie **[!UICONTROL Assets]** aus.

   1. Kopieren Sie die Projekt- und Umgebungs-IDs aus der URL und speichern Sie sie:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Öffnen Sie vom Commerce-Administrator aus die AEM Assets-Integrationskonfiguration.

   1. Wechseln Sie zu **[!UICONTROL Store]** > Konfiguration > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![AEM Assets-Integration aktivieren](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Program ID]** und **[!UICONTROL Environment ID]** der AEM Assets-Umgebung ein.

1. Geben Sie die **[!UICONTROL Asset Selector IMS Client ID]** ein, falls verfügbar.

   Die [IMS-ID](../getting-started/adobe-ims-config.md) wird vom [[!UICONTROL Assets Selector]](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/overview-asset-selector) benötigt, der Bilder für Kategorien und/oder [!DNL Page Builder] auswählt.

1. Wählen Sie die [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) für die Authentifizierung von Anfragen zwischen Commerce und dem Asset Matching-Service aus.

1. Zulassen, dass Commerce eingehende Updates von AEM Assets akzeptiert, indem **[!UICONTROL Integration enabled]** auf `Yes` gesetzt wird.

   Konfigurieren Sie nach der Aktivierung der Integration die Regel für den Asset-Abgleich .

   ![AEM Assets-Integration - Asset-Übereinstimmungsregel auswählen](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Definieren Sie die Zuordnungsregel für die Asset-Synchronisierung.

   1. Wählen Sie **[!UICONTROL Match by product SKU]** aus.

   1. Fügen Sie den [AEM Assets-Metadatenfeldnamen](aem-assets-configure-aem.md#configure-metadata) der für Commerce-Produkt-SKUs definiert ist, in das **[!UICONTROL Match by product SKU attribute name]** ein, `commerce:skus`. B.

   ![AEM Assets-Integration - Asset-Übereinstimmungsregel auswählen](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]** auswählen, um Aktualisierungen anzuwenden und die Synchronisierung der Assets zu starten
