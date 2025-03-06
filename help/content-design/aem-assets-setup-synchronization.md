---
title: Integration konfigurieren
description: Erfahren Sie, wie Sie Ihre Adobe Commerce- und Experience Manager Assets-Projekte verbinden, um die Synchronisierung von Assets zwischen diesen beiden Systemen zu aktivieren.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 3522c3d3d772be5278206c10d8e699c2c4cc31af
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Integration konfigurieren

Konfigurieren Sie die Integration, indem Sie Commerce mit der AEM Assets-Instanz verbinden und die entsprechende Strategie für die Synchronisierung von Assets auswählen.

Nachdem Sie das AEM Assets-Projekt identifiziert haben, wählen Sie die Zuordnungsregel für die Synchronisierung von Assets zwischen Adobe Commerce und AEM Assets aus.

- **[!UICONTROL Match by product SKU]** - Standardregel, die die SKU in den Asset-Metadaten mit der [Commerce-Produkt-SKU](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/glossary#sku) abgleicht, um sicherzustellen, dass Assets mit den richtigen Produkten verknüpft sind.

- **[!UICONTROL Custom match]** - Matching-Regel für komplexere Szenarien oder spezifische Geschäftsanforderungen, die eine benutzerdefinierte Matching-Logik erfordern. Für die Implementierung des benutzerdefinierten Abgleichs ist die Entwicklung von benutzerdefiniertem Code in Adobe Developer App Builder erforderlich, um zu definieren, wie Assets mit Produkten abgeglichen werden. Weitere Details folgen in Kürze…

Verwenden Sie für die Ersteinrichtung die Standardregel *Übereinstimmung nach Produkt-SKU*.

## Voraussetzungen

- [Installieren des AEM Assets-Pakets](aem-assets-configure-aem.md)

- [Installieren Sie Adobe Commerce-](aem-assets-configure-commerce.md), um die Erweiterung hinzuzufügen und die erforderlichen Anmeldeinformationen und Verbindungen zur Verwendung der Erweiterung zu generieren.

- Erstellen Sie ein Support-Ticket, um die Aktivierung für die Integration von AEM Assets für Commerce anzufordern. Fügen Sie im Ticket die **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** und **[!UICONTROL IMS Org ID]** für die AEM Assets-Authoring-Umgebung ein, mit der Sie eine Verbindung zu Commerce herstellen möchten.

  >[!TIP]
  >
  > (Optional) Geben Sie die **[!UICONTROL Asset Selector IMS Client ID]** an, falls verfügbar. Siehe [ImsAuthProps](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app) in der *AEM Assets-Selektor*-Dokumentation.

## Konfigurieren der Verbindung

1. Rufen Sie die Projekt- und Umgebungs-ID der ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start)0}AEM Assets-Autorenumgebung ab.[

   1. Öffnen Sie die AEM Sites-Konsole und wählen Sie **[!UICONTROL Assets]** aus.

   1. Kopieren Sie die Projekt- und Umgebungs-IDs aus der URL und speichern Sie sie:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`
1. Öffnen Sie vom Commerce-Administrator aus die AEM Assets-Integrationskonfiguration.

   1. Wechseln Sie zu **[!UICONTROL Store]** > Konfiguration > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![AEM Assets-Integration aktivieren](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Program ID]** und **[!UICONTROL Environment ID]** der AEM Assets-Umgebung ein.

   Bearbeiten Sie die Konfigurationswerte, indem Sie die Auswahl aus der *[!UICONTROL Use system value]* entfernen.

1. Geben Sie die **[!UICONTROL Asset Selector IMS Client ID]** ein, falls verfügbar.

   Die [Asset-Selektor-IMS](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props)Client-ID) wird vom [!UICONTROL Assets Selector] benötigt, einer AEM Assets-Funktion, mit der Benutzende visuelle Assets direkt in Commerce-Produktseiten einbetten können.

1. Wählen Sie die [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) für die Authentifizierung von Anfragen zwischen Commerce und dem Asset Matching-Service aus.

1. Legen Sie **[!UICONTROL Integration enabled]** auf `Yes` fest, damit Commerce eingehende Updates von AEM Assets annehmen kann.

   Nach der Aktivierung der Integration stehen zusätzliche Konfigurationsoptionen zur Verfügung, um Kriterien für die Asset-Zuordnung anzugeben.

1. Definieren Sie die Zuordnungsregel für die Asset-Synchronisierung.

   1. Wählen Sie **[!UICONTROL Match by product SKU]** oder **[!UICONTROL Custom match (Requires App Builder)]** aus.

   1. Fügen Sie den [AEM Assets-Metadatenfeldnamen](aem-assets-configure-aem.md#configure-metadata) der für Commerce-Produkt-SKUs definiert ist, in das **[!UICONTROL Match by product SKU attribute name]** ein, `commerce:skus`. B.

1. Wählen Sie **[!UICONTROL Save Config]** aus, um Aktualisierungen anzuwenden und die Synchronisierung von Assets zu starten.

   Durch die Konfigurationsaktualisierung wird der anfängliche Synchronisierungsprozess Trigger, sodass Commerce eingehende Aktualisierungen von AEM Assets annehmen kann. Die für die Synchronisierung erforderliche Zeit hängt vom Volumen der Assets und von bestimmten Konfigurationen ab. Die Integration nutzt automatisierte Prozesse, um die für die Synchronisierung erforderliche Zeit zu minimieren.

## Nächster Schritt

[Verwenden von AEM Assets mit Commerce](aem-assets-manage.md)
