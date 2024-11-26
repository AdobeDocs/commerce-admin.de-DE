---
title: Aktivieren der Asset-Synchronisierung
description: Erfahren Sie, wie Sie Ihre Adobe Commerce- und Experience Manager Assets-Projekte verbinden, um die Asset-Synchronisierung zwischen diesen beiden Systemen zu ermöglichen.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e069f0a99ed9289b22cafe06fe2f787912cbba23
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Aktivieren der Asset-Synchronisierung

Während des Aktivierungsprozesses registrieren Sie die Mandantenkennung für das Projekt mit der Programm- und Umgebungs-ID für Ihre AEM Authoring-Umgebung. Diese IDs identifizieren das AEM Assets-Projekt, mit dem Sie eine Verbindung herstellen, und geben die Anmeldeinformationen an, um die Kommunikation zwischen den Commerce- und AEM Assets-Umgebungen zu ermöglichen.

Nachdem Sie das AEM Asset-Projekt identifiziert haben, wählen Sie die passende Regel zum Synchronisieren von Assets zwischen Adobe Commerce und AEM Assets aus.

- **[!UICONTROL Match by product SKU]** - Standardregel, die die SKU in den Asset-Metadaten mit der [Commerce-Produkt-SKU](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku) abgleicht, um sicherzustellen, dass Assets den richtigen Produkten zugeordnet sind.

- **[!UICONTROL Custom match]** - Übereinstimmende Regel für komplexere Szenarien oder spezifische Geschäftsanforderungen, für die eine benutzerdefinierte Übereinstimmungslogik erforderlich ist. Die Implementierung benutzerdefinierter Abgleiche erfordert die Entwicklung von benutzerdefiniertem Code in Adobe Developer App Builder, um zu definieren, wie Assets mit Produkten abgeglichen werden. Weitere Details werden bald folgen...

Verwenden Sie für das erstmalige Onboarding die standardmäßige Regel *Übereinstimmung mit Produkt-SKU* .

## Voraussetzungen

- [Konfigurieren AEM Experience Manager Assets zum Verwalten von Commerce-Assets](#aem-assets-configure-aem)
- [Installieren und konfigurieren Sie die AEM Assets-Integration für Commerce](#aem-assets-configure-commerce.md) , um die Erweiterung hinzuzufügen und die erforderlichen Anmeldeinformationen und Verbindungen für die Verwendung der Erweiterung zu generieren.

## Verbindung konfigurieren

1. Rufen Sie die Projekt- und Umgebungs-ID der [AEM Assets-Autorenumgebung](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) ab.

   1. Öffnen Sie die AEM Sites-Konsole und wählen Sie **[!UICONTROL Assets]** aus.

   1. Kopieren und speichern Sie die Projekt- und Umgebungs-IDs aus der URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Öffnen Sie über Commerce Admin die AEM Assets-Integrationskonfiguration.

   1. Gehen Sie zu **[!UICONTROL Store]** > Konfiguration > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![AEM Assets-Integration aktivieren Sie die Integration](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Geben Sie die AEM Assets-Umgebung **[!UICONTROL Program ID]** und **[!UICONTROL Environment ID]** ein.

1. Geben Sie **[!UICONTROL Asset Selector IMS Client ID] ein.

   Mit der [IMS-ID](../getting-started/adobe-ims-config.md) können Sie AEM Assets in den Seitenaufbau integrieren.

1. Wählen Sie [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)** für Authentifizierungsanfragen zwischen Commerce und dem Asset-Abgleichdienst aus.

1. Erlauben Sie Commerce, eingehende Aktualisierungen von AEM Assets zu akzeptieren, indem Sie **[!UICONTROL Integration enabled]** auf `Yes` setzen.

   Nachdem Sie die Integration aktiviert haben, konfigurieren Sie die Asset-Übereinstimmungsregel.

   ![AEM Assets-Integration: Auswahl der Asset-Übereinstimmungsregel](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Definieren Sie die passende Regel für die Asset-Synchronisierung.

   1. Wählen Sie **[!UICONTROL Match by product SKU]** aus.

   1. Fügen Sie den für Commerce-Produkt-SKUs definierten [AEM Assets-Metadatenfeldnamen](aem-assets-configure-aem.md#configure-metadata) im Feld **[!UICONTROL Match by product SKU attribute name]** hinzu, z. B. `commerce:skus`.

   ![AEM Assets-Integration: Auswahl der Asset-Übereinstimmungsregel](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Wählen Sie **[!UICONTROL Save Config]** aus, um Aktualisierungen anzuwenden und die Asset-Synchronisierung zu starten.
