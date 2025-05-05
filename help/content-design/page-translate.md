---
title: Übersetzen von Inhaltsseiten
description: Erfahren Sie, wie Sie eine übersetzte Version jeder Seite erstellen, die in der jeweiligen Store-Ansicht verfügbar ist.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Übersetzen von Inhaltsseiten

Wenn Ihr Store mehrere Ansichten in verschiedenen [Sprachen](../stores-purchase/store-localize.md) hat und Sie das Gebietsschema für jede Ansicht auf eine andere Sprache festgelegt haben, ist das Ergebnis eine teilweise übersetzte Site. Der nächste Schritt besteht darin, eine übersetzte Version jeder Seite zu erstellen, die in der jeweiligen Store-Ansicht verfügbar ist. Die Spalte [!UICONTROL Store View] der _[!UICONTROL Manage Pages]_&#x200B;zeigt jede Ansicht an, die über eine übersetzte Version der Seite verfügt.

Um eine Inhaltsseite zu übersetzen, müssen Sie eine weitere Seite erstellen, die denselben URL-Schlüssel wie das Original hat, aber der bestimmten Store-Ansicht zugewiesen ist. Aktualisieren Sie dann die Seite für die spezifische Ansicht mit dem übersetzten Text. Das folgende Beispiel zeigt, wie Sie eine übersetzte Version der Seite _Über uns_ für die spanische Store-Ansicht erstellen.

## Schritt 1: URL-Schlüssel für die zu übersetzende Seite kopieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie im Raster die zu übersetzende Seite und öffnen Sie sie im _Bearbeiten_-Modus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Search Engine Optimization]** und kopieren Sie die **[!UICONTROL URL Key]** in die Zwischenablage.

1. Um zum _[!UICONTROL Pages]_&#x200B;Raster zurückzukehren, klicken Sie in der oberen Schaltflächenleiste auf **[!UICONTROL Back]**.

## Schritt 2: Hinzufügen einer Seite für die übersetzten Inhalte

1. Klicken Sie auf **[!UICONTROL Add New Page]**.

1. Geben Sie die übersetzten **[!UICONTROL Page Title]** ein.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Content]** und füllen Sie den übersetzten Text für die Seite aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Search Engine Optimization]** und führen Sie folgende Schritte aus:

   - Fügen Sie die **[!UICONTROL URL Key]** ein, die Sie von der Originalseite kopiert haben.

   - Geben Sie den übersetzten Text für **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]** und **[!UICONTROL Meta Description]** ein.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Page in Websites]** und legen Sie **[!UICONTROL Store View]** auf die Store-Ansicht fest, in der die Seite verfügbar sein soll.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Design]** und legen Sie die **[!UICONTROL Layout]** der Seite fest.

1. Klicken Sie auf **[!UICONTROL Save]**.

1. Aktualisieren Sie nach Aufforderung alle ungültigen [Caches](../systems/cache-management.md).

## Schritt 3: Überprüfen der Übersetzung

Um die Übersetzung zu überprüfen, gehen Sie zur Storefront und verwenden Sie die Sprachauswahl, um die Store-Ansicht zu ändern.

Beachten Sie, dass sich noch einige Elemente auf der Seite befinden, die übersetzt werden sollten, darunter die Fußzeilen-Links [Block](block-add.md), die [Begrüßungsnachricht](../getting-started/storefront-branding.md#change-the-welcome-message) und [Produktinformationen](../stores-purchase/store-localize.md#localize-products).
