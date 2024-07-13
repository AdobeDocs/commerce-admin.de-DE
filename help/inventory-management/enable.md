---
title: "Enable [!DNL Inventory Management]"
description: Erfahren Sie, wie Sie [!DNL Inventory Management] auf globaler Store- oder Produktebene aktivieren.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Inventory Management] aktivieren

Um Ihren Produktbestand zu verwalten, aktivieren Sie [!DNL Inventory Management] auf der globalen Store- oder Produktebene. Wenn die Option _Stock verwalten_ aktiviert ist, verfolgt [!DNL Inventory Management] die für die Site verfügbaren Produktmengen automatisch über konfigurierte Lager und Quellen. Jede Funktion und Option beginnt mit dem Tracking und Reporting, sobald sie aktiviert ist, ohne zusätzliche Konfiguration.

Ihr Geschäft läuft und Inventaraktualisierungen mit der Geschwindigkeit des Umsatzes. Wenn Kunden kaufen, erhalten Sie exakte, aktualisierte Informationen für verfügbare Lager pro Vertriebskanal und Quelle. Verfügbare Mengen werden pro Lager aktualisiert, wenn Kunden Produkte zum Warenkorb hinzufügen und Käufe abschließen und wenn und Sie Bestellungen verwalten, Sendungen erstellen und Erstattungen vornehmen. Ankunft von neuen oder übertragenen Lagerergänzungen in Ihren Quellen, sofort verfügbar für Online-Verkäufe. Aufstockungen werden bis zu bestimmten Schwellenwerten ohne unendliche Bestellungen oder zusätzliche Konfigurationen ausgeführt. Und Sie geben einen Teil- oder Vollversand aus einer oder mehreren Quellen mit Empfehlungen ab und geben Ihnen so die volle Kontrolle über die Auftragserfüllung und die Lagerbestände.

>[!NOTE]
>
>Standardmäßig ist [!DNL Inventory Management] bei der Installation oder Aktualisierung von [!DNL Commerce] aktiviert. Je nach Ihren geschäftlichen Anforderungen können Sie die getrackten [!DNL Inventory Management] innerhalb von [!DNL Commerce] aktivieren oder deaktivieren.

Wie diese Einstellung in Einzel- und Mehrfachquellen-Inventaren funktioniert:

- Um [!DNL Inventory Management] zu verwenden, aktivieren Sie _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] -Einstellungen auf Produktebene überschreiben die Speicherkonfiguration.

- Um Order Management oder Dienste von Drittanbietern (z. B. ERP) zu verwenden, deaktivieren Sie [!UICONTROL Manage Stock].

- Wenn die Konfiguration auf Produktebene den Systemstandard verwendet, überschreibt die Speicherkonfiguration.

Wenn [!DNL Inventory Management] aktiviert ist, sehen Sie Folgendes, um alle Einstellungen zu konfigurieren:

- [Konfigurieren globaler Optionen](global-options.md) - Einstellungen, die sich auf Ihren gesamten Katalog auswirken, werden als Systemstandardeinstellungen betrachtet.

- [Konfigurieren von Produktoptionen](product-options.md) - Einstellungen für ein bestimmtes Produkt, das globale Optionen außer Kraft setzt.

## [!DNL Inventory Management] aktivieren oder deaktivieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Catalog]** und wählen Sie **[!UICONTROL Inventory]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) _Produktspeicheroptionen_ und konfigurieren Sie:

   ![Optionen für Produktspeicher](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Um den Bestand zu verwalten und alle [!DNL Commerce]-Funktionen zu verwenden, setzen Sie **[!UICONTROL Manage Stock]** auf `Yes` (Standard).

   - Um [!DNL Inventory Management] zu deaktivieren, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** und legen Sie **[!UICONTROL Manage Stock]** auf `No` fest.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Verwalten von Lagern

Siehe [Globale Optionen konfigurieren](global-options.md).

## Verwalten von Lagern für ein Produkt

Siehe [Konfigurieren von Produktoptionen](product-options.md).
