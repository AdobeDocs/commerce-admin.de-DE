---
title: Seitenlayouts
description: Erfahren Sie mehr über die Seitenlayoutabschnitte und wie Sie Standardlayouts konfigurieren.
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---

# Seitenlayouts

Das Layout jeder Seite in Ihrem Store besteht aus verschiedenen Abschnitten oder Containern, die die Kopf-, Fußzeilen- und Inhaltsbereiche der Seite definieren. Je nach Layout kann jede Seite über eine, zwei, drei Spalten oder mehr verfügen. Sie können sich das Layout als _Bodenplan_ der Seite vorstellen und ein bestimmtes Layout zuweisen, das als Standard für CMS-, Produkt- und Kategorieseiten verwendet werden soll.

Auf der Seite schwebt der Inhaltsbaustein, um den verfügbaren Platz gemäß dem Abschnitt des [Seitenlayouts](layout-updates.md) zu füllen, in dem er angezeigt werden soll. Beachten Sie, dass sich der Inhalt des Hauptbereichs erweitert, wenn Sie das Layout von einem dreiseitigen in ein zweispaltiges Layout ändern. Beachten Sie außerdem, dass alle Blöcke, die mit der nicht verwendeten Seitenleiste verknüpft sind, scheinbar verschwinden. Wenn Sie jedoch das dreiseitige Layout wiederherstellen, werden die Blöcke wieder angezeigt. Dieser flüssige Ansatz (das &quot;_flüssige Layout_&quot;) ermöglicht es, das Seitenlayout zu ändern, ohne den Inhalt neu erstellen zu müssen. Wenn Sie die Arbeit mit einzelnen HTML-Seiten gewohnt sind, erfordert dieser modulare Ansatz, _Baustein_, eine andere Denkweise.

