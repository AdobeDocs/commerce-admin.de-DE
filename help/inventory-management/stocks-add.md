---
title: Hinzufügen eines Inventartracks
description: Erfahren Sie, wie Sie Verkaufskanäle (Websites) mit einer Lager- und Zuordnungsquelle versehen und so eine direkte Verknüpfung zu Verkaufsmengen und Produktinventaren herstellen können.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 1%

---

# Hinzufügen eines Lagers

Stocks ordnen Ihre Quellen den Verkaufskanälen (oder Websites) zu und stellen so einen direkten Link zu Verkaufsmengen und Produktinventaren dar.

Beim Erstellen eines benutzerdefinierten Lagers weisen Sie Websites und Quellen zu. Quellen können aktivierte und deaktivierte Quellen enthalten. Sie können beispielsweise ein Lager zu Ihrem Lager hinzufügen, indem Sie den Speicherort für die Verwaltung des Bestands vorbereiten und Sendungen abschließen.

Nach dem Hinzufügen von Quellen müssen Sie die Reihenfolge der Quellen von oben (erste) nach unten (letzte) priorisieren. Diese Bestellung wirkt sich auf Empfehlungen während des Bestellversands aus.

![Neuer Stock](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Lagerbestand hinzufügen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Klicken **[!UICONTROL Add New Stock]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL General]** und geben Sie einen eindeutigen **[!UICONTROL Name]** zur Identifizierung des neuen Bestands.

   ![Allgemeine Aktienoptionen](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Sales Channels]** und wählen Sie **[!UICONTROL Websites]** wo dieser Bestand verfügbar ist.

   Halten Sie bei einer Multisite-Installation die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Website.

   >[!NOTE]
   >
   >Wenn Sie eine Website oder einen Vertriebskanal auswählen, die einem anderen Lager zugewiesen ist, wird die Zuweisung von dieser Ressource aufgehoben. Alle Sales Channel, die keinem benutzerdefinierten Lager zugewiesen sind, werden dem Standardbestand zugewiesen.

   ![Sales Channel Optionen für Bestände](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Sources]** und führen Sie für alle anderen Lager als den Standard folgende Schritte aus:

   - Klicken **[!UICONTROL Assign Sources]**.

   ![Zugewiesene Quellen](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Aktivieren Sie die Kontrollkästchen für alle Quellen, die Sie dem Lager zuweisen möchten.

   >[!IMPORTANT]
   >
   >Wenn Sie dieselbe Quelle mehreren Lagern zuweisen, könnte dies zu einem Überverkauf der Produkte führen, die dieser Quelle zugeordnet sind.

   - Klicken **[!UICONTROL Done]**.

     Die hinzugefügten Quellen werden in Zugewiesene Quellen angezeigt.

     ![Zuweisen von Quellen zu Lagern](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Verwendung ![Symbol &quot;Sortieren&quot;](assets/icon-sort.png) , um die Quellen per Drag-and-Drop von oben (erste) nach unten (letzte) in eine Priorität zu ziehen.

   Die Quellbestellung ist bei Versandbestellungen wichtig.

   ![Beispiel für zugewiesene Quellen](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. Im _[!UICONTROL Save]_(![Menüpfeil](../assets/icon-menu-down-arrow-red.png)), wählen Sie **[!UICONTROL Save & Close]**.

## Feldbeschreibungen

| Feld | Beschreibung |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Name des Lagers. Beispiel: `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Definiert die [Umfang](../getting-started/websites-stores-views.md#scope-settings) des Bestands durch Zuweisung des Bestands zu bestimmten Websites als _Vertriebskanäle_. Wählen Sie eine oder mehrere Websites pro Lager aus. Jede Website kann nur einem Lager zugewiesen werden. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Weist diesem Bestand Inventarquellen zu. Benutzerdefinierte Quellen können nicht dem Standardbestand zugewiesen werden. |
| [!UICONTROL Assigned Sources] | Liste der zugewiesenen Quellen. Ziehen Sie die Quellen per Drag-and-Drop ![Symbol &quot;Sortieren&quot;](assets/icon-sort.png) in eine priorisierte Bestellung für die Auftragserfüllung und den Versand.<br/><br/>**[!UICONTROL Code]**- Eindeutige Code-ID für die Quelle.<br/>**[!UICONTROL Name]** - Namensbeschreibung für die Quelle.<br/>**[!UICONTROL Unassign]**- Entfernen Sie die zugewiesene Quelle aus dem Lager mit ![Papierkorbsymbol](../assets/icon-delete-trashcan-solid.png). |
