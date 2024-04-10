---
title: Kundengruppen
description: Verwenden Sie Kundengruppen , um zu bestimmen, welche Rabatte Kunden zur Verfügung stehen, die einer Gruppe zugeordnet sind, und um die Steuerklasse zu bestimmen, die der Gruppe zugeordnet ist.
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: 805ceef0fe67c1ed2a4fbd06e6f02d9ad252ecef
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Kundengruppen

Kundengruppen bestimmen, welche Rabatte verfügbar sind und welche Steuerklasse mit der Gruppe verknüpft ist. Die Standardkundengruppen sind `General`, `Not Logged In`, und `Wholesale`.

![Kundengruppen](assets/customer-groups.png){width="700" zoomable="yes"}

## Filtern Sie die [!UICONTROL Customer Groups] auflisten

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Klick **[!UICONTROL Filters]**.

1. Geben Sie Kriterien für die Suche nach Gruppen ein, einschließlich eines Bereichs von IDs, Gruppe oder Steuerklasse.

   ![Filteroptionen](assets/groups-filters.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Apply Filters]**.

## Erstellen einer Kundengruppe

>[!NOTE]
>
>Admin-Benutzende, die keinen Zugriff auf alle Websites haben (ihnen wurde eine Rolle mit dem Status „Benutzerdefiniert“ zugewiesen) [!UICONTROL Role Scope]) kann keine Kundengruppen erstellen, ändern oder löschen.

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Klick **[!UICONTROL Add New Customer Group]**.

1. für [!DNL **Group Name]Geben Sie ** einen eindeutigen Namen mit weniger als 32 Zeichen ein, um die Gruppe zu identifizieren.

1. Wählen Sie die **[!UICONTROL Tax Class]** Das gilt für die Gruppe.

   ![Gruppeninformationen](assets/group-information.png){width="600" zoomable="yes"}

1. Wählen Sie die **[!UICONTROL Excluded Website(s)]** die Sie aus der Gruppe ausschließen möchten.

   >[!IMPORTANT]
   >
   >Das Ausschließen von Websites kann den Produktpreis und die Indizierungszeit für Katalogregeln verringern, da ausgeschlossene Websites nicht indiziert werden. Wenn eine Kundengruppe mit einem hinzugefügten Website-Ausschluss gespeichert wird, werden die Produktpreis-, Katalogregel- und Katalogsuchindizes ungültig. Wenn Sie über viele Produkte, Websites und Kundengruppen verfügen, wird empfohlen, den Neuindizierungsprozess anzuhalten, bis Sie Websites aus den Kundengruppen ausgeschlossen haben.

   Standardmäßig sind keine Websites ausgeschlossen. Um mehrere Werte auszuwählen, halten Sie die Taste gedrückt. _Strg_ -Taste (PC) oder _Befehl_ Drücken Sie die Taste (Mac) und klicken Sie auf die einzelnen Optionen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Customer Group]**.

## Bearbeiten einer Kundengruppe

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Öffnen Sie den Datensatz im Bearbeitungsmodus.

1. Nehmen Sie die erforderlichen Änderungen vor.

1. Klicken Sie abschließend auf **[!UICONTROL Save Customer Group]**.

## Zuweisen eines Kunden zu einer anderen Gruppe

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden in der Liste und aktivieren Sie das Kontrollkästchen in der ersten Spalte.

1. Legen Sie die **Aktionen** steuern auf `Assign a Customer Group` und wählen Sie die Gruppe aus dem Menü aus.

   ![Zuweisen einer Kundengruppe](assets/group-assign.png){width="600" zoomable="yes"}

1. Klicken Sie nach Aufforderung zur Bestätigung auf **OK**.

## Verknüpfen einer Kundengruppe mit bestimmten Rabatten

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Wählen Sie die Warenkorb-Preisregel aus, mit der Sie eine Gruppe für den angewendeten Rabatt verknüpfen möchten, oder [Erstellen einer Preisregel](../merchandising-promotions/price-rules-catalog.md).

1. Wählen Sie die Kundengruppen aus, für die die Regel gilt.

   ![Kundengruppe zu bestimmten Rabatten](assets/group-discount.png){width="600" zoomable="yes"}

1. Klick **[!UICONTROL Save]**.

>[!NOTE]
>
> Sie können auch Vorabpreise verwenden, um Produktrabatte auf Kundengruppen anzuwenden. Siehe [Erweiterte Preise](../catalog/product-price-group.md).

## Löschen einer Kundengruppe

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Öffnen Sie den Datensatz im Bearbeitungsmodus.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Delete Customer Group]**.

1. Klicken Sie nach Aufforderung zur Bestätigung auf **OK**.

## Demo zu Kundengruppen

In dieser Demo erfahren Sie, wie Sie Kundengruppen erstellen:

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12)
