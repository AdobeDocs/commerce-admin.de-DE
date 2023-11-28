---
title: Inhaltsseite übersetzen
description: Erfahren Sie, wie Sie eine übersetzte Version jeder Seite erstellen, die in der jeweiligen Store-Ansicht verfügbar ist.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Inhaltsseite übersetzen

Wenn Ihr Store mehrere Ansichten in verschiedenen [languages](../stores-purchase/store-localize.md)und Sie das Gebietsschema für jede Ansicht auf eine andere Sprache festgelegt haben, ist das Ergebnis eine teilweise übersetzte Site. Der nächste Schritt besteht darin, eine übersetzte Version jeder Seite zu erstellen, die in der jeweiligen Store-Ansicht verfügbar ist. Die [!UICONTROL Store View] Spalte _[!UICONTROL Manage Pages]_zeigt jede Ansicht an, die eine übersetzte Version der Seite hat.

Um eine Inhaltsseite zu übersetzen, müssen Sie eine andere Seite erstellen, die über denselben URL-Schlüssel wie das Original verfügt, aber der spezifischen Store-Ansicht zugewiesen ist. Aktualisieren Sie dann die Seite für die jeweilige Ansicht mit dem übersetzten Text. Das folgende Beispiel zeigt, wie eine übersetzte Version der _Über uns_ -Seite für die spanische Store-Ansicht.

## Schritt 1: Kopieren Sie den URL-Schlüssel für die zu übersetzende Seite

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie im Raster nach der zu übersetzenden Seite und öffnen Sie sie in _edit_ -Modus.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Optimization]** und kopieren Sie die **[!UICONTROL URL Key]** in die Zwischenablage.

1. So kehren Sie zur _[!UICONTROL Pages]_Raster, klicken **[!UICONTROL Back]**in der oberen Schaltflächenleiste.

## Schritt 2: Hinzufügen einer Seite für den übersetzten Inhalt

1. Klicken **[!UICONTROL Add New Page]**.

1. Übersetzte Sprache eingeben **[!UICONTROL Page Title]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Content]** und füllen Sie den übersetzten Text für die Seite aus.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Optimization]** und führen Sie folgende Schritte aus:

   - Fügen Sie die **[!UICONTROL URL Key]** von der Originalseite kopiert wurde.

   - Geben Sie den übersetzten Text für die **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]**, und **[!UICONTROL Meta Description]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Page in Websites]** Abschnitt und Satz **[!UICONTROL Store View]** in die Store-Ansicht, in der die Seite verfügbar sein soll.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Design]** und legen Sie die Spalte fest. **[!UICONTROL Layout]** der Seite.

1. Klicken **[!UICONTROL Save]**.

1. Wenn Sie dazu aufgefordert werden, aktualisieren Sie alle ungültigen [Caches](../systems/cache-management.md).

## Schritt 3: Überprüfen der Übersetzung

Um die Übersetzung zu überprüfen, gehen Sie zur Storefront und verwenden Sie die Sprachauswahl, um die Store-Ansicht zu ändern.

Beachten Sie, dass auf der Seite noch einige Elemente übersetzt werden müssen, einschließlich der Fußzeilenlinks des Unternehmens [block](block-add.md), die [Willkommensnachricht](../getting-started/storefront-branding.md#change-the-welcome-message), und [Produktinformationen](../stores-purchase/store-localize.md#localize-products).
