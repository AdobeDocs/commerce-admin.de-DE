---
title: Lagerbestandsmengen pro Produkt zuweisen
description: Erfahren Sie, wie Sie die Lagerbestandsmengen für Ihr Produkt aktualisieren und die verfügbaren Lagermengen verfolgen können.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Mengen je Erzeugnis zuweisen

Nach dem Hinzufügen [sources](sources-assign-per-product.md), aktualisieren Sie die Lagerbestandsmengen für Ihr Produkt. Diese Werte verfolgen die verfügbaren Lagerbestände.

Um den Bestand einer Quelle vor Sendungen zu verbergen, ohne die Quelle zu entfernen, legen Sie _[!UICONTROL Source Item Status]_nach `Out of Stock`. Die SSA- und Versandoptionen greifen nur auf die Quellen zu, die als `In Stock` mit verfügbarer Lagerbestandsmenge.

Alle aktualisierten Mengen und Quellen werden im Produktraster angezeigt.

## Mengen aktualisieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Suchen und öffnen Sie ein Produkt im Bearbeitungsmodus.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Sources]** Abschnitt.

1. Satz **[!UICONTROL Source Item Status]** nach `In Stock`.

1. Um die Menge des Vorrats zu aktualisieren, geben Sie einen Betrag für **[!UICONTROL Qty]**.

1. Führen Sie einen der folgenden Schritte aus, um eine Meldung für die Lagerbestandsmengen festzulegen:

   - Benutzerdefinierte Menge benachrichtigen - Deaktivieren Sie die Option **[!UICONTROL Use Default]** aktivieren und einen Betrag eingeben in **[!UICONTROL Notify Qty]**.
   - Standardmenge benachrichtigen - Wählen Sie die **[!UICONTROL Use Default]** aktivieren. [!DNL Commerce] überprüft und verwendet die Einstellung in _[!UICONTROL Advanced Inventory]_oder globale Store-Konfiguration.

   ![Aktualisieren der Produktmengen pro Quelle](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Führen Sie einen der folgenden Schritte aus, um zu speichern:

   - Klicken **[!UICONTROL Save]**.

   - Im **[!UICONTROL Save]** (![Menüpfeil](../assets/icon-menu-down-arrow-red.png)), wählen Sie **[!UICONTROL Save & Close]**.


Das Produktraster wird mit einer Liste aller Quellen und der zugehörigen Mengen aktualisiert. Bewegen Sie bei Produkten mit mehr als fünf zugewiesenen Quellen den Mauszeiger über die _[!UICONTROL Quantity per Source]_-Spalte, um die vollständige Liste anzuzeigen.

![Erzeugnismengen je Quelle](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
