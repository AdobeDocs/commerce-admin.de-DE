---
title: "Aktivieren [!DNL Inventory Management]"
description: Erfahren Sie, wie Sie [!DNL Inventory Management] auf globaler Store- oder Produktebene.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Aktivieren [!DNL Inventory Management]

Um Ihr Produktinventar zu verwalten, aktivieren Sie [!DNL Inventory Management] auf globaler Store- oder Produktebene. Wenn die Variable _Verwalten von Lagern_ -Option aktiviert ist, [!DNL Inventory Management] verfolgt automatisch die für die Site verfügbaren Produktmengen über konfigurierte Lager und Quellen. Jede Funktion und Option beginnt mit dem Tracking und Reporting, sobald sie aktiviert ist, ohne zusätzliche Konfiguration.

Ihr Geschäft läuft und Inventaraktualisierungen mit der Geschwindigkeit des Umsatzes. Wenn Kunden kaufen, erhalten Sie exakte, aktualisierte Informationen für verfügbare Lager pro Vertriebskanal und Quelle. Verfügbare Mengen werden pro Lager aktualisiert, wenn Kunden Produkte zum Warenkorb hinzufügen und Käufe abschließen und wenn und Sie Bestellungen verwalten, Sendungen erstellen und Erstattungen vornehmen. Ankunft von neuen oder übertragenen Lagerergänzungen in Ihren Quellen, sofort verfügbar für Online-Verkäufe. Aufstockungen werden bis zu bestimmten Schwellenwerten ohne unendliche Bestellungen oder zusätzliche Konfigurationen ausgeführt. Und Sie geben einen Teil- oder Vollversand aus einer oder mehreren Quellen mit Empfehlungen ab und geben Ihnen so die volle Kontrolle über die Auftragserfüllung und die Lagerbestände.

>[!NOTE]
>
>Standardmäßig ist [!DNL Inventory Management] wird bei der Installation oder Aktualisierung aktiviert [!DNL Commerce]. Je nach Ihren geschäftlichen Anforderungen können Sie die getrackten [!DNL Inventory Management] Innerhalb [!DNL Commerce].

Wie diese Einstellung in Einzel- und Mehrfachquellen-Inventaren funktioniert:

- Verwendung [!DNL Inventory Management], aktivieren _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] -Einstellungen auf der Produktebene überschreiben die Store-Konfiguration.

- Um die Auftragsverwaltung oder Dienste von Drittanbietern (wie ERP) zu verwenden, deaktivieren Sie [!UICONTROL Manage Stock].

- Wenn die Konfiguration auf Produktebene den Systemstandard verwendet, überschreibt die Speicherkonfiguration.

Mit [!DNL Inventory Management] aktiviert ist, sehen Sie Folgendes, um alle Einstellungen zu konfigurieren:

- [Konfigurieren globaler Optionen](global-options.md) - Einstellungen, die sich auf Ihren gesamten Katalog auswirken, werden als Systemstandardeinstellungen betrachtet.

- [Konfigurieren von Produktoptionen](product-options.md) - Einstellungen für ein bestimmtes Produkt, das globale Optionen außer Kraft setzt.

## Aktivieren oder Deaktivieren [!DNL Inventory Management]

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Inventory]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) _Optionen für Produktspeicher_ und konfigurieren Sie:

   ![Optionen für Produktspeicher](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Verwalten des Bestands und Verwenden aller [!DNL Commerce] Funktionen, Satz **[!UICONTROL Manage Stock]** nach `Yes` (Standard).

   - So deaktivieren Sie [!DNL Inventory Management], deaktivieren Sie die **[!UICONTROL Use system value]** Kontrollkästchen und festlegen **[!UICONTROL Manage Stock]** nach `No`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Verwalten von Lagern

Siehe [Globale Optionen konfigurieren](global-options.md).

## Verwalten von Lagern für ein Produkt

Siehe [Konfigurieren von Produktoptionen](product-options.md).
