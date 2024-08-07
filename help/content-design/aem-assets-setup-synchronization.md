---
title: Aktivieren der Asset-Synchronisierung
description: Erfahren Sie, wie Sie Ihre Adobe Commerce- und Experience Manager Assets-Projekte verbinden, um die Asset-Synchronisierung zwischen diesen beiden Systemen zu ermöglichen.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 508e9e1d23a4b6e70ada22e2a22c0dcd401393a9
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Aktivieren der Asset-Synchronisierung

>[!BEGINSHADEBOX]

**Voraussetzungen**

- [Konfigurieren AEM Experience Manager Assets zum Verwalten von Commerce-Assets](#aem-assets-configure-aem)
- [Installieren und konfigurieren Sie die AEM Assets-Integration für Commerce](#aem-assets-configure-commerce.md) , um die Erweiterung hinzuzufügen und die erforderlichen Anmeldeinformationen und Verbindungen für die Verwendung der Erweiterung zu generieren.

>[!ENDSHADEBOX]

Während dieses Aktivierungsprozesses registrieren Sie Ihre Mandantenkennung, indem Sie die Programm- und Umgebungs-ID für Ihre AEM Authoring-Umgebung angeben. Diese IDs identifizieren das AEM Assets-Projekt, mit dem Sie eine Verbindung herstellen, und stellen die Anmeldeinformationen bereit, um die Kommunikation und Workflows zwischen Commerce und AEM Assets zu aktivieren.

Nachdem Sie das AEM Asset-Projekt identifiziert haben, wählen Sie die passende Regel für die Synchronisierung von Assets zwischen Adobe Commerce und AEM Assets aus.

Die AEM Assets-Integration für Commerce unterstützt zwei Übereinstimmungsregeln für die Synchronisierung von Assets zwischen Adobe Commerce und AEM Assets.

- **Nach Produkt-SKU abgleichen**: Dies ist die standardmäßige Übereinstimmungsregel, die Assets auf Grundlage der Bestandseinheit (Stock Keeping Unit, SKU) des Produkts abgleicht. Die SKU ist eine eindeutige Kennung für jedes Produkt. Diese Regel stimmt die SKU in den Asset-Metadaten mit der Commerce-Produkt-SKU überein, um sicherzustellen, dass Assets mit den richtigen Produkten verknüpft sind.

- **Benutzerdefinierte Übereinstimmung**: Diese Übereinstimmungsregel dient für komplexere Szenarien oder spezifische Geschäftsanforderungen, die eine benutzerdefinierte Übereinstimmungslogik erfordern. Um diese Regel verwenden zu können, müssen Sie benutzerdefinierten Code in Adobe Developer App Builder implementieren, der definiert, wie Assets mit Produkten abgeglichen werden. Weitere Details werden bald folgen...

Verwenden Sie für das erstmalige Onboarding die standardmäßige `Match by product sku` -Regel. Bei Bedarf können Sie die passende Regel später ändern.

## Integration aktivieren

1. Rufen Sie die Projekt- und Umgebungs-ID für Ihre [AEM Assets-Authoring-Umgebung](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) ab.

   1. Öffnen Sie die AEM Sites-Konsole und wählen Sie **[!UICONTROL Assets]** aus.

   1. Kopieren und speichern Sie die Projekt- und Umgebungs-IDs aus der URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Öffnen Sie über Commerce Admin die AEM Assets-Integrationskonfiguration.

   1. Wählen Sie **[!UICONTROL Store]** > Konfiguration > **[!UICONTROL CATALOG]** > **[!UICONTROL Catalog]** aus.

   1. Erweitern Sie **[!UICONTROL Experience Manager Assets integration]**.

      ![AEM Assets-Integration aktivieren Sie die Integration](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Identifizieren Sie das Experience Manager Assets-Projekt, mit dem eine Verbindung hergestellt werden soll, indem Sie die Werte **[!UICONTROL Program ID]** und **[!UICONTROL Environment ID]** eingeben.

1. Fügen Sie die OAUTH-Anmeldeinformationen hinzu, um API-Anfragen zwischen Adobe Commerce und dem ARES-Dienst zu authentifizieren, indem Sie die Option &quot;**[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)**&quot;, z. B. &quot;`Assets integration`&quot;, auswählen.

1. Erlauben Sie Commerce, eingehende Aktualisierungen von AEM Assets zu akzeptieren, indem Sie **[!UICONTROL Enable integration]** auf `Yes` setzen.

   Nachdem Sie die Integration aktiviert haben, können Sie die Asset-Übereinstimmungsregel konfigurieren.

   ![AEM Assets-Integration: Auswahl der Asset-Übereinstimmungsregel](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Definieren Sie die passende Regel für die Asset-Synchronisierung.

   1. Wählen Sie **[!UICONTROL Match by product SKU]** aus.

   1. Fügen Sie den für Commerce-Produkt-SKUs definierten [AEM Assets-Metadatenfeldnamen](aem-assets-configure-aem.md#configure-metadata) im Feld **[!UICONTROL Match by product SKU attribute name]** hinzu, z. B. `commerce:skus`.

1. Wenden Sie die Konfiguration an und starten Sie den Synchronisierungsprozess durch Auswahl von **[!UICONTROL Save Config]**.
