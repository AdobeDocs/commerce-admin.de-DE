---
title: "Installieren, Aktualisieren und Entfernen [!DNL Inventory Management]"
description: Erfahren Sie, wie Sie das [!DNL Inventory Management] Metapaket verwalten.
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
source-git-commit: d6c81da4b4e0674d6699e9781921ccb2160b9983
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# Installieren, Aktualisieren und Entfernen von [!DNL Inventory Management]

[!DNL Inventory Management] -Module bieten alle Inventarfunktionen und -optionen für Einzelhändler und Händler aus mehreren Quellen, um Produktmengen und Lager für Vertriebskanäle zu verwalten. Diese Funktionen sind in den Versionen 2.4.x von Adobe Commerce und Magento Open Source verfügbar.

Diese Funktionen und Erweiterungen wurden im Rahmen des [Inventarprojekts](https://github.com/magento/inventory) durch das Magento Open Source Community Engineering-Programm entwickelt.

[!DNL Inventory Management] installiert in den Versionen 2.3.x und 2.4.x von Adobe Commerce und Magento Open Source, wobei alle Funktionen standardmäßig aktiviert sind. Für die Aktivierung dieser Bestandsfunktionen sind keine zusätzlichen Schritte erforderlich. Für Upgrades von v2.1.x oder 2.2.x sind möglicherweise zusätzliche Schritte erforderlich. Siehe [Aktualisieren von Inventory management](#upgrade-inventory-management).

Es wird empfohlen, die Installation gemäß [Schnellstart-Installation vor Ort](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"} durchzuführen. Installieren Sie mit einem Metapaket , um alle [!DNL Inventory Management] -Module zu empfangen.

Die folgende Zeile im `composer.json`-Metapaket installiert [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Eine Liste der [!DNL Inventory Management] Metapaket-Versionen finden Sie in den [Versionshinweisen](release-notes.md).

Der Installationsprozess [!DNL Inventory Management] fügt alle Module zur Datei `<Magento_installation_directory>/app/etc/config.php` hinzu. Ein `1` -Wert gibt an, dass das entsprechende Modul aktiviert ist. Die folgende Liste von Modulen wird hinzugefügt:

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

## Funktionen für [!DNL Inventory Management] aktivieren

Bei der Installation, Aktualisierung oder Aktualisierung ist die Option _[!UICONTROL Manage Stock]_im Admin standardmäßig aktiviert. Diese Option ermöglicht die Bestandsverfolgung und -verwaltung, wirkt sich jedoch nicht auf den Modulstatus aus. Informationen zum Deaktivieren von Modulen finden Sie im nächsten Abschnitt.

Weitere Informationen zu Konfigurationen finden Sie unter [Konfigurieren von Inventory management](configuration.md).

## Inventory management deaktivieren

>[!IMPORTANT]
>
>Die Verwendung der standardmäßigen [!DNL Inventory Management] -Module wird dringend empfohlen. Das alternative Modul [!DNL CatalogInventory] , das für Systeme mit deaktivierten [!DNL Inventory Management] -Modulen verwendet wird, ist jetzt veraltet. Das Deaktivieren der [!DNL Inventory Management] -Module kann zu einem instabilen System und verschiedenen Problemen führen.

Sie können [!DNL Inventory Management] -Module deaktivieren, um:

* Beschleunigen Sie die Aktualisierung für Händler, die von 2.0.x, 2.1.x, 2.2.x oder 2.3.x auf 2.4.x migrieren.
* Verwenden Sie benutzerdefinierte oder Drittanbieter-Inventar- und Auftragsverwaltungssystemmodule.

Informationen zum Deaktivieren der entsprechenden Module finden Sie auf der Seite [Module aktivieren oder deaktivieren](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) im _Installationshandbuch_ .

Nach Abschluss stellt das System eine Liste der Module und Werte in `<Magento_installation_directory>/app/etc/config.php` bereit, beginnend mit:

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>Wenn Sie die OMS Connector-Module installiert haben, stellen Sie sicher, dass Sie das `Magento_InventoryMessageBus`-Modul, ein Connector-Modul, nicht deaktivieren. Es ist erforderlich, den Connector mit OMS zu verwenden.

## Entfernen von Inventory management

>[!IMPORTANT]
>
>Die Verwendung der standardmäßigen [!DNL Inventory Management] -Module wird dringend empfohlen. Das alternative [!DNL CatalogInventory]-Modul, das für Systeme mit entfernten [!DNL Inventory Management] -Modulen verwendet wird, wird jetzt nicht mehr unterstützt. Das Entfernen der [!DNL Inventory Management] -Module kann zu einem instabilen System und verschiedenen Problemen führen.

Wenn Sie die Funktion [!DNL Inventory Management] nicht verwenden möchten, können Sie diese Module entfernen (deinstallieren). Um alle Module über die Composer-Datei zu entfernen, fügen Sie `composer.json` Folgendes hinzu:

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

Wenn diese Änderung abgeschlossen ist, führen Sie die Komponenteninstallation aus und entfernt diese Inventory management-Module automatisch.

## Inventory management aktualisieren

### Vorherige [!DNL Commerce] -Versionen

Beim Aktualisieren oder Aktualisieren einer vorhandenen 2.1.x, 2.2.x oder 2.3.x-Installation auf Adobe Commerce oder Magento Open Source 2.4.x sind die [!DNL Inventory Management] -Module standardmäßig deaktiviert. Diese Standardeinstellung ist eine Vorsichtsmaßnahme, um rückwärtskompatible Aktualisierungen zu verhindern und Order Management (OMS) besser zu unterstützen.

>[!NOTE]
>
>Order Management unterstützt [!DNL Inventory Management] nicht. Beim Aktualisieren werden die [!DNL Inventory Management] -Module deaktiviert, damit OMS und [!DNL Commerce] 2.3.x nahtlos funktionieren.


So aktivieren Sie [!DNL Inventory Management] -Module:

1. Bearbeiten Sie die Datei &quot;`<Commerce_installation_directory>/app/etc/config.php`&quot;.
1. Ändern Sie alle Inventarmodule von `0` in `1`, um sie zu aktivieren.
1. Datenbank aktualisieren:

   ```bash
   bin/magento setup:upgrade
   ```

1. Cache leeren:

   ```bash
   bin/magento cache:clean
   ```

Es wird empfohlen, die [Reservierungsinkonsistenzbefehle](cli.md) nach der Aktualisierung zu verwenden. Beim Upgrade werden alle Ihre Produkte dem Standardbestand hinzugefügt. Wenn Sie ausstehende Bestellungen haben, aktualisieren die Befehle Ihre Verkaufsmenge und Reservierungen für den Vertrieb und die Bestellabwicklung korrekt.

### Vorherige [!DNL Inventory Management] -Versionen

Führen Sie beim Upgrade von früheren Versionen von [!DNL Inventory Management] auf die neueste Version die normalen Schritte zum Erweiterungs-Upgrade aus.

Aktualisieren Sie für die neueste Version Ihres Metapakets:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Weitere Informationen zu Commerce-Upgrades finden Sie in den folgenden Handbüchern:

* [Commerce-Aktualisierungshandbuch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [Module aktivieren oder deaktivieren](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
