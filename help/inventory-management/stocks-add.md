---
title: Hinzufügen eines Inventartracks
description: Erfahren Sie, wie Sie Verkaufskanäle (Websites) mit einer Lager- und Zuordnungsquelle versehen und so eine direkte Verknüpfung zu Verkaufsmengen und Produktinventaren herstellen können.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Hinzufügen eines Lagers

Stocks ordnen Ihre Quellen den Verkaufskanälen (oder Websites) zu und stellen so einen direkten Link zu Verkaufsmengen und Produktinventaren dar.

Beim Erstellen eines benutzerdefinierten Lagers weisen Sie Websites und Quellen zu. Quellen können aktivierte und deaktivierte Quellen enthalten. Sie können beispielsweise ein Lager zu Ihrem Lager hinzufügen, indem Sie den Speicherort für die Verwaltung des Bestands vorbereiten und Sendungen abschließen.

Nach dem Hinzufügen von Quellen müssen Sie die Reihenfolge der Quellen von oben (erste) nach unten (letzte) priorisieren. Diese Bestellung wirkt sich auf Empfehlungen während des Bestellversands aus.

![Neuer Stock](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Lagerbestand hinzufügen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Klicken Sie auf **[!UICONTROL Add New Stock]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL General]** und geben Sie einen eindeutigen **[!UICONTROL Name]** ein, um den neuen Bestand zu identifizieren.

   ![Allgemeine Aktienoptionen](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Sales Channels]** und wählen Sie die **[!UICONTROL Websites]** aus, wo dieser Bestand verfügbar ist.

   Halten Sie bei einer Multisite-Installation die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Website.

   >[!NOTE]
   >
   >Wenn Sie eine Website oder einen Vertriebskanal auswählen, die einem anderen Lager zugewiesen ist, wird die Zuweisung von dieser Ressource aufgehoben. Alle Sales Channel, die keinem benutzerdefinierten Lager zugewiesen sind, werden dem Standardbestand zugewiesen.

   ![Optionen für Sales Channel für Lager](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Sources]** und führen Sie für alle anderen Lager als den Standard Folgendes aus:

   - Klicken Sie auf **[!UICONTROL Assign Sources]**.

   ![Zugewiesene Quellen](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Aktivieren Sie die Kontrollkästchen für alle Quellen, die Sie dem Lager zuweisen möchten.

   >[!IMPORTANT]
   >
   >Wenn Sie dieselbe Quelle mehreren Lagern zuweisen, könnte dies zu einem Überverkauf der Produkte führen, die dieser Quelle zugeordnet sind.

   - Klicken Sie auf **[!UICONTROL Done]**.

     Die hinzugefügten Quellen werden in Zugewiesene Quellen angezeigt.

     ![Zuweisen von Quellen zu Lager](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Verwenden Sie das Symbol ![Sortieren](assets/icon-sort.png) , um die Quellen per Drag-and-Drop von oben (erste) nach unten (letzte) in eine Priorität zu ziehen.

   Die Quellbestellung ist bei Versandbestellungen wichtig.

   ![Beispiel für zugewiesene Quellen](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. Wählen Sie im Menü _[!UICONTROL Save]_(![Menüpfeil](../assets/icon-menu-down-arrow-red.png)) die Option **[!UICONTROL Save & Close]**.

## Feldbeschreibungen

| Feld | Beschreibung |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Name des Lagers. Beispiel: `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Definiert den [Umfang](../getting-started/websites-stores-views.md#scope-settings) des Lagers, indem der Bestand bestimmten Websites als _Verkaufskanäle_ zugewiesen wird. Wählen Sie eine oder mehrere Websites pro Lager aus. Jede Website kann nur einem Lager zugewiesen werden. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Weist diesem Bestand Inventarquellen zu. Benutzerdefinierte Quellen können nicht dem Standardbestand zugewiesen werden. |
| [!UICONTROL Assigned Sources] | Liste der zugewiesenen Quellen. Ziehen Sie die Quellen mit dem Symbol ![Sortieren](assets/icon-sort.png) in eine priorisierte Reihenfolge, um die Bestellung zu erfüllen und zu versenden.<br/><br/>**[!UICONTROL Code]**- Eindeutige Code-ID für die Quelle.<br/>**[!UICONTROL Name]** - Namensbeschreibung für die Quelle.<br/>**[!UICONTROL Unassign]**- Entfernt die zugewiesene Quelle mit dem ![Papierkorbsymbol](../assets/icon-delete-trashcan-solid.png) aus dem Lager. |
