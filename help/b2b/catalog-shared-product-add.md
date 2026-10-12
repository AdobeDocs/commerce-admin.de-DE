---
title: Hinzufügen von Produkten zu einem freigegebenen Katalog
description: Erfahren Sie, wie Sie Produkte zu einem freigegebenen Katalog hinzufügen, entweder einzeln oder in Gruppen nach Kategorie.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
TQID: 'https://experienceleague.adobe.com/f-5xQDov-Q3tfYw8MBDQPinimUIUkGe-q2Nfzm8L9ps'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
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
source-wordcount: '402'
ht-degree: 0%
---
# Hinzufügen von Produkten zu einem freigegebenen Katalog

Produkte können einem freigegebenen Katalog entweder einzeln oder in Gruppen mit mehreren Produkten nach Kategorie hinzugefügt werden.

Die folgenden Anforderungen müssen erfüllt sein, damit ein komplexes Produkt (z. B. Bundle, Gruppiert oder Konfigurierbar) in der Storefront in einem freigegebenen Katalog sichtbar ist:

- Alle [zugehörigen Produkte](../catalog/product-configurations.md) und Optionen müssen demselben freigegebenen Katalog zugewiesen und im primären Katalog aktiviert sein.
- Für [konfigurierbare](../catalog/product-create-configurable.md) und [gruppierte](../catalog/product-create-grouped.md) Produkte sind nur die aktivierten zugehörigen Produkte sichtbar.
- Für ein [Bundle](../catalog/product-create-bundle.md)-Produkt müssen alle Optionen im freigegebenen Katalog enthalten sein.

  ![Produkte für Katalog auswählen](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Methode 1: Ein Produkt hinzufügen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wechseln Sie für das Produkt im Raster, das Sie hinzufügen möchten, zur Spalte _[!UICONTROL Action]_und klicken Sie auf **[!UICONTROL Edit]**.

1. Scrollen Sie nach unten, erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _[!UICONTROL Product in Shared Catalogs]_und führen Sie die folgenden Schritte aus:

   - Aktivieren Sie das Kontrollkästchen jedes freigegebenen Katalogs, in dem das Produkt angezeigt werden soll. Um alle Kataloge auszuwählen, klicken Sie auf **[!UICONTROL Select all]**.

     ![Produkt in freigegebenen Katalogen](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     Der Name jedes ausgewählten Katalogs wird im Feld _[!UICONTROL Shared Catalogs]_angezeigt.

     ![Freigegebene Kataloge zugewiesen](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Klicken Sie auf **[!UICONTROL Done]** , um die Einstellungen zu speichern.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Methode 2: Mehrere Produkte hinzufügen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Wechseln Sie für den freigegebenen Katalog im Raster zur Spalte _[!UICONTROL Action]_und wählen Sie **[!UICONTROL Set Pricing and Structure]**aus.

1. Führen Sie in der Kategoriestruktur einen der folgenden Schritte aus:

   - Um alle Produkte einzubeziehen, klicken Sie auf **[!UICONTROL Select all]** oder aktivieren Sie das Kontrollkästchen der übergeordneten Kategorie.
   - Um bestimmte Produktkategorien einzubeziehen, aktivieren Sie das Kontrollkästchen jeder Kategorie, die Sie einbeziehen möchten.
   - Um ein einzelnes Produkt ein- oder auszuschließen, aktivieren bzw. deaktivieren Sie das Kontrollkästchen des Produkts.

   Die Notation unter jeder Kategorie in der Baumstruktur zeigt die Anzahl der Produkte aus der Kategorie an, die derzeit im freigegebenen Katalog enthalten sind. Die Notation unter der [Stammkategorie](../catalog/category-root.md) zeigt die Gesamtzahl der Produkte aus allen Kategorien an, die derzeit für den freigegebenen Katalog ausgewählt sind.

1. Um Kategorieprodukte im Raster anzuzeigen, klicken Sie auf den Namen der Kategorie in der Baumstruktur.

   Wenn eine Kategorie ausgewählt wird, geschieht Folgendes:

   - Der Umschalter in der ersten Spalte des Rasters ist für jedes ausgewählte Produkt auf `On` festgelegt.
   - Wenn ein Produkt mehreren Kategorien zugewiesen ist und in einer dieser Kategorien weggelassen wird, bleibt es in den anderen Kategorien und über [Katalogsuche](../catalog/search.md) verfügbar.
   - Das System setzt [Kategorieberechtigungen](../catalog/category-permissions.md) für die ausgewählten Produkte automatisch auf `Allow`.
