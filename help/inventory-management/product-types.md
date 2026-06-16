---
title: Produktarten
description: Erfahren Sie [!DNL Inventory Management]  wie die Inventar- und Bestellverwaltung für alle Adobe Commerce- und Magento Open Source-Produktarten unterstützt.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 213
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
