---
title: Navigation oben
description: Erfahren Sie, wie Sie das Hauptmenü eines Stores definieren, das wie ein Verzeichnis für die verschiedenen Abteilungen funktioniert.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Navigation oben

Das Hauptmenü Ihres Stores ähnelt einem Verzeichnis für die verschiedenen Abteilungen in Ihrem Geschäft. Jede Option stellt eine andere Produktkategorie dar. Die Position und Darstellung der oberen Navigation kann je nach Thema variieren, aber die Funktionsweise ist im Wesentlichen identisch.

![Obere Navigation](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

Die Kategoriestruktur Ihres Katalogs kann beeinflussen, wie gut Ihre Site von Suchmaschinen indiziert wird. Je tiefer eine Kategorie verschachtelt ist, desto unwahrscheinlicher ist eine gründliche Indizierung. Im Allgemeinen ist die Verwendung zwischen einer und drei sichtbaren Ebenen die effektivste. Die [Stammkategorie](category-root.md) zählt als erste Ebene, wird jedoch nicht im Menü angezeigt. Die maximale Anzahl der in der oberen Navigation verfügbaren Ebenen wird durch die Konfiguration bestimmt. Darüber hinaus kann die Anzahl der Menüebenen begrenzt sein, die von Ihrem Store-Design unterstützt werden. Beispielsweise unterstützt das Beispiel-Luma-Design bis zu fünf Ebenen, einschließlich der Stammebene.

## Menüebenen zählen

| Posten | Beschreibung |
|--- |--- |
| Ebene 1 | Die erste Ebene ist die Stammkategorie, die in den Beispieldaten den Namen &quot;Standardkategorie&quot;trägt. Der Stammordner ist ein Container für das Menü und sein Name erscheint nicht als Option im Menü. |
| Ebene 2 | Auf einem Desktop-Display ist die obere Navigation das Hauptmenü, das oben auf der Seite angezeigt wird. Auf einem Mobilgerät wird das Hauptmenü in der Regel als Flyout-Menü mit Optionen angezeigt. Die Optionen der zweiten Ebene im Store &quot;Luma&quot;sind _Neue Funktionen_, _Frauen_, _Männer_, _Fanggerät_, _Schulung_, und _Verkauf_. |
| Ebene 3 | Die dritte Ebene wird unter jeder Hauptmenüoption angezeigt. Beispiel: unter _Frauen_, sind die Optionen der dritten Ebene _Tops_ und _Unterleib_. |
| Ebene 4 | Die Optionen der vierten Ebene sind Unterkategorien, die von einer Option der dritten Ebene abfliegen. Beispiel: unter _Tops_, sind die Menüoptionen der vierten Ebene _Jacken_, _Hoodies &amp; Sweatshirts_, _Tees_, und _Brand &amp; Tanks_. |

{style="table-layout:auto"}

## Festlegen der oberen Navigation

Damit eine Kategorie in der oberen Navigation eines Stores angezeigt wird, führen Sie die folgenden Schritte aus:

### Schritt 1: Erstellen einer Kategorie

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Legen Sie eine **[!UICONTROL Store View]** um zu bestimmen, wo die neue Kategorie verfügbar sein soll.

1. Wählen Sie im Kategoriebaum die übergeordnete Kategorie der neuen Kategorie aus.

   Wenn Sie von Anfang an ohne Daten beginnen, enthält die Liste möglicherweise nur zwei Kategorien: _Standardkategorie_, das der Stamm ist, und ein _Beispielkategorie_.

1. Klicken **[!UICONTROL Add Subcategory]**.

1. Füllen Sie die grundlegenden Informationen mit den folgenden Einstellungen aus:

   - **[!UICONTROL Enable Category]** auf `Yes`
   - **[!UICONTROL Include in Menu]** auf `Yes`

1. Anzeigeeinstellung **[!UICONTROL Anchor]** nach `Yes`.

1. Alle anderen erforderlichen Angaben [Kategorieneinstellungen](category-create.md).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

Bei einer Multistore-Installation kann ein anderes Hauptmenü als [Stammkategorie](category-root.md) für jeden [store](../stores-purchase/stores.md#add-stores).

### Schritt 2: Festlegen der Tiefe der oberen Navigation

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern Sie die **[!UICONTROL Category Top Navigation]** Abschnitt.

   ![Obere Kategorienavigation](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   Da die Tiefe der oberen Navigation eine globale [Konfigurationsbereich](../getting-started/websites-stores-views.md#scope-settings)festgelegt ist, gilt die Einstellung für alle Websites, Stores und Store-Ansichten in der Commerce-Installation. Die _[!UICONTROL Category Top Navigation]_Konfigurationsabschnitt ist nur verfügbar, wenn_[!UICONTROL Store View]_ in der linken oberen Ecke auf `Default Config`.

   Eine detaillierte Liste dieser Optionen finden Sie unter [Obere Kategorienavigation](../configuration-reference/catalog/catalog.md#layered-navigation) im _Konfigurationsreferenz_.

1. Um die Anzahl der Unterkategorien zu begrenzen, die in der oberen Navigation angezeigt werden, geben Sie die Zahl für **[!UICONTROL Maximal Depth]**.

   Der Standardwert ist `0`, wodurch die Anzahl der Unterkategorien nicht begrenzt wird.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
