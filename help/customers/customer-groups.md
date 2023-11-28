---
title: Kundengruppen
description: Verwenden Sie Kundengruppen, um zu bestimmen, welche Rabatte für Kunden verfügbar sind, die einer Gruppe zugewiesen sind, und die mit der Gruppe verbundene Steuerklasse.
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Kundengruppen

Kundengruppen bestimmen, welche Rabatte verfügbar sind und welche Steuerklasse mit der Gruppe verbunden ist. Die standardmäßigen Kundengruppen sind `General`, `Not Logged In`, und `Wholesale`.

![Kundengruppen](assets/customer-groups.png){width="700" zoomable="yes"}

## Filtern Sie die [!UICONTROL Customer Groups] Liste

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Klicken **[!UICONTROL Filters]**.

1. Geben Sie Kriterien für die Suche nach Gruppen ein, einschließlich einer Reihe von IDs, Gruppen oder Steuerklassen.

   ![Filteroptionen](assets/groups-filters.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Apply Filters]**.

## Erstellen einer Kundengruppe

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Klicken **[!UICONTROL Add New Customer Group]**.

1. Für [!DNL **Group Name]** geben Sie einen eindeutigen Namen ein, der weniger als 32 Zeichen umfasst, um die Gruppe zu identifizieren.

1. Wählen Sie die **[!UICONTROL Tax Class]** die für die Gruppe gilt.

   ![Gruppeninformationen](assets/group-information.png){width="600" zoomable="yes"}

1. Wählen Sie die **[!UICONTROL Excluded Website(s)]** die Sie aus der Gruppe ausschließen möchten.

   >[!IMPORTANT]
   >
   >Das Ausschließen von Websites kann den Produktpreis und die Indexierungszeit für Katalogregeln verringern, da ausgeschlossene Websites nicht indiziert werden. Wenn eine Kundengruppe mit einem hinzugefügten Website-Ausschluss gespeichert wird, werden der Produktpreis, die Katalogregel und die Katalogsuchindizes invalidiert. Wenn Sie viele Produkte, Websites und Kundengruppen haben, wird empfohlen, den Neuindizierungsprozess so lange anzuhalten, bis Sie Websites aus den Kundengruppen ausgeschlossen haben.

   Standardmäßig sind keine Websites ausgeschlossen. Um mehrere Werte auszuwählen, halten Sie die _Strg_ Schlüssel (PC) oder _Befehl_ und klicken Sie auf die einzelnen Optionen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Customer Group]**.

## Bearbeiten einer Kundengruppe

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Öffnen Sie den Datensatz im Bearbeitungsmodus.

1. Nehmen Sie die erforderlichen Änderungen vor.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Customer Group]**.

## Einen Kunden einer anderen Gruppe zuweisen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden in der Liste und aktivieren Sie das Kontrollkästchen in der ersten Spalte.

1. Legen Sie die **Aktionen** Kontrolle an `Assign a Customer Group` und wählen Sie die Gruppe aus dem Menü aus.

   ![Zuweisen einer Kundengruppe](assets/group-assign.png){width="600" zoomable="yes"}

1. Klicken Sie bei Aufforderung zur Bestätigung auf **OK**.

## Kundengruppen spezifische Rabatte zuordnen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Wählen Sie die Preisregel für den Warenkorb aus, der eine Gruppe für den angewendeten Rabatt zugeordnet werden soll, oder [eine Preisregel erstellen](../merchandising-promotions/price-rules-catalog.md).

1. Wählen Sie die Kundengruppen aus, für die die Regel gilt.

   ![Kundengruppe zu bestimmten Rabatten](assets/group-discount.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save]**.

>[!NOTE]
>
> Sie können auch die Vorab-Preisgestaltung verwenden, um Produktrabatte auf Kundengruppen anzuwenden. Siehe [Erweiterte Preise](../catalog/product-price-group.md).

## Eine Kundengruppe löschen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Öffnen Sie den Datensatz im Bearbeitungsmodus.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Delete Customer Group]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **OK**.

## Demo zu Kundengruppen

In dieser Demo erfahren Sie mehr über die Erstellung von Kundengruppen:

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12)
