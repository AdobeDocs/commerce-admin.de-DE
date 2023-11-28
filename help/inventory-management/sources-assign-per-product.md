---
title: Zuweisen von Inventarquellen pro Produkt
description: Erfahren Sie, wie Sie einem Produkt eine Lagerbestandsquelle zuweisen.
exl-id: 7e47be25-633e-4f5d-bb61-0d9e79b6dbad
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Zuweisen von Quellen pro Produkt

Vor der Änderung von Mengen und Einstellungen müssen Sie [sources](sources-manage.md) zu den Erzeugnissen.

{{$include /help/_includes/unassign-source.md}}

## Zuweisen von Quellen zu einem Produkt

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie ein Produkt in _Bearbeiten_ -Modus.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Sources]** Abschnitt.

   In diesem Abschnitt können Sie die Quelle ändern, Lagerbestandsmengen aktualisieren und vieles mehr.

   >[!NOTE]
   >
   >Derzeit unterstützen nur einfache, konfigurierbare, virtuelle, herunterladbare und gruppierte Produkte mehrere Quellen. Bundle-Produkte können nur mit der Standardquelle und dem Standardbestand erstellt und verwaltet werden.

   ![Abschnitt &quot;Produktquellen&quot;](assets/inventory-product-sources-before.png){width="600" zoomable="yes"}

1. Um eine Quelle hinzuzufügen, klicken Sie auf **[!UICONTROL Assign Sources]**.

1. Im _[!UICONTROL Assign Sources]_aktivieren Sie das Kontrollkästchen neben allen Quellen, die Sie für das Produkt zuweisen möchten.

   ![Produkt - Quellen zuweisen](assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. Klicks **[!UICONTROL Done]** , um die Quellen hinzuzufügen.

1. Führen Sie einen der folgenden Schritte aus, um zu speichern:

   - Klicken **[!UICONTROL Save]**.
   - Im _[!UICONTROL Save]_ (![Menüpfeil](../assets/icon-menu-down-arrow-red.png)), wählen Sie **[!UICONTROL Save & Close]**.

Aktualisieren Sie nach dem Zuweisen von Quellen die [Lagermenge](quantities-assign-per-product.md) für jede Produktquelle.
