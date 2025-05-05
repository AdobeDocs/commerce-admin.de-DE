---
title: Installieren, Aktualisieren und Entfernen [!DNL Inventory Management]
description: Erfahren Sie, wie Sie das  [!DNL Inventory Management] -Paket verwalten.
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Installieren, Aktualisieren und Entfernen von [!DNL Inventory Management]

[!DNL Inventory Management] Module bieten alle Inventarfunktionen und Optionen für Einzelhändler und Händler mit mehreren Quellen, um Produktmengen und Lagerbestände für Vertriebskanäle zu verwalten. Diese Funktionen sind in Version 2.4.x von Adobe Commerce und Magento Open Source verfügbar.

Diese Funktionen und Erweiterungen wurden im Rahmen des [Inventory-Projekts](https://github.com/magento/inventory) im Rahmen des Magento Open Source Community Engineering-Programms entwickelt.

[!DNL Inventory Management] wird in den Versionen 2.3.x und 2.4.x von Adobe Commerce und Magento Open Source installiert, wobei alle Funktionen standardmäßig aktiviert sind. Zur Aktivierung dieser Inventarfunktionen sind keine zusätzlichen Schritte erforderlich. Bei Upgrades von Version 2.1.x oder 2.2.x sind möglicherweise zusätzliche Schritte erforderlich. Siehe [Inventory management aktualisieren](#upgrade-inventory-management).

Die Installation gemäß [Schnellstart-Installation vor Ort](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"} wird empfohlen. Installieren Sie mit einem Metapaket, um alle [!DNL Inventory Management] Module zu erhalten.

Die folgende Zeile im `composer.json`-Metapaket installiert [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Eine Liste [!DNL Inventory Management] Metapaket-Versionen finden Sie in den [Versionshinweisen](release-notes.md).

Der [!DNL Inventory Management]-Installationsprozess fügt alle Module zur `<Magento_installation_directory>/app/etc/config.php` hinzu. Ein `1` gibt an, dass das entsprechende Modul aktiviert ist. Die folgende Liste von Modulen wird hinzugefügt:

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## [!DNL Inventory Management] aktivieren

Nach der Installation, dem Upgrade oder der Aktualisierung ist die Option _[!UICONTROL Manage Stock]_in Admin standardmäßig aktiviert. Diese Option ermöglicht die Inventarverfolgung und -verwaltung, hat jedoch keine Auswirkungen auf den Modulstatus. Informationen zum Deaktivieren von Modulen finden Sie im nächsten Abschnitt.

Weitere Informationen zu Konfigurationen finden Sie unter [Konfigurieren von Inventory management](configuration.md).

## Inventory management deaktivieren

>[!IMPORTANT]
>
>Es wird dringend empfohlen, die standardmäßigen [!DNL Inventory Management]-Module zu verwenden. Das alternative [!DNL CatalogInventory]-Modul, das für Systeme mit deaktivierten [!DNL Inventory Management]-Modulen verwendet wird, wird jetzt nicht mehr unterstützt. Die Deaktivierung der [!DNL Inventory Management] kann zu einem instabilen System führen und verschiedene Probleme verursachen.

Sie können [!DNL Inventory Management] Module deaktivieren, um:

* Beschleunigen Sie den Upgrade-Prozess für Händler, die von 2.0.x, 2.1.x, 2.2.x oder 2.3.x auf 2.4.x migrieren.
* Verwenden Sie benutzerdefinierte oder Systemmodule für Inventar- und Bestellverwaltung von Drittanbietern.

Informationen zum Deaktivieren der [ Module finden ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) auf der Seite _Module aktivieren oder deaktivieren_ im Installationshandbuch.

Nach Abschluss des Vorgangs stellt das System eine Liste der Module und Werte in `<Magento_installation_directory>/app/etc/config.php` bereit, beginnend mit:

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>Wenn Sie die OMS-Connector-Module installiert haben, stellen Sie sicher, dass Sie das `Magento_InventoryMessageBus`-Modul, ein Connector-Modul, nicht deaktivieren. Es ist erforderlich, den Connector mit OMS zu verwenden.

## Inventory management entfernen

>[!IMPORTANT]
>
>Es wird dringend empfohlen, die standardmäßigen [!DNL Inventory Management]-Module zu verwenden. Das alternative [!DNL CatalogInventory]-Modul, das für Systeme mit entfernten [!DNL Inventory Management]-Modulen verwendet wird, wird jetzt nicht mehr unterstützt. Das Entfernen der [!DNL Inventory Management] kann zu einem instabilen System führen und verschiedene Probleme verursachen.

Wenn Sie die [!DNL Inventory Management] nicht verwenden möchten, können Sie diese Module entfernen (deinstallieren). Um alle Module über die Composer-Datei zu entfernen, fügen Sie Folgendes zu `composer.json` hinzu:

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

Wenn diese Änderung abgeschlossen ist, führen Sie die Composer-Installation aus, und diese Inventory management-Module werden automatisch entfernt.

## Inventory management aktualisieren

### Frühere [!DNL Commerce]

Beim Aktualisieren oder Aktualisieren einer bestehenden 2.1.x-, 2.2.x- oder 2.3.x-Installation auf Adobe Commerce oder Magento Open Source 2.4.x sind [!DNL Inventory Management]-Module standardmäßig deaktiviert. Diese Standardeinstellung ist eine Vorsichtsmaßnahme, um abwärtsinkompatible Upgrades zu verhindern und Order Management (OMS) besser zu unterstützen.

>[!NOTE]
>
>Order Management unterstützt [!DNL Inventory Management] nicht. Beim Upgrade werden [!DNL Inventory Management] Module deaktiviert, damit OMS und [!DNL Commerce] 2.3.x nahtlos funktionieren.


So aktivieren Sie [!DNL Inventory Management]:

1. Bearbeiten Sie die `<Commerce_installation_directory>/app/etc/config.php`.
1. Ändern Sie alle Inventarmodule von `0` zu `1`, um sie zu aktivieren.
1. Datenbank aktualisieren:

   ```bash
   bin/magento setup:upgrade
   ```

1. Cache leeren:

   ```bash
   bin/magento cache:clean
   ```

Es wird empfohlen, nach dem Upgrade die Befehle [Reservierungsinkonsistenzen](cli.md) zu verwenden. Beim Upgrade werden alle Ihre Produkte zum Standardbestand hinzugefügt. Wenn Sie ausstehende Bestellungen haben, aktualisieren die Befehle Ihre Verkaufsmenge und Reservierungen für Verkauf und Bestellabwicklung korrekt.

### Frühere [!DNL Inventory Management]

Führen Sie beim Upgrade von früheren Versionen von [!DNL Inventory Management] auf die neueste Version die normalen Upgrade-Schritte für Erweiterungen aus.

Aktualisieren Sie Ihre Metapaket-Version, um die neueste Version zu erhalten:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

In den folgenden Handbüchern finden Sie weitere Informationen zu Commerce-Upgrades:

* [Aktualisierungshandbuch für Commerce](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [Module aktivieren oder deaktivieren](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
