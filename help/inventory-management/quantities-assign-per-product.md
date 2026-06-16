---
title: Lagermengen pro Produkt zuweisen
description: Erfahren Sie, wie Sie die Lagermengen für Ihr Produkt aktualisieren und die verfügbaren Lagerbestände verfolgen können.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/0OBXyHUbsWVXmEnWEWd0CGcBNhci57w8HGtDCGCWuOk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 210
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
