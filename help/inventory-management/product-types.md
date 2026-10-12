---
title: Produktarten
description: Erfahren Sie, wie [!DNL Inventory Management] die Inventar- und Bestellverwaltung für alle Adobe Commerce- und Magento Open Source-Produktarten unterstützt.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
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
source-wordcount: '214'
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