![Zweispaltige Standardspalte mit Layout der linken Balkenseite](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## Standardlayouts konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Web]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Default Layouts]** .

   ![Standard-Layouts](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. Wählen Sie die **[!UICONTROL Default Product Layout]** aus, die Sie für Produktseiten verwenden möchten.

   Diese Einstellung legt das Layout fest, das standardmäßig für Produktseiten verwendet wird.

   - `No layout updates` - Layoutaktualisierungen sind für Produktseiten nicht verfügbar.
   - `Empty` - Verwendet ein leeres Layout für Produktseiten.
   - `1 column` - Verwendet ein einspaltiges Layout für Produktseiten.
   - `2 columns with left bar` - Verwendet ein zweispaltiges Layout mit der Seitenleiste auf der linken Seite für Produktseiten.
   - `2 columns with right bar` - Verwendet ein zweispaltiges Layout mit der Seitenleiste auf der rechten Seite für Produktseiten.
   - `3 columns` - Verwendet ein dreiseitiges Layout mit Seitenleisten auf der linken und rechten Seite für Produktseiten.

   Wenn [Seitenaufbau](../page-builder/introduction.md) aktiviert ist, stehen zusätzliche Optionen für die volle Breite zur Verfügung. Anschließend können Sie mit den Inhaltstools des Seitenaufbaus das Layout für Ihre Produktseiten entwerfen.

   - `Page -- Full Width` - Verwendet das Layout _Seite - Vollbreite_ für Produktseiten.
   - `Category -- Full Width` - Verwendet das Layout _Kategorie - volle Breite_ für Produktseiten.
   - `Product -- Full Width` - (Empfohlen) Verwendet das Layout _Produkt - Vollständige Breite_ für Produktseiten.

1. Wählen Sie die **[!UICONTROL Default Category Layout]** aus, die Sie für Kategorieseiten verwenden möchten.

   Diese Einstellung bestimmt das Layout, das standardmäßig für Kategorieseiten verwendet wird.

   - `No layout updates` - Layoutaktualisierungen sind nicht für Kategorieseiten verfügbar.
   - `Empty` - Verwendet ein leeres Layout für Kategorieseiten.
   - `1 column` - Verwendet ein einzelnes Spaltenlayout für Kategorieseiten.
   - `2 columns with left bar` - Verwendet ein zweispaltiges Layout mit der Seitenleiste links für Kategorieseiten.
   - `2 columns with right bar` - Verwendet ein zweispaltiges Layout mit der Seitenleiste auf der rechten Seite für Kategorieseiten.
   - `3 columns` - Verwendet ein dreiseitiges Layout mit Seitenleisten auf der linken und rechten Seite für Kategorieseiten.

   Wenn [Seitenaufbau](../page-builder/introduction.md) aktiviert ist, stehen zusätzliche Optionen für die volle Breite zur Verfügung. Anschließend können Sie mit den Inhaltstools des Seitenaufbaus das Layout für Ihre Kategorieseiten entwerfen.

   - `Page -- Full Width` - Verwendet das Layout _Seite - Vollbreite_ für Kategorieseiten.
   - `Category -- Full Width` - (Empfohlen) Verwendet das Layout _Kategorie - Vollständige Breite_ für Kategorieseiten.
   - `Product -- Full Width` - Verwendet das Layout _Produkt - Vollständige Breite_ für Kategorieseiten.

1. Wählen Sie die **[!UICONTROL Default Page Layout]** aus, die Sie für CMS-Seiten verwenden möchten.

   Diese Einstellung bestimmt das Layout, das standardmäßig für CMS-Seiten verwendet wird.

   - `No layout updates` - Layoutaktualisierungen sind für CMS-Seiten nicht verfügbar.
   - `Empty` - Verwendet ein leeres Layout für CMS-Seiten.
   - `1 column` - Verwendet ein einspaltiges Layout für CMS-Seiten.
   - `2 columns with left bar` - Verwendet ein zweispaltiges Layout mit der Seitenleiste auf der linken Seite für CMS-Seiten.
   - `2 columns with right bar` - Verwendet ein zweispaltiges Layout mit der Seitenleiste auf der rechten Seite für CMS-Seiten.
   - `3 columns` - Verwendet ein dreiseitiges Layout mit Seitenleisten auf der linken und rechten Seite für CMS-Seiten.

   Wenn [Seitenaufbau](../page-builder/introduction.md) aktiviert ist, stehen zusätzliche Optionen für die volle Breite zur Verfügung. Anschließend können Sie mit den Inhaltstools des Seitenaufbaus das Layout für Ihre CMS-Seiten entwerfen.

   - `Page -- Full Width` - (Empfohlen) Verwendet das Layout _Seite - Vollständige Breite_ für CMS-Seiten.
   - `Category - Full Width` - Verwendet das Layout _Kategorie - Vollbreite_ für CMS-Seiten.
   - `Product - Full Width` - Verwendet das Layout _Produkt - Vollständige Breite_ für CMS-Seiten.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Standardmäßige Seitenlayouts

### Eine Spalte

![Diagramm - einspaltiges Layout](./assets/layout-1-col-th.png){zoomable="yes"}

Mit dem Layout _[!UICONTROL 1 Column]_können Sie eine dramatische Startseite mit einem großen Bild oder Fokus erstellen. Sie eignet sich auch für Landingpages oder andere Seiten mit einer Kombination aus Text, Bildern und Videos.

### Zwei Spalten mit linker Leiste

![Diagramm - zweispaltiges Layout mit linker Leiste](./assets/layout-2-col-lft-bar-th.png){zoomable="yes"}

Das Layout _[!UICONTROL 2 Columns with Left Bar]_wird häufig für Seiten mit Navigation auf der linken Seite verwendet, z. B. für einen Katalog oder Suchergebnisseiten mit geschichteter Navigation. Es ist auch eine hervorragende Wahl für Startseiten, die zusätzliche Navigation benötigen oder Bausteine unterstützender Inhalte auf der linken Seite.

### Zwei Spalten mit rechter Leiste

![Diagramm - zweispaltiges Layout mit rechter Leiste](./assets/layout-2-col-rt-bar-th.png){zoomable="yes"}

Bei einem Layout mit dem Format _[!UICONTROL 2 Columns with Right Bar]_ist der Hauptinhaltsbereich groß genug für ein auffälliges Bild oder Banner. Dieses Layout wird häufig auch für Produktseiten mit Bausteinen mit unterstützendem Inhalt auf der rechten Seite verwendet.

### Drei Spalten

![Diagramm - Layout mit drei Spalten](./assets/layout-3-col-th.png){zoomable="yes"}

Das Layout _[!UICONTROL 3 Column]_verfügt über eine mittlere Spalte, die für den Haupttext der Seite breit genug ist, wobei auf jeder Seite Platz für zusätzliche Navigation und unterstützende Inhalte vorhanden ist.

### Empty

![Diagramm - leeres Layout](./assets/layout-blank-th.png){zoomable="yes"}

Mit dem Layout _[!UICONTROL Empty]_können benutzerdefinierte Seitenlayouts definiert werden.
