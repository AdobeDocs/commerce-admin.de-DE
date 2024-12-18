---
title: Produktarten
description: Erfahren Sie [!DNL Inventory Management]  wie die Inventar- und Bestellverwaltung für alle Adobe Commerce- und Magento Open Source-Produkttypen unterstützt.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Produktarten

[!DNL Inventory Management] unterstützt die Bestands- und Bestellverwaltung für alle Produkttypen in Adobe Commerce und Magento Open Source: einfach, konfigurierbar, virtuell, herunterladbar, gebündelt und gruppiert. Optionen und Anforderungen können je nach Produkttyp für Quellen, Lager und Versand unterschiedlich sein.

- [Händler aus einer Hand](merchant-sourcing.md#single-source-merchants) Produkteinstellungen und -mengen erstellen und aktualisieren, ohne dass zusätzliche Aktualisierungen erforderlich sind. Alle erstellten und neu importierten Produkte werden automatisch dem Standard-Source und dem Standard-Stock zugewiesen, die Kunden sofort zur Verfügung stehen, wenn sie aktiviert und auf Lager sind.

- [Händler mit mehreren Quellen](merchant-sourcing.md#multi-source-merchants) Weisen Sie während oder nach der Produkterstellung Quellen, Mengen pro Quelle und Einstellungen zu. [!DNL Commerce] weist alle neu importierten Produkte der Standard-Source zu, sodass zusätzliche Bearbeitungen für die Zuordnung von Quellen und Mengen erforderlich sind.

| Produkttyp | Auswahlalgorithmus für Versand und Source |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Unterstützt SSA-Empfehlungen und -Überschreibungen beim Versand. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Unterstützt SSA-Empfehlungen und -Überschreibungen beim Versand. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Verwendet immer die SSA-Empfehlung. Das System führt den Algorithmus implizit aus, wenn es Rechnungen erstellt, und verwendet immer die vorgeschlagenen Ergebnisse.<br/>Sie können diese Ergebnisse nicht anpassen. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Verwendet immer die SSA-Empfehlung. Das System führt den Algorithmus implizit aus, wenn es Rechnungen erstellt, und verwendet immer die vorgeschlagenen Ergebnisse. <br/>Sie können diese Ergebnisse nicht anpassen. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Unterstützt SSA-Empfehlungen und -Überschreibungen beim Versand. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Unterstützt SSA-Empfehlungen und -Überschreibungen beim Versand. |
