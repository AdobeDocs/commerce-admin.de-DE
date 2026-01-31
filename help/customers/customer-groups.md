---
title: Kundengruppen
description: Verwenden Sie Kundengruppen, um zu bestimmen, welche Rabatte Kunden zur Verfügung stehen, die einer Gruppe zugeordnet sind, und um die Steuerklasse zu bestimmen, die der Gruppe zugeordnet ist.
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: 17469d27128030b54fad6cf563a4b53f5f119eed
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Kundengruppen

Kundengruppen bestimmen, welche Rabatte verfügbar sind und welche Steuerklasse mit der Gruppe verknüpft ist. Die standardmäßigen Kundengruppen sind `General`, `Not Logged In` und `Wholesale`.

![Kundengruppen](assets/customer-groups.png){width="700" zoomable="yes"}

## Filtern der [!UICONTROL Customer Groups]

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Klicken Sie auf **[!UICONTROL Filters]**.

1. Geben Sie Kriterien für die Suche nach Gruppen ein, einschließlich eines Bereichs von IDs, Gruppe oder Steuerklasse.

   ![Filteroptionen](assets/groups-filters.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Apply Filters]**.

## Erstellen einer Kundengruppe

>[!NOTE]
>
>Admin-Benutzende, die keinen Zugriff auf alle Websites haben (denen eine Rolle mit einem „benutzerdefinierten“ [!UICONTROL Role Scope] zugewiesen wurde), können keine Kundengruppen erstellen, ändern oder löschen.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Klicken Sie auf **[!UICONTROL Add New Customer Group]**.

1. Geben Sie für [!DNL **Group Name]** einen eindeutigen Namen mit weniger als 32 Zeichen ein, um die Gruppe zu identifizieren.

1. Wählen Sie die **[!UICONTROL Tax Class]** aus, die für die Gruppe gilt.

   ![Gruppeninformationen](assets/group-information.png){width="600" zoomable="yes"}

1. Wählen Sie die **[!UICONTROL Excluded Website(s)]** aus, die Sie aus der Gruppe ausschließen möchten.

   >[!IMPORTANT]
   >
   >Das Ausschließen von Websites kann die Indizierungszeit für Produktpreise und Katalogregeln verringern, da ausgeschlossene Websites nicht indiziert sind. Wenn eine Kundengruppe mit einem hinzugefügten Website-Ausschluss gespeichert wird, werden die Produktpreis-, Katalogregel- und Katalogsuchindizes ungültig. Wenn Sie über viele Produkte, Websites und Kundengruppen verfügen, wird empfohlen, den Neuindizierungsprozess anzuhalten, bis Sie Websites aus den Kundengruppen ausgeschlossen haben.

   Standardmäßig sind keine Websites ausgeschlossen. Um mehrere Werte auszuwählen, halten Sie die _Strg_-Taste (PC) oder die _Befehlstaste_ (Mac) gedrückt und klicken Sie auf jede Option.

1. Klicken Sie abschließend auf **[!UICONTROL Save Customer Group]**.

## Bearbeiten einer Kundengruppe

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Öffnen Sie den Datensatz im Bearbeitungsmodus.

1. Nehmen Sie die erforderlichen Änderungen vor.

1. Klicken Sie abschließend auf **[!UICONTROL Save Customer Group]**.

## Zuweisen eines Kunden zu einer anderen Gruppe

>[!NOTE]
>
>Nach dem Ändern der Unternehmensgruppe muss sich ein Firmenbenutzer abmelden und in der Storefront anmelden, um neue Preise im Katalog zu sehen.
>Nachdem ein Kunde einer Firma zugewiesen wurde, ist die Kundengruppe schreibgeschützt und kann von einem Administrator nicht aktualisiert werden.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden in der Liste und aktivieren Sie das Kontrollkästchen in der ersten Spalte.

1. Legen Sie das **Aktionen**-Steuerelement auf `Assign a Customer Group` fest und wählen Sie die Gruppe aus dem Menü aus.

   ![Zuweisen einer Kundengruppe](assets/group-assign.png){width="600" zoomable="yes"}

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **OK**.

## Verknüpfen einer Kundengruppe mit bestimmten Rabatten

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Wählen Sie die Preisregel für den Warenkorb aus, mit der Sie eine Gruppe für den angewendeten Rabatt verknüpfen möchten, oder [ Sie eine Preisregel ](../merchandising-promotions/price-rules-catalog.md).

1. Wählen Sie die Kundengruppen aus, für die die Regel gilt.

   ![Kundengruppe mit bestimmten Rabatten](assets/group-discount.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
> Sie können auch Vorab-Preise verwenden, um Produktrabatte auf Kundengruppen anzuwenden. Siehe [Erweiterte Preise](../catalog/product-price-group.md).

## Löschen einer Kundengruppe

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Öffnen Sie den Datensatz im Bearbeitungsmodus.

1. Klicken Sie in der Schaltflächenleiste auf **[!UICONTROL Delete Customer Group]**.

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **OK**.

## Demo zu Kundengruppen

In dieser Demo erfahren Sie mehr über das Erstellen von Kundengruppen:

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12&learn=on)
