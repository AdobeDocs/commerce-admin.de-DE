---
title: Produkttypen
description: Erfahren Sie mehr [!DNL Inventory Management] unterstützt die Inventar- und Bestellverwaltung für alle Adobe Commerce- und Magento Open Source-Produkttypen.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Produkttypen

[!DNL Inventory Management] unterstützt die Bestandsverwaltung und Bestellverwaltung für alle Produkttypen in Adobe Commerce und Magento Open Source: einfach, konfigurierbar, virtuell, herunterladbar, gebündelt und gruppiert. Die Optionen und Anforderungen können je nach Produkttyp für Quellen, Lager und Versand unterschiedlich sein.

- [Einzelquell-Händler](merchant-sourcing.md#single-source-merchants) Produkteinstellungen und -mengen erstellen und aktualisieren, ohne dass zusätzliche Updates erforderlich sind. Alle erstellten und neu importierten Produkte werden automatisch der Standardquelle und dem Standardbestand zugewiesen, die den Kunden sofort zur Verfügung stehen, wenn diese Option aktiviert ist, und auf Lager.

- [Händler mit mehreren Quellen](merchant-sourcing.md#multi-source-merchants) Zuteilung von Quellen, Mengen pro Quelle und Einstellungen während oder nach der Erstellung des Produkts. [!DNL Commerce] weist alle neu importierten Produkte der Standardquelle zu, was zusätzliche Änderungen zur Zuweisung von Quellen und Mengen erfordert.

| Produkttyp | Versandalgorithmus und Quellauswahlalgorithmus |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Unterstützt SSA-Empfehlungen und -Überschreibungen für den Versand. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Unterstützt SSA-Empfehlungen und -Überschreibungen für den Versand. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Verwendet immer die SSA-Empfehlung. Das System führt den Algorithmus implizit aus, wenn Rechnungen erstellt werden, und verwendet immer die vorgeschlagenen Ergebnisse.<br/>Sie können diese Ergebnisse nicht anpassen. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Verwendet immer die SSA-Empfehlung. Das System führt den Algorithmus implizit aus, wenn Rechnungen erstellt werden, und verwendet immer die vorgeschlagenen Ergebnisse. <br/>Sie können diese Ergebnisse nicht anpassen. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Unterstützt SSA-Empfehlungen und -Überschreibungen für den Versand. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Unterstützt SSA-Empfehlungen und -Überschreibungen für den Versand. |
