---
title: Inhaltsseite übersetzen
description: Erfahren Sie, wie Sie eine übersetzte Version jeder Seite erstellen, die in der jeweiligen Store-Ansicht verfügbar ist.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Inhaltsseite übersetzen

Wenn Ihr Store mehrere Ansichten in verschiedenen [Sprachen](../stores-purchase/store-localize.md) hat und Sie das Gebietsschema für jede Ansicht auf eine andere Sprache festgelegt haben, ist das Ergebnis eine teilweise übersetzte Site. Der nächste Schritt besteht darin, eine übersetzte Version jeder Seite zu erstellen, die in der jeweiligen Store-Ansicht verfügbar ist. Die Spalte [!UICONTROL Store View] der Liste _[!UICONTROL Manage Pages]_zeigt jede Ansicht an, die eine übersetzte Version der Seite aufweist.

Um eine Inhaltsseite zu übersetzen, müssen Sie eine andere Seite erstellen, die über denselben URL-Schlüssel wie das Original verfügt, aber der spezifischen Store-Ansicht zugewiesen ist. Aktualisieren Sie dann die Seite für die jeweilige Ansicht mit dem übersetzten Text. Das folgende Beispiel zeigt, wie eine übersetzte Version der Seite _Über uns_ für die spanische Store-Ansicht erstellt wird.

## Schritt 1: Kopieren Sie den URL-Schlüssel für die zu übersetzende Seite

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie im Raster die zu übersetzende Seite und öffnen Sie sie im Modus _Bearbeiten_ .

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Search Engine Optimization]** und kopieren Sie die **[!UICONTROL URL Key]** in die Zwischenablage.

1. Um zum Raster _[!UICONTROL Pages]_zurückzukehren, klicken Sie in der oberen Schaltflächenleiste auf **[!UICONTROL Back]**.

## Schritt 2: Hinzufügen einer Seite für den übersetzten Inhalt

1. Klicken Sie auf **[!UICONTROL Add New Page]**.

1. Geben Sie die übersetzte **[!UICONTROL Page Title]** ein.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Content]** und füllen Sie den übersetzten Text für die Seite aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Search Engine Optimization]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   - Fügen Sie die **[!UICONTROL URL Key]** ein, die Sie von der Originalseite kopiert haben.

   - Geben Sie den übersetzten Text für die **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]** und **[!UICONTROL Meta Description]** ein.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Page in Websites]** und legen Sie **[!UICONTROL Store View]** auf die Store-Ansicht fest, in der die Seite verfügbar sein soll.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Design]** und legen Sie die Spalte **[!UICONTROL Layout]** der Seite fest.

1. Klicken Sie auf **[!UICONTROL Save]**.

1. Aktualisieren Sie bei Aufforderung alle ungültigen [Caches](../systems/cache-management.md).

## Schritt 3: Überprüfen der Übersetzung

Um die Übersetzung zu überprüfen, gehen Sie zur Storefront und verwenden Sie die Sprachauswahl, um die Store-Ansicht zu ändern.

Beachten Sie, dass auf der Seite noch einige Elemente übersetzt werden müssen, darunter die Fußzeilenlinks des Unternehmens [block](block-add.md), die [Willkommensnachricht](../getting-started/storefront-branding.md#change-the-welcome-message) und die [Produktinformationen](../stores-purchase/store-localize.md#localize-products).
