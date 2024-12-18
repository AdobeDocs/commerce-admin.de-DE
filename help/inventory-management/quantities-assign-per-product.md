---
title: Lagermengen pro Produkt zuweisen
description: Erfahren Sie, wie Sie die Lagermengen für Ihr Produkt aktualisieren und die verfügbaren Lagerbestände verfolgen können.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Mengen pro Produkt zuweisen

Nachdem Sie [Quellen](sources-assign-per-product.md) hinzugefügt haben, aktualisieren Sie die Lagermengen für Ihr Produkt. Diese Werte verfolgen die verfügbaren Lagerbestände im Bestand.

Um das Inventar einer Bezugsquelle für Lieferungen auszublenden, ohne die Bezugsquelle zu entfernen, setzen Sie _[!UICONTROL Source Item Status]_auf `Out of Stock`. Die SSA- und Lieferoptionen greifen nur auf Quellen zu, die als `In Stock` mit verfügbarer Lagermenge aufgeführt sind.

Alle aktualisierten Mengen und Quellen werden im Produktraster angezeigt.

## Mengen aktualisieren

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Suchen und öffnen Sie ein Produkt im Bearbeitungsmodus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Sources]** .

1. Legen Sie **[!UICONTROL Source Item Status]** auf `In Stock` fest.

1. Um die Menge für den Lagerbestand zu aktualisieren, geben Sie einen Betrag für **[!UICONTROL Qty]** ein.

1. Führen Sie einen der folgenden Schritte aus, um eine Benachrichtigung für Lagermengen einzurichten:

   - Benutzerdefinierte Menge benachrichtigen - Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use Default]** und geben Sie einen Betrag in **[!UICONTROL Notify Qty]** ein.
   - Standardmenge benachrichtigen - Aktivieren Sie das Kontrollkästchen &quot;**[!UICONTROL Use Default]**&quot;. [!DNL Commerce] prüft und verwendet die -Einstellung in _[!UICONTROL Advanced Inventory]_oder der Konfiguration des globalen Speichers.

   ![Aktualisieren der Produktmengen pro Source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Führen Sie einen der folgenden Schritte aus, um zu speichern:

   - Klicken Sie auf **[!UICONTROL Save]**.

   - Wählen Sie im Menü **[!UICONTROL Save]** (![Menüpfeil](../assets/icon-menu-down-arrow-red.png)) die Option **[!UICONTROL Save & Close]**.


Das Produktraster wird mit einer Liste aller Quellen und der zugehörigen Mengen aktualisiert. Bewegen Sie bei Produkten mit mehr als fünf zugewiesenen Quellen den Mauszeiger über die Spalte _[!UICONTROL Quantity per Source]_, um die vollständige Liste anzuzeigen.

![Produktmengen pro Quelle](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
